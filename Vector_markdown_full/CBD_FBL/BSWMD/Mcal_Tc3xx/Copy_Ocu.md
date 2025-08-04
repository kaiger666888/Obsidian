# Ocu - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:15

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Ocu](#ocu)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Ocu

#### 基本信息

- **UUID**: `ECUC:0af21bca-816d-40d5-81dc-c06db552bc20`
- **模块名称**: `Ocu`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of Ocu (Output Compare Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. OcuConfigSet

**容器属性**:

- **UUID**: `ECUC:708b6105-962d-46a4-86e6-92d896d5ecde`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container is the base of a Configuration Set, which contains the configured OCU channels. This way, different configuration sets can be defined for post-build process.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. OcuCountdirection

- **UUID**: `ECUC:c2bbb410-5753-45e3-a775-df91cb2517de`
- **参数名**: `OcuCountdirection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `OCU_UPCOUNTING`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `OCU_UPCOUNTING` (来源: AUTOSAR_ECUC)
- **描述**: This parameter indicates the count direction for the whole OCU driver.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. OcuChannel

**容器属性**:

- **UUID**: `ECUC:e88a1d0f-132b-4956-9864-707d68da3489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual OCU channel.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. OcuAssignedHardwareChannel

- **UUID**: `ECUC:9c795ca1-61ba-4c2d-827e-36de73c8bb13`
- **参数名**: `OcuAssignedHardwareChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The physical hardware channel that is assigned to this logical channel. This parameter is not-editable or not used. Hardware Channel is configured through GtmTimerUsed(../GtmTimerOutputModuleConfiguration/..)

########## 2. OcuChannelId

- **UUID**: `ECUC:886c0d42-b594-4a74-9900-ee040e4fc513`
- **参数名**: `OcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the OCU channel. This value will be assigned to the symbolic name derived from the OcuChannel container short name. It defines the assignment of the channel to the physical OCU hardware channel.

########## 3. OcuChannelTickDuration

- **UUID**: `ECUC:2a5c5bb3-5b7f-495b-bb9d-51402d46acb5`
- **参数名**: `OcuChannelTickDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..32768]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the tick duration of the counter of the channel. This parameter is the number of the input clock edges (rising edges or falling edges exclusively) counted each time to increase the counter by one unit.Note: This parameter is not-used,not editable and default value is set to 1

########## 4. OcuDefaultThreshold

- **UUID**: `ECUC:1720e99c-a652-4c42-9bf1-79676c4151a5`
- **参数名**: `OcuDefaultThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of comparison threshold used for Initialization.

########## 5. OcuHardwareTriggeredAdc

- **UUID**: `ECUC:954fd7bc-a2b9-4561-913e-e7f64009c0f9`
- **参数名**: `OcuHardwareTriggeredAdc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to allow the OCU channel to trigger an ADC channel upon compare match. The value of the parameter represents the ADC physical channel to trigger.

########## 6. OcuHardwareTriggeredDMA

- **UUID**: `ECUC:13fd5615-ebe0-4355-bbb7-c463a8d0cbca`
- **参数名**: `OcuHardwareTriggeredDMA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..127]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to allow the OCU channel to trigger a DMA channel upon compare match. The value of the parameter represents the DMA physical channel to trigger.

########## 7. OcuMaxCounterValue

- **UUID**: `ECUC:bdfef2e5-45dd-4d48-87d0-e1803b9ccc3d`
- **参数名**: `OcuMaxCounterValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum value in ticks, the counter of the OCU channel is able to count.

######### BOOLEAN 类型参数

########## 1. OcuOuptutPinUsed

- **UUID**: `ECUC:6e816ecb-78d9-4084-8954-6c4aeb5de2e2`
- **参数名**: `OcuOuptutPinUsed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information about the usage of an output pin on this channel.

######### ENUMERATION 类型参数

########## 1. OcuOutputPinDefaultState

- **UUID**: `ECUC:3cb6c8a7-1cfe-4a65-9f85-402d00d8688e`
- **参数名**: `OcuOutputPinDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `OCU_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `OCU_HIGH` (来源: AUTOSAR_ECUC)
  - `OCU_LOW` (来源: AUTOSAR_ECUC)
- **描述**: The parameter OcuOutputPinDefaultState represents the state that a pin associated with a channel shall be set to after initialisation.

######### FUNCTION-NAME 类型参数

########## 1. OcuNotification

- **UUID**: `ECUC:fa8b80e7-80af-46d6-ab00-4b4824f11ce6`
- **参数名**: `OcuNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..0]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Definition of a function pointer to a Callback function.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e1d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this OCU Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_OCU_DRIVER

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
  - `GTM_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS2` (来源: INFINEON_AURIX2G)
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

####### 2. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e1d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this OCU Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_OCU_DRIVER

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
  - `GTM_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS2` (来源: INFINEON_AURIX2G)
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

####### 3. OcuGroup

**容器属性**:

- **UUID**: `ECUC:9b03f8ea-f80b-42a8-b7f5-c9cb70869d68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuGroup`
- **多重性**: [0..1]

**容器描述**:

This container contains the parameters for configuring an OCU group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. OcuGroupId

- **UUID**: `ECUC:db2a2d12-e0af-424a-b1c8-e71aaa9259db`
- **参数名**: `OcuGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric ID of the group. This parameter is the symbolic name of the group.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. OcuGroupDefinition

- **UUID**: `ECUC:a93b7394-19f3-4b2b-9bee-21d741f7eb7c`
- **引用名**: `OcuGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of OcuChannels to an OcuGroup.

####### 4. OcuHWSpecificSettings

**容器属性**:

- **UUID**: `ECUC:dcea9ee9-4968-40fe-9ee6-bd4f9bea8e81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuHWSpecificSettings`
- **多重性**: [0..1]

**容器描述**:

This container contains Ocu-specific parameters for selecting the clock source and setting optional prescalers if supported by hardware.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. OcuClockSource

- **UUID**: `ECUC:cac98a9b-63c8-4156-85d9-bb801075e1b9`
- **参数名**: `OcuClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..0]
- **默认值**: `UNUSED`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: AUTOSAR_ECUC)
- **描述**: The OCU driver specific clock input for the unit can statically be configured to select different clock sources if provided by hardware. Enumeration literals are defined vendor specific.

########## 2. OcuPrescale

- **UUID**: `ECUC:52e0de61-eeaf-49f2-ada4-5e69b1b341a5`
- **参数名**: `OcuPrescale`
- **数据类型**: ENUMERATION
- **多重性**: [0..0]
- **默认值**: `UNUSED`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: AUTOSAR_ECUC)
- **描述**: Optional OCU driver specific clock prescale factor, if supported by hardware. Implementation is defined vendor specific.

##### 2. OcuChannel

**容器属性**:

- **UUID**: `ECUC:e88a1d0f-132b-4956-9864-707d68da3489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual OCU channel.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. OcuAssignedHardwareChannel

- **UUID**: `ECUC:9c795ca1-61ba-4c2d-827e-36de73c8bb13`
- **参数名**: `OcuAssignedHardwareChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The physical hardware channel that is assigned to this logical channel. This parameter is not-editable or not used. Hardware Channel is configured through GtmTimerUsed(../GtmTimerOutputModuleConfiguration/..)

######## 2. OcuChannelId

- **UUID**: `ECUC:886c0d42-b594-4a74-9900-ee040e4fc513`
- **参数名**: `OcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the OCU channel. This value will be assigned to the symbolic name derived from the OcuChannel container short name. It defines the assignment of the channel to the physical OCU hardware channel.

######## 3. OcuChannelTickDuration

- **UUID**: `ECUC:2a5c5bb3-5b7f-495b-bb9d-51402d46acb5`
- **参数名**: `OcuChannelTickDuration`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..32768]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the tick duration of the counter of the channel. This parameter is the number of the input clock edges (rising edges or falling edges exclusively) counted each time to increase the counter by one unit.Note: This parameter is not-used,not editable and default value is set to 1

######## 4. OcuDefaultThreshold

- **UUID**: `ECUC:1720e99c-a652-4c42-9bf1-79676c4151a5`
- **参数名**: `OcuDefaultThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of comparison threshold used for Initialization.

######## 5. OcuHardwareTriggeredAdc

- **UUID**: `ECUC:954fd7bc-a2b9-4561-913e-e7f64009c0f9`
- **参数名**: `OcuHardwareTriggeredAdc`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..383]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to allow the OCU channel to trigger an ADC channel upon compare match. The value of the parameter represents the ADC physical channel to trigger.

######## 6. OcuHardwareTriggeredDMA

- **UUID**: `ECUC:13fd5615-ebe0-4355-bbb7-c463a8d0cbca`
- **参数名**: `OcuHardwareTriggeredDMA`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..127]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to allow the OCU channel to trigger a DMA channel upon compare match. The value of the parameter represents the DMA physical channel to trigger.

######## 7. OcuMaxCounterValue

- **UUID**: `ECUC:bdfef2e5-45dd-4d48-87d0-e1803b9ccc3d`
- **参数名**: `OcuMaxCounterValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum value in ticks, the counter of the OCU channel is able to count.

####### BOOLEAN 类型参数

######## 1. OcuOuptutPinUsed

- **UUID**: `ECUC:6e816ecb-78d9-4084-8954-6c4aeb5de2e2`
- **参数名**: `OcuOuptutPinUsed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information about the usage of an output pin on this channel.

####### ENUMERATION 类型参数

######## 1. OcuOutputPinDefaultState

- **UUID**: `ECUC:3cb6c8a7-1cfe-4a65-9f85-402d00d8688e`
- **参数名**: `OcuOutputPinDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `OCU_LOW`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `OCU_HIGH` (来源: AUTOSAR_ECUC)
  - `OCU_LOW` (来源: AUTOSAR_ECUC)
- **描述**: The parameter OcuOutputPinDefaultState represents the state that a pin associated with a channel shall be set to after initialisation.

####### FUNCTION-NAME 类型参数

######## 1. OcuNotification

- **UUID**: `ECUC:fa8b80e7-80af-46d6-ab00-4b4824f11ce6`
- **参数名**: `OcuNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..0]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Definition of a function pointer to a Callback function.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e1d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this OCU Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_OCU_DRIVER

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
  - `GTM_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS2` (来源: INFINEON_AURIX2G)
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

##### 3. GtmTimerOutputModuleConfiguration

**容器属性**:

- **UUID**: `ECUC:c2253a76-e1d8-4a8f-b303-ce80ffc0e870`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerOutputModuleConfiguration`
- **多重性**: [0..1]

**容器描述**:

Choose GTM TOM/ATOM channel which will be used by this OCU Channel.                              Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_OCU_DRIVER

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
  - `GTM_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `GTM_TBU_TS2` (来源: INFINEON_AURIX2G)
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

##### 4. OcuGroup

**容器属性**:

- **UUID**: `ECUC:9b03f8ea-f80b-42a8-b7f5-c9cb70869d68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuGroup`
- **多重性**: [0..1]

**容器描述**:

This container contains the parameters for configuring an OCU group.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. OcuGroupId

- **UUID**: `ECUC:db2a2d12-e0af-424a-b1c8-e71aaa9259db`
- **参数名**: `OcuGroupId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric ID of the group. This parameter is the symbolic name of the group.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. OcuGroupDefinition

- **UUID**: `ECUC:a93b7394-19f3-4b2b-9bee-21d741f7eb7c`
- **引用名**: `OcuGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Ocu/OcuConfigSet/OcuChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Assignment of OcuChannels to an OcuGroup.

##### 5. OcuHWSpecificSettings

**容器属性**:

- **UUID**: `ECUC:dcea9ee9-4968-40fe-9ee6-bd4f9bea8e81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuHWSpecificSettings`
- **多重性**: [0..1]

**容器描述**:

This container contains Ocu-specific parameters for selecting the clock source and setting optional prescalers if supported by hardware.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. OcuClockSource

- **UUID**: `ECUC:cac98a9b-63c8-4156-85d9-bb801075e1b9`
- **参数名**: `OcuClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..0]
- **默认值**: `UNUSED`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: AUTOSAR_ECUC)
- **描述**: The OCU driver specific clock input for the unit can statically be configured to select different clock sources if provided by hardware. Enumeration literals are defined vendor specific.

######## 2. OcuPrescale

- **UUID**: `ECUC:52e0de61-eeaf-49f2-ada4-5e69b1b341a5`
- **参数名**: `OcuPrescale`
- **数据类型**: ENUMERATION
- **多重性**: [0..0]
- **默认值**: `UNUSED`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UNUSED` (来源: AUTOSAR_ECUC)
- **描述**: Optional OCU driver specific clock prescale factor, if supported by hardware. Implementation is defined vendor specific.

##### 6. OcuConfigurationOfOptionalApis

**容器属性**:

- **UUID**: `ECUC:3b497cda-e5be-4ddd-a1eb-b03026591a87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuConfigurationOfOptionalApis`
- **多重性**: [0..1]

**容器描述**:

Configuration of optional APIs.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. OcuDeInitApi

- **UUID**: `ECUC:ece1e485-7112-4cc3-af64-f9e7d1c5f761`
- **参数名**: `OcuDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_DeInit() from the code.

######## 2. OcuGetCounterApi

- **UUID**: `ECUC:2b6a491c-9f49-4ce5-8bb5-ebc72f7acd8a`
- **参数名**: `OcuGetCounterApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_GetCounter() from the code.

######## 3. OcuNotificationSupported

- **UUID**: `ECUC:a078c655-6060-433b-8e43-e007388c733b`
- **参数名**: `OcuNotificationSupported`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Ocu_EnableNotification() and Ocu_DisableNotification() from the code.

######## 4. OcuSetAbsoluteThresholdApi

- **UUID**: `ECUC:1d04356b-a77f-4adc-b124-141cd519ad93`
- **参数名**: `OcuSetAbsoluteThresholdApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_SetAbsoluteThreshold() from the code.

######## 5. OcuSetPinActionApi

- **UUID**: `ECUC:fcab4421-8eda-4da4-9c69-24801273fab7`
- **参数名**: `OcuSetPinActionApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_SetPinAction() from the code.

######## 6. OcuSetPinStateApi

- **UUID**: `ECUC:c36e8660-4995-4cbe-b664-645a361723c9`
- **参数名**: `OcuSetPinStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_SetPinState() from the code.

######## 7. OcuSetRelativeThresholdApi

- **UUID**: `ECUC:aa3df9f3-f48b-402f-b1a2-e05546637c64`
- **参数名**: `OcuSetRelativeThresholdApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_SetRelativeThreshold() from the code.

######## 8. OcuVersionInfoApi

- **UUID**: `ECUC:aece3736-8fed-4937-8fa3-90f560dc6b2c`
- **参数名**: `OcuVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch to indicate that the Ocu_GetVersionInfo() is supported.

######## 9. OcuInitCheckApi

- **UUID**: `ECUC:4d3911ac-2595-4dc7-a69e-66453109d78a`
- **参数名**: `OcuInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Ocu_InitCheck() from the code.
                            true: Ocu_InitCheck() can be used.
                            false: Ocu_InitCheck() can not be used.

##### 7. OcuGeneral

**容器属性**:

- **UUID**: `ECUC:95eb7fd8-be1a-4fc7-b857-a748a2ba401d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `OcuGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the module-wide configuration parameters of the OCU Driver.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. OcuDevErrorDetect

- **UUID**: `ECUC:fa74e280-1309-474e-a17f-06568b6c5212`
- **参数名**: `OcuDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. OcuMultiCoreErrorDetect

- **UUID**: `ECUC:7224bf75-cdc8-408f-1111-9e7118a84`
- **参数名**: `OcuMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the MultiCore Development Error Detection on or off. true: Enabled. false: Disabled.

######## 3. OcuSafetyEnable

- **UUID**: `be837339-bdd5-4cda-123w-54e2011c110a`
- **参数名**: `OcuSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch for enabling/Disabling OcuSafetyEnable

##### 8. CommonPublishedInformation

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
- **作用域**: LOCAL
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
- **作用域**: LOCAL
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
- **作用域**: LOCAL
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
- **作用域**: LOCAL
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
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `125`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
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
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix derivative used for the implementation

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

1. **Ocu**
