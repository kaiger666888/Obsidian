# SecOC - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:30

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [SecOC](#secoc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. SecOC

#### 基本信息

- **UUID**: `ECUC:916e6567-92b2-4cc2-b45f-5a34c3daf255`
- **模块名称**: `SecOC`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the SecOC (SecureOnboardCommunication) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.3.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. SecOCGeneral

**容器属性**:

- **UUID**: `ECUC:d974b231-dfd7-4419-9f0d-489b957b765b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCGeneral`
- **多重性**: [1..1]

**容器描述**:

Contains the general configuration parameters of the SecOC module.

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. SecOCDevErrorDetect

- **UUID**: `ECUC:b350a403-5388-4f68-9cf1-1c1349445692`
- **参数名**: `SecOCDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the development error detection and notification on or off.

######## 2. SecOCEnableForcedPassOverride

- **UUID**: `ECUC:f820fbce-18ab-47c5-8f88-9dee469bc75b`
- **参数名**: `SecOCEnableForcedPassOverride`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: When this configuration option is set to TRUE then the functionality inside the function SecOC_VerifyStatusOverride to forcibly override the VerifyStatus to "Pass" is enabled.

######## 3. SecOcIgnoreVerificationResult

- **UUID**: `ECUC:c2015929-5526-4d40-9671-12984967fec0`
- **参数名**: `SecOcIgnoreVerificationResult`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The result of the authentication process (e.g. MAC Verify) is ignored after the first try and the SecOC proceeds like the result was a success. The calculation of the authenticator is still done, only its result will be ignored.

######## 4. SecOCVersionInfoApi

- **UUID**: `ECUC:6a9ce3ed-77e5-4cd3-bbb9-6f22ed1626a1`
- **参数名**: `SecOCVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If true the SecOC_GetVersionInfo API is available.

####### FLOAT 类型参数

######## 1. SecOCMainFunctionPeriodRx

- **UUID**: `ECUC:e98911f2-9c55-4584-9857-8426b140cf41`
- **参数名**: `SecOCMainFunctionPeriodRx`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allows to configure the time for the MainFunction of the Rx path (as float in seconds).

######## 2. SecOCMainFunctionPeriodTx

- **UUID**: `ECUC:db84819e-b5d4-4e04-a976-3c892b5ce0df`
- **参数名**: `SecOCMainFunctionPeriodTx`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allows to configure the time for the MainFunction of the Tx path (as float in seconds).

####### STRING 类型参数

######## 1. SecOCMaxAlignScalarType

- **UUID**: `ECUC:a7746493-ddf2-45f5-bdbc-410ccc7aff78`
- **参数名**: `SecOCMaxAlignScalarType`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: The scalar type which has the maximum alignment restrictions on the given platform. This type can be e.g. uint8, uint16 or uint32.

####### ENUMERATION 类型参数

######## 1. SecOCQueryFreshnessValue

- **UUID**: `ECUC:632d9b52-9ebb-4611-9175-413ffce45c70`
- **参数名**: `SecOCQueryFreshnessValue`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CFUNC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CFUNC` (来源: AUTOSAR_ECUC)
  - `RTE` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies if the freshness value shall be determined through a C-function (CD) or a software component (SW-C).

####### FUNCTION-NAME 类型参数

######## 1. SecOCVerificationStatusCallout

- **UUID**: `ECUC:88f43685-965b-48a5-99cd-724c925ab9bc`
- **参数名**: `SecOCVerificationStatusCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Entry address of the customer specific call out routine which shall be invoked in case of a verification attempt.

##### 2. SecOCRxPduProcessing

**容器属性**:

- **UUID**: `ECUC:84ac6f7d-9b6b-4033-afe4-6ea5dcd6b15d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxPduProcessing`
- **多重性**: [0..infinite]

**容器描述**:

Contains the parameters to configure the RxPdus to be verified by the SecOC module.

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. SecOCAuthDataFreshnessLen

- **UUID**: `ECUC:15c4140f-6852-47c5-aa8c-5341962e605c`
- **参数名**: `SecOCAuthDataFreshnessLen`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The length of the external authentic PDU data in bits (uint16).

######## 2. SecOCAuthDataFreshnessStartPosition

- **UUID**: `ECUC:6b514eaf-8659-49bf-837c-4b233cfb8213`
- **参数名**: `SecOCAuthDataFreshnessStartPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value determines the start position in bits (uint16) of the Authentic PDU that shall be passed on to the Freshness SWC. The bit position starts counting from the MSB of the first byte of the PDU.

######## 3. SecOCAuthenticationBuildAttempts

- **UUID**: `ECUC:939f4eb8-2949-8394-6695-55513ba98481`
- **参数名**: `SecOCAuthenticationBuildAttempts`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the number of authentication build attempts.

######## 4. SecOCAuthenticationVerifyAttempts

- **UUID**: `ECUC:62039fef-5c98-42f5-8204-42b14fee133c`
- **参数名**: `SecOCAuthenticationVerifyAttempts`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the number of authentication verify attempts that are to be carried out when the verification of the authentication information failed for a given Secured I-PDU. If zero is set, then only one authentication verification attempt is done.

######## 5. SecOCAuthInfoTxLength

- **UUID**: `ECUC:1d737833-2f08-8744-4b14-5954fb59a1d9`
- **参数名**: `SecOCAuthInfoTxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the length in bits of the authentication code to be included in the payload of the Secured I-PDU.

######## 6. SecOCDataId

- **UUID**: `ECUC:62a5b06c-7e84-8fef-5f12-44cc3ef04d4f`
- **参数名**: `SecOCDataId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines a unique numerical identifier for the Secured I-PDU.

######## 7. SecOCFreshnessValueId

- **UUID**: `ECUC:7e2042fb-6eaf-8b3c-5bc5-6746e75a807f`
- **参数名**: `SecOCFreshnessValueId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the Id of the Freshness Value.

######## 8. SecOCFreshnessValueLength

- **UUID**: `ECUC:0325c14a-6710-89b7-6789-82ba4a4c96f1`
- **参数名**: `SecOCFreshnessValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..64]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the complete length in bits of the Freshness Value. As long as the key doesn't change the counter shall not overflow. The length of the counter shall be determined based on the expected life time of the corresponding key and frequency of usage of the counter.

######## 9. SecOCFreshnessValueTxLength

- **UUID**: `ECUC:b30f81b7-9bab-8d92-6a67-e79c10523977`
- **参数名**: `SecOCFreshnessValueTxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..64]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the length in bits of the Freshness Value to be included in the payload of the Secured I-PDU. This length is specific to the least significant bits of the complete Freshness Counter. If the parameter is 0 no Freshness Value is included in the Secured I-PDU.

######## 10. SecOCReceptionQueueSize

- **UUID**: `ECUC:c3a4683e-b733-4ff7-8987-301a8ff7e55c`
- **参数名**: `SecOCReceptionQueueSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the queue size in case the overflow strategy for receiving PDUs is set to QUEUE.

####### BOOLEAN 类型参数

######## 1. SecOCUseAuthDataFreshness

- **UUID**: `ECUC:b7d5a803-39a6-4c32-8b4d-1bb409518e01`
- **参数名**: `SecOCUseAuthDataFreshness`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: A Boolean value that indicates if a part of the Authentic-PDU shall be passed on to the SWC that verifies and generates the Freshness. If it is set to TRUE, the values SecOCAuthDataFreshnessStartPosition and SecOCAuthDataFreshnessLen must be set to specify the bit position and length within the Authentic-PDU.

####### ENUMERATION 类型参数

######## 1. SecOCReceptionOverflowStrategy

- **UUID**: `ECUC:9aab4468-17ce-4921-b104-eaa693a18107`
- **参数名**: `SecOCReceptionOverflowStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `QUEUE` (来源: AUTOSAR_ECUC)
  - `REJECT` (来源: AUTOSAR_ECUC)
  - `REPLACE` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines the overflow strategy for receiving PDUs

######## 2. SecOCVerificationStatusPropagationMode

- **UUID**: `ECUC:f3484e24-4b91-438e-bb7c-4bc7469c5ca7`
- **参数名**: `SecOCVerificationStatusPropagationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BOTH` (来源: AUTOSAR_ECUC)
  - `FAILURE_ONLY` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
- **描述**: This parameter is used to describe the propagation of the status of each verification attempt from the SecOC module to SWCs.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCSameBufferPduRef

- **UUID**: `ECUC:e2fdffb8-2e63-869a-340b-807e017f95be`
- **引用名**: `SecOCSameBufferPduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SecOCSameBufferPduCollection`
- **完整路径**: `/AUTOSAR/EcucDefs/SecOC/SecOCSameBufferPduCollection`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This reference is used to collect Pdus that are using the same SecOC buffer.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SecOCRxAuthServiceConfigRef

- **UUID**: `ECUC:135e1ad2-b132-4b29-b4f7-577ceba4d50f`
- **引用名**: `SecOCRxAuthServiceConfigRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference is used to define which crypto service function is called for authentication.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. SecOCRxAuthenticPduLayer

**容器属性**:

- **UUID**: `ECUC:fe87ddb5-fcdc-45ff-ba4b-d688a3943e5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPduLayer`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was verified.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. SecOCPduType

- **UUID**: `ECUC:c7a83543-ecfc-8780-5f35-903027fca582`
- **参数名**: `SecOCPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SECOC_IFPDU` (来源: AUTOSAR_ECUC)
  - `SECOC_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines API Type to use for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxAuthenticLayerPduRef

- **UUID**: `ECUC:8a365fa6-92e8-426b-83ce-2447690ce342`
- **引用名**: `SecOCRxAuthenticLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 2. SecOCRxSecuredPdu

**容器属性**:

- **UUID**: `ECUC:eec91efc-2ddf-4d96-9944-f966b70fb710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxSecuredPdu`
- **多重性**: [0..1]

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCRxSecuredLayerPduId

- **UUID**: `ECUC:4e926dd6-0c6f-4ac2-8abb-5ed5687c5a69`
- **参数名**: `SecOCRxSecuredLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxSecuredLayerPduRef

- **UUID**: `ECUC:ee06badc-d404-4032-afa3-f09f8849e756`
- **引用名**: `SecOCRxSecuredLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 3. SecOCRxSecuredPduCollection

**容器属性**:

- **UUID**: `ECUC:f9ab58b5-f3c8-435f-a0f9-cabfafd185bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxSecuredPduCollection`
- **多重性**: [0..1]

**容器描述**:

This container specifies two Pdus that are received by the SecOC module from the PduR and a message linking between them.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SecOCRxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SecOCRxAuthenticPduId

- **UUID**: `ECUC:20339ed9-a5f9-40e8-a20d-72cc560a0090`
- **参数名**: `SecOCRxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SecOCRxAuthenticPduRef

- **UUID**: `ECUC:df07be45-f938-4937-802c-15353271afe9`
- **引用名**: `SecOCRxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

######### 2. SecOCRxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SecOCRxCryptographicPduId

- **UUID**: `ECUC:f0f03b01-0ca7-499a-b8b8-d9ab68829e13`
- **参数名**: `SecOCRxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SecOCRxCryptographicPduRef

- **UUID**: `ECUC:408b66b0-5a3a-4c10-ae65-2a94f557e26a`
- **引用名**: `SecOCRxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

######### 3. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SecOCMessageLinkLen

- **UUID**: `ECUC:e8019d75-51c9-c9b7-dc27-a7075822d745`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

############ 2. SecOCMessageLinkPos

- **UUID**: `ECUC:d0abe4b3-c06a-d228-dd24-a2d98e7b5cf3`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

####### 4. SecOCRxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCRxAuthenticPduId

- **UUID**: `ECUC:20339ed9-a5f9-40e8-a20d-72cc560a0090`
- **参数名**: `SecOCRxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxAuthenticPduRef

- **UUID**: `ECUC:df07be45-f938-4937-802c-15353271afe9`
- **引用名**: `SecOCRxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 5. SecOCRxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCRxCryptographicPduId

- **UUID**: `ECUC:f0f03b01-0ca7-499a-b8b8-d9ab68829e13`
- **参数名**: `SecOCRxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxCryptographicPduRef

- **UUID**: `ECUC:408b66b0-5a3a-4c10-ae65-2a94f557e26a`
- **引用名**: `SecOCRxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 6. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:e8019d75-51c9-c9b7-dc27-a7075822d745`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

########## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:d0abe4b3-c06a-d228-dd24-a2d98e7b5cf3`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

####### 7. SecOCRxSecuredPduLayer

**容器属性**:

- **UUID**: `ECUC:0d17ebb7-f591-4e4e-b2f0-0ccedce78b25`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SecOCRxSecuredPduLayer`
- **多重性**: [1..1]

**容器选择**:

- **SecOCRxSecuredPdu**
  - UUID: `ECUC:eec91efc-2ddf-4d96-9944-f966b70fb710`
  - 描述: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.
- **SecOCRxSecuredPduCollection**
  - UUID: `ECUC:f9ab58b5-f3c8-435f-a0f9-cabfafd185bb`
  - 描述: This container specifies two Pdus that are received by the SecOC module from the PduR and a message linking between them.
- **SecOCRxAuthenticPdu**
  - UUID: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
  - 描述: This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.
- **SecOCRxCryptographicPdu**
  - UUID: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
  - 描述: This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.
- **SecOCUseMessageLink**
  - UUID: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
  - 描述: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.

##### 3. SecOCRxAuthenticPduLayer

**容器属性**:

- **UUID**: `ECUC:fe87ddb5-fcdc-45ff-ba4b-d688a3943e5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPduLayer`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was verified.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. SecOCPduType

- **UUID**: `ECUC:c7a83543-ecfc-8780-5f35-903027fca582`
- **参数名**: `SecOCPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SECOC_IFPDU` (来源: AUTOSAR_ECUC)
  - `SECOC_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines API Type to use for communication with PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCRxAuthenticLayerPduRef

- **UUID**: `ECUC:8a365fa6-92e8-426b-83ce-2447690ce342`
- **引用名**: `SecOCRxAuthenticLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 4. SecOCRxSecuredPdu

**容器属性**:

- **UUID**: `ECUC:eec91efc-2ddf-4d96-9944-f966b70fb710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxSecuredPdu`
- **多重性**: [0..1]

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCRxSecuredLayerPduId

- **UUID**: `ECUC:4e926dd6-0c6f-4ac2-8abb-5ed5687c5a69`
- **参数名**: `SecOCRxSecuredLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCRxSecuredLayerPduRef

- **UUID**: `ECUC:ee06badc-d404-4032-afa3-f09f8849e756`
- **引用名**: `SecOCRxSecuredLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 5. SecOCRxSecuredPduCollection

**容器属性**:

- **UUID**: `ECUC:f9ab58b5-f3c8-435f-a0f9-cabfafd185bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxSecuredPduCollection`
- **多重性**: [0..1]

**容器描述**:

This container specifies two Pdus that are received by the SecOC module from the PduR and a message linking between them.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SecOCRxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCRxAuthenticPduId

- **UUID**: `ECUC:20339ed9-a5f9-40e8-a20d-72cc560a0090`
- **参数名**: `SecOCRxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxAuthenticPduRef

- **UUID**: `ECUC:df07be45-f938-4937-802c-15353271afe9`
- **引用名**: `SecOCRxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 2. SecOCRxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCRxCryptographicPduId

- **UUID**: `ECUC:f0f03b01-0ca7-499a-b8b8-d9ab68829e13`
- **参数名**: `SecOCRxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCRxCryptographicPduRef

- **UUID**: `ECUC:408b66b0-5a3a-4c10-ae65-2a94f557e26a`
- **引用名**: `SecOCRxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 3. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:e8019d75-51c9-c9b7-dc27-a7075822d745`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

########## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:d0abe4b3-c06a-d228-dd24-a2d98e7b5cf3`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

##### 6. SecOCRxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCRxAuthenticPduId

- **UUID**: `ECUC:20339ed9-a5f9-40e8-a20d-72cc560a0090`
- **参数名**: `SecOCRxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCRxAuthenticPduRef

- **UUID**: `ECUC:df07be45-f938-4937-802c-15353271afe9`
- **引用名**: `SecOCRxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 7. SecOCRxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCRxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCRxCryptographicPduId

- **UUID**: `ECUC:f0f03b01-0ca7-499a-b8b8-d9ab68829e13`
- **参数名**: `SecOCRxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for SecOC_PduRRxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCRxCryptographicPduRef

- **UUID**: `ECUC:408b66b0-5a3a-4c10-ae65-2a94f557e26a`
- **引用名**: `SecOCRxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 8. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:e8019d75-51c9-c9b7-dc27-a7075822d745`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

######## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:d0abe4b3-c06a-d228-dd24-a2d98e7b5cf3`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

##### 9. SecOCSameBufferPduCollection

**容器属性**:

- **UUID**: `ECUC:38a259eb-8522-47b9-8d04-b2ccdf116e02`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCSameBufferPduCollection`
- **多重性**: [0..infinite]

**容器描述**:

SecOCBuffer configuration that may be used by a collection of Pdus.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCBufferLength

- **UUID**: `ECUC:ce097fa0-d6cf-4f98-ba0f-726d0ee6803e`
- **参数名**: `SecOCBufferLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the Buffer in bytes that is used by the SecOC module.

##### 10. SecOCTxPduProcessing

**容器属性**:

- **UUID**: `ECUC:bd305409-5c26-4f43-bf5d-6efdb81e535b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxPduProcessing`
- **多重性**: [0..infinite]

**容器描述**:

Contains the parameters to configure the TxPdus to be secured by the SecOC module.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. SecOCAuthenticationBuildAttempts

- **UUID**: `ECUC:cc233343-ea04-92a4-760e-55a916f1267f`
- **参数名**: `SecOCAuthenticationBuildAttempts`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the number of authentication build attempts.

######## 2. SecOCAuthInfoTxLength

- **UUID**: `ECUC:55f75cbe-efc3-9654-5a8d-59acd6a143d7`
- **参数名**: `SecOCAuthInfoTxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the length in bits of the authentication code to be included in the payload of the Secured I-PDU.

######## 3. SecOCDataId

- **UUID**: `ECUC:9b2994f8-3f3f-9eff-6e8b-45241a37ef4d`
- **参数名**: `SecOCDataId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines a unique numerical identifier for the Secured I-PDU.

######## 4. SecOCFreshnessValueId

- **UUID**: `ECUC:b6a42787-2f6a-9a4c-6b3e-679ec2a2227d`
- **参数名**: `SecOCFreshnessValueId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the Id of the Freshness Value.

######## 5. SecOCFreshnessValueLength

- **UUID**: `ECUC:3ba9a5d6-27cb-98c7-7702-8312259438ef`
- **参数名**: `SecOCFreshnessValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..64]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the complete length in bits of the Freshness Value. As long as the key doesn't change the counter shall not overflow. The length of the counter shall be determined based on the expected life time of the corresponding key and frequency of usage of the counter.

######## 6. SecOCFreshnessValueTxLength

- **UUID**: `ECUC:eb936643-5c66-9ca2-79e0-e7f3eb99db75`
- **参数名**: `SecOCFreshnessValueTxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..64]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the length in bits of the Freshness Value to be included in the payload of the Secured I-PDU. This length is specific to the least significant bits of the complete Freshness Counter. If the parameter is 0 no Freshness Value is included in the Secured I-PDU.

####### BOOLEAN 类型参数

######## 1. SecOCProvideTxTruncatedFreshnessValue

- **UUID**: `ECUC:04f3b3b9-6144-4f28-8f86-529fd6db25cd`
- **参数名**: `SecOCProvideTxTruncatedFreshnessValue`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies if the Tx query freshness function provides the truncated freshness info instead of generating this by SecOC In this case, SecOC shall add this data to the Authentic PDU instead of truncating the freshness value.

######## 2. SecOCUseTxConfirmation

- **UUID**: `ECUC:1cf993ac-e97a-4695-939f-d9a66e0d812a`
- **参数名**: `SecOCUseTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: A Boolean value that indicates if the function SecOC_SPduTxConfirmation shall be called for this PDU.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCSameBufferPduRef

- **UUID**: `ECUC:1b81e443-ef1e-95aa-4384-80d5dcc737bc`
- **引用名**: `SecOCSameBufferPduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `SecOCSameBufferPduCollection`
- **完整路径**: `/AUTOSAR/EcucDefs/SecOC/SecOCSameBufferPduCollection`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This reference is used to collect Pdus that are using the same SecOC buffer.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SecOCTxAuthServiceConfigRef

- **UUID**: `ECUC:0e085d61-00be-4364-841d-fb7fdc670ed7`
- **引用名**: `SecOCTxAuthServiceConfigRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **来源**: AUTOSAR_ECUC
- **描述**: This reference is used to define which crypto service function is called for authentication.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. SecOCTxAuthenticPduLayer

**容器属性**:

- **UUID**: `ECUC:88fc782a-117f-4db3-88d6-e3e263ea3988`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPduLayer`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac generation is provided.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxAuthenticLayerPduId

- **UUID**: `ECUC:6d3ef2f7-0768-4e56-8ed5-25d006a9b48b`
- **参数名**: `SecOCTxAuthenticLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRTransmit.

######### ENUMERATION 类型参数

########## 1. SecOCPduType

- **UUID**: `ECUC:521ccfb8-019f-8f34-2dc0-9d89e852a0ad`
- **参数名**: `SecOCPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SECOC_IFPDU` (来源: AUTOSAR_ECUC)
  - `SECOC_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines API Type to use for communication with PduR.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxAuthenticLayerPduRef

- **UUID**: `ECUC:f3889cc4-627c-4e47-b2e0-8936f0298dd1`
- **引用名**: `SecOCTxAuthenticLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 2. SecOCTxSecuredPdu

**容器属性**:

- **UUID**: `ECUC:7cbe5ea3-b956-4f43-8865-2d9eef01d0bd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxSecuredPdu`
- **多重性**: [0..1]

**容器描述**:

This container specifies one Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. This Pdu contains the cryptographic information.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxSecuredLayerPduId

- **UUID**: `ECUC:37a3a0b7-9500-4659-92c0-0100526f02ac`
- **参数名**: `SecOCTxSecuredLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxSecuredLayerPduRef

- **UUID**: `ECUC:f4f69e53-8605-4d16-acbe-45db1e6eb0d4`
- **引用名**: `SecOCTxSecuredLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 3. SecOCTxSecuredPduCollection

**容器属性**:

- **UUID**: `ECUC:818bd2c9-6dbe-4382-8b0b-9864ae0016a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxSecuredPduCollection`
- **多重性**: [0..1]

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. Two separate Pdus are transmitted to the PduR:

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SecOCTxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SecOCTxAuthenticPduId

- **UUID**: `ECUC:fd73c019-8d14-4d07-a5d9-bc9f6af4f2c0`
- **参数名**: `SecOCTxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SecOCTxAuthenticPduRef

- **UUID**: `ECUC:abab787a-645e-4ad0-af50-f59116b3586d`
- **引用名**: `SecOCTxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

######### 2. SecOCTxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SecOCTxCryptographicPduId

- **UUID**: `ECUC:4bcd8e92-7491-4724-8868-e8961ffccc6c`
- **参数名**: `SecOCTxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SecOCTxCryptographicPduRef

- **UUID**: `ECUC:f4745072-90e6-4aa3-9005-6d676efba509`
- **引用名**: `SecOCTxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

######### 3. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SecOCMessageLinkLen

- **UUID**: `ECUC:6fe21788-cbbf-c9da-c639-74ac56516832`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

############ 2. SecOCMessageLinkPos

- **UUID**: `ECUC:588c5ec7-3a60-d24b-c736-707e8ca9ede0`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

####### 4. SecOCTxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxAuthenticPduId

- **UUID**: `ECUC:fd73c019-8d14-4d07-a5d9-bc9f6af4f2c0`
- **参数名**: `SecOCTxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxAuthenticPduRef

- **UUID**: `ECUC:abab787a-645e-4ad0-af50-f59116b3586d`
- **引用名**: `SecOCTxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 5. SecOCTxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxCryptographicPduId

- **UUID**: `ECUC:4bcd8e92-7491-4724-8868-e8961ffccc6c`
- **参数名**: `SecOCTxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxCryptographicPduRef

- **UUID**: `ECUC:f4745072-90e6-4aa3-9005-6d676efba509`
- **引用名**: `SecOCTxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 6. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:6fe21788-cbbf-c9da-c639-74ac56516832`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

########## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:588c5ec7-3a60-d24b-c736-707e8ca9ede0`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

####### 7. SecOCTxSecuredPduLayer

**容器属性**:

- **UUID**: `ECUC:f28c4013-a122-48f9-8116-a9c2e70746e8`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SecOCTxSecuredPduLayer`
- **多重性**: [1..1]

**容器选择**:

- **SecOCTxSecuredPdu**
  - UUID: `ECUC:7cbe5ea3-b956-4f43-8865-2d9eef01d0bd`
  - 描述: This container specifies one Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. This Pdu contains the cryptographic information.
- **SecOCTxSecuredPduCollection**
  - UUID: `ECUC:818bd2c9-6dbe-4382-8b0b-9864ae0016a8`
  - 描述: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. Two separate Pdus are transmitted to the PduR:
- **SecOCTxAuthenticPdu**
  - UUID: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
  - 描述: This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.
- **SecOCTxCryptographicPdu**
  - UUID: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
  - 描述: This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.
- **SecOCUseMessageLink**
  - UUID: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
  - 描述: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

##### 11. SecOCTxAuthenticPduLayer

**容器属性**:

- **UUID**: `ECUC:88fc782a-117f-4db3-88d6-e3e263ea3988`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPduLayer`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac generation is provided.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SecOCTxAuthenticLayerPduId

- **UUID**: `ECUC:6d3ef2f7-0768-4e56-8ed5-25d006a9b48b`
- **参数名**: `SecOCTxAuthenticLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for SecOC_PduRTransmit.

####### ENUMERATION 类型参数

######## 1. SecOCPduType

- **UUID**: `ECUC:521ccfb8-019f-8f34-2dc0-9d89e852a0ad`
- **参数名**: `SecOCPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SECOC_IFPDU` (来源: AUTOSAR_ECUC)
  - `SECOC_TPPDU` (来源: AUTOSAR_ECUC)
- **描述**: This parameter defines API Type to use for communication with PduR.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCTxAuthenticLayerPduRef

- **UUID**: `ECUC:f3889cc4-627c-4e47-b2e0-8936f0298dd1`
- **引用名**: `SecOCTxAuthenticLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 12. SecOCTxSecuredPdu

**容器属性**:

- **UUID**: `ECUC:7cbe5ea3-b956-4f43-8865-2d9eef01d0bd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxSecuredPdu`
- **多重性**: [0..1]

**容器描述**:

This container specifies one Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. This Pdu contains the cryptographic information.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCTxSecuredLayerPduId

- **UUID**: `ECUC:37a3a0b7-9500-4659-92c0-0100526f02ac`
- **参数名**: `SecOCTxSecuredLayerPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCTxSecuredLayerPduRef

- **UUID**: `ECUC:f4f69e53-8605-4d16-acbe-45db1e6eb0d4`
- **引用名**: `SecOCTxSecuredLayerPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 13. SecOCTxSecuredPduCollection

**容器属性**:

- **UUID**: `ECUC:818bd2c9-6dbe-4382-8b0b-9864ae0016a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxSecuredPduCollection`
- **多重性**: [0..1]

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. Two separate Pdus are transmitted to the PduR:

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SecOCTxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxAuthenticPduId

- **UUID**: `ECUC:fd73c019-8d14-4d07-a5d9-bc9f6af4f2c0`
- **参数名**: `SecOCTxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxAuthenticPduRef

- **UUID**: `ECUC:abab787a-645e-4ad0-af50-f59116b3586d`
- **引用名**: `SecOCTxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 2. SecOCTxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SecOCTxCryptographicPduId

- **UUID**: `ECUC:4bcd8e92-7491-4724-8868-e8961ffccc6c`
- **参数名**: `SecOCTxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SecOCTxCryptographicPduRef

- **UUID**: `ECUC:f4745072-90e6-4aa3-9005-6d676efba509`
- **引用名**: `SecOCTxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

####### 3. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:6fe21788-cbbf-c9da-c639-74ac56516832`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

########## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:588c5ec7-3a60-d24b-c736-707e8ca9ede0`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

##### 14. SecOCTxAuthenticPdu

**容器属性**:

- **UUID**: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxAuthenticPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCTxAuthenticPduId

- **UUID**: `ECUC:fd73c019-8d14-4d07-a5d9-bc9f6af4f2c0`
- **参数名**: `SecOCTxAuthenticPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Authentic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCTxAuthenticPduRef

- **UUID**: `ECUC:abab787a-645e-4ad0-af50-f59116b3586d`
- **引用名**: `SecOCTxAuthenticPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 15. SecOCTxCryptographicPdu

**容器属性**:

- **UUID**: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCTxCryptographicPdu`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SecOCTxCryptographicPduId

- **UUID**: `ECUC:4bcd8e92-7491-4724-8868-e8961ffccc6c`
- **参数名**: `SecOCTxCryptographicPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: PDU identifier of the Cryptographic I-PDU assigned by SecOC module. Used by PduR for confirmation (SecOC_PduRTxConfirmation) and for TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SecOCTxCryptographicPduRef

- **UUID**: `ECUC:f4745072-90e6-4aa3-9005-6d676efba509`
- **引用名**: `SecOCTxCryptographicPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the global Pdu.

##### 16. SecOCUseMessageLink

**容器属性**:

- **UUID**: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SecOCUseMessageLink`
- **多重性**: [0..1]

**容器描述**:

SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SecOCMessageLinkLen

- **UUID**: `ECUC:6fe21788-cbbf-c9da-c639-74ac56516832`
- **参数名**: `SecOCMessageLinkLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Length of the Message Linker inside the Authentic I-PDU in bits.

######## 2. SecOCMessageLinkPos

- **UUID**: `ECUC:588c5ec7-3a60-d24b-c736-707e8ca9ede0`
- **参数名**: `SecOCMessageLinkPos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Message Linker inside the Authentic I-PDU in bits.

##### 17. SecOCRxSecuredPduLayer

**容器属性**:

- **UUID**: `ECUC:0d17ebb7-f591-4e4e-b2f0-0ccedce78b25`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SecOCRxSecuredPduLayer`
- **多重性**: [1..1]

**容器选择**:

- **SecOCRxSecuredPdu**
  - UUID: `ECUC:eec91efc-2ddf-4d96-9944-f966b70fb710`
  - 描述: This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.
- **SecOCRxSecuredPduCollection**
  - UUID: `ECUC:f9ab58b5-f3c8-435f-a0f9-cabfafd185bb`
  - 描述: This container specifies two Pdus that are received by the SecOC module from the PduR and a message linking between them.
- **SecOCRxAuthenticPdu**
  - UUID: `ECUC:90f8a475-b3c9-41c7-b693-8b818f376daa`
  - 描述: This container specifies the Authetic Pdu that is received by the SecOC module from the PduR.
- **SecOCRxCryptographicPdu**
  - UUID: `ECUC:372ebdd2-f32e-4581-a563-f907d6f610a4`
  - 描述: This container specifies the Cryptographic Pdu that is received by the SecOC module from the PduR.
- **SecOCUseMessageLink**
  - UUID: `ECUC:e1f46a76-00ec-88f9-2ef3-6f898dbf561e`
  - 描述: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

**容器描述**:

This container specifies the Pdu that is received by the SecOC module from the PduR. For this Pdu the Mac verification is provided.

##### 18. SecOCTxSecuredPduLayer

**容器属性**:

- **UUID**: `ECUC:f28c4013-a122-48f9-8116-a9c2e70746e8`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SecOCTxSecuredPduLayer`
- **多重性**: [1..1]

**容器选择**:

- **SecOCTxSecuredPdu**
  - UUID: `ECUC:7cbe5ea3-b956-4f43-8865-2d9eef01d0bd`
  - 描述: This container specifies one Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. This Pdu contains the cryptographic information.
- **SecOCTxSecuredPduCollection**
  - UUID: `ECUC:818bd2c9-6dbe-4382-8b0b-9864ae0016a8`
  - 描述: This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated. Two separate Pdus are transmitted to the PduR:
- **SecOCTxAuthenticPdu**
  - UUID: `ECUC:b8592877-9bb3-489b-af8c-a71c95eb88f8`
  - 描述: This container specifies the Authetic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.
- **SecOCTxCryptographicPdu**
  - UUID: `ECUC:f4548f58-7b28-494a-a772-380b0138620b`
  - 描述: This container specifies the Cryptographic Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.
- **SecOCUseMessageLink**
  - UUID: `ECUC:69d4e489-7ae2-891c-1905-3d2e8bede70b`
  - 描述: SecOC links an Authentic I-PDU and Cryptographic I-PDU together by repeating a specific part (Message Linker) of the Authentic I-PDU in the Cryptographic I-PDU.

**容器描述**:

This container specifies the Pdu that is transmitted by the SecOC module to the PduR after the Mac was generated.

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

1. **SecOC**
