# vHsm

## 模块描述

Configuration of the vHsm module.

## 容器列表

### 1. vHsmGeneral

**描述**: Container for the configuration of the vHsm Firmware

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmSoftResetLimit
  长名称: ''
  描述: |
    Maximum number of software resets before going to halt.
    
    This may not be available on all platforms.
  默认值: 8
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmDevErrorDetect
  长名称: ''
  描述: Enable DET
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vHsmUserRevision
  长名称: ''
  描述: This parameter is freely configurable and is synced to the application configuration
      (/MICROSAR/Crypto_30_vHsm/Crypto/CryptovHsm/CryptoHsmUserRevision). Use this to have a
      compare value that the configuration of application and vHSM are in sync.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vHsmRedirection
  长名称: ''
  描述: Enable job input/output redirection to key elements. This is a Autosar 4.4 feature. Therefore
      a Crypto driver is needed which also supports this feature.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vHsmAdditionalSettings
  长名称: ''
  描述: |
    This parameter provides hardware specific settings for the vHsm Hal component,
     e.g. enables several Hal callouts in the vHsm_Core component.
    
    This parameter is set automatically by Hal implementation so Integrator shall not modify it.
  默认值: ENABLE_API_GET_CODE_FLASH_ADDRESS
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vHsmUserConfigurationFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to vHsm_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vHsmEnableRamLoopCallout
  长名称: ''
  描述: Enable a callout which is cyclically called during the RAM loop.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vHsmGenerateRandomIpcValues
  长名称: ''
  描述: |
    Generate two uint32 and a 16 byte array of random data to the IPC.
    This random data can be read from IPC at startup without using a Crypto driver.
    Use-Cases are e.g. canary for stack protection.
    
    When enabled, this may increase the startup time significantly depending on the hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vHsmGenerateRandomStackProtectionCanary
  长名称: ''
  描述: |
    Generate a uint32 value used as canary for stack protection.
    
    When enabled, this may increase the startup time significantly depending on the hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vHsmInvalidNvMBlockBehaviour
  长名称: vHsm Invalid NvM Block Behaviour
  描述: |
    If NvM blocks have never been written they will produce an error during ReadAll at startup of
    the vHsm.
    
    Make sure to persist all NvM Blocks during the first startup at least once or always  ignore the
    error about invalid blocks by setting this option to VHSM_IGNORE_INVALID_BLOCKS
    Otherwise the vHsm will trigger a software reset on the next startup.
    
    Persisting all blocks during first startup can be done by either setting this option to
    VHSM_REPERSIST_INVALID_BLOCKS or calling vHsm_NvM_Repersist() in vHsm_FirstStartup_Callout().
    
    Info: If a NvM Block is read as invalid, the contained keys will have the init values as
    configured in the LibCv driver.
  默认值: VHSM_IGNORE_INVALID_BLOCKS
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: vHsmMainFunctionPeriod
  长名称: ''
  描述: |
    Specifies the period of main function vHsm_MainFunction in seconds.
    
    If the parameter is available, the cyclic operations of the vHsm are processed in a cyclic task.
    If the parameter is not set the cyclic operations are  processed in background task
  默认值: 0.01
  最小值: 0
  最大值: 3600
```

### 2. vHsmMemoryArea

**描述**: Whitelist of the memory sections which is regarded as valid memory for input and/or output depending
on the configuration.

Attention!
Keep in mind that a wrong configuration may expose vHsm internal secure memory areas to be used
inside jobs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmMemoryAreaStart
  长名称: ''
  描述: Start address of the memory area
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmMemoryAreaStop
  长名称: ''
  描述: End address of the memory area
  默认值: 4294967295
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmMemoryAreaType
  长名称: ''
  描述: Type of the memory area
  默认值: VHSM_MEMORY_AREA_READ
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vHsmMemoryAreaId
  长名称: ''
  描述: Id of the memory area
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vHsmAllowDynamicConfig
  长名称: ''
  描述: For some memory sections the Hal can configure the boundaries during runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vHsmMemoryAreaUser
  长名称: ''
  描述: |
    Defines which core uses this memory area.
    
    HSM:
    - The Hsm will use this area for the whitelist during pointer checking
    - The Area will not be synchronized to the memory areas of the driver on the host application
    core.
    
    HOST:
    - The Hsm will ignore this area during pointer checking.
    - This area will be synchronized to the driver on host application core
    
    BOTH:
    - The Hsm will use this area for the whitelist during pointer checking
    - This area will be synchronized to the driver on host application core
  默认值: BOTH
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vHsmMemoryAreaPriority
  长名称: ''
  描述: |
    The priority of the memory area.
    The higher the value, the higher the areas priority.
    The area with the highest priority will be checked first.
    To get the best performance assign a high priority to areas which are used very often.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 3. vHsmDevelopment

**描述**: This container must only be used during development

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmOptionByteModification
  长名称: ''
  描述: |
    This option enables the application cores to edit the option bytes.
    
    If enabled, this renders the HSM unsecure, because the HSM can be disabled completely!
    This is not available on all hardware platforms.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vHsmTraceInfo
  长名称: ''
  描述: Print out debug information on the console in the multi debugger.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vHsmTraceWarning
  长名称: ''
  描述: Print out debug information on the console in the multi debugger.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vHsmTraceDebug
  长名称: ''
  描述: Print out debug information on the console in the multi debugger.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vHsmTraceError
  长名称: ''
  描述: Print out debug information on the console in the multi debugger.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vHsmTraceKeyStorage
  长名称: ''
  描述: Print the state and changes of the KeyStorage
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vHsmUpgradeProtectionModification
  长名称: ''
  描述: |
    This option enables the application cores to edit the upgrade protection.
    
    If enabled, this renders the HSM unsecure, because the HSM can be disabled completely!
    This is not available on all hardware platforms.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vHsmEnableSecureBootAutostart
  长名称: ''
  描述: Enable the autostart of secure boot
  默认值: true
  最小值: ''
  最大值: ''
```

### 4. vHsmChannelMapping

**描述**: This container is for defining the which CryIf channels are used for the different use cases

该容器没有参数。

### 5. vHsmKeyMapping

**描述**: This container is for defining which Crypto keys are used for the different use cases.
Also the key properties can be defined here (e.g. Write Once, Secure Boot protected)

该容器没有参数。

### 6. vHsmRandomInit

**描述**: A key and its element can be initialized with random value and set to valid at the first startup

该容器没有参数。

### 7. vHsmKeyRouting

**描述**: A key routing gives the vHSM the possibility to call key operations of another driver for the given
key. Due to this, Custom driver or Hardware driver can participate on the key functions, can extend
or prohibit the execution or simply bypass them.

该容器没有参数。

### 8. vHsmIpc

**描述**: Used to configure the IPC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmIpcChannels
  长名称: ''
  描述: |
    Each IPC Instance consists of one or more channels. Each channel can hold a job request.
    The vHsm will poll the channels inside an IPC one after another and will process the containing
    jobs.
  默认值: 4
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: vHsmIpcProtocolVersion
  长名称: ''
  描述: |
    Protocol version used to communicate with the vHsm Driver over IPC.
    
    Protocol Version 1 is deprecated!
  默认值: 2
  最小值: 1
  最大值: 2
```

### 9. vHsmIpcInstance

**描述**: This container represents an IPC instance and therefore the number of distinct memory areas of which
each contain an IPC which will be polled for incoming jobs.

If there are more than one Instance of a corresponding vHSM Crypto Driver on application side (e,g,
one per core) , create one instance for each.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmDriverPreconfigDestination
  长名称: ''
  描述: |
    The vHSM is always generation a Pre-Config file for the Crypto_30_vHsm which can be used to sync
    the configuration between the vHsm and the driver which is located inside another SIP.
    With this parameter, the target folder and filename of the generated Pre-Config file can be
    influenced.
    If parameter is no present or empty, the pre config is generated in the following directory:
    $(GenDataFolder)/vHsmPreconfig_$(InstanceName)/Crypto_30_vHsm_bswmd_Pre.arxml
    
    The Pre-Config file will contain:
    - The available primitives inside the vHsm_LibCv driver object
    - The available and configured keys of the LibCv driver including its types and elements.
    - Some vHSM data like Protocol and Sync parameter
    
    Specify the path to the file e.g.:
    - C:\Vector\vHsm\Crypto_30_vHsm_bswmd_Pre.arxml
    - $(DpaProjectFolder)\Config\vHsmPreConfig\Crypto_30_vHsm_bswmd_Pre.arxml
    
    Beside the DaVinci Configurator variables, $(InstanceName) can be used as placeholder to use the
    shortname of this IPC instance in the path.
    
    Attention: Target folder should exist, only the last folder can be created during generation!
    
    In the application configuration of the other SIP containing the crypto driver, add the folder
    with the generated Pre-Config to the Additional Definitions using the Project Settings Dialog.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vHsmIpcHardwareUnit
  长名称: ''
  描述: |
    Id of the Hw IPC which is used to determine the init state of the IPC or to provide the ready
    state of the HSM
    
    Most platforms only have one hardware unit. Therefore the parameter is mostly set to 0.
    Depending on the used platform, a hardware unit can either be a dedicated IPC hardware/channel
    or just a register.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: vHsmResponseInterruptFlagSetMask
  长名称: ''
  描述: The mask which will be written to the register which triggers an interrupt the the Host core
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vHsmIpcAddress
  长名称: ''
  描述: |
    Linker-Symbol or Address of the IPC memory.
    
    If this parameter is not available, the vHsm Firmware generates a buffer (shared IPC memory)
    which needs to be linked to the correct address in the memory.
    
    If the parameter is created, the address is used and no buffer is created.
    The memory area needs to be reserved e.g. by the linker scrip
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vHsmIpcInstanceId
  长名称: ''
  描述: Id of the Ipc instance
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: vHsmResponseInterruptFlagSetAddress
  长名称: ''
  描述: Address of the register which is used to trigger the interrupt to the host core
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 10. vHsmFirmwareUpdate

**描述**: Used to configure the vHsm Firmware Update

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmUpdaterAddress
  长名称: ''
  描述: |
    Label of the Address of the vhsm Firmware Updater.
    
    This label will be used as jump address after Crypto_30_vHsm_KeyElementSet has been called for
    the key element CRYPTO_KE_CUSTOM_VHSM_FIRMWARE_UPDATE_START_UPDATER after a firmware update job
    has been executed successfully.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vHsmJumpToUpdaterRestriction
  长名称: ''
  描述: |
    Allow the jump to updater only when the firmware update job was successful.
    If this option is disabled, a preceding firmware update job is not necessary to be able to let
    the vHsm Firmware jump to the updater.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. vHsmSecureBoot

**描述**: Configure secure boot related parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmSecureBootSplitSize
  长名称: ''
  描述: During secure boot it is possible to do job processing in the meantime. To get a low latency
      in job processing, the secure boot segment check can be divided into multiple
      computation chunks. The number of bytes which will be checked in each chunk can be
      configured with this parameter.
  默认值: 256
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmSecureBootQueueSize
  长名称: ''
  描述: Number of parallel secure boot segments which can be processed.
  默认值: 10
  最小值: 2
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmSecureBootCyclicVerificationSplitSize
  长名称: ''
  描述: During secure boot it is possible to do job processing in the meantime. To get a low latency
      in job processing, the cyclic verification of secure boot segment can be divided into
      multiple computation chunks. The number of bytes which will be checked in each chunk can
      be configured with this parameter.
  默认值: 256
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vHsmSecureBootSegmentSuccessCallout
  长名称: ''
  描述: Enable triggering the call of vHsm_SecureBoot_SegmentSuccess_Callout(groupId) if the
      verification of a segment was successful.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vHsmSecureBootForcedSequentialProcessingOnFirstVerification
  长名称: ''
  描述: |
    Force parallel segments to be processed sequential/immediately on their first verification. This
    leads to the CMAC being written to the data flash and will be always available for comparison on
    subsequent startups.
    
    Info:
    On the first verification of a secure boot slot, there will be write access to the data flash
    because of storing the CMAC.
    This can lead to issues when performing parallel secure boot verification on platforms which are
    not able to process concurrent data flash access from HSM and Application core at the same time.
    
    Enabling the option is only needed when:
    - Platform does not allow concurrent data flash access
    - Parallel segments have not been provisioned with the secure boot update
    
    Attention:
    - Enabling this option may lead to increased startup time during the first startup when there
    are autostart groups containing parallel segments.
    - Ensure that when the segment verification is triggered from the application core, the HSM is
    allowed to write to the data flash.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vHsmSecureBootStorageMethod
  长名称: ''
  描述: |
    Select the storage type of the secure boot information.
    
    VHSM_STORAGE_IN_NVM:
    The NvM is directly used for the key storage. This reduces memory overhead (RAM, Data and Code
    flash).
    
    VHSM_STORAGE_IN_CSM (deprecated):
    Keys and key elements are used to store the secure boot information.
    Persisting is done by the LibCv driver with the help of the NvM in the background.
  默认值: VHSM_STORAGE_IN_NVM
  最小值: ''
  最大值: ''
```

### 12. vHsmSecureBootGroup

**描述**: Container describing a secure boot group which can be used to group and process multiple segments at
once.

Also the autostart behavior and its conditions can be configured for each secure boot group.

All segments in a group can be reconfigured with a secure boot update.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmSecureBootGroupId
  长名称: ''
  描述: Unique Id can be chosen freely to identify a Secure Boot Group used in the Segmentation List.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmAutostart
  长名称: ''
  描述: |
    TRUE:
    The verification will be started during startup of the vHsm.
    This can be restricted by a runtime condition like a custom callout. See
    /MICROSAR/vHsm/vHsmSecureBoot/vHsmSecureBootGroup/vHsmAutostartCondition
    
    FALSE:
    The verification of the slot is started by e.g the bootloader.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vHsmCyclicVerification
  长名称: ''
  描述: |
    If enabled, this option will restart the verification of the group and the contained parallel
    and sequential segments.
    This way, the segments will be verified continuously.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vHsmNvBlockRevision
  长名称: ''
  描述: |
    Revision of the NvBlock.
    
    If this parameter is changed, the CRC will change and the NvBlock will be invalid which will
    result in the secure boot beeing set to initial values.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vHsmNvBlockCrcLayoutChecksum
  长名称: ''
  描述: |
    CRC checksum over the NvBlock layout.
    If the CRC does not match the data flash content, the secure boot information for this group
    will b set to the initial values.
    
    CRC Calculation is influenced by:
    - Number of segments
    - Tag length of the reerenced verification method
    - Tag handling
    - NvBlock revision
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: vHsmTagHandling
  长名称: ''
  描述: |
    A tag is needed in order to detect memory manipulations in flash.
    The different methods of tag handling are described below with specific advantages (+) and
    disadvantages (-).
    
    VHSM_GROUP_TAG
    - Sanctions and processing must be same for all segments in the group
    - SegmentList during secure boot update can either contain sequential or parallel segments.
    (Processing mode NONE is additionally possible in both cases)
    - Single segments can not be selected for processing individually during secure boot
    
    VHSM_PROCESSING_TAG:
    + Each group needs to store 2 tags
    + SegmentList during secure boot update can contain both sequential and parallel segements
    + Different algorithms for sequential and parallel jobs are possible
    - Sanction must be the same for all segments in the group -> only one sanction is triggered if
    one of the segments fail
    - Single segments can not be selected for processing individually processing
    
    VHSM_SEGMENT_TAG:
    + SegmentList during secure boot update can contain both sequential and parallel segements
    + Sanctions can be configured for each segment individually
    + Starting the secure boot processing of a single segment is possible
    - Each segment needs to store a tag.
    - Sequential and Parallel Csm jobs need to use the same algorithm
  默认值: VHSM_GROUP_TAG
  最小值: ''
  最大值: ''
```

### 13. vHsmCustomCallout

**描述**: boolean vHsm_Custom_IsSecureBootAllowAutostart_Callout(vHsm_SecureBootGroupIterType
secureBootGroupIndex) is called.
If the function returns TRUE, the autostart will be performed. This can be used for e.g. checking
the current reset vector.

该容器没有参数。

### 14. vHsmSecureBootSegment

**描述**: A secure boot segment is a memory area which can be secured with a CMAC during secure boot.
A segment is part of a group and can be updated with secure software download or as part of a secure
boot update.

该容器没有参数。

### 15. vHsmSecureBootSegmentInitValues

**描述**: Init values for the segment. The values can be changed during runtime with secure boot update and
secure software download.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmAddress
  长名称: ''
  描述: |
    This is the init value which will be stored during the startup.
    
    Attention:
    It will overwrite the init value configured for the key element!
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmLength
  长名称: ''
  描述: |
    This is the init value which will be stored during the startup.
    
    Attention:
    It will overwrite the init value configured for the key element!
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmSanction
  长名称: ''
  描述: The sanction which shall be performed
  默认值: SANCTION_RESET
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vHsmSecureBootMode
  长名称: ''
  描述: Processing Type of the segment.
  默认值: SEQUENTIAL
  最小值: ''
  最大值: ''
```

### 16. vHsmCustomCalloutCyclic

**描述**: boolean vHsm_Custom_IsSecureBootAllowCyclic_Callout(vHsm_SecureBootGroupIterType
secureBootGroupIndex, uint32 secureBootGroup) is called.
If the function returns TRUE, the cyclic verification will be performed. This can be used for
disabling the cyclic verification during FBL and only enable it during APPL runtime.

该容器没有参数。

### 17. vHsmCompareInternalTag

**描述**: Compare a computed Tag (e.g. Cmac or Hash) against a Tag stored in the NvM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmTagLength
  长名称: ''
  描述: |
    Length of the Tag (e.g. CMAC or HASH)
    
    Autofilled with information from CsmJobs
  默认值: 16
  最小值: 0
  最大值: 4294967295
```

### 18. vHsmSecureBootUpdate

**描述**: This container configures the CSM jobs used for hash and signature generation. Secureboot update
uses a signed segment list to update the secure boot segments of a group.

该容器没有参数。

### 19. vHsmSecureSoftwareDownload

**描述**: This container configured the key, channel und primitive used during secure software download which
uses signed data to update a single secure boot segment.

Deprecated

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmAllowAddressChange
  长名称: ''
  描述: |
    Allow the change of the address during secure software download.
    If disabled, this implies that a correct init value for the address is already set in each
    secure boot segment.
  默认值: false
  最小值: ''
  最大值: ''
```

### 20. vHsmSecureBootVerificationJob

**描述**: Contains the jobs which will be used for verification.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmSecureBootVerificationJobId
  长名称: ''
  描述: Id of the verification job
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 21. vHsmLog

**描述**: Container for the events

该容器没有参数。

### 22. vHsmLogEvent

**描述**: Container for the event log

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmCounterSize
  长名称: ''
  描述: |
    Size of the counter which is incremented on each occurrence of the event.
    Valid values are 1, 2 or 4 bytes.
  默认值: 4
  最小值: 1
  最大值: 4
- 
  序号: 2
  名称: vHsmTimestampSize
  长名称: ''
  描述: The content of the timestamp will be filled with the vHsm_Log_GetTimestamp_Callout(LogEventId)
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmLogEventId
  长名称: ''
  描述: Id of the event
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vHsmDataSize
  长名称: ''
  描述: Size of the event data
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vHsmMaxEntries
  长名称: ''
  描述: Maximum number of entries before old entries are overwritten
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: vHsmNvProcessing
  长名称: ''
  描述: This option defines how the log for this event will be persisted.
  默认值: NV_PROCESSING_IMMEDIATE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vHsmFillLevelThreshold
  长名称: ''
  描述: |
    If the fill level is reached the function vHsm_Log_FillLevelReachedCallout(vHsmLogEventId) is
    called.
    
    If the fill level is set to 100 and the callout appears, all subsequent events will overwrite
    older entries from now on.
  默认值: 1
  最小值: 1
  最大值: 100
- 
  序号: 8
  名称: vHsmExportStrategy
  长名称: ''
  描述: Configure the way the log will be exported.
  默认值: EXPORT_ALL_FILO
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vHsmDiscardWhenFull
  长名称: ''
  描述: |
    Discard new elements when the log is full.
    Otherwise the last element will be overwritten.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vHsmEventCallout
  长名称: ''
  描述: The function vHsm_Log_EventCallout(logEventId) is called when the event occurs
  默认值: false
  最小值: ''
  最大值: ''
```

### 23. vHsmScheduling

**描述**: Container to configure scheduling and parallel processing with the help of the OS or interrupts
triggered to vHSM

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmOsSupport
  长名称: ''
  描述: |
    Enable this option when OS is available and shall be used.
    This way, different driver objects can be processed in different tasks with various priorities.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vHsmInterruptMode
  长名称: ''
  描述: |
    Fetch the jobs only inside the ISR. If disabled, fetching will be performed in MainLoop.
    
    This option needs to be disabled when a driver on application core is used (< R24) which does
    not trigger interrupts at each job request.
    Do not use interrupt processed jobs if this option is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vHsmIsrForProcessing
  长名称: ''
  描述: |
    Select the category of the ISR in which the channels to be processed directly in ISR will be
    executed.
    
    CATEGORY_1:
    - Fastest processing time
    - No additional context switches
    - Stack must be reserved manually
    
    CATEGORY_2:
    - Additional context switch necessary to switch from ISR1 to ISR2
    - OS can be used to configure the stack size
  默认值: CATEGORY_1
  最小值: ''
  最大值: ''
```

### 24. vHsmSchedulableEntities

**描述**: Each schedulable entity will create a runnable which can be mapped to a task. All referenced
channels will be then processed in this task, when a corresponding job is received from the IPC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmSchedulableEntityId
  长名称: ''
  描述: Id of the task mapping
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 25. vHsmPublishedInformation

**描述**: vHsmPublishedInformation is used for additional published parameters and information.
This container is pre-configured and shall not be configured manually.

该容器没有参数。

### 26. vHsmDerivativeInformation

**描述**: Contains all derivative specific information needed by the vHsm generator.

该容器没有参数。

### 27. vHsmIpcHardwareUnit

**描述**: A hardware ipc can be used by an IPC instance to share information about e.g IPC initialized state
and HSM ready.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmIpcHardwareUnitId
  长名称: ''
  描述: Id of the hardware unit
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 28. Hsm

**描述**: Contains the register addresses needed by the HSM

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmHost2HsmAddress
  长名称: Host2Hsm Address
  描述: Address of the register which is used to communicate from Host to the HSM core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmHsm2HostAddress
  长名称: Hsm2Host Address
  描述: Address of the register which is used to communicate from HSM to the Host core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmResponseInterruptFlagSetAddress
  长名称: ''
  描述: The address to use by vHsm for triggering an interrupt to the Host
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 29. Host

**描述**: Contains the register addresses needed by the Host

#### 参数列表

```yaml
- 
  序号: 1
  名称: vHsmHost2HsmAddress
  长名称: Host2Hsm Address
  描述: Address of the register which is used to communicate from Host to the HSM core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vHsmHsm2HostAddress
  长名称: Hsm2Host Address
  描述: Address of the register which is used to communicate from HSM to the Host core
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vHsmRequestInterruptFlagSetAddress
  长名称: ''
  描述: The address used by Crypto Driver of the Host to trigger an interrupt to the vHsm
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vHsmResponseInterruptFlagClearAddress
  长名称: ''
  描述: The address used in the Crypto Driver of the Host to clear the ISR flag of a response ISR from
      Hsm.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vHsmResponseInterruptFlagClearValue
  长名称: ''
  描述: Value which needs to be written by the Crypto Driver of the Host to the given address to clear
      the response flag.
  默认值: 1
  最小值: 0
  最大值: 1
```

