# Fls - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:18

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fls](#fls)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fls

#### 基本信息

- **UUID**: `ECUC:d05369fd-d6e0-44c1-8a9f-9d2a5561badf`
- **模块名称**: `Fls`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Fls (internal or external flash driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. FlsConfigSet

**容器属性**:

- **UUID**: `ECUC:3d6f9ca5-bb01-4ee7-bd4f-253b60f2cc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Container for runtime configuration parameters of the flash driver.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. FlsAcErase

- **UUID**: `ECUC:2a204be2-76ae-465c-b358-c7c06f4d42ce`
- **参数名**: `FlsAcErase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address offset in RAM to which the erase flash access code shall be loaded.

######## 2. FlsAcWrite

- **UUID**: `ECUC:326f888f-0676-4eec-a10e-f8159c0655ee`
- **参数名**: `FlsAcWrite`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Address offset in RAM to which the write flash access code shall be loaded.

######## 3. FlsMaxReadFastMode

- **UUID**: `ECUC:1095bfd8-716a-4dfb-a62d-89ee6d513df9`
- **参数名**: `FlsMaxReadFastMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum number of bytes to read or compare in one cycle of the flash driver's job processing function in fast mode.

######## 4. FlsMaxReadNormalMode

- **UUID**: `ECUC:fc26eec9-3ec1-4860-a1e2-905f73d14265`
- **参数名**: `FlsMaxReadNormalMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum number of bytes to read or compare in one cycle of the flash driver's job processing function in normal mode.

######## 5. FlsMaxWriteFastMode

- **UUID**: `ECUC:006f40ff-e794-490e-9ec6-057e04aada0c`
- **参数名**: `FlsMaxWriteFastMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum number of bytes to write in one cycle of the flash driver's job processing function in fast mode.

######## 6. FlsMaxWriteNormalMode

- **UUID**: `ECUC:b03a7114-6d17-46c2-9f4b-2853f0e44291`
- **参数名**: `FlsMaxWriteNormalMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum number of bytes to write in one cycle of the flash driver's job processing function in normal mode.

######## 7. FlsProtection

- **UUID**: `ECUC:78d9a61d-5c1e-494b-95b2-09349577769b`
- **参数名**: `FlsProtection`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Erase/write protection settings. Only relevant if supported by hardware.

####### FLOAT 类型参数

######## 1. FlsCallCycle

- **UUID**: `ECUC:cec56299-7876-4cfc-9811-10a8cdc9b035`
- **参数名**: `FlsCallCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Cycle time of calls of the flash driver's main function (in seconds).

####### ENUMERATION 类型参数

######## 1. FlsDefaultMode

- **UUID**: `ECUC:f72e69f0-f52b-4383-9077-224b9258cf31`
- **参数名**: `FlsDefaultMode`
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
- **描述**: This parameter is the default FLS device mode after initialization.

####### FUNCTION-NAME 类型参数

######## 1. FlsJobEndNotification

- **UUID**: `ECUC:01bf35d4-f65a-4e62-8fcb-bc18bb89b960`
- **参数名**: `FlsJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job end notification routine provided by some upper layer module, typically the Fee module.

######## 2. FlsJobErrorNotification

- **UUID**: `ECUC:da44a748-916b-4a62-a4cf-44f5fbb45d0c`
- **参数名**: `FlsJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job error notification routine provided by some upper layer module, typically the Fee module.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FlsDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:fe9f0540-d42d-403b-800e-5698c8b8f894`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **5** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FLS_E_COMPARE_FAILED

- **UUID**: `ECUC:1afc7fa9-2d93-470a-a7e9-d183ba72fb34`
- **引用名**: `FLS_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash compare failed (HW)" has occurred.

########## 2. FLS_E_ERASE_FAILED

- **UUID**: `ECUC:f339bf7e-b28f-4c49-a70b-75a714eace96`
- **引用名**: `FLS_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash erase failed (HW)" has occurred.

########## 3. FLS_E_READ_FAILED

- **UUID**: `ECUC:494d3058-fb65-44de-bed8-0231d2858800`
- **引用名**: `FLS_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash read failed (HW)" has occurred.

########## 4. FLS_E_UNEXPECTED_FLASH_ID

- **UUID**: `ECUC:c32b2d32-9bdc-4b84-af48-c829dc459d97`
- **引用名**: `FLS_E_UNEXPECTED_FLASH_ID`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Expected hardware ID not matched" has occurred.

########## 5. FLS_E_WRITE_FAILED

- **UUID**: `ECUC:cfc28b37-3775-4e16-8d98-e05917d2ed66`
- **引用名**: `FLS_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash write failed (HW)" has occurred.

####### 2. FlsExternalDriver

**容器属性**:

- **UUID**: `ECUC:81c36c86-d308-47d4-bc55-a02b401446e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsExternalDriver`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is present for external Flash drivers only. Internal Flash drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FlsSpiReference

- **UUID**: `ECUC:0124051e-19cb-4f30-8c5a-476d3847afb6`
- **引用名**: `FlsSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SPI sequence (required for external Flash drivers).

####### 3. FlsSectorList

**容器属性**:

- **UUID**: `ECUC:48a5cfc6-7ab9-44e4-a3eb-9e4eb901c845`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSectorList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

List of flashable sectors and pages.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration description of a flashable sector

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

############ 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector.

############ 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector.

############ 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of this sector.

####### 4. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration description of a flashable sector

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

########## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector.

########## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector.

########## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of this sector.

##### 2. FlsDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:fe9f0540-d42d-403b-800e-5698c8b8f894`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **5** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FLS_E_COMPARE_FAILED

- **UUID**: `ECUC:1afc7fa9-2d93-470a-a7e9-d183ba72fb34`
- **引用名**: `FLS_E_COMPARE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash compare failed (HW)" has occurred.

######## 2. FLS_E_ERASE_FAILED

- **UUID**: `ECUC:f339bf7e-b28f-4c49-a70b-75a714eace96`
- **引用名**: `FLS_E_ERASE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash erase failed (HW)" has occurred.

######## 3. FLS_E_READ_FAILED

- **UUID**: `ECUC:494d3058-fb65-44de-bed8-0231d2858800`
- **引用名**: `FLS_E_READ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash read failed (HW)" has occurred.

######## 4. FLS_E_UNEXPECTED_FLASH_ID

- **UUID**: `ECUC:c32b2d32-9bdc-4b84-af48-c829dc459d97`
- **引用名**: `FLS_E_UNEXPECTED_FLASH_ID`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Expected hardware ID not matched" has occurred.

######## 5. FLS_E_WRITE_FAILED

- **UUID**: `ECUC:cfc28b37-3775-4e16-8d98-e05917d2ed66`
- **引用名**: `FLS_E_WRITE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Flash write failed (HW)" has occurred.

##### 3. FlsExternalDriver

**容器属性**:

- **UUID**: `ECUC:81c36c86-d308-47d4-bc55-a02b401446e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsExternalDriver`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is present for external Flash drivers only. Internal Flash drivers do not use the parameter listed in this container, hence its multiplicity is 0 for internal drivers.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FlsSpiReference

- **UUID**: `ECUC:0124051e-19cb-4f30-8c5a-476d3847afb6`
- **引用名**: `FlsSpiReference`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SPI sequence (required for external Flash drivers).

##### 4. FlsSectorList

**容器属性**:

- **UUID**: `ECUC:48a5cfc6-7ab9-44e4-a3eb-9e4eb901c845`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSectorList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

List of flashable sectors and pages.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration description of a flashable sector

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

########## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector.

########## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector.

########## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of this sector.

##### 5. FlsSector

**容器属性**:

- **UUID**: `ECUC:4a46d887-b3be-41a3-aa7b-031bfa23ac7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsSector`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration description of a flashable sector

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FlsNumberOfSectors

- **UUID**: `ECUC:182b2aa9-9cd0-4305-91a4-e9a69decf610`
- **参数名**: `FlsNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for FlsSectorSize and

######## 2. FlsPageSize

- **UUID**: `ECUC:ad1fae4e-3ea1-4584-a148-c8669780a684`
- **参数名**: `FlsPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector.

######## 3. FlsSectorSize

- **UUID**: `ECUC:3994527a-0bfb-4ec5-8864-374a51cade70`
- **参数名**: `FlsSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector.

######## 4. FlsSectorStartaddress

- **UUID**: `ECUC:61630dd0-0649-4365-ad45-d691f452ce17`
- **参数名**: `FlsSectorStartaddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Start address of this sector.

##### 6. FlsGeneral

**容器属性**:

- **UUID**: `ECUC:3091e295-abe7-43a0-98f4-e60da9dc4945`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for general parameters of the flash driver. These parameters are always pre-compile.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. FlsBaseAddress

- **UUID**: `ECUC:ea05556a-aa1f-4a79-8824-757f1614471c`
- **参数名**: `FlsBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The flash memory start address (see also FLS208 and FLS209).

######## 2. FlsDriverIndex

- **UUID**: `ECUC:24f7c0cd-07e7-40be-82f4-001abe599d00`
- **参数名**: `FlsDriverIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the driver, used by FEE.

######## 3. FlsTotalSize

- **UUID**: `ECUC:a8cdc4a9-dcbe-4c4e-82e9-d76da4755fe2`
- **参数名**: `FlsTotalSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The total amount of flash memory in bytes (see also FLS208 and FLS209).

####### BOOLEAN 类型参数

######## 1. FlsAcLoadOnJobStart

- **UUID**: `ECUC:622bd1f2-a9e0-4043-9b1a-8baa38771911`
- **参数名**: `FlsAcLoadOnJobStart`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The flash driver shall load the flash access code to RAM whenever an erase or write job is started and unload (overwrite) it after that job has been finished or canceled.

######## 2. FlsCancelApi

- **UUID**: `ECUC:893eebfb-c839-4cbf-8310-bdb18b1a08e5`
- **参数名**: `FlsCancelApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable and disable the Fls_Cancel function.

######## 3. FlsCompareApi

- **UUID**: `ECUC:b694dc7a-1a2c-45f5-84df-452bb9b75354`
- **参数名**: `FlsCompareApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable and disable the Fls_Compare function.

######## 4. FlsDevErrorDetect

- **UUID**: `ECUC:6f390fca-9815-44eb-91ab-841f2b962337`
- **参数名**: `FlsDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection (see FLS077).

######## 5. FlsGetJobResultApi

- **UUID**: `ECUC:760f215b-bb6c-4810-950c-be3df14fa844`
- **参数名**: `FlsGetJobResultApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable and disable the Fls_GetJobResult function.

######## 6. FlsGetStatusApi

- **UUID**: `ECUC:e5af54cf-a0b9-49e0-87a3-044cafdfe2c1`
- **参数名**: `FlsGetStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable and disable the Fls_GetStatus function.

######## 7. FlsSetModeApi

- **UUID**: `ECUC:b5756f12-6f52-4348-9416-7cf894e79a8d`
- **参数名**: `FlsSetModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable and disable the Fls_SetMode function.

######## 8. FlsUseInterrupts

- **UUID**: `ECUC:88a2d255-2439-43a9-888a-c21a750ac380`
- **参数名**: `FlsUseInterrupts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Job processing triggered by hardware interrupt.

######## 9. FlsVersionInfoApi

- **UUID**: `ECUC:b18ae536-69a0-4336-a3ca-9d170d7b33d9`
- **参数名**: `FlsVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

##### 7. FlsPublishedInformation

**容器属性**:

- **UUID**: `ECUC:8e0d2c5d-45de-462e-ba90-f372ccf8e6de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FlsPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FlsAcLocationErase

- **UUID**: `ECUC:2ed61e35-84bc-47f4-9c77-22b984edd9ba`
- **参数名**: `FlsAcLocationErase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Position in RAM, to which the erase flash access code has to be loaded.

######## 2. FlsAcLocationWrite

- **UUID**: `ECUC:a5573b35-3446-4cb4-8396-4c7db3aa207a`
- **参数名**: `FlsAcLocationWrite`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Position in RAM, to which the write flash access code has to be loaded.

######## 3. FlsAcSizeErase

- **UUID**: `ECUC:b60ed9c5-bf85-4cb5-84ed-a9de40ed10a6`
- **参数名**: `FlsAcSizeErase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Number of bytes in RAM needed for the erase flash access code.

######## 4. FlsAcSizeWrite

- **UUID**: `ECUC:06a20d0b-9d96-42d3-96e2-e2eb5171101f`
- **参数名**: `FlsAcSizeWrite`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Number of bytes in RAM needed for the write flash access code.

######## 5. FlsErasedValue

- **UUID**: `ECUC:4b2ea1ec-cdcb-4ba5-b243-4ec4a94fe866`
- **参数名**: `FlsErasedValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: The contents of an erased flash memory cell.

######## 6. FlsSpecifiedEraseCycles

- **UUID**: `ECUC:0fed8a26-c89e-4a57-9a52-08d5e936bc27`
- **参数名**: `FlsSpecifiedEraseCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Number of erase cycles specified for the flash device (usually given in the device data sheet).

####### FLOAT 类型参数

######## 1. FlsEraseTime

- **UUID**: `ECUC:9854b5e9-7313-45e6-b78e-52fa98bd13d8`
- **参数名**: `FlsEraseTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Maximum time to erase one complete flash sector.

######## 2. FlsWriteTime

- **UUID**: `ECUC:61ce65fd-81a1-4a8e-93b4-9ab14d046848`
- **参数名**: `FlsWriteTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Maximum time to program one complete flash page.

####### STRING 类型参数

######## 1. FlsExpectedHwId

- **UUID**: `ECUC:b75b0b3e-e68a-4a74-984c-875387d3aa04`
- **参数名**: `FlsExpectedHwId`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of the hardware device that is expected by this driver (the device for which this driver has been implemented).

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

1. **Fls**
