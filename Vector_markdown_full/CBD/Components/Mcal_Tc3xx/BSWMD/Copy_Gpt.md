# Gpt - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:07

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Gpt](#gpt)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Gpt

#### 基本信息

- **UUID**: `ECUC:865c8c0e-f964-4d70-92a9-ff60c9da4cee`
- **模块名称**: `Gpt`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Gpt (General Purpose Timer) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2017-09-25
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. GptChannelConfigSet

**容器属性**:

- **UUID**: `ECUC:4979fd66-44c0-4740-bb83-130a05d7b9e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container is the base of a Configuration Set which contains the configured GPT channels. This way, different configuration sets can be defined for post-build process.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. GptChannelConfiguration

**容器属性**:

- **UUID**: `ECUC:3bd21bc7-c30d-4c8f-9c92-12d0728d28fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfiguration`
- **多重性**: [1..197]

**容器描述**:

Configuration of an individual GPT channel.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. GptChannelId

- **UUID**: `ECUC:6837c6f8-ac45-45c2-ad43-e9c4bd938987`
- **参数名**: `GptChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..196]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the GPT channel. This value will be assigned to the symbolic name derived of the GptChannelConfiguration container short name.

########## 2. GptChannelTickValueMax

- **UUID**: `ECUC:e9a0902c-4d36-49a6-9ee6-b96c7e2020a3`
- **参数名**: `GptChannelTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `65535`
- **取值范围**: [0..16777215]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

######### BOOLEAN 类型参数

########## 1. GptEnableWakeup

- **UUID**: `ECUC:050adbdf-4788-4c6d-bb7c-189e1fdada87`
- **参数名**: `GptEnableWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables wakeup capability of MCU for a channel.                               Enabled only if GptReportWakeupSource is True.

######### FLOAT 类型参数

########## 1. GptChannelTickFrequency

- **UUID**: `ECUC:8091bd1f-9e25-428e-a01c-43ba9fdc009e`
- **参数名**: `GptChannelTickFrequency`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0`
- **取值范围**: [0.0..65535.0]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the tick frequency of the timer channel in Hz.

######### ENUMERATION 类型参数

########## 1. GptAssignedHwUnit

- **UUID**: `ECUC:d096a707-71e0-412f-a76d-b0c298d22a2f`
- **参数名**: `GptAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GPT12` (来源: INFINEON_AURIX2G)
  - `GTM` (来源: INFINEON_AURIX2G)
- **描述**: Specifies the timer hardware used for this Gpt channel.

########## 2. GptChannelMode

- **UUID**: `ECUC:d096a707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT_CH_MODE_CONTINUOUS`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPT_CH_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `GPT_CH_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Specifies the behavior of the timer channel after the target time is reached.

########## 3. GptTimerChannelUsage

- **UUID**: `ECUC:d096f707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptTimerChannelUsage`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT_TIMER_CHANNEL_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GPT_PREDEF_TIMERCH_1US_16BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_1US_16_24BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_1US_16_24_32BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_100US_32BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_TIMER_CHANNEL_NORMAL` (来源: INFINEON_AURIX2G)
- **描述**: Specifies the grade of enabling the GPT Predef Timers for this channel.

######### FUNCTION-NAME 类型参数

########## 1. GptNotification

- **UUID**: `ECUC:ebfb835b-d90b-4928-831b-b544eef5b204`
- **参数名**: `GptNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_GptNotification0`
- **描述**: Function pointer to callback function (for non-wakeup notification)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GptChannelClkSrcRef

- **UUID**: `ECUC:28265a09-7e26-491d-95dd-8e4122a9fb97`
- **引用名**: `GptChannelClkSrcRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptDriverConfiguration/GptClockReferencePoint`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the GptClockReferencePoint from which the channel.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]

**容器描述**:

Function pointer to callback function (for wakeup notification).

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.                                   Enabled only if GptReportWakeupSource and GptEnableWakeup are True

######### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..3]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this GPT Driver. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_GPT_DRIVER

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
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
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

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

######### 3. Gpt12TimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e871`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Gpt12TimerOutputModuleConfiguration`
- **多重性**: [0..2]

**容器描述**:

Choose GPT12 channel which will be used by this GPT Driver.                                 Referred timer channel in MCU should have GPT12Timerblock as USED_BY_GPT_DRIVER

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. Gpt12ChannelClockDivider

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f3`
- **参数名**: `Gpt12ChannelClockDivider`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter decides the divider value of this timer channel. This value depends on the prescalar configured in MCU

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. Gpt12TimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3586`
- **引用名**: `Gpt12TimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 2. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]

**容器描述**:

Function pointer to callback function (for wakeup notification).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.                                   Enabled only if GptReportWakeupSource and GptEnableWakeup are True

####### 3. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..3]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this GPT Driver. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_GPT_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
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
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

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

####### 4. Gpt12TimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e871`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Gpt12TimerOutputModuleConfiguration`
- **多重性**: [0..2]

**容器描述**:

Choose GPT12 channel which will be used by this GPT Driver.                                 Referred timer channel in MCU should have GPT12Timerblock as USED_BY_GPT_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. Gpt12ChannelClockDivider

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f3`
- **参数名**: `Gpt12ChannelClockDivider`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter decides the divider value of this timer channel. This value depends on the prescalar configured in MCU

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. Gpt12TimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3586`
- **引用名**: `Gpt12TimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 2. GptChannelConfiguration

**容器属性**:

- **UUID**: `ECUC:3bd21bc7-c30d-4c8f-9c92-12d0728d28fb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptChannelConfiguration`
- **多重性**: [1..197]

**容器描述**:

Configuration of an individual GPT channel.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. GptChannelId

- **UUID**: `ECUC:6837c6f8-ac45-45c2-ad43-e9c4bd938987`
- **参数名**: `GptChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..196]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the GPT channel. This value will be assigned to the symbolic name derived of the GptChannelConfiguration container short name.

######## 2. GptChannelTickValueMax

- **UUID**: `ECUC:e9a0902c-4d36-49a6-9ee6-b96c7e2020a3`
- **参数名**: `GptChannelTickValueMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `65535`
- **取值范围**: [0..16777215]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer rolls over to zero.

####### BOOLEAN 类型参数

######## 1. GptEnableWakeup

- **UUID**: `ECUC:050adbdf-4788-4c6d-bb7c-189e1fdada87`
- **参数名**: `GptEnableWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables wakeup capability of MCU for a channel.                               Enabled only if GptReportWakeupSource is True.

####### FLOAT 类型参数

######## 1. GptChannelTickFrequency

- **UUID**: `ECUC:8091bd1f-9e25-428e-a01c-43ba9fdc009e`
- **参数名**: `GptChannelTickFrequency`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1.0`
- **取值范围**: [0.0..65535.0]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the tick frequency of the timer channel in Hz.

####### ENUMERATION 类型参数

######## 1. GptAssignedHwUnit

- **UUID**: `ECUC:d096a707-71e0-412f-a76d-b0c298d22a2f`
- **参数名**: `GptAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GPT12` (来源: INFINEON_AURIX2G)
  - `GTM` (来源: INFINEON_AURIX2G)
- **描述**: Specifies the timer hardware used for this Gpt channel.

######## 2. GptChannelMode

- **UUID**: `ECUC:d096a707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptChannelMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT_CH_MODE_CONTINUOUS`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPT_CH_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `GPT_CH_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **描述**: Specifies the behavior of the timer channel after the target time is reached.

######## 3. GptTimerChannelUsage

- **UUID**: `ECUC:d096f707-71e0-412f-a76d-b0c298d22a2e`
- **参数名**: `GptTimerChannelUsage`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT_TIMER_CHANNEL_NORMAL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GPT_PREDEF_TIMERCH_1US_16BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_1US_16_24BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_1US_16_24_32BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_PREDEF_TIMERCH_100US_32BIT_ENABLED` (来源: INFINEON_AURIX2G)
  - `GPT_TIMER_CHANNEL_NORMAL` (来源: INFINEON_AURIX2G)
- **描述**: Specifies the grade of enabling the GPT Predef Timers for this channel.

####### FUNCTION-NAME 类型参数

######## 1. GptNotification

- **UUID**: `ECUC:ebfb835b-d90b-4928-831b-b544eef5b204`
- **参数名**: `GptNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `IoHwAb_GptNotification0`
- **描述**: Function pointer to callback function (for non-wakeup notification)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. GptChannelClkSrcRef

- **UUID**: `ECUC:28265a09-7e26-491d-95dd-8e4122a9fb97`
- **引用名**: `GptChannelClkSrcRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptDriverConfiguration/GptClockReferencePoint`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the GptClockReferencePoint from which the channel.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]

**容器描述**:

Function pointer to callback function (for wakeup notification).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.                                   Enabled only if GptReportWakeupSource and GptEnableWakeup are True

####### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..3]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this GPT Driver. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_GPT_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
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
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

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

####### 3. Gpt12TimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e871`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Gpt12TimerOutputModuleConfiguration`
- **多重性**: [0..2]

**容器描述**:

Choose GPT12 channel which will be used by this GPT Driver.                                 Referred timer channel in MCU should have GPT12Timerblock as USED_BY_GPT_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. Gpt12ChannelClockDivider

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f3`
- **参数名**: `Gpt12ChannelClockDivider`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter decides the divider value of this timer channel. This value depends on the prescalar configured in MCU

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. Gpt12TimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3586`
- **引用名**: `Gpt12TimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 3. GptWakeupConfiguration

**容器属性**:

- **UUID**: `ECUC:1e4712bb-f384-47fd-b5f3-9aa93036757a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptWakeupConfiguration`
- **多重性**: [0..1]

**容器描述**:

Function pointer to callback function (for wakeup notification).

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. GptWakeupSourceRef

- **UUID**: `ECUC:95b50a0d-7238-4494-91b4-430aa279da61`
- **引用名**: `GptWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: In case the wakeup-capability is true this value is transmitted to the Ecu State Manager.                                   Enabled only if GptReportWakeupSource and GptEnableWakeup are True

##### 4. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..3]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this GPT Driver. Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_GPT_DRIVER

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f2`
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
- **描述**: This parameter decides the Clock Source for TOM/ATOM timer.

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

##### 5. Gpt12TimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e871`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `Gpt12TimerOutputModuleConfiguration`
- **多重性**: [0..2]

**容器描述**:

Choose GPT12 channel which will be used by this GPT Driver.                                 Referred timer channel in MCU should have GPT12Timerblock as USED_BY_GPT_DRIVER

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. Gpt12ChannelClockDivider

- **UUID**: `ECUC:31514abb-3296-4c09-bdb7-d0909f1440f3`
- **参数名**: `Gpt12ChannelClockDivider`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter decides the divider value of this timer channel. This value depends on the prescalar configured in MCU

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. Gpt12TimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3586`
- **引用名**: `Gpt12TimerUsed`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **目标引用列表**:
  - `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 6. GptConfigurationOfOptApiServices

**容器属性**:

- **UUID**: `ECUC:90664429-2ed4-41ca-bcf2-01b0a2746af8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptConfigurationOfOptApiServices`
- **多重性**: [0..1]

**容器描述**:

This container contains all configuration switches for configuring optional API services of the GPT driver.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. GptDeinitApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484cbf`
- **参数名**: `GptDeinitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Gpt_DeInit() from the code.

######## 2. GptEnableDisableNotificationApi

- **UUID**: `ECUC:027ab717-0873-44c6-b93d-0f24ee62e86f`
- **参数名**: `GptEnableDisableNotificationApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Gpt_EnableNotification() and Gpt_DisableNotification from the code.

######## 3. GptTimeElapsedApi

- **UUID**: `ECUC:058aeda8-3c76-4d95-b2cc-5016fd1bd1fe`
- **参数名**: `GptTimeElapsedApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Gpt_GetTimeElapsed() from the code

######## 4. GptTimeRemainingApi

- **UUID**: `ECUC:5161a68e-b5aa-479a-a9b0-615efa4cd7e4`
- **参数名**: `GptTimeRemainingApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Gpt_GetTimeRemaining() from the code.

######## 5. GptVersionInfoApi

- **UUID**: `ECUC:92f35bef-c3fa-4df9-80e5-fde7d2101466`
- **参数名**: `GptVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Gpt_GetVersionInfo() from the code.

######## 6. GptWakeupFunctionalityApi

- **UUID**: `ECUC:22859cbc-8346-4a44-a605-211d23a78203`
- **参数名**: `GptWakeupFunctionalityApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Gpt_SetMode(), Gpt_EnableWakeup() Gpt_DisableWakeup() and Gpt_CheckWakeup() from the code.

##### 7. GptDriverConfiguration

**容器属性**:

- **UUID**: `ECUC:2f5dc4e3-3ec4-4d52-b768-29135bf6010f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptDriverConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the module-wide configuration (parameters) of the GPT Driver

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. GptDevErrorDetect

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec226fb5b17`
- **参数名**: `GptDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. GptMultiCoreErrorDetect

- **UUID**: `ECUC:412da385-6bf4-4829-87e4-8ec226fb5b17`
- **参数名**: `GptMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Multicore Default Error Tracer (Det) detection and notification ON or OFF.

######## 3. GptReportWakeupSource

- **UUID**: `ECUC:53a4201b-75d1-4987-905d-e27a656712ff`
- **参数名**: `GptReportWakeupSource`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables/Disables wakeup source reporting.

######## 4. GptPredefTimer100us32bitEnable

- **UUID**: `ECUC:3180661f-752e-4a2b-8c41-90892cd0a655`
- **参数名**: `GptPredefTimer100us32bitEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables/disables the GPT Predef Timer 100?s32bit.

######## 5. GptSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `GptSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

######## 6. GptReadAcrossCores

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b18`
- **参数名**: `GptReadAcrossCores`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable reading the timer value from all cores.

######## 7. GptInitCheckApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484ecf`
- **参数名**: `GptInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Gpt_InitCheck() from the code.

####### ENUMERATION 类型参数

######## 1. GptPredefTimer1usEnablingGrade

- **UUID**: `ECUC:92c9cf6f-d2a3-45c4-af10-157a0b5ab06b`
- **参数名**: `GptPredefTimer1usEnablingGrade`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT_PREDEF_TIMER_1US_DISABLED`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `GPT_PREDEF_TIMER_1US_16BIT_ENABLED` (来源: AUTOSAR_ECUC)
  - `GPT_PREDEF_TIMER_1US_16_24BIT_ENABLED` (来源: AUTOSAR_ECUC)
  - `GPT_PREDEF_TIMER_1US_16_24_32BIT_ENABLED` (来源: AUTOSAR_ECUC)
  - `GPT_PREDEF_TIMER_1US_DISABLED` (来源: AUTOSAR_ECUC)
- **描述**: Specifies the grade of enabling the GPT Predef Timers with 1?s tick duration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. GptClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:8eb48a5f-43d7-4a7a-bedb-9f520c5165b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptClockReferencePoint`
- **多重性**: [1..256]

**容器描述**:

This container contains a parameter, which represents a reference to a container of the type McuClockReferencePoint (defined in module MCU).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. GptClockReference

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2bd`
- **引用名**: `GptClockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a container of the type McuClockReferencePoint, to select an input clock.

########## 2. GptClockReferenceConfig

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2be`
- **引用名**: `GptClockReferenceConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to a container of the type McuClockReferencePointConfig, to select an input clock.

##### 8. GptClockReferencePoint

**容器属性**:

- **UUID**: `ECUC:8eb48a5f-43d7-4a7a-bedb-9f520c5165b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GptClockReferencePoint`
- **多重性**: [1..256]

**容器描述**:

This container contains a parameter, which represents a reference to a container of the type McuClockReferencePoint (defined in module MCU).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. GptClockReference

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2bd`
- **引用名**: `GptClockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a container of the type McuClockReferencePoint, to select an input clock.

######## 2. GptClockReferenceConfig

- **UUID**: `ECUC:ff94d0f2-e4d4-4b60-b980-6ea07438f2be`
- **引用名**: `GptClockReferenceConfig`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePointConfig`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePointConfig`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: Reference to a container of the type McuClockReferencePointConfig, to select an input clock.

##### 9. CommonPublishedInformation

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
- **默认值**: `100`
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

1. **Gpt**
