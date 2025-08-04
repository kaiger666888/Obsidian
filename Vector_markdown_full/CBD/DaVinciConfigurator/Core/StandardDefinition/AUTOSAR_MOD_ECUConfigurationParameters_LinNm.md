# LinNm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:25

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LinNm](#linnm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LinNm

#### 基本信息

- **UUID**: `ECUC:5fffd262-bff3-4654-9e04-15186d0d360d`
- **模块名称**: `LinNm`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration Parameters for the Lin Nm module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **2** 个配置容器：

##### 1. LinNmGlobalConfig

**容器属性**:

- **UUID**: `ECUC:534f84b2-6d05-4c99-8dee-8f74bf3e15a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinNmGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the global configuration parameter of the LinNm.

###### 参数配置

此容器包含 **13** 个参数：

####### BOOLEAN 类型参数

######## 1. LinNmBusSynchronizationEnabled

- **UUID**: `ECUC:34aeae50-3f53-4ad2-ae2f-6d24cae5270b`
- **参数名**: `LinNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling bus synchronization support of the LinNm. This feature is required for NM Coordinator nodes only.

######## 2. LinNmComControlEnabled

- **UUID**: `ECUC:fffa7ced-3e7e-4677-bb33-686b51c7ba4e`
- **参数名**: `LinNmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Communication Control support.

######## 3. LinNmComUserDataSupport

- **UUID**: `ECUC:78d67e94-71c4-4acd-a90f-6b1307b0c31e`
- **参数名**: `LinNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the NM COM user data support

######## 4. LinNmCoordinatorSyncSupport

- **UUID**: `ECUC:9a677008-f8c6-4f6c-9719-52b509bbd794`
- **参数名**: `LinNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the coordinator synchronisation support.

######## 5. LinNmDevErrorDetect

- **UUID**: `ECUC:b7386aaf-43d7-44ef-aa6d-86024fcef154`
- **参数名**: `LinNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 6. LinNmNodeDetectionEnabled

- **UUID**: `ECUC:92b9c19d-7cb6-4146-bfd4-b36550278e56`
- **参数名**: `LinNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Node Detection feature.

######## 7. LinNmNodeIdEnabled

- **UUID**: `ECUC:91d52af8-19d3-4449-98d1-c902af211678`
- **参数名**: `LinNmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling transmission of the source node identifier in NM messages.

######## 8. LinNmPassiveModeEnabled

- **UUID**: `ECUC:67c1b2c5-48f6-41bb-8e42-f128d18c1530`
- **参数名**: `LinNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling support of the Passive Mode of the LinNm.

######## 9. LinNmRemoteSleepIndicationEnabled

- **UUID**: `ECUC:61c8f2bc-ea1c-415d-be2d-debd42b3dd45`
- **参数名**: `LinNmRemoteSleepIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling Remote Sleep Indication support. This feature is required for NM Coordinator nodes only.

######## 10. LinNmStateChangeIndEnabled

- **UUID**: `ECUC:ab459bd1-c4a1-4d4f-8b8a-5e8c70fa6c6e`
- **参数名**: `LinNmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Network Management state change notification.

######## 11. LinNmSynchronizationPointEnabled

- **UUID**: `ECUC:9e87222e-0b46-41f5-8407-11b4e8ff44e8`
- **参数名**: `LinNmSynchronizationPointEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the Synchronize NM feature.

######## 12. LinNmUserDataEnabled

- **UUID**: `ECUC:52314590-0421-48d3-bbf2-e15b7ec4f3b7`
- **参数名**: `LinNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling User Data support.

######## 13. LinNmVersionInfoApi

- **UUID**: `ECUC:f7596ee2-cac8-4869-998d-8eda86c28e5f`
- **参数名**: `LinNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling version info API support.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LinNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:a5ee4f06-740c-4bbb-bdfe-d5d513102e68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of the LinNm.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinNmComMNetworkHandleRef

- **UUID**: `ECUC:a58e0dac-8547-4692-a211-9779f082a36c`
- **引用名**: `LinNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

##### 2. LinNmChannelConfig

**容器属性**:

- **UUID**: `ECUC:a5ee4f06-740c-4bbb-bdfe-d5d513102e68`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinNmChannelConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the channel specific configuration parameter of the LinNm.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinNmComMNetworkHandleRef

- **UUID**: `ECUC:a58e0dac-8547-4692-a211-9779f082a36c`
- **引用名**: `LinNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This reference points to the unique channel defined by the ComMChannel and provides access to the unique channel index value in ComMChannelId.

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

1. **LinNm**
