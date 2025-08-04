# FiM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FiM](#fim)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FiM

#### 基本信息

- **UUID**: `ECUC:3a868adf-7ee4-48a9-ae4f-f9121051c21c`
- **模块名称**: `FiM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FiM (Function Inhibition Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **10** 个配置容器：

##### 1. FiMConfigSet

**容器属性**:

- **UUID**: `ECUC:92c3d3e8-2d78-4cf6-8662-253c9568de3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the FiM module supporting multiple configuration sets.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. FiMEventSummary

**容器属性**:

- **UUID**: `ECUC:7136c4ed-9dc7-4d52-b03d-348ab1b7a203`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMEventSummary`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The summarized EventId definition record consists of a summarized event ID and a specific EventId.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInputSumEventRef

- **UUID**: `ECUC:000aaf34-3a3b-4147-a87d-9edf2e9867bd`
- **引用名**: `FiMInputSumEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 2. FiMOutputSumEventRef

- **UUID**: `ECUC:fd8d61f6-3a8a-4177-bd17-de31c415a9bd`
- **引用名**: `FiMOutputSumEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 2. FiMFID

**容器属性**:

- **UUID**: `ECUC:3ec17008-a8aa-4e4d-b1b9-74a3176cc2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMFID`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container includes symbolic names of all FIDs.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FiMFunctionId

- **UUID**: `ECUC:4e9128d4-fc8a-4ef3-b331-52606638dd6c`
- **参数名**: `FiMFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The configuration parameter is used as an ID which represents a functionality. FiMFunctionId is the unique identifier assigned during FIM configuration.

####### 3. FiMInhibitionConfiguration

**容器属性**:

- **UUID**: `ECUC:09954cb0-1956-4c20-a3ce-8ee76f5b30d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhibitionConfiguration`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container includes all configuration parameters concerning the relationship between event and FID.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FiMInhInhibitionMask

- **UUID**: `ECUC:443b29c5-cf49-4c7b-8582-59e6e0532312`
- **参数名**: `FiMInhInhibitionMask`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FIM_LAST_FAILED` (来源: AUTOSAR_ECUC)
  - `FIM_NOT_TESTED` (来源: AUTOSAR_ECUC)
  - `FIM_TESTED` (来源: AUTOSAR_ECUC)
  - `FIM_TESTED_AND_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The configuration parameter is used to specify the inhibition mask for an event - FID relation.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FiMInhFunctionIdRef

- **UUID**: `ECUC:d62211af-faa5-4deb-8f43-c5180e45ee6c`
- **引用名**: `FiMInhFunctionIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. FiMInhEventId

**容器属性**:

- **UUID**: `ECUC:6a36a36f-e5c2-402d-84ea-b4cd27145786`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhEventId`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

The configuration parameter is used for an existing DEM event and summarized events as well.

########## 配置容器

本模块包含 **3** 个配置容器：

########### 1. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

########### 2. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

########### 3. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

######### 2. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

######### 3. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

######### 4. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

####### 4. FiMInhEventId

**容器属性**:

- **UUID**: `ECUC:6a36a36f-e5c2-402d-84ea-b4cd27145786`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhEventId`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

The configuration parameter is used for an existing DEM event and summarized events as well.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

######### 2. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

######### 3. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

####### 5. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

####### 6. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

####### 7. FiMSummaryEventId

**容器属性**:

- **UUID**: `ECUC:c2b04e53-d5ee-4941-832c-5c95aeb4bf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMSummaryEventId`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container defines the name of a summarized event.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FiMEventSumId

- **UUID**: `ECUC:906d9540-09ca-492a-a104-3d425367d0a3`
- **参数名**: `FiMEventSumId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The summarized EventId definition record defines the existence of a summarized event with a specific name. This summarized event can be referenced in the EventSummary (as FimSummaryEventId) and Inhibition configuration (as FimInhEventId).

####### 8. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

##### 2. FiMEventSummary

**容器属性**:

- **UUID**: `ECUC:7136c4ed-9dc7-4d52-b03d-348ab1b7a203`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMEventSummary`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The summarized EventId definition record consists of a summarized event ID and a specific EventId.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FiMInputSumEventRef

- **UUID**: `ECUC:000aaf34-3a3b-4147-a87d-9edf2e9867bd`
- **引用名**: `FiMInputSumEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 2. FiMOutputSumEventRef

- **UUID**: `ECUC:fd8d61f6-3a8a-4177-bd17-de31c415a9bd`
- **引用名**: `FiMOutputSumEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 3. FiMFID

**容器属性**:

- **UUID**: `ECUC:3ec17008-a8aa-4e4d-b1b9-74a3176cc2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMFID`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container includes symbolic names of all FIDs.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FiMFunctionId

- **UUID**: `ECUC:4e9128d4-fc8a-4ef3-b331-52606638dd6c`
- **参数名**: `FiMFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The configuration parameter is used as an ID which represents a functionality. FiMFunctionId is the unique identifier assigned during FIM configuration.

##### 4. FiMInhibitionConfiguration

**容器属性**:

- **UUID**: `ECUC:09954cb0-1956-4c20-a3ce-8ee76f5b30d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhibitionConfiguration`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container includes all configuration parameters concerning the relationship between event and FID.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FiMInhInhibitionMask

- **UUID**: `ECUC:443b29c5-cf49-4c7b-8582-59e6e0532312`
- **参数名**: `FiMInhInhibitionMask`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FIM_LAST_FAILED` (来源: AUTOSAR_ECUC)
  - `FIM_NOT_TESTED` (来源: AUTOSAR_ECUC)
  - `FIM_TESTED` (来源: AUTOSAR_ECUC)
  - `FIM_TESTED_AND_FAILED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The configuration parameter is used to specify the inhibition mask for an event - FID relation.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FiMInhFunctionIdRef

- **UUID**: `ECUC:d62211af-faa5-4deb-8f43-c5180e45ee6c`
- **引用名**: `FiMInhFunctionIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FiMFID`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMFID`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FiMInhEventId

**容器属性**:

- **UUID**: `ECUC:6a36a36f-e5c2-402d-84ea-b4cd27145786`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhEventId`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

The configuration parameter is used for an existing DEM event and summarized events as well.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

######### 2. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

######### 3. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

####### 2. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

####### 3. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

####### 4. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

##### 5. FiMInhEventId

**容器属性**:

- **UUID**: `ECUC:6a36a36f-e5c2-402d-84ea-b4cd27145786`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhEventId`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

The configuration parameter is used for an existing DEM event and summarized events as well.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

####### 2. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

####### 3. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

##### 6. FiMInhChoiceDemRef

**容器属性**:

- **UUID**: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceDemRef`
- **多重性**: [0..1]
- **多配置容器**: false

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FiMInhEventRef

- **UUID**: `ECUC:938340c0-461d-4a84-9d24-6ff1e28f935d`
- **引用名**: `FiMInhEventRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC

##### 7. FiMInhChoiceSumRef

**容器属性**:

- **UUID**: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMInhChoiceSumRef`
- **多重性**: [0..1]
- **多配置容器**: false

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FiMInhSumRef

- **UUID**: `ECUC:00638370-e1ec-4ce4-9ac1-f7e7c49c0345`
- **引用名**: `FiMInhSumRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `FiMSummaryEventId`
- **完整路径**: `/AUTOSAR/EcucDefs/FiM/FiMConfigSet/FiMSummaryEventId`
- **来源**: AUTOSAR_ECUC

##### 8. FiMSummaryEventId

**容器属性**:

- **UUID**: `ECUC:c2b04e53-d5ee-4941-832c-5c95aeb4bf31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMSummaryEventId`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container defines the name of a summarized event.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FiMEventSumId

- **UUID**: `ECUC:906d9540-09ca-492a-a104-3d425367d0a3`
- **参数名**: `FiMEventSumId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The summarized EventId definition record defines the existence of a summarized event with a specific name. This summarized event can be referenced in the EventSummary (as FimSummaryEventId) and Inhibition configuration (as FimInhEventId).

##### 9. FiMGeneral

**容器属性**:

- **UUID**: `ECUC:1fefbc13-e456-4fa8-a5e3-9fd767440f73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FiMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. FiMMaxEventFidLinks

- **UUID**: `ECUC:27eb74f2-ad3f-4ed4-8eff-9046978b012c`
- **参数名**: `FiMMaxEventFidLinks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the total maximum number of links between EventIds and FIDs.

######## 2. FiMMaxEventsPerFid

- **UUID**: `ECUC:ad1776ee-5a14-4823-83f5-922ee80dcdeb`
- **参数名**: `FiMMaxEventsPerFid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the maximum number of EventIds that can be linked to a single FID.

######## 3. FiMMaxFidsPerEvent

- **UUID**: `ECUC:9926ad1c-02e6-4b88-bb3d-e160c0bcd33f`
- **参数名**: `FiMMaxFidsPerEvent`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the maximum number of FIDs that can be linked to a single event.

######## 4. FiMMaxSummaryEvents

- **UUID**: `ECUC:0756305a-56e5-4d42-99cc-07be6edb08bd`
- **参数名**: `FiMMaxSummaryEvents`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the maximum number of summarized events that can be configured.

######## 5. FiMMaxSummaryLinks

- **UUID**: `ECUC:45127248-c9d3-451b-a035-46855f9f5388`
- **参数名**: `FiMMaxSummaryLinks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the total maximum number of links between EventIds and summarized events.

######## 6. FiMMaxTotalLinks

- **UUID**: `ECUC:6ca81d5f-ee4a-48fd-a987-f736dae99803`
- **参数名**: `FiMMaxTotalLinks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the total maximum number of links between EventIds and FIDs plus the number of links between EventIds and summarized events.

####### BOOLEAN 类型参数

######## 1. FiMDataFixed

- **UUID**: `ECUC:a3ee7adb-c2d7-43a6-b8ed-b8526cf06ed1`
- **参数名**: `FiMDataFixed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable or disable calibration of inhibit relations The scope of the parameter is to meet the requirement (FIM008) to have the option to calibrate inhibit data on the one hand side and also to provide the option to protect inhibit data for consistency reasons.

######## 2. FiMDevErrorDetect

- **UUID**: `ECUC:b40e8f55-914f-4246-a740-8dec760c175a`
- **参数名**: `FiMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter is used to switch on or to switch off the detection of development errors during development.

######## 3. FiMEventUpdateTriggeredByDem

- **UUID**: `ECUC:15432f09-f726-48c2-8e36-3805bdaa7814`
- **参数名**: `FiMEventUpdateTriggeredByDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter specifies the way FIM obtains status of EventIds.

######## 4. FiMVersionInfoApi

- **UUID**: `ECUC:707f04d4-21c1-4396-8ffb-9cdea7af6a9f`
- **参数名**: `FiMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter is used to switch on or to switch off the API to get the version information.

####### FLOAT 类型参数

######## 1. FiMTaskTime

- **UUID**: `ECUC:c3ad0321-2dfe-4e88-88a9-ccabd4e3cf55`
- **参数名**: `FiMTaskTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.1]
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allow to configure the time for the periodic cyclic task. Please note: This configuration value shall be equal to the value in the Basic Software Scheduler configuration of the RTE module.

##### 10. FiMInhRefChoice

**容器属性**:

- **UUID**: `ECUC:a76c6271-ce5b-4fe6-aa3c-e4b054925253`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FiMInhRefChoice`
- **多重性**: [1..1]

**容器选择**:

- **FiMInhChoiceDemRef**
  - UUID: `ECUC:74ebb3d5-4ab1-4f29-b5b3-22523e4dfd2c`
- **FiMInhChoiceSumRef**
  - UUID: `ECUC:e85c9418-b2ae-4520-9c4a-1f446ed03c47`

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

1. **FiM**
