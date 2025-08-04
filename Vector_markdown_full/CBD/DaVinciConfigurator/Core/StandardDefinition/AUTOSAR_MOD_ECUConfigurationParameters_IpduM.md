# IpduM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:22

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [IpduM](#ipdum)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. IpduM

#### 基本信息

- **UUID**: `ECUC:01c1cba1-1af2-40e0-a551-2417ba71f3fb`
- **模块名称**: `IpduM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the IpduM (Ipdu Multiplexer) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **17** 个配置容器：

##### 1. IpduMConfig

**容器属性**:

- **UUID**: `ECUC:7af0ef33-3531-4c92-8769-330c3db2f19b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the sub containers of the IpduM module. The IpduMTxPathway subcontainer includes information about sent I-PDUs. The IpduMRxPathway includes information about received I-PDUs.

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. IpduMRxPathway

**容器属性**:

- **UUID**: `ECUC:7bedc87c-e833-4e9a-8ca3-ac8d731e7639`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxPathway`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters received I-PDUs by the IpduM module.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. IpduMRxIndication

**容器属性**:

- **UUID**: `ECUC:79391c0f-2367-4aaa-9fe1-0499addc12a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming RxIndication calls.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxHandleId

- **UUID**: `ECUC:0033a86b-82e6-4de0-ba8f-63fb49ed2d56`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

########### ENUMERATION 类型参数

############ 1. IpduMByteOrder

- **UUID**: `ECUC:0a091ae2-be9b-9515-59e3-e1ccee37c364`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMRxIndicationPduRef

- **UUID**: `ECUC:1072e012-067c-4a46-a7d3-c732cc72e5fb`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the received Pdu representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 2. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 2. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 6. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 2. IpduMRxIndication

**容器属性**:

- **UUID**: `ECUC:79391c0f-2367-4aaa-9fe1-0499addc12a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming RxIndication calls.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxHandleId

- **UUID**: `ECUC:0033a86b-82e6-4de0-ba8f-63fb49ed2d56`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `ECUC:0a091ae2-be9b-9515-59e3-e1ccee37c364`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMRxIndicationPduRef

- **UUID**: `ECUC:1072e012-067c-4a46-a7d3-c732cc72e5fb`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the received Pdu representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 2. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 3. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 6. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 7. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 8. IpduMTxPathway

**容器属性**:

- **UUID**: `ECUC:9cdee255-853a-4712-9486-6c862bb07011`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxPathway`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters transmitted I-PDUs by the IpduM module.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. IpduMTxRequest

**容器属性**:

- **UUID**: `ECUC:0d77339e-affa-4b47-9dbc-2b2b999e0703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. IpduMIPduUnusedAreasDefault

- **UUID**: `ECUC:69073676-9fa7-4288-b2e0-3026caff1032`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IpduM module fills not used areas of an I-PDU with this bit-pattern

############ 2. IpduMTxConfirmationPduId

- **UUID**: `ECUC:258cd7c4-f9ec-4228-9e80-8c7b5065c561`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The handle Id to be used by the PduR to confirm the transmission of this Pdu.

########### FLOAT 类型参数

############ 1. IpduMTxConfirmationTimeout

- **UUID**: `ECUC:8773e2ec-6b2b-4eca-b47a-aba1d3576810`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation.

########### ENUMERATION 类型参数

############ 1. IpduMByteOrder

- **UUID**: `ECUC:9e473272-4b2e-95b2-57bf-085ed9f9b7c3`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

############ 2. IpduMTxTriggerMode

- **UUID**: `ECUC:69612ecd-3531-4049-b5c0-7524610ef2bc`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `STATIC_OR_DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `STATIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether to send the multiplexed I-PDU immediately or at some later date.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMInitialDynamicPart

- **UUID**: `ECUC:360b8673-3660-4296-bce3-e0c4f605a64e`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU.

############ 2. IpduMOutgoingPduRef

- **UUID**: `ECUC:9c9ad385-0306-44ac-a575-b5c32377b397`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU defining the outgoing I-PDU.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

########### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

############# BOOLEAN 类型参数

############## 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############## 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

############# BOOLEAN 类型参数

############## 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############## 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

################ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

########### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 2. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 3. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 6. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 9. IpduMTxRequest

**容器属性**:

- **UUID**: `ECUC:0d77339e-affa-4b47-9dbc-2b2b999e0703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `ECUC:69073676-9fa7-4288-b2e0-3026caff1032`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IpduM module fills not used areas of an I-PDU with this bit-pattern

########## 2. IpduMTxConfirmationPduId

- **UUID**: `ECUC:258cd7c4-f9ec-4228-9e80-8c7b5065c561`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The handle Id to be used by the PduR to confirm the transmission of this Pdu.

######### FLOAT 类型参数

########## 1. IpduMTxConfirmationTimeout

- **UUID**: `ECUC:8773e2ec-6b2b-4eca-b47a-aba1d3576810`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `ECUC:9e473272-4b2e-95b2-57bf-085ed9f9b7c3`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

########## 2. IpduMTxTriggerMode

- **UUID**: `ECUC:69612ecd-3531-4049-b5c0-7524610ef2bc`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `STATIC_OR_DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `STATIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether to send the multiplexed I-PDU immediately or at some later date.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMInitialDynamicPart

- **UUID**: `ECUC:360b8673-3660-4296-bce3-e0c4f605a64e`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU.

########## 2. IpduMOutgoingPduRef

- **UUID**: `ECUC:9c9ad385-0306-44ac-a575-b5c32377b397`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU defining the outgoing I-PDU.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 10. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 11. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 12. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 13. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 14. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 2. IpduMRxPathway

**容器属性**:

- **UUID**: `ECUC:7bedc87c-e833-4e9a-8ca3-ac8d731e7639`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxPathway`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters received I-PDUs by the IpduM module.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. IpduMRxIndication

**容器属性**:

- **UUID**: `ECUC:79391c0f-2367-4aaa-9fe1-0499addc12a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming RxIndication calls.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxHandleId

- **UUID**: `ECUC:0033a86b-82e6-4de0-ba8f-63fb49ed2d56`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `ECUC:0a091ae2-be9b-9515-59e3-e1ccee37c364`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMRxIndicationPduRef

- **UUID**: `ECUC:1072e012-067c-4a46-a7d3-c732cc72e5fb`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the received Pdu representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 2. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 2. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 6. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

##### 3. IpduMRxIndication

**容器属性**:

- **UUID**: `ECUC:79391c0f-2367-4aaa-9fe1-0499addc12a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxIndication`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the configuration for incoming RxIndication calls.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMRxHandleId

- **UUID**: `ECUC:0033a86b-82e6-4de0-ba8f-63fb49ed2d56`
- **参数名**: `IpduMRxHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches this value then it is unpacked according to the specification in this container.

####### ENUMERATION 类型参数

######## 1. IpduMByteOrder

- **UUID**: `ECUC:0a091ae2-be9b-9515-59e3-e1ccee37c364`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMRxIndicationPduRef

- **UUID**: `ECUC:1072e012-067c-4a46-a7d3-c732cc72e5fb`
- **引用名**: `IpduMRxIndicationPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the received Pdu representation in the ECU Configuration Description exchange file.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 2. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 3. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

##### 4. IpduMRxDynamicPart

**容器属性**:

- **UUID**: `ECUC:f1397a3c-d592-43f4-b7c2-f27fa8343387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the dynamic part of incoming RxIndication calls. When an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU for the dynamic part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. IpduMRxSelectorValue

- **UUID**: `ECUC:3f6485c6-3099-46d6-8c29-8472e98b8156`
- **参数名**: `IpduMRxSelectorValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the selector value that this container refers to.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMOutgoingDynamicPduRef

- **UUID**: `ECUC:4e7f0043-612c-4d35-b62a-db8642482b3e`
- **引用名**: `IpduMOutgoingDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent PDU representation in the ECU Configuration Description exchange file.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:d5fbfafb-4179-84a3-5b98-49b555b0dcf8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `ECUC:71341c72-5251-d1df-199a-529813c95762`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `ECUC:bcca77f4-d678-cded-10e1-da764dd064cb`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 6. IpduMRxStaticPart

**容器属性**:

- **UUID**: `ECUC:4928f0b1-4227-4382-a2e5-c6dc41caf280`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMRxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration for the static part of incoming RxIndication calls. On reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMOutgoingStaticPduRef

- **UUID**: `ECUC:0e3f6906-b529-4773-b5dc-18f321d17d07`
- **引用名**: `IpduMOutgoingStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When the new I-PDU is sent out it is sent with this I-PDU ID. Reference to the sent Pdu representation in the ECU Configuration Description exchange file.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 7. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:2deb716f-ae0e-8431-46bb-1e11ef479bf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `ECUC:c92392e6-bee6-d16d-04bd-26f4ad60165b`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `ECUC:14b9ee69-430d-cd7b-fc04-aed2e76723c4`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 8. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:7812a762-87eb-986f-2dc8-b97e52a6cd82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:f25ae367-aac9-e609-e486-87a52b031fdd`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

######## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:b542e6ee-166c-e294-bddc-23c4350a221e`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

##### 9. IpduMTxPathway

**容器属性**:

- **UUID**: `ECUC:9cdee255-853a-4712-9486-6c862bb07011`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxPathway`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Contains the configuration parameters transmitted I-PDUs by the IpduM module.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. IpduMTxRequest

**容器属性**:

- **UUID**: `ECUC:0d77339e-affa-4b47-9dbc-2b2b999e0703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `ECUC:69073676-9fa7-4288-b2e0-3026caff1032`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IpduM module fills not used areas of an I-PDU with this bit-pattern

########## 2. IpduMTxConfirmationPduId

- **UUID**: `ECUC:258cd7c4-f9ec-4228-9e80-8c7b5065c561`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The handle Id to be used by the PduR to confirm the transmission of this Pdu.

######### FLOAT 类型参数

########## 1. IpduMTxConfirmationTimeout

- **UUID**: `ECUC:8773e2ec-6b2b-4eca-b47a-aba1d3576810`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation.

######### ENUMERATION 类型参数

########## 1. IpduMByteOrder

- **UUID**: `ECUC:9e473272-4b2e-95b2-57bf-085ed9f9b7c3`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

########## 2. IpduMTxTriggerMode

- **UUID**: `ECUC:69612ecd-3531-4049-b5c0-7524610ef2bc`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `STATIC_OR_DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `STATIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether to send the multiplexed I-PDU immediately or at some later date.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMInitialDynamicPart

- **UUID**: `ECUC:360b8673-3660-4296-bce3-e0c4f605a64e`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU.

########## 2. IpduMOutgoingPduRef

- **UUID**: `ECUC:9c9ad385-0306-44ac-a575-b5c32377b397`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU defining the outgoing I-PDU.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

############ 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

######### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

########### BOOLEAN 类型参数

############ 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

############ 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

######### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 2. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 3. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 6. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 10. IpduMTxRequest

**容器属性**:

- **UUID**: `ECUC:0d77339e-affa-4b47-9dbc-2b2b999e0703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxRequest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This is used to specify the configuration for Transmit requests.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. IpduMIPduUnusedAreasDefault

- **UUID**: `ECUC:69073676-9fa7-4288-b2e0-3026caff1032`
- **参数名**: `IpduMIPduUnusedAreasDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IpduM module fills not used areas of an I-PDU with this bit-pattern

######## 2. IpduMTxConfirmationPduId

- **UUID**: `ECUC:258cd7c4-f9ec-4228-9e80-8c7b5065c561`
- **参数名**: `IpduMTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The handle Id to be used by the PduR to confirm the transmission of this Pdu.

####### FLOAT 类型参数

######## 1. IpduMTxConfirmationTimeout

- **UUID**: `ECUC:8773e2ec-6b2b-4eca-b47a-aba1d3576810`
- **参数名**: `IpduMTxConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This timeout (in seconds) defines the timeout period for monitoring the reception of the TxConfirmation.

####### ENUMERATION 类型参数

######## 1. IpduMByteOrder

- **UUID**: `ECUC:9e473272-4b2e-95b2-57bf-085ed9f9b7c3`
- **参数名**: `IpduMByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for the selectorField within the MultiplexedPdu.

######## 2. IpduMTxTriggerMode

- **UUID**: `ECUC:69612ecd-3531-4049-b5c0-7524610ef2bc`
- **参数名**: `IpduMTxTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `STATIC_OR_DYNAMIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
  - `STATIC_PART_TRIGGER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether to send the multiplexed I-PDU immediately or at some later date.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMInitialDynamicPart

- **UUID**: `ECUC:360b8673-3660-4296-bce3-e0c4f605a64e`
- **引用名**: `IpduMInitialDynamicPart`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `IpduMTxDynamicPart`
- **完整路径**: `/AUTOSAR/EcucDefs/IpduM/IpduMConfig/IpduMTxPathway/IpduMTxRequest/IpduMTxDynamicPart`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the dynamic part that shall be used to initialize this multiplexed TX-I-PDU.

######## 2. IpduMOutgoingPduRef

- **UUID**: `ECUC:9c9ad385-0306-44ac-a575-b5c32377b397`
- **引用名**: `IpduMOutgoingPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU defining the outgoing I-PDU.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

########## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

####### 2. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 3. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 4. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

######### BOOLEAN 类型参数

########## 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

########## 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

############ 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

####### 5. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 11. IpduMSelectorFieldPosition

**容器属性**:

- **UUID**: `ECUC:0c50bef2-147e-990c-2ba3-e0103e68c1e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSelectorFieldPosition`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of the selector field.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSelectorFieldLength

- **UUID**: `ECUC:8698faf7-375c-e6a6-e261-ae3716c5143c`
- **参数名**: `IpduMSelectorFieldLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the selector field in bits.

######## 2. IpduMSelectorFieldPosition

- **UUID**: `ECUC:4980fe7d-a2ff-e331-bbb7-4a5620cc167d`
- **参数名**: `IpduMSelectorFieldPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selector field bit position in the multiplexed Pdu.

##### 12. IpduMTxDynamicPart

**容器属性**:

- **UUID**: `ECUC:3796101d-e7a3-4b52-98c6-f1127db9a143`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxDynamicPart`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the dynamic part.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IpduMTxDynamicHandleId

- **UUID**: `ECUC:6387c164-c4f0-42c4-b7ef-3d03708e8e86`
- **参数名**: `IpduMTxDynamicHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.

####### BOOLEAN 类型参数

######## 1. IpduMJitUpdate

- **UUID**: `ECUC:d09eccc9-8102-9927-19b6-15b5f18d8936`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

######## 2. IpduMTxDynamicConfirmation

- **UUID**: `ECUC:b6ce8ccd-e819-4c1d-82a5-1a795a79cdf2`
- **参数名**: `IpduMTxDynamicConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the dynamic part is generated.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMTxDynamicPduRef

- **UUID**: `ECUC:ccb1bc43-ddaa-499b-a564-619481758ef8`
- **引用名**: `IpduMTxDynamicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 13. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:1c5890dc-538a-8c01-3c9c-48482b364ab4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `ECUC:b790b253-6462-d93d-fa9e-512ae94ec51e`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `ECUC:03270dd5-e889-d54b-f1e5-d9092355d287`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 14. IpduMTxStaticPart

**容器属性**:

- **UUID**: `ECUC:2e0c7ae8-2ee8-4e7b-8199-63de477c9b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMTxStaticPart`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This container is used for the static part of a TxRequest configuration. Therefore, for each outgoing I-PDU there will be one instance of this container for the static part if it exists.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. IpduMTxStaticHandleId

- **UUID**: `ECUC:70025d88-e703-48fd-bf16-be6df3b135db`
- **参数名**: `IpduMTxStaticHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.

####### BOOLEAN 类型参数

######## 1. IpduMJitUpdate

- **UUID**: `ECUC:c7153793-c847-9c50-0288-8881bb508325`
- **参数名**: `IpduMJitUpdate`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of the PduR.

######## 2. IpduMTxStaticConfirmation

- **UUID**: `ECUC:4ce07ee5-1ee2-4cb7-a88e-a1a5fbc52dcb`
- **参数名**: `IpduMTxStaticConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A transmit request can be confirmed by the lower layer. If this parameter is set to true a confirmation of the I-PDU in COM representing the static part is generated.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. IpduMTxStaticPduRef

- **UUID**: `ECUC:1e7ba123-6e03-4f9c-b63c-cb74d7b31a9c`
- **引用名**: `IpduMTxStaticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Pdu representation in the ECU Configuration Description exchange file to be transmitted.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

########## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 15. IpduMSegment

**容器属性**:

- **UUID**: `ECUC:12cefba6-9acf-8f2a-256e-bb13f4f944a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMSegment`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This contains the location and the length of a segment. A segment must fit inside the I-PDU. The segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same position in the destination I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. IpduMSegmentLength

- **UUID**: `ECUC:ae071d1d-aba7-dc66-e370-c3f6b311bf0d`
- **参数名**: `IpduMSegmentLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2032]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the segment in bits.

######## 2. IpduMSegmentPosition

- **UUID**: `ECUC:f99d78a0-2fce-d874-dab8-4bd4ed18cc76`
- **参数名**: `IpduMSegmentPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Segments bit position in the multiplexed Pdu.

##### 16. IpduMGeneral

**容器属性**:

- **UUID**: `ECUC:315d58cd-393b-43c9-9743-757f43d5e78e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Contains the general configuration parameters of IpduM.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. IpduMDevErrorDetect

- **UUID**: `ECUC:2ab08891-5dd2-4861-8432-8aedd0b61dfe`
- **参数名**: `IpduMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Active/Deactivate the detection of development errors, for production code this parameter has to be False.

######## 2. IpduMStaticPartExists

- **UUID**: `ECUC:9974a5d3-b6a8-4d53-98a8-415803a91d78`
- **参数名**: `IpduMStaticPartExists`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is to allow optimizations in the case the IpduM will never be used with a static part.

######## 3. IpduMVersionInfoApi

- **UUID**: `ECUC:c3f380d8-b5fb-4fe4-a1ef-fc16979aaed6`
- **参数名**: `IpduMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Active/Deactivate the version information API.

####### FLOAT 类型参数

######## 1. IpduMConfigurationTimeBase

- **UUID**: `ECUC:f674624b-eb02-4426-bda6-e01d27e1c4f2`
- **参数名**: `IpduMConfigurationTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..3600]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The cycle time with which IpduM_MainFunction should  be invoked (in seconds).

##### 17. IpduMPublishedInformation

**容器属性**:

- **UUID**: `ECUC:e49398c4-0f28-425e-8177-a0d5623eccfe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpduMPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. IpduMRxDirectComInvocation

- **UUID**: `ECUC:7624ef7a-7214-43a6-96a5-a30a54b6af64`
- **参数名**: `IpduMRxDirectComInvocation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-LINK-TIME
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: If set to TRUE the COM invocation optimization as defined in

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

1. **IpduM**
