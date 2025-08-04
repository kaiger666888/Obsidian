# Crc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:04

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crc](#crc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crc

#### 基本信息

- **UUID**: `ECUC:8fc09477-4d31-48bf-9fcc-0f2e51345aad`
- **模块名称**: `Crc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Crc (Crc routines) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. CrcGeneral

**容器属性**:

- **UUID**: `ECUC:022760ec-ae2e-4125-96ad-ca206d355f95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CrcGeneral`
- **多重性**: [0..1]

**容器描述**:

General configuration of CRC module

###### 参数配置

此容器包含 **21** 个参数：

####### INTEGER 类型参数

######## 1. Crc8ReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b36d`
- **参数名**: `Crc8ReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 2. Crc8H2FReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b36e`
- **参数名**: `Crc8H2FReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 3. Crc16ReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b36f`
- **参数名**: `Crc16ReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 4. Crc16ARCReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b37f`
- **参数名**: `Crc16ARCReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 5. Crc32ReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b370`
- **参数名**: `Crc32ReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 6. Crc32P4ReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b371`
- **参数名**: `Crc32P4ReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

######## 7. Crc64ReturnErrorValue

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b37d`
- **参数名**: `Crc64ReturnErrorValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Error value that will be returned in case of an invalid input parameter.

####### BOOLEAN 类型参数

######## 1. CrcVersionInfoApi

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b36b`
- **参数名**: `CrcVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

######## 2. CrcSafetyEnable

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b36c`
- **参数名**: `CrcSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Pre-processor switch to enable / disable the Safety checks for all APIs

######## 3. CrcDma8bitApi

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b37a`
- **参数名**: `CrcDma8bitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable/disable 8-bit SAE J1850 polynomial for CRC calculation while using the DMA based API.

######## 4. CrcDma16bitApi

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b37b`
- **参数名**: `CrcDma16bitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable/disable 16-bit CCITT-FALSE CRC16 polynomial for CRC calculation while using the DMA based API.

######## 5. CrcDma32bitApi

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b37c`
- **参数名**: `CrcDma32bitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable/disable 32-bit IEEE-802.3 polynomial for CRC calculation while using the DMA based API.

######## 6. CrcDma32P4bitApi

- **UUID**: `ECUC:5b2dc178-9f79-43a7-a2d5-f492d356b52d`
- **参数名**: `CrcDma32P4bitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable/disable 32-bit (0xF4ACFB13) polynomail for CRC calculation while using the DMA based API.

####### ENUMERATION 类型参数

######## 1. Crc16ARCMode

- **UUID**: `ECUC:f5200da9-3201-4437-9fab-df223f93111e`
- **参数名**: `Crc16ARCMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_16_ARC_HARDWARE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CRC_16_ARC_HARDWARE` (来源: INFINEON_AURIX2G)
  - `CRC_16_ARC_RUNTIME` (来源: INFINEON_AURIX2G)
  - `CRC_16_ARC_TABLE` (来源: INFINEON_AURIX2G)
- **描述**: Switch to select one of the available 16-bit CRC16ARC polynomial methods

######## 2. Crc16Mode

- **UUID**: `ECUC:57dcff50-89c4-444b-b345-2c797a2880f7`
- **参数名**: `Crc16Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_16_HARDWARE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_16_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_16_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_16_TABLE` (来源: AUTOSAR_ECUC)
- **描述**: Switch to select one of the available CRC 16-bit (CCITT) calculation methods

######## 3. Crc32Mode

- **UUID**: `ECUC:17071ba5-9db3-4cb9-a8ec-b5c97e935977`
- **参数名**: `Crc32Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_32_HARDWARE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_32_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_32_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_32_TABLE` (来源: AUTOSAR_ECUC)
- **描述**: Switch to select one of the available CRC 32-bit (IEEE-802.3 CRC32 Ethernet Standard) calculation methods

######## 4. Crc32P4Mode

- **UUID**: `ECUC:27a43b49-5515-4849-a334-4e1c9703d3de`
- **参数名**: `Crc32P4Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_32P4_TABLE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_32P4_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_32P4_TABLE` (来源: AUTOSAR_ECUC)
- **描述**: Switch to select one of the available CRC 32-bit E2E Profile 4 calculation methods.

######## 5. Crc64Mode

- **UUID**: `ECUC:33ac1f0b-Fa33-4b56-B750-96ea5fa92070`
- **参数名**: `Crc64Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_64_TABLE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CRC_64_RUNTIME` (来源: INFINEON_AURIX2G)
  - `CRC_64_TABLE` (来源: INFINEON_AURIX2G)
- **描述**: Switch to select one of the available CRC 64-bit calculation methods.

######## 6. Crc8H2FMode

- **UUID**: `ECUC:4e2ed5e0-022e-415d-9e9c-ce4263e08b97`
- **参数名**: `Crc8H2FMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_8H2F_HARDWARE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_8H2F_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_8H2F_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_8H2F_TABLE` (来源: AUTOSAR_ECUC)
- **描述**: Switch to select one of the available CRC 8-bit (2Fh polynomial) calculation methods

######## 7. Crc8Mode

- **UUID**: `ECUC:965dd362-cb66-40a5-bdb1-1b6521fc6a0e`
- **参数名**: `Crc8Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_8_HARDWARE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_8_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_8_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_8_TABLE` (来源: AUTOSAR_ECUC)
- **描述**: Switch to select one of the available CRC 8-bit (SAE J1850) calculation methods

######## 8. CrcRuntimeApiMode

- **UUID**: `ECUC:965dd362-cb66-40a5-bdb1-1b6521fc6a0d`
- **参数名**: `CrcRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRC_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CRC_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `CRC_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: Switch to select one of the available CRC implementation mode

##### 2. CrcChannelConfig

**容器属性**:

- **UUID**: `ECUC:c03229fe-2dca-418e-a47c-1ab11e6c1922`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CrcChannelConfig`
- **多重性**: [0..6]

**容器描述**:

CRC Configuration of FCE channels, callback functions and alloctaion of DMA channel

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CrcChannelId

- **UUID**: `ECUC:c03229fe-3aca-418e-a47c-1ab11e6c2032`
- **参数名**: `CrcChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: CRC Allocation of FCE channels

####### FUNCTION-NAME 类型参数

######## 1. CrcResultNotification

- **UUID**: `ECUC:c03229fe-5dca-418e-a47c-1ab11e6c2252`
- **参数名**: `CrcResultNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: User defined result callback function

######## 2. CrcErrorNotification

- **UUID**: `ECUC:c03229fe-5dca-418e-a47c-1ab11e6c2253`
- **参数名**: `CrcErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: User defined error callback functionr

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CrcDmaChannel

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `CrcDmaChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter contains reference to DMA resource allocated to FCE

##### 3. CrcPublishedInformation

**容器属性**:

- **UUID**: `ECUC:9e1f6afd-afe0-45c8-a88c-30d587a71e8d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CrcPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

Note that these parameters do not have any configuration class setting, since they are published information.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CrcInitialValue16

- **UUID**: `ECUC:9647a421-47c3-4e83-83ca-3f409051a573`
- **参数名**: `CrcInitialValue16`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `65535`
- **取值范围**: [65535..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 16-bit CRC calculation.

######## 2. CrcInitialValue16ARC

- **UUID**: `ECUC:9647a421-47c3-4e83-83ca-3f409051cc1c`
- **参数名**: `CrcInitialValue16ARC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 16-bit CRC16ARC calculation

######## 3. CrcInitialValue8

- **UUID**: `ECUC:9647a421-47c3-4e83-83ca-3f409051a572`
- **参数名**: `CrcInitialValue8`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [255..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 8-bit CRC calculation.

######## 4. CrcInitialValue8H2F

- **UUID**: `ECUC:9647a421-47c3-4e83-83ca-3f409051a571`
- **参数名**: `CrcInitialValue8H2F`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `255`
- **取值范围**: [255..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 8-bit CRC8H2F calculation.

######## 5. CrcInitialValue32

- **UUID**: `ECUC:3c5bfda0-c90e-4757-aafd-2e297b37168b`
- **参数名**: `CrcInitialValue32`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [4294967295..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 32-bit CRC calculation.

######## 6. CrcInitialValue32P4

- **UUID**: `ECUC:3c5bfda0-c90e-4757-aafd-2e287b27177c`
- **参数名**: `CrcInitialValue32P4`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [4294967295..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 32-bit CRC32P4 calculation.

######## 7. CrcInitialValue64

- **UUID**: `ECUC:3c5bfda0-c90e-4757-aafd-2e287b27178b`
- **参数名**: `CrcInitialValue64`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `18446744073709551615`
- **取值范围**: [0..18446744073709551615]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial value for the 64-bit CRC64 calculation.

##### 4. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-88fe-1166b258bb8a`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-bff0-eb2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e10017d4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8f4b87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `20`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `201`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-a68e-5f0c416501d1`
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
- **描述**: Aurix derivative used for the implementation

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

1. **Crc**
