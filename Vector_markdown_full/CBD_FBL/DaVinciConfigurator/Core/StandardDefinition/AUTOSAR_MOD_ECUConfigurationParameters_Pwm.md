# Pwm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:55

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Pwm](#pwm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Pwm

#### 基本信息

- **UUID**: `ECUC:13aa2440-e790-4121-9e12-3a380efb0d6b`
- **模块名称**: `Pwm`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of Pwm (Pulse Width Modulation) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. PwmChannelConfigSet

**容器属性**:

- **UUID**: `ECUC:64be7cd3-9cb3-4e87-b679-3a43aaf7f82c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannelConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Multiple Configuration Set Container

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PwmChannel

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b383-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual PWM channel.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. PwmChannelId

- **UUID**: `ECUC:3a0e3f14-a2b9-428e-9b76-6a361c8b2ea4`
- **参数名**: `PwmChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the PwmChannel container short name.

########## 2. PwmDutycycleDefault

- **UUID**: `ECUC:daa5c051-75d5-4a20-8b6a-ca34afab3ddd`
- **参数名**: `PwmDutycycleDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value of duty cycle used for Initialization

######### FLOAT 类型参数

########## 1. PwmPeriodDefault

- **UUID**: `ECUC:2e258b97-f1d8-4dc0-ad1a-dbdc0445568b`
- **参数名**: `PwmPeriodDefault`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value of period used for Initialization.(in seconds).

######### ENUMERATION 类型参数

########## 1. PwmChannelClass

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `PwmChannelClass`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_FIXED_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_SHIFTED` (来源: AUTOSAR_ECUC)
  - `PWM_VARIABLE_PERIOD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Class of PWM Channel.

########## 2. PwmIdleState

- **UUID**: `ECUC:7cc25f83-b89c-4ba0-8766-7ba087185c97`
- **参数名**: `PwmIdleState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is stopped (e.g. call of Pwm_SetOutputToIdle).

########## 3. PwmPolarity

- **UUID**: `ECUC:a31896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the starting polarity of each PWM channel.

######### FUNCTION-NAME 类型参数

########## 1. PwmNotification

- **UUID**: `ECUC:44bb38ac-d409-4b1d-96be-ec84466c1019`
- **参数名**: `PwmNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `"NULL"`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the Callback function.

##### 2. PwmChannel

**容器属性**:

- **UUID**: `ECUC:c2253a76-e0d8-4a8f-b383-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual PWM channel.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. PwmChannelId

- **UUID**: `ECUC:3a0e3f14-a2b9-428e-9b76-6a361c8b2ea4`
- **参数名**: `PwmChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the PwmChannel container short name.

######## 2. PwmDutycycleDefault

- **UUID**: `ECUC:daa5c051-75d5-4a20-8b6a-ca34afab3ddd`
- **参数名**: `PwmDutycycleDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..32768]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value of duty cycle used for Initialization

####### FLOAT 类型参数

######## 1. PwmPeriodDefault

- **UUID**: `ECUC:2e258b97-f1d8-4dc0-ad1a-dbdc0445568b`
- **参数名**: `PwmPeriodDefault`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Value of period used for Initialization.(in seconds).

####### ENUMERATION 类型参数

######## 1. PwmChannelClass

- **UUID**: `ECUC:31505abb-2296-4c99-bdb7-d0909f0440f2`
- **参数名**: `PwmChannelClass`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_FIXED_PERIOD` (来源: AUTOSAR_ECUC)
  - `PWM_FIXED_PERIOD_SHIFTED` (来源: AUTOSAR_ECUC)
  - `PWM_VARIABLE_PERIOD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Class of PWM Channel.

######## 2. PwmIdleState

- **UUID**: `ECUC:7cc25f83-b89c-4ba0-8766-7ba087185c97`
- **参数名**: `PwmIdleState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is stopped (e.g. call of Pwm_SetOutputToIdle).

######## 3. PwmPolarity

- **UUID**: `ECUC:a31896f1-a4ab-4dc8-a116-aff3df41810f`
- **参数名**: `PwmPolarity`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PWM_HIGH` (来源: AUTOSAR_ECUC)
  - `PWM_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the starting polarity of each PWM channel.

####### FUNCTION-NAME 类型参数

######## 1. PwmNotification

- **UUID**: `ECUC:44bb38ac-d409-4b1d-96be-ec84466c1019`
- **参数名**: `PwmNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `"NULL"`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the Callback function.

##### 3. PwmConfigurationOfOptApiServices

**容器属性**:

- **UUID**: `ECUC:946d9f33-9bb7-48d7-8278-0f6efdacfaeb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmConfigurationOfOptApiServices`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. PwmDeInitApi

- **UUID**: `ECUC:3e3da645-2c56-4fd5-9fe6-2b2cd88ed6d8`
- **参数名**: `PwmDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Pwm_DeInit() from the code.

######## 2. PwmGetOutputState

- **UUID**: `ECUC:8a7eb9e8-f5d3-4585-855b-72634c98da24`
- **参数名**: `PwmGetOutputState`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 3. PwmSetDutyCycle

- **UUID**: `ECUC:bf14870c-ef7a-4d27-a6c0-4ebd02c8fdfe`
- **参数名**: `PwmSetDutyCycle`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 4. PwmSetOutputToIdle

- **UUID**: `ECUC:45d9cbcc-c5b7-4c76-8469-5b65f7e9d6cd`
- **参数名**: `PwmSetOutputToIdle`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 5. PwmSetPeriodAndDuty

- **UUID**: `ECUC:bbb4cf88-5a3a-4053-8eae-023f3990279e`
- **参数名**: `PwmSetPeriodAndDuty`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 6. PwmVersionInfoApi

- **UUID**: `ECUC:33bfc216-9d93-4694-90c5-39340e82c758`
- **参数名**: `PwmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to indicate that the Pwm_ GetVersionInfo is supported

##### 4. PwmGeneral

**容器属性**:

- **UUID**: `ECUC:9e045944-b70f-48ae-9745-0344fa64c653`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PwmGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. PwmIndex

- **UUID**: `ECUC:1559f6dc-e859-4216-8c88-0f8836ae115e`
- **参数名**: `PwmIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. PwmDevErorDetect

- **UUID**: `ECUC:7ee4dbf7-92ca-43f8-bedf-cd012b1d5f01`
- **参数名**: `PwmDevErorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the development error detection.

######## 2. PwmDutycycleUpdatedEndperiod

- **UUID**: `ECUC:873477b1-c07e-4208-b92e-4e1875570984`
- **参数名**: `PwmDutycycleUpdatedEndperiod`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the update of the duty cycle parameter at the end of the current period.

######## 3. PwmNotificationSupported

- **UUID**: `ECUC:39804e4a-209d-4df8-ade1-4e0cd88cc57d`
- **参数名**: `PwmNotificationSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to indicate that the notifications are supported

######## 4. PwmPeriodUpdatedEndperiod

- **UUID**: `ECUC:da85e8d7-af3c-4ad4-a700-43ea0462bee4`
- **参数名**: `PwmPeriodUpdatedEndperiod`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the update of the period parameter at the end of the current period.

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

1. **Pwm**
