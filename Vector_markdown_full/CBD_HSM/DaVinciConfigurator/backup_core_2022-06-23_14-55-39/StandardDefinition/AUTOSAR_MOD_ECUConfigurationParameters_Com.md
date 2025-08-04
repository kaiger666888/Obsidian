# Com - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Com](#com)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Com

#### 基本信息

- **UUID**: `ECUC:2e6263f8-c461-4abc-ba24-cd51feab06dd`
- **模块名称**: `Com`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the AUTOSAR COM module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **25** 个配置容器：

##### 1. ComConfig

**容器属性**:

- **UUID**: `ECUC:31da4c36-26a7-4ed7-9350-4d63f12cf7b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR COM module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ComConfigurationId

- **UUID**: `ECUC:81fad989-399a-4cb8-b894-5169d0a11f75`
- **参数名**: `ComConfigurationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This ID is returned by a call to Com_GetConfigurationId.

###### 配置容器

本模块包含 **23** 个配置容器：

####### 1. ComGwMapping

**容器属性**:

- **UUID**: `ECUC:c290eaea-e207-4f2e-89a5-134d43a125a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. ComGwDestinationDescription

**容器属性**:

- **UUID**: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwDestinationDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComBitPosition

- **UUID**: `ECUC:a9d55d52-13f7-9895-1dba-0e140e8f522f`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

############ 2. ComUpdateBitPosition

- **UUID**: `ECUC:53d6e619-a6d4-8b2c-3f29-7230c53687ce`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

########### STRING 类型参数

############ 1. ComSignalInitValue

- **UUID**: `ECUC:2a96aa3d-e035-8a97-31c5-ffa140233a68`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

########### ENUMERATION 类型参数

############ 1. ComSignalEndianness

- **UUID**: `ECUC:0b9384a4-946a-94a7-2a07-5ba84e265ac2`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

############ 2. ComTransferProperty

- **UUID**: `ECUC:ecf98909-3c1d-91ca-3903-106b9cedcad2`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ComGwIPduRef

- **UUID**: `ECUC:b2a6fa40-d2bf-8b35-35e3-7f71a89ce3da`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############## 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############# ENUMERATION 类型参数

############## 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

######### 2. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

######### 3. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. ComGwSignalRef

- **UUID**: `ECUC:89dd8bb0-170c-d8ba-21c3-b5c6074dd9e5`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

######### 4. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. ComGwSignalRef

- **UUID**: `ECUC:b1619906-12b7-dc89-37b5-b42a44fb9a60`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

######### 5. ComGwSourceDescription

**容器属性**:

- **UUID**: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSourceDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. ComBitPosition

- **UUID**: `ECUC:80714b1d-25ca-98ce-4488-e89e1022769a`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

############ 2. ComBitSize

- **UUID**: `ECUC:e17b033e-b6c3-90ee-7203-cd4b7de89d71`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

############ 3. ComSignalLength

- **UUID**: `ECUC:12040cb4-a560-97a6-5180-695531bc5419`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

############ 4. ComUpdateBitPosition

- **UUID**: `ECUC:2a72d3e4-b8a7-8b65-65f8-4cbac6c9ac39`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

########### ENUMERATION 类型参数

############ 1. ComSignalEndianness

- **UUID**: `ECUC:e22f726f-a63d-94e0-50d6-36324fb97f2d`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

############ 2. ComSignalType

- **UUID**: `ECUC:e06cfb18-5b4d-959b-507b-e5f3dc438131`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ComGwIPduRef

- **UUID**: `ECUC:8942e80b-e492-8b6e-5cb2-59fbaa300845`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

######### 6. ComGwDestination

**容器属性**:

- **UUID**: `ECUC:007f74c9-4d99-4605-a6cd-abd1ce2c888c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwDestination`
- **多重性**: [1..infinite]

**容器选择**:

- **ComGwDestinationDescription**
  - UUID: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
  - 描述: Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.
- **ComFilter**
  - UUID: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
  - 描述: This container contains the configuration parameters of the AUTOSAR COM module's Filters.
- **ComGwSignal**
  - UUID: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

**容器描述**:

Each instance of this choice container allows to define one routing destination either by reference to an already configured COM signal / signal group or by a  destination description container.

######### 7. ComGwSource

**容器属性**:

- **UUID**: `ECUC:2803821f-4944-49d4-bcbf-aa360bda4907`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwSource`
- **多重性**: [1..1]

**容器选择**:

- **ComGwSignal**
  - UUID: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.
- **ComGwSourceDescription**
  - UUID: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
  - 描述: Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

**容器描述**:

This choice container allows the definition of the gateway source signal either by reference to an already configured COM signal / signal group or by a  source description container.

####### 2. ComGwDestinationDescription

**容器属性**:

- **UUID**: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwDestinationDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:a9d55d52-13f7-9895-1dba-0e140e8f522f`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComUpdateBitPosition

- **UUID**: `ECUC:53d6e619-a6d4-8b2c-3f29-7230c53687ce`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### STRING 类型参数

########## 1. ComSignalInitValue

- **UUID**: `ECUC:2a96aa3d-e035-8a97-31c5-ffa140233a68`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:0b9384a4-946a-94a7-2a07-5ba84e265ac2`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComTransferProperty

- **UUID**: `ECUC:ecf98909-3c1d-91ca-3903-106b9cedcad2`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComGwIPduRef

- **UUID**: `ECUC:b2a6fa40-d2bf-8b35-35e3-7f71a89ce3da`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 3. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 4. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ComGwSignalRef

- **UUID**: `ECUC:89dd8bb0-170c-d8ba-21c3-b5c6074dd9e5`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

####### 5. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ComGwSignalRef

- **UUID**: `ECUC:b1619906-12b7-dc89-37b5-b42a44fb9a60`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

####### 6. ComGwSourceDescription

**容器属性**:

- **UUID**: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSourceDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:80714b1d-25ca-98ce-4488-e89e1022769a`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComBitSize

- **UUID**: `ECUC:e17b033e-b6c3-90ee-7203-cd4b7de89d71`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

########## 3. ComSignalLength

- **UUID**: `ECUC:12040cb4-a560-97a6-5180-695531bc5419`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

########## 4. ComUpdateBitPosition

- **UUID**: `ECUC:2a72d3e4-b8a7-8b65-65f8-4cbac6c9ac39`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:e22f726f-a63d-94e0-50d6-36324fb97f2d`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComSignalType

- **UUID**: `ECUC:e06cfb18-5b4d-959b-507b-e5f3dc438131`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComGwIPduRef

- **UUID**: `ECUC:8942e80b-e492-8b6e-5cb2-59fbaa300845`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

####### 7. ComIPdu

**容器属性**:

- **UUID**: `ECUC:2369f6e2-91a1-4a41-9a26-ca4deec17900`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's I-PDUs.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduHandleId

- **UUID**: `ECUC:ae2fd4f0-9482-4454-8bad-fa692d275b39`
- **参数名**: `ComIPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID of this I-PDU. The ComIPduHandleId is required by the API calls to receive I-PDUs from the PduR (ComIP-duDirection: Receive). For Tx-I-PDUs (ComIPduDirection: Send) this handle Id is used by the PduR to confirm the transmission of the ComIPdu. In case no Tx-Confirmation is configured for a Tx-I-PDU, the ComIPduHandleId is not used.

######### BOOLEAN 类型参数

########## 1. ComIPduCancellationSupport

- **UUID**: `ECUC:590e65ba-bcf3-4622-a02c-f9cd1768902b`
- **参数名**: `ComIPduCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines for I-PDUs with ComIPduType NORMAL:

######### ENUMERATION 类型参数

########## 1. ComIPduDirection

- **UUID**: `ECUC:602c5de9-9aae-48e0-90c5-5e40a3ee1562`
- **参数名**: `ComIPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RECEIVE` (来源: AUTOSAR_ECUC)
  - `SEND` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The direction defines if this I-PDU, and therefore the contributing signals and signal groups, shall be sent or received.

########## 2. ComIPduSignalProcessing

- **UUID**: `ECUC:d23c5427-29e4-4828-9509-d2a6e953bced`
- **参数名**: `ComIPduSignalProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEFERRED` (来源: AUTOSAR_ECUC)
  - `IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For the definition of the two modes Immediate and Deferred.

########## 3. ComIPduType

- **UUID**: `ECUC:c64c0d10-9152-443d-91b9-13195e7eb049`
- **参数名**: `ComIPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NORMAL` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if this I-PDU is a normal I-PDU that can be sent unfragmented or if this is a large I-PDU that shall be sent via the Transport Protocol of the underlying bus.

######### FUNCTION-NAME 类型参数

########## 1. ComIPduCallout

- **UUID**: `ECUC:dfd7f113-2d92-42e3-9682-466e04f70473`
- **参数名**: `ComIPduCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the existence and the name of a callout function for the corresponding I-PDU. If this parameter is omitted no I-PDU callout shall take place for the corresponding I-PDU.

########## 2. ComIPduTriggerTransmitCallout

- **UUID**: `ECUC:142dca8a-fcb4-4444-ba45-c5954999b77f`
- **参数名**: `ComIPduTriggerTransmitCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If there is a trigger transmit callout defined for this I-PDU this parameter contains the name of the callout function.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. ComIPduGroupRef

- **UUID**: `ECUC:b55a77e7-c54c-4f56-aec1-e222f78228ba`
- **引用名**: `ComIPduGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I-PDU groups this I-PDU belongs to.

########## 2. ComIPduSignalGroupRef

- **UUID**: `ECUC:7171db05-bd44-4f33-8fcc-345182c94c9b`
- **引用名**: `ComIPduSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all signal groups contained in this I-Pdu

########## 3. ComIPduSignalRef

- **UUID**: `ECUC:ee4c14ce-6b3a-44d8-b206-b5e824aefbaa`
- **引用名**: `ComIPduSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all signals contained in this I-PDU.

########## 4. ComPduIdRef

- **UUID**: `ECUC:55b82985-70d9-400f-9e67-3d51f7f00ac9`
- **引用名**: `ComPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. ComIPduCounter

**容器属性**:

- **UUID**: `ECUC:138ce27a-5e66-468b-98f8-0983b735c064`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduCounter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the configuration parameters of PDU Counter.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. ComIPduCounterSize

- **UUID**: `ECUC:6960bb22-331a-4158-92a2-5dbb400df6ab`
- **参数名**: `ComIPduCounterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of PDU Counter expressed in bits

############ 2. ComIPduCounterStartPosition

- **UUID**: `ECUC:415ccc35-3f77-4f12-bb9f-7043ea53d655`
- **参数名**: `ComIPduCounterStartPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of PDU counter expressed in bits from start position of data content

############ 3. ComIPduCounterThreshold

- **UUID**: `ECUC:314f81b7-17b3-4607-9cc1-732bacf2abf5`
- **参数名**: `ComIPduCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold value of I-PDU counter algorithm, see COM590.

########### FUNCTION-NAME 类型参数

############ 1. ComIPduCounterErrorNotification

- **UUID**: `ECUC:4859caf3-c801-4c24-abcc-3a0b2d51adca`
- **参数名**: `ComIPduCounterErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Com_CbkCounterErr callback function to be called. If this

######### 2. ComIPduReplication

**容器属性**:

- **UUID**: `ECUC:57263070-9b06-41b7-9e1c-33b4d1c65828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduReplication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the information needed for each I-PDU replicated.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. ComIPduReplicationQuorum

- **UUID**: `ECUC:fe74bf86-eac7-4720-8293-5addf106b811`
- **参数名**: `ComIPduReplicationQuorum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of identical I-PDUs needed for successful voting.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ComIPduReplicaRef

- **UUID**: `ECUC:f03e9979-e355-481d-a1ca-f1ae44448996`
- **引用名**: `ComIPduReplicaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..2]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to replicas PduR PDUs of this IPDU.

######### 3. ComTxIPdu

**容器属性**:

- **UUID**: `ECUC:46a4bca4-69d5-4f21-88ea-b445b29a6601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxIPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains additional transmission related configuration parameters of the AUTOSAR COM module's I-PDUs.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. ComTxIPduUnusedAreasDefault

- **UUID**: `ECUC:af4f2f68-10af-48ca-8c08-dd0ab4921c81`
- **参数名**: `ComTxIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR COM module fills not used areas of an I-PDU with this byte pattern. This attribute is mandatory to avoid undefined behaviour. This byte-pattern will be repeated throughout the I-PDU before any init-values or update-bits were set.

########### FLOAT 类型参数

############ 1. ComMinimumDelayTime

- **UUID**: `ECUC:f1629245-0cb7-4189-9861-19caabedb323`
- **参数名**: `ComMinimumDelayTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC V3.0
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU in seconds. The MDT is independent of the possible different transmission modes. There is only one minimum delay time parameter for one I-PDU. The minimum delay timer is not reset by changing the transmission mode. Hence, it is not allowed to violate the minimum delay time by transmission mode changes. It is not possible to monitor the minimum delay time for I-PDUs that are requested using the Com_TriggerTransmit API.

########### ENUMERATION 类型参数

############ 1. ComTxIPduClearUpdateBit

- **UUID**: `ECUC:f3654eba-0ff7-40df-aad5-71812f896052`
- **参数名**: `ComTxIPduClearUpdateBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Confirmation` (来源: AUTOSAR_ECUC)
  - `Transmit` (来源: AUTOSAR_ECUC)
  - `TriggerTransmit` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines when the update-bits of signals or signal groups, contained in this I-PDU, will be cleared.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############## 参数配置

此容器包含 **5** 个参数：

############### INTEGER 类型参数

################ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############### FLOAT 类型参数

################ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

################ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

################ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############### ENUMERATION 类型参数

################ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

########### 2. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

########### 3. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############## 参数配置

此容器包含 **5** 个参数：

############### INTEGER 类型参数

################ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############### FLOAT 类型参数

################ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

################ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

################ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############### ENUMERATION 类型参数

################ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

########### 4. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 4. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 5. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 6. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 7. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 8. ComIPduCounter

**容器属性**:

- **UUID**: `ECUC:138ce27a-5e66-468b-98f8-0983b735c064`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduCounter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the configuration parameters of PDU Counter.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduCounterSize

- **UUID**: `ECUC:6960bb22-331a-4158-92a2-5dbb400df6ab`
- **参数名**: `ComIPduCounterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of PDU Counter expressed in bits

########## 2. ComIPduCounterStartPosition

- **UUID**: `ECUC:415ccc35-3f77-4f12-bb9f-7043ea53d655`
- **参数名**: `ComIPduCounterStartPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of PDU counter expressed in bits from start position of data content

########## 3. ComIPduCounterThreshold

- **UUID**: `ECUC:314f81b7-17b3-4607-9cc1-732bacf2abf5`
- **参数名**: `ComIPduCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold value of I-PDU counter algorithm, see COM590.

######### FUNCTION-NAME 类型参数

########## 1. ComIPduCounterErrorNotification

- **UUID**: `ECUC:4859caf3-c801-4c24-abcc-3a0b2d51adca`
- **参数名**: `ComIPduCounterErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Com_CbkCounterErr callback function to be called. If this

####### 9. ComIPduReplication

**容器属性**:

- **UUID**: `ECUC:57263070-9b06-41b7-9e1c-33b4d1c65828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduReplication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the information needed for each I-PDU replicated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduReplicationQuorum

- **UUID**: `ECUC:fe74bf86-eac7-4720-8293-5addf106b811`
- **参数名**: `ComIPduReplicationQuorum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of identical I-PDUs needed for successful voting.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComIPduReplicaRef

- **UUID**: `ECUC:f03e9979-e355-481d-a1ca-f1ae44448996`
- **引用名**: `ComIPduReplicaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..2]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to replicas PduR PDUs of this IPDU.

####### 10. ComTxIPdu

**容器属性**:

- **UUID**: `ECUC:46a4bca4-69d5-4f21-88ea-b445b29a6601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxIPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains additional transmission related configuration parameters of the AUTOSAR COM module's I-PDUs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. ComTxIPduUnusedAreasDefault

- **UUID**: `ECUC:af4f2f68-10af-48ca-8c08-dd0ab4921c81`
- **参数名**: `ComTxIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR COM module fills not used areas of an I-PDU with this byte pattern. This attribute is mandatory to avoid undefined behaviour. This byte-pattern will be repeated throughout the I-PDU before any init-values or update-bits were set.

######### FLOAT 类型参数

########## 1. ComMinimumDelayTime

- **UUID**: `ECUC:f1629245-0cb7-4189-9861-19caabedb323`
- **参数名**: `ComMinimumDelayTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC V3.0
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU in seconds. The MDT is independent of the possible different transmission modes. There is only one minimum delay time parameter for one I-PDU. The minimum delay timer is not reset by changing the transmission mode. Hence, it is not allowed to violate the minimum delay time by transmission mode changes. It is not possible to monitor the minimum delay time for I-PDUs that are requested using the Com_TriggerTransmit API.

######### ENUMERATION 类型参数

########## 1. ComTxIPduClearUpdateBit

- **UUID**: `ECUC:f3654eba-0ff7-40df-aad5-71812f896052`
- **参数名**: `ComTxIPduClearUpdateBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Confirmation` (来源: AUTOSAR_ECUC)
  - `Transmit` (来源: AUTOSAR_ECUC)
  - `TriggerTransmit` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines when the update-bits of signals or signal groups, contained in this I-PDU, will be cleared.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 2. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 3. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 4. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 11. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 12. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 13. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 14. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 15. ComIPduGroup

**容器属性**:

- **UUID**: `ECUC:9c06af69-2cee-4cff-958e-722ca870926f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's I-PDU groups.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduGroupHandleId

- **UUID**: `ECUC:0db9c161-2c65-400c-a788-45eafacdc525`
- **参数名**: `ComIPduGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID of this I-PDU Group .

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComIPduGroupGroupRef

- **UUID**: `ECUC:8cd1cdc0-4ac4-408d-88a4-6c307023695e`
- **引用名**: `ComIPduGroupGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all I-PDU groups that includes this I-PDU group. If this reference is omitted this I-PDU group does not belong to another I-PDU group.

####### 16. ComSignal

**容器属性**:

- **UUID**: `ECUC:6821e00a-9135-4a29-8f7e-394c346f3711`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's signals.

######## 参数配置

此容器包含 **18** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:0efae823-5158-984a-1a9c-09ac9a5a7a3d`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComBitSize

- **UUID**: `ECUC:7004a044-e251-906a-4816-ee5a0820a114`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

########## 3. ComHandleId

- **UUID**: `ECUC:6fb9c4af-5fec-8dba-480b-f6827831ff5c`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

########## 4. ComSignalLength

- **UUID**: `ECUC:a08da9ba-d0ee-9722-2793-8a63bbf457bc`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

########## 5. ComUpdateBitPosition

- **UUID**: `ECUC:b8fc70ea-e435-8ae1-3c0b-6dc95101afdc`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### FLOAT 类型参数

########## 1. ComFirstTimeout

- **UUID**: `ECUC:efde3e34-acb9-8a6b-4cee-a372064d2d67`
- **参数名**: `ComFirstTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is used immediately after start (or restart) of the deadline monitoring service. The timeout period of the successive periods is configured by COM263_Conf.

########## 2. ComTimeout

- **UUID**: `ECUC:7fdf73ac-5b6f-9942-422a-b04f791e2cd8`
- **参数名**: `ComTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the deadline monitoring timeout period in seconds. The period for the first timeout period can be configured separately by COM183_Conf.

######### STRING 类型参数

########## 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:fe1e31f9-f103-902d-1a4a-641326ab89d0`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

########## 2. ComSignalInitValue

- **UUID**: `ECUC:8fbc350f-1d96-8a4c-2ea7-fb39cbee6276`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

######### ENUMERATION 类型参数

########## 1. ComDataInvalidAction

- **UUID**: `ECUC:0b851468-e9b8-8eb5-23bd-7f1f24242421`
- **参数名**: `ComDataInvalidAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NOTIFY` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon reception of an invalid signal.

########## 2. ComRxDataTimeoutAction

- **UUID**: `ECUC:f4b36b66-eb9b-96f7-40cd-1942ddc22bd5`
- **参数名**: `ComRxDataTimeoutAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NONE` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon expiration of the  reception deadline monitoring timer.

########## 3. ComSignalEndianness

- **UUID**: `ECUC:70b90f75-d1cb-945c-26e9-5740d9f182d0`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 4. ComSignalType

- **UUID**: `ECUC:6ef6981e-86db-9517-268f-0702667b84d4`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

########## 5. ComTransferProperty

- **UUID**: `ECUC:521f13da-797e-917f-35e5-0c0428b8f2e0`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

######### FUNCTION-NAME 类型参数

########## 1. ComErrorNotification

- **UUID**: `ECUC:1dfd0b59-8b1e-8f59-40fd-3d57a237f88c`
- **参数名**: `ComErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.

########## 2. ComInvalidNotification

- **UUID**: `ECUC:0c9bd76e-1519-9774-43ff-0d2dab2d1446`
- **参数名**: `ComInvalidNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the function which notifies the RTE about the reception of an invalidated signal/ signal group. Only applicable if ComDataInvalidAction is configured to NOTIFY.

########## 3. ComNotification

- **UUID**: `ECUC:01cfe381-c4e1-9609-35fd-75f7b8646113`
- **参数名**: `ComNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxAck callback function to be called.

########## 4. ComTimeoutNotification

- **UUID**: `ECUC:c14a1a71-124c-957d-32e0-7977e8ff640b`
- **参数名**: `ComTimeoutNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxTOut callback function to be called.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:c5ba8319-d7d4-97bc-3e3e-f33ac5481dc0`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ab01c3ee-dd49-8ae7-11da-6503b3be2510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:dd2a92fe-b6d2-d09b-cc41-653b5b8908d1`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:6d4a7106-d6ef-cf8a-b2e9-43658762d0f1`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:cdc14898-ce42-d2ab-c204-3f9a3168402d`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:c46320cf-cd93-cefc-d116-4df67394fb1d`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:31660687-4963-ccdc-b4f4-34b84acd436b`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:bfd4f837-ab5f-d1f8-aa48-97c8a5479380`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:fa799a14-63ac-d43c-95ee-d212e74cb5d4`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 17. ComFilter

**容器属性**:

- **UUID**: `ECUC:ab01c3ee-dd49-8ae7-11da-6503b3be2510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:dd2a92fe-b6d2-d09b-cc41-653b5b8908d1`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:6d4a7106-d6ef-cf8a-b2e9-43658762d0f1`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:cdc14898-ce42-d2ab-c204-3f9a3168402d`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:c46320cf-cd93-cefc-d116-4df67394fb1d`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:31660687-4963-ccdc-b4f4-34b84acd436b`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:bfd4f837-ab5f-d1f8-aa48-97c8a5479380`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:fa799a14-63ac-d43c-95ee-d212e74cb5d4`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 18. ComSignalGroup

**容器属性**:

- **UUID**: `ECUC:ec4cc19d-8379-4c52-a8aa-9d4d0f11759c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComSignalGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's signal groups.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. ComHandleId

- **UUID**: `ECUC:f3e4a642-5230-8fe3-6138-5a8352d43de7`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

########## 2. ComUpdateBitPosition

- **UUID**: `ECUC:3d27527d-d679-8d0a-5537-d1ca2ba3ee67`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### FLOAT 类型参数

########## 1. ComFirstTimeout

- **UUID**: `ECUC:74091fc7-9efd-8c94-661b-0772e0ef6bf2`
- **参数名**: `ComFirstTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is used immediately after start (or restart) of the deadline monitoring service. The timeout period of the successive periods is configured by COM263_Conf.

########## 2. ComTimeout

- **UUID**: `ECUC:040a553f-4db3-9b6b-5b57-145053c06b63`
- **参数名**: `ComTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the deadline monitoring timeout period in seconds. The period for the first timeout period can be configured separately by COM183_Conf.

######### ENUMERATION 类型参数

########## 1. ComDataInvalidAction

- **UUID**: `ECUC:8faff5fb-dbfc-90de-3ce9-e31ffec662ac`
- **参数名**: `ComDataInvalidAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NOTIFY` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon reception of an invalid signal.

########## 2. ComRxDataTimeoutAction

- **UUID**: `ECUC:78de4cf9-dddf-9920-59f9-7d43b8646a60`
- **参数名**: `ComRxDataTimeoutAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NONE` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon expiration of the  reception deadline monitoring timer.

########## 3. ComTransferProperty

- **UUID**: `ECUC:d649f56d-6bc2-93a8-4f11-7005035b316b`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

######### FUNCTION-NAME 类型参数

########## 1. ComErrorNotification

- **UUID**: `ECUC:a227ecec-7d62-9182-5a29-a1587cda3717`
- **参数名**: `ComErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.

########## 2. ComInvalidNotification

- **UUID**: `ECUC:90c6b901-075d-999d-5d2b-712e85cf52d1`
- **参数名**: `ComInvalidNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the function which notifies the RTE about the reception of an invalidated signal/ signal group. Only applicable if ComDataInvalidAction is configured to NOTIFY.

########## 3. ComNotification

- **UUID**: `ECUC:85fac514-b725-9832-4f29-d9f893069f9e`
- **参数名**: `ComNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxAck callback function to be called.

########## 4. ComTimeoutNotification

- **UUID**: `ECUC:4574fc04-0490-97a6-4c0c-dd78c3a1a296`
- **参数名**: `ComTimeoutNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxTOut callback function to be called.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ComSystemTemplateSignalGroupRef

- **UUID**: `ECUC:915b9295-5b7d-414e-abc1-47140c383e4e`
- **引用名**: `ComSystemTemplateSignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignalGroup (SystemTemplate)  which this ComSignalGroup represents.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. ComGroupSignal

**容器属性**:

- **UUID**: `ECUC:bc99abe1-7836-48fc-a311-6428aaf3773b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGroupSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of group signals. I.e. signals that are included within a signal group.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. ComBitPosition

- **UUID**: `ECUC:6372b3fa-3859-971d-2e2f-348910deba67`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

############ 2. ComBitSize

- **UUID**: `ECUC:c47c6c1b-c952-8f3d-5baa-19367ea4e13e`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

############ 3. ComHandleId

- **UUID**: `ECUC:c4319086-46ed-8c8d-5b9f-215eeeb63f86`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

############ 4. ComSignalLength

- **UUID**: `ECUC:f5057591-b7ef-95f5-3b26-b540327897e6`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

########### STRING 类型参数

############ 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:5295fdd0-d804-8f00-2ddd-8eef9d2fc9fa`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

############ 2. ComSignalInitValue

- **UUID**: `ECUC:e43400e6-0497-891f-423b-26164272a2a0`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

########### ENUMERATION 类型参数

############ 1. ComSignalEndianness

- **UUID**: `ECUC:c530db4c-b8cc-932f-3a7c-821d5075c2fa`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

############ 2. ComSignalType

- **UUID**: `ECUC:c36e63f5-6ddc-93ea-3a22-31dedcffc4fe`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

############ 3. ComTransferProperty

- **UUID**: `ECUC:74335baf-cc2f-4470-9926-0dde9c21f642`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optionally defines whether this group signal shall contribute to the TRIGGERED_ON_CHANGE transfer property of the signal group. If at least one  group signal of a signal group has the "ComTransferProperty" configured all other group signals of that signal group shall have the attribute configured as well.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:1a324ef0-bed5-968f-51d2-1e173bcc5dea`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############## 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############## 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############# ENUMERATION 类型参数

############## 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

######### 2. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 19. ComGroupSignal

**容器属性**:

- **UUID**: `ECUC:bc99abe1-7836-48fc-a311-6428aaf3773b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGroupSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of group signals. I.e. signals that are included within a signal group.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:6372b3fa-3859-971d-2e2f-348910deba67`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComBitSize

- **UUID**: `ECUC:c47c6c1b-c952-8f3d-5baa-19367ea4e13e`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

########## 3. ComHandleId

- **UUID**: `ECUC:c4319086-46ed-8c8d-5b9f-215eeeb63f86`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

########## 4. ComSignalLength

- **UUID**: `ECUC:f5057591-b7ef-95f5-3b26-b540327897e6`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

######### STRING 类型参数

########## 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:5295fdd0-d804-8f00-2ddd-8eef9d2fc9fa`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

########## 2. ComSignalInitValue

- **UUID**: `ECUC:e43400e6-0497-891f-423b-26164272a2a0`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:c530db4c-b8cc-932f-3a7c-821d5075c2fa`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComSignalType

- **UUID**: `ECUC:c36e63f5-6ddc-93ea-3a22-31dedcffc4fe`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

########## 3. ComTransferProperty

- **UUID**: `ECUC:74335baf-cc2f-4470-9926-0dde9c21f642`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optionally defines whether this group signal shall contribute to the TRIGGERED_ON_CHANGE transfer property of the signal group. If at least one  group signal of a signal group has the "ComTransferProperty" configured all other group signals of that signal group shall have the attribute configured as well.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:1a324ef0-bed5-968f-51d2-1e173bcc5dea`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 20. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 21. ComTimeBase

**容器属性**:

- **UUID**: `ECUC:6ab9e562-e6e7-42d2-b654-5851adc09e3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTimeBase`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the timebase parameters for Tx, Rx and routing.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. ComGwTimeBase

- **UUID**: `ECUC:7eec51bf-3de0-4c96-b3b9-3ed94229efdf`
- **参数名**: `ComGwTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionRouteSignals in seconds. This parameter may be used by the COM generator to transform the values of the signal gateway related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

########## 2. ComRxTimeBase

- **UUID**: `ECUC:75011746-cdd3-476e-b865-12008e7fa625`
- **参数名**: `ComRxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionRx in seconds. This parameter may be used by the COM generator to transform the values of the reception related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

########## 3. ComTxTimeBase

- **UUID**: `ECUC:e546fc3c-05c3-48e4-b0d1-15b4d0f450fc`
- **参数名**: `ComTxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionTx in seconds. This parameter may be used by the COM generator to transform the values of the transmission related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

####### 22. ComGwDestination

**容器属性**:

- **UUID**: `ECUC:007f74c9-4d99-4605-a6cd-abd1ce2c888c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwDestination`
- **多重性**: [1..infinite]

**容器选择**:

- **ComGwDestinationDescription**
  - UUID: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
  - 描述: Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.
- **ComFilter**
  - UUID: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
  - 描述: This container contains the configuration parameters of the AUTOSAR COM module's Filters.
- **ComGwSignal**
  - UUID: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

**容器描述**:

Each instance of this choice container allows to define one routing destination either by reference to an already configured COM signal / signal group or by a  destination description container.

####### 23. ComGwSource

**容器属性**:

- **UUID**: `ECUC:2803821f-4944-49d4-bcbf-aa360bda4907`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwSource`
- **多重性**: [1..1]

**容器选择**:

- **ComGwSignal**
  - UUID: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.
- **ComGwSourceDescription**
  - UUID: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
  - 描述: Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

**容器描述**:

This choice container allows the definition of the gateway source signal either by reference to an already configured COM signal / signal group or by a  source description container.

##### 2. ComGwMapping

**容器属性**:

- **UUID**: `ECUC:c290eaea-e207-4f2e-89a5-134d43a125a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwMapping`
- **多重性**: [0..infinite]
- **多配置容器**: false

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. ComGwDestinationDescription

**容器属性**:

- **UUID**: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwDestinationDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:a9d55d52-13f7-9895-1dba-0e140e8f522f`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComUpdateBitPosition

- **UUID**: `ECUC:53d6e619-a6d4-8b2c-3f29-7230c53687ce`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### STRING 类型参数

########## 1. ComSignalInitValue

- **UUID**: `ECUC:2a96aa3d-e035-8a97-31c5-ffa140233a68`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:0b9384a4-946a-94a7-2a07-5ba84e265ac2`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComTransferProperty

- **UUID**: `ECUC:ecf98909-3c1d-91ca-3903-106b9cedcad2`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComGwIPduRef

- **UUID**: `ECUC:b2a6fa40-d2bf-8b35-35e3-7f71a89ce3da`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 2. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 3. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ComGwSignalRef

- **UUID**: `ECUC:89dd8bb0-170c-d8ba-21c3-b5c6074dd9e5`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

####### 4. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. ComGwSignalRef

- **UUID**: `ECUC:b1619906-12b7-dc89-37b5-b42a44fb9a60`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

####### 5. ComGwSourceDescription

**容器属性**:

- **UUID**: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSourceDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:80714b1d-25ca-98ce-4488-e89e1022769a`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComBitSize

- **UUID**: `ECUC:e17b033e-b6c3-90ee-7203-cd4b7de89d71`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

########## 3. ComSignalLength

- **UUID**: `ECUC:12040cb4-a560-97a6-5180-695531bc5419`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

########## 4. ComUpdateBitPosition

- **UUID**: `ECUC:2a72d3e4-b8a7-8b65-65f8-4cbac6c9ac39`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:e22f726f-a63d-94e0-50d6-36324fb97f2d`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComSignalType

- **UUID**: `ECUC:e06cfb18-5b4d-959b-507b-e5f3dc438131`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComGwIPduRef

- **UUID**: `ECUC:8942e80b-e492-8b6e-5cb2-59fbaa300845`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

####### 6. ComGwDestination

**容器属性**:

- **UUID**: `ECUC:007f74c9-4d99-4605-a6cd-abd1ce2c888c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwDestination`
- **多重性**: [1..infinite]

**容器选择**:

- **ComGwDestinationDescription**
  - UUID: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
  - 描述: Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.
- **ComFilter**
  - UUID: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
  - 描述: This container contains the configuration parameters of the AUTOSAR COM module's Filters.
- **ComGwSignal**
  - UUID: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

**容器描述**:

Each instance of this choice container allows to define one routing destination either by reference to an already configured COM signal / signal group or by a  destination description container.

####### 7. ComGwSource

**容器属性**:

- **UUID**: `ECUC:2803821f-4944-49d4-bcbf-aa360bda4907`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwSource`
- **多重性**: [1..1]

**容器选择**:

- **ComGwSignal**
  - UUID: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.
- **ComGwSourceDescription**
  - UUID: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
  - 描述: Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

**容器描述**:

This choice container allows the definition of the gateway source signal either by reference to an already configured COM signal / signal group or by a  source description container.

##### 3. ComGwDestinationDescription

**容器属性**:

- **UUID**: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwDestinationDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. ComBitPosition

- **UUID**: `ECUC:a9d55d52-13f7-9895-1dba-0e140e8f522f`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

######## 2. ComUpdateBitPosition

- **UUID**: `ECUC:53d6e619-a6d4-8b2c-3f29-7230c53687ce`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

####### STRING 类型参数

######## 1. ComSignalInitValue

- **UUID**: `ECUC:2a96aa3d-e035-8a97-31c5-ffa140233a68`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

####### ENUMERATION 类型参数

######## 1. ComSignalEndianness

- **UUID**: `ECUC:0b9384a4-946a-94a7-2a07-5ba84e265ac2`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

######## 2. ComTransferProperty

- **UUID**: `ECUC:ecf98909-3c1d-91ca-3903-106b9cedcad2`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComGwIPduRef

- **UUID**: `ECUC:b2a6fa40-d2bf-8b35-35e3-7f71a89ce3da`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 4. ComFilter

**容器属性**:

- **UUID**: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. ComFilterMask

- **UUID**: `ECUC:7805082d-7971-d0e6-cf5f-69a2cfbde0c3`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 2. ComFilterMax

- **UUID**: `ECUC:0824e635-998e-cfd5-b607-47ccfb97a8e3`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 3. ComFilterMin

- **UUID**: `ECUC:689bbdc7-90e1-d2f6-c522-4401a59d181f`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 4. ComFilterOffset

- **UUID**: `ECUC:5f3d95fe-9032-cf47-d434-525de7c9d30f`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 5. ComFilterPeriod

- **UUID**: `ECUC:cc407bb6-0c02-cd27-b812-391fbf021b5d`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

######## 6. ComFilterX

- **UUID**: `ECUC:5aaf6d66-6dfe-d243-ad66-9c30197c6b72`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

####### ENUMERATION 类型参数

######## 1. ComFilterAlgorithm

- **UUID**: `ECUC:95540f43-264b-d487-990c-d67a5b818dc6`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 5. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. ComGwSignalRef

- **UUID**: `ECUC:89dd8bb0-170c-d8ba-21c3-b5c6074dd9e5`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

##### 6. ComGwSignal

**容器属性**:

- **UUID**: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSignal`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. ComGwSignalRef

- **UUID**: `ECUC:b1619906-12b7-dc89-37b5-b42a44fb9a60`
- **引用名**: `ComGwSignalRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup/ComGroupSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
  - `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an object of a gateway relation. Either to a ComSignal, ComGroupSignal or to a SignalGroup.

##### 7. ComGwSourceDescription

**容器属性**:

- **UUID**: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGwSourceDescription`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. ComBitPosition

- **UUID**: `ECUC:80714b1d-25ca-98ce-4488-e89e1022769a`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

######## 2. ComBitSize

- **UUID**: `ECUC:e17b033e-b6c3-90ee-7203-cd4b7de89d71`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

######## 3. ComSignalLength

- **UUID**: `ECUC:12040cb4-a560-97a6-5180-695531bc5419`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

######## 4. ComUpdateBitPosition

- **UUID**: `ECUC:2a72d3e4-b8a7-8b65-65f8-4cbac6c9ac39`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

####### ENUMERATION 类型参数

######## 1. ComSignalEndianness

- **UUID**: `ECUC:e22f726f-a63d-94e0-50d6-36324fb97f2d`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

######## 2. ComSignalType

- **UUID**: `ECUC:e06cfb18-5b4d-959b-507b-e5f3dc438131`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComGwIPduRef

- **UUID**: `ECUC:8942e80b-e492-8b6e-5cb2-59fbaa300845`
- **引用名**: `ComGwIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComIPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an I-PDU of a Signal Gateway source or destination description.

##### 8. ComIPdu

**容器属性**:

- **UUID**: `ECUC:2369f6e2-91a1-4a41-9a26-ca4deec17900`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's I-PDUs.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. ComIPduHandleId

- **UUID**: `ECUC:ae2fd4f0-9482-4454-8bad-fa692d275b39`
- **参数名**: `ComIPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID of this I-PDU. The ComIPduHandleId is required by the API calls to receive I-PDUs from the PduR (ComIP-duDirection: Receive). For Tx-I-PDUs (ComIPduDirection: Send) this handle Id is used by the PduR to confirm the transmission of the ComIPdu. In case no Tx-Confirmation is configured for a Tx-I-PDU, the ComIPduHandleId is not used.

####### BOOLEAN 类型参数

######## 1. ComIPduCancellationSupport

- **UUID**: `ECUC:590e65ba-bcf3-4622-a02c-f9cd1768902b`
- **参数名**: `ComIPduCancellationSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines for I-PDUs with ComIPduType NORMAL:

####### ENUMERATION 类型参数

######## 1. ComIPduDirection

- **UUID**: `ECUC:602c5de9-9aae-48e0-90c5-5e40a3ee1562`
- **参数名**: `ComIPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RECEIVE` (来源: AUTOSAR_ECUC)
  - `SEND` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The direction defines if this I-PDU, and therefore the contributing signals and signal groups, shall be sent or received.

######## 2. ComIPduSignalProcessing

- **UUID**: `ECUC:d23c5427-29e4-4828-9509-d2a6e953bced`
- **参数名**: `ComIPduSignalProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DEFERRED` (来源: AUTOSAR_ECUC)
  - `IMMEDIATE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For the definition of the two modes Immediate and Deferred.

######## 3. ComIPduType

- **UUID**: `ECUC:c64c0d10-9152-443d-91b9-13195e7eb049`
- **参数名**: `ComIPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NORMAL` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if this I-PDU is a normal I-PDU that can be sent unfragmented or if this is a large I-PDU that shall be sent via the Transport Protocol of the underlying bus.

####### FUNCTION-NAME 类型参数

######## 1. ComIPduCallout

- **UUID**: `ECUC:dfd7f113-2d92-42e3-9682-466e04f70473`
- **参数名**: `ComIPduCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the existence and the name of a callout function for the corresponding I-PDU. If this parameter is omitted no I-PDU callout shall take place for the corresponding I-PDU.

######## 2. ComIPduTriggerTransmitCallout

- **UUID**: `ECUC:142dca8a-fcb4-4444-ba45-c5954999b77f`
- **参数名**: `ComIPduTriggerTransmitCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If there is a trigger transmit callout defined for this I-PDU this parameter contains the name of the callout function.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. ComIPduGroupRef

- **UUID**: `ECUC:b55a77e7-c54c-4f56-aec1-e222f78228ba`
- **引用名**: `ComIPduGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the I-PDU groups this I-PDU belongs to.

######## 2. ComIPduSignalGroupRef

- **UUID**: `ECUC:7171db05-bd44-4f33-8fcc-345182c94c9b`
- **引用名**: `ComIPduSignalGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComSignalGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignalGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all signal groups contained in this I-Pdu

######## 3. ComIPduSignalRef

- **UUID**: `ECUC:ee4c14ce-6b3a-44d8-b206-b5e824aefbaa`
- **引用名**: `ComIPduSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all signals contained in this I-PDU.

######## 4. ComPduIdRef

- **UUID**: `ECUC:55b82985-70d9-400f-9e67-3d51f7f00ac9`
- **引用名**: `ComPduIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. ComIPduCounter

**容器属性**:

- **UUID**: `ECUC:138ce27a-5e66-468b-98f8-0983b735c064`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduCounter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the configuration parameters of PDU Counter.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduCounterSize

- **UUID**: `ECUC:6960bb22-331a-4158-92a2-5dbb400df6ab`
- **参数名**: `ComIPduCounterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of PDU Counter expressed in bits

########## 2. ComIPduCounterStartPosition

- **UUID**: `ECUC:415ccc35-3f77-4f12-bb9f-7043ea53d655`
- **参数名**: `ComIPduCounterStartPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of PDU counter expressed in bits from start position of data content

########## 3. ComIPduCounterThreshold

- **UUID**: `ECUC:314f81b7-17b3-4607-9cc1-732bacf2abf5`
- **参数名**: `ComIPduCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold value of I-PDU counter algorithm, see COM590.

######### FUNCTION-NAME 类型参数

########## 1. ComIPduCounterErrorNotification

- **UUID**: `ECUC:4859caf3-c801-4c24-abcc-3a0b2d51adca`
- **参数名**: `ComIPduCounterErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Com_CbkCounterErr callback function to be called. If this

####### 2. ComIPduReplication

**容器属性**:

- **UUID**: `ECUC:57263070-9b06-41b7-9e1c-33b4d1c65828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduReplication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the information needed for each I-PDU replicated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ComIPduReplicationQuorum

- **UUID**: `ECUC:fe74bf86-eac7-4720-8293-5addf106b811`
- **参数名**: `ComIPduReplicationQuorum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of identical I-PDUs needed for successful voting.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComIPduReplicaRef

- **UUID**: `ECUC:f03e9979-e355-481d-a1ca-f1ae44448996`
- **引用名**: `ComIPduReplicaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..2]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to replicas PduR PDUs of this IPDU.

####### 3. ComTxIPdu

**容器属性**:

- **UUID**: `ECUC:46a4bca4-69d5-4f21-88ea-b445b29a6601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxIPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains additional transmission related configuration parameters of the AUTOSAR COM module's I-PDUs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. ComTxIPduUnusedAreasDefault

- **UUID**: `ECUC:af4f2f68-10af-48ca-8c08-dd0ab4921c81`
- **参数名**: `ComTxIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR COM module fills not used areas of an I-PDU with this byte pattern. This attribute is mandatory to avoid undefined behaviour. This byte-pattern will be repeated throughout the I-PDU before any init-values or update-bits were set.

######### FLOAT 类型参数

########## 1. ComMinimumDelayTime

- **UUID**: `ECUC:f1629245-0cb7-4189-9861-19caabedb323`
- **参数名**: `ComMinimumDelayTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC V3.0
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU in seconds. The MDT is independent of the possible different transmission modes. There is only one minimum delay time parameter for one I-PDU. The minimum delay timer is not reset by changing the transmission mode. Hence, it is not allowed to violate the minimum delay time by transmission mode changes. It is not possible to monitor the minimum delay time for I-PDUs that are requested using the Com_TriggerTransmit API.

######### ENUMERATION 类型参数

########## 1. ComTxIPduClearUpdateBit

- **UUID**: `ECUC:f3654eba-0ff7-40df-aad5-71812f896052`
- **参数名**: `ComTxIPduClearUpdateBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Confirmation` (来源: AUTOSAR_ECUC)
  - `Transmit` (来源: AUTOSAR_ECUC)
  - `TriggerTransmit` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines when the update-bits of signals or signal groups, contained in this I-PDU, will be cleared.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 2. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 3. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

############ 参数配置

此容器包含 **5** 个参数：

############# INTEGER 类型参数

############## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

############# FLOAT 类型参数

############## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############# ENUMERATION 类型参数

############## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

######### 4. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 4. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 5. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 6. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 7. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 9. ComIPduCounter

**容器属性**:

- **UUID**: `ECUC:138ce27a-5e66-468b-98f8-0983b735c064`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduCounter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the configuration parameters of PDU Counter.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. ComIPduCounterSize

- **UUID**: `ECUC:6960bb22-331a-4158-92a2-5dbb400df6ab`
- **参数名**: `ComIPduCounterSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of PDU Counter expressed in bits

######## 2. ComIPduCounterStartPosition

- **UUID**: `ECUC:415ccc35-3f77-4f12-bb9f-7043ea53d655`
- **参数名**: `ComIPduCounterStartPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of PDU counter expressed in bits from start position of data content

######## 3. ComIPduCounterThreshold

- **UUID**: `ECUC:314f81b7-17b3-4607-9cc1-732bacf2abf5`
- **参数名**: `ComIPduCounterThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold value of I-PDU counter algorithm, see COM590.

####### FUNCTION-NAME 类型参数

######## 1. ComIPduCounterErrorNotification

- **UUID**: `ECUC:4859caf3-c801-4c24-abcc-3a0b2d51adca`
- **参数名**: `ComIPduCounterErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of Com_CbkCounterErr callback function to be called. If this

##### 10. ComIPduReplication

**容器属性**:

- **UUID**: `ECUC:57263070-9b06-41b7-9e1c-33b4d1c65828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduReplication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container contains the information needed for each I-PDU replicated.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ComIPduReplicationQuorum

- **UUID**: `ECUC:fe74bf86-eac7-4720-8293-5addf106b811`
- **参数名**: `ComIPduReplicationQuorum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The number of identical I-PDUs needed for successful voting.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComIPduReplicaRef

- **UUID**: `ECUC:f03e9979-e355-481d-a1ca-f1ae44448996`
- **引用名**: `ComIPduReplicaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..2]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to replicas PduR PDUs of this IPDU.

##### 11. ComTxIPdu

**容器属性**:

- **UUID**: `ECUC:46a4bca4-69d5-4f21-88ea-b445b29a6601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxIPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains additional transmission related configuration parameters of the AUTOSAR COM module's I-PDUs.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. ComTxIPduUnusedAreasDefault

- **UUID**: `ECUC:af4f2f68-10af-48ca-8c08-dd0ab4921c81`
- **参数名**: `ComTxIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR COM module fills not used areas of an I-PDU with this byte pattern. This attribute is mandatory to avoid undefined behaviour. This byte-pattern will be repeated throughout the I-PDU before any init-values or update-bits were set.

####### FLOAT 类型参数

######## 1. ComMinimumDelayTime

- **UUID**: `ECUC:f1629245-0cb7-4189-9861-19caabedb323`
- **参数名**: `ComMinimumDelayTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC V3.0
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU in seconds. The MDT is independent of the possible different transmission modes. There is only one minimum delay time parameter for one I-PDU. The minimum delay timer is not reset by changing the transmission mode. Hence, it is not allowed to violate the minimum delay time by transmission mode changes. It is not possible to monitor the minimum delay time for I-PDUs that are requested using the Com_TriggerTransmit API.

####### ENUMERATION 类型参数

######## 1. ComTxIPduClearUpdateBit

- **UUID**: `ECUC:f3654eba-0ff7-40df-aad5-71812f896052`
- **参数名**: `ComTxIPduClearUpdateBit`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Confirmation` (来源: AUTOSAR_ECUC)
  - `Transmit` (来源: AUTOSAR_ECUC)
  - `TriggerTransmit` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines when the update-bits of signals or signal groups, contained in this I-PDU, will be cleared.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 2. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 3. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

########### FLOAT 类型参数

############ 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

############ 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

############ 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########### ENUMERATION 类型参数

############ 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

####### 4. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 12. ComTxModeFalse

**容器属性**:

- **UUID**: `ECUC:94b40004-9c9e-4156-9f49-4b4d102d260d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeFalse`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to false.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 13. ComTxMode

**容器属性**:

- **UUID**: `ECUC:a765973c-9c32-8f36-59d0-25e9fe09f415`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:6fb3519d-c40b-db38-fd08-70f912baedec`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

####### FLOAT 类型参数

######## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:faeb57d4-bfe7-d50c-eb8c-1ef6d82df89a`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

######## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:ce45c969-d5d9-d305-f36e-8e8a95353990`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:c4e629ae-8c57-d86c-180d-80c1a8431e94`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

####### ENUMERATION 类型参数

######## 1. ComTxModeMode

- **UUID**: `ECUC:2cfd31fd-6975-d281-1948-06fb4cb75607`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 14. ComTxModeTrue

**容器属性**:

- **UUID**: `ECUC:be11f44a-ac3e-49f0-a62c-aa0a0e4b16d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxModeTrue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes in the case the ComFilter evaluates to true.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

######### FLOAT 类型参数

########## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

########## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

########## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######### ENUMERATION 类型参数

########## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 15. ComTxMode

**容器属性**:

- **UUID**: `ECUC:d0c38b82-abd2-97d0-60b3-84a6fc27e4db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTxMode`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. ComTxModeNumberOfRepetitions

- **UUID**: `ECUC:991145e3-d3ab-e3d2-03eb-cfb610d8deb2`
- **参数名**: `ComTxModeNumberOfRepetitions`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of repetitions for the transmission mode DIRECT and the event driven part of transmission mode MIXED.

####### FLOAT 类型参数

######## 1. ComTxModeRepetitionPeriod

- **UUID**: `ECUC:24494c1a-cf87-dda6-f26f-7db3d64be960`
- **参数名**: `ComTxModeRepetitionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the multiple transmissions in case ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is configured to DIRECT or MIXED. In case of the mixed transmission mode only the event driven part is affected.

######## 2. ComTxModeTimeOffset

- **UUID**: `ECUC:f7a3bdaf-e579-db9f-fa51-ed4793532a56`
- **参数名**: `ComTxModeTimeOffset`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

######## 3. ComTxModeTimePeriod

- **UUID**: `ECUC:ee441df4-9bf7-e106-1ef0-df7ea6610f5a`
- **参数名**: `ComTxModeTimePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repetition period in seconds of the periodic transmission requests in case ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode only the periodic part is affected.

####### ENUMERATION 类型参数

######## 1. ComTxModeMode

- **UUID**: `ECUC:565b2643-7915-db1b-202b-65b84ad546cd`
- **参数名**: `ComTxModeMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PERIODIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The available transmission modes described in [18] shall be extended by the additional mode None.

##### 16. ComIPduGroup

**容器属性**:

- **UUID**: `ECUC:9c06af69-2cee-4cff-958e-722ca870926f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComIPduGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's I-PDU groups.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ComIPduGroupHandleId

- **UUID**: `ECUC:0db9c161-2c65-400c-a788-45eafacdc525`
- **参数名**: `ComIPduGroupHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID of this I-PDU Group .

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComIPduGroupGroupRef

- **UUID**: `ECUC:8cd1cdc0-4ac4-408d-88a4-6c307023695e`
- **引用名**: `ComIPduGroupGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComIPduGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComIPduGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all I-PDU groups that includes this I-PDU group. If this reference is omitted this I-PDU group does not belong to another I-PDU group.

##### 17. ComSignal

**容器属性**:

- **UUID**: `ECUC:6821e00a-9135-4a29-8f7e-394c346f3711`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's signals.

###### 参数配置

此容器包含 **18** 个参数：

####### INTEGER 类型参数

######## 1. ComBitPosition

- **UUID**: `ECUC:0efae823-5158-984a-1a9c-09ac9a5a7a3d`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

######## 2. ComBitSize

- **UUID**: `ECUC:7004a044-e251-906a-4816-ee5a0820a114`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

######## 3. ComHandleId

- **UUID**: `ECUC:6fb9c4af-5fec-8dba-480b-f6827831ff5c`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

######## 4. ComSignalLength

- **UUID**: `ECUC:a08da9ba-d0ee-9722-2793-8a63bbf457bc`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

######## 5. ComUpdateBitPosition

- **UUID**: `ECUC:b8fc70ea-e435-8ae1-3c0b-6dc95101afdc`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

####### FLOAT 类型参数

######## 1. ComFirstTimeout

- **UUID**: `ECUC:efde3e34-acb9-8a6b-4cee-a372064d2d67`
- **参数名**: `ComFirstTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is used immediately after start (or restart) of the deadline monitoring service. The timeout period of the successive periods is configured by COM263_Conf.

######## 2. ComTimeout

- **UUID**: `ECUC:7fdf73ac-5b6f-9942-422a-b04f791e2cd8`
- **参数名**: `ComTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the deadline monitoring timeout period in seconds. The period for the first timeout period can be configured separately by COM183_Conf.

####### STRING 类型参数

######## 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:fe1e31f9-f103-902d-1a4a-641326ab89d0`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

######## 2. ComSignalInitValue

- **UUID**: `ECUC:8fbc350f-1d96-8a4c-2ea7-fb39cbee6276`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

####### ENUMERATION 类型参数

######## 1. ComDataInvalidAction

- **UUID**: `ECUC:0b851468-e9b8-8eb5-23bd-7f1f24242421`
- **参数名**: `ComDataInvalidAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NOTIFY` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon reception of an invalid signal.

######## 2. ComRxDataTimeoutAction

- **UUID**: `ECUC:f4b36b66-eb9b-96f7-40cd-1942ddc22bd5`
- **参数名**: `ComRxDataTimeoutAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NONE` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon expiration of the  reception deadline monitoring timer.

######## 3. ComSignalEndianness

- **UUID**: `ECUC:70b90f75-d1cb-945c-26e9-5740d9f182d0`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

######## 4. ComSignalType

- **UUID**: `ECUC:6ef6981e-86db-9517-268f-0702667b84d4`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

######## 5. ComTransferProperty

- **UUID**: `ECUC:521f13da-797e-917f-35e5-0c0428b8f2e0`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

####### FUNCTION-NAME 类型参数

######## 1. ComErrorNotification

- **UUID**: `ECUC:1dfd0b59-8b1e-8f59-40fd-3d57a237f88c`
- **参数名**: `ComErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.

######## 2. ComInvalidNotification

- **UUID**: `ECUC:0c9bd76e-1519-9774-43ff-0d2dab2d1446`
- **参数名**: `ComInvalidNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the function which notifies the RTE about the reception of an invalidated signal/ signal group. Only applicable if ComDataInvalidAction is configured to NOTIFY.

######## 3. ComNotification

- **UUID**: `ECUC:01cfe381-c4e1-9609-35fd-75f7b8646113`
- **参数名**: `ComNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxAck callback function to be called.

######## 4. ComTimeoutNotification

- **UUID**: `ECUC:c14a1a71-124c-957d-32e0-7977e8ff640b`
- **参数名**: `ComTimeoutNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxTOut callback function to be called.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:c5ba8319-d7d4-97bc-3e3e-f33ac5481dc0`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ab01c3ee-dd49-8ae7-11da-6503b3be2510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:dd2a92fe-b6d2-d09b-cc41-653b5b8908d1`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:6d4a7106-d6ef-cf8a-b2e9-43658762d0f1`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:cdc14898-ce42-d2ab-c204-3f9a3168402d`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:c46320cf-cd93-cefc-d116-4df67394fb1d`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:31660687-4963-ccdc-b4f4-34b84acd436b`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:bfd4f837-ab5f-d1f8-aa48-97c8a5479380`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:fa799a14-63ac-d43c-95ee-d212e74cb5d4`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 18. ComFilter

**容器属性**:

- **UUID**: `ECUC:ab01c3ee-dd49-8ae7-11da-6503b3be2510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. ComFilterMask

- **UUID**: `ECUC:dd2a92fe-b6d2-d09b-cc41-653b5b8908d1`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 2. ComFilterMax

- **UUID**: `ECUC:6d4a7106-d6ef-cf8a-b2e9-43658762d0f1`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 3. ComFilterMin

- **UUID**: `ECUC:cdc14898-ce42-d2ab-c204-3f9a3168402d`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 4. ComFilterOffset

- **UUID**: `ECUC:c46320cf-cd93-cefc-d116-4df67394fb1d`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 5. ComFilterPeriod

- **UUID**: `ECUC:31660687-4963-ccdc-b4f4-34b84acd436b`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

######## 6. ComFilterX

- **UUID**: `ECUC:bfd4f837-ab5f-d1f8-aa48-97c8a5479380`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

####### ENUMERATION 类型参数

######## 1. ComFilterAlgorithm

- **UUID**: `ECUC:fa799a14-63ac-d43c-95ee-d212e74cb5d4`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 19. ComSignalGroup

**容器属性**:

- **UUID**: `ECUC:ec4cc19d-8379-4c52-a8aa-9d4d0f11759c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComSignalGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters of the AUTOSAR COM module's signal groups.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. ComHandleId

- **UUID**: `ECUC:f3e4a642-5230-8fe3-6138-5a8352d43de7`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

######## 2. ComUpdateBitPosition

- **UUID**: `ECUC:3d27527d-d679-8d0a-5537-d1ca2ba3ee67`
- **参数名**: `ComUpdateBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Bit position of update-bit inside I-PDU.

####### FLOAT 类型参数

######## 1. ComFirstTimeout

- **UUID**: `ECUC:74091fc7-9efd-8c94-661b-0772e0ef6bf2`
- **参数名**: `ComFirstTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is used immediately after start (or restart) of the deadline monitoring service. The timeout period of the successive periods is configured by COM263_Conf.

######## 2. ComTimeout

- **UUID**: `ECUC:040a553f-4db3-9b6b-5b57-145053c06b63`
- **参数名**: `ComTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the length of the deadline monitoring timeout period in seconds. The period for the first timeout period can be configured separately by COM183_Conf.

####### ENUMERATION 类型参数

######## 1. ComDataInvalidAction

- **UUID**: `ECUC:8faff5fb-dbfc-90de-3ce9-e31ffec662ac`
- **参数名**: `ComDataInvalidAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NOTIFY` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon reception of an invalid signal.

######## 2. ComRxDataTimeoutAction

- **UUID**: `ECUC:78de4cf9-dddf-9920-59f9-7d43b8646a60`
- **参数名**: `ComRxDataTimeoutAction`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NONE` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the action performed upon expiration of the  reception deadline monitoring timer.

######## 3. ComTransferProperty

- **UUID**: `ECUC:d649f56d-6bc2-93a8-4f11-7005035b316b`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_WITHOUT_REPETITION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a write access to this signal can trigger the transmission of the corresponding I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the corresponding I-PDU.

####### FUNCTION-NAME 类型参数

######## 1. ComErrorNotification

- **UUID**: `ECUC:a227ecec-7d62-9182-5a29-a1587cda3717`
- **参数名**: `ComErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.

######## 2. ComInvalidNotification

- **UUID**: `ECUC:90c6b901-075d-999d-5d2b-712e85cf52d1`
- **参数名**: `ComInvalidNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the function which notifies the RTE about the reception of an invalidated signal/ signal group. Only applicable if ComDataInvalidAction is configured to NOTIFY.

######## 3. ComNotification

- **UUID**: `ECUC:85fac514-b725-9832-4f29-d9f893069f9e`
- **参数名**: `ComNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxAck callback function to be called.

######## 4. ComTimeoutNotification

- **UUID**: `ECUC:4574fc04-0490-97a6-4c0c-dd78c3a1a296`
- **参数名**: `ComTimeoutNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On sender side: Name of Com_CbkTxTOut callback function to be called.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. ComSystemTemplateSignalGroupRef

- **UUID**: `ECUC:915b9295-5b7d-414e-abc1-47140c383e4e`
- **引用名**: `ComSystemTemplateSignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignalGroup (SystemTemplate)  which this ComSignalGroup represents.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. ComGroupSignal

**容器属性**:

- **UUID**: `ECUC:bc99abe1-7836-48fc-a311-6428aaf3773b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGroupSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of group signals. I.e. signals that are included within a signal group.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. ComBitPosition

- **UUID**: `ECUC:6372b3fa-3859-971d-2e2f-348910deba67`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

########## 2. ComBitSize

- **UUID**: `ECUC:c47c6c1b-c952-8f3d-5baa-19367ea4e13e`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

########## 3. ComHandleId

- **UUID**: `ECUC:c4319086-46ed-8c8d-5b9f-215eeeb63f86`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

########## 4. ComSignalLength

- **UUID**: `ECUC:f5057591-b7ef-95f5-3b26-b540327897e6`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

######### STRING 类型参数

########## 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:5295fdd0-d804-8f00-2ddd-8eef9d2fc9fa`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

########## 2. ComSignalInitValue

- **UUID**: `ECUC:e43400e6-0497-891f-423b-26164272a2a0`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

######### ENUMERATION 类型参数

########## 1. ComSignalEndianness

- **UUID**: `ECUC:c530db4c-b8cc-932f-3a7c-821d5075c2fa`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

########## 2. ComSignalType

- **UUID**: `ECUC:c36e63f5-6ddc-93ea-3a22-31dedcffc4fe`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

########## 3. ComTransferProperty

- **UUID**: `ECUC:74335baf-cc2f-4470-9926-0dde9c21f642`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optionally defines whether this group signal shall contribute to the TRIGGERED_ON_CHANGE transfer property of the signal group. If at least one  group signal of a signal group has the "ComTransferProperty" configured all other group signals of that signal group shall have the attribute configured as well.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:1a324ef0-bed5-968f-51d2-1e173bcc5dea`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

############ 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

############ 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########### ENUMERATION 类型参数

############ 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

####### 2. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 20. ComGroupSignal

**容器属性**:

- **UUID**: `ECUC:bc99abe1-7836-48fc-a311-6428aaf3773b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGroupSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of group signals. I.e. signals that are included within a signal group.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ComBitPosition

- **UUID**: `ECUC:6372b3fa-3859-971d-2e2f-348910deba67`
- **参数名**: `ComBitPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not in the shadow buffer. If the endianness conversion is configured to Opaque the parameter ComBitPosition shall define the bit0 of the first byte like in little endian byte order

######## 2. ComBitSize

- **UUID**: `ECUC:c47c6c1b-c952-8f3d-5baa-19367ea4e13e`
- **参数名**: `ComBitSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bits, for non-array signal types.

######## 3. ComHandleId

- **UUID**: `ECUC:c4319086-46ed-8c8d-5b9f-215eeeb63f86`
- **参数名**: `ComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The numerical value used as the ID.

######## 4. ComSignalLength

- **UUID**: `ECUC:f5057591-b7ef-95f5-3b26-b540327897e6`
- **参数名**: `ComSignalLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description:

####### STRING 类型参数

######## 1. ComSignalDataInvalidValue

- **UUID**: `ECUC:5295fdd0-d804-8f00-2ddd-8eef9d2fc9fa`
- **参数名**: `ComSignalDataInvalidValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the data invalid value of the signal.

######## 2. ComSignalInitValue

- **UUID**: `ECUC:e43400e6-0497-891f-423b-26164272a2a0`
- **参数名**: `ComSignalInitValue`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 默认值: `0`
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for this signal. The default value is 0.

####### ENUMERATION 类型参数

######## 1. ComSignalEndianness

- **UUID**: `ECUC:c530db4c-b8cc-932f-3a7c-821d5075c2fa`
- **参数名**: `ComSignalEndianness`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
  - `OPAQUE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the endianness of the signal's network representation.

######## 2. ComSignalType

- **UUID**: `ECUC:c36e63f5-6ddc-93ea-3a22-31dedcffc4fe`
- **参数名**: `ComSignalType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOOLEAN` (来源: AUTOSAR_ECUC)
  - `FLOAT32` (来源: AUTOSAR_ECUC)
  - `FLOAT64` (来源: AUTOSAR_ECUC)
  - `SINT16` (来源: AUTOSAR_ECUC)
  - `SINT32` (来源: AUTOSAR_ECUC)
  - `SINT64` (来源: AUTOSAR_ECUC)
  - `SINT8` (来源: AUTOSAR_ECUC)
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT32` (来源: AUTOSAR_ECUC)
  - `UINT64` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
  - `UINT8_DYN` (来源: AUTOSAR_ECUC)
  - `UINT8_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by examining the value of this attribute.

######## 3. ComTransferProperty

- **UUID**: `ECUC:74335baf-cc2f-4470-9926-0dde9c21f642`
- **参数名**: `ComTransferProperty`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PENDING` (来源: AUTOSAR_ECUC)
  - `TRIGGERED_ON_CHANGE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optionally defines whether this group signal shall contribute to the TRIGGERED_ON_CHANGE transfer property of the signal group. If at least one  group signal of a signal group has the "ComTransferProperty" configured all other group signals of that signal group shall have the attribute configured as well.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. ComSystemTemplateSystemSignalRef

- **UUID**: `ECUC:1a324ef0-bed5-968f-51d2-1e173bcc5dea`
- **引用名**: `ComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this ComSignal (or ComGroupSignal) represents.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

########## 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

########## 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######### ENUMERATION 类型参数

########## 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 21. ComFilter

**容器属性**:

- **UUID**: `ECUC:ff798fc5-c44a-89ba-256d-8fe02a42653a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComFilter`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the AUTOSAR COM module's Filters.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. ComFilterMask

- **UUID**: `ECUC:31a25ed5-9dd3-cf6e-dfd4-9017d20d48fb`
- **参数名**: `ComFilterMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 2. ComFilterMax

- **UUID**: `ECUC:c1c23cdd-bdf0-ce5d-c67c-6e41fde7111b`
- **参数名**: `ComFilterMax`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 3. ComFilterMin

- **UUID**: `ECUC:2239146f-b543-d17e-d597-6a76a7ec8057`
- **参数名**: `ComFilterMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 4. ComFilterOffset

- **UUID**: `ECUC:18daeca6-b494-cdcf-e4a9-78d2ea193b47`
- **参数名**: `ComFilterOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

######## 5. ComFilterPeriod

- **UUID**: `ECUC:85ddd25e-3064-cbaf-c887-5f94c1518395`
- **参数名**: `ComFilterPeriod`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.

######## 6. ComFilterX

- **UUID**: `ECUC:144cc40e-9260-d0cb-bddb-c2a51bcbd3aa`
- **参数名**: `ComFilterX`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The name of this attribute corresponds to the parameter name in the [17] specification of Reception Filtering.

####### ENUMERATION 类型参数

######## 1. ComFilterAlgorithm

- **UUID**: `ECUC:4ef165eb-4aad-d30f-a981-fcef5dd0f5fe`
- **参数名**: `ComFilterAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ALWAYS` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_MASKED_OLD` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_DIFFERS_X` (来源: AUTOSAR_ECUC)
  - `MASKED_NEW_EQUALS_X` (来源: AUTOSAR_ECUC)
  - `NEVER` (来源: AUTOSAR_ECUC)
  - `NEW_IS_OUTSIDE` (来源: AUTOSAR_ECUC)
  - `NEW_IS_WITHIN` (来源: AUTOSAR_ECUC)
  - `ONE_EVERY_N` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The range of values is specified in the [17] specification, chapter 2.2.2, Reception Filtering.

##### 22. ComTimeBase

**容器属性**:

- **UUID**: `ECUC:6ab9e562-e6e7-42d2-b654-5851adc09e3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComTimeBase`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the timebase parameters for Tx, Rx and routing.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. ComGwTimeBase

- **UUID**: `ECUC:7eec51bf-3de0-4c96-b3b9-3ed94229efdf`
- **参数名**: `ComGwTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionRouteSignals in seconds. This parameter may be used by the COM generator to transform the values of the signal gateway related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

######## 2. ComRxTimeBase

- **UUID**: `ECUC:75011746-cdd3-476e-b865-12008e7fa625`
- **参数名**: `ComRxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionRx in seconds. This parameter may be used by the COM generator to transform the values of the reception related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

######## 3. ComTxTimeBase

- **UUID**: `ECUC:e546fc3c-05c3-48e4-b0d1-15b4d0f450fc`
- **参数名**: `ComTxTimeBase`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The period between successive calls to Com_MainFunctionTx in seconds. This parameter may be used by the COM generator to transform the values of the transmission related timing configuration parameters of the COM module to internal implementation specific counter or tick values. The COM module's internal timing handling is implementation specific.

##### 23. ComGeneral

**容器属性**:

- **UUID**: `ECUC:2a2e4d9c-0065-4cfe-ba7b-9a73a0e988db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. ComSupportedIPduGroups

- **UUID**: `ECUC:2bd0c280-d8db-4a93-b38f-bc18a85780aa`
- **参数名**: `ComSupportedIPduGroups`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of supported I-PDU groups.

####### BOOLEAN 类型参数

######## 1. ComConfigurationUseDet

- **UUID**: `ECUC:9bb66a6b-aa9c-4e13-b9d6-a5382d3a4be4`
- **参数名**: `ComConfigurationUseDet`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The error hook shall contain code to call the Det.

######## 2. ComEnableMDTForCyclicTransmission

- **UUID**: `ECUC:0777156b-b5c5-45cd-93c3-2d1a66cc8ffe`
- **参数名**: `ComEnableMDTForCyclicTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables globally for the whole Com module the minimum delay time monitoring for cyclic and repeated transmissions (ComTxModeMode=PERIODIC or ComTxModeMode=MIXED for the cyclic transmissions, ComTxModeNumberOfRepetitions > 0 for repeated transmissions).

######## 3. ComRetryFailedTransmitRequests

- **UUID**: `ECUC:2200aba4-3c6c-4fc4-818a-f5c1d08fd959`
- **参数名**: `ComRetryFailedTransmitRequests`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this Parameter is set to true, retry of failed transmission requests is enabled. If this Parameter is not present, the default value is assumed.

######## 4. ComVersionInfoApi

- **UUID**: `ECUC:391f5569-abda-4a3d-bfb1-af45fba3d69a`
- **参数名**: `ComVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the version information API (Com_GetVersionInfo).

##### 24. ComGwDestination

**容器属性**:

- **UUID**: `ECUC:007f74c9-4d99-4605-a6cd-abd1ce2c888c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwDestination`
- **多重性**: [1..infinite]

**容器选择**:

- **ComGwDestinationDescription**
  - UUID: `ECUC:02fc5539-53d4-4a74-929c-3db3a8a40f03`
  - 描述: Description of a gateway destination. This container allows defining a gateway destination without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.
- **ComFilter**
  - UUID: `ECUC:45dc391d-9fe8-8b32-14f8-696b27f2fd02`
  - 描述: This container contains the configuration parameters of the AUTOSAR COM module's Filters.
- **ComGwSignal**
  - UUID: `ECUC:6f4a2e6b-5d24-918f-64e6-23afaf9c2337`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.

**容器描述**:

Each instance of this choice container allows to define one routing destination either by reference to an already configured COM signal / signal group or by a  destination description container.

##### 25. ComGwSource

**容器属性**:

- **UUID**: `ECUC:2803821f-4944-49d4-bcbf-aa360bda4907`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `ComGwSource`
- **多重性**: [1..1]

**容器选择**:

- **ComGwSignal**
  - UUID: `ECUC:96ce3bc1-58cf-955e-7ad8-2213ed49e3b2`
  - 描述: This container allows specifying a gateway source or destination respectively with a reference to a ComSignal, a ComGroupSignal or a ComSignalGroup.
- **ComGwSourceDescription**
  - UUID: `ECUC:d9984304-65a7-4aad-b96b-183daa37336e`
  - 描述: Description of a gateway source. This container allows defining a gateway source without the configuration of a complete COM signal. This allows adding / changing gateway relations post build without the configuration of new signals.

**容器描述**:

This choice container allows the definition of the gateway source signal either by reference to an already configured COM signal / signal group or by a  source description container.

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

1. **Com**
