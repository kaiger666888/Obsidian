# Spi - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:57

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Spi](#spi)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Spi

#### 基本信息

- **UUID**: `ECUC:c9bf8ca4-b837-488e-884e-650fb6a34dee`
- **模块名称**: `Spi`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Spi (Serial Peripheral Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. SpiDriver

**容器属性**:

- **UUID**: `ECUC:56a72daf-c292-43bd-9989-a7d0120ded9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDriver`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Configuration of one instance (if multiplicity is 1, it is the sole configuration) of an SPI driver.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SpiMaxChannel

- **UUID**: `ECUC:0b8b6daa-25d6-4474-b831-47457b71a111`
- **参数名**: `SpiMaxChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the number of Channels configured. It will be gathered by tools during the configuration stage.

######## 2. SpiMaxJob

- **UUID**: `ECUC:d0bedae2-a4fe-4171-bd96-d73b06d23ac4`
- **参数名**: `SpiMaxJob`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Total number of Jobs configured.

######## 3. SpiMaxSequence

- **UUID**: `ECUC:1815d8ea-5da2-491e-9524-6625c11c90cf`
- **参数名**: `SpiMaxSequence`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Total number of Sequences configured.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. SpiChannel

**容器属性**:

- **UUID**: `ECUC:f2748179-dbc5-4754-b29d-73ae022425e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-channel

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelId

- **UUID**: `ECUC:57cf4873-901e-44b3-8e63-0c4280de938d`
- **参数名**: `SpiChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Channel ID, used as parameter in SPI API functions.

########## 2. SpiDataWidth

- **UUID**: `ECUC:1aa15934-fb17-437e-9366-be307c42368b`
- **参数名**: `SpiDataWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the width of a transmitted data unit.

########## 3. SpiDefaultData

- **UUID**: `ECUC:464acbf4-53a4-4964-843d-432be296ecb9`
- **参数名**: `SpiDefaultData`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default data to be transmitted when (for internal buffer or external buffer) the pointer passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is NULL.

########## 4. SpiEbMaxLength

- **UUID**: `ECUC:202d39ab-4e1d-4eaa-a539-8a106e07b926`
- **参数名**: `SpiEbMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the maximum size (in bytes) of data buffers in case of EB Channels and only.

########## 5. SpiIbNBuffers

- **UUID**: `ECUC:4de36954-b7d2-4c48-9bd6-6e0196eba21a`
- **参数名**: `SpiIbNBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the maximum number of data buffers in case of IB Channels and only.

######### ENUMERATION 类型参数

########## 1. SpiChannelType

- **UUID**: `ECUC:6b345ae6-4631-4cb8-af29-b9a20aeb6d8c`
- **参数名**: `SpiChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EB` (来源: AUTOSAR_ECUC)
  - `IB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer usage with EB/IB channel.

########## 2. SpiTransferStart

- **UUID**: `ECUC:c8e19a9c-9ff2-4b2d-8f31-5b59e7a65181`
- **参数名**: `SpiTransferStart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LSB` (来源: AUTOSAR_ECUC)
  - `MSB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the first starting bit for transmission.

####### 2. SpiDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:8ee1511e-a250-43ec-84a7-20ed59600fc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SPI_E_HARDWARE_ERROR

- **UUID**: `ECUC:16a6922a-5961-4442-ae00-f898421141f3`
- **引用名**: `SPI_E_HARDWARE_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when a hardware error was detected. If the reference is not configured the error shall not be reported.

####### 3. SpiExternalDevice

**容器属性**:

- **UUID**: `ECUC:801f9c6a-fd4a-4d1b-a2f3-d9cf1d1145b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiExternalDevice`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The communication settings of an external device. Closely linked to SpiJob.

######## 参数配置

此容器包含 **9** 个参数：

######### BOOLEAN 类型参数

########## 1. SpiEnableCs

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c4e`
- **参数名**: `SpiEnableCs`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables or not the Chip Select handling functions. If this parameter is enabled then parameter SpiCsSelection further details the type of chip selection.

######### FLOAT 类型参数

########## 1. SpiBaudrate

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3c448`
- **参数名**: `SpiBaudrate`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the communication baudrate - This parameter allows

########## 2. SpiTimeClk2Cs

- **UUID**: `ECUC:756a5087-687e-43ae-8607-2470f7de9db7`
- **参数名**: `SpiTimeClk2Cs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1E-4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timing between clock and chip select (in seconds) - This parameter allows to use a range of values from 0 up to 0.0001 seconds.

######### STRING 类型参数

########## 1. SpiCsIdentifier

- **UUID**: `ECUC:af7c2eb8-32b9-40eb-b810-52c4dae7caf4`
- **参数名**: `SpiCsIdentifier`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the symbolic name to identify the Chip Select (CS) allocated to this Job.

######### ENUMERATION 类型参数

########## 1. SpiCsPolarity

- **UUID**: `ECUC:07cb58ef-8a6f-4146-9ab5-380cb5de8918`
- **参数名**: `SpiCsPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the active polarity of Chip Select.

########## 2. SpiCsSelection

- **UUID**: `ECUC:6654d212-8ab8-41d7-8479-520af776eb1c`
- **参数名**: `SpiCsSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CS_VIA_PERIPHERAL_ENGINE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CS_VIA_GPIO` (来源: AUTOSAR_ECUC)
  - `CS_VIA_PERIPHERAL_ENGINE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the Chip select handling is enabled (see SpiEnableCs), then this parameter specifies if the chip select is handled automatically by Peripheral HW engine or via general purpose IO by Spi driver.

########## 3. SpiDataShiftEdge

- **UUID**: `ECUC:3500cbba-2a1c-4073-873f-83083f11ce53`
- **参数名**: `SpiDataShiftEdge`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LEADING` (来源: AUTOSAR_ECUC)
  - `TRAILING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the SPI data shift edge.

########## 4. SpiHwUnit

- **UUID**: `ECUC:c9df357c-60ad-4f37-ac85-1c24c9fbacb7`
- **参数名**: `SpiHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CSIB0` (来源: AUTOSAR_ECUC)
  - `CSIB1` (来源: AUTOSAR_ECUC)
  - `CSIB2` (来源: AUTOSAR_ECUC)
  - `CSIB3` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the symbolic name to identify the HW SPI Hardware

########## 5. SpiShiftClockIdleLevel

- **UUID**: `ECUC:da746c64-de65-4db4-a5db-bcccb49f3c56`
- **参数名**: `SpiShiftClockIdleLevel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the SPI shift clock idle level.

####### 4. SpiJob

**容器属性**:

- **UUID**: `ECUC:02dff674-91c0-4b9a-a3a8-32619f35d54c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-Job, amongst others the connection between the internal SPI unit and the special settings for an external device is done.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SpiJobId

- **UUID**: `ECUC:3ea95b90-3a95-48b4-ab87-e0a8fe7221fd`
- **参数名**: `SpiJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Job ID, used as parameter in SPI API functions.

########## 2. SpiJobPriority

- **UUID**: `ECUC:18823873-1f2a-4df0-a761-3c3a4540b359`
- **参数名**: `SpiJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority set accordingly to SPI093: 0, lowest, 3, highest priority

######### ENUMERATION 类型参数

########## 1. SpiHwUnitSynchronous

- **UUID**: `ECUC:42dd7af3-c6e8-47f5-92f0-de2a43e78475`
- **参数名**: `SpiHwUnitSynchronous`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If SpiHwUnitSynchronous is set to "SYNCHRONOUS", the SpiJob uses its containing SpiDriver in a synchronous manner. If it is set to "ASYNCHRONOUS", it uses the driver in an asynchronous way. If the parameter is not set, the SpiChannel uses the driver also in an asynchronous way.

######### FUNCTION-NAME 类型参数

########## 1. SpiJobEndNotification

- **UUID**: `ECUC:74518a4a-bc61-4898-915d-7deca2577064`
- **参数名**: `SpiJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a notification function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiDeviceAssignment

- **UUID**: `ECUC:ffde9462-b41e-487a-8d62-d4940bae49b7`
- **引用名**: `SpiDeviceAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiExternalDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiExternalDevice`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external device used by this job

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

References to SPI channels and their order within the Job.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the order of Channels within the Job.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A job reference to a SPI channel.

####### 5. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

References to SPI channels and their order within the Job.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the order of Channels within the Job.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A job reference to a SPI channel.

####### 6. SpiSequence

**容器属性**:

- **UUID**: `ECUC:3cb6ec10-7596-4a7e-9ee9-b08170958ddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiSequence`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-sequence

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SpiSequenceId

- **UUID**: `ECUC:2f5ec946-17d2-4d3b-aadc-f03cfc2d985c`
- **参数名**: `SpiSequenceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Sequence ID, used as parameter in SPI API functions.

######### BOOLEAN 类型参数

########## 1. SpiInterruptibleSequence

- **UUID**: `ECUC:8f6b2ed8-3991-4bfe-bec5-cb279b9ca41d`
- **参数名**: `SpiInterruptibleSequence`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter allows or not this Sequence to be suspended by another one.

######### FUNCTION-NAME 类型参数

########## 1. SpiSeqEndNotification

- **UUID**: `ECUC:2e282067-fed0-4803-aa66-d641c71663e7`
- **参数名**: `SpiSeqEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a notification function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiJobAssignment

- **UUID**: `ECUC:d88727e5-d5c4-4148-adeb-aab0bef83355`
- **引用名**: `SpiJobAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiJob`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A sequence references several jobs, which are executed during a communication sequence

##### 2. SpiChannel

**容器属性**:

- **UUID**: `ECUC:f2748179-dbc5-4754-b29d-73ae022425e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-channel

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelId

- **UUID**: `ECUC:57cf4873-901e-44b3-8e63-0c4280de938d`
- **参数名**: `SpiChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Channel ID, used as parameter in SPI API functions.

######## 2. SpiDataWidth

- **UUID**: `ECUC:1aa15934-fb17-437e-9366-be307c42368b`
- **参数名**: `SpiDataWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..32]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the width of a transmitted data unit.

######## 3. SpiDefaultData

- **UUID**: `ECUC:464acbf4-53a4-4964-843d-432be296ecb9`
- **参数名**: `SpiDefaultData`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default data to be transmitted when (for internal buffer or external buffer) the pointer passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is NULL.

######## 4. SpiEbMaxLength

- **UUID**: `ECUC:202d39ab-4e1d-4eaa-a539-8a106e07b926`
- **参数名**: `SpiEbMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the maximum size (in bytes) of data buffers in case of EB Channels and only.

######## 5. SpiIbNBuffers

- **UUID**: `ECUC:4de36954-b7d2-4c48-9bd6-6e0196eba21a`
- **参数名**: `SpiIbNBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the maximum number of data buffers in case of IB Channels and only.

####### ENUMERATION 类型参数

######## 1. SpiChannelType

- **UUID**: `ECUC:6b345ae6-4631-4cb8-af29-b9a20aeb6d8c`
- **参数名**: `SpiChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EB` (来源: AUTOSAR_ECUC)
  - `IB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer usage with EB/IB channel.

######## 2. SpiTransferStart

- **UUID**: `ECUC:c8e19a9c-9ff2-4b2d-8f31-5b59e7a65181`
- **参数名**: `SpiTransferStart`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LSB` (来源: AUTOSAR_ECUC)
  - `MSB` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the first starting bit for transmission.

##### 3. SpiDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:8ee1511e-a250-43ec-84a7-20ed59600fc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SPI_E_HARDWARE_ERROR

- **UUID**: `ECUC:16a6922a-5961-4442-ae00-f898421141f3`
- **引用名**: `SPI_E_HARDWARE_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when a hardware error was detected. If the reference is not configured the error shall not be reported.

##### 4. SpiExternalDevice

**容器属性**:

- **UUID**: `ECUC:801f9c6a-fd4a-4d1b-a2f3-d9cf1d1145b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiExternalDevice`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The communication settings of an external device. Closely linked to SpiJob.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. SpiEnableCs

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c4e`
- **参数名**: `SpiEnableCs`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables or not the Chip Select handling functions. If this parameter is enabled then parameter SpiCsSelection further details the type of chip selection.

####### FLOAT 类型参数

######## 1. SpiBaudrate

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3c448`
- **参数名**: `SpiBaudrate`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the communication baudrate - This parameter allows

######## 2. SpiTimeClk2Cs

- **UUID**: `ECUC:756a5087-687e-43ae-8607-2470f7de9db7`
- **参数名**: `SpiTimeClk2Cs`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1E-4]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timing between clock and chip select (in seconds) - This parameter allows to use a range of values from 0 up to 0.0001 seconds.

####### STRING 类型参数

######## 1. SpiCsIdentifier

- **UUID**: `ECUC:af7c2eb8-32b9-40eb-b810-52c4dae7caf4`
- **参数名**: `SpiCsIdentifier`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the symbolic name to identify the Chip Select (CS) allocated to this Job.

####### ENUMERATION 类型参数

######## 1. SpiCsPolarity

- **UUID**: `ECUC:07cb58ef-8a6f-4146-9ab5-380cb5de8918`
- **参数名**: `SpiCsPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the active polarity of Chip Select.

######## 2. SpiCsSelection

- **UUID**: `ECUC:6654d212-8ab8-41d7-8479-520af776eb1c`
- **参数名**: `SpiCsSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CS_VIA_PERIPHERAL_ENGINE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CS_VIA_GPIO` (来源: AUTOSAR_ECUC)
  - `CS_VIA_PERIPHERAL_ENGINE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the Chip select handling is enabled (see SpiEnableCs), then this parameter specifies if the chip select is handled automatically by Peripheral HW engine or via general purpose IO by Spi driver.

######## 3. SpiDataShiftEdge

- **UUID**: `ECUC:3500cbba-2a1c-4073-873f-83083f11ce53`
- **参数名**: `SpiDataShiftEdge`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LEADING` (来源: AUTOSAR_ECUC)
  - `TRAILING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the SPI data shift edge.

######## 4. SpiHwUnit

- **UUID**: `ECUC:c9df357c-60ad-4f37-ac85-1c24c9fbacb7`
- **参数名**: `SpiHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CSIB0` (来源: AUTOSAR_ECUC)
  - `CSIB1` (来源: AUTOSAR_ECUC)
  - `CSIB2` (来源: AUTOSAR_ECUC)
  - `CSIB3` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is the symbolic name to identify the HW SPI Hardware

######## 5. SpiShiftClockIdleLevel

- **UUID**: `ECUC:da746c64-de65-4db4-a5db-bcccb49f3c56`
- **参数名**: `SpiShiftClockIdleLevel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the SPI shift clock idle level.

##### 5. SpiJob

**容器属性**:

- **UUID**: `ECUC:02dff674-91c0-4b9a-a3a8-32619f35d54c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-Job, amongst others the connection between the internal SPI unit and the special settings for an external device is done.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SpiJobId

- **UUID**: `ECUC:3ea95b90-3a95-48b4-ab87-e0a8fe7221fd`
- **参数名**: `SpiJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Job ID, used as parameter in SPI API functions.

######## 2. SpiJobPriority

- **UUID**: `ECUC:18823873-1f2a-4df0-a761-3c3a4540b359`
- **参数名**: `SpiJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority set accordingly to SPI093: 0, lowest, 3, highest priority

####### ENUMERATION 类型参数

######## 1. SpiHwUnitSynchronous

- **UUID**: `ECUC:42dd7af3-c6e8-47f5-92f0-de2a43e78475`
- **参数名**: `SpiHwUnitSynchronous`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If SpiHwUnitSynchronous is set to "SYNCHRONOUS", the SpiJob uses its containing SpiDriver in a synchronous manner. If it is set to "ASYNCHRONOUS", it uses the driver in an asynchronous way. If the parameter is not set, the SpiChannel uses the driver also in an asynchronous way.

####### FUNCTION-NAME 类型参数

######## 1. SpiJobEndNotification

- **UUID**: `ECUC:74518a4a-bc61-4898-915d-7deca2577064`
- **参数名**: `SpiJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a notification function.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiDeviceAssignment

- **UUID**: `ECUC:ffde9462-b41e-487a-8d62-d4940bae49b7`
- **引用名**: `SpiDeviceAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiExternalDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiExternalDevice`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external device used by this job

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

References to SPI channels and their order within the Job.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the order of Channels within the Job.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A job reference to a SPI channel.

##### 6. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

References to SPI channels and their order within the Job.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the order of Channels within the Job.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A job reference to a SPI channel.

##### 7. SpiSequence

**容器属性**:

- **UUID**: `ECUC:3cb6ec10-7596-4a7e-9ee9-b08170958ddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiSequence`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

All data needed to configure one SPI-sequence

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SpiSequenceId

- **UUID**: `ECUC:2f5ec946-17d2-4d3b-aadc-f03cfc2d985c`
- **参数名**: `SpiSequenceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: SPI Sequence ID, used as parameter in SPI API functions.

####### BOOLEAN 类型参数

######## 1. SpiInterruptibleSequence

- **UUID**: `ECUC:8f6b2ed8-3991-4bfe-bec5-cb279b9ca41d`
- **参数名**: `SpiInterruptibleSequence`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter allows or not this Sequence to be suspended by another one.

####### FUNCTION-NAME 类型参数

######## 1. SpiSeqEndNotification

- **UUID**: `ECUC:2e282067-fed0-4803-aa66-d641c71663e7`
- **参数名**: `SpiSeqEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to a notification function.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiJobAssignment

- **UUID**: `ECUC:d88727e5-d5c4-4148-adeb-aab0bef83355`
- **引用名**: `SpiJobAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `SpiJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiJob`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A sequence references several jobs, which are executed during a communication sequence

##### 8. SpiGeneral

**容器属性**:

- **UUID**: `ECUC:e8854824-b4c9-4618-aa5b-46efc092de25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration settings for SPI-Handler

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelBuffersAllowed

- **UUID**: `ECUC:0067ac2f-f0fd-40dc-9bd8-9e982207d046`
- **参数名**: `SpiChannelBuffersAllowed`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the SPI Handler/Driver Channel Buffers usage allowed and

######## 2. SpiLevelDelivered

- **UUID**: `ECUC:f15843c0-09d6-43d4-8794-73a66d2c4505`
- **参数名**: `SpiLevelDelivered`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the SPI Handler/Driver level of scalable functionality that is

####### BOOLEAN 类型参数

######## 1. SpiCancelApi

- **UUID**: `ECUC:e2c6330e-7d7f-4d1c-b975-e46ef315e714`
- **参数名**: `SpiCancelApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Spi_Cancel function ON or OFF.

######## 2. SpiDevErrorDetect

- **UUID**: `ECUC:a50f2a2c-5374-496e-a509-5073192fe0a5`
- **参数名**: `SpiDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 3. SpiHwStatusApi

- **UUID**: `ECUC:4e6873dc-5c72-45d4-a49a-f37d8bad7f2b`
- **参数名**: `SpiHwStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Spi_GetHWUnitStatus function ON or OFF.

######## 4. SpiInterruptibleSeqAllowed

- **UUID**: `ECUC:f010eb50-2a4e-4a75-ab18-1ab5413ac8ae`
- **参数名**: `SpiInterruptibleSeqAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Interruptible Sequences handling functionality ON or OFF.

######## 5. SpiSupportConcurrentSyncTransmit

- **UUID**: `ECUC:d38d155d-a5e5-4354-bc92-8f1e56f3fca1`
- **参数名**: `SpiSupportConcurrentSyncTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether concurrent Spi_SyncTransmit() calls for different sequences shall be configurable.

######## 6. SpiVersionInfoApi

- **UUID**: `ECUC:8629314a-5451-4737-a52a-3f967ae9aba8`
- **参数名**: `SpiVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Spi_GetVersionInfo function ON or OFF.

##### 9. SpiPublishedInformation

**容器属性**:

- **UUID**: `ECUC:ab74629f-37d4-453b-b708-5dc31fe4fe2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container holding all SPI specific published information parameters

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SpiMaxHwUnit

- **UUID**: `ECUC:3e514982-2194-4b74-8c2e-baa2b264704d`
- **参数名**: `SpiMaxHwUnit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-LINK-TIME
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Number of different SPI hardware microcontroller peripherals (units/busses) available and handled by this SPI Handler/Driver module.

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

1. **Spi**
