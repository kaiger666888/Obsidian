# Wdg - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:03

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Wdg](#wdg)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Wdg

#### 基本信息

- **UUID**: `428d8310-83eb-4499-a76f-9aebe7413581`
- **模块名称**: `Wdg`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Wdg (Watchdog driver) module.

#### 版本历史

共有 **11** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2016-02-05T05:08:10+01:00
- **发布者**: virmid

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2016-02-05T05:09:23+01:00
- **发布者**: virmid

*此版本无详细变更记录*

##### 3. 版本 1.00.02

- **状态**: released
- **发布日期**: 2016-02-05T05:09:35+01:00
- **发布者**: virmid

*此版本无详细变更记录*

##### 4. 版本 1.00.03

- **状态**: released
- **发布日期**: 2016-02-05T05:09:55+01:00
- **发布者**: virmid

*此版本无详细变更记录*

##### 5. 版本 2.00.00

- **发布日期**: 2016-02-05T05:10:00+01:00
- **发布者**: virmid

**变更内容**:

##### 6. 版本 2.01.00

- **发布日期**: 2016-05-02T02:38:22+02:00
- **发布者**: virmid

**变更内容**:

##### 7. 版本 2.02.00

- **状态**: released
- **发布日期**: 2020-10-02T13:45:10+02:00
- **发布者**: virzln

**变更内容**:

##### 8. 版本 2.02.01

- **状态**: released
- **发布日期**: 2020-10-29T15:01:43+01:00
- **发布者**: virskl

**变更内容**:

##### 9. 版本 2.02.02

- **状态**: released
- **发布日期**: 2023-10-30T09:15:22+01:00
- **发布者**: rwerhahn

**变更内容**:

##### 10. 版本 2.02.03

- **状态**: released
- **发布日期**: 2024-02-21T14:55:22+01:00
- **发布者**: makstaller

**变更内容**:

##### 11. 版本 2.02.04

- **发布日期**: 2024-05-21T13:06:19+02:00
- **发布者**: mneudecker

**变更内容**:

#### 配置容器

本模块包含 **10** 个配置容器：

##### 1. WdgDemEventParameterRefs

**容器属性**:

- **UUID**: `41738582-4d18-4991-89a4-1b99a53f7b1d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgDemEventParameterRefs`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **2** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WDG_E_DISABLE_REJECTED

- **UUID**: `87f4196b-0ec8-41f7-817c-503f80f2c02f`
- **引用名**: `WDG_E_DISABLE_REJECTED`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization or mode switch failed because it would disable the watchdog" has occurred.

######## 2. WDG_E_MODE_FAILED

- **UUID**: `caf65aaa-71d0-4d56-99a1-8e387e78700c`
- **引用名**: `WDG_E_MODE_FAILED`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
  - `/AUTOSAR/Dem/DemConfigSet/DemEventParameter`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Setting a watchdog mode failed (during initialization or mode switch)" has occurred.

##### 2. WdgGeneral

**容器属性**:

- **UUID**: `8a4d86cc-ed7f-4aa9-9078-71385f88f6c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

All general parameters of the watchdog driver are collected here.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. WdgIndex

- **UUID**: `633b594a-0efc-4351-b5f4-f173daac5dd8`
- **参数名**: `WdgIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Represents the watchdog driver's ID so that it can be referenced by the watchdog interface.

####### BOOLEAN 类型参数

######## 1. WdgDevErrorDetect

- **UUID**: `8800850d-f073-480a-9164-7f5bed56d530`
- **参数名**: `WdgDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable / disable development error detection for this module.

######## 2. WdgDisableAllowed

- **UUID**: `4efbcfa5-d4d9-4b69-82f9-10d4abed3188`
- **参数名**: `WdgDisableAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to allow / forbid disabling the watchdog driver during runtime.

######## 3. WdgVersionInfoApi

- **UUID**: `d62b5d00-165d-4ad8-9cf8-30b004527ef0`
- **参数名**: `WdgVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable / disable the version information API

######## 4. WdgSafeBswChecks

- **UUID**: `64e7a97c-c8de-4e66-accb-3a8e891225cb`
- **参数名**: `WdgSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used.

These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. WdgInitialTimeout

- **UUID**: `1189506a-8b14-4ca8-a9e6-b6841cd54bdd`
- **参数名**: `WdgInitialTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial timeout (sec) for the trigger condition to be initialized during Init function. It shall be not larger than WdgMaxTimeout.

######## 2. WdgMaxTimeout

- **UUID**: `478ceb5f-b44b-4e6d-b6b5-55f748074bbd`
- **参数名**: `WdgMaxTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum timeout (sec) to which the watchdog trigger condition can be initialized.

####### STRING 类型参数

######## 1. WdgUserConfigFile

- **UUID**: `4f320e16-af66-4b8d-b975-1f1f49b9b042`
- **参数名**: `WdgUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external text file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. WdgRunArea

- **UUID**: `41650ede-da87-4eed-8200-bc88fad18cb5`
- **参数名**: `WdgRunArea`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `RAM` (来源: AUTOSAR_ECUC)
  - `ROM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.

Represents the watchdog driver execution area is either from ROM(Flash) or RAM as required with the particular microcontroller.

####### FUNCTION-NAME 类型参数

######## 1. WdgTriggerLocation

- **UUID**: `7a2ec91e-33df-4148-b4b4-c4a334320f1d`
- **参数名**: `WdgTriggerLocation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Sbc_Wdg_Trigger`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Location (memory address) of the watchdog trigger routine.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgSbcRef

- **UUID**: `911561b9-5072-4f46-8de4-76860c212d5c`
- **引用名**: `WdgSbcRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/Sbc/Sbc/SbcDevice/SbcWatchdogPeripheral`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to SbcDevice

##### 3. WdgPublishedInformation

**容器属性**:

- **UUID**: `a838f3e9-deab-40ec-af1b-01c49c320d35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgPublishedInformation`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container holding all Wdg specific published information parameters

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. WdgOffModeSupported

- **UUID**: `4b6277c1-7cc0-4a16-9fcf-d66354b2ad5d`
- **参数名**: `WdgOffModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates if WDGIF_OFF_MODE is supported.

True: WDGIF_OFF_MODE is supported.
False: WDGIF_OFF_MODE is not supported.

######## 2. WdgSlowModeSupported

- **UUID**: `59cc8f87-daab-4bc0-82a9-545d5e0207c2`
- **参数名**: `WdgSlowModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates if WDGIF_SLOW_MODE is supported.

True: WDGIF_SLOW_MODE is supported.
False: WDGIF_SLOW_MODE is not supported.

######## 3. WdgFastModeSupported

- **UUID**: `a0bf6bb3-3aa1-469c-ac17-9622e569689b`
- **参数名**: `WdgFastModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates if WDGIF_FAST_MODE is supported.

True: WDGIF_FAST_MODE is supported.
False: WDGIF_FAST_MODE is not supported.

####### ENUMERATION 类型参数

######## 1. WdgTriggerMode

- **UUID**: `2a41b851-6cf0-4b47-ba17-768e6859b839`
- **参数名**: `WdgTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDG_BOTH` (来源: AUTOSAR_ECUC)
  - `WDG_TOGGLE` (来源: AUTOSAR_ECUC)
  - `WDG_WINDOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Watchdog trigger mode (toggle/window/both)

##### 4. WdgSettingsConfig

**容器属性**:

- **UUID**: `fdf23809-b68a-49f3-a749-d521ea6cc35a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Configuration items for the different watchdog settings, including those for external watchdog hardware.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. WdgDefaultMode

- **UUID**: `03bf83ba-7fec-4c87-b8f1-04f0026cce9b`
- **参数名**: `WdgDefaultMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default mode for watchdog driver initialization.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. WdgExternalConfiguration

**容器属性**:

- **UUID**: `04a3b4af-265e-4639-9607-6f16fe4a2c06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration items for an external watchdog hardware.

Not used.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. WdgExternalContainerRef

- **UUID**: `7dc2ced4-bcb0-4c71-bd64-65cf77eddc29`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.

Reference to either a DioChannelGroup or an SpiSequence.

####### 2. WdgSettingsFast

**容器属性**:

- **UUID**: `eec892fc-19f0-4d5a-a798-7fb87c032275`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "fast" mode.

####### 3. WdgSettingsOff

**容器属性**:

- **UUID**: `09db0060-cf25-495b-aff7-877395e7d734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

####### 4. WdgSettingsSlow

**容器属性**:

- **UUID**: `11f6ed77-aa42-4711-aa8b-2d0dfd312091`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

####### 5. WdgGptChannelParameterRef

**容器属性**:

- **UUID**: `44f51083-00fd-470a-9414-4fc2af4e2451`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgGptChannelParameterRef`
- **多重性**: [1..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. WdgTickValueMax

- **UUID**: `b47b2adc-e441-47e6-aee0-a1630aeb6042`
- **参数名**: `WdgTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

######### FLOAT 类型参数

########## 1. WdgTriggerTimerFreq

- **UUID**: `6bbb5759-7f52-45ed-b0da-489a504ddb64`
- **参数名**: `WdgTriggerTimerFreq`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [1..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of gpt channel reference WdgTriggerTimer in Hz

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. WdgTriggerTimer

- **UUID**: `d32ae747-6bdf-4686-8c0d-cd77f5cc40f8`
- **引用名**: `WdgTriggerTimer`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to GptChannel that is used to time watchdog triggering.

##### 5. WdgExternalConfiguration

**容器属性**:

- **UUID**: `04a3b4af-265e-4639-9607-6f16fe4a2c06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration items for an external watchdog hardware.

Not used.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgExternalContainerRef

- **UUID**: `7dc2ced4-bcb0-4c71-bd64-65cf77eddc29`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used.

Reference to either a DioChannelGroup or an SpiSequence.

##### 6. WdgSettingsFast

**容器属性**:

- **UUID**: `eec892fc-19f0-4d5a-a798-7fb87c032275`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "fast" mode.

##### 7. WdgSettingsOff

**容器属性**:

- **UUID**: `09db0060-cf25-495b-aff7-877395e7d734`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

##### 8. WdgSettingsSlow

**容器属性**:

- **UUID**: `11f6ed77-aa42-4711-aa8b-2d0dfd312091`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

##### 9. WdgGptChannelParameterRef

**容器属性**:

- **UUID**: `44f51083-00fd-470a-9414-4fc2af4e2451`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgGptChannelParameterRef`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. WdgTickValueMax

- **UUID**: `b47b2adc-e441-47e6-aee0-a1630aeb6042`
- **参数名**: `WdgTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

####### FLOAT 类型参数

######## 1. WdgTriggerTimerFreq

- **UUID**: `6bbb5759-7f52-45ed-b0da-489a504ddb64`
- **参数名**: `WdgTriggerTimerFreq`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [1..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of gpt channel reference WdgTriggerTimer in Hz

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgTriggerTimer

- **UUID**: `d32ae747-6bdf-4686-8c0d-cd77f5cc40f8`
- **引用名**: `WdgTriggerTimer`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
  - `/AUTOSAR/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to GptChannel that is used to time watchdog triggering.

##### 10. WdgAsr3Compatibility

**容器属性**:

- **UUID**: `9e168d3f-d0fa-42ce-9a8d-83c82f1307b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgAsr3Compatibility`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container to configure ASR3 compatibility

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. WdgTriggerTimeout

- **UUID**: `474ad7f7-3dd4-4142-b1a0-71afce89ef89`
- **参数名**: `WdgTriggerTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The timeout (sec) for the trigger condition to be set everytime when Wdg_Trigger is called.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Wdg_30_Sbc

- **UUID**: `23647588-f5d1-4744-b6fd-45982db4cb08`
- **包名称**: `Wdg_30_Sbc`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Wdg_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Wdg**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Wdg_Pre**
2. **Wdg_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Wdg_Impl

- **UUID**: `58986bf1-f41f-4377-bf56-fba0a50fc30b`
- **实现名称**: `Wdg_Impl`
- **编程语言**: C
- **软件版本**: 4.00.04
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Wdg_Pre

- **UUID**: `26f63182-33c5-4cb8-b5e9-53b2b3521243`
- **配置名称**: `Wdg_Pre`
- **定义引用**: `/MICROSAR/Wdg_30_Sbc/Wdg`

### 2. Wdg_Rec

- **UUID**: `07627711-326f-4dd6-a23e-a28a9151fa84`
- **配置名称**: `Wdg_Rec`
- **定义引用**: `/MICROSAR/Wdg_30_Sbc/Wdg`
