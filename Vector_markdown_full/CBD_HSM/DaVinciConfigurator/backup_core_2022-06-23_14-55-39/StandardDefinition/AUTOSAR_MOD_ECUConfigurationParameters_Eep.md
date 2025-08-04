# Eep - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:16

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Eep](#eep)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Eep

#### 基本信息

- **UUID**: `ECUC:49083375-9770-4483-8866-d41c78e241d8`
- **模块名称**: `Eep`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Eep (internal or external EEPROM driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. EepGeneral

**容器属性**:

- **UUID**: `ECUC:6da1fefd-2d94-4e4c-87c0-b8c5d54ca8a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for general configuration parameters of the EEPROM driver. These parameters are always pre-compile.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. EepDriverIndex

- **UUID**: `ECUC:96eee13f-3fcb-45ce-8d57-4f1eded7fd6a`
- **参数名**: `EepDriverIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the driver, used by EA.

####### BOOLEAN 类型参数

######## 1. EepDevErrorDetect

- **UUID**: `ECUC:34bdb341-a3c2-4585-9d4a-daed9188fc2d`
- **参数名**: `EepDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection.

######## 2. EepUseInterrupts

- **UUID**: `ECUC:6a43f4bc-8323-4d01-9e82-db9508a6b105`
- **参数名**: `EepUseInterrupts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches to activate or deactivate interrupt controlled job processing.

######## 3. EepVersionInfoApi

- **UUID**: `ECUC:cb753447-bc0a-4671-bf6a-c5dcc44a3ea6`
- **参数名**: `EepVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

######## 4. EepWriteCycleReduction

- **UUID**: `ECUC:4e64ffde-a9c2-48e4-bdae-d8a8ec934815`
- **参数名**: `EepWriteCycleReduction`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches to activate or deactivate write cycle reduction (EEPROM value is read and compared before being overwritten).

##### 2. EepInitConfiguration

**容器属性**:

- **UUID**: `ECUC:1d88d79f-231e-493b-aa52-a1f87930e29f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepInitConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Container for runtime configuration parameters of the EEPROM driver.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. EepBaseAddress

- **UUID**: `ECUC:93028e05-dd0d-4650-a460-ee33cbdd8f93`
- **参数名**: `EepBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the EEPROM device base address.

######## 2. EepFastReadBlockSize

- **UUID**: `ECUC:718f371b-74b1-4141-9437-8770a496a258`
- **参数名**: `EepFastReadBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bytes read within one job processing cycle in fast mode. If the hardware does not support burst mode this parameter shall be set to the same value as EepNormalReadBlockSize.

######## 3. EepFastWriteBlockSize

- **UUID**: `ECUC:fc08a723-5488-443b-93ab-478d2b220909`
- **参数名**: `EepFastWriteBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bytes written within one job processing cycle in fast mode. If the hardware does not support burst mode this parameter shall be set to the same value as EepNormalWriteBlockSize.

######## 4. EepNormalReadBlockSize

- **UUID**: `ECUC:81549dd6-bf82-4ce2-a262-76f0358f9276`
- **参数名**: `EepNormalReadBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bytes read within one job processing cycle in normal mode.

######## 5. EepNormalWriteBlockSize

- **UUID**: `ECUC:7a91bdde-f3bd-49a9-81fd-0ab35b04d095`
- **参数名**: `EepNormalWriteBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bytes written within one job processing cycle in normal mode.

######## 6. EepSize

- **UUID**: `ECUC:219d63b3-6fa5-4b89-a7d0-1ec872410990`
- **参数名**: `EepSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the used size of EEPROM device in bytes.

####### FLOAT 类型参数

######## 1. EepJobCallCycle

- **UUID**: `ECUC:44cd6d1b-c896-43ea-b128-9b94a37e2954`
- **参数名**: `EepJobCallCycle`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Call cycle time of the EEPROM driver's main function. Unit: [s]

####### ENUMERATION 类型参数

######## 1. EepDefaultMode

- **UUID**: `ECUC:9c1fed5a-c53a-4c20-8c29-4e34b6322482`
- **参数名**: `EepDefaultMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MEMIF_MODE_SLOW`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MEMIF_MODE_FAST` (来源: AUTOSAR_ECUC)
  - `MEMIF_MODE_SLOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the default EEPROM device mode after initialization.

####### FUNCTION-NAME 类型参数

######## 1. EepJobEndNotification

- **UUID**: `ECUC:e7e2472b-ed57-4e7f-9490-d5b911248f96`
- **参数名**: `EepJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a callback function for positive job result (see EEP045).

######## 2. EepJobErrorNotification

- **UUID**: `ECUC:7c61ec01-82b4-43bd-bcce-6524e202beb8`
- **参数名**: `EepJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a callback function for negative job result (see EEP046).

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. EepDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:f3c207bc-d0c9-4c5f-a034-2498e1382e7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EEP_E_COMPARE_FAILED

- **UUID**: `ECUC:b236cc11-6d52-43a9-90e2-c603000008aa`
- **引用名**: `EEP_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM compare failed (HW)" has occurred.

########## 2. EEP_E_ERASE_FAILED

- **UUID**: `ECUC:a608077a-8dc5-405a-b6cc-58503b75e8cc`
- **引用名**: `EEP_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM erase failed (HW)" has occurred.

########## 3. EEP_E_READ_FAILED

- **UUID**: `ECUC:9284ad29-e97d-4c90-9c4d-e98d33b1aea4`
- **引用名**: `EEP_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM read failed (HW)" has occurred.

########## 4. EEP_E_WRITE_FAILED

- **UUID**: `ECUC:751adede-047f-4d2e-87ae-cf9b6fc59891`
- **引用名**: `EEP_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM write failed (HW)" has occurred.

####### 2. EepExternalDriver

**容器属性**:

- **UUID**: `ECUC:9bc3df65-6bc4-48df-8a95-07072be0543f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepExternalDriver`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is present for external EEPROM drivers only. Internal EEPROM drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EepSpiReference

- **UUID**: `ECUC:8f856d0e-d1b1-433c-b744-a19a895cba7c`
- **引用名**: `EepSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SPI sequence (required for external EEPROM drivers).

##### 3. EepDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:f3c207bc-d0c9-4c5f-a034-2498e1382e7a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **4** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EEP_E_COMPARE_FAILED

- **UUID**: `ECUC:b236cc11-6d52-43a9-90e2-c603000008aa`
- **引用名**: `EEP_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM compare failed (HW)" has occurred.

######## 2. EEP_E_ERASE_FAILED

- **UUID**: `ECUC:a608077a-8dc5-405a-b6cc-58503b75e8cc`
- **引用名**: `EEP_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM erase failed (HW)" has occurred.

######## 3. EEP_E_READ_FAILED

- **UUID**: `ECUC:9284ad29-e97d-4c90-9c4d-e98d33b1aea4`
- **引用名**: `EEP_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM read failed (HW)" has occurred.

######## 4. EEP_E_WRITE_FAILED

- **UUID**: `ECUC:751adede-047f-4d2e-87ae-cf9b6fc59891`
- **引用名**: `EEP_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "EEPROM write failed (HW)" has occurred.

##### 4. EepExternalDriver

**容器属性**:

- **UUID**: `ECUC:9bc3df65-6bc4-48df-8a95-07072be0543f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepExternalDriver`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is present for external EEPROM drivers only. Internal EEPROM drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EepSpiReference

- **UUID**: `ECUC:8f856d0e-d1b1-433c-b744-a19a895cba7c`
- **引用名**: `EepSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SPI sequence (required for external EEPROM drivers).

##### 5. EepPublishedInformation

**容器属性**:

- **UUID**: `ECUC:51498e4e-e34f-4241-ae3e-86fc4685b744`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EepPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. EepAllowedWriteCycles

- **UUID**: `ECUC:870ed76e-b5cb-4605-b433-94f94b0f6434`
- **参数名**: `EepAllowedWriteCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Specified maximum number of write cycles under worst case conditions of specific EEPROM hardware (e.g. +90°C)

######## 2. EepEraseUnitSize

- **UUID**: `ECUC:6c4c9f5c-dbf4-43a7-ba08-406df75515ee`
- **参数名**: `EepEraseUnitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Size of smallest erasable EEPROM data unit in bytes.

######## 3. EepEraseValue

- **UUID**: `ECUC:e69dd195-2fd5-4471-850e-feb249bb6588`
- **参数名**: `EepEraseValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Value of an erased EEPROM cell.

######## 4. EepMinimumAddressType

- **UUID**: `ECUC:58609988-e3ca-4203-8b93-bea4ae0073e9`
- **参数名**: `EepMinimumAddressType`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Minimum expected size of Eep_AddressType.

######## 5. EepMinimumLengthType

- **UUID**: `ECUC:702265b2-2f77-4ca5-afd9-a3f0d3580c32`
- **参数名**: `EepMinimumLengthType`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Minimum expected size of Eep_LengthType.

######## 6. EepReadUnitSize

- **UUID**: `ECUC:d127b029-adfb-4a94-80c4-4dc025ac741a`
- **参数名**: `EepReadUnitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Size of smallest readable EEPROM data unit in bytes.

######## 7. EepSpecifiedEraseCycles

- **UUID**: `ECUC:99bff377-0e9c-40b2-92ce-a3af104eabc9`
- **参数名**: `EepSpecifiedEraseCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Number of erase cycles specified for the EEP device (usually given in the device data sheet).

######## 8. EepTotalSize

- **UUID**: `ECUC:9d0a8d95-b232-4c89-a9ba-4677ff838ef3`
- **参数名**: `EepTotalSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Total size of EEPROM in bytes.

######## 9. EepWriteUnitSize

- **UUID**: `ECUC:746236e5-885d-4706-9ebf-34e5b6010e8f`
- **参数名**: `EepWriteUnitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Size of smallest writeable EEPROM data unit in bytes.

####### FLOAT 类型参数

######## 1. EepEraseTime

- **UUID**: `ECUC:651eda0b-e259-4961-8279-8f9d504f195a`
- **参数名**: `EepEraseTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Maximum time for erasing one EEPROM data unit.

######## 2. EepWriteTime

- **UUID**: `ECUC:2bae1105-caf2-4b57-b023-63ed87ea4ed5`
- **参数名**: `EepWriteTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Maximum time for writing one EEPROM data unit.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Eep**
