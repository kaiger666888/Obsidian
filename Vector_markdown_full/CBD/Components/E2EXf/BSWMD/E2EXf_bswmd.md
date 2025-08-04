# E2EXf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:50

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [E2EXf](#e2exf)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-1.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. E2EXf

#### 基本信息

- **UUID**: `33fb6b96-2414-4bc2-a882-53e399262869`
- **模块名称**: `E2EXf`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

End to End Transformer (E2EXF) is used by the Runtime Environment (RTE) to ensure correct communication of safety related signals. It works by appending and checking an additional end to end header to bytestreams that are either sent directly or created by other transformers. 
#Transformer #Safety #RuntimeEnvironment #Communication
#AUTOSAR

#### 版本历史

共有 **26** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2016-05-18T11:36:44+02:00
- **发布者**: visssf

**变更内容**:

##### 2. 版本 1.00.01

- **发布日期**: 2017-01-20T08:50:00+01:00
- **发布者**: vissi

**变更内容**:

##### 3. 版本 1.01.00

- **发布日期**: 2017-01-20T09:30:00+01:00
- **发布者**: vissi

**变更内容**:

##### 4. 版本 1.02.00

- **发布日期**: 2017-05-19T09:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 5. 版本 1.03.00

- **发布日期**: 2017-06-30T09:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 6. 版本 1.04.00

- **发布日期**: 2017-08-29T13:30:00+01:00
- **发布者**: vissi

**变更内容**:

##### 7. 版本 1.05.00

- **发布日期**: 2017-11-20T14:00:00+01:00
- **发布者**: vissi

**变更内容**:

##### 8. 版本 1.06.00

- **发布日期**: 2018-05-05T15:00:26+02:00
- **发布者**: visso

**变更内容**:

##### 9. 版本 1.07.00

- **发布日期**: 2018-09-24T14:29:07+02:00
- **发布者**: visso

**变更内容**:

##### 10. 版本 1.08.00

- **发布日期**: 2019-04-04T11:53:33+02:00
- **发布者**: visso

**变更内容**:

##### 11. 版本 1.09.00

- **发布日期**: 2019-08-28T15:03:37+02:00
- **发布者**: visso

**变更内容**:

##### 12. 版本 1.10.00

- **发布日期**: 2020-04-06T19:07:53+02:00
- **发布者**: visso

**变更内容**:

##### 13. 版本 1.11.00

- **发布日期**: 2020-09-21T17:18:01+02:00
- **发布者**: visso

**变更内容**:

##### 14. 版本 1.12.00

- **发布日期**: 2021-03-23T20:01:54+01:00
- **发布者**: visso

**变更内容**:

##### 15. 版本 1.13.00

- **发布日期**: 2021-09-08T10:39:45+02:00
- **发布者**: visso

**变更内容**:

##### 16. 版本 1.14.00

- **发布日期**: 2021-09-29T17:05:14+02:00
- **发布者**: visssf

**变更内容**:

##### 17. 版本 1.15.00

- **发布日期**: 2021-12-07T14:33:03+01:00
- **发布者**: visso

**变更内容**:

##### 18. 版本 1.16.00

- **发布日期**: 2022-04-21T11:17:26+02:00
- **发布者**: visso

**变更内容**:

##### 19. 版本 1.17.00

- **发布日期**: 2022-07-07T09:56:30+02:00
- **发布者**: visso

**变更内容**:

##### 20. 版本 4.31.00

- **发布日期**: 2022-09-01T14:16:21+02:00
- **发布者**: visso

**变更内容**:

##### 21. 版本 4.32.00

- **发布日期**: 2022-10-18T16:12:10+02:00
- **发布者**: visso

**变更内容**:

##### 22. 版本 4.33.00

- **发布日期**: 2023-04-05T10:43:07+02:00
- **发布者**: visso

**变更内容**:

##### 23. 版本 4.34.00

- **发布日期**: 2023-05-05T09:59:53+02:00
- **发布者**: visso

**变更内容**:

##### 24. 版本 4.35.00

- **发布日期**: 2023-09-14T17:42:40+02:00
- **发布者**: visso

**变更内容**:

##### 25. 版本 4.36.00

- **发布日期**: 2023-11-09T10:28:49+01:00
- **发布者**: visso

**变更内容**:

##### 26. 版本 4.37.00

- **发布日期**: 2024-03-14T15:55:57+01:00
- **发布者**: visso

**变更内容**:

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. XfrmGeneral

**容器属性**:

- **UUID**: `5630cd57-9196-44e3-a835-337c3163ce62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. XfrmDevErrorDetect

- **UUID**: `a19c462c-80a3-43b2-9685-f143abd2af25`
- **参数名**: `XfrmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. XfrmVersionInfoApi

- **UUID**: `89cce8c8-7cad-4cd5-ac55-3266044db89e`
- **参数名**: `XfrmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Activate/Deactivate the version information API.

######## 3. XfrmSafeBswChecks

- **UUID**: `914a80cc-857d-4cb6-ad3e-205302bb19d5`
- **参数名**: `XfrmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 4. XfrmLegacyStateMachine

- **UUID**: `4bf0212b-aa14-402e-950a-cf8fd10d4b89`
- **参数名**: `XfrmLegacyStateMachine`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If this parameter is set to true, E2E_SMConfigType is generated according to AUTOSAR 4.4 with only a single WindowSize field.
Otherwise, E2E_SMConfigType is generated according to AUTOSAR 22-11 with additional fields
for WindowSizeInit, WindowSizeInvalid, WindowSizeValid, ClearToInvalid and TransitToInvalid.

##### 2. XfrmImplementationMapping

**容器属性**:

- **UUID**: `afeed3e9-e87b-4814-9c74-03e005887db0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmImplementationMapping`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

For each transformer (TransformationTechnology) in a transformer chain (DataTransformation) which is applied to an ISignal it is necessary to specify the BswModuleEntry which implements it. This is the container to hold these mappings.

###### 引用关系

此容器包含 **4** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfrmTransformerBswModuleEntryRef

- **UUID**: `85b77634-5d10-4469-89df-f2d34d386704`
- **引用名**: `XfrmTransformerBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry which implements the referenced transformer on the sending/calling side.

######## 2. XfrmInvTransformerBswModuleEntryRef

- **UUID**: `a9f292f9-079e-4cf1-b2e6-c515fb47c959`
- **引用名**: `XfrmInvTransformerBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: BSW-MODULE-ENTRY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the BswModuleEntry which implements the referenced inverse transformer on the receiving/called side.

######## 3. XfrmTransformationTechnologyRef

- **UUID**: `a6ceae9f-fea6-4a81-9c83-2f3e73e4161d`
- **引用名**: `XfrmTransformationTechnologyRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: TRANSFORMATION-TECHNOLOGY
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the TransformationTechnology in the DataTransformation of the system description for which the implementation (BswModuleEntry) shall be mapped.

####### INSTANCE-REFERENCE 类型引用

######## 1. XfrmVariableDataPrototypeInstanceRef

- **UUID**: `64275e1d-6f49-4af4-a300-6f5c23b69a21`
- **引用名**: `XfrmVariableDataPrototypeInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [0..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Instance Reference to a VariableDataPrototype in case a dedicated transformer BswModuleEntry is required per VariableDataPrototype access.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. XfrmDemEventParameterRefs

**容器属性**:

- **UUID**: `652b2e6f-dbd7-435b-b11b-071dc97550d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. XFRM_E_MALFORMED_MESSAGE

- **UUID**: `8071526f-7385-43a6-ac7b-1a5a7e57c770`
- **引用名**: `XFRM_E_MALFORMED_MESSAGE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to configured DEM event to report if malformed messages were received by the transformer.

####### 2. XfrmSignal

**容器属性**:

- **UUID**: `a1795e1e-66c9-443e-9c07-e1ab80856b25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmSignal`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Reference to the signal in the system description that transports the transformed data.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. XfrmISignalGroupRef

- **UUID**: `7a5ba172-5505-42b9-88d0-952f7c1ef2d3`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

######### 2. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. XfrmISignalRef

- **UUID**: `83ff32da-f185-40dc-a64a-0260ea857de1`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

######### 3. XfrmSignalChoice

**容器属性**:

- **UUID**: `d69f5919-ad89-454e-b640-69fd35c0b035`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

####### 3. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalGroupRef

- **UUID**: `7a5ba172-5505-42b9-88d0-952f7c1ef2d3`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

####### 4. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalRef

- **UUID**: `83ff32da-f185-40dc-a64a-0260ea857de1`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

####### 5. XfrmSignalChoice

**容器属性**:

- **UUID**: `d69f5919-ad89-454e-b640-69fd35c0b035`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

##### 3. XfrmDemEventParameterRefs

**容器属性**:

- **UUID**: `652b2e6f-dbd7-435b-b11b-071dc97550d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. XFRM_E_MALFORMED_MESSAGE

- **UUID**: `8071526f-7385-43a6-ac7b-1a5a7e57c770`
- **引用名**: `XFRM_E_MALFORMED_MESSAGE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to configured DEM event to report if malformed messages were received by the transformer.

##### 4. XfrmSignal

**容器属性**:

- **UUID**: `a1795e1e-66c9-443e-9c07-e1ab80856b25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmSignal`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Reference to the signal in the system description that transports the transformed data.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalGroupRef

- **UUID**: `7a5ba172-5505-42b9-88d0-952f7c1ef2d3`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

####### 2. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. XfrmISignalRef

- **UUID**: `83ff32da-f185-40dc-a64a-0260ea857de1`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

####### 3. XfrmSignalChoice

**容器属性**:

- **UUID**: `d69f5919-ad89-454e-b640-69fd35c0b035`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

##### 5. XfrmISignalGroupRefChoice

**容器属性**:

- **UUID**: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalGroupRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignalGroup in the system description that transports the transformed data.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfrmISignalGroupRef

- **UUID**: `7a5ba172-5505-42b9-88d0-952f7c1ef2d3`
- **引用名**: `XfrmISignalGroupRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-GROUP
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignalGroup in the system description that transports the transformed data.

##### 6. XfrmISignalRefChoice

**容器属性**:

- **UUID**: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `XfrmISignalRefChoice`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Reference to the ISignal in the system description that transports the transformed data.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. XfrmISignalRef

- **UUID**: `83ff32da-f185-40dc-a64a-0260ea857de1`
- **引用名**: `XfrmISignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to the ISignal in the system description that transports the transformed data.

##### 7. XfrmSignalChoice

**容器属性**:

- **UUID**: `d69f5919-ad89-454e-b640-69fd35c0b035`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `XfrmSignalChoice`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **XfrmISignalGroupRefChoice**
  - UUID: `4bc8b0b7-47ff-425e-b81e-2f4b88d1a1d3`
  - 描述: Reference to the ISignalGroup in the system description that transports the transformed data.
- **XfrmISignalRefChoice**
  - UUID: `b904dcfe-b4c4-473b-8464-54f4b628a5b3`
  - 描述: Reference to the ISignal in the system description that transports the transformed data.

**容器描述**:

Choice whether an ISignal or an ISignalGroup shall be referenced.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **E2EXf**

##### BSW-IMPLEMENTATION 类型元素

1. **E2EXf_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **E2EXf_Pre**
2. **E2EXf_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. E2EXf_Impl

- **UUID**: `85387749-83e8-475c-b46f-d6de4e00d726`
- **实现名称**: `E2EXf_Impl`
- **编程语言**: C
- **软件版本**: 4.37.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. E2EXf_Pre

- **UUID**: `50482603-dafe-4772-af56-3cdbec2c6bfa`
- **配置名称**: `E2EXf_Pre`
- **定义引用**: `/MICROSAR/E2EXf`

### 2. E2EXf_Rec

- **UUID**: `839b69c2-1e6d-4b42-8800-0792b155c0db`
- **配置名称**: `E2EXf_Rec`
- **定义引用**: `/MICROSAR/E2EXf`
