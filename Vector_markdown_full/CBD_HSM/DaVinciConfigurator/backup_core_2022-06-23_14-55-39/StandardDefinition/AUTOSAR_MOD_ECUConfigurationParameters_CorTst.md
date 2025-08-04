# CorTst - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CorTst](#cortst)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CorTst

#### 基本信息

- **UUID**: `ECUC:e0638552-23b0-40f3-af0c-0d0c9be0ab6b`
- **模块名称**: `CorTst`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the CorTst module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. CorTstBackgroundConfigSet

**容器属性**:

- **UUID**: `ECUC:4abd3c77-cd49-4b0a-8f98-61eac791284d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstBackgroundConfigSet`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Multiple Configuration Set Container, defines background mode.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CorTstSelect

**容器属性**:

- **UUID**: `ECUC:fdc54cb3-66d7-9413-104e-6eec9b6ab710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstSelect`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters to select individual tests for foreground mode and background mode. The availability is hardware and implementation specific.

######## 参数配置

此容器包含 **7** 个参数：

######### BOOLEAN 类型参数

########## 1. CorTstAddress

- **UUID**: `ECUC:b5360c0b-037a-d9d9-a493-656c04bfcfbc`
- **参数名**: `CorTstAddress`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core address test.

########## 2. CorTstAlu

- **UUID**: `ECUC:7bd51b24-c3a7-daa6-b81e-8561e03812a7`
- **参数名**: `CorTstAlu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core ALU test.

########## 3. CorTstCache

- **UUID**: `ECUC:8a28cded-0efd-dac7-b7b1-768a1f552bf1`
- **参数名**: `CorTstCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core cache test.

########## 4. CorTstInterrupt

- **UUID**: `ECUC:797547b1-830a-e048-aa5e-f3c5e919339d`
- **参数名**: `CorTstInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core interrupt test

########## 5. CorTstMemoryIf

- **UUID**: `ECUC:e15bc8c9-cf05-d7c6-a084-0d5318d8454d`
- **参数名**: `CorTstMemoryIf`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core memory interface test

########## 6. CorTstMpu

- **UUID**: `ECUC:d512a17d-5d8a-dffa-cd7d-8653fc6f823d`
- **参数名**: `CorTstMpu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core MPU test

########## 7. CorTstRegister

- **UUID**: `ECUC:c8dfedab-ee43-e033-99fd-cbd7c4ef97fe`
- **参数名**: `CorTstRegister`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core register test

##### 2. CorTstSelect

**容器属性**:

- **UUID**: `ECUC:fdc54cb3-66d7-9413-104e-6eec9b6ab710`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstSelect`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters to select individual tests for foreground mode and background mode. The availability is hardware and implementation specific.

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. CorTstAddress

- **UUID**: `ECUC:b5360c0b-037a-d9d9-a493-656c04bfcfbc`
- **参数名**: `CorTstAddress`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core address test.

######## 2. CorTstAlu

- **UUID**: `ECUC:7bd51b24-c3a7-daa6-b81e-8561e03812a7`
- **参数名**: `CorTstAlu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core ALU test.

######## 3. CorTstCache

- **UUID**: `ECUC:8a28cded-0efd-dac7-b7b1-768a1f552bf1`
- **参数名**: `CorTstCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core cache test.

######## 4. CorTstInterrupt

- **UUID**: `ECUC:797547b1-830a-e048-aa5e-f3c5e919339d`
- **参数名**: `CorTstInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core interrupt test

######## 5. CorTstMemoryIf

- **UUID**: `ECUC:e15bc8c9-cf05-d7c6-a084-0d5318d8454d`
- **参数名**: `CorTstMemoryIf`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core memory interface test

######## 6. CorTstMpu

- **UUID**: `ECUC:d512a17d-5d8a-dffa-cd7d-8653fc6f823d`
- **参数名**: `CorTstMpu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core MPU test

######## 7. CorTstRegister

- **UUID**: `ECUC:c8dfedab-ee43-e033-99fd-cbd7c4ef97fe`
- **参数名**: `CorTstRegister`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core register test

##### 3. CorTstConfigApiServices

**容器属性**:

- **UUID**: `ECUC:8598c4af-2127-4229-9ad7-a5dbb94c82ee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstConfigApiServices`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. CorTstAbortApi

- **UUID**: `ECUC:317dc460-8c74-4fd2-9109-00ed4751554f`
- **参数名**: `CorTstAbortApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_Abort() from the code.

######## 2. CorTstGetCurrentStatus

- **UUID**: `ECUC:6191aa54-d5fb-4ac5-8706-eb3e7bf2866d`
- **参数名**: `CorTstGetCurrentStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_GetCurrentStatus() from the code.

######## 3. CorTstGetFgndSignature

- **UUID**: `ECUC:9d8e4991-d8a1-4e54-af0f-cc62e300cf21`
- **参数名**: `CorTstGetFgndSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_GetFgndSignature() from the code.

######## 4. CorTstGetSignature

- **UUID**: `ECUC:c59a0625-5199-4aaf-a0d3-a4b391e1db4f`
- **参数名**: `CorTstGetSignature`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_GetSignature() from the code.

######## 5. CorTstGetStateApi

- **UUID**: `ECUC:a503e197-9147-444f-b094-30f772ca7114`
- **参数名**: `CorTstGetStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_GetState() from the code.

######## 6. CorTstStartApi

- **UUID**: `ECUC:497b13d5-6a95-452c-ad96-bb61a204ef07`
- **参数名**: `CorTstStartApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_Start() from the code.

######## 7. CorTstVersionInfoApi

- **UUID**: `ECUC:6f877a50-ab0c-4014-b659-3115c4c0a493`
- **参数名**: `CorTstVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service CorTst_GetVersionInfo() from the code.

##### 4. CorTstDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:2279068b-7746-4d4b-a8cb-47afe4e2a309`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CORTST_E_CORE_FAILURE

- **UUID**: `ECUC:e0838ca8-7d10-444e-b0ac-898050fc6917`
- **引用名**: `CORTST_E_CORE_FAILURE`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "CORE failure" has occured.

##### 5. CorTstForegroundConfigSet

**容器属性**:

- **UUID**: `ECUC:5ac54b8c-2d57-4461-aee7-c4542623c585`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstForegroundConfigSet`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Multiple Configuration Set Container , defines foreground mode.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CorTstTestIdFgnd

- **UUID**: `ECUC:d214eee0-143e-4d6e-a306-365ec26a5177`
- **参数名**: `CorTstTestIdFgnd`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the Id of this specific foreground test configuration. The value shall be used in the call to the API CorTst_Start(CorTst_TestIdFgndType TestId).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CorTstSelect

**容器属性**:

- **UUID**: `ECUC:0dcd5bc7-c6e5-8d6a-2f9d-d155f9fd5448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstSelect`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters to select individual tests for foreground mode and background mode. The availability is hardware and implementation specific.

######## 参数配置

此容器包含 **7** 个参数：

######### BOOLEAN 类型参数

########## 1. CorTstAddress

- **UUID**: `ECUC:c53e1b1f-6388-d330-c3e2-c7d563526cf4`
- **参数名**: `CorTstAddress`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core address test.

########## 2. CorTstAlu

- **UUID**: `ECUC:8bdd2a39-23b5-d3fd-d76d-e7cb3ecaafdf`
- **参数名**: `CorTstAlu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core ALU test.

########## 3. CorTstCache

- **UUID**: `ECUC:9a30dd01-6f0b-d41e-d700-d8f37de7c929`
- **参数名**: `CorTstCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core cache test.

########## 4. CorTstInterrupt

- **UUID**: `ECUC:897d56c5-e318-d99f-c9ae-562f47abd0d5`
- **参数名**: `CorTstInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core interrupt test

########## 5. CorTstMemoryIf

- **UUID**: `ECUC:f163d7de-2f13-d11d-bfd3-6fbc776ae285`
- **参数名**: `CorTstMemoryIf`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core memory interface test

########## 6. CorTstMpu

- **UUID**: `ECUC:e51ab091-bd98-d951-eccc-e8bd5b021f75`
- **参数名**: `CorTstMpu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core MPU test

########## 7. CorTstRegister

- **UUID**: `ECUC:d8e7fcc0-4e51-d98a-b94d-2e4123823536`
- **参数名**: `CorTstRegister`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core register test

##### 6. CorTstSelect

**容器属性**:

- **UUID**: `ECUC:0dcd5bc7-c6e5-8d6a-2f9d-d155f9fd5448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstSelect`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies configuration parameters to select individual tests for foreground mode and background mode. The availability is hardware and implementation specific.

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. CorTstAddress

- **UUID**: `ECUC:c53e1b1f-6388-d330-c3e2-c7d563526cf4`
- **参数名**: `CorTstAddress`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core address test.

######## 2. CorTstAlu

- **UUID**: `ECUC:8bdd2a39-23b5-d3fd-d76d-e7cb3ecaafdf`
- **参数名**: `CorTstAlu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core ALU test.

######## 3. CorTstCache

- **UUID**: `ECUC:9a30dd01-6f0b-d41e-d700-d8f37de7c929`
- **参数名**: `CorTstCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core cache test.

######## 4. CorTstInterrupt

- **UUID**: `ECUC:897d56c5-e318-d99f-c9ae-562f47abd0d5`
- **参数名**: `CorTstInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core interrupt test

######## 5. CorTstMemoryIf

- **UUID**: `ECUC:f163d7de-2f13-d11d-bfd3-6fbc776ae285`
- **参数名**: `CorTstMemoryIf`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core memory interface test

######## 6. CorTstMpu

- **UUID**: `ECUC:e51ab091-bd98-d951-eccc-e8bd5b021f75`
- **参数名**: `CorTstMpu`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core MPU test

######## 7. CorTstRegister

- **UUID**: `ECUC:d8e7fcc0-4e51-d98a-b94d-2e4123823536`
- **参数名**: `CorTstRegister`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable/Disables core register test

##### 7. CorTstGeneral

**容器属性**:

- **UUID**: `ECUC:418d5d15-2b92-4fe4-b26d-b56fd36d767b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CorTstGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CorTstFgndTestNumber

- **UUID**: `ECUC:04f7d432-2924-49b3-b8ac-81a39b03d802`
- **参数名**: `CorTstFgndTestNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter holds the number of test configurations available for the foreground tests as defined in this configuration.

######## 2. CorTstTestIntervalIdEndValue

- **UUID**: `ECUC:056b7ede-f135-4798-84e9-c7a70289599a`
- **参数名**: `CorTstTestIntervalIdEndValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the end value of the Test Interval Id.

####### BOOLEAN 类型参数

######## 1. CorTstDevErrorDetect

- **UUID**: `ECUC:1cebc962-a05b-49a6-b0e4-f1423dec097b`
- **参数名**: `CorTstDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the development error detection.

######## 2. CorTstNotificationSupported

- **UUID**: `ECUC:2ff3d6f0-16cf-4efb-ba96-260ba8e5f6cb`
- **参数名**: `CorTstNotificationSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to indicate that the notification is supported.

######## 3. CorTstTestResultMode

- **UUID**: `ECUC:d2f1c839-0863-41b0-a96f-c70dee2fa4c6`
- **参数名**: `CorTstTestResultMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling test result comparison within the Core test driver. In this mode a core test result OK or NOTOK shall not be calculated from the core test driver. Within core test driver no comparison against the reference value is processed.

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

1. **CorTst**
