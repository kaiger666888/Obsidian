# Cdd - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:58

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Cdd](#cdd)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Cdd

#### 基本信息

- **UUID**: `75b6b250-bcbf-4796-b89c-7788f4c96bde`
- **模块名称**: `Cdd`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

The CDD module describes the minimal requirements that are necessary for the configuration of a Complex Driver with access to the MICROSAR communication stack.

#### 版本历史

共有 **9** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2011-12-05
- **发布者**: visms

**变更内容**:

##### 2. 版本 2.00.00

- **状态**: released
- **发布日期**: 2011-11-09
- **发布者**: visms

**变更内容**:

##### 3. 版本 2.01.00

- **状态**: released
- **发布日期**: 2012-10-30
- **发布者**: visms

**变更内容**:

##### 4. 版本 2.02.00

- **状态**: released
- **发布日期**: 2013-07-09
- **发布者**: visms

**变更内容**:

##### 5. 版本 2.02.00

- **状态**: released
- **发布日期**: 2013-10-23
- **发布者**: visbms

**变更内容**:

##### 6. 版本 2.03.00

- **状态**: released
- **发布日期**: 2014-03-14
- **发布者**: visbms

**变更内容**:

##### 7. 版本 2.04.00

- **状态**: released
- **发布日期**: 2014-05-07
- **发布者**: visms

**变更内容**:

##### 8. 版本 3.00.00

- **状态**: released
- **发布日期**: 2015-12-10
- **发布者**: visms

**变更内容**:

##### 9. 版本 4.00.00

- **状态**: released
- **发布日期**: 2018-04-10T14:41:05+02:00
- **发布者**: visms

**变更内容**:

#### 配置容器

本模块包含 **19** 个配置容器：

##### 1. CddComStackContribution

**容器属性**:

- **UUID**: `6324a9f1-57e8-4f22-ac45-f4788ee656b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComStackContribution`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Contribution of COM Stack modules.

###### 配置容器

本模块包含 **17** 个配置容器：

####### 1. CddComIfUpperLayerContribution

**容器属性**:

- **UUID**: `4eb55953-e1c9-46c3-bfbb-854a92e0a1c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects parameters for the configuration of a Complex Driver that serves as the UpperLayer of a Com Interface module (e.g. CanIf, FrIf).

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `b5db045e-b750-4374-88dc-c005d6e70aa6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the CDD through communication stack.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddComIfHandleId

- **UUID**: `b557210e-e180-47b3-a7d5-00a4175beab5`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComIfPduRef

- **UUID**: `d9ac6a8e-ba7a-4351-80ca-0e009d061bee`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `5263ae0e-bc7f-4029-a29e-233fcb1d4773`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted by the CDD through communication stack.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddComIfHandleId

- **UUID**: `cf64056b-4447-419c-bae7-1920ad572379`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComIfPduRef

- **UUID**: `339a808f-a35e-4e1a-807c-8a732de26efe`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `b5db045e-b750-4374-88dc-c005d6e70aa6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `b557210e-e180-47b3-a7d5-00a4175beab5`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `d9ac6a8e-ba7a-4351-80ca-0e009d061bee`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `5263ae0e-bc7f-4029-a29e-233fcb1d4773`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `cf64056b-4447-419c-bae7-1920ad572379`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `339a808f-a35e-4e1a-807c-8a732de26efe`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. CddComMLowerLayerContribution

**容器属性**:

- **UUID**: `359aba17-2cfa-4f1b-9f46-3a4241c30fd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerContribution`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Communication Manager module.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `46db85fd-6028-440b-8c28-22ce5329300a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComMLowerLayerChannelRef

- **UUID**: `15e21fcd-efc1-498e-973c-21d95a3b1db0`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

####### 5. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `46db85fd-6028-440b-8c28-22ce5329300a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComMLowerLayerChannelRef

- **UUID**: `15e21fcd-efc1-498e-973c-21d95a3b1db0`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

####### 6. CddGenericNmLowerLayerContribution

**容器属性**:

- **UUID**: `5da398b5-a8b1-4c0f-83ef-4559e3ca5fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerContribution`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Generic NM module.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ea4aa6cc-932b-47d5-9a9f-df7c04f0f9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `b8d93d94-3974-4972-9ced-b508728b7c85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 7. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ea4aa6cc-932b-47d5-9a9f-df7c04f0f9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `b8d93d94-3974-4972-9ced-b508728b7c85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 8. CddPduRLowerLayerContribution

**容器属性**:

- **UUID**: `472beadf-c929-4236-b486-87ab5b4600ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the LowerLayer of the Pdu Router module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `7f255f9e-0841-4b2a-856d-9b3d87147d67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU that is received by the Complex Driver and forwarded to the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRLowerLayerHandleId

- **UUID**: `797c5e4b-587b-4450-9968-8f754af9b028`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRLowerLayerPduRef

- **UUID**: `fc5b32a4-1c82-41af-bc70-bf715a353f8c`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `1e448fd7-b811-46ff-8243-092b0124ff4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU that is received by the Complex Driver from the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRLowerLayerHandleId

- **UUID**: `494ffc30-bab3-4f75-bed3-87e14b62de8a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRLowerLayerPduRef

- **UUID**: `6a71c385-1bbb-4494-8745-f23651d3979f`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `7f255f9e-0841-4b2a-856d-9b3d87147d67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU that is received by the Complex Driver and forwarded to the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `797c5e4b-587b-4450-9968-8f754af9b028`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `fc5b32a4-1c82-41af-bc70-bf715a353f8c`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `1e448fd7-b811-46ff-8243-092b0124ff4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU that is received by the Complex Driver from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `494ffc30-bab3-4f75-bed3-87e14b62de8a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `6a71c385-1bbb-4494-8745-f23651d3979f`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. CddPduRUpperLayerContribution

**容器属性**:

- **UUID**: `20df7305-bd40-4180-9503-6c54f2a53761`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the Pdu Router module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `a013cb87-68ba-4b1e-80d4-0e5f3633a4b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the Complex Driver from the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRUpperLayerHandleId

- **UUID**: `04191e6f-a97c-448a-b067-58f3be38ab8d`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRUpperLayerPduRef

- **UUID**: `08b6af03-b340-434b-92c0-bfceab97f090`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `78369d0e-e11b-43d0-85f0-a421f110b98d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted from the Complex Driver to the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRUpperLayerHandleId

- **UUID**: `56912387-288f-4230-93bf-f63698dec8bf`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRUpperLayerPduRef

- **UUID**: `3dd052c4-c151-45ab-85c5-646123befd3d`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 12. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `a013cb87-68ba-4b1e-80d4-0e5f3633a4b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the Complex Driver from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `04191e6f-a97c-448a-b067-58f3be38ab8d`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `08b6af03-b340-434b-92c0-bfceab97f090`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 13. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `78369d0e-e11b-43d0-85f0-a421f110b98d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted from the Complex Driver to the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `56912387-288f-4230-93bf-f63698dec8bf`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `3dd052c4-c151-45ab-85c5-646123befd3d`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 14. CddJ1939RmContribution

**容器属性**:

- **UUID**: `cd27f041-a2c0-4275-b82c-e342b5c5da40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddJ1939RmContribution`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container collects parameters for the configuration of a Complex Driver that serves as UpperLayer of the J1939Rm module.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. CddJ1939RmRequestIndication

- **UUID**: `863f99de-d754-4c6c-9533-8de009e6eeb4`
- **参数名**: `CddJ1939RmRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm RequestIndication for this CDD. The RequestIndication provides information about a received J1939 RQST message which affects a J1939Rm user that references this CDD.

Prototype of the RequestIndication:
void <Cdd>_RequestIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn, uint8 sourceAddress, uint8 destAddress, uint8 priority)

########## 2. CddJ1939RmAckIndication

- **UUID**: `b61dbb6e-8bdb-462a-adf9-6f39a3f5f0a6`
- **参数名**: `CddJ1939RmAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm AckIndication for this CDD. The AckIndication provides information about a received J1939 ACKM message which affects a J1939Rm user that references this CDD.

Prototype of the AckIndication:
void <Cdd>_AckIndication(uint8 node, NetworkHandleType channel, uint32 ackPgn, uint8 ackCode, uint8 ackAddress, uint8 sourceAddress, uint8 priority)

########## 3. CddJ1939RmRequestTimeoutIndication

- **UUID**: `24bbb827-4f47-4ea1-8704-699997253ed7`
- **参数名**: `CddJ1939RmRequestTimeoutIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm RequestTimeoutIndication for this CDD. The RequestTimeoutIndication is called after time out of a transmitted J1939 RQST message.

Prototype of the AckIndication:
void <Cdd>_RequestTimeoutIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn, uint8 destAddress)

####### 15. CddSoAdUpperLayerContribution

**容器属性**:

- **UUID**: `6fdc622b-e8e6-4ed4-a132-4ab288f7657f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `9f8374e9-4512-4c39-92e8-1a824d7a93e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CddSoAdUpperLayerHandleId

- **UUID**: `dc627d77-4dd6-4606-be1c-38e1b70a8709`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########### ENUMERATION 类型参数

############ 1. CddPduRApiType

- **UUID**: `0b4469cf-4971-4e98-8441-4a75b49e5506`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddSoAdUpperLayerPduRef

- **UUID**: `710afe0b-bee3-4da7-a62b-949982842796`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `7939631b-94a4-4613-aa26-12427365c119`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CddSoAdUpperLayerHandleId

- **UUID**: `437bf1b9-c2b0-437b-b400-57daadf5d602`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########### ENUMERATION 类型参数

############ 1. CddPduRApiType

- **UUID**: `18946c4c-496d-4cf5-95af-9dfad997219c`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddSoAdUpperLayerPduRef

- **UUID**: `10a90951-9028-4ccb-b797-a428aa638aa5`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 16. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `9f8374e9-4512-4c39-92e8-1a824d7a93e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `dc627d77-4dd6-4606-be1c-38e1b70a8709`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######### ENUMERATION 类型参数

########## 1. CddPduRApiType

- **UUID**: `0b4469cf-4971-4e98-8441-4a75b49e5506`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `710afe0b-bee3-4da7-a62b-949982842796`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 17. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `7939631b-94a4-4613-aa26-12427365c119`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `437bf1b9-c2b0-437b-b400-57daadf5d602`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######### ENUMERATION 类型参数

########## 1. CddPduRApiType

- **UUID**: `18946c4c-496d-4cf5-95af-9dfad997219c`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `10a90951-9028-4ccb-b797-a428aa638aa5`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 2. CddComIfUpperLayerContribution

**容器属性**:

- **UUID**: `4eb55953-e1c9-46c3-bfbb-854a92e0a1c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects parameters for the configuration of a Complex Driver that serves as the UpperLayer of a Com Interface module (e.g. CanIf, FrIf).

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `b5db045e-b750-4374-88dc-c005d6e70aa6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `b557210e-e180-47b3-a7d5-00a4175beab5`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `d9ac6a8e-ba7a-4351-80ca-0e009d061bee`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `5263ae0e-bc7f-4029-a29e-233fcb1d4773`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `cf64056b-4447-419c-bae7-1920ad572379`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `339a808f-a35e-4e1a-807c-8a732de26efe`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 3. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `b5db045e-b750-4374-88dc-c005d6e70aa6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the CDD through communication stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddComIfHandleId

- **UUID**: `b557210e-e180-47b3-a7d5-00a4175beab5`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComIfPduRef

- **UUID**: `d9ac6a8e-ba7a-4351-80ca-0e009d061bee`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 4. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `5263ae0e-bc7f-4029-a29e-233fcb1d4773`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted by the CDD through communication stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddComIfHandleId

- **UUID**: `cf64056b-4447-419c-bae7-1920ad572379`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComIfPduRef

- **UUID**: `339a808f-a35e-4e1a-807c-8a732de26efe`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 5. CddComMLowerLayerContribution

**容器属性**:

- **UUID**: `359aba17-2cfa-4f1b-9f46-3a4241c30fd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerContribution`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Communication Manager module.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `46db85fd-6028-440b-8c28-22ce5329300a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComMLowerLayerChannelRef

- **UUID**: `15e21fcd-efc1-498e-973c-21d95a3b1db0`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

##### 6. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `46db85fd-6028-440b-8c28-22ce5329300a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComMLowerLayerChannelRef

- **UUID**: `15e21fcd-efc1-498e-973c-21d95a3b1db0`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

##### 7. CddGenericNmLowerLayerContribution

**容器属性**:

- **UUID**: `5da398b5-a8b1-4c0f-83ef-4559e3ca5fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerContribution`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Generic NM module.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ea4aa6cc-932b-47d5-9a9f-df7c04f0f9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `b8d93d94-3974-4972-9ced-b508728b7c85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 8. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ea4aa6cc-932b-47d5-9a9f-df7c04f0f9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `b8d93d94-3974-4972-9ced-b508728b7c85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 9. CddPduRLowerLayerContribution

**容器属性**:

- **UUID**: `472beadf-c929-4236-b486-87ab5b4600ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the LowerLayer of the Pdu Router module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `7f255f9e-0841-4b2a-856d-9b3d87147d67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU that is received by the Complex Driver and forwarded to the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `797c5e4b-587b-4450-9968-8f754af9b028`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `fc5b32a4-1c82-41af-bc70-bf715a353f8c`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `1e448fd7-b811-46ff-8243-092b0124ff4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU that is received by the Complex Driver from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `494ffc30-bab3-4f75-bed3-87e14b62de8a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `6a71c385-1bbb-4494-8745-f23651d3979f`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `7f255f9e-0841-4b2a-856d-9b3d87147d67`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Rx PDU that is received by the Complex Driver and forwarded to the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRLowerLayerHandleId

- **UUID**: `797c5e4b-587b-4450-9968-8f754af9b028`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRLowerLayerPduRef

- **UUID**: `fc5b32a4-1c82-41af-bc70-bf715a353f8c`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `1e448fd7-b811-46ff-8243-092b0124ff4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Tx PDU that is received by the Complex Driver from the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRLowerLayerHandleId

- **UUID**: `494ffc30-bab3-4f75-bed3-87e14b62de8a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRLowerLayerPduRef

- **UUID**: `6a71c385-1bbb-4494-8745-f23651d3979f`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. CddPduRUpperLayerContribution

**容器属性**:

- **UUID**: `20df7305-bd40-4180-9503-6c54f2a53761`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the Pdu Router module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `a013cb87-68ba-4b1e-80d4-0e5f3633a4b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the Complex Driver from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `04191e6f-a97c-448a-b067-58f3be38ab8d`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `08b6af03-b340-434b-92c0-bfceab97f090`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `78369d0e-e11b-43d0-85f0-a421f110b98d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted from the Complex Driver to the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `56912387-288f-4230-93bf-f63698dec8bf`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `3dd052c4-c151-45ab-85c5-646123befd3d`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 13. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `a013cb87-68ba-4b1e-80d4-0e5f3633a4b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are received by the Complex Driver from the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRUpperLayerHandleId

- **UUID**: `04191e6f-a97c-448a-b067-58f3be38ab8d`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRUpperLayerPduRef

- **UUID**: `08b6af03-b340-434b-92c0-bfceab97f090`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 14. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `78369d0e-e11b-43d0-85f0-a421f110b98d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are transmitted from the Complex Driver to the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRUpperLayerHandleId

- **UUID**: `56912387-288f-4230-93bf-f63698dec8bf`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRUpperLayerPduRef

- **UUID**: `3dd052c4-c151-45ab-85c5-646123befd3d`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 15. CddJ1939RmContribution

**容器属性**:

- **UUID**: `cd27f041-a2c0-4275-b82c-e342b5c5da40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddJ1939RmContribution`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container collects parameters for the configuration of a Complex Driver that serves as UpperLayer of the J1939Rm module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. CddJ1939RmRequestIndication

- **UUID**: `863f99de-d754-4c6c-9533-8de009e6eeb4`
- **参数名**: `CddJ1939RmRequestIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm RequestIndication for this CDD. The RequestIndication provides information about a received J1939 RQST message which affects a J1939Rm user that references this CDD.

Prototype of the RequestIndication:
void <Cdd>_RequestIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn, uint8 sourceAddress, uint8 destAddress, uint8 priority)

######## 2. CddJ1939RmAckIndication

- **UUID**: `b61dbb6e-8bdb-462a-adf9-6f39a3f5f0a6`
- **参数名**: `CddJ1939RmAckIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm AckIndication for this CDD. The AckIndication provides information about a received J1939 ACKM message which affects a J1939Rm user that references this CDD.

Prototype of the AckIndication:
void <Cdd>_AckIndication(uint8 node, NetworkHandleType channel, uint32 ackPgn, uint8 ackCode, uint8 ackAddress, uint8 sourceAddress, uint8 priority)

######## 3. CddJ1939RmRequestTimeoutIndication

- **UUID**: `24bbb827-4f47-4ea1-8704-699997253ed7`
- **参数名**: `CddJ1939RmRequestTimeoutIndication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables the J1939Rm RequestTimeoutIndication for this CDD. The RequestTimeoutIndication is called after time out of a transmitted J1939 RQST message.

Prototype of the AckIndication:
void <Cdd>_RequestTimeoutIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn, uint8 destAddress)

##### 16. CddSoAdUpperLayerContribution

**容器属性**:

- **UUID**: `6fdc622b-e8e6-4ed4-a132-4ab288f7657f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerContribution`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the SoAd module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `9f8374e9-4512-4c39-92e8-1a824d7a93e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `dc627d77-4dd6-4606-be1c-38e1b70a8709`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######### ENUMERATION 类型参数

########## 1. CddPduRApiType

- **UUID**: `0b4469cf-4971-4e98-8441-4a75b49e5506`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `710afe0b-bee3-4da7-a62b-949982842796`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `7939631b-94a4-4613-aa26-12427365c119`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `437bf1b9-c2b0-437b-b400-57daadf5d602`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######### ENUMERATION 类型参数

########## 1. CddPduRApiType

- **UUID**: `18946c4c-496d-4cf5-95af-9dfad997219c`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `10a90951-9028-4ccb-b797-a428aa638aa5`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 17. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `9f8374e9-4512-4c39-92e8-1a824d7a93e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CddSoAdUpperLayerHandleId

- **UUID**: `dc627d77-4dd6-4606-be1c-38e1b70a8709`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

####### ENUMERATION 类型参数

######## 1. CddPduRApiType

- **UUID**: `0b4469cf-4971-4e98-8441-4a75b49e5506`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddSoAdUpperLayerPduRef

- **UUID**: `710afe0b-bee3-4da7-a62b-949982842796`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 18. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `7939631b-94a4-4613-aa26-12427365c119`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CddSoAdUpperLayerHandleId

- **UUID**: `437bf1b9-c2b0-437b-b400-57daadf5d602`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

####### ENUMERATION 类型参数

######## 1. CddPduRApiType

- **UUID**: `18946c4c-496d-4cf5-95af-9dfad997219c`
- **参数名**: `CddPduRApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter configures the type of the CDD interface (IF/TP)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddSoAdUpperLayerPduRef

- **UUID**: `10a90951-9028-4ccb-b797-a428aa638aa5`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 19. CddEcucPartitionInteraction

**容器属性**:

- **UUID**: `adf96491-768a-4054-b950-4b32fc8f3a0e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddEcucPartitionInteraction`
- **多重性**: [0..0]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This optional container holds the partition interaction configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. CddPartitionStoppedFunctionName

- **UUID**: `55729a45-4f45-481e-8e2b-f79cc2b657ff`
- **参数名**: `CddPartitionStoppedFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Function name to be called when the partition which is triggering the complex driver is stopped.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddEcucPartitionRef

- **UUID**: `1aa0842a-a59e-4523-bf49-0b35b0bcbfa0`
- **引用名**: `CddEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the "EcucPartition" which executes the software which triggers the CDD.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Cdd_AsrCdd

- **UUID**: `cb31de97-0864-496a-bc38-e2c46a4f8b62`
- **包名称**: `Cdd_AsrCdd`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Cdd_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Cdd**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Cdd_Pre**
2. **Cdd_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Cdd_Impl

- **UUID**: `1b146ab9-a82a-4198-bb4a-ec3546768fc2`
- **实现名称**: `Cdd_Impl`
- **编程语言**: C
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Cdd_Pre

- **UUID**: `294ccb9a-0d35-41ff-aa35-ce0df33bc24c`
- **配置名称**: `Cdd_Pre`
- **定义引用**: `/MICROSAR/Cdd_AsrCdd/Cdd`

### 2. Cdd_Rec

- **UUID**: `568092ac-662d-490f-85c5-08e7d920374c`
- **配置名称**: `Cdd_Rec`
- **定义引用**: `/MICROSAR/Cdd_AsrCdd/Cdd`
