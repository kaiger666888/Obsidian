# Cdd - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:09

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Cdd](#cdd)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Cdd

#### 基本信息

- **UUID**: `ECUC:1286e7ac-4948-4b92-8227-61d9d064283c`
- **模块名称**: `Cdd`
- **多重性**: [0..infinite]

#### 模块描述

The CDD module describes the minimal requirements that are necessary for the configuration of a CDD with respect to the surrounding standardized BSW modules.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. CddComStackContribution

**容器属性**:

- **UUID**: `ECUC:6c020b3e-c61f-45e6-988c-8b1dd46692b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComStackContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Contribution of COM Stack modules.

###### 配置容器

本模块包含 **16** 个配置容器：

####### 1. CddComIfUpperLayerContribution

**容器属性**:

- **UUID**: `ECUC:a85003e9-585f-44b6-b499-633eeaa58362`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the UpperLayer of the Com Interface module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:c94191ae-a883-4bb9-ac3e-841fc5f69c09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddComIfHandleId

- **UUID**: `ECUC:cd9c5fb8-5f36-4b7a-8e90-ee6b8e7ba22c`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComIfPduRef

- **UUID**: `ECUC:4a9c0e26-9b38-48f8-8180-5dcee98e0fad`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:ef09dcb2-7fd7-49cc-a931-f39a4eecac1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddComIfHandleId

- **UUID**: `ECUC:b807ad28-9b7a-4650-8414-360909b41c1e`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComIfPduRef

- **UUID**: `ECUC:5f78db18-cb6f-41b4-84a2-55d58da0cb0c`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:c94191ae-a883-4bb9-ac3e-841fc5f69c09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `ECUC:cd9c5fb8-5f36-4b7a-8e90-ee6b8e7ba22c`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `ECUC:4a9c0e26-9b38-48f8-8180-5dcee98e0fad`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:ef09dcb2-7fd7-49cc-a931-f39a4eecac1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `ECUC:b807ad28-9b7a-4650-8414-360909b41c1e`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `ECUC:5f78db18-cb6f-41b4-84a2-55d58da0cb0c`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 4. CddComMLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:15f24c4f-fbb3-4669-80f3-9b197deb7c62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Communication Manager module.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:56004dbf-51bf-4a1c-a027-483d08639255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddComMLowerLayerChannelRef

- **UUID**: `ECUC:5351dd2e-6f89-4c5c-9fc8-4a301d7cdac9`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

####### 5. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:56004dbf-51bf-4a1c-a027-483d08639255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComMLowerLayerChannelRef

- **UUID**: `ECUC:5351dd2e-6f89-4c5c-9fc8-4a301d7cdac9`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

####### 6. CddGenericNmLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:d97e1043-dd9e-4703-a719-607ce792be19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Generic NM module.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:119abe0c-226e-4251-abb0-d59123945082`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `ECUC:f5240286-e1ac-4c12-9f47-0c23e033cf85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 7. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:119abe0c-226e-4251-abb0-d59123945082`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `ECUC:f5240286-e1ac-4c12-9f47-0c23e033cf85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

####### 8. CddPduRLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:d4920631-85b0-4376-8743-3babb19cdc29`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Pdu Router module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:32300c99-13ae-4fe8-8bba-93f316788818`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:74dd8870-0180-4f4a-85cb-5c53a1be131a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:f4dbfb7a-93e4-4404-83f1-e66f3d41df74`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:186d1878-40b0-4a5a-aae4-8ba77dd3ce93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:e95cede4-9ee6-493d-9905-de3c13f222ec`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:5662fa00-3ca4-4663-ae73-ffde4f9379b5`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 9. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:32300c99-13ae-4fe8-8bba-93f316788818`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:74dd8870-0180-4f4a-85cb-5c53a1be131a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:f4dbfb7a-93e4-4404-83f1-e66f3d41df74`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 10. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:186d1878-40b0-4a5a-aae4-8ba77dd3ce93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:e95cede4-9ee6-493d-9905-de3c13f222ec`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:5662fa00-3ca4-4663-ae73-ffde4f9379b5`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 11. CddPduRUpperLayerContribution

**容器属性**:

- **UUID**: `ECUC:2eaf17e0-7822-4cb2-8cce-9083ec9291d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the UpperLayer of the Pdu Router module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:8f579ded-0098-42fc-81eb-9fc765136ed6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:331ea11f-6ea6-47c4-9231-db5716ea9e69`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:ce526005-b88e-4fc2-a44e-9112c948af82`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:a52124c4-5abd-4b6a-8f67-a04f970428a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:ba3c213c-e704-46a1-a0e5-a59e7a501d50`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:245c3911-45a2-40e6-aae4-29b332894893`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 12. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:8f579ded-0098-42fc-81eb-9fc765136ed6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:331ea11f-6ea6-47c4-9231-db5716ea9e69`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:ce526005-b88e-4fc2-a44e-9112c948af82`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 13. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:a52124c4-5abd-4b6a-8f67-a04f970428a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:ba3c213c-e704-46a1-a0e5-a59e7a501d50`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:245c3911-45a2-40e6-aae4-29b332894893`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 14. CddSoAdUpperLayerContribution

**容器属性**:

- **UUID**: `12e74aa2-3d7e-4da2-8f57-52a2d1421c74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the SoAd module.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `a98634d8-a722-4ba1-956b-db956ed559e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddSoAdUpperLayerHandleId

- **UUID**: `58919aed-6985-480a-8699-c2b092e9b930`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddSoAdUpperLayerPduRef

- **UUID**: `cea75abe-0a6c-4d37-b4e9-4128e4403e1d`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `5ea321bf-1281-4831-bd47-150e96dd8f28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CddSoAdUpperLayerHandleId

- **UUID**: `3a186a1d-7c19-45b9-a70b-1ea0870d5912`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CddSoAdUpperLayerPduRef

- **UUID**: `29adab3b-3877-4f3a-9383-5bc2da9f4f59`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 15. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `a98634d8-a722-4ba1-956b-db956ed559e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `58919aed-6985-480a-8699-c2b092e9b930`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `cea75abe-0a6c-4d37-b4e9-4128e4403e1d`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 16. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `5ea321bf-1281-4831-bd47-150e96dd8f28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `3a186a1d-7c19-45b9-a70b-1ea0870d5912`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `29adab3b-3877-4f3a-9383-5bc2da9f4f59`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 2. CddComIfUpperLayerContribution

**容器属性**:

- **UUID**: `ECUC:a85003e9-585f-44b6-b499-633eeaa58362`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the UpperLayer of the Com Interface module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:c94191ae-a883-4bb9-ac3e-841fc5f69c09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `ECUC:cd9c5fb8-5f36-4b7a-8e90-ee6b8e7ba22c`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `ECUC:4a9c0e26-9b38-48f8-8180-5dcee98e0fad`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:ef09dcb2-7fd7-49cc-a931-f39a4eecac1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddComIfHandleId

- **UUID**: `ECUC:b807ad28-9b7a-4650-8414-360909b41c1e`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComIfPduRef

- **UUID**: `ECUC:5f78db18-cb6f-41b4-84a2-55d58da0cb0c`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 3. CddComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:c94191ae-a883-4bb9-ac3e-841fc5f69c09`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddComIfHandleId

- **UUID**: `ECUC:cd9c5fb8-5f36-4b7a-8e90-ee6b8e7ba22c`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComIfPduRef

- **UUID**: `ECUC:4a9c0e26-9b38-48f8-8180-5dcee98e0fad`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 4. CddComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:ef09dcb2-7fd7-49cc-a931-f39a4eecac1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComIfUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddComIfHandleId

- **UUID**: `ECUC:b807ad28-9b7a-4650-8414-360909b41c1e`
- **参数名**: `CddComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComIfPduRef

- **UUID**: `ECUC:5f78db18-cb6f-41b4-84a2-55d58da0cb0c`
- **引用名**: `CddComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 5. CddComMLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:15f24c4f-fbb3-4669-80f3-9b197deb7c62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Communication Manager module.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:56004dbf-51bf-4a1c-a027-483d08639255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddComMLowerLayerChannelRef

- **UUID**: `ECUC:5351dd2e-6f89-4c5c-9fc8-4a301d7cdac9`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

##### 6. CddComMLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:56004dbf-51bf-4a1c-a027-483d08639255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddComMLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the network specific parameters.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddComMLowerLayerChannelRef

- **UUID**: `ECUC:5351dd2e-6f89-4c5c-9fc8-4a301d7cdac9`
- **引用名**: `CddComMLowerLayerChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: Unique handle to identify one certain network. Reference to one of the network handles configured for the ComM.

##### 7. CddGenericNmLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:d97e1043-dd9e-4703-a719-607ce792be19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Generic NM module.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:119abe0c-226e-4251-abb0-d59123945082`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `ECUC:f5240286-e1ac-4c12-9f47-0c23e033cf85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 8. CddGenericNmLowerLayerChannel

**容器属性**:

- **UUID**: `ECUC:119abe0c-226e-4251-abb0-d59123945082`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddGenericNmLowerLayerChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

NM Channel specific configuration parameters.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddGenericNmComMNetworkHandleRef

- **UUID**: `ECUC:f5240286-e1ac-4c12-9f47-0c23e033cf85`
- **引用名**: `CddGenericNmComMNetworkHandleRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 9. CddPduRLowerLayerContribution

**容器属性**:

- **UUID**: `ECUC:d4920631-85b0-4376-8743-3babb19cdc29`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the LowerLayer of the Pdu Router module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:32300c99-13ae-4fe8-8bba-93f316788818`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:74dd8870-0180-4f4a-85cb-5c53a1be131a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:f4dbfb7a-93e4-4404-83f1-e66f3d41df74`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:186d1878-40b0-4a5a-aae4-8ba77dd3ce93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:e95cede4-9ee6-493d-9905-de3c13f222ec`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:5662fa00-3ca4-4663-ae73-ffde4f9379b5`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 10. CddPduRLowerLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:32300c99-13ae-4fe8-8bba-93f316788818`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:74dd8870-0180-4f4a-85cb-5c53a1be131a`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:f4dbfb7a-93e4-4404-83f1-e66f3d41df74`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 11. CddPduRLowerLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:186d1878-40b0-4a5a-aae4-8ba77dd3ce93`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRLowerLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRLowerLayerHandleId

- **UUID**: `ECUC:e95cede4-9ee6-493d-9905-de3c13f222ec`
- **参数名**: `CddPduRLowerLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRLowerLayerPduRef

- **UUID**: `ECUC:5662fa00-3ca4-4663-ae73-ffde4f9379b5`
- **引用名**: `CddPduRLowerLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 12. CddPduRUpperLayerContribution

**容器属性**:

- **UUID**: `ECUC:2eaf17e0-7822-4cb2-8cce-9083ec9291d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Device Driver that serves as the UpperLayer of the Pdu Router module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:8f579ded-0098-42fc-81eb-9fc765136ed6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:331ea11f-6ea6-47c4-9231-db5716ea9e69`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:ce526005-b88e-4fc2-a44e-9112c948af82`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:a52124c4-5abd-4b6a-8f67-a04f970428a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:ba3c213c-e704-46a1-a0e5-a59e7a501d50`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:245c3911-45a2-40e6-aae4-29b332894893`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 13. CddPduRUpperLayerRxPdu

**容器属性**:

- **UUID**: `ECUC:8f579ded-0098-42fc-81eb-9fc765136ed6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerRxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:331ea11f-6ea6-47c4-9231-db5716ea9e69`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:ce526005-b88e-4fc2-a44e-9112c948af82`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 14. CddPduRUpperLayerTxPdu

**容器属性**:

- **UUID**: `ECUC:a52124c4-5abd-4b6a-8f67-a04f970428a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddPduRUpperLayerTxPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddPduRUpperLayerHandleId

- **UUID**: `ECUC:ba3c213c-e704-46a1-a0e5-a59e7a501d50`
- **参数名**: `CddPduRUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddPduRUpperLayerPduRef

- **UUID**: `ECUC:245c3911-45a2-40e6-aae4-29b332894893`
- **引用名**: `CddPduRUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 15. CddSoAdUpperLayerContribution

**容器属性**:

- **UUID**: `12e74aa2-3d7e-4da2-8f57-52a2d1421c74`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerContribution`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Parameters that are necessary for the configuration of a Complex Driver that serves as the UpperLayer of the SoAd module.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `a98634d8-a722-4ba1-956b-db956ed559e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `58919aed-6985-480a-8699-c2b092e9b930`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `cea75abe-0a6c-4d37-b4e9-4128e4403e1d`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `5ea321bf-1281-4831-bd47-150e96dd8f28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CddSoAdUpperLayerHandleId

- **UUID**: `3a186a1d-7c19-45b9-a70b-1ea0870d5912`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CddSoAdUpperLayerPduRef

- **UUID**: `29adab3b-3877-4f3a-9383-5bc2da9f4f59`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 16. CddSoAdUpperLayerRxPdu

**容器属性**:

- **UUID**: `a98634d8-a722-4ba1-956b-db956ed559e7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerRxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddSoAdUpperLayerHandleId

- **UUID**: `58919aed-6985-480a-8699-c2b092e9b930`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddSoAdUpperLayerPduRef

- **UUID**: `cea75abe-0a6c-4d37-b4e9-4128e4403e1d`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 17. CddSoAdUpperLayerTxPdu

**容器属性**:

- **UUID**: `5ea321bf-1281-4831-bd47-150e96dd8f28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddSoAdUpperLayerTxPdu`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CddSoAdUpperLayerHandleId

- **UUID**: `3a186a1d-7c19-45b9-a70b-1ea0870d5912`
- **参数名**: `CddSoAdUpperLayerHandleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddSoAdUpperLayerPduRef

- **UUID**: `29adab3b-3877-4f3a-9383-5bc2da9f4f59`
- **引用名**: `CddSoAdUpperLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 18. CddEcucPartitionInteraction

**容器属性**:

- **UUID**: `ECUC:5ddb5cdf-4b83-4980-b535-5aa4c700316f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CddEcucPartitionInteraction`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container holds the partition interaction configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. CddPartitionStoppedFunctionName

- **UUID**: `ECUC:b329985d-d398-4f17-93cd-f29503da4d52`
- **参数名**: `CddPartitionStoppedFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Function name to be called when the partition which is triggering the complex driver is stopped.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CddEcucPartitionRef

- **UUID**: `ECUC:46cceb2a-0c28-49ac-8bad-7558446a366c`
- **引用名**: `CddEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the "EcucPartition" which executes the software which triggers the CDD.

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

1. **Cdd**
