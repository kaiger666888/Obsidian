# ComM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:10

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [ComM](#comm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. ComM

#### 基本信息

- **UUID**: `ECUC:a2cd582b-3dfc-4ed4-a2e2-2689961a7bd6`
- **模块名称**: `ComM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the ComM (Communications Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. ComMConfigSet

**容器属性**:

- **UUID**: `ECUC:b99721da-102c-4cc0-9c83-c98463c2e955`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container is the base for a multiple configuration set.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. ComMPncEnabled

- **UUID**: `ECUC:f1435a9f-e043-47f2-8b3d-f55d9e9a9609`
- **参数名**: `ComMPncEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether in this configuration set the partial networking is enabled.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. ComMChannel

**容器属性**:

- **UUID**: `ECUC:90795662-87ac-4770-b3db-ea5b1b699d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the bus channel(s). The channel parameters shall be harmonized within the whole communication stack.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. ComMChannelId

- **UUID**: `ECUC:cb043376-bcae-41fa-991d-de06f78c3aaf`
- **参数名**: `ComMChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identification number of the corresponding channel.

######### BOOLEAN 类型参数

########## 1. ComMFullCommRequestNotificationEnabled

- **UUID**: `ECUC:5fc93aa9-f6aa-44c3-89de-82c4f5707088`
- **参数名**: `ComMFullCommRequestNotificationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the optional SenderReceiver Port of Interface ComM_CurrentChannelRequest will be provided for this channel.

########## 2. ComMGlobalNvmBlockDescriptor

- **UUID**: `ECUC:caf4d31a-18b3-4294-a662-c1d088e5ecf5`
- **参数名**: `ComMGlobalNvmBlockDescriptor`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to "true", the NoWakeUp inhibition state of the channel shall be stored (in some implementation specific way) in the block pointed to by ComMGlobalNvmBlockDescriptor.

########## 3. ComMNoCom

- **UUID**: `ECUC:17917b15-1312-4f24-82d0-b7a10bb15f1b`
- **参数名**: `ComMNoCom`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not allowed to change state of ComM channel to COMM_SILENT_COMMUNICATION or COMM_FULL_COMMUNICATION.

########## 4. ComMNoWakeup

- **UUID**: `ECUC:a0280203-5946-4765-a644-7bd991eefc77`
- **参数名**: `ComMNoWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if an ECU is not allowed to wake-up the channel.

######### FLOAT 类型参数

########## 1. ComMMainFunctionPeriod

- **UUID**: `ECUC:2bdc3b86-fad7-4474-a8c8-6b0186779b9f`
- **参数名**: `ComMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..0.1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period in seconds that the MainFunction has to be triggered with.

######### ENUMERATION 类型参数

########## 1. ComMBusType

- **UUID**: `ECUC:65ce688f-3deb-4005-832a-8ee8283a38c8`
- **参数名**: `ComMBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `COMM_BUS_TYPE_CAN` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_ETH` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_FR` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_INTERNAL` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_LIN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type of the channel.

########## 2. ComMPncGatewayType

- **UUID**: `ECUC:b0f7f164-57d2-47c8-8167-1bba23ba1cd8`
- **参数名**: `ComMPncGatewayType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `COMM_GATEWAY_TYPE_ACTIVE` (来源: AUTOSAR_ECUC)
  - `COMM_GATEWAY_TYPE_PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the Partial Network Gateway behaviour of a ComMChannel.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. ComMNetworkManagement

**容器属性**:

- **UUID**: `ECUC:fe18e019-1dc0-4fcb-818a-6e88f759c44f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMNetworkManagement`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the networkmanagement.

########## 参数配置

此容器包含 **3** 个参数：

########### BOOLEAN 类型参数

############ 1. ComMPncNmRequest

- **UUID**: `ECUC:effa8797-5912-4db6-96f1-ebb32ff15a4e`
- **参数名**: `ComMPncNmRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter equals true then every time a FULL Communication is requested due to a change in the PNC state machine to PNC_REQUESTED Nm shall be called using the API Nm_NetworkRequest.

########### FLOAT 类型参数

############ 1. ComMNmLightTimeout

- **UUID**: `ECUC:d4d7b08e-0dbf-4558-bad7-70c29e72889a`
- **参数名**: `ComMNmLightTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the timeout (in seconds) after COMM_FULL_COMMUNICATION sub-state COMM_FULL_COM_READY_SLEEP is left.

########### ENUMERATION 类型参数

############ 1. ComMNmVariant

- **UUID**: `ECUC:26eeb597-a431-438b-bf4b-e3e94b449731`
- **参数名**: `ComMNmVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FULL` (来源: AUTOSAR_ECUC)
  - `LIGHT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the functionality of the networkmanagement.

######### 2. ComMUserPerChannel

**容器属性**:

- **UUID**: `ECUC:58549c51-4697-4a43-b94d-6417b3e4fa46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUserPerChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is linked to a channel.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. ComMUserChannel

- **UUID**: `ECUC:6b08cbd2-a09b-40fb-9872-291825c1f312`
- **引用名**: `ComMUserChannel`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUser that corresponds to this channel user.

####### 2. ComMNetworkManagement

**容器属性**:

- **UUID**: `ECUC:fe18e019-1dc0-4fcb-818a-6e88f759c44f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMNetworkManagement`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the networkmanagement.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. ComMPncNmRequest

- **UUID**: `ECUC:effa8797-5912-4db6-96f1-ebb32ff15a4e`
- **参数名**: `ComMPncNmRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter equals true then every time a FULL Communication is requested due to a change in the PNC state machine to PNC_REQUESTED Nm shall be called using the API Nm_NetworkRequest.

######### FLOAT 类型参数

########## 1. ComMNmLightTimeout

- **UUID**: `ECUC:d4d7b08e-0dbf-4558-bad7-70c29e72889a`
- **参数名**: `ComMNmLightTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the timeout (in seconds) after COMM_FULL_COMMUNICATION sub-state COMM_FULL_COM_READY_SLEEP is left.

######### ENUMERATION 类型参数

########## 1. ComMNmVariant

- **UUID**: `ECUC:26eeb597-a431-438b-bf4b-e3e94b449731`
- **参数名**: `ComMNmVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FULL` (来源: AUTOSAR_ECUC)
  - `LIGHT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the functionality of the networkmanagement.

####### 3. ComMUserPerChannel

**容器属性**:

- **UUID**: `ECUC:58549c51-4697-4a43-b94d-6417b3e4fa46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUserPerChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is linked to a channel.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComMUserChannel

- **UUID**: `ECUC:6b08cbd2-a09b-40fb-9872-291825c1f312`
- **引用名**: `ComMUserChannel`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUser that corresponds to this channel user.

####### 4. ComMPnc

**容器属性**:

- **UUID**: `ECUC:17e918b2-c76d-4759-bcf8-d21a596a0889`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPnc`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the partial network cluster (PNC).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ComMPncId

- **UUID**: `ECUC:1643dcc8-5f57-4824-9f2b-3cb688295e53`
- **参数名**: `ComMPncId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..47]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Partial network cluster identification number.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ComMChannelPerPnc

- **UUID**: `ECUC:6da71784-b6df-457d-b8b1-c366ff0552fa`
- **引用名**: `ComMChannelPerPnc`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel that is required for this PNC.

########## 2. ComMUserPerPnc

- **UUID**: `ECUC:12a13260-51e1-45fd-83ba-c07fdf38d1d7`
- **引用名**: `ComMUserPerPnc`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUsers that correspond to this PNC.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. ComMPncComSignal

**容器属性**:

- **UUID**: `ECUC:4cc8713c-1b73-42c8-99cf-78a4661ae670`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPncComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents the PncComSignals which are used to communicate the EIRA and ERA status of this PNC.

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. ComMPncComSignalDirection

- **UUID**: `ECUC:57a6e338-45b6-4f13-aaee-957a757b025e`
- **参数名**: `ComMPncComSignalDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RX` (来源: AUTOSAR_ECUC)
  - `TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the communication direction of this PncComSignal.

############ 2. ComMPncComSignalKind

- **UUID**: `ECUC:67c219de-2c8a-40f8-9ebe-3d220e8d9e20`
- **参数名**: `ComMPncComSignalKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EIRA` (来源: AUTOSAR_ECUC)
  - `ERA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether this PncComSignal represents EIRA or ERA PNC information.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. ComMPncComSignalChannelRef

- **UUID**: `ECUC:a1ef1f83-6722-4a5b-b52f-a4826cf9fc27`
- **引用名**: `ComMPncComSignalChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel which is used to determine whether this PncComSignal shall participate in the active or passive role (via the parameter ComMPncGatewayType of the ComMChannel).

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ComMPncComSignalRef

- **UUID**: `ECUC:e12a1731-6f7b-498e-824b-4fb8dc4fd033`
- **引用名**: `ComMPncComSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which is used to transport the partial network channel request information.

####### 5. ComMPncComSignal

**容器属性**:

- **UUID**: `ECUC:4cc8713c-1b73-42c8-99cf-78a4661ae670`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPncComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents the PncComSignals which are used to communicate the EIRA and ERA status of this PNC.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. ComMPncComSignalDirection

- **UUID**: `ECUC:57a6e338-45b6-4f13-aaee-957a757b025e`
- **参数名**: `ComMPncComSignalDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RX` (来源: AUTOSAR_ECUC)
  - `TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the communication direction of this PncComSignal.

########## 2. ComMPncComSignalKind

- **UUID**: `ECUC:67c219de-2c8a-40f8-9ebe-3d220e8d9e20`
- **参数名**: `ComMPncComSignalKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EIRA` (来源: AUTOSAR_ECUC)
  - `ERA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether this PncComSignal represents EIRA or ERA PNC information.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ComMPncComSignalChannelRef

- **UUID**: `ECUC:a1ef1f83-6722-4a5b-b52f-a4826cf9fc27`
- **引用名**: `ComMPncComSignalChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel which is used to determine whether this PncComSignal shall participate in the active or passive role (via the parameter ComMPncGatewayType of the ComMChannel).

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ComMPncComSignalRef

- **UUID**: `ECUC:e12a1731-6f7b-498e-824b-4fb8dc4fd033`
- **引用名**: `ComMPncComSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which is used to transport the partial network channel request information.

####### 6. ComMUser

**容器属性**:

- **UUID**: `ECUC:ad498327-129b-4e5e-b929-99d087791ccd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUser`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is designated to request Communication modes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. ComMUserIdentifier

- **UUID**: `ECUC:0793657a-b528-43bb-bd2d-69b50cdd52cf`
- **参数名**: `ComMUserIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: An identifier that is needed to refer to a user in the system which is designated to request Communication Modes.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComMUserEcucPartitionRef

- **UUID**: `ECUC:819cb3d5-38e8-4899-9c4b-ed41a0003895`
- **引用名**: `ComMUserEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes in which "EcucPartition" the requester is executed. When the

##### 2. ComMChannel

**容器属性**:

- **UUID**: `ECUC:90795662-87ac-4770-b3db-ea5b1b699d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the bus channel(s). The channel parameters shall be harmonized within the whole communication stack.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. ComMChannelId

- **UUID**: `ECUC:cb043376-bcae-41fa-991d-de06f78c3aaf`
- **参数名**: `ComMChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel identification number of the corresponding channel.

####### BOOLEAN 类型参数

######## 1. ComMFullCommRequestNotificationEnabled

- **UUID**: `ECUC:5fc93aa9-f6aa-44c3-89de-82c4f5707088`
- **参数名**: `ComMFullCommRequestNotificationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the optional SenderReceiver Port of Interface ComM_CurrentChannelRequest will be provided for this channel.

######## 2. ComMGlobalNvmBlockDescriptor

- **UUID**: `ECUC:caf4d31a-18b3-4294-a662-c1d088e5ecf5`
- **参数名**: `ComMGlobalNvmBlockDescriptor`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to "true", the NoWakeUp inhibition state of the channel shall be stored (in some implementation specific way) in the block pointed to by ComMGlobalNvmBlockDescriptor.

######## 3. ComMNoCom

- **UUID**: `ECUC:17917b15-1312-4f24-82d0-b7a10bb15f1b`
- **参数名**: `ComMNoCom`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Not allowed to change state of ComM channel to COMM_SILENT_COMMUNICATION or COMM_FULL_COMMUNICATION.

######## 4. ComMNoWakeup

- **UUID**: `ECUC:a0280203-5946-4765-a644-7bd991eefc77`
- **参数名**: `ComMNoWakeup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if an ECU is not allowed to wake-up the channel.

####### FLOAT 类型参数

######## 1. ComMMainFunctionPeriod

- **UUID**: `ECUC:2bdc3b86-fad7-4474-a8c8-6b0186779b9f`
- **参数名**: `ComMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..0.1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period in seconds that the MainFunction has to be triggered with.

####### ENUMERATION 类型参数

######## 1. ComMBusType

- **UUID**: `ECUC:65ce688f-3deb-4005-832a-8ee8283a38c8`
- **参数名**: `ComMBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `COMM_BUS_TYPE_CAN` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_ETH` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_FR` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_INTERNAL` (来源: AUTOSAR_ECUC)
  - `COMM_BUS_TYPE_LIN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type of the channel.

######## 2. ComMPncGatewayType

- **UUID**: `ECUC:b0f7f164-57d2-47c8-8167-1bba23ba1cd8`
- **参数名**: `ComMPncGatewayType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `COMM_GATEWAY_TYPE_ACTIVE` (来源: AUTOSAR_ECUC)
  - `COMM_GATEWAY_TYPE_PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the Partial Network Gateway behaviour of a ComMChannel.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. ComMNetworkManagement

**容器属性**:

- **UUID**: `ECUC:fe18e019-1dc0-4fcb-818a-6e88f759c44f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMNetworkManagement`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the networkmanagement.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. ComMPncNmRequest

- **UUID**: `ECUC:effa8797-5912-4db6-96f1-ebb32ff15a4e`
- **参数名**: `ComMPncNmRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter equals true then every time a FULL Communication is requested due to a change in the PNC state machine to PNC_REQUESTED Nm shall be called using the API Nm_NetworkRequest.

######### FLOAT 类型参数

########## 1. ComMNmLightTimeout

- **UUID**: `ECUC:d4d7b08e-0dbf-4558-bad7-70c29e72889a`
- **参数名**: `ComMNmLightTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the timeout (in seconds) after COMM_FULL_COMMUNICATION sub-state COMM_FULL_COM_READY_SLEEP is left.

######### ENUMERATION 类型参数

########## 1. ComMNmVariant

- **UUID**: `ECUC:26eeb597-a431-438b-bf4b-e3e94b449731`
- **参数名**: `ComMNmVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FULL` (来源: AUTOSAR_ECUC)
  - `LIGHT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the functionality of the networkmanagement.

####### 2. ComMUserPerChannel

**容器属性**:

- **UUID**: `ECUC:58549c51-4697-4a43-b94d-6417b3e4fa46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUserPerChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is linked to a channel.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. ComMUserChannel

- **UUID**: `ECUC:6b08cbd2-a09b-40fb-9872-291825c1f312`
- **引用名**: `ComMUserChannel`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUser that corresponds to this channel user.

##### 3. ComMNetworkManagement

**容器属性**:

- **UUID**: `ECUC:fe18e019-1dc0-4fcb-818a-6e88f759c44f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMNetworkManagement`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the networkmanagement.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. ComMPncNmRequest

- **UUID**: `ECUC:effa8797-5912-4db6-96f1-ebb32ff15a4e`
- **参数名**: `ComMPncNmRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter equals true then every time a FULL Communication is requested due to a change in the PNC state machine to PNC_REQUESTED Nm shall be called using the API Nm_NetworkRequest.

####### FLOAT 类型参数

######## 1. ComMNmLightTimeout

- **UUID**: `ECUC:d4d7b08e-0dbf-4558-bad7-70c29e72889a`
- **参数名**: `ComMNmLightTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the timeout (in seconds) after COMM_FULL_COMMUNICATION sub-state COMM_FULL_COM_READY_SLEEP is left.

####### ENUMERATION 类型参数

######## 1. ComMNmVariant

- **UUID**: `ECUC:26eeb597-a431-438b-bf4b-e3e94b449731`
- **参数名**: `ComMNmVariant`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FULL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FULL` (来源: AUTOSAR_ECUC)
  - `LIGHT` (来源: AUTOSAR_ECUC)
  - `NONE` (来源: AUTOSAR_ECUC)
  - `PASSIVE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the functionality of the networkmanagement.

##### 4. ComMUserPerChannel

**容器属性**:

- **UUID**: `ECUC:58549c51-4697-4a43-b94d-6417b3e4fa46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUserPerChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is linked to a channel.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComMUserChannel

- **UUID**: `ECUC:6b08cbd2-a09b-40fb-9872-291825c1f312`
- **引用名**: `ComMUserChannel`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUser that corresponds to this channel user.

##### 5. ComMPnc

**容器属性**:

- **UUID**: `ECUC:17e918b2-c76d-4759-bcf8-d21a596a0889`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPnc`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of the partial network cluster (PNC).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ComMPncId

- **UUID**: `ECUC:1643dcc8-5f57-4824-9f2b-3cb688295e53`
- **参数名**: `ComMPncId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..47]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Partial network cluster identification number.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ComMChannelPerPnc

- **UUID**: `ECUC:6da71784-b6df-457d-b8b1-c366ff0552fa`
- **引用名**: `ComMChannelPerPnc`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel that is required for this PNC.

######## 2. ComMUserPerPnc

- **UUID**: `ECUC:12a13260-51e1-45fd-83ba-c07fdf38d1d7`
- **引用名**: `ComMUserPerPnc`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMUser`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMUser`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMUsers that correspond to this PNC.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. ComMPncComSignal

**容器属性**:

- **UUID**: `ECUC:4cc8713c-1b73-42c8-99cf-78a4661ae670`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPncComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents the PncComSignals which are used to communicate the EIRA and ERA status of this PNC.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. ComMPncComSignalDirection

- **UUID**: `ECUC:57a6e338-45b6-4f13-aaee-957a757b025e`
- **参数名**: `ComMPncComSignalDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RX` (来源: AUTOSAR_ECUC)
  - `TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the communication direction of this PncComSignal.

########## 2. ComMPncComSignalKind

- **UUID**: `ECUC:67c219de-2c8a-40f8-9ebe-3d220e8d9e20`
- **参数名**: `ComMPncComSignalKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EIRA` (来源: AUTOSAR_ECUC)
  - `ERA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether this PncComSignal represents EIRA or ERA PNC information.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. ComMPncComSignalChannelRef

- **UUID**: `ECUC:a1ef1f83-6722-4a5b-b52f-a4826cf9fc27`
- **引用名**: `ComMPncComSignalChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel which is used to determine whether this PncComSignal shall participate in the active or passive role (via the parameter ComMPncGatewayType of the ComMChannel).

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ComMPncComSignalRef

- **UUID**: `ECUC:e12a1731-6f7b-498e-824b-4fb8dc4fd033`
- **引用名**: `ComMPncComSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which is used to transport the partial network channel request information.

##### 6. ComMPncComSignal

**容器属性**:

- **UUID**: `ECUC:4cc8713c-1b73-42c8-99cf-78a4661ae670`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMPncComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Represents the PncComSignals which are used to communicate the EIRA and ERA status of this PNC.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. ComMPncComSignalDirection

- **UUID**: `ECUC:57a6e338-45b6-4f13-aaee-957a757b025e`
- **参数名**: `ComMPncComSignalDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RX` (来源: AUTOSAR_ECUC)
  - `TX` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the communication direction of this PncComSignal.

######## 2. ComMPncComSignalKind

- **UUID**: `ECUC:67c219de-2c8a-40f8-9ebe-3d220e8d9e20`
- **参数名**: `ComMPncComSignalKind`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EIRA` (来源: AUTOSAR_ECUC)
  - `ERA` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether this PncComSignal represents EIRA or ERA PNC information.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. ComMPncComSignalChannelRef

- **UUID**: `ECUC:a1ef1f83-6722-4a5b-b52f-a4826cf9fc27`
- **引用名**: `ComMPncComSignalChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComMChannel which is used to determine whether this PncComSignal shall participate in the active or passive role (via the parameter ComMPncGatewayType of the ComMChannel).

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ComMPncComSignalRef

- **UUID**: `ECUC:e12a1731-6f7b-498e-824b-4fb8dc4fd033`
- **引用名**: `ComMPncComSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which is used to transport the partial network channel request information.

##### 7. ComMUser

**容器属性**:

- **UUID**: `ECUC:ad498327-129b-4e5e-b929-99d087791ccd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMUser`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains a list of identifiers that are needed to refer to a user in the system which is designated to request Communication modes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. ComMUserIdentifier

- **UUID**: `ECUC:0793657a-b528-43bb-bd2d-69b50cdd52cf`
- **参数名**: `ComMUserIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: An identifier that is needed to refer to a user in the system which is designated to request Communication Modes.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. ComMUserEcucPartitionRef

- **UUID**: `ECUC:819cb3d5-38e8-4899-9c4b-ed41a0003895`
- **引用名**: `ComMUserEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Denotes in which "EcucPartition" the requester is executed. When the

##### 8. ComMGeneral

**容器属性**:

- **UUID**: `ECUC:c129122f-1f78-42ac-8b31-1eb279dc2894`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `ComMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration parameters of the Communication Manager.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. ComMEcuGroupClassification

- **UUID**: `ECUC:d34d3082-5711-4aa4-b750-071f85ef3eba`
- **参数名**: `ComMEcuGroupClassification`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether a mode inhibition affects the ECU or not.

####### BOOLEAN 类型参数

######## 1. ComMDevErrorDetect

- **UUID**: `ECUC:0d223c34-88b4-4953-b63d-178406689302`
- **参数名**: `ComMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. ComMDirectUserMapping

- **UUID**: `ECUC:a4afa581-00d4-4e58-bcc3-4b9290cacd24`
- **参数名**: `ComMDirectUserMapping`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is set to true the configuration tool shall automatically create a ComMUser per ComMPnc and a ComMUser per ComMChannel.

######## 3. ComMModeLimitationEnabled

- **UUID**: `ECUC:971d7f76-156e-4c9f-9505-96e129ac1dc0`
- **参数名**: `ComMModeLimitationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: true if mode limitation functionality shall be enabled.

######## 4. ComMPncGatewayEnabled

- **UUID**: `ECUC:e0289a33-1330-4699-98a8-2c8ddb9a5caf`
- **参数名**: `ComMPncGatewayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of Partial Network Gateway.

######## 5. ComMPncSupport

- **UUID**: `ECUC:c49308fd-bcec-4897-b490-792c801843a2`
- **参数名**: `ComMPncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

######## 6. ComMSynchronousWakeUp

- **UUID**: `ECUC:35235a58-2a7e-4268-a93a-37dc5d45746e`
- **参数名**: `ComMSynchronousWakeUp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Wake up of one channel shall lead to a wake up of all channels if true.

######## 7. ComMVersionInfoApi

- **UUID**: `ECUC:2639fcad-20af-4d85-aa2d-ce65ecec04ad`
- **参数名**: `ComMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the possibility to read the published information with the service ComM_GetPublishedInformation().

######## 8. ComMWakeupInhibitionEnabled

- **UUID**: `ECUC:7d54078b-b946-4024-ba5c-43ab7cdb93bd`
- **参数名**: `ComMWakeupInhibitionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: true if wake up inhibition functionality enabled.

####### FLOAT 类型参数

######## 1. ComMPncPrepareSleepTimer

- **UUID**: `ECUC:1cbe2590-ca34-4d84-985b-39a0fab8df28`
- **参数名**: `ComMPncPrepareSleepTimer`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time in seconds the PNC state machine shall wait in PNC_PREPARE_SLEEP.

######## 2. ComMTMinFullComModeDuration

- **UUID**: `ECUC:a03ca45f-4cb6-4775-8311-909b855c5f10`
- **参数名**: `ComMTMinFullComModeDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0.001..65]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum time duration in seconds, spent in the COMM_FULL_COMMUNICATION sub-state COMM_FULL_COM_NETWORK_REQUESTED.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ComMGlobalNvMBlockDescriptor

- **UUID**: `ECUC:31ffd67e-427e-4a21-b549-99d95768dd2d`
- **引用名**: `ComMGlobalNvMBlockDescriptor`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to NVRAM block containing the none volatile data. If this parameter is not configured it means that no NVRam is used at all.

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

1. **ComM**
