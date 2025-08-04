# Wdg - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:12

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Wdg](#wdg)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Wdg

#### 基本信息

- **UUID**: `ECUC:63541b2b-c94a-451e-abfe-cc1f96b6e723`
- **模块名称**: `Wdg`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Wdg (Watchdog driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **12** 个配置容器：

##### 1. WdgGeneral

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4981-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgGeneral`
- **多重性**: [0..1]

**容器描述**:

All general parameters of the watchdog driver are collected here.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. WdgIndex

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc1`
- **参数名**: `WdgIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Represents the watchdog driver's ID so that it can be referenced by the watchdog interface.

####### BOOLEAN 类型参数

######## 1. WdgDevErrorDetect

- **UUID**: `ECUC:286ff3be-9991-46b5-8518-85a9324954dd`
- **参数名**: `WdgDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. WdgSafetyEnable

- **UUID**: `ECUC:286ff3be-9991-46b5-8518-85a9324977ee`
- **参数名**: `WdgSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Safety Error detection and notification ON or OFF.

######## 3. WdgInitCheckApi

- **UUID**: `ECUC:286ff3be-9991-46b5-8518-85a9324788ff`
- **参数名**: `WdgInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Init Check API to ON or OFF.

######## 4. WdgDisableAllowed

- **UUID**: `ECUC:9ab89355-5ba4-4293-94b5-fb189cbcc2b2`
- **参数名**: `WdgDisableAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is disabled.                        Instead, WdgCPUDisableAllowed is provided to enable/disable CPU specific Wdg for every CPU Wdg configured.                        Compile switch to allow / forbid disabling the watchdog driver during runtime.

######## 5. WdgVersionInfoApi

- **UUID**: `ECUC:c8084b58-82da-4677-8381-3ed7b707dfdb`
- **参数名**: `WdgVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Compile switch to enable / disable the version information API

####### FLOAT 类型参数

######## 1. WdgInitialTimeout

- **UUID**: `ECUC:c20d7853-9f81-4e43-84e4-e8378cdc3ba4`
- **参数名**: `WdgInitialTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is disabled.                                   Instead, WdgCPUInitialTimeout is provided as initial timeout for every CPU Wdg configured.                                   This initial timeout (sec) for the trigger condition to be initialized during Init function. It shall be not larger than WdgMaxTimeout.

######## 2. WdgMaxTimeout

- **UUID**: `ECUC:fc6fa127-3b50-43b7-b660-6ee4ed01a755`
- **参数名**: `WdgMaxTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `32`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is disabled.                        Instead, WdgCPUMaxTimeout is provided as maximum CPU specific Wdg timeout for every CPU Wdg configured.                        The maximum timeout (sec) to which the watchdog trigger condition can be initialized.

####### ENUMERATION 类型参数

######## 1. WdgTriggerTimerSelection

- **UUID**: `ECUC:1df59d7c-8eb1-4ada-8bb0-1293237f6551`
- **参数名**: `WdgTriggerTimerSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `STM_TIMER`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_TIMER` (来源: INFINEON_AURIX2G)
  - `STM_TIMER` (来源: INFINEON_AURIX2G)
- **描述**: Hardware timer used to service WDG during STC window period.

######## 2. WdgRunArea

- **UUID**: `ECUC:1df59d7c-8eb1-4ada-8bb0-1293237f6550`
- **参数名**: `WdgRunArea`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ROM`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAM` (来源: AUTOSAR_ECUC)
  - `ROM` (来源: AUTOSAR_ECUC)
- **描述**: This feature is not provided by IFX.This parameter is disabled.                           Represents the watchdog driver execution area is either from ROM(Flash) or RAM as required with the particular microcontroller.

######## 3. WdgInitApiMode

- **UUID**: `c6db7011-0bd1-49c5-b0dd-4a21ffd0a185`
- **参数名**: `WdgInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `WDG_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `WDG_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `WDG_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for WDG initialization API.

######## 4. WdgRuntimeApiMode

- **UUID**: `c6db7011-0ff1-49c5-b0dd-4a21ffd0a185`
- **参数名**: `WdgRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `WDG_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `WDG_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
  - `WDG_MCAL_USER1` (来源: INFINEON_AURIX2G)
- **描述**: This parameter selects the operating modes for WDG runtime APIs

####### FUNCTION-NAME 类型参数

######## 1. WdgTriggerLocation

- **UUID**: `ECUC:18986e28-613e-472f-9099-6889c30148cb`
- **参数名**: `WdgTriggerLocation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: This feature is not provided by IFX.This parameter is disabled.Location (memory address) of the watchdog trigger routine.

##### 2. WdgSettingsConfig

**容器属性**:

- **UUID**: `ECUC:aa5bea66-87cc-4d25-8725-2f031a550397`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsConfig`
- **多重性**: [1..6]

**容器描述**:

Configuration items for the different watchdog settings, including those for external watchdog hardware.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. WdgCoreId

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc2`
- **参数名**: `WdgCoreId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..5]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: true
- **描述**: This parameter refers to CORE ID to which the watchdog settings belong

######## 2. WdgCPUInitialPassword

- **UUID**: `ECUC:fc6fa127-3b50-47b7-b770-6ee7ed01a777`
- **参数名**: `WdgCPUInitialPassword`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..16383]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Initial password for the password access.

####### BOOLEAN 类型参数

######## 1. WdgCPUDisableAllowed

- **UUID**: `ECUC:9ab89355-5bc4-4293-94b5-fb191cbcc2b2`
- **参数名**: `WdgCPUDisableAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Core specific switch to allow / forbid disabling the watchdog driver during runtime.

####### FLOAT 类型参数

######## 1. WdgCPUInitialTimeout

- **UUID**: `ECUC:c20d7853-9f81-4e43-85e5-e8378cdc3ba4`
- **参数名**: `WdgCPUInitialTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The initial timeout (sec) for the trigger condition to be initialized during Init function for a core. It shall be not larger than WdgMaxTimeout of the core.

######## 2. WdgCPUMaxTimeout

- **UUID**: `ECUC:fc6fa127-3b50-43b7-b770-6ee4ed01a755`
- **参数名**: `WdgCPUMaxTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `32`
- **取值范围**: [0.0..65.535]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The maximum timeout (sec) to which the watchdog trigger condition can be initialized for a core.

####### ENUMERATION 类型参数

######## 1. WdgDefaultMode

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc1f`
- **参数名**: `WdgDefaultMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `WDGIF_SLOW_MODE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **描述**: Default mode for watchdog driver initialization.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. WdgSystemClockRef

- **UUID**: `9ef075e8-51b4-4d4b-bb53-fc516d8f2b23`
- **引用名**: `WdgSystemClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter refers to the system clock configured using the Mcu_InitClock function.

This parameter should refer to a valid McuClockSetting Configuration (/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig)

Also the WDG module will work correctly only for this system clock setting. No changes should be done to the system clock if WDG is to be kept functioning.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. WdgExternalConfiguration

**容器属性**:

- **UUID**: `ECUC:d4132c73-7eee-4a7a-80a8-e3f6c256baca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]

**容器描述**:

This configuration is not provided as the external watchdog is not supported by IFX.Configuration items for an external watchdog hardware

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. WdgExternalContainerRef

- **UUID**: `ECUC:ece56c85-00e0-4720-bd8c-0d33665138c0`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **描述**: Reference to either

####### 2. WdgSettingsFast

**容器属性**:

- **UUID**: `ECUC:8b2ff9f0-4ec8-4fbb-9089-eff1c3aad425`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog drivers fast mode.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. WdgFastModeTimeoutValue

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc3`
- **参数名**: `WdgFastModeTimeoutValue`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.16777216]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Fast mode timeout in seconds for WDT

####### 3. WdgSettingsSlow

**容器属性**:

- **UUID**: `ECUC:82e6dd1d-aa7e-40af-b0db-7ff521f64749`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

######## 参数配置

此容器包含 **1** 个参数：

######### FLOAT 类型参数

########## 1. WdgSlowModeTimeoutValue

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc4`
- **参数名**: `WdgSlowModeTimeoutValue`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..10.73741824]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Slow mode timeout in seconds for WDT

####### 4. WdgSettingsOff

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

####### 5. WdgTriggerTimerSetting

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgTriggerTimerSetting`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM\STM hardware

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. WdgSlowRefreshTime

- **UUID**: `0c7609d5-0960-4a73-b682-2e9aadedfa1c`
- **参数名**: `WdgSlowRefreshTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.015`
- **取值范围**: [0.001..10.73741824]
- **来源**: INFINEON_AURIX2G
- **描述**: Slow mode Gtm/Stm callback period in seconds for WDT.

########## 2. WdgFastRefreshTime

- **UUID**: `0c7609d5-0960-4a73-b682-2e9aadedfa1d`
- **参数名**: `WdgFastRefreshTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.007`
- **取值范围**: [0.001..0.16777216]
- **来源**: INFINEON_AURIX2G
- **描述**: Fast mode Gtm/Stm callback period in seconds for WDT.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. GtmTimerConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM timer hardware.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 6. GtmTimerConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM timer hardware.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 7. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 3. WdgExternalConfiguration

**容器属性**:

- **UUID**: `ECUC:d4132c73-7eee-4a7a-80a8-e3f6c256baca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]

**容器描述**:

This configuration is not provided as the external watchdog is not supported by IFX.Configuration items for an external watchdog hardware

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgExternalContainerRef

- **UUID**: `ECUC:ece56c85-00e0-4720-bd8c-0d33665138c0`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **描述**: Reference to either

##### 4. WdgSettingsFast

**容器属性**:

- **UUID**: `ECUC:8b2ff9f0-4ec8-4fbb-9089-eff1c3aad425`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog drivers fast mode.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. WdgFastModeTimeoutValue

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc3`
- **参数名**: `WdgFastModeTimeoutValue`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.16777216]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Fast mode timeout in seconds for WDT

##### 5. WdgSettingsSlow

**容器属性**:

- **UUID**: `ECUC:82e6dd1d-aa7e-40af-b0db-7ff521f64749`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. WdgSlowModeTimeoutValue

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc4`
- **参数名**: `WdgSlowModeTimeoutValue`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..10.73741824]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Slow mode timeout in seconds for WDT

##### 6. WdgSettingsOff

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [0..1]

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

##### 7. WdgTriggerTimerSetting

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgTriggerTimerSetting`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM\STM hardware

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. WdgSlowRefreshTime

- **UUID**: `0c7609d5-0960-4a73-b682-2e9aadedfa1c`
- **参数名**: `WdgSlowRefreshTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.015`
- **取值范围**: [0.001..10.73741824]
- **来源**: INFINEON_AURIX2G
- **描述**: Slow mode Gtm/Stm callback period in seconds for WDT.

######## 2. WdgFastRefreshTime

- **UUID**: `0c7609d5-0960-4a73-b682-2e9aadedfa1d`
- **参数名**: `WdgFastRefreshTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.007`
- **取值范围**: [0.001..0.16777216]
- **来源**: INFINEON_AURIX2G
- **描述**: Fast mode Gtm/Stm callback period in seconds for WDT.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. GtmTimerConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM timer hardware.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 8. GtmTimerConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration elements for configuring GTM timer hardware.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 9. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TOM/ATOM channel Configuration for GTM.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. GtmTimerClockSelect

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc4e`
- **参数名**: `GtmTimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_FIXED_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_FIXED_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_FIXED_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for GTM timer.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTomAllocationConf/McuGtmTomChannelAllocationConf`
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmAtomAllocationConf/McuGtmAtomChannelAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 10. WdgDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WDG_E_DISABLE_REJECTED

- **UUID**: `ECUC:48a148f3-55ae-4fc2-9159-68566b6da4de`
- **引用名**: `WDG_E_DISABLE_REJECTED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization or mode switch failed because it would disable the watchdog" has occurred.

######## 2. WDG_E_MODE_FAILED

- **UUID**: `ECUC:8d2358b4-1d83-4c70-b73c-8700019f161f`
- **引用名**: `WDG_E_MODE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Setting a watchdog mode failed (during initialization or mode switch)" has occurred.

##### 11. WdgPublishedInformation

**容器属性**:

- **UUID**: `ECUC:a3ab7732-c7a9-4ecd-b346-5574a81f6562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Container holding all WDG specific published information parameters

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. WdgTriggerMode

- **UUID**: `ECUC:7b066c98-77c0-40de-868a-0410e014c775`
- **参数名**: `WdgTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `WDG_WINDOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDG_BOTH` (来源: AUTOSAR_ECUC)
  - `WDG_TOGGLE` (来源: AUTOSAR_ECUC)
  - `WDG_WINDOW` (来源: AUTOSAR_ECUC)
- **描述**: Watchdog trigger mode (toggle/window/both)

##### 12. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **10** 个参数：

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
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `102`
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

######## 2. VendorApiInfix

- **UUID**: `ad363b41-e945-4717-b12f-c2f800ef138e`
- **参数名**: `VendorApiInfix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Scu`
- **描述**: In driver modules which can be instantiated several times on a single ECU, BSW00347 requires that the name of APIs is extended by the VendorId and a vendor specific name.
This parameter is used to specify the vendor specific name. In total, the implementation specific name is generated as follows:
<ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>.

E.g.  assuming that the VendorId of the implementer is 17 and the implementer chose a VendorApiInfix of "Scu" a api name Wdg_SetMode defined in the SWS will translate to Wdg_17_Scu_SetMode.

This parameter is mandatory for all modules with upper multiplicity > 1. It shall not be used for modules with upper multiplicity =1.

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

1. **Wdg**
