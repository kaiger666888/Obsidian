# LinSM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:52

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LinSM](#linsm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LinSM

#### 基本信息

- **UUID**: `ECUC:240b0def-26c5-4bd2-ae58-1b5b570c70a4`
- **模块名称**: `LinSM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Lin State Manager module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. LinSMConfigSet

**容器属性**:

- **UUID**: `ECUC:e7feb268-3b18-485b-a48b-efc93ff35bec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container describes one of multiple configuration sets of LinSm.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. LinSMChannel

**容器属性**:

- **UUID**: `ECUC:8a11f492-22a7-4281-9060-5dae0f844c5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes each LIN channel the LinSM is connected to.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. LinSMSleepSupport

- **UUID**: `ECUC:dbc022f5-65ae-421b-bdb7-4e547fa5b0de`
- **参数名**: `LinSMSleepSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Some LIN clusters does not need sleep, they will just shut off. This parameter will affect the behavior to achieve the no communication state.

########## 2. LinSMTransceiverPassiveMode

- **UUID**: `ECUC:725086a2-39ce-474c-8be0-51d4f15000cb`
- **参数名**: `LinSMTransceiverPassiveMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects STANDBY (true) or SLEEP (false) transceiver mode when entering LINSM_NO_COM.

######### FLOAT 类型参数

########## 1. LinSMConfirmationTimeout

- **UUID**: `ECUC:f789b753-d4a6-41c6-858d-74962c64921e`
- **参数名**: `LinSMConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in seconds for the goto sleep and wakeup calls to LinIf. The timeout must be longer than a goto-sleep command on the bus (i.e. it is bit rate dependent).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinSMComMNetworkHandleRef

- **UUID**: `ECUC:da189e8d-231d-4b36-8d21-f413789897a0`
- **引用名**: `LinSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain LIN network. Reference to one of the network handles configured in the ComM.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinSMSchedule

**容器属性**:

- **UUID**: `ECUC:822d7642-7685-45cb-a7f9-6438539a9b18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMSchedule`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The schedule references to a schedule that is located in the LinIf configuration. Moreover, the PDU groups are located in the COM configuration. Note that there are two references to PDU groups. The simple reason is that a PDU group is only allowed to contain one direction (TX or RX).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. LinSMScheduleIndex

- **UUID**: `ECUC:f5c68884-c8e8-4f73-93dd-92f3e25b8532`
- **参数名**: `LinSMScheduleIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This index parameter can be used by the BswM as a  SymbolicNameReference target. The LinSM just forwards the request from the BswM to LinIf. Note that the value of the LinSMScheduleIndex shall be the same as the value from the LinIf.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. LinSMScheduleIndexRef

- **UUID**: `ECUC:9627768d-4365-4d19-8861-3d50af9d645c`
- **引用名**: `LinSMScheduleIndexRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a schedule table in the LinIf configuration

####### 2. LinSMSchedule

**容器属性**:

- **UUID**: `ECUC:822d7642-7685-45cb-a7f9-6438539a9b18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMSchedule`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The schedule references to a schedule that is located in the LinIf configuration. Moreover, the PDU groups are located in the COM configuration. Note that there are two references to PDU groups. The simple reason is that a PDU group is only allowed to contain one direction (TX or RX).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. LinSMScheduleIndex

- **UUID**: `ECUC:f5c68884-c8e8-4f73-93dd-92f3e25b8532`
- **参数名**: `LinSMScheduleIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This index parameter can be used by the BswM as a  SymbolicNameReference target. The LinSM just forwards the request from the BswM to LinIf. Note that the value of the LinSMScheduleIndex shall be the same as the value from the LinIf.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinSMScheduleIndexRef

- **UUID**: `ECUC:9627768d-4365-4d19-8861-3d50af9d645c`
- **引用名**: `LinSMScheduleIndexRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a schedule table in the LinIf configuration

##### 2. LinSMChannel

**容器属性**:

- **UUID**: `ECUC:8a11f492-22a7-4281-9060-5dae0f844c5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes each LIN channel the LinSM is connected to.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. LinSMSleepSupport

- **UUID**: `ECUC:dbc022f5-65ae-421b-bdb7-4e547fa5b0de`
- **参数名**: `LinSMSleepSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Some LIN clusters does not need sleep, they will just shut off. This parameter will affect the behavior to achieve the no communication state.

######## 2. LinSMTransceiverPassiveMode

- **UUID**: `ECUC:725086a2-39ce-474c-8be0-51d4f15000cb`
- **参数名**: `LinSMTransceiverPassiveMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects STANDBY (true) or SLEEP (false) transceiver mode when entering LINSM_NO_COM.

####### FLOAT 类型参数

######## 1. LinSMConfirmationTimeout

- **UUID**: `ECUC:f789b753-d4a6-41c6-858d-74962c64921e`
- **参数名**: `LinSMConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in seconds for the goto sleep and wakeup calls to LinIf. The timeout must be longer than a goto-sleep command on the bus (i.e. it is bit rate dependent).

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinSMComMNetworkHandleRef

- **UUID**: `ECUC:da189e8d-231d-4b36-8d21-f413789897a0`
- **引用名**: `LinSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain LIN network. Reference to one of the network handles configured in the ComM.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LinSMSchedule

**容器属性**:

- **UUID**: `ECUC:822d7642-7685-45cb-a7f9-6438539a9b18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMSchedule`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The schedule references to a schedule that is located in the LinIf configuration. Moreover, the PDU groups are located in the COM configuration. Note that there are two references to PDU groups. The simple reason is that a PDU group is only allowed to contain one direction (TX or RX).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. LinSMScheduleIndex

- **UUID**: `ECUC:f5c68884-c8e8-4f73-93dd-92f3e25b8532`
- **参数名**: `LinSMScheduleIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This index parameter can be used by the BswM as a  SymbolicNameReference target. The LinSM just forwards the request from the BswM to LinIf. Note that the value of the LinSMScheduleIndex shall be the same as the value from the LinIf.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinSMScheduleIndexRef

- **UUID**: `ECUC:9627768d-4365-4d19-8861-3d50af9d645c`
- **引用名**: `LinSMScheduleIndexRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a schedule table in the LinIf configuration

##### 3. LinSMSchedule

**容器属性**:

- **UUID**: `ECUC:822d7642-7685-45cb-a7f9-6438539a9b18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMSchedule`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The schedule references to a schedule that is located in the LinIf configuration. Moreover, the PDU groups are located in the COM configuration. Note that there are two references to PDU groups. The simple reason is that a PDU group is only allowed to contain one direction (TX or RX).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. LinSMScheduleIndex

- **UUID**: `ECUC:f5c68884-c8e8-4f73-93dd-92f3e25b8532`
- **参数名**: `LinSMScheduleIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This index parameter can be used by the BswM as a  SymbolicNameReference target. The LinSM just forwards the request from the BswM to LinIf. Note that the value of the LinSMScheduleIndex shall be the same as the value from the LinIf.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinSMScheduleIndexRef

- **UUID**: `ECUC:9627768d-4365-4d19-8861-3d50af9d645c`
- **引用名**: `LinSMScheduleIndexRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a schedule table in the LinIf configuration

##### 4. LinSMGeneral

**容器属性**:

- **UUID**: `ECUC:d2be68b0-eae8-4082-b021-e1c67fdc3a4b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinSMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains general parameters of LIN State Manager module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. LinSMDevErrorDetect

- **UUID**: `ECUC:720778ca-0908-4c9a-b0f7-b3f7e2258bb1`
- **参数名**: `LinSMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. LinSMVersionInfoApi

- **UUID**: `ECUC:ef96408d-a53b-442d-87f2-d537f8761957`
- **参数名**: `LinSMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the LinSM_GetVersionInfo function ON or OFF.

####### FLOAT 类型参数

######## 1. LinSMMainProcessingPeriod

- **UUID**: `ECUC:a7cedc57-8695-465d-8362-47dc7178afee`
- **参数名**: `LinSMMainProcessingPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Fixed period that the MainFunction shall be called.

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

1. **LinSM**
