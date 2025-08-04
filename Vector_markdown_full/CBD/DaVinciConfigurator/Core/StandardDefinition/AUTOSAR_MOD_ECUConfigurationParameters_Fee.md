# Fee - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Fee](#fee)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Fee

#### 基本信息

- **UUID**: `ECUC:25e46613-7e63-4604-a81c-33867a9d91f7`
- **模块名称**: `Fee`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Fee (Flash EEPROM Emulation) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. FeeBlockConfiguration

**容器属性**:

- **UUID**: `ECUC:3e3f6a41-1274-4d00-b94d-504e69110cfa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeBlockConfiguration`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of block specific parameters for the Flash EEPROM Emulation module.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. FeeBlockNumber

- **UUID**: `ECUC:0a407883-2fc6-4823-a26e-ea079aa7e73f`
- **参数名**: `FeeBlockNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Block identifier (handle).

######## 2. FeeBlockSize

- **UUID**: `ECUC:24bf18c3-8512-4334-8585-6c7937444d1d`
- **参数名**: `FeeBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of a logical block in bytes.

######## 3. FeeNumberOfWriteCycles

- **UUID**: `ECUC:b55e41d9-f6b5-4613-937e-2b83fe37a654`
- **参数名**: `FeeNumberOfWriteCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of write cycles required for this block.

####### BOOLEAN 类型参数

######## 1. FeeImmediateData

- **UUID**: `ECUC:b1116e04-53cd-44a7-8056-f43434aa82c8`
- **参数名**: `FeeImmediateData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Marker for high priority data.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FeeDeviceIndex

- **UUID**: `ECUC:f3bfa469-e131-4f58-bb89-ca7fc4548d25`
- **引用名**: `FeeDeviceIndex`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FlsGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Fls/FlsGeneral`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Device index (handle).

##### 2. FeeGeneral

**容器属性**:

- **UUID**: `ECUC:40da9e07-9e9a-4777-85e7-a111b37d8453`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeeGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container for general parameters. These parameters are not specific to a block.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. FeeIndex

- **UUID**: `ECUC:0de3db3d-02d0-4bbd-a4df-8e82cfa0ec48`
- **参数名**: `FeeIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. FeeVirtualPageSize

- **UUID**: `ECUC:cfc06841-4637-4082-9f2e-57de66655c6f`
- **参数名**: `FeeVirtualPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The size in bytes to which logical blocks shall be aligned.

####### BOOLEAN 类型参数

######## 1. FeeDevErrorDetect

- **UUID**: `ECUC:f262f806-4d29-4ef6-b4c1-6167282e1f21`
- **参数名**: `FeeDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection.

######## 2. FeePollingMode

- **UUID**: `ECUC:cbbd2e13-d937-4e0f-8546-6ea5cc3b7eeb`
- **参数名**: `FeePollingMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable the polling mode for this module.

######## 3. FeeSetModeSupported

- **UUID**: `ECUC:f064e794-edd8-4288-b518-84c07839383d`
- **参数名**: `FeeSetModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compiler switch to enable/disable the 'SetMode' functionality of the FEE module.

######## 4. FeeVersionInfoApi

- **UUID**: `ECUC:e66783a5-0bb8-4060-83ed-985d387af3a5`
- **参数名**: `FeeVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

####### FUNCTION-NAME 类型参数

######## 1. FeeNvmJobEndNotification

- **UUID**: `ECUC:3b4f73c8-354a-4d0e-86e6-0e2d07ba5590`
- **参数名**: `FeeNvmJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job end notification routine provided by the upper layer module (NvM_JobEndNotification).

######## 2. FeeNvmJobErrorNotification

- **UUID**: `ECUC:9a658f03-834b-4dd3-add7-58b968076e7d`
- **参数名**: `FeeNvmJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job error notification routine provided by the upper layer module (NvM_JobErrorNotification).

##### 3. FeePublishedInformation

**容器属性**:

- **UUID**: `ECUC:c99d74b3-e634-4c09-b512-87583d22c249`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FeePublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FeeBlockOverhead

- **UUID**: `ECUC:05f4fdfa-6b05-4960-973e-f62746494b3d`
- **参数名**: `FeeBlockOverhead`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Management overhead per logical block in bytes.

######## 2. FeePageOverhead

- **UUID**: `ECUC:ff042c2b-4ea3-4cc9-b210-6b4956da10d9`
- **参数名**: `FeePageOverhead`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Management overhead per page in bytes.

####### FLOAT 类型参数

######## 1. FeeMaximumBlockingTime

- **UUID**: `ECUC:4c8210b6-42e3-416f-a8cc-f2c6b95f3131`
- **参数名**: `FeeMaximumBlockingTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: The maximum time the FEE module's API routines shall be blocked (delayed) by internal operations.

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

1. **Fee**
