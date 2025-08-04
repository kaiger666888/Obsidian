# Csm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:39

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Csm](#csm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Csm

#### 基本信息

- **UUID**: `77cfbfad-6641-418a-a8da-801d0684cb2c`
- **模块名称**: `Csm`
- **类别**: `STANDARDIZED_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Csm (CryptoServiceManager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.3.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **85** 个配置容器：

##### 1. CsmCallbacks

**容器属性**:

- **UUID**: `342b4bc5-2620-4ce3-a9f4-c1c6d9dc84d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallbacks`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for callback function configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmCallback

**容器属性**:

- **UUID**: `d7c28795-a361-428d-8a25-db342dbb8d88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallback`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a callback function

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CsmCallbackId

- **UUID**: `10bef6b6-959b-42c6-8374-fe34651b9733`
- **参数名**: `CsmCallbackId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the callback function.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackFunc

- **UUID**: `e831c7bb-062a-4944-906b-d14f1cb6581c`
- **参数名**: `CsmCallbackFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if an asynchronous operation has finished. The corresponding job has to be configured to be processed asynchronously.

##### 2. CsmCallback

**容器属性**:

- **UUID**: `d7c28795-a361-428d-8a25-db342dbb8d88`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmCallback`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a callback function

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmCallbackId

- **UUID**: `10bef6b6-959b-42c6-8374-fe34651b9733`
- **参数名**: `CsmCallbackId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the callback function.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackFunc

- **UUID**: `e831c7bb-062a-4944-906b-d14f1cb6581c`
- **参数名**: `CsmCallbackFunc`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if an asynchronous operation has finished. The corresponding job has to be configured to be processed asynchronously.

##### 3. CsmGeneral

**容器属性**:

- **UUID**: `6c473c7b-024e-411c-af04-5e9db9e0cfee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for common configuration options.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPrivateKeyMaxLength

- **UUID**: `89daa413-cf8a-4ce1-8ea9-f92822e77f9a`
- **参数名**: `CsmAsymPrivateKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum length in bytes of an asymmetric public key for all algorithm

######## 2. CsmAsymPublicKeyMaxLength

- **UUID**: `346a2ed2-7409-4777-b09f-3078f147bba2`
- **参数名**: `CsmAsymPublicKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum length in bytes of an asymmetric key for all algorithm

######## 3. CsmSymKeyMaxLength

- **UUID**: `462ef3d1-41a4-4271-b007-d8bb83a8ead5`
- **参数名**: `CsmSymKeyMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum length in bytes of a symmetric key for all algorithm

######## 4. CsmMaximumBlockingTime

- **UUID**: `b7a347c6-aa82-41f4-961d-852f498170aa`
- **参数名**: `CsmMaximumBlockingTime`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If interruption is turned on with the configuration option CsmUseInterruption, this option configures the maximum time in microseconds the main function shall be allowed to run before it must interrupt itself. The lowest allowed value for the option is implementation dependent.

####### BOOLEAN 类型参数

######## 1. CsmDevErrorDetect

- **UUID**: `4a03c406-fd48-4e99-b9ae-9229840b0d9c`
- **参数名**: `CsmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the development error detection and notification on or off.

######## 2. CsmUseDeprecated

- **UUID**: `56ec4226-d07d-45c5-afd2-445555d041cc`
- **参数名**: `CsmUseDeprecated`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Decides if the deprecated interfaces shall be used (Backwards combatibility).

######## 3. CsmVersionInfoApi

- **UUID**: `3c64e199-54f0-4303-b29e-5da2d7247994`
- **参数名**: `CsmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable availability of the API Csm_GetVersionInfo().

######## 4. CsmUseInterruption

- **UUID**: `d853cad8-e4e2-4977-b9f2-17184080d35a`
- **参数名**: `CsmUseInterruption`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable interruption of job processing.

######## 5. CsmUseSyncJobProcessing

- **UUID**: `8e386d82-5b4c-4a81-b5bf-0ac1f89ab39d`
- **参数名**: `CsmUseSyncJobProcessing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable synchronous job processing.

####### FLOAT 类型参数

######## 1. CsmMainFunctionPeriod

- **UUID**: `5d5e67e3-efcc-4923-9ab4-af1a3ea2cf0a`
- **参数名**: `CsmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period of main function Csm_MainFunction in seconds.

####### STRING 类型参数

######## 1. CsmMaxAlignScalarType

- **UUID**: `4585a508-9698-43e0-acfd-3624f4e1c906`
- **参数名**: `CsmMaxAlignScalarType`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The scalar type which has the maximum alignment restrictions on the given platform.

######## 2. CsmCustomIncludeFiles

- **UUID**: `4b17c60c-e3c3-41cd-aa5d-2db4872b3d9f`
- **参数名**: `CsmCustomIncludeFiles`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 4. CsmJobs

**容器属性**:

- **UUID**: `da734be0-47e8-4c26-bdbf-26dc4957d4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJobs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of CSM jobs.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmJob

**容器属性**:

- **UUID**: `3096ab5e-0c60-4aed-8627-835991e31bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJob`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of CSM job. The container name serves as a symbolic name for the identifier of a job configuration.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. CsmJobId

- **UUID**: `77849ab6-7c4e-4dd5-a606-245df73f05c1`
- **参数名**: `CsmJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CSM job

########## 2. CsmJobPriority

- **UUID**: `2a85fc0a-acc6-463f-9125-4455d2e16873`
- **参数名**: `CsmJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the job.

######### BOOLEAN 类型参数

########## 1. CsmJobPrimitiveCallbackUpdateNotification

- **UUID**: `0f1dac97-99ce-460a-94da-07e45b85c769`
- **参数名**: `CsmJobPrimitiveCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates, whether the callback function shall be called, if the UPDATE operation has been finished.

########## 2. CsmJobUsePort

- **UUID**: `752c6965-15ef-4251-aad3-6e24c857266d`
- **参数名**: `CsmJobUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Does the job need RTE interfaces?

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. CsmJobKeyRef

- **UUID**: `86cf7ebb-ed1c-478d-b649-66c660e94042`
- **引用名**: `CsmJobKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key which shall be used for the CsmPrimitive. It's possible to use a CsmKey for different jobs

########## 2. CsmJobPrimitiveCallbackRef

- **UUID**: `b8d0db0d-b741-4cfa-9bda-323ea3a6630a`
- **引用名**: `CsmJobPrimitiveCallbackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallback`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmCallbacks/CsmCallback`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CsmCallback.

########## 3. CsmJobPrimitiveRef

- **UUID**: `692153f7-27eb-4452-aa47-11526ca56b85`
- **引用名**: `CsmJobPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmPrimitives`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmPrimitives`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CsmPrimitive.

########## 4. CsmJobQueueRef

- **UUID**: `203a292a-7c69-45f1-9990-bf31d42745b6`
- **引用名**: `CsmJobQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue.

##### 5. CsmJob

**容器属性**:

- **UUID**: `3096ab5e-0c60-4aed-8627-835991e31bbe`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmJob`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of CSM job. The container name serves as a symbolic name for the identifier of a job configuration.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. CsmJobId

- **UUID**: `77849ab6-7c4e-4dd5-a606-245df73f05c1`
- **参数名**: `CsmJobId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CSM job

######## 2. CsmJobPriority

- **UUID**: `2a85fc0a-acc6-463f-9125-4455d2e16873`
- **参数名**: `CsmJobPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of the job.

####### BOOLEAN 类型参数

######## 1. CsmJobPrimitiveCallbackUpdateNotification

- **UUID**: `0f1dac97-99ce-460a-94da-07e45b85c769`
- **参数名**: `CsmJobPrimitiveCallbackUpdateNotification`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates, whether the callback function shall be called, if the UPDATE operation has been finished.

######## 2. CsmJobUsePort

- **UUID**: `752c6965-15ef-4251-aad3-6e24c857266d`
- **参数名**: `CsmJobUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Does the job need RTE interfaces?

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. CsmJobKeyRef

- **UUID**: `86cf7ebb-ed1c-478d-b649-66c660e94042`
- **引用名**: `CsmJobKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key which shall be used for the CsmPrimitive. It's possible to use a CsmKey for different jobs

######## 2. CsmJobPrimitiveCallbackRef

- **UUID**: `b8d0db0d-b741-4cfa-9bda-323ea3a6630a`
- **引用名**: `CsmJobPrimitiveCallbackRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmCallback`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmCallbacks/CsmCallback`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CsmCallback.

######## 3. CsmJobPrimitiveRef

- **UUID**: `692153f7-27eb-4452-aa47-11526ca56b85`
- **引用名**: `CsmJobPrimitiveRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmPrimitives`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmPrimitives`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CsmPrimitive.

######## 4. CsmJobQueueRef

- **UUID**: `203a292a-7c69-45f1-9990-bf31d42745b6`
- **引用名**: `CsmJobQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue.

##### 6. CsmKeys

**容器属性**:

- **UUID**: `da4b1551-3b36-4629-8da8-64a5d8784cb7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeys`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CSM key configurations.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKey

**容器属性**:

- **UUID**: `73b38f1a-330b-477e-a86f-aa0cb6c45236`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKey`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM key. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CsmKeyId

- **UUID**: `4cb4439f-2105-4b1f-8e90-308a1e4f901b`
- **参数名**: `CsmKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CsmKey

######### BOOLEAN 类型参数

########## 1. CsmKeyUsePort

- **UUID**: `874341ce-cbd0-45de-b220-4c163a2c90e6`
- **参数名**: `CsmKeyUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Does the key need RTE interfaces?

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmKeyRef

- **UUID**: `87cd2ccc-c13b-4b38-b544-553c938e6ba0`
- **引用名**: `CsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CryIfKey. The underlying CryIfKey refers to a specific CryptoKey in the Crypto Driver.

##### 7. CsmKey

**容器属性**:

- **UUID**: `73b38f1a-330b-477e-a86f-aa0cb6c45236`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKey`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM key. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyId

- **UUID**: `4cb4439f-2105-4b1f-8e90-308a1e4f901b`
- **参数名**: `CsmKeyId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the CsmKey

####### BOOLEAN 类型参数

######## 1. CsmKeyUsePort

- **UUID**: `874341ce-cbd0-45de-b220-4c163a2c90e6`
- **参数名**: `CsmKeyUsePort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Does the key need RTE interfaces?

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmKeyRef

- **UUID**: `87cd2ccc-c13b-4b38-b544-553c938e6ba0`
- **引用名**: `CsmKeyRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfKey`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the used CryIfKey. The underlying CryIfKey refers to a specific CryptoKey in the Crypto Driver.

##### 8. CsmPrimitives

**容器属性**:

- **UUID**: `75ac8914-876c-47b6-bc22-5e44aeea7173`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmPrimitives`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of CsmPrimitives

###### 配置容器

本模块包含 **22** 个配置容器：

####### 1. CsmAEADDecrypt

**容器属性**:

- **UUID**: `b739f3e1-7603-4cb5-b560-8dfbeb36bc6e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configuration of AEAD decryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `092ae8e2-3de5-4d75-8d04-10ca423c7aaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `450e2edf-5a3c-4ff0-ab05-7125b48a878d`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD decryption key in bytes

############ 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `8bd3fccf-b370-4cd1-8265-f1fb1ac6867a`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

############ 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `5f714dd2-50c2-49f8-9e7a-ca8cbd6d076d`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext in bytes

############ 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `bc1a2108-2948-4811-ac8b-76bfdfd0bbcc`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output plaintext length in bytes

############ 5. CsmAEADDecryptTagLength

- **UUID**: `1daea247-1ea8-4036-8959-bb3b2c6a0243`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input Tag length in BITS

########### STRING 类型参数

############ 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `3b625cb7-be1a-4386-a828-4151a2f7cdc5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

############ 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `1d192f2d-3ee5-4c04-840a-9b98402c9fec`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `a1cb1a6c-5691-450a-90b5-8345448f00c2`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADDecryptAlgorithmMode

- **UUID**: `a1184a25-3707-472a-aa82-fee42f93bb1e`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmAEADDecryptProcessing

- **UUID**: `afba8b6e-7465-4474-9630-84c6f3208639`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. CsmAEADDecryptKeyRef

- **UUID**: `b5a0cf4d-314f-4eb2-994c-e02a2cb01647`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that decryption primitive.

############ 2. CsmAEADDecryptQueueRef

- **UUID**: `94dddc37-a55c-4ce4-9606-6f4e39a46fbf`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that decryption primitive.

####### 2. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `092ae8e2-3de5-4d75-8d04-10ca423c7aaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `450e2edf-5a3c-4ff0-ab05-7125b48a878d`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD decryption key in bytes

########## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `8bd3fccf-b370-4cd1-8265-f1fb1ac6867a`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `5f714dd2-50c2-49f8-9e7a-ca8cbd6d076d`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext in bytes

########## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `bc1a2108-2948-4811-ac8b-76bfdfd0bbcc`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output plaintext length in bytes

########## 5. CsmAEADDecryptTagLength

- **UUID**: `1daea247-1ea8-4036-8959-bb3b2c6a0243`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input Tag length in BITS

######### STRING 类型参数

########## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `3b625cb7-be1a-4386-a828-4151a2f7cdc5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

########## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `1d192f2d-3ee5-4c04-840a-9b98402c9fec`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `a1cb1a6c-5691-450a-90b5-8345448f00c2`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmMode

- **UUID**: `a1184a25-3707-472a-aa82-fee42f93bb1e`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmAEADDecryptProcessing

- **UUID**: `afba8b6e-7465-4474-9630-84c6f3208639`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADDecryptKeyRef

- **UUID**: `b5a0cf4d-314f-4eb2-994c-e02a2cb01647`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that decryption primitive.

########## 2. CsmAEADDecryptQueueRef

- **UUID**: `94dddc37-a55c-4ce4-9606-6f4e39a46fbf`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that decryption primitive.

####### 3. CsmAEADEncrypt

**容器属性**:

- **UUID**: `291d8ff1-5965-48dd-8225-92258399195a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configuration of AEAD encryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `e74cce7c-8f3c-429a-9fef-e47a222c8641`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `7de3cf6f-8066-453c-b9df-b00cfc339694`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD encryption key in bytes

############ 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `6bf021a4-c465-4f38-9efd-c79b55cb7472`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

############ 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `8f7c6f2a-f15e-4edc-9903-a4769b9be669`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output ciphertext length in bytes

############ 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `8141367d-8ba0-43bf-b352-f9d3d0e9c97d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

############ 5. CsmAEADEncryptTagLength

- **UUID**: `16c80a2a-2521-4a39-9d26-94be17c35bba`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output Tag length in bytes

########### STRING 类型参数

############ 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `db453e7a-f929-4ee7-b079-a69f6ed2de1e`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

############ 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `593d4d36-cc4c-4d60-a640-3d51e3c0bbc1`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `44247018-817a-4c07-9d09-738087f0a12f`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmAEADEncryptAlgorithmMode

- **UUID**: `b9f7e510-bf5e-449e-bf06-4362033c7abd`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmAEADEncryptProcessing

- **UUID**: `a3064817-3b35-451c-9fba-b97a489ecb30`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. CsmAEADEncryptKeyRef

- **UUID**: `92414fc6-7e7b-414b-81a9-78d0ff2e369b`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that encryption primitive.

############ 2. CsmAEADEncryptQueueRef

- **UUID**: `25c269ce-976c-4db3-af94-566b5de1570e`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that encryption primitive.

####### 4. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `e74cce7c-8f3c-429a-9fef-e47a222c8641`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `7de3cf6f-8066-453c-b9df-b00cfc339694`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD encryption key in bytes

########## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `6bf021a4-c465-4f38-9efd-c79b55cb7472`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `8f7c6f2a-f15e-4edc-9903-a4769b9be669`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output ciphertext length in bytes

########## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `8141367d-8ba0-43bf-b352-f9d3d0e9c97d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

########## 5. CsmAEADEncryptTagLength

- **UUID**: `16c80a2a-2521-4a39-9d26-94be17c35bba`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output Tag length in bytes

######### STRING 类型参数

########## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `db453e7a-f929-4ee7-b079-a69f6ed2de1e`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

########## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `593d4d36-cc4c-4d60-a640-3d51e3c0bbc1`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `44247018-817a-4c07-9d09-738087f0a12f`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmMode

- **UUID**: `b9f7e510-bf5e-449e-bf06-4362033c7abd`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmAEADEncryptProcessing

- **UUID**: `a3064817-3b35-451c-9fba-b97a489ecb30`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADEncryptKeyRef

- **UUID**: `92414fc6-7e7b-414b-81a9-78d0ff2e369b`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that encryption primitive.

########## 2. CsmAEADEncryptQueueRef

- **UUID**: `25c269ce-976c-4db3-af94-566b5de1570e`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that encryption primitive.

####### 5. CsmDecrypt

**容器属性**:

- **UUID**: `46e267a3-d80d-47d7-a6fa-cb5043e82778`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of Decryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmDecryptConfig

**容器属性**:

- **UUID**: `70f0bc96-eee5-467a-9e61-4685c54041c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `02da7cab-eba0-48ef-8d37-93c51c8d4235`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the encryption key in bytes

############ 2. CsmDecryptDataMaxLength

- **UUID**: `1fe43d94-68f5-4d8f-978a-f2beff28f8dd`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext length in bytes

############ 3. CsmDecryptResultMaxLength

- **UUID**: `ec875ce6-56bb-4a13-b18c-c9661079c293`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output plaintext length in bytes

########### STRING 类型参数

############ 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `18ce426e-9a84-42a8-85c9-742b1a236180`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

############ 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `c5e762ce-2a8e-4dea-8a69-64319c3ab4e2`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `23ae0e82-92a9-422f-8907-8800ccbfd491`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `b0ca8007-09d0-483c-a315-70ae3a828a44`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmDecryptAlgorithmMode

- **UUID**: `87f3baca-123a-40d2-ab1c-67a609eb4dbb`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `f03e2853-49cc-4b88-9297-acfe4b9676ee`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 4. CsmDecryptProcessing

- **UUID**: `350fc09d-2fc3-4427-a4e4-5cdb52540dce`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 6. CsmDecryptConfig

**容器属性**:

- **UUID**: `70f0bc96-eee5-467a-9e61-4685c54041c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `02da7cab-eba0-48ef-8d37-93c51c8d4235`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the encryption key in bytes

########## 2. CsmDecryptDataMaxLength

- **UUID**: `1fe43d94-68f5-4d8f-978a-f2beff28f8dd`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext length in bytes

########## 3. CsmDecryptResultMaxLength

- **UUID**: `ec875ce6-56bb-4a13-b18c-c9661079c293`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output plaintext length in bytes

######### STRING 类型参数

########## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `18ce426e-9a84-42a8-85c9-742b1a236180`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

########## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `c5e762ce-2a8e-4dea-8a69-64319c3ab4e2`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `23ae0e82-92a9-422f-8907-8800ccbfd491`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `b0ca8007-09d0-483c-a315-70ae3a828a44`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmMode

- **UUID**: `87f3baca-123a-40d2-ab1c-67a609eb4dbb`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `f03e2853-49cc-4b88-9297-acfe4b9676ee`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmDecryptProcessing

- **UUID**: `350fc09d-2fc3-4427-a4e4-5cdb52540dce`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 7. CsmEncrypt

**容器属性**:

- **UUID**: `3f4b7ccf-df57-454a-86db-54556e64957c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of Encryption primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmEncryptConfig

**容器属性**:

- **UUID**: `0714939b-250c-4472-8483-d555cab5d6ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. CsmEncryptDataMaxLength

- **UUID**: `6e378d3e-eb6d-45ac-9fa1-3cb39366237d`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

############ 2. CsmEncryptResultMaxLength

- **UUID**: `c809b99b-cb37-46f3-b5de-d54a58c7952a`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output cipher length in bytes

########### STRING 类型参数

############ 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `e6e09321-1edc-405b-b19a-22cc81b1076c`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

############ 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `48b668ed-5a9d-4900-ae5e-b9eb6833b076`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `3a45778b-dccf-4f3d-bd22-ebdeb04c9292`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

########### ENUMERATION 类型参数

############ 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `b7865263-d6a8-4a50-80ad-2c064e4648be`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmEncryptAlgorithmMode

- **UUID**: `64c306cf-0947-4016-bd96-b398aaad3d3f`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `572d8304-0329-4bab-8d72-49c9a9452dd5`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

############ 4. CsmEncryptProcessing

- **UUID**: `b31a4d25-56d8-419b-9280-7c6c91cb5194`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 8. CsmEncryptConfig

**容器属性**:

- **UUID**: `0714939b-250c-4472-8483-d555cab5d6ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmEncryptDataMaxLength

- **UUID**: `6e378d3e-eb6d-45ac-9fa1-3cb39366237d`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

########## 2. CsmEncryptResultMaxLength

- **UUID**: `c809b99b-cb37-46f3-b5de-d54a58c7952a`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output cipher length in bytes

######### STRING 类型参数

########## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `e6e09321-1edc-405b-b19a-22cc81b1076c`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

########## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `48b668ed-5a9d-4900-ae5e-b9eb6833b076`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `3a45778b-dccf-4f3d-bd22-ebdeb04c9292`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `b7865263-d6a8-4a50-80ad-2c064e4648be`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmMode

- **UUID**: `64c306cf-0947-4016-bd96-b398aaad3d3f`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `572d8304-0329-4bab-8d72-49c9a9452dd5`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmEncryptProcessing

- **UUID**: `b31a4d25-56d8-419b-9280-7c6c91cb5194`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 9. CsmHash

**容器属性**:

- **UUID**: `ffe193d3-66e3-4771-bc96-2f0034e89ec9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Hash Configurations

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmHashConfig

**容器属性**:

- **UUID**: `2cc4aa34-4ee8-40f9-b31d-214325317379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. CsmHashDataMaxLength

- **UUID**: `b2d54e57-087d-4d3c-8643-c0d33d8ac296`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

############ 2. CsmHashResultLength

- **UUID**: `5a3e0d0d-17df-4d63-94b8-ec6d0c16ecb4`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output hash length in bytes

########### STRING 类型参数

############ 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `236996b7-c73d-4be2-8aad-03c1fef3e31c`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

############ 2. CsmHashAlgorithmModeCustom

- **UUID**: `af6c08c7-5241-4643-af19-3003ff3887b9`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom primitive mode.

############ 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `e1396f5c-2564-435f-8f71-14f363f92a61`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmHashAlgorithmFamiliy

- **UUID**: `0e3e2464-c73d-4ffe-885c-b9c11f22a394`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmHashAlgorithmMode

- **UUID**: `92882e2f-45b6-4090-8595-4e24760418db`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmHashAlgorithmSecondaryFamily

- **UUID**: `a9336cbc-de94-44d9-8f6a-064a19bac97f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

############ 4. CsmHashProcessing

- **UUID**: `5a743541-d1ce-4ada-9121-344647e8003c`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 10. CsmHashConfig

**容器属性**:

- **UUID**: `2cc4aa34-4ee8-40f9-b31d-214325317379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmHashDataMaxLength

- **UUID**: `b2d54e57-087d-4d3c-8643-c0d33d8ac296`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

########## 2. CsmHashResultLength

- **UUID**: `5a3e0d0d-17df-4d63-94b8-ec6d0c16ecb4`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output hash length in bytes

######### STRING 类型参数

########## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `236996b7-c73d-4be2-8aad-03c1fef3e31c`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

########## 2. CsmHashAlgorithmModeCustom

- **UUID**: `af6c08c7-5241-4643-af19-3003ff3887b9`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom primitive mode.

########## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `e1396f5c-2564-435f-8f71-14f363f92a61`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmHashAlgorithmFamiliy

- **UUID**: `0e3e2464-c73d-4ffe-885c-b9c11f22a394`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmMode

- **UUID**: `92882e2f-45b6-4090-8595-4e24760418db`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmHashAlgorithmSecondaryFamily

- **UUID**: `a9336cbc-de94-44d9-8f6a-064a19bac97f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmHashProcessing

- **UUID**: `5a743541-d1ce-4ada-9121-344647e8003c`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 11. CsmMacGenerate

**容器属性**:

- **UUID**: `76c1ab44-cf00-4731-a9db-6f0a9f1c10cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of MacGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `c2671334-6ddd-435d-82aa-ad0dca40aeea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `4127714a-c247-426a-a1bd-d10ba5e97cb9`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the MAC key in bytes

############ 2. CsmMacGenerateDataMaxLength

- **UUID**: `667bf375-f2f6-42c6-937b-41c851114f7e`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

############ 3. CsmMacGenerateResultLength

- **UUID**: `5850299b-6489-4341-b9e9-93bc30da7655`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output MAC length in bytes

########### STRING 类型参数

############ 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `5d1b05de-53d1-4315-b2bf-7df6413955e8`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family,

############ 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `9604fe54-b9ba-413c-bfea-2676a8ebbc2e`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f23baa62-39ce-43fd-bca9-edeb8e9ab805`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

########### ENUMERATION 类型参数

############ 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `40188569-ca18-4705-bcd2-cf85d544b99e`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacGenerateAlgorithmMode

- **UUID**: `193d295a-43a0-4a74-81f7-3d5059e5f603`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `b2679827-345c-47a8-9b74-f999c9ee15c9`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 4. CsmMacGenerateProcessing

- **UUID**: `a422fc73-9626-413c-8faa-f6adac56081c`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 12. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `c2671334-6ddd-435d-82aa-ad0dca40aeea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `4127714a-c247-426a-a1bd-d10ba5e97cb9`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the MAC key in bytes

########## 2. CsmMacGenerateDataMaxLength

- **UUID**: `667bf375-f2f6-42c6-937b-41c851114f7e`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

########## 3. CsmMacGenerateResultLength

- **UUID**: `5850299b-6489-4341-b9e9-93bc30da7655`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output MAC length in bytes

######### STRING 类型参数

########## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `5d1b05de-53d1-4315-b2bf-7df6413955e8`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family,

########## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `9604fe54-b9ba-413c-bfea-2676a8ebbc2e`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f23baa62-39ce-43fd-bca9-edeb8e9ab805`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

######### ENUMERATION 类型参数

########## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `40188569-ca18-4705-bcd2-cf85d544b99e`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmMode

- **UUID**: `193d295a-43a0-4a74-81f7-3d5059e5f603`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `b2679827-345c-47a8-9b74-f999c9ee15c9`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmMacGenerateProcessing

- **UUID**: `a422fc73-9626-413c-8faa-f6adac56081c`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 13. CsmMacVerify

**容器属性**:

- **UUID**: `8e223550-7ebc-44ce-84c7-4d05411daa04`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of MacVerify primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `aa358ae1-2419-4ccd-913d-2f79785805de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. CsmMacVerifyCompareLength

- **UUID**: `8264e0ae-cee8-43ed-9fa0-9e553543a5b8`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input MAC length, that shall be verified, in BITS

############ 2. CsmMacVerifyDataMaxLength

- **UUID**: `b273ce86-523f-4ffc-bae5-338a2349b4d3`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length, for whichs MAC shall be verified, in bytes

########### STRING 类型参数

############ 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `b24ba482-9b00-4ddf-bb79-cd7db6e9a952`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service

############ 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ddeadbff-a998-4e01-b761-0b54a3b66474`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

########### ENUMERATION 类型参数

############ 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `3a1f9128-e737-4548-a8a1-60ac975c10b5`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `eb37521b-6cfb-4292-9cbd-4607934da293`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

############ 3. CsmMacVerifyProcessing

- **UUID**: `9ef96e0b-55be-41ed-b00b-4b13e6a12af3`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 14. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `aa358ae1-2419-4ccd-913d-2f79785805de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacVerifyCompareLength

- **UUID**: `8264e0ae-cee8-43ed-9fa0-9e553543a5b8`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input MAC length, that shall be verified, in BITS

########## 2. CsmMacVerifyDataMaxLength

- **UUID**: `b273ce86-523f-4ffc-bae5-338a2349b4d3`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length, for whichs MAC shall be verified, in bytes

######### STRING 类型参数

########## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `b24ba482-9b00-4ddf-bb79-cd7db6e9a952`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ddeadbff-a998-4e01-b761-0b54a3b66474`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

######### ENUMERATION 类型参数

########## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `3a1f9128-e737-4548-a8a1-60ac975c10b5`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `eb37521b-6cfb-4292-9cbd-4607934da293`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 3. CsmMacVerifyProcessing

- **UUID**: `9ef96e0b-55be-41ed-b00b-4b13e6a12af3`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 15. CsmRandomGenerate

**容器属性**:

- **UUID**: `ec02cfc2-8484-454b-a808-9a61cc8c8f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of RandomGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `e0f13b04-04b6-4c86-a85a-f035dd5bb7e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. CsmRandomGenerateResultLength

- **UUID**: `b3d30c52-8e6b-4cac-a1f5-54adf3220495`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the random generate key in bytes

########### STRING 类型参数

############ 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `fc859224-bea1-48ae-8fe3-525653d8ee10`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

############ 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `bcae0710-fa1d-499d-b70b-023ba0d2f70b`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

############ 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `57b3224f-6783-458b-aa80-3ffbdca65503`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `e13eb029-eab0-429e-b592-b6c2daa56d33`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmRandomGenerateAlgorithmMode

- **UUID**: `371136e3-8c98-41f2-aeb1-dc1a3b0b4346`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `b30aa787-6af6-457c-b8c3-53f2dde767ba`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

############ 4. CsmRandomGenerateProcessing

- **UUID**: `8c64cdef-3c23-42fa-9458-e8323e5a2430`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 16. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `e0f13b04-04b6-4c86-a85a-f035dd5bb7e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CsmRandomGenerateResultLength

- **UUID**: `b3d30c52-8e6b-4cac-a1f5-54adf3220495`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the random generate key in bytes

######### STRING 类型参数

########## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `fc859224-bea1-48ae-8fe3-525653d8ee10`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

########## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `bcae0710-fa1d-499d-b70b-023ba0d2f70b`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

########## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `57b3224f-6783-458b-aa80-3ffbdca65503`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `e13eb029-eab0-429e-b592-b6c2daa56d33`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmMode

- **UUID**: `371136e3-8c98-41f2-aeb1-dc1a3b0b4346`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `b30aa787-6af6-457c-b8c3-53f2dde767ba`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmRandomGenerateProcessing

- **UUID**: `8c64cdef-3c23-42fa-9458-e8323e5a2430`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 17. CsmSecureCounter

**容器属性**:

- **UUID**: `ae8fcb3a-3062-4256-a7a5-fc85315fba62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounter`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SecureCounter primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `3cc03b6b-07cd-4ae6-b4a0-015f78d5f527`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CsmSecureCounterQueueRef

- **UUID**: `793a134a-bab0-4c8b-92cd-1a983c713dc2`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used. Queue is referred in Job.
		This parameter refers to the queue used for that secure counter.

####### 18. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `3cc03b6b-07cd-4ae6-b4a0-015f78d5f527`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CsmSecureCounterQueueRef

- **UUID**: `793a134a-bab0-4c8b-92cd-1a983c713dc2`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used. Queue is referred in Job.
		This parameter refers to the queue used for that secure counter.

####### 19. CsmSignatureGenerate

**容器属性**:

- **UUID**: `913d2545-13ac-4c53-981c-83558b0ed28f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SignatureGenerate primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `12372ff1-ccaf-4025-b434-09f6e2abf3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `bd934cfe-20e9-4a41-a8b9-b03f4c3f7404`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length in bytes

############ 2. CsmSignatureGenerateKeyLength

- **UUID**: `3768ba31-9eef-4607-a5df-1784aecf4b07`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the signature generate key in bytes

############ 3. CsmSignatureGenerateResultLength

- **UUID**: `7d370d85-987d-47ba-937b-629c2b08efd3`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output signature length in bytes

########### STRING 类型参数

############ 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `98d26f76-c63a-4c1b-a4e6-68d2e458dc7b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service.

############ 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `cb3f8a86-07d7-4858-ab41-563eebe4f954`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `5ff7ce61-5c6a-469d-9945-b21783480a5f`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

########### ENUMERATION 类型参数

############ 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `b03c8cdd-335b-4a99-bcb0-f56de0db845b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureGenerateAlgorithmMode

- **UUID**: `caf4f4d1-064a-4b7a-86b2-56baff592e6f`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `831ec95b-fc47-4b7c-a3d2-d9b0100c573a`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 4. CsmSignatureGenerateProcessing

- **UUID**: `d803212c-5e03-45d5-87b5-5ee154a69c97`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 20. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `12372ff1-ccaf-4025-b434-09f6e2abf3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `bd934cfe-20e9-4a41-a8b9-b03f4c3f7404`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length in bytes

########## 2. CsmSignatureGenerateKeyLength

- **UUID**: `3768ba31-9eef-4607-a5df-1784aecf4b07`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the signature generate key in bytes

########## 3. CsmSignatureGenerateResultLength

- **UUID**: `7d370d85-987d-47ba-937b-629c2b08efd3`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output signature length in bytes

######### STRING 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `98d26f76-c63a-4c1b-a4e6-68d2e458dc7b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `cb3f8a86-07d7-4858-ab41-563eebe4f954`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `5ff7ce61-5c6a-469d-9945-b21783480a5f`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `b03c8cdd-335b-4a99-bcb0-f56de0db845b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmMode

- **UUID**: `caf4f4d1-064a-4b7a-86b2-56baff592e6f`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `831ec95b-fc47-4b7c-a3d2-d9b0100c573a`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateProcessing

- **UUID**: `d803212c-5e03-45d5-87b5-5ee154a69c97`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

####### 21. CsmSignatureVerify

**容器属性**:

- **UUID**: `86ec2b03-ed09-48a8-9b17-0cbc21a0d0be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SignatureVerify primitives

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `619a235d-53d8-47ce-b976-2abfbc4886d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. CsmSignatureVerifyCompareLength

- **UUID**: `17ac44ee-4818-4575-90e7-4cafcec2d8e6`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

############ 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `7b017ac6-521a-43de-9157-fdbf386df7d7`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

########### STRING 类型参数

############ 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `e0646614-cdcc-4655-9cea-e03a8454e7da`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

############ 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `b44042b1-bd7f-4c61-952e-a8e050c3c889`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

############ 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `081135af-8d85-4042-8587-cfe8564aaf2a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########### ENUMERATION 类型参数

############ 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `5170fc84-26a0-4b6e-b180-4e9c9fcb0d39`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 2. CsmSignatureVerifyAlgorithmMode

- **UUID**: `3826b457-6bb3-408b-acfd-87dbca97fc65`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

############ 3. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `fc3181fd-48b8-4935-be61-bd186567e81a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

############ 4. CsmSignatureVerifyProcessing

- **UUID**: `4479e8a3-fe1c-4a38-891d-3ee77e67a830`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

####### 22. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `619a235d-53d8-47ce-b976-2abfbc4886d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureVerifyCompareLength

- **UUID**: `17ac44ee-4818-4575-90e7-4cafcec2d8e6`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

########## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `7b017ac6-521a-43de-9157-fdbf386df7d7`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

######### STRING 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `e0646614-cdcc-4655-9cea-e03a8454e7da`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `b44042b1-bd7f-4c61-952e-a8e050c3c889`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `081135af-8d85-4042-8587-cfe8564aaf2a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `5170fc84-26a0-4b6e-b180-4e9c9fcb0d39`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmMode

- **UUID**: `3826b457-6bb3-408b-acfd-87dbca97fc65`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `fc3181fd-48b8-4935-be61-bd186567e81a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 4. CsmSignatureVerifyProcessing

- **UUID**: `4479e8a3-fe1c-4a38-891d-3ee77e67a830`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 9. CsmAEADDecrypt

**容器属性**:

- **UUID**: `b739f3e1-7603-4cb5-b560-8dfbeb36bc6e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configuration of AEAD decryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `092ae8e2-3de5-4d75-8d04-10ca423c7aaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `450e2edf-5a3c-4ff0-ab05-7125b48a878d`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD decryption key in bytes

########## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `8bd3fccf-b370-4cd1-8265-f1fb1ac6867a`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `5f714dd2-50c2-49f8-9e7a-ca8cbd6d076d`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext in bytes

########## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `bc1a2108-2948-4811-ac8b-76bfdfd0bbcc`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output plaintext length in bytes

########## 5. CsmAEADDecryptTagLength

- **UUID**: `1daea247-1ea8-4036-8959-bb3b2c6a0243`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input Tag length in BITS

######### STRING 类型参数

########## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `3b625cb7-be1a-4386-a828-4151a2f7cdc5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

########## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `1d192f2d-3ee5-4c04-840a-9b98402c9fec`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `a1cb1a6c-5691-450a-90b5-8345448f00c2`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADDecryptAlgorithmMode

- **UUID**: `a1184a25-3707-472a-aa82-fee42f93bb1e`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmAEADDecryptProcessing

- **UUID**: `afba8b6e-7465-4474-9630-84c6f3208639`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADDecryptKeyRef

- **UUID**: `b5a0cf4d-314f-4eb2-994c-e02a2cb01647`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that decryption primitive.

########## 2. CsmAEADDecryptQueueRef

- **UUID**: `94dddc37-a55c-4ce4-9606-6f4e39a46fbf`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that decryption primitive.

##### 10. CsmAEADDecryptConfig

**容器属性**:

- **UUID**: `092ae8e2-3de5-4d75-8d04-10ca423c7aaa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. CsmAEADDecryptAlgorithmKeyLength

- **UUID**: `450e2edf-5a3c-4ff0-ab05-7125b48a878d`
- **参数名**: `CsmAEADDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD decryption key in bytes

######## 2. CsmAEADDecryptAssociatedDataMaxLength

- **UUID**: `8bd3fccf-b370-4cd1-8265-f1fb1ac6867a`
- **参数名**: `CsmAEADDecryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

######## 3. CsmAEADDecryptCiphertextMaxLength

- **UUID**: `5f714dd2-50c2-49f8-9e7a-ca8cbd6d076d`
- **参数名**: `CsmAEADDecryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext in bytes

######## 4. CsmAEADDecryptPlaintextMaxLength

- **UUID**: `bc1a2108-2948-4811-ac8b-76bfdfd0bbcc`
- **参数名**: `CsmAEADDecryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output plaintext length in bytes

######## 5. CsmAEADDecryptTagLength

- **UUID**: `1daea247-1ea8-4036-8959-bb3b2c6a0243`
- **参数名**: `CsmAEADDecryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input Tag length in BITS

####### STRING 类型参数

######## 1. CsmAEADDecryptAlgorithmFamilyCustom

- **UUID**: `3b625cb7-be1a-4386-a828-4151a2f7cdc5`
- **参数名**: `CsmAEADDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADDecryptAlgorithmFamily.

######## 2. CsmAEADDecryptAlgorithmModeCustom

- **UUID**: `1d192f2d-3ee5-4c04-840a-9b98402c9fec`
- **参数名**: `CsmAEADDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmAEADDecryptAlgorithmFamiliy

- **UUID**: `a1cb1a6c-5691-450a-90b5-8345448f00c2`
- **参数名**: `CsmAEADDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADDecryptAlgorithmMode

- **UUID**: `a1184a25-3707-472a-aa82-fee42f93bb1e`
- **参数名**: `CsmAEADDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmAEADDecryptProcessing

- **UUID**: `afba8b6e-7465-4474-9630-84c6f3208639`
- **参数名**: `CsmAEADDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CsmAEADDecryptKeyRef

- **UUID**: `b5a0cf4d-314f-4eb2-994c-e02a2cb01647`
- **引用名**: `CsmAEADDecryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that decryption primitive.

######## 2. CsmAEADDecryptQueueRef

- **UUID**: `94dddc37-a55c-4ce4-9606-6f4e39a46fbf`
- **引用名**: `CsmAEADDecryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that decryption primitive.

##### 11. CsmAEADEncrypt

**容器属性**:

- **UUID**: `291d8ff1-5965-48dd-8225-92258399195a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configuration of AEAD encryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `e74cce7c-8f3c-429a-9fef-e47a222c8641`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `7de3cf6f-8066-453c-b9df-b00cfc339694`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD encryption key in bytes

########## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `6bf021a4-c465-4f38-9efd-c79b55cb7472`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

########## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `8f7c6f2a-f15e-4edc-9903-a4769b9be669`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output ciphertext length in bytes

########## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `8141367d-8ba0-43bf-b352-f9d3d0e9c97d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

########## 5. CsmAEADEncryptTagLength

- **UUID**: `16c80a2a-2521-4a39-9d26-94be17c35bba`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output Tag length in bytes

######### STRING 类型参数

########## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `db453e7a-f929-4ee7-b079-a69f6ed2de1e`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

########## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `593d4d36-cc4c-4d60-a640-3d51e3c0bbc1`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `44247018-817a-4c07-9d09-738087f0a12f`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmAEADEncryptAlgorithmMode

- **UUID**: `b9f7e510-bf5e-449e-bf06-4362033c7abd`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmAEADEncryptProcessing

- **UUID**: `a3064817-3b35-451c-9fba-b97a489ecb30`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. CsmAEADEncryptKeyRef

- **UUID**: `92414fc6-7e7b-414b-81a9-78d0ff2e369b`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that encryption primitive.

########## 2. CsmAEADEncryptQueueRef

- **UUID**: `25c269ce-976c-4db3-af94-566b5de1570e`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that encryption primitive.

##### 12. CsmAEADEncryptConfig

**容器属性**:

- **UUID**: `e74cce7c-8f3c-429a-9fef-e47a222c8641`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAEADEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. CsmAEADEncryptAlgorithmKeyLength

- **UUID**: `7de3cf6f-8066-453c-b9df-b00cfc339694`
- **参数名**: `CsmAEADEncryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the AEAD encryption key in bytes

######## 2. CsmAEADEncryptAssociatedDataMaxLength

- **UUID**: `6bf021a4-c465-4f38-9efd-c79b55cb7472`
- **参数名**: `CsmAEADEncryptAssociatedDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input associated data length in bytes

######## 3. CsmAEADEncryptCiphertextMaxLength

- **UUID**: `8f7c6f2a-f15e-4edc-9903-a4769b9be669`
- **参数名**: `CsmAEADEncryptCiphertextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output ciphertext length in bytes

######## 4. CsmAEADEncryptPlaintextMaxLength

- **UUID**: `8141367d-8ba0-43bf-b352-f9d3d0e9c97d`
- **参数名**: `CsmAEADEncryptPlaintextMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

######## 5. CsmAEADEncryptTagLength

- **UUID**: `16c80a2a-2521-4a39-9d26-94be17c35bba`
- **参数名**: `CsmAEADEncryptTagLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output Tag length in bytes

####### STRING 类型参数

######## 1. CsmAEADEncryptAlgorithmFamilyCustom

- **UUID**: `db453e7a-f929-4ee7-b079-a69f6ed2de1e`
- **参数名**: `CsmAEADEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmAEADEncryptAlgorithmFamily.

######## 2. CsmAEADEncryptAlgorithmModeCustom

- **UUID**: `593d4d36-cc4c-4d60-a640-3d51e3c0bbc1`
- **参数名**: `CsmAEADEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmAEADEncryptAlgorithmFamiliy

- **UUID**: `44247018-817a-4c07-9d09-738087f0a12f`
- **参数名**: `CsmAEADEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_3DES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_AES` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmAEADEncryptAlgorithmMode

- **UUID**: `b9f7e510-bf5e-449e-bf06-4362033c7abd`
- **参数名**: `CsmAEADEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_GCM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmAEADEncryptProcessing

- **UUID**: `a3064817-3b35-451c-9fba-b97a489ecb30`
- **参数名**: `CsmAEADEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CsmAEADEncryptKeyRef

- **UUID**: `92414fc6-7e7b-414b-81a9-78d0ff2e369b`
- **引用名**: `CsmAEADEncryptKeyRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmKey`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmKeys/CsmKey`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the key used for that encryption primitive.

######## 2. CsmAEADEncryptQueueRef

- **UUID**: `25c269ce-976c-4db3-af94-566b5de1570e`
- **引用名**: `CsmAEADEncryptQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to the queue used for that encryption primitive.

##### 13. CsmDecrypt

**容器属性**:

- **UUID**: `46e267a3-d80d-47d7-a6fa-cb5043e82778`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of Decryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmDecryptConfig

**容器属性**:

- **UUID**: `70f0bc96-eee5-467a-9e61-4685c54041c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `02da7cab-eba0-48ef-8d37-93c51c8d4235`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the encryption key in bytes

########## 2. CsmDecryptDataMaxLength

- **UUID**: `1fe43d94-68f5-4d8f-978a-f2beff28f8dd`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext length in bytes

########## 3. CsmDecryptResultMaxLength

- **UUID**: `ec875ce6-56bb-4a13-b18c-c9661079c293`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output plaintext length in bytes

######### STRING 类型参数

########## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `18ce426e-9a84-42a8-85c9-742b1a236180`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

########## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `c5e762ce-2a8e-4dea-8a69-64319c3ab4e2`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `23ae0e82-92a9-422f-8907-8800ccbfd491`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `b0ca8007-09d0-483c-a315-70ae3a828a44`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmDecryptAlgorithmMode

- **UUID**: `87f3baca-123a-40d2-ab1c-67a609eb4dbb`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `f03e2853-49cc-4b88-9297-acfe4b9676ee`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmDecryptProcessing

- **UUID**: `350fc09d-2fc3-4427-a4e4-5cdb52540dce`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 14. CsmDecryptConfig

**容器属性**:

- **UUID**: `70f0bc96-eee5-467a-9e61-4685c54041c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDecryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM decryption interface. The container name serves as a symbolic name for the identifier of an decryption interface.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. CsmDecryptAlgorithmKeyLength

- **UUID**: `02da7cab-eba0-48ef-8d37-93c51c8d4235`
- **参数名**: `CsmDecryptAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the encryption key in bytes

######## 2. CsmDecryptDataMaxLength

- **UUID**: `1fe43d94-68f5-4d8f-978a-f2beff28f8dd`
- **参数名**: `CsmDecryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input ciphertext length in bytes

######## 3. CsmDecryptResultMaxLength

- **UUID**: `ec875ce6-56bb-4a13-b18c-c9661079c293`
- **参数名**: `CsmDecryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output plaintext length in bytes

####### STRING 类型参数

######## 1. CsmDecryptAlgorithmFamilyCustom

- **UUID**: `18ce426e-9a84-42a8-85c9-742b1a236180`
- **参数名**: `CsmDecryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmDecryptAlgorithmFamily.

######## 2. CsmDecryptAlgorithmModeCustom

- **UUID**: `c5e762ce-2a8e-4dea-8a69-64319c3ab4e2`
- **参数名**: `CsmDecryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmDecryptAlgorithmSecondaryFamilyCustom

- **UUID**: `23ae0e82-92a9-422f-8907-8800ccbfd491`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmDecryptAlgorithmFamiliy

- **UUID**: `b0ca8007-09d0-483c-a315-70ae3a828a44`
- **参数名**: `CsmDecryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmDecryptAlgorithmMode

- **UUID**: `87f3baca-123a-40d2-ab1c-67a609eb4dbb`
- **参数名**: `CsmDecryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmDecryptAlgorithmSecondaryFamily

- **UUID**: `f03e2853-49cc-4b88-9297-acfe4b9676ee`
- **参数名**: `CsmDecryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 4. CsmDecryptProcessing

- **UUID**: `350fc09d-2fc3-4427-a4e4-5cdb52540dce`
- **参数名**: `CsmDecryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 15. CsmEncrypt

**容器属性**:

- **UUID**: `3f4b7ccf-df57-454a-86db-54556e64957c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of Encryption primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmEncryptConfig

**容器属性**:

- **UUID**: `0714939b-250c-4472-8483-d555cab5d6ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmEncryptDataMaxLength

- **UUID**: `6e378d3e-eb6d-45ac-9fa1-3cb39366237d`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

########## 2. CsmEncryptResultMaxLength

- **UUID**: `c809b99b-cb37-46f3-b5de-d54a58c7952a`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output cipher length in bytes

######### STRING 类型参数

########## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `e6e09321-1edc-405b-b19a-22cc81b1076c`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

########## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `48b668ed-5a9d-4900-ae5e-b9eb6833b076`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `3a45778b-dccf-4f3d-bd22-ebdeb04c9292`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

######### ENUMERATION 类型参数

########## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `b7865263-d6a8-4a50-80ad-2c064e4648be`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmEncryptAlgorithmMode

- **UUID**: `64c306cf-0947-4016-bd96-b398aaad3d3f`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `572d8304-0329-4bab-8d72-49c9a9452dd5`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmEncryptProcessing

- **UUID**: `b31a4d25-56d8-419b-9280-7c6c91cb5194`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 16. CsmEncryptConfig

**容器属性**:

- **UUID**: `0714939b-250c-4472-8483-d555cab5d6ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmEncryptConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM encryption interface. The container name serves as a symbolic name for the identifier of an encryption interface.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CsmEncryptDataMaxLength

- **UUID**: `6e378d3e-eb6d-45ac-9fa1-3cb39366237d`
- **参数名**: `CsmEncryptDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input plaintext length in bytes

######## 2. CsmEncryptResultMaxLength

- **UUID**: `c809b99b-cb37-46f3-b5de-d54a58c7952a`
- **参数名**: `CsmEncryptResultMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the output cipher length in bytes

####### STRING 类型参数

######## 1. CsmEncryptAlgorithmFamilyCustom

- **UUID**: `e6e09321-1edc-405b-b19a-22cc81b1076c`
- **参数名**: `CsmEncryptAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmEncryptAlgorithmFamily.

######## 2. CsmEncryptAlgorithmModeCustom

- **UUID**: `48b668ed-5a9d-4900-ae5e-b9eb6833b076`
- **参数名**: `CsmEncryptAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmEncryptAlgorithmSecondaryFamilyCustom

- **UUID**: `3a45778b-dccf-4f3d-bd22-ebdeb04c9292`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service

####### ENUMERATION 类型参数

######## 1. CsmEncryptAlgorithmFamiliy

- **UUID**: `b7865263-d6a8-4a50-80ad-2c064e4648be`
- **参数名**: `CsmEncryptAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmEncryptAlgorithmMode

- **UUID**: `64c306cf-0947-4016-bd96-b398aaad3d3f`
- **参数名**: `CsmEncryptAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmEncryptAlgorithmSecondaryFamily

- **UUID**: `572d8304-0329-4bab-8d72-49c9a9452dd5`
- **参数名**: `CsmEncryptAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

######## 4. CsmEncryptProcessing

- **UUID**: `b31a4d25-56d8-419b-9280-7c6c91cb5194`
- **参数名**: `CsmEncryptProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 17. CsmHash

**容器属性**:

- **UUID**: `ffe193d3-66e3-4771-bc96-2f0034e89ec9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHash`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for Hash Configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmHashConfig

**容器属性**:

- **UUID**: `2cc4aa34-4ee8-40f9-b31d-214325317379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmHashDataMaxLength

- **UUID**: `b2d54e57-087d-4d3c-8643-c0d33d8ac296`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

########## 2. CsmHashResultLength

- **UUID**: `5a3e0d0d-17df-4d63-94b8-ec6d0c16ecb4`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output hash length in bytes

######### STRING 类型参数

########## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `236996b7-c73d-4be2-8aad-03c1fef3e31c`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

########## 2. CsmHashAlgorithmModeCustom

- **UUID**: `af6c08c7-5241-4643-af19-3003ff3887b9`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom primitive mode.

########## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `e1396f5c-2564-435f-8f71-14f363f92a61`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmHashAlgorithmFamiliy

- **UUID**: `0e3e2464-c73d-4ffe-885c-b9c11f22a394`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmHashAlgorithmMode

- **UUID**: `92882e2f-45b6-4090-8595-4e24760418db`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmHashAlgorithmSecondaryFamily

- **UUID**: `a9336cbc-de94-44d9-8f6a-064a19bac97f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmHashProcessing

- **UUID**: `5a743541-d1ce-4ada-9121-344647e8003c`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 18. CsmHashConfig

**容器属性**:

- **UUID**: `2cc4aa34-4ee8-40f9-b31d-214325317379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM hash. The container name serves as a symbolic name for the identifier of a key configuration.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CsmHashDataMaxLength

- **UUID**: `b2d54e57-087d-4d3c-8643-c0d33d8ac296`
- **参数名**: `CsmHashDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

######## 2. CsmHashResultLength

- **UUID**: `5a3e0d0d-17df-4d63-94b8-ec6d0c16ecb4`
- **参数名**: `CsmHashResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output hash length in bytes

####### STRING 类型参数

######## 1. CsmHashAlgorithmFamilyCustom

- **UUID**: `236996b7-c73d-4be2-8aad-03c1fef3e31c`
- **参数名**: `CsmHashAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmHashAlgorithmFamily.

######## 2. CsmHashAlgorithmModeCustom

- **UUID**: `af6c08c7-5241-4643-af19-3003ff3887b9`
- **参数名**: `CsmHashAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom primitive mode.

######## 3. CsmHashAlgorithmSecondaryFamilyCustom

- **UUID**: `e1396f5c-2564-435f-8f71-14f363f92a61`
- **参数名**: `CsmHashAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmHashAlgorithmFamiliy

- **UUID**: `0e3e2464-c73d-4ffe-885c-b9c11f22a394`
- **参数名**: `CsmHashAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmHashAlgorithmMode

- **UUID**: `92882e2f-45b6-4090-8595-4e24760418db`
- **参数名**: `CsmHashAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOMODE_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmHashAlgorithmSecondaryFamily

- **UUID**: `a9336cbc-de94-44d9-8f6a-064a19bac97f`
- **参数名**: `CsmHashAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

######## 4. CsmHashProcessing

- **UUID**: `5a743541-d1ce-4ada-9121-344647e8003c`
- **参数名**: `CsmHashProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 19. CsmMacGenerate

**容器属性**:

- **UUID**: `76c1ab44-cf00-4731-a9db-6f0a9f1c10cb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of MacGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `c2671334-6ddd-435d-82aa-ad0dca40aeea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `4127714a-c247-426a-a1bd-d10ba5e97cb9`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the MAC key in bytes

########## 2. CsmMacGenerateDataMaxLength

- **UUID**: `667bf375-f2f6-42c6-937b-41c851114f7e`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

########## 3. CsmMacGenerateResultLength

- **UUID**: `5850299b-6489-4341-b9e9-93bc30da7655`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output MAC length in bytes

######### STRING 类型参数

########## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `5d1b05de-53d1-4315-b2bf-7df6413955e8`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family,

########## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `9604fe54-b9ba-413c-bfea-2676a8ebbc2e`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f23baa62-39ce-43fd-bca9-edeb8e9ab805`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

######### ENUMERATION 类型参数

########## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `40188569-ca18-4705-bcd2-cf85d544b99e`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacGenerateAlgorithmMode

- **UUID**: `193d295a-43a0-4a74-81f7-3d5059e5f603`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `b2679827-345c-47a8-9b74-f999c9ee15c9`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 4. CsmMacGenerateProcessing

- **UUID**: `a422fc73-9626-413c-8faa-f6adac56081c`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 20. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `c2671334-6ddd-435d-82aa-ad0dca40aeea`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM mac generation interface. The container name serves as a symbolic name for the identifier of a MAC generation interface.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacGenerateAlgorithmKeyLength

- **UUID**: `4127714a-c247-426a-a1bd-d10ba5e97cb9`
- **参数名**: `CsmMacGenerateAlgorithmKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the MAC key in bytes

######## 2. CsmMacGenerateDataMaxLength

- **UUID**: `667bf375-f2f6-42c6-937b-41c851114f7e`
- **参数名**: `CsmMacGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length in bytes

######## 3. CsmMacGenerateResultLength

- **UUID**: `5850299b-6489-4341-b9e9-93bc30da7655`
- **参数名**: `CsmMacGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output MAC length in bytes

####### STRING 类型参数

######## 1. CsmMacGenerateAlgorithmFamilyCustom

- **UUID**: `5d1b05de-53d1-4315-b2bf-7df6413955e8`
- **参数名**: `CsmMacGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the name of the custom algorithm family,

######## 2. CsmMacGenerateAlgorithmModeCustom

- **UUID**: `9604fe54-b9ba-413c-bfea-2676a8ebbc2e`
- **参数名**: `CsmMacGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmMacGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `f23baa62-39ce-43fd-bca9-edeb8e9ab805`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmHashAlgorithmSecondaryFamilyCustom.

####### ENUMERATION 类型参数

######## 1. CsmMacGenerateAlgorithmFamiliy

- **UUID**: `40188569-ca18-4705-bcd2-cf85d544b99e`
- **参数名**: `CsmMacGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacGenerateAlgorithmMode

- **UUID**: `193d295a-43a0-4a74-81f7-3d5059e5f603`
- **参数名**: `CsmMacGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmMacGenerateAlgorithmSecondaryFamily

- **UUID**: `b2679827-345c-47a8-9b74-f999c9ee15c9`
- **参数名**: `CsmMacGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 4. CsmMacGenerateProcessing

- **UUID**: `a422fc73-9626-413c-8faa-f6adac56081c`
- **参数名**: `CsmMacGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 21. CsmMacVerify

**容器属性**:

- **UUID**: `8e223550-7ebc-44ce-84c7-4d05411daa04`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of MacVerify primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `aa358ae1-2419-4ccd-913d-2f79785805de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CsmMacVerifyCompareLength

- **UUID**: `8264e0ae-cee8-43ed-9fa0-9e553543a5b8`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input MAC length, that shall be verified, in BITS

########## 2. CsmMacVerifyDataMaxLength

- **UUID**: `b273ce86-523f-4ffc-bae5-338a2349b4d3`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length, for whichs MAC shall be verified, in bytes

######### STRING 类型参数

########## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `b24ba482-9b00-4ddf-bb79-cd7db6e9a952`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service

########## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ddeadbff-a998-4e01-b761-0b54a3b66474`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

######### ENUMERATION 类型参数

########## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `3a1f9128-e737-4548-a8a1-60ac975c10b5`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `eb37521b-6cfb-4292-9cbd-4607934da293`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

########## 3. CsmMacVerifyProcessing

- **UUID**: `9ef96e0b-55be-41ed-b00b-4b13e6a12af3`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 22. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `aa358ae1-2419-4ccd-913d-2f79785805de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM MAC verification interface. The container name serves as a symbolic name for the identifier of a MAC generation interface

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacVerifyCompareLength

- **UUID**: `8264e0ae-cee8-43ed-9fa0-9e553543a5b8`
- **参数名**: `CsmMacVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input MAC length, that shall be verified, in BITS

######## 2. CsmMacVerifyDataMaxLength

- **UUID**: `b273ce86-523f-4ffc-bae5-338a2349b4d3`
- **参数名**: `CsmMacVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max size of the input data length, for whichs MAC shall be verified, in bytes

####### STRING 类型参数

######## 1. CsmMacVerifyAlgorithmFamilyCustom

- **UUID**: `b24ba482-9b00-4ddf-bb79-cd7db6e9a952`
- **参数名**: `CsmMacVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service

######## 2. CsmMacVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `ddeadbff-a998-4e01-b761-0b54a3b66474`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the second the name of the custom algorithm, if CRYPTO_ALGOFAM_CUSTOM is set as CsmMacVerifyAlgorithmSecondaryFamily

####### ENUMERATION 类型参数

######## 1. CsmMacVerifyAlgorithmFamiliy

- **UUID**: `3a1f9128-e737-4548-a8a1-60ac975c10b5`
- **参数名**: `CsmMacVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmMacVerifyAlgorithmSecondaryFamily

- **UUID**: `eb37521b-6cfb-4292-9cbd-4607934da293`
- **参数名**: `CsmMacVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the secondary algorithm family used for the crypto service

######## 3. CsmMacVerifyProcessing

- **UUID**: `9ef96e0b-55be-41ed-b00b-4b13e6a12af3`
- **参数名**: `CsmMacVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 23. CsmRandomGenerate

**容器属性**:

- **UUID**: `ec02cfc2-8484-454b-a808-9a61cc8c8f71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of RandomGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `e0f13b04-04b6-4c86-a85a-f035dd5bb7e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CsmRandomGenerateResultLength

- **UUID**: `b3d30c52-8e6b-4cac-a1f5-54adf3220495`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the random generate key in bytes

######### STRING 类型参数

########## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `fc859224-bea1-48ae-8fe3-525653d8ee10`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

########## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `bcae0710-fa1d-499d-b70b-023ba0d2f70b`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

########## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `57b3224f-6783-458b-aa80-3ffbdca65503`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `e13eb029-eab0-429e-b592-b6c2daa56d33`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmRandomGenerateAlgorithmMode

- **UUID**: `371136e3-8c98-41f2-aeb1-dc1a3b0b4346`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `b30aa787-6af6-457c-b8c3-53f2dde767ba`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

########## 4. CsmRandomGenerateProcessing

- **UUID**: `8c64cdef-3c23-42fa-9458-e8323e5a2430`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 24. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `e0f13b04-04b6-4c86-a85a-f035dd5bb7e9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM random generator. The container name serves as a symbolic name for the identifier of a random generator configuration.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. CsmRandomGenerateResultLength

- **UUID**: `b3d30c52-8e6b-4cac-a1f5-54adf3220495`
- **参数名**: `CsmRandomGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the random generate key in bytes

####### STRING 类型参数

######## 1. CsmRandomGenerateAlgorithmFamilyCustom

- **UUID**: `fc859224-bea1-48ae-8fe3-525653d8ee10`
- **参数名**: `CsmRandomGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomAlgorithmFamily

######## 2. CsmRandomGenerateAlgorithmModeCustom

- **UUID**: `bcae0710-fa1d-499d-b70b-023ba0d2f70b`
- **参数名**: `CsmRandomGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmRandomGenerateAlgorithmFamily.

######## 3. CsmRandomGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `57b3224f-6783-458b-aa80-3ffbdca65503`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as Csm RandomAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmRandomGenerateAlgorithmFamiliy

- **UUID**: `e13eb029-eab0-429e-b592-b6c2daa56d33`
- **参数名**: `CsmRandomGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmRandomGenerateAlgorithmMode

- **UUID**: `371136e3-8c98-41f2-aeb1-dc1a3b0b4346`
- **参数名**: `CsmRandomGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmRandomGenerateAlgorithmSecondaryFamily

- **UUID**: `b30aa787-6af6-457c-b8c3-53f2dde767ba`
- **参数名**: `CsmRandomGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_NOT_SET` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service

######## 4. CsmRandomGenerateProcessing

- **UUID**: `8c64cdef-3c23-42fa-9458-e8323e5a2430`
- **参数名**: `CsmRandomGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 25. CsmSecureCounter

**容器属性**:

- **UUID**: `ae8fcb3a-3062-4256-a7a5-fc85315fba62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounter`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SecureCounter primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `3cc03b6b-07cd-4ae6-b4a0-015f78d5f527`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CsmSecureCounterQueueRef

- **UUID**: `793a134a-bab0-4c8b-92cd-1a983c713dc2`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used. Queue is referred in Job.
		This parameter refers to the queue used for that secure counter.

##### 26. CsmSecureCounterConfig

**容器属性**:

- **UUID**: `3cc03b6b-07cd-4ae6-b4a0-015f78d5f527`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSecureCounterConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM counter. The container name serves as a symbolic name for the identifier of a secure counter configuration.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CsmSecureCounterQueueRef

- **UUID**: `793a134a-bab0-4c8b-92cd-1a983c713dc2`
- **引用名**: `CsmSecureCounterQueueRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CsmQueue`
- **完整路径**: `/AUTOSAR/EcucDefs/Csm/CsmQueues/CsmQueue`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not used. Queue is referred in Job.
		This parameter refers to the queue used for that secure counter.

##### 27. CsmSignatureGenerate

**容器属性**:

- **UUID**: `913d2545-13ac-4c53-981c-83558b0ed28f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerate`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SignatureGenerate primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `12372ff1-ccaf-4025-b434-09f6e2abf3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `bd934cfe-20e9-4a41-a8b9-b03f4c3f7404`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length in bytes

########## 2. CsmSignatureGenerateKeyLength

- **UUID**: `3768ba31-9eef-4607-a5df-1784aecf4b07`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the signature generate key in bytes

########## 3. CsmSignatureGenerateResultLength

- **UUID**: `7d370d85-987d-47ba-937b-629c2b08efd3`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output signature length in bytes

######### STRING 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `98d26f76-c63a-4c1b-a4e6-68d2e458dc7b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service.

########## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `cb3f8a86-07d7-4858-ab41-563eebe4f954`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `5ff7ce61-5c6a-469d-9945-b21783480a5f`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `b03c8cdd-335b-4a99-bcb0-f56de0db845b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureGenerateAlgorithmMode

- **UUID**: `caf4f4d1-064a-4b7a-86b2-56baff592e6f`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `831ec95b-fc47-4b7c-a3d2-d9b0100c573a`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 4. CsmSignatureGenerateProcessing

- **UUID**: `d803212c-5e03-45d5-87b5-5ee154a69c97`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 28. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `12372ff1-ccaf-4025-b434-09f6e2abf3f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature generation interface. The container name serves as a symbolic name for the identifier of signature generation interface.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureGenerateDataMaxLength

- **UUID**: `bd934cfe-20e9-4a41-a8b9-b03f4c3f7404`
- **参数名**: `CsmSignatureGenerateDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length in bytes

######## 2. CsmSignatureGenerateKeyLength

- **UUID**: `3768ba31-9eef-4607-a5df-1784aecf4b07`
- **参数名**: `CsmSignatureGenerateKeyLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the signature generate key in bytes

######## 3. CsmSignatureGenerateResultLength

- **UUID**: `7d370d85-987d-47ba-937b-629c2b08efd3`
- **参数名**: `CsmSignatureGenerateResultLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the output signature length in bytes

####### STRING 类型参数

######## 1. CsmSignatureGenerateAlgorithmFamilyCustom

- **UUID**: `98d26f76-c63a-4c1b-a4e6-68d2e458dc7b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service.

######## 2. CsmSignatureGenerateAlgorithmModeCustom

- **UUID**: `cb3f8a86-07d7-4858-ab41-563eebe4f954`
- **参数名**: `CsmSignatureGenerateAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmSignatureGenerateAlgorithmSecondaryFamilyCustom

- **UUID**: `5ff7ce61-5c6a-469d-9945-b21783480a5f`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the second name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is set as CsmSignatureGenerateAlgorithmSecondaryFamily.

####### ENUMERATION 类型参数

######## 1. CsmSignatureGenerateAlgorithmFamiliy

- **UUID**: `b03c8cdd-335b-4a99-bcb0-f56de0db845b`
- **参数名**: `CsmSignatureGenerateAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureGenerateAlgorithmMode

- **UUID**: `caf4f4d1-064a-4b7a-86b2-56baff592e6f`
- **参数名**: `CsmSignatureGenerateAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmSignatureGenerateAlgorithmSecondaryFamily

- **UUID**: `831ec95b-fc47-4b7c-a3d2-d9b0100c573a`
- **参数名**: `CsmSignatureGenerateAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRYPTO_ALGOFAM_NOT_SET`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 4. CsmSignatureGenerateProcessing

- **UUID**: `d803212c-5e03-45d5-87b5-5ee154a69c97`
- **参数名**: `CsmSignatureGenerateProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback

##### 29. CsmSignatureVerify

**容器属性**:

- **UUID**: `86ec2b03-ed09-48a8-9b17-0cbc21a0d0be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerify`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Configurations of SignatureVerify primitives

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `619a235d-53d8-47ce-b976-2abfbc4886d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CsmSignatureVerifyCompareLength

- **UUID**: `17ac44ee-4818-4575-90e7-4cafcec2d8e6`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

########## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `7b017ac6-521a-43de-9157-fdbf386df7d7`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

######### STRING 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `e0646614-cdcc-4655-9cea-e03a8454e7da`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

########## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `b44042b1-bd7f-4c61-952e-a8e050c3c889`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `081135af-8d85-4042-8587-cfe8564aaf2a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######### ENUMERATION 类型参数

########## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `5170fc84-26a0-4b6e-b180-4e9c9fcb0d39`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 2. CsmSignatureVerifyAlgorithmMode

- **UUID**: `3826b457-6bb3-408b-acfd-87dbca97fc65`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

########## 3. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `fc3181fd-48b8-4935-be61-bd186567e81a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

########## 4. CsmSignatureVerifyProcessing

- **UUID**: `4479e8a3-fe1c-4a38-891d-3ee77e67a830`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 30. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `619a235d-53d8-47ce-b976-2abfbc4886d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM signature verification interface. The container name serves as a symbolic name for the identifier of signature verification interface.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureVerifyCompareLength

- **UUID**: `17ac44ee-4818-4575-90e7-4cafcec2d8e6`
- **参数名**: `CsmSignatureVerifyCompareLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

######## 2. CsmSignatureVerifyDataMaxLength

- **UUID**: `7b017ac6-521a-43de-9157-fdbf386df7d7`
- **参数名**: `CsmSignatureVerifyDataMaxLength`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the input data length, for whichs signature shall be verified, in bytes

####### STRING 类型参数

######## 1. CsmSignatureVerifyAlgorithmFamilyCustom

- **UUID**: `e0646614-cdcc-4655-9cea-e03a8454e7da`
- **参数名**: `CsmSignatureVerifyAlgorithmFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

######## 2. CsmSignatureVerifyAlgorithmModeCustom

- **UUID**: `b44042b1-bd7f-4c61-952e-a8e050c3c889`
- **参数名**: `CsmSignatureVerifyAlgorithmModeCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom algorithm mode used for the crypto service

######## 3. CsmSignatureVerifyAlgorithmSecondaryFamilyCustom

- **UUID**: `081135af-8d85-4042-8587-cfe8564aaf2a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamilyCustom`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the custom secondary algorithm family used for the crypto service. This is the name of the custom algorithm family, if CRYPTO_ALGOFAM_CUSTOM is used as CsmSignatureVerifyAlgorithmFamily.

####### ENUMERATION 类型参数

######## 1. CsmSignatureVerifyAlgorithmFamiliy

- **UUID**: `5170fc84-26a0-4b6e-b180-4e9c9fcb0d39`
- **参数名**: `CsmSignatureVerifyAlgorithmFamiliy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOFAM_BRAINPOOL` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ECCNIST` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_ED25519` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOFAM_RSA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 2. CsmSignatureVerifyAlgorithmMode

- **UUID**: `3826b457-6bb3-408b-acfd-87dbca97fc65`
- **参数名**: `CsmSignatureVerifyAlgorithmMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRYPTO_ALGOMODE_CUSTOM` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_NOT_SET` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PKCS1_v1_5` (来源: AUTOSAR_ECUC)
  - `CRYPTO_ALGOMODE_RSASSA_PSS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm mode used for the crypto service

######## 3. CsmSignatureVerifyAlgorithmSecondaryFamily

- **UUID**: `fc3181fd-48b8-4935-be61-bd186567e81a`
- **参数名**: `CsmSignatureVerifyAlgorithmSecondaryFamily`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the algorithm family used for the crypto service. This parameter defines the most significant part of the algorithm.

######## 4. CsmSignatureVerifyProcessing

- **UUID**: `4479e8a3-fe1c-4a38-891d-3ee77e67a830`
- **参数名**: `CsmSignatureVerifyProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CSM_ASYNCHRONOUS` (来源: AUTOSAR_ECUC)
  - `CSM_SYNCHRONOUS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines how the interface shall be used for that primitive. Synchronous processing returns with the result while asynchronous processing returns without processing the job. The caller will be notified by the corresponding callback.

##### 31. CsmQueues

**容器属性**:

- **UUID**: `af440b9f-dd73-4d6c-87de-6cf07bb00884`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueues`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for CSM queue configurations

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmQueue

**容器属性**:

- **UUID**: `642d787c-395f-4b6e-98c4-85d30705ff95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueue`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM queue. The container name serves as a symbolic name for the identifier of a queue configuration.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CsmQueueSize

- **UUID**: `a36284d3-53ec-4e83-bd06-6c89f877480e`
- **参数名**: `CsmQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the CsmQueue. If jobs cannot be processed by the underlying hardware since the hardware is busy, the jobs stay in the prioritized queue. If the queue is full, the next job will be rejected.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CsmChannelRef

- **UUID**: `783ac688-7be8-48ed-871d-8460cc545eec`
- **引用名**: `CsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to the underlying Crypto Interface channel.

##### 32. CsmQueue

**容器属性**:

- **UUID**: `642d787c-395f-4b6e-98c4-85d30705ff95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmQueue`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Container for configuration of a CSM queue. The container name serves as a symbolic name for the identifier of a queue configuration.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmQueueSize

- **UUID**: `a36284d3-53ec-4e83-bd06-6c89f877480e`
- **参数名**: `CsmQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the CsmQueue. If jobs cannot be processed by the underlying hardware since the hardware is busy, the jobs stay in the prioritized queue. If the queue is full, the next job will be rejected.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CsmChannelRef

- **UUID**: `783ac688-7be8-48ed-871d-8460cc545eec`
- **引用名**: `CsmChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CryIfChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CryIf/CryIfChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refers to the underlying Crypto Interface channel.

##### 33. CsmAsymDecrypt

**容器属性**:

- **UUID**: `9fb26569-9a0b-4323-9feb-9baa4e40e55a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymDecrypt primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymDecryptMaxKeySize

- **UUID**: `f3a99177-88c1-46d9-a258-85ef728b089c`
- **参数名**: `CsmAsymDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymmetrical decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymDecryptConfig

**容器属性**:

- **UUID**: `b33dbb5e-eead-4c69-b15d-3c1021300354`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymDecryptInitConfiguration

- **UUID**: `7a8a00ad-e714-496d-9be9-85ac452b58c8`
- **参数名**: `CsmAsymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymDecryptPrimitiveName

- **UUID**: `82a4db8f-82eb-465c-97ef-6a0ee6e8d0b7`
- **参数名**: `CsmAsymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymDecrypt

- **UUID**: `0b3ddea5-649a-45f0-b305-afe222d28c58`
- **参数名**: `CsmCallbackAsymDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 34. CsmAsymDecryptConfig

**容器属性**:

- **UUID**: `b33dbb5e-eead-4c69-b15d-3c1021300354`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymDecryptInitConfiguration

- **UUID**: `7a8a00ad-e714-496d-9be9-85ac452b58c8`
- **参数名**: `CsmAsymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymDecryptPrimitiveName

- **UUID**: `82a4db8f-82eb-465c-97ef-6a0ee6e8d0b7`
- **参数名**: `CsmAsymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymDecrypt

- **UUID**: `0b3ddea5-649a-45f0-b305-afe222d28c58`
- **参数名**: `CsmCallbackAsymDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 35. CsmAsymEncrypt

**容器属性**:

- **UUID**: `2a67c3c0-6432-49e7-8849-31391d911793`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymEncrypt primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymEncryptMaxKeySize

- **UUID**: `0b6ee349-2a6a-4a67-9f9a-6b8158cda111`
- **参数名**: `CsmAsymEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymmetrical encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymEncryptConfig

**容器属性**:

- **UUID**: `b287df23-6fdf-4e05-9fa0-7e0606d98f75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymEncryptInitConfiguration

- **UUID**: `e54df844-7e7b-4ae1-89d5-7c55516d032c`
- **参数名**: `CsmAsymEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymEncryptPrimitiveName

- **UUID**: `30bec222-c614-4f64-89e7-6f6fad972277`
- **参数名**: `CsmAsymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymEncrypt

- **UUID**: `7c0c1644-16fe-4041-b19f-7e86e7f269e5`
- **参数名**: `CsmCallbackAsymEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 36. CsmAsymEncryptConfig

**容器属性**:

- **UUID**: `b287df23-6fdf-4e05-9fa0-7e0606d98f75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymEncryptInitConfiguration

- **UUID**: `e54df844-7e7b-4ae1-89d5-7c55516d032c`
- **参数名**: `CsmAsymEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymEncryptPrimitiveName

- **UUID**: `30bec222-c614-4f64-89e7-6f6fad972277`
- **参数名**: `CsmAsymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymEncrypt

- **UUID**: `7c0c1644-16fe-4041-b19f-7e86e7f269e5`
- **参数名**: `CsmCallbackAsymEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 37. CsmAsymPrivateKeyExtract

**容器属性**:

- **UUID**: `c8da83ed-7c91-436a-86bc-f377fe360bac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyExtract`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyExtract primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPrivateKeyExtractMaxKeySize

- **UUID**: `34727ec9-ff79-4c90-807f-4e04e91afedd`
- **参数名**: `CsmAsymPrivateKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymmetrical private key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymPrivateKeyExtractConfig

**容器属性**:

- **UUID**: `fdfc95a1-d1c0-47a9-8e22-2fa0920ef5f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyExtract.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymPrivateKeyExtractInitConfiguration

- **UUID**: `e953f171-fe5a-4bfa-a772-b99d49187f3e`
- **参数名**: `CsmAsymPrivateKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymPrivateKeyExtractPrimitiveName

- **UUID**: `9a7cf245-a086-40f5-979e-00b46308981d`
- **参数名**: `CsmAsymPrivateKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymPrivateKeyExtract

- **UUID**: `4413f7a2-6bb4-4d84-b09c-ec164e56326c`
- **参数名**: `CsmCallbackAsymPrivateKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 38. CsmAsymPrivateKeyExtractConfig

**容器属性**:

- **UUID**: `fdfc95a1-d1c0-47a9-8e22-2fa0920ef5f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyExtract.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymPrivateKeyExtractInitConfiguration

- **UUID**: `e953f171-fe5a-4bfa-a772-b99d49187f3e`
- **参数名**: `CsmAsymPrivateKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymPrivateKeyExtractPrimitiveName

- **UUID**: `9a7cf245-a086-40f5-979e-00b46308981d`
- **参数名**: `CsmAsymPrivateKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymPrivateKeyExtract

- **UUID**: `4413f7a2-6bb4-4d84-b09c-ec164e56326c`
- **参数名**: `CsmCallbackAsymPrivateKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 39. CsmAsymPrivateKeyWrapAsym

**容器属性**:

- **UUID**: `85b8b27c-eb6e-4e19-b5bc-e817830be05d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapAsym`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyWrapSym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPrivateKeyWrapAsymMaxPrivKeySize

- **UUID**: `5a5d15a5-9481-4c75-83f9-741a7fe84e7c`
- **参数名**: `CsmAsymPrivateKeyWrapAsymMaxPrivKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private key types used in all CRY primitives which implement an asymmetrical private key wrapping.

######## 2. CsmAsymPrivateKeyWrapAsymMaxPubKeySize

- **UUID**: `5f72fc17-a543-4e42-919c-dfa5ea76f555`
- **参数名**: `CsmAsymPrivateKeyWrapAsymMaxPubKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all public key types used in all CRY primitives which implement an asymmetrical private key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymPrivateKeyWrapAsymConfig

**容器属性**:

- **UUID**: `334df2e0-b37d-4945-b31d-0b6d195de61e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapAsymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymPrivateKeyWrapAsymInitConfiguration

- **UUID**: `8cf73cdc-cad2-4791-84c9-c6c1a841500c`
- **参数名**: `CsmAsymPrivateKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymPrivateKeyWrapAsymPrimitiveName

- **UUID**: `39040f9e-f52b-44e1-861d-6bdaaab899b9`
- **参数名**: `CsmAsymPrivateKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymPrivateKeyWrapAsym

- **UUID**: `1877e760-b6ba-4b6f-95c2-5ab73ac418b4`
- **参数名**: `CsmCallbackAsymPrivateKeyWrapAsym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 40. CsmAsymPrivateKeyWrapAsymConfig

**容器属性**:

- **UUID**: `334df2e0-b37d-4945-b31d-0b6d195de61e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapAsymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymPrivateKeyWrapAsymInitConfiguration

- **UUID**: `8cf73cdc-cad2-4791-84c9-c6c1a841500c`
- **参数名**: `CsmAsymPrivateKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymPrivateKeyWrapAsymPrimitiveName

- **UUID**: `39040f9e-f52b-44e1-861d-6bdaaab899b9`
- **参数名**: `CsmAsymPrivateKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymPrivateKeyWrapAsym

- **UUID**: `1877e760-b6ba-4b6f-95c2-5ab73ac418b4`
- **参数名**: `CsmCallbackAsymPrivateKeyWrapAsym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 41. CsmAsymPrivateKeyWrapSym

**容器属性**:

- **UUID**: `8868b248-5bc2-40ff-9f1f-e1cadaead327`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapSym`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPrivateKeyWrapSym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPrivateKeyWrapSymMaxPrivKeySize

- **UUID**: `acc76fd2-5f5b-460b-b603-a83921cf3022`
- **参数名**: `CsmAsymPrivateKeyWrapSymMaxPrivKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CRY primitives which implement an asymetric private key wrapping.

######## 2. CsmAsymPrivateKeyWrapSymMaxSymKeySize

- **UUID**: `49d06f9c-b820-4219-971a-2adc568a370f`
- **参数名**: `CsmAsymPrivateKeyWrapSymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymetrical private key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymPrivateKeyWrapSymConfig

**容器属性**:

- **UUID**: `9c201e5c-59e1-4c2c-9b8e-a27745041a1a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapSymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapSym. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymPrivateKeyWrapSymInitConfiguration

- **UUID**: `52aaef53-bdcb-4b4b-bf3f-f670bb36f036`
- **参数名**: `CsmAsymPrivateKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymPrivateKeyWrapSymPrimitiveName

- **UUID**: `7550c651-8e5d-44c1-af55-0c700c2f71ff`
- **参数名**: `CsmAsymPrivateKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymPrivateKeyWrapSym

- **UUID**: `71af6d12-3e82-40d5-95b3-c47b7fcdb2e9`
- **参数名**: `CsmCallbackAsymPrivateKeyWrapSym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 42. CsmAsymPrivateKeyWrapSymConfig

**容器属性**:

- **UUID**: `9c201e5c-59e1-4c2c-9b8e-a27745041a1a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPrivateKeyWrapSymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPrivateKeyWrapSym. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymPrivateKeyWrapSymInitConfiguration

- **UUID**: `52aaef53-bdcb-4b4b-bf3f-f670bb36f036`
- **参数名**: `CsmAsymPrivateKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymPrivateKeyWrapSymPrimitiveName

- **UUID**: `7550c651-8e5d-44c1-af55-0c700c2f71ff`
- **参数名**: `CsmAsymPrivateKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymPrivateKeyWrapSym

- **UUID**: `71af6d12-3e82-40d5-95b3-c47b7fcdb2e9`
- **参数名**: `CsmCallbackAsymPrivateKeyWrapSym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 43. CsmAsymPublicKeyExtract

**容器属性**:

- **UUID**: `329fae2f-917f-41c5-ace8-e095bf5c678c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPublicKeyExtract`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of AsymPublicKeyExtract primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmAsymPublicKeyExtractMaxKeySize

- **UUID**: `f9f03f1e-8197-431d-9ace-263e82f0f4c6`
- **参数名**: `CsmAsymPublicKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymmetrical public key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmAsymPublicKeyExtractConfig

**容器属性**:

- **UUID**: `ac2288e0-4851-4481-b126-5a33295f3da6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPublicKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPublicKeyExtract.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmAsymPublicKeyExtractInitConfiguration

- **UUID**: `fbe5d199-c287-427c-a8ff-baa9db0ce995`
- **参数名**: `CsmAsymPublicKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmAsymPublicKeyExtractPrimitiveName

- **UUID**: `ccee8c30-6adc-4899-833c-66114acc3b00`
- **参数名**: `CsmAsymPublicKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackAsymPublicKeyExtract

- **UUID**: `bd995c50-095c-46e1-83b4-61ac3f5f49ed`
- **参数名**: `CsmCallbackAsymPublicKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 44. CsmAsymPublicKeyExtractConfig

**容器属性**:

- **UUID**: `ac2288e0-4851-4481-b126-5a33295f3da6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmAsymPublicKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service AsymPublicKeyExtract.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmAsymPublicKeyExtractInitConfiguration

- **UUID**: `fbe5d199-c287-427c-a8ff-baa9db0ce995`
- **参数名**: `CsmAsymPublicKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmAsymPublicKeyExtractPrimitiveName

- **UUID**: `ccee8c30-6adc-4899-833c-66114acc3b00`
- **参数名**: `CsmAsymPublicKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackAsymPublicKeyExtract

- **UUID**: `bd995c50-095c-46e1-83b4-61ac3f5f49ed`
- **参数名**: `CsmCallbackAsymPublicKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 45. CsmChecksum

**容器属性**:

- **UUID**: `0716dc66-c745-4159-89e9-47ed37ed7e29`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmChecksum`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of Checksum primitives.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmChecksumConfig

**容器属性**:

- **UUID**: `1a5f8a95-da00-41ba-aa41-0672bfe530b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmChecksumConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service Checksum. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmChecksumInitConfiguration

- **UUID**: `e6489ae3-2a12-4220-af68-f299d95ed8a4`
- **参数名**: `CsmChecksumInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmChecksumPrimitiveName

- **UUID**: `bbfddf01-1d80-4782-9238-906a2a44d6f0`
- **参数名**: `CsmChecksumPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackChecksum

- **UUID**: `5892ddc8-24bc-4547-8962-3942944d0d03`
- **参数名**: `CsmCallbackChecksum`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 46. CsmChecksumConfig

**容器属性**:

- **UUID**: `1a5f8a95-da00-41ba-aa41-0672bfe530b0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmChecksumConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service Checksum. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmChecksumInitConfiguration

- **UUID**: `e6489ae3-2a12-4220-af68-f299d95ed8a4`
- **参数名**: `CsmChecksumInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmChecksumPrimitiveName

- **UUID**: `bbfddf01-1d80-4782-9238-906a2a44d6f0`
- **参数名**: `CsmChecksumPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackChecksum

- **UUID**: `5892ddc8-24bc-4547-8962-3942944d0d03`
- **参数名**: `CsmCallbackChecksum`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 47. CsmDemEventParameterRefs

**容器属性**:

- **UUID**: `6fadaebb-8cae-40ce-8d05-7861d1f532de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CSM_E_INIT_FAILED

- **UUID**: `99865f68-093b-4d38-8a64-527b7a7ceee4`
- **引用名**: `CSM_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Initialization of CSM module failed" has occured.

##### 48. CsmHash

**容器属性**:

- **UUID**: `fe68712a-e9a3-4fe5-b2d5-038964094a84`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHash`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of Hash primitives.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmHashConfig

**容器属性**:

- **UUID**: `ca3af9e5-dfee-488e-875f-482361bf96c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configurations for the Hash service. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmHashInitConfiguration

- **UUID**: `1b548c2f-d7f9-4296-8053-0e0b4b9c978f`
- **参数名**: `CsmHashInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmHashPrimitiveName

- **UUID**: `c3f688e4-a216-4062-a17d-0a638dd90c9e`
- **参数名**: `CsmHashPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackHash

- **UUID**: `027f32fc-55af-4872-84d4-f89dab4c3888`
- **参数名**: `CsmCallbackHash`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 49. CsmHashConfig

**容器属性**:

- **UUID**: `ca3af9e5-dfee-488e-875f-482361bf96c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmHashConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configurations for the Hash service. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmHashInitConfiguration

- **UUID**: `1b548c2f-d7f9-4296-8053-0e0b4b9c978f`
- **参数名**: `CsmHashInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmHashPrimitiveName

- **UUID**: `c3f688e4-a216-4062-a17d-0a638dd90c9e`
- **参数名**: `CsmHashPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackHash

- **UUID**: `027f32fc-55af-4872-84d4-f89dab4c3888`
- **参数名**: `CsmCallbackHash`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 50. CsmKeyDerive

**容器属性**:

- **UUID**: `64cfbc1d-c891-40c8-bd2b-60a0f1b6d055`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDerive`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyDerive primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyDeriveMaxKeySize

- **UUID**: `ed7c2f40-6fad-4aa1-9944-93ed4bc1a29e`
- **参数名**: `CsmKeyDeriveMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a key derivation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKeyDeriveConfig

**容器属性**:

- **UUID**: `90d3ed6f-a29b-4439-b696-0f9cbb846074`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDeriveConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyDerive. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmKeyDeriveInitConfiguration

- **UUID**: `7b4c7407-1d2a-4553-b68c-f5ed6b2388b9`
- **参数名**: `CsmKeyDeriveInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmKeyDerivePrimitiveName

- **UUID**: `493634e1-9fe3-477a-8847-75ea09f31294`
- **参数名**: `CsmKeyDerivePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackKeyDerive

- **UUID**: `8ba6c251-5ff6-4d4e-a6c2-dea5e0e2af19`
- **参数名**: `CsmCallbackKeyDerive`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 51. CsmKeyDeriveConfig

**容器属性**:

- **UUID**: `90d3ed6f-a29b-4439-b696-0f9cbb846074`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDeriveConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyDerive. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmKeyDeriveInitConfiguration

- **UUID**: `7b4c7407-1d2a-4553-b68c-f5ed6b2388b9`
- **参数名**: `CsmKeyDeriveInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmKeyDerivePrimitiveName

- **UUID**: `493634e1-9fe3-477a-8847-75ea09f31294`
- **参数名**: `CsmKeyDerivePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackKeyDerive

- **UUID**: `8ba6c251-5ff6-4d4e-a6c2-dea5e0e2af19`
- **参数名**: `CsmCallbackKeyDerive`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 52. CsmKeyDeriveSymKey

**容器属性**:

- **UUID**: `940e2278-429d-4411-a34a-fc0a579cb369`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDeriveSymKey`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of CsmKeyDeriveSymKey primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyDeriveSymKeyMaxSymKeySize

- **UUID**: `f60b427e-ab2f-4c31-8e8d-91c744d3c54f`
- **参数名**: `CsmKeyDeriveSymKeyMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a key derivation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKeyDeriveSymKeyConfig

**容器属性**:

- **UUID**: `8156e10f-45ec-4e49-8e50-1a2f6e9cb584`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDeriveSymKeyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service CsmKeyDeriveSymKey. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmKeyDeriveSymKeyInitConfiguration

- **UUID**: `ed8acad4-bb43-4b2b-ad62-91cb8bbb6b5c`
- **参数名**: `CsmKeyDeriveSymKeyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmKeyDeriveSymKeyPrimitiveName

- **UUID**: `e5f768e9-6ab9-4ce2-9149-07bd31e14cf7`
- **参数名**: `CsmKeyDeriveSymKeyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackKeyDeriveSymKey

- **UUID**: `3cc11cbb-9467-4463-a3e0-0cf311917b0e`
- **参数名**: `CsmCallbackKeyDeriveSymKey`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 53. CsmKeyDeriveSymKeyConfig

**容器属性**:

- **UUID**: `8156e10f-45ec-4e49-8e50-1a2f6e9cb584`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyDeriveSymKeyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service CsmKeyDeriveSymKey. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmKeyDeriveSymKeyInitConfiguration

- **UUID**: `ed8acad4-bb43-4b2b-ad62-91cb8bbb6b5c`
- **参数名**: `CsmKeyDeriveSymKeyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmKeyDeriveSymKeyPrimitiveName

- **UUID**: `e5f768e9-6ab9-4ce2-9149-07bd31e14cf7`
- **参数名**: `CsmKeyDeriveSymKeyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackKeyDeriveSymKey

- **UUID**: `3cc11cbb-9467-4463-a3e0-0cf311917b0e`
- **参数名**: `CsmCallbackKeyDeriveSymKey`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 54. CsmKeyExchangeCalcPubVal

**容器属性**:

- **UUID**: `a5f46697-dc17-4421-b949-d842c3d93fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcPubVal`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyExchangeCalcPubVal primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyExchangeCalcPubValMaxBaseTypeSize

- **UUID**: `d0739dea-c57f-4490-9b15-e105cc7ffd8d`
- **参数名**: `CsmKeyExchangeCalcPubValMaxBaseTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all base types used in all CRY primitives which implement a public value calculation.

######## 2. CsmKeyExchangeCalcPubValMaxPrivateTypeSize

- **UUID**: `a3768e3f-b8f7-4d38-b34d-15c9ea2628b3`
- **参数名**: `CsmKeyExchangeCalcPubValMaxPrivateTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CRY primitives which implement a public value calculation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `38d047ba-f86d-4bc6-b834-622bc4410a35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcPubValConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmKeyExchangeCalcPubValInitConfiguration

- **UUID**: `57768c8e-8bb5-4283-9776-c8dd587123ce`
- **参数名**: `CsmKeyExchangeCalcPubValInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmKeyExchangeCalcPubValPrimitiveName

- **UUID**: `6ccd203c-adda-4c3e-8ddf-31d3ddfebe93`
- **参数名**: `CsmKeyExchangeCalcPubValPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackKeyExchangeCalcPubVal

- **UUID**: `1b59b103-cb9e-4954-a8be-a4fd774578a5`
- **参数名**: `CsmCallbackKeyExchangeCalcPubVal`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 55. CsmKeyExchangeCalcPubValConfig

**容器属性**:

- **UUID**: `38d047ba-f86d-4bc6-b834-622bc4410a35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcPubValConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcPubVal. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmKeyExchangeCalcPubValInitConfiguration

- **UUID**: `57768c8e-8bb5-4283-9776-c8dd587123ce`
- **参数名**: `CsmKeyExchangeCalcPubValInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmKeyExchangeCalcPubValPrimitiveName

- **UUID**: `6ccd203c-adda-4c3e-8ddf-31d3ddfebe93`
- **参数名**: `CsmKeyExchangeCalcPubValPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackKeyExchangeCalcPubVal

- **UUID**: `1b59b103-cb9e-4954-a8be-a4fd774578a5`
- **参数名**: `CsmCallbackKeyExchangeCalcPubVal`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 56. CsmKeyExchangeCalcSecret

**容器属性**:

- **UUID**: `3981ef51-dbab-45f1-81c6-92db63817b59`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSecret`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyExchangeCalcSecret primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyExchangeCalcSecretMaxBaseTypeSize

- **UUID**: `55179fac-5030-45c4-ac87-77914a7c395a`
- **参数名**: `CsmKeyExchangeCalcSecretMaxBaseTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all base types used in all CRY primitives which implement a shared secret calculation.

######## 2. CsmKeyExchangeCalcSecretMaxPrivateTypeSize

- **UUID**: `e7e0d8de-70c6-49ff-9432-470d4170057d`
- **参数名**: `CsmKeyExchangeCalcSecretMaxPrivateTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CRY primitives which implement a shared secret calculation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `b4006496-c761-40f7-9f5a-432ca3804da1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSecretConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmKeyExchangeCalcSecretInitConfiguration

- **UUID**: `d71f3849-c5c0-4091-a59b-c51a1883cc47`
- **参数名**: `CsmKeyExchangeCalcSecretInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmKeyExchangeCalcSecretPrimitiveName

- **UUID**: `e14757bf-753b-4b14-bdd2-e0d3d27d2927`
- **参数名**: `CsmKeyExchangeCalcSecretPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackKeyExchangeCalcSecret

- **UUID**: `9cdb2df2-011a-4bab-ad42-6c17a8dd1d3d`
- **参数名**: `CsmCallbackKeyExchangeCalcSecret`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 57. CsmKeyExchangeCalcSecretConfig

**容器属性**:

- **UUID**: `b4006496-c761-40f7-9f5a-432ca3804da1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSecretConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSecret. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmKeyExchangeCalcSecretInitConfiguration

- **UUID**: `d71f3849-c5c0-4091-a59b-c51a1883cc47`
- **参数名**: `CsmKeyExchangeCalcSecretInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmKeyExchangeCalcSecretPrimitiveName

- **UUID**: `e14757bf-753b-4b14-bdd2-e0d3d27d2927`
- **参数名**: `CsmKeyExchangeCalcSecretPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackKeyExchangeCalcSecret

- **UUID**: `9cdb2df2-011a-4bab-ad42-6c17a8dd1d3d`
- **参数名**: `CsmCallbackKeyExchangeCalcSecret`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 58. CsmKeyExchangeCalcSymKey

**容器属性**:

- **UUID**: `19989517-3625-44b7-8bcd-18b57861f6fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSymKey`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of KeyExchangeCalcSymKey primitives.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CsmKeyExchangeCalcSymKeyMaxBaseTypeSize

- **UUID**: `068c9295-7105-4289-a895-ad0a38490d7a`
- **参数名**: `CsmKeyExchangeCalcSymKeyMaxBaseTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all base types used in all CRY primitives which implement a symmetrical key calculation.

######## 2. CsmKeyExchangeCalcSymKeyMaxPrivateTypeSize

- **UUID**: `28d630f0-2720-426c-bcf9-f073e5556168`
- **参数名**: `CsmKeyExchangeCalcSymKeyMaxPrivateTypeSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all private information types used in all CRY primitives which implement a symmetrical key calculation.

######## 3. CsmKeyExchangeCalcSymKeyMaxSymKeySize

- **UUID**: `3e4ff5f6-f976-4d5b-8fda-26553baf20fd`
- **参数名**: `CsmKeyExchangeCalcSymKeyMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical key calculation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmKeyExchangeCalcSymKeyConfig

**容器属性**:

- **UUID**: `a613fb3d-6e11-4c16-9fb3-8246faf6270f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSymKeyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSymKey. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmKeyExchangeCalcSymKeyInitConfiguration

- **UUID**: `9cf31fb8-7949-4d4e-af38-5612a258d80f`
- **参数名**: `CsmKeyExchangeCalcSymKeyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmKeyExchangeCalcSymKeyPrimitiveName

- **UUID**: `0e0593b8-57fd-4fd0-b372-a98f3a00a367`
- **参数名**: `CsmKeyExchangeCalcSymKeyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackKeyExchangeCalcSymKey

- **UUID**: `74ba7a61-2d62-45e1-8d93-f5bea120c772`
- **参数名**: `CsmCallbackKeyExchangeCalcSymKey`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 59. CsmKeyExchangeCalcSymKeyConfig

**容器属性**:

- **UUID**: `a613fb3d-6e11-4c16-9fb3-8246faf6270f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmKeyExchangeCalcSymKeyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service KeyExchangeCalcSymKey. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmKeyExchangeCalcSymKeyInitConfiguration

- **UUID**: `9cf31fb8-7949-4d4e-af38-5612a258d80f`
- **参数名**: `CsmKeyExchangeCalcSymKeyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmKeyExchangeCalcSymKeyPrimitiveName

- **UUID**: `0e0593b8-57fd-4fd0-b372-a98f3a00a367`
- **参数名**: `CsmKeyExchangeCalcSymKeyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackKeyExchangeCalcSymKey

- **UUID**: `74ba7a61-2d62-45e1-8d93-f5bea120c772`
- **参数名**: `CsmCallbackKeyExchangeCalcSymKey`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 60. CsmMacGenerate

**容器属性**:

- **UUID**: `3c432015-c246-4abe-8238-1641d59eb474`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerate`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of MacGenerate primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacGenerateMaxKeySize

- **UUID**: `58f9faa3-823f-4655-a76b-851edd55cb9c`
- **参数名**: `CsmMacGenerateMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a MAC generation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `cf620d4e-2171-4921-b508-01ec6bb907dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configurations for the MacGenerate service. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmMacGenerateInitConfiguration

- **UUID**: `3eb4a998-3085-4c38-b84c-0b9f9d45edc3`
- **参数名**: `CsmMacGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmMacGeneratePrimitiveName

- **UUID**: `8f585a42-8205-4e39-b73a-f517bb736c82`
- **参数名**: `CsmMacGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackMacGenerate

- **UUID**: `1503de5f-cd6e-4fe7-bd68-4b3c571956e0`
- **参数名**: `CsmCallbackMacGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 61. CsmMacGenerateConfig

**容器属性**:

- **UUID**: `cf620d4e-2171-4921-b508-01ec6bb907dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configurations for the MacGenerate service. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmMacGenerateInitConfiguration

- **UUID**: `3eb4a998-3085-4c38-b84c-0b9f9d45edc3`
- **参数名**: `CsmMacGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmMacGeneratePrimitiveName

- **UUID**: `8f585a42-8205-4e39-b73a-f517bb736c82`
- **参数名**: `CsmMacGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackMacGenerate

- **UUID**: `1503de5f-cd6e-4fe7-bd68-4b3c571956e0`
- **参数名**: `CsmCallbackMacGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 62. CsmMacVerify

**容器属性**:

- **UUID**: `dbc936d8-2019-4d9c-a639-5999b7bea4f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerify`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of MacVerify primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmMacVerifyMaxKeySize

- **UUID**: `8eae851b-fc8f-41a3-9c68-03e4d523cf34`
- **参数名**: `CsmMacVerifyMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a MAC verification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `ae4e6e14-f07b-4d0e-b08c-4198eacd203f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service MacVerify. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmMacVerifyInitConfiguration

- **UUID**: `eabaa3ec-48c8-4ffb-b601-352dcf08c062`
- **参数名**: `CsmMacVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmMacVerifyPrimitiveName

- **UUID**: `1d0f8057-375f-496a-b10f-76980e14d8fd`
- **参数名**: `CsmMacVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackMacVerify

- **UUID**: `5e02e6f1-f24a-423f-945e-d43776dd211c`
- **参数名**: `CsmCallbackMacVerify`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 63. CsmMacVerifyConfig

**容器属性**:

- **UUID**: `ae4e6e14-f07b-4d0e-b08c-4198eacd203f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmMacVerifyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service MacVerify. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmMacVerifyInitConfiguration

- **UUID**: `eabaa3ec-48c8-4ffb-b601-352dcf08c062`
- **参数名**: `CsmMacVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmMacVerifyPrimitiveName

- **UUID**: `1d0f8057-375f-496a-b10f-76980e14d8fd`
- **参数名**: `CsmMacVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackMacVerify

- **UUID**: `5e02e6f1-f24a-423f-945e-d43776dd211c`
- **参数名**: `CsmCallbackMacVerify`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 64. CsmRandomGenerate

**容器属性**:

- **UUID**: `8e78ccf7-56b1-4953-b913-97f80c668e6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerate`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of RandomGenerate primitives.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `78639a0b-120f-4de5-a0fd-23ce47de80ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmRandomGenerateInitConfiguration

- **UUID**: `bc65df2a-9406-45a8-adef-aad99ff63534`
- **参数名**: `CsmRandomGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmRandomGeneratePrimitiveName

- **UUID**: `02054966-a590-4ea8-b679-84b2ec32d788`
- **参数名**: `CsmRandomGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackRandomGenerate

- **UUID**: `0081a51f-3e56-426a-92b3-663754e4623b`
- **参数名**: `CsmCallbackRandomGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 65. CsmRandomGenerateConfig

**容器属性**:

- **UUID**: `78639a0b-120f-4de5-a0fd-23ce47de80ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmRandomGenerateInitConfiguration

- **UUID**: `bc65df2a-9406-45a8-adef-aad99ff63534`
- **参数名**: `CsmRandomGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmRandomGeneratePrimitiveName

- **UUID**: `02054966-a590-4ea8-b679-84b2ec32d788`
- **参数名**: `CsmRandomGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackRandomGenerate

- **UUID**: `0081a51f-3e56-426a-92b3-663754e4623b`
- **参数名**: `CsmCallbackRandomGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 66. CsmRandomSeed

**容器属性**:

- **UUID**: `9dd58103-32ac-4a14-b658-85b037efd2e4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomSeed`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of RandomSeed primitives.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmRandomSeedConfig

**容器属性**:

- **UUID**: `a5f35999-cc53-4c55-9bcf-993da8681bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomSeedConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomSeed. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmRandomSeedInitConfiguration

- **UUID**: `565c4e76-6fde-4391-b881-3a49c937107d`
- **参数名**: `CsmRandomSeedInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmRandomSeedPrimitiveName

- **UUID**: `85debb31-caae-4057-a42b-bac260b0b35d`
- **参数名**: `CsmRandomSeedPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackRandomSeed

- **UUID**: `23cadc6e-0435-4907-8ed5-e57b2817545e`
- **参数名**: `CsmCallbackRandomSeed`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 67. CsmRandomSeedConfig

**容器属性**:

- **UUID**: `a5f35999-cc53-4c55-9bcf-993da8681bb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmRandomSeedConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service RandomSeed. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmRandomSeedInitConfiguration

- **UUID**: `565c4e76-6fde-4391-b881-3a49c937107d`
- **参数名**: `CsmRandomSeedInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmRandomSeedPrimitiveName

- **UUID**: `85debb31-caae-4057-a42b-bac260b0b35d`
- **参数名**: `CsmRandomSeedPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackRandomSeed

- **UUID**: `23cadc6e-0435-4907-8ed5-e57b2817545e`
- **参数名**: `CsmCallbackRandomSeed`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 68. CsmSignatureGenerate

**容器属性**:

- **UUID**: `e531f986-79e9-4f51-8710-e7f0cc87d52f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerate`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SignatureGenerate primitives

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureGenerateMaxKeySize

- **UUID**: `cbe9989f-f3bf-4f90-b752-85f1ac745cf0`
- **参数名**: `CsmSignatureGenerateMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a signature generation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `3101a0ce-7691-4c82-a11e-acffc1e48756`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSignatureGenerateInitConfiguration

- **UUID**: `25e2ce24-fd48-43ce-b64b-d3a18e4883e5`
- **参数名**: `CsmSignatureGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSignatureGeneratePrimitiveName

- **UUID**: `94a03e7e-fa02-4454-81c2-299070d8e033`
- **参数名**: `CsmSignatureGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSignatureGenerate

- **UUID**: `c1a4a4d0-a0e8-490b-bd75-1f4e16fee15b`
- **参数名**: `CsmCallbackSignatureGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 69. CsmSignatureGenerateConfig

**容器属性**:

- **UUID**: `3101a0ce-7691-4c82-a11e-acffc1e48756`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureGenerateConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureGenerate. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSignatureGenerateInitConfiguration

- **UUID**: `25e2ce24-fd48-43ce-b64b-d3a18e4883e5`
- **参数名**: `CsmSignatureGenerateInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSignatureGeneratePrimitiveName

- **UUID**: `94a03e7e-fa02-4454-81c2-299070d8e033`
- **参数名**: `CsmSignatureGeneratePrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSignatureGenerate

- **UUID**: `c1a4a4d0-a0e8-490b-bd75-1f4e16fee15b`
- **参数名**: `CsmCallbackSignatureGenerate`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 70. CsmSignatureVerify

**容器属性**:

- **UUID**: `87271917-ec0a-4c51-a7f7-824a217e5022`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerify`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SignatureVerify primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSignatureVerifyMaxKeySize

- **UUID**: `69732082-a8a1-4a5a-a02a-80105ea29e12`
- **参数名**: `CsmSignatureVerifyMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a signature verification.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6449700e-459b-4b89-8aa6-42df6ed5e0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureVerify. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSignatureVerifyInitConfiguration

- **UUID**: `5d34a497-8fc8-4604-945c-94fd18e92a3b`
- **参数名**: `CsmSignatureVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSignatureVerifyPrimitiveName

- **UUID**: `951fa05f-4464-4c9f-baff-99100c67a6ec`
- **参数名**: `CsmSignatureVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSignatureVerify

- **UUID**: `3423d44e-2389-4f6c-a7d0-d1001502930a`
- **参数名**: `CsmCallbackSignatureVerify`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 71. CsmSignatureVerifyConfig

**容器属性**:

- **UUID**: `6449700e-459b-4b89-8aa6-42df6ed5e0c3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSignatureVerifyConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SignatureVerify. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSignatureVerifyInitConfiguration

- **UUID**: `5d34a497-8fc8-4604-945c-94fd18e92a3b`
- **参数名**: `CsmSignatureVerifyInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSignatureVerifyPrimitiveName

- **UUID**: `951fa05f-4464-4c9f-baff-99100c67a6ec`
- **参数名**: `CsmSignatureVerifyPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSignatureVerify

- **UUID**: `3423d44e-2389-4f6c-a7d0-d1001502930a`
- **参数名**: `CsmCallbackSignatureVerify`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 72. CsmSymBlockDecrypt

**容器属性**:

- **UUID**: `68bb2701-2f8e-4cdd-a619-4bb3ebaa53c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymBlockDecrypt primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymBlockDecryptMaxKeySize

- **UUID**: `03c35a0d-3de9-46e7-a4f1-7e1977e24962`
- **参数名**: `CsmSymBlockDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical block decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymBlockDecryptConfig

**容器属性**:

- **UUID**: `ce937528-e3bf-4cbd-8814-2919dee285b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymBlockDecryptInitConfiguration

- **UUID**: `a4fae46f-22ef-49d9-8872-34663e382116`
- **参数名**: `CsmSymBlockDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymBlockDecryptPrimitiveName

- **UUID**: `6b1de68c-fcc8-4381-8e3e-42756f96a7bb`
- **参数名**: `CsmSymBlockDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymBlockDecrypt

- **UUID**: `6b63f27f-9a53-47a5-96d5-5f27d4f7e55c`
- **参数名**: `CsmCallbackSymBlockDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 73. CsmSymBlockDecryptConfig

**容器属性**:

- **UUID**: `ce937528-e3bf-4cbd-8814-2919dee285b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockDecrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymBlockDecryptInitConfiguration

- **UUID**: `a4fae46f-22ef-49d9-8872-34663e382116`
- **参数名**: `CsmSymBlockDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymBlockDecryptPrimitiveName

- **UUID**: `6b1de68c-fcc8-4381-8e3e-42756f96a7bb`
- **参数名**: `CsmSymBlockDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymBlockDecrypt

- **UUID**: `6b63f27f-9a53-47a5-96d5-5f27d4f7e55c`
- **参数名**: `CsmCallbackSymBlockDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 74. CsmSymBlockEncrypt

**容器属性**:

- **UUID**: `87937807-a8da-4416-8f66-91926206e879`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymBlockEncrypt primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymBlockEncryptMaxKeySize

- **UUID**: `41ffaf70-23c0-4962-8590-8dac99e957ed`
- **参数名**: `CsmSymBlockEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical block encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymBlockEncryptConfig

**容器属性**:

- **UUID**: `c30fadc7-8c41-41c5-9855-e83f701417de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymBlockEncryptInitConfiguration

- **UUID**: `b9084f4c-1860-406f-ad8a-718e0cbd0c8f`
- **参数名**: `CsmSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymBlockEncryptPrimitiveName

- **UUID**: `d6e97a8b-711a-4db2-936b-3fc539672e81`
- **参数名**: `CsmSymBlockEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymBlockEncrypt

- **UUID**: `ca22d10f-bad5-4786-b849-a78ed0ba8fbe`
- **参数名**: `CsmCallbackSymBlockEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 75. CsmSymBlockEncryptConfig

**容器属性**:

- **UUID**: `c30fadc7-8c41-41c5-9855-e83f701417de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymBlockEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymBlockEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymBlockEncryptInitConfiguration

- **UUID**: `b9084f4c-1860-406f-ad8a-718e0cbd0c8f`
- **参数名**: `CsmSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymBlockEncryptPrimitiveName

- **UUID**: `d6e97a8b-711a-4db2-936b-3fc539672e81`
- **参数名**: `CsmSymBlockEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymBlockEncrypt

- **UUID**: `ca22d10f-bad5-4786-b849-a78ed0ba8fbe`
- **参数名**: `CsmCallbackSymBlockEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 76. CsmSymDecrypt

**容器属性**:

- **UUID**: `c4a05a94-fcef-48df-9a76-a16c74c6cc96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymDecrypt primitives

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymDecryptMaxKeySize

- **UUID**: `0fa8606f-e70b-40fd-b273-bc8b0f6a1ae0`
- **参数名**: `CsmSymDecryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical decryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymDecryptConfig

**容器属性**:

- **UUID**: `69964c3f-4120-4941-bd6b-1c8bd49e6a98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymDecrypt.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymDecryptInitConfiguration

- **UUID**: `fb83e59c-7046-4444-ac49-2a19c5e5d919`
- **参数名**: `CsmSymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymDecryptPrimitiveName

- **UUID**: `a051e25f-f559-445f-9221-1f256ae29e93`
- **参数名**: `CsmSymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymDecrypt

- **UUID**: `09e22343-b2c4-4636-aba4-7d6dc0111b5a`
- **参数名**: `CsmCallbackSymDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 77. CsmSymDecryptConfig

**容器属性**:

- **UUID**: `69964c3f-4120-4941-bd6b-1c8bd49e6a98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymDecryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymDecrypt.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymDecryptInitConfiguration

- **UUID**: `fb83e59c-7046-4444-ac49-2a19c5e5d919`
- **参数名**: `CsmSymDecryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymDecryptPrimitiveName

- **UUID**: `a051e25f-f559-445f-9221-1f256ae29e93`
- **参数名**: `CsmSymDecryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymDecrypt

- **UUID**: `09e22343-b2c4-4636-aba4-7d6dc0111b5a`
- **参数名**: `CsmCallbackSymDecrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 78. CsmSymEncrypt

**容器属性**:

- **UUID**: `4f9e190b-ca4c-4bd7-b919-ff24a568f590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymEncrypt`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymEncrypt primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymEncryptMaxKeySize

- **UUID**: `25215674-59db-445e-bc4a-8b46f3ee9ec2`
- **参数名**: `CsmSymEncryptMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical encryption.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymEncryptConfig

**容器属性**:

- **UUID**: `25b827ee-c6b9-467f-891f-1de0ce56bea2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymBlockEncryptInitConfiguration

- **UUID**: `5a7fcf52-7bef-4fe7-84a7-c4e829107ddc`
- **参数名**: `CsmSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymEncryptPrimitiveName

- **UUID**: `15db686f-c02e-40d5-a278-27e72467b4fc`
- **参数名**: `CsmSymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymEncrypt

- **UUID**: `bca4a1e7-7919-4c35-a670-af00244bcf95`
- **参数名**: `CsmCallbackSymEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 79. CsmSymEncryptConfig

**容器属性**:

- **UUID**: `25b827ee-c6b9-467f-891f-1de0ce56bea2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymEncryptConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymEncrypt. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymBlockEncryptInitConfiguration

- **UUID**: `5a7fcf52-7bef-4fe7-84a7-c4e829107ddc`
- **参数名**: `CsmSymBlockEncryptInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymEncryptPrimitiveName

- **UUID**: `15db686f-c02e-40d5-a278-27e72467b4fc`
- **参数名**: `CsmSymEncryptPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymEncrypt

- **UUID**: `bca4a1e7-7919-4c35-a670-af00244bcf95`
- **参数名**: `CsmCallbackSymEncrypt`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 80. CsmSymKeyExtract

**容器属性**:

- **UUID**: `7efdc48e-4f8a-4b18-b646-fc0ae644c2c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyExtract`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyExtract primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymKeyExtractMaxKeySize

- **UUID**: `9dc06c67-1915-4738-adf7-e34e15ec674d`
- **参数名**: `CsmSymKeyExtractMaxKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement a symmetrical key extraction.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymKeyExtractConfig

**容器属性**:

- **UUID**: `3abf783f-75f9-4416-b4bf-67fc54913f13`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyExtract. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymKeyExtractInitConfiguration

- **UUID**: `c5b2c29c-e6a9-4f91-9149-85df4ea72099`
- **参数名**: `CsmSymKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymKeyExtractPrimitiveName

- **UUID**: `d2a9320d-af2b-456d-ada2-d50ea6a4c36f`
- **参数名**: `CsmSymKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymKeyExtract

- **UUID**: `24f2af08-3e4f-4dc3-b412-fb28b0424dad`
- **参数名**: `CsmCallbackSymKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 81. CsmSymKeyExtractConfig

**容器属性**:

- **UUID**: `3abf783f-75f9-4416-b4bf-67fc54913f13`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyExtractConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyExtract. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymKeyExtractInitConfiguration

- **UUID**: `c5b2c29c-e6a9-4f91-9149-85df4ea72099`
- **参数名**: `CsmSymKeyExtractInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymKeyExtractPrimitiveName

- **UUID**: `d2a9320d-af2b-456d-ada2-d50ea6a4c36f`
- **参数名**: `CsmSymKeyExtractPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymKeyExtract

- **UUID**: `24f2af08-3e4f-4dc3-b412-fb28b0424dad`
- **参数名**: `CsmCallbackSymKeyExtract`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 82. CsmSymKeyWrapAsym

**容器属性**:

- **UUID**: `40f55c00-56df-438b-beee-690dbf458e77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapAsym`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyWrapSym primitives.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymKeyWrapAsymMaxPubKeySize

- **UUID**: `c880bc92-7d0a-4b11-9d78-b6930492abb3`
- **参数名**: `CsmSymKeyWrapAsymMaxPubKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum length, in bytes, of all public key  types used in all CRY primitives which implement an asymmetrical key wrapping.

######## 2. CsmSymKeyWrapAsymMaxSymKeySize

- **UUID**: `c0d2491f-aeb9-406a-82ba-c3ec33736b0d`
- **参数名**: `CsmSymKeyWrapAsymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an asymmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymKeyWrapAsymConfig

**容器属性**:

- **UUID**: `b97138c7-3d49-4cf1-8ea6-8c0ffafbbb77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapAsymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymKeyWrapAsymInitConfiguration

- **UUID**: `cd9b2448-fb3a-47e6-bb2f-122873a61092`
- **参数名**: `CsmSymKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymKeyWrapAsymPrimitiveName

- **UUID**: `21c67f5e-9140-4a1b-b635-962d827e3835`
- **参数名**: `CsmSymKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymKeyWrapAsym

- **UUID**: `f865ae55-7e66-4997-b38b-8e8d642b43db`
- **参数名**: `CsmCallbackSymKeyWrapAsym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 83. CsmSymKeyWrapAsymConfig

**容器属性**:

- **UUID**: `b97138c7-3d49-4cf1-8ea6-8c0ffafbbb77`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapAsymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapAsym. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymKeyWrapAsymInitConfiguration

- **UUID**: `cd9b2448-fb3a-47e6-bb2f-122873a61092`
- **参数名**: `CsmSymKeyWrapAsymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymKeyWrapAsymPrimitiveName

- **UUID**: `21c67f5e-9140-4a1b-b635-962d827e3835`
- **参数名**: `CsmSymKeyWrapAsymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymKeyWrapAsym

- **UUID**: `f865ae55-7e66-4997-b38b-8e8d642b43db`
- **参数名**: `CsmCallbackSymKeyWrapAsym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 84. CsmSymKeyWrapSym

**容器属性**:

- **UUID**: `d24e3239-8965-4da6-9b84-38f0f9ca6cba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapSym`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for incorporation of SymKeyWrapSym primitives.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CsmSymKeyWrapSymMaxSymKeySize

- **UUID**: `201e1b9d-2a0f-4a92-a84a-a42f8d0e8266`
- **参数名**: `CsmSymKeyWrapSymMaxSymKeySize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum, in bytes, of all key lengths used in all CRY primitives which implement an symmetrical key wrapping.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CsmSymKeyWrapSymConfig

**容器属性**:

- **UUID**: `8bb111a5-443d-47ac-965d-8dbd525e5181`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapSymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapSym. The container name serves as a symbolic name for the identifier of a service configuration.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. CsmSymKeyWrapSymInitConfiguration

- **UUID**: `c448975e-0512-4c13-ad73-0bef3c004ec4`
- **参数名**: `CsmSymKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

########## 2. CsmSymKeyWrapSymPrimitiveName

- **UUID**: `5f52b113-1146-4f93-ab2b-5e2f22652433`
- **参数名**: `CsmSymKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

######### FUNCTION-NAME 类型参数

########## 1. CsmCallbackSymKeyWrapSym

- **UUID**: `c9c986bf-715e-4295-b5d0-dc46313c616d`
- **参数名**: `CsmCallbackSymKeyWrapSym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

##### 85. CsmSymKeyWrapSymConfig

**容器属性**:

- **UUID**: `8bb111a5-443d-47ac-965d-8dbd525e5181`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CsmSymKeyWrapSymConfig`
- **多重性**: [0..32]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for configuration of service SymKeyWrapSym. The container name serves as a symbolic name for the identifier of a service configuration.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. CsmSymKeyWrapSymInitConfiguration

- **UUID**: `c448975e-0512-4c13-ad73-0bef3c004ec4`
- **参数名**: `CsmSymKeyWrapSymInitConfiguration`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C symbol which contains the configuration of the underlying cryptographic primitive.

######## 2. CsmSymKeyWrapSymPrimitiveName

- **UUID**: `5f52b113-1146-4f93-ab2b-5e2f22652433`
- **参数名**: `CsmSymKeyWrapSymPrimitiveName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the cryptographic primitive to use.

####### FUNCTION-NAME 类型参数

######## 1. CsmCallbackSymKeyWrapSym

- **UUID**: `c9c986bf-715e-4295-b5d0-dc46313c616d`
- **参数名**: `CsmCallbackSymKeyWrapSym`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Callback function to be called if service has finished.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `3eee0e85-7e59-4556-993a-89107c5203c4`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `7c03fef5-12e6-4144-8882-c14dce2584b8`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Csm**
