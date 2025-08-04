# Icu - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:48

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Icu](#icu)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Icu

#### 基本信息

- **UUID**: `ECUC:9d858769-7cc7-46c3-941e-129083aef5cb`
- **模块名称**: `Icu`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Icu (Input Capture Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. IcuConfigSet

**容器属性**:

- **UUID**: `ECUC:65e11074-8c5d-4fb7-b332-10e4889287f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is the base for a multiple configuration set

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IcuMaxChannel

- **UUID**: `ECUC:65e2f79c-922e-4180-90dc-0819fc20f890`
- **参数名**: `IcuMaxChannel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the number of Channels configured. It will be gathered by tools during the configuration stage.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. IcuChannel

**容器属性**:

- **UUID**: `ECUC:74f0ce69-2156-4784-bae9-57ea4699e6e4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual ICU channel.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. IcuChannelId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `IcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the IcuChannel container short name.

######### BOOLEAN 类型参数

########## 1. IcuWakeupCapability

- **UUID**: `ECUC:fc806d81-9561-454b-8c39-aed26d6e49bf`
- **参数名**: `IcuWakeupCapability`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Information about the wakeup-capability of this channel.

######### ENUMERATION 类型参数

########## 1. IcuDefaultStartEdge

- **UUID**: `ECUC:29f03c55-e634-4f63-90cf-2027f4cd10f1`
- **参数名**: `IcuDefaultStartEdge`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ICU_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ICU_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the default-activation-edge which shall be used for this channel if there was no activation-edge configured by the call of service Icu_SetActivationCondition().

########## 2. IcuMeasurementMode

- **UUID**: `ECUC:b9e816ea-2297-4329-8830-328ccdeabda3`
- **参数名**: `IcuMeasurementMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_MODE_EDGE_COUNTER` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_EDGE_DETECT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_MEASUREMENT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_TIMESTAMP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the measurement mode of this channel.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

########## 参数配置

此容器包含 **1** 个参数：

########### FUNCTION-NAME 类型参数

############ 1. IcuSignalNotification

- **UUID**: `ECUC:98319c3e-7a97-4edf-8ec1-9da0994e2db2`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function for signal notification.

######### 2. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_ACTIVE_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the property that could be measured in case the mode is "IcuSignalMeasurement".

######### 3. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the handling of the buffer in case the mode is "Timestamp"

########### FUNCTION-NAME 类型参数

############ 1. IcuTimestampNotification

- **UUID**: `ECUC:0a447661-94c2-4817-b14f-930ee4258f2f`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function if the number of requested timestamps

######### 4. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]
- **多配置容器**: false

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
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM) .

####### 2. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. IcuSignalNotification

- **UUID**: `ECUC:98319c3e-7a97-4edf-8ec1-9da0994e2db2`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function for signal notification.

####### 3. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_ACTIVE_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the property that could be measured in case the mode is "IcuSignalMeasurement".

####### 4. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the handling of the buffer in case the mode is "Timestamp"

######### FUNCTION-NAME 类型参数

########## 1. IcuTimestampNotification

- **UUID**: `ECUC:0a447661-94c2-4817-b14f-930ee4258f2f`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function if the number of requested timestamps

####### 5. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]
- **多配置容器**: false

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
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM) .

##### 2. IcuChannel

**容器属性**:

- **UUID**: `ECUC:74f0ce69-2156-4784-bae9-57ea4699e6e4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual ICU channel.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. IcuChannelId

- **UUID**: `ECUC:3e518668-f29a-463d-b183-d4b4d1c28766`
- **参数名**: `IcuChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the IcuChannel container short name.

####### BOOLEAN 类型参数

######## 1. IcuWakeupCapability

- **UUID**: `ECUC:fc806d81-9561-454b-8c39-aed26d6e49bf`
- **参数名**: `IcuWakeupCapability`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Information about the wakeup-capability of this channel.

####### ENUMERATION 类型参数

######## 1. IcuDefaultStartEdge

- **UUID**: `ECUC:29f03c55-e634-4f63-90cf-2027f4cd10f1`
- **参数名**: `IcuDefaultStartEdge`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ICU_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ICU_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the default-activation-edge which shall be used for this channel if there was no activation-edge configured by the call of service Icu_SetActivationCondition().

######## 2. IcuMeasurementMode

- **UUID**: `ECUC:b9e816ea-2297-4329-8830-328ccdeabda3`
- **参数名**: `IcuMeasurementMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_MODE_EDGE_COUNTER` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_EDGE_DETECT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_SIGNAL_MEASUREMENT` (来源: AUTOSAR_ECUC)
  - `ICU_MODE_TIMESTAMP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the measurement mode of this channel.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. IcuSignalNotification

- **UUID**: `ECUC:98319c3e-7a97-4edf-8ec1-9da0994e2db2`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function for signal notification.

####### 2. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_ACTIVE_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the property that could be measured in case the mode is "IcuSignalMeasurement".

####### 3. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the handling of the buffer in case the mode is "Timestamp"

######### FUNCTION-NAME 类型参数

########## 1. IcuTimestampNotification

- **UUID**: `ECUC:0a447661-94c2-4817-b14f-930ee4258f2f`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function if the number of requested timestamps

####### 4. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]
- **多配置容器**: false

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
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM) .

##### 3. IcuSignalEdgeDetection

**容器属性**:

- **UUID**: `ECUC:761a76f3-f5c6-4715-a916-9a077db4a160`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalEdgeDetection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalEdgeDetection"

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. IcuSignalNotification

- **UUID**: `ECUC:98319c3e-7a97-4edf-8ec1-9da0994e2db2`
- **参数名**: `IcuSignalNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function for signal notification.

##### 4. IcuSignalMeasurement

**容器属性**:

- **UUID**: `ECUC:d5664952-203b-47c4-9c69-bc138c81857b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuSignalMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuSignalMeasurement"

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. IcuSignalMeasurementProperty

- **UUID**: `ECUC:dd5a6572-bc3a-4853-985d-753d3392a183`
- **参数名**: `IcuSignalMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_ACTIVE_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_DUTY_CYCLE` (来源: AUTOSAR_ECUC)
  - `ICU_HIGH_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_LOW_TIME` (来源: AUTOSAR_ECUC)
  - `ICU_PERIOD_TIME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the property that could be measured in case the mode is "IcuSignalMeasurement".

##### 5. IcuTimestampMeasurement

**容器属性**:

- **UUID**: `ECUC:3bb68cd5-7dfc-43b4-b64f-f601cb9d99ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuTimestampMeasurement`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) in case the measurement mode is "IcuTimestamp"

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. IcuTimestampMeasurementProperty

- **UUID**: `ECUC:b13ccde7-442b-4468-a875-28648408d95e`
- **参数名**: `IcuTimestampMeasurementProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ICU_CIRCULAR_BUFFER` (来源: AUTOSAR_ECUC)
  - `ICU_LINEAR_BUFFER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the handling of the buffer in case the mode is "Timestamp"

####### FUNCTION-NAME 类型参数

######## 1. IcuTimestampNotification

- **UUID**: `ECUC:0a447661-94c2-4817-b14f-930ee4258f2f`
- **参数名**: `IcuTimestampNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Notification function if the number of requested timestamps

##### 6. IcuWakeup

**容器属性**:

- **UUID**: `ECUC:1e4f92c1-8c4d-4ae4-8cc8-2ef213419e4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuWakeup`
- **多重性**: [0..1]
- **多配置容器**: false

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
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If the wakeup-capability is true the wakeup source referenced  is transmitted to the ECU State Manager (EcuM) .

##### 7. IcuGeneral

**容器属性**:

- **UUID**: `ECUC:1d7a6ee1-8bc5-4f5f-b509-c17e210792d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Configuration of general ICU parameters.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IcuIndex

- **UUID**: `ECUC:d3ffe4e8-d2bc-40ad-bb95-f07834be136a`
- **参数名**: `IcuIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. IcuDevErrorDetect

- **UUID**: `ECUC:7224bf75-cdc8-408f-91ff-3a99e7a18f84`
- **参数名**: `IcuDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification

######## 2. IcuReportWakeupSource

- **UUID**: `ECUC:4f4c8d4b-1b31-4832-9593-481e273767fb`
- **参数名**: `IcuReportWakeupSource`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling Wakeup source reporting.

##### 8. IcuOptionalApis

**容器属性**:

- **UUID**: `ECUC:52e9680e-5f55-4fd1-b0bc-888491b8943f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IcuOptionalApis`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains all configuration switches for configuring optional API services of the ICU driver.

###### 参数配置

此容器包含 **13** 个参数：

####### BOOLEAN 类型参数

######## 1. IcuDeInitApi

- **UUID**: `ECUC:4d39ccac-2595-4da7-a69e-66453109d78a`
- **参数名**: `IcuDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_DeInit() from the code.

######## 2. IcuDisableWakeupApi

- **UUID**: `ECUC:6d684a90-4bd5-46f1-98c7-5ee0c87a4d3b`
- **参数名**: `IcuDisableWakeupApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_DisableWakeup() from the code.

######## 3. IcuEdgeCountApi

- **UUID**: `ECUC:cdf40ca5-30d2-4ef5-ab1f-8718f7c34a1b`
- **参数名**: `IcuEdgeCountApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes all services related to the edge counting functionality as listed below, from the code: Icu_ResetEdgeCount(), Icu_EnableEdgeCount(), Icu_DisableEdgeCount(), Icu_GetEdgeNumbers().

######## 4. IcuEdgeDetectApi

- **UUID**: `ECUC:c7120c6a-ec51-4ec8-af9f-6ff680d2a9a8`
- **参数名**: `IcuEdgeDetectApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services related to the edge detection functionality, from the code:

######## 5. IcuEnableWakeupApi

- **UUID**: `ECUC:c66b6658-f92b-44db-849d-d21fd3ec8bd7`
- **参数名**: `IcuEnableWakeupApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_EnableWakeup() from the code.

######## 6. IcuGetDutyCycleValuesApi

- **UUID**: `ECUC:8c295fd4-29a0-4f33-8275-5e5885f0d0da`
- **参数名**: `IcuGetDutyCycleValuesApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_GetDutyCycleValues() from the code.

######## 7. IcuGetInputStateApi

- **UUID**: `ECUC:45a58d33-058d-473d-bb4e-16e883293e42`
- **参数名**: `IcuGetInputStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_GetInputState() from the code.

######## 8. IcuGetTimeElapsedApi

- **UUID**: `ECUC:a87b3e59-925b-48f0-9e65-7dd842060e1a`
- **参数名**: `IcuGetTimeElapsedApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_GetTimeElapsed() from the code.

######## 9. IcuGetVersionInfoApi

- **UUID**: `ECUC:ab4fff0d-bcf9-4cd4-8d5f-a8c599f9f4a6`
- **参数名**: `IcuGetVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_GetVersionInfo() from the code.

######## 10. IcuSetModeApi

- **UUID**: `ECUC:b06b2a5f-8d05-4cfc-819d-b2c1823f26c6`
- **参数名**: `IcuSetModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_SetMode() from the code.

######## 11. IcuSignalMeasurementApi

- **UUID**: `ECUC:e7f32d8d-d9d3-485b-ae88-cf3658bfbaf9`
- **参数名**: `IcuSignalMeasurementApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services Icu_StartSignalMeasurement() and Icu_StopSignalMeasurement() from the code.

######## 12. IcuTimestampApi

- **UUID**: `ECUC:b4d200cd-fefe-4c78-8338-cccedb398ee1`
- **参数名**: `IcuTimestampApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes all services related to the timestamping functionality as listed below from the code: Icu_StartTimestamp(), Icu_StopTimestamp(), Icu_GetTimestampIndex().

######## 13. IcuWakeupFunctionalityApi

- **UUID**: `ECUC:ac569439-e703-4088-ac80-d9ccdeebf2fc`
- **参数名**: `IcuWakeupFunctionalityApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Icu_CheckWakeup() from the code.

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

1. **Icu**
