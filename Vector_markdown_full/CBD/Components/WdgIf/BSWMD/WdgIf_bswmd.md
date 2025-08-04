# WdgIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [WdgIf](#wdgif)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. WdgIf

#### 基本信息

- **UUID**: `ECUC:a2dc5f81-f4d5-4986-bf4b-38652d4a8126`
- **模块名称**: `WdgIf`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Watchdog Interface. The interface allows the Watchdog Manager to select the correct Watchdog Driver - and thus the watchdog device - while retaining the API and functionality or the underlying driver.

#Safety #Supervision
#AUTOSAR

#### 版本历史

共有 **9** 个版本记录：

##### 1. 版本 6.00.00

- **状态**: released
- **发布日期**: 2016-06-16T01:55:18+02:00
- **发布者**: virchl

**变更内容**:

##### 2. 版本 6.00.01

- **状态**: released
- **发布日期**: 2016-10-21T07:46:14+02:00
- **发布者**: virchl

**变更内容**:

##### 3. 版本 6.01.00

- **状态**: released
- **发布日期**: 2017-01-04T03:41:23+01:00
- **发布者**: virchl

**变更内容**:

##### 4. 版本 6.01.01

- **状态**: released
- **发布日期**: 2018-05-29T09:01:46+02:00
- **发布者**: virchl

**变更内容**:

##### 5. 版本 6.02.00

- **状态**: released
- **发布日期**: 2018-11-09T13:56:36+01:00
- **发布者**: virchl

**变更内容**:

##### 6. 版本 6.03.00

- **状态**: released
- **发布日期**: 2019-08-06T01:00:02+02:00
- **发布者**: vircre

**变更内容**:

##### 7. 版本 6.04.00

- **状态**: released
- **发布日期**: 2021-01-20T11:26:33+01:00
- **发布者**: virbka

**变更内容**:

##### 8. 版本 7.00.00

- **状态**: released
- **发布日期**: 2021-07-23T14:33:06+02:00
- **发布者**: virbmz

**变更内容**:

##### 9. 版本 7.00.01

- **状态**: released
- **发布日期**: 2022-08-31T16:48:01+02:00
- **发布者**: virbmz

**变更内容**:

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. WdgIfDevice

**容器属性**:

- **UUID**: `ECUC:b5418b77-eccf-4831-acdd-b50dbb01413b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfDevice`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

It contains the information for the selection of a particular Watchdog device in case multiple Watchdog drivers are connected.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. WdgIfDeviceIndex

- **UUID**: `ECUC:41e5cd64-56e8-4593-b945-b615918cd5a7`
- **参数名**: `WdgIfDeviceIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Represents the watchdog Device ID so that it can be referenced by the watchdog manager.

####### STRING 类型参数

######## 1. WdgIfDeviceIncludeFile

- **UUID**: `3921e479-8a07-47fe-9bf8-471577f93ca8`
- **参数名**: `WdgIfDeviceIncludeFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the file name of the include file of the referenced watchdog device.

If the information is present in the referenced watchdog driver's description file, this parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case this field stays empty or another include file is required, please enter the include file manually.

####### FUNCTION-NAME 类型参数

######## 1. WdgIfDeviceSetMode

- **UUID**: `adce0337-34f6-4a56-90ac-305fe54f988c`
- **参数名**: `WdgIfDeviceSetMode`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the function name of the 'WdgIf_SetMode()'-service of the referenced watchdog device.

If the information is present in the referenced watchdog driver's description file, this parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case this field stays empty or another include file is required, please enter the function name manually.

The function to be called has to have a signature equal to the according AUTOSAR 4 API service specified in the Watchdog Driver:

void Wdg_SetMode(WdgIf_ModeType Mode)

######## 2. WdgIfDeviceSetTriggerCondition

- **UUID**: `b227f688-2379-41a0-b86e-bfa29240397c`
- **参数名**: `WdgIfDeviceSetTriggerCondition`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the function name of the 'WdgIf_SetTriggerCondition()'-service of the referenced watchdog device.

If the information is present in the referenced watchdog driver's description file, this parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case this field stays empty or another include file is required, please enter the function name manually.

The function to be called has to have a signature equal to the according AUTOSAR 4 API service specified in the Watchdog Driver:

void Wdg_SetTriggerCondition(uint16 timeout)

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgIfDriverRef

- **UUID**: `ECUC:c18b762d-1ffc-4203-9936-4e4539c6fea6`
- **引用名**: `WdgIfDriverRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Wdg/WdgGeneral`
  - `/MICROSAR/WdgIf/WdgIfStateCombiner/WdgIfStateCombinerMaster`
  - `/MICROSAR/WdgIf/WdgIfStateCombiner/WdgIfStateCombinerSlave`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the watchdog driver of this watchdog device or to a master or slave State Combiner instance.

##### 2. WdgIfGeneral

**容器属性**:

- **UUID**: `ECUC:2199b96d-33aa-488f-a1ae-99f6d4bd3c6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container collects all generic watchdog interface parameters.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. WdgIfDevErrorDetect

- **UUID**: `ECUC:4363aa34-c419-4350-b2cb-75ec7dfda67f`
- **参数名**: `WdgIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the development error reporting.

true: Development error reporting enabled
false: Development error reporting disabled

######## 2. WdgIfVersionInfoApi

- **UUID**: `ECUC:313c10c6-c907-4f72-a6d8-722b8886775b`
- **参数名**: `WdgIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the service returning the version information.

true: Version information service enabled
false: Version information service disabled

######## 3. WdgIfUseStateCombiner

- **UUID**: `b378669d-ebe0-4233-8fd6-bd9637f32e6b`
- **参数名**: `WdgIfUseStateCombiner`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the usage of the State Combiner feature, which is part of the WdgIf. If enabled, it allows WdgM instances running on different processor cores to share and trigger one watchdog device.

true: WdgIf State Combiner is enabled and must be configured.
false: WdgIf State Combiner is disabled.

##### 3. WdgIfStateCombiner

**容器属性**:

- **UUID**: `161c3800-7b98-4fcc-909c-625fadc351ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombiner`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes the optional  feature of the Safe Watchdog Interface - the State Combiner.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. WdgIfStateCombinerGeneral

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4981-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

All general parameters of the StateCombiner are collected here.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. WdgIfStateCombinerSpinlockID

- **UUID**: `df0f3704-27f5-4123-afc8-9fed0c812cec`
- **参数名**: `WdgIfStateCombinerSpinlockID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the spinlock used by the StateCombiner for inter-core synchronization.

Note: A direct reference to a configured OSSpinlock can be set within the parameter State Combiner OS Spinlock.

########## 2. WdgIfStateCombinerStartUpSyncCycles

- **UUID**: `e17b5cfd-f237-4306-9ba8-e572df587147`
- **参数名**: `WdgIfStateCombinerStartUpSyncCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of master cycles during start-up in which the master does not check the slave triggering. Used to synchronize master and slave during start-up.

######### BOOLEAN 类型参数

########## 1. WdgIfStateCombinerUseOsSpinlock

- **UUID**: `3a2855dd-871c-444c-aee9-2c12fd5f9d8b`
- **参数名**: `WdgIfStateCombinerUseOsSpinlock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the usage of OS spinlock mechanism. 

Note: If no OS spinlock is used a user-defined spinlock must be implemented - the file Appl_Spinlock.h will be inlcuded (instead of Os.h).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. WdgIfStateCombinerOSSpinlock

- **UUID**: `56e4476c-105c-4bfe-ba64-a614e8f9d678`
- **引用名**: `WdgIfStateCombinerOSSpinlock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsSpinlock`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsSpinlock`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the spinlock used by the StateCombiner for inter-core synchronization.

####### 2. WdgIfStateCombinerMaster

**容器属性**:

- **UUID**: `9fedf590-c93a-4244-b281-83a5d279a9f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerMaster`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters for the State Combiner master device.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. WdgIfStateCombinerMasterWdgRef

- **UUID**: `2935aef6-734d-4d71-91c1-d37edc0dea15`
- **引用名**: `WdgIfStateCombinerMasterWdgRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Wdg/WdgGeneral`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the watchdog driver serviced by the StateCombiner master.

######### CHOICE-REFERENCE 类型引用

########## 1. WdgIfGlobalMemoryAppTaskRef

- **UUID**: `29660165-6bd3-4bda-881e-01e75b971d4e`
- **引用名**: `WdgIfGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application. In case of OS SC3 the global variables of this State Combiner master device module should be placed in the same memory segment as the application that the overlying Watchdog Manager module is part of.

####### 3. WdgIfStateCombinerSlave

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4a81-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerSlave`
- **多重性**: [1..9]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Parameters for the State Combiner slave.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. WdgIfStateCombinerReferenceCycle

- **UUID**: `4799060c-77c0-44e6-9aab-10d62da2f50a`
- **参数名**: `WdgIfStateCombinerReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the reference cycle of the master for this slave.

########## 2. WdgIfStateCombinerSlaveIncrementsMin

- **UUID**: `68de33f7-fbe8-4a5d-885a-23ebc9e471d8`
- **参数名**: `WdgIfStateCombinerSlaveIncrementsMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the minimum allowed number of increments (triggers) for slave instance in one master check period.

Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMin is equal to WdgIfStateCombinerSlaveIncrementsMax.

########## 3. WdgIfStateCombinerSlaveIncrementsMax

- **UUID**: `6fc1fb14-aeeb-436b-a117-a82cf01783a0`
- **参数名**: `WdgIfStateCombinerSlaveIncrementsMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum allowed number of increments (triggers) for slave instance in one master check period.

Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMax is equal to WdgIfStateCombinerSlaveIncrementsMin.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. WdgIfGlobalMemoryAppTaskRef

- **UUID**: `5ce282c9-71d2-4d44-a769-acad2946221b`
- **引用名**: `WdgIfGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used.

Reference to an OS Application. In case of OS SC3 the global variables of this State Combiner slave device should be placed in the same memory segment as the application that the overlying Watchdog Manager module is part of.

##### 4. WdgIfStateCombinerGeneral

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4981-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

All general parameters of the StateCombiner are collected here.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. WdgIfStateCombinerSpinlockID

- **UUID**: `df0f3704-27f5-4123-afc8-9fed0c812cec`
- **参数名**: `WdgIfStateCombinerSpinlockID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID of the spinlock used by the StateCombiner for inter-core synchronization.

Note: A direct reference to a configured OSSpinlock can be set within the parameter State Combiner OS Spinlock.

######## 2. WdgIfStateCombinerStartUpSyncCycles

- **UUID**: `e17b5cfd-f237-4306-9ba8-e572df587147`
- **参数名**: `WdgIfStateCombinerStartUpSyncCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of master cycles during start-up in which the master does not check the slave triggering. Used to synchronize master and slave during start-up.

####### BOOLEAN 类型参数

######## 1. WdgIfStateCombinerUseOsSpinlock

- **UUID**: `3a2855dd-871c-444c-aee9-2c12fd5f9d8b`
- **参数名**: `WdgIfStateCombinerUseOsSpinlock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This preprocessor switch enables/disables the usage of OS spinlock mechanism. 

Note: If no OS spinlock is used a user-defined spinlock must be implemented - the file Appl_Spinlock.h will be inlcuded (instead of Os.h).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. WdgIfStateCombinerOSSpinlock

- **UUID**: `56e4476c-105c-4bfe-ba64-a614e8f9d678`
- **引用名**: `WdgIfStateCombinerOSSpinlock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsSpinlock`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsSpinlock`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the spinlock used by the StateCombiner for inter-core synchronization.

##### 5. WdgIfStateCombinerMaster

**容器属性**:

- **UUID**: `9fedf590-c93a-4244-b281-83a5d279a9f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerMaster`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Parameters for the State Combiner master device.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. WdgIfStateCombinerMasterWdgRef

- **UUID**: `2935aef6-734d-4d71-91c1-d37edc0dea15`
- **引用名**: `WdgIfStateCombinerMasterWdgRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Wdg/WdgGeneral`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the watchdog driver serviced by the StateCombiner master.

####### CHOICE-REFERENCE 类型引用

######## 1. WdgIfGlobalMemoryAppTaskRef

- **UUID**: `29660165-6bd3-4bda-881e-01e75b971d4e`
- **引用名**: `WdgIfGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS Application. In case of OS SC3 the global variables of this State Combiner master device module should be placed in the same memory segment as the application that the overlying Watchdog Manager module is part of.

##### 6. WdgIfStateCombinerSlave

**容器属性**:

- **UUID**: `ECUC:d3088cb2-0610-4a81-bede-0f4539127001`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfStateCombinerSlave`
- **多重性**: [1..9]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Parameters for the State Combiner slave.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. WdgIfStateCombinerReferenceCycle

- **UUID**: `4799060c-77c0-44e6-9aab-10d62da2f50a`
- **参数名**: `WdgIfStateCombinerReferenceCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the reference cycle of the master for this slave.

######## 2. WdgIfStateCombinerSlaveIncrementsMin

- **UUID**: `68de33f7-fbe8-4a5d-885a-23ebc9e471d8`
- **参数名**: `WdgIfStateCombinerSlaveIncrementsMin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the minimum allowed number of increments (triggers) for slave instance in one master check period.

Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMin is equal to WdgIfStateCombinerSlaveIncrementsMax.

######## 3. WdgIfStateCombinerSlaveIncrementsMax

- **UUID**: `6fc1fb14-aeeb-436b-a117-a82cf01783a0`
- **参数名**: `WdgIfStateCombinerSlaveIncrementsMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum allowed number of increments (triggers) for slave instance in one master check period.

Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMax is equal to WdgIfStateCombinerSlaveIncrementsMin.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. WdgIfGlobalMemoryAppTaskRef

- **UUID**: `5ce282c9-71d2-4d44-a769-acad2946221b`
- **引用名**: `WdgIfGlobalMemoryAppTaskRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsApplication`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used.

Reference to an OS Application. In case of OS SC3 the global variables of this State Combiner slave device should be placed in the same memory segment as the application that the overlying Watchdog Manager module is part of.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **WdgIf_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **WdgIf**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **WdgIf_Pre**
2. **WdgIf_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. WdgIf_Impl

- **UUID**: `ad84c620-a803-42c5-8183-2f6ad36564c7`
- **实现名称**: `WdgIf_Impl`
- **编程语言**: C
- **软件版本**: 5.05.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.02
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. WdgIf_Pre

- **UUID**: `28184d7b-e19b-467f-b69d-57195ed2cbe6`
- **配置名称**: `WdgIf_Pre`
- **定义引用**: `/MICROSAR/WdgIf`

### 2. WdgIf_Rec

- **UUID**: `50672f52-7b42-4e19-82ce-8dc1298afa02`
- **配置名称**: `WdgIf_Rec`
- **定义引用**: `/MICROSAR/WdgIf`
