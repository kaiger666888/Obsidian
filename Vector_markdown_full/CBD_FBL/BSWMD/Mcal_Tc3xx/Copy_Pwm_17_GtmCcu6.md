# Pwm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:15

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Pwm](#pwm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Pwm

#### 基本信息

- **UUID**: `ECUC:13aa2440-e790-4121-9e12-3a380efb0d6b`
- **模块名称**: `Pwm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of Pwm (Pulse Width Modulation) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. PwmChannelConfigSet

**容器属性**:

- **UUID**: `ECUC:64be7cd3-9cb3-4e87-b679-3a43aaf7f82c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannelConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR Pwm module.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. PwmChannel

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b383-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual PWM channel.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. PwmChannelId

- **UUID**: `ECUC:3a0e3f14-a2b9-428e-9b76-6a361c8b2ea4`
- **参数名**: `PwmChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the PwmChannel container short name.

########## 2. PwmDutycycleDefault

- **UUID**: `ECUC:daa5c051-75d5-4a20-8b6a-ca34afab3ddd`
- **参数名**: `PwmDutycycleDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of duty cycle used for Initialization
                           Depends on PwmDutyShiftInTicks parameter.
                           When the PwmDutyShiftInTicks is OFF, the Dutycyle should be entered as percentage:
                           0, represents 0%
                           0x8000 represents 100%
                           When the PwmDutyShiftInTicks is ON, the Dutycyle should be entered as absolute ticks:
                           0, represents 0%
                           Same value as Period value represents 100%

########## 3. PwmPeriodDefault

- **UUID**: `ECUC:2e258b97-f1d8-4dc0-ad1a-dbdc0445568b`
- **参数名**: `PwmPeriodDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Period of the channel. Input Value in absolute ticks.
                          This parameter does not impact the channels of class PWM_FIXED_PERIOD_SHIFTED and PWM_FIXED_PERIOD_CENTER_ALIGNED.

########## 4. PwmShiftValue

- **UUID**: `ECUC:a44896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmShiftValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Shift Value for PWM_FIXED_PERIOD_SHIFTED Signal.
                           Valid only when PwmChannelClass is PWM_FIXED_PERIOD_SHIFTED.
                           This depends on PwmDutyShiftInTicks parameter.
                           When the PwmDutyShiftInTicks is OFF, the Shift value should be entered as percentage:
                           0, represents 0%
                           0x8000 represents 100%
                           When the PwmDutyShiftInTicks is ON, the Shift value should be entered as absolute ticks:
                           0, represents 0%
                           Same value as Period value represents 100%

######### BOOLEAN 类型参数

########## 1. PwmCoherentUpdate

- **UUID**: `ECUC:c987dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **参数名**: `PwmCoherentUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Setting this parameter to true determines channel is coherent ot not.

######### ENUMERATION 类型参数

########## 1. PwmChannelClass

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `PwmChannelClass`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_FIXED_PERIOD`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_FIXED_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_SHIFTED` (来源: AUTOSAR_ECUC)
  - `PWM_VARIABLE_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_CENTER_ALIGNED` (来源: AUTOSAR_ECUC)
- **描述**: Class of PWM Channel.  ImplementationType: Pwm_17_GtmCcu6_ChannelClassType.

########## 2. PwmAssignedHwUnit

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0909f0440c6`
- **参数名**: `PwmAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM` (来源: INFINEON_AURIX2G)
  - `CCU6` (来源: INFINEON_AURIX2G)
- **描述**: The HW resource used for PWM Generation.

########## 3. PwmIdleState

- **UUID**: `ECUC:7cc25f83-b89c-4ba0-8766-7ba087185c97`
- **参数名**: `PwmIdleState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **描述**: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is stopped (e.g. call of Pwm_SetOutputToIdle).

########## 4. PwmPolarity

- **UUID**: `ECUC:a31896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Defines the starting polarity of each PWM channel.

######### FUNCTION-NAME 类型参数

########## 1. PwmNotification

- **UUID**: `ECUC:44bb38ac-d409-4b1d-96be-ec84466c1019`
- **参数名**: `PwmNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Definition of the Callback function.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. PwmMcuClockReferencePoint

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `PwmMcuClockReferencePoint`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter contains reference to the McuClockReferencePoint

########## 2. PwmReferenceChannel

- **UUID**: `ECUC:ca45dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `PwmReferenceChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PwmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference channel for PWM_FIXED_PERIOD_SHIFTED, and PWM_FIXED_PERIOD_CENTER_ALIGNED.
                             Reference should be a channel of PWM_FIXED_PERIOD Only.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_PWM_DRIVER

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. GtmTimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-d0909f1440f2`
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

######### 2. CCU6CC6Configuration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e2d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

Choose CCU6 T12/T13 channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have CCU6ChannelUsage as USED_BY_PWM_DRIVER

########## 参数配置

此容器包含 **4** 个参数：

########### BOOLEAN 类型参数

############ 1. CCU6TimerPrescalarEnabled

- **UUID**: `ECUC:2e3da645-2c56-4fd5-9fe6-2b2cf98ed6d8`
- **参数名**: `CCU6TimerPrescalarEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power CCU6TimerClockSelect)                                      if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power (CCU6TimerClockSelect+8) )

########### ENUMERATION 类型参数

############ 1. CCU6TimerUsed

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0919f0440f2`
- **参数名**: `CCU6TimerUsed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `T12`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `T12` (来源: INFINEON_AURIX2G)
  - `T13` (来源: INFINEON_AURIX2G)
- **描述**: Selects Timer T12/T13.                            Note: Kernel selection is done in parameter CCU6KernelUsed..

############ 2. Cc6xChannel

- **UUID**: `b209c80f-1111-422e-8f00-fa776e66e9fb`
- **参数名**: `Cc6xChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Cc60`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `Cc60` (来源: INFINEON_AURIX2G)
  - `Cc61` (来源: INFINEON_AURIX2G)
  - `Cc62` (来源: INFINEON_AURIX2G)
- **描述**: Cc6 channel selection from the selected kernel

############ 3. CCU6TimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-a0909f1440f2`
- **参数名**: `CCU6TimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCU6_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCU6_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for T12/T13 timer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3589`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels.                             Note: CCU6 resource allocation is done at kernel level for each module.                             Once the kernel is allocated to the module,  T12 or T13 timer of the kernel can only be assigned to one of the channels within the module.

####### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_PWM_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-d0909f1440f2`
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

####### 3. CCU6CC6Configuration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e2d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

Choose CCU6 T12/T13 channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have CCU6ChannelUsage as USED_BY_PWM_DRIVER

######## 参数配置

此容器包含 **4** 个参数：

######### BOOLEAN 类型参数

########## 1. CCU6TimerPrescalarEnabled

- **UUID**: `ECUC:2e3da645-2c56-4fd5-9fe6-2b2cf98ed6d8`
- **参数名**: `CCU6TimerPrescalarEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power CCU6TimerClockSelect)                                      if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power (CCU6TimerClockSelect+8) )

######### ENUMERATION 类型参数

########## 1. CCU6TimerUsed

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0919f0440f2`
- **参数名**: `CCU6TimerUsed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `T12`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `T12` (来源: INFINEON_AURIX2G)
  - `T13` (来源: INFINEON_AURIX2G)
- **描述**: Selects Timer T12/T13.                            Note: Kernel selection is done in parameter CCU6KernelUsed..

########## 2. Cc6xChannel

- **UUID**: `b209c80f-1111-422e-8f00-fa776e66e9fb`
- **参数名**: `Cc6xChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Cc60`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `Cc60` (来源: INFINEON_AURIX2G)
  - `Cc61` (来源: INFINEON_AURIX2G)
  - `Cc62` (来源: INFINEON_AURIX2G)
- **描述**: Cc6 channel selection from the selected kernel

########## 3. CCU6TimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-a0909f1440f2`
- **参数名**: `CCU6TimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCU6_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCU6_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for T12/T13 timer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3589`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels.                             Note: CCU6 resource allocation is done at kernel level for each module.                             Once the kernel is allocated to the module,  T12 or T13 timer of the kernel can only be assigned to one of the channels within the module.

##### 2. PwmChannel

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b383-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual PWM channel.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. PwmChannelId

- **UUID**: `ECUC:3a0e3f14-a2b9-428e-9b76-6a361c8b2ea4`
- **参数名**: `PwmChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the PwmChannel container short name.

######## 2. PwmDutycycleDefault

- **UUID**: `ECUC:daa5c051-75d5-4a20-8b6a-ca34afab3ddd`
- **参数名**: `PwmDutycycleDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of duty cycle used for Initialization
                           Depends on PwmDutyShiftInTicks parameter.
                           When the PwmDutyShiftInTicks is OFF, the Dutycyle should be entered as percentage:
                           0, represents 0%
                           0x8000 represents 100%
                           When the PwmDutyShiftInTicks is ON, the Dutycyle should be entered as absolute ticks:
                           0, represents 0%
                           Same value as Period value represents 100%

######## 3. PwmPeriodDefault

- **UUID**: `ECUC:2e258b97-f1d8-4dc0-ad1a-dbdc0445568b`
- **参数名**: `PwmPeriodDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Period of the channel. Input Value in absolute ticks.
                          This parameter does not impact the channels of class PWM_FIXED_PERIOD_SHIFTED and PWM_FIXED_PERIOD_CENTER_ALIGNED.

######## 4. PwmShiftValue

- **UUID**: `ECUC:a44896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmShiftValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Shift Value for PWM_FIXED_PERIOD_SHIFTED Signal.
                           Valid only when PwmChannelClass is PWM_FIXED_PERIOD_SHIFTED.
                           This depends on PwmDutyShiftInTicks parameter.
                           When the PwmDutyShiftInTicks is OFF, the Shift value should be entered as percentage:
                           0, represents 0%
                           0x8000 represents 100%
                           When the PwmDutyShiftInTicks is ON, the Shift value should be entered as absolute ticks:
                           0, represents 0%
                           Same value as Period value represents 100%

####### BOOLEAN 类型参数

######## 1. PwmCoherentUpdate

- **UUID**: `ECUC:c987dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **参数名**: `PwmCoherentUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Setting this parameter to true determines channel is coherent ot not.

####### ENUMERATION 类型参数

######## 1. PwmChannelClass

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `PwmChannelClass`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_FIXED_PERIOD`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_FIXED_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_SHIFTED` (来源: AUTOSAR_ECUC)
  - `PWM_VARIABLE_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_CENTER_ALIGNED` (来源: AUTOSAR_ECUC)
- **描述**: Class of PWM Channel.  ImplementationType: Pwm_17_GtmCcu6_ChannelClassType.

######## 2. PwmAssignedHwUnit

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0909f0440c6`
- **参数名**: `PwmAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM` (来源: INFINEON_AURIX2G)
  - `CCU6` (来源: INFINEON_AURIX2G)
- **描述**: The HW resource used for PWM Generation.

######## 3. PwmIdleState

- **UUID**: `ECUC:7cc25f83-b89c-4ba0-8766-7ba087185c97`
- **参数名**: `PwmIdleState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **描述**: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is stopped (e.g. call of Pwm_SetOutputToIdle).

######## 4. PwmPolarity

- **UUID**: `ECUC:a31896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `PWM_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **描述**: Defines the starting polarity of each PWM channel.

####### FUNCTION-NAME 类型参数

######## 1. PwmNotification

- **UUID**: `ECUC:44bb38ac-d409-4b1d-96be-ec84466c1019`
- **参数名**: `PwmNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL_PTR`
- **描述**: Definition of the Callback function.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. PwmMcuClockReferencePoint

- **UUID**: `ECUC:c945dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `PwmMcuClockReferencePoint`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter contains reference to the McuClockReferencePoint

######## 2. PwmReferenceChannel

- **UUID**: `ECUC:ca45dd5e-1a5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `PwmReferenceChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PwmChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet/PwmChannel`
- **来源**: INFINEON_AURIX2G
- **描述**: Reference channel for PWM_FIXED_PERIOD_SHIFTED, and PWM_FIXED_PERIOD_CENTER_ALIGNED.
                             Reference should be a channel of PWM_FIXED_PERIOD Only.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_PWM_DRIVER

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-d0909f1440f2`
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

####### 2. CCU6CC6Configuration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e2d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

Choose CCU6 T12/T13 channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have CCU6ChannelUsage as USED_BY_PWM_DRIVER

######## 参数配置

此容器包含 **4** 个参数：

######### BOOLEAN 类型参数

########## 1. CCU6TimerPrescalarEnabled

- **UUID**: `ECUC:2e3da645-2c56-4fd5-9fe6-2b2cf98ed6d8`
- **参数名**: `CCU6TimerPrescalarEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power CCU6TimerClockSelect)                                      if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power (CCU6TimerClockSelect+8) )

######### ENUMERATION 类型参数

########## 1. CCU6TimerUsed

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0919f0440f2`
- **参数名**: `CCU6TimerUsed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `T12`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `T12` (来源: INFINEON_AURIX2G)
  - `T13` (来源: INFINEON_AURIX2G)
- **描述**: Selects Timer T12/T13.                            Note: Kernel selection is done in parameter CCU6KernelUsed..

########## 2. Cc6xChannel

- **UUID**: `b209c80f-1111-422e-8f00-fa776e66e9fb`
- **参数名**: `Cc6xChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Cc60`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `Cc60` (来源: INFINEON_AURIX2G)
  - `Cc61` (来源: INFINEON_AURIX2G)
  - `Cc62` (来源: INFINEON_AURIX2G)
- **描述**: Cc6 channel selection from the selected kernel

########## 3. CCU6TimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-a0909f1440f2`
- **参数名**: `CCU6TimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCU6_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCU6_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for T12/T13 timer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3589`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels.                             Note: CCU6 resource allocation is done at kernel level for each module.                             Once the kernel is allocated to the module,  T12 or T13 timer of the kernel can only be assigned to one of the channels within the module.

##### 3. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_PWM_DRIVER

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. GtmTimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-d0909f1440f2`
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

##### 4. CCU6CC6Configuration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e2d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

Choose CCU6 T12/T13 channel which will be used by this PWM Channel.                              Referred timer channel in MCU should have CCU6ChannelUsage as USED_BY_PWM_DRIVER

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. CCU6TimerPrescalarEnabled

- **UUID**: `ECUC:2e3da645-2c56-4fd5-9fe6-2b2cf98ed6d8`
- **参数名**: `CCU6TimerPrescalarEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power CCU6TimerClockSelect)                                      if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power (CCU6TimerClockSelect+8) )

####### ENUMERATION 类型参数

######## 1. CCU6TimerUsed

- **UUID**: `ECUC:31505abb-2296-4c09-bdb7-d0919f0440f2`
- **参数名**: `CCU6TimerUsed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `T12`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `T12` (来源: INFINEON_AURIX2G)
  - `T13` (来源: INFINEON_AURIX2G)
- **描述**: Selects Timer T12/T13.                            Note: Kernel selection is done in parameter CCU6KernelUsed..

######## 2. Cc6xChannel

- **UUID**: `b209c80f-1111-422e-8f00-fa776e66e9fb`
- **参数名**: `Cc6xChannel`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `Cc60`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `Cc60` (来源: INFINEON_AURIX2G)
  - `Cc61` (来源: INFINEON_AURIX2G)
  - `Cc62` (来源: INFINEON_AURIX2G)
- **描述**: Cc6 channel selection from the selected kernel

######## 3. CCU6TimerClockSelect

- **UUID**: `ECUC:31505abb-3296-4c09-bdb7-a0909f1440f2`
- **参数名**: `CCU6TimerClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCU6_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCU6_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `CCU6_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This parameter decides the Clock Source for T12/T13 timer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3589`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: ECU
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels.                             Note: CCU6 resource allocation is done at kernel level for each module.                             Once the kernel is allocated to the module,  T12 or T13 timer of the kernel can only be assigned to one of the channels within the module.

##### 5. PwmConfigurationOfOptApiServices

**容器属性**:

- **UUID**: `ECUC:946d9f33-9bb7-48d7-8278-0f6efdacfaeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmConfigurationOfOptApiServices`
- **多重性**: [0..1]

**容器描述**:

This container has global switches of PWM APIs.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. PwmDeInitApi

- **UUID**: `ECUC:3e3da645-2c56-4fd5-9fe6-2b2cd88ed6d8`
- **参数名**: `PwmDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_DeInit() from the code.

######## 2. PwmGetOutputState

- **UUID**: `ECUC:8a7eb9e8-f5d3-4585-855b-72634c98da24`
- **参数名**: `PwmGetOutputState`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_GetOutputState() from the code.

######## 3. PwmSetDutyCycle

- **UUID**: `ECUC:bf14870c-ef7a-4d27-a6c0-4ebd02c8fdfe`
- **参数名**: `PwmSetDutyCycle`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_SetDutyCycle() from the code.

######## 4. PwmSetOutputToIdle

- **UUID**: `ECUC:45d9cbcc-c5b7-4c76-8469-5b65f7e9d6cd`
- **参数名**: `PwmSetOutputToIdle`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_SetOutputToIdle() from the code.

######## 5. PwmSetPeriodAndDuty

- **UUID**: `ECUC:bbb4cf88-5a3a-4053-8eae-023f3990279e`
- **参数名**: `PwmSetPeriodAndDuty`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_SetPeriodAndDuty() from the code.

######## 6. PwmVersionInfoApi

- **UUID**: `ECUC:33bfc216-9d93-4694-90c5-39340e82c758`
- **参数名**: `PwmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch to indicate that the Pwm_ GetVersionInfo is supported

##### 6. PwmGeneral

**容器属性**:

- **UUID**: `ECUC:9e045944-b70f-48ae-9745-0344fa64c653`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmGeneral`
- **多重性**: [0..1]

**容器描述**:

General settings for the PWM driver.

###### 参数配置

此容器包含 **14** 个参数：

####### INTEGER 类型参数

######## 1. PwmIndex

- **UUID**: `ECUC:1559f6dc-e859-4216-8c88-0f8836ae115e`
- **参数名**: `PwmIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. PwmDevErrorDetect

- **UUID**: `ECUC:7ee4dbf7-92ca-43f8-bedf-cd012b1d5f01`
- **参数名**: `PwmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. PwmMultiCoreErrorDetect

- **UUID**: `ECUC:7ee4dbf7-92ca-43f8-bedf-cd912b1d5f01`
- **参数名**: `PwmMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the Multicore error detection and notification ON or OFF.

######## 3. PwmDutycycleUpdatedEndperiod

- **UUID**: `ECUC:873477b1-c07e-4208-b92e-4e1875570984`
- **参数名**: `PwmDutycycleUpdatedEndperiod`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch for enabling the update of the duty cycle parameter at the end of the current period.                        PWM_VARIABLE_PERIOD channel class will not get affected with this parameter setting.

######## 4. PwmLowPowerStatesSupport

- **UUID**: `ECUC:2abff61e-374e-4c26-bcc6-6486e894e765`
- **参数名**: `PwmLowPowerStatesSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes all power state management related APIs (PWM_SetPowerState, PWM_GetCurrentPowerState, PWM_GetTargetPowerState, PWM_PreparePowerState, PWM_Main_PowerTransitionManager), indicating if the HW offers low power state management.

######## 5. PwmNotificationSupported

- **UUID**: `ECUC:39804e4a-209d-4df8-ade1-4e0cd88cc57d`
- **参数名**: `PwmNotificationSupported`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch to indicate that the notifications are supported

######## 6. PwmPeriodUpdatedEndperiod

- **UUID**: `ECUC:da85e8d7-af3c-4ad4-a700-43ea0462bee4`
- **参数名**: `PwmPeriodUpdatedEndperiod`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch for enabling the update of the period parameter at the end of the current period.                    PWM_FIXED_PERIOD, PWM_FIXED_PERIOD_SHIFTED and PWM_FIXED_PERIOD_CENTER_ALIGNED channel class will not get affected with this parameter setting.

######## 7. PwmChannelCoherentSelection

- **UUID**: `ECUC:da85e6d7-af3c-4ad4-a700-43ea0462bee4`
- **参数名**: `PwmChannelCoherentSelection`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch for enabling the update of the period / duty parameter at the end of the current period
                     channel wise. Switching on this parameter obsoletes PwmDutycycleUpdatedEndperiod and
                     PwmPeriodUpdatedEndperiod.

######## 8. PwmHandleShiftByOffset

- **UUID**: `ECUC:da85e8d7-af3c-4ad4-a710-43ea0462bee4`
- **参数名**: `PwmHandleShiftByOffset`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch for enabling Speacial handling for shifted channels.

######## 9. PwmDutyShiftInTicks

- **UUID**: `ECUC:da85e8d7-af3c-4ad4-a700-43ea0562bee4`
- **参数名**: `PwmDutyShiftInTicks`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch for Pwm Duty Cycle type:
                     Disabled - Duty Cycle and Shift value in percentage.
                     Enabled - Duty Cycle and Shift value in timer ticks.
                     User has to take care of entering the right values for PwmDutycycleDefault and PwmShiftValue based on this selection.

######## 10. PwmEnable0Or100DutyNotification

- **UUID**: `ECUC:da45e8d7-af3c-4ad4-a700-43ea0462bee4`
- **参数名**: `PwmEnable0Or100DutyNotification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch to enable notification for 0% and 100% duty for variable and fixed period channels.

######## 11. PwmPowerStateAsynchTransitionMode

- **UUID**: `ECUC:a510f93f-3393-467e-8c07-090d589c89f6`
- **参数名**: `PwmPowerStateAsynchTransitionMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / disables support of the PWM Driver to the asynchronous power state transition.

######## 12. PwmSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `PwmSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

######## 13. PwmInitCheckApi

- **UUID**: `ECUC:dbfab416-7231-4c9e-b7a2-2580d8484ecf`
- **参数名**: `PwmInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Pwm_17_GtmCcu6_InitCheck() from the code.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PwmPowerStateConfig

**容器属性**:

- **UUID**: `ECUC:32734417-2e9b-48db-930e-3df1591c3887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmPowerStateConfig`
- **多重性**: [0..1]

**容器描述**:

Each instance of this parameter defines a power state and the callback to be called when this power state is reached.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PwmPowerState

- **UUID**: `ECUC:ee4c6090-0034-4736-bdd2-7ad86f21e9d3`
- **参数名**: `PwmPowerState`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Each instance of this parameter describes a different power state supported by the PWM HW. It should be defined by the HW supplier and used by the PWMDriver to reference specific HW configurations which set the PWM HW module in the referenced power state.

######### FUNCTION-NAME 类型参数

########## 1. PwmPowerStateReadyCbkRef

- **UUID**: `ECUC:6e8869ff-d465-40bf-9296-d75dce548e58`
- **参数名**: `PwmPowerStateReadyCbkRef`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `PwmPowerStateCbk`
- **描述**: Each instance of this parameter contains a reference to a power mode callback defined in a CDD or IoHwAbs component.

##### 7. PwmPowerStateConfig

**容器属性**:

- **UUID**: `ECUC:32734417-2e9b-48db-930e-3df1591c3887`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmPowerStateConfig`
- **多重性**: [0..1]

**容器描述**:

Each instance of this parameter defines a power state and the callback to be called when this power state is reached.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. PwmPowerState

- **UUID**: `ECUC:ee4c6090-0034-4736-bdd2-7ad86f21e9d3`
- **参数名**: `PwmPowerState`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..9223372036854775807]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Each instance of this parameter describes a different power state supported by the PWM HW. It should be defined by the HW supplier and used by the PWMDriver to reference specific HW configurations which set the PWM HW module in the referenced power state.

####### FUNCTION-NAME 类型参数

######## 1. PwmPowerStateReadyCbkRef

- **UUID**: `ECUC:6e8869ff-d465-40bf-9296-d75dce548e58`
- **参数名**: `PwmPowerStateReadyCbkRef`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `PwmPowerStateCbk`
- **描述**: Each instance of this parameter contains a reference to a power mode callback defined in a CDD or IoHwAbs component.

##### 8. CommonPublishedInformation

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
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
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
- **默认值**: `121`
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

######## 1. VendorApiInfix

- **UUID**: `ad363b41-e945-4717-b12f-c2f800ef138e`
- **参数名**: `VendorApiInfix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `GtmCcu6`
- **描述**: In driver modules which can be instantiated several times on a single ECU, BSW00347 requires that the name of APIs is extended by the VendorId and a vendor specific name.
                  This parameter is used to specify the vendor specific name. In total, the implementation specific name is generated as follows:
                  <ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>.

                  E.g.  assuming that the VendorId of the implementor is 123 and the implementer chose a VendorApiInfix of "v11r456" a api name Can_Write defined in the SWS will translate to Can_123_v11r456Write.
                  This parameter is mandatory for all modules with upper multiplicity > 1. It shall not be used for modules with upper multiplicity =1.

######## 2. Release

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

1. **Pwm**
