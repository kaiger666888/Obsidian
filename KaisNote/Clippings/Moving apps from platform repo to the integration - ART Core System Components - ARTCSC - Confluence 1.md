---
title: "Moving apps from platform repo to the integration - ART Core System Components - ARTCSC - Confluence"
source: "https://confluence.volvocars.biz/pages/viewpage.action?spaceKey=ARTCSC&title=Moving+apps+from+platform+repo+to+the+integration"
author:
  - "[[Safi]]"
  - "[[Mostafa]]"
published:
created: 2025-07-28
description:
tags:
  - "clippings"
---
[Confluence Community Site](https://intranet.volvocars.net/sites/VIRA/SitePages/Confluence.aspx) **|** [Confluence Training Portal](https://intranet.volvocars.net/sites/VIRA/SitePages/Confluence-Training-Portal.aspx) **|** [Contact Confluence Team](https://volvocars.service-now.com/sp?id=sc_cat_item&sys_id=89e18f68dbbb2f00536509c2ba961961) **|** [Self Service Portal](https://jira-vira.volvocars.biz/messenger/)

## Removing an app from the platform

1. Remove the dependency to the app from the recipe in the conandata.yml file
2. Generate the ecu\_extract using the gen\_proj.bat
3. Clean the EcucValueCollection (ECUFlatView): remove "assembly connections" and "DataTypeMappingSets" related to the app
4. Correct the naming convention of the Dem Events related to the app: remove "Event\_" from the beginning of the name
5. Run RTE Base Config
6. Clean the Rte config from the removed references: it could be events, event\_to\_task\_mappings, or instances
7. Clean MemMap: remove all the missing references related to the app
8. Clean linker: remove all the pragmas related to the app all (it almost always contains part of the name of the swcs you remove)
9. Clean platform/inc folder: remove the header files related to the app swcs, specially the {swcs}\_MemMap.h files
10. Clean conan build
11. Create the platform conan package to be used in the integration repo later and set the option when you do "conan create. --profile=windows\_ctc\_debug -o locked\_deps=True"

**General recommendation: amend your commit with the changes of each step**

## Additional steps needed for removing SWC having NV needs

1. Generate ECU extract without removing the application
2. Create new NVData Interface for similar to the one from SWC
	- For this go to generated SystemExtract\_flattened\_patched.arxml search for
		<NV-DATA-INTERFACE>
		<SHORT-NAME>ur\_SWcNVDataInterface</SHORT-NAME>, copy the entire NVData Interface tag
	- Paste it as element under tag <SHORT-NAME>PortInterface</SHORT-NAME> in NvBlockSwc.arxml
3. Create new Datatype similar to the one used in NVDATA Interface of the SWC
	- For this go to generated SystemExtract\_flattened\_patched.arxml search for

<APPLICATION-RECORD-DATA-TYPE> and <APPLICATION-ARRAY-DATA-TYPE>

<SHORT-NAME>urSWCdatatype</SHORT-NAME>, copy the entire Datatype tag related to the NVDATA Interface

1. - Paste it as element under tag <SHORT-NAME>DataType</SHORT-NAME> in NvBlockSwc.arxml

4\. Create new Implementation Datatype similar to the one used in NVDATA Interface of the SWC

1. - For this go to generated SystemExtract\_flattened\_patched.arxml search for

<IMPLEMENTATION-DATA-TYPE>

<SHORT-NAME>urSWCdatatype</SHORT-NAME>

1. - Paste it as element under tag <SHORT-NAME>DataTypeImplementation</SHORT-NAME> in NvBlockSwc.arxml

5\. Map the new Datatype and DataTypeImplementation to the NvBlockSwc\_DataTypeMappingSet

1. - For this go to generated SystemExtract\_flattened\_patched.arxml search for

<DATA-TYPE-MAP>

<APPLICATION-DATA-TYPE-REF DEST="APPLICATION-RECORD-DATA-TYPE">/DataType/urSWCdatatype</APPLICATION-DATA-TYPE-REF> and copy and add it to NvBlockSwc\_DataTypeMappingSet in NvBlockSwc.arxml

6\. Search for <NV-BLOCK-DESCRIPTOR> and find the respective NV Block for your SWC, in it replace DataTypeImplementation/DataTypeMappings/SWCDatatype with

/DataTypeMappings/NvBlockSwc\_DataTypeMappingSet

7\. In NvBlockSwc.arxml, in the Dataype mapping remove the SWC Datatypemapping set if present

## Adding an app in the integration

1. Update the recipe in the conandata.yml file according to the platform recipe (remaining apps in the platform) and append the app you wanna integrate newly and update the corresponding conan package you created from the platform in the recipe as well
2. Ensure you use the correct and compatible version of cbs (usually integ cbs version > platform cbs version) in conanfile.py
3. Append the set recompile\_apps in conanfile.py with name of the app
4. Do conan install and conan build until you got the Rte\_mapping\_output.csv in the build folder (you could run the generate\_ecuextract and rte\_csv\_generation), you can stop the build then.
5. Take out the rows related to the app you are adding from Rte\_mapping\_output.csv and append it to the csv file in the root folder of the repo
6. Make sure you set the correct task and partition for the added runnables in the csv file
7. Do conan build

## Test platform and integration SW in CI

Loop for each app:

- Remove app in platform and increase minium version in conandata.yml so that minor version is higher than the minor part of the recorded locked version of the platform in integration  
	Example:  
	- If tioc\_integration/conandata.yml looks like this:  
		`  tioc_platform:`  
		`    locked: "tioc_platform/6.**2**.0-pre.15+0875c5c@vcc-platform/stable"`  
		`    unlocked: "locked"`
	- tioc\_platform/conandata.yml needs to have this:  
		`version:`  
		`  minimum: "6.**3**.0"`
- Add app in Integration and temporarily set unlocked version to platform: major  
	Example:
	- tioc\_integration/conandata.yml looks like this:  
		`  tioc_platform:`  
		`    locked: "tioc_platform/6.2.0-pre.15+0875c5c@vcc-platform/stable"`  
		`    unlocked: "**major**"`
- Push both to gerrit with the same topic  
	Setting topic on command line: `git push origin HEAD:refs/for/master -o topic=remove_<app>`  
	Setting topic in Gerrit GUI:  
	![](https://confluence.volvocars.biz/download/thumbnails/845759546/image-2025-6-5_14-17-31.png?version=1&modificationDate=1749125851577&api=v2)
- Wait for build. Expected overall outcome is Failed with the following status:
	- \*\_platform build successful
	- \*\_platform\_ld build successful
	- \*\_integration build not skipped and successful
	- \*\_integration\_ld build **failed  
		**
- Purpose of previous step is to verify, before submit, that the changed platform and the changed integration builds together:
	- The \*\_platform and \*\_platform\_ld jobs show that your platform change builds as-is
	- The \*\_integration build shows that the artifact created by platform\_ld together with your integration change builds - so this is the main result we are after here.
	- The \*\_integration\_ld build fails as that will try to build with the unchanged version recorded as platform/locked in conandata.yml. Since that still has the app you have removed in the platform change, it is expected to fail.
- Remove topic from platform:  
	![](https://confluence.volvocars.biz/download/thumbnails/845759546/image-2025-6-5_14-19-22.png?version=1&modificationDate=1749125963067&api=v2)
- Recheck platform  
	![](https://confluence.volvocars.biz/download/attachments/845759546/image-2025-6-5_14-20-18.png?version=1&modificationDate=1749126018720&api=v2)
- Wait for build (should be rather fast, as platform from previous build should be fetched instead of built). Expected overall outcome is success with the following status:
	- \*\_platform build successful
	- \*\_platform\_ld build successful
	- \*\_integration build **skipped**
	- \*\_integration\_ld build **not listed**
- Have someone else review platform with +2, Gate should start
- Wait for build. Expected overall outcome is success with the following status:
	- \*\_platform build successful
	- \*\_platform\_ld build successful
	- \*\_integration build **skipped**
	- \*\_integration\_ld build **not listed**
- Update integration change:
	- Remove topic
	- change back to platform unlocked: locked
	- Update platform locked version with the -pre version as submitted in previous step  
		Example:  
		tioc\_integration/conandata.yml looks like this:  
		`tioc_platform:`  
		`    locked: "tioc_platform/6.2.0-pre.16+a123b45@vcc-platform/stable"`  
		`    unlocked: "locked"`
- Wait for build. Expected overall outcome is success with the following status:
	- \*\_integration build successful
	- \*\_integration\_ld build successful
- The POD test is triggered after check. You should have all passed except a test related to complete diag on partnumber. Please see [BuildAvoidanceVictoriaCaveats.pptx](https://mysite.volvocars.net/:p:/r/personal/dblixt2_volvocars_com/Documents/Microsoft%20Teams%20chattfiler/BuildAvoidanceVictoriaCaveats.pptx?d=w53ac44d9488c4649a1da995a880c5a61&csf=1&web=1&e=aC9UyX) if you have problem finding test reports in Victoria.
- Have someone else review integration with +2, Gate should start
- When integration is finished, successful and submitted by Zuul, restart loop for the next app.
- Meanwhile, trigger the nightly tests for each app you add to the SW in the integration