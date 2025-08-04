# KeyM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:50

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [KeyM](#keym)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00046.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. KeyM

#### 基本信息

- **UUID**: `ECUC:2c32c289-42f6-4153-a1ce-77cd061d5106`
- **模块名称**: `KeyM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Mcu (Microcontroller Unit) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. KeyMCertificate

**容器属性**:

- **UUID**: `ECUC:3815cf41-1e38-4f31-8316-290f53f87b15`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificate`
- **多重性**: [0..65535]

**容器描述**:

This container contains the certificate configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCertificateId

- **UUID**: `ECUC:42bf49af-2780-4ce5-88d7-d3d0501fb612`
- **参数名**: `KeyMCertificateId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Identifier of the certificate. The set of configured identifiers shall be consecutive and gapless.

######## 2. KeyMCertificateMaxLength

- **UUID**: `ECUC:f1343d36-0755-43bc-a626-3da68b6f8744`
- **参数名**: `KeyMCertificateMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specify the maximum length in bytes of the certificate.

####### STRING 类型参数

######## 1. KeyMCertificateName

- **UUID**: `ECUC:e21f95a8-4e7a-4a1a-bb5d-8c0fd7c771cb`
- **参数名**: `KeyMCertificateName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Provides a unique name of the certificate for identification. The certificate provisional will reference certificates by this unique name.

####### ENUMERATION 类型参数

######## 1. KeyMCertAlgorithmType

- **UUID**: `ECUC:833f15f1-acba-490a-89bc-2f3c96ee3100`
- **参数名**: `KeyMCertAlgorithmType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ECC` (来源: AUTOSAR_ECUC)
  - `RSA` (来源: AUTOSAR_ECUC)
- **描述**: Specify in which format the certificate will be provided.

######## 2. KeyMCertFormatType

- **UUID**: `ECUC:86316f90-026e-413a-851c-9c2aced9aeb3`
- **参数名**: `KeyMCertFormatType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRL` (来源: AUTOSAR_ECUC)
  - `CVC` (来源: AUTOSAR_ECUC)
  - `X509` (来源: AUTOSAR_ECUC)
- **描述**: Specify in which format the certificate will be provided.

####### FUNCTION-NAME 类型参数

######## 1. KeyMCertificateVerifyCallbackNotificationFunc

- **UUID**: `ECUC:ebcbed71-f13e-46e9-a146-da6c53f4c4ca`
- **参数名**: `KeyMCertificateVerifyCallbackNotificationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter provides the function name for the callback <KeyM_CertificateVerifyCallbackNotification>. It indicates if a certificate verification operation was finished and provides its status. If this parameter is omitted, no callback will be provided.

######## 2. KeyMServiceCertificateCallbackNotificationFunc

- **UUID**: `ECUC:d9025e69-d1ed-4faa-85bb-a00ed47f9de3`
- **参数名**: `KeyMServiceCertificateCallbackNotificationFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: This parameter provides the function name for the service certificate callback <KeyM_ServiceCertificateCallbackNotification>. It indicates if a certificate service operation was finished and provides its status. If this parameter is not set, no callback will be provided.

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. KeyMCertCertificateElementRuleRef

- **UUID**: `ECUC:2c88eb12-cf5a-4a2d-8ff9-8e27b3bed786`
- **引用名**: `KeyMCertCertificateElementRuleRef`
- **引用类型**: REFERENCE
- **多重性**: [0..65535]
- **目标**: `KeyMCertificateElementRule`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificateElementVerification/KeyMCertificateElementRule`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to certificate element rules which should be verified within the certification validation step.

######## 2. KeyMCertCsmSignatureVerifyJobRef

- **UUID**: `ECUC:67ed4fda-4206-4e75-9111-2966e5d9902e`
- **引用名**: `KeyMCertCsmSignatureVerifyJobRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the CSM job that is used to verify the signature

######## 3. KeyMCertCsmSignatureVerifyKeyRef

- **UUID**: `ECUC:e9ce61a5-4ce4-4d45-8c2b-cbc5b3b1c021`
- **引用名**: `KeyMCertCsmSignatureVerifyKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: References to the CSM key associated to the CSM signature verify job. This parameter can be omitted if the certificate is stored in CSM and the public key automatically references to the signature verify job, e.g. with virtual key.

######## 4. KeyMCertPrivateKeyStorageCryptoKeyRef

- **UUID**: `ECUC:aab20642-2950-456b-9bd7-7a168f45be8e`
- **引用名**: `KeyMCertPrivateKeyStorageCryptoKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `KeyMCryptoKey`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCryptoKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Defines a storage location of the private key of a certificate.

######## 5. KeyMCertTimebaseRef

- **UUID**: `ECUC:4d76500f-0d56-4ccd-9df5-1b47805e06e3`
- **引用名**: `KeyMCertTimebaseRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This is a reference to an StbM time base to validate the validity period. Alternatively, KeyMCertificateElementVerification with the KeyMCertificateElement of CertificateValidityPeriodNotBefore or CertificateValidityPeriodNotAfter could be used.

######## 6. KeyMCertUpperHierarchicalCertRef

- **UUID**: `ECUC:1163298a-1bd8-48d9-a87b-4a9a50e9baeb`
- **引用名**: `KeyMCertUpperHierarchicalCertRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificate`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Identifier of the certificate that is the next higher in the PKI hierarchical structure. The reference points to itself for root certificates.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. KeyMCertificateElement

**容器属性**:

- **UUID**: `ECUC:916dce37-7040-42ed-8d54-97c123489837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElement`
- **多重性**: [0..65535]

**容器描述**:

This container contains the certificate element configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementId

- **UUID**: `ECUC:2621613d-e293-4088-85bc-a657a70f4c95`
- **参数名**: `KeyMCertificateElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Identifier of a certificate element.

########## 2. KeyMCertificateElementMaxLength

- **UUID**: `ECUC:c48692bc-26ad-437e-976a-4d2cf53152d9`
- **参数名**: `KeyMCertificateElementMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum length in bytes

########## 3. KeyMCertificateElementObjectType

- **UUID**: `ECUC:8e8dce5a-8c49-474e-a3b7-9fd4cd0933ac`
- **参数名**: `KeyMCertificateElementObjectType`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Certificate elements are stored in ASN.1 format. In this item the type of ASN.1 TLV can be specified (e.g. INTEGER has the value '2'). This can be used to identify only such certificate elements. If the type is different, the element is not included in the search.

######### BOOLEAN 类型参数

########## 1. KeyMCertificateElementHasIteration

- **UUID**: `ECUC:e9b02987-4a5b-4d83-a066-ba6f2d9588d0`
- **参数名**: `KeyMCertificateElementHasIteration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines if the certificate element can occur more than one time. If so, the iterator can be used to retrieve the individual data values of this certificate element.

######### STRING 类型参数

########## 1. KeyMCertificateElementObjectId

- **UUID**: `ECUC:6ed83f67-b000-43d8-9fe8-202e0b54217c`
- **参数名**: `KeyMCertificateElementObjectId`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This is the object identifier (OID) that is used to identify the certificate element within its element structure.

######### ENUMERATION 类型参数

########## 1. KeyMCertificateElementOfStructure

- **UUID**: `ECUC:99fb2f38-edfb-494f-8fcd-6601360e8797`
- **参数名**: `KeyMCertificateElementOfStructure`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CertificateExtension` (来源: AUTOSAR_ECUC)
  - `CertificateIssuerName` (来源: AUTOSAR_ECUC)
  - `CertificateIssuerUniqueIdentifier` (来源: AUTOSAR_ECUC)
  - `CertificateSerialNumber` (来源: AUTOSAR_ECUC)
  - `CertificateSignature` (来源: AUTOSAR_ECUC)
  - `CertificateSignatureAlgorithm` (来源: AUTOSAR_ECUC)
  - `CertificateSignatureAlgorithmID` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectName` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectPublicKeyInfo_PublicKeyAlgorithm` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectPublicKeyInfo_SubjectPublicKey` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectUniqueIdentifier` (来源: AUTOSAR_ECUC)
  - `CertificateValidityPeriodNotAfter` (来源: AUTOSAR_ECUC)
  - `CertificateValidityPeriodNotBefore` (来源: AUTOSAR_ECUC)
  - `CertificateVersionNumber` (来源: AUTOSAR_ECUC)
- **描述**: This defines in which structure the certificate element is located.

##### 2. KeyMCertificateElement

**容器属性**:

- **UUID**: `ECUC:916dce37-7040-42ed-8d54-97c123489837`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElement`
- **多重性**: [0..65535]

**容器描述**:

This container contains the certificate element configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCertificateElementId

- **UUID**: `ECUC:2621613d-e293-4088-85bc-a657a70f4c95`
- **参数名**: `KeyMCertificateElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Identifier of a certificate element.

######## 2. KeyMCertificateElementMaxLength

- **UUID**: `ECUC:c48692bc-26ad-437e-976a-4d2cf53152d9`
- **参数名**: `KeyMCertificateElementMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum length in bytes

######## 3. KeyMCertificateElementObjectType

- **UUID**: `ECUC:8e8dce5a-8c49-474e-a3b7-9fd4cd0933ac`
- **参数名**: `KeyMCertificateElementObjectType`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Certificate elements are stored in ASN.1 format. In this item the type of ASN.1 TLV can be specified (e.g. INTEGER has the value '2'). This can be used to identify only such certificate elements. If the type is different, the element is not included in the search.

####### BOOLEAN 类型参数

######## 1. KeyMCertificateElementHasIteration

- **UUID**: `ECUC:e9b02987-4a5b-4d83-a066-ba6f2d9588d0`
- **参数名**: `KeyMCertificateElementHasIteration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines if the certificate element can occur more than one time. If so, the iterator can be used to retrieve the individual data values of this certificate element.

####### STRING 类型参数

######## 1. KeyMCertificateElementObjectId

- **UUID**: `ECUC:6ed83f67-b000-43d8-9fe8-202e0b54217c`
- **参数名**: `KeyMCertificateElementObjectId`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This is the object identifier (OID) that is used to identify the certificate element within its element structure.

####### ENUMERATION 类型参数

######## 1. KeyMCertificateElementOfStructure

- **UUID**: `ECUC:99fb2f38-edfb-494f-8fcd-6601360e8797`
- **参数名**: `KeyMCertificateElementOfStructure`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CertificateExtension` (来源: AUTOSAR_ECUC)
  - `CertificateIssuerName` (来源: AUTOSAR_ECUC)
  - `CertificateIssuerUniqueIdentifier` (来源: AUTOSAR_ECUC)
  - `CertificateSerialNumber` (来源: AUTOSAR_ECUC)
  - `CertificateSignature` (来源: AUTOSAR_ECUC)
  - `CertificateSignatureAlgorithm` (来源: AUTOSAR_ECUC)
  - `CertificateSignatureAlgorithmID` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectName` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectPublicKeyInfo_PublicKeyAlgorithm` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectPublicKeyInfo_SubjectPublicKey` (来源: AUTOSAR_ECUC)
  - `CertificateSubjectUniqueIdentifier` (来源: AUTOSAR_ECUC)
  - `CertificateValidityPeriodNotAfter` (来源: AUTOSAR_ECUC)
  - `CertificateValidityPeriodNotBefore` (来源: AUTOSAR_ECUC)
  - `CertificateVersionNumber` (来源: AUTOSAR_ECUC)
- **描述**: This defines in which structure the certificate element is located.

##### 3. KeyMCertificateElementVerification

**容器属性**:

- **UUID**: `ECUC:3ffd48cf-01a3-4efd-903f-21db48ed1901`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementVerification`
- **多重性**: [0..65535]

**容器描述**:

This container defines if and how certificate elements are to be verified.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. KeyMCertificateElementCondition

**容器属性**:

- **UUID**: `ECUC:17ab2852-86c7-4e7b-8d40-640f79e771cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementCondition`
- **多重性**: [1..infinite]

**容器描述**:

This container contains the configuration of KeyElement compare conditions which can be used as arguments for a KeyMCertificateElementRule.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. KeyMCertElementConditionType

- **UUID**: `ECUC:0a932241-93b6-477b-9fc7-3a9facc1ca5b`
- **参数名**: `KeyMCertElementConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_EQUALS` (来源: AUTOSAR_ECUC)
  - `KEYM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
  - `KEYM_GREATER_OR_EQUAL` (来源: AUTOSAR_ECUC)
  - `KEYM_LESS_OR_EQUAL` (来源: AUTOSAR_ECUC)
  - `KEYM_LESS_THAN` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:a8273668-6dda-4c41-bdf8-4a7fed4fe494`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a certificate element used for the condition.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. KeyMCertificateElementConditionValue

**容器属性**:

- **UUID**: `ECUC:c11870ee-9aef-4325-8581-b1a710df3475`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionValue`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration of a compare value.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

################ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

########### 2. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

########### 3. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

########### 4. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

########### 5. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

############ 引用关系

此容器包含 **1** 个引用：

############# INSTANCE-REFERENCE 类型引用

############## 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

######### 2. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 3. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 4. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

######### 5. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

######### 6. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

####### 2. KeyMCertificateElementConditionValue

**容器属性**:

- **UUID**: `ECUC:c11870ee-9aef-4325-8581-b1a710df3475`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionValue`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration of a compare value.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 2. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 3. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

######### 4. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

######### 5. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

####### 3. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 4. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

########## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 5. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

####### 6. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

####### 7. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

####### 8. KeyMCertificateElementRule

**容器属性**:

- **UUID**: `ECUC:1f2eba51-597b-47d9-be85-5c481d7e896c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementRule`
- **多重性**: [1..infinite]

**容器描述**:

This container contains the configuration of a mode rule which represents a logical expression with KeyMCertificateElementCondition or other KeyMCertificateElementRule as arguments.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. KeyMLogicalOperator

- **UUID**: `ECUC:9d8f4f53-0ef8-4e58-8b6e-e0358fadd2af`
- **参数名**: `KeyMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_AND` (来源: AUTOSAR_ECUC)
  - `KEYM_OR` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. KeyMArgumentRef

- **UUID**: `ECUC:5cf0c58f-8240-4063-a80c-77a1ab45fa1f`
- **引用名**: `KeyMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/KeyM/KeyMCertificateElementVerification/KeyMCertificateElementCondition`
  - `/AUTOSAR/EcucDefs/KeyM/KeyMCertificateElementVerification/KeyMCertificateElementRule`
- **描述**: This is a choice reference either to a condition or another rule serving as sub-expression.

##### 4. KeyMCertificateElementCondition

**容器属性**:

- **UUID**: `ECUC:17ab2852-86c7-4e7b-8d40-640f79e771cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementCondition`
- **多重性**: [1..infinite]

**容器描述**:

This container contains the configuration of KeyElement compare conditions which can be used as arguments for a KeyMCertificateElementRule.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. KeyMCertElementConditionType

- **UUID**: `ECUC:0a932241-93b6-477b-9fc7-3a9facc1ca5b`
- **参数名**: `KeyMCertElementConditionType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_EQUALS` (来源: AUTOSAR_ECUC)
  - `KEYM_EQUALS_NOT` (来源: AUTOSAR_ECUC)
  - `KEYM_GREATER_OR_EQUAL` (来源: AUTOSAR_ECUC)
  - `KEYM_LESS_OR_EQUAL` (来源: AUTOSAR_ECUC)
  - `KEYM_LESS_THAN` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies what kind of comparison that is made for the evaluation of the mode condition.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:a8273668-6dda-4c41-bdf8-4a7fed4fe494`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a certificate element used for the condition.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. KeyMCertificateElementConditionValue

**容器属性**:

- **UUID**: `ECUC:c11870ee-9aef-4325-8581-b1a710df3475`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionValue`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration of a compare value.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 2. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

######### 3. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

######### 4. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

######### 5. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

########## 引用关系

此容器包含 **1** 个引用：

########### INSTANCE-REFERENCE 类型引用

############ 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

####### 2. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 3. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

########## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 4. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

####### 5. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

####### 6. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

##### 5. KeyMCertificateElementConditionValue

**容器属性**:

- **UUID**: `ECUC:c11870ee-9aef-4325-8581-b1a710df3475`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionValue`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration of a compare value.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

############ 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 2. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

########## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

####### 3. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

####### 4. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

####### 5. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

######## 引用关系

此容器包含 **1** 个引用：

######### INSTANCE-REFERENCE 类型引用

########## 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

##### 6. KeyMCertificateElementConditionArray

**容器属性**:

- **UUID**: `ECUC:89771f22-b2dc-4cdf-a312-c24056fd5649`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArray`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a array compare value.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

########## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

##### 7. KeyMCertificateElementConditionArrayElement

**容器属性**:

- **UUID**: `ECUC:4495dc20-4a95-42cc-a198-65fc85d12f38`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionArrayElement`
- **多重性**: [0..infinite]

**容器描述**:

This container contains the configuration of a array compare value.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCertificateElementConditionArrayElementIndex

- **UUID**: `ECUC:4be41af0-534e-4c8d-a1d3-b2a5a72814f6`
- **参数名**: `KeyMCertificateElementConditionArrayElementIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index to an element of the compare value array.

######## 2. KeyMCertificateElementConditionArrayElementValue

- **UUID**: `ECUC:e26110cd-6886-4560-bfb0-aadd9848615b`
- **参数名**: `KeyMCertificateElementConditionArrayElementValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of an array element compare value.

##### 8. KeyMCertificateElementConditionCerificateElement

**容器属性**:

- **UUID**: `ECUC:a0a5d896-ef4c-40c0-b0fa-1be6e13c4f9c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionCerificateElement`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a certificate element as a compare value.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. KeyMCertificateElementRef

- **UUID**: `ECUC:487e7273-509c-41ca-9d43-d82a0f59669f`
- **引用名**: `KeyMCertificateElementRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `KeyMCertificateElement`
- **完整路径**: `/AUTOSAR/EcucDefs/KeyM/KeyMCertificate/KeyMCertificateElement`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to another certificate element.

##### 9. KeyMCertificateElementConditionPrimitive

**容器属性**:

- **UUID**: `ECUC:1a82aa94-28e5-43e1-b16f-c6be50cdd91e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionPrimitive`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a primitive compare value.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCertificateElementConditionPrimitiveValue

- **UUID**: `ECUC:05ba59f2-a105-44f4-bb48-23fd7b4a0099`
- **参数名**: `KeyMCertificateElementConditionPrimitiveValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Primitive compare value

##### 10. KeyMCertificateElementConditionSenderReceiver

**容器属性**:

- **UUID**: `ECUC:2cacb3c7-dd85-48de-abc1-696513fe2634`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementConditionSenderReceiver`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration of a dynamic compare value in a sender-/receiver interface.

###### 引用关系

此容器包含 **1** 个引用：

####### INSTANCE-REFERENCE 类型引用

######## 1. KeyMCertificateElementConditionSenderReceiver

- **UUID**: `ECUC:dd509ab8-cfe0-463e-9f54-9ae2d1753345`
- **引用名**: `KeyMCertificateElementConditionSenderReceiver`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: AUTOSAR-DATA-PROTOTYPE
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: This parameter references a mode in a particular mode request port of a software component that is used for the condition.

##### 11. KeyMCertificateElementRule

**容器属性**:

- **UUID**: `ECUC:1f2eba51-597b-47d9-be85-5c481d7e896c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCertificateElementRule`
- **多重性**: [1..infinite]

**容器描述**:

This container contains the configuration of a mode rule which represents a logical expression with KeyMCertificateElementCondition or other KeyMCertificateElementRule as arguments.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. KeyMLogicalOperator

- **UUID**: `ECUC:9d8f4f53-0ef8-4e58-8b6e-e0358fadd2af`
- **参数名**: `KeyMLogicalOperator`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_AND` (来源: AUTOSAR_ECUC)
  - `KEYM_OR` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies the logical operator to be used in the logical expression. If the expression only consists of a single condition this parameter shall not be used.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. KeyMArgumentRef

- **UUID**: `ECUC:5cf0c58f-8240-4063-a80c-77a1ab45fa1f`
- **引用名**: `KeyMArgumentRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/KeyM/KeyMCertificateElementVerification/KeyMCertificateElementCondition`
  - `/AUTOSAR/EcucDefs/KeyM/KeyMCertificateElementVerification/KeyMCertificateElementRule`
- **描述**: This is a choice reference either to a condition or another rule serving as sub-expression.

##### 12. KeyMCryptoKey

**容器属性**:

- **UUID**: `ECUC:cb7ddbfe-c4a8-4749-8527-7034a8ca7fc6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMCryptoKey`
- **多重性**: [0..65535]

**容器描述**:

This container contains the crypto keys that can be updated.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCryptoKeyId

- **UUID**: `ECUC:8975041a-b2a2-49ad-b6fc-33bba2022cc7`
- **参数名**: `KeyMCryptoKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Identifier of the crypto key. The set of configured identifiers shall be consecutive and gapless.

######## 2. KeyMCryptoKeyMaxLength

- **UUID**: `ECUC:8fd4ffc9-082a-45ab-b12a-4987a23a0199`
- **参数名**: `KeyMCryptoKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The maximum size in bytes of a CryptoKey.

####### STRING 类型参数

######## 1. KeyMCryptoKeyCryptoProps

- **UUID**: `ECUC:4c9fece2-ef77-4930-915d-322e6015d2ce`
- **参数名**: `KeyMCryptoKeyCryptoProps`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: If set, it will provide additional hints to the crypto key that is used by KeyM to identify the key.

######## 2. KeyMCryptoKeyGenerationInfo

- **UUID**: `ECUC:f43d582f-210e-4025-be82-b023cc4f5b9c`
- **参数名**: `KeyMCryptoKeyGenerationInfo`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: This data may contain static data for key derivation. If a key is configured to be derived from another key and this configuration item is set, the data will be added as salt.

######## 3. KeyMCryptoKeyName

- **UUID**: `ECUC:dc6e7951-c064-45c7-b2e8-5a05d04db2da`
- **参数名**: `KeyMCryptoKeyName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Provides a unique name of the key for identification. The key master will reference keys by this unique key name.

####### ENUMERATION 类型参数

######## 1. KeyMCryptoCsmVerifyJobType

- **UUID**: `ECUC:912bcc9b-1b55-42b7-8c00-0b1ca88a0787`
- **参数名**: `KeyMCryptoCsmVerifyJobType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_VERIFY_AEADDECRYPT` (来源: AUTOSAR_ECUC)
  - `KEYM_VERIFY_AEADENCRYPT` (来源: AUTOSAR_ECUC)
  - `KEYM_VERIFY_DECRYPT` (来源: AUTOSAR_ECUC)
  - `KEYM_VERIFY_ENCRYPT` (来源: AUTOSAR_ECUC)
  - `KEYM_VERIFY_MACGENERATE` (来源: AUTOSAR_ECUC)
  - `KEYM_VERIFY_MACVERIFY` (来源: AUTOSAR_ECUC)
- **描述**: Specifies what type of function for key verification operation is used.

######## 2. KeyMCryptoKeyGenerationType

- **UUID**: `ECUC:4a4b5642-a609-4867-b42c-4873de2c5ec9`
- **参数名**: `KeyMCryptoKeyGenerationType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_DERIVED_KEY` (来源: AUTOSAR_ECUC)
  - `KEYM_STORED_KEY` (来源: AUTOSAR_ECUC)
- **描述**: Specifies how the CryptoKey will be generated. If it is derived from another key or simply stored with KeyElementSet.

######## 3. KeyMCryptoKeyStorage

- **UUID**: `ECUC:48980e5b-3563-48e4-97eb-2c690cfbc0cf`
- **参数名**: `KeyMCryptoKeyStorage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `KEYM_STORAGE_IN_CSM` (来源: AUTOSAR_ECUC)
  - `KEYM_STORAGE_IN_NVM` (来源: AUTOSAR_ECUC)
  - `KEYM_STORAGE_IN_RAM` (来源: AUTOSAR_ECUC)
- **描述**: Specify the storage location of the certificate.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. KeyMCryptoKeyCsmKeySourceDeriveRef

- **UUID**: `ECUC:7c31c6b4-3cfd-4216-a5d4-20b0f5162a9a`
- **引用名**: `KeyMCryptoKeyCsmKeySourceDeriveRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Defines a reference to the associated CSM key that is used as source for the key derivation of this key.

######## 2. KeyMCryptoKeyCsmKeyTargetRef

- **UUID**: `ECUC:5c0d2ee8-98a8-457a-ade4-e71b8ffcf60a`
- **引用名**: `KeyMCryptoKeyCsmKeyTargetRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Defines a reference to the associated CSM key that shall be generated.

######## 3. KeyMCryptoKeyCsmVerifyJobRef

- **UUID**: `ECUC:70948f00-8e9a-415e-a4be-f3433f38b43b`
- **引用名**: `KeyMCryptoKeyCsmVerifyJobRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmJob`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmJobs/CsmJob`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Defines the crypto job that the key verify function can use for verification of a certain key.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. KeyMNvmBlock

**容器属性**:

- **UUID**: `ECUC:aaecb708-e348-4e7f-98b9-55976b41bbda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMNvmBlock`
- **多重性**: [0..1]

**容器描述**:

Configuration of optional usage of Nvm in case the KeyM module requires non volatile memory in the Ecu to store information (e.g. crypto keys or certificates).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. KeyMNvmBlockDescriptorRef

- **UUID**: `ECUC:d5177ff2-7eeb-4f17-8c72-ace047a6b8c6`
- **引用名**: `KeyMNvmBlockDescriptorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

##### 13. KeyMNvmBlock

**容器属性**:

- **UUID**: `ECUC:aaecb708-e348-4e7f-98b9-55976b41bbda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMNvmBlock`
- **多重性**: [0..1]

**容器描述**:

Configuration of optional usage of Nvm in case the KeyM module requires non volatile memory in the Ecu to store information (e.g. crypto keys or certificates).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. KeyMNvmBlockDescriptorRef

- **UUID**: `ECUC:d5177ff2-7eeb-4f17-8c72-ace047a6b8c6`
- **引用名**: `KeyMNvmBlockDescriptorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

##### 14. KeyMGeneral

**容器属性**:

- **UUID**: `ECUC:9d2fb602-a28e-4112-9023-a1e4b8142752`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `KeyMGeneral`
- **多重性**: [1..1]

**容器描述**:

This container holds general configuration (parameters) for key manager.

###### 参数配置

此容器包含 **16** 个参数：

####### INTEGER 类型参数

######## 1. KeyMCertificateChainMaxDepth

- **UUID**: `ECUC:93e8454c-327c-4c5d-af9e-86bef1e243ff`
- **参数名**: `KeyMCertificateChainMaxDepth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of certificates defined in a certificate chain.

######## 2. KeyMKeyCertNameMaxLength

- **UUID**: `ECUC:824a6d50-891d-4098-abf6-0cc9ce186663`
- **参数名**: `KeyMKeyCertNameMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum length in bytes of certificate or key names used for the service interface.

####### BOOLEAN 类型参数

######## 1. KeyMCertificateManagerEnabled

- **UUID**: `ECUC:f173f54b-3515-437b-a967-89ce33c9bb97`
- **参数名**: `KeyMCertificateManagerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the part that manages certificates.

######## 2. KeyMCryptoKeyHandlerPrepareEnabled

- **UUID**: `ECUC:41b3c83c-1579-4f21-8e15-5a8b096e7726`
- **参数名**: `KeyMCryptoKeyHandlerPrepareEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the key handler prepare function call. If set to true, the corresponding key handler function shall be provided.

######## 3. KeyMCryptoKeyHandlerServiceCertificateEnabled

- **UUID**: `ECUC:fbe91daf-ff5f-4d8f-a12f-77d9c58a11a6`
- **参数名**: `KeyMCryptoKeyHandlerServiceCertificateEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the key handler service function call. If set to true, the certificate submodule function KeyM_KH_ServiceCertificate() shall be provided.

######## 4. KeyMCryptoKeyHandlerStartFinalizeEnabled

- **UUID**: `ECUC:b516e06a-b1c2-4203-a4b4-45428261a079`
- **参数名**: `KeyMCryptoKeyHandlerStartFinalizeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the key handler start and finalize function call. If set to true, the key handler functions KeyM_KH_Start() and KeyM_KH_Finalize() shall be provided.

######## 5. KeyMCryptoKeyHandlerUpdateEnabled

- **UUID**: `ECUC:c1b319d8-348d-4493-9739-2ce852e061b7`
- **参数名**: `KeyMCryptoKeyHandlerUpdateEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the call to the key handler update function KeyM_KH_Update(). If set to true, the corresponding key handler function shall be provided.

######## 6. KeyMCryptoKeyHandlerVerifyEnabled

- **UUID**: `ECUC:e410b31b-0dcd-4955-8154-f88762d62f06`
- **参数名**: `KeyMCryptoKeyHandlerVerifyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the call to the key handler verify function KeyM_KH_Verify(). If set to true, the corresponding key handler function shall be provided.

######## 7. KeyMCryptoKeyManagerEnabled

- **UUID**: `ECUC:aedc2796-e45a-4dad-b10f-da248b0c53a9`
- **参数名**: `KeyMCryptoKeyManagerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the part that manages crypto key operations.

######## 8. KeyMCryptoKeyPrepareFunctionEnabled

- **UUID**: `ECUC:a9b1a74c-8aec-43b5-bfe1-416d6504f7fd`
- **参数名**: `KeyMCryptoKeyPrepareFunctionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the prepare function of the key manager. If set to true, the KeyM_Prepare() function has to be called accordingly.

######## 9. KeyMCryptoKeyStartFinalizeFunctionEnabled

- **UUID**: `ECUC:3796e262-a4db-4891-a00d-6b7f4d2fbbc3`
- **参数名**: `KeyMCryptoKeyStartFinalizeFunctionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the start and Finish function of the key manager. If set to true, the KeyM_Start() and KeyM_Finalize() functions have to be called.

######## 10. KeyMCryptoKeyVerifyAsyncMode

- **UUID**: `ECUC:0030a464-4346-4ad6-9206-996fddd7b8d3`
- **参数名**: `KeyMCryptoKeyVerifyAsyncMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines if the function KeyM_Verify() runs in synchronous or asynchronous mode

######## 11. KeyMCryptoKeyVerifyFunctionEnabled

- **UUID**: `ECUC:df771ead-177f-40b8-8b68-6a00fb321a29`
- **参数名**: `KeyMCryptoKeyVerifyFunctionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the verify function of the key manager. If set to true, the KeyM_Verify() function can be called.

######## 12. KeyMDevErrorDetect

- **UUID**: `ECUC:2d4d2418-06c2-4e91-bf73-494b04273e8f`
- **参数名**: `KeyMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the development error detection and notification on or off.

######## 13. KeyMServiceCertificateFunctionEnabled

- **UUID**: `ECUC:4c250ea2-741a-4313-bd7b-4b14a4a3c9fe`
- **参数名**: `KeyMServiceCertificateFunctionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the certificate service function of the key manager. If set to true, the KeyM_ServiceCertificate() function has to be called accordingly.

####### FLOAT 类型参数

######## 1. KeyMMainFunctionPeriod

- **UUID**: `ECUC:635a874c-e116-4bc1-8b5b-c20bcb85630f`
- **参数名**: `KeyMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the period of main function KeyM_MainFunction in seconds.

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

1. **KeyM**
