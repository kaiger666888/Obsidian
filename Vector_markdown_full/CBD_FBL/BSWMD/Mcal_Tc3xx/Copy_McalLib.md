# McalLib - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:14

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [McalLib](#mcallib)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. McalLib

#### 基本信息

- **UUID**: `13aa2440-e790-4121-9e12-3a380efb0d6b`
- **模块名称**: `McalLib`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Published information of Mcal Library.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2017-05-10
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. McalLibPublishedInformation

**容器属性**:

- **UUID**: `dcc39b88-cc2b-4358-ba88-30120722c6ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McalLibPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

This is the general container that contains the pre-build configuration parameters

###### 参数配置

此容器包含 **26** 个参数：

####### INTEGER 类型参数

######## 1. McalLibMcalAvailableCores

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b258bcca`
- **参数名**: `McalLibMcalAvailableCores`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `6`
- **取值范围**: [6..6]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the number of cores available on the current variant of Aurix2G HW.

######## 2. McalLibDsprCore0StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b358bcca`
- **参数名**: `McalLibDsprCore0StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1879048192`
- **取值范围**: [1879048192..1879048192]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 0 of the current variant of Aurix2G HW.

######## 3. McalLibDsprCore0EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b458bcca`
- **参数名**: `McalLibDsprCore0EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1879293951`
- **取值范围**: [1879293951..1879293951]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 0 of the current variant of Aurix2G HW.

######## 4. McalLibDsprCore1StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b558bcca`
- **参数名**: `McalLibDsprCore1StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1610612736`
- **取值范围**: [1610612736..1610612736]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 1 of the current variant of Aurix2G HW.

######## 5. McalLibDsprCore1EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b658bcca`
- **参数名**: `McalLibDsprCore1EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1610858495`
- **取值范围**: [1610858495..1610858495]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 1 of the current variant of Aurix2G HW.

######## 6. McalLibDsprCore2StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b758bcca`
- **参数名**: `McalLibDsprCore2StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1342177280`
- **取值范围**: [1342177280..1342177280]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 2 of the current variant of Aurix2G HW.

######## 7. McalLibDsprCore2EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b858bcca`
- **参数名**: `McalLibDsprCore2EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1342275583`
- **取值范围**: [1342275583..1342275583]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 2 of the current variant of Aurix2G HW.

######## 8. McalLibDsprCore3StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b958bcca`
- **参数名**: `McalLibDsprCore3StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1073741824`
- **取值范围**: [1073741824..1073741824]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 3 of the current variant of Aurix2G HW.

######## 9. McalLibDsprCore3EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b268bcca`
- **参数名**: `McalLibDsprCore3EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1073840127`
- **取值范围**: [1073840127..1073840127]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 3 of the current variant of Aurix2G HW.

######## 10. McalLibDsprCore4StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b278bcca`
- **参数名**: `McalLibDsprCore4StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `805306368`
- **取值范围**: [805306368..805306368]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 4 of the current variant of Aurix2G HW.

######## 11. McalLibDsprCore4EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b288bcca`
- **参数名**: `McalLibDsprCore4EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `805404671`
- **取值范围**: [805404671..805404671]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 4 of the current variant of Aurix2G HW.

######## 12. McalLibDsprCore5StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b298bcca`
- **参数名**: `McalLibDsprCore5StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `268435456`
- **取值范围**: [268435456..268435456]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR start address for Core 5 of the current variant of Aurix2G HW.

######## 13. McalLibDsprCore5EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b259bcca`
- **参数名**: `McalLibDsprCore5EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `268533759`
- **取值范围**: [268533759..268533759]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the DSPR end address for Core 5 of the current variant of Aurix2G HW.

######## 14. McalLibPsprCore0StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1167b258bcca`
- **参数名**: `McalLibPsprCore0StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1880096768`
- **取值范围**: [1880096768..1880096768]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 0 of the current variant of Aurix2G HW.

######## 15. McalLibPsprCore0EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1168b258bcca`
- **参数名**: `McalLibPsprCore0EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1880162303`
- **取值范围**: [1880162303..1880162303]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 0 of the current variant of Aurix2G HW.

######## 16. McalLibPsprCore1StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1169b258bcca`
- **参数名**: `McalLibPsprCore1StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1611661312`
- **取值范围**: [1611661312..1611661312]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 1 of the current variant of Aurix2G HW.

######## 17. McalLibPsprCore1EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1176b258bcca`
- **参数名**: `McalLibPsprCore1EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1611726847`
- **取值范围**: [1611726847..1611726847]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 1 of the current variant of Aurix2G HW.

######## 18. McalLibPsprCore2StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1186b258bcca`
- **参数名**: `McalLibPsprCore2StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1343225856`
- **取值范围**: [1343225856..1343225856]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 2 of the current variant of Aurix2G HW.

######## 19. McalLibPsprCore2EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1196b258bcca`
- **参数名**: `McalLibPsprCore2EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1343291391`
- **取值范围**: [1343291391..1343291391]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 2 of the current variant of Aurix2G HW.

######## 20. McalLibPsprCore3StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1266b258bcca`
- **参数名**: `McalLibPsprCore3StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1074790400`
- **取值范围**: [1074790400..1074790400]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 3 of the current variant of Aurix2G HW.

######## 21. McalLibPsprCore3EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1366b258bcca`
- **参数名**: `McalLibPsprCore3EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1074855935`
- **取值范围**: [1074855935..1074855935]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 3 of the current variant of Aurix2G HW.

######## 22. McalLibPsprCore4StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1466b258bcca`
- **参数名**: `McalLibPsprCore4StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `806354944`
- **取值范围**: [806354944..806354944]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 4 of the current variant of Aurix2G HW.

######## 23. McalLibPsprCore4EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1566b258bcca`
- **参数名**: `McalLibPsprCore4EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `806420479`
- **取值范围**: [806420479..806420479]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 4 of the current variant of Aurix2G HW.

######## 24. McalLibPsprCore5StartAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1666b258bcca`
- **参数名**: `McalLibPsprCore5StartAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `269484032`
- **取值范围**: [269484032..269484032]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR start address for Core 5 of the current variant of Aurix2G HW.

######## 25. McalLibPsprCore5EndAddr

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1766b258bcca`
- **参数名**: `McalLibPsprCore5EndAddr`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `269549567`
- **取值范围**: [269549567..269549567]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the PSPR end address for Core 5 of the current variant of Aurix2G HW.

######## 26. McalLibBackUpClockFreq

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1866b258bcca`
- **参数名**: `McalLibBackUpClockFreq`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `100`
- **取值范围**: [100..100]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Mentions the backup clock frequency of the current variant of Aurix2G HW.

##### 2. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35cc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

This container contains the published information of the Mcal Library.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-3333-1166b358b887`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-3333-ea2704aaecc6`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-3333-e100aad4cc54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Revision version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-3333-8fab87d8cc27`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-3333-2a7e5a54ccf9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-3333-a81dae0cc4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-3333-f33b08cce638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-3333-5f0c41cc01d1`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix2G derivative used for the implementation

##### 3. McalLibGeneral

**容器属性**:

- **UUID**: `ECUC:9d811d70-8cc9-4c5c-bb07-fc5de786d2ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McalLibGeneral`
- **多重性**: [0..1]

**容器描述**:

Module wide configuration parameters of the McalLib driver.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. McalLibSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `McalLibSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **McalLib**
