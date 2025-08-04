# Wdg - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Wdg](#wdg)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Wdg

#### 基本信息

- **UUID**: `ECUC:63541b2b-c94a-451e-abfe-cc1f96b6e723`
- **模块名称**: `Wdg`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Wdg (Watchdog driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. WdgDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:2a57363a-0c1a-4080-b066-ef5dacdfa7b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

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
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization or mode switch failed because it would disable the watchdog" has occurred.

######## 2. WDG_E_MODE_FAILED

- **UUID**: `ECUC:8d2358b4-1d83-4c70-b73c-8700019f161f`
- **引用名**: `WDG_E_MODE_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Setting a watchdog mode failed (during initialization or mode switch)" has occurred.

##### 2. WdgGeneral

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4981-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

All general parameters of the watchdog driver are collected here.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. WdgIndex

- **UUID**: `ECUC:5bc72261-2c22-4c7e-9999-80651ba3fdc1`
- **参数名**: `WdgIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Represents the watchdog driver's ID so that it can be referenced by the watchdog interface.

####### BOOLEAN 类型参数

######## 1. WdgDevErrorDetect

- **UUID**: `ECUC:286ff3be-9991-46b5-8518-85a9324954dd`
- **参数名**: `WdgDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable / disable development error detection for this module.

######## 2. WdgDisableAllowed

- **UUID**: `ECUC:9ab89355-5ba4-4293-94b5-fb189cbcc2b2`
- **参数名**: `WdgDisableAllowed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to allow / forbid disabling the watchdog driver during runtime.

######## 3. WdgVersionInfoApi

- **UUID**: `ECUC:c8084b58-82da-4677-8381-3ed7b707dfdb`
- **参数名**: `WdgVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable / disable the version information API

####### FLOAT 类型参数

######## 1. WdgInitialTimeout

- **UUID**: `ECUC:c20d7853-9f81-4e43-84e4-e8378cdc3ba4`
- **参数名**: `WdgInitialTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The initial timeout (sec) for the trigger condition to be initialized during Init function. It shall be not larger than WdgMaxTimeout.

######## 2. WdgMaxTimeout

- **UUID**: `ECUC:fc6fa127-3b50-43b7-b660-6ee4ed01a755`
- **参数名**: `WdgMaxTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum timeout (sec) to which the watchdog trigger condition can be initialized.

####### ENUMERATION 类型参数

######## 1. WdgRunArea

- **UUID**: `ECUC:1df59d7c-8eb1-4ada-8bb0-1293237f6550`
- **参数名**: `WdgRunArea`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RAM` (来源: AUTOSAR_ECUC)
  - `ROM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Represents the watchdog driver execution area is either from ROM(Flash) or RAM as required with the particular microcontroller.

####### FUNCTION-NAME 类型参数

######## 1. WdgTriggerLocation

- **UUID**: `ECUC:18986e28-613e-472f-9099-6889c30148cb`
- **参数名**: `WdgTriggerLocation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Location (memory address) of the watchdog trigger routine.

##### 3. WdgPublishedInformation

**容器属性**:

- **UUID**: `ECUC:a3ab7732-c7a9-4ecd-b346-5574a81f6562`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container holding all Wdg specific published information parameters

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. WdgTriggerMode

- **UUID**: `ECUC:7b066c98-77c0-40de-868a-0410e014c775`
- **参数名**: `WdgTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDG_BOTH` (来源: AUTOSAR_ECUC)
  - `WDG_TOGGLE` (来源: AUTOSAR_ECUC)
  - `WDG_WINDOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-LINK-TIME
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Watchdog trigger mode (toggle/window/both)

##### 4. WdgSettingsConfig

**容器属性**:

- **UUID**: `ECUC:aa5bea66-87cc-4d25-8725-2f031a550397`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Configuration items for the different watchdog settings, including those for external watchdog hardware.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. WdgDefaultMode

- **UUID**: `ECUC:e13b2659-66ee-430f-8004-7378de27cc1f`
- **参数名**: `WdgDefaultMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `WDGIF_FAST_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_OFF_MODE` (来源: AUTOSAR_ECUC)
  - `WDGIF_SLOW_MODE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Default mode for watchdog driver initialization.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. WdgExternalConfiguration

**容器属性**:

- **UUID**: `ECUC:d4132c73-7eee-4a7a-80a8-e3f6c256baca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration items for an external watchdog hardware

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. WdgExternalContainerRef

- **UUID**: `ECUC:ece56c85-00e0-4720-bd8c-0d33665138c0`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to either

####### 2. WdgSettingsFast

**容器属性**:

- **UUID**: `ECUC:8b2ff9f0-4ec8-4fbb-9089-eff1c3aad425`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "fast" mode.

####### 3. WdgSettingsOff

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

####### 4. WdgSettingsSlow

**容器属性**:

- **UUID**: `ECUC:82e6dd1d-aa7e-40af-b0db-7ff521f64749`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

##### 5. WdgExternalConfiguration

**容器属性**:

- **UUID**: `ECUC:d4132c73-7eee-4a7a-80a8-e3f6c256baca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgExternalConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration items for an external watchdog hardware

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgExternalContainerRef

- **UUID**: `ECUC:ece56c85-00e0-4720-bd8c-0d33665138c0`
- **引用名**: `WdgExternalContainerRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to either

##### 6. WdgSettingsFast

**容器属性**:

- **UUID**: `ECUC:8b2ff9f0-4ec8-4fbb-9089-eff1c3aad425`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsFast`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "fast" mode.

##### 7. WdgSettingsOff

**容器属性**:

- **UUID**: `ECUC:9f99b3ba-302b-4bb6-8e30-421676aebaab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsOff`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "off" mode.

##### 8. WdgSettingsSlow

**容器属性**:

- **UUID**: `ECUC:82e6dd1d-aa7e-40af-b0db-7ff521f64749`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgSettingsSlow`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Hardware dependent settings for the watchdog driver's "slow" mode.

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

1. **Wdg**
