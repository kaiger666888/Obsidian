# Adc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:05

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Adc](#adc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Adc

#### 基本信息

- **UUID**: `ECUC:c03229fe-4dca-445e-a47c-1ae11e6c1832`
- **模块名称**: `Adc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Adc (Analog Digital Conversion) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. AdcConfigSet

**容器属性**:

- **UUID**: `ECUC:fc6e0617-8c73-4b71-b09e-dfb10b76e50d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This is the base container that contains the post-build selectable configuration parameters

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. AdcHwUnit

**容器属性**:

- **UUID**: `ECUC:c67e7c58-3daf-455b-a213-95ae94b248d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnit`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Driver configuration (parameters) depending on grouping of channels

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. AdcPrescale

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcPrescale`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional ADC module specific clock prescale factor, if supported by hardware.

######### ENUMERATION 类型参数

########## 1. AdcClockSource

- **UUID**: `ECUC:08f7956c-d858-438f-9504-12df1ba10e73`
- **参数名**: `AdcClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ADC module specific clock input for the conversion  unit can

########## 2. AdcHwUnitId

- **UUID**: `ECUC:7aa61340-e385-4037-b899-40ce3e595755`
- **参数名**: `AdcHwUnitId`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

############ 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: High limit - used for limit checking.

############ 3. AdcChannelId

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1024]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

############ 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Low limit - used for limit checking.

############ 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel resolution in bits.

############ 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

########### BOOLEAN 类型参数

############ 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables limit checking for an ADC channel.

########### ENUMERATION 类型参数

############ 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

############ 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper reference voltage source for each channel.

############ 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower reference voltage source for each channel.

######### 2. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Group configuration (parameters).

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric ID of the group. This parameter is the symbolic name to be used on the API. This symbolic name allows accessing Channel Group data. This value will be assigned to the symbolic name derived of the AdcGroup container shortName.

############ 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority level of the AdcGroup.

############ 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

############ 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

########### ENUMERATION 类型参数

############ 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of access mode to group conversion results.

############ 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of conversion mode supported by the driver.

############ 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

############ 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of source event that starts a group conversion.

############ 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

############ 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

########### FUNCTION-NAME 类型参数

############ 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for each group

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Assignment of AdcChannels to a AdcGroups.

####### 2. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

########## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: High limit - used for limit checking.

########## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1024]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

########## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Low limit - used for limit checking.

########## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel resolution in bits.

########## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

######### BOOLEAN 类型参数

########## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables limit checking for an ADC channel.

######### ENUMERATION 类型参数

########## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

########## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper reference voltage source for each channel.

########## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower reference voltage source for each channel.

####### 3. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Group configuration (parameters).

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric ID of the group. This parameter is the symbolic name to be used on the API. This symbolic name allows accessing Channel Group data. This value will be assigned to the symbolic name derived of the AdcGroup container shortName.

########## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority level of the AdcGroup.

########## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

########## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

######### ENUMERATION 类型参数

########## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of access mode to group conversion results.

########## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of conversion mode supported by the driver.

########## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

########## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of source event that starts a group conversion.

########## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

########## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

######### FUNCTION-NAME 类型参数

########## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for each group

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Assignment of AdcChannels to a AdcGroups.

##### 2. AdcHwUnit

**容器属性**:

- **UUID**: `ECUC:c67e7c58-3daf-455b-a213-95ae94b248d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcHwUnit`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Driver configuration (parameters) depending on grouping of channels

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. AdcPrescale

- **UUID**: `ECUC:ea7f8f6d-5d98-4bc4-808e-dc02c4c233ac`
- **参数名**: `AdcPrescale`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional ADC module specific clock prescale factor, if supported by hardware.

####### ENUMERATION 类型参数

######## 1. AdcClockSource

- **UUID**: `ECUC:08f7956c-d858-438f-9504-12df1ba10e73`
- **参数名**: `AdcClockSource`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The ADC module specific clock input for the conversion  unit can

######## 2. AdcHwUnitId

- **UUID**: `ECUC:7aa61340-e385-4037-b899-40ce3e595755`
- **参数名**: `AdcHwUnitId`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data. Enumeration literals are defined vendor specific.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

########## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: High limit - used for limit checking.

########## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1024]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

########## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Low limit - used for limit checking.

########## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel resolution in bits.

########## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

######### BOOLEAN 类型参数

########## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables limit checking for an ADC channel.

######### ENUMERATION 类型参数

########## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

########## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper reference voltage source for each channel.

########## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower reference voltage source for each channel.

####### 2. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Group configuration (parameters).

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric ID of the group. This parameter is the symbolic name to be used on the API. This symbolic name allows accessing Channel Group data. This value will be assigned to the symbolic name derived of the AdcGroup container shortName.

########## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority level of the AdcGroup.

########## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

########## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

######### ENUMERATION 类型参数

########## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of access mode to group conversion results.

########## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of conversion mode supported by the driver.

########## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

########## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of source event that starts a group conversion.

########## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

########## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

######### FUNCTION-NAME 类型参数

########## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for each group

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Assignment of AdcChannels to a AdcGroups.

##### 3. AdcChannel

**容器属性**:

- **UUID**: `ECUC:bfd7d43b-017d-4755-9a41-2bf12e38403d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel configuration (parameters) depending on the hardware capability.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. AdcChannelConvTime

- **UUID**: `ECUC:cda3fa6e-3f00-43a3-a05e-5c97744e6aaf`
- **参数名**: `AdcChannelConvTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of conversion time, i.e. the time during which the analogue value is converted into digital representation, (in clock cycles) for each channel, if supported by hardware.

######## 2. AdcChannelHighLimit

- **UUID**: `ECUC:65b39edf-db50-479b-becd-268512557336`
- **参数名**: `AdcChannelHighLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: High limit - used for limit checking.

######## 3. AdcChannelId

- **UUID**: `ECUC:482b876b-9787-4e46-875a-559b7a1427f2`
- **参数名**: `AdcChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1024]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the assignment of the channel to the physical ADC  hardware channel.

######## 4. AdcChannelLowLimit

- **UUID**: `ECUC:bd3f78a2-2b94-419a-961c-5ad47f5a8bcb`
- **参数名**: `AdcChannelLowLimit`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Low limit - used for limit checking.

######## 5. AdcChannelResolution

- **UUID**: `ECUC:c05e44f5-f418-4772-9ed3-ba767591baf1`
- **参数名**: `AdcChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel resolution in bits.

######## 6. AdcChannelSampTime

- **UUID**: `ECUC:d11259ac-99d0-488f-9cc6-a66170fbb368`
- **参数名**: `AdcChannelSampTime`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock cycles) for each channel, if supported by hardware.

####### BOOLEAN 类型参数

######## 1. AdcChannelLimitCheck

- **UUID**: `ECUC:6c8938e0-f362-4cdc-8711-6d4b429215b3`
- **参数名**: `AdcChannelLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables limit checking for an ADC channel.

####### ENUMERATION 类型参数

######## 1. AdcChannelRangeSelect

- **UUID**: `ECUC:8b1c1853-c817-448a-982b-cb15f700c87d`
- **参数名**: `AdcChannelRangeSelect`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_RANGE_ALWAYS` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_BETWEEN` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_NOT_UNDER_LOW` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_OVER_HIGH` (来源: AUTOSAR_ECUC)
  - `ADC_RANGE_UNDER_LOW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In case of active limit checking: defines which conversion values are taken into account related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.

######## 2. AdcChannelRefVoltsrcHigh

- **UUID**: `ECUC:94395609-bae2-465a-9878-df86ada9bffb`
- **参数名**: `AdcChannelRefVoltsrcHigh`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper reference voltage source for each channel.

######## 3. AdcChannelRefVoltsrcLow

- **UUID**: `ECUC:582225d2-20d0-47eb-a3c1-f387a68cb7c4`
- **参数名**: `AdcChannelRefVoltsrcLow`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower reference voltage source for each channel.

##### 4. AdcGroup

**容器属性**:

- **UUID**: `ECUC:21b450f5-989b-4095-a451-d237d777751c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Group configuration (parameters).

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. AdcGroupId

- **UUID**: `ECUC:65e3660c-73a4-4172-8d28-4edb71e96153`
- **参数名**: `AdcGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric ID of the group. This parameter is the symbolic name to be used on the API. This symbolic name allows accessing Channel Group data. This value will be assigned to the symbolic name derived of the AdcGroup container shortName.

######## 2. AdcGroupPriority

- **UUID**: `ECUC:c3c0273d-3fbb-48ea-b64a-6c6592d6a05c`
- **参数名**: `AdcGroupPriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority level of the AdcGroup.

######## 3. AdcHwTrigTimer

- **UUID**: `ECUC:ac85f536-5cf6-43f3-a6a7-d824eed38461`
- **参数名**: `AdcHwTrigTimer`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reload value of the ADC module embedded timer (only if supported by ADC hardware).

######## 4. AdcStreamingNumSamples

- **UUID**: `ECUC:ba5e660f-1505-40bb-9b17-7ce8a5655235`
- **参数名**: `AdcStreamingNumSamples`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of ADC values to be acquired per channel in streaming access mode.

####### ENUMERATION 类型参数

######## 1. AdcGroupAccessMode

- **UUID**: `ECUC:faad1eb6-43b4-4195-bacc-6245556acb07`
- **参数名**: `AdcGroupAccessMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ACCESS_MODE_SINGLE` (来源: AUTOSAR_ECUC)
  - `ADC_ACCESS_MODE_STREAMING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of access mode to group conversion results.

######## 2. AdcGroupConversionMode

- **UUID**: `ECUC:25721d0a-d8a7-4ea3-96ab-49ced3030fce`
- **参数名**: `AdcGroupConversionMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_CONV_MODE_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `ADC_CONV_MODE_ONESHOT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of conversion mode supported by the driver.

######## 3. AdcGroupReplacement

- **UUID**: `ECUC:f348b1d0-aabc-46ee-a71a-02cc6e49dca6`
- **参数名**: `AdcGroupReplacement`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_GROUP_REPL_ABORT_RESTART` (来源: AUTOSAR_ECUC)
  - `ADC_GROUP_REPL_SUSPEND_RESUME` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted by a group which has a higher priority.

######## 4. AdcGroupTriggSrc

- **UUID**: `ECUC:1fb3e310-c03a-4a29-b2d2-f8d71765c6fc`
- **参数名**: `AdcGroupTriggSrc`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_TRIGG_SRC_HW` (来源: AUTOSAR_ECUC)
  - `ADC_TRIGG_SRC_SW` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of source event that starts a group conversion.

######## 5. AdcHwTrigSignal

- **UUID**: `ECUC:70c09b6d-3cac-4db1-bee8-aafef6b9d2cf`
- **参数名**: `AdcHwTrigSignal`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_HW_TRIG_BOTH_EDGES` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_FALLING_EDGE` (来源: AUTOSAR_ECUC)
  - `ADC_HW_TRIG_RISING_EDGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures on which edge of the hardware trigger signal the driver should react, i.e. start the conversion (only if supported by the ADC hardware).

######## 6. AdcStreamingBufferMode

- **UUID**: `ECUC:7ea9390c-d8f5-44c3-baf2-d2575ef9e9c8`
- **参数名**: `AdcStreamingBufferMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_STREAM_BUFFER_CIRCULAR` (来源: AUTOSAR_ECUC)
  - `ADC_STREAM_BUFFER_LINEAR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the stream buffer is reached).

####### FUNCTION-NAME 类型参数

######## 1. AdcNotification

- **UUID**: `ECUC:f43bffda-8d3a-4520-b424-b558fcbe752c`
- **参数名**: `AdcNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function for each group

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. AdcGroupDefinition

- **UUID**: `ECUC:fc412877-d8ab-4b65-96e8-0498ac13762e`
- **引用名**: `AdcGroupDefinition`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `AdcChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Adc/AdcConfigSet/AdcHwUnit/AdcChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Assignment of AdcChannels to a AdcGroups.

##### 5. AdcGeneral

**容器属性**:

- **UUID**: `ECUC:da0aaff6-3ed6-4a15-824e-dc32f3a8bd93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration (parameters) of the ADC Driver software module.

###### 参数配置

此容器包含 **11** 个参数：

####### BOOLEAN 类型参数

######## 1. AdcDeInitApi

- **UUID**: `ECUC:16c0e8fd-6160-4ffb-b5a0-0fa22757dbae`
- **参数名**: `AdcDeInitApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Adc_DeInit() from the code.

######## 2. AdcDevErrorDetect

- **UUID**: `ECUC:db321b92-621a-4a62-8778-09b8845d8f2c`
- **参数名**: `AdcDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 3. AdcEnableLimitCheck

- **UUID**: `ECUC:36543fc4-cdc1-453b-9706-844d76e6fa30`
- **参数名**: `AdcEnableLimitCheck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables limit checking feature in the ADC driver.

######## 4. AdcEnableQueuing

- **UUID**: `ECUC:cf5318b5-011b-4128-8393-02dd46fe52b5`
- **参数名**: `AdcEnableQueuing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines, if the queuing mechanism is active in case of priority mechanism disabled.

######## 5. AdcEnableStartStopGroupApi

- **UUID**: `ECUC:94b12c2c-4231-424c-90c9-a55ee72663fe`
- **参数名**: `AdcEnableStartStopGroupApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services Adc_StartGroupConversion() and Adc_StopGroupConversion() from the code.

######## 6. AdcGrpNotifCapability

- **UUID**: `ECUC:b2cfcb7b-0a84-4c50-bebd-32ee405e4300`
- **参数名**: `AdcGrpNotifCapability`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines, if the group notification mechanism (the functions to enable and disable the notifications) is available at runtime.

######## 7. AdcHwTriggerApi

- **UUID**: `ECUC:e5c85e73-38e2-47ae-85e9-c39d1b361249`
- **参数名**: `AdcHwTriggerApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the services Adc_EnableHardwareTrigger() and Adc_DisableHardwareTrigger() from the code.

######## 8. AdcReadGroupApi

- **UUID**: `ECUC:6fe4295d-02b9-4c34-b9f2-337c2df6bd58`
- **参数名**: `AdcReadGroupApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Adc_ReadGroup() and from the code.

######## 9. AdcVersionInfoApi

- **UUID**: `ECUC:8ea4cb56-cf5e-4afc-95ce-cebac08ac0e6`
- **参数名**: `AdcVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Adc_GetVersionInfo() from the code.

####### ENUMERATION 类型参数

######## 1. AdcPriorityImplementation

- **UUID**: `ECUC:7e0e69e5-6004-4264-a9b3-f0559f2409d6`
- **参数名**: `AdcPriorityImplementation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_PRIORITY_HW` (来源: AUTOSAR_ECUC)
  - `ADC_PRIORITY_HW_SW` (来源: AUTOSAR_ECUC)
  - `ADC_PRIORITY_NONE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines whether a priority mechanism is available for prioritization of the conversion requests and if available, the type of prioritization mechanism. The selection applies for groups with trigger source software and trigger source hardware. Two

######## 2. AdcResultAlignment

- **UUID**: `ECUC:b269a17e-8b68-4182-8879-338205ac27ca`
- **参数名**: `AdcResultAlignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ADC_ALIGN_LEFT` (来源: AUTOSAR_ECUC)
  - `ADC_ALIGN_RIGHT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Alignment of ADC raw results in ADC result buffer (left/right alignment).

##### 6. AdcPublishedInformation

**容器属性**:

- **UUID**: `ECUC:e435c52c-58b2-4506-ae6c-da9a9b76ad99`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `AdcPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. AdcMaxChannelResolution

- **UUID**: `ECUC:8f00599e-47d5-4046-bce8-9cbefac7e41a`
- **参数名**: `AdcMaxChannelResolution`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Maximum Channel resolution in bits (does not specify accuracy).

####### BOOLEAN 类型参数

######## 1. AdcChannelValueSigned

- **UUID**: `ECUC:f002ab5c-bf89-4fc2-ba13-6909a2c2e75a`
- **参数名**: `AdcChannelValueSigned`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Information whether the result value of the ADC driver has sign information (true) or not (false). If the result shall be interpreted as signed value it shall apply to C-language rules.

######## 2. AdcGroupFirstChannelFixed

- **UUID**: `ECUC:1c22f85b-d656-4563-86ec-1823df41ebed`
- **参数名**: `AdcGroupFirstChannelFixed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Information whether the first channel of an ADC Channel group can be configured (false) or is fixed (true) to a value determined by the ADC HW Unit.

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

1. **Adc**
