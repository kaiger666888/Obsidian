# PduR - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:29

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [PduR](#pdur)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. PduR

#### 基本信息

- **UUID**: `ECUC:fadc19f9-cb7a-425e-bb8a-1c29a01e6c62`
- **模块名称**: `PduR`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the PduR (PDU Router) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. PduRBswModules

**容器属性**:

- **UUID**: `ECUC:9d14c1e3-3ffa-4e41-b827-3cdbdc976db5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRBswModules`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container describes a specific BSW module (upper/CDD/lower/IpduM) that the PDU Router shall interface to.

###### 参数配置

此容器包含 **11** 个参数：

####### BOOLEAN 类型参数

######## 1. PduRCancelReceive

- **UUID**: `ECUC:4dc154b1-b714-4c7b-b8c4-a1c2ebcfcf45`
- **参数名**: `PduRCancelReceive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the Transport protocol module supports the CancelReceive API or not. Value true the API is supported.

######## 2. PduRCancelTransmit

- **UUID**: `ECUC:7ff785b2-60cb-4bcb-a1aa-6aa874772c77`
- **参数名**: `PduRCancelTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the CancelTransmit API or not. Value true the API is supported.

######## 3. PduRChangeParameterRequestApi

- **UUID**: `ECUC:94688c7e-2198-4728-95dd-513fc60e3f52`
- **参数名**: `PduRChangeParameterRequestApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter, if set to true, enables the PduR_<Up>ChangeParameterRequest Api for this Module.

######## 4. PduRCommunicationInterface

- **UUID**: `ECUC:6c9ea706-3cd4-48c2-b7df-d5421edc59c4`
- **参数名**: `PduRCommunicationInterface`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the Communication Interface APIs or not. Value true the APIs are supported.

######## 5. PduRLowerModule

- **UUID**: `ECUC:c20d973d-127f-45d4-9a6a-ef154ccb7e07`
- **参数名**: `PduRLowerModule`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PduRLowerModule will decide who will call the APIs and who will implement the APIs.

######## 6. PduRRetransmission

- **UUID**: `ECUC:a3f90acf-2c9a-4438-a2c2-6701847a1b59`
- **参数名**: `PduRRetransmission`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true this means that the destination transport protocol module will use the retransmission feature. This parameter might be set to false if the retransmission feature is not used, even though the destination transport protocol is supporting it.

######## 7. PduRTransportProtocol

- **UUID**: `ECUC:4ac6882a-dc4f-4b05-a4d7-cfced6cc2756`
- **参数名**: `PduRTransportProtocol`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PDU Router module shall use the API parameters specified for transport protocol interface.

######## 8. PduRTriggertransmit

- **UUID**: `ECUC:0e442b0f-7d31-4ded-a613-2baeaaf68da8`
- **参数名**: `PduRTriggertransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the TriggerTransmit API or not. Value true the API is supported.

######## 9. PduRTxConfirmation

- **UUID**: `ECUC:2713176a-55c3-4062-9ec9-a7358e2faed8`
- **参数名**: `PduRTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the TxConfirmation API or not. Value true the API is supported.

######## 10. PduRUpperModule

- **UUID**: `ECUC:c1a824b7-1988-4486-9e22-e6f984fa970b`
- **参数名**: `PduRUpperModule`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The PduRUpperModule will decide who will call the APIs and who will implement the APIs.

######## 11. PduRUseTag

- **UUID**: `ECUC:8193a707-ad69-46d8-ad08-50365d2f2f2c`
- **参数名**: `PduRUseTag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter, if set to true, enables the usage of the tag (<up>) in the following API calls:

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. PduRBswModuleRef

- **UUID**: `ECUC:43b65d8a-1610-46bb-9997-0fb06b6a52f8`
- **引用名**: `PduRBswModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to one BSW module's configuration (i.e. not the ECUC parameter definition template).

##### 2. PduRGeneral

**容器属性**:

- **UUID**: `ECUC:92bfa44f-5c0a-408f-b100-ca90c67b8b61`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduR and specifies the general configuration parameters of the PDU Router.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. PduRDevErrorDetect

- **UUID**: `ECUC:87e2a6a8-4a23-42d9-895d-8829dacb4181`
- **参数名**: `PduRDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true then PDU Router will enable the error-reporting to the Development Error Tracer (DET).

######## 2. PduRVersionInfoApi

- **UUID**: `ECUC:32d6ed3e-46fd-4315-a3db-aa69215a7163`
- **参数名**: `PduRVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true the PduR_GetVersionInfo API is available.

######## 3. PduRZeroCostOperation

- **UUID**: `ECUC:b9d6831c-1933-4de2-ae7c-5f83dee1dcef`
- **参数名**: `PduRZeroCostOperation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set the PduR configuration generator will report an error if zero-cost-operation cannot be fulfilled.

##### 3. PduRRoutingTables

**容器属性**:

- **UUID**: `ECUC:21e5e0e0-f062-4273-937e-556059ca8e9f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingTables`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Represents one table of routing paths.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduRConfigurationId

- **UUID**: `ECUC:bf4f85f7-161c-4c10-8f21-684f008c9fdf`
- **参数名**: `PduRConfigurationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of the configuration of the PduR configuration. This identification can be read using the PduR API.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. PduRRoutingPathGroup

**容器属性**:

- **UUID**: `ECUC:227b5ecb-d5eb-4221-b99f-52bb63ffbdcd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPathGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container groups routing path destinations. Destinations are used instead of routing paths since a routing path can be 1:n. It is desirable to be able to enable/disable a specific bus (i.e. a destination) rather than a routing path. Of course it is possible to create groups that covers specific routing paths as well.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRRoutingPathGroupId

- **UUID**: `ECUC:47f4043a-68dc-4e5a-92b2-37abd8b4d2dc`
- **参数名**: `PduRRoutingPathGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of the routing group.

######### BOOLEAN 类型参数

########## 1. PduRIsEnabledAtInit

- **UUID**: `ECUC:08bfffe3-e6dc-43c7-85b3-2324e0005b2e`
- **参数名**: `PduRIsEnabledAtInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true this routing path group will be enabled after initializing the PDU Router module (i.e. enabled in the PduR_Init function).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. PduRDestPduRef

- **UUID**: `ECUC:b36c1774-b6e5-44e0-80be-55fd3694f0db`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `PduRDestPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingTable/PduRRoutingPath/PduRDestPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference selects one destination of the routing path.

####### 2. PduRRoutingTable

**容器属性**:

- **UUID**: `ECUC:278d644b-290e-4404-a833-1f94cec37e04`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingTable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents one container of routing paths. Each container is either minimum routing or not.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. PduRIsMinimumRouting

- **UUID**: `ECUC:a161fe81-d390-4704-b13d-c8ba1435f5a7`
- **参数名**: `PduRIsMinimumRouting`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the container contains routing paths that are of the type minimum routing or not.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. PduRRoutingPath

**容器属性**:

- **UUID**: `ECUC:b34f639c-dc43-4ee1-874f-2af20abf1420`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPath`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingTable and specifies the routing path of a PDU.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

############## 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

############# BOOLEAN 类型参数

############## 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

############# ENUMERATION 类型参数

############## 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

############## 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

############## 配置容器

本模块包含 **1** 个配置容器：

############### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

################ 参数配置

此容器包含 **2** 个参数：

################# INTEGER 类型参数

################## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

############# 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 2. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 3. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 4. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

######### 2. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

############ 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

########### BOOLEAN 类型参数

############ 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

########### ENUMERATION 类型参数

############ 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

############ 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 3. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 4. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 5. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

####### 3. PduRRoutingPath

**容器属性**:

- **UUID**: `ECUC:b34f639c-dc43-4ee1-874f-2af20abf1420`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPath`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingTable and specifies the routing path of a PDU.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

############ 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

########### BOOLEAN 类型参数

############ 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

########### ENUMERATION 类型参数

############ 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

############ 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 2. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 3. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 4. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

####### 4. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

########## 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

######### BOOLEAN 类型参数

########## 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

######### ENUMERATION 类型参数

########## 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

########## 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 5. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 6. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

########## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 7. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

####### 8. PduRTpBufferTable

**容器属性**:

- **UUID**: `ECUC:4c947152-28c5-48b4-96b2-9c06c3532959`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBufferTable`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container will specify the needed buffers for gatewaying using TP. It is not connected to the specific routing path destination to allow a more efficient buffer handling.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRMaxTpBufferNumber

- **UUID**: `ECUC:abf0585e-ee9b-449f-b424-b7c99bedfcba`
- **参数名**: `PduRMaxTpBufferNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: maximum number of TP buffers.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRTpBuffer

**容器属性**:

- **UUID**: `ECUC:91959d7d-19f9-41e9-8da1-51a2767f0392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through TP.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. PduRTpBufferLength

- **UUID**: `ECUC:78b6c36d-0423-44ee-8182-34f51e04aaee`
- **参数名**: `PduRTpBufferLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the TP buffer in number of bytes

####### 9. PduRTpBuffer

**容器属性**:

- **UUID**: `ECUC:91959d7d-19f9-41e9-8da1-51a2767f0392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through TP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRTpBufferLength

- **UUID**: `ECUC:78b6c36d-0423-44ee-8182-34f51e04aaee`
- **参数名**: `PduRTpBufferLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the TP buffer in number of bytes

####### 10. PduRTxBufferTable

**容器属性**:

- **UUID**: `ECUC:2a4738bb-3c54-4bcd-9953-62ab057e5565`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBufferTable`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container will specify the needed buffers for gatewaying using communication interface. It not defined per routing path to allow reusage of buffers.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRMaxTxBufferNumber

- **UUID**: `ECUC:38dd3ea6-2b96-402b-ae50-9f6e1a241522`
- **参数名**: `PduRMaxTxBufferNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: maximum number of Tx buffers.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRTxBuffer

**容器属性**:

- **UUID**: `ECUC:49403503-38ea-4903-a735-464e90ac37c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through communication interface.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRPduMaxLength

- **UUID**: `ECUC:5b99114f-dfc8-451b-abc9-b4190f4e3de0`
- **参数名**: `PduRPduMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tx buffer in number of bytes.

############ 2. PduRTxBufferDepth

- **UUID**: `ECUC:92eacf11-0c59-4c59-8647-1254f459175b`
- **参数名**: `PduRTxBufferDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Pdus that can be stored in the buffer. If value is 1 then the buffer semantic is "last is best". If the value is greater then 1 then the buffer semnatic is a FiFo.

####### 11. PduRTxBuffer

**容器属性**:

- **UUID**: `ECUC:49403503-38ea-4903-a735-464e90ac37c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through communication interface.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRPduMaxLength

- **UUID**: `ECUC:5b99114f-dfc8-451b-abc9-b4190f4e3de0`
- **参数名**: `PduRPduMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tx buffer in number of bytes.

########## 2. PduRTxBufferDepth

- **UUID**: `ECUC:92eacf11-0c59-4c59-8647-1254f459175b`
- **参数名**: `PduRTxBufferDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Pdus that can be stored in the buffer. If value is 1 then the buffer semantic is "last is best". If the value is greater then 1 then the buffer semnatic is a FiFo.

##### 4. PduRRoutingPathGroup

**容器属性**:

- **UUID**: `ECUC:227b5ecb-d5eb-4221-b99f-52bb63ffbdcd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPathGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container groups routing path destinations. Destinations are used instead of routing paths since a routing path can be 1:n. It is desirable to be able to enable/disable a specific bus (i.e. a destination) rather than a routing path. Of course it is possible to create groups that covers specific routing paths as well.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. PduRRoutingPathGroupId

- **UUID**: `ECUC:47f4043a-68dc-4e5a-92b2-37abd8b4d2dc`
- **参数名**: `PduRRoutingPathGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of the routing group.

####### BOOLEAN 类型参数

######## 1. PduRIsEnabledAtInit

- **UUID**: `ECUC:08bfffe3-e6dc-43c7-85b3-2324e0005b2e`
- **参数名**: `PduRIsEnabledAtInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true this routing path group will be enabled after initializing the PDU Router module (i.e. enabled in the PduR_Init function).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. PduRDestPduRef

- **UUID**: `ECUC:b36c1774-b6e5-44e0-80be-55fd3694f0db`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `PduRDestPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRRoutingTable/PduRRoutingPath/PduRDestPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference selects one destination of the routing path.

##### 5. PduRRoutingTable

**容器属性**:

- **UUID**: `ECUC:278d644b-290e-4404-a833-1f94cec37e04`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingTable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents one container of routing paths. Each container is either minimum routing or not.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. PduRIsMinimumRouting

- **UUID**: `ECUC:a161fe81-d390-4704-b13d-c8ba1435f5a7`
- **参数名**: `PduRIsMinimumRouting`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the container contains routing paths that are of the type minimum routing or not.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. PduRRoutingPath

**容器属性**:

- **UUID**: `ECUC:b34f639c-dc43-4ee1-874f-2af20abf1420`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPath`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingTable and specifies the routing path of a PDU.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

############ 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

########### BOOLEAN 类型参数

############ 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

########### ENUMERATION 类型参数

############ 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

############ 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

################ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

########### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 2. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 3. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 4. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

####### 2. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

########## 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

######### BOOLEAN 类型参数

########## 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

######### ENUMERATION 类型参数

########## 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

########## 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 3. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 4. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

########## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 5. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

##### 6. PduRRoutingPath

**容器属性**:

- **UUID**: `ECUC:b34f639c-dc43-4ee1-874f-2af20abf1420`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRRoutingPath`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingTable and specifies the routing path of a PDU.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

########## 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

######### BOOLEAN 类型参数

########## 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

######### ENUMERATION 类型参数

########## 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

########## 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

######### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 2. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 3. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

########## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 4. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

##### 7. PduRDestPdu

**容器属性**:

- **UUID**: `ECUC:b454f3f4-3809-451b-9d41-9e2a9439efa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDestPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be routed.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. PduRDestPduHandleId

- **UUID**: `ECUC:1ba27146-785d-4d14-b4af-c8ce7a67ee2a`
- **参数名**: `PduRDestPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol modules for confirmation.

######## 2. PduRTpThreshold

- **UUID**: `ECUC:5f377d0a-4d8f-4d86-a1de-d229bb138759`
- **参数名**: `PduRTpThreshold`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the number of bytes which shall be received before transmission on the destination bus may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not be larger than the length of the related TP Buffer.

####### BOOLEAN 类型参数

######## 1. PduRTransmissionConfirmation

- **UUID**: `ECUC:52c9d454-13f2-4658-a44c-fb5e437eb037`
- **参数名**: `PduRTransmissionConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is only for communication interfaces. Transport protocol modules will always call the TxConfirmation function.

####### ENUMERATION 类型参数

######## 1. PduRDestPduDataProvision

- **UUID**: `ECUC:28bfa72a-3116-4c8d-a7be-f4fcbc364c52`
- **参数名**: `PduRDestPduDataProvision`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `PDUR_DIRECT` (来源: AUTOSAR_ECUC)
  - `PDUR_TRIGGERTRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies how data are provided: direct (as part of the Transmit call) or via the TriggerTransmit callback function. Only required for non-TP I-PDUs (local and gatewayed).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. PduRDestPduRef

- **UUID**: `ECUC:aec3f7af-e5fd-4278-a8da-c2077fe5576e`
- **引用名**: `PduRDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination PDU reference; reference to unique PDU identifier which shall be used by the PDU Router instead of the source PDU ID when calling the related function of the destination module.

######## 2. PduRDestTxBufferRef

- **UUID**: `ECUC:6dcee2de-24d2-42c5-a3c2-90f3f3e7ae72`
- **引用名**: `PduRDestTxBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `PduRTxBuffer`
- **完整路径**: `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables/PduRTxBufferTable/PduRTxBuffer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a buffer that is allocated in the PduRTxBuffer. Having a global (for PduR) list of buffers allows reusage and hence less memory consumption.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

############ 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

####### 2. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

########## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

##### 8. PduRDefaultValue

**容器属性**:

- **UUID**: `ECUC:1f0d235b-3a07-49ff-82f3-f44f25001666`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValue`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies the default value of the I-PDU. Only required for gateway operation and if at least one PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

########## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

##### 9. PduRDefaultValueElement

**容器属性**:

- **UUID**: `ECUC:d3da5970-3037-44e6-9144-add5b3ec9f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRDefaultValueElement`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each value element is represented by the element and the position in an array.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. PduRDefaultValueElement

- **UUID**: `ECUC:ba80d004-c08d-4071-9649-9dd8b030575b`
- **参数名**: `PduRDefaultValueElement`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The default value consists of a number of elements. Each element is one byte long and the number of elements is specified by SduLength. The position of this parameter in the container is specified by the PduRElementBytePosition parameter.

######## 2. PduRDefaultValueElementBytePosition

- **UUID**: `ECUC:f70a2789-5103-4cec-9e84-9bba77bf25f8`
- **参数名**: `PduRDefaultValueElementBytePosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the byte position of the element within the default value

##### 10. PduRSrcPdu

**容器属性**:

- **UUID**: `ECUC:91525ed0-6a1c-468b-91ec-479bc8da0b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRSrcPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be routed.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduRSourcePduHandleId

- **UUID**: `ECUC:9281db8e-b425-4608-8acf-8622ee8969fd`
- **参数名**: `PduRSourcePduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier assigned by PDU Router.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. PduRSrcPduRef

- **UUID**: `ECUC:96fa6c63-feae-4e75-bc15-ad55c4eac4af`
- **引用名**: `PduRSrcPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source PDU reference; reference to unique PDU identifier which shall be used for the requested PDU Router operation.

##### 11. PduRTpBufferTable

**容器属性**:

- **UUID**: `ECUC:4c947152-28c5-48b4-96b2-9c06c3532959`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBufferTable`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container will specify the needed buffers for gatewaying using TP. It is not connected to the specific routing path destination to allow a more efficient buffer handling.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduRMaxTpBufferNumber

- **UUID**: `ECUC:abf0585e-ee9b-449f-b424-b7c99bedfcba`
- **参数名**: `PduRMaxTpBufferNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: maximum number of TP buffers.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PduRTpBuffer

**容器属性**:

- **UUID**: `ECUC:91959d7d-19f9-41e9-8da1-51a2767f0392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through TP.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. PduRTpBufferLength

- **UUID**: `ECUC:78b6c36d-0423-44ee-8182-34f51e04aaee`
- **参数名**: `PduRTpBufferLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the TP buffer in number of bytes

##### 12. PduRTpBuffer

**容器属性**:

- **UUID**: `ECUC:91959d7d-19f9-41e9-8da1-51a2767f0392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTpBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through TP.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduRTpBufferLength

- **UUID**: `ECUC:78b6c36d-0423-44ee-8182-34f51e04aaee`
- **参数名**: `PduRTpBufferLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the TP buffer in number of bytes

##### 13. PduRTxBufferTable

**容器属性**:

- **UUID**: `ECUC:2a4738bb-3c54-4bcd-9953-62ab057e5565`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBufferTable`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container will specify the needed buffers for gatewaying using communication interface. It not defined per routing path to allow reusage of buffers.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. PduRMaxTxBufferNumber

- **UUID**: `ECUC:38dd3ea6-2b96-402b-ae50-9f6e1a241522`
- **参数名**: `PduRMaxTxBufferNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: maximum number of Tx buffers.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. PduRTxBuffer

**容器属性**:

- **UUID**: `ECUC:49403503-38ea-4903-a735-464e90ac37c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through communication interface.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. PduRPduMaxLength

- **UUID**: `ECUC:5b99114f-dfc8-451b-abc9-b4190f4e3de0`
- **参数名**: `PduRPduMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tx buffer in number of bytes.

########## 2. PduRTxBufferDepth

- **UUID**: `ECUC:92eacf11-0c59-4c59-8647-1254f459175b`
- **参数名**: `PduRTxBufferDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Pdus that can be stored in the buffer. If value is 1 then the buffer semantic is "last is best". If the value is greater then 1 then the buffer semnatic is a FiFo.

##### 14. PduRTxBuffer

**容器属性**:

- **UUID**: `ECUC:49403503-38ea-4903-a735-464e90ac37c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `PduRTxBuffer`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Specifies a buffer used for gatwaying through communication interface.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. PduRPduMaxLength

- **UUID**: `ECUC:5b99114f-dfc8-451b-abc9-b4190f4e3de0`
- **参数名**: `PduRPduMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Tx buffer in number of bytes.

######## 2. PduRTxBufferDepth

- **UUID**: `ECUC:92eacf11-0c59-4c59-8647-1254f459175b`
- **参数名**: `PduRTxBufferDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Pdus that can be stored in the buffer. If value is 1 then the buffer semantic is "last is best". If the value is greater then 1 then the buffer semnatic is a FiFo.

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

1. **PduR**
