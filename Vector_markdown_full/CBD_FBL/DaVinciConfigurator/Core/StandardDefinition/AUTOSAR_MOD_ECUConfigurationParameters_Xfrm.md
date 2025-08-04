# Xfrm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Xfrm](#xfrm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Xfrm

#### 基本信息

- **UUID**: `ECUC:0cabde10-00d9-4b21-a0ac-b7f8bd1f2051`
- **模块名称**: `Xfrm`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. XfrmGeneral

**容器属性**:

- **UUID**: `ECUC:51b96242-7adc-49c3-911f-94278ac3842c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmGeneral`
- **多重性**: [1..1]

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. XfrmDevErrorDetect

- **UUID**: `ECUC:ffd3a6de-0b2b-4cd5-a30f-91ec91a16495`
- **参数名**: `XfrmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

##### 2. XfrmImplementationMapping

**容器属性**:

- **UUID**: `ECUC:eded25d2-5365-4797-9e40-b39b486d09b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmImplementationMapping`
- **多重性**: [1..infinite]

**容器描述**:

For each transformer (TransformationTechnology) in a transformer chain (DataTransformation) which is applied to an ISignal it is necessary to specify the BswModuleEntry which implements it. This is the container to hold these mappings.

###### 引用关系

此容器包含 **5** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfmTransformationBswModuleEntryRef

- **UUID**: `ECUC:16ff50c1-d926-446f-b584-c6da1115e6b2`
- **引用名**: `XfmTransformationBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter is set to obsolete and will be removed in future. Please use XfrmTransformerBswModuleEntryRef instead.

######## 2. XfrmInvTransformerBswModuleEntryRef

- **UUID**: `ECUC:33b97e34-7ced-4043-ac2e-1a8ba1f27604`
- **引用名**: `XfrmInvTransformerBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the BswModuleEntry which implements the referenced inverse transformer on the receiving/called side.

######## 3. XfrmTransformationTechnologyRef

- **UUID**: `ECUC:ada02b50-d9a3-4cb6-a027-066235b538e5`
- **引用名**: `XfrmTransformationTechnologyRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRANSFORMATION-TECHNOLOGY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the TransformationTechnology in the DataTransformation of the system description for which the implementation (BswModuleEntry) shall be mapped.

######## 4. XfrmTransformerBswModuleEntryRef

- **UUID**: `ECUC:858c9ad5-ebaf-4aab-93db-57efa051b60a`
- **引用名**: `XfrmTransformerBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the BswModuleEntry which implements the referenced transformer on the sending/calling side.

####### INSTANCE-REFERENCE 类型引用

######## 1. XfrmVariableDataPrototypeInstanceRef

- **UUID**: `ECUC:39715fc0-99c5-45a3-8ca2-acad41857d9a`
- **引用名**: `XfrmVariableDataPrototypeInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Instance Reference to a VariableDataPrototype in case a dedicated transformer BswModuleEntry is required per VariableDataPrototype access.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. XfrmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:852ef53a-b7ca-4880-b8e3-5add4f585fda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. XFRM_E_MALFORMED_MESSAGE

- **UUID**: `ECUC:f7ad2f1b-8438-41cc-91e0-a7c9f0fc59e9`
- **引用名**: `XFRM_E_MALFORMED_MESSAGE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to configured DEM event to report if malformed messages were received by the transformer.

####### 2. XfrmSignal

**容器属性**:

- **UUID**: `ECUC:7d7b1d99-364e-4dee-a4b1-a0d3b33adf93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmSignal`
- **多重性**: [0..1]

**容器描述**:

Reference to the signal in the system description that transports the transformed data.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. XfrmISignalGroupRef

- **UUID**: `ECUC:05651da3-05d2-4ea2-bb50-1b2773b7749f`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

######### 2. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. XfrmISignalRef

- **UUID**: `ECUC:4272b6aa-98b6-48f3-9d4e-31b38eb69cc6`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

######### 3. XfrmSignalChoice

**容器属性**:

- **UUID**: `ECUC:5f62f597-3b33-4fef-a3e3-05a10a21cbe2`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

####### 3. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalGroupRef

- **UUID**: `ECUC:05651da3-05d2-4ea2-bb50-1b2773b7749f`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

####### 4. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalRef

- **UUID**: `ECUC:4272b6aa-98b6-48f3-9d4e-31b38eb69cc6`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

####### 5. XfrmSignalChoice

**容器属性**:

- **UUID**: `ECUC:5f62f597-3b33-4fef-a3e3-05a10a21cbe2`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

##### 3. XfrmDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:852ef53a-b7ca-4880-b8e3-5add4f585fda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. XFRM_E_MALFORMED_MESSAGE

- **UUID**: `ECUC:f7ad2f1b-8438-41cc-91e0-a7c9f0fc59e9`
- **引用名**: `XFRM_E_MALFORMED_MESSAGE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to configured DEM event to report if malformed messages were received by the transformer.

##### 4. XfrmSignal

**容器属性**:

- **UUID**: `ECUC:7d7b1d99-364e-4dee-a4b1-a0d3b33adf93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmSignal`
- **多重性**: [0..1]

**容器描述**:

Reference to the signal in the system description that transports the transformed data.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalGroupRef

- **UUID**: `ECUC:05651da3-05d2-4ea2-bb50-1b2773b7749f`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

####### 2. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalRef

- **UUID**: `ECUC:4272b6aa-98b6-48f3-9d4e-31b38eb69cc6`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

####### 3. XfrmSignalChoice

**容器属性**:

- **UUID**: `ECUC:5f62f597-3b33-4fef-a3e3-05a10a21cbe2`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

##### 5. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfrmISignalGroupRef

- **UUID**: `ECUC:05651da3-05d2-4ea2-bb50-1b2773b7749f`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

##### 6. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfrmISignalRef

- **UUID**: `ECUC:4272b6aa-98b6-48f3-9d4e-31b38eb69cc6`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

##### 7. XfrmSignalChoice

**容器属性**:

- **UUID**: `ECUC:5f62f597-3b33-4fef-a3e3-05a10a21cbe2`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `ECUC:a9da40ce-5733-4ecb-9932-ecda432c1e65`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `ECUC:860a576f-7827-4a93-9103-b69431d1033d`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

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

1. **Xfrm**
