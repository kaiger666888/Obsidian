# FrNm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:20

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrNm](#frnm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrNm

#### 基本信息

- **UUID**: `ECUC:fb2763f4-dd57-4ab8-83c1-bac35d27373c`
- **模块名称**: `FrNm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

The Flexray Nm module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **13** 个配置容器：

##### 1. FrNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:1e8c6f6c-4887-43c7-89d0-bd5fab7cf16e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters for all FlexRay NM channels.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. FrNmChannel

**容器属性**:

- **UUID**: `ECUC:05184f67-a45b-4cfe-9bb8-de642badc1a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters for a FlexRay NM Channel.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. FrNmChannelIdentifiers

**容器属性**:

- **UUID**: `ECUC:392d860d-8822-4778-be94-d9cbed0b21ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelIdentifiers`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance specific identifiers related to the respective FlexRay Channel.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. FrNmCarWakeUpBitPosition

- **UUID**: `ECUC:46c00b05-85d3-4b39-8872-173d65b1c644`
- **参数名**: `FrNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

############ 2. FrNmCarWakeUpBytePosition

- **UUID**: `ECUC:9e73c3fd-aee1-4205-92d6-dd243caeabef`
- **参数名**: `FrNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

############ 3. FrNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:dc72fdd9-ddf9-4609-8a69-47c570140089`
- **参数名**: `FrNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM

############ 4. FrNmNodeId

- **UUID**: `ECUC:1336f412-cc1a-4792-90bc-1b4a097aeb23`
- **参数名**: `FrNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: NM node identifier configured for the respective FlexRay Channel.

########### BOOLEAN 类型参数

############ 1. FrNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:11e654c1-51b4-49c6-81f8-55ce807fcf71`
- **参数名**: `FrNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier

############ 2. FrNmCarWakeUpRxEnabled

- **UUID**: `ECUC:26b48e2c-d069-4791-8ad8-2dd5841736d6`
- **参数名**: `FrNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

############ 3. FrNmControlBitVectorActive

- **UUID**: `ECUC:4a785248-5bd5-487e-9708-64a2bf0c3e51`
- **参数名**: `FrNmControlBitVectorActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the control bit vector support for a Fr Nm Channel.

############ 4. FrNmPnEnabled

- **UUID**: `ECUC:349def50-5c4c-494f-b926-68c7f7ac48dd`
- **参数名**: `FrNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

############ 5. FrNmPnEraCalcEnabled

- **UUID**: `ECUC:526200f2-436e-48a5-8c28-65a323bbdddc`
- **参数名**: `FrNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for external requests. (ERA)

############ 6. FrNmRepeatMessageBitActive

- **UUID**: `ECUC:9aee0aa4-e86f-474c-8010-bb0771ace103`
- **参数名**: `FrNmRepeatMessageBitActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the repeat message bit support for a Fr Nm Channel.

############ 7. FrNmSynchronizationPointEnabled

- **UUID**: `ECUC:c151df15-fc03-40c4-9285-aae0f136d924`
- **参数名**: `FrNmSynchronizationPointEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this channel shall provide the synchronization point indication to the NM Interface.

########### ENUMERATION 类型参数

############ 1. FrNmPduScheduleVariant

- **UUID**: `ECUC:96d8cf2f-2ba5-4983-aa99-178b623a4e19`
- **参数名**: `FrNmPduScheduleVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: ECUC_AUTOSAR
- **符号名值**: false
- **可选值**:
  - `FRNM_PDU_SCHEDULE_VARIANT_1` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_2` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_3` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_4` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_5` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_6` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_7` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the PDU scheduling variant that should be used for this channel.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmPnEraRxNSduRef

- **UUID**: `ECUC:ff73aa08-9564-4998-9da8-b7206971ecac`
- **引用名**: `FrNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrNmChannelHandle

- **UUID**: `ECUC:d88b8b09-0d28-40bb-89e5-84fefce71b68`
- **引用名**: `FrNmChannelHandle`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identifier configured for the respective instance of the NM.

############ 2. FrNmComMNetworkHandleRef

- **UUID**: `ECUC:ddb2fe63-3279-4fb4-bb06-2f8e9cdf0615`
- **引用名**: `FrNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

############# BOOLEAN 类型参数

############## 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############## 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

########### 2. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

############# BOOLEAN 类型参数

############## 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############## 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

########### 3. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

######### 2. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

########### BOOLEAN 类型参数

############ 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

######### 3. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

########### BOOLEAN 类型参数

############ 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

######### 4. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

######### 5. FrNmChannelTiming

**容器属性**:

- **UUID**: `ECUC:2356fc9a-7552-44bd-b5b4-179696eb1a91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelTiming`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance-specific timing related to the respective FlexRay  Channel.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. FrNmReadySleepCnt

- **UUID**: `ECUC:a9817d84-0c8f-4a31-8040-f27af96ef907`
- **参数名**: `FrNmReadySleepCnt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numbers of repetitions in the ready sleep state before NM switches to bus sleep mode.

########### BOOLEAN 类型参数

############ 1. FrNmVoteInhibitionEnabled

- **UUID**: `ECUC:07bc7e1b-0745-4b11-aee0-b57f63a5a0ce`
- **参数名**: `FrNmVoteInhibitionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the inhibition of vote changes from the next-to-last repetition cycle to the last repetition cycle before the Ready Sleep Counter expires.

########### FLOAT 类型参数

############ 1. FrNmMainFunctionPeriod

- **UUID**: `ECUC:58d441c8-743c-4926-b25c-71caf8e00134`
- **参数名**: `FrNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.02]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the processing cycle of the main function of FrNm module in seconds.

############ 2. FrNmMsgTimeoutTime

- **UUID**: `ECUC:3d5fd516-450d-4d36-ab4b-414bc5a48c0f`
- **参数名**: `FrNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout  of a NM-message. It determines in seconds how long the NM shall wait with notification of transmission failure while communication errors occur on the bus.

############ 3. FrNmRemoteSleepIndTime

- **UUID**: `ECUC:9b7ae88e-33fb-4927-95e9-f4441d6bf81a`
- **参数名**: `FrNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication. It defines the time in seconds how long it shall take to recognize that all other nodes are ready to sleep.

############ 4. FrNmRepeatMessageTime

- **UUID**: `ECUC:9abb6684-afa7-4305-8dbe-72b1f8d86950`
- **参数名**: `FrNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State. Defines the time in seconds how long the NM shall stay in the Repeat Message State.

############ 5. FrNmSyncLossTimer

- **UUID**: `ECUC:64df2e0c-eea2-4701-a8c7-ed8ceb35b5d7`
- **参数名**: `FrNmSyncLossTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for the SyncLossTimer in seconds.

########### ENUMERATION 类型参数

############ 1. FrNmDataCycle

- **UUID**: `ECUC:1cf96def-c175-476e-971f-d65c5034e9f0`
- **参数名**: `FrNmDataCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the NM Data of all ECUs on the FlexRay bus

############ 2. FrNmRepetitionCycle

- **UUID**: `ECUC:db5217ed-e261-4a17-9816-14bb85964dac`
- **参数名**: `FrNmRepetitionCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Flexray Schedule Cycles used to repeat the transmission of the Nm vote of all ECUs on the Flexray Bus.

############ 3. FrNmVotingCycle

- **UUID**: `ECUC:ed9e0181-e5db-440b-92d9-bdacf0c385e2`
- **参数名**: `FrNmVotingCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the Nm vote of all ECUs on the FlexRay Bus.

####### 2. FrNmChannelIdentifiers

**容器属性**:

- **UUID**: `ECUC:392d860d-8822-4778-be94-d9cbed0b21ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelIdentifiers`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance specific identifiers related to the respective FlexRay Channel.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. FrNmCarWakeUpBitPosition

- **UUID**: `ECUC:46c00b05-85d3-4b39-8872-173d65b1c644`
- **参数名**: `FrNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

########## 2. FrNmCarWakeUpBytePosition

- **UUID**: `ECUC:9e73c3fd-aee1-4205-92d6-dd243caeabef`
- **参数名**: `FrNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

########## 3. FrNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:dc72fdd9-ddf9-4609-8a69-47c570140089`
- **参数名**: `FrNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM

########## 4. FrNmNodeId

- **UUID**: `ECUC:1336f412-cc1a-4792-90bc-1b4a097aeb23`
- **参数名**: `FrNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: NM node identifier configured for the respective FlexRay Channel.

######### BOOLEAN 类型参数

########## 1. FrNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:11e654c1-51b4-49c6-81f8-55ce807fcf71`
- **参数名**: `FrNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier

########## 2. FrNmCarWakeUpRxEnabled

- **UUID**: `ECUC:26b48e2c-d069-4791-8ad8-2dd5841736d6`
- **参数名**: `FrNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

########## 3. FrNmControlBitVectorActive

- **UUID**: `ECUC:4a785248-5bd5-487e-9708-64a2bf0c3e51`
- **参数名**: `FrNmControlBitVectorActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the control bit vector support for a Fr Nm Channel.

########## 4. FrNmPnEnabled

- **UUID**: `ECUC:349def50-5c4c-494f-b926-68c7f7ac48dd`
- **参数名**: `FrNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

########## 5. FrNmPnEraCalcEnabled

- **UUID**: `ECUC:526200f2-436e-48a5-8c28-65a323bbdddc`
- **参数名**: `FrNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for external requests. (ERA)

########## 6. FrNmRepeatMessageBitActive

- **UUID**: `ECUC:9aee0aa4-e86f-474c-8010-bb0771ace103`
- **参数名**: `FrNmRepeatMessageBitActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the repeat message bit support for a Fr Nm Channel.

########## 7. FrNmSynchronizationPointEnabled

- **UUID**: `ECUC:c151df15-fc03-40c4-9285-aae0f136d924`
- **参数名**: `FrNmSynchronizationPointEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this channel shall provide the synchronization point indication to the NM Interface.

######### ENUMERATION 类型参数

########## 1. FrNmPduScheduleVariant

- **UUID**: `ECUC:96d8cf2f-2ba5-4983-aa99-178b623a4e19`
- **参数名**: `FrNmPduScheduleVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: ECUC_AUTOSAR
- **符号名值**: false
- **可选值**:
  - `FRNM_PDU_SCHEDULE_VARIANT_1` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_2` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_3` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_4` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_5` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_6` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_7` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the PDU scheduling variant that should be used for this channel.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmPnEraRxNSduRef

- **UUID**: `ECUC:ff73aa08-9564-4998-9da8-b7206971ecac`
- **引用名**: `FrNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrNmChannelHandle

- **UUID**: `ECUC:d88b8b09-0d28-40bb-89e5-84fefce71b68`
- **引用名**: `FrNmChannelHandle`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identifier configured for the respective instance of the NM.

########## 2. FrNmComMNetworkHandleRef

- **UUID**: `ECUC:ddb2fe63-3279-4fb4-bb06-2f8e9cdf0615`
- **引用名**: `FrNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

########### BOOLEAN 类型参数

############ 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

######### 2. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

########### BOOLEAN 类型参数

############ 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

######### 3. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 3. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

######### BOOLEAN 类型参数

########## 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

####### 4. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

######### BOOLEAN 类型参数

########## 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

####### 5. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 6. FrNmChannelTiming

**容器属性**:

- **UUID**: `ECUC:2356fc9a-7552-44bd-b5b4-179696eb1a91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelTiming`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance-specific timing related to the respective FlexRay  Channel.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. FrNmReadySleepCnt

- **UUID**: `ECUC:a9817d84-0c8f-4a31-8040-f27af96ef907`
- **参数名**: `FrNmReadySleepCnt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numbers of repetitions in the ready sleep state before NM switches to bus sleep mode.

######### BOOLEAN 类型参数

########## 1. FrNmVoteInhibitionEnabled

- **UUID**: `ECUC:07bc7e1b-0745-4b11-aee0-b57f63a5a0ce`
- **参数名**: `FrNmVoteInhibitionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the inhibition of vote changes from the next-to-last repetition cycle to the last repetition cycle before the Ready Sleep Counter expires.

######### FLOAT 类型参数

########## 1. FrNmMainFunctionPeriod

- **UUID**: `ECUC:58d441c8-743c-4926-b25c-71caf8e00134`
- **参数名**: `FrNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.02]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the processing cycle of the main function of FrNm module in seconds.

########## 2. FrNmMsgTimeoutTime

- **UUID**: `ECUC:3d5fd516-450d-4d36-ab4b-414bc5a48c0f`
- **参数名**: `FrNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout  of a NM-message. It determines in seconds how long the NM shall wait with notification of transmission failure while communication errors occur on the bus.

########## 3. FrNmRemoteSleepIndTime

- **UUID**: `ECUC:9b7ae88e-33fb-4927-95e9-f4441d6bf81a`
- **参数名**: `FrNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication. It defines the time in seconds how long it shall take to recognize that all other nodes are ready to sleep.

########## 4. FrNmRepeatMessageTime

- **UUID**: `ECUC:9abb6684-afa7-4305-8dbe-72b1f8d86950`
- **参数名**: `FrNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State. Defines the time in seconds how long the NM shall stay in the Repeat Message State.

########## 5. FrNmSyncLossTimer

- **UUID**: `ECUC:64df2e0c-eea2-4701-a8c7-ed8ceb35b5d7`
- **参数名**: `FrNmSyncLossTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for the SyncLossTimer in seconds.

######### ENUMERATION 类型参数

########## 1. FrNmDataCycle

- **UUID**: `ECUC:1cf96def-c175-476e-971f-d65c5034e9f0`
- **参数名**: `FrNmDataCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the NM Data of all ECUs on the FlexRay bus

########## 2. FrNmRepetitionCycle

- **UUID**: `ECUC:db5217ed-e261-4a17-9816-14bb85964dac`
- **参数名**: `FrNmRepetitionCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Flexray Schedule Cycles used to repeat the transmission of the Nm vote of all ECUs on the Flexray Bus.

########## 3. FrNmVotingCycle

- **UUID**: `ECUC:ed9e0181-e5db-440b-92d9-bdacf0c385e2`
- **参数名**: `FrNmVotingCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the Nm vote of all ECUs on the FlexRay Bus.

##### 2. FrNmChannel

**容器属性**:

- **UUID**: `ECUC:05184f67-a45b-4cfe-9bb8-de642badc1a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters for a FlexRay NM Channel.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. FrNmChannelIdentifiers

**容器属性**:

- **UUID**: `ECUC:392d860d-8822-4778-be94-d9cbed0b21ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelIdentifiers`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance specific identifiers related to the respective FlexRay Channel.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. FrNmCarWakeUpBitPosition

- **UUID**: `ECUC:46c00b05-85d3-4b39-8872-173d65b1c644`
- **参数名**: `FrNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

########## 2. FrNmCarWakeUpBytePosition

- **UUID**: `ECUC:9e73c3fd-aee1-4205-92d6-dd243caeabef`
- **参数名**: `FrNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

########## 3. FrNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:dc72fdd9-ddf9-4609-8a69-47c570140089`
- **参数名**: `FrNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM

########## 4. FrNmNodeId

- **UUID**: `ECUC:1336f412-cc1a-4792-90bc-1b4a097aeb23`
- **参数名**: `FrNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: NM node identifier configured for the respective FlexRay Channel.

######### BOOLEAN 类型参数

########## 1. FrNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:11e654c1-51b4-49c6-81f8-55ce807fcf71`
- **参数名**: `FrNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier

########## 2. FrNmCarWakeUpRxEnabled

- **UUID**: `ECUC:26b48e2c-d069-4791-8ad8-2dd5841736d6`
- **参数名**: `FrNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

########## 3. FrNmControlBitVectorActive

- **UUID**: `ECUC:4a785248-5bd5-487e-9708-64a2bf0c3e51`
- **参数名**: `FrNmControlBitVectorActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the control bit vector support for a Fr Nm Channel.

########## 4. FrNmPnEnabled

- **UUID**: `ECUC:349def50-5c4c-494f-b926-68c7f7ac48dd`
- **参数名**: `FrNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

########## 5. FrNmPnEraCalcEnabled

- **UUID**: `ECUC:526200f2-436e-48a5-8c28-65a323bbdddc`
- **参数名**: `FrNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for external requests. (ERA)

########## 6. FrNmRepeatMessageBitActive

- **UUID**: `ECUC:9aee0aa4-e86f-474c-8010-bb0771ace103`
- **参数名**: `FrNmRepeatMessageBitActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the repeat message bit support for a Fr Nm Channel.

########## 7. FrNmSynchronizationPointEnabled

- **UUID**: `ECUC:c151df15-fc03-40c4-9285-aae0f136d924`
- **参数名**: `FrNmSynchronizationPointEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this channel shall provide the synchronization point indication to the NM Interface.

######### ENUMERATION 类型参数

########## 1. FrNmPduScheduleVariant

- **UUID**: `ECUC:96d8cf2f-2ba5-4983-aa99-178b623a4e19`
- **参数名**: `FrNmPduScheduleVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: ECUC_AUTOSAR
- **符号名值**: false
- **可选值**:
  - `FRNM_PDU_SCHEDULE_VARIANT_1` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_2` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_3` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_4` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_5` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_6` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_7` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the PDU scheduling variant that should be used for this channel.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmPnEraRxNSduRef

- **UUID**: `ECUC:ff73aa08-9564-4998-9da8-b7206971ecac`
- **引用名**: `FrNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrNmChannelHandle

- **UUID**: `ECUC:d88b8b09-0d28-40bb-89e5-84fefce71b68`
- **引用名**: `FrNmChannelHandle`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identifier configured for the respective instance of the NM.

########## 2. FrNmComMNetworkHandleRef

- **UUID**: `ECUC:ddb2fe63-3279-4fb4-bb06-2f8e9cdf0615`
- **引用名**: `FrNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

########### BOOLEAN 类型参数

############ 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

######### 2. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

########### BOOLEAN 类型参数

############ 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

############ 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

######### 3. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 2. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

######### BOOLEAN 类型参数

########## 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

####### 3. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

######### BOOLEAN 类型参数

########## 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

####### 4. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

####### 5. FrNmChannelTiming

**容器属性**:

- **UUID**: `ECUC:2356fc9a-7552-44bd-b5b4-179696eb1a91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelTiming`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance-specific timing related to the respective FlexRay  Channel.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. FrNmReadySleepCnt

- **UUID**: `ECUC:a9817d84-0c8f-4a31-8040-f27af96ef907`
- **参数名**: `FrNmReadySleepCnt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numbers of repetitions in the ready sleep state before NM switches to bus sleep mode.

######### BOOLEAN 类型参数

########## 1. FrNmVoteInhibitionEnabled

- **UUID**: `ECUC:07bc7e1b-0745-4b11-aee0-b57f63a5a0ce`
- **参数名**: `FrNmVoteInhibitionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the inhibition of vote changes from the next-to-last repetition cycle to the last repetition cycle before the Ready Sleep Counter expires.

######### FLOAT 类型参数

########## 1. FrNmMainFunctionPeriod

- **UUID**: `ECUC:58d441c8-743c-4926-b25c-71caf8e00134`
- **参数名**: `FrNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.02]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the processing cycle of the main function of FrNm module in seconds.

########## 2. FrNmMsgTimeoutTime

- **UUID**: `ECUC:3d5fd516-450d-4d36-ab4b-414bc5a48c0f`
- **参数名**: `FrNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout  of a NM-message. It determines in seconds how long the NM shall wait with notification of transmission failure while communication errors occur on the bus.

########## 3. FrNmRemoteSleepIndTime

- **UUID**: `ECUC:9b7ae88e-33fb-4927-95e9-f4441d6bf81a`
- **参数名**: `FrNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication. It defines the time in seconds how long it shall take to recognize that all other nodes are ready to sleep.

########## 4. FrNmRepeatMessageTime

- **UUID**: `ECUC:9abb6684-afa7-4305-8dbe-72b1f8d86950`
- **参数名**: `FrNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State. Defines the time in seconds how long the NM shall stay in the Repeat Message State.

########## 5. FrNmSyncLossTimer

- **UUID**: `ECUC:64df2e0c-eea2-4701-a8c7-ed8ceb35b5d7`
- **参数名**: `FrNmSyncLossTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for the SyncLossTimer in seconds.

######### ENUMERATION 类型参数

########## 1. FrNmDataCycle

- **UUID**: `ECUC:1cf96def-c175-476e-971f-d65c5034e9f0`
- **参数名**: `FrNmDataCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the NM Data of all ECUs on the FlexRay bus

########## 2. FrNmRepetitionCycle

- **UUID**: `ECUC:db5217ed-e261-4a17-9816-14bb85964dac`
- **参数名**: `FrNmRepetitionCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Flexray Schedule Cycles used to repeat the transmission of the Nm vote of all ECUs on the Flexray Bus.

########## 3. FrNmVotingCycle

- **UUID**: `ECUC:ed9e0181-e5db-440b-92d9-bdacf0c385e2`
- **参数名**: `FrNmVotingCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the Nm vote of all ECUs on the FlexRay Bus.

##### 3. FrNmChannelIdentifiers

**容器属性**:

- **UUID**: `ECUC:392d860d-8822-4778-be94-d9cbed0b21ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelIdentifiers`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance specific identifiers related to the respective FlexRay Channel.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. FrNmCarWakeUpBitPosition

- **UUID**: `ECUC:46c00b05-85d3-4b39-8872-173d65b1c644`
- **参数名**: `FrNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Bit position of the CWU within the NM-Message.

######## 2. FrNmCarWakeUpBytePosition

- **UUID**: `ECUC:9e73c3fd-aee1-4205-92d6-dd243caeabef`
- **参数名**: `FrNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [2..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Byte position of the CWU within the NM-Message.

######## 3. FrNmCarWakeUpFilterNodeId

- **UUID**: `ECUC:dc72fdd9-ddf9-4609-8a69-47c570140089`
- **参数名**: `FrNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit within the NM

######## 4. FrNmNodeId

- **UUID**: `ECUC:1336f412-cc1a-4792-90bc-1b4a097aeb23`
- **参数名**: `FrNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: NM node identifier configured for the respective FlexRay Channel.

####### BOOLEAN 类型参数

######## 1. FrNmCarWakeUpFilterEnabled

- **UUID**: `ECUC:11e654c1-51b4-49c6-81f8-55ce807fcf71`
- **参数名**: `FrNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CWU filtering is supported, only the CWU bit within the NM message with source node identifier

######## 2. FrNmCarWakeUpRxEnabled

- **UUID**: `ECUC:26b48e2c-d069-4791-8ad8-2dd5841736d6`
- **参数名**: `FrNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of CarWakeUp bit evaluation in received NM messages.

######## 3. FrNmControlBitVectorActive

- **UUID**: `ECUC:4a785248-5bd5-487e-9708-64a2bf0c3e51`
- **参数名**: `FrNmControlBitVectorActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the control bit vector support for a Fr Nm Channel.

######## 4. FrNmPnEnabled

- **UUID**: `ECUC:349def50-5c4c-494f-b926-68c7f7ac48dd`
- **参数名**: `FrNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

######## 5. FrNmPnEraCalcEnabled

- **UUID**: `ECUC:526200f2-436e-48a5-8c28-65a323bbdddc`
- **参数名**: `FrNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for external requests. (ERA)

######## 6. FrNmRepeatMessageBitActive

- **UUID**: `ECUC:9aee0aa4-e86f-474c-8010-bb0771ace103`
- **参数名**: `FrNmRepeatMessageBitActive`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to activate or deactivate the repeat message bit support for a Fr Nm Channel.

######## 7. FrNmSynchronizationPointEnabled

- **UUID**: `ECUC:c151df15-fc03-40c4-9285-aae0f136d924`
- **参数名**: `FrNmSynchronizationPointEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this channel shall provide the synchronization point indication to the NM Interface.

####### ENUMERATION 类型参数

######## 1. FrNmPduScheduleVariant

- **UUID**: `ECUC:96d8cf2f-2ba5-4983-aa99-178b623a4e19`
- **参数名**: `FrNmPduScheduleVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: ECUC_AUTOSAR
- **符号名值**: false
- **可选值**:
  - `FRNM_PDU_SCHEDULE_VARIANT_1` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_2` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_3` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_4` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_5` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_6` (来源: AUTOSAR_ECUC)
  - `FRNM_PDU_SCHEDULE_VARIANT_7` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the PDU scheduling variant that should be used for this channel.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. FrNmPnEraRxNSduRef

- **UUID**: `ECUC:ff73aa08-9564-4998-9da8-b7206971ecac`
- **引用名**: `FrNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrNmChannelHandle

- **UUID**: `ECUC:d88b8b09-0d28-40bb-89e5-84fefce71b68`
- **引用名**: `FrNmChannelHandle`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfCluster`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identifier configured for the respective instance of the NM.

######## 2. FrNmComMNetworkHandleRef

- **UUID**: `ECUC:ddb2fe63-3279-4fb4-bb06-2f8e9cdf0615`
- **引用名**: `FrNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

######### BOOLEAN 类型参数

########## 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

####### 2. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

######### BOOLEAN 类型参数

########## 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

########## 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

####### 3. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 4. FrNmRxPdu

**容器属性**:

- **UUID**: `ECUC:63cf01ce-91f9-4153-816e-f9bfd840a359`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmRxPdu`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM RX PDU:s.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FrNmRxPduId

- **UUID**: `ECUC:7cd2b9bd-afa1-43c8-97ff-11ca0d0d8b85`
- **参数名**: `FrNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: PDU identifier configured for the respective FlexRay Channel.

####### BOOLEAN 类型参数

######## 1. FrNmRxPduContainsData

- **UUID**: `ECUC:7f31b219-7c94-4c4e-85be-eb7fc3c12e67`
- **参数名**: `FrNmRxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

######## 2. FrNmRxPduContainsVote

- **UUID**: `ECUC:55b5885d-6ec5-4dd2-bcdf-24c305343e53`
- **参数名**: `FrNmRxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrNmRxPduRef

- **UUID**: `ECUC:7da7bb4c-20d1-4236-a079-9444644d5e91`
- **引用名**: `FrNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the FrIf module to derive the PDU Id.

##### 5. FrNmTxPdu

**容器属性**:

- **UUID**: `ECUC:3efcbe06-052f-466f-9a7d-6b0210483245`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmTxPdu`
- **多重性**: [0..2]
- **多配置容器**: false

**容器描述**:

This container describes the FlexRay NM TX PDU:s.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FrNmTxConfirmationPduId

- **UUID**: `ECUC:98bb1321-c1ec-4d09-94dd-d436b09a40e7`
- **参数名**: `FrNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the LowerLayer.

####### BOOLEAN 类型参数

######## 1. FrNmTxPduContainsData

- **UUID**: `ECUC:8dd21f51-d00e-4530-8a8e-c29ffd4fde38`
- **参数名**: `FrNmTxPduContainsData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Data.

######## 2. FrNmTxPduContainsVote

- **UUID**: `ECUC:62201e56-78be-4224-9dec-ba8319e9c3d8`
- **参数名**: `FrNmTxPduContainsVote`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameted defines if the PDU contains NM Vote information.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrNmTxPduRef

- **UUID**: `ECUC:a6fbc267-d93c-49b9-87fb-672ddc7d41a1`
- **引用名**: `FrNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference is used to derive the PDU Id that is defined by the FrIf module.

##### 6. FrNmUserDataTxPdu

**容器属性**:

- **UUID**: `ECUC:4d810673-368e-4375-bc96-e41197a52b50`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmUserDataTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if FrNmComUserDataSupport is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrNmTxUserDataPduId

- **UUID**: `ECUC:f668be4e-b74c-4470-a577-d9e4cdb7804f`
- **参数名**: `FrNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrNmTxUserDataPduRef

- **UUID**: `ECUC:97285808-d295-4a50-b81f-188ec22b0b9f`
- **引用名**: `FrNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

##### 7. FrNmChannelTiming

**容器属性**:

- **UUID**: `ECUC:2356fc9a-7552-44bd-b5b4-179696eb1a91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmChannelTiming`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains instance-specific timing related to the respective FlexRay  Channel.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. FrNmReadySleepCnt

- **UUID**: `ECUC:a9817d84-0c8f-4a31-8040-f27af96ef907`
- **参数名**: `FrNmReadySleepCnt`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numbers of repetitions in the ready sleep state before NM switches to bus sleep mode.

####### BOOLEAN 类型参数

######## 1. FrNmVoteInhibitionEnabled

- **UUID**: `ECUC:07bc7e1b-0745-4b11-aee0-b57f63a5a0ce`
- **参数名**: `FrNmVoteInhibitionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the inhibition of vote changes from the next-to-last repetition cycle to the last repetition cycle before the Ready Sleep Counter expires.

####### FLOAT 类型参数

######## 1. FrNmMainFunctionPeriod

- **UUID**: `ECUC:58d441c8-743c-4926-b25c-71caf8e00134`
- **参数名**: `FrNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..0.02]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the processing cycle of the main function of FrNm module in seconds.

######## 2. FrNmMsgTimeoutTime

- **UUID**: `ECUC:3d5fd516-450d-4d36-ab4b-414bc5a48c0f`
- **参数名**: `FrNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout  of a NM-message. It determines in seconds how long the NM shall wait with notification of transmission failure while communication errors occur on the bus.

######## 3. FrNmRemoteSleepIndTime

- **UUID**: `ECUC:9b7ae88e-33fb-4927-95e9-f4441d6bf81a`
- **参数名**: `FrNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Remote Sleep Indication. It defines the time in seconds how long it shall take to recognize that all other nodes are ready to sleep.

######## 4. FrNmRepeatMessageTime

- **UUID**: `ECUC:9abb6684-afa7-4305-8dbe-72b1f8d86950`
- **参数名**: `FrNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout for Repeat Message State. Defines the time in seconds how long the NM shall stay in the Repeat Message State.

######## 5. FrNmSyncLossTimer

- **UUID**: `ECUC:64df2e0c-eea2-4701-a8c7-ed8ceb35b5d7`
- **参数名**: `FrNmSyncLossTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for the SyncLossTimer in seconds.

####### ENUMERATION 类型参数

######## 1. FrNmDataCycle

- **UUID**: `ECUC:1cf96def-c175-476e-971f-d65c5034e9f0`
- **参数名**: `FrNmDataCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the NM Data of all ECUs on the FlexRay bus

######## 2. FrNmRepetitionCycle

- **UUID**: `ECUC:db5217ed-e261-4a17-9816-14bb85964dac`
- **参数名**: `FrNmRepetitionCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Flexray Schedule Cycles used to repeat the transmission of the Nm vote of all ECUs on the Flexray Bus.

######## 3. FrNmVotingCycle

- **UUID**: `ECUC:ed9e0181-e5db-440b-92d9-bdacf0c385e2`
- **参数名**: `FrNmVotingCycle`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRNM_CYCLE_VALUE_1` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_16` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_2` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_32` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_4` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_64` (来源: AUTOSAR_ECUC)
  - `FRNM_CYCLE_VALUE_8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of FlexRay Schedule Cycles needed to transmit the Nm vote of all ECUs on the FlexRay Bus.

##### 8. FrNmGlobalConfig

**容器属性**:

- **UUID**: `ECUC:7edc1874-5801-4b83-b345-19f2142af522`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains all global configuration parameters for the FrNm module.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. FrNmGlobalConstants

**容器属性**:

- **UUID**: `ECUC:962266d0-f81a-4094-9a31-63a650d5913c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalConstants`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module constants related to the FlexRay NM functionality.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrNmNumberOfClusters

- **UUID**: `ECUC:7565429e-2410-4128-9c07-b645646c1079`
- **参数名**: `FrNmNumberOfClusters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of AUTOSAR FR NM clusters allowed within one ECU.

####### 2. FrNmGlobalFeatures

**容器属性**:

- **UUID**: `ECUC:616c80a9-5f86-46e8-a7ba-78508b63d5d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalFeatures`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module features related to the FlexRay NM functionality.

######## 参数配置

此容器包含 **18** 个参数：

######### BOOLEAN 类型参数

########## 1. FrNmBusSynchronizationEnabled

- **UUID**: `ECUC:9a3e0c9a-a50d-4019-be35-1059c3dd79fd`
- **参数名**: `FrNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the bus synchronisation.

########## 2. FrNmComUserDataSupport

- **UUID**: `ECUC:17000d55-c5bd-4ac5-9efe-e2c4e5052983`
- **参数名**: `FrNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the user data support.

########## 3. FrNmControlBitVectorEnabled

- **UUID**: `ECUC:2cb7ef4d-f70e-40fd-bb45-29ada16ab4ef`
- **参数名**: `FrNmControlBitVectorEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling control bit vector support.

########## 4. FrNmCoordinatorSyncSupport

- **UUID**: `ECUC:c05a9f18-421f-4c84-bd1e-5af35deaa75e`
- **参数名**: `FrNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the coordinator synchronisation support.

########## 5. FrNmCycleCounterEmulation

- **UUID**: `ECUC:71df21c0-cd59-494f-9f4a-124cd48f5f7a`
- **参数名**: `FrNmCycleCounterEmulation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the cycle counter emulation.

########## 6. FrNmDualChannelPduEnable

- **UUID**: `ECUC:15847d6a-d301-4daf-a454-a315119f6d9b`
- **参数名**: `FrNmDualChannelPduEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the support of dual channel transmission and reception of NM messages.

########## 7. FrNmHwVoteEnable

- **UUID**: `ECUC:e02357fd-fd64-49a4-bee0-000f5961eeb2`
- **参数名**: `FrNmHwVoteEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the processing of FlexRay Hardware aggregated NM-Votes.

########## 8. FrNmNodeDetectionEnabled

- **UUID**: `ECUC:f2fc1c6c-eca4-4b38-9436-189c355c4711`
- **参数名**: `FrNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling node detection support.

########## 9. FrNmPassiveModeEnabled

- **UUID**: `ECUC:40eea516-843f-45bd-b78f-d15727841c63`
- **参数名**: `FrNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Passive Mode Configuration support.

########## 10. FrNmPduRxIndicationEnabled

- **UUID**: `ECUC:a099b8ce-748d-4d14-b589-53b45c2af30c`
- **参数名**: `FrNmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling PDU reception indication.

########## 11. FrNmPnEiraCalcEnabled

- **UUID**: `ECUC:08325234-1f20-4c36-af9c-69a50a057b17`
- **参数名**: `FrNmPnEiraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for internal an external requests. (EIRA)

########## 12. FrNmRemoteSleepIndicationEnabled

- **UUID**: `ECUC:a870374a-2eec-49b1-96fa-26e1eb75db29`
- **参数名**: `FrNmRemoteSleepIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling remote sleep indication.

########## 13. FrNmRepeatMessageBitEnabled

- **UUID**: `ECUC:0b907a7d-32eb-4355-a790-6d7faf26f97f`
- **参数名**: `FrNmRepeatMessageBitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the repeat message bit support.

########## 14. FrNmSourceNodeIdentifierEnabled

- **UUID**: `ECUC:575e6efa-9286-43c6-b386-dadc8bcd69cf`
- **参数名**: `FrNmSourceNodeIdentifierEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling SourceNodeIdentifier support.

########## 15. FrNmStateChangeIndicationEnabled

- **UUID**: `ECUC:f1c0e977-487b-4d8e-9dac-e6543fee8e90`
- **参数名**: `FrNmStateChangeIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling state change indication.

########## 16. FrNmUserDataEnabled

- **UUID**: `ECUC:02def680-51fd-441e-ad69-204a40f17680`
- **参数名**: `FrNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling user data support.

########## 17. FrNmVotingNextToLastRepetitionCycleDisable

- **UUID**: `ECUC:37b00527-fec3-43ff-92c6-07b2439173d3`
- **参数名**: `FrNmVotingNextToLastRepetitionCycleDisable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for disabling vote changes in the last two

######### FLOAT 类型参数

########## 1. FrNmPnResetTime

- **UUID**: `ECUC:1d9f1e60-fd35-45bc-babc-64a9be8fae74`
- **参数名**: `FrNmPnResetTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of PN requests in the EIRA and in the ERA. The value shall be the same for every channel. Thus it is a global config parameter.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrNmPnEiraRxNSduRef

- **UUID**: `ECUC:debf2dcf-ce84-4c52-af2b-642dbffb8346`
- **引用名**: `FrNmPnEiraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrNmPnInfo

**容器属性**:

- **UUID**: `ECUC:c9c3ed55-f3ee-4f54-8a6b-bd2e106b0dc7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnInfo`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrNmPnInfoLength

- **UUID**: `ECUC:40000c94-20d8-4ed6-846a-871548acdae4`
- **参数名**: `FrNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

############ 2. FrNmPnInfoOffset

- **UUID**: `ECUC:ee5f3372-e457-432f-85d7-4d2d91c3aedd`
- **参数名**: `FrNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

############## 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

######### 2. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

############ 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

####### 3. FrNmPnInfo

**容器属性**:

- **UUID**: `ECUC:c9c3ed55-f3ee-4f54-8a6b-bd2e106b0dc7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnInfo`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrNmPnInfoLength

- **UUID**: `ECUC:40000c94-20d8-4ed6-846a-871548acdae4`
- **参数名**: `FrNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

########## 2. FrNmPnInfoOffset

- **UUID**: `ECUC:ee5f3372-e457-432f-85d7-4d2d91c3aedd`
- **参数名**: `FrNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

############ 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

####### 4. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

########## 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

####### 5. FrNmGlobalProperties

**容器属性**:

- **UUID**: `ECUC:68a43ddd-1574-4f64-acd3-76b9e1cf8c05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalProperties`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module properties related to the FlexRay NM functionality.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. FrNmDevErrorDetect

- **UUID**: `ECUC:655ce540-eff7-4d25-a44f-e77db6f2ba9e`
- **参数名**: `FrNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection

########## 2. FrNmMainAcrossFrCycle

- **UUID**: `ECUC:f92b6421-10d1-4982-85a8-397e63bb89b9`
- **参数名**: `FrNmMainAcrossFrCycle`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter describing if the execution of FrNm_Main function crosses the FlexRay cycle boundary or not.

########## 3. FrNmVersionInfoApi

- **UUID**: `ECUC:59f1cf7c-7889-4ace-aa12-38016361dc4e`
- **参数名**: `FrNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling version info API support.

##### 9. FrNmGlobalConstants

**容器属性**:

- **UUID**: `ECUC:962266d0-f81a-4094-9a31-63a650d5913c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalConstants`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module constants related to the FlexRay NM functionality.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrNmNumberOfClusters

- **UUID**: `ECUC:7565429e-2410-4128-9c07-b645646c1079`
- **参数名**: `FrNmNumberOfClusters`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of AUTOSAR FR NM clusters allowed within one ECU.

##### 10. FrNmGlobalFeatures

**容器属性**:

- **UUID**: `ECUC:616c80a9-5f86-46e8-a7ba-78508b63d5d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalFeatures`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module features related to the FlexRay NM functionality.

###### 参数配置

此容器包含 **18** 个参数：

####### BOOLEAN 类型参数

######## 1. FrNmBusSynchronizationEnabled

- **UUID**: `ECUC:9a3e0c9a-a50d-4019-be35-1059c3dd79fd`
- **参数名**: `FrNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the bus synchronisation.

######## 2. FrNmComUserDataSupport

- **UUID**: `ECUC:17000d55-c5bd-4ac5-9efe-e2c4e5052983`
- **参数名**: `FrNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/disable the user data support.

######## 3. FrNmControlBitVectorEnabled

- **UUID**: `ECUC:2cb7ef4d-f70e-40fd-bb45-29ada16ab4ef`
- **参数名**: `FrNmControlBitVectorEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling control bit vector support.

######## 4. FrNmCoordinatorSyncSupport

- **UUID**: `ECUC:c05a9f18-421f-4c84-bd1e-5af35deaa75e`
- **参数名**: `FrNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the coordinator synchronisation support.

######## 5. FrNmCycleCounterEmulation

- **UUID**: `ECUC:71df21c0-cd59-494f-9f4a-124cd48f5f7a`
- **参数名**: `FrNmCycleCounterEmulation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the cycle counter emulation.

######## 6. FrNmDualChannelPduEnable

- **UUID**: `ECUC:15847d6a-d301-4daf-a454-a315119f6d9b`
- **参数名**: `FrNmDualChannelPduEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the support of dual channel transmission and reception of NM messages.

######## 7. FrNmHwVoteEnable

- **UUID**: `ECUC:e02357fd-fd64-49a4-bee0-000f5961eeb2`
- **参数名**: `FrNmHwVoteEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the processing of FlexRay Hardware aggregated NM-Votes.

######## 8. FrNmNodeDetectionEnabled

- **UUID**: `ECUC:f2fc1c6c-eca4-4b38-9436-189c355c4711`
- **参数名**: `FrNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling node detection support.

######## 9. FrNmPassiveModeEnabled

- **UUID**: `ECUC:40eea516-843f-45bd-b78f-d15727841c63`
- **参数名**: `FrNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Passive Mode Configuration support.

######## 10. FrNmPduRxIndicationEnabled

- **UUID**: `ECUC:a099b8ce-748d-4d14-b589-53b45c2af30c`
- **参数名**: `FrNmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling PDU reception indication.

######## 11. FrNmPnEiraCalcEnabled

- **UUID**: `ECUC:08325234-1f20-4c36-af9c-69a50a057b17`
- **参数名**: `FrNmPnEiraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if FrNm calculates the PN request information for internal an external requests. (EIRA)

######## 12. FrNmRemoteSleepIndicationEnabled

- **UUID**: `ECUC:a870374a-2eec-49b1-96fa-26e1eb75db29`
- **参数名**: `FrNmRemoteSleepIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling remote sleep indication.

######## 13. FrNmRepeatMessageBitEnabled

- **UUID**: `ECUC:0b907a7d-32eb-4355-a790-6d7faf26f97f`
- **参数名**: `FrNmRepeatMessageBitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the repeat message bit support.

######## 14. FrNmSourceNodeIdentifierEnabled

- **UUID**: `ECUC:575e6efa-9286-43c6-b386-dadc8bcd69cf`
- **参数名**: `FrNmSourceNodeIdentifierEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling SourceNodeIdentifier support.

######## 15. FrNmStateChangeIndicationEnabled

- **UUID**: `ECUC:f1c0e977-487b-4d8e-9dac-e6543fee8e90`
- **参数名**: `FrNmStateChangeIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling state change indication.

######## 16. FrNmUserDataEnabled

- **UUID**: `ECUC:02def680-51fd-441e-ad69-204a40f17680`
- **参数名**: `FrNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling user data support.

######## 17. FrNmVotingNextToLastRepetitionCycleDisable

- **UUID**: `ECUC:37b00527-fec3-43ff-92c6-07b2439173d3`
- **参数名**: `FrNmVotingNextToLastRepetitionCycleDisable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for disabling vote changes in the last two

####### FLOAT 类型参数

######## 1. FrNmPnResetTime

- **UUID**: `ECUC:1d9f1e60-fd35-45bc-babc-64a9be8fae74`
- **参数名**: `FrNmPnResetTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of PN requests in the EIRA and in the ERA. The value shall be the same for every channel. Thus it is a global config parameter.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrNmPnEiraRxNSduRef

- **UUID**: `ECUC:debf2dcf-ce84-4c52-af2b-642dbffb8346`
- **引用名**: `FrNmPnEiraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Pdu in the COM-Stack.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FrNmPnInfo

**容器属性**:

- **UUID**: `ECUC:c9c3ed55-f3ee-4f54-8a6b-bd2e106b0dc7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnInfo`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrNmPnInfoLength

- **UUID**: `ECUC:40000c94-20d8-4ed6-846a-871548acdae4`
- **参数名**: `FrNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

########## 2. FrNmPnInfoOffset

- **UUID**: `ECUC:ee5f3372-e457-432f-85d7-4d2d91c3aedd`
- **参数名**: `FrNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

############ 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

####### 2. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

########## 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

##### 11. FrNmPnInfo

**容器属性**:

- **UUID**: `ECUC:c9c3ed55-f3ee-4f54-8a6b-bd2e106b0dc7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnInfo`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

PN information configuration

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrNmPnInfoLength

- **UUID**: `ECUC:40000c94-20d8-4ed6-846a-871548acdae4`
- **参数名**: `FrNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the length of the PN request information in the NM message.

######## 2. FrNmPnInfoOffset

- **UUID**: `ECUC:ee5f3372-e457-432f-85d7-4d2d91c3aedd`
- **参数名**: `FrNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [1..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

########## 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

##### 12. FrNmPnFilterMaskByte

**容器属性**:

- **UUID**: `ECUC:91459ad1-8fd1-4332-8c12-48678acedb89`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmPnFilterMaskByte`
- **多重性**: [0..7]
- **多配置容器**: false

**容器描述**:

Filter mask byte configuration

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrNmPnFilterMaskByteIndex

- **UUID**: `ECUC:4adc8277-4162-45d5-9f9e-abc1ef4db5c9`
- **参数名**: `FrNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the filter mask byte. Specifies the position within the filter mask byte array.

######## 2. FrNmPnFilterMaskByteValue

- **UUID**: `ECUC:5c21384c-6bf7-4bcf-b7e5-07c82b0f5e84`
- **参数名**: `FrNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter to configure the filter mask byte.

##### 13. FrNmGlobalProperties

**容器属性**:

- **UUID**: `ECUC:68a43ddd-1574-4f64-acd3-76b9e1cf8c05`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrNmGlobalProperties`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains module properties related to the FlexRay NM functionality.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. FrNmDevErrorDetect

- **UUID**: `ECUC:655ce540-eff7-4d25-a44f-e77db6f2ba9e`
- **参数名**: `FrNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection

######## 2. FrNmMainAcrossFrCycle

- **UUID**: `ECUC:f92b6421-10d1-4982-85a8-397e63bb89b9`
- **参数名**: `FrNmMainAcrossFrCycle`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter describing if the execution of FrNm_Main function crosses the FlexRay cycle boundary or not.

######## 3. FrNmVersionInfoApi

- **UUID**: `ECUC:59f1cf7c-7889-4ace-aa12-38016361dc4e`
- **参数名**: `FrNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling version info API support.

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

1. **FrNm**
