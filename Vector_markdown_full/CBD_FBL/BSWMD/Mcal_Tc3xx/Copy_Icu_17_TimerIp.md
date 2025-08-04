# Icu - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:13

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Icu](#icu)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Icu

#### 基本信息

- **UUID**: `ECUC:9d858769-7cc7-46c3-941e-129083aef5cb`
- **模块名称**: `Icu`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the Icu (Input Capture Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. IcuConfigSet

**容器属性**:

- **UUID**: `65a6f4ae-155b-4591-a60b-3f0347afebd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuConfigSet`
- **多重性**: [0..1]

**容器描述**:

This container is the base for a multiple configuration set

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IcuMaxChannel

- **UUID**: `ECUC:65e2f79c-922e-4180-90dc-0819fc20f890`
- **参数名**: `IcuMaxChannel`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter contains the number of Channels configured. It will be gathered by tools during the configuration stage.
                            calculation Formula = Number of configured Icu Channels Implementation Type: Icu_ChannelType. 
                            This parameter doesn't have any influence on the generated
                            code file

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. IcuChannel

**容器属性**:

- **UUID**: `ECUC:74f0ce69-2156-4784-bae9-57ea4699e6e4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual ICU channel.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IcuChannelId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `IcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the IcuChannel container short name.

######### BOOLEAN 类型参数

########## 1. IcuWakeupCapability

- **UUID**: `3d13cb29-7981-4b70-b47a-e845a87a133e`
- **参数名**: `IcuWakeupCapability`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information about the wakeup-capability of this channel.
                          true: Channel is wakeup capable.
                          false: Channel is not wakeup capable.

######### ENUMERATION 类型参数

########## 1. IcuDefaultStartEdge

- **UUID**: `ECUC:29f03c55-e634-4f63-90cf-2027f4cd10f1`
- **参数名**: `IcuDefaultStartEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ICU_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ICU_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures the default-activation-edge which shall be used for this channel if there was no activation-edge configured by the call of service Icu_SetActivationCondition().For PERIOD signal measurement, the configured edge is the start of period. For DUTY measurement, the configured edge is the start of Active time and period. Both Edges can not be configured for PERIOD. For DUTY measurement, BOTH EDGES, First edge seen after call of Icu_StartSignalMeasurement is considered as the start of measurement. The parameter is un-editable for HIGH TIME and LOW TIME measurement. Implementation Type: Icu_ActivationType

########## 2. IcuMeasurementMode

- **UUID**: `ECUC:b9e816ea-2297-4329-8830-328ccdeabda3`
- **参数名**: `IcuMeasurementMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_MODE_SIGNAL_EDGE_DETECT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_MODE_EDGE_COUNTER` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_EDGE_DETECT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_MEASUREMENT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_TIMESTAMP` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_INCREMENTAL_INTERFACE` (来源: AUTOSAR_ECUC)
- **描述**: Configures the measurement mode of this channel.
                             Implementation Type: Icu_MeasurementModeType

########## 3. IcuAssignedHwUnit

- **UUID**: `7e52945f-67bf-490d-9478-754ff8913bc0`
- **参数名**: `IcuAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GTM` (来源: INFINEON_AURIX2G)
  - `CCU6` (来源: INFINEON_AURIX2G)
  - `ERU` (来源: INFINEON_AURIX2G)
  - `GPT12` (来源: INFINEON_AURIX2G)
- **描述**: The HW resource required for the measurement.
                                   TIM, ERU and CCU

######## 配置容器

本模块包含 **11** 个配置容器：

######### 1. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. IcuSignalNotification

- **UUID**: `a2f4d444-95fa-48c1-b6de-ae42f4e51f0e`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function for signal notification.

######### 2. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LOW_TIME`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **描述**: Configures the property that could be measured in case the mode is IcuSignalMeasurement.
                                This property can not be changed during runtime.Implementation Type: Icu_SignalMeasurementPropertyType

######### 3. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LINEAR_BUFFER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **描述**: Configures the handling of the buffer in case the mode is Timestamp; Implementation Type: Icu_TimestampBufferType

########### FUNCTION-NAME 类型参数

############ 1. IcuTimestampNotification

- **UUID**: `594bd914-d64a-476a-8b5e-b5ae10c32a35`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function if the number of requested timestamps (Notification interval is greater 0) are acquired.

######### 4. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) needed to configure a wakeup capable channel

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. IcuChannelWakeupInfo

- **UUID**: `ECUC:f78189c5-99ae-4266-ba74-122fb3ce7b26`
- **引用名**: `IcuChannelWakeupInfo`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM).
                              Implementation Type: reference to EcuM_WakeupSourceType

######### 5. GtmTimerInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-94523f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGtmTimChannelAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTimAllocationConf/McuGtmTimChannelAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

############# ENUMERATION 类型参数

############## 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

############## 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

############## 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

############## 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

############## 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

########### 2. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

############## 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

############# BOOLEAN 类型参数

############## 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

############# ENUMERATION 类型参数

############## 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

############## 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

############## 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

######### 6. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

########### ENUMERATION 类型参数

############ 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

############ 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

############ 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

############ 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

############ 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

######### 7. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

############ 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

########### BOOLEAN 类型参数

############ 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

########### ENUMERATION 类型参数

############ 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

############ 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

############ 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

######### 8. CCU6CC6Configuration

**容器属性**:

- **UUID**: `e150fb37-a611-4a0f-8b78-9451218b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. Cc6xChannel

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

############ 2. CCChannelInputSelection

- **UUID**: `b209c80f-87bd-422e-8f00-fa776e66e9fb`
- **参数名**: `CCChannelInputSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCINA_PORT2_PIN0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCINA_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN6` (来源: INFINEON_AURIX2G)
  - `CCIND_EVR_WUT_TRIGGER_O` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU4_PDOUT4` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_CAN0_INTR12` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN9` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU5_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: Input Selection for CCx channel.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l77-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

############# BOOLEAN 类型参数

############## 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

############# ENUMERATION 类型参数

############## 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

######### 9. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### BOOLEAN 类型参数

############ 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### ENUMERATION 类型参数

############ 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

######### 10. ERUInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-91123f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ERUInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the ERS and OGU Configuration

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EruInputPin

- **UUID**: `20ee392a-1640-45fd-80f2-0c6bd7d1ef0d`
- **参数名**: `EruInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERU_INPUT0A_PORT15_PIN4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ERU_INPUT0A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0C_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1C_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2A_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2C_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3A_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3B_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3C_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4A_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4D_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5A_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6A_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6B_ESR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6D_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7A_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7B_ESR1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7C_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: Eru Input selection for the ERU unit

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. EruErsReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruErsReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the ERU channels (ERS and OGU).

############ 2. EruOguReference

- **UUID**: `ECUC:c945dd5e-1l78-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruOguReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######### 11. GPT12Configuration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-9drt3f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GPT12Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the GPT12 Configuration for GPT12

########## 参数配置

此容器包含 **3** 个参数：

########### ENUMERATION 类型参数

############ 1. GPT12InputPortSelection

- **UUID**: `20e392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12InputPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12_T2INA_PORT00_PIN7`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GPT12_T2INA_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T2INB_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INA_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INB_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INC_SCU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INA_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INB_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INA_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INB_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INA_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INB_PORT10_PIN2` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Input selection for the GPT12 unit

############ 2. GPT12DirPortSelection

- **UUID**: `20d392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12DirPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `NONE` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDA_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDB_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDA_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDB_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDA_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDB_PORT33_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Direction Input selection for the GPT12 unit

############ 3. GPT12CounterType

- **UUID**: `20d392b-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12CounterType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_1_COUNT_INPUT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ICU_1_COUNT_INPUT` (来源: INFINEON_AURIX2G)
  - `ICU_2_COUNT_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Counting mechanism

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. GPT12BlockReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4sdeec1185`
- **引用名**: `GPT12BlockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGpt12ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GPT12 timer channels Block.

####### 2. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. IcuSignalNotification

- **UUID**: `a2f4d444-95fa-48c1-b6de-ae42f4e51f0e`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function for signal notification.

####### 3. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LOW_TIME`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **描述**: Configures the property that could be measured in case the mode is IcuSignalMeasurement.
                                This property can not be changed during runtime.Implementation Type: Icu_SignalMeasurementPropertyType

####### 4. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LINEAR_BUFFER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **描述**: Configures the handling of the buffer in case the mode is Timestamp; Implementation Type: Icu_TimestampBufferType

######### FUNCTION-NAME 类型参数

########## 1. IcuTimestampNotification

- **UUID**: `594bd914-d64a-476a-8b5e-b5ae10c32a35`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function if the number of requested timestamps (Notification interval is greater 0) are acquired.

####### 5. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) needed to configure a wakeup capable channel

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. IcuChannelWakeupInfo

- **UUID**: `ECUC:f78189c5-99ae-4266-ba74-122fb3ce7b26`
- **引用名**: `IcuChannelWakeupInfo`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM).
                              Implementation Type: reference to EcuM_WakeupSourceType

####### 6. GtmTimerInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-94523f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGtmTimChannelAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTimAllocationConf/McuGtmTimChannelAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

########### ENUMERATION 类型参数

############ 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

############ 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

############ 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

############ 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

############ 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

######### 2. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

############ 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

########### BOOLEAN 类型参数

############ 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

########### ENUMERATION 类型参数

############ 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

############ 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

############ 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

####### 7. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

######### ENUMERATION 类型参数

########## 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

########## 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

########## 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

########## 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

########## 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

####### 8. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

########## 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

######### BOOLEAN 类型参数

########## 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

######### ENUMERATION 类型参数

########## 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

########## 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

########## 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

####### 9. CCU6CC6Configuration

**容器属性**:

- **UUID**: `e150fb37-a611-4a0f-8b78-9451218b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. Cc6xChannel

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

########## 2. CCChannelInputSelection

- **UUID**: `b209c80f-87bd-422e-8f00-fa776e66e9fb`
- **参数名**: `CCChannelInputSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCINA_PORT2_PIN0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCINA_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN6` (来源: INFINEON_AURIX2G)
  - `CCIND_EVR_WUT_TRIGGER_O` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU4_PDOUT4` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_CAN0_INTR12` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN9` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU5_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: Input Selection for CCx channel.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l77-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### BOOLEAN 类型参数

############ 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### ENUMERATION 类型参数

############ 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

####### 10. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### BOOLEAN 类型参数

########## 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### ENUMERATION 类型参数

########## 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

####### 11. ERUInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-91123f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ERUInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the ERS and OGU Configuration

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EruInputPin

- **UUID**: `20ee392a-1640-45fd-80f2-0c6bd7d1ef0d`
- **参数名**: `EruInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERU_INPUT0A_PORT15_PIN4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ERU_INPUT0A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0C_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1C_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2A_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2C_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3A_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3B_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3C_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4A_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4D_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5A_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6A_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6B_ESR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6D_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7A_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7B_ESR1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7C_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: Eru Input selection for the ERU unit

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. EruErsReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruErsReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the ERU channels (ERS and OGU).

########## 2. EruOguReference

- **UUID**: `ECUC:c945dd5e-1l78-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruOguReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 12. GPT12Configuration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-9drt3f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GPT12Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the GPT12 Configuration for GPT12

######## 参数配置

此容器包含 **3** 个参数：

######### ENUMERATION 类型参数

########## 1. GPT12InputPortSelection

- **UUID**: `20e392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12InputPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12_T2INA_PORT00_PIN7`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GPT12_T2INA_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T2INB_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INA_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INB_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INC_SCU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INA_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INB_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INA_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INB_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INA_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INB_PORT10_PIN2` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Input selection for the GPT12 unit

########## 2. GPT12DirPortSelection

- **UUID**: `20d392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12DirPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `NONE` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDA_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDB_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDA_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDB_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDA_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDB_PORT33_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Direction Input selection for the GPT12 unit

########## 3. GPT12CounterType

- **UUID**: `20d392b-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12CounterType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_1_COUNT_INPUT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ICU_1_COUNT_INPUT` (来源: INFINEON_AURIX2G)
  - `ICU_2_COUNT_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Counting mechanism

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GPT12BlockReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4sdeec1185`
- **引用名**: `GPT12BlockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGpt12ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GPT12 timer channels Block.

##### 2. IcuChannel

**容器属性**:

- **UUID**: `ECUC:74f0ce69-2156-4784-bae9-57ea4699e6e4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuChannel`
- **多重性**: [1..1]

**容器描述**:

Configuration of an individual ICU channel.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. IcuChannelId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `IcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the IcuChannel container short name.

####### BOOLEAN 类型参数

######## 1. IcuWakeupCapability

- **UUID**: `3d13cb29-7981-4b70-b47a-e845a87a133e`
- **参数名**: `IcuWakeupCapability`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Information about the wakeup-capability of this channel.
                          true: Channel is wakeup capable.
                          false: Channel is not wakeup capable.

####### ENUMERATION 类型参数

######## 1. IcuDefaultStartEdge

- **UUID**: `ECUC:29f03c55-e634-4f63-90cf-2027f4cd10f1`
- **参数名**: `IcuDefaultStartEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_RISING_EDGE`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ICU_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ICU_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **描述**: Configures the default-activation-edge which shall be used for this channel if there was no activation-edge configured by the call of service Icu_SetActivationCondition().For PERIOD signal measurement, the configured edge is the start of period. For DUTY measurement, the configured edge is the start of Active time and period. Both Edges can not be configured for PERIOD. For DUTY measurement, BOTH EDGES, First edge seen after call of Icu_StartSignalMeasurement is considered as the start of measurement. The parameter is un-editable for HIGH TIME and LOW TIME measurement. Implementation Type: Icu_ActivationType

######## 2. IcuMeasurementMode

- **UUID**: `ECUC:b9e816ea-2297-4329-8830-328ccdeabda3`
- **参数名**: `IcuMeasurementMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_MODE_SIGNAL_EDGE_DETECT`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_MODE_EDGE_COUNTER` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_EDGE_DETECT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_MEASUREMENT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_TIMESTAMP` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_INCREMENTAL_INTERFACE` (来源: AUTOSAR_ECUC)
- **描述**: Configures the measurement mode of this channel.
                             Implementation Type: Icu_MeasurementModeType

######## 3. IcuAssignedHwUnit

- **UUID**: `7e52945f-67bf-490d-9478-754ff8913bc0`
- **参数名**: `IcuAssignedHwUnit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM`
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GTM` (来源: INFINEON_AURIX2G)
  - `CCU6` (来源: INFINEON_AURIX2G)
  - `ERU` (来源: INFINEON_AURIX2G)
  - `GPT12` (来源: INFINEON_AURIX2G)
- **描述**: The HW resource required for the measurement.
                                   TIM, ERU and CCU

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. IcuSignalNotification

- **UUID**: `a2f4d444-95fa-48c1-b6de-ae42f4e51f0e`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function for signal notification.

####### 2. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LOW_TIME`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **描述**: Configures the property that could be measured in case the mode is IcuSignalMeasurement.
                                This property can not be changed during runtime.Implementation Type: Icu_SignalMeasurementPropertyType

####### 3. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LINEAR_BUFFER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **描述**: Configures the handling of the buffer in case the mode is Timestamp; Implementation Type: Icu_TimestampBufferType

######### FUNCTION-NAME 类型参数

########## 1. IcuTimestampNotification

- **UUID**: `594bd914-d64a-476a-8b5e-b5ae10c32a35`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function if the number of requested timestamps (Notification interval is greater 0) are acquired.

####### 4. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) needed to configure a wakeup capable channel

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. IcuChannelWakeupInfo

- **UUID**: `ECUC:f78189c5-99ae-4266-ba74-122fb3ce7b26`
- **引用名**: `IcuChannelWakeupInfo`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM).
                              Implementation Type: reference to EcuM_WakeupSourceType

####### 5. GtmTimerInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-94523f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGtmTimChannelAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTimAllocationConf/McuGtmTimChannelAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

########### ENUMERATION 类型参数

############ 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

############ 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

############ 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

############ 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

############ 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

######### 2. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

############ 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

########### BOOLEAN 类型参数

############ 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

########### ENUMERATION 类型参数

############ 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

############ 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

############ 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

####### 6. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

######### ENUMERATION 类型参数

########## 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

########## 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

########## 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

########## 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

########## 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

####### 7. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

########## 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

######### BOOLEAN 类型参数

########## 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

######### ENUMERATION 类型参数

########## 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

########## 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

########## 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

####### 8. CCU6CC6Configuration

**容器属性**:

- **UUID**: `e150fb37-a611-4a0f-8b78-9451218b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. Cc6xChannel

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

########## 2. CCChannelInputSelection

- **UUID**: `b209c80f-87bd-422e-8f00-fa776e66e9fb`
- **参数名**: `CCChannelInputSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCINA_PORT2_PIN0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCINA_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN6` (来源: INFINEON_AURIX2G)
  - `CCIND_EVR_WUT_TRIGGER_O` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU4_PDOUT4` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_CAN0_INTR12` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN9` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU5_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: Input Selection for CCx channel.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l77-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### BOOLEAN 类型参数

############ 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

########### ENUMERATION 类型参数

############ 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

####### 9. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### BOOLEAN 类型参数

########## 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### ENUMERATION 类型参数

########## 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

####### 10. ERUInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-91123f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ERUInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the ERS and OGU Configuration

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EruInputPin

- **UUID**: `20ee392a-1640-45fd-80f2-0c6bd7d1ef0d`
- **参数名**: `EruInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERU_INPUT0A_PORT15_PIN4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ERU_INPUT0A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0C_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1C_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2A_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2C_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3A_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3B_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3C_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4A_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4D_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5A_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6A_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6B_ESR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6D_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7A_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7B_ESR1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7C_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: Eru Input selection for the ERU unit

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. EruErsReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruErsReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the ERU channels (ERS and OGU).

########## 2. EruOguReference

- **UUID**: `ECUC:c945dd5e-1l78-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruOguReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

####### 11. GPT12Configuration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-9drt3f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GPT12Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the GPT12 Configuration for GPT12

######## 参数配置

此容器包含 **3** 个参数：

######### ENUMERATION 类型参数

########## 1. GPT12InputPortSelection

- **UUID**: `20e392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12InputPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12_T2INA_PORT00_PIN7`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GPT12_T2INA_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T2INB_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INA_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INB_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INC_SCU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INA_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INB_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INA_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INB_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INA_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INB_PORT10_PIN2` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Input selection for the GPT12 unit

########## 2. GPT12DirPortSelection

- **UUID**: `20d392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12DirPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `NONE` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDA_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDB_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDA_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDB_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDA_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDB_PORT33_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Direction Input selection for the GPT12 unit

########## 3. GPT12CounterType

- **UUID**: `20d392b-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12CounterType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_1_COUNT_INPUT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ICU_1_COUNT_INPUT` (来源: INFINEON_AURIX2G)
  - `ICU_2_COUNT_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Counting mechanism

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. GPT12BlockReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4sdeec1185`
- **引用名**: `GPT12BlockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGpt12ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GPT12 timer channels Block.

##### 3. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. IcuSignalNotification

- **UUID**: `a2f4d444-95fa-48c1-b6de-ae42f4e51f0e`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function for signal notification.

##### 4. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LOW_TIME`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **描述**: Configures the property that could be measured in case the mode is IcuSignalMeasurement.
                                This property can not be changed during runtime.Implementation Type: Icu_SignalMeasurementPropertyType

##### 5. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_LINEAR_BUFFER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **描述**: Configures the handling of the buffer in case the mode is Timestamp; Implementation Type: Icu_TimestampBufferType

####### FUNCTION-NAME 类型参数

######## 1. IcuTimestampNotification

- **UUID**: `594bd914-d64a-476a-8b5e-b5ae10c32a35`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
  - 默认值: `NULL`
- **描述**: Notification function if the number of requested timestamps (Notification interval is greater 0) are acquired.

##### 6. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration (parameters) needed to configure a wakeup capable channel

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. IcuChannelWakeupInfo

- **UUID**: `ECUC:f78189c5-99ae-4266-ba74-122fb3ce7b26`
- **引用名**: `IcuChannelWakeupInfo`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM).
                              Implementation Type: reference to EcuM_WakeupSourceType

##### 7. GtmTimerInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-94523f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GtmTimerInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. GtmTimerUsed

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `GtmTimerUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGtmTimChannelAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGtmAllocationConf/McuGtmTimAllocationConf/McuGtmTimChannelAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

######### ENUMERATION 类型参数

########## 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

########## 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

########## 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

########## 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

########## 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

####### 2. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

########## 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

######### BOOLEAN 类型参数

########## 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

######### ENUMERATION 类型参数

########## 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

########## 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

########## 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

##### 8. TimChannelGeneral

**容器属性**:

- **UUID**: `07f27c5d-7c2e-40d3-ae46-40ba97792032`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelGeneral`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Channel General Configuration

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. OverflowISRThreshold

- **UUID**: `fb29b6d7-d3b5-4c98-bac8-b674b47368e0`
- **参数名**: `OverflowISRThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt and execution flow entering ICU ISR. User must configure the threshold to contain the maximum latency and must be lesser than the actual measured time. The threshold will be in the ticks of the CMU_CLK selected for that TIM channel.                                               The threshold should consider interrupt latency, other high priority interrupts and the latency to reach the ICU ISR.                                               The threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.

####### ENUMERATION 类型参数

######## 1. TimChannelInputSelect

- **UUID**: `44b6b528-6240-4ba6-85c5-9cb69b213850`
- **参数名**: `TimChannelInputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `INPUT_OF_CURRENT_TIM_CHANNEL`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `INPUT_OF_CURRENT_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
  - `INPUT_OF_PREVIOUS_TIM_CHANNEL` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Input for the channel
                                    INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM Channel will be the input assigned to this channel.
                                    INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM channel will be the input assigned to the previous channel. Please note, the Port and Pin number applicable in this case is
                                    the configuration in TimChannelPortPinSelect for the previous channel and not the Port and Pin configured for this channel.

######## 2. TimChannelPortPinSelect

- **UUID**: `e48606de-7745-414d-8cc2-cb606e877ec0`
- **参数名**: `TimChannelPortPinSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `SEL0_NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `SEL0_NONE` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT14_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT14_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT14_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT33_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT33_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT11_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT32_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT20_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT15_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT14_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT11_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT20_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT13_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT11_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT33_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT00_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT33_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL6_PORT22_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT21_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL13_PORT10_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT02_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL7_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN12` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT02_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL15_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL14_PORT33_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT33_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN13` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT11_PIN14` (来源: INFINEON_AURIX2G)
  - `SEL5_PORT11_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT34_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT14_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL4_PORT22_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT33_PIN15` (来源: INFINEON_AURIX2G)
  - `SEL8_PORT22_PIN10` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT22_PIN11` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT34_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL3_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT00_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL9_PORT32_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT34_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL12_PORT21_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT01_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL10_PORT00_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL11_PORT21_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN6` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN7` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN5` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN8` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN4` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT23_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT23_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN3` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN2` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL2_PORT12_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT22_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT12_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN0` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN1` (来源: INFINEON_AURIX2G)
  - `SEL1_PORT11_PIN4` (来源: INFINEON_AURIX2G)
- **描述**: This decides the input port and pin of the TIM Channel. This value is applicable for this channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'

######## 3. TimChannelClockSelect

- **UUID**: `e0e8a863-d29f-42c9-b32f-be917ae6b680`
- **参数名**: `TimChannelClockSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_2` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_3` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_4` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_5` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Clock Source for TIM Channel

######## 4. TimChannelGpr0InputSelect

- **UUID**: `f11c7a62-fff8-4374-8a96-ff336d21ecf8`
- **参数名**: `TimChannelGpr0InputSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TIMEBASE_TBU_TS0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `TIMEBASE_TBU_TS0` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS1` (来源: INFINEON_AURIX2G)
  - `TIMEBASE_TBU_TS2` (来源: INFINEON_AURIX2G)
- **描述**: This decides the value captured in GPR0 register of TIM Channel.

######## 5. TimInterruptMode

- **UUID**: `fb29b6d7-d3b5-4c88-bac8-b674b47368e0`
- **参数名**: `TimInterruptMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_INTERRUPT_LEVEL_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_INTERRUPT_LEVEL_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_PULSE_NOTIFY_MODE` (来源: INFINEON_AURIX2G)
  - `GTM_INTERRUPT_SINGLE_PULSE_MODE` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Interrupt mode to use.

##### 9. TimChannelFilterConfig

**容器属性**:

- **UUID**: `216ef17c-7539-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TimChannelFilterConfig`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. TimChFilterTimeForRisingEdge

- **UUID**: `0a65f41c-4dc1-4a76-a655-00015d757948`
- **参数名**: `TimChFilterTimeForRisingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input

######## 2. TimChFilterTimeForFallingEdge

- **UUID**: `64bac732-bc38-4036-8f60-b61b2d3cc02c`
- **参数名**: `TimChFilterTimeForFallingEdge`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..16777215]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input

####### BOOLEAN 类型参数

######## 1. TimChannelFilterEnable

- **UUID**: `202f45ca-cad5-4170-a515-56eb752ea787`
- **参数名**: `TimChannelFilterEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enables Filter for the Channel. This sets FLT_EN for the channel

####### ENUMERATION 类型参数

######## 1. TimChFilterCounterFreqSelect

- **UUID**: `a4b65ef9-e5b3-4c4e-8001-b73efdfdd8ca`
- **参数名**: `TimChFilterCounterFreqSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GTM_CONFIGURABLE_CLOCK_0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `GTM_CONFIGURABLE_CLOCK_0` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_1` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_6` (来源: INFINEON_AURIX2G)
  - `GTM_CONFIGURABLE_CLOCK_7` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ for the channel

######## 2. TimChFilterModeForRisingEdge

- **UUID**: `e6287088-6c79-45db-a7fb-06d1898fa79b`
- **参数名**: `TimChFilterModeForRisingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Rising Edge of the TIM Channel Input

######## 3. TimChFilterModeForFallingEdge

- **UUID**: `89102148-5155-4a8a-ae12-7862c001ded2`
- **参数名**: `TimChFilterModeForFallingEdge`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `IMMEDIATE_EDGE_PROPAGATION_MODE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `IMMEDIATE_EDGE_PROPAGATION_MODE` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_UPDOWN_COUNTER` (来源: INFINEON_AURIX2G)
  - `DEGLITCH_WITH_HOLD_COUNTER` (来源: INFINEON_AURIX2G)
- **描述**: This decides the Filter Mode for Falling Edge of the TIM Channel Input

##### 10. CCU6CC6Configuration

**容器属性**:

- **UUID**: `e150fb37-a611-4a0f-8b78-9451218b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6CC6Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the TIM Configuration for GTM

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. Cc6xChannel

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

######## 2. CCChannelInputSelection

- **UUID**: `b209c80f-87bd-422e-8f00-fa776e66e9fb`
- **参数名**: `CCChannelInputSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CCINA_PORT2_PIN0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `CCINA_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN6` (来源: INFINEON_AURIX2G)
  - `CCIND_EVR_WUT_TRIGGER_O` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT2_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU4_PDOUT4` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN1` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN0` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN7` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN3` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN2` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN8` (来源: INFINEON_AURIX2G)
  - `CCIND_CAN0_INTR12` (来源: INFINEON_AURIX2G)
  - `CCINA_PORT0_PIN5` (来源: INFINEON_AURIX2G)
  - `CCINB_PORT2_PIN4` (来源: INFINEON_AURIX2G)
  - `CCINC_PORT0_PIN9` (来源: INFINEON_AURIX2G)
  - `CCIND_ERU_OGU5_PDOUT5` (来源: INFINEON_AURIX2G)
- **描述**: Input Selection for CCx channel.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CCU6KernelUsed

- **UUID**: `ECUC:c945dd5e-1l77-4bcc-a8ab-0a4d19ec3585`
- **引用名**: `CCU6KernelUsed`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuCcu6ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuCcu6ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the CCU6 kernels

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### BOOLEAN 类型参数

########## 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

######### ENUMERATION 类型参数

########## 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

##### 11. CCU6xParameters

**容器属性**:

- **UUID**: `216ef17c-7569-4d9d-845b-a170143c9466`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CCU6xParameters`
- **多重性**: [0..1]

**容器描述**:

This holds the filter specific configurations for the channels.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. T12ClkSelection

- **UUID**: `DCE:981b87c5-759d-60cb-b3df-3af8acac9564`
- **参数名**: `T12ClkSelection`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: INFINEON_AURIX2G
- **描述**: T12 configuration - clock selection
                                    if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

####### BOOLEAN 类型参数

######## 1. T12PrescalerEnabled

- **UUID**: `DCE:30a57b07-9296-6398-aa9a-1f0cd7ca53e2`
- **参数名**: `T12PrescalerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: INFINEON_AURIX2G
- **描述**: if T12PrescalerEnabled -false
                                    ft12 = fcc6 divided by (2 power T12ClkSelection)
                                    if T12PrescalerEnabled -true
                                    ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )

####### ENUMERATION 类型参数

######## 1. CCU6InterruptNode

- **UUID**: `ECUC:b9e816ea-2207-4329-8830-328ccdeabda3`
- **参数名**: `CCU6InterruptNode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NODE_SR0`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `NODE_SR0` (来源: INFINEON_AURIX2G)
  - `NODE_SR1` (来源: INFINEON_AURIX2G)
  - `NODE_SR2` (来源: INFINEON_AURIX2G)
  - `NODE_SR3` (来源: INFINEON_AURIX2G)
- **描述**: Interrupt node to be used for the kernel

##### 12. ERUInputConfiguration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-91123f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ERUInputConfiguration`
- **多重性**: [0..1]

**容器描述**:

This container contains the ERS and OGU Configuration

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EruInputPin

- **UUID**: `20ee392a-1640-45fd-80f2-0c6bd7d1ef0d`
- **参数名**: `EruInputPin`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ERU_INPUT0A_PORT15_PIN4`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ERU_INPUT0A_PORT15_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0B_CCU60_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0C_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0D_MSC0_FCLP` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT0E_STM5_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1A_PORT14_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1B_CCU61_COUT60` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1C_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT1D_STM0_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2A_PORT10_PIN2` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2B_PORT02_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2C_PORT00_PIN4` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT2D_ERAY0_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3A_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3B_PORT14_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3C_PORT02_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT3D_STM1_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4A_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4B_GTM_TOM0_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4C_GPT120_T3OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT4D_PORT15_PIN5` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5A_PORT15_PIN8` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5B_GTM_TOM1_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5C_GPT120_T6OUT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT5D_STM2_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6A_PORT20_PIN0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6B_ESR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6D_PORT11_PIN10` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6E_STM3_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT6F_GTM_TOM2_12` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7A_PORT20_PIN9` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7B_ESR1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7C_PORT15_PIN1` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7D_ERAY1_MT` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7E_STM4_STMIR0` (来源: INFINEON_AURIX2G)
  - `ERU_INPUT7F_GTM_TOM3_12` (来源: INFINEON_AURIX2G)
- **描述**: Eru Input selection for the ERU unit

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. EruErsReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruErsReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelInputLineConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelInputLineConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the ERU channels (ERS and OGU).

######## 2. EruOguReference

- **UUID**: `ECUC:c945dd5e-1l78-4bcc-a8ab-0a4d19ec1185`
- **引用名**: `EruOguReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuEruChannelOutputUnitConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuEruAllocationConf/McuEruChannelOutputUnitConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GTM timer channels (TOM/ATOM).

##### 13. GPT12Configuration

**容器属性**:

- **UUID**: `e150fb37-a6f3-4a0f-8b78-9drt3f8b76f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `GPT12Configuration`
- **多重性**: [0..1]

**容器描述**:

This container contains the GPT12 Configuration for GPT12

###### 参数配置

此容器包含 **3** 个参数：

####### ENUMERATION 类型参数

######## 1. GPT12InputPortSelection

- **UUID**: `20e392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12InputPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `GPT12_T2INA_PORT00_PIN7`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `GPT12_T2INA_PORT00_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T2INB_PORT33_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INA_PORT02_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INB_PORT10_PIN4` (来源: INFINEON_AURIX2G)
  - `GPT12_T3INC_SCU_PDOUT4` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INA_PORT02_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T4INB_PORT10_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INA_PORT21_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T5INB_PORT10_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INA_PORT20_PIN3` (来源: INFINEON_AURIX2G)
  - `GPT12_T6INB_PORT10_PIN2` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Input selection for the GPT12 unit

######## 2. GPT12DirPortSelection

- **UUID**: `20d392a-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12DirPortSelection`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `NONE` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDA_PORT00_PIN8` (来源: INFINEON_AURIX2G)
  - `GPT12_T2EUDB_PORT33_PIN6` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDA_PORT02_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T3EUDB_PORT10_PIN7` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDA_PORT00_PIN9` (来源: INFINEON_AURIX2G)
  - `GPT12_T4EUDB_PORT33_PIN5` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Direction Input selection for the GPT12 unit

######## 3. GPT12CounterType

- **UUID**: `20d392b-1640-45fd-80f2-0c6ghtd1ef0d`
- **参数名**: `GPT12CounterType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_1_COUNT_INPUT`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **可选值**:
  - `ICU_1_COUNT_INPUT` (来源: INFINEON_AURIX2G)
  - `ICU_2_COUNT_INPUT` (来源: INFINEON_AURIX2G)
- **描述**: GPT12 Counting mechanism

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. GPT12BlockReference

- **UUID**: `ECUC:c945dd5e-1l5b-4bcc-a8ab-0a4sdeec1185`
- **引用名**: `GPT12BlockReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuGpt12ModuleAllocationConf`
- **完整路径**: `/AURIX2G/EcucDefs/Mcu/McuHardwareResourceAllocationConf/McuGpt12ModuleAllocationConf`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **描述**: This parameter lists all the GPT12 timer channels Block.

##### 14. IcuGeneral

**容器属性**:

- **UUID**: `ECUC:1d7a6ee1-8bc5-4f5f-b509-c111110711`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuGeneral`
- **多重性**: [0..1]

**容器描述**:

Configuration of general ICU parameters.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. IcuIndex

- **UUID**: `ECUC:d3ffe4e8-d2bc-40ad-bb95-f0711111136a`
- **参数名**: `IcuIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. IcuDevErrorDetect

- **UUID**: `ECUC:7224bf75-cdc8-408f-1111-9e7118f84`
- **参数名**: `IcuDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Development Error Detection on or off. true: Enabled. false: Disabled.

######## 2. IcuMultiCoreErrorDetect

- **UUID**: `ECUC:7224bf75-cdc8-408f-1111-9e7118a84`
- **参数名**: `IcuMultiCoreErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switches the MultiCore Development Error Detection on or off. true: Enabled. false: Disabled.

######## 3. IcuReportWakeupSource

- **UUID**: `be837339-bdd5-4cda-9025-74e2011c110a`
- **参数名**: `IcuReportWakeupSource`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch for enabling Wakeup source reporting. true: Report Wakeup source. false: Do not report Wakeup source.

######## 4. IcuSafetyEnable

- **UUID**: `be837339-bdd5-4cda-123w-74e2011c110a`
- **参数名**: `IcuSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Switch for enabling/Disabling IcuSafetyEnable

####### ENUMERATION 类型参数

######## 1. IcuRuntimeApiMode

- **UUID**: `ECUC:b9e816ea-3457-ght9-8830-328ccdeabda3`
- **参数名**: `IcuRuntimeApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ICU_MCAL_USER1` (来源: INFINEON_AURIX2G)
  - `ICU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
- **描述**: IcuRuntimeApiMode for ICU_MCAL_USER1, ICU_MCAL_SUPERVISOR

######## 2. IcuInitDeInitApiMode

- **UUID**: `ECUC:b9e816ea-3457-dsc9-8830-328ccdeabda3`
- **参数名**: `IcuInitDeInitApiMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ICU_MCAL_SUPERVISOR`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **可选值**:
  - `ICU_MCAL_USER1` (来源: INFINEON_AURIX2G)
  - `ICU_MCAL_SUPERVISOR` (来源: INFINEON_AURIX2G)
- **描述**: IcuInitDeInitApiMode for ICU_MCAL_USER1, ICU_MCAL_SUPERVISOR

##### 15. IcuOptionalApis

**容器属性**:

- **UUID**: `ECUC:52e9680e-5f55-4fd1-b11c-888491b8943f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuOptionalApis`
- **多重性**: [0..1]

**容器描述**:

This container contains all configuration switches for configuring optional API services of the ICU driver.

###### 参数配置

此容器包含 **15** 个参数：

####### BOOLEAN 类型参数

######## 1. IcuDeInitApi

- **UUID**: `ECUC:4d3911ac-2595-4da6-a69e-66453109d78a`
- **参数名**: `IcuDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_DeInit() from the code.
                        true: Icu_17_TimerIp_DeInit() can be used.
                        false: Icu_17_TimerIp_DeInit() can not be used.

######## 2. IcuInitCheckApi

- **UUID**: `ECUC:4d3911ac-2595-4da7-a69e-66453109d78a`
- **参数名**: `IcuInitCheckApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_InitCheck() from the code.
                        true: Icu_17_TimerIp_InitCheck() can be used.
                        false: Icu_17_TimerIp_InitCheck() can not be used.

######## 3. IcuDisableWakeupApi

- **UUID**: `1c9d1a58-049f-4539-aed4-a74b83ecdac6`
- **参数名**: `IcuDisableWakeupApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_DisableWakeup() from the code.
                        true: Icu_17_TimerIp_DisableWakeup() can be used.
                        false: Icu_17_TimerIp_DisableWakeup() can not be used.

######## 4. IcuEdgeCountApi

- **UUID**: `f204ba98-1a51-4ea5-bc96-ee2f4fb47241`
- **参数名**: `IcuEdgeCountApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes all services related to the edge counting functionality as listed below, from the code: Icu_17_TimerIp_ResetEdgeCount(), Icu_17_TimerIp_EnableEdgeCount(), Icu_17_TimerIp_DisableEdgeCount(), Icu_17_TimerIp_GetEdgeNumbers().
                    true: The services listed above can be used.
                    false: The services listed above can not be used.

######## 5. IcuEdgeDetectApi

- **UUID**: `cc472968-f36b-4c51-83c2-5da51a119c20`
- **参数名**: `IcuEdgeDetectApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes all services related to the edge detection functionality as listed below from the code: Icu_17_TimerIp_EnableEdgeDetection(),Icu_17_TimerIp_DisableEdgeDetection().
                    true: The services listed above can be used.
                    false: The services listed above can not be used.

######## 6. IcuEnableWakeupApi

- **UUID**: `958e3d82-c0a1-4892-1070-66dc62bed707`
- **参数名**: `IcuEnableWakeupApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_EnableWakeup() from the code.
                        true: Icu_17_TimerIp_EnableWakeup() can be used.
                        false: Icu_17_TimerIp_EnableWakeup() can not be used.

######## 7. IcuGetDutyCycleValuesApi

- **UUID**: `24520859-5d13-4c7e-be40-0d521f7deef8`
- **参数名**: `IcuGetDutyCycleValuesApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_GetDutyCycleValues() from the code.
                    true: Icu_17_TimerIp_GetDutyCycleValues() can be used.
                    false: Icu_17_TimerIp_GetDutyCycleValues() can not be used.

######## 8. IcuGetInputStateApi

- **UUID**: `c32d5ba1-ce39-4a79-a7b9-619d6fd2d9ce`
- **参数名**: `IcuGetInputStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_GetInputState() from the code.
                    true: Icu_17_TimerIp_GetInputState() can be used.
                    false: Icu_17_TimerIp_GetInputState() can not be used.

######## 9. IcuGetTimeElapsedApi

- **UUID**: `8e8c1887-31ee-46af-a84c-dd91dd9de7ae`
- **参数名**: `IcuGetTimeElapsedApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_GetTimeElapsed() from the code.
                    true: Icu_17_TimerIp_GetTimeElapsed() can be used.
                    false: Icu_17_TimerIp_GetTimeElapsed() can not be used.

######## 10. IcuGetVersionInfoApi

- **UUID**: `ECUC:ab4fff0d-bcf9-4cd4-8d5f-a8c599f9f4a6`
- **参数名**: `IcuGetVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_GetVersionInfo() from the code.
                    true: Icu_17_TimerIp_GetVersionInfo() can be used.
                    false: Icu_17_TimerIp_GetVersionInfo() can not be used.

######## 11. IcuSetModeApi

- **UUID**: `ef8081f4-2cba-4963-bb09-07cd437e9623`
- **参数名**: `IcuSetModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_SetMode() from the code.
                    true: Icu_17_TimerIp_SetMode() can be used.
                    false: Icu_17_TimerIp_SetMode() can not be used.

######## 12. IcuSignalMeasurementApi

- **UUID**: `8238ef5e-f421-4be4-9e5e-5c27f9f515d1`
- **参数名**: `IcuSignalMeasurementApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the services Icu_17_TimerIp_StartSignalMeasurement() and Icu_17_TimerIp_StopSignalMeasurement() from the code.
                    true: Icu_17_TimerIp_StartSignalMeasurement() and Icu_17_TimerIp_StopSignalMeasurement() can be used.
                    false: Icu_17_TimerIp_StartSignalMeasurement() and Icu_17_TimerIp_StopSignalMeasurement() can not be used.

######## 13. IcuTimestampApi

- **UUID**: `5c4306bc-6934-4639-9830-e32bc2541fce`
- **参数名**: `IcuTimestampApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes all services related to the timestamping functionality as listed below from the code: Icu_17_TimerIp_StartTimestamp(), Icu_17_TimerIp_StopTimestamp(), Icu_17_TimerIp_GetTimestampIndex().
                    true: The services listed above can be used.
                    false: The services listed above can not be used.

######## 14. IcuWakeupFunctionalityApi

- **UUID**: `958e3d82-c0a1-4892-a070-66dc62bed708`
- **参数名**: `IcuWakeupFunctionalityApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Icu_17_TimerIp_CheckWakeup() from the code.
                    true: Icu_17_TimerIp_CheckWakeup() can be used.
                    false: Icu_17_TimerIp_CheckWakeup() can not be used.

######## 15. IcuIncrementalInterfaceApi

- **UUID**: `958e3e82-c0a1-4892-a070-66dc62bed708`
- **参数名**: `IcuIncrementalInterfaceApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Adds / removes the services related to incremental interface mode from the code.
                    true: Incremental Interface mode API can be used.
                    false: Incremental Interface mode API can not be used.

##### 16. CommonPublishedInformation

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
- **默认值**: `1`
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
- **默认值**: `122`
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

######## 1. VendorApiInfix

- **UUID**: `ad363b41-e945-4717-b12f-c2f800ef138e`
- **参数名**: `VendorApiInfix`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `TimerIp`
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

1. **Icu**
