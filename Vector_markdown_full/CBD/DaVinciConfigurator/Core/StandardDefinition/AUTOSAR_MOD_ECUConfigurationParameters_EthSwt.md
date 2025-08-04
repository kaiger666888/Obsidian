# EthSwt - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:16

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthSwt](#ethswt)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthSwt

#### 基本信息

- **UUID**: `ECUC:79dfb782-ae0e-4458-acea-4fd1bf19c6d8`
- **模块名称**: `EthSwt`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the EthSwt (Ethernet Switch Driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.6.0

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. EthSwtConfig

**容器属性**:

- **UUID**: `ECUC:022b64c0-dcee-45d9-8dab-0ec9632c50ec`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtConfig`
- **多重性**: [1..infinite]

**容器描述**:

Configuration of one Ethernet Switch.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtIdx

- **UUID**: `ECUC:666187aa-c9d0-4ff8-9b55-50a3526b0ced`
- **参数名**: `EthSwtIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Specifies the instance ID of the configured Ethernet Switch.

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. EthSwtDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:d9439cbe-74df-469f-9869-1e59b2158ca8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHSWT_E_ACCESS

- **UUID**: `ECUC:6d0e97ed-01b9-4f47-b005-2742bb9752b8`
- **引用名**: `ETHSWT_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Ethernet Switch Access Failure" has occurred.

####### 2. EthSwtNvm

**容器属性**:

- **UUID**: `ECUC:d7833215-cb74-44be-9b61-ac433690ccf7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtNvm`
- **多重性**: [0..1]

**容器描述**:

Configuration of one Ethernet Switch Nvm usage in case the module requires non volatile memory in the Ecu to store switch configuration.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthSwtNvmBlockDescriptorRef

- **UUID**: `ECUC:d80a068c-a983-4a55-9329-88e4e7488c1f`
- **引用名**: `EthSwtNvmBlockDescriptorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

####### 3. EthSwtPort

**容器属性**:

- **UUID**: `ECUC:60c612bd-d595-4d5e-80cc-0b360b27db11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPort`
- **多重性**: [1..infinite]

**容器描述**:

Configuration of one Ethernet Switch Port.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortIdx

- **UUID**: `ECUC:01e9df96-9db2-47ba-9086-9aa958cf08c4`
- **参数名**: `EthSwtPortIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Specifies the instance ID of the configured Ethernet Switch Port.

######### BOOLEAN 类型参数

########## 1. EthSwtPortEnableLinkDownCallback

- **UUID**: `ECUC:ef9ae984-adc2-43f9-bb45-398f6a12e6f2`
- **参数名**: `EthSwtPortEnableLinkDownCallback`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables the callback <User>_LinkDown for this EthSwtPort if an IEEE802.1X link loss is detected.

######### STRING 类型参数

########## 1. EthSwtPortPredefinedMacAddresses

- **UUID**: `ECUC:144e0e11-79ac-4473-9457-b4203cc98786`
- **参数名**: `EthSwtPortPredefinedMacAddresses`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[0-9a-fA-F]{2}[[:-][0-9a-fA-F]{2}]{5}`
- **描述**: Specifies a list of 48-bit physical addresses (MAC addresses) which can be reached via this port in network byte order.

######### ENUMERATION 类型参数

########## 1. EthSwtPortPhysicalLayerType

- **UUID**: `ECUC:0ba2ef58-bb99-4b33-a847-bd2c6dfa503b`
- **参数名**: `EthSwtPortPhysicalLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_PORT_BASE_T` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_BROAD_R_REACH` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_RTPGE` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_X_MII` (来源: AUTOSAR_ECUC)
- **描述**: Defines the physical layer type on this EthSwtPort.

########## 2. EthSwtPortSpeed

- **UUID**: `ECUC:d91d6ae3-d025-4366-a127-fe31196c8183`
- **参数名**: `EthSwtPortSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_PORT_SPEED_10` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_SPEED_100` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_SPEED_1000` (来源: AUTOSAR_ECUC)
- **描述**: Defines the communication speed in Mbit per second on this EthSwtPort in case no EthSwtPortTrcvRef is defined.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthSwtPortTrcvRef

- **UUID**: `ECUC:87a2557d-4030-4760-b6ad-713aad1cfcca`
- **引用名**: `EthSwtPortTrcvRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthTrcvConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet/EthTrcvConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ethernet transceiver driver this EthSwtPort is connected with.

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. EthSwtPortEgress

**容器属性**:

- **UUID**: `ECUC:c6580740-35c3-4d5f-89a3-e3e5f39d23ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortEgress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port Egress behavior.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EthSwtPortEgressLastSchedulerRef

- **UUID**: `ECUC:cea09fae-5a0f-486e-b7cc-4f3db96b65fa`
- **引用名**: `EthSwtPortEgressLastSchedulerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortScheduler`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the port scheduler which is the last in the egress port structure.

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

########### 2. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

############## 引用关系

此容器包含 **1** 个引用：

############### CHOICE-REFERENCE 类型引用

################ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

########### 3. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

########### 4. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

########### 5. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

############## 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

############# ENUMERATION 类型参数

############## 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

######### 2. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

######### 3. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 4. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 5. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

######### 6. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

############ 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

########### ENUMERATION 类型参数

############ 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

######### 7. EthSwtPortIngress

**容器属性**:

- **UUID**: `ECUC:6201a610-faee-41a6-b33f-1055b2dc404e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortIngress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port ingress behavior.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortIngressVlanModification

- **UUID**: `ECUC:fb3ff4fc-7e38-4211-a5ef-e4de2de24e19`
- **参数名**: `EthSwtPortIngressVlanModification`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all messages which arrive at this ingress port will be tagged with this VLAN Id. This tagging happen also if the arriving message already has a VLAN Id, it will be overwritten by the defined one.

############ 2. EthSwtPortTrafficClassAssignment

- **UUID**: `ECUC:dfae6cad-011a-422c-b718-6c61c19a5607`
- **参数名**: `EthSwtPortTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all arriving messages at this ingress port shall be assigned this traffic class.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

############## 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

########### 2. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

############## 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

######### 8. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

############ 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

######### 9. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

############ 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

####### 4. EthSwtPortEgress

**容器属性**:

- **UUID**: `ECUC:c6580740-35c3-4d5f-89a3-e3e5f39d23ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortEgress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port Egress behavior.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthSwtPortEgressLastSchedulerRef

- **UUID**: `ECUC:cea09fae-5a0f-486e-b7cc-4f3db96b65fa`
- **引用名**: `EthSwtPortEgressLastSchedulerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortScheduler`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the port scheduler which is the last in the egress port structure.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

######### 2. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 3. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 4. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

######### 5. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

############ 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

########### ENUMERATION 类型参数

############ 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

####### 5. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

####### 6. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 7. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 8. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

####### 9. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

########## 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

######### ENUMERATION 类型参数

########## 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

####### 10. EthSwtPortIngress

**容器属性**:

- **UUID**: `ECUC:6201a610-faee-41a6-b33f-1055b2dc404e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortIngress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port ingress behavior.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortIngressVlanModification

- **UUID**: `ECUC:fb3ff4fc-7e38-4211-a5ef-e4de2de24e19`
- **参数名**: `EthSwtPortIngressVlanModification`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all messages which arrive at this ingress port will be tagged with this VLAN Id. This tagging happen also if the arriving message already has a VLAN Id, it will be overwritten by the defined one.

########## 2. EthSwtPortTrafficClassAssignment

- **UUID**: `ECUC:dfae6cad-011a-422c-b718-6c61c19a5607`
- **参数名**: `EthSwtPortTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all arriving messages at this ingress port shall be assigned this traffic class.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

############ 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

######### 2. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

############ 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

####### 11. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

########## 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

####### 12. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

########## 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

####### 13. EthSwtSpi

**容器属性**:

- **UUID**: `ECUC:c613caa3-1ff6-49c8-99cc-5883e9aeaef5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpi`
- **多重性**: [0..1]

**容器描述**:

Configuration of one Ethernet Switch SPI access (if SPI is used).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthSwtSpiSequence

**容器属性**:

- **UUID**: `ECUC:b08a8fff-5509-479d-b072-f6441b4c9aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpiSequence`
- **多重性**: [1..infinite]

**容器描述**:

Container gives EthSwt driver information about one SPI sequence.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. EthSwtSpiAccessSynchronous

- **UUID**: `ECUC:d73351bc-6c36-4ba9-8fc7-b907d1ee6787`
- **参数名**: `EthSwtSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthSwtSpiSequenceName

- **UUID**: `ECUC:203cb639-e275-46ff-ac61-574e4e9d48cc`
- **引用名**: `EthSwtSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Spi sequence configuration container.

####### 14. EthSwtSpiSequence

**容器属性**:

- **UUID**: `ECUC:b08a8fff-5509-479d-b072-f6441b4c9aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpiSequence`
- **多重性**: [1..infinite]

**容器描述**:

Container gives EthSwt driver information about one SPI sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. EthSwtSpiAccessSynchronous

- **UUID**: `ECUC:d73351bc-6c36-4ba9-8fc7-b907d1ee6787`
- **参数名**: `EthSwtSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthSwtSpiSequenceName

- **UUID**: `ECUC:203cb639-e275-46ff-ac61-574e4e9d48cc`
- **引用名**: `EthSwtSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Spi sequence configuration container.

##### 2. EthSwtDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:d9439cbe-74df-469f-9869-1e59b2158ca8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHSWT_E_ACCESS

- **UUID**: `ECUC:6d0e97ed-01b9-4f47-b005-2742bb9752b8`
- **引用名**: `ETHSWT_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Ethernet Switch Access Failure" has occurred.

##### 3. EthSwtNvm

**容器属性**:

- **UUID**: `ECUC:d7833215-cb74-44be-9b61-ac433690ccf7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtNvm`
- **多重性**: [0..1]

**容器描述**:

Configuration of one Ethernet Switch Nvm usage in case the module requires non volatile memory in the Ecu to store switch configuration.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthSwtNvmBlockDescriptorRef

- **UUID**: `ECUC:d80a068c-a983-4a55-9329-88e4e7488c1f`
- **引用名**: `EthSwtNvmBlockDescriptorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

##### 4. EthSwtPort

**容器属性**:

- **UUID**: `ECUC:60c612bd-d595-4d5e-80cc-0b360b27db11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPort`
- **多重性**: [1..infinite]

**容器描述**:

Configuration of one Ethernet Switch Port.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortIdx

- **UUID**: `ECUC:01e9df96-9db2-47ba-9086-9aa958cf08c4`
- **参数名**: `EthSwtPortIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Specifies the instance ID of the configured Ethernet Switch Port.

####### BOOLEAN 类型参数

######## 1. EthSwtPortEnableLinkDownCallback

- **UUID**: `ECUC:ef9ae984-adc2-43f9-bb45-398f6a12e6f2`
- **参数名**: `EthSwtPortEnableLinkDownCallback`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables the callback <User>_LinkDown for this EthSwtPort if an IEEE802.1X link loss is detected.

####### STRING 类型参数

######## 1. EthSwtPortPredefinedMacAddresses

- **UUID**: `ECUC:144e0e11-79ac-4473-9457-b4203cc98786`
- **参数名**: `EthSwtPortPredefinedMacAddresses`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[0-9a-fA-F]{2}[[:-][0-9a-fA-F]{2}]{5}`
- **描述**: Specifies a list of 48-bit physical addresses (MAC addresses) which can be reached via this port in network byte order.

####### ENUMERATION 类型参数

######## 1. EthSwtPortPhysicalLayerType

- **UUID**: `ECUC:0ba2ef58-bb99-4b33-a847-bd2c6dfa503b`
- **参数名**: `EthSwtPortPhysicalLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_PORT_BASE_T` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_BROAD_R_REACH` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_RTPGE` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_X_MII` (来源: AUTOSAR_ECUC)
- **描述**: Defines the physical layer type on this EthSwtPort.

######## 2. EthSwtPortSpeed

- **UUID**: `ECUC:d91d6ae3-d025-4366-a127-fe31196c8183`
- **参数名**: `EthSwtPortSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_PORT_SPEED_10` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_SPEED_100` (来源: AUTOSAR_ECUC)
  - `ETHSWT_PORT_SPEED_1000` (来源: AUTOSAR_ECUC)
- **描述**: Defines the communication speed in Mbit per second on this EthSwtPort in case no EthSwtPortTrcvRef is defined.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthSwtPortTrcvRef

- **UUID**: `ECUC:87a2557d-4030-4760-b6ad-713aad1cfcca`
- **引用名**: `EthSwtPortTrcvRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthTrcvConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet/EthTrcvConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the ethernet transceiver driver this EthSwtPort is connected with.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. EthSwtPortEgress

**容器属性**:

- **UUID**: `ECUC:c6580740-35c3-4d5f-89a3-e3e5f39d23ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortEgress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port Egress behavior.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthSwtPortEgressLastSchedulerRef

- **UUID**: `ECUC:cea09fae-5a0f-486e-b7cc-4f3db96b65fa`
- **引用名**: `EthSwtPortEgressLastSchedulerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortScheduler`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the port scheduler which is the last in the egress port structure.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

######### 2. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 3. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

######### 4. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

######### 5. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

############ 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

########### ENUMERATION 类型参数

############ 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

####### 2. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

####### 3. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 4. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 5. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

####### 6. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

########## 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

######### ENUMERATION 类型参数

########## 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

####### 7. EthSwtPortIngress

**容器属性**:

- **UUID**: `ECUC:6201a610-faee-41a6-b33f-1055b2dc404e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortIngress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port ingress behavior.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortIngressVlanModification

- **UUID**: `ECUC:fb3ff4fc-7e38-4211-a5ef-e4de2de24e19`
- **参数名**: `EthSwtPortIngressVlanModification`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all messages which arrive at this ingress port will be tagged with this VLAN Id. This tagging happen also if the arriving message already has a VLAN Id, it will be overwritten by the defined one.

########## 2. EthSwtPortTrafficClassAssignment

- **UUID**: `ECUC:dfae6cad-011a-422c-b718-6c61c19a5607`
- **参数名**: `EthSwtPortTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all arriving messages at this ingress port shall be assigned this traffic class.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

############ 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

######### 2. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

############ 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

####### 8. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

########## 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

####### 9. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

########## 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

##### 5. EthSwtPortEgress

**容器属性**:

- **UUID**: `ECUC:c6580740-35c3-4d5f-89a3-e3e5f39d23ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortEgress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port Egress behavior.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EthSwtPortEgressLastSchedulerRef

- **UUID**: `ECUC:cea09fae-5a0f-486e-b7cc-4f3db96b65fa`
- **引用名**: `EthSwtPortEgressLastSchedulerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortScheduler`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the port scheduler which is the last in the egress port structure.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

####### 2. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 3. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

####### 4. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

####### 5. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

########## 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

######### ENUMERATION 类型参数

########## 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

##### 6. EthSwtPortFifo

**容器属性**:

- **UUID**: `ECUC:79e247c0-ddf3-45c7-b51a-fefa41629204`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortFifo`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Fifo in the egress port.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortFifoTrafficClassAssignment

- **UUID**: `ECUC:68706570-2b3c-4981-b961-8cc4c6d1c36d`
- **参数名**: `EthSwtPortFifoTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..8]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines which traffic classes are assigned to this Fifo.

##### 7. EthSwtPortScheduler

**容器属性**:

- **UUID**: `ECUC:bbb43a98-8b9c-4764-acbc-cc9802fab490`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortScheduler`
- **多重性**: [1..infinite]

**容器描述**:

Represents a Scheduler in the egress port.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EthSwtPortSchedulerAlgorithm

- **UUID**: `ECUC:d39b10ea-dd5f-4ceb-ab57-145f22eec37c`
- **参数名**: `EthSwtPortSchedulerAlgorithm`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_SCHEDULER_DEFICIT_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_STRICT_PRIORITY` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SCHEDULER_WEIGHTED_ROUND_ROBIN` (来源: AUTOSAR_ECUC)
- **描述**: Defines the scheduler algorithm.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

##### 8. EthSwtPortSchedulerPredecessor

**容器属性**:

- **UUID**: `ECUC:6d84c3e2-51aa-4c9d-b19b-7d4244143ba4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortSchedulerPredecessor`
- **多重性**: [1..infinite]

**容器描述**:

Defines an ordered list of predecessors for this scheduler.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortSchedulerPredecessorOrder

- **UUID**: `ECUC:452dd519-f0b5-4a80-a860-f7d0dd679034`
- **参数名**: `EthSwtPortSchedulerPredecessorOrder`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the order of the scheduler predecessors.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. EthSwtPortEgressPredecessorRef

- **UUID**: `ECUC:15fd9ee4-6e23-44a6-9243-51481779d06c`
- **引用名**: `EthSwtPortEgressPredecessorRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortScheduler`
  - `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortShaper`
- **描述**: Choice reference to the scheduler predecessor.

##### 9. EthSwtPortShaper

**容器属性**:

- **UUID**: `ECUC:dde897f6-7f5d-4d5d-aa27-3a650416db47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortShaper`
- **多重性**: [0..infinite]

**容器描述**:

Represents a Shaper in the egress port.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortShaperIdleSlope

- **UUID**: `ECUC:c3e7b5a1-91a9-4e1d-882c-ab494f6fcac6`
- **参数名**: `EthSwtPortShaperIdleSlope`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Defines the increase of credit in bits per second for the AVB shaper.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EthSwtPortEgressPredecessorFifoRef

- **UUID**: `ECUC:cbe06380-bb22-4f68-b4fe-ab4a25574793`
- **引用名**: `EthSwtPortEgressPredecessorFifoRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPortFifo`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort/EthSwtPortEgress/EthSwtPortFifo`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the fifo which is the predecessor for this shaper.

##### 10. EthSwtPortVlanForwarding

**容器属性**:

- **UUID**: `ECUC:e2b2252c-6874-4b5b-a5f7-3fe9b374750f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortVlanForwarding`
- **多重性**: [0..infinite]

**容器描述**:

Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN Id.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortVlanDefaultPriority

- **UUID**: `ECUC:bd79d7ea-4554-4ea8-854f-3be9beea261e`
- **参数名**: `EthSwtPortVlanDefaultPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the standard output-priority outgoing messages will be tagged with.

######## 2. EthSwtPortVlanForwardingId

- **UUID**: `ECUC:da2b6dd7-513d-451c-b6a7-b652af979ace`
- **参数名**: `EthSwtPortVlanForwardingId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Determines the VLAN Id the VlanForwarding shall apply to.

####### ENUMERATION 类型参数

######## 1. EthSwtPortVlanForwardingType

- **UUID**: `ECUC:4e0b90c2-142f-4599-9ac1-b77f78c77b4c`
- **参数名**: `EthSwtPortVlanForwardingType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHSWT_NOT_SENT` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_TAGGED` (来源: AUTOSAR_ECUC)
  - `ETHSWT_SENT_UNTAGGED` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the message with a specific VLAN Id shall be handled.

##### 11. EthSwtPortIngress

**容器属性**:

- **UUID**: `ECUC:6201a610-faee-41a6-b33f-1055b2dc404e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPortIngress`
- **多重性**: [1..1]

**容器描述**:

Configuration of one Ethernet Switch Port ingress behavior.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPortIngressVlanModification

- **UUID**: `ECUC:fb3ff4fc-7e38-4211-a5ef-e4de2de24e19`
- **参数名**: `EthSwtPortIngressVlanModification`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [1..4094]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all messages which arrive at this ingress port will be tagged with this VLAN Id. This tagging happen also if the arriving message already has a VLAN Id, it will be overwritten by the defined one.

######## 2. EthSwtPortTrafficClassAssignment

- **UUID**: `ECUC:dfae6cad-011a-422c-b718-6c61c19a5607`
- **参数名**: `EthSwtPortTrafficClassAssignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this parameter is defined all arriving messages at this ingress port shall be assigned this traffic class.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

########## 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

####### 2. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

########## 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

##### 12. EthSwtPriorityRegeneration

**容器属性**:

- **UUID**: `ECUC:8a1a555a-1e95-45e3-bc8f-e9414c3363d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityRegeneration`
- **多重性**: [0..8]

**容器描述**:

Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by EthSwtPriorityRegenerationRegeneratedPriority.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPriorityRegenerationIngressPriority

- **UUID**: `ECUC:f991d5ac-24d3-43a6-81e1-5368c7df2b7f`
- **参数名**: `EthSwtPriorityRegenerationIngressPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority of the incoming message.

######## 2. EthSwtPriorityRegenerationRegeneratedPriority

- **UUID**: `ECUC:ed4e5a31-7f83-4c6a-9725-e59f7a500303`
- **参数名**: `EthSwtPriorityRegenerationRegeneratedPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority the incoming message will be tagged with.

##### 13. EthSwtPriorityTrafficClassAssignment

**容器属性**:

- **UUID**: `ECUC:ebce6c0b-f226-42e1-82eb-f26ad54d1a75`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtPriorityTrafficClassAssignment`
- **多重性**: [0..8]

**容器描述**:

Defines a priority based traffic class assignment. All messages with a specific priority (EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class (EthSwtPriorityTrafficClassAssignmentTrafficClass).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtPriorityTrafficClassAssignmentPriority

- **UUID**: `ECUC:806b5fe1-238e-4332-aeca-a209cc150a6a`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Message priority.

######## 2. EthSwtPriorityTrafficClassAssignmentTrafficClass

- **UUID**: `ECUC:8e1ada3b-fe7e-4632-b7a5-40284b38abb3`
- **参数名**: `EthSwtPriorityTrafficClassAssignmentTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Traffic Class value.

##### 14. EthSwtSpi

**容器属性**:

- **UUID**: `ECUC:c613caa3-1ff6-49c8-99cc-5883e9aeaef5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpi`
- **多重性**: [0..1]

**容器描述**:

Configuration of one Ethernet Switch SPI access (if SPI is used).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthSwtSpiSequence

**容器属性**:

- **UUID**: `ECUC:b08a8fff-5509-479d-b072-f6441b4c9aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpiSequence`
- **多重性**: [1..infinite]

**容器描述**:

Container gives EthSwt driver information about one SPI sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. EthSwtSpiAccessSynchronous

- **UUID**: `ECUC:d73351bc-6c36-4ba9-8fc7-b907d1ee6787`
- **参数名**: `EthSwtSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthSwtSpiSequenceName

- **UUID**: `ECUC:203cb639-e275-46ff-ac61-574e4e9d48cc`
- **引用名**: `EthSwtSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Spi sequence configuration container.

##### 15. EthSwtSpiSequence

**容器属性**:

- **UUID**: `ECUC:b08a8fff-5509-479d-b072-f6441b4c9aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtSpiSequence`
- **多重性**: [1..infinite]

**容器描述**:

Container gives EthSwt driver information about one SPI sequence.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. EthSwtSpiAccessSynchronous

- **UUID**: `ECUC:d73351bc-6c36-4ba9-8fc7-b907d1ee6787`
- **参数名**: `EthSwtSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthSwtSpiSequenceName

- **UUID**: `ECUC:203cb639-e275-46ff-ac61-574e4e9d48cc`
- **引用名**: `EthSwtSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Spi sequence configuration container.

##### 16. EthSwtGeneral

**容器属性**:

- **UUID**: `ECUC:3d96a192-1204-4873-9177-991e498850f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSwtGeneral`
- **多重性**: [1..1]

**容器描述**:

General configuration of Ethernet Switch Driver module.

###### 参数配置

此容器包含 **22** 个参数：

####### INTEGER 类型参数

######## 1. EthSwtIndex

- **UUID**: `ECUC:1cb88db2-2bb7-4324-bc58-84083b1e22ed`
- **参数名**: `EthSwtIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. EthSwtDevErrorDetect

- **UUID**: `ECUC:df00580a-6987-4b2d-a90f-46da57fbc3a8`
- **参数名**: `EthSwtDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables development error detection.

######## 2. EthSwtEnableVlanApi

- **UUID**: `ECUC:bd96990d-3af9-4d53-b41e-b6d34720b860`
- **参数名**: `EthSwtEnableVlanApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_EnableVLAN API.

######## 3. EthSwtGetArlTableApi

- **UUID**: `ECUC:ddea1320-b490-4d2d-810b-1f04b314d7ff`
- **参数名**: `EthSwtGetArlTableApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetArlTable API.

######## 4. EthSwtGetBufferLevelApi

- **UUID**: `ECUC:90b58238-c1c1-4ce9-8d14-dc4fd778da98`
- **参数名**: `EthSwtGetBufferLevelApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables API to fetch the switch buffer utilization.

######## 5. EthSwtGetDropCountApi

- **UUID**: `ECUC:de712ddb-6adf-4518-9e40-b39f61b00f8d`
- **参数名**: `EthSwtGetDropCountApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetDropCount API.

######## 6. EthSwtGetEtherStatsApi

- **UUID**: `ECUC:b5dd0d07-c466-4867-8913-e86738cbd1c4`
- **参数名**: `EthSwtGetEtherStatsApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetEtherStats API.

######## 7. EthSwtGetMacLearningModeApi

- **UUID**: `ECUC:34b67e5b-3aff-48ba-87dc-4a6977cf12b0`
- **参数名**: `EthSwtGetMacLearningModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetMacLearningMode API.

######## 8. EthSwtGetPortMacAddrApi

- **UUID**: `ECUC:cc4070df-e3d1-48f8-81a8-d51c9a7b84e3`
- **参数名**: `EthSwtGetPortMacAddrApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetPortMacAddr API.

######## 9. EthSwtGetSwitchRegApi

- **UUID**: `ECUC:73bf4d9d-c9bb-42bb-b602-cc4923f629e6`
- **参数名**: `EthSwtGetSwitchRegApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_GetSwitchReg API.

######## 10. EthSwtPersistentConfigurationResult

- **UUID**: `ECUC:f8450fe6-4d29-4e15-bd03-cf5ae09526f8`
- **参数名**: `EthSwtPersistentConfigurationResult`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables the callback API <User>_PersistentConfigurationResult.

######## 11. EthSwtReadTrcvRegisterApi

- **UUID**: `ECUC:e1967e31-054e-4403-a7b9-b8c88de81c56`
- **参数名**: `EthSwtReadTrcvRegisterApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_ReadTrcvRegister API.

######## 12. EthSwtResetConfigurationApi

- **UUID**: `ECUC:16af361b-4414-4cf5-aa22-08737cdb74b4`
- **参数名**: `EthSwtResetConfigurationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_ResetConfiguration API.

######## 13. EthSwtSetMacLearningModeApi

- **UUID**: `ECUC:f419814f-256a-4219-8b31-f12ec7f7372a`
- **参数名**: `EthSwtSetMacLearningModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_SetMacLearningMode API.

######## 14. EthSwtSetSwitchRegApi

- **UUID**: `ECUC:0425871a-a7ea-4b22-93ec-75e00a77a5bf`
- **参数名**: `EthSwtSetSwitchRegApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_SetSwitchReg API.

######## 15. EthSwtStoreConfigurationApi

- **UUID**: `ECUC:9012e251-d823-4ec7-ab36-04c58eef5efc`
- **参数名**: `EthSwtStoreConfigurationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_StoreConfiguration API.

######## 16. EthSwtVersionInfoApi

- **UUID**: `ECUC:e884d0d0-8bb9-472b-ae56-eca768f1a331`
- **参数名**: `EthSwtVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables version info API.

######## 17. EthSwtWriteTrcvRegisterApi

- **UUID**: `ECUC:c1518a91-3da5-4941-a1ce-b7ca69fb86eb`
- **参数名**: `EthSwtWriteTrcvRegisterApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables / Disables EthSwt_WriteTrcvRegister API.

####### STRING 类型参数

######## 1. EthSwtPublicCddHeaderFile

- **UUID**: `ECUC:6e2b80fe-5da2-48cb-a5c6-df33a57a4438`
- **参数名**: `EthSwtPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: Defines header files for callback functions which shall be included in case of CDDs.

####### FUNCTION-NAME 类型参数

######## 1. EthSwtLinkDownUser

- **UUID**: `ECUC:d84f11d1-8ece-4319-b463-9153fb20709c`
- **参数名**: `EthSwtLinkDownUser`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Defines the <User> function name for the <User>_LinkDown callback.

######## 2. EthSwtLinkUpUser

- **UUID**: `ECUC:6231011e-406a-4302-ad0e-635210f97a84`
- **参数名**: `EthSwtLinkUpUser`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Defines the <User> function name for the <User>_LinkUp callback.

######## 3. EthSwtPersistentConfigurationResultUser

- **UUID**: `ECUC:04d72fa0-52c3-4588-84af-e897ba51d7ba`
- **参数名**: `EthSwtPersistentConfigurationResultUser`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Defines the <User> function name for the <User>_PersistentConfigurationResult callback.

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

1. **EthSwt**
