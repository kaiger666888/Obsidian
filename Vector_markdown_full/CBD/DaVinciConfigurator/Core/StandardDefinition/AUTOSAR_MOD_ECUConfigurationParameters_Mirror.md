# Mirror - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:28

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Mirror](#mirror)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Mirror

#### 基本信息

- **UUID**: `ECUC:11d28e20-e294-45b9-9e29-2341ad61f58a`
- **模块名称**: `Mirror`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Bus Mirroring module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **23** 个配置容器：

##### 1. MirrorConfigSet

**容器属性**:

- **UUID**: `ECUC:539657fe-e286-4613-9b8d-fdd230ebcbc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorConfigSet`
- **多重性**: [1..1]

**容器描述**:

Contains the configuration parameters and sub containers of the Bus Mirroring module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorInitialDestNetworkRef

- **UUID**: `ECUC:af918ef0-c362-40d1-8e64-62a94cdbb357`
- **引用名**: `MirrorInitialDestNetworkRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MirrorDestNetwork`
- **完整路径**: `/AUTOSAR/EcucDefs/Mirror/MirrorConfigSet/MirrorDestNetwork`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the destination bus that is selected after initialization of the Bus Mirroring module.

###### 配置容器

本模块包含 **21** 个配置容器：

####### 1. MirrorDestNetworkCan

**容器属性**:

- **UUID**: `ECUC:73a13c4f-a479-4098-8553-5bbbe16d4d15`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkCan`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a CAN network.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestQueueSize

- **UUID**: `ECUC:18eb842b-8c78-8411-2ab1-04cfacbd65da`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

########## 2. MirrorNetworkId

- **UUID**: `ECUC:bf924085-73d8-856c-124e-6f6b4836ea34`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

########## 3. MirrorStatusCanId

- **UUID**: `ECUC:b8c713ec-706d-4817-9bd3-b50ba4e07abe`
- **参数名**: `MirrorStatusCanId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID of the CAN status frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:f75be2f1-37db-8592-15f0-0db3e03f5c18`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorDestPduId

- **UUID**: `ECUC:d1426d3b-dab1-d3c4-ca39-18ce6b944508`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

########### BOOLEAN 类型参数

############ 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:a47c238f-3b2c-d5f1-cd8b-b166349b1d47`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. MirrorDestPduRef

- **UUID**: `ECUC:6bd3dfb5-d58b-d579-be9d-4a8443545e14`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 2. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:d1426d3b-dab1-d3c4-ca39-18ce6b944508`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:a47c238f-3b2c-d5f1-cd8b-b166349b1d47`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:6bd3dfb5-d58b-d579-be9d-4a8443545e14`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 3. MirrorDestNetworkCdd

**容器属性**:

- **UUID**: `ECUC:995ee602-9605-4818-8401-6f5a175ff541`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkCdd`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a user defined network.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestQueueSize

- **UUID**: `ECUC:3ea92dde-7e04-8b91-295f-186de2b00e06`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

########## 2. MirrorNetworkId

- **UUID**: `ECUC:e54fea38-6564-8cec-10fc-83097e299260`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######### FLOAT 类型参数

########## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:51136aab-3bdd-97cd-31f5-1e367be2483b`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:1d198ca4-2967-8d12-149e-215216320444`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorDestPduId

- **UUID**: `ECUC:f70016ee-cc3d-db44-c8e7-2c6ca186ed34`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

########### BOOLEAN 类型参数

############ 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:ca39cd42-2cb8-dd71-cc39-c5046a8dc573`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. MirrorDestPduRef

- **UUID**: `ECUC:91918968-c717-dcf9-bd4b-5e2279470640`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 4. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:f70016ee-cc3d-db44-c8e7-2c6ca186ed34`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:ca39cd42-2cb8-dd71-cc39-c5046a8dc573`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:91918968-c717-dcf9-bd4b-5e2279470640`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 5. MirrorDestNetworkFlexRay

**容器属性**:

- **UUID**: `ECUC:9e7671d5-6db7-425a-9d34-ea1fcb1f1d97`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkFlexRay`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a FlexRay network.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestQueueSize

- **UUID**: `ECUC:43c0b9b1-55b6-85d3-4292-9333966f365c`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

########## 2. MirrorNetworkId

- **UUID**: `ECUC:ea67760b-3d16-872e-2a2f-fdcf31e8bab6`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######### FLOAT 类型参数

########## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:562af67e-138f-920f-4b28-98fc2fa17091`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:22311877-0119-8754-2dd1-9c17c9f12c9a`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorDestPduId

- **UUID**: `ECUC:fc17a2c1-a3ef-d586-e21a-a7325546158a`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

########### BOOLEAN 类型参数

############ 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:cf515915-046a-d7b3-e56d-3fca1e4cedc9`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. MirrorDestPduRef

- **UUID**: `ECUC:96a9153b-9ec9-d73b-d67e-d8e82d062e96`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 6. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:fc17a2c1-a3ef-d586-e21a-a7325546158a`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:cf515915-046a-d7b3-e56d-3fca1e4cedc9`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:96a9153b-9ec9-d73b-d67e-d8e82d062e96`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 7. MirrorDestNetworkIp

**容器属性**:

- **UUID**: `ECUC:169bda70-2964-43c5-8fc0-69ffdcdf8504`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkIp`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing an IP network.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestQueueSize

- **UUID**: `ECUC:bbe6224c-1163-873e-351e-1313a82f9dc9`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

########## 2. MirrorNetworkId

- **UUID**: `ECUC:628cdea5-f8c3-8899-1cbb-7daf43a92223`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######### FLOAT 类型参数

########## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:ce505f18-cf3c-937a-3db4-18dc4161d7fe`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:9a568111-bcc6-88bf-205d-1bf7dbb19407`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorDestPduId

- **UUID**: `ECUC:743d0b5c-5f9c-d6f1-d4a6-271267067cf7`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

########### BOOLEAN 类型参数

############ 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:4776c1af-c017-d91e-d7f8-bfaa300d5536`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. MirrorDestPduRef

- **UUID**: `ECUC:0ece7dd6-5a76-d8a6-c90a-58c83ec69603`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 8. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:743d0b5c-5f9c-d6f1-d4a6-271267067cf7`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:4776c1af-c017-d91e-d7f8-bfaa300d5536`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:0ece7dd6-5a76-d8a6-c90a-58c83ec69603`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

####### 9. MirrorSourceNetworkCan

**容器属性**:

- **UUID**: `ECUC:bf1ac273-1d6f-4867-9b2e-bf8780539a8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkCan`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a CAN network.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorNetworkId

- **UUID**: `ECUC:0b0bc6a8-ecce-8d3b-2829-d336e71d37ad`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

########## 2. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:41d815f5-4dcf-916a-5261-828c1cb3bc0f`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:42d56914-b0d1-8d61-2bcb-717f7f25a991`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. MirrorSourceCanMaskBasedIdMapping

**容器属性**:

- **UUID**: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanMaskBasedIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a set of CAN IDs.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceCanMaskBasedIdMappingDestBaseId

- **UUID**: `ECUC:7391b334-bdb0-4493-9141-d4dd26195fb7`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingDestBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the masked parts of the original CAN ID to form the mapped CAN ID.

############ 2. MirrorSourceCanMaskBasedIdMappingSourceCanIdCode

- **UUID**: `ECUC:938935ec-a55f-4e62-ad99-c0a29b00f872`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked original CAN IDs.

############ 3. MirrorSourceCanMaskBasedIdMappingSourceCanIdMask

- **UUID**: `ECUC:e18a0a8e-8442-41be-8d49-0b5d66536e75`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to original CAN IDs before comparison.

######### 2. MirrorSourceCanSingleIdMapping

**容器属性**:

- **UUID**: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanSingleIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a single CAN ID.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceCanSingleIdMappingDestCanId

- **UUID**: `ECUC:55d4d638-ab55-49e4-a179-fb1ced20e29d`
- **参数名**: `MirrorSourceCanSingleIdMappingDestCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mapped CAN ID.

############ 2. MirrorSourceCanSingleIdMappingSourceCanId

- **UUID**: `ECUC:39bebd46-42f9-4e15-b381-b74887402fc6`
- **参数名**: `MirrorSourceCanSingleIdMappingSourceCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Original CAN ID.

######### 3. MirrorSourceCanFilter

**容器属性**:

- **UUID**: `ECUC:243df727-33a7-4094-bd61-f06dab1b20fc`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceCanFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for CAN frames.

####### 10. MirrorSourceCanMaskBasedIdMapping

**容器属性**:

- **UUID**: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanMaskBasedIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a set of CAN IDs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceCanMaskBasedIdMappingDestBaseId

- **UUID**: `ECUC:7391b334-bdb0-4493-9141-d4dd26195fb7`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingDestBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the masked parts of the original CAN ID to form the mapped CAN ID.

########## 2. MirrorSourceCanMaskBasedIdMappingSourceCanIdCode

- **UUID**: `ECUC:938935ec-a55f-4e62-ad99-c0a29b00f872`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked original CAN IDs.

########## 3. MirrorSourceCanMaskBasedIdMappingSourceCanIdMask

- **UUID**: `ECUC:e18a0a8e-8442-41be-8d49-0b5d66536e75`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to original CAN IDs before comparison.

####### 11. MirrorSourceCanSingleIdMapping

**容器属性**:

- **UUID**: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanSingleIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a single CAN ID.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceCanSingleIdMappingDestCanId

- **UUID**: `ECUC:55d4d638-ab55-49e4-a179-fb1ced20e29d`
- **参数名**: `MirrorSourceCanSingleIdMappingDestCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mapped CAN ID.

########## 2. MirrorSourceCanSingleIdMappingSourceCanId

- **UUID**: `ECUC:39bebd46-42f9-4e15-b381-b74887402fc6`
- **参数名**: `MirrorSourceCanSingleIdMappingSourceCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Original CAN ID.

####### 12. MirrorSourceNetworkFlexRay

**容器属性**:

- **UUID**: `ECUC:196f4efb-a4ac-42f6-a993-c2896eca9138`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkFlexRay`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a FlexRay network.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorNetworkId

- **UUID**: `ECUC:65605331-740b-87ca-368e-d638d5942e57`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

########## 2. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:9c2ca27d-d50c-8bf9-60c6-858e0b2ab2b9`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:9d29f59d-380e-87f0-3a30-74816d9ca03b`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MirrorSourceFlexRayFilter

**容器属性**:

- **UUID**: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceFlexRayFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for FlexRay frames.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceFlexRayFilterCycleRepetition

- **UUID**: `ECUC:11138f7c-791a-4ca8-b659-5a819bff190d`
- **参数名**: `MirrorSourceFlexRayFilterCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle repetition of accepted cycles.

############ 2. MirrorSourceFlexRayFilterId

- **UUID**: `ECUC:d3bcc935-43d4-42ca-a380-201741468604`
- **参数名**: `MirrorSourceFlexRayFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured FlexRay filter.

############ 3. MirrorSourceFlexRayFilterLowerBaseCycle

- **UUID**: `ECUC:2bbaf964-4218-4bb3-b3b5-2fd1b99e98f5`
- **参数名**: `MirrorSourceFlexRayFilterLowerBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest base cycle number that is accepted by the filter.

############ 4. MirrorSourceFlexRayFilterLowerSlot

- **UUID**: `ECUC:269170cd-0a7a-4729-b22e-8aa4ab5498a6`
- **参数名**: `MirrorSourceFlexRayFilterLowerSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest slot ID that is accepted by the filter.

############ 5. MirrorSourceFlexRayFilterUpperBaseCycle

- **UUID**: `ECUC:40339b2b-3707-4eb3-a057-8d3676fb8929`
- **参数名**: `MirrorSourceFlexRayFilterUpperBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest base cycle number that is accepted by the filter.

############ 6. MirrorSourceFlexRayFilterUpperSlot

- **UUID**: `ECUC:95005864-50a0-4544-ab8f-ea42e18faa50`
- **参数名**: `MirrorSourceFlexRayFilterUpperSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest slot ID that is accepted by the filter.

########### ENUMERATION 类型参数

############ 1. MirrorSourceFlexRayFilterChannelAssignment

- **UUID**: `ECUC:5f9b1c34-eed6-48c2-9389-dbf9edb5cb23`
- **参数名**: `MirrorSourceFlexRayFilterChannelAssignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MIRROR_FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **描述**: FlexRay channels accepted by the filter.

####### 13. MirrorSourceFlexRayFilter

**容器属性**:

- **UUID**: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceFlexRayFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for FlexRay frames.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceFlexRayFilterCycleRepetition

- **UUID**: `ECUC:11138f7c-791a-4ca8-b659-5a819bff190d`
- **参数名**: `MirrorSourceFlexRayFilterCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle repetition of accepted cycles.

########## 2. MirrorSourceFlexRayFilterId

- **UUID**: `ECUC:d3bcc935-43d4-42ca-a380-201741468604`
- **参数名**: `MirrorSourceFlexRayFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured FlexRay filter.

########## 3. MirrorSourceFlexRayFilterLowerBaseCycle

- **UUID**: `ECUC:2bbaf964-4218-4bb3-b3b5-2fd1b99e98f5`
- **参数名**: `MirrorSourceFlexRayFilterLowerBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest base cycle number that is accepted by the filter.

########## 4. MirrorSourceFlexRayFilterLowerSlot

- **UUID**: `ECUC:269170cd-0a7a-4729-b22e-8aa4ab5498a6`
- **参数名**: `MirrorSourceFlexRayFilterLowerSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest slot ID that is accepted by the filter.

########## 5. MirrorSourceFlexRayFilterUpperBaseCycle

- **UUID**: `ECUC:40339b2b-3707-4eb3-a057-8d3676fb8929`
- **参数名**: `MirrorSourceFlexRayFilterUpperBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest base cycle number that is accepted by the filter.

########## 6. MirrorSourceFlexRayFilterUpperSlot

- **UUID**: `ECUC:95005864-50a0-4544-ab8f-ea42e18faa50`
- **参数名**: `MirrorSourceFlexRayFilterUpperSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest slot ID that is accepted by the filter.

######### ENUMERATION 类型参数

########## 1. MirrorSourceFlexRayFilterChannelAssignment

- **UUID**: `ECUC:5f9b1c34-eed6-48c2-9389-dbf9edb5cb23`
- **参数名**: `MirrorSourceFlexRayFilterChannelAssignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MIRROR_FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **描述**: FlexRay channels accepted by the filter.

####### 14. MirrorSourceNetworkLin

**容器属性**:

- **UUID**: `ECUC:7ecfe087-407f-4304-812c-b7883b7ba44e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkLin`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a LIN network.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorNetworkId

- **UUID**: `ECUC:cac0e4bd-0fde-87d8-0e27-cb37a245416d`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

########## 2. MirrorSourceLinToCanBaseId

- **UUID**: `ECUC:70e5b399-e99f-4694-9ca2-bc953ecccef1`
- **参数名**: `MirrorSourceLinToCanBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the LIN frame ID to form the CAN ID.

########## 3. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:018d3409-70df-8c07-385f-7a8cd7dbc5cf`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:028a8728-d3e1-87fe-11c9-69803a4db351`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. MirrorSourceLinFilterMask

**容器属性**:

- **UUID**: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterMask`
- **多重性**: [0..1]

**容器描述**:

Pre-configured mask based filter for LIN frames.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:ffc2ae14-1e6a-8c1a-58b3-c1dffc17d098`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

############ 2. MirrorSourceLinFilterLinIdCode

- **UUID**: `ECUC:b305c041-c486-4a86-a494-75e49517191b`
- **参数名**: `MirrorSourceLinFilterLinIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked frame IDs.

############ 3. MirrorSourceLinFilterLinIdMask

- **UUID**: `ECUC:4dbe5a5d-fbaa-42a5-b5a7-3f7a6c446928`
- **参数名**: `MirrorSourceLinFilterLinIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to frame IDs before comparison.

######### 2. MirrorSourceLinFilterRange

**容器属性**:

- **UUID**: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterRange`
- **多重性**: [0..1]

**容器描述**:

Pre-configured range filter for LIN frames.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:728e83b9-d958-89d3-479a-3aac2eb049b4`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

############ 2. MirrorSourceLinFilterLower

- **UUID**: `ECUC:1fcabbf5-226b-4547-9a81-b6a6f5542334`
- **参数名**: `MirrorSourceLinFilterLower`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest frame ID that is accepted by the filter.

############ 3. MirrorSourceLinFilterUpper

- **UUID**: `ECUC:b80946d1-0525-4872-8fd3-ea8e33b8166f`
- **参数名**: `MirrorSourceLinFilterUpper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest frame ID that is accepted by the filter.

######### 3. MirrorSourceLinToCanIdMapping

**容器属性**:

- **UUID**: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinToCanIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for mapping a LIN frame ID to a special CAN ID.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. MirrorSourceLinToCanIdMappingCanId

- **UUID**: `ECUC:2e88518b-16c9-4955-95f9-63a784f9040a`
- **参数名**: `MirrorSourceLinToCanIdMappingCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID which lies outside of the range mapping.

############ 2. MirrorSourceLinToCanIdMappingLinId

- **UUID**: `ECUC:cb40fca3-ffa0-4d97-b60f-907223d8665e`
- **参数名**: `MirrorSourceLinToCanIdMappingLinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Frame ID which is excluded from the range mapping.

######### 4. MirrorSourceLinFilter

**容器属性**:

- **UUID**: `ECUC:1e4417bb-57d9-4580-a315-b7e73366ec73`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceLinFilter`
- **多重性**: [0..255]

**容器选择**:

- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.

**容器描述**:

Pre-configured filter for LIN frames.

####### 15. MirrorSourceLinFilterMask

**容器属性**:

- **UUID**: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterMask`
- **多重性**: [0..1]

**容器描述**:

Pre-configured mask based filter for LIN frames.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:ffc2ae14-1e6a-8c1a-58b3-c1dffc17d098`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

########## 2. MirrorSourceLinFilterLinIdCode

- **UUID**: `ECUC:b305c041-c486-4a86-a494-75e49517191b`
- **参数名**: `MirrorSourceLinFilterLinIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked frame IDs.

########## 3. MirrorSourceLinFilterLinIdMask

- **UUID**: `ECUC:4dbe5a5d-fbaa-42a5-b5a7-3f7a6c446928`
- **参数名**: `MirrorSourceLinFilterLinIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to frame IDs before comparison.

####### 16. MirrorSourceLinFilterRange

**容器属性**:

- **UUID**: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterRange`
- **多重性**: [0..1]

**容器描述**:

Pre-configured range filter for LIN frames.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:728e83b9-d958-89d3-479a-3aac2eb049b4`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

########## 2. MirrorSourceLinFilterLower

- **UUID**: `ECUC:1fcabbf5-226b-4547-9a81-b6a6f5542334`
- **参数名**: `MirrorSourceLinFilterLower`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest frame ID that is accepted by the filter.

########## 3. MirrorSourceLinFilterUpper

- **UUID**: `ECUC:b80946d1-0525-4872-8fd3-ea8e33b8166f`
- **参数名**: `MirrorSourceLinFilterUpper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest frame ID that is accepted by the filter.

####### 17. MirrorSourceLinToCanIdMapping

**容器属性**:

- **UUID**: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinToCanIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for mapping a LIN frame ID to a special CAN ID.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinToCanIdMappingCanId

- **UUID**: `ECUC:2e88518b-16c9-4955-95f9-63a784f9040a`
- **参数名**: `MirrorSourceLinToCanIdMappingCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID which lies outside of the range mapping.

########## 2. MirrorSourceLinToCanIdMappingLinId

- **UUID**: `ECUC:cb40fca3-ffa0-4d97-b60f-907223d8665e`
- **参数名**: `MirrorSourceLinToCanIdMappingLinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Frame ID which is excluded from the range mapping.

####### 18. MirrorDestNetwork

**容器属性**:

- **UUID**: `ECUC:67c6fc95-b52e-4e51-a575-1ba2ddde4392`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorDestNetwork`
- **多重性**: [1..infinite]

**容器选择**:

- **MirrorDestNetworkCan**
  - UUID: `ECUC:73a13c4f-a479-4098-8553-5bbbe16d4d15`
  - 描述: Destination bus representing a CAN network.
- **MirrorDestPdu**
  - UUID: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkCdd**
  - UUID: `ECUC:995ee602-9605-4818-8401-6f5a175ff541`
  - 描述: Destination bus representing a user defined network.
- **MirrorDestPdu**
  - UUID: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkFlexRay**
  - UUID: `ECUC:9e7671d5-6db7-425a-9d34-ea1fcb1f1d97`
  - 描述: Destination bus representing a FlexRay network.
- **MirrorDestPdu**
  - UUID: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkIp**
  - UUID: `ECUC:169bda70-2964-43c5-8fc0-69ffdcdf8504`
  - 描述: Destination bus representing an IP network.
- **MirrorDestPdu**
  - UUID: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.

**容器描述**:

Destination bus to which frames are sent by the Bus Mirroring module.

####### 19. MirrorSourceNetwork

**容器属性**:

- **UUID**: `ECUC:934898d0-3ed1-4649-9e6f-19077c1b9e7d`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceNetwork`
- **多重性**: [1..infinite]

**容器选择**:

- **MirrorSourceNetworkCan**
  - UUID: `ECUC:bf1ac273-1d6f-4867-9b2e-bf8780539a8e`
  - 描述: Source bus representing a CAN network.
- **MirrorSourceCanMaskBasedIdMapping**
  - UUID: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
  - 描述: Rule for remapping a set of CAN IDs.
- **MirrorSourceCanSingleIdMapping**
  - UUID: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
  - 描述: Rule for remapping a single CAN ID.
- **MirrorSourceNetworkFlexRay**
  - UUID: `ECUC:196f4efb-a4ac-42f6-a993-c2896eca9138`
  - 描述: Source bus representing a FlexRay network.
- **MirrorSourceFlexRayFilter**
  - UUID: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
  - 描述: Pre-configured filter for FlexRay frames.
- **MirrorSourceNetworkLin**
  - UUID: `ECUC:7ecfe087-407f-4304-812c-b7883b7ba44e`
  - 描述: Source bus representing a LIN network.
- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.
- **MirrorSourceLinToCanIdMapping**
  - UUID: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
  - 描述: Rule for mapping a LIN frame ID to a special CAN ID.

**容器描述**:

Source bus from which frames are received by the Bus Mirroring module.

####### 20. MirrorSourceCanFilter

**容器属性**:

- **UUID**: `ECUC:243df727-33a7-4094-bd61-f06dab1b20fc`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceCanFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for CAN frames.

####### 21. MirrorSourceLinFilter

**容器属性**:

- **UUID**: `ECUC:1e4417bb-57d9-4580-a315-b7e73366ec73`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceLinFilter`
- **多重性**: [0..255]

**容器选择**:

- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.

**容器描述**:

Pre-configured filter for LIN frames.

##### 2. MirrorDestNetworkCan

**容器属性**:

- **UUID**: `ECUC:73a13c4f-a479-4098-8553-5bbbe16d4d15`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkCan`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a CAN network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestQueueSize

- **UUID**: `ECUC:18eb842b-8c78-8411-2ab1-04cfacbd65da`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

######## 2. MirrorNetworkId

- **UUID**: `ECUC:bf924085-73d8-856c-124e-6f6b4836ea34`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######## 3. MirrorStatusCanId

- **UUID**: `ECUC:b8c713ec-706d-4817-9bd3-b50ba4e07abe`
- **参数名**: `MirrorStatusCanId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID of the CAN status frame.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:f75be2f1-37db-8592-15f0-0db3e03f5c18`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:d1426d3b-dab1-d3c4-ca39-18ce6b944508`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:a47c238f-3b2c-d5f1-cd8b-b166349b1d47`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:6bd3dfb5-d58b-d579-be9d-4a8443545e14`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 3. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestPduId

- **UUID**: `ECUC:d1426d3b-dab1-d3c4-ca39-18ce6b944508`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

####### BOOLEAN 类型参数

######## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:a47c238f-3b2c-d5f1-cd8b-b166349b1d47`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorDestPduRef

- **UUID**: `ECUC:6bd3dfb5-d58b-d579-be9d-4a8443545e14`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 4. MirrorDestNetworkCdd

**容器属性**:

- **UUID**: `ECUC:995ee602-9605-4818-8401-6f5a175ff541`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkCdd`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a user defined network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestQueueSize

- **UUID**: `ECUC:3ea92dde-7e04-8b91-295f-186de2b00e06`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

######## 2. MirrorNetworkId

- **UUID**: `ECUC:e54fea38-6564-8cec-10fc-83097e299260`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

####### FLOAT 类型参数

######## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:51136aab-3bdd-97cd-31f5-1e367be2483b`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:1d198ca4-2967-8d12-149e-215216320444`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:f70016ee-cc3d-db44-c8e7-2c6ca186ed34`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:ca39cd42-2cb8-dd71-cc39-c5046a8dc573`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:91918968-c717-dcf9-bd4b-5e2279470640`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 5. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestPduId

- **UUID**: `ECUC:f70016ee-cc3d-db44-c8e7-2c6ca186ed34`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

####### BOOLEAN 类型参数

######## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:ca39cd42-2cb8-dd71-cc39-c5046a8dc573`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorDestPduRef

- **UUID**: `ECUC:91918968-c717-dcf9-bd4b-5e2279470640`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 6. MirrorDestNetworkFlexRay

**容器属性**:

- **UUID**: `ECUC:9e7671d5-6db7-425a-9d34-ea1fcb1f1d97`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkFlexRay`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing a FlexRay network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestQueueSize

- **UUID**: `ECUC:43c0b9b1-55b6-85d3-4292-9333966f365c`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

######## 2. MirrorNetworkId

- **UUID**: `ECUC:ea67760b-3d16-872e-2a2f-fdcf31e8bab6`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

####### FLOAT 类型参数

######## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:562af67e-138f-920f-4b28-98fc2fa17091`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:22311877-0119-8754-2dd1-9c17c9f12c9a`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:fc17a2c1-a3ef-d586-e21a-a7325546158a`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:cf515915-046a-d7b3-e56d-3fca1e4cedc9`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:96a9153b-9ec9-d73b-d67e-d8e82d062e96`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 7. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestPduId

- **UUID**: `ECUC:fc17a2c1-a3ef-d586-e21a-a7325546158a`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

####### BOOLEAN 类型参数

######## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:cf515915-046a-d7b3-e56d-3fca1e4cedc9`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorDestPduRef

- **UUID**: `ECUC:96a9153b-9ec9-d73b-d67e-d8e82d062e96`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 8. MirrorDestNetworkIp

**容器属性**:

- **UUID**: `ECUC:169bda70-2964-43c5-8fc0-69ffdcdf8504`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestNetworkIp`
- **多重性**: [0..1]

**容器描述**:

Destination bus representing an IP network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestQueueSize

- **UUID**: `ECUC:bbe6224c-1163-873e-351e-1313a82f9dc9`
- **参数名**: `MirrorDestQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of frames that can be stored in the output queue for the destination bus.

######## 2. MirrorNetworkId

- **UUID**: `ECUC:628cdea5-f8c3-8899-1cbb-7daf43a92223`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

####### FLOAT 类型参数

######## 1. MirrorDestTransmissionDeadline

- **UUID**: `ECUC:ce505f18-cf3c-937a-3db4-18dc4161d7fe`
- **参数名**: `MirrorDestTransmissionDeadline`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..0.655]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Time in seconds after which the collection of source frames into the destination frame stopped and  the frame is sent at the latest.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:9a568111-bcc6-88bf-205d-1bf7dbb19407`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorDestPduId

- **UUID**: `ECUC:743d0b5c-5f9c-d6f1-d4a6-271267067cf7`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

######### BOOLEAN 类型参数

########## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:4776c1af-c017-d91e-d7f8-bfaa300d5536`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MirrorDestPduRef

- **UUID**: `ECUC:0ece7dd6-5a76-d8a6-c90a-58c83ec69603`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 9. MirrorDestPdu

**容器属性**:

- **UUID**: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorDestPdu`
- **多重性**: [1..infinite]

**容器描述**:

I-PDU used for transmission of the mirrored frames on the destination bus.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorDestPduId

- **UUID**: `ECUC:743d0b5c-5f9c-d6f1-d4a6-271267067cf7`
- **参数名**: `MirrorDestPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: I-PDU identifier used for TxConfirmation from PduR.

####### BOOLEAN 类型参数

######## 1. MirrorDestPduUsesTriggerTransmit

- **UUID**: `ECUC:4776c1af-c017-d91e-d7f8-bfaa300d5536`
- **参数名**: `MirrorDestPduUsesTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches transmission via TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorDestPduRef

- **UUID**: `ECUC:0ece7dd6-5a76-d8a6-c90a-58c83ec69603`
- **引用名**: `MirrorDestPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Pdu object representing the I-PDU.

##### 10. MirrorSourceNetworkCan

**容器属性**:

- **UUID**: `ECUC:bf1ac273-1d6f-4867-9b2e-bf8780539a8e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkCan`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a CAN network.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorNetworkId

- **UUID**: `ECUC:0b0bc6a8-ecce-8d3b-2829-d336e71d37ad`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######## 2. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:41d815f5-4dcf-916a-5261-828c1cb3bc0f`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:42d56914-b0d1-8d61-2bcb-717f7f25a991`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. MirrorSourceCanMaskBasedIdMapping

**容器属性**:

- **UUID**: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanMaskBasedIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a set of CAN IDs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceCanMaskBasedIdMappingDestBaseId

- **UUID**: `ECUC:7391b334-bdb0-4493-9141-d4dd26195fb7`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingDestBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the masked parts of the original CAN ID to form the mapped CAN ID.

########## 2. MirrorSourceCanMaskBasedIdMappingSourceCanIdCode

- **UUID**: `ECUC:938935ec-a55f-4e62-ad99-c0a29b00f872`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked original CAN IDs.

########## 3. MirrorSourceCanMaskBasedIdMappingSourceCanIdMask

- **UUID**: `ECUC:e18a0a8e-8442-41be-8d49-0b5d66536e75`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to original CAN IDs before comparison.

####### 2. MirrorSourceCanSingleIdMapping

**容器属性**:

- **UUID**: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanSingleIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a single CAN ID.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceCanSingleIdMappingDestCanId

- **UUID**: `ECUC:55d4d638-ab55-49e4-a179-fb1ced20e29d`
- **参数名**: `MirrorSourceCanSingleIdMappingDestCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mapped CAN ID.

########## 2. MirrorSourceCanSingleIdMappingSourceCanId

- **UUID**: `ECUC:39bebd46-42f9-4e15-b381-b74887402fc6`
- **参数名**: `MirrorSourceCanSingleIdMappingSourceCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Original CAN ID.

####### 3. MirrorSourceCanFilter

**容器属性**:

- **UUID**: `ECUC:243df727-33a7-4094-bd61-f06dab1b20fc`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceCanFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for CAN frames.

##### 11. MirrorSourceCanMaskBasedIdMapping

**容器属性**:

- **UUID**: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanMaskBasedIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a set of CAN IDs.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceCanMaskBasedIdMappingDestBaseId

- **UUID**: `ECUC:7391b334-bdb0-4493-9141-d4dd26195fb7`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingDestBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the masked parts of the original CAN ID to form the mapped CAN ID.

######## 2. MirrorSourceCanMaskBasedIdMappingSourceCanIdCode

- **UUID**: `ECUC:938935ec-a55f-4e62-ad99-c0a29b00f872`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked original CAN IDs.

######## 3. MirrorSourceCanMaskBasedIdMappingSourceCanIdMask

- **UUID**: `ECUC:e18a0a8e-8442-41be-8d49-0b5d66536e75`
- **参数名**: `MirrorSourceCanMaskBasedIdMappingSourceCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to original CAN IDs before comparison.

##### 12. MirrorSourceCanSingleIdMapping

**容器属性**:

- **UUID**: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceCanSingleIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for remapping a single CAN ID.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceCanSingleIdMappingDestCanId

- **UUID**: `ECUC:55d4d638-ab55-49e4-a179-fb1ced20e29d`
- **参数名**: `MirrorSourceCanSingleIdMappingDestCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mapped CAN ID.

######## 2. MirrorSourceCanSingleIdMappingSourceCanId

- **UUID**: `ECUC:39bebd46-42f9-4e15-b381-b74887402fc6`
- **参数名**: `MirrorSourceCanSingleIdMappingSourceCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Original CAN ID.

##### 13. MirrorSourceNetworkFlexRay

**容器属性**:

- **UUID**: `ECUC:196f4efb-a4ac-42f6-a993-c2896eca9138`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkFlexRay`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a FlexRay network.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorNetworkId

- **UUID**: `ECUC:65605331-740b-87ca-368e-d638d5942e57`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######## 2. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:9c2ca27d-d50c-8bf9-60c6-858e0b2ab2b9`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:9d29f59d-380e-87f0-3a30-74816d9ca03b`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MirrorSourceFlexRayFilter

**容器属性**:

- **UUID**: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceFlexRayFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for FlexRay frames.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceFlexRayFilterCycleRepetition

- **UUID**: `ECUC:11138f7c-791a-4ca8-b659-5a819bff190d`
- **参数名**: `MirrorSourceFlexRayFilterCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle repetition of accepted cycles.

########## 2. MirrorSourceFlexRayFilterId

- **UUID**: `ECUC:d3bcc935-43d4-42ca-a380-201741468604`
- **参数名**: `MirrorSourceFlexRayFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured FlexRay filter.

########## 3. MirrorSourceFlexRayFilterLowerBaseCycle

- **UUID**: `ECUC:2bbaf964-4218-4bb3-b3b5-2fd1b99e98f5`
- **参数名**: `MirrorSourceFlexRayFilterLowerBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest base cycle number that is accepted by the filter.

########## 4. MirrorSourceFlexRayFilterLowerSlot

- **UUID**: `ECUC:269170cd-0a7a-4729-b22e-8aa4ab5498a6`
- **参数名**: `MirrorSourceFlexRayFilterLowerSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest slot ID that is accepted by the filter.

########## 5. MirrorSourceFlexRayFilterUpperBaseCycle

- **UUID**: `ECUC:40339b2b-3707-4eb3-a057-8d3676fb8929`
- **参数名**: `MirrorSourceFlexRayFilterUpperBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest base cycle number that is accepted by the filter.

########## 6. MirrorSourceFlexRayFilterUpperSlot

- **UUID**: `ECUC:95005864-50a0-4544-ab8f-ea42e18faa50`
- **参数名**: `MirrorSourceFlexRayFilterUpperSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest slot ID that is accepted by the filter.

######### ENUMERATION 类型参数

########## 1. MirrorSourceFlexRayFilterChannelAssignment

- **UUID**: `ECUC:5f9b1c34-eed6-48c2-9389-dbf9edb5cb23`
- **参数名**: `MirrorSourceFlexRayFilterChannelAssignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MIRROR_FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **描述**: FlexRay channels accepted by the filter.

##### 14. MirrorSourceFlexRayFilter

**容器属性**:

- **UUID**: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceFlexRayFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for FlexRay frames.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceFlexRayFilterCycleRepetition

- **UUID**: `ECUC:11138f7c-791a-4ca8-b659-5a819bff190d`
- **参数名**: `MirrorSourceFlexRayFilterCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Cycle repetition of accepted cycles.

######## 2. MirrorSourceFlexRayFilterId

- **UUID**: `ECUC:d3bcc935-43d4-42ca-a380-201741468604`
- **参数名**: `MirrorSourceFlexRayFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured FlexRay filter.

######## 3. MirrorSourceFlexRayFilterLowerBaseCycle

- **UUID**: `ECUC:2bbaf964-4218-4bb3-b3b5-2fd1b99e98f5`
- **参数名**: `MirrorSourceFlexRayFilterLowerBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest base cycle number that is accepted by the filter.

######## 4. MirrorSourceFlexRayFilterLowerSlot

- **UUID**: `ECUC:269170cd-0a7a-4729-b22e-8aa4ab5498a6`
- **参数名**: `MirrorSourceFlexRayFilterLowerSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest slot ID that is accepted by the filter.

######## 5. MirrorSourceFlexRayFilterUpperBaseCycle

- **UUID**: `ECUC:40339b2b-3707-4eb3-a057-8d3676fb8929`
- **参数名**: `MirrorSourceFlexRayFilterUpperBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest base cycle number that is accepted by the filter.

######## 6. MirrorSourceFlexRayFilterUpperSlot

- **UUID**: `ECUC:95005864-50a0-4544-ab8f-ea42e18faa50`
- **参数名**: `MirrorSourceFlexRayFilterUpperSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest slot ID that is accepted by the filter.

####### ENUMERATION 类型参数

######## 1. MirrorSourceFlexRayFilterChannelAssignment

- **UUID**: `ECUC:5f9b1c34-eed6-48c2-9389-dbf9edb5cb23`
- **参数名**: `MirrorSourceFlexRayFilterChannelAssignment`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `MIRROR_FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `MIRROR_FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **描述**: FlexRay channels accepted by the filter.

##### 15. MirrorSourceNetworkLin

**容器属性**:

- **UUID**: `ECUC:7ecfe087-407f-4304-812c-b7883b7ba44e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceNetworkLin`
- **多重性**: [0..1]

**容器描述**:

Source bus representing a LIN network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorNetworkId

- **UUID**: `ECUC:cac0e4bd-0fde-87d8-0e27-cb37a245416d`
- **参数名**: `MirrorNetworkId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Network ID of the bus.

######## 2. MirrorSourceLinToCanBaseId

- **UUID**: `ECUC:70e5b399-e99f-4694-9ca2-bc953ecccef1`
- **参数名**: `MirrorSourceLinToCanBaseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Base ID merged with the LIN frame ID to form the CAN ID.

######## 3. MirrorSourceMaxDynamicFilters

- **UUID**: `ECUC:018d3409-70df-8c07-385f-7a8cd7dbc5cf`
- **参数名**: `MirrorSourceMaxDynamicFilters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorComMNetworkHandleRef

- **UUID**: `ECUC:028a8728-d3e1-87fe-11c9-69803a4db351`
- **引用名**: `MirrorComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ComMChannel that represents the bus.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. MirrorSourceLinFilterMask

**容器属性**:

- **UUID**: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterMask`
- **多重性**: [0..1]

**容器描述**:

Pre-configured mask based filter for LIN frames.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:ffc2ae14-1e6a-8c1a-58b3-c1dffc17d098`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

########## 2. MirrorSourceLinFilterLinIdCode

- **UUID**: `ECUC:b305c041-c486-4a86-a494-75e49517191b`
- **参数名**: `MirrorSourceLinFilterLinIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked frame IDs.

########## 3. MirrorSourceLinFilterLinIdMask

- **UUID**: `ECUC:4dbe5a5d-fbaa-42a5-b5a7-3f7a6c446928`
- **参数名**: `MirrorSourceLinFilterLinIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to frame IDs before comparison.

####### 2. MirrorSourceLinFilterRange

**容器属性**:

- **UUID**: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterRange`
- **多重性**: [0..1]

**容器描述**:

Pre-configured range filter for LIN frames.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:728e83b9-d958-89d3-479a-3aac2eb049b4`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

########## 2. MirrorSourceLinFilterLower

- **UUID**: `ECUC:1fcabbf5-226b-4547-9a81-b6a6f5542334`
- **参数名**: `MirrorSourceLinFilterLower`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest frame ID that is accepted by the filter.

########## 3. MirrorSourceLinFilterUpper

- **UUID**: `ECUC:b80946d1-0525-4872-8fd3-ea8e33b8166f`
- **参数名**: `MirrorSourceLinFilterUpper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest frame ID that is accepted by the filter.

####### 3. MirrorSourceLinToCanIdMapping

**容器属性**:

- **UUID**: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinToCanIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for mapping a LIN frame ID to a special CAN ID.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. MirrorSourceLinToCanIdMappingCanId

- **UUID**: `ECUC:2e88518b-16c9-4955-95f9-63a784f9040a`
- **参数名**: `MirrorSourceLinToCanIdMappingCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID which lies outside of the range mapping.

########## 2. MirrorSourceLinToCanIdMappingLinId

- **UUID**: `ECUC:cb40fca3-ffa0-4d97-b60f-907223d8665e`
- **参数名**: `MirrorSourceLinToCanIdMappingLinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Frame ID which is excluded from the range mapping.

####### 4. MirrorSourceLinFilter

**容器属性**:

- **UUID**: `ECUC:1e4417bb-57d9-4580-a315-b7e73366ec73`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceLinFilter`
- **多重性**: [0..255]

**容器选择**:

- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.

**容器描述**:

Pre-configured filter for LIN frames.

##### 16. MirrorSourceLinFilterMask

**容器属性**:

- **UUID**: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterMask`
- **多重性**: [0..1]

**容器描述**:

Pre-configured mask based filter for LIN frames.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:ffc2ae14-1e6a-8c1a-58b3-c1dffc17d098`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

######## 2. MirrorSourceLinFilterLinIdCode

- **UUID**: `ECUC:b305c041-c486-4a86-a494-75e49517191b`
- **参数名**: `MirrorSourceLinFilterLinIdCode`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value to match masked frame IDs.

######## 3. MirrorSourceLinFilterLinIdMask

- **UUID**: `ECUC:4dbe5a5d-fbaa-42a5-b5a7-3f7a6c446928`
- **参数名**: `MirrorSourceLinFilterLinIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Mask applied to frame IDs before comparison.

##### 17. MirrorSourceLinFilterRange

**容器属性**:

- **UUID**: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinFilterRange`
- **多重性**: [0..1]

**容器描述**:

Pre-configured range filter for LIN frames.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceLinFilterId

- **UUID**: `ECUC:728e83b9-d958-89d3-479a-3aac2eb049b4`
- **参数名**: `MirrorSourceLinFilterId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Unique identifier of the pre-configured LIN filter.

######## 2. MirrorSourceLinFilterLower

- **UUID**: `ECUC:1fcabbf5-226b-4547-9a81-b6a6f5542334`
- **参数名**: `MirrorSourceLinFilterLower`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Lowest frame ID that is accepted by the filter.

######## 3. MirrorSourceLinFilterUpper

- **UUID**: `ECUC:b80946d1-0525-4872-8fd3-ea8e33b8166f`
- **参数名**: `MirrorSourceLinFilterUpper`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Highest frame ID that is accepted by the filter.

##### 18. MirrorSourceLinToCanIdMapping

**容器属性**:

- **UUID**: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorSourceLinToCanIdMapping`
- **多重性**: [0..infinite]

**容器描述**:

Rule for mapping a LIN frame ID to a special CAN ID.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MirrorSourceLinToCanIdMappingCanId

- **UUID**: `ECUC:2e88518b-16c9-4955-95f9-63a784f9040a`
- **参数名**: `MirrorSourceLinToCanIdMappingCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: CAN ID which lies outside of the range mapping.

######## 2. MirrorSourceLinToCanIdMappingLinId

- **UUID**: `ECUC:cb40fca3-ffa0-4d97-b60f-907223d8665e`
- **参数名**: `MirrorSourceLinToCanIdMappingLinId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Frame ID which is excluded from the range mapping.

##### 19. MirrorGeneral

**容器属性**:

- **UUID**: `ECUC:c10221a3-adc7-41bb-9178-2bc6c4a7799a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MirrorGeneral`
- **多重性**: [1..1]

**容器描述**:

Contains the general configuration parameters of the module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. MirrorDevErrorDetect

- **UUID**: `ECUC:90ac8ce3-488c-41d7-b10c-7014a56c1d5d`
- **参数名**: `MirrorDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the development error detection and notification on or off.

######## 2. MirrorVersionInfoApi

- **UUID**: `ECUC:c3dde24c-7869-46ff-bb52-f28ba0afc96e`
- **参数名**: `MirrorVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **描述**: Pre-processor switch for enabling version info API support.

####### FLOAT 类型参数

######## 1. MirrorMainFunctionPeriod

- **UUID**: `ECUC:f3eab8dd-7701-4919-92dd-b676e58d567e`
- **参数名**: `MirrorMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Execution cycle of Mirror_MainFunction() in seconds.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MirrorStbRef

- **UUID**: `ECUC:9495ec19-61fc-4037-ad8c-342a2c402222`
- **引用名**: `MirrorStbRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the StbM time base to use for acquiring the time stamps used in the mirroring protocol.

##### 20. MirrorDestNetwork

**容器属性**:

- **UUID**: `ECUC:67c6fc95-b52e-4e51-a575-1ba2ddde4392`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorDestNetwork`
- **多重性**: [1..infinite]

**容器选择**:

- **MirrorDestNetworkCan**
  - UUID: `ECUC:73a13c4f-a479-4098-8553-5bbbe16d4d15`
  - 描述: Destination bus representing a CAN network.
- **MirrorDestPdu**
  - UUID: `ECUC:b03db011-758a-8c53-1e37-97c17518b8d4`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkCdd**
  - UUID: `ECUC:995ee602-9605-4818-8401-6f5a175ff541`
  - 描述: Destination bus representing a user defined network.
- **MirrorDestPdu**
  - UUID: `ECUC:d5fb59c4-6716-93d3-1ce5-ab5fab0b6100`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkFlexRay**
  - UUID: `ECUC:9e7671d5-6db7-425a-9d34-ea1fcb1f1d97`
  - 描述: Destination bus representing a FlexRay network.
- **MirrorDestPdu**
  - UUID: `ECUC:db12e597-3ec8-8e15-3619-26255eca8956`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.
- **MirrorDestNetworkIp**
  - UUID: `ECUC:169bda70-2964-43c5-8fc0-69ffdcdf8504`
  - 描述: Destination bus representing an IP network.
- **MirrorDestPdu**
  - UUID: `ECUC:53384e31-fa75-8f80-28a4-a605708af0c3`
  - 描述: I-PDU used for transmission of the mirrored frames on the destination bus.

**容器描述**:

Destination bus to which frames are sent by the Bus Mirroring module.

##### 21. MirrorSourceNetwork

**容器属性**:

- **UUID**: `ECUC:934898d0-3ed1-4649-9e6f-19077c1b9e7d`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceNetwork`
- **多重性**: [1..infinite]

**容器选择**:

- **MirrorSourceNetworkCan**
  - UUID: `ECUC:bf1ac273-1d6f-4867-9b2e-bf8780539a8e`
  - 描述: Source bus representing a CAN network.
- **MirrorSourceCanMaskBasedIdMapping**
  - UUID: `ECUC:3bc146bf-1a97-4938-90f7-98950a9bc67e`
  - 描述: Rule for remapping a set of CAN IDs.
- **MirrorSourceCanSingleIdMapping**
  - UUID: `ECUC:c14ac4d4-ffe0-4ac6-8cac-10c9878b0200`
  - 描述: Rule for remapping a single CAN ID.
- **MirrorSourceNetworkFlexRay**
  - UUID: `ECUC:196f4efb-a4ac-42f6-a993-c2896eca9138`
  - 描述: Source bus representing a FlexRay network.
- **MirrorSourceFlexRayFilter**
  - UUID: `ECUC:633f5c26-22ac-4c6c-aab7-3ebfc586b8a9`
  - 描述: Pre-configured filter for FlexRay frames.
- **MirrorSourceNetworkLin**
  - UUID: `ECUC:7ecfe087-407f-4304-812c-b7883b7ba44e`
  - 描述: Source bus representing a LIN network.
- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.
- **MirrorSourceLinToCanIdMapping**
  - UUID: `ECUC:9726f8c7-feb6-41a0-934f-f48564e33f42`
  - 描述: Rule for mapping a LIN frame ID to a special CAN ID.

**容器描述**:

Source bus from which frames are received by the Bus Mirroring module.

##### 22. MirrorSourceCanFilter

**容器属性**:

- **UUID**: `ECUC:243df727-33a7-4094-bd61-f06dab1b20fc`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceCanFilter`
- **多重性**: [0..255]

**容器描述**:

Pre-configured filter for CAN frames.

##### 23. MirrorSourceLinFilter

**容器属性**:

- **UUID**: `ECUC:1e4417bb-57d9-4580-a315-b7e73366ec73`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `MirrorSourceLinFilter`
- **多重性**: [0..255]

**容器选择**:

- **MirrorSourceLinFilterMask**
  - UUID: `ECUC:aa296492-4325-4afb-a4ac-448c3281ecc0`
  - 描述: Pre-configured mask based filter for LIN frames.
- **MirrorSourceLinFilterRange**
  - UUID: `ECUC:1cf53a37-fe13-48b4-9392-bd58651a65dc`
  - 描述: Pre-configured range filter for LIN frames.

**容器描述**:

Pre-configured filter for LIN frames.

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

1. **Mirror**
