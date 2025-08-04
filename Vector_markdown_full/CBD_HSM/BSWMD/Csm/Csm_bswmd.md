# Csm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:42

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Csm](#csm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Csm

#### 基本信息

- **UUID**: `2f3e6142-f730-47bf-a890-c3990a2a6b17`
- **模块名称**: `Csm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Csm (CryptoServiceManager) module.

#### 版本历史

共有 **23** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: beta
- **发布日期**: 2016-07-19T04:21:54+02:00
- **发布者**: visrpp

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: beta
- **发布日期**: 2016-12-06T05:33:21+01:00
- **发布者**: vismss

**变更内容**:

##### 3. 版本 1.00.02

- **状态**: beta
- **发布日期**: 2016-12-16T01:25:55+01:00
- **发布者**: vismss

**变更内容**:

##### 4. 版本 1.00.03

- **状态**: beta
- **发布日期**: 2017-01-04T11:12:48+01:00
- **发布者**: vismss

**变更内容**:

##### 5. 版本 1.00.04

- **状态**: beta
- **发布日期**: 2017-01-24T11:20:26+01:00
- **发布者**: vismss

**变更内容**:

##### 6. 版本 1.01.00

- **状态**: beta
- **发布日期**: 2017-02-17T01:17:26+01:00
- **发布者**: visgut

**变更内容**:

##### 7. 版本 1.01.00

- **状态**: beta
- **发布日期**: 2017-03-27T04:36:38+02:00
- **发布者**: visgut

**变更内容**:

##### 8. 版本 1.01.01

- **状态**: beta
- **发布日期**: 2017-04-13T01:19:28+02:00
- **发布者**: visrpp

**变更内容**:

##### 9. 版本 2.00.00

- **状态**: released
- **发布日期**: 2017-04-21T05:43:16+02:00
- **发布者**: visrpp

**变更内容**:

##### 10. 版本 2.01.00

- **状态**: released
- **发布日期**: 2017-06-08T02:14:02+02:00
- **发布者**: vismaw

**变更内容**:

##### 11. 版本 2.02.00

- **状态**: released
- **发布日期**: 2017-07-13T09:53:24+02:00
- **发布者**: visrpp

**变更内容**:

##### 12. 版本 2.03.00

- **状态**: released
- **发布日期**: 2017-08-31T06:27:07+02:00
- **发布者**: visrpp

**变更内容**:

##### 13. 版本 2.03.01

- **状态**: released
- **发布日期**: 2018-03-15T02:49:00+01:00
- **发布者**: visrpp

**变更内容**:

##### 14. 版本 3.00.00

- **状态**: released
- **发布日期**: 2018-07-17T01:32:34+02:00
- **发布者**: vismaw

**变更内容**:

##### 15. 版本 3.01.00

- **状态**: released
- **发布日期**: 2018-08-21T06:06:47+02:00
- **发布者**: vismaw

**变更内容**:

##### 16. 版本 3.01.01

- **状态**: released
- **发布日期**: 2018-10-23T13:38:01+02:00
- **发布者**: vismwe

**变更内容**:

##### 17. 版本 4.00.00

- **状态**: released
- **发布日期**: 2019-01-07T15:10:44+01:00
- **发布者**: vismaw

**变更内容**:

##### 18. 版本 4.01.00

- **状态**: released
- **发布日期**: 2019-01-07T15:11:23+01:00
- **发布者**: vismaw

**变更内容**:

##### 19. 版本 4.01.01

- **状态**: released
- **发布日期**: 2019-06-19T10:18:18+02:00
- **发布者**: vismaw

**变更内容**:

##### 20. 版本 4.02.00

- **状态**: released
- **发布日期**: 2019-07-24T14:13:22+02:00
- **发布者**: vismaw

**变更内容**:

##### 21. 版本 5.00.00

- **状态**: released
- **发布日期**: 2019-11-05T14:21:18+01:00
- **发布者**: visenc

**变更内容**:

##### 22. 版本 5.00.01

- **状态**: released
- **发布日期**: 2020-01-20T11:28:06+01:00
- **发布者**: visewl

**变更内容**:

##### 23. 版本 5.01.00

- **状态**: released
- **发布日期**: 2020-07-08T12:12:20+02:00
- **发布者**: visrpp

**变更内容**:

#### 配置容器

本模块包含 **53** 个配置容器：

##### 1. CsmCallbacks

**容器属性**:

- **UUID**: `fc86491e-ff97-4641-8bf5-c328c614837e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallbacks`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for callback function configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmCallback

**容器属性**:

- **UUID**: `74ba6a3d-cf33-447d-958d-8773fc9b81e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallback`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a callback function

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CsmCallbackId

- **UUID**: `25538517-6669-43a6-a588-d8902f1fa889`
- **参数名**: `CsmCallbackId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the callback function.

######### ENUMERATION 类型参数

########## 1. CsmBswCallbackAsrVersion

- **UUID**: `9df71d3d-2b9b-42ef-bc30-32d800511859`
- **参数名**: `CsmBswCallbackAsrVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_03`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the configured callback when it is used as BSW callback.

CSM_ASR_VERSION_4_03: void <CallbackFunc> (Crypto_JobType* job, Std_ReturnType result)
CSM_ASR_VERSION_4_04: void <CallbackFunc> (const uint32 jobID, Csm_ResultType result)
CSM_ASR_VERSION_R19_11: void <CallbackFunc> (const Crypto_JobType* job, Crypto_ResultType result)

Defaults to CSM_ASR_VERSION_4_03 if unset.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackFunc

- **UUID**: `d795bc71-9255-496a-a842-7bdbd5d5b4a8`
- **参数名**: `CsmCallbackFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Callback function to be called if an asynchronous operation has finished. The corresponding job has to be configured to be processed asynchronously.

##### 2. CsmCallback

**容器属性**:

- **UUID**: `74ba6a3d-cf33-447d-958d-8773fc9b81e6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallback`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a callback function

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CsmCallbackId

- **UUID**: `25538517-6669-43a6-a588-d8902f1fa889`
- **参数名**: `CsmCallbackId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the callback function.

####### ENUMERATION 类型参数

######## 1. CsmBswCallbackAsrVersion

- **UUID**: `9df71d3d-2b9b-42ef-bc30-32d800511859`
- **参数名**: `CsmBswCallbackAsrVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_03`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the configured callback when it is used as BSW callback.

CSM_ASR_VERSION_4_03: void <CallbackFunc> (Crypto_JobType* job, Std_ReturnType result)
CSM_ASR_VERSION_4_04: void <CallbackFunc> (const uint32 jobID, Csm_ResultType result)
CSM_ASR_VERSION_R19_11: void <CallbackFunc> (const Crypto_JobType* job, Crypto_ResultType result)

Defaults to CSM_ASR_VERSION_4_03 if unset.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackFunc

- **UUID**: `d795bc71-9255-496a-a842-7bdbd5d5b4a8`
- **参数名**: `CsmCallbackFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Callback function to be called if an asynchronous operation has finished. The corresponding job has to be configured to be processed asynchronously.

##### 3. CsmGeneral

**容器属性**:

- **UUID**: `a501cbc5-6ee1-4b5d-8156-561f1f7ad107`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPrivateKeyMaxLength

- **UUID**: `b522d0bc-2acc-4977-84e1-536f85518256`
- **参数名**: `CsmAsymPrivateKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Not used and not supported.
Maximum length in bytes of an asymmetric public key for all algorithm.

######## 2. CsmAsymPublicKeyMaxLength

- **UUID**: `78969447-cc26-4580-9508-1ece7659ec77`
- **参数名**: `CsmAsymPublicKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1024`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Not used and not supported.
Maximum length in bytes of an asymmetric key for all algorithm.

######## 3. CsmSymKeyMaxLength

- **UUID**: `3d8c1b2c-7abd-4506-9dd9-bc24a076d313`
- **参数名**: `CsmSymKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Not used and not supported.
Maximum length in bytes of a symmetric key for all algorithm

####### BOOLEAN 类型参数

######## 1. CsmDevErrorDetect

- **UUID**: `b0917fd8-4b8e-4807-a548-6b87b7d41e43`
- **参数名**: `CsmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Switches the development error detection and notification on or off.

######## 2. CsmUseDeprecated

- **UUID**: `d252b78a-4982-4ec7-a9ef-defd245ff7db`
- **参数名**: `CsmUseDeprecated`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Not used and not supported.
Decides if the deprecated interfaces shall be used (Backwards compatibility).

######## 3. CsmVersionInfoApi

- **UUID**: `d58ead22-3f63-44e2-b0c3-2eea9b6bf61c`
- **参数名**: `CsmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Pre-processor switch to enable and disable availability of the API Csm_GetVersionInfo().

######## 4. CsmCallbackStartNotification

- **UUID**: `0ad9aeee-e94b-43dc-8778-17c0b73baf7a`
- **参数名**: `CsmCallbackStartNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: In ASR 4.3.0, only callbacks for Update (if CsmJobPrimitiveCallbackUpdateNotification is enabled) and Finish shall be forwarded to application. If this switch is enabled, Callback is also notified if Start was handled and every Update is notified too (CsmJobPrimitiveCallbackUpdateNotification is ignored).

######## 5. CsmCancelationDuringProcessing

- **UUID**: `11a7aa48-ea31-425a-9e59-6e5ffd28b70e`
- **参数名**: `CsmCancelationDuringProcessing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, Csm allows cancelation during the processing of an asynchronous job. 
Due to this, CRYPTO_E_JOB_CANCELED of lower layer is supported and forwarded to application (this return value was introduced in ASR 4.4).

If enabled, the runtime of a asynchronous job is slightly increased because the callback needs to enter an exclusive area to check the state.

######## 6. CsmSafeBswChecks

- **UUID**: `612d72b0-90a5-4f2c-a482-d227188707d6`
- **参数名**: `CsmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables safety checks. These checks improve robustness. E.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. CsmMainFunctionPeriod

- **UUID**: `562d1096-15ca-4c21-a1ca-79065413843e`
- **参数名**: `CsmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..1.7976931348623157E+308]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the period of main function Csm_MainFunction in seconds.

####### STRING 类型参数

######## 1. CsmCustomIncludeFiles

- **UUID**: `9bd084e8-daa9-4a61-ac7c-fbc373d69548`
- **参数名**: `CsmCustomIncludeFiles`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最小长度: 3
- **描述**: Include custom header file.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobTypeLayout

**容器属性**:

- **UUID**: `f6957e3f-4aad-44dd-9102-00c7088e7603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobTypeLayout`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration options for the Csm data structure Crypto_JobType and used sub data structures.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. CsmJobTypeLayoutAsr430Compatibility

- **UUID**: `1fccca04-08ca-4702-9cf4-b68d06cde6c4`
- **参数名**: `CsmJobTypeLayoutAsr430Compatibility`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has - according to Autosar - the fields 'jobState' and 'jobPrimitiveInputOutput'. These field names changed from AUTOSAR 4.3.0 to AUTOSAR 4.3.1. These fields defined by AUTOSAR 4.3.0 could be required by an underlying Crypto Driver.

If enabled, the Crypto_JobType is extended by the fields 'state' and 'PrimitiveInputOutput' as they are named in AUTOSAR 4.3.0.
If disabled, these fields are not contained in the definition of the Crypto_JobType and the Crypto_JobType is defined as specified in AUTOSAR 4.3.1.

########## 2. CsmJobTypeLayoutVarMembers

- **UUID**: `d1286308-af0a-4378-80c8-868f02555434`
- **参数名**: `CsmJobTypeLayoutVarMembers`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has in its sub data structures - according to Autosar- certain fields (e.g. 'jobId') which are defined as const fields. If a variable of this type shall be used in different use cases, these fields might be overwritten. This could be a requirement of an underlying Crypto Driver.

If enabled, the const members of Crypto_JobType's sub data structures are defined as non-const members
If disabled, the Crypto_JobType's sub data structures stay as defined according to Autosar.

########## 3. CsmJobTypeLayoutInput64

- **UUID**: `3a3f31b9-a979-4a10-bd8a-c2785d4424c7`
- **参数名**: `CsmJobTypeLayoutInput64`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'input64'. By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'input64' exists within the Crypto_JobPrimitiveInputOutputType.
If disabled, the field 'input64' doesn't exist within the Crypto_JobPrimitiveInputOutputType.

########## 4. CsmJobTypeLayoutOutput64Ptr

- **UUID**: `0257c7c2-a0d9-40f4-85b4-a519905ac996`
- **参数名**: `CsmJobTypeLayoutOutput64Ptr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'output64Ptr'. By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'output64Ptr' exists within the Crypto_JobPrimitiveInputOutputType.
If disabled, the field 'output64Ptr' doesn't exist within the Crypto_JobPrimitiveInputOutputType.

########## 5. CsmJobTypeLayoutRedirectionInfoRef

- **UUID**: `dc4ece26-688c-4553-a0ed-b2bb3f366d4f`
- **参数名**: `CsmJobTypeLayoutRedirectionInfoRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has the field 'jobRedirectionInfoRef'. This field can be switched off if it not required in order to reduce memory usage.

If enabled, the field 'jobRedirectionInfoRef' exists within the Crypto_JobType.
If disabled, the field 'jobRedirectionInfoRef' doesn't exist within the Crypto_JobType.

##### 4. CsmJobTypeLayout

**容器属性**:

- **UUID**: `f6957e3f-4aad-44dd-9102-00c7088e7603`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobTypeLayout`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration options for the Csm data structure Crypto_JobType and used sub data structures.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. CsmJobTypeLayoutAsr430Compatibility

- **UUID**: `1fccca04-08ca-4702-9cf4-b68d06cde6c4`
- **参数名**: `CsmJobTypeLayoutAsr430Compatibility`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has - according to Autosar - the fields 'jobState' and 'jobPrimitiveInputOutput'. These field names changed from AUTOSAR 4.3.0 to AUTOSAR 4.3.1. These fields defined by AUTOSAR 4.3.0 could be required by an underlying Crypto Driver.

If enabled, the Crypto_JobType is extended by the fields 'state' and 'PrimitiveInputOutput' as they are named in AUTOSAR 4.3.0.
If disabled, these fields are not contained in the definition of the Crypto_JobType and the Crypto_JobType is defined as specified in AUTOSAR 4.3.1.

######## 2. CsmJobTypeLayoutVarMembers

- **UUID**: `d1286308-af0a-4378-80c8-868f02555434`
- **参数名**: `CsmJobTypeLayoutVarMembers`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has in its sub data structures - according to Autosar- certain fields (e.g. 'jobId') which are defined as const fields. If a variable of this type shall be used in different use cases, these fields might be overwritten. This could be a requirement of an underlying Crypto Driver.

If enabled, the const members of Crypto_JobType's sub data structures are defined as non-const members
If disabled, the Crypto_JobType's sub data structures stay as defined according to Autosar.

######## 3. CsmJobTypeLayoutInput64

- **UUID**: `3a3f31b9-a979-4a10-bd8a-c2785d4424c7`
- **参数名**: `CsmJobTypeLayoutInput64`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'input64'. By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'input64' exists within the Crypto_JobPrimitiveInputOutputType.
If disabled, the field 'input64' doesn't exist within the Crypto_JobPrimitiveInputOutputType.

######## 4. CsmJobTypeLayoutOutput64Ptr

- **UUID**: `0257c7c2-a0d9-40f4-85b4-a519905ac996`
- **参数名**: `CsmJobTypeLayoutOutput64Ptr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to Autosar - the field 'output64Ptr'. By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'output64Ptr' exists within the Crypto_JobPrimitiveInputOutputType.
If disabled, the field 'output64Ptr' doesn't exist within the Crypto_JobPrimitiveInputOutputType.

######## 5. CsmJobTypeLayoutRedirectionInfoRef

- **UUID**: `dc4ece26-688c-4553-a0ed-b2bb3f366d4f`
- **参数名**: `CsmJobTypeLayoutRedirectionInfoRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobType has the field 'jobRedirectionInfoRef'. This field can be switched off if it not required in order to reduce memory usage.

If enabled, the field 'jobRedirectionInfoRef' exists within the Crypto_JobType.
If disabled, the field 'jobRedirectionInfoRef' doesn't exist within the Crypto_JobType.

##### 5. CsmJobs

**容器属性**:

- **UUID**: `218d90af-78b5-4092-bb14-049fd37b22d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for configuration of CSM jobs.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJob

**容器属性**:

- **UUID**: `8b866d41-ea5b-4e3d-bfd1-3bdfe21f5353`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJob`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of CSM job. The container name serves as a symbolic name for the identifier of a job configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobId

- **UUID**: `b4292d14-34aa-40b4-822e-7aa95d2c7414`
- **参数名**: `CsmJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the CSM job

########## 2. CsmJobPriority

- **UUID**: `a86f159f-7a11-46ae-b903-2b7cff47d112`
- **参数名**: `CsmJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Priority of the job.
The higher the value, the higher the job's priority.

######### BOOLEAN 类型参数

########## 1. CsmJobPrimitiveCallbackUpdateNotification

- **UUID**: `46d9db8a-5573-4514-a503-52b2a8a4a48f`
- **参数名**: `CsmJobPrimitiveCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter indicates, whether the callback function shall be called, if the UPDATE operation has been finished.

########## 2. CsmJobUsePort

- **UUID**: `3f58d478-639c-494f-a71c-dded3efd2507`
- **参数名**: `CsmJobUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Does the job need RTE interfaces?

######### ENUMERATION 类型参数

########## 1. CsmProcessingMode

- **UUID**: `b3ead402-72a8-4fe5-9700-4af97b22aa9f`
- **参数名**: `CsmProcessingMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_PROCESSING_SYNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_PROCESSING_ASYNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_PROCESSING_SYNC` (来源: AUTOSAR_ECUC)
- **描述**: Determines how the interface shall be used for that job. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

########## 2. CsmJobInterfaceUsePort

- **UUID**: `2270b16b-f834-4ef2-a790-015ca30763ca`
- **参数名**: `CsmJobInterfaceUsePort`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_USE_FNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_USE_FNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT_OPTIMIZED` (来源: AUTOSAR_ECUC)
- **描述**: Does the job need RTE interfaces?

######## 引用关系

此容器包含 **6** 个引用：

######### REFERENCE 类型引用

########## 1. CsmJobKeyRef

- **UUID**: `f2ce2b3e-107c-431d-90dc-617c42bf3c4d`
- **引用名**: `CsmJobKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key which shall be used for the CsmPrimitive. It's possible to use a CsmKey for different jobs

########## 2. CsmJobPrimitiveCallbackRef

- **UUID**: `96a9b469-fac7-463a-a9b5-7c7d330c53ca`
- **引用名**: `CsmJobPrimitiveCallbackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallback`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmCallbacks/CsmCallback`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CsmCallback.

########## 3. CsmJobPrimitiveRef

- **UUID**: `72d2fe52-81d6-496a-a011-de45774943d0`
- **引用名**: `CsmJobPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmPrimitives`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmPrimitives`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CsmPrimitive.

########## 4. CsmJobQueueRef

- **UUID**: `2e583119-a325-4454-8d0e-c27c79cf64aa`
- **引用名**: `CsmJobQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the queue.

########## 5. CsmJobCalloutRef

- **UUID**: `59569436-cced-4273-a82b-7bd0809cf1ae`
- **引用名**: `CsmJobCalloutRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallout`
- **完整路径**: `/MICROSAR/Csm/CsmCallouts/CsmCallout`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used CsmCallout. It contains a pre- and a post-job callout reference.

########## 6. CsmInOutRedirectionRef

- **UUID**: `e050a4fb-582f-454c-875d-a37c9886beae`
- **引用名**: `CsmInOutRedirectionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmInOutRedirection`
- **完整路径**: `/MICROSAR/Csm/CsmInOutRedirections/CsmInOutRedirection`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used redirection

##### 6. CsmJob

**容器属性**:

- **UUID**: `8b866d41-ea5b-4e3d-bfd1-3bdfe21f5353`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJob`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of CSM job. The container name serves as a symbolic name for the identifier of a job configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. CsmJobId

- **UUID**: `b4292d14-34aa-40b4-822e-7aa95d2c7414`
- **参数名**: `CsmJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the CSM job

######## 2. CsmJobPriority

- **UUID**: `a86f159f-7a11-46ae-b903-2b7cff47d112`
- **参数名**: `CsmJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Priority of the job.
The higher the value, the higher the job's priority.

####### BOOLEAN 类型参数

######## 1. CsmJobPrimitiveCallbackUpdateNotification

- **UUID**: `46d9db8a-5573-4514-a503-52b2a8a4a48f`
- **参数名**: `CsmJobPrimitiveCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter indicates, whether the callback function shall be called, if the UPDATE operation has been finished.

######## 2. CsmJobUsePort

- **UUID**: `3f58d478-639c-494f-a71c-dded3efd2507`
- **参数名**: `CsmJobUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Does the job need RTE interfaces?

####### ENUMERATION 类型参数

######## 1. CsmProcessingMode

- **UUID**: `b3ead402-72a8-4fe5-9700-4af97b22aa9f`
- **参数名**: `CsmProcessingMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_PROCESSING_SYNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_PROCESSING_ASYNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_PROCESSING_SYNC` (来源: AUTOSAR_ECUC)
- **描述**: Determines how the interface shall be used for that job. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

######## 2. CsmJobInterfaceUsePort

- **UUID**: `2270b16b-f834-4ef2-a790-015ca30763ca`
- **参数名**: `CsmJobInterfaceUsePort`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_USE_FNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_USE_FNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT_OPTIMIZED` (来源: AUTOSAR_ECUC)
- **描述**: Does the job need RTE interfaces?

###### 引用关系

此容器包含 **6** 个引用：

####### REFERENCE 类型引用

######## 1. CsmJobKeyRef

- **UUID**: `f2ce2b3e-107c-431d-90dc-617c42bf3c4d`
- **引用名**: `CsmJobKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key which shall be used for the CsmPrimitive. It's possible to use a CsmKey for different jobs

######## 2. CsmJobPrimitiveCallbackRef

- **UUID**: `96a9b469-fac7-463a-a9b5-7c7d330c53ca`
- **引用名**: `CsmJobPrimitiveCallbackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallback`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmCallbacks/CsmCallback`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CsmCallback.

######## 3. CsmJobPrimitiveRef

- **UUID**: `72d2fe52-81d6-496a-a011-de45774943d0`
- **引用名**: `CsmJobPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmPrimitives`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmPrimitives`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CsmPrimitive.

######## 4. CsmJobQueueRef

- **UUID**: `2e583119-a325-4454-8d0e-c27c79cf64aa`
- **引用名**: `CsmJobQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the queue.

######## 5. CsmJobCalloutRef

- **UUID**: `59569436-cced-4273-a82b-7bd0809cf1ae`
- **引用名**: `CsmJobCalloutRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallout`
- **完整路径**: `/MICROSAR/Csm/CsmCallouts/CsmCallout`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: This parameter refers to the used CsmCallout. It contains a pre- and a post-job callout reference.

######## 6. CsmInOutRedirectionRef

- **UUID**: `e050a4fb-582f-454c-875d-a37c9886beae`
- **引用名**: `CsmInOutRedirectionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmInOutRedirection`
- **完整路径**: `/MICROSAR/Csm/CsmInOutRedirections/CsmInOutRedirection`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used redirection

##### 7. CsmKeys

**容器属性**:

- **UUID**: `4cb8b98c-1b7b-429c-affc-ec2ae093ce84`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeys`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for CSM key configurations.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKey

**容器属性**:

- **UUID**: `74ee2dc7-cc3c-4b0a-95c3-0a2ddfe41e40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKey`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CsmKeyId

- **UUID**: `57020012-e309-40c0-be16-a1d2abfb72c6`
- **参数名**: `CsmKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the CsmKey

######### BOOLEAN 类型参数

########## 1. CsmKeyUsePort

- **UUID**: `79075724-12fb-45cd-a32e-babc2cf8ba69`
- **参数名**: `CsmKeyUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Does the key need RTE interfaces?

######### ENUMERATION 类型参数

########## 1. CsmKeySwcInterfaceVersion

- **UUID**: `425e730e-32cd-4d7f-8ea5-bcbad80a0b08`
- **参数名**: `CsmKeySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this key should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 changes the direction of the operation KeyElementGet's keyLength parameter from OUT to INOUT and introduces the following additional error codes to the interface's operations:
CertificateParse:		CSM_E_KEY_EMPTY
CertificateVerify:		CSM_E_KEY_EMPTY
KeyCopy:			CSM_E_KEY_EMPTY
KeyDerive:		CSM_E_KEY_EMPTY, CSM_E_BUSY, CSM_E_KEY_READ_FAIL, CSM_E_KEY_WRITE_FAIL, CSM_E_KEY_SIZE_MISMATCH
KeyElementCopy:		CSM_E_KEY_EMPTY
KeyElementGet:		CSM_E_KEY_EMPTY
KeyExchangeCalcPubVal:	CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
KeyExchangeCalcSecret:	CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
KeyGenerate:		CSM_E_KEY_EMPTY, CSM_E_BUSY

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmKeyRef

- **UUID**: `b4890c85-9cb9-4d8e-b36e-c2c7ba57c963`
- **引用名**: `CsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CryIfKey. The underlying CryIfKey refers to a specific CryptoKey in the Crypto Driver.

##### 8. CsmKey

**容器属性**:

- **UUID**: `74ee2dc7-cc3c-4b0a-95c3-0a2ddfe41e40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKey`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyId

- **UUID**: `57020012-e309-40c0-be16-a1d2abfb72c6`
- **参数名**: `CsmKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: Identifier of the CsmKey

####### BOOLEAN 类型参数

######## 1. CsmKeyUsePort

- **UUID**: `79075724-12fb-45cd-a32e-babc2cf8ba69`
- **参数名**: `CsmKeyUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Does the key need RTE interfaces?

####### ENUMERATION 类型参数

######## 1. CsmKeySwcInterfaceVersion

- **UUID**: `425e730e-32cd-4d7f-8ea5-bcbad80a0b08`
- **参数名**: `CsmKeySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this key should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 changes the direction of the operation KeyElementGet's keyLength parameter from OUT to INOUT and introduces the following additional error codes to the interface's operations:
CertificateParse:		CSM_E_KEY_EMPTY
CertificateVerify:		CSM_E_KEY_EMPTY
KeyCopy:			CSM_E_KEY_EMPTY
KeyDerive:		CSM_E_KEY_EMPTY, CSM_E_BUSY, CSM_E_KEY_READ_FAIL, CSM_E_KEY_WRITE_FAIL, CSM_E_KEY_SIZE_MISMATCH
KeyElementCopy:		CSM_E_KEY_EMPTY
KeyElementGet:		CSM_E_KEY_EMPTY
KeyExchangeCalcPubVal:	CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
KeyExchangeCalcSecret:	CSM_E_KEY_EMPTY, CSM_E_SMALL_BUFFER
KeyGenerate:		CSM_E_KEY_EMPTY, CSM_E_BUSY

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmKeyRef

- **UUID**: `b4890c85-9cb9-4d8e-b36e-c2c7ba57c963`
- **引用名**: `CsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the used CryIfKey. The underlying CryIfKey refers to a specific CryptoKey in the Crypto Driver.

##### 9. CsmPrimitives

**容器属性**:

- **UUID**: `87f9b2de-8c3d-40c2-b1b3-a7253f073a79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmPrimitives`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of CsmPrimitives

###### 配置容器

本模块包含 **38** 个配置容器：

####### 1. CsmAEADDecrypt

**容器属性**:

- **UUID**: `d735c9b4-5191-4bd0-9e22-95d135a5f8bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration of AEAD decryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `16c65ae5-43de-4174-a48f-4ab5956b8cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `1a375493-ae95-4425-8b6b-a342672efe0e`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD decryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

############ 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `131fa2cb-7ecf-4d51-80ca-79b98bc1e39f`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

############ 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `56ebf065-e00d-4601-b69a-c90433f31988`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext in bytes

############ 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `9ddf7bec-61c1-40ea-b19d-4ba731d99f3a`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output plaintext length in bytes

############ 5. CsmAEADDecryptTagLength

- **UUID**: `8e257428-879e-477c-a103-aab2faa944e0`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input Tag length in BITS

########### STRING 类型参数

############ 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `a87f8f86-eebf-444d-acb5-cae57d1710e5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

############ 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `241cecfa-d109-4faf-be60-c1dd46bdb214`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `f04e5c20-2a65-47dd-b1c9-496192e5b440`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `d11fcb27-97f7-4a1f-b9d6-2d9a16b5dc47`
- **参数名**: `CsmAEADDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `d60f7329-32e8-4664-a6a7-dba74b6b0ed9`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmAEADDecryptProcessing

- **UUID**: `40356098-006c-48dd-8158-24bd2058a580`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 5. CsmAEADDecryptSwcInterfaceVersion

- **UUID**: `2cb71cb2-be50-4758-9b1d-de819297646b`
- **参数名**: `CsmAEADDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADDecrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. CsmAEADDecryptKeyRef

- **UUID**: `4d6b66b0-38c0-453c-94e7-f127ebf34c54`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that decryption primitive.

############ 2. CsmAEADDecryptQueueRef

- **UUID**: `be0a5c60-555f-4d2f-88bd-959bcf2a484c`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that decryption primitive.

####### 2. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `16c65ae5-43de-4174-a48f-4ab5956b8cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `1a375493-ae95-4425-8b6b-a342672efe0e`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD decryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `131fa2cb-7ecf-4d51-80ca-79b98bc1e39f`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `56ebf065-e00d-4601-b69a-c90433f31988`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext in bytes

########## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `9ddf7bec-61c1-40ea-b19d-4ba731d99f3a`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output plaintext length in bytes

########## 5. CsmAEADDecryptTagLength

- **UUID**: `8e257428-879e-477c-a103-aab2faa944e0`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input Tag length in BITS

######### STRING 类型参数

########## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `a87f8f86-eebf-444d-acb5-cae57d1710e5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

########## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `241cecfa-d109-4faf-be60-c1dd46bdb214`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `f04e5c20-2a65-47dd-b1c9-496192e5b440`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `d11fcb27-97f7-4a1f-b9d6-2d9a16b5dc47`
- **参数名**: `CsmAEADDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `d60f7329-32e8-4664-a6a7-dba74b6b0ed9`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmAEADDecryptProcessing

- **UUID**: `40356098-006c-48dd-8158-24bd2058a580`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmAEADDecryptSwcInterfaceVersion

- **UUID**: `2cb71cb2-be50-4758-9b1d-de819297646b`
- **参数名**: `CsmAEADDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADDecrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADDecryptKeyRef

- **UUID**: `4d6b66b0-38c0-453c-94e7-f127ebf34c54`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that decryption primitive.

########## 2. CsmAEADDecryptQueueRef

- **UUID**: `be0a5c60-555f-4d2f-88bd-959bcf2a484c`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that decryption primitive.

####### 3. CsmAEADEncrypt

**容器属性**:

- **UUID**: `e7936f4e-bb99-4d9e-8aee-47dec52a6980`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration of AEAD encryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `54b685a3-6832-4bf2-9563-eec537185b81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `fb4eb104-97f9-4d53-ba5c-2765d320dda6`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD encryption key. 
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

############ 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `8a1ce7e6-8e61-41a1-afa3-5c79304cad26`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

############ 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `bdd2a300-d67f-41ae-8082-da127b4eae97`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output ciphertext length in bytes

############ 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `d9061c72-2361-4ee0-8253-cb8eea63742d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

############ 5. CsmAEADEncryptTagLength

- **UUID**: `8217dc92-f473-4931-88eb-ce1e2375345e`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output Tag length in bytes

########### STRING 类型参数

############ 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `ff509353-8812-4f4a-b7f6-43afadd0f0a6`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

############ 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `a176d168-1857-4312-846b-9ab8787e0f8b`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `e62e6830-3cde-4ac8-956c-19896fd94b82`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `4974fb0a-4e0b-4ff5-9c7b-c9fa5bdc3522`
- **参数名**: `CsmAEADEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c91e9329-6c87-4c92-8a2e-e60bd76b0362`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmAEADEncryptProcessing

- **UUID**: `6faf775c-33f9-4896-a687-54d2f0caf4dc`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 5. CsmAEADEncryptSwcInterfaceVersion

- **UUID**: `1fbe048c-9241-434f-a667-2bf715865234`
- **参数名**: `CsmAEADEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Encrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. CsmAEADEncryptKeyRef

- **UUID**: `c13bfd9d-cb0a-4a57-b828-a42e20d40d10`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that encryption primitive.

############ 2. CsmAEADEncryptQueueRef

- **UUID**: `f545978a-e55c-4de2-b878-b6577bc63eb2`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that encryption primitive.

####### 4. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `54b685a3-6832-4bf2-9563-eec537185b81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `fb4eb104-97f9-4d53-ba5c-2765d320dda6`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD encryption key. 
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `8a1ce7e6-8e61-41a1-afa3-5c79304cad26`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `bdd2a300-d67f-41ae-8082-da127b4eae97`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output ciphertext length in bytes

########## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `d9061c72-2361-4ee0-8253-cb8eea63742d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

########## 5. CsmAEADEncryptTagLength

- **UUID**: `8217dc92-f473-4931-88eb-ce1e2375345e`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output Tag length in bytes

######### STRING 类型参数

########## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `ff509353-8812-4f4a-b7f6-43afadd0f0a6`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

########## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `a176d168-1857-4312-846b-9ab8787e0f8b`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `e62e6830-3cde-4ac8-956c-19896fd94b82`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `4974fb0a-4e0b-4ff5-9c7b-c9fa5bdc3522`
- **参数名**: `CsmAEADEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c91e9329-6c87-4c92-8a2e-e60bd76b0362`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmAEADEncryptProcessing

- **UUID**: `6faf775c-33f9-4896-a687-54d2f0caf4dc`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmAEADEncryptSwcInterfaceVersion

- **UUID**: `1fbe048c-9241-434f-a667-2bf715865234`
- **参数名**: `CsmAEADEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Encrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADEncryptKeyRef

- **UUID**: `c13bfd9d-cb0a-4a57-b828-a42e20d40d10`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that encryption primitive.

########## 2. CsmAEADEncryptQueueRef

- **UUID**: `f545978a-e55c-4de2-b878-b6577bc63eb2`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that encryption primitive.

####### 5. CsmDecrypt

**容器属性**:

- **UUID**: `3142a8d1-ace8-4b5e-b6f8-667ac803e0ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of Decryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmDecryptConfig

**容器属性**:

- **UUID**: `2ae2e6d4-c7af-4152-b0c1-aeefa146c6ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `9a39cc5b-729a-4928-84a6-633485a41f07`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

############ 2. CsmDecryptDataMaxLength

- **UUID**: `7283c433-24f9-4fe0-80d5-e5295282bde2`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext length in bytes

############ 3. CsmDecryptResultMaxLength

- **UUID**: `9f54d592-38e2-4c07-b93c-e4933a71ac42`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output plaintext length in bytes

########### STRING 类型参数

############ 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `bd69c14c-5a37-44a0-a0ff-643272e145c2`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

############ 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `6ebaefc8-18b9-4b58-af48-3ac48cdb0009`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `fffb4375-774e-4aa6-a06b-f93c1d07d58b`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `88e56366-b730-43b9-b746-53572abab161`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmDecryptAlgorithmFamily

- **UUID**: `1c98b7e1-1a0b-42d3-876c-eb54087630e8`
- **参数名**: `CsmDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmDecryptAlgorithmMode

- **UUID**: `51f3901a-1309-4d83-bc21-60e882dc4ec1`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `c9e2923d-fd05-4ce1-8dac-fca49691429a`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 5. CsmDecryptProcessing

- **UUID**: `76b71b58-ebea-4dc8-8e8e-e88b19672af6`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmDecryptSwcInterfaceVersion

- **UUID**: `68c5f9dc-0e59-4fc8-a302-10a91ef97517`
- **参数名**: `CsmDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Decrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 6. CsmDecryptConfig

**容器属性**:

- **UUID**: `2ae2e6d4-c7af-4152-b0c1-aeefa146c6ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `9a39cc5b-729a-4928-84a6-633485a41f07`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmDecryptDataMaxLength

- **UUID**: `7283c433-24f9-4fe0-80d5-e5295282bde2`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext length in bytes

########## 3. CsmDecryptResultMaxLength

- **UUID**: `9f54d592-38e2-4c07-b93c-e4933a71ac42`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output plaintext length in bytes

######### STRING 类型参数

########## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `bd69c14c-5a37-44a0-a0ff-643272e145c2`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

########## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `6ebaefc8-18b9-4b58-af48-3ac48cdb0009`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `fffb4375-774e-4aa6-a06b-f93c1d07d58b`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `88e56366-b730-43b9-b746-53572abab161`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmFamily

- **UUID**: `1c98b7e1-1a0b-42d3-876c-eb54087630e8`
- **参数名**: `CsmDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmDecryptAlgorithmMode

- **UUID**: `51f3901a-1309-4d83-bc21-60e882dc4ec1`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `c9e2923d-fd05-4ce1-8dac-fca49691429a`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 5. CsmDecryptProcessing

- **UUID**: `76b71b58-ebea-4dc8-8e8e-e88b19672af6`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmDecryptSwcInterfaceVersion

- **UUID**: `68c5f9dc-0e59-4fc8-a302-10a91ef97517`
- **参数名**: `CsmDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Decrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 7. CsmEncrypt

**容器属性**:

- **UUID**: `85c74ce5-750b-4c1b-8773-d8e6d98d6cd3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of Encryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmEncryptConfig

**容器属性**:

- **UUID**: `e76a2714-5720-4560-93ed-4e955de2c30d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmEncryptDataMaxLength

- **UUID**: `9b814c0a-ace5-4277-bcef-e8f5bb2080c3`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

############ 2. CsmEncryptResultMaxLength

- **UUID**: `cc22b951-be04-4e12-90e0-11ad5414678c`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output cipher length in bytes

############ 3. CsmEncryptAlgorithmKeyLength

- **UUID**: `c827e260-516b-4f43-af56-6551b4cb7b55`
- **参数名**: `CsmEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########### STRING 类型参数

############ 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `8f551a9c-bced-433f-98c9-fdc4419f60ef`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

############ 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `0e06ee40-f2a8-4bdd-9457-63811c02d212`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `e738fda2-8cea-4556-8845-77efd342d8e2`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `7efe5788-c82e-46bf-a4b3-51a410dd6561`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmEncryptAlgorithmFamily

- **UUID**: `106cf0bf-54b7-4eed-a6be-d8baf03d1c0d`
- **参数名**: `CsmEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmEncryptAlgorithmMode

- **UUID**: `12940fb2-2a5c-4b07-b8cd-c9648f7de946`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `5d4934ca-4bbe-4f79-bb2a-84ec1a8373a1`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

############ 5. CsmEncryptProcessing

- **UUID**: `353f410c-be0b-40bc-8004-7afef00b6950`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmEncryptSwcInterfaceVersion

- **UUID**: `dda01b88-4a62-490c-9e70-8b9e8d22bf93`
- **参数名**: `CsmEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADEncrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 8. CsmEncryptConfig

**容器属性**:

- **UUID**: `e76a2714-5720-4560-93ed-4e955de2c30d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmEncryptDataMaxLength

- **UUID**: `9b814c0a-ace5-4277-bcef-e8f5bb2080c3`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

########## 2. CsmEncryptResultMaxLength

- **UUID**: `cc22b951-be04-4e12-90e0-11ad5414678c`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output cipher length in bytes

########## 3. CsmEncryptAlgorithmKeyLength

- **UUID**: `c827e260-516b-4f43-af56-6551b4cb7b55`
- **参数名**: `CsmEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `8f551a9c-bced-433f-98c9-fdc4419f60ef`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

########## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `0e06ee40-f2a8-4bdd-9457-63811c02d212`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `e738fda2-8cea-4556-8845-77efd342d8e2`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `7efe5788-c82e-46bf-a4b3-51a410dd6561`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmFamily

- **UUID**: `106cf0bf-54b7-4eed-a6be-d8baf03d1c0d`
- **参数名**: `CsmEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmEncryptAlgorithmMode

- **UUID**: `12940fb2-2a5c-4b07-b8cd-c9648f7de946`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `5d4934ca-4bbe-4f79-bb2a-84ec1a8373a1`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmEncryptProcessing

- **UUID**: `353f410c-be0b-40bc-8004-7afef00b6950`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmEncryptSwcInterfaceVersion

- **UUID**: `dda01b88-4a62-490c-9e70-8b9e8d22bf93`
- **参数名**: `CsmEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADEncrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 9. CsmHash

**容器属性**:

- **UUID**: `3351d4ea-8498-4215-b0f2-faec50099c63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHash`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for Hash Configurations

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmHashConfig

**容器属性**:

- **UUID**: `5ff1390d-0b6f-4982-8411-1fb9f766a00c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. CsmHashDataMaxLength

- **UUID**: `bcb708d8-5908-4839-b6b8-284b1e70b27e`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

############ 2. CsmHashResultLength

- **UUID**: `78a5b9e2-5899-40c6-aa61-99c764ea7d28`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output hash length in bytes

########### STRING 类型参数

############ 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `1dfe4aab-ec07-417c-af6e-b28dd3e08978`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

############ 2. CsmHashAlgorithmModeCustom

- **UUID**: `ce7eee6e-f2b2-4a7e-af1f-a53ed6c28b41`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

############ 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `c4924324-32c5-4e14-ba8d-277f011e1c55`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmHashAlgorithmFamiliy

- **UUID**: `40be8690-0416-47e8-84c1-4d2a88a8b840`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmHashAlgorithmFamily

- **UUID**: `46dd10e9-0400-47a6-93df-e1ab429d97b0`
- **参数名**: `CsmHashAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmHashAlgorithmMode

- **UUID**: `303f6a0d-de7b-4177-a2b7-e227f4a560c7`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmHashAlgorithmSecondaryFamily

- **UUID**: `16e9468d-057b-48fe-90bf-a1f77116912f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

############ 5. CsmHashProcessing

- **UUID**: `5043a314-1ac4-4756-950a-1a8f81e21d4a`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmHashSwcInterfaceVersion

- **UUID**: `62c5e599-d6d5-4c34-94b7-7701ed0e7f1d`
- **参数名**: `CsmHashSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
CancelJob: 	CSM_E_JOB_CANCELED

####### 10. CsmHashConfig

**容器属性**:

- **UUID**: `5ff1390d-0b6f-4982-8411-1fb9f766a00c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. CsmHashDataMaxLength

- **UUID**: `bcb708d8-5908-4839-b6b8-284b1e70b27e`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########## 2. CsmHashResultLength

- **UUID**: `78a5b9e2-5899-40c6-aa61-99c764ea7d28`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output hash length in bytes

######### STRING 类型参数

########## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `1dfe4aab-ec07-417c-af6e-b28dd3e08978`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

########## 2. CsmHashAlgorithmModeCustom

- **UUID**: `ce7eee6e-f2b2-4a7e-af1f-a53ed6c28b41`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `c4924324-32c5-4e14-ba8d-277f011e1c55`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmHashAlgorithmFamiliy

- **UUID**: `40be8690-0416-47e8-84c1-4d2a88a8b840`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmFamily

- **UUID**: `46dd10e9-0400-47a6-93df-e1ab429d97b0`
- **参数名**: `CsmHashAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmHashAlgorithmMode

- **UUID**: `303f6a0d-de7b-4177-a2b7-e227f4a560c7`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmHashAlgorithmSecondaryFamily

- **UUID**: `16e9468d-057b-48fe-90bf-a1f77116912f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmHashProcessing

- **UUID**: `5043a314-1ac4-4756-950a-1a8f81e21d4a`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmHashSwcInterfaceVersion

- **UUID**: `62c5e599-d6d5-4c34-94b7-7701ed0e7f1d`
- **参数名**: `CsmHashSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
CancelJob: 	CSM_E_JOB_CANCELED

####### 11. CsmMacGenerate

**容器属性**:

- **UUID**: `5689caab-3a47-4e1f-abec-e67486d5d270`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of MacGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `7ba6c34e-58b4-40d4-86f6-ae9f10fa275d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `590ebb0b-bf74-4b1d-a0f5-b4c275140d97`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

############ 2. CsmMacGenerateDataMaxLength

- **UUID**: `fd1ef23f-ad64-4d11-9212-303ad907c894`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

############ 3. CsmMacGenerateResultLength

- **UUID**: `f4a8c073-d9b3-4a1d-8408-dce31f4d359e`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output MAC length in bytes

########### STRING 类型参数

############ 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `1de2c6ef-33f7-484c-9497-311fef6cf93f`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family,

############ 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `594894f7-3af5-41a8-b5ae-39bcd9ba71a4`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `88e91b76-faa9-47c0-9b05-aabe458e4f93`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

########### ENUMERATION 类型参数

############ 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `8150635e-893f-45b5-ba70-e46c07d3f7ca`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `3cd160db-ec74-4c1c-a038-c6bcbfb749e6`
- **参数名**: `CsmMacGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmMacGenerateAlgorithmMode

- **UUID**: `b20b076b-c935-4ebf-9c43-e67708061c97`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `33158cac-def0-464a-a065-8809b45a08e5`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 5. CsmMacGenerateProcessing

- **UUID**: `ccd17e6f-db6e-47cb-bfd7-9d7931acdb10`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmMacGenerateSwcInterfaceVersion

- **UUID**: `e5ea84ff-eec6-4c95-928d-1b01a6fcebce`
- **参数名**: `CsmMacGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacGenerate:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 12. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `7ba6c34e-58b4-40d4-86f6-ae9f10fa275d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `590ebb0b-bf74-4b1d-a0f5-b4c275140d97`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmMacGenerateDataMaxLength

- **UUID**: `fd1ef23f-ad64-4d11-9212-303ad907c894`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########## 3. CsmMacGenerateResultLength

- **UUID**: `f4a8c073-d9b3-4a1d-8408-dce31f4d359e`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output MAC length in bytes

######### STRING 类型参数

########## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `1de2c6ef-33f7-484c-9497-311fef6cf93f`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family,

########## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `594894f7-3af5-41a8-b5ae-39bcd9ba71a4`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `88e91b76-faa9-47c0-9b05-aabe458e4f93`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

######### ENUMERATION 类型参数

########## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `8150635e-893f-45b5-ba70-e46c07d3f7ca`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `3cd160db-ec74-4c1c-a038-c6bcbfb749e6`
- **参数名**: `CsmMacGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `b20b076b-c935-4ebf-9c43-e67708061c97`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `33158cac-def0-464a-a065-8809b45a08e5`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 5. CsmMacGenerateProcessing

- **UUID**: `ccd17e6f-db6e-47cb-bfd7-9d7931acdb10`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmMacGenerateSwcInterfaceVersion

- **UUID**: `e5ea84ff-eec6-4c95-928d-1b01a6fcebce`
- **参数名**: `CsmMacGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacGenerate:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 13. CsmMacVerify

**容器属性**:

- **UUID**: `0fb8fdb0-acbd-41c1-8075-dc6823e67967`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of MacVerify primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `66b6a9f8-f77b-400b-8a23-a8ace40a7407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmMacVerifyCompareLength

- **UUID**: `9a257862-800a-4742-a8f4-9cc855f4905b`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input MAC length, that shall be verified, in BITS

############ 2. CsmMacVerifyDataMaxLength

- **UUID**: `64861c81-aee1-4ed7-8d77-ba208097628c`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length, for which MAC shall be verified, in bytes

############ 3. CsmMacVerifyAlgorithmKeyLength

- **UUID**: `56ef7bb5-ab53-4834-93f0-503621405261`
- **参数名**: `CsmMacVerifyAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########### STRING 类型参数

############ 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `92314156-249e-44e7-9850-3a057508a969`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service

############ 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `22d21fa5-fc9f-461b-b0d4-0380bbf7c5e1`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

############ 3. CsmMacVerifyAlgorithmModeCustom

- **UUID**: `b336d831-ce60-483e-8524-605f32e14298`
- **参数名**: `CsmMacVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

########### ENUMERATION 类型参数

############ 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `c9caa2c2-cb89-4785-bc64-f4a3f052c5aa`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `d8789fbe-192f-4655-8084-98495d873a73`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `f770d9cf-44da-409d-ad7c-94b9c666a9ed`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 4. CsmMacVerifyProcessing

- **UUID**: `abdc3e40-3d83-4e6e-8a6a-9bbbf2ade8ba`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 5. CsmMacVerifyAlgorithmMode

- **UUID**: `fb6e75e9-c8ad-4304-914b-76929329f588`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service.

############ 6. CsmMacVerifySwcInterfaceVersion

- **UUID**: `d48a2a24-274e-46ae-9ca1-4e4b93fb2d8a`
- **参数名**: `CsmMacVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 14. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `66b6a9f8-f77b-400b-8a23-a8ace40a7407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacVerifyCompareLength

- **UUID**: `9a257862-800a-4742-a8f4-9cc855f4905b`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input MAC length, that shall be verified, in BITS

########## 2. CsmMacVerifyDataMaxLength

- **UUID**: `64861c81-aee1-4ed7-8d77-ba208097628c`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length, for which MAC shall be verified, in bytes

########## 3. CsmMacVerifyAlgorithmKeyLength

- **UUID**: `56ef7bb5-ab53-4834-93f0-503621405261`
- **参数名**: `CsmMacVerifyAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `92314156-249e-44e7-9850-3a057508a969`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `22d21fa5-fc9f-461b-b0d4-0380bbf7c5e1`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

########## 3. CsmMacVerifyAlgorithmModeCustom

- **UUID**: `b336d831-ce60-483e-8524-605f32e14298`
- **参数名**: `CsmMacVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

######### ENUMERATION 类型参数

########## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `c9caa2c2-cb89-4785-bc64-f4a3f052c5aa`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `d8789fbe-192f-4655-8084-98495d873a73`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `f770d9cf-44da-409d-ad7c-94b9c666a9ed`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmMacVerifyProcessing

- **UUID**: `abdc3e40-3d83-4e6e-8a6a-9bbbf2ade8ba`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmMacVerifyAlgorithmMode

- **UUID**: `fb6e75e9-c8ad-4304-914b-76929329f588`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service.

########## 6. CsmMacVerifySwcInterfaceVersion

- **UUID**: `d48a2a24-274e-46ae-9ca1-4e4b93fb2d8a`
- **参数名**: `CsmMacVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 15. CsmRandomGenerate

**容器属性**:

- **UUID**: `2c2523be-f7d5-456d-bd14-3e890d2b2bc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of RandomGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `5729fbf0-2ba4-4d84-b9b8-a87c57a86115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. CsmRandomGenerateResultLength

- **UUID**: `02bde8ad-ea44-4565-b540-da57744cdd52`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the random generate key in bytes

########### STRING 类型参数

############ 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `5e9f3c5f-88e2-4c48-bb64-a219725f3094`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

############ 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `0786f734-73c8-4207-84d6-755086325eda`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

############ 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `d72d056c-c840-464e-9171-186e25f1313d`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `65f30f84-9ed7-45a4-95e6-1034fcc13342`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `6d5b7b2d-2137-453c-853d-7f2ae2ccfa34`
- **参数名**: `CsmRandomGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f4ef354d-df08-41c2-8d42-80029955fb0b`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `5c94efa0-646e-40e7-9e4f-3d3c917c6028`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

############ 5. CsmRandomGenerateProcessing

- **UUID**: `f2551403-d13a-4c3d-833b-bd8e298d093e`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

####### 16. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `5729fbf0-2ba4-4d84-b9b8-a87c57a86115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmRandomGenerateResultLength

- **UUID**: `02bde8ad-ea44-4565-b540-da57744cdd52`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the random generate key in bytes

######### STRING 类型参数

########## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `5e9f3c5f-88e2-4c48-bb64-a219725f3094`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

########## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `0786f734-73c8-4207-84d6-755086325eda`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

########## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `d72d056c-c840-464e-9171-186e25f1313d`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `65f30f84-9ed7-45a4-95e6-1034fcc13342`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `6d5b7b2d-2137-453c-853d-7f2ae2ccfa34`
- **参数名**: `CsmRandomGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f4ef354d-df08-41c2-8d42-80029955fb0b`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `5c94efa0-646e-40e7-9e4f-3d3c917c6028`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmRandomGenerateProcessing

- **UUID**: `f2551403-d13a-4c3d-833b-bd8e298d093e`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

####### 17. CsmSecureCounter

**容器属性**:

- **UUID**: `cdabafe4-0b67-40e1-bef0-19206cfa15e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounter`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SecureCounter primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `95cde3f3-6e48-4dba-a938-f51be4b8a8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. CsmSecureCounterProcessing

- **UUID**: `2be95d73-e5ed-4a3b-941e-b463234083eb`
- **参数名**: `CsmSecureCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_SYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS`
  - `CSM_SYNCHRONOUS`
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CsmSecureCounterQueueRef

- **UUID**: `2da71ed8-ae40-4ca7-b488-da34778d7efc`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that secure counter.

####### 18. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `95cde3f3-6e48-4dba-a938-f51be4b8a8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmSecureCounterProcessing

- **UUID**: `2be95d73-e5ed-4a3b-941e-b463234083eb`
- **参数名**: `CsmSecureCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_SYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS`
  - `CSM_SYNCHRONOUS`
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CsmSecureCounterQueueRef

- **UUID**: `2da71ed8-ae40-4ca7-b488-da34778d7efc`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that secure counter.

####### 19. CsmSignatureGenerate

**容器属性**:

- **UUID**: `28a93b87-e9d7-497e-9f52-ce15e06cf9f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SignatureGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `ec921f3e-c770-4020-8b3b-08d5b3c22c59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `01208c6b-02d1-4d0d-a463-593aa9f12e81`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length in bytes

############ 2. CsmSignatureGenerateKeyLength

- **UUID**: `28ad616e-0a1a-4585-bfab-8a125fdd1314`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature generate key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

############ 3. CsmSignatureGenerateResultLength

- **UUID**: `b065f2f1-9299-4539-b5e7-4383ade6da2c`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output signature length in bytes

########### STRING 类型参数

############ 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `b754a5c1-c09f-410e-b828-3f9efeeebb91`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `ace204e5-2409-41b3-a3a4-9ea39ee9500e`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f57c8137-e31a-4162-80d0-4cea6105a303`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `07e9c943-419c-48a5-a740-0d9c127a71d6`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `bd8a72ad-e365-4046-a007-d3360338e326`
- **参数名**: `CsmSignatureGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `7e3cbb74-9cbe-4198-ae9b-a333d932ee9a`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `94efbcdb-91b9-44f2-ade8-25e4752311ac`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 5. CsmSignatureGenerateProcessing

- **UUID**: `ca5a333c-29c9-4023-b788-897958ae0837`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmSignatureGenerateSwcInterfaceVersion

- **UUID**: `5fca0b76-bea9-45c8-a2bc-89cf19bc4973`
- **参数名**: `CsmSignatureGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 20. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `ec921f3e-c770-4020-8b3b-08d5b3c22c59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `01208c6b-02d1-4d0d-a463-593aa9f12e81`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length in bytes

########## 2. CsmSignatureGenerateKeyLength

- **UUID**: `28ad616e-0a1a-4585-bfab-8a125fdd1314`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature generate key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 3. CsmSignatureGenerateResultLength

- **UUID**: `b065f2f1-9299-4539-b5e7-4383ade6da2c`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output signature length in bytes

######### STRING 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `b754a5c1-c09f-410e-b828-3f9efeeebb91`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `ace204e5-2409-41b3-a3a4-9ea39ee9500e`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f57c8137-e31a-4162-80d0-4cea6105a303`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `07e9c943-419c-48a5-a740-0d9c127a71d6`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `bd8a72ad-e365-4046-a007-d3360338e326`
- **参数名**: `CsmSignatureGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `7e3cbb74-9cbe-4198-ae9b-a333d932ee9a`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `94efbcdb-91b9-44f2-ade8-25e4752311ac`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 5. CsmSignatureGenerateProcessing

- **UUID**: `ca5a333c-29c9-4023-b788-897958ae0837`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmSignatureGenerateSwcInterfaceVersion

- **UUID**: `5fca0b76-bea9-45c8-a2bc-89cf19bc4973`
- **参数名**: `CsmSignatureGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 21. CsmSignatureVerify

**容器属性**:

- **UUID**: `c5d57db1-7d62-43f2-8331-8cba257184e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SignatureVerify primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6762b960-93af-48bb-bfdc-7e7f2d5bfb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. CsmSignatureVerifyCompareLength

- **UUID**: `b13fff76-aa93-4fa4-9118-da905815eaf0`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

############ 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `3ad0c1d5-eaad-40d5-8433-ac9209c79c77`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

############ 3. CsmSignatureVerifyKeyLength

- **UUID**: `447dba54-7daf-4820-91fd-c6c2c675f4c0`
- **参数名**: `CsmSignatureVerifyKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature verify key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########### STRING 类型参数

############ 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `7a3383da-ef67-4f83-907c-53b9bf9b21a1`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

############ 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `77d20415-becd-4d5e-a574-d56e52e8652d`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `002eb5ee-ac8a-4b48-b188-8d5946776c12`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########### ENUMERATION 类型参数

############ 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `bd7c744b-b792-4fde-883e-251afe07124f`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `71c1a792-dc01-46ee-81d7-acc47a4ed31a`
- **参数名**: `CsmSignatureVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `580d0c6b-145d-4b80-9105-7a851aa09293`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `e43b33d0-92b8-4425-b9a2-74fdf2e9a5ae`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 5. CsmSignatureVerifyProcessing

- **UUID**: `778f1b69-78fd-4321-b1bf-eadb9eecb250`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

############ 6. CsmSignatureVerifySwcInterfaceVersion

- **UUID**: `14fdc583-e086-4028-a223-717684e9e1bd`
- **参数名**: `CsmSignatureVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 22. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6762b960-93af-48bb-bfdc-7e7f2d5bfb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureVerifyCompareLength

- **UUID**: `b13fff76-aa93-4fa4-9118-da905815eaf0`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

########## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `3ad0c1d5-eaad-40d5-8433-ac9209c79c77`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

########## 3. CsmSignatureVerifyKeyLength

- **UUID**: `447dba54-7daf-4820-91fd-c6c2c675f4c0`
- **参数名**: `CsmSignatureVerifyKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature verify key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `7a3383da-ef67-4f83-907c-53b9bf9b21a1`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `77d20415-becd-4d5e-a574-d56e52e8652d`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `002eb5ee-ac8a-4b48-b188-8d5946776c12`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `bd7c744b-b792-4fde-883e-251afe07124f`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `71c1a792-dc01-46ee-81d7-acc47a4ed31a`
- **参数名**: `CsmSignatureVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `580d0c6b-145d-4b80-9105-7a851aa09293`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `e43b33d0-92b8-4425-b9a2-74fdf2e9a5ae`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 5. CsmSignatureVerifyProcessing

- **UUID**: `778f1b69-78fd-4321-b1bf-eadb9eecb250`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmSignatureVerifySwcInterfaceVersion

- **UUID**: `14fdc583-e086-4028-a223-717684e9e1bd`
- **参数名**: `CsmSignatureVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

####### 23. CsmJobKeySetValid

**容器属性**:

- **UUID**: `a1db257a-7cbd-44cd-99bc-d2ec2220f0c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValid`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeySetValid primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

####### 24. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

####### 25. CsmJobKeyExchangeCalcPubVal

**容器属性**:

- **UUID**: `af6f30ca-e432-4970-89de-36e298ef961b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubVal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyExchangeCalcPubVal primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `15688ba9-0142-4fae-a0f6-63e40e663d8b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubValConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a key configuration.

########## 参数配置

此容器包含 **7** 个参数：

########### STRING 类型参数

############ 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom

- **UUID**: `b16995dc-e03d-4d42-a86a-f45148f6955f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 2. CsmJobKeyExchangeCalcPubValAlgorithmModeCustom

- **UUID**: `6ef6109b-d458-4036-859a-4d6dd7a6d236`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

############ 3. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom

- **UUID**: `13d6d865-52e2-4177-b927-69fe37acd552`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used .

########### ENUMERATION 类型参数

############ 1. CsmJobKeyExchangeCalcPubValAlgorithmFamiliy

- **UUID**: `031de714-ca71-4d4c-a674-af021dec067f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `9fd613c7-a8cd-45fd-938b-40f825dfed47`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `87269892-d6e7-4911-86a5-3363b3e86a9e`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `28dd9b0a-0d2a-4a45-93e1-0fbca48bcd26`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 26. CsmJobKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `15688ba9-0142-4fae-a0f6-63e40e663d8b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubValConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom

- **UUID**: `b16995dc-e03d-4d42-a86a-f45148f6955f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmModeCustom

- **UUID**: `6ef6109b-d458-4036-859a-4d6dd7a6d236`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom

- **UUID**: `13d6d865-52e2-4177-b927-69fe37acd552`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used .

######### ENUMERATION 类型参数

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamiliy

- **UUID**: `031de714-ca71-4d4c-a674-af021dec067f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `9fd613c7-a8cd-45fd-938b-40f825dfed47`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `87269892-d6e7-4911-86a5-3363b3e86a9e`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `28dd9b0a-0d2a-4a45-93e1-0fbca48bcd26`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 27. CsmJobKeyExchangeCalcSecret

**容器属性**:

- **UUID**: `6c193f86-0d38-43d9-9bd7-c49c44d38aa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecret`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyExchangeCalcSecret primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `7cc3e7e7-dff2-4e9c-a2c3-f13bfed833f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecretConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

########## 参数配置

此容器包含 **7** 个参数：

########### STRING 类型参数

############ 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom

- **UUID**: `2249f7fa-8204-4759-ac13-4318e2358fdd`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 2. CsmJobKeyExchangeCalcSecretAlgorithmModeCustom

- **UUID**: `1343feb6-56c0-4c08-b649-cbf1081c2c07`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

############ 3. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom

- **UUID**: `56c74b6a-53d7-4998-ac73-c9e572f0e807`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobKeyExchangeCalcSecretAlgorithmFamiliy

- **UUID**: `3f4f6dec-cf68-4fab-bd65-6c52970be6c3`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `22383b97-f8a3-424c-bf31-03aed722dcce`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `79645796-8ef0-42a2-963e-8552543c8365`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `2521a0d6-572b-4cce-b73b-c921e5fa38ed`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 28. CsmJobKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `7cc3e7e7-dff2-4e9c-a2c3-f13bfed833f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecretConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom

- **UUID**: `2249f7fa-8204-4759-ac13-4318e2358fdd`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmModeCustom

- **UUID**: `1343feb6-56c0-4c08-b649-cbf1081c2c07`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom

- **UUID**: `56c74b6a-53d7-4998-ac73-c9e572f0e807`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamiliy

- **UUID**: `3f4f6dec-cf68-4fab-bd65-6c52970be6c3`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `22383b97-f8a3-424c-bf31-03aed722dcce`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `79645796-8ef0-42a2-963e-8552543c8365`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `2521a0d6-572b-4cce-b73b-c921e5fa38ed`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 29. CsmJobKeyDerive

**容器属性**:

- **UUID**: `193cb819-106c-464e-8849-1538a60171c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDerive`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyDerive primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeyDeriveConfig

**容器属性**:

- **UUID**: `ea77b905-c682-448a-81d5-308ed051222e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDeriveConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key derive operation. The container name serves as a symbolic name for the identifier of a key derive configuration.

########## 参数配置

此容器包含 **7** 个参数：

########### STRING 类型参数

############ 1. CsmJobKeyDeriveAlgorithmModeCustom

- **UUID**: `da7f433d-c834-4c2c-b010-2d3c90fd7b48`
- **参数名**: `CsmJobKeyDeriveAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

############ 2. CsmJobKeyDeriveAlgorithmFamilyCustom

- **UUID**: `644c6329-a1cc-4c41-9606-5dacc2eee303`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 3. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom

- **UUID**: `5d47bc1f-89a9-4d69-ad05-32cd8155a645`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobKeyDeriveAlgorithmFamiliy

- **UUID**: `ef281c96-a78a-404d-8b3c-2a69fb22c571`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `567569b7-f26e-4d9f-b973-ba32e460241a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `e600b709-5a0d-49cf-9237-a4ab86964a30`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmJobKeyDeriveAlgorithmSecondaryFamily

- **UUID**: `fbd98446-c450-4ef0-8cc1-9df908a805ea`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 30. CsmJobKeyDeriveConfig

**容器属性**:

- **UUID**: `ea77b905-c682-448a-81d5-308ed051222e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDeriveConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key derive operation. The container name serves as a symbolic name for the identifier of a key derive configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyDeriveAlgorithmModeCustom

- **UUID**: `da7f433d-c834-4c2c-b010-2d3c90fd7b48`
- **参数名**: `CsmJobKeyDeriveAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

########## 2. CsmJobKeyDeriveAlgorithmFamilyCustom

- **UUID**: `644c6329-a1cc-4c41-9606-5dacc2eee303`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 3. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom

- **UUID**: `5d47bc1f-89a9-4d69-ad05-32cd8155a645`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyDeriveAlgorithmFamiliy

- **UUID**: `ef281c96-a78a-404d-8b3c-2a69fb22c571`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `567569b7-f26e-4d9f-b973-ba32e460241a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `e600b709-5a0d-49cf-9237-a4ab86964a30`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyDeriveAlgorithmSecondaryFamily

- **UUID**: `fbd98446-c450-4ef0-8cc1-9df908a805ea`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 31. CsmJobRandomSeed

**容器属性**:

- **UUID**: `b99f061c-207a-4862-bd17-bbb358989f0b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeed`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of RandomSeed primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobRandomSeedConfig

**容器属性**:

- **UUID**: `d8a2b8d8-f086-47b4-93a7-8b14fdb26ab1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeedConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random seed operation. The container name serves as a symbolic name for the identifier of a random seed configuration.

########## 参数配置

此容器包含 **6** 个参数：

########### STRING 类型参数

############ 1. CsmJobRandomSeedAlgorithmFamilyCustom

- **UUID**: `bffe13c5-ebf9-4036-9779-19656e3cea60`
- **参数名**: `CsmJobRandomSeedAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

############ 2. CsmJobRandomSeedAlgorithmModeCustom

- **UUID**: `dc676f46-ce44-4f5c-a7ba-db0387523cbc`
- **参数名**: `CsmJobRandomSeedAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

############ 3. CsmJobRandomSeedAlgorithmSecondaryFamilyCustom

- **UUID**: `b5789bb6-3ac9-4a16-b1c6-b4ac5a5a965f`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobRandomSeedAlgorithmMode

- **UUID**: `1d1775eb-1efd-44a2-897c-8d3d5eea1859`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 2. CsmJobRandomSeedAlgorithmSecondaryFamily

- **UUID**: `566fb76a-36f8-4ff6-95ea-e72dc0f7f820`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

############ 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `bf0df573-32e6-49de-8cca-db8d277a3af2`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

####### 32. CsmJobRandomSeedConfig

**容器属性**:

- **UUID**: `d8a2b8d8-f086-47b4-93a7-8b14fdb26ab1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeedConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random seed operation. The container name serves as a symbolic name for the identifier of a random seed configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### STRING 类型参数

########## 1. CsmJobRandomSeedAlgorithmFamilyCustom

- **UUID**: `bffe13c5-ebf9-4036-9779-19656e3cea60`
- **参数名**: `CsmJobRandomSeedAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobRandomSeedAlgorithmModeCustom

- **UUID**: `dc676f46-ce44-4f5c-a7ba-db0387523cbc`
- **参数名**: `CsmJobRandomSeedAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 3. CsmJobRandomSeedAlgorithmSecondaryFamilyCustom

- **UUID**: `b5789bb6-3ac9-4a16-b1c6-b4ac5a5a965f`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobRandomSeedAlgorithmMode

- **UUID**: `1d1775eb-1efd-44a2-897c-8d3d5eea1859`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 2. CsmJobRandomSeedAlgorithmSecondaryFamily

- **UUID**: `566fb76a-36f8-4ff6-95ea-e72dc0f7f820`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `bf0df573-32e6-49de-8cca-db8d277a3af2`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

####### 33. CsmJobKeyGenerate

**容器属性**:

- **UUID**: `39234e8f-11d2-47fe-a004-8cf3cfdf3a80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeyGenerateConfig

**容器属性**:

- **UUID**: `d6eb3dda-2dbb-4134-83ff-a2a860f0c3ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key generate operation. The container name serves as a symbolic name for the identifier of a key generate configuration.

########## 参数配置

此容器包含 **7** 个参数：

########### STRING 类型参数

############ 1. CsmJobKeyGenerateAlgorithmModeCustom

- **UUID**: `2f147e45-8821-45d9-b6ce-d303bf78f9a4`
- **参数名**: `CsmJobKeyGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

############ 2. CsmJobKeyGenerateAlgorithmFamilyCustom

- **UUID**: `53674cb8-88db-464b-a63c-53855148c553`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 3. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `1272d3b2-2b0e-489f-9f59-9c5b56ff2060`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobKeyGenerateAlgorithmFamiliy

- **UUID**: `97222373-b47d-412a-8014-f378fd38dd60`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `b8140a6c-5f24-463a-a3fc-bbca1143290f`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `d4c0fc39-08df-46f6-89e8-5447c4326572`
- **参数名**: `CsmJobKeyGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmJobKeyGenerateAlgorithmSecondaryFamily

- **UUID**: `e9efd092-be94-4c48-a1d8-33d4e8e00b60`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 34. CsmJobKeyGenerateConfig

**容器属性**:

- **UUID**: `d6eb3dda-2dbb-4134-83ff-a2a860f0c3ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key generate operation. The container name serves as a symbolic name for the identifier of a key generate configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyGenerateAlgorithmModeCustom

- **UUID**: `2f147e45-8821-45d9-b6ce-d303bf78f9a4`
- **参数名**: `CsmJobKeyGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

########## 2. CsmJobKeyGenerateAlgorithmFamilyCustom

- **UUID**: `53674cb8-88db-464b-a63c-53855148c553`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 3. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `1272d3b2-2b0e-489f-9f59-9c5b56ff2060`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyGenerateAlgorithmFamiliy

- **UUID**: `97222373-b47d-412a-8014-f378fd38dd60`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `b8140a6c-5f24-463a-a3fc-bbca1143290f`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `d4c0fc39-08df-46f6-89e8-5447c4326572`
- **参数名**: `CsmJobKeyGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyGenerateAlgorithmSecondaryFamily

- **UUID**: `e9efd092-be94-4c48-a1d8-33d4e8e00b60`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 35. CsmJobCertificateParse

**容器属性**:

- **UUID**: `00081a11-438d-4d59-8f81-f3c8df28c18c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParse`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of CertificateParse primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobCertificateParseConfig

**容器属性**:

- **UUID**: `8305d7f7-c8e7-4f03-9f0d-7a27306e5d91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParseConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateParse. The container name serves as a symbolic name for the identifier of a key configuration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. CsmJobCertificateParseDataMaxLength

- **UUID**: `38b53552-8b36-459c-9522-e356b137557e`
- **参数名**: `CsmJobCertificateParseDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########### STRING 类型参数

############ 1. CsmJobCertificateParseAlgorithmFamilyCustom

- **UUID**: `46608e1c-9258-4b2a-9c7f-49c6e49131f4`
- **参数名**: `CsmJobCertificateParseAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

############ 2. CsmJobCertificateParseAlgorithmModeCustom

- **UUID**: `83b39cc7-11dd-4b7b-ae34-21fc09397d32`
- **参数名**: `CsmJobCertificateParseAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

############ 3. CsmJobCertificateParseAlgorithmSecondaryFamilyCustom

- **UUID**: `a134720a-976d-4c39-b209-9973c28af5aa`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobCertificateParseAlgorithmMode

- **UUID**: `b128956c-1e57-4ccd-9fde-5a9402b644a9`
- **参数名**: `CsmJobCertificateParseAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 2. CsmJobCertificateParseAlgorithmSecondaryFamily

- **UUID**: `d125abf0-d21f-433f-9f49-a2ab60a162d8`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 36. CsmJobCertificateParseConfig

**容器属性**:

- **UUID**: `8305d7f7-c8e7-4f03-9f0d-7a27306e5d91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParseConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateParse. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobCertificateParseDataMaxLength

- **UUID**: `38b53552-8b36-459c-9522-e356b137557e`
- **参数名**: `CsmJobCertificateParseDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######### STRING 类型参数

########## 1. CsmJobCertificateParseAlgorithmFamilyCustom

- **UUID**: `46608e1c-9258-4b2a-9c7f-49c6e49131f4`
- **参数名**: `CsmJobCertificateParseAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobCertificateParseAlgorithmModeCustom

- **UUID**: `83b39cc7-11dd-4b7b-ae34-21fc09397d32`
- **参数名**: `CsmJobCertificateParseAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobCertificateParseAlgorithmSecondaryFamilyCustom

- **UUID**: `a134720a-976d-4c39-b209-9973c28af5aa`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobCertificateParseAlgorithmMode

- **UUID**: `b128956c-1e57-4ccd-9fde-5a9402b644a9`
- **参数名**: `CsmJobCertificateParseAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 2. CsmJobCertificateParseAlgorithmSecondaryFamily

- **UUID**: `d125abf0-d21f-433f-9f49-a2ab60a162d8`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 37. CsmJobCertificateVerify

**容器属性**:

- **UUID**: `e19f001a-6b1d-4ebb-8ad6-7c3965c5347c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of CertificateVerify primitves

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobCertificateVerifyConfig

**容器属性**:

- **UUID**: `40a122f0-fa36-43ac-b6b5-c2792be71852`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateVerify. The container name serves as a symbolic name for the identifier of a key configuration.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. CsmJobCertificateVerifyDataMaxLength

- **UUID**: `64cfd2e1-3153-479a-bc35-ab8208b5f625`
- **参数名**: `CsmJobCertificateVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########### STRING 类型参数

############ 1. CsmJobCertificateVerifyAlgorithmFamilyCustom

- **UUID**: `17327682-7639-46b9-9b36-226d28c86ee6`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

############ 2. CsmJobCertificateVerifyAlgorithmModeCustom

- **UUID**: `e5864b7c-f3ec-4b23-91b2-36474f4012e3`
- **参数名**: `CsmJobCertificateVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

############ 3. CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ffe2c517-b33d-4709-8234-78e06dec4261`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########### ENUMERATION 类型参数

############ 1. CsmJobCertificateVerifyAlgorithmFamiliy

- **UUID**: `7ddc57e7-4d4d-43cd-a5af-f6b8d7ef052c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

####### 38. CsmJobCertificateVerifyConfig

**容器属性**:

- **UUID**: `40a122f0-fa36-43ac-b6b5-c2792be71852`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateVerify. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobCertificateVerifyDataMaxLength

- **UUID**: `64cfd2e1-3153-479a-bc35-ab8208b5f625`
- **参数名**: `CsmJobCertificateVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######### STRING 类型参数

########## 1. CsmJobCertificateVerifyAlgorithmFamilyCustom

- **UUID**: `17327682-7639-46b9-9b36-226d28c86ee6`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobCertificateVerifyAlgorithmModeCustom

- **UUID**: `e5864b7c-f3ec-4b23-91b2-36474f4012e3`
- **参数名**: `CsmJobCertificateVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ffe2c517-b33d-4709-8234-78e06dec4261`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobCertificateVerifyAlgorithmFamiliy

- **UUID**: `7ddc57e7-4d4d-43cd-a5af-f6b8d7ef052c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 10. CsmAEADDecrypt

**容器属性**:

- **UUID**: `d735c9b4-5191-4bd0-9e22-95d135a5f8bc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration of AEAD decryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `16c65ae5-43de-4174-a48f-4ab5956b8cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `1a375493-ae95-4425-8b6b-a342672efe0e`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD decryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `131fa2cb-7ecf-4d51-80ca-79b98bc1e39f`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `56ebf065-e00d-4601-b69a-c90433f31988`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext in bytes

########## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `9ddf7bec-61c1-40ea-b19d-4ba731d99f3a`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output plaintext length in bytes

########## 5. CsmAEADDecryptTagLength

- **UUID**: `8e257428-879e-477c-a103-aab2faa944e0`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input Tag length in BITS

######### STRING 类型参数

########## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `a87f8f86-eebf-444d-acb5-cae57d1710e5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

########## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `241cecfa-d109-4faf-be60-c1dd46bdb214`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `f04e5c20-2a65-47dd-b1c9-496192e5b440`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `d11fcb27-97f7-4a1f-b9d6-2d9a16b5dc47`
- **参数名**: `CsmAEADDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `d60f7329-32e8-4664-a6a7-dba74b6b0ed9`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmAEADDecryptProcessing

- **UUID**: `40356098-006c-48dd-8158-24bd2058a580`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmAEADDecryptSwcInterfaceVersion

- **UUID**: `2cb71cb2-be50-4758-9b1d-de819297646b`
- **参数名**: `CsmAEADDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADDecrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADDecryptKeyRef

- **UUID**: `4d6b66b0-38c0-453c-94e7-f127ebf34c54`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that decryption primitive.

########## 2. CsmAEADDecryptQueueRef

- **UUID**: `be0a5c60-555f-4d2f-88bd-959bcf2a484c`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that decryption primitive.

##### 11. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `16c65ae5-43de-4174-a48f-4ab5956b8cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `1a375493-ae95-4425-8b6b-a342672efe0e`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD decryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `131fa2cb-7ecf-4d51-80ca-79b98bc1e39f`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

######## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `56ebf065-e00d-4601-b69a-c90433f31988`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext in bytes

######## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `9ddf7bec-61c1-40ea-b19d-4ba731d99f3a`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output plaintext length in bytes

######## 5. CsmAEADDecryptTagLength

- **UUID**: `8e257428-879e-477c-a103-aab2faa944e0`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input Tag length in BITS

####### STRING 类型参数

######## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `a87f8f86-eebf-444d-acb5-cae57d1710e5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

######## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `241cecfa-d109-4faf-be60-c1dd46bdb214`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `f04e5c20-2a65-47dd-b1c9-496192e5b440`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `d11fcb27-97f7-4a1f-b9d6-2d9a16b5dc47`
- **参数名**: `CsmAEADDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `d60f7329-32e8-4664-a6a7-dba74b6b0ed9`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmAEADDecryptProcessing

- **UUID**: `40356098-006c-48dd-8158-24bd2058a580`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 5. CsmAEADDecryptSwcInterfaceVersion

- **UUID**: `2cb71cb2-be50-4758-9b1d-de819297646b`
- **参数名**: `CsmAEADDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADDecrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CsmAEADDecryptKeyRef

- **UUID**: `4d6b66b0-38c0-453c-94e7-f127ebf34c54`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that decryption primitive.

######## 2. CsmAEADDecryptQueueRef

- **UUID**: `be0a5c60-555f-4d2f-88bd-959bcf2a484c`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that decryption primitive.

##### 12. CsmAEADEncrypt

**容器属性**:

- **UUID**: `e7936f4e-bb99-4d9e-8aee-47dec52a6980`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration of AEAD encryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `54b685a3-6832-4bf2-9563-eec537185b81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `fb4eb104-97f9-4d53-ba5c-2765d320dda6`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD encryption key. 
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `8a1ce7e6-8e61-41a1-afa3-5c79304cad26`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `bdd2a300-d67f-41ae-8082-da127b4eae97`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output ciphertext length in bytes

########## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `d9061c72-2361-4ee0-8253-cb8eea63742d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

########## 5. CsmAEADEncryptTagLength

- **UUID**: `8217dc92-f473-4931-88eb-ce1e2375345e`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output Tag length in bytes

######### STRING 类型参数

########## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `ff509353-8812-4f4a-b7f6-43afadd0f0a6`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

########## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `a176d168-1857-4312-846b-9ab8787e0f8b`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `e62e6830-3cde-4ac8-956c-19896fd94b82`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `4974fb0a-4e0b-4ff5-9c7b-c9fa5bdc3522`
- **参数名**: `CsmAEADEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c91e9329-6c87-4c92-8a2e-e60bd76b0362`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmAEADEncryptProcessing

- **UUID**: `6faf775c-33f9-4896-a687-54d2f0caf4dc`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmAEADEncryptSwcInterfaceVersion

- **UUID**: `1fbe048c-9241-434f-a667-2bf715865234`
- **参数名**: `CsmAEADEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Encrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADEncryptKeyRef

- **UUID**: `c13bfd9d-cb0a-4a57-b828-a42e20d40d10`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that encryption primitive.

########## 2. CsmAEADEncryptQueueRef

- **UUID**: `f545978a-e55c-4de2-b878-b6577bc63eb2`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that encryption primitive.

##### 13. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `54b685a3-6832-4bf2-9563-eec537185b81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `fb4eb104-97f9-4d53-ba5c-2765d320dda6`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the AEAD encryption key. 
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `8a1ce7e6-8e61-41a1-afa3-5c79304cad26`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input associated data length in bytes

######## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `bdd2a300-d67f-41ae-8082-da127b4eae97`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output ciphertext length in bytes

######## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `d9061c72-2361-4ee0-8253-cb8eea63742d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

######## 5. CsmAEADEncryptTagLength

- **UUID**: `8217dc92-f473-4931-88eb-ce1e2375345e`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output Tag length in bytes

####### STRING 类型参数

######## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `ff509353-8812-4f4a-b7f6-43afadd0f0a6`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

######## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `a176d168-1857-4312-846b-9ab8787e0f8b`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `e62e6830-3cde-4ac8-956c-19896fd94b82`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `4974fb0a-4e0b-4ff5-9c7b-c9fa5bdc3522`
- **参数名**: `CsmAEADEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c91e9329-6c87-4c92-8a2e-e60bd76b0362`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmAEADEncryptProcessing

- **UUID**: `6faf775c-33f9-4896-a687-54d2f0caf4dc`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 5. CsmAEADEncryptSwcInterfaceVersion

- **UUID**: `1fbe048c-9241-434f-a667-2bf715865234`
- **参数名**: `CsmAEADEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Encrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CsmAEADEncryptKeyRef

- **UUID**: `c13bfd9d-cb0a-4a57-b828-a42e20d40d10`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used for that encryption primitive.

######## 2. CsmAEADEncryptQueueRef

- **UUID**: `f545978a-e55c-4de2-b878-b6577bc63eb2`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that encryption primitive.

##### 14. CsmDecrypt

**容器属性**:

- **UUID**: `3142a8d1-ace8-4b5e-b6f8-667ac803e0ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of Decryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmDecryptConfig

**容器属性**:

- **UUID**: `2ae2e6d4-c7af-4152-b0c1-aeefa146c6ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `9a39cc5b-729a-4928-84a6-633485a41f07`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmDecryptDataMaxLength

- **UUID**: `7283c433-24f9-4fe0-80d5-e5295282bde2`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext length in bytes

########## 3. CsmDecryptResultMaxLength

- **UUID**: `9f54d592-38e2-4c07-b93c-e4933a71ac42`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output plaintext length in bytes

######### STRING 类型参数

########## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `bd69c14c-5a37-44a0-a0ff-643272e145c2`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

########## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `6ebaefc8-18b9-4b58-af48-3ac48cdb0009`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `fffb4375-774e-4aa6-a06b-f93c1d07d58b`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `88e56366-b730-43b9-b746-53572abab161`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmFamily

- **UUID**: `1c98b7e1-1a0b-42d3-876c-eb54087630e8`
- **参数名**: `CsmDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmDecryptAlgorithmMode

- **UUID**: `51f3901a-1309-4d83-bc21-60e882dc4ec1`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `c9e2923d-fd05-4ce1-8dac-fca49691429a`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 5. CsmDecryptProcessing

- **UUID**: `76b71b58-ebea-4dc8-8e8e-e88b19672af6`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmDecryptSwcInterfaceVersion

- **UUID**: `68c5f9dc-0e59-4fc8-a302-10a91ef97517`
- **参数名**: `CsmDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Decrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 15. CsmDecryptConfig

**容器属性**:

- **UUID**: `2ae2e6d4-c7af-4152-b0c1-aeefa146c6ea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `9a39cc5b-729a-4928-84a6-633485a41f07`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######## 2. CsmDecryptDataMaxLength

- **UUID**: `7283c433-24f9-4fe0-80d5-e5295282bde2`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input ciphertext length in bytes

######## 3. CsmDecryptResultMaxLength

- **UUID**: `9f54d592-38e2-4c07-b93c-e4933a71ac42`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output plaintext length in bytes

####### STRING 类型参数

######## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `bd69c14c-5a37-44a0-a0ff-643272e145c2`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

######## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `6ebaefc8-18b9-4b58-af48-3ac48cdb0009`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `fffb4375-774e-4aa6-a06b-f93c1d07d58b`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `88e56366-b730-43b9-b746-53572abab161`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmDecryptAlgorithmFamily

- **UUID**: `1c98b7e1-1a0b-42d3-876c-eb54087630e8`
- **参数名**: `CsmDecryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmDecryptAlgorithmMode

- **UUID**: `51f3901a-1309-4d83-bc21-60e882dc4ec1`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `c9e2923d-fd05-4ce1-8dac-fca49691429a`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 5. CsmDecryptProcessing

- **UUID**: `76b71b58-ebea-4dc8-8e8e-e88b19672af6`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmDecryptSwcInterfaceVersion

- **UUID**: `68c5f9dc-0e59-4fc8-a302-10a91ef97517`
- **参数名**: `CsmDecryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
Decrypt:		CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 16. CsmEncrypt

**容器属性**:

- **UUID**: `85c74ce5-750b-4c1b-8773-d8e6d98d6cd3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncrypt`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of Encryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmEncryptConfig

**容器属性**:

- **UUID**: `e76a2714-5720-4560-93ed-4e955de2c30d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmEncryptDataMaxLength

- **UUID**: `9b814c0a-ace5-4277-bcef-e8f5bb2080c3`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

########## 2. CsmEncryptResultMaxLength

- **UUID**: `cc22b951-be04-4e12-90e0-11ad5414678c`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output cipher length in bytes

########## 3. CsmEncryptAlgorithmKeyLength

- **UUID**: `c827e260-516b-4f43-af56-6551b4cb7b55`
- **参数名**: `CsmEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `8f551a9c-bced-433f-98c9-fdc4419f60ef`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

########## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `0e06ee40-f2a8-4bdd-9457-63811c02d212`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `e738fda2-8cea-4556-8845-77efd342d8e2`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `7efe5788-c82e-46bf-a4b3-51a410dd6561`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmFamily

- **UUID**: `106cf0bf-54b7-4eed-a6be-d8baf03d1c0d`
- **参数名**: `CsmEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmEncryptAlgorithmMode

- **UUID**: `12940fb2-2a5c-4b07-b8cd-c9648f7de946`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `5d4934ca-4bbe-4f79-bb2a-84ec1a8373a1`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmEncryptProcessing

- **UUID**: `353f410c-be0b-40bc-8004-7afef00b6950`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmEncryptSwcInterfaceVersion

- **UUID**: `dda01b88-4a62-490c-9e70-8b9e8d22bf93`
- **参数名**: `CsmEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADEncrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 17. CsmEncryptConfig

**容器属性**:

- **UUID**: `e76a2714-5720-4560-93ed-4e955de2c30d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmEncryptDataMaxLength

- **UUID**: `9b814c0a-ace5-4277-bcef-e8f5bb2080c3`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input plaintext length in bytes

######## 2. CsmEncryptResultMaxLength

- **UUID**: `cc22b951-be04-4e12-90e0-11ad5414678c`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the output cipher length in bytes

######## 3. CsmEncryptAlgorithmKeyLength

- **UUID**: `c827e260-516b-4f43-af56-6551b4cb7b55`
- **参数名**: `CsmEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the encryption key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

####### STRING 类型参数

######## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `8f551a9c-bced-433f-98c9-fdc4419f60ef`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

######## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `0e06ee40-f2a8-4bdd-9457-63811c02d212`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `e738fda2-8cea-4556-8845-77efd342d8e2`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `7efe5788-c82e-46bf-a4b3-51a410dd6561`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECIES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmEncryptAlgorithmFamily

- **UUID**: `106cf0bf-54b7-4eed-a6be-d8baf03d1c0d`
- **参数名**: `CsmEncryptAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmEncryptAlgorithmMode

- **UUID**: `12940fb2-2a5c-4b07-b8cd-c9648f7de946`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_12ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_20ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_8ROUNDS` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CBC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTR` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_ECB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_OFB` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_OAEP` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSAES_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_XTS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `5d4934ca-4bbe-4f79-bb2a-84ec1a8373a1`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

######## 5. CsmEncryptProcessing

- **UUID**: `353f410c-be0b-40bc-8004-7afef00b6950`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmEncryptSwcInterfaceVersion

- **UUID**: `dda01b88-4a62-490c-9e70-8b9e8d22bf93`
- **参数名**: `CsmEncryptSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
AEADEncrypt:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 18. CsmHash

**容器属性**:

- **UUID**: `3351d4ea-8498-4215-b0f2-faec50099c63`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHash`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for Hash Configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmHashConfig

**容器属性**:

- **UUID**: `5ff1390d-0b6f-4982-8411-1fb9f766a00c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. CsmHashDataMaxLength

- **UUID**: `bcb708d8-5908-4839-b6b8-284b1e70b27e`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########## 2. CsmHashResultLength

- **UUID**: `78a5b9e2-5899-40c6-aa61-99c764ea7d28`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output hash length in bytes

######### STRING 类型参数

########## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `1dfe4aab-ec07-417c-af6e-b28dd3e08978`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

########## 2. CsmHashAlgorithmModeCustom

- **UUID**: `ce7eee6e-f2b2-4a7e-af1f-a53ed6c28b41`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `c4924324-32c5-4e14-ba8d-277f011e1c55`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmHashAlgorithmFamiliy

- **UUID**: `40be8690-0416-47e8-84c1-4d2a88a8b840`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmFamily

- **UUID**: `46dd10e9-0400-47a6-93df-e1ab429d97b0`
- **参数名**: `CsmHashAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmHashAlgorithmMode

- **UUID**: `303f6a0d-de7b-4177-a2b7-e227f4a560c7`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmHashAlgorithmSecondaryFamily

- **UUID**: `16e9468d-057b-48fe-90bf-a1f77116912f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmHashProcessing

- **UUID**: `5043a314-1ac4-4756-950a-1a8f81e21d4a`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmHashSwcInterfaceVersion

- **UUID**: `62c5e599-d6d5-4c34-94b7-7701ed0e7f1d`
- **参数名**: `CsmHashSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
CancelJob: 	CSM_E_JOB_CANCELED

##### 19. CsmHashConfig

**容器属性**:

- **UUID**: `5ff1390d-0b6f-4982-8411-1fb9f766a00c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. CsmHashDataMaxLength

- **UUID**: `bcb708d8-5908-4839-b6b8-284b1e70b27e`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######## 2. CsmHashResultLength

- **UUID**: `78a5b9e2-5899-40c6-aa61-99c764ea7d28`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output hash length in bytes

####### STRING 类型参数

######## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `1dfe4aab-ec07-417c-af6e-b28dd3e08978`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

######## 2. CsmHashAlgorithmModeCustom

- **UUID**: `ce7eee6e-f2b2-4a7e-af1f-a53ed6c28b41`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

######## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `c4924324-32c5-4e14-ba8d-277f011e1c55`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmHashAlgorithmFamiliy

- **UUID**: `40be8690-0416-47e8-84c1-4d2a88a8b840`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmHashAlgorithmFamily

- **UUID**: `46dd10e9-0400-47a6-93df-e1ab429d97b0`
- **参数名**: `CsmHashAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmHashAlgorithmMode

- **UUID**: `303f6a0d-de7b-4177-a2b7-e227f4a560c7`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmHashAlgorithmSecondaryFamily

- **UUID**: `16e9468d-057b-48fe-90bf-a1f77116912f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

######## 5. CsmHashProcessing

- **UUID**: `5043a314-1ac4-4756-950a-1a8f81e21d4a`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmHashSwcInterfaceVersion

- **UUID**: `62c5e599-d6d5-4c34-94b7-7701ed0e7f1d`
- **参数名**: `CsmHashSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
CancelJob: 	CSM_E_JOB_CANCELED

##### 20. CsmMacGenerate

**容器属性**:

- **UUID**: `5689caab-3a47-4e1f-abec-e67486d5d270`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of MacGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `7ba6c34e-58b4-40d4-86f6-ae9f10fa275d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `590ebb0b-bf74-4b1d-a0f5-b4c275140d97`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 2. CsmMacGenerateDataMaxLength

- **UUID**: `fd1ef23f-ad64-4d11-9212-303ad907c894`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

########## 3. CsmMacGenerateResultLength

- **UUID**: `f4a8c073-d9b3-4a1d-8408-dce31f4d359e`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output MAC length in bytes

######### STRING 类型参数

########## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `1de2c6ef-33f7-484c-9497-311fef6cf93f`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family,

########## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `594894f7-3af5-41a8-b5ae-39bcd9ba71a4`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `88e91b76-faa9-47c0-9b05-aabe458e4f93`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

######### ENUMERATION 类型参数

########## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `8150635e-893f-45b5-ba70-e46c07d3f7ca`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `3cd160db-ec74-4c1c-a038-c6bcbfb749e6`
- **参数名**: `CsmMacGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `b20b076b-c935-4ebf-9c43-e67708061c97`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `33158cac-def0-464a-a065-8809b45a08e5`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 5. CsmMacGenerateProcessing

- **UUID**: `ccd17e6f-db6e-47cb-bfd7-9d7931acdb10`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmMacGenerateSwcInterfaceVersion

- **UUID**: `e5ea84ff-eec6-4c95-928d-1b01a6fcebce`
- **参数名**: `CsmMacGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacGenerate:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 21. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `7ba6c34e-58b4-40d4-86f6-ae9f10fa275d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `590ebb0b-bf74-4b1d-a0f5-b4c275140d97`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######## 2. CsmMacGenerateDataMaxLength

- **UUID**: `fd1ef23f-ad64-4d11-9212-303ad907c894`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######## 3. CsmMacGenerateResultLength

- **UUID**: `f4a8c073-d9b3-4a1d-8408-dce31f4d359e`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output MAC length in bytes

####### STRING 类型参数

######## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `1de2c6ef-33f7-484c-9497-311fef6cf93f`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family,

######## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `594894f7-3af5-41a8-b5ae-39bcd9ba71a4`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `88e91b76-faa9-47c0-9b05-aabe458e4f93`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

####### ENUMERATION 类型参数

######## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `8150635e-893f-45b5-ba70-e46c07d3f7ca`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `3cd160db-ec74-4c1c-a038-c6bcbfb749e6`
- **参数名**: `CsmMacGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `b20b076b-c935-4ebf-9c43-e67708061c97`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `33158cac-def0-464a-a065-8809b45a08e5`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 5. CsmMacGenerateProcessing

- **UUID**: `ccd17e6f-db6e-47cb-bfd7-9d7931acdb10`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmMacGenerateSwcInterfaceVersion

- **UUID**: `e5ea84ff-eec6-4c95-928d-1b01a6fcebce`
- **参数名**: `CsmMacGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacGenerate:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 22. CsmMacVerify

**容器属性**:

- **UUID**: `0fb8fdb0-acbd-41c1-8075-dc6823e67967`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of MacVerify primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `66b6a9f8-f77b-400b-8a23-a8ace40a7407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacVerifyCompareLength

- **UUID**: `9a257862-800a-4742-a8f4-9cc855f4905b`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input MAC length, that shall be verified, in BITS

########## 2. CsmMacVerifyDataMaxLength

- **UUID**: `64861c81-aee1-4ed7-8d77-ba208097628c`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length, for which MAC shall be verified, in bytes

########## 3. CsmMacVerifyAlgorithmKeyLength

- **UUID**: `56ef7bb5-ab53-4834-93f0-503621405261`
- **参数名**: `CsmMacVerifyAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `92314156-249e-44e7-9850-3a057508a969`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `22d21fa5-fc9f-461b-b0d4-0380bbf7c5e1`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

########## 3. CsmMacVerifyAlgorithmModeCustom

- **UUID**: `b336d831-ce60-483e-8524-605f32e14298`
- **参数名**: `CsmMacVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

######### ENUMERATION 类型参数

########## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `c9caa2c2-cb89-4785-bc64-f4a3f052c5aa`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `d8789fbe-192f-4655-8084-98495d873a73`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `f770d9cf-44da-409d-ad7c-94b9c666a9ed`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmMacVerifyProcessing

- **UUID**: `abdc3e40-3d83-4e6e-8a6a-9bbbf2ade8ba`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 5. CsmMacVerifyAlgorithmMode

- **UUID**: `fb6e75e9-c8ad-4304-914b-76929329f588`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service.

########## 6. CsmMacVerifySwcInterfaceVersion

- **UUID**: `d48a2a24-274e-46ae-9ca1-4e4b93fb2d8a`
- **参数名**: `CsmMacVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 23. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `66b6a9f8-f77b-400b-8a23-a8ace40a7407`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacVerifyCompareLength

- **UUID**: `9a257862-800a-4742-a8f4-9cc855f4905b`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input MAC length, that shall be verified, in BITS

######## 2. CsmMacVerifyDataMaxLength

- **UUID**: `64861c81-aee1-4ed7-8d77-ba208097628c`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length, for which MAC shall be verified, in bytes

######## 3. CsmMacVerifyAlgorithmKeyLength

- **UUID**: `56ef7bb5-ab53-4834-93f0-503621405261`
- **参数名**: `CsmMacVerifyAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the MAC key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

####### STRING 类型参数

######## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `92314156-249e-44e7-9850-3a057508a969`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service

######## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `22d21fa5-fc9f-461b-b0d4-0380bbf7c5e1`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

######## 3. CsmMacVerifyAlgorithmModeCustom

- **UUID**: `b336d831-ce60-483e-8524-605f32e14298`
- **参数名**: `CsmMacVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

####### ENUMERATION 类型参数

######## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `c9caa2c2-cb89-4785-bc64-f4a3f052c5aa`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `d8789fbe-192f-4655-8084-98495d873a73`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `f770d9cf-44da-409d-ad7c-94b9c666a9ed`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 4. CsmMacVerifyProcessing

- **UUID**: `abdc3e40-3d83-4e6e-8a6a-9bbbf2ade8ba`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 5. CsmMacVerifyAlgorithmMode

- **UUID**: `fb6e75e9-c8ad-4304-914b-76929329f588`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service.

######## 6. CsmMacVerifySwcInterfaceVersion

- **UUID**: `d48a2a24-274e-46ae-9ca1-4e4b93fb2d8a`
- **参数名**: `CsmMacVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
MacVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 24. CsmRandomGenerate

**容器属性**:

- **UUID**: `2c2523be-f7d5-456d-bd14-3e890d2b2bc8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of RandomGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `5729fbf0-2ba4-4d84-b9b8-a87c57a86115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmRandomGenerateResultLength

- **UUID**: `02bde8ad-ea44-4565-b540-da57744cdd52`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the random generate key in bytes

######### STRING 类型参数

########## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `5e9f3c5f-88e2-4c48-bb64-a219725f3094`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

########## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `0786f734-73c8-4207-84d6-755086325eda`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

########## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `d72d056c-c840-464e-9171-186e25f1313d`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `65f30f84-9ed7-45a4-95e6-1034fcc13342`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `6d5b7b2d-2137-453c-853d-7f2ae2ccfa34`
- **参数名**: `CsmRandomGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f4ef354d-df08-41c2-8d42-80029955fb0b`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `5c94efa0-646e-40e7-9e4f-3d3c917c6028`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

########## 5. CsmRandomGenerateProcessing

- **UUID**: `f2551403-d13a-4c3d-833b-bd8e298d093e`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

##### 25. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `5729fbf0-2ba4-4d84-b9b8-a87c57a86115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CsmRandomGenerateResultLength

- **UUID**: `02bde8ad-ea44-4565-b540-da57744cdd52`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the random generate key in bytes

####### STRING 类型参数

######## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `5e9f3c5f-88e2-4c48-bb64-a219725f3094`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

######## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `0786f734-73c8-4207-84d6-755086325eda`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

######## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `d72d056c-c840-464e-9171-186e25f1313d`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `65f30f84-9ed7-45a4-95e6-1034fcc13342`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_AES` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RNG` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA1` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `6d5b7b2d-2137-453c-853d-7f2ae2ccfa34`
- **参数名**: `CsmRandomGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f4ef354d-df08-41c2-8d42-80029955fb0b`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `5c94efa0-646e-40e7-9e4f-3d3c917c6028`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service

######## 5. CsmRandomGenerateProcessing

- **UUID**: `f2551403-d13a-4c3d-833b-bd8e298d093e`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

##### 26. CsmSecureCounter

**容器属性**:

- **UUID**: `cdabafe4-0b67-40e1-bef0-19206cfa15e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounter`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SecureCounter primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `95cde3f3-6e48-4dba-a938-f51be4b8a8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmSecureCounterProcessing

- **UUID**: `2be95d73-e5ed-4a3b-941e-b463234083eb`
- **参数名**: `CsmSecureCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_SYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS`
  - `CSM_SYNCHRONOUS`
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CsmSecureCounterQueueRef

- **UUID**: `2da71ed8-ae40-4ca7-b488-da34778d7efc`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that secure counter.

##### 27. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `95cde3f3-6e48-4dba-a938-f51be4b8a8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. CsmSecureCounterProcessing

- **UUID**: `2be95d73-e5ed-4a3b-941e-b463234083eb`
- **参数名**: `CsmSecureCounterProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_SYNCHRONOUS`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS`
  - `CSM_SYNCHRONOUS`
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CsmSecureCounterQueueRef

- **UUID**: `2da71ed8-ae40-4ca7-b488-da34778d7efc`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Not used. Queue is referred in Job.
This parameter refers to the queue used for that secure counter.

##### 28. CsmSignatureGenerate

**容器属性**:

- **UUID**: `28a93b87-e9d7-497e-9f52-ce15e06cf9f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SignatureGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `ec921f3e-c770-4020-8b3b-08d5b3c22c59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `01208c6b-02d1-4d0d-a463-593aa9f12e81`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length in bytes

########## 2. CsmSignatureGenerateKeyLength

- **UUID**: `28ad616e-0a1a-4585-bfab-8a125fdd1314`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature generate key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

########## 3. CsmSignatureGenerateResultLength

- **UUID**: `b065f2f1-9299-4539-b5e7-4383ade6da2c`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output signature length in bytes

######### STRING 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `b754a5c1-c09f-410e-b828-3f9efeeebb91`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `ace204e5-2409-41b3-a3a4-9ea39ee9500e`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f57c8137-e31a-4162-80d0-4cea6105a303`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `07e9c943-419c-48a5-a740-0d9c127a71d6`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `bd8a72ad-e365-4046-a007-d3360338e326`
- **参数名**: `CsmSignatureGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `7e3cbb74-9cbe-4198-ae9b-a333d932ee9a`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `94efbcdb-91b9-44f2-ade8-25e4752311ac`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 5. CsmSignatureGenerateProcessing

- **UUID**: `ca5a333c-29c9-4023-b788-897958ae0837`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmSignatureGenerateSwcInterfaceVersion

- **UUID**: `5fca0b76-bea9-45c8-a2bc-89cf19bc4973`
- **参数名**: `CsmSignatureGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 29. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `ec921f3e-c770-4020-8b3b-08d5b3c22c59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `01208c6b-02d1-4d0d-a463-593aa9f12e81`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length in bytes

######## 2. CsmSignatureGenerateKeyLength

- **UUID**: `28ad616e-0a1a-4585-bfab-8a125fdd1314`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature generate key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######## 3. CsmSignatureGenerateResultLength

- **UUID**: `b065f2f1-9299-4539-b5e7-4383ade6da2c`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the output signature length in bytes

####### STRING 类型参数

######## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `b754a5c1-c09f-410e-b828-3f9efeeebb91`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `ace204e5-2409-41b3-a3a4-9ea39ee9500e`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f57c8137-e31a-4162-80d0-4cea6105a303`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `07e9c943-419c-48a5-a740-0d9c127a71d6`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `bd8a72ad-e365-4046-a007-d3360338e326`
- **参数名**: `CsmSignatureGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `7e3cbb74-9cbe-4198-ae9b-a333d932ee9a`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `94efbcdb-91b9-44f2-ade8-25e4752311ac`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 5. CsmSignatureGenerateProcessing

- **UUID**: `ca5a333c-29c9-4023-b788-897958ae0837`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmSignatureGenerateSwcInterfaceVersion

- **UUID**: `5fca0b76-bea9-45c8-a2bc-89cf19bc4973`
- **参数名**: `CsmSignatureGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 30. CsmSignatureVerify

**容器属性**:

- **UUID**: `c5d57db1-7d62-43f2-8331-8cba257184e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of SignatureVerify primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6762b960-93af-48bb-bfdc-7e7f2d5bfb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureVerifyCompareLength

- **UUID**: `b13fff76-aa93-4fa4-9118-da905815eaf0`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

########## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `3ad0c1d5-eaad-40d5-8433-ac9209c79c77`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

########## 3. CsmSignatureVerifyKeyLength

- **UUID**: `447dba54-7daf-4820-91fd-c6c2c675f4c0`
- **参数名**: `CsmSignatureVerifyKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature verify key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

######### STRING 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `7a3383da-ef67-4f83-907c-53b9bf9b21a1`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `77d20415-becd-4d5e-a574-d56e52e8652d`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `002eb5ee-ac8a-4b48-b188-8d5946776c12`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `bd7c744b-b792-4fde-883e-251afe07124f`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `71c1a792-dc01-46ee-81d7-acc47a4ed31a`
- **参数名**: `CsmSignatureVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `580d0c6b-145d-4b80-9105-7a851aa09293`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `e43b33d0-92b8-4425-b9a2-74fdf2e9a5ae`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 5. CsmSignatureVerifyProcessing

- **UUID**: `778f1b69-78fd-4321-b1bf-eadb9eecb250`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

########## 6. CsmSignatureVerifySwcInterfaceVersion

- **UUID**: `14fdc583-e086-4028-a223-717684e9e1bd`
- **参数名**: `CsmSignatureVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 31. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6762b960-93af-48bb-bfdc-7e7f2d5bfb6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureVerifyCompareLength

- **UUID**: `b13fff76-aa93-4fa4-9118-da905815eaf0`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

######## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `3ad0c1d5-eaad-40d5-8433-ac9209c79c77`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the input data length, for which signature shall be verified, in bytes

######## 3. CsmSignatureVerifyKeyLength

- **UUID**: `447dba54-7daf-4820-91fd-c6c2c675f4c0`
- **参数名**: `CsmSignatureVerifyKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the signature verify key.
This value is generated as constant value without any modifications. Thus, this value needs to be set either in bytes or in bits depending on what is expected by the required Crypto Driver.
E.g. set 8 if eight bytes are required, but set 64 if sixty-four bits are required.

####### STRING 类型参数

######## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `7a3383da-ef67-4f83-907c-53b9bf9b21a1`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `77d20415-becd-4d5e-a574-d56e52e8652d`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `002eb5ee-ac8a-4b48-b188-8d5946776c12`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

####### ENUMERATION 类型参数

######## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `bd7c744b-b792-4fde-883e-251afe07124f`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_ED25519` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_RSA` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `71c1a792-dc01-46ee-81d7-acc47a4ed31a`
- **参数名**: `CsmSignatureVerifyAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `580d0c6b-145d-4b80-9105-7a851aa09293`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `e43b33d0-92b8-4425-b9a2-74fdf2e9a5ae`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BLAKE` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 5. CsmSignatureVerifyProcessing

- **UUID**: `778f1b69-78fd-4321-b1bf-eadb9eecb250`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: Vector Informatik)
  - `CSM_SYNCHRONOUS` (来源: Vector Informatik)
- **描述**: Not used.
Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

Csm will ignore this parameter since it is obsolete as of AUTOSAR 4.4. However, other modules may still rely on its value.
It is strongly encouraged to make this parameter consistent with the ProcessingMode parameter in the Jobs that use this primitive. If multiple Jobs with different Processing Modes shall use the same Primitive, the respective Primitive may need to be duplicated and the duplicate's Processing parameter adapted accordingly.

######## 6. CsmSignatureVerifySwcInterfaceVersion

- **UUID**: `14fdc583-e086-4028-a223-717684e9e1bd`
- **参数名**: `CsmSignatureVerifySwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification

Compared to AUTOSAR 4.3.x, AUTOSAR 4.4.0 introduces the following additional error codes to the interface's operations:
SignatureVerify:	CSM_E_KEY_NOT_VALID, 
		CSM_E_KEY_SIZE_MISMATCH,
		CSM_E_KEY_EMPTY
CancelJob: 	CSM_E_JOB_CANCELED

##### 32. CsmJobKeySetValid

**容器属性**:

- **UUID**: `a1db257a-7cbd-44cd-99bc-d2ec2220f0c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValid`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeySetValid primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

##### 33. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

##### 34. CsmJobKeyExchangeCalcPubVal

**容器属性**:

- **UUID**: `af6f30ca-e432-4970-89de-36e298ef961b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubVal`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyExchangeCalcPubVal primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `15688ba9-0142-4fae-a0f6-63e40e663d8b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubValConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom

- **UUID**: `b16995dc-e03d-4d42-a86a-f45148f6955f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmModeCustom

- **UUID**: `6ef6109b-d458-4036-859a-4d6dd7a6d236`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom

- **UUID**: `13d6d865-52e2-4177-b927-69fe37acd552`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used .

######### ENUMERATION 类型参数

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamiliy

- **UUID**: `031de714-ca71-4d4c-a674-af021dec067f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `9fd613c7-a8cd-45fd-938b-40f825dfed47`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `87269892-d6e7-4911-86a5-3363b3e86a9e`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `28dd9b0a-0d2a-4a45-93e1-0fbca48bcd26`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 35. CsmJobKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `15688ba9-0142-4fae-a0f6-63e40e663d8b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubValConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### STRING 类型参数

######## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom

- **UUID**: `b16995dc-e03d-4d42-a86a-f45148f6955f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 2. CsmJobKeyExchangeCalcPubValAlgorithmModeCustom

- **UUID**: `6ef6109b-d458-4036-859a-4d6dd7a6d236`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

######## 3. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom

- **UUID**: `13d6d865-52e2-4177-b927-69fe37acd552`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used .

####### ENUMERATION 类型参数

######## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamiliy

- **UUID**: `031de714-ca71-4d4c-a674-af021dec067f`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `9fd613c7-a8cd-45fd-938b-40f825dfed47`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `87269892-d6e7-4911-86a5-3363b3e86a9e`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `28dd9b0a-0d2a-4a45-93e1-0fbca48bcd26`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 36. CsmJobKeyExchangeCalcSecret

**容器属性**:

- **UUID**: `6c193f86-0d38-43d9-9bd7-c49c44d38aa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecret`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyExchangeCalcSecret primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `7cc3e7e7-dff2-4e9c-a2c3-f13bfed833f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecretConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom

- **UUID**: `2249f7fa-8204-4759-ac13-4318e2358fdd`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmModeCustom

- **UUID**: `1343feb6-56c0-4c08-b649-cbf1081c2c07`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom

- **UUID**: `56c74b6a-53d7-4998-ac73-c9e572f0e807`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamiliy

- **UUID**: `3f4f6dec-cf68-4fab-bd65-6c52970be6c3`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `22383b97-f8a3-424c-bf31-03aed722dcce`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `79645796-8ef0-42a2-963e-8552543c8365`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `2521a0d6-572b-4cce-b73b-c921e5fa38ed`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 37. CsmJobKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `7cc3e7e7-dff2-4e9c-a2c3-f13bfed833f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecretConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### STRING 类型参数

######## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom

- **UUID**: `2249f7fa-8204-4759-ac13-4318e2358fdd`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 2. CsmJobKeyExchangeCalcSecretAlgorithmModeCustom

- **UUID**: `1343feb6-56c0-4c08-b649-cbf1081c2c07`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

######## 3. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom

- **UUID**: `56c74b6a-53d7-4998-ac73-c9e572f0e807`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamiliy

- **UUID**: `3f4f6dec-cf68-4fab-bd65-6c52970be6c3`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `22383b97-f8a3-424c-bf31-03aed722dcce`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `79645796-8ef0-42a2-963e-8552543c8365`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `2521a0d6-572b-4cce-b73b-c921e5fa38ed`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 38. CsmJobKeyDerive

**容器属性**:

- **UUID**: `193cb819-106c-464e-8849-1538a60171c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDerive`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyDerive primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeyDeriveConfig

**容器属性**:

- **UUID**: `ea77b905-c682-448a-81d5-308ed051222e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDeriveConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key derive operation. The container name serves as a symbolic name for the identifier of a key derive configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyDeriveAlgorithmModeCustom

- **UUID**: `da7f433d-c834-4c2c-b010-2d3c90fd7b48`
- **参数名**: `CsmJobKeyDeriveAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

########## 2. CsmJobKeyDeriveAlgorithmFamilyCustom

- **UUID**: `644c6329-a1cc-4c41-9606-5dacc2eee303`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 3. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom

- **UUID**: `5d47bc1f-89a9-4d69-ad05-32cd8155a645`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyDeriveAlgorithmFamiliy

- **UUID**: `ef281c96-a78a-404d-8b3c-2a69fb22c571`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `567569b7-f26e-4d9f-b973-ba32e460241a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `e600b709-5a0d-49cf-9237-a4ab86964a30`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyDeriveAlgorithmSecondaryFamily

- **UUID**: `fbd98446-c450-4ef0-8cc1-9df908a805ea`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 39. CsmJobKeyDeriveConfig

**容器属性**:

- **UUID**: `ea77b905-c682-448a-81d5-308ed051222e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDeriveConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key derive operation. The container name serves as a symbolic name for the identifier of a key derive configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### STRING 类型参数

######## 1. CsmJobKeyDeriveAlgorithmModeCustom

- **UUID**: `da7f433d-c834-4c2c-b010-2d3c90fd7b48`
- **参数名**: `CsmJobKeyDeriveAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

######## 2. CsmJobKeyDeriveAlgorithmFamilyCustom

- **UUID**: `644c6329-a1cc-4c41-9606-5dacc2eee303`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 3. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom

- **UUID**: `5d47bc1f-89a9-4d69-ad05-32cd8155a645`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobKeyDeriveAlgorithmFamiliy

- **UUID**: `ef281c96-a78a-404d-8b3c-2a69fb22c571`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `567569b7-f26e-4d9f-b973-ba32e460241a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `e600b709-5a0d-49cf-9237-a4ab86964a30`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmJobKeyDeriveAlgorithmSecondaryFamily

- **UUID**: `fbd98446-c450-4ef0-8cc1-9df908a805ea`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 40. CsmJobRandomSeed

**容器属性**:

- **UUID**: `b99f061c-207a-4862-bd17-bbb358989f0b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeed`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of RandomSeed primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobRandomSeedConfig

**容器属性**:

- **UUID**: `d8a2b8d8-f086-47b4-93a7-8b14fdb26ab1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeedConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random seed operation. The container name serves as a symbolic name for the identifier of a random seed configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### STRING 类型参数

########## 1. CsmJobRandomSeedAlgorithmFamilyCustom

- **UUID**: `bffe13c5-ebf9-4036-9779-19656e3cea60`
- **参数名**: `CsmJobRandomSeedAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobRandomSeedAlgorithmModeCustom

- **UUID**: `dc676f46-ce44-4f5c-a7ba-db0387523cbc`
- **参数名**: `CsmJobRandomSeedAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 3. CsmJobRandomSeedAlgorithmSecondaryFamilyCustom

- **UUID**: `b5789bb6-3ac9-4a16-b1c6-b4ac5a5a965f`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobRandomSeedAlgorithmMode

- **UUID**: `1d1775eb-1efd-44a2-897c-8d3d5eea1859`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 2. CsmJobRandomSeedAlgorithmSecondaryFamily

- **UUID**: `566fb76a-36f8-4ff6-95ea-e72dc0f7f820`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `bf0df573-32e6-49de-8cca-db8d277a3af2`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

##### 41. CsmJobRandomSeedConfig

**容器属性**:

- **UUID**: `d8a2b8d8-f086-47b4-93a7-8b14fdb26ab1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeedConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random seed operation. The container name serves as a symbolic name for the identifier of a random seed configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### STRING 类型参数

######## 1. CsmJobRandomSeedAlgorithmFamilyCustom

- **UUID**: `bffe13c5-ebf9-4036-9779-19656e3cea60`
- **参数名**: `CsmJobRandomSeedAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######## 2. CsmJobRandomSeedAlgorithmModeCustom

- **UUID**: `dc676f46-ce44-4f5c-a7ba-db0387523cbc`
- **参数名**: `CsmJobRandomSeedAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######## 3. CsmJobRandomSeedAlgorithmSecondaryFamilyCustom

- **UUID**: `b5789bb6-3ac9-4a16-b1c6-b4ac5a5a965f`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobRandomSeedAlgorithmMode

- **UUID**: `1d1775eb-1efd-44a2-897c-8d3d5eea1859`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CTRDRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_HMAC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_2_4` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_SIPHASH_4_8` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 2. CsmJobRandomSeedAlgorithmSecondaryFamily

- **UUID**: `566fb76a-36f8-4ff6-95ea-e72dc0f7f820`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

######## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `bf0df573-32e6-49de-8cca-db8d277a3af2`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RIPEMD160` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RNG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA1` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA2_512_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_224` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_384` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHA3_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

##### 42. CsmJobKeyGenerate

**容器属性**:

- **UUID**: `39234e8f-11d2-47fe-a004-8cf3cfdf3a80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerate`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeyGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeyGenerateConfig

**容器属性**:

- **UUID**: `d6eb3dda-2dbb-4134-83ff-a2a860f0c3ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key generate operation. The container name serves as a symbolic name for the identifier of a key generate configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### STRING 类型参数

########## 1. CsmJobKeyGenerateAlgorithmModeCustom

- **UUID**: `2f147e45-8821-45d9-b6ce-d303bf78f9a4`
- **参数名**: `CsmJobKeyGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

########## 2. CsmJobKeyGenerateAlgorithmFamilyCustom

- **UUID**: `53674cb8-88db-464b-a63c-53855148c553`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 3. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `1272d3b2-2b0e-489f-9f59-9c5b56ff2060`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyGenerateAlgorithmFamiliy

- **UUID**: `97222373-b47d-412a-8014-f378fd38dd60`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `b8140a6c-5f24-463a-a3fc-bbca1143290f`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `d4c0fc39-08df-46f6-89e8-5447c4326572`
- **参数名**: `CsmJobKeyGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmJobKeyGenerateAlgorithmSecondaryFamily

- **UUID**: `e9efd092-be94-4c48-a1d8-33d4e8e00b60`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 43. CsmJobKeyGenerateConfig

**容器属性**:

- **UUID**: `d6eb3dda-2dbb-4134-83ff-a2a860f0c3ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key generate operation. The container name serves as a symbolic name for the identifier of a key generate configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### STRING 类型参数

######## 1. CsmJobKeyGenerateAlgorithmModeCustom

- **UUID**: `2f147e45-8821-45d9-b6ce-d303bf78f9a4`
- **参数名**: `CsmJobKeyGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm mode used for the crypto service.

######## 2. CsmJobKeyGenerateAlgorithmFamilyCustom

- **UUID**: `53674cb8-88db-464b-a63c-53855148c553`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 3. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `1272d3b2-2b0e-489f-9f59-9c5b56ff2060`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobKeyGenerateAlgorithmFamiliy

- **UUID**: `97222373-b47d-412a-8014-f378fd38dd60`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `b8140a6c-5f24-463a-a3fc-bbca1143290f`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `d4c0fc39-08df-46f6-89e8-5447c4326572`
- **参数名**: `CsmJobKeyGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmJobKeyGenerateAlgorithmSecondaryFamily

- **UUID**: `e9efd092-be94-4c48-a1d8-33d4e8e00b60`
- **参数名**: `CsmJobKeyGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 44. CsmJobCertificateParse

**容器属性**:

- **UUID**: `00081a11-438d-4d59-8f81-f3c8df28c18c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParse`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of CertificateParse primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobCertificateParseConfig

**容器属性**:

- **UUID**: `8305d7f7-c8e7-4f03-9f0d-7a27306e5d91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParseConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateParse. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobCertificateParseDataMaxLength

- **UUID**: `38b53552-8b36-459c-9522-e356b137557e`
- **参数名**: `CsmJobCertificateParseDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######### STRING 类型参数

########## 1. CsmJobCertificateParseAlgorithmFamilyCustom

- **UUID**: `46608e1c-9258-4b2a-9c7f-49c6e49131f4`
- **参数名**: `CsmJobCertificateParseAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobCertificateParseAlgorithmModeCustom

- **UUID**: `83b39cc7-11dd-4b7b-ae34-21fc09397d32`
- **参数名**: `CsmJobCertificateParseAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobCertificateParseAlgorithmSecondaryFamilyCustom

- **UUID**: `a134720a-976d-4c39-b209-9973c28af5aa`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobCertificateParseAlgorithmMode

- **UUID**: `b128956c-1e57-4ccd-9fde-5a9402b644a9`
- **参数名**: `CsmJobCertificateParseAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 2. CsmJobCertificateParseAlgorithmSecondaryFamily

- **UUID**: `d125abf0-d21f-433f-9f49-a2ab60a162d8`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 45. CsmJobCertificateParseConfig

**容器属性**:

- **UUID**: `8305d7f7-c8e7-4f03-9f0d-7a27306e5d91`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateParseConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateParse. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. CsmJobCertificateParseDataMaxLength

- **UUID**: `38b53552-8b36-459c-9522-e356b137557e`
- **参数名**: `CsmJobCertificateParseDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

####### STRING 类型参数

######## 1. CsmJobCertificateParseAlgorithmFamilyCustom

- **UUID**: `46608e1c-9258-4b2a-9c7f-49c6e49131f4`
- **参数名**: `CsmJobCertificateParseAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######## 2. CsmJobCertificateParseAlgorithmModeCustom

- **UUID**: `83b39cc7-11dd-4b7b-ae34-21fc09397d32`
- **参数名**: `CsmJobCertificateParseAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

######## 3. CsmJobCertificateParseAlgorithmSecondaryFamilyCustom

- **UUID**: `a134720a-976d-4c39-b209-9973c28af5aa`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobCertificateParseAlgorithmMode

- **UUID**: `b128956c-1e57-4ccd-9fde-5a9402b644a9`
- **参数名**: `CsmJobCertificateParseAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 2. CsmJobCertificateParseAlgorithmSecondaryFamily

- **UUID**: `d125abf0-d21f-433f-9f49-a2ab60a162d8`
- **参数名**: `CsmJobCertificateParseAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 46. CsmJobCertificateVerify

**容器属性**:

- **UUID**: `e19f001a-6b1d-4ebb-8ad6-7c3965c5347c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of CertificateVerify primitves

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobCertificateVerifyConfig

**容器属性**:

- **UUID**: `40a122f0-fa36-43ac-b6b5-c2792be71852`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateVerify. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobCertificateVerifyDataMaxLength

- **UUID**: `64cfd2e1-3153-479a-bc35-ab8208b5f625`
- **参数名**: `CsmJobCertificateVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

######### STRING 类型参数

########## 1. CsmJobCertificateVerifyAlgorithmFamilyCustom

- **UUID**: `17327682-7639-46b9-9b36-226d28c86ee6`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

########## 2. CsmJobCertificateVerifyAlgorithmModeCustom

- **UUID**: `e5864b7c-f3ec-4b23-91b2-36474f4012e3`
- **参数名**: `CsmJobCertificateVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ffe2c517-b33d-4709-8234-78e06dec4261`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######### ENUMERATION 类型参数

########## 1. CsmJobCertificateVerifyAlgorithmFamiliy

- **UUID**: `7ddc57e7-4d4d-43cd-a5af-f6b8d7ef052c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 47. CsmJobCertificateVerifyConfig

**容器属性**:

- **UUID**: `40a122f0-fa36-43ac-b6b5-c2792be71852`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerifyConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM CsmJobCertificateVerify. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CsmJobCertificateVerifyDataMaxLength

- **UUID**: `64cfd2e1-3153-479a-bc35-ab8208b5f625`
- **参数名**: `CsmJobCertificateVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Max size of the input data length in bytes

####### STRING 类型参数

######## 1. CsmJobCertificateVerifyAlgorithmFamilyCustom

- **UUID**: `17327682-7639-46b9-9b36-226d28c86ee6`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

######## 2. CsmJobCertificateVerifyAlgorithmModeCustom

- **UUID**: `e5864b7c-f3ec-4b23-91b2-36474f4012e3`
- **参数名**: `CsmJobCertificateVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of the custom primitive mode.

######## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ffe2c517-b33d-4709-8234-78e06dec4261`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used.

####### ENUMERATION 类型参数

######## 1. CsmJobCertificateVerifyAlgorithmFamiliy

- **UUID**: `7ddc57e7-4d4d-43cd-a5af-f6b8d7ef052c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 48. CsmQueues

**容器属性**:

- **UUID**: `36453455-0361-49da-afa3-70430677dd9a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueues`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for CSM queue configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmQueue

**容器属性**:

- **UUID**: `f60f94b1-4deb-4b45-adcc-916576801412`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueue`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM queue. The container name serves as a symbolic name for the identifier of a queue configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CsmQueueSize

- **UUID**: `9211e48c-c944-4df1-8b41-a1262bd6eabd`
- **参数名**: `CsmQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the CsmQueue. If jobs cannot be processed by the underlying hardware since the hardware is busy, the jobs stay in the prioritized queue. If the queue is full, the next job will be rejected.

######### BOOLEAN 类型参数

########## 1. CsmTriggerAsynchJobsInCallback

- **UUID**: `dc9f21c1-adc6-4e69-bf7a-ff79254df0ef`
- **参数名**: `CsmTriggerAsynchJobsInCallback`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, jobs will be triggered (given to the CryIf for processing) directly if the CryIf notifies the Csm that the last job was finished. Both is handled in the Csm_CallbackNotification().

If not enabled, the next job will be given to the CryIf for processing in the next mainfunction cycle.

########## 2. CsmJobSharing

- **UUID**: `8aa945bd-f119-424c-bf5f-7a882adf6d72`
- **参数名**: `CsmJobSharing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, Csm will use shared job objects per queue instead of reserving an own job object for each configured job. This highly reduces the amount of needed RAM but increases the runtime due to setting up the complete job with every usage.

The Csm will reserve the following amount of job objects:
1 for all synchrnous jobs of the queue (if there are any)
Queue size + 1 for all asynchronous jobs (if there are any)
This means the queue of the Csm can be filled completely while one job is currenlty processed by the crypto driver object.
If the crypto driver object which handles the job of this queue also implements a queing mechanism, either increase the queue size of Csm accordingly to get the necessary amount of job objects, or deactivate the job sharing.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmChannelRef

- **UUID**: `c23e5c7b-4e05-4481-893c-45173483bdac`
- **引用名**: `CsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the underlying Crypto Interface channel.
Violation: Ref Target points currently to CryIf/CryIfKeys/CryIfKey instead of CryIf/CryIfChannel as defined in ASR 4.3

##### 49. CsmQueue

**容器属性**:

- **UUID**: `f60f94b1-4deb-4b45-adcc-916576801412`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueue`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM queue. The container name serves as a symbolic name for the identifier of a queue configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CsmQueueSize

- **UUID**: `9211e48c-c944-4df1-8b41-a1262bd6eabd`
- **参数名**: `CsmQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Size of the CsmQueue. If jobs cannot be processed by the underlying hardware since the hardware is busy, the jobs stay in the prioritized queue. If the queue is full, the next job will be rejected.

####### BOOLEAN 类型参数

######## 1. CsmTriggerAsynchJobsInCallback

- **UUID**: `dc9f21c1-adc6-4e69-bf7a-ff79254df0ef`
- **参数名**: `CsmTriggerAsynchJobsInCallback`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, jobs will be triggered (given to the CryIf for processing) directly if the CryIf notifies the Csm that the last job was finished. Both is handled in the Csm_CallbackNotification().

If not enabled, the next job will be given to the CryIf for processing in the next mainfunction cycle.

######## 2. CsmJobSharing

- **UUID**: `8aa945bd-f119-424c-bf5f-7a882adf6d72`
- **参数名**: `CsmJobSharing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, Csm will use shared job objects per queue instead of reserving an own job object for each configured job. This highly reduces the amount of needed RAM but increases the runtime due to setting up the complete job with every usage.

The Csm will reserve the following amount of job objects:
1 for all synchrnous jobs of the queue (if there are any)
Queue size + 1 for all asynchronous jobs (if there are any)
This means the queue of the Csm can be filled completely while one job is currenlty processed by the crypto driver object.
If the crypto driver object which handles the job of this queue also implements a queing mechanism, either increase the queue size of Csm accordingly to get the necessary amount of job objects, or deactivate the job sharing.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmChannelRef

- **UUID**: `c23e5c7b-4e05-4481-893c-45173483bdac`
- **引用名**: `CsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Refers to the underlying Crypto Interface channel.
Violation: Ref Target points currently to CryIf/CryIfKeys/CryIfKey instead of CryIf/CryIfChannel as defined in ASR 4.3

##### 50. CsmCallouts

**容器属性**:

- **UUID**: `b9e97fae-50e8-459d-b185-39d1eaad7ee5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallouts`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Container for callout function configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmCallout

**容器属性**:

- **UUID**: `f9317712-d834-4282-83f5-8ab93916d14b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallout`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of callout functions

######## 参数配置

此容器包含 **2** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. CsmPreJobCalloutFunc

- **UUID**: `b07df688-9d7b-41a4-977a-97510728fa73`
- **参数名**: `CsmPreJobCalloutFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Callout function which will be called before the corresponding job is executed.

########## 2. CsmPostJobCalloutFunc

- **UUID**: `6675f641-8fa1-4b4f-9239-dc5058d6b633`
- **参数名**: `CsmPostJobCalloutFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Callout function which will be called after the corresponding job is executed.

##### 51. CsmCallout

**容器属性**:

- **UUID**: `f9317712-d834-4282-83f5-8ab93916d14b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallout`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of callout functions

###### 参数配置

此容器包含 **2** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. CsmPreJobCalloutFunc

- **UUID**: `b07df688-9d7b-41a4-977a-97510728fa73`
- **参数名**: `CsmPreJobCalloutFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Callout function which will be called before the corresponding job is executed.

######## 2. CsmPostJobCalloutFunc

- **UUID**: `6675f641-8fa1-4b4f-9239-dc5058d6b633`
- **参数名**: `CsmPostJobCalloutFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Callout function which will be called after the corresponding job is executed.

##### 52. CsmInOutRedirections

**容器属性**:

- **UUID**: `3ed8d006-fced-44a5-84aa-4da7b9741294`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmInOutRedirections`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configuration for Csm redirection configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmInOutRedirection

**容器属性**:

- **UUID**: `67736253-1482-4d36-a2d1-311aea3aee80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmInOutRedirection`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a Csm redirection. A redirection lets a Csm job use a specific key element as input or/and output.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CsmInputKeyElementId

- **UUID**: `8709825c-2a68-47e3-9f57-bc604b7251fa`
- **参数名**: `CsmInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as input.

########## 2. CsmSecondaryInputKeyElementId

- **UUID**: `50d6cd30-6cfd-470f-a74e-f3478f64e6cb`
- **参数名**: `CsmSecondaryInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as secondary input.

########## 3. CsmTertiaryInputKeyElementId

- **UUID**: `df3df7ac-d2d4-41a4-81c0-598f539e4a3c`
- **参数名**: `CsmTertiaryInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as tertiary input.

########## 4. CsmOutputKeyElementId

- **UUID**: `f79133cd-8456-4e58-8bd2-10bdd4767cc4`
- **参数名**: `CsmOutputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as output.

########## 5. CsmSecondaryOutputKeyElementId

- **UUID**: `1313fbeb-3857-4fa4-b211-4536faf795e8`
- **参数名**: `CsmSecondaryOutputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as secondary output.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. CsmInputKeyRef

- **UUID**: `98a947c6-a16b-4e6c-8044-d1e3d085c4e0`
- **引用名**: `CsmInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as input,

########## 2. CsmSecondaryInputKeyRef

- **UUID**: `26a5809c-61d7-4a71-b52b-43b1c6183a72`
- **引用名**: `CsmSecondaryInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as secondary input,

########## 3. CsmTertiaryInputKeyRef

- **UUID**: `9efe74c6-806b-4e72-96dd-c351a5e2088b`
- **引用名**: `CsmTertiaryInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as tertiary input,

########## 4. CsmOutputKeyRef

- **UUID**: `57730c57-7959-457f-91ca-42e5dab48b44`
- **引用名**: `CsmOutputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as output,

########## 5. CsmSecondaryOutputKeyRef

- **UUID**: `69594a6d-b615-4333-99a8-00ee67f61c71`
- **引用名**: `CsmSecondaryOutputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as secondary output.

##### 53. CsmInOutRedirection

**容器属性**:

- **UUID**: `67736253-1482-4d36-a2d1-311aea3aee80`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmInOutRedirection`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of a Csm redirection. A redirection lets a Csm job use a specific key element as input or/and output.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CsmInputKeyElementId

- **UUID**: `8709825c-2a68-47e3-9f57-bc604b7251fa`
- **参数名**: `CsmInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as input.

######## 2. CsmSecondaryInputKeyElementId

- **UUID**: `50d6cd30-6cfd-470f-a74e-f3478f64e6cb`
- **参数名**: `CsmSecondaryInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as secondary input.

######## 3. CsmTertiaryInputKeyElementId

- **UUID**: `df3df7ac-d2d4-41a4-81c0-598f539e4a3c`
- **参数名**: `CsmTertiaryInputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as tertiary input.

######## 4. CsmOutputKeyElementId

- **UUID**: `f79133cd-8456-4e58-8bd2-10bdd4767cc4`
- **参数名**: `CsmOutputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as output.

######## 5. CsmSecondaryOutputKeyElementId

- **UUID**: `1313fbeb-3857-4fa4-b211-4536faf795e8`
- **参数名**: `CsmSecondaryOutputKeyElementId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Identifier of the key element used as secondary output.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. CsmInputKeyRef

- **UUID**: `98a947c6-a16b-4e6c-8044-d1e3d085c4e0`
- **引用名**: `CsmInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as input,

######## 2. CsmSecondaryInputKeyRef

- **UUID**: `26a5809c-61d7-4a71-b52b-43b1c6183a72`
- **引用名**: `CsmSecondaryInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as secondary input,

######## 3. CsmTertiaryInputKeyRef

- **UUID**: `9efe74c6-806b-4e72-96dd-c351a5e2088b`
- **引用名**: `CsmTertiaryInputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as tertiary input,

######## 4. CsmOutputKeyRef

- **UUID**: `57730c57-7959-457f-91ca-42e5dab48b44`
- **引用名**: `CsmOutputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as output,

######## 5. CsmSecondaryOutputKeyRef

- **UUID**: `69594a6d-b615-4333-99a8-00ee67f61c71`
- **引用名**: `CsmSecondaryOutputKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter refers to the key used as secondary output.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Csm**

##### BSW-IMPLEMENTATION 类型元素

1. **Csm_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Csm_Pre**
2. **Csm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Csm_Impl

- **UUID**: `bea33e28-3574-4303-9ea7-106c12f56ff8`
- **实现名称**: `Csm_Impl`
- **编程语言**: C
- **软件版本**: 5.01.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.04.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Csm_Pre

- **UUID**: `09ac86b2-eb5e-47f6-a12b-bc935b501849`
- **配置名称**: `Csm_Pre`
- **定义引用**: `/MICROSAR/Csm`

### 2. Csm_Rec

- **UUID**: `d4f0c305-9e8e-4b1d-a795-9450e352662e`
- **配置名称**: `Csm_Rec`
- **定义引用**: `/MICROSAR/Csm`
