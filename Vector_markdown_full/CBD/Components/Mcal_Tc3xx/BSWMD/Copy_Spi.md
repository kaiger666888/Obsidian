# Spi - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Spi](#spi)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Spi

#### 基本信息

- **UUID**: `ECUC:c9bf8ca4-b837-488e-884e-650fb6a34dee`
- **模块名称**: `Spi`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Spi (Serial Peripheral Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. SpiDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:8ee1511e-a250-43ec-84a7-20ed59600fc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDemEventParameterRefs`
- **多重性**: [0..1]

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
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to configured DEM event to report "Hardware failure". If the reference is not configured the error shall not be reported.

##### 2. SpiDriver

**容器属性**:

- **UUID**: `ECUC:56a72daf-c292-43bd-9989-a7d0120ded9e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDriver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR Spi module.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SpiMaxChannel

- **UUID**: `ECUC:0b8b6daa-25d6-4474-b831-47457b71a111`
- **参数名**: `SpiMaxChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the number of Channels configured. It will be gathered by tools during the configuration stage. Note: this parameter should be Removed and Added after the SpiChannel configuration is completed(Since, tool does not auto-refresh the default value)

######## 2. SpiMaxJob

- **UUID**: `ECUC:d0bedae2-a4fe-4171-bd96-d73b06d23ac4`
- **参数名**: `SpiMaxJob`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..5000]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Total number of Jobs configured. It will be gathered by tools during the configuration stage. Note: this parameter should be Removed and Added after the SpiJob configuration is completed(Since, tool does not auto-refresh the default value)

######## 3. SpiMaxSequence

- **UUID**: `ECUC:1815d8ea-5da2-491e-9524-6625c11c90cf`
- **参数名**: `SpiMaxSequence`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Total number of Sequences configured. It will be gathered by tools during the configuration stage. Note: this parameter should be Removed and Added after the SpiSequence configuration is completed(Since, tool does not auto-refresh the default value)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiSystemClock

- **UUID**: `7a12e6a7-f02f-4d95-8b8a-87a36bed8fb9`
- **引用名**: `SpiSystemClock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter is read from the MCU System clock configured - refer to McuQspiFrequency and McuQspiClockSourceSelection in McuClocksettingsConfig container

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. SpiChannel

**容器属性**:

- **UUID**: `ECUC:f2748179-dbc5-4754-b29d-73ae022425e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannel`
- **多重性**: [1..255]

**容器描述**:

All data needed to configure one SPI-channel

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelId

- **UUID**: `ECUC:57cf4873-901e-44b3-8e63-0c4280de938d`
- **参数名**: `SpiChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Channel ID, used as parameter in SPI API functions. It is published in the Spi_Cfg.h file

########## 2. SpiDataWidth

- **UUID**: `ECUC:1aa15934-fb17-437e-9366-be307c42368b`
- **参数名**: `SpiDataWidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [2..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is the width of a transmitted data unit.

########## 3. SpiDefaultData

- **UUID**: `ECUC:464acbf4-53a4-4964-843d-432be296ecb9`
- **参数名**: `SpiDefaultData`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The default data to be transmitted when (for internal buffer or external buffer) the pointer passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is NULL.

########## 4. SpiEbMaxLength

- **UUID**: `ECUC:202d39ab-4e1d-4eaa-a539-8a106e07b926`
- **参数名**: `SpiEbMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8190`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum size (number of data elements) of data buffers in case of EB Channels and only.

########## 5. SpiIbNBuffers

- **UUID**: `ECUC:4de36954-b7d2-4c48-9bd6-6e0196eba21a`
- **参数名**: `SpiIbNBuffers`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum number of data buffers in case of IB Channels and only.

######### ENUMERATION 类型参数

########## 1. SpiChannelType

- **UUID**: `ECUC:6b345ae6-4631-4cb8-af29-b9a20aeb6d8c`
- **参数名**: `SpiChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `EB`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EB` (来源: AUTOSAR_ECUC)
  - `IB` (来源: AUTOSAR_ECUC)
- **描述**: Buffer usage with EB/IB channel.

########## 2. SpiTransferStart

- **UUID**: `ECUC:c8e19a9c-9ff2-4b2d-8f31-5b59e7a65181`
- **参数名**: `SpiTransferStart`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LSB`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LSB` (来源: AUTOSAR_ECUC)
  - `MSB` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the first starting bit for transmission.

####### 2. SpiExternalDevice

**容器属性**:

- **UUID**: `ECUC:801f9c6a-fd4a-4d1b-a2f3-d9cf1d1145b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiExternalDevice`
- **多重性**: [1..1]

**容器描述**:

The communication settings of an external device. Closely linked to SpiJob.

######## 参数配置

此容器包含 **14** 个参数：

######### BOOLEAN 类型参数

########## 1. SpiEnableCs

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c4e`
- **参数名**: `SpiEnableCs`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables or not the Chip Select handling functions. If this parameter is enabled then parameter SpiCsSelection further details the type of chip selection.

########## 2. SpiAutoCalcBaudParams

- **UUID**: `d8a811c9-2c44-4532-b207-03e295103c7a`
- **参数名**: `SpiAutoCalcBaudParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables or not the automatic calculation of qspi baudrate parameters.  If this value is ON, then the Hw parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

########## 3. SpiAutoCalcDelayParams

- **UUID**: `d8a811c9-2c44-4532-b207-03e295123c7a`
- **参数名**: `SpiAutoCalcDelayParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables or not the automatic calculation of qspi Delay parameters.

######### FLOAT 类型参数

########## 1. SpiBaudrate

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3c448`
- **参数名**: `SpiBaudrate`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `640000.0`
- **取值范围**: [9600.0..3.3E7]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is the communication baudrate - This parameter allows

########## 2. SpiIdleTime

- **UUID**: `ce2120ab-166a-4676-891e-07d8bd1b7275`
- **参数名**: `SpiIdleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..0.098304]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: IDLEA / IDLEB Time .

########## 3. SpiTrailingTime

- **UUID**: `ce2120ab-166a-4676-891e-07d8bd1b7255`
- **参数名**: `SpiTrailingTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..0.098304]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Trailing Time - the time between the last edge of the clock and the CS De-assertion. It is also the time between the data elements in the SpiChannel

########## 4. SpiTimeClk2Cs

- **UUID**: `ECUC:756a5087-687e-43ae-8607-2470f7de9db7`
- **参数名**: `SpiTimeClk2Cs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..1.0E-4]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timing between clock and chip select (in seconds) or the Lead time - This parameter allows to use a range of values from 0 up to 0.0001 seconds.

######### STRING 类型参数

########## 1. SpiCsIdentifier

- **UUID**: `ECUC:af7c2eb8-32b9-40eb-b810-52c4dae7caf4`
- **参数名**: `SpiCsIdentifier`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `CHANNEL0`
- **描述**: This parameter is the symbolic name to identify the Chip Select (CS) allocated to this Job.

######### ENUMERATION 类型参数

########## 1. SpiCsPolarity

- **UUID**: `ECUC:07cb58ef-8a6f-4146-9ab5-380cb5de8918`
- **参数名**: `SpiCsPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the active polarity of Chip Select.

########## 2. SpiCsSelection

- **UUID**: `ECUC:6654d212-8ab8-41d7-8479-520af776eb1c`
- **参数名**: `SpiCsSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CS_VIA_PERIPHERAL_ENGINE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CS_VIA_GPIO` (来源: AUTOSAR_ECUC)
  - `CS_VIA_PERIPHERAL_ENGINE` (来源: AUTOSAR_ECUC)
- **描述**: When the Chip select handling is enabled (see SpiEnableCs), then this parameter specifies if the chip select is handled automatically by Peripheral HW engine or via general purpose IO by Spi driver.

########## 3. SpiDataShiftEdge

- **UUID**: `ECUC:3500cbba-2a1c-4073-873f-83083f11ce53`
- **参数名**: `SpiDataShiftEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LEADING`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LEADING` (来源: AUTOSAR_ECUC)
  - `TRAILING` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the SPI data shift edge.

########## 4. SpiHwUnit

- **UUID**: `ECUC:c9df357c-60ad-4f37-ac85-1c24c9fbacb7`
- **参数名**: `SpiHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `QSPI0`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `QSPI0` (来源: AUTOSAR_ECUC)
  - `QSPI1` (来源: AUTOSAR_ECUC)
  - `QSPI2` (来源: AUTOSAR_ECUC)
  - `QSPI3` (来源: AUTOSAR_ECUC)
  - `QSPI4` (来源: AUTOSAR_ECUC)
  - `QSPI5` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is the symbolic name to identify the HW SPI Hardware

########## 5. SpiShiftClockIdleLevel

- **UUID**: `ECUC:da746c64-de65-4db4-a5db-bcccb49f3c56`
- **参数名**: `SpiShiftClockIdleLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the SPI shift clock idle level.

########## 6. SpiParitySupport

- **UUID**: `d8a81ac9-2b44-4555-b207-03e295103c7b`
- **参数名**: `SpiParitySupport`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `UNUSED`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: INFINEON_AURIX2G)
  - `EVEN` (来源: INFINEON_AURIX2G)
  - `ODD` (来源: INFINEON_AURIX2G)
- **描述**: When the SpiParitySupport is selected SPI data Transmission/Reception incorporates an additional bit making the parity EVEN or ODD based on selection

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SpiCsGpio

**容器属性**:

- **UUID**: `DCE:d8394d8c-6029-69ac-b7ce-0b57c6a97003`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiCsGpio`
- **多重性**: [0..1]

**容器描述**:

Container for the selection of Chipselect

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SpiCsGpioPortSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiCsGpioPortSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..41]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port no used for Chipselect

############ 2. SpiCsGpioPinSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b21b30e`
- **参数名**: `SpiCsGpioPinSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port pin no used for Chipselect

######### 2. SpiBaudrateParams

**容器属性**:

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3f448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiBaudrateParams`
- **多重性**: [0..1]

**容器描述**:

This container has the parameters which are responsible for the Baudrate

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. SpiBaudParamTQ

- **UUID**: `993206b8-2a62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamTQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Global time quantum value, Qspi TQ Hw parameter. If SpiAutoCalcBaudParams value is ON, then the HW baudrate parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

############ 2. SpiBaudParamQ

- **UUID**: `993206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..63]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Qspi Q Hw parameter

############ 3. SpiBaudParamA

- **UUID**: `9a3206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines one of the bit segment A in a period, Qspi A Hw parameter

############ 4. SpiBaudParamB

- **UUID**: `9a3506b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamB`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi B Hw parameter

############ 5. SpiBaudParamC

- **UUID**: `9a3246b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi C Hw parameter

######### 3. SpiDelayParams

**容器属性**:

- **UUID**: `ce2120ab-166a-4686-891e-07d8bd1b7255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDelayParams`
- **多重性**: [0..1]

**容器描述**:

THis container has the parameters which are responsible for the delay configuration during transmission

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. SpiDelayParamTrailPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b14b30e`
- **参数名**: `SpiDelayParamTrailPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail delay prescalar Hw parameter

############ 2. SpiDelayParamTrailLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiDelayParamTrailLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail Hw parameter

############ 3. SpiDelayParamIdlePre

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b30e`
- **参数名**: `SpiDelayParamIdlePre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Idle delay prescalar Hw parameter

############ 4. SpiDelayParamIdleLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b31e`
- **参数名**: `SpiDelayParamIdleLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi IDLE delay Hw parameter

############ 5. SpiDelayParamLeadPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b11b30e`
- **参数名**: `SpiDelayParamLeadPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Lead delay prescalar Hw parameter

############ 6. SpiDelayParamLeadLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b21b31e`
- **参数名**: `SpiDelayParamLeadLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `7`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi LEAD delay Hw parameter

####### 3. SpiCsGpio

**容器属性**:

- **UUID**: `DCE:d8394d8c-6029-69ac-b7ce-0b57c6a97003`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiCsGpio`
- **多重性**: [0..1]

**容器描述**:

Container for the selection of Chipselect

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SpiCsGpioPortSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiCsGpioPortSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..41]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port no used for Chipselect

########## 2. SpiCsGpioPinSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b21b30e`
- **参数名**: `SpiCsGpioPinSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port pin no used for Chipselect

####### 4. SpiBaudrateParams

**容器属性**:

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3f448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiBaudrateParams`
- **多重性**: [0..1]

**容器描述**:

This container has the parameters which are responsible for the Baudrate

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SpiBaudParamTQ

- **UUID**: `993206b8-2a62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamTQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Global time quantum value, Qspi TQ Hw parameter. If SpiAutoCalcBaudParams value is ON, then the HW baudrate parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

########## 2. SpiBaudParamQ

- **UUID**: `993206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..63]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Qspi Q Hw parameter

########## 3. SpiBaudParamA

- **UUID**: `9a3206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines one of the bit segment A in a period, Qspi A Hw parameter

########## 4. SpiBaudParamB

- **UUID**: `9a3506b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamB`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi B Hw parameter

########## 5. SpiBaudParamC

- **UUID**: `9a3246b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi C Hw parameter

####### 5. SpiDelayParams

**容器属性**:

- **UUID**: `ce2120ab-166a-4686-891e-07d8bd1b7255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDelayParams`
- **多重性**: [0..1]

**容器描述**:

THis container has the parameters which are responsible for the delay configuration during transmission

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SpiDelayParamTrailPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b14b30e`
- **参数名**: `SpiDelayParamTrailPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail delay prescalar Hw parameter

########## 2. SpiDelayParamTrailLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiDelayParamTrailLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail Hw parameter

########## 3. SpiDelayParamIdlePre

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b30e`
- **参数名**: `SpiDelayParamIdlePre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Idle delay prescalar Hw parameter

########## 4. SpiDelayParamIdleLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b31e`
- **参数名**: `SpiDelayParamIdleLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi IDLE delay Hw parameter

########## 5. SpiDelayParamLeadPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b11b30e`
- **参数名**: `SpiDelayParamLeadPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Lead delay prescalar Hw parameter

########## 6. SpiDelayParamLeadLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b21b31e`
- **参数名**: `SpiDelayParamLeadLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `7`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi LEAD delay Hw parameter

####### 6. SpiJob

**容器属性**:

- **UUID**: `ECUC:02dff674-91c0-4b9a-a3a8-32619f35d54c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiJob`
- **多重性**: [1..65535]

**容器描述**:

All data needed to configure one SPI-Job, amongst others the connection between the internal SPI unit and the special settings for an external device is done.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SpiJobId

- **UUID**: `ECUC:3ea95b90-3a95-48b4-ab87-e0a8fe7221fd`
- **参数名**: `SpiJobId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..5000]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Job ID, used as parameter in SPI API functions.

########## 2. SpiJobPriority

- **UUID**: `ECUC:18823873-1f2a-4df0-a761-3c3a4540b359`
- **参数名**: `SpiJobPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority set accordingly to SPI093: 0, lowest, 3, highest priority

######### BOOLEAN 类型参数

########## 1. SpiFrameBasedCS

- **UUID**: `ECUC:a50f2a2c-5376-496e-a509-5073192fe0a6`
- **参数名**: `SpiFrameBasedCS`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: enable frame based chip select

######### ENUMERATION 类型参数

########## 1. SpiHwUnitSynchronous

- **UUID**: `ECUC:42dd7af3-c6e8-47f5-92f0-de2a43e78475`
- **参数名**: `SpiHwUnitSynchronous`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ASYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **描述**: If SpiHwUnitSynchronous is set to "SYNCHRONOUS", the SpiJob uses its containing SpiDriver in a synchronous manner. If it is set to "ASYNCHRONOUS", it uses the driver in an asynchronous way. If the parameter is not set, the SpiChannel uses the driver also in an asynchronous way.

######### FUNCTION-NAME 类型参数

########## 1. SpiJobEndNotification

- **UUID**: `ECUC:74518a4a-bc61-4898-915d-7deca2577064`
- **参数名**: `SpiJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiDeviceAssignment

- **UUID**: `ECUC:ffde9462-b41e-487a-8d62-d4940bae49b7`
- **引用名**: `SpiDeviceAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiExternalDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiExternalDevice`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the external device used by this job

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..1]

**容器描述**:

References to SPI channels and their order within the Job.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the order of Channels within the Job.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A job reference to a SPI channel.

####### 7. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..1]

**容器描述**:

References to SPI channels and their order within the Job.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the order of Channels within the Job.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A job reference to a SPI channel.

####### 8. SpiSequence

**容器属性**:

- **UUID**: `ECUC:3cb6ec10-7596-4a7e-9ee9-b08170958ddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiSequence`
- **多重性**: [1..255]

**容器描述**:

All data needed to configure one SPI-sequence

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SpiSequenceId

- **UUID**: `ECUC:2f5ec946-17d2-4d3b-aadc-f03cfc2d985c`
- **参数名**: `SpiSequenceId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Sequence ID, used as parameter in SPI API functions.

######### BOOLEAN 类型参数

########## 1. SpiInterruptibleSequence

- **UUID**: `ECUC:8f6b2ed8-3991-4bfe-bec5-cb279b9ca41d`
- **参数名**: `SpiInterruptibleSequence`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter allows or not this Sequence to be suspended by another one.

######### FUNCTION-NAME 类型参数

########## 1. SpiSeqEndNotification

- **UUID**: `ECUC:2e282067-fed0-4803-aa66-d641c71663e7`
- **参数名**: `SpiSeqEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiJobAssignment

- **UUID**: `ECUC:d88727e5-d5c4-4148-adeb-aab0bef83355`
- **引用名**: `SpiJobAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiJob`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A sequence references several jobs, which are executed during a communication sequence

##### 3. SpiChannel

**容器属性**:

- **UUID**: `ECUC:f2748179-dbc5-4754-b29d-73ae022425e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannel`
- **多重性**: [1..255]

**容器描述**:

All data needed to configure one SPI-channel

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelId

- **UUID**: `ECUC:57cf4873-901e-44b3-8e63-0c4280de938d`
- **参数名**: `SpiChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Channel ID, used as parameter in SPI API functions. It is published in the Spi_Cfg.h file

######## 2. SpiDataWidth

- **UUID**: `ECUC:1aa15934-fb17-437e-9366-be307c42368b`
- **参数名**: `SpiDataWidth`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8`
- **取值范围**: [2..32]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is the width of a transmitted data unit.

######## 3. SpiDefaultData

- **UUID**: `ECUC:464acbf4-53a4-4964-843d-432be296ecb9`
- **参数名**: `SpiDefaultData`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The default data to be transmitted when (for internal buffer or external buffer) the pointer passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is NULL.

######## 4. SpiEbMaxLength

- **UUID**: `ECUC:202d39ab-4e1d-4eaa-a539-8a106e07b926`
- **参数名**: `SpiEbMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `8190`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum size (number of data elements) of data buffers in case of EB Channels and only.

######## 5. SpiIbNBuffers

- **UUID**: `ECUC:4de36954-b7d2-4c48-9bd6-6e0196eba21a`
- **参数名**: `SpiIbNBuffers`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the maximum number of data buffers in case of IB Channels and only.

####### ENUMERATION 类型参数

######## 1. SpiChannelType

- **UUID**: `ECUC:6b345ae6-4631-4cb8-af29-b9a20aeb6d8c`
- **参数名**: `SpiChannelType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `EB`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EB` (来源: AUTOSAR_ECUC)
  - `IB` (来源: AUTOSAR_ECUC)
- **描述**: Buffer usage with EB/IB channel.

######## 2. SpiTransferStart

- **UUID**: `ECUC:c8e19a9c-9ff2-4b2d-8f31-5b59e7a65181`
- **参数名**: `SpiTransferStart`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LSB`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LSB` (来源: AUTOSAR_ECUC)
  - `MSB` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the first starting bit for transmission.

##### 4. SpiExternalDevice

**容器属性**:

- **UUID**: `ECUC:801f9c6a-fd4a-4d1b-a2f3-d9cf1d1145b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiExternalDevice`
- **多重性**: [1..1]

**容器描述**:

The communication settings of an external device. Closely linked to SpiJob.

###### 参数配置

此容器包含 **14** 个参数：

####### BOOLEAN 类型参数

######## 1. SpiEnableCs

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c4e`
- **参数名**: `SpiEnableCs`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables or not the Chip Select handling functions. If this parameter is enabled then parameter SpiCsSelection further details the type of chip selection.

######## 2. SpiAutoCalcBaudParams

- **UUID**: `d8a811c9-2c44-4532-b207-03e295103c7a`
- **参数名**: `SpiAutoCalcBaudParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables or not the automatic calculation of qspi baudrate parameters.  If this value is ON, then the Hw parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

######## 3. SpiAutoCalcDelayParams

- **UUID**: `d8a811c9-2c44-4532-b207-03e295123c7a`
- **参数名**: `SpiAutoCalcDelayParams`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables or not the automatic calculation of qspi Delay parameters.

####### FLOAT 类型参数

######## 1. SpiBaudrate

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3c448`
- **参数名**: `SpiBaudrate`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `640000.0`
- **取值范围**: [9600.0..3.3E7]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is the communication baudrate - This parameter allows

######## 2. SpiIdleTime

- **UUID**: `ce2120ab-166a-4676-891e-07d8bd1b7275`
- **参数名**: `SpiIdleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..0.098304]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: IDLEA / IDLEB Time .

######## 3. SpiTrailingTime

- **UUID**: `ce2120ab-166a-4676-891e-07d8bd1b7255`
- **参数名**: `SpiTrailingTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..0.098304]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Trailing Time - the time between the last edge of the clock and the CS De-assertion. It is also the time between the data elements in the SpiChannel

######## 4. SpiTimeClk2Cs

- **UUID**: `ECUC:756a5087-687e-43ae-8607-2470f7de9db7`
- **参数名**: `SpiTimeClk2Cs`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.0000001`
- **取值范围**: [4.0E-8..1.0E-4]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timing between clock and chip select (in seconds) or the Lead time - This parameter allows to use a range of values from 0 up to 0.0001 seconds.

####### STRING 类型参数

######## 1. SpiCsIdentifier

- **UUID**: `ECUC:af7c2eb8-32b9-40eb-b810-52c4dae7caf4`
- **参数名**: `SpiCsIdentifier`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `CHANNEL0`
- **描述**: This parameter is the symbolic name to identify the Chip Select (CS) allocated to this Job.

####### ENUMERATION 类型参数

######## 1. SpiCsPolarity

- **UUID**: `ECUC:07cb58ef-8a6f-4146-9ab5-380cb5de8918`
- **参数名**: `SpiCsPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the active polarity of Chip Select.

######## 2. SpiCsSelection

- **UUID**: `ECUC:6654d212-8ab8-41d7-8479-520af776eb1c`
- **参数名**: `SpiCsSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CS_VIA_PERIPHERAL_ENGINE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CS_VIA_GPIO` (来源: AUTOSAR_ECUC)
  - `CS_VIA_PERIPHERAL_ENGINE` (来源: AUTOSAR_ECUC)
- **描述**: When the Chip select handling is enabled (see SpiEnableCs), then this parameter specifies if the chip select is handled automatically by Peripheral HW engine or via general purpose IO by Spi driver.

######## 3. SpiDataShiftEdge

- **UUID**: `ECUC:3500cbba-2a1c-4073-873f-83083f11ce53`
- **参数名**: `SpiDataShiftEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LEADING`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LEADING` (来源: AUTOSAR_ECUC)
  - `TRAILING` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the SPI data shift edge.

######## 4. SpiHwUnit

- **UUID**: `ECUC:c9df357c-60ad-4f37-ac85-1c24c9fbacb7`
- **参数名**: `SpiHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `QSPI0`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `QSPI0` (来源: AUTOSAR_ECUC)
  - `QSPI1` (来源: AUTOSAR_ECUC)
  - `QSPI2` (来源: AUTOSAR_ECUC)
  - `QSPI3` (来源: AUTOSAR_ECUC)
  - `QSPI4` (来源: AUTOSAR_ECUC)
  - `QSPI5` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is the symbolic name to identify the HW SPI Hardware

######## 5. SpiShiftClockIdleLevel

- **UUID**: `ECUC:da746c64-de65-4db4-a5db-bcccb49f3c56`
- **参数名**: `SpiShiftClockIdleLevel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `HIGH` (来源: AUTOSAR_ECUC)
  - `LOW` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the SPI shift clock idle level.

######## 6. SpiParitySupport

- **UUID**: `d8a81ac9-2b44-4555-b207-03e295103c7b`
- **参数名**: `SpiParitySupport`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `UNUSED`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: INFINEON_AURIX2G)
  - `EVEN` (来源: INFINEON_AURIX2G)
  - `ODD` (来源: INFINEON_AURIX2G)
- **描述**: When the SpiParitySupport is selected SPI data Transmission/Reception incorporates an additional bit making the parity EVEN or ODD based on selection

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SpiCsGpio

**容器属性**:

- **UUID**: `DCE:d8394d8c-6029-69ac-b7ce-0b57c6a97003`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiCsGpio`
- **多重性**: [0..1]

**容器描述**:

Container for the selection of Chipselect

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SpiCsGpioPortSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiCsGpioPortSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..41]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port no used for Chipselect

########## 2. SpiCsGpioPinSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b21b30e`
- **参数名**: `SpiCsGpioPinSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port pin no used for Chipselect

####### 2. SpiBaudrateParams

**容器属性**:

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3f448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiBaudrateParams`
- **多重性**: [0..1]

**容器描述**:

This container has the parameters which are responsible for the Baudrate

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. SpiBaudParamTQ

- **UUID**: `993206b8-2a62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamTQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Global time quantum value, Qspi TQ Hw parameter. If SpiAutoCalcBaudParams value is ON, then the HW baudrate parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

########## 2. SpiBaudParamQ

- **UUID**: `993206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..63]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Qspi Q Hw parameter

########## 3. SpiBaudParamA

- **UUID**: `9a3206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines one of the bit segment A in a period, Qspi A Hw parameter

########## 4. SpiBaudParamB

- **UUID**: `9a3506b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamB`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi B Hw parameter

########## 5. SpiBaudParamC

- **UUID**: `9a3246b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi C Hw parameter

####### 3. SpiDelayParams

**容器属性**:

- **UUID**: `ce2120ab-166a-4686-891e-07d8bd1b7255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDelayParams`
- **多重性**: [0..1]

**容器描述**:

THis container has the parameters which are responsible for the delay configuration during transmission

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SpiDelayParamTrailPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b14b30e`
- **参数名**: `SpiDelayParamTrailPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail delay prescalar Hw parameter

########## 2. SpiDelayParamTrailLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiDelayParamTrailLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail Hw parameter

########## 3. SpiDelayParamIdlePre

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b30e`
- **参数名**: `SpiDelayParamIdlePre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Idle delay prescalar Hw parameter

########## 4. SpiDelayParamIdleLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b31e`
- **参数名**: `SpiDelayParamIdleLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi IDLE delay Hw parameter

########## 5. SpiDelayParamLeadPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b11b30e`
- **参数名**: `SpiDelayParamLeadPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Lead delay prescalar Hw parameter

########## 6. SpiDelayParamLeadLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b21b31e`
- **参数名**: `SpiDelayParamLeadLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `7`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi LEAD delay Hw parameter

##### 5. SpiCsGpio

**容器属性**:

- **UUID**: `DCE:d8394d8c-6029-69ac-b7ce-0b57c6a97003`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiCsGpio`
- **多重性**: [0..1]

**容器描述**:

Container for the selection of Chipselect

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SpiCsGpioPortSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiCsGpioPortSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..41]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port no used for Chipselect

######## 2. SpiCsGpioPinSelection

- **UUID**: `9a3246b8-2b22-4b16-9364-c89f3b21b30e`
- **参数名**: `SpiCsGpioPinSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..15]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Gpio port pin no used for Chipselect

##### 6. SpiBaudrateParams

**容器属性**:

- **UUID**: `ECUC:f1768d73-9a2c-4e95-aeda-d9f3b0f3f448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiBaudrateParams`
- **多重性**: [0..1]

**容器描述**:

This container has the parameters which are responsible for the Baudrate

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SpiBaudParamTQ

- **UUID**: `993206b8-2a62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamTQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Global time quantum value, Qspi TQ Hw parameter. If SpiAutoCalcBaudParams value is ON, then the HW baudrate parameters TQ,Q,A,B,C are calculated based on SpiBaudrate

######## 2. SpiBaudParamQ

- **UUID**: `993206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamQ`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..63]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines Qspi Q Hw parameter

######## 3. SpiBaudParamA

- **UUID**: `9a3206b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter defines one of the bit segment A in a period, Qspi A Hw parameter

######## 4. SpiBaudParamB

- **UUID**: `9a3506b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamB`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi B Hw parameter

######## 5. SpiBaudParamC

- **UUID**: `9a3246b8-2b62-4b16-9314-c89f3b01b30e`
- **参数名**: `SpiBaudParamC`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..3]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi C Hw parameter

##### 7. SpiDelayParams

**容器属性**:

- **UUID**: `ce2120ab-166a-4686-891e-07d8bd1b7255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiDelayParams`
- **多重性**: [0..1]

**容器描述**:

THis container has the parameters which are responsible for the delay configuration during transmission

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SpiDelayParamTrailPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b14b30e`
- **参数名**: `SpiDelayParamTrailPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail delay prescalar Hw parameter

######## 2. SpiDelayParamTrailLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b01b30e`
- **参数名**: `SpiDelayParamTrailLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Trail Hw parameter

######## 3. SpiDelayParamIdlePre

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b30e`
- **参数名**: `SpiDelayParamIdlePre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Idle delay prescalar Hw parameter

######## 4. SpiDelayParamIdleLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b11b31e`
- **参数名**: `SpiDelayParamIdleLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi IDLE delay Hw parameter

######## 5. SpiDelayParamLeadPre

- **UUID**: `9a3246b8-2b62-4b16-9384-c89f3b11b30e`
- **参数名**: `SpiDelayParamLeadPre`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi Lead delay prescalar Hw parameter

######## 6. SpiDelayParamLeadLength

- **UUID**: `9a3246b8-2b62-4b16-9364-c89f3b21b31e`
- **参数名**: `SpiDelayParamLeadLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `7`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Qspi LEAD delay Hw parameter

##### 8. SpiJob

**容器属性**:

- **UUID**: `ECUC:02dff674-91c0-4b9a-a3a8-32619f35d54c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiJob`
- **多重性**: [1..65535]

**容器描述**:

All data needed to configure one SPI-Job, amongst others the connection between the internal SPI unit and the special settings for an external device is done.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. SpiJobId

- **UUID**: `ECUC:3ea95b90-3a95-48b4-ab87-e0a8fe7221fd`
- **参数名**: `SpiJobId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..5000]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Job ID, used as parameter in SPI API functions.

######## 2. SpiJobPriority

- **UUID**: `ECUC:18823873-1f2a-4df0-a761-3c3a4540b359`
- **参数名**: `SpiJobPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority set accordingly to SPI093: 0, lowest, 3, highest priority

####### BOOLEAN 类型参数

######## 1. SpiFrameBasedCS

- **UUID**: `ECUC:a50f2a2c-5376-496e-a509-5073192fe0a6`
- **参数名**: `SpiFrameBasedCS`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: enable frame based chip select

####### ENUMERATION 类型参数

######## 1. SpiHwUnitSynchronous

- **UUID**: `ECUC:42dd7af3-c6e8-47f5-92f0-de2a43e78475`
- **参数名**: `SpiHwUnitSynchronous`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ASYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **描述**: If SpiHwUnitSynchronous is set to "SYNCHRONOUS", the SpiJob uses its containing SpiDriver in a synchronous manner. If it is set to "ASYNCHRONOUS", it uses the driver in an asynchronous way. If the parameter is not set, the SpiChannel uses the driver also in an asynchronous way.

####### FUNCTION-NAME 类型参数

######## 1. SpiJobEndNotification

- **UUID**: `ECUC:74518a4a-bc61-4898-915d-7deca2577064`
- **参数名**: `SpiJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiDeviceAssignment

- **UUID**: `ECUC:ffde9462-b41e-487a-8d62-d4940bae49b7`
- **引用名**: `SpiDeviceAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiExternalDevice`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiExternalDevice`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the external device used by this job

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..1]

**容器描述**:

References to SPI channels and their order within the Job.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the order of Channels within the Job.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A job reference to a SPI channel.

##### 9. SpiChannelList

**容器属性**:

- **UUID**: `ECUC:ab2edd79-9273-437e-a4a1-61b8a5b3813c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiChannelList`
- **多重性**: [1..1]

**容器描述**:

References to SPI channels and their order within the Job.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelIndex

- **UUID**: `ECUC:3bcaf670-2b2d-489f-aea5-9799fdf9c2c3`
- **参数名**: `SpiChannelIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the order of Channels within the Job.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiChannelAssignment

- **UUID**: `ECUC:58235e11-5f21-4c3a-a9da-696b588bac80`
- **引用名**: `SpiChannelAssignment`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A job reference to a SPI channel.

##### 10. SpiSequence

**容器属性**:

- **UUID**: `ECUC:3cb6ec10-7596-4a7e-9ee9-b08170958ddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiSequence`
- **多重性**: [1..255]

**容器描述**:

All data needed to configure one SPI-sequence

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SpiSequenceId

- **UUID**: `ECUC:2f5ec946-17d2-4d3b-aadc-f03cfc2d985c`
- **参数名**: `SpiSequenceId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: SPI Sequence ID, used as parameter in SPI API functions.

####### BOOLEAN 类型参数

######## 1. SpiInterruptibleSequence

- **UUID**: `ECUC:8f6b2ed8-3991-4bfe-bec5-cb279b9ca41d`
- **参数名**: `SpiInterruptibleSequence`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter allows or not this Sequence to be suspended by another one.

####### FUNCTION-NAME 类型参数

######## 1. SpiSeqEndNotification

- **UUID**: `ECUC:2e282067-fed0-4803-aa66-d641c71663e7`
- **参数名**: `SpiSeqEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter is a reference to a notification function.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SpiJobAssignment

- **UUID**: `ECUC:d88727e5-d5c4-4148-adeb-aab0bef83355`
- **引用名**: `SpiJobAssignment`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiJob`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: A sequence references several jobs, which are executed during a communication sequence

##### 11. SpiGeneral

**容器属性**:

- **UUID**: `ECUC:e8854824-b4c9-4618-aa5b-46efc092de25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiGeneral`
- **多重性**: [0..1]

**容器描述**:

General configuration settings for SPI-Handler

###### 参数配置

此容器包含 **17** 个参数：

####### INTEGER 类型参数

######## 1. SpiChannelBuffersAllowed

- **UUID**: `ECUC:0067ac2f-f0fd-40dc-9bd8-9e982207d046`
- **参数名**: `SpiChannelBuffersAllowed`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Selects the SPI Handler/Driver Channel Buffers usage 0 - IB (Internal Buffer), 1 - EB (External Buffer), 2 - Both

######## 2. SpiLevelDelivered

- **UUID**: `ECUC:f15843c0-09d6-43d4-8794-73a66d2c4505`
- **参数名**: `SpiLevelDelivered`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..2]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Selects the SPI Handler/Driver level of scalable functionality that is                            available and delivered.                            SpiLevelDelivered is 0(LEVEL0): The driver handles only simple synchronous transmission on all available SPI busses(QSPIx)                            SpiLevelDelivered is 1(LEVEL1): The driver handles only simple asynchronous transmission on all available SPI busses(QSPIx)                            SpiLevelDelivered is 2(LEVEL2): The LEVEL2 which is an enhanced behavior of the driver will handle both synchronous and asynchronous                            transmissions.

######## 3. SpiSyncTransmitTimeoutDuration

- **UUID**: `6da13a69-ebb2-42d3-abb2-b63e218cac9e`
- **参数名**: `SpiSyncTransmitTimeoutDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `65535`
- **取值范围**: [100..4294967295]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The parameter is used as timeout loop counter while waiting for data transmission/reception of 1 data element.

####### BOOLEAN 类型参数

######## 1. SpiCancelApi

- **UUID**: `ECUC:e2c6330e-7d7f-4d1c-b975-e46ef315e714`
- **参数名**: `SpiCancelApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Spi_Cancel function ON or OFF.

######## 2. SpiInitCheckApi

- **UUID**: `c6db7011-0bd1-49c5-b0dd-4a21ffd0a385`
- **参数名**: `SpiInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables init checks for APIs

######## 3. SpiMultiCoreErrorDetect

- **UUID**: `c6db7011-0bd1-49c5-b05d-4a21ffd0a385`
- **参数名**: `SpiMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter disables multicore configuration checks

######## 4. SpiDevErrorDetect

- **UUID**: `ECUC:a50f2a2c-5374-496e-a509-5073192fe0a5`
- **参数名**: `SpiDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 5. SpiSafetyEnable

- **UUID**: `ECUC:a50f2a2c-5374-496e-a509-5073192fe0a6`
- **参数名**: `SpiSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Default safety check for QSPI ON or OFF.

######## 6. SpiHwStatusApi

- **UUID**: `ECUC:4e6873dc-5c72-45d4-a49a-f37d8bad7f2b`
- **参数名**: `SpiHwStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Spi_GetHWUnitStatus function ON or OFF.

######## 7. SpiEnableLoopBackApi

- **UUID**: `ECUC:4e6873dc-5c72-46d4-a49a-f37d8bad7f2b`
- **参数名**: `SpiEnableLoopBackApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Spi_ControlLoopBack function ON or OFF.

######## 8. SpiInterruptibleSeqAllowed

- **UUID**: `ECUC:f010eb50-2a4e-4a75-ab18-1ab5413ac8ae`
- **参数名**: `SpiInterruptibleSeqAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Interruptible Sequences handling functionality ON or OFF.

######## 9. SpiSupportConcurrentSyncTransmit

- **UUID**: `ECUC:d38d155d-a5e5-4354-bc92-8f1e56f3fca1`
- **参数名**: `SpiSupportConcurrentSyncTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies whether concurrent Spi_SyncTransmit() calls for different sequences shall be configurable.

######## 10. SpiVersionInfoApi

- **UUID**: `ECUC:8629314a-5451-4737-a52a-3f967ae9aba8`
- **参数名**: `SpiVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Spi_GetVersionInfo function ON or OFF.

####### FLOAT 类型参数

######## 1. SpiMainFunctionPeriod

- **UUID**: `ECUC:e7157b90-1fd3-4067-8cb1-e5e01f6c482e`
- **参数名**: `SpiMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [1.0E-7..1.0]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the cycle time of the function Spi_MainFunction_Handling in seconds. The parameter is not used by the driver it self, but it is used by upper layer.

####### STRING 类型参数

######## 1. SpiUserCallbackHeaderFile

- **UUID**: `ECUC:aba4ab85-f272-4176-9ef8-77dae4986166`
- **参数名**: `SpiUserCallbackHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Spi_UserDefined_Cbk.h`
- **描述**: Header file name which will be included by the Spi. The value of this parameter shall be used as q-char-sequence according to ISO C90 section 6.10.2 "source file inclusion". The parameter value MUST NOT represent a path, since ISO C90 does not specify how such a path is treated (i.e., this is implementation defined (and additionally depends on the operating system and the underlying file system)).

####### ENUMERATION 类型参数

######## 1. SpiInitDeInitApiMode

- **UUID**: `c6db7011-0bd1-49c5-b0dd-4a21ffd0a185`
- **参数名**: `SpiInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SPI_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SPI_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `SPI_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for MCU initialization, de-initialization APIs

######## 2. SpiRuntimeApiMode

- **UUID**: `c6db7011-0ff1-49c5-b0dd-4a21ffd0a185`
- **参数名**: `SpiRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SPI_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SPI_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `SPI_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for SPI runtime APIs

##### 12. SpiHwConfiguration

**容器属性**:

- **UUID**: `ECUC:8627314a-5451-4737-a52a-3f967ae9aba8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container has the QSPI specific configuration which is PC type

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SpiHwConfigurationQspi

**容器属性**:

- **UUID**: `DCE:46354a81-d2f8-6a3d-9a0a-546962bdd901`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwConfigurationQspi`
- **多重性**: [1..6]

**容器描述**:

Container for the SpiHwConfigurationQspix

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SpiJobQueueLengthQspix

- **UUID**: `6da13a69-ebb2-42d3-abb2-b63e218cac91`
- **参数名**: `SpiJobQueueLengthQspix`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The parameter is used to specify the Job Queue size. The size should be chosen properly so as to accommodate the runtime Sequence transmission requests. Note: in SpiLevelDelivered = 2, if the HW is Synchronous, configuring this parameter should be ignored and default value could be kept.

########## 2. SpiSLSO0StrobeDelay

- **UUID**: `6da13a69-ebb2-42d3-abb2-b63e218cad91`
- **参数名**: `SpiSLSO0StrobeDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..31]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The parameter is used to specify the Strobe delay to be configured for SLSO0 in External Demultiplexer mode

######### BOOLEAN 类型参数

########## 1. SpiSleepEnableQspix

- **UUID**: `20398301-18ac-4596-83ef-b364ac76a8c1`
- **参数名**: `SpiSleepEnableQspix`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: To control QSPIx sleep mode

########## 2. SpiExternalDemux

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c5f`
- **参数名**: `SpiExternalDemux`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables/disables the external demultiplexer feature of QSPI HW

######### ENUMERATION 类型参数

########## 1. SpiHwConfigKernel

- **UUID**: `ECUC:af7c2eb8-52b9-40eb-b810-52c4daa7caf4`
- **参数名**: `SpiHwConfigKernel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `QSPI0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **可选值**:
  - `QSPI0` (来源: INFINEON_AURIX2G)
  - `QSPI1` (来源: INFINEON_AURIX2G)
  - `QSPI2` (来源: INFINEON_AURIX2G)
  - `QSPI3` (来源: INFINEON_AURIX2G)
  - `QSPI4` (来源: INFINEON_AURIX2G)
  - `QSPI5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is the symbolic name to identify the Kernel ID configuration

########## 2. SpiHWPinMRSTQspix

- **UUID**: `8cb2b502-2224-4dd2-917b-f73778ef1854`
- **参数名**: `SpiHWPinMRSTQspix`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `MRST0A_PORT20_PIN12`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `MRST0A_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `MRST0B_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `MRST0C_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `MRST1A_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST1B_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST2A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `MRST2B_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `MRST2CN_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST2CP_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST2D_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `MRST2E_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST2FN_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `MRST2FP_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `MRST3A_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `MRST3B_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `MRST3C_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `MRST4A_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `MRST4B_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST4CN_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST4CP_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST4DN_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `MRST4DP_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST5B_PORT14_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: Port Pin selection for Master_Receive_Slave_Transmit

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SpiHwDmaConfigurationQspi

**容器属性**:

- **UUID**: `DCE:d4d23ce0-5d7f-6675-8216-3ae14eb45983`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwDmaConfigurationQspi`
- **多重性**: [0..1]

**容器描述**:

Spi DMA Configuration For QSPI node

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SpiHwDmaChannelReceptionRef

- **UUID**: `083bfb84-a97f-421f-ad57-5bee661ea350`
- **引用名**: `SpiHwDmaChannelReceptionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI reception.

############ 2. SpiHwDmaChannelTransmissionRef

- **UUID**: `d27b20e2-b898-4d7a-bb7c-3833cb3dfbe4`
- **引用名**: `SpiHwDmaChannelTransmissionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI transmission.

####### 2. SpiHwDmaConfigurationQspi

**容器属性**:

- **UUID**: `DCE:d4d23ce0-5d7f-6675-8216-3ae14eb45983`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwDmaConfigurationQspi`
- **多重性**: [0..1]

**容器描述**:

Spi DMA Configuration For QSPI node

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SpiHwDmaChannelReceptionRef

- **UUID**: `083bfb84-a97f-421f-ad57-5bee661ea350`
- **引用名**: `SpiHwDmaChannelReceptionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI reception.

########## 2. SpiHwDmaChannelTransmissionRef

- **UUID**: `d27b20e2-b898-4d7a-bb7c-3833cb3dfbe4`
- **引用名**: `SpiHwDmaChannelTransmissionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI transmission.

##### 13. SpiHwConfigurationQspi

**容器属性**:

- **UUID**: `DCE:46354a81-d2f8-6a3d-9a0a-546962bdd901`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwConfigurationQspi`
- **多重性**: [1..6]

**容器描述**:

Container for the SpiHwConfigurationQspix

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SpiJobQueueLengthQspix

- **UUID**: `6da13a69-ebb2-42d3-abb2-b63e218cac91`
- **参数名**: `SpiJobQueueLengthQspix`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The parameter is used to specify the Job Queue size. The size should be chosen properly so as to accommodate the runtime Sequence transmission requests. Note: in SpiLevelDelivered = 2, if the HW is Synchronous, configuring this parameter should be ignored and default value could be kept.

######## 2. SpiSLSO0StrobeDelay

- **UUID**: `6da13a69-ebb2-42d3-abb2-b63e218cad91`
- **参数名**: `SpiSLSO0StrobeDelay`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [2..31]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The parameter is used to specify the Strobe delay to be configured for SLSO0 in External Demultiplexer mode

####### BOOLEAN 类型参数

######## 1. SpiSleepEnableQspix

- **UUID**: `20398301-18ac-4596-83ef-b364ac76a8c1`
- **参数名**: `SpiSleepEnableQspix`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: To control QSPIx sleep mode

######## 2. SpiExternalDemux

- **UUID**: `ECUC:914e2e80-7c97-4d1c-8546-1eaaefae8c5f`
- **参数名**: `SpiExternalDemux`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter enables/disables the external demultiplexer feature of QSPI HW

####### ENUMERATION 类型参数

######## 1. SpiHwConfigKernel

- **UUID**: `ECUC:af7c2eb8-52b9-40eb-b810-52c4daa7caf4`
- **参数名**: `SpiHwConfigKernel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `QSPI0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **可选值**:
  - `QSPI0` (来源: INFINEON_AURIX2G)
  - `QSPI1` (来源: INFINEON_AURIX2G)
  - `QSPI2` (来源: INFINEON_AURIX2G)
  - `QSPI3` (来源: INFINEON_AURIX2G)
  - `QSPI4` (来源: INFINEON_AURIX2G)
  - `QSPI5` (来源: INFINEON_AURIX2G)
- **描述**: This parameter is the symbolic name to identify the Kernel ID configuration

######## 2. SpiHWPinMRSTQspix

- **UUID**: `8cb2b502-2224-4dd2-917b-f73778ef1854`
- **参数名**: `SpiHWPinMRSTQspix`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `MRST0A_PORT20_PIN12`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `MRST0A_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `MRST0B_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `MRST0C_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `MRST1A_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST1B_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST2A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `MRST2B_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `MRST2CN_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST2CP_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST2D_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `MRST2E_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST2FN_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `MRST2FP_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `MRST3A_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `MRST3B_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `MRST3C_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `MRST4A_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `MRST4B_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST4CN_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `MRST4CP_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `MRST4DN_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `MRST4DP_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `MRST5B_PORT14_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: Port Pin selection for Master_Receive_Slave_Transmit

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SpiHwDmaConfigurationQspi

**容器属性**:

- **UUID**: `DCE:d4d23ce0-5d7f-6675-8216-3ae14eb45983`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwDmaConfigurationQspi`
- **多重性**: [0..1]

**容器描述**:

Spi DMA Configuration For QSPI node

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SpiHwDmaChannelReceptionRef

- **UUID**: `083bfb84-a97f-421f-ad57-5bee661ea350`
- **引用名**: `SpiHwDmaChannelReceptionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI reception.

########## 2. SpiHwDmaChannelTransmissionRef

- **UUID**: `d27b20e2-b898-4d7a-bb7c-3833cb3dfbe4`
- **引用名**: `SpiHwDmaChannelTransmissionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI transmission.

##### 14. SpiHwDmaConfigurationQspi

**容器属性**:

- **UUID**: `DCE:d4d23ce0-5d7f-6675-8216-3ae14eb45983`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiHwDmaConfigurationQspi`
- **多重性**: [0..1]

**容器描述**:

Spi DMA Configuration For QSPI node

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SpiHwDmaChannelReceptionRef

- **UUID**: `083bfb84-a97f-421f-ad57-5bee661ea350`
- **引用名**: `SpiHwDmaChannelReceptionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI reception.

######## 2. SpiHwDmaChannelTransmissionRef

- **UUID**: `d27b20e2-b898-4d7a-bb7c-3833cb3dfbe4`
- **引用名**: `SpiHwDmaChannelTransmissionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DmaChannelConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Dma/DmaChannelConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refer DMA channel configuration in MCU. Used for SPI transmission.

##### 15. SpiPublishedInformation

**容器属性**:

- **UUID**: `ECUC:ab74629f-37d4-453b-b708-5dc31fe4fe2f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SpiPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Container holding all SPI specific published information parameters

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SpiMaxHwUnit

- **UUID**: `ECUC:3e514982-2194-4b74-8c2e-baa2b264704d`
- **参数名**: `SpiMaxHwUnit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `6`
- **取值范围**: [0..6]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of different SPI hardware microcontroller peripherals (units/busses) available and handled by this SPI Handler/Driver module.

##### 16. CommonPublishedInformation

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
- **默认值**: `83`
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
- **描述**: Aurix2G derivative used for the implementation

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

1. **Spi**
