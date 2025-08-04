# IdsM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:22

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [IdsM](#idsm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. IdsM

#### 基本信息

- **UUID**: `ECUC:25a5bbf7-d1ec-4aba-b7da-d5c5dec46574`
- **模块名称**: `IdsM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.6.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **19** 个配置容器：

##### 1. IdsMConfiguration

**容器属性**:

- **UUID**: `ECUC:866fcf14-e969-4210-8dd6-4e00b9be3ffe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMConfiguration`
- **多重性**: [1..1]

**容器描述**:

Configuration parameters of the module IdsM.

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. IdsMBlockState

**容器属性**:

- **UUID**: `ECUC:d8265eaa-4f18-4f90-b20f-b338b752043a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockState`
- **多重性**: [0..16]

**容器描述**:

Configuration of an IdsM blocking state used in the IdsMStateBlockFilter to suspend the collection of security events.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMBlockStateID

- **UUID**: `ECUC:e21413a7-209b-4948-9d11-06001721543f`
- **参数名**: `IdsMBlockStateID`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This value specifies the identifier of this block state.

####### 2. IdsMBufferConfiguration

**容器属性**:

- **UUID**: `ECUC:5e1657b1-6115-49e5-8eac-cbd36e0499f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBufferConfiguration`
- **多重性**: [1..1]

**容器描述**:

Configuration of the event buffers and context data buffers used by IdsM.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. IdsMContextDataBuffer

**容器属性**:

- **UUID**: `ECUC:26f7e8e3-1b66-44f6-b421-e6dd5c2b5517`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMContextDataBuffer`
- **多重性**: [0..65535]

**容器描述**:

Buffer that is reserved to store the context data of SEvs.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IdsMContextDataBufferSize

- **UUID**: `ECUC:70e91b48-c638-4d5a-ab88-32282341f28c`
- **参数名**: `IdsMContextDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of the context data buffer in bytes.

############ 2. IdsMNumberOfContextDataBuffers

- **UUID**: `ECUC:85998eee-8ca9-4c00-95fa-64efc873705c`
- **参数名**: `IdsMNumberOfContextDataBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of buffers with the configured buffer size specified in IdsMContextDataBufferSize.

######### 2. IdsMEventBuffers

**容器属性**:

- **UUID**: `ECUC:5848403a-1327-4ac9-89a3-716f3540dffa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventBuffers`
- **多重性**: [1..1]

**容器描述**:

Buffers used to store the SEvs.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IdsMNumberOfEventBuffers

- **UUID**: `ECUC:a9dc8ecd-be3f-427a-a009-32f166a0b887`
- **参数名**: `IdsMNumberOfEventBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of event buffers used to store the SEvs.

####### 3. IdsMContextDataBuffer

**容器属性**:

- **UUID**: `ECUC:26f7e8e3-1b66-44f6-b421-e6dd5c2b5517`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMContextDataBuffer`
- **多重性**: [0..65535]

**容器描述**:

Buffer that is reserved to store the context data of SEvs.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMContextDataBufferSize

- **UUID**: `ECUC:70e91b48-c638-4d5a-ab88-32282341f28c`
- **参数名**: `IdsMContextDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of the context data buffer in bytes.

########## 2. IdsMNumberOfContextDataBuffers

- **UUID**: `ECUC:85998eee-8ca9-4c00-95fa-64efc873705c`
- **参数名**: `IdsMNumberOfContextDataBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of buffers with the configured buffer size specified in IdsMContextDataBufferSize.

####### 4. IdsMEventBuffers

**容器属性**:

- **UUID**: `ECUC:5848403a-1327-4ac9-89a3-716f3540dffa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventBuffers`
- **多重性**: [1..1]

**容器描述**:

Buffers used to store the SEvs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMNumberOfEventBuffers

- **UUID**: `ECUC:a9dc8ecd-be3f-427a-a009-32f166a0b887`
- **参数名**: `IdsMNumberOfEventBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of event buffers used to store the SEvs.

####### 5. IdsMEvent

**容器属性**:

- **UUID**: `ECUC:e70a08c3-32f8-4390-9aa2-866043b9874f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEvent`
- **多重性**: [1..65535]

**容器描述**:

Configuration of the IdsM Event unit which is reported by a sensor and its parameters.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. IdsMExternalEventId

- **UUID**: `ECUC:bd2bad0b-fbba-47fb-ab7a-c737f8deb8d2`
- **参数名**: `IdsMExternalEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The external security event ID which is reported to the sink.

########## 2. IdsMInternalEventId

- **UUID**: `ECUC:732df840-9a52-401f-8413-2fc1760f5926`
- **参数名**: `IdsMInternalEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Consecutive number used internally as an identifier by the IdsM module.

########## 3. IdsMSensorInstanceId

- **UUID**: `ECUC:4a6d6186-7a34-4953-82de-80c34bf0abff`
- **参数名**: `IdsMSensorInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The instance ID of the sensor which reports security events to the IdsM.

######### BOOLEAN 类型参数

########## 1. IdsMSinkDem

- **UUID**: `ECUC:b0a4b1b3-9091-4b22-9964-5115f1a9a83b`
- **参数名**: `IdsMSinkDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The QSEv will be sent to the Dem Module into a Security Event Memory (Sem) to persist it on the local ECU.

########## 2. IdsMSinkIdsR

- **UUID**: `ECUC:ed375659-c559-46ba-9a1c-9b1e7c58f100`
- **参数名**: `IdsMSinkIdsR`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The QSEv will be sent to the IDS Reporter.

######### ENUMERATION 类型参数

########## 1. IdsMReportingModeFilter

- **UUID**: `ECUC:7a72af33-c614-4a15-93e5-4832363cde91`
- **参数名**: `IdsMReportingModeFilter`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BRIEF` (来源: AUTOSAR_ECUC)
  - `BRIEF_BYPASSING_FILTERS` (来源: AUTOSAR_ECUC)
  - `DETAILED` (来源: AUTOSAR_ECUC)
  - `DETAILED_BYPASSING_FILTERS` (来源: AUTOSAR_ECUC)
  - `OFF` (来源: AUTOSAR_ECUC)
- **描述**: The reporting mode filter defines the level of detail of the reporting. Whether SEv should be dropped, forwarded with context data or forwarded without context data.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMFilterChainRef

- **UUID**: `ECUC:897a0dde-a85c-4d79-80fa-1349fb0efdd5`
- **引用名**: `IdsMFilterChainRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `IdsMFilterChain`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMFilterChain`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a configured IdsM filter chain.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IdsMServiceInterfaceOptions

**容器属性**:

- **UUID**: `ECUC:698ec7cc-32aa-4257-8a42-f175b817d741`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMServiceInterfaceOptions`
- **多重性**: [0..1]

**容器描述**:

Adittional configuration parameters of a SEv when the sensor is a SW-C or application.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IdsMEventMaxContextDataSize

- **UUID**: `ECUC:03c40bca-9707-45a3-937d-45086d6ec045`
- **参数名**: `IdsMEventMaxContextDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of bytes used by the IdsM and the RTE when forwarding context data of the corresponding security event.

########### ENUMERATION 类型参数

############ 1. IdsMAdditionalParameterOption

- **UUID**: `ECUC:6abc25c8-28dd-4c49-b992-a8c45184a191`
- **参数名**: `IdsMAdditionalParameterOption`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Count` (来源: AUTOSAR_ECUC)
  - `CountTimestamp` (来源: AUTOSAR_ECUC)
  - `None` (来源: AUTOSAR_ECUC)
- **描述**: In addition to the optional context data the Service Port Interface can be extended by the following parameters:

####### 6. IdsMServiceInterfaceOptions

**容器属性**:

- **UUID**: `ECUC:698ec7cc-32aa-4257-8a42-f175b817d741`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMServiceInterfaceOptions`
- **多重性**: [0..1]

**容器描述**:

Adittional configuration parameters of a SEv when the sensor is a SW-C or application.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMEventMaxContextDataSize

- **UUID**: `ECUC:03c40bca-9707-45a3-937d-45086d6ec045`
- **参数名**: `IdsMEventMaxContextDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of bytes used by the IdsM and the RTE when forwarding context data of the corresponding security event.

######### ENUMERATION 类型参数

########## 1. IdsMAdditionalParameterOption

- **UUID**: `ECUC:6abc25c8-28dd-4c49-b992-a8c45184a191`
- **参数名**: `IdsMAdditionalParameterOption`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Count` (来源: AUTOSAR_ECUC)
  - `CountTimestamp` (来源: AUTOSAR_ECUC)
  - `None` (来源: AUTOSAR_ECUC)
- **描述**: In addition to the optional context data the Service Port Interface can be extended by the following parameters:

####### 7. IdsMFilterChain

**容器属性**:

- **UUID**: `ECUC:2221f5d5-f14a-4c6b-940f-e5b6aa0b485f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterChain`
- **多重性**: [0..infinite]

**容器描述**:

A filter chain is a combination of filters that affects one or more SEvs.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. IdsMBlockStateFilter

**容器属性**:

- **UUID**: `ECUC:0c2ac614-a899-4621-acae-95b263a60603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockStateFilter`
- **多重性**: [0..1]

**容器描述**:

This state filter drops SEvs if the current State reported by the BswM is in this state filter list.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IdsMBlockStateReference

- **UUID**: `ECUC:38f6a73e-bd6c-4328-9714-eca2d3605693`
- **引用名**: `IdsMBlockStateReference`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `IdsMBlockState`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMBlockState`
- **来源**: AUTOSAR_ECUC
- **描述**: The collection of SEvs during this state will be suspended.

######### 2. IdsMEventAggregationFilter

**容器属性**:

- **UUID**: `ECUC:efa00707-d51b-4c23-93e9-b253cae6cfaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventAggregationFilter`
- **多重性**: [0..1]

**容器描述**:

All received events of a certain event ID that are received by this filter during a single aggregation time interval are not forwarded immediately.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. IdsMEventAggregationTimeInterval

- **UUID**: `ECUC:694d9eb9-a207-496c-8730-01e537a83376`
- **参数名**: `IdsMEventAggregationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the aggregation time interval (as float in seconds).

########### ENUMERATION 类型参数

############ 1. IdsMContextDataSourceSelector

- **UUID**: `ECUC:b6e61cfd-ad89-4fa3-9189-56ae66943fb0`
- **参数名**: `IdsMContextDataSourceSelector`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IDSM_FILTERS_CTX_USE_FIRST` (来源: AUTOSAR_ECUC)
  - `IDSM_FILTERS_CTX_USE_LAST` (来源: AUTOSAR_ECUC)
- **描述**: The resulting SEv from the aggregation filter contains the context data from one of the following two sources:

######### 3. IdsMEventThresholdFilter

**容器属性**:

- **UUID**: `ECUC:b61de7e1-fba1-44cd-ba1e-c9c791406ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventThresholdFilter`
- **多重性**: [0..1]

**容器描述**:

During each time interval "IdsMEventThresholdTimeInterval", the filter drops the first "IdsMEventThresholdNumber - 1" SEvs and forwards all other incoming SEvs immediately until the end of the time interval.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IdsMEventThresholdNumber

- **UUID**: `ECUC:0475d6ea-a834-4b40-aad0-e0b46a682b55`
- **参数名**: `IdsMEventThresholdNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter assigns the threshold 'p' for each SEv ID affected by this threshold filter.

########### FLOAT 类型参数

############ 1. IdsMEventThresholdTimeInterval

- **UUID**: `ECUC:ad16168c-46c7-4522-a792-baedb09c35bf`
- **参数名**: `IdsMEventThresholdTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the threshold time interval (as float in seconds).

######### 4. IdsMForwardEveryNthFilter

**容器属性**:

- **UUID**: `ECUC:695c19c9-276c-45a0-9ba2-d3d6d4ed8c9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMForwardEveryNthFilter`
- **多重性**: [0..1]

**容器描述**:

Out of all incoming SEVs, drop all but every nth. Those will be forwarded without modification.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IdsMNthParameter

- **UUID**: `ECUC:ee62536b-c70a-4ddb-8912-13bb53fafb20`
- **参数名**: `IdsMNthParameter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: For each SEv ID for which this filter is configured, this parameter assigns the appropriate n.

####### 8. IdsMBlockStateFilter

**容器属性**:

- **UUID**: `ECUC:0c2ac614-a899-4621-acae-95b263a60603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockStateFilter`
- **多重性**: [0..1]

**容器描述**:

This state filter drops SEvs if the current State reported by the BswM is in this state filter list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMBlockStateReference

- **UUID**: `ECUC:38f6a73e-bd6c-4328-9714-eca2d3605693`
- **引用名**: `IdsMBlockStateReference`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `IdsMBlockState`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMBlockState`
- **来源**: AUTOSAR_ECUC
- **描述**: The collection of SEvs during this state will be suspended.

####### 9. IdsMEventAggregationFilter

**容器属性**:

- **UUID**: `ECUC:efa00707-d51b-4c23-93e9-b253cae6cfaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventAggregationFilter`
- **多重性**: [0..1]

**容器描述**:

All received events of a certain event ID that are received by this filter during a single aggregation time interval are not forwarded immediately.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. IdsMEventAggregationTimeInterval

- **UUID**: `ECUC:694d9eb9-a207-496c-8730-01e537a83376`
- **参数名**: `IdsMEventAggregationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the aggregation time interval (as float in seconds).

######### ENUMERATION 类型参数

########## 1. IdsMContextDataSourceSelector

- **UUID**: `ECUC:b6e61cfd-ad89-4fa3-9189-56ae66943fb0`
- **参数名**: `IdsMContextDataSourceSelector`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IDSM_FILTERS_CTX_USE_FIRST` (来源: AUTOSAR_ECUC)
  - `IDSM_FILTERS_CTX_USE_LAST` (来源: AUTOSAR_ECUC)
- **描述**: The resulting SEv from the aggregation filter contains the context data from one of the following two sources:

####### 10. IdsMEventThresholdFilter

**容器属性**:

- **UUID**: `ECUC:b61de7e1-fba1-44cd-ba1e-c9c791406ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventThresholdFilter`
- **多重性**: [0..1]

**容器描述**:

During each time interval "IdsMEventThresholdTimeInterval", the filter drops the first "IdsMEventThresholdNumber - 1" SEvs and forwards all other incoming SEvs immediately until the end of the time interval.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMEventThresholdNumber

- **UUID**: `ECUC:0475d6ea-a834-4b40-aad0-e0b46a682b55`
- **参数名**: `IdsMEventThresholdNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter assigns the threshold 'p' for each SEv ID affected by this threshold filter.

######### FLOAT 类型参数

########## 1. IdsMEventThresholdTimeInterval

- **UUID**: `ECUC:ad16168c-46c7-4522-a792-baedb09c35bf`
- **参数名**: `IdsMEventThresholdTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the threshold time interval (as float in seconds).

####### 11. IdsMForwardEveryNthFilter

**容器属性**:

- **UUID**: `ECUC:695c19c9-276c-45a0-9ba2-d3d6d4ed8c9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMForwardEveryNthFilter`
- **多重性**: [0..1]

**容器描述**:

Out of all incoming SEVs, drop all but every nth. Those will be forwarded without modification.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMNthParameter

- **UUID**: `ECUC:ee62536b-c70a-4ddb-8912-13bb53fafb20`
- **参数名**: `IdsMNthParameter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: For each SEv ID for which this filter is configured, this parameter assigns the appropriate n.

####### 12. IdsMPdus

**容器属性**:

- **UUID**: `ECUC:a3e37ae3-41a1-46ad-a68c-cd998eec577a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMPdus`
- **多重性**: [0..1]

**容器描述**:

Configuration of the PDU references used to send the events data.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. IdsMIfTxPdu

**容器属性**:

- **UUID**: `ECUC:960e8aa4-56f7-4c8f-9a50-bb8abfc985d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMIfTxPdu`
- **多重性**: [0..1]

**容器描述**:

IF PDU used to transmit a QSEv via the PduR to the IdsR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IdsMIfTxPduHandleId

- **UUID**: `ECUC:12a355b1-04d0-45d2-8dd9-082abaa0d620`
- **参数名**: `IdsMIfTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IdsMIfTxPduRef

- **UUID**: `ECUC:27db4f61-ca7b-4384-8462-978ac7e2492c`
- **引用名**: `IdsMIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the IF PDU used for transmission of the QSEvs.

######### 2. IdsMTpTxPdu

**容器属性**:

- **UUID**: `ECUC:df65cd55-d05d-4f34-a277-11289bd8b1ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMTpTxPdu`
- **多重性**: [0..1]

**容器描述**:

TP PDU used to transmit a QSEv via the PduR to the IdsR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IdsMTpTxPduHandleId

- **UUID**: `ECUC:b4bfc732-56e7-458e-8523-c54aa0f58f95`
- **参数名**: `IdsMTpTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IdsMTpTxPduRef

- **UUID**: `ECUC:94ee1d70-7a96-4278-ae8c-df0e4a4f760b`
- **引用名**: `IdsMTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the TP PDU used for transmission of the QSEvs.

####### 13. IdsMIfTxPdu

**容器属性**:

- **UUID**: `ECUC:960e8aa4-56f7-4c8f-9a50-bb8abfc985d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMIfTxPdu`
- **多重性**: [0..1]

**容器描述**:

IF PDU used to transmit a QSEv via the PduR to the IdsR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMIfTxPduHandleId

- **UUID**: `ECUC:12a355b1-04d0-45d2-8dd9-082abaa0d620`
- **参数名**: `IdsMIfTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMIfTxPduRef

- **UUID**: `ECUC:27db4f61-ca7b-4384-8462-978ac7e2492c`
- **引用名**: `IdsMIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the IF PDU used for transmission of the QSEvs.

####### 14. IdsMTpTxPdu

**容器属性**:

- **UUID**: `ECUC:df65cd55-d05d-4f34-a277-11289bd8b1ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMTpTxPdu`
- **多重性**: [0..1]

**容器描述**:

TP PDU used to transmit a QSEv via the PduR to the IdsR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMTpTxPduHandleId

- **UUID**: `ECUC:b4bfc732-56e7-458e-8523-c54aa0f58f95`
- **参数名**: `IdsMTpTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMTpTxPduRef

- **UUID**: `ECUC:94ee1d70-7a96-4278-ae8c-df0e4a4f760b`
- **引用名**: `IdsMTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the TP PDU used for transmission of the QSEvs.

##### 2. IdsMBlockState

**容器属性**:

- **UUID**: `ECUC:d8265eaa-4f18-4f90-b20f-b338b752043a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockState`
- **多重性**: [0..16]

**容器描述**:

Configuration of an IdsM blocking state used in the IdsMStateBlockFilter to suspend the collection of security events.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IdsMBlockStateID

- **UUID**: `ECUC:e21413a7-209b-4948-9d11-06001721543f`
- **参数名**: `IdsMBlockStateID`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This value specifies the identifier of this block state.

##### 3. IdsMBufferConfiguration

**容器属性**:

- **UUID**: `ECUC:5e1657b1-6115-49e5-8eac-cbd36e0499f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBufferConfiguration`
- **多重性**: [1..1]

**容器描述**:

Configuration of the event buffers and context data buffers used by IdsM.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. IdsMContextDataBuffer

**容器属性**:

- **UUID**: `ECUC:26f7e8e3-1b66-44f6-b421-e6dd5c2b5517`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMContextDataBuffer`
- **多重性**: [0..65535]

**容器描述**:

Buffer that is reserved to store the context data of SEvs.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMContextDataBufferSize

- **UUID**: `ECUC:70e91b48-c638-4d5a-ab88-32282341f28c`
- **参数名**: `IdsMContextDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of the context data buffer in bytes.

########## 2. IdsMNumberOfContextDataBuffers

- **UUID**: `ECUC:85998eee-8ca9-4c00-95fa-64efc873705c`
- **参数名**: `IdsMNumberOfContextDataBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of buffers with the configured buffer size specified in IdsMContextDataBufferSize.

####### 2. IdsMEventBuffers

**容器属性**:

- **UUID**: `ECUC:5848403a-1327-4ac9-89a3-716f3540dffa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventBuffers`
- **多重性**: [1..1]

**容器描述**:

Buffers used to store the SEvs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMNumberOfEventBuffers

- **UUID**: `ECUC:a9dc8ecd-be3f-427a-a009-32f166a0b887`
- **参数名**: `IdsMNumberOfEventBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of event buffers used to store the SEvs.

##### 4. IdsMContextDataBuffer

**容器属性**:

- **UUID**: `ECUC:26f7e8e3-1b66-44f6-b421-e6dd5c2b5517`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMContextDataBuffer`
- **多重性**: [0..65535]

**容器描述**:

Buffer that is reserved to store the context data of SEvs.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IdsMContextDataBufferSize

- **UUID**: `ECUC:70e91b48-c638-4d5a-ab88-32282341f28c`
- **参数名**: `IdsMContextDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of the context data buffer in bytes.

######## 2. IdsMNumberOfContextDataBuffers

- **UUID**: `ECUC:85998eee-8ca9-4c00-95fa-64efc873705c`
- **参数名**: `IdsMNumberOfContextDataBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of buffers with the configured buffer size specified in IdsMContextDataBufferSize.

##### 5. IdsMEventBuffers

**容器属性**:

- **UUID**: `ECUC:5848403a-1327-4ac9-89a3-716f3540dffa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventBuffers`
- **多重性**: [1..1]

**容器描述**:

Buffers used to store the SEvs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IdsMNumberOfEventBuffers

- **UUID**: `ECUC:a9dc8ecd-be3f-427a-a009-32f166a0b887`
- **参数名**: `IdsMNumberOfEventBuffers`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The number of event buffers used to store the SEvs.

##### 6. IdsMEvent

**容器属性**:

- **UUID**: `ECUC:e70a08c3-32f8-4390-9aa2-866043b9874f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEvent`
- **多重性**: [1..65535]

**容器描述**:

Configuration of the IdsM Event unit which is reported by a sensor and its parameters.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. IdsMExternalEventId

- **UUID**: `ECUC:bd2bad0b-fbba-47fb-ab7a-c737f8deb8d2`
- **参数名**: `IdsMExternalEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The external security event ID which is reported to the sink.

######## 2. IdsMInternalEventId

- **UUID**: `ECUC:732df840-9a52-401f-8413-2fc1760f5926`
- **参数名**: `IdsMInternalEventId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65535`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Consecutive number used internally as an identifier by the IdsM module.

######## 3. IdsMSensorInstanceId

- **UUID**: `ECUC:4a6d6186-7a34-4953-82de-80c34bf0abff`
- **参数名**: `IdsMSensorInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The instance ID of the sensor which reports security events to the IdsM.

####### BOOLEAN 类型参数

######## 1. IdsMSinkDem

- **UUID**: `ECUC:b0a4b1b3-9091-4b22-9964-5115f1a9a83b`
- **参数名**: `IdsMSinkDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The QSEv will be sent to the Dem Module into a Security Event Memory (Sem) to persist it on the local ECU.

######## 2. IdsMSinkIdsR

- **UUID**: `ECUC:ed375659-c559-46ba-9a1c-9b1e7c58f100`
- **参数名**: `IdsMSinkIdsR`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The QSEv will be sent to the IDS Reporter.

####### ENUMERATION 类型参数

######## 1. IdsMReportingModeFilter

- **UUID**: `ECUC:7a72af33-c614-4a15-93e5-4832363cde91`
- **参数名**: `IdsMReportingModeFilter`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BRIEF` (来源: AUTOSAR_ECUC)
  - `BRIEF_BYPASSING_FILTERS` (来源: AUTOSAR_ECUC)
  - `DETAILED` (来源: AUTOSAR_ECUC)
  - `DETAILED_BYPASSING_FILTERS` (来源: AUTOSAR_ECUC)
  - `OFF` (来源: AUTOSAR_ECUC)
- **描述**: The reporting mode filter defines the level of detail of the reporting. Whether SEv should be dropped, forwarded with context data or forwarded without context data.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IdsMFilterChainRef

- **UUID**: `ECUC:897a0dde-a85c-4d79-80fa-1349fb0efdd5`
- **引用名**: `IdsMFilterChainRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `IdsMFilterChain`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMFilterChain`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a configured IdsM filter chain.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IdsMServiceInterfaceOptions

**容器属性**:

- **UUID**: `ECUC:698ec7cc-32aa-4257-8a42-f175b817d741`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMServiceInterfaceOptions`
- **多重性**: [0..1]

**容器描述**:

Adittional configuration parameters of a SEv when the sensor is a SW-C or application.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMEventMaxContextDataSize

- **UUID**: `ECUC:03c40bca-9707-45a3-937d-45086d6ec045`
- **参数名**: `IdsMEventMaxContextDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of bytes used by the IdsM and the RTE when forwarding context data of the corresponding security event.

######### ENUMERATION 类型参数

########## 1. IdsMAdditionalParameterOption

- **UUID**: `ECUC:6abc25c8-28dd-4c49-b992-a8c45184a191`
- **参数名**: `IdsMAdditionalParameterOption`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Count` (来源: AUTOSAR_ECUC)
  - `CountTimestamp` (来源: AUTOSAR_ECUC)
  - `None` (来源: AUTOSAR_ECUC)
- **描述**: In addition to the optional context data the Service Port Interface can be extended by the following parameters:

##### 7. IdsMServiceInterfaceOptions

**容器属性**:

- **UUID**: `ECUC:698ec7cc-32aa-4257-8a42-f175b817d741`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMServiceInterfaceOptions`
- **多重性**: [0..1]

**容器描述**:

Adittional configuration parameters of a SEv when the sensor is a SW-C or application.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IdsMEventMaxContextDataSize

- **UUID**: `ECUC:03c40bca-9707-45a3-937d-45086d6ec045`
- **参数名**: `IdsMEventMaxContextDataSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1500]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of bytes used by the IdsM and the RTE when forwarding context data of the corresponding security event.

####### ENUMERATION 类型参数

######## 1. IdsMAdditionalParameterOption

- **UUID**: `ECUC:6abc25c8-28dd-4c49-b992-a8c45184a191`
- **参数名**: `IdsMAdditionalParameterOption`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Count` (来源: AUTOSAR_ECUC)
  - `CountTimestamp` (来源: AUTOSAR_ECUC)
  - `None` (来源: AUTOSAR_ECUC)
- **描述**: In addition to the optional context data the Service Port Interface can be extended by the following parameters:

##### 8. IdsMFilterChain

**容器属性**:

- **UUID**: `ECUC:2221f5d5-f14a-4c6b-940f-e5b6aa0b485f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterChain`
- **多重性**: [0..infinite]

**容器描述**:

A filter chain is a combination of filters that affects one or more SEvs.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. IdsMBlockStateFilter

**容器属性**:

- **UUID**: `ECUC:0c2ac614-a899-4621-acae-95b263a60603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockStateFilter`
- **多重性**: [0..1]

**容器描述**:

This state filter drops SEvs if the current State reported by the BswM is in this state filter list.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMBlockStateReference

- **UUID**: `ECUC:38f6a73e-bd6c-4328-9714-eca2d3605693`
- **引用名**: `IdsMBlockStateReference`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `IdsMBlockState`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMBlockState`
- **来源**: AUTOSAR_ECUC
- **描述**: The collection of SEvs during this state will be suspended.

####### 2. IdsMEventAggregationFilter

**容器属性**:

- **UUID**: `ECUC:efa00707-d51b-4c23-93e9-b253cae6cfaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventAggregationFilter`
- **多重性**: [0..1]

**容器描述**:

All received events of a certain event ID that are received by this filter during a single aggregation time interval are not forwarded immediately.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. IdsMEventAggregationTimeInterval

- **UUID**: `ECUC:694d9eb9-a207-496c-8730-01e537a83376`
- **参数名**: `IdsMEventAggregationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the aggregation time interval (as float in seconds).

######### ENUMERATION 类型参数

########## 1. IdsMContextDataSourceSelector

- **UUID**: `ECUC:b6e61cfd-ad89-4fa3-9189-56ae66943fb0`
- **参数名**: `IdsMContextDataSourceSelector`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IDSM_FILTERS_CTX_USE_FIRST` (来源: AUTOSAR_ECUC)
  - `IDSM_FILTERS_CTX_USE_LAST` (来源: AUTOSAR_ECUC)
- **描述**: The resulting SEv from the aggregation filter contains the context data from one of the following two sources:

####### 3. IdsMEventThresholdFilter

**容器属性**:

- **UUID**: `ECUC:b61de7e1-fba1-44cd-ba1e-c9c791406ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventThresholdFilter`
- **多重性**: [0..1]

**容器描述**:

During each time interval "IdsMEventThresholdTimeInterval", the filter drops the first "IdsMEventThresholdNumber - 1" SEvs and forwards all other incoming SEvs immediately until the end of the time interval.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMEventThresholdNumber

- **UUID**: `ECUC:0475d6ea-a834-4b40-aad0-e0b46a682b55`
- **参数名**: `IdsMEventThresholdNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter assigns the threshold 'p' for each SEv ID affected by this threshold filter.

######### FLOAT 类型参数

########## 1. IdsMEventThresholdTimeInterval

- **UUID**: `ECUC:ad16168c-46c7-4522-a792-baedb09c35bf`
- **参数名**: `IdsMEventThresholdTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the threshold time interval (as float in seconds).

####### 4. IdsMForwardEveryNthFilter

**容器属性**:

- **UUID**: `ECUC:695c19c9-276c-45a0-9ba2-d3d6d4ed8c9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMForwardEveryNthFilter`
- **多重性**: [0..1]

**容器描述**:

Out of all incoming SEVs, drop all but every nth. Those will be forwarded without modification.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMNthParameter

- **UUID**: `ECUC:ee62536b-c70a-4ddb-8912-13bb53fafb20`
- **参数名**: `IdsMNthParameter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: For each SEv ID for which this filter is configured, this parameter assigns the appropriate n.

##### 9. IdsMBlockStateFilter

**容器属性**:

- **UUID**: `ECUC:0c2ac614-a899-4621-acae-95b263a60603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMBlockStateFilter`
- **多重性**: [0..1]

**容器描述**:

This state filter drops SEvs if the current State reported by the BswM is in this state filter list.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IdsMBlockStateReference

- **UUID**: `ECUC:38f6a73e-bd6c-4328-9714-eca2d3605693`
- **引用名**: `IdsMBlockStateReference`
- **引用类型**: REFERENCE
- **多重性**: [1..16]
- **目标**: `IdsMBlockState`
- **完整路径**: `/AUTOSAR/EcucDefs/IdsM/IdsMConfiguration/IdsMBlockState`
- **来源**: AUTOSAR_ECUC
- **描述**: The collection of SEvs during this state will be suspended.

##### 10. IdsMEventAggregationFilter

**容器属性**:

- **UUID**: `ECUC:efa00707-d51b-4c23-93e9-b253cae6cfaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventAggregationFilter`
- **多重性**: [0..1]

**容器描述**:

All received events of a certain event ID that are received by this filter during a single aggregation time interval are not forwarded immediately.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. IdsMEventAggregationTimeInterval

- **UUID**: `ECUC:694d9eb9-a207-496c-8730-01e537a83376`
- **参数名**: `IdsMEventAggregationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the aggregation time interval (as float in seconds).

####### ENUMERATION 类型参数

######## 1. IdsMContextDataSourceSelector

- **UUID**: `ECUC:b6e61cfd-ad89-4fa3-9189-56ae66943fb0`
- **参数名**: `IdsMContextDataSourceSelector`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IDSM_FILTERS_CTX_USE_FIRST` (来源: AUTOSAR_ECUC)
  - `IDSM_FILTERS_CTX_USE_LAST` (来源: AUTOSAR_ECUC)
- **描述**: The resulting SEv from the aggregation filter contains the context data from one of the following two sources:

##### 11. IdsMEventThresholdFilter

**容器属性**:

- **UUID**: `ECUC:b61de7e1-fba1-44cd-ba1e-c9c791406ef6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMEventThresholdFilter`
- **多重性**: [0..1]

**容器描述**:

During each time interval "IdsMEventThresholdTimeInterval", the filter drops the first "IdsMEventThresholdNumber - 1" SEvs and forwards all other incoming SEvs immediately until the end of the time interval.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IdsMEventThresholdNumber

- **UUID**: `ECUC:0475d6ea-a834-4b40-aad0-e0b46a682b55`
- **参数名**: `IdsMEventThresholdNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter assigns the threshold 'p' for each SEv ID affected by this threshold filter.

####### FLOAT 类型参数

######## 1. IdsMEventThresholdTimeInterval

- **UUID**: `ECUC:ad16168c-46c7-4522-a792-baedb09c35bf`
- **参数名**: `IdsMEventThresholdTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the threshold time interval (as float in seconds).

##### 12. IdsMForwardEveryNthFilter

**容器属性**:

- **UUID**: `ECUC:695c19c9-276c-45a0-9ba2-d3d6d4ed8c9d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMForwardEveryNthFilter`
- **多重性**: [0..1]

**容器描述**:

Out of all incoming SEVs, drop all but every nth. Those will be forwarded without modification.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IdsMNthParameter

- **UUID**: `ECUC:ee62536b-c70a-4ddb-8912-13bb53fafb20`
- **参数名**: `IdsMNthParameter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: For each SEv ID for which this filter is configured, this parameter assigns the appropriate n.

##### 13. IdsMPdus

**容器属性**:

- **UUID**: `ECUC:a3e37ae3-41a1-46ad-a68c-cd998eec577a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMPdus`
- **多重性**: [0..1]

**容器描述**:

Configuration of the PDU references used to send the events data.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. IdsMIfTxPdu

**容器属性**:

- **UUID**: `ECUC:960e8aa4-56f7-4c8f-9a50-bb8abfc985d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMIfTxPdu`
- **多重性**: [0..1]

**容器描述**:

IF PDU used to transmit a QSEv via the PduR to the IdsR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMIfTxPduHandleId

- **UUID**: `ECUC:12a355b1-04d0-45d2-8dd9-082abaa0d620`
- **参数名**: `IdsMIfTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMIfTxPduRef

- **UUID**: `ECUC:27db4f61-ca7b-4384-8462-978ac7e2492c`
- **引用名**: `IdsMIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the IF PDU used for transmission of the QSEvs.

####### 2. IdsMTpTxPdu

**容器属性**:

- **UUID**: `ECUC:df65cd55-d05d-4f34-a277-11289bd8b1ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMTpTxPdu`
- **多重性**: [0..1]

**容器描述**:

TP PDU used to transmit a QSEv via the PduR to the IdsR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IdsMTpTxPduHandleId

- **UUID**: `ECUC:b4bfc732-56e7-458e-8523-c54aa0f58f95`
- **参数名**: `IdsMTpTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IdsMTpTxPduRef

- **UUID**: `ECUC:94ee1d70-7a96-4278-ae8c-df0e4a4f760b`
- **引用名**: `IdsMTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the TP PDU used for transmission of the QSEvs.

##### 14. IdsMIfTxPdu

**容器属性**:

- **UUID**: `ECUC:960e8aa4-56f7-4c8f-9a50-bb8abfc985d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMIfTxPdu`
- **多重性**: [0..1]

**容器描述**:

IF PDU used to transmit a QSEv via the PduR to the IdsR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IdsMIfTxPduHandleId

- **UUID**: `ECUC:12a355b1-04d0-45d2-8dd9-082abaa0d620`
- **参数名**: `IdsMIfTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IdsMIfTxPduRef

- **UUID**: `ECUC:27db4f61-ca7b-4384-8462-978ac7e2492c`
- **引用名**: `IdsMIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the IF PDU used for transmission of the QSEvs.

##### 15. IdsMTpTxPdu

**容器属性**:

- **UUID**: `ECUC:df65cd55-d05d-4f34-a277-11289bd8b1ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMTpTxPdu`
- **多重性**: [0..1]

**容器描述**:

TP PDU used to transmit a QSEv via the PduR to the IdsR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IdsMTpTxPduHandleId

- **UUID**: `ECUC:b4bfc732-56e7-458e-8523-c54aa0f58f95`
- **参数名**: `IdsMTpTxPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IdsM does not use this parameter, content will be ignored.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IdsMTpTxPduRef

- **UUID**: `ECUC:94ee1d70-7a96-4278-ae8c-df0e4a4f760b`
- **引用名**: `IdsMTpTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the TP PDU used for transmission of the QSEvs.

##### 16. IdsMGeneral

**容器属性**:

- **UUID**: `ECUC:bfeec448-1b5e-4e6f-9475-20a6e1c23683`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMGeneral`
- **多重性**: [1..1]

**容器描述**:

General configuration parameters of IdsM.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. IdsMInstanceId

- **UUID**: `ECUC:25eff5b0-8330-409d-b80d-ce8228f1a451`
- **参数名**: `IdsMInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The unique identifier of the sending IdsM instance.

######## 2. IdsMSignatureGenerateResultLength

- **UUID**: `ECUC:2b99434a-cbc1-4d50-a34c-71f3d77635bd`
- **参数名**: `IdsMSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the length in bytes of the signature calculated by the crypto services. This parameter should be set when the IdsMSignatureSupport is enabled.

####### BOOLEAN 类型参数

######## 1. IdsMDevErrorDetect

- **UUID**: `ECUC:761c90cd-be79-4b6f-a8ac-f36a9d62bb80`
- **参数名**: `IdsMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables/disables the Development Error Detection and Notification.

######## 2. IdsMDiagnosticSupport

- **UUID**: `ECUC:d2edbf39-71cd-4a8d-8aa2-5c8bd554743b`
- **参数名**: `IdsMDiagnosticSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables or disables the Dcm APIs which are used to read and write certain values of the IdsM module through the diagnostic communication manager.

######## 3. IdsMSignatureSupport

- **UUID**: `ECUC:7397a9e2-93b3-4d64-85e5-26505789f41e`
- **参数名**: `IdsMSignatureSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables/disables the functionality of sending messages to the network with a signature of encryption calculated by the crypto services.

######## 4. IdsMVersionInfoApi

- **UUID**: `ECUC:b2aca049-0322-403f-90b9-48cd735886b3`
- **参数名**: `IdsMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables/disables the function IdsM_GetVersionInfo() to get major, minor and patch version information of the module.

####### FLOAT 类型参数

######## 1. IdsMMainFunctionPeriod

- **UUID**: `ECUC:4d87e6e9-3494-4df2-9b3c-7a69466b342a`
- **参数名**: `IdsMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The period between successive calls to the IdsM main function (as float in seconds).

####### ENUMERATION 类型参数

######## 1. IdsMTimestampOption

- **UUID**: `ECUC:2cb9ea29-1f8d-4957-b0a5-e553d70451df`
- **参数名**: `IdsMTimestampOption`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `AUTOSAR` (来源: AUTOSAR_ECUC)
  - `Custom` (来源: AUTOSAR_ECUC)
  - `None` (来源: AUTOSAR_ECUC)
- **描述**: This parameter enables/disables the functionality of having a timestamp field as part of a QSEv and if the origin of the timestamp is from the AUTOSAR stack or from the application (custom timestamp).

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. IdsMCsmJobReference

- **UUID**: `ECUC:89c7127a-746f-466a-912f-5b4235c39644`
- **引用名**: `IdsMCsmJobReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references the Csm job that is used to generate signatures when qualified security events must be signed.

######## 2. IdsMNvmBlockDescriptor

- **UUID**: `ECUC:33ed89b2-644b-43ef-95fe-ba0164884167`
- **引用名**: `IdsMNvmBlockDescriptor`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **描述**: Choose a NvM block descriptor reference, that is used to load and store the non-volatile data of IdsM module.

######## 3. IdsMStbMSynchronizedTimeBaseReference

- **UUID**: `ECUC:9b607fed-864a-40f8-b9be-0efd8576a4de`
- **引用名**: `IdsMStbMSynchronizedTimeBaseReference`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references the time source when the origin of the timestamp is AUTOSAR.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. IdsMGlobalRateLimitationFilters

**容器属性**:

- **UUID**: `ECUC:3b9b4e6d-a5b1-48e7-93b4-5975e20c0526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMGlobalRateLimitationFilters`
- **多重性**: [0..1]

**容器描述**:

Global rate limitation filters for all SEvs.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. IdsMFilterEventRateLimitation

**容器属性**:

- **UUID**: `ECUC:3f150bd6-bc83-4fda-97cf-ee53a38e90b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterEventRateLimitation`
- **多重性**: [0..1]

**容器描述**:

For configurable time intervals of length "IdsMRateLimitationTimeInterval" this filter forwards all the SEvs until reaching the limit "IdsMRateLimitationMaximumEvents".

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IdsMRateLimitationMaximumEvents

- **UUID**: `ECUC:f63c79d5-290e-4e49-9aeb-89bc12111b9a`
- **参数名**: `IdsMRateLimitationMaximumEvents`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of SEvs which are passed on by this filter in a single rate limitation time interval.

########### FLOAT 类型参数

############ 1. IdsMRateLimitationTimeInterval

- **UUID**: `ECUC:7f83aa6e-4e22-4820-a780-b10725c4d5b9`
- **参数名**: `IdsMRateLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time interval length of the event rate limitation filter (as float in seconds).

######### 2. IdsMFilterTrafficLimitation

**容器属性**:

- **UUID**: `ECUC:4ab683fb-cd78-466a-a2a4-66436cf106be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterTrafficLimitation`
- **多重性**: [0..1]

**容器描述**:

The traffic limitation filter forwards all the incoming SEvs until reaching the limit "IdsMTrafficLimitationMaximumBytes".

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IdsMTrafficLimitationMaximumBytes

- **UUID**: `ECUC:e1a4273f-4445-4289-8d7c-32d33421a2da`
- **参数名**: `IdsMTrafficLimitationMaximumBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to be sent out by the IdsM in a single traffic limitation time interval.

########### FLOAT 类型参数

############ 1. IdsMTrafficLimitationTimeInterval

- **UUID**: `ECUC:57f260e9-2178-4dcf-ae42-2871d4045391`
- **参数名**: `IdsMTrafficLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the traffic limitation time interval (as float in seconds).

####### 2. IdsMFilterEventRateLimitation

**容器属性**:

- **UUID**: `ECUC:3f150bd6-bc83-4fda-97cf-ee53a38e90b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterEventRateLimitation`
- **多重性**: [0..1]

**容器描述**:

For configurable time intervals of length "IdsMRateLimitationTimeInterval" this filter forwards all the SEvs until reaching the limit "IdsMRateLimitationMaximumEvents".

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMRateLimitationMaximumEvents

- **UUID**: `ECUC:f63c79d5-290e-4e49-9aeb-89bc12111b9a`
- **参数名**: `IdsMRateLimitationMaximumEvents`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of SEvs which are passed on by this filter in a single rate limitation time interval.

######### FLOAT 类型参数

########## 1. IdsMRateLimitationTimeInterval

- **UUID**: `ECUC:7f83aa6e-4e22-4820-a780-b10725c4d5b9`
- **参数名**: `IdsMRateLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time interval length of the event rate limitation filter (as float in seconds).

####### 3. IdsMFilterTrafficLimitation

**容器属性**:

- **UUID**: `ECUC:4ab683fb-cd78-466a-a2a4-66436cf106be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterTrafficLimitation`
- **多重性**: [0..1]

**容器描述**:

The traffic limitation filter forwards all the incoming SEvs until reaching the limit "IdsMTrafficLimitationMaximumBytes".

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMTrafficLimitationMaximumBytes

- **UUID**: `ECUC:e1a4273f-4445-4289-8d7c-32d33421a2da`
- **参数名**: `IdsMTrafficLimitationMaximumBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to be sent out by the IdsM in a single traffic limitation time interval.

######### FLOAT 类型参数

########## 1. IdsMTrafficLimitationTimeInterval

- **UUID**: `ECUC:57f260e9-2178-4dcf-ae42-2871d4045391`
- **参数名**: `IdsMTrafficLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the traffic limitation time interval (as float in seconds).

##### 17. IdsMGlobalRateLimitationFilters

**容器属性**:

- **UUID**: `ECUC:3b9b4e6d-a5b1-48e7-93b4-5975e20c0526`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMGlobalRateLimitationFilters`
- **多重性**: [0..1]

**容器描述**:

Global rate limitation filters for all SEvs.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. IdsMFilterEventRateLimitation

**容器属性**:

- **UUID**: `ECUC:3f150bd6-bc83-4fda-97cf-ee53a38e90b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterEventRateLimitation`
- **多重性**: [0..1]

**容器描述**:

For configurable time intervals of length "IdsMRateLimitationTimeInterval" this filter forwards all the SEvs until reaching the limit "IdsMRateLimitationMaximumEvents".

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMRateLimitationMaximumEvents

- **UUID**: `ECUC:f63c79d5-290e-4e49-9aeb-89bc12111b9a`
- **参数名**: `IdsMRateLimitationMaximumEvents`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of SEvs which are passed on by this filter in a single rate limitation time interval.

######### FLOAT 类型参数

########## 1. IdsMRateLimitationTimeInterval

- **UUID**: `ECUC:7f83aa6e-4e22-4820-a780-b10725c4d5b9`
- **参数名**: `IdsMRateLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time interval length of the event rate limitation filter (as float in seconds).

####### 2. IdsMFilterTrafficLimitation

**容器属性**:

- **UUID**: `ECUC:4ab683fb-cd78-466a-a2a4-66436cf106be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterTrafficLimitation`
- **多重性**: [0..1]

**容器描述**:

The traffic limitation filter forwards all the incoming SEvs until reaching the limit "IdsMTrafficLimitationMaximumBytes".

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IdsMTrafficLimitationMaximumBytes

- **UUID**: `ECUC:e1a4273f-4445-4289-8d7c-32d33421a2da`
- **参数名**: `IdsMTrafficLimitationMaximumBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to be sent out by the IdsM in a single traffic limitation time interval.

######### FLOAT 类型参数

########## 1. IdsMTrafficLimitationTimeInterval

- **UUID**: `ECUC:57f260e9-2178-4dcf-ae42-2871d4045391`
- **参数名**: `IdsMTrafficLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the traffic limitation time interval (as float in seconds).

##### 18. IdsMFilterEventRateLimitation

**容器属性**:

- **UUID**: `ECUC:3f150bd6-bc83-4fda-97cf-ee53a38e90b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterEventRateLimitation`
- **多重性**: [0..1]

**容器描述**:

For configurable time intervals of length "IdsMRateLimitationTimeInterval" this filter forwards all the SEvs until reaching the limit "IdsMRateLimitationMaximumEvents".

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IdsMRateLimitationMaximumEvents

- **UUID**: `ECUC:f63c79d5-290e-4e49-9aeb-89bc12111b9a`
- **参数名**: `IdsMRateLimitationMaximumEvents`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of SEvs which are passed on by this filter in a single rate limitation time interval.

####### FLOAT 类型参数

######## 1. IdsMRateLimitationTimeInterval

- **UUID**: `ECUC:7f83aa6e-4e22-4820-a780-b10725c4d5b9`
- **参数名**: `IdsMRateLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time interval length of the event rate limitation filter (as float in seconds).

##### 19. IdsMFilterTrafficLimitation

**容器属性**:

- **UUID**: `ECUC:4ab683fb-cd78-466a-a2a4-66436cf106be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IdsMFilterTrafficLimitation`
- **多重性**: [0..1]

**容器描述**:

The traffic limitation filter forwards all the incoming SEvs until reaching the limit "IdsMTrafficLimitationMaximumBytes".

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IdsMTrafficLimitationMaximumBytes

- **UUID**: `ECUC:e1a4273f-4445-4289-8d7c-32d33421a2da`
- **参数名**: `IdsMTrafficLimitationMaximumBytes`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum number of bytes to be sent out by the IdsM in a single traffic limitation time interval.

####### FLOAT 类型参数

######## 1. IdsMTrafficLimitationTimeInterval

- **UUID**: `ECUC:57f260e9-2178-4dcf-ae42-2871d4045391`
- **参数名**: `IdsMTrafficLimitationTimeInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the traffic limitation time interval (as float in seconds).

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

1. **IdsM**
