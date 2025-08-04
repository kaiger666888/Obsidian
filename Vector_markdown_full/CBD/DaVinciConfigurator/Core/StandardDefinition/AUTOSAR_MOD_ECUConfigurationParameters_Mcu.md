# Mcu - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:27

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Mcu](#mcu)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Mcu

#### 基本信息

- **UUID**: `ECUC:cd6efdb7-686d-48a9-80ec-f361585dcbc3`
- **模块名称**: `Mcu`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Mcu (Microcontroler Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. McuGeneralConfiguration

**容器属性**:

- **UUID**: `ECUC:0a0f46f3-25a3-4d80-bef0-2752b7304463`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuGeneralConfiguration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the MCU driver.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. McuDevErrorDetect

- **UUID**: `ECUC:a940168d-eeab-4151-a78e-381ce11c5706`
- **参数名**: `McuDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the development error detection and reporting.

######## 2. McuGetRamStateApi

- **UUID**: `ECUC:ea4753f1-1822-458f-a149-613e06cf9d75`
- **参数名**: `McuGetRamStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable/disable the API Mcu_GetRamState.

######## 3. McuInitClock

- **UUID**: `ECUC:3ad589e7-8c66-4cfc-b54f-f07908d45ea0`
- **参数名**: `McuInitClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to FALSE, the clock initialization has to be disabled from the MCU driver. This concept applies when there are some write once clock registers and a bootloader is present. If this parameter is set to TRUE, the MCU driver is responsible of the clock initialization.

######## 4. McuNoPll

- **UUID**: `ECUC:80005e5b-81c8-4254-9253-65722170a8d2`
- **参数名**: `McuNoPll`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be set True, if the H/W does not have a PLL or the PLL circuitry is enabled after the power on without S/W intervention. In this case MCU_DistributePllClock has to be disabled and  MCU_GetPllStatus has to return MCU_PLL_STATUS_UNDEFINED. Otherwise this parameters has to be set False

######## 5. McuPerformResetApi

- **UUID**: `ECUC:88316ee4-ac23-418d-a433-20ccecc20da2`
- **参数名**: `McuPerformResetApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the use of the function Mcu_PerformReset()

######## 6. McuVersionInfoApi

- **UUID**: `ECUC:c573aff5-6a13-491f-a869-7a125b7ca0e4`
- **参数名**: `McuVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

##### 2. McuModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:885e3d9d-b8f4-4142-98ae-050bd6d9c6ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuModuleConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration (parameters) of the MCU driver

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. McuNumberOfMcuModes

- **UUID**: `ECUC:a0e5878f-ad7b-4ec1-a4cf-26394deb5ac6`
- **参数名**: `McuNumberOfMcuModes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the number of Modes available for the MCU.

######## 2. McuRamSectors

- **UUID**: `ECUC:5c7ef78a-cb1b-4ea9-978f-f6c78cd8d738`
- **参数名**: `McuRamSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the number of RAM sectors available for the MCU.

######## 3. McuResetSetting

- **UUID**: `ECUC:8182a6cf-4323-418c-bb8c-277225bae6da`
- **参数名**: `McuResetSetting`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter relates to the MCU specific reset configuration. This applies to the function Mcu_PerformReset, which performs a microcontroller reset using the hardware feature of the microcontroller.

####### ENUMERATION 类型参数

######## 1. McuClockSrcFailureNotification

- **UUID**: `ECUC:303ee5f9-8122-452c-a715-a46983e7fe5e`
- **参数名**: `McuClockSrcFailureNotification`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DISABLED` (来源: AUTOSAR_ECUC)
  - `ENABLED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables clock failure notification. In case this feature is not supported by HW the setting should be disabled.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. McuClockSettingConfig

**容器属性**:

- **UUID**: `ECUC:f63efc1c-b907-462f-8bb7-4089e77f95f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockSettingConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the Clock settings of the MCU.  Please see MCU031 for more information on the MCU clock settings.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. McuClockSettingId

- **UUID**: `ECUC:d2d2ea3f-9a7b-4fbf-9e20-b87bd423a209`
- **参数名**: `McuClockSettingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Id of this McuClockSettingConfig to be used as argument for the API call "Mcu_InitClock".

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. McuClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:11433bf7-4c9a-4499-ba86-d4f2b6e3186e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines a reference point in the Mcu Clock tree. It defines the frequency which then can be used by other modules as an input value. Lower multiplictiy is 1, as even in the simpliest case (only one frequency is used), there is one frequency to be defined.

########## 参数配置

此容器包含 **1** 个参数：

########### FLOAT 类型参数

############ 1. McuClockReferencePointFrequency

- **UUID**: `ECUC:602fa1f9-cadd-4b16-9b2e-d9ef5c152f96`
- **参数名**: `McuClockReferencePointFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the frequency for the specific instance of the McuClockReferencePoint container. It shall be given in Hz.

####### 2. McuClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:11433bf7-4c9a-4499-ba86-d4f2b6e3186e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines a reference point in the Mcu Clock tree. It defines the frequency which then can be used by other modules as an input value. Lower multiplictiy is 1, as even in the simpliest case (only one frequency is used), there is one frequency to be defined.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. McuClockReferencePointFrequency

- **UUID**: `ECUC:602fa1f9-cadd-4b16-9b2e-d9ef5c152f96`
- **参数名**: `McuClockReferencePointFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the frequency for the specific instance of the McuClockReferencePoint container. It shall be given in Hz.

####### 3. McuDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4c697a37-02d8-42df-8696-0c9f592008c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. MCU_E_CLOCK_FAILURE

- **UUID**: `ECUC:66c8e900-6197-42a3-8e25-a695aa21788e`
- **引用名**: `MCU_E_CLOCK_FAILURE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Clock source failure".

####### 4. McuModeSettingConf

**容器属性**:

- **UUID**: `ECUC:32517397-6199-41a5-bfb1-6bebf9df26ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuModeSettingConf`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the Mode setting of the MCU.  Please see MCU035 for more information on the MCU mode settings.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. McuMode

- **UUID**: `ECUC:f0450b1d-51c7-4e23-9bd7-0488035ae777`
- **参数名**: `McuMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter represents the MCU Mode settings.

####### 5. McuRamSectorSettingConf

**容器属性**:

- **UUID**: `ECUC:067acd14-020b-4eaf-9597-b9c52b6fca43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuRamSectorSettingConf`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the RAM Sector setting. Please see MCU030 for more information on RAM sec-tor settings.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. McuRamDefaultValue

- **UUID**: `ECUC:e25b2477-20d6-43c4-8551-041fc23d8eeb`
- **参数名**: `McuRamDefaultValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Data pre-setting to be initialized

########## 2. McuRamSectionBaseAddress

- **UUID**: `ECUC:c24586f9-4f43-42cc-87fd-05fe91e91f5c`
- **参数名**: `McuRamSectionBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the MCU RAM section base address

########## 3. McuRamSectionSize

- **UUID**: `ECUC:7221c8a7-78ec-4cc3-8cfe-6c93010660cb`
- **参数名**: `McuRamSectionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter represents the MCU RAM Section size in bytes.

##### 3. McuClockSettingConfig

**容器属性**:

- **UUID**: `ECUC:f63efc1c-b907-462f-8bb7-4089e77f95f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockSettingConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the Clock settings of the MCU.  Please see MCU031 for more information on the MCU clock settings.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. McuClockSettingId

- **UUID**: `ECUC:d2d2ea3f-9a7b-4fbf-9e20-b87bd423a209`
- **参数名**: `McuClockSettingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The Id of this McuClockSettingConfig to be used as argument for the API call "Mcu_InitClock".

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. McuClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:11433bf7-4c9a-4499-ba86-d4f2b6e3186e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines a reference point in the Mcu Clock tree. It defines the frequency which then can be used by other modules as an input value. Lower multiplictiy is 1, as even in the simpliest case (only one frequency is used), there is one frequency to be defined.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. McuClockReferencePointFrequency

- **UUID**: `ECUC:602fa1f9-cadd-4b16-9b2e-d9ef5c152f96`
- **参数名**: `McuClockReferencePointFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the frequency for the specific instance of the McuClockReferencePoint container. It shall be given in Hz.

##### 4. McuClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:11433bf7-4c9a-4499-ba86-d4f2b6e3186e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container defines a reference point in the Mcu Clock tree. It defines the frequency which then can be used by other modules as an input value. Lower multiplictiy is 1, as even in the simpliest case (only one frequency is used), there is one frequency to be defined.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. McuClockReferencePointFrequency

- **UUID**: `ECUC:602fa1f9-cadd-4b16-9b2e-d9ef5c152f96`
- **参数名**: `McuClockReferencePointFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the frequency for the specific instance of the McuClockReferencePoint container. It shall be given in Hz.

##### 5. McuDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4c697a37-02d8-42df-8696-0c9f592008c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. MCU_E_CLOCK_FAILURE

- **UUID**: `ECUC:66c8e900-6197-42a3-8e25-a695aa21788e`
- **引用名**: `MCU_E_CLOCK_FAILURE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Clock source failure".

##### 6. McuModeSettingConf

**容器属性**:

- **UUID**: `ECUC:32517397-6199-41a5-bfb1-6bebf9df26ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuModeSettingConf`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the Mode setting of the MCU.  Please see MCU035 for more information on the MCU mode settings.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. McuMode

- **UUID**: `ECUC:f0450b1d-51c7-4e23-9bd7-0488035ae777`
- **参数名**: `McuMode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter represents the MCU Mode settings.

##### 7. McuRamSectorSettingConf

**容器属性**:

- **UUID**: `ECUC:067acd14-020b-4eaf-9597-b9c52b6fca43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuRamSectorSettingConf`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the RAM Sector setting. Please see MCU030 for more information on RAM sec-tor settings.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. McuRamDefaultValue

- **UUID**: `ECUC:e25b2477-20d6-43c4-8551-041fc23d8eeb`
- **参数名**: `McuRamDefaultValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the Data pre-setting to be initialized

######## 2. McuRamSectionBaseAddress

- **UUID**: `ECUC:c24586f9-4f43-42cc-87fd-05fe91e91f5c`
- **参数名**: `McuRamSectionBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall represent the MCU RAM section base address

######## 3. McuRamSectionSize

- **UUID**: `ECUC:7221c8a7-78ec-4cc3-8cfe-6c93010660cb`
- **参数名**: `McuRamSectionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter represents the MCU RAM Section size in bytes.

##### 8. McuPublishedInformation

**容器属性**:

- **UUID**: `ECUC:8051fc81-2a32-4e81-8e62-c3701213a9f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container holding all MCU specific published information parameters

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. McuResetReasonConf

**容器属性**:

- **UUID**: `ECUC:6dad17e9-21eb-47f5-a6c3-6ccc06977645`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuResetReasonConf`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the different type of reset reason that can be retrieved from Mcu_GetResetReason Api.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. McuResetReason

- **UUID**: `ECUC:8b8a721a-1726-4a04-8f61-da75604611b2`
- **参数名**: `McuResetReason`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: The parameter represents the different type of reset that a Micro supports. This parameter is referenced by the parameter EcuMResetReason in the ECU State manager module.

##### 9. McuResetReasonConf

**容器属性**:

- **UUID**: `ECUC:6dad17e9-21eb-47f5-a6c3-6ccc06977645`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `McuResetReasonConf`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the different type of reset reason that can be retrieved from Mcu_GetResetReason Api.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. McuResetReason

- **UUID**: `ECUC:8b8a721a-1726-4a04-8f61-da75604611b2`
- **参数名**: `McuResetReason`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: The parameter represents the different type of reset that a Micro supports. This parameter is referenced by the parameter EcuMResetReason in the ECU State manager module.

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

1. **Mcu**
