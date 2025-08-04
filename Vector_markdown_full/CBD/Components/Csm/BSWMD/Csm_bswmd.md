# Csm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:45

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

The Crypto Service Manager (CSM) provides synchronous or asynchronous services to enable a unique access to basic cryptographic functionalities for all software modules. The CSM provides an abstraction layer, which offers an AUTOSAR standardized interface to higher software layers to access these functionalities required for security related use cases. Since functionality required by a software module can be different to the functionality required by other software modules, there is the possibility to configure and initialize the services provided by the CSM individually for each software module.

#Crypto #Cryptographic #Cryptography #Security
#AUTOSAR
#ServiceComponent

#### 版本历史

共有 **32** 个版本记录：

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

##### 24. 版本 6.00.00

- **状态**: released
- **发布日期**: 2020-12-14T13:26:36+01:00
- **发布者**: vismxe

**变更内容**:

##### 25. 版本 6.01.00

- **状态**: released
- **发布日期**: 2021-03-16T14:31:00+01:00
- **发布者**: visenc

**变更内容**:

##### 26. 版本 6.01.01

- **状态**: released
- **发布日期**: 2021-06-07T18:31:38+02:00
- **发布者**: visrpp

**变更内容**:

##### 27. 版本 6.02.00

- **状态**: released
- **发布日期**: 2021-11-26T19:01:39+01:00
- **发布者**: visewl

**变更内容**:

##### 28. 版本 6.03.00

- **状态**: released
- **发布日期**: 2022-03-10T15:47:05+01:00
- **发布者**: visrpp

**变更内容**:

##### 29. 版本 7.00.00

- **状态**: released
- **发布日期**: 2023-01-18T15:48:22+01:00
- **发布者**: visrpp

**变更内容**:

##### 30. 版本 7.01.00

- **状态**: released
- **发布日期**: 2023-04-12T12:24:44+02:00
- **发布者**: visfnn

**变更内容**:

##### 31. 版本 7.02.00

- **状态**: released
- **发布日期**: 2023-07-27T15:46:45+02:00
- **发布者**: visfnn

**变更内容**:

##### 32. 版本 7.02.01

- **状态**: released
- **发布日期**: 2024-02-15T14:43:05+01:00
- **发布者**: vismwe

**变更内容**:

#### 配置容器

本模块包含 **58** 个配置容器：

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

########## 1. CsmCallbackAsrVersion

- **UUID**: `9df71d3d-2b9b-42ef-bc30-32d800511859`
- **参数名**: `CsmCallbackAsrVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the configured callback when it is used as BSW or SWC callback.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the differences between the versions are listed:

CSM_ASR_VERSION_R20_11:
BSW: void <CallbackFunc> (uint32 jobId, Crypto_ResultType result)
SWC: same as in CSM_ASR_VERSION_R19_11

CSM_ASR_VERSION_R19_11:
BSW: void <CallbackFunc> (const Crypto_JobType* job, Crypto_ResultType result)
SWC: CallbackNotification operation with Crypto_ResultType as argument. Provided port name is CallbackNotification_<Job.name>

CSM_ASR_VERSION_4_04:
BSW: void <CallbackFunc> (const uint32 jobID, Csm_ResultType result)
SWC: CallbackNotification operation with Csm_ResultType as argument. Provided port name is CallbackNotification_<Job.name>

CSM_ASR_VERSION_4_03:
BSW: void <CallbackFunc> (Crypto_JobType* job, Std_ReturnType result)
SWC: CallbackNotification operation with Csm_ResultType as argument. Provided port name is <CallbackFunc>_Callback


Defaults to latest version (CSM_ASR_VERSION_R20_11) if unset.

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

######## 1. CsmCallbackAsrVersion

- **UUID**: `9df71d3d-2b9b-42ef-bc30-32d800511859`
- **参数名**: `CsmCallbackAsrVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the configured callback when it is used as BSW or SWC callback.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the differences between the versions are listed:

CSM_ASR_VERSION_R20_11:
BSW: void <CallbackFunc> (uint32 jobId, Crypto_ResultType result)
SWC: same as in CSM_ASR_VERSION_R19_11

CSM_ASR_VERSION_R19_11:
BSW: void <CallbackFunc> (const Crypto_JobType* job, Crypto_ResultType result)
SWC: CallbackNotification operation with Crypto_ResultType as argument. Provided port name is CallbackNotification_<Job.name>

CSM_ASR_VERSION_4_04:
BSW: void <CallbackFunc> (const uint32 jobID, Csm_ResultType result)
SWC: CallbackNotification operation with Csm_ResultType as argument. Provided port name is CallbackNotification_<Job.name>

CSM_ASR_VERSION_4_03:
BSW: void <CallbackFunc> (Crypto_JobType* job, Std_ReturnType result)
SWC: CallbackNotification operation with Csm_ResultType as argument. Provided port name is <CallbackFunc>_Callback


Defaults to latest version (CSM_ASR_VERSION_R20_11) if unset.

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

此容器包含 **13** 个参数：

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

Attention: If enabled additional preconditions must be fulfilled. The user must ensure that the callback notifications from lower layer cannot be interrupted by a cancel operation (e.g., by a task switch). This can be ensured by the task mapping.

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

######## 7. CsmMultiPartitionRuntimeChecks

- **UUID**: `288c6874-5556-4fd6-946b-a334c663d1ae`
- **参数名**: `CsmMultiPartitionRuntimeChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled, additional checks are performed to prevent the execution of jobs by the wrong partition.

######## 8. CsmSwcUseErrorCodesCsmPrefix

- **UUID**: `49611ad7-af91-496f-ba58-4dc8d84face0`
- **参数名**: `CsmSwcUseErrorCodesCsmPrefix`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Enabling this parameter forces the Csm to use SWC error codes prefixed with CSM_E instead of CRYPTO_E for SWC interfaces which shall use a version between CSM_ASR_VERSION_R19_11 and CSM_ASR_VERSION_R21_11.

Rational: Starting from Csm version 7.0.0 to 7.2.0, SWC interfaces according to AUTOSAR R19-11 to R21-11 were provided nonconforming by Csm due to the usage of error codes prefixed with CSM_E instead of CRYPTO_E (ESCAN00116232).

This parameter is deprecated and shall only be turned on if an existing project relies on the former provided nonconforming interfaces.

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

####### ENUMERATION 类型参数

######## 1. CsmSwcMainInterfaceVersion

- **UUID**: `a31747c9-66ac-4665-b6af-82bb484ccf3d`
- **参数名**: `CsmSwcMainInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_R21_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: This parameter sets the main SwcInterface version.
Since this Csm implementation supports multiple AUTOSAR versions which provide different, incompatible variations of the same interface, names of the interfaces must be different. This applies to all interfaces which are not dependent on a specific job or primitive, e.g. the port optimized CsmHash interfaces using data references as argument. Therefore, this Csm implementation provides all interfaces using the specified name postfixed by the AUTOSAR version introducing the latest change to the corresponding interface, resulting in e,g. CsmHashAsrR19_11. The interfaces matching the here configured main SwcInterface version are provided with the name defined by AUTOSAR in addition, e.g. CsmHash.

Rational:
The postfixing only affects the name of the provided Client/Server Port Interfaces but not their operations!
The name of the interface is only relevant if the interfaces of the Csm are directly referenced by a SWC. SWCs which provide their own interface description are not affected and can be connected to the Csm ports independently of Csm's Port Interface name.

With the parameter set to enumeration value NONE, only the postfixed interfaces are available.

###### 配置容器

本模块包含 **3** 个配置容器：

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

此容器包含 **10** 个参数：

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
- **描述**: The Crypto_JobType has - according to AUTOSAR - the fields 'jobState' and 'jobPrimitiveInputOutput'. These field names changed from AUTOSAR 4.3.0 to AUTOSAR 4.3.1. These fields defined by AUTOSAR 4.3.0 could be required by an underlying Crypto Driver.

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
- **描述**: The Crypto_JobType has in its sub data structures - according to AUTOSAR- certain fields (e.g. 'jobId') which are defined as const fields. If a variable of this type shall be used in different use cases, these fields might be overwritten. This could be a requirement of an underlying Crypto Driver.

If enabled, the const members of Crypto_JobType's sub data structures are defined as non-const members
If disabled, the Crypto_JobType's sub data structures stay as defined according to AUTOSAR.

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
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to AUTOSAR 4.3.0 up to R19 - the field 'input64'. In AUTOSAR R20, this field was removed.
By default, this field is switched off in order to reduce memory usage.
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
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to AUTOSAR 4.3.0 up to R19 - the field 'output64Ptr'. In AUTOSAR R20, this field was removed.
By default, this field is switched off in order to reduce memory usage.
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

########## 6. CsmJobTypeLayoutJobInfoPtr

- **UUID**: `d50ad87e-4631-4001-89db-846a1dd70c74`
- **参数名**: `CsmJobTypeLayoutJobInfoPtr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobInfoType has been removed by AUTOSAR in R21-11 and was replaced by a direct members in the Crypto_JobType ( jobId and jobPriority).
As this field is normally only used by the Csm itself, this field can be switched off in order to reduce memory usage since this implementation of the Csm makes use of the direct members of the Crypto_JobInfoType.
However, this field can be switched on if it is required by some underlying crypto driver.

If enabled, the field 'jobInfo' exists within the Crypto_JobType
If disabled, the field 'jobInfo' doesn't exist within the Crypto_JobType

########## 7. CsmJobTypeLayoutSecureCounterId

- **UUID**: `9ce03199-862a-4ca2-9385-923be433139a`
- **参数名**: `CsmJobTypeLayoutSecureCounterId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInfoType has - according to AUTOSAR 4.3.x - the field 'secureCounterId'. In AUTOSAR 4.4.0, this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'secureCounterId' exists within the Crypto_JobPrimitiveInfoType.
If disabled, the field 'secureCounterId' doesn't exist within the Crypto_JobPrimitiveInfoType.

########## 8. CsmJobTypeLayoutCallbackUpdateNotification

- **UUID**: `b2405efd-e7e4-4f81-ba91-b3c4297bd965`
- **参数名**: `CsmJobTypeLayoutCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInfoType has - according to AUTOSAR 4.3.x up to 4.4.0 - the field 'callbackUpdateNotification'. In AUTOSAR R19, this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'callbackUpdateNotification' exists within the Crypto_JobPrimitiveInfoType.
If disabled, the field 'callbackUpdateNotification' doesn't exist within the Crypto_JobPrimitiveInfoType.

########## 9. CsmJobTypeLayoutResultLength

- **UUID**: `00ba901c-6f1a-47be-8c23-daf5f8b8eaeb`
- **参数名**: `CsmJobTypeLayoutResultLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_PrimitiveInfoType has - according to AUTOSAR 4.3.x up to R19-11 - the field 'resultLength'. In AUTOSAR R20-11 this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'resultLength' exists within the Crypto_PrimitiveInfoType.
If disabled, the field 'resultLength' doesn't exist within the Crypto_PrimitiveInfoType.

######### ENUMERATION 类型参数

########## 1. CsmJobTypeLayoutFieldOrdering

- **UUID**: `37cd46fa-9a2c-4de6-a597-a5056b917eff`
- **参数名**: `CsmJobTypeLayoutFieldOrdering`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_R21_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Although it is not guaranteed, this implementation of the Csm tries to keep the ordering of the elements in the main job structure (Crypto_JobType) according to AUTOSAR to support also Crypto Drivers build as library. As AUTOSAR varies the ordering in its versions, this parameter is used to determine the ordering which the implementation shall follow.

Following, the differences are listed:

CSM_ASR_VERSION_R21_11:
jobRedirectionInfoRef was moved from the position below the cryptoKeyId to the new position below jobPrimitiveInfo.

CSM_ASR_VERSION_4_03:
Default order as originally defined by AUTOSAR

####### 2. CsmBswApiCompatibility

**容器属性**:

- **UUID**: `ca3109f6-56a3-4528-9ca6-eb9f631e54f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswApiCompatibility`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container includes settings for the compatibility of the provided interfaces by Csm, e.g. differentiating between AUTOSAR versions.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmDefaultJobKeyApiVersion

- **UUID**: `b44a5e20-5045-446f-9079-b080230f336e`
- **参数名**: `CsmDefaultJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmBswUserConfiguration

**容器属性**:

- **UUID**: `38fa94f5-c0c0-4b01-8b82-867920071695`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswUserConfiguration`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

With this container, the default configuration of the Bsw Csm Api can be overwritten on a per user (i.e. a Bsw module) base.
This is necessary if different users make use of the Csm but require different versions of the Csm interfaces.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. CsmUserIdentificationDefine

- **UUID**: `7667f77f-9954-4381-ae86-19ec28ba6440`
- **参数名**: `CsmUserIdentificationDefine`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MIP_SOURCE`
  - 最小长度: 1
- **描述**: This is a list of preprocessor defines used to identify and differentiate between the users of the Csm. Based on these defines, the Csm module header provides its interfaces in different versions to the user.

This is only possible, if the Csm user provides an unique preprocessor define before including the Csm module header, e.g.,

#define <MIP>_SOURCE
#include "Csm.h"

void func()
{
  Csm_<Service>(a, b ,c)
}

Due to this, Csm module header is able to provide interfaces according to this CsmBswUserConfiguration.

########### ENUMERATION 类型参数

############ 1. CsmJobKeyApiVersion

- **UUID**: `02578916-3d8c-4847-a0c2-6e60e22962aa`
- **参数名**: `CsmJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

####### 3. CsmBswUserConfiguration

**容器属性**:

- **UUID**: `38fa94f5-c0c0-4b01-8b82-867920071695`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswUserConfiguration`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

With this container, the default configuration of the Bsw Csm Api can be overwritten on a per user (i.e. a Bsw module) base.
This is necessary if different users make use of the Csm but require different versions of the Csm interfaces.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CsmUserIdentificationDefine

- **UUID**: `7667f77f-9954-4381-ae86-19ec28ba6440`
- **参数名**: `CsmUserIdentificationDefine`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MIP_SOURCE`
  - 最小长度: 1
- **描述**: This is a list of preprocessor defines used to identify and differentiate between the users of the Csm. Based on these defines, the Csm module header provides its interfaces in different versions to the user.

This is only possible, if the Csm user provides an unique preprocessor define before including the Csm module header, e.g.,

#define <MIP>_SOURCE
#include "Csm.h"

void func()
{
  Csm_<Service>(a, b ,c)
}

Due to this, Csm module header is able to provide interfaces according to this CsmBswUserConfiguration.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyApiVersion

- **UUID**: `02578916-3d8c-4847-a0c2-6e60e22962aa`
- **参数名**: `CsmJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

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

此容器包含 **10** 个参数：

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
- **描述**: The Crypto_JobType has - according to AUTOSAR - the fields 'jobState' and 'jobPrimitiveInputOutput'. These field names changed from AUTOSAR 4.3.0 to AUTOSAR 4.3.1. These fields defined by AUTOSAR 4.3.0 could be required by an underlying Crypto Driver.

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
- **描述**: The Crypto_JobType has in its sub data structures - according to AUTOSAR- certain fields (e.g. 'jobId') which are defined as const fields. If a variable of this type shall be used in different use cases, these fields might be overwritten. This could be a requirement of an underlying Crypto Driver.

If enabled, the const members of Crypto_JobType's sub data structures are defined as non-const members
If disabled, the Crypto_JobType's sub data structures stay as defined according to AUTOSAR.

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
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to AUTOSAR 4.3.0 up to R19 - the field 'input64'. In AUTOSAR R20, this field was removed.
By default, this field is switched off in order to reduce memory usage.
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
- **描述**: The Crypto_JobPrimitiveInputOutputType has - according to AUTOSAR 4.3.0 up to R19 - the field 'output64Ptr'. In AUTOSAR R20, this field was removed.
By default, this field is switched off in order to reduce memory usage.
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

######## 6. CsmJobTypeLayoutJobInfoPtr

- **UUID**: `d50ad87e-4631-4001-89db-846a1dd70c74`
- **参数名**: `CsmJobTypeLayoutJobInfoPtr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobInfoType has been removed by AUTOSAR in R21-11 and was replaced by a direct members in the Crypto_JobType ( jobId and jobPriority).
As this field is normally only used by the Csm itself, this field can be switched off in order to reduce memory usage since this implementation of the Csm makes use of the direct members of the Crypto_JobInfoType.
However, this field can be switched on if it is required by some underlying crypto driver.

If enabled, the field 'jobInfo' exists within the Crypto_JobType
If disabled, the field 'jobInfo' doesn't exist within the Crypto_JobType

######## 7. CsmJobTypeLayoutSecureCounterId

- **UUID**: `9ce03199-862a-4ca2-9385-923be433139a`
- **参数名**: `CsmJobTypeLayoutSecureCounterId`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInfoType has - according to AUTOSAR 4.3.x - the field 'secureCounterId'. In AUTOSAR 4.4.0, this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'secureCounterId' exists within the Crypto_JobPrimitiveInfoType.
If disabled, the field 'secureCounterId' doesn't exist within the Crypto_JobPrimitiveInfoType.

######## 8. CsmJobTypeLayoutCallbackUpdateNotification

- **UUID**: `b2405efd-e7e4-4f81-ba91-b3c4297bd965`
- **参数名**: `CsmJobTypeLayoutCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_JobPrimitiveInfoType has - according to AUTOSAR 4.3.x up to 4.4.0 - the field 'callbackUpdateNotification'. In AUTOSAR R19, this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'callbackUpdateNotification' exists within the Crypto_JobPrimitiveInfoType.
If disabled, the field 'callbackUpdateNotification' doesn't exist within the Crypto_JobPrimitiveInfoType.

######## 9. CsmJobTypeLayoutResultLength

- **UUID**: `00ba901c-6f1a-47be-8c23-daf5f8b8eaeb`
- **参数名**: `CsmJobTypeLayoutResultLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The Crypto_PrimitiveInfoType has - according to AUTOSAR 4.3.x up to R19-11 - the field 'resultLength'. In AUTOSAR R20-11 this field was removed.
By default, this field is switched off in order to reduce memory usage.
This field can be switched on if it is required by the underlying crypto driver.

If enabled, the field 'resultLength' exists within the Crypto_PrimitiveInfoType.
If disabled, the field 'resultLength' doesn't exist within the Crypto_PrimitiveInfoType.

####### ENUMERATION 类型参数

######## 1. CsmJobTypeLayoutFieldOrdering

- **UUID**: `37cd46fa-9a2c-4de6-a597-a5056b917eff`
- **参数名**: `CsmJobTypeLayoutFieldOrdering`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_R21_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Although it is not guaranteed, this implementation of the Csm tries to keep the ordering of the elements in the main job structure (Crypto_JobType) according to AUTOSAR to support also Crypto Drivers build as library. As AUTOSAR varies the ordering in its versions, this parameter is used to determine the ordering which the implementation shall follow.

Following, the differences are listed:

CSM_ASR_VERSION_R21_11:
jobRedirectionInfoRef was moved from the position below the cryptoKeyId to the new position below jobPrimitiveInfo.

CSM_ASR_VERSION_4_03:
Default order as originally defined by AUTOSAR

##### 5. CsmBswApiCompatibility

**容器属性**:

- **UUID**: `ca3109f6-56a3-4528-9ca6-eb9f631e54f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswApiCompatibility`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container includes settings for the compatibility of the provided interfaces by Csm, e.g. differentiating between AUTOSAR versions.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. CsmDefaultJobKeyApiVersion

- **UUID**: `b44a5e20-5045-446f-9079-b080230f336e`
- **参数名**: `CsmDefaultJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmBswUserConfiguration

**容器属性**:

- **UUID**: `38fa94f5-c0c0-4b01-8b82-867920071695`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswUserConfiguration`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

With this container, the default configuration of the Bsw Csm Api can be overwritten on a per user (i.e. a Bsw module) base.
This is necessary if different users make use of the Csm but require different versions of the Csm interfaces.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. CsmUserIdentificationDefine

- **UUID**: `7667f77f-9954-4381-ae86-19ec28ba6440`
- **参数名**: `CsmUserIdentificationDefine`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MIP_SOURCE`
  - 最小长度: 1
- **描述**: This is a list of preprocessor defines used to identify and differentiate between the users of the Csm. Based on these defines, the Csm module header provides its interfaces in different versions to the user.

This is only possible, if the Csm user provides an unique preprocessor define before including the Csm module header, e.g.,

#define <MIP>_SOURCE
#include "Csm.h"

void func()
{
  Csm_<Service>(a, b ,c)
}

Due to this, Csm module header is able to provide interfaces according to this CsmBswUserConfiguration.

######### ENUMERATION 类型参数

########## 1. CsmJobKeyApiVersion

- **UUID**: `02578916-3d8c-4847-a0c2-6e60e22962aa`
- **参数名**: `CsmJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

##### 6. CsmBswUserConfiguration

**容器属性**:

- **UUID**: `38fa94f5-c0c0-4b01-8b82-867920071695`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmBswUserConfiguration`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

With this container, the default configuration of the Bsw Csm Api can be overwritten on a per user (i.e. a Bsw module) base.
This is necessary if different users make use of the Csm but require different versions of the Csm interfaces.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. CsmUserIdentificationDefine

- **UUID**: `7667f77f-9954-4381-ae86-19ec28ba6440`
- **参数名**: `CsmUserIdentificationDefine`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `MIP_SOURCE`
  - 最小长度: 1
- **描述**: This is a list of preprocessor defines used to identify and differentiate between the users of the Csm. Based on these defines, the Csm module header provides its interfaces in different versions to the user.

This is only possible, if the Csm user provides an unique preprocessor define before including the Csm module header, e.g.,

#define <MIP>_SOURCE
#include "Csm.h"

void func()
{
  Csm_<Service>(a, b ,c)
}

Due to this, Csm module header is able to provide interfaces according to this CsmBswUserConfiguration.

####### ENUMERATION 类型参数

######## 1. CsmJobKeyApiVersion

- **UUID**: `02578916-3d8c-4847-a0c2-6e60e22962aa`
- **参数名**: `CsmJobKeyApiVersion`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Determines the signature of the Csm_JobKey<Service> functions.

CSM_ASR_VERSION_4_04:
The Csm_JobKey<Service> APIs provide an keyId parameter as second parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint32 keyId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

CSM_ASR_VERSION_R21_11:
The Csm_JobKey<Service> APIs does not have an keyId parameter. E.g.
Csm_JobKeyExchangeCalcPubVal(uint32 jobId, uint8* publicValuePtr, uint32* publicValueLengthPtr)

##### 7. CsmJobs

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

此容器包含 **7** 个参数：

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
CRYPTO_USE_FNC: Job is used by BSW, no port is created
CRYPTO_USE_PORT: A server port is created using the interface defining arguments as arrays on a per primitive base.
CRYPTO_USE_PORT_OPTIMIZED: A server port is created using an interface defining arguments as data reference on a per service base. This is the preferred option for new configurations.

Hint: The SWC interfaces can differ between the AUTOSAR versions. Please consider the <Primitive>SwcInterfaceVersion parameter of the referenced CsmPrimitive.

########## 3. CsmJobServiceInterfaceContextUsePort

- **UUID**: `fe263b59-cd38-40e0-9612-5fdaedfdc513`
- **参数名**: `CsmJobServiceInterfaceContextUsePort`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRYPTO_USE_FUNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_USE_FUNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT` (来源: AUTOSAR_ECUC)
- **描述**: Does the job need RTE interfaces for context operations

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

##### 8. CsmJob

**容器属性**:

- **UUID**: `8b866d41-ea5b-4e3d-bfd1-3bdfe21f5353`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJob`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of CSM job. The container name serves as a symbolic name for the identifier of a job configuration.

###### 参数配置

此容器包含 **7** 个参数：

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
CRYPTO_USE_FNC: Job is used by BSW, no port is created
CRYPTO_USE_PORT: A server port is created using the interface defining arguments as arrays on a per primitive base.
CRYPTO_USE_PORT_OPTIMIZED: A server port is created using an interface defining arguments as data reference on a per service base. This is the preferred option for new configurations.

Hint: The SWC interfaces can differ between the AUTOSAR versions. Please consider the <Primitive>SwcInterfaceVersion parameter of the referenced CsmPrimitive.

######## 3. CsmJobServiceInterfaceContextUsePort

- **UUID**: `fe263b59-cd38-40e0-9612-5fdaedfdc513`
- **参数名**: `CsmJobServiceInterfaceContextUsePort`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CRYPTO_USE_FUNC`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_USE_FUNC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_USE_PORT` (来源: AUTOSAR_ECUC)
- **描述**: Does the job need RTE interfaces for context operations

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

##### 9. CsmKeys

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
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this key should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
KeyGetStatus: 		API was added
KeySetInvalid:		API was added

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyCopy:					CSM_E_SMALL_BUFFER was removed and CRYPTO_E_KEY_NOT_AVAILABLE was added as error code. Intentionally, this was already removed in AUTOSAR 4.4 but missed in MICROSAR.
KeyDerive:				CRYPTO_E_KEY_NOT_AVAILABLE was added as error code.
KeyElementCopy:		CSM_E_SMALL_BUFFER was removed and CRYPTO_E_KEY_NOT_AVAILABLE was added as error code. Intentionally, this was already removed in AUTOSAR 4.4 but missed in MICROSAR.
KeyElementGet:		CSM_E_SMALL_BUFFER was removed as error code.
KeyExchangeCalcPubVal:	CSM_E_SMALL_BUFFER was removed as error code. CRYPTO_E_KEY_NOT_VALID was added as error code.
KeyExchangeCalcSecret:	CSM_E_SMALL_BUFFER was removed as error code. CRYPTO_E_KEY_NOT_VALID was added as error code.
KeyGenerate:			CRYPTO_E_KEY_NOT_VALID was added as error code.
RandomSeed: 			CRYPTO_E_KEY_NOT_VALID and CRYPTO_E_KEY_EMPTY were added as error code.

AUTOSAR 4.4.0:
CertificateParse:		CSM_E_KEY_EMPTY was added as error code.
CertificateVerify:		CSM_E_KEY_EMPTY was added as error code.
KeyCopy:					CSM_E_KEY_EMPTY was added as error code.
KeyDerive:				CSM_E_KEY_EMPTY, CSM_E_BUSY, CSM_E_KEY_READ_FAIL, CSM_E_KEY_WRITE_FAIL and CSM_E_KEY_SIZE_MISMATCH were added as error code.
KeyElementCopy:		CSM_E_KEY_EMPTY was added as error code.
KeyElementGet:		CSM_E_KEY_EMPTY was added as error code. Direction of keyLength parameter changed from OUT to INOUT
KeyExchangeCalcPubVal:	CSM_E_KEY_EMPTY and CSM_E_SMALL_BUFFER were added as error code.
KeyExchangeCalcSecret:	CSM_E_KEY_EMPTY and CSM_E_SMALL_BUFFER were added as error code.
KeyGenerate:			CSM_E_KEY_EMPTY and CSM_E_BUSY were added as error code.

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

##### 10. CsmKey

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
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_03` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this key should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
KeyGetStatus: 		API was added
KeySetInvalid:		API was added

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyCopy:					CSM_E_SMALL_BUFFER was removed and CRYPTO_E_KEY_NOT_AVAILABLE was added as error code. Intentionally, this was already removed in AUTOSAR 4.4 but missed in MICROSAR.
KeyDerive:				CRYPTO_E_KEY_NOT_AVAILABLE was added as error code.
KeyElementCopy:		CSM_E_SMALL_BUFFER was removed and CRYPTO_E_KEY_NOT_AVAILABLE was added as error code. Intentionally, this was already removed in AUTOSAR 4.4 but missed in MICROSAR.
KeyElementGet:		CSM_E_SMALL_BUFFER was removed as error code.
KeyExchangeCalcPubVal:	CSM_E_SMALL_BUFFER was removed as error code. CRYPTO_E_KEY_NOT_VALID was added as error code.
KeyExchangeCalcSecret:	CSM_E_SMALL_BUFFER was removed as error code. CRYPTO_E_KEY_NOT_VALID was added as error code.
KeyGenerate:			CRYPTO_E_KEY_NOT_VALID was added as error code.
RandomSeed: 			CRYPTO_E_KEY_NOT_VALID and CRYPTO_E_KEY_EMPTY were added as error code.

AUTOSAR 4.4.0:
CertificateParse:		CSM_E_KEY_EMPTY was added as error code.
CertificateVerify:		CSM_E_KEY_EMPTY was added as error code.
KeyCopy:					CSM_E_KEY_EMPTY was added as error code.
KeyDerive:				CSM_E_KEY_EMPTY, CSM_E_BUSY, CSM_E_KEY_READ_FAIL, CSM_E_KEY_WRITE_FAIL and CSM_E_KEY_SIZE_MISMATCH were added as error code.
KeyElementCopy:		CSM_E_KEY_EMPTY was added as error code.
KeyElementGet:		CSM_E_KEY_EMPTY was added as error code. Direction of keyLength parameter changed from OUT to INOUT
KeyExchangeCalcPubVal:	CSM_E_KEY_EMPTY and CSM_E_SMALL_BUFFER were added as error code.
KeyExchangeCalcSecret:	CSM_E_KEY_EMPTY and CSM_E_SMALL_BUFFER were added as error code.
KeyGenerate:			CSM_E_KEY_EMPTY and CSM_E_BUSY were added as error code.

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

##### 11. CsmPrimitives

**容器属性**:

- **UUID**: `87f9b2de-8c3d-40c2-b1b3-a7253f073a79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmPrimitives`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container for configuration of CsmPrimitives

###### 配置容器

本模块包含 **40** 个配置容器：

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

此容器包含 **13** 个参数：

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

- **UUID**: `5b5f5064-26da-445b-a342-972b74f55a6c`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `5c2bf479-1ec2-431e-ac84-3100a0010fe9`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `f7de62ed-eeb5-46a1-914e-1b955e234a72`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADDecrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADDecrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADDecrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

############ 6. CsmAEADDecryptAlgorithmSecondaryFamily

- **UUID**: `244aaabd-1f92-4582-882f-464a29d695c8`
- **参数名**: `CsmAEADDecryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

########## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that decryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmAEADDecryptAlgorithmFamilyCustomRef

- **UUID**: `b105dc08-b071-47eb-bf6d-9d91ee548fe8`
- **引用名**: `CsmAEADDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `28d72189-656f-4722-be6f-4a8758272ea4`
- **引用名**: `CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmAEADDecryptAlgorithmModeCustomRef

- **UUID**: `1e9402fb-e3c0-44bd-9566-af67865cdf08`
- **引用名**: `CsmAEADDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **13** 个参数：

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

- **UUID**: `5b5f5064-26da-445b-a342-972b74f55a6c`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `5c2bf479-1ec2-431e-ac84-3100a0010fe9`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `f7de62ed-eeb5-46a1-914e-1b955e234a72`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADDecrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADDecrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADDecrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 6. CsmAEADDecryptAlgorithmSecondaryFamily

- **UUID**: `244aaabd-1f92-4582-882f-464a29d695c8`
- **参数名**: `CsmAEADDecryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

######## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that decryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmAEADDecryptAlgorithmFamilyCustomRef

- **UUID**: `b105dc08-b071-47eb-bf6d-9d91ee548fe8`
- **引用名**: `CsmAEADDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `28d72189-656f-4722-be6f-4a8758272ea4`
- **引用名**: `CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmAEADDecryptAlgorithmModeCustomRef

- **UUID**: `1e9402fb-e3c0-44bd-9566-af67865cdf08`
- **引用名**: `CsmAEADDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **13** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `d7ccdc02-2258-4122-94a7-ea3468ef8a82`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c61a45e5-063a-4701-8e6b-518102fd4ede`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADEncrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADEncrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADEncrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

############ 6. CsmAEADEncryptAlgorithmSecondaryFamily

- **UUID**: `5b90f8cb-a424-4fc3-bd55-7618c8f46eae`
- **参数名**: `CsmAEADEncryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

########## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that encryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmAEADEncryptAlgorithmFamilyCustomRef

- **UUID**: `244798ad-9a03-4329-b748-ffeb3795f198`
- **引用名**: `CsmAEADEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `07bbe773-85ee-430c-a6cf-0ba28569450c`
- **引用名**: `CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmAEADEncryptAlgorithmModeCustomRef

- **UUID**: `6672736f-acb5-45f3-8543-bad534c95aa1`
- **引用名**: `CsmAEADEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **13** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `d7ccdc02-2258-4122-94a7-ea3468ef8a82`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c61a45e5-063a-4701-8e6b-518102fd4ede`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADEncrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADEncrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADEncrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 6. CsmAEADEncryptAlgorithmSecondaryFamily

- **UUID**: `5b90f8cb-a424-4fc3-bd55-7618c8f46eae`
- **参数名**: `CsmAEADEncryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

######## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that encryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmAEADEncryptAlgorithmFamilyCustomRef

- **UUID**: `244798ad-9a03-4329-b748-ffeb3795f198`
- **引用名**: `CsmAEADEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `07bbe773-85ee-430c-a6cf-0ba28569450c`
- **引用名**: `CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmAEADEncryptAlgorithmModeCustomRef

- **UUID**: `6672736f-acb5-45f3-8543-bad534c95aa1`
- **引用名**: `CsmAEADEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmDecryptAlgorithmFamily

- **UUID**: `067a0b0b-2c36-4bfe-878a-41d63398b8d1`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmDecryptAlgorithmMode

- **UUID**: `eb16d648-67ff-41ec-a807-9f4be6617b52`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

############ 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `334ec12f-5d76-492d-a46e-f72d24b77abd`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Decrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Decrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Decrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmDecryptAlgorithmFamilyCustomRef

- **UUID**: `9f9a44fe-beb8-42c5-8282-c5ebcb9a3789`
- **引用名**: `CsmDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmDecryptAlgorithmModeCustomRef

- **UUID**: `2bd4ff85-fa12-4ae3-89f3-1849d6541d18`
- **引用名**: `CsmDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

############ 3. CsmDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `02bbe7f2-2865-47ed-8f06-495bc8a97175`
- **引用名**: `CsmDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmFamily

- **UUID**: `067a0b0b-2c36-4bfe-878a-41d63398b8d1`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmDecryptAlgorithmMode

- **UUID**: `eb16d648-67ff-41ec-a807-9f4be6617b52`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

########## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `334ec12f-5d76-492d-a46e-f72d24b77abd`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Decrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Decrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Decrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmDecryptAlgorithmFamilyCustomRef

- **UUID**: `9f9a44fe-beb8-42c5-8282-c5ebcb9a3789`
- **引用名**: `CsmDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmDecryptAlgorithmModeCustomRef

- **UUID**: `2bd4ff85-fa12-4ae3-89f3-1849d6541d18`
- **引用名**: `CsmDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `02bbe7f2-2865-47ed-8f06-495bc8a97175`
- **引用名**: `CsmDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmEncryptAlgorithmFamily

- **UUID**: `656ef405-9566-4a34-9d35-6afae928a038`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmEncryptAlgorithmMode

- **UUID**: `dad7391d-fc75-41b6-94bd-efbaa6fa0440`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `5e59f9c0-8b8b-47de-b252-7e226836b168`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Encrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Encrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Encrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmEncryptAlgorithmFamilyCustomRef

- **UUID**: `1e62dd7a-7b9c-47b9-a8d3-4619d857aa06`
- **引用名**: `CsmEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `73d7e641-c1cf-4521-aeee-bc0241627555`
- **引用名**: `CsmEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmEncryptAlgorithmModeCustomRef

- **UUID**: `3908c67f-45bf-488f-b9f3-c7f475ed3f99`
- **引用名**: `CsmEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmFamily

- **UUID**: `656ef405-9566-4a34-9d35-6afae928a038`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmEncryptAlgorithmMode

- **UUID**: `dad7391d-fc75-41b6-94bd-efbaa6fa0440`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `5e59f9c0-8b8b-47de-b252-7e226836b168`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Encrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Encrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Encrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmEncryptAlgorithmFamilyCustomRef

- **UUID**: `1e62dd7a-7b9c-47b9-a8d3-4619d857aa06`
- **引用名**: `CsmEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `73d7e641-c1cf-4521-aeee-bc0241627555`
- **引用名**: `CsmEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmEncryptAlgorithmModeCustomRef

- **UUID**: `3908c67f-45bf-488f-b9f3-c7f475ed3f99`
- **引用名**: `CsmEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmHashAlgorithmFamily

- **UUID**: `fbb012bd-de9b-4db2-b6df-486e8d2ecec2`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmHashAlgorithmMode

- **UUID**: `109868fb-feb6-4648-a2ca-a269419c2c26`
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

- **UUID**: `5715a7e8-fc20-4f4c-88a9-c5f36af4490a`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Hash: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface. Change resultLength type from uint32 to Csm_LengthPtr and direction form IN_OUT to IN of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Hash: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmHashAlgorithmFamilyCustomRef

- **UUID**: `bde78863-3f36-414a-981b-9735f9219144`
- **引用名**: `CsmHashAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmHashAlgorithmModeCustomRef

- **UUID**: `4fcdc09d-590d-43ec-bb33-ac1add47edbd`
- **引用名**: `CsmHashAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

############ 3. CsmHashAlgorithmSecondaryFamilyCustomRef

- **UUID**: `048a2538-3ebb-4593-b69e-0822e29a1cde`
- **引用名**: `CsmHashAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmFamily

- **UUID**: `fbb012bd-de9b-4db2-b6df-486e8d2ecec2`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmHashAlgorithmMode

- **UUID**: `109868fb-feb6-4648-a2ca-a269419c2c26`
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

- **UUID**: `5715a7e8-fc20-4f4c-88a9-c5f36af4490a`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Hash: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface. Change resultLength type from uint32 to Csm_LengthPtr and direction form IN_OUT to IN of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Hash: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmHashAlgorithmFamilyCustomRef

- **UUID**: `bde78863-3f36-414a-981b-9735f9219144`
- **引用名**: `CsmHashAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmHashAlgorithmModeCustomRef

- **UUID**: `4fcdc09d-590d-43ec-bb33-ac1add47edbd`
- **引用名**: `CsmHashAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmHashAlgorithmSecondaryFamilyCustomRef

- **UUID**: `048a2538-3ebb-4593-b69e-0822e29a1cde`
- **引用名**: `CsmHashAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `f15df24c-8bdc-4a66-bed0-4f162398e0ff`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmMacGenerateAlgorithmMode

- **UUID**: `c21f55d4-16cc-418f-babc-b792a1bda52c`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `ddc7afc3-a400-4a2b-aff7-d6c1cace3574`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY  were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmMacGenerateAlgorithmFamilyCustomRef

- **UUID**: `31a386eb-e49c-4a35-883f-b7e007dfb2ff`
- **引用名**: `CsmMacGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmMacGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `9a75d195-17b7-47f9-9e97-050307760fe7`
- **引用名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmMacGenerateAlgorithmModeCustomRef

- **UUID**: `a93d985e-4d9c-47fd-80ba-5e07cb415efd`
- **引用名**: `CsmMacGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `f15df24c-8bdc-4a66-bed0-4f162398e0ff`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `c21f55d4-16cc-418f-babc-b792a1bda52c`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `ddc7afc3-a400-4a2b-aff7-d6c1cace3574`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY  were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmMacGenerateAlgorithmFamilyCustomRef

- **UUID**: `31a386eb-e49c-4a35-883f-b7e007dfb2ff`
- **引用名**: `CsmMacGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmMacGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `9a75d195-17b7-47f9-9e97-050307760fe7`
- **引用名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmMacGenerateAlgorithmModeCustomRef

- **UUID**: `a93d985e-4d9c-47fd-80ba-5e07cb415efd`
- **引用名**: `CsmMacGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `acfccba0-40c4-4cb7-9af9-e897fafba1f0`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `145cfa03-f41d-40fe-82f6-649fdb84a6ed`
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

- **UUID**: `efd413e4-cfd7-4eac-9bec-ed129d19e591`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmMacVerifyAlgorithmFamilyCustomRef

- **UUID**: `3883d61b-afde-4f71-a463-22843de48281`
- **引用名**: `CsmMacVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmMacVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `57e2a69b-6e37-4846-817a-cdf527d29463`
- **引用名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmMacVerifyAlgorithmModeCustomRef

- **UUID**: `c452c1fa-4724-4604-9f79-bd2b49ad734b`
- **引用名**: `CsmMacVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `acfccba0-40c4-4cb7-9af9-e897fafba1f0`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `145cfa03-f41d-40fe-82f6-649fdb84a6ed`
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

- **UUID**: `efd413e4-cfd7-4eac-9bec-ed129d19e591`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmMacVerifyAlgorithmFamilyCustomRef

- **UUID**: `3883d61b-afde-4f71-a463-22843de48281`
- **引用名**: `CsmMacVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `57e2a69b-6e37-4846-817a-cdf527d29463`
- **引用名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmMacVerifyAlgorithmModeCustomRef

- **UUID**: `c452c1fa-4724-4604-9f79-bd2b49ad734b`
- **引用名**: `CsmMacVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **10** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `61442e13-e04d-42cc-80e2-a3b46bd8bb4d`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f6b6ffeb-4268-4593-a452-01e16ad01daa`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `69921ec6-36a4-435b-9eb8-9cc92b55a462`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
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

############ 6. CsmRandomGenerateSwcInterfaceVersion

- **UUID**: `19f780e3-ed5f-40e2-bfb6-337862fd5779`
- **参数名**: `CsmRandomGenerateSwcInterfaceVersion`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use VoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomGenerate: CSM_E_ENTROPY_EXHAUSTION was replaced by CRYPTO_E_ENTROPY_EXHAUSTED as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
RandomGenerate: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmRandomGenerateAlgorithmFamilyCustomRef

- **UUID**: `80c7cf25-19fe-42be-926d-69e6c8235d5b`
- **引用名**: `CsmRandomGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `16510492-95d8-4f95-806b-467e17c45bbf`
- **引用名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmRandomGenerateAlgorithmModeCustomRef

- **UUID**: `0e0b0404-92e8-48a9-b1c2-c0b80af78cf9`
- **引用名**: `CsmRandomGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **10** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `61442e13-e04d-42cc-80e2-a3b46bd8bb4d`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f6b6ffeb-4268-4593-a452-01e16ad01daa`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `69921ec6-36a4-435b-9eb8-9cc92b55a462`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
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

########## 6. CsmRandomGenerateSwcInterfaceVersion

- **UUID**: `19f780e3-ed5f-40e2-bfb6-337862fd5779`
- **参数名**: `CsmRandomGenerateSwcInterfaceVersion`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use VoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomGenerate: CSM_E_ENTROPY_EXHAUSTION was replaced by CRYPTO_E_ENTROPY_EXHAUSTED as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
RandomGenerate: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmRandomGenerateAlgorithmFamilyCustomRef

- **UUID**: `80c7cf25-19fe-42be-926d-69e6c8235d5b`
- **引用名**: `CsmRandomGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `16510492-95d8-4f95-806b-467e17c45bbf`
- **引用名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmRandomGenerateAlgorithmModeCustomRef

- **UUID**: `0e0b0404-92e8-48a9-b1c2-c0b80af78cf9`
- **引用名**: `CsmRandomGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `538fa491-38fe-45b9-8289-60ce79d5e4dd`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `1f3d9b63-29e2-4a9e-bb39-677d57795e61`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `15c0e759-a028-404b-988d-239b3fa56666`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmSignatureGenerateAlgorithmFamilyCustomRef

- **UUID**: `7ced7c6c-9420-4681-8777-e28ffe61ebfd`
- **引用名**: `CsmSignatureGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3786cedf-e80c-4ad5-96f8-837aab9be24c`
- **引用名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmSignatureGenerateAlgorithmModeCustomRef

- **UUID**: `a7c1abb3-bc2a-481e-b5eb-326d080c5e96`
- **引用名**: `CsmSignatureGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `538fa491-38fe-45b9-8289-60ce79d5e4dd`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `1f3d9b63-29e2-4a9e-bb39-677d57795e61`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `15c0e759-a028-404b-988d-239b3fa56666`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmSignatureGenerateAlgorithmFamilyCustomRef

- **UUID**: `7ced7c6c-9420-4681-8777-e28ffe61ebfd`
- **引用名**: `CsmSignatureGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3786cedf-e80c-4ad5-96f8-837aab9be24c`
- **引用名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmSignatureGenerateAlgorithmModeCustomRef

- **UUID**: `a7c1abb3-bc2a-481e-b5eb-326d080c5e96`
- **引用名**: `CsmSignatureGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `5c184fc5-9687-4d7a-a675-445f1b16670f`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `a780bc2e-c5da-4f0e-91da-b9fa05b5ce22`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `efc43a8e-adce-477b-93d5-65f6565d6e6e`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmSignatureVerifyAlgorithmFamilyCustomRef

- **UUID**: `d6c97e68-05ba-4edf-8c83-64913beb06ca`
- **引用名**: `CsmSignatureVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c681bd0e-3ef7-4959-b7e7-be853f8c2da9`
- **引用名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmSignatureVerifyAlgorithmModeCustomRef

- **UUID**: `36941c8d-16b6-4d58-bd1f-39400859a2ea`
- **引用名**: `CsmSignatureVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `5c184fc5-9687-4d7a-a675-445f1b16670f`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `a780bc2e-c5da-4f0e-91da-b9fa05b5ce22`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `efc43a8e-adce-477b-93d5-65f6565d6e6e`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmSignatureVerifyAlgorithmFamilyCustomRef

- **UUID**: `d6c97e68-05ba-4edf-8c83-64913beb06ca`
- **引用名**: `CsmSignatureVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c681bd0e-3ef7-4959-b7e7-be853f8c2da9`
- **引用名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmSignatureVerifyAlgorithmModeCustomRef

- **UUID**: `36941c8d-16b6-4d58-bd1f-39400859a2ea`
- **引用名**: `CsmSignatureVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

########## 参数配置

此容器包含 **4** 个参数：

########### ENUMERATION 类型参数

############ 1. CsmJobKeySetValidAlgorithmFamily

- **UUID**: `ed673cad-22d4-4668-855c-d61cd7403106`
- **参数名**: `CsmJobKeySetValidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeySetValidAlgorithmMode

- **UUID**: `b833e53c-0d81-4551-b1c8-55c7084c066f`
- **参数名**: `CsmJobKeySetValidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

############ 3. CsmJobKeySetValidAlgorithmSecondaryFamily

- **UUID**: `208f0cbe-7431-40ac-b44b-6a9e7a2604b9`
- **参数名**: `CsmJobKeySetValidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

############ 4. CsmJobKeySetValidSwcInterfaceVersion

- **UUID**: `e2b6e0e4-7a54-4e1b-8f36-116572865615`
- **参数名**: `CsmJobKeySetValidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetValid: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeySetValidAlgorithmFamilyCustomRef

- **UUID**: `2daa2d23-fb97-4bc8-a3c7-d42e57d3bebc`
- **引用名**: `CsmJobKeySetValidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeySetValidAlgorithmModeCustomRef

- **UUID**: `6ee204ae-e2d8-4604-9b06-c3914bb399a9`
- **引用名**: `CsmJobKeySetValidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

############ 3. CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4538005b-01b5-4031-ab49-6daa2df178de`
- **引用名**: `CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

####### 24. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmJobKeySetValidAlgorithmFamily

- **UUID**: `ed673cad-22d4-4668-855c-d61cd7403106`
- **参数名**: `CsmJobKeySetValidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeySetValidAlgorithmMode

- **UUID**: `b833e53c-0d81-4551-b1c8-55c7084c066f`
- **参数名**: `CsmJobKeySetValidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

########## 3. CsmJobKeySetValidAlgorithmSecondaryFamily

- **UUID**: `208f0cbe-7431-40ac-b44b-6a9e7a2604b9`
- **参数名**: `CsmJobKeySetValidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

########## 4. CsmJobKeySetValidSwcInterfaceVersion

- **UUID**: `e2b6e0e4-7a54-4e1b-8f36-116572865615`
- **参数名**: `CsmJobKeySetValidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetValid: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeySetValidAlgorithmFamilyCustomRef

- **UUID**: `2daa2d23-fb97-4bc8-a3c7-d42e57d3bebc`
- **引用名**: `CsmJobKeySetValidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeySetValidAlgorithmModeCustomRef

- **UUID**: `6ee204ae-e2d8-4604-9b06-c3914bb399a9`
- **引用名**: `CsmJobKeySetValidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4538005b-01b5-4031-ab49-6daa2df178de`
- **引用名**: `CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `e137a61d-936b-46e0-be72-269cdcd2b897`
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
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `6068cf87-5927-47c9-83c3-0961a316f1ce`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
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

############ 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `7494946f-8e19-43f6-ae42-1b8e4b5c5ce7`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

############ 5. CsmJobKeyExchangeCalcPubValSwcInterfaceVersion

- **UUID**: `4aa19e7d-2770-4409-b112-ff7c7614bac0`
- **参数名**: `CsmJobKeyExchangeCalcPubValSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcPubVal: Removal of key argument.

AUTOSAR R20-11:
KeyExchangeCalcPubVal: Changed type of publicValuePtr argument to VoidPtr resulting in just one interface for all jobs again.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcPubVal: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of publicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef

- **UUID**: `44b11427-e7c3-4cba-9230-677b3ce99a37`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef

- **UUID**: `be609eee-00c7-42e5-ac82-b758c7bd1777`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef

- **UUID**: `88cbcf59-6eeb-4d12-b6b3-b273b574d506`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `e137a61d-936b-46e0-be72-269cdcd2b897`
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
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `6068cf87-5927-47c9-83c3-0961a316f1ce`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
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

########## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `7494946f-8e19-43f6-ae42-1b8e4b5c5ce7`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyExchangeCalcPubValSwcInterfaceVersion

- **UUID**: `4aa19e7d-2770-4409-b112-ff7c7614bac0`
- **参数名**: `CsmJobKeyExchangeCalcPubValSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcPubVal: Removal of key argument.

AUTOSAR R20-11:
KeyExchangeCalcPubVal: Changed type of publicValuePtr argument to VoidPtr resulting in just one interface for all jobs again.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcPubVal: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of publicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef

- **UUID**: `44b11427-e7c3-4cba-9230-677b3ce99a37`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef

- **UUID**: `be609eee-00c7-42e5-ac82-b758c7bd1777`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef

- **UUID**: `88cbcf59-6eeb-4d12-b6b3-b273b574d506`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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

- **UUID**: `c2ea1921-3d7b-44f4-90df-5b0fc96edc5e`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `7ccbe3ec-788b-4b8f-b983-edbf7021273f`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `d170acc7-4d54-4878-9864-82c4dc55a10c`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
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

############ 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `59a614ad-bbe1-4e64-a002-402c09dfbd14`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

############ 5. CsmJobKeyExchangeCalcSecretSwcInterfaceVersion

- **UUID**: `1eff66c3-f0e0-4f6c-8d45-dd6510d14173`
- **参数名**: `CsmJobKeyExchangeCalcSecretSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11_A` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above
CSM_ASR_VERSION_R21_11_A: Interface adheres to AUTOSAR R21-11 with some changes (see detailled description below)

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcSecret: Removal of key argument.
CSM_ASR_VERSION_R21_11_A: This variant provides an alternative version of the interface using VoidPtr as type for the publicValuePtr argument resulting in just one interface for all jobs again. This is provided as all other primitives were changed to VoidPtr in R20 but this primitive which might be a mistake in AUTOSAR.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcSecret: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of partnerPublicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became Job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef

- **UUID**: `7e970ce2-29f5-402e-aba9-b54beb6af571`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef

- **UUID**: `564e3a23-64c0-41fe-bb58-69d6df67f632`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef

- **UUID**: `af185df5-c417-4922-a001-99c628e0b8aa`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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

- **UUID**: `c2ea1921-3d7b-44f4-90df-5b0fc96edc5e`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `7ccbe3ec-788b-4b8f-b983-edbf7021273f`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `d170acc7-4d54-4878-9864-82c4dc55a10c`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
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

########## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `59a614ad-bbe1-4e64-a002-402c09dfbd14`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyExchangeCalcSecretSwcInterfaceVersion

- **UUID**: `1eff66c3-f0e0-4f6c-8d45-dd6510d14173`
- **参数名**: `CsmJobKeyExchangeCalcSecretSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11_A` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above
CSM_ASR_VERSION_R21_11_A: Interface adheres to AUTOSAR R21-11 with some changes (see detailled description below)

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcSecret: Removal of key argument.
CSM_ASR_VERSION_R21_11_A: This variant provides an alternative version of the interface using VoidPtr as type for the publicValuePtr argument resulting in just one interface for all jobs again. This is provided as all other primitives were changed to VoidPtr in R20 but this primitive which might be a mistake in AUTOSAR.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcSecret: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of partnerPublicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became Job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef

- **UUID**: `7e970ce2-29f5-402e-aba9-b54beb6af571`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef

- **UUID**: `564e3a23-64c0-41fe-bb58-69d6df67f632`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef

- **UUID**: `af185df5-c417-4922-a001-99c628e0b8aa`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `705b1e3e-3dd0-4180-ac3d-7b9e34d1c81a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
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

############ 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `3f583317-6ff9-4777-b17c-85f21394c53a`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `3824e56d-cd86-4db2-a6ab-1e6b355f452c`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

############ 5. CsmJobKeyDeriveSwcInterfaceVersion

- **UUID**: `221f2273-a738-41b8-8a25-b015395e11d2`
- **参数名**: `CsmJobKeyDeriveSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyDerive: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeyDeriveAlgorithmFamilyCustomRef

- **UUID**: `ccdd442d-de9d-46ec-bff4-237468c55114`
- **引用名**: `CsmJobKeyDeriveAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3e9f0ec0-0ac4-41cb-ad6f-af0bfaff00e6`
- **引用名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmJobKeyDeriveAlgorithmModeCustomRef

- **UUID**: `f4c8b7e5-4b17-4438-8c38-1ee6be0c0f28`
- **引用名**: `CsmJobKeyDeriveAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `705b1e3e-3dd0-4180-ac3d-7b9e34d1c81a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
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

########## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `3f583317-6ff9-4777-b17c-85f21394c53a`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `3824e56d-cd86-4db2-a6ab-1e6b355f452c`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyDeriveSwcInterfaceVersion

- **UUID**: `221f2273-a738-41b8-8a25-b015395e11d2`
- **参数名**: `CsmJobKeyDeriveSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyDerive: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyDeriveAlgorithmFamilyCustomRef

- **UUID**: `ccdd442d-de9d-46ec-bff4-237468c55114`
- **引用名**: `CsmJobKeyDeriveAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3e9f0ec0-0ac4-41cb-ad6f-af0bfaff00e6`
- **引用名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyDeriveAlgorithmModeCustomRef

- **UUID**: `f4c8b7e5-4b17-4438-8c38-1ee6be0c0f28`
- **引用名**: `CsmJobKeyDeriveAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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

- **UUID**: `361efddb-8ac0-4b56-9bdd-37baa251920d`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `07734932-e17c-4be0-85a1-df5773761f58`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

############ 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `569097f7-9f43-42fe-a38b-d35a245d60ca`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.
Backward compatibility to R19-11. Use CsmJobRandomSeedAlgorithmFamily instead.

############ 4. CsmJobRandomSeedAlgorithmFamily

- **UUID**: `88cf73da-37bc-43cd-97ad-edca04902dd1`
- **参数名**: `CsmJobRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_DRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_FIPS186` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 5. CsmJobRandomSeedSwcInterfaceVersion

- **UUID**: `09a39b83-8dc1-46d5-a3f1-ce74f31557c8`
- **参数名**: `CsmJobRandomSeedSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomSeed: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobRandomSeedAlgorithmFamilyCustomRef

- **UUID**: `b725033b-d47b-43f4-aedb-a99be63bbfdd`
- **引用名**: `CsmJobRandomSeedAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef

- **UUID**: `bc3ba5aa-ca20-4ec7-be71-cf2afad634e1`
- **引用名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmJobRandomSeedAlgorithmModeCustomRef

- **UUID**: `57f10df5-f6f9-4e9e-88f4-9fb0a74b5abe`
- **引用名**: `CsmJobRandomSeedAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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

- **UUID**: `361efddb-8ac0-4b56-9bdd-37baa251920d`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `07734932-e17c-4be0-85a1-df5773761f58`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `569097f7-9f43-42fe-a38b-d35a245d60ca`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.
Backward compatibility to R19-11. Use CsmJobRandomSeedAlgorithmFamily instead.

########## 4. CsmJobRandomSeedAlgorithmFamily

- **UUID**: `88cf73da-37bc-43cd-97ad-edca04902dd1`
- **参数名**: `CsmJobRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_DRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_FIPS186` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 5. CsmJobRandomSeedSwcInterfaceVersion

- **UUID**: `09a39b83-8dc1-46d5-a3f1-ce74f31557c8`
- **参数名**: `CsmJobRandomSeedSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomSeed: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobRandomSeedAlgorithmFamilyCustomRef

- **UUID**: `b725033b-d47b-43f4-aedb-a99be63bbfdd`
- **引用名**: `CsmJobRandomSeedAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef

- **UUID**: `bc3ba5aa-ca20-4ec7-be71-cf2afad634e1`
- **引用名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobRandomSeedAlgorithmModeCustomRef

- **UUID**: `57f10df5-f6f9-4e9e-88f4-9fb0a74b5abe`
- **引用名**: `CsmJobRandomSeedAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `5365712e-e3de-4ca3-ba79-b6f767678608`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `172a7064-caca-4fbb-b1ea-06d7b60325d1`
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

- **UUID**: `f2a4d424-64cf-4d94-ad8d-6167569f0c84`
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

############ 5. CsmJobKeyGenerateSwcInterfaceVersion

- **UUID**: `91523466-05d1-45e2-8b0a-569d06191c59`
- **参数名**: `CsmJobKeyGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyGenerate: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyGenerate: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeyGenerateAlgorithmFamilyCustomRef

- **UUID**: `78a6eb7f-560e-4e6e-b15f-bd2e98577bf0`
- **引用名**: `CsmJobKeyGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c587de11-9e9f-4ecf-a536-bbed44d9234c`
- **引用名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

############ 3. CsmJobKeyGenerateAlgorithmModeCustomRef

- **UUID**: `355daa76-f017-4c13-8207-71d4f1f091c3`
- **引用名**: `CsmJobKeyGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `5365712e-e3de-4ca3-ba79-b6f767678608`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `172a7064-caca-4fbb-b1ea-06d7b60325d1`
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

- **UUID**: `f2a4d424-64cf-4d94-ad8d-6167569f0c84`
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

########## 5. CsmJobKeyGenerateSwcInterfaceVersion

- **UUID**: `91523466-05d1-45e2-8b0a-569d06191c59`
- **参数名**: `CsmJobKeyGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyGenerate: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyGenerate: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyGenerateAlgorithmFamilyCustomRef

- **UUID**: `78a6eb7f-560e-4e6e-b15f-bd2e98577bf0`
- **引用名**: `CsmJobKeyGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c587de11-9e9f-4ecf-a536-bbed44d9234c`
- **引用名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyGenerateAlgorithmModeCustomRef

- **UUID**: `355daa76-f017-4c13-8207-71d4f1f091c3`
- **引用名**: `CsmJobKeyGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

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
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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

Configurations of CertificateVerify primitives

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
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
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

############ 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
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
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
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

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
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

####### 39. CsmJobKeySetInvalid

**容器属性**:

- **UUID**: `344050ac-e162-48be-8e2d-2f7f58519e84`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalid`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeySetInvalid primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmJobKeySetInvalidConfig

**容器属性**:

- **UUID**: `5590b0b9-4afe-4384-9b56-1c87427978b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set invalid operation.

########## 参数配置

此容器包含 **4** 个参数：

########### ENUMERATION 类型参数

############ 1. CsmJobKeySetInvalidAlgorithmFamily

- **UUID**: `0531a385-e7e7-4608-b8a1-4fe9cd5c8526`
- **参数名**: `CsmJobKeySetInvalidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmJobKeySetInvalidAlgorithmMode

- **UUID**: `f12d993c-da30-4176-9fc5-f38a3fc6cdd7`
- **参数名**: `CsmJobKeySetInvalidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

############ 3. CsmJobKeySetInvalidAlgorithmSecondaryFamily

- **UUID**: `4e1e7bee-7f09-4dcf-87fa-15007e0c3b75`
- **参数名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

############ 4. CsmJobKeySetInvalidSwcInterfaceVersion

- **UUID**: `5028b042-85a3-4fec-811f-88f7711e4c1b`
- **参数名**: `CsmJobKeySetInvalidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetInvalid: Removal of key argument.

AUTOSAR R20-11:
Introduction of this primitive

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CsmJobKeySetInvalidAlgorithmFamilyCustomRef

- **UUID**: `3d23e8b9-c2b5-48d5-8bce-746b5d4fbd7e`
- **引用名**: `CsmJobKeySetInvalidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

############ 2. CsmJobKeySetInvalidAlgorithmModeCustomRef

- **UUID**: `e3a9233c-13b0-45fe-90d2-1d058bbfeb43`
- **引用名**: `CsmJobKeySetInvalidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

############ 3. CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4036bfca-5fe5-40b2-ab5c-135c6c95333d`
- **引用名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

####### 40. CsmJobKeySetInvalidConfig

**容器属性**:

- **UUID**: `5590b0b9-4afe-4384-9b56-1c87427978b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set invalid operation.

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmJobKeySetInvalidAlgorithmFamily

- **UUID**: `0531a385-e7e7-4608-b8a1-4fe9cd5c8526`
- **参数名**: `CsmJobKeySetInvalidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeySetInvalidAlgorithmMode

- **UUID**: `f12d993c-da30-4176-9fc5-f38a3fc6cdd7`
- **参数名**: `CsmJobKeySetInvalidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

########## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamily

- **UUID**: `4e1e7bee-7f09-4dcf-87fa-15007e0c3b75`
- **参数名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

########## 4. CsmJobKeySetInvalidSwcInterfaceVersion

- **UUID**: `5028b042-85a3-4fec-811f-88f7711e4c1b`
- **参数名**: `CsmJobKeySetInvalidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetInvalid: Removal of key argument.

AUTOSAR R20-11:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeySetInvalidAlgorithmFamilyCustomRef

- **UUID**: `3d23e8b9-c2b5-48d5-8bce-746b5d4fbd7e`
- **引用名**: `CsmJobKeySetInvalidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeySetInvalidAlgorithmModeCustomRef

- **UUID**: `e3a9233c-13b0-45fe-90d2-1d058bbfeb43`
- **引用名**: `CsmJobKeySetInvalidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4036bfca-5fe5-40b2-ab5c-135c6c95333d`
- **引用名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 12. CsmAEADDecrypt

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

此容器包含 **13** 个参数：

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

- **UUID**: `5b5f5064-26da-445b-a342-972b74f55a6c`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `5c2bf479-1ec2-431e-ac84-3100a0010fe9`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `f7de62ed-eeb5-46a1-914e-1b955e234a72`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADDecrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADDecrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADDecrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 6. CsmAEADDecryptAlgorithmSecondaryFamily

- **UUID**: `244aaabd-1f92-4582-882f-464a29d695c8`
- **参数名**: `CsmAEADDecryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

######## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that decryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmAEADDecryptAlgorithmFamilyCustomRef

- **UUID**: `b105dc08-b071-47eb-bf6d-9d91ee548fe8`
- **引用名**: `CsmAEADDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `28d72189-656f-4722-be6f-4a8758272ea4`
- **引用名**: `CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmAEADDecryptAlgorithmModeCustomRef

- **UUID**: `1e9402fb-e3c0-44bd-9566-af67865cdf08`
- **引用名**: `CsmAEADDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 13. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `16c65ae5-43de-4174-a48f-4ab5956b8cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

###### 参数配置

此容器包含 **13** 个参数：

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

- **UUID**: `5b5f5064-26da-445b-a342-972b74f55a6c`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADDecryptAlgorithmFamily

- **UUID**: `5c2bf479-1ec2-431e-ac84-3100a0010fe9`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmAEADDecryptAlgorithmMode

- **UUID**: `f7de62ed-eeb5-46a1-914e-1b955e234a72`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADDecrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADDecrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADDecrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 6. CsmAEADDecryptAlgorithmSecondaryFamily

- **UUID**: `244aaabd-1f92-4582-882f-464a29d695c8`
- **参数名**: `CsmAEADDecryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

###### 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that decryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmAEADDecryptAlgorithmFamilyCustomRef

- **UUID**: `b105dc08-b071-47eb-bf6d-9d91ee548fe8`
- **引用名**: `CsmAEADDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `28d72189-656f-4722-be6f-4a8758272ea4`
- **引用名**: `CsmAEADDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmAEADDecryptAlgorithmModeCustomRef

- **UUID**: `1e9402fb-e3c0-44bd-9566-af67865cdf08`
- **引用名**: `CsmAEADDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 14. CsmAEADEncrypt

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

此容器包含 **13** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `d7ccdc02-2258-4122-94a7-ea3468ef8a82`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c61a45e5-063a-4701-8e6b-518102fd4ede`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADEncrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADEncrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADEncrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

########## 6. CsmAEADEncryptAlgorithmSecondaryFamily

- **UUID**: `5b90f8cb-a424-4fc3-bd55-7618c8f46eae`
- **参数名**: `CsmAEADEncryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

######## 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that encryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmAEADEncryptAlgorithmFamilyCustomRef

- **UUID**: `244798ad-9a03-4329-b748-ffeb3795f198`
- **引用名**: `CsmAEADEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `07bbe773-85ee-430c-a6cf-0ba28569450c`
- **引用名**: `CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmAEADEncryptAlgorithmModeCustomRef

- **UUID**: `6672736f-acb5-45f3-8543-bad534c95aa1`
- **引用名**: `CsmAEADEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 15. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `54b685a3-6832-4bf2-9563-eec537185b81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

###### 参数配置

此容器包含 **13** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADEncryptAlgorithmFamily

- **UUID**: `d7ccdc02-2258-4122-94a7-ea3468ef8a82`
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
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmAEADEncryptAlgorithmMode

- **UUID**: `c61a45e5-063a-4701-8e6b-518102fd4ede`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
AEADEncrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
AEADEncrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
AEADEncrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 6. CsmAEADEncryptAlgorithmSecondaryFamily

- **UUID**: `5b90f8cb-a424-4fc3-bd55-7618c8f46eae`
- **参数名**: `CsmAEADEncryptAlgorithmSecondaryFamily`
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
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
- **描述**: Defines the secondary family used for the crypto service

###### 引用关系

此容器包含 **5** 个引用：

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
- **描述**: Not used and not supported.
According to AUTOSAR, this is a mandatory parameter which refers to the key used for that encryption primitive. As primitive and key are coupled by a CsmJob, this parameter has no function. So, simply configure a dummy key.

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

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmAEADEncryptAlgorithmFamilyCustomRef

- **UUID**: `244798ad-9a03-4329-b748-ffeb3795f198`
- **引用名**: `CsmAEADEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `07bbe773-85ee-430c-a6cf-0ba28569450c`
- **引用名**: `CsmAEADEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmAEADEncryptAlgorithmModeCustomRef

- **UUID**: `6672736f-acb5-45f3-8543-bad534c95aa1`
- **引用名**: `CsmAEADEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 16. CsmDecrypt

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmFamily

- **UUID**: `067a0b0b-2c36-4bfe-878a-41d63398b8d1`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmDecryptAlgorithmMode

- **UUID**: `eb16d648-67ff-41ec-a807-9f4be6617b52`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

########## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `334ec12f-5d76-492d-a46e-f72d24b77abd`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Decrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Decrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Decrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmDecryptAlgorithmFamilyCustomRef

- **UUID**: `9f9a44fe-beb8-42c5-8282-c5ebcb9a3789`
- **引用名**: `CsmDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmDecryptAlgorithmModeCustomRef

- **UUID**: `2bd4ff85-fa12-4ae3-89f3-1849d6541d18`
- **引用名**: `CsmDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `02bbe7f2-2865-47ed-8f06-495bc8a97175`
- **引用名**: `CsmDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 17. CsmDecryptConfig

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmDecryptAlgorithmFamily

- **UUID**: `067a0b0b-2c36-4bfe-878a-41d63398b8d1`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmDecryptAlgorithmMode

- **UUID**: `eb16d648-67ff-41ec-a807-9f4be6617b52`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

######## 4. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `334ec12f-5d76-492d-a46e-f72d24b77abd`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Decrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Decrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Decrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmDecryptAlgorithmFamilyCustomRef

- **UUID**: `9f9a44fe-beb8-42c5-8282-c5ebcb9a3789`
- **引用名**: `CsmDecryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmDecryptAlgorithmModeCustomRef

- **UUID**: `2bd4ff85-fa12-4ae3-89f3-1849d6541d18`
- **引用名**: `CsmDecryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

######## 3. CsmDecryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `02bbe7f2-2865-47ed-8f06-495bc8a97175`
- **引用名**: `CsmDecryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 18. CsmEncrypt

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmFamily

- **UUID**: `656ef405-9566-4a34-9d35-6afae928a038`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmEncryptAlgorithmMode

- **UUID**: `dad7391d-fc75-41b6-94bd-efbaa6fa0440`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `5e59f9c0-8b8b-47de-b252-7e226836b168`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Encrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Encrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Encrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmEncryptAlgorithmFamilyCustomRef

- **UUID**: `1e62dd7a-7b9c-47b9-a8d3-4619d857aa06`
- **引用名**: `CsmEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `73d7e641-c1cf-4521-aeee-bc0241627555`
- **引用名**: `CsmEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmEncryptAlgorithmModeCustomRef

- **UUID**: `3908c67f-45bf-488f-b9f3-c7f475ed3f99`
- **引用名**: `CsmEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 19. CsmEncryptConfig

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECIES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmEncryptAlgorithmFamily

- **UUID**: `656ef405-9566-4a34-9d35-6afae928a038`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmEncryptAlgorithmMode

- **UUID**: `dad7391d-fc75-41b6-94bd-efbaa6fa0440`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `5e59f9c0-8b8b-47de-b252-7e226836b168`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Encrypt: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Encrypt: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
Encrypt: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmEncryptAlgorithmFamilyCustomRef

- **UUID**: `1e62dd7a-7b9c-47b9-a8d3-4619d857aa06`
- **引用名**: `CsmEncryptAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmEncryptAlgorithmSecondaryFamilyCustomRef

- **UUID**: `73d7e641-c1cf-4521-aeee-bc0241627555`
- **引用名**: `CsmEncryptAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmEncryptAlgorithmModeCustomRef

- **UUID**: `3908c67f-45bf-488f-b9f3-c7f475ed3f99`
- **引用名**: `CsmEncryptAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 20. CsmHash

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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmFamily

- **UUID**: `fbb012bd-de9b-4db2-b6df-486e8d2ecec2`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmHashAlgorithmMode

- **UUID**: `109868fb-feb6-4648-a2ca-a269419c2c26`
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

- **UUID**: `5715a7e8-fc20-4f4c-88a9-c5f36af4490a`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Hash: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface. Change resultLength type from uint32 to Csm_LengthPtr and direction form IN_OUT to IN of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Hash: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmHashAlgorithmFamilyCustomRef

- **UUID**: `bde78863-3f36-414a-981b-9735f9219144`
- **引用名**: `CsmHashAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmHashAlgorithmModeCustomRef

- **UUID**: `4fcdc09d-590d-43ec-bb33-ac1add47edbd`
- **引用名**: `CsmHashAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmHashAlgorithmSecondaryFamilyCustomRef

- **UUID**: `048a2538-3ebb-4593-b69e-0822e29a1cde`
- **引用名**: `CsmHashAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 21. CsmHashConfig

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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmHashAlgorithmFamily

- **UUID**: `fbb012bd-de9b-4db2-b6df-486e8d2ecec2`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmHashAlgorithmMode

- **UUID**: `109868fb-feb6-4648-a2ca-a269419c2c26`
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

- **UUID**: `5715a7e8-fc20-4f4c-88a9-c5f36af4490a`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
Hash: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface. Change resultLength type from uint32 to Csm_LengthPtr and direction form IN_OUT to IN of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
Hash: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmHashAlgorithmFamilyCustomRef

- **UUID**: `bde78863-3f36-414a-981b-9735f9219144`
- **引用名**: `CsmHashAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmHashAlgorithmModeCustomRef

- **UUID**: `4fcdc09d-590d-43ec-bb33-ac1add47edbd`
- **引用名**: `CsmHashAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

######## 3. CsmHashAlgorithmSecondaryFamilyCustomRef

- **UUID**: `048a2538-3ebb-4593-b69e-0822e29a1cde`
- **引用名**: `CsmHashAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 22. CsmMacGenerate

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `f15df24c-8bdc-4a66-bed0-4f162398e0ff`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `c21f55d4-16cc-418f-babc-b792a1bda52c`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `ddc7afc3-a400-4a2b-aff7-d6c1cace3574`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY  were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmMacGenerateAlgorithmFamilyCustomRef

- **UUID**: `31a386eb-e49c-4a35-883f-b7e007dfb2ff`
- **引用名**: `CsmMacGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmMacGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `9a75d195-17b7-47f9-9e97-050307760fe7`
- **引用名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmMacGenerateAlgorithmModeCustomRef

- **UUID**: `a93d985e-4d9c-47fd-80ba-5e07cb415efd`
- **引用名**: `CsmMacGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 23. CsmMacGenerateConfig

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacGenerateAlgorithmFamily

- **UUID**: `f15df24c-8bdc-4a66-bed0-4f162398e0ff`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmMacGenerateAlgorithmMode

- **UUID**: `c21f55d4-16cc-418f-babc-b792a1bda52c`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `ddc7afc3-a400-4a2b-aff7-d6c1cace3574`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY  were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmMacGenerateAlgorithmFamilyCustomRef

- **UUID**: `31a386eb-e49c-4a35-883f-b7e007dfb2ff`
- **引用名**: `CsmMacGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmMacGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `9a75d195-17b7-47f9-9e97-050307760fe7`
- **引用名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmMacGenerateAlgorithmModeCustomRef

- **UUID**: `a93d985e-4d9c-47fd-80ba-5e07cb415efd`
- **引用名**: `CsmMacGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 24. CsmMacVerify

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `acfccba0-40c4-4cb7-9af9-e897fafba1f0`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `145cfa03-f41d-40fe-82f6-649fdb84a6ed`
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

- **UUID**: `efd413e4-cfd7-4eac-9bec-ed129d19e591`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmMacVerifyAlgorithmFamilyCustomRef

- **UUID**: `3883d61b-afde-4f71-a463-22843de48281`
- **引用名**: `CsmMacVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `57e2a69b-6e37-4846-817a-cdf527d29463`
- **引用名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmMacVerifyAlgorithmModeCustomRef

- **UUID**: `c452c1fa-4724-4604-9f79-bd2b49ad734b`
- **引用名**: `CsmMacVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 25. CsmMacVerifyConfig

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacVerifyAlgorithmFamily

- **UUID**: `acfccba0-40c4-4cb7-9af9-e897fafba1f0`
- **参数名**: `CsmMacVerifyAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EIA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_POLY1305` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SIPHASH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `145cfa03-f41d-40fe-82f6-649fdb84a6ed`
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

- **UUID**: `efd413e4-cfd7-4eac-9bec-ed129d19e591`
- **参数名**: `CsmMacVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
MacVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
MacVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmMacVerifyAlgorithmFamilyCustomRef

- **UUID**: `3883d61b-afde-4f71-a463-22843de48281`
- **引用名**: `CsmMacVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `57e2a69b-6e37-4846-817a-cdf527d29463`
- **引用名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmMacVerifyAlgorithmModeCustomRef

- **UUID**: `c452c1fa-4724-4604-9f79-bd2b49ad734b`
- **引用名**: `CsmMacVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 26. CsmRandomGenerate

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

此容器包含 **10** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `61442e13-e04d-42cc-80e2-a3b46bd8bb4d`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f6b6ffeb-4268-4593-a452-01e16ad01daa`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `69921ec6-36a4-435b-9eb8-9cc92b55a462`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
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

########## 6. CsmRandomGenerateSwcInterfaceVersion

- **UUID**: `19f780e3-ed5f-40e2-bfb6-337862fd5779`
- **参数名**: `CsmRandomGenerateSwcInterfaceVersion`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use VoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomGenerate: CSM_E_ENTROPY_EXHAUSTION was replaced by CRYPTO_E_ENTROPY_EXHAUSTED as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
RandomGenerate: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmRandomGenerateAlgorithmFamilyCustomRef

- **UUID**: `80c7cf25-19fe-42be-926d-69e6c8235d5b`
- **引用名**: `CsmRandomGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `16510492-95d8-4f95-806b-467e17c45bbf`
- **引用名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmRandomGenerateAlgorithmModeCustomRef

- **UUID**: `0e0b0404-92e8-48a9-b1c2-c0b80af78cf9`
- **引用名**: `CsmRandomGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 27. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `5729fbf0-2ba4-4d84-b9b8-a87c57a86115`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

###### 参数配置

此容器包含 **10** 个参数：

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
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_1_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_BLAKE_2s_512` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CHACHA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmRandomGenerateAlgorithmFamily

- **UUID**: `61442e13-e04d-42cc-80e2-a3b46bd8bb4d`
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
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmRandomGenerateAlgorithmMode

- **UUID**: `f6b6ffeb-4268-4593-a452-01e16ad01daa`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `69921ec6-36a4-435b-9eb8-9cc92b55a462`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
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

######## 6. CsmRandomGenerateSwcInterfaceVersion

- **UUID**: `19f780e3-ed5f-40e2-bfb6-337862fd5779`
- **参数名**: `CsmRandomGenerateSwcInterfaceVersion`
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
MacVerify: Use VoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomGenerate: CSM_E_ENTROPY_EXHAUSTION was replaced by CRYPTO_E_ENTROPY_EXHAUSTED as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
RandomGenerate: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmRandomGenerateAlgorithmFamilyCustomRef

- **UUID**: `80c7cf25-19fe-42be-926d-69e6c8235d5b`
- **引用名**: `CsmRandomGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `16510492-95d8-4f95-806b-467e17c45bbf`
- **引用名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmRandomGenerateAlgorithmModeCustomRef

- **UUID**: `0e0b0404-92e8-48a9-b1c2-c0b80af78cf9`
- **引用名**: `CsmRandomGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 28. CsmSecureCounter

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

##### 29. CsmSecureCounterConfig

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

##### 30. CsmSignatureGenerate

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `538fa491-38fe-45b9-8289-60ce79d5e4dd`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `1f3d9b63-29e2-4a9e-bb39-677d57795e61`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `15c0e759-a028-404b-988d-239b3fa56666`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmSignatureGenerateAlgorithmFamilyCustomRef

- **UUID**: `7ced7c6c-9420-4681-8777-e28ffe61ebfd`
- **引用名**: `CsmSignatureGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3786cedf-e80c-4ad5-96f8-837aab9be24c`
- **引用名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmSignatureGenerateAlgorithmModeCustomRef

- **UUID**: `a7c1abb3-bc2a-481e-b5eb-326d080c5e96`
- **引用名**: `CsmSignatureGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 31. CsmSignatureGenerateConfig

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureGenerateAlgorithmFamily

- **UUID**: `538fa491-38fe-45b9-8289-60ce79d5e4dd`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmSignatureGenerateAlgorithmMode

- **UUID**: `1f3d9b63-29e2-4a9e-bb39-677d57795e61`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `15c0e759-a028-404b-988d-239b3fa56666`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureGenerate: Use VoidPtr and ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureGenerate: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureGenerate: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmSignatureGenerateAlgorithmFamilyCustomRef

- **UUID**: `7ced7c6c-9420-4681-8777-e28ffe61ebfd`
- **引用名**: `CsmSignatureGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3786cedf-e80c-4ad5-96f8-837aab9be24c`
- **引用名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmSignatureGenerateAlgorithmModeCustomRef

- **UUID**: `a7c1abb3-bc2a-481e-b5eb-326d080c5e96`
- **引用名**: `CsmSignatureGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 32. CsmSignatureVerify

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `5c184fc5-9687-4d7a-a675-445f1b16670f`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `a780bc2e-c5da-4f0e-91da-b9fa05b5ce22`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `efc43a8e-adce-477b-93d5-65f6565d6e6e`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmSignatureVerifyAlgorithmFamilyCustomRef

- **UUID**: `d6c97e68-05ba-4edf-8c83-64913beb06ca`
- **引用名**: `CsmSignatureVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c681bd0e-3ef7-4959-b7e7-be853f8c2da9`
- **引用名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmSignatureVerifyAlgorithmModeCustomRef

- **UUID**: `36941c8d-16b6-4d58-bd1f-39400859a2ea`
- **引用名**: `CsmSignatureVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 33. CsmSignatureVerifyConfig

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
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureVerifyAlgorithmFamily

- **UUID**: `5c184fc5-9687-4d7a-a675-445f1b16670f`
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
  - `CRYPTO_ALGOFAM_ECDSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM2` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmSignatureVerifyAlgorithmMode

- **UUID**: `a780bc2e-c5da-4f0e-91da-b9fa05b5ce22`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
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
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `efc43a8e-adce-477b-93d5-65f6565d6e6e`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
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
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_03: Interface adheres to AUTOSAR 4.3.x specification
CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R20-11:
SignatureVerify: Use ConstVoidPtr instead of Csm_DataPtr (uint8) as type for data pointers of data reference interface

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
SignatureVerify: CSM_E_SMALL_BUFFER was removed as error code.
CancelJob: API was removed from the primitive based interface using arrays as arguments (CRYPTO_USE_PORT)

AUTOSAR 4.4.0:
SignatureVerify: CSM_E_KEY_NOT_VALID, CSM_E_KEY_SIZE_MISMATCH and CSM_E_KEY_EMPTY were added as error code.
CancelJob: CSM_E_JOB_CANCELED was added as error code.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmSignatureVerifyAlgorithmFamilyCustomRef

- **UUID**: `d6c97e68-05ba-4edf-8c83-64913beb06ca`
- **引用名**: `CsmSignatureVerifyAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c681bd0e-3ef7-4959-b7e7-be853f8c2da9`
- **引用名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmSignatureVerifyAlgorithmModeCustomRef

- **UUID**: `36941c8d-16b6-4d58-bd1f-39400859a2ea`
- **引用名**: `CsmSignatureVerifyAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 34. CsmJobKeySetValid

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

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmJobKeySetValidAlgorithmFamily

- **UUID**: `ed673cad-22d4-4668-855c-d61cd7403106`
- **参数名**: `CsmJobKeySetValidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeySetValidAlgorithmMode

- **UUID**: `b833e53c-0d81-4551-b1c8-55c7084c066f`
- **参数名**: `CsmJobKeySetValidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

########## 3. CsmJobKeySetValidAlgorithmSecondaryFamily

- **UUID**: `208f0cbe-7431-40ac-b44b-6a9e7a2604b9`
- **参数名**: `CsmJobKeySetValidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

########## 4. CsmJobKeySetValidSwcInterfaceVersion

- **UUID**: `e2b6e0e4-7a54-4e1b-8f36-116572865615`
- **参数名**: `CsmJobKeySetValidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetValid: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeySetValidAlgorithmFamilyCustomRef

- **UUID**: `2daa2d23-fb97-4bc8-a3c7-d42e57d3bebc`
- **引用名**: `CsmJobKeySetValidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeySetValidAlgorithmModeCustomRef

- **UUID**: `6ee204ae-e2d8-4604-9b06-c3914bb399a9`
- **引用名**: `CsmJobKeySetValidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4538005b-01b5-4031-ab49-6daa2df178de`
- **引用名**: `CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 35. CsmJobKeySetValidConfig

**容器属性**:

- **UUID**: `726bcb44-722c-46d9-93fe-337a18cea189`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetValidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set valid operation. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. CsmJobKeySetValidAlgorithmFamily

- **UUID**: `ed673cad-22d4-4668-855c-d61cd7403106`
- **参数名**: `CsmJobKeySetValidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeySetValidAlgorithmMode

- **UUID**: `b833e53c-0d81-4551-b1c8-55c7084c066f`
- **参数名**: `CsmJobKeySetValidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

######## 3. CsmJobKeySetValidAlgorithmSecondaryFamily

- **UUID**: `208f0cbe-7431-40ac-b44b-6a9e7a2604b9`
- **参数名**: `CsmJobKeySetValidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

######## 4. CsmJobKeySetValidSwcInterfaceVersion

- **UUID**: `e2b6e0e4-7a54-4e1b-8f36-116572865615`
- **参数名**: `CsmJobKeySetValidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetValid: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeySetValidAlgorithmFamilyCustomRef

- **UUID**: `2daa2d23-fb97-4bc8-a3c7-d42e57d3bebc`
- **引用名**: `CsmJobKeySetValidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeySetValidAlgorithmModeCustomRef

- **UUID**: `6ee204ae-e2d8-4604-9b06-c3914bb399a9`
- **引用名**: `CsmJobKeySetValidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

######## 3. CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4538005b-01b5-4031-ab49-6daa2df178de`
- **引用名**: `CsmJobKeySetValidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 36. CsmJobKeyExchangeCalcPubVal

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `e137a61d-936b-46e0-be72-269cdcd2b897`
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
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `6068cf87-5927-47c9-83c3-0961a316f1ce`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
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

########## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `7494946f-8e19-43f6-ae42-1b8e4b5c5ce7`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyExchangeCalcPubValSwcInterfaceVersion

- **UUID**: `4aa19e7d-2770-4409-b112-ff7c7614bac0`
- **参数名**: `CsmJobKeyExchangeCalcPubValSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcPubVal: Removal of key argument.

AUTOSAR R20-11:
KeyExchangeCalcPubVal: Changed type of publicValuePtr argument to VoidPtr resulting in just one interface for all jobs again.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcPubVal: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of publicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef

- **UUID**: `44b11427-e7c3-4cba-9230-677b3ce99a37`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef

- **UUID**: `be609eee-00c7-42e5-ac82-b758c7bd1777`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef

- **UUID**: `88cbcf59-6eeb-4d12-b6b3-b273b574d506`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 37. CsmJobKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `15688ba9-0142-4fae-a0f6-63e40e663d8b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcPubValConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyExchangeCalcPubValAlgorithmFamily

- **UUID**: `e137a61d-936b-46e0-be72-269cdcd2b897`
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
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyExchangeCalcPubValAlgorithmMode

- **UUID**: `6068cf87-5927-47c9-83c3-0961a316f1ce`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmMode`
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

######## 4. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily

- **UUID**: `7494946f-8e19-43f6-ae42-1b8e4b5c5ce7`
- **参数名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

######## 5. CsmJobKeyExchangeCalcPubValSwcInterfaceVersion

- **UUID**: `4aa19e7d-2770-4409-b112-ff7c7614bac0`
- **参数名**: `CsmJobKeyExchangeCalcPubValSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcPubVal: Removal of key argument.

AUTOSAR R20-11:
KeyExchangeCalcPubVal: Changed type of publicValuePtr argument to VoidPtr resulting in just one interface for all jobs again.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcPubVal: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of publicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef

- **UUID**: `44b11427-e7c3-4cba-9230-677b3ce99a37`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef

- **UUID**: `be609eee-00c7-42e5-ac82-b758c7bd1777`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef

- **UUID**: `88cbcf59-6eeb-4d12-b6b3-b273b574d506`
- **引用名**: `CsmJobKeyExchangeCalcPubValAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 38. CsmJobKeyExchangeCalcSecret

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

此容器包含 **8** 个参数：

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

- **UUID**: `c2ea1921-3d7b-44f4-90df-5b0fc96edc5e`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `7ccbe3ec-788b-4b8f-b983-edbf7021273f`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `d170acc7-4d54-4878-9864-82c4dc55a10c`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
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

########## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `59a614ad-bbe1-4e64-a002-402c09dfbd14`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyExchangeCalcSecretSwcInterfaceVersion

- **UUID**: `1eff66c3-f0e0-4f6c-8d45-dd6510d14173`
- **参数名**: `CsmJobKeyExchangeCalcSecretSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11_A` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above
CSM_ASR_VERSION_R21_11_A: Interface adheres to AUTOSAR R21-11 with some changes (see detailled description below)

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcSecret: Removal of key argument.
CSM_ASR_VERSION_R21_11_A: This variant provides an alternative version of the interface using VoidPtr as type for the publicValuePtr argument resulting in just one interface for all jobs again. This is provided as all other primitives were changed to VoidPtr in R20 but this primitive which might be a mistake in AUTOSAR.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcSecret: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of partnerPublicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became Job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef

- **UUID**: `7e970ce2-29f5-402e-aba9-b54beb6af571`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef

- **UUID**: `564e3a23-64c0-41fe-bb58-69d6df67f632`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef

- **UUID**: `af185df5-c417-4922-a001-99c628e0b8aa`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 39. CsmJobKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `7cc3e7e7-dff2-4e9c-a2c3-f13bfed833f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyExchangeCalcSecretConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM JobKeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a JobKeyExchangeCalcSecret configuration.

###### 参数配置

此容器包含 **8** 个参数：

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

- **UUID**: `c2ea1921-3d7b-44f4-90df-5b0fc96edc5e`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyExchangeCalcSecretAlgorithmFamily

- **UUID**: `7ccbe3ec-788b-4b8f-b983-edbf7021273f`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_DH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyExchangeCalcSecretAlgorithmMode

- **UUID**: `d170acc7-4d54-4878-9864-82c4dc55a10c`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmMode`
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

######## 4. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily

- **UUID**: `59a614ad-bbe1-4e64-a002-402c09dfbd14`
- **参数名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

######## 5. CsmJobKeyExchangeCalcSecretSwcInterfaceVersion

- **UUID**: `1eff66c3-f0e0-4f6c-8d45-dd6510d14173`
- **参数名**: `CsmJobKeyExchangeCalcSecretSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11_A` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above
CSM_ASR_VERSION_R21_11_A: Interface adheres to AUTOSAR R21-11 with some changes (see detailled description below)

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyExchangeCalcSecret: Removal of key argument.
CSM_ASR_VERSION_R21_11_A: This variant provides an alternative version of the interface using VoidPtr as type for the publicValuePtr argument resulting in just one interface for all jobs again. This is provided as all other primitives were changed to VoidPtr in R20 but this primitive which might be a mistake in AUTOSAR.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyExchangeCalcSecret: CRYPTO_E_KEY_NOT_VALID was added and CSM_E_SMALL_BUFFER was removed as error code. Changed type of partnerPublicValuePtr argument to Csm_KeyDataType_{Key}. Thus, interface became Job dependent.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef

- **UUID**: `7e970ce2-29f5-402e-aba9-b54beb6af571`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef

- **UUID**: `564e3a23-64c0-41fe-bb58-69d6df67f632`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef

- **UUID**: `af185df5-c417-4922-a001-99c628e0b8aa`
- **引用名**: `CsmJobKeyExchangeCalcSecretAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 40. CsmJobKeyDerive

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `705b1e3e-3dd0-4180-ac3d-7b9e34d1c81a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
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

########## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `3f583317-6ff9-4777-b17c-85f21394c53a`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `3824e56d-cd86-4db2-a6ab-1e6b355f452c`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 5. CsmJobKeyDeriveSwcInterfaceVersion

- **UUID**: `221f2273-a738-41b8-8a25-b015395e11d2`
- **参数名**: `CsmJobKeyDeriveSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyDerive: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyDeriveAlgorithmFamilyCustomRef

- **UUID**: `ccdd442d-de9d-46ec-bff4-237468c55114`
- **引用名**: `CsmJobKeyDeriveAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3e9f0ec0-0ac4-41cb-ad6f-af0bfaff00e6`
- **引用名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyDeriveAlgorithmModeCustomRef

- **UUID**: `f4c8b7e5-4b17-4438-8c38-1ee6be0c0f28`
- **引用名**: `CsmJobKeyDeriveAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 41. CsmJobKeyDeriveConfig

**容器属性**:

- **UUID**: `ea77b905-c682-448a-81d5-308ed051222e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyDeriveConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key derive operation. The container name serves as a symbolic name for the identifier of a key derive configuration.

###### 参数配置

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_HKDF` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_KDFX963` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_PBKDF2` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyDeriveAlgorithmFamily

- **UUID**: `705b1e3e-3dd0-4180-ac3d-7b9e34d1c81a`
- **参数名**: `CsmJobKeyDeriveAlgorithmFamily`
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

######## 3. CsmJobKeyDeriveAlgorithmMode

- **UUID**: `3f583317-6ff9-4777-b17c-85f21394c53a`
- **参数名**: `CsmJobKeyDeriveAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `3824e56d-cd86-4db2-a6ab-1e6b355f452c`
- **参数名**: `CsmJobKeyDeriveAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

######## 5. CsmJobKeyDeriveSwcInterfaceVersion

- **UUID**: `221f2273-a738-41b8-8a25-b015395e11d2`
- **参数名**: `CsmJobKeyDeriveSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyDerive: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeyDeriveAlgorithmFamilyCustomRef

- **UUID**: `ccdd442d-de9d-46ec-bff4-237468c55114`
- **引用名**: `CsmJobKeyDeriveAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef

- **UUID**: `3e9f0ec0-0ac4-41cb-ad6f-af0bfaff00e6`
- **引用名**: `CsmJobKeyDeriveAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmJobKeyDeriveAlgorithmModeCustomRef

- **UUID**: `f4c8b7e5-4b17-4438-8c38-1ee6be0c0f28`
- **引用名**: `CsmJobKeyDeriveAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 42. CsmJobRandomSeed

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

此容器包含 **8** 个参数：

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

- **UUID**: `361efddb-8ac0-4b56-9bdd-37baa251920d`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `07734932-e17c-4be0-85a1-df5773761f58`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

########## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `569097f7-9f43-42fe-a38b-d35a245d60ca`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.
Backward compatibility to R19-11. Use CsmJobRandomSeedAlgorithmFamily instead.

########## 4. CsmJobRandomSeedAlgorithmFamily

- **UUID**: `88cf73da-37bc-43cd-97ad-edca04902dd1`
- **参数名**: `CsmJobRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_DRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_FIPS186` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 5. CsmJobRandomSeedSwcInterfaceVersion

- **UUID**: `09a39b83-8dc1-46d5-a3f1-ce74f31557c8`
- **参数名**: `CsmJobRandomSeedSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomSeed: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobRandomSeedAlgorithmFamilyCustomRef

- **UUID**: `b725033b-d47b-43f4-aedb-a99be63bbfdd`
- **引用名**: `CsmJobRandomSeedAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef

- **UUID**: `bc3ba5aa-ca20-4ec7-be71-cf2afad634e1`
- **引用名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobRandomSeedAlgorithmModeCustomRef

- **UUID**: `57f10df5-f6f9-4e9e-88f4-9fb0a74b5abe`
- **引用名**: `CsmJobRandomSeedAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 43. CsmJobRandomSeedConfig

**容器属性**:

- **UUID**: `d8a2b8d8-f086-47b4-93a7-8b14fdb26ab1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobRandomSeedConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM random seed operation. The container name serves as a symbolic name for the identifier of a random seed configuration.

###### 参数配置

此容器包含 **8** 个参数：

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

- **UUID**: `361efddb-8ac0-4b56-9bdd-37baa251920d`
- **参数名**: `CsmJobRandomSeedAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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

- **UUID**: `07734932-e17c-4be0-85a1-df5773761f58`
- **参数名**: `CsmJobRandomSeedAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

######## 3. CsmRandomSeedAlgorithmFamily

- **UUID**: `569097f7-9f43-42fe-a38b-d35a245d60ca`
- **参数名**: `CsmRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: Vector Informatik)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: Vector Informatik)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.
Backward compatibility to R19-11. Use CsmJobRandomSeedAlgorithmFamily instead.

######## 4. CsmJobRandomSeedAlgorithmFamily

- **UUID**: `88cf73da-37bc-43cd-97ad-edca04902dd1`
- **参数名**: `CsmJobRandomSeedAlgorithmFamily`
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
  - `CRYPTO_ALGOFAM_DRBG` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_EEA3` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_FIPS186` (来源: AUTOSAR_ECUC)
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
  - `CRYPTO_ALGOFAM_SHAKE128` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SHAKE256` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_SM3` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 5. CsmJobRandomSeedSwcInterfaceVersion

- **UUID**: `09a39b83-8dc1-46d5-a3f1-ce74f31557c8`
- **参数名**: `CsmJobRandomSeedSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
RandomSeed: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
RandomSeed: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobRandomSeedAlgorithmFamilyCustomRef

- **UUID**: `b725033b-d47b-43f4-aedb-a99be63bbfdd`
- **引用名**: `CsmJobRandomSeedAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef

- **UUID**: `bc3ba5aa-ca20-4ec7-be71-cf2afad634e1`
- **引用名**: `CsmJobRandomSeedAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmJobRandomSeedAlgorithmModeCustomRef

- **UUID**: `57f10df5-f6f9-4e9e-88f4-9fb0a74b5abe`
- **引用名**: `CsmJobRandomSeedAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 44. CsmJobKeyGenerate

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

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `5365712e-e3de-4ca3-ba79-b6f767678608`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `172a7064-caca-4fbb-b1ea-06d7b60325d1`
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

- **UUID**: `f2a4d424-64cf-4d94-ad8d-6167569f0c84`
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

########## 5. CsmJobKeyGenerateSwcInterfaceVersion

- **UUID**: `91523466-05d1-45e2-8b0a-569d06191c59`
- **参数名**: `CsmJobKeyGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyGenerate: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyGenerate: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeyGenerateAlgorithmFamilyCustomRef

- **UUID**: `78a6eb7f-560e-4e6e-b15f-bd2e98577bf0`
- **引用名**: `CsmJobKeyGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c587de11-9e9f-4ecf-a536-bbed44d9234c`
- **引用名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

########## 3. CsmJobKeyGenerateAlgorithmModeCustomRef

- **UUID**: `355daa76-f017-4c13-8207-71d4f1f091c3`
- **引用名**: `CsmJobKeyGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 45. CsmJobKeyGenerateConfig

**容器属性**:

- **UUID**: `d6eb3dda-2dbb-4134-83ff-a2a860f0c3ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeyGenerateConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key generate operation. The container name serves as a symbolic name for the identifier of a key generate configuration.

###### 参数配置

此容器包含 **8** 个参数：

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
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeyGenerateAlgorithmFamily

- **UUID**: `5365712e-e3de-4ca3-ba79-b6f767678608`
- **参数名**: `CsmJobKeyGenerateAlgorithmFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCANSI` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCSEC` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECDH` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_X25519` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 3. CsmJobKeyGenerateAlgorithmMode

- **UUID**: `172a7064-caca-4fbb-b1ea-06d7b60325d1`
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

- **UUID**: `f2a4d424-64cf-4d94-ad8d-6167569f0c84`
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

######## 5. CsmJobKeyGenerateSwcInterfaceVersion

- **UUID**: `91523466-05d1-45e2-8b0a-569d06191c59`
- **参数名**: `CsmJobKeyGenerateSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_4_04`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_4_04` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R19_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_4_04: Interface adheres to AUTOSAR 4.4.0 specification
CSM_ASR_VERSION_R19_11: Interface adheres to AUTOSAR R19-11 specification
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeyGenerate: Removal of key argument.

AUTOSAR R19-11:
SWC error codes were prefixed with CRYPTO_E instead of CSM_E.
KeyGenerate: CRYPTO_E_KEY_NOT_VALID was added as error code.

AUTOSAR 4.4.0:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeyGenerateAlgorithmFamilyCustomRef

- **UUID**: `78a6eb7f-560e-4e6e-b15f-bd2e98577bf0`
- **引用名**: `CsmJobKeyGenerateAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef

- **UUID**: `c587de11-9e9f-4ecf-a536-bbed44d9234c`
- **引用名**: `CsmJobKeyGenerateAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

######## 3. CsmJobKeyGenerateAlgorithmModeCustomRef

- **UUID**: `355daa76-f017-4c13-8207-71d4f1f091c3`
- **引用名**: `CsmJobKeyGenerateAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

##### 46. CsmJobCertificateParse

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
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 47. CsmJobCertificateParseConfig

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
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
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
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **描述**: Determines the algorithm family used for the crypto service.

##### 48. CsmJobCertificateVerify

**容器属性**:

- **UUID**: `e19f001a-6b1d-4ebb-8ad6-7c3965c5347c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobCertificateVerify`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of CertificateVerify primitives

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
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
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

########## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
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

##### 49. CsmJobCertificateVerifyConfig

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
- **描述**: Not used.
Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobCertificateVerifyAlgorithmMode

- **UUID**: `eb542ee7-dae5-421f-a0d4-7b3deaa90c2c`
- **参数名**: `CsmJobCertificateVerifyAlgorithmMode`
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

######## 3. CsmJobCertificateVerifyAlgorithmSecondaryFamily

- **UUID**: `178392cf-22ea-4d0d-ad70-ec7b77c348f9`
- **参数名**: `CsmJobCertificateVerifyAlgorithmSecondaryFamily`
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

##### 50. CsmJobKeySetInvalid

**容器属性**:

- **UUID**: `344050ac-e162-48be-8e2d-2f7f58519e84`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalid`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Configurations of KeySetInvalid primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJobKeySetInvalidConfig

**容器属性**:

- **UUID**: `5590b0b9-4afe-4384-9b56-1c87427978b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set invalid operation.

######## 参数配置

此容器包含 **4** 个参数：

######### ENUMERATION 类型参数

########## 1. CsmJobKeySetInvalidAlgorithmFamily

- **UUID**: `0531a385-e7e7-4608-b8a1-4fe9cd5c8526`
- **参数名**: `CsmJobKeySetInvalidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmJobKeySetInvalidAlgorithmMode

- **UUID**: `f12d993c-da30-4176-9fc5-f38a3fc6cdd7`
- **参数名**: `CsmJobKeySetInvalidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

########## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamily

- **UUID**: `4e1e7bee-7f09-4dcf-87fa-15007e0c3b75`
- **参数名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

########## 4. CsmJobKeySetInvalidSwcInterfaceVersion

- **UUID**: `5028b042-85a3-4fec-811f-88f7711e4c1b`
- **参数名**: `CsmJobKeySetInvalidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetInvalid: Removal of key argument.

AUTOSAR R20-11:
Introduction of this primitive

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmJobKeySetInvalidAlgorithmFamilyCustomRef

- **UUID**: `3d23e8b9-c2b5-48d5-8bce-746b5d4fbd7e`
- **引用名**: `CsmJobKeySetInvalidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

########## 2. CsmJobKeySetInvalidAlgorithmModeCustomRef

- **UUID**: `e3a9233c-13b0-45fe-90d2-1d058bbfeb43`
- **引用名**: `CsmJobKeySetInvalidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

########## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4036bfca-5fe5-40b2-ab5c-135c6c95333d`
- **引用名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 51. CsmJobKeySetInvalidConfig

**容器属性**:

- **UUID**: `5590b0b9-4afe-4384-9b56-1c87427978b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobKeySetInvalidConfig`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container for configuration of a CSM key set invalid operation.

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. CsmJobKeySetInvalidAlgorithmFamily

- **UUID**: `0531a385-e7e7-4608-b8a1-4fe9cd5c8526`
- **参数名**: `CsmJobKeySetInvalidAlgorithmFamily`
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
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmJobKeySetInvalidAlgorithmMode

- **UUID**: `f12d993c-da30-4176-9fc5-f38a3fc6cdd7`
- **参数名**: `CsmJobKeySetInvalidAlgorithmMode`
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
- **描述**: Determines the algorithm mode used for the crypto service.

######## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamily

- **UUID**: `4e1e7bee-7f09-4dcf-87fa-15007e0c3b75`
- **参数名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamily`
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
- **描述**: Determines the secondary algorithm family used for the crypto service.

######## 4. CsmJobKeySetInvalidSwcInterfaceVersion

- **UUID**: `5028b042-85a3-4fec-811f-88f7711e4c1b`
- **参数名**: `CsmJobKeySetInvalidSwcInterfaceVersion`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `CSM_ASR_VERSION_R20_11`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASR_VERSION_R20_11` (来源: Vector Informatik)
  - `CSM_ASR_VERSION_R21_11` (来源: Vector Informatik)
- **描述**: Specifies the AUTOSAR version that the Client-Server-Interfaces of this primitive should adhere to.

CSM_ASR_VERSION_R20_11: Interface adheres to AUTOSAR R20-11
CSM_ASR_VERSION_R21_11: Interface adheres to AUTOSAR R21-11 specification and above

In the following, the changes introduced with the respective version are listed:

AUTOSAR R21-11:
KeySetInvalid: Removal of key argument.

AUTOSAR R20-11:
Introduction of this primitive

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmJobKeySetInvalidAlgorithmFamilyCustomRef

- **UUID**: `3d23e8b9-c2b5-48d5-8bce-746b5d4fbd7e`
- **引用名**: `CsmJobKeySetInvalidAlgorithmFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family custom container

######## 2. CsmJobKeySetInvalidAlgorithmModeCustomRef

- **UUID**: `e3a9233c-13b0-45fe-90d2-1d058bbfeb43`
- **引用名**: `CsmJobKeySetInvalidAlgorithmModeCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmModeCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmModeCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm mode custom container

######## 3. CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef

- **UUID**: `4036bfca-5fe5-40b2-ab5c-135c6c95333d`
- **引用名**: `CsmJobKeySetInvalidAlgorithmSecondaryFamilyCustomRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CryptoPrimitiveAlgorithmFamilyCustom`
- **完整路径**: `/AUTOSAR/EcucDefs/Crypto/CryptoPrimitives/CryptoPrimitiveAlgorithmFamilyCustom`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a customer specific algorithm family container in the Crypto Driver

##### 52. CsmQueues

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
1 for all synchronous jobs of the queue (if there are any)
Queue size + 1 for all asynchronous jobs (if there are any)
This means the queue of the Csm can be filled completely while one job is currenlty processed by the crypto driver object.
If the crypto driver object which handles the job of this queue also implements a queing mechanism, either increase the queue size of Csm accordingly to get the necessary amount of job objects, or deactivate the job sharing.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmQueueMainFunctionRef

- **UUID**: `39947f56-7622-4964-b81d-002a536c67f2`
- **引用名**: `CsmQueueMainFunctionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmMainFunction`
- **完整路径**: `/MICROSAR/Csm/CsmMainFunction`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to CsmMainFunction, where the according CsmQueue is assigned to.

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

##### 53. CsmQueue

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
1 for all synchronous jobs of the queue (if there are any)
Queue size + 1 for all asynchronous jobs (if there are any)
This means the queue of the Csm can be filled completely while one job is currenlty processed by the crypto driver object.
If the crypto driver object which handles the job of this queue also implements a queing mechanism, either increase the queue size of Csm accordingly to get the necessary amount of job objects, or deactivate the job sharing.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CsmQueueMainFunctionRef

- **UUID**: `39947f56-7622-4964-b81d-002a536c67f2`
- **引用名**: `CsmQueueMainFunctionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmMainFunction`
- **完整路径**: `/MICROSAR/Csm/CsmMainFunction`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to CsmMainFunction, where the according CsmQueue is assigned to.

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

##### 54. CsmCallouts

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

##### 55. CsmCallout

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

##### 56. CsmInOutRedirections

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

##### 57. CsmInOutRedirection

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

##### 58. CsmMainFunction

**容器属性**:

- **UUID**: `2436276f-d4e9-4bfb-b826-17e9adc70a86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMainFunction`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Each element of this container defines one instance of Csm_MainFunction.
For each partition, where the Csm module shall be instantiated, at least one MainFunction instance needs to be configured.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. CsmMainFunctionPeriod

- **UUID**: `73898bb7-c05e-4a92-ab5d-fb0fbcc8f307`
- **参数名**: `CsmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0..1.7976931348623157E+308]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the period of main function Csm_MainFunction in seconds.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CsmMainFunctionPartitionRef

- **UUID**: `da464018-6212-438b-8413-1c30b26b520b`
- **引用名**: `CsmMainFunctionPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to EcucPartition, where the according CsmMainFunction
instance is assigned to.

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
- **软件版本**: 7.02.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.07.00
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
