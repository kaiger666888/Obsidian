# Gpt - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:48

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Gpt](#gpt)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Gpt

#### 基本信息

- **UUID**: `ECUC:865c8c0e-f964-4d70-92a9-ff60c9da4cee`
- **模块名称**: `Gpt`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Gpt (General Purpose Timer) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. GptChannelConfigSet

**容器属性**:

- **UUID**: `ECUC:4979fd66-44c0-4740-bb83-130a05d7b9e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is the base of a Configuration Set which contains the configured GPT channels. This way, different configuration sets can be defined for post-build process.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. GptChannelConfiguration

**容器属性**:

- **UUID**: `ECUC:3bd21bc7-c30d-4c8f-9c92-12d0728d28fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfiguration`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual GPT channel.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. GptChannelId

- **UUID**: `ECUC:6837c6f8-ac45-45c2-ad43-e9c4bd938987`
- **参数名**: `GptChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the GPT channel. This value will be assigned to the symbolic name derived of the GptChannelConfiguration container short name.

########## 2. GptChannelTickValueMax

- **UUID**: `ECUC:e9a0902c-4d36-49a6-9ee6-b96c7e2020a3`
- **参数名**: `GptChannelTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

######### BOOLEAN 类型参数

########## 1. GptEnableWakeup

- **UUID**: `ECUC:050adbdf-4788-4c6d-bb7c-189e1fdada87`
- **参数名**: `GptEnableWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables wakeup capability of MCU for a channel.

######### FLOAT 类型参数

########## 1. GptChannelTickFrequency

- **UUID**: `ECUC:8091bd1f-9e25-428e-a01c-43ba9fdc009e`
- **参数名**: `GptChannelTickFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the tick frequency of the timer channel in Hz.

######### ENUMERATION 类型参数

########## 1. GptChannelMode

- **UUID**: `ECUC:d096f707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPT_CH_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `GPT_CH_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the behaviour of the timer channel after the target time is reached.

######### FUNCTION-NAME 类型参数

########## 1. GptNotification

- **UUID**: `ECUC:ebfb835b-d90b-4928-831b-b544eef5b204`
- **参数名**: `GptNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function pointer to callback function (for non-wakeup notification)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GptChannelClkSrcRef

- **UUID**: `ECUC:28265a09-7e26-491d-95dd-8e4122a9fb97`
- **引用名**: `GptChannelClkSrcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `GptClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptDriverConfiguration/GptClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the GptClockReferencePoint from which the channel

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Function pointer to callback function (for non-wakeup notification).

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.

####### 2. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Function pointer to callback function (for non-wakeup notification).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.

##### 2. GptChannelConfiguration

**容器属性**:

- **UUID**: `ECUC:3bd21bc7-c30d-4c8f-9c92-12d0728d28fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfiguration`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual GPT channel.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. GptChannelId

- **UUID**: `ECUC:6837c6f8-ac45-45c2-ad43-e9c4bd938987`
- **参数名**: `GptChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the GPT channel. This value will be assigned to the symbolic name derived of the GptChannelConfiguration container short name.

######## 2. GptChannelTickValueMax

- **UUID**: `ECUC:e9a0902c-4d36-49a6-9ee6-b96c7e2020a3`
- **参数名**: `GptChannelTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

####### BOOLEAN 类型参数

######## 1. GptEnableWakeup

- **UUID**: `ECUC:050adbdf-4788-4c6d-bb7c-189e1fdada87`
- **参数名**: `GptEnableWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables wakeup capability of MCU for a channel.

####### FLOAT 类型参数

######## 1. GptChannelTickFrequency

- **UUID**: `ECUC:8091bd1f-9e25-428e-a01c-43ba9fdc009e`
- **参数名**: `GptChannelTickFrequency`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the tick frequency of the timer channel in Hz.

####### ENUMERATION 类型参数

######## 1. GptChannelMode

- **UUID**: `ECUC:d096f707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPT_CH_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `GPT_CH_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the behaviour of the timer channel after the target time is reached.

####### FUNCTION-NAME 类型参数

######## 1. GptNotification

- **UUID**: `ECUC:ebfb835b-d90b-4928-831b-b544eef5b204`
- **参数名**: `GptNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function pointer to callback function (for non-wakeup notification)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. GptChannelClkSrcRef

- **UUID**: `ECUC:28265a09-7e26-491d-95dd-8e4122a9fb97`
- **引用名**: `GptChannelClkSrcRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `GptClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptDriverConfiguration/GptClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the GptClockReferencePoint from which the channel

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Function pointer to callback function (for non-wakeup notification).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.

##### 3. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Function pointer to callback function (for non-wakeup notification).

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.

##### 4. GptConfigurationOfOptApiServices

**容器属性**:

- **UUID**: `ECUC:90664429-2ed4-41ca-bcf2-01b0a2746af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptConfigurationOfOptApiServices`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains all configuration switches for configuring optional API services of the GPT driver.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. GptDeinitApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484cbf`
- **参数名**: `GptDeinitApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Gpt_DeInit() from the code.

######## 2. GptEnableDisableNotificationApi

- **UUID**: `ECUC:027ab717-0873-44c6-b93d-0f24ee62e86f`
- **参数名**: `GptEnableDisableNotificationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services Gpt_EnableNotification() and Gpt_DisableNotification from the code.

######## 3. GptTimeElapsedApi

- **UUID**: `ECUC:058aeda8-3c76-4d95-b2cc-5016fd1bd1fe`
- **参数名**: `GptTimeElapsedApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Gpt_GetTimeElapsed() from the code

######## 4. GptTimeRemainingApi

- **UUID**: `ECUC:5161a68e-b5aa-479a-a9b0-615efa4cd7e4`
- **参数名**: `GptTimeRemainingApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Gpt_GetTimeRemaining() from the code.

######## 5. GptVersionInfoApi

- **UUID**: `ECUC:92f35bef-c3fa-4df9-80e5-fde7d2101466`
- **参数名**: `GptVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Gpt_GetVersionInfo() from the code.

######## 6. GptWakeupFunctionalityApi

- **UUID**: `ECUC:22859cbc-8346-4a44-a605-211d23a78203`
- **参数名**: `GptWakeupFunctionalityApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services Gpt_SetMode(), Gpt_EnableWakeup() Gpt_DisableWakeup() and Gpt_CheckWakeup() from the code.

##### 5. GptDriverConfiguration

**容器属性**:

- **UUID**: `ECUC:2f5dc4e3-3ec4-4d52-b768-29135bf6010f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptDriverConfiguration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the module-wide configuration (parameters) of the GPT Driver

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. GptDevErrorDetect

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec226fb5b17`
- **参数名**: `GptDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables development error detection.

######## 2. GptReportWakeupSource

- **UUID**: `ECUC:53a4201b-75d1-4987-905d-e27a656712ff`
- **参数名**: `GptReportWakeupSource`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables wakeup source reporting.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. GptClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:8eb48a5f-43d7-4a7a-bedb-9f520c5165b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a parameter, which represents a reference to a container of the type McuClockReferencePoint (defined in module MCU).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GptClockReference

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2bd`
- **引用名**: `GptClockReference`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a container of the type McuClockReferencePoint, to select an input clock.

##### 6. GptClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:8eb48a5f-43d7-4a7a-bedb-9f520c5165b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptClockReferencePoint`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a parameter, which represents a reference to a container of the type McuClockReferencePoint (defined in module MCU).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. GptClockReference

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2bd`
- **引用名**: `GptClockReference`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a container of the type McuClockReferencePoint, to select an input clock.

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

1. **Gpt**
