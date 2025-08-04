# SoAd - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:30

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [SoAd](#soad)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. SoAd

#### 基本信息

- **UUID**: `ECUC:685233c2-8734-4c8d-9ca2-b7c467e7505c`
- **模块名称**: `SoAd`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the SoAd (Socket Adaptor) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. SoAdBswModules

**容器属性**:

- **UUID**: `ECUC:38cf01c7-4a15-4541-a1a4-ddbdff0a6d2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdBswModules`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container describes a specific BSW module that the SoAd shall interface to.

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. SoAdIf

- **UUID**: `ECUC:61c7651e-6ad8-41c3-abc3-2dd2cee6a53e`
- **参数名**: `SoAdIf`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the Communication Interface APIs or not. Value true means that the APIs are supported. A module can have both Communication Interface APIs and Transport Protocol APIs (e.g. the PduR module).

######## 2. SoAdIfTriggerTransmit

- **UUID**: `ECUC:69f17a2e-4075-40ca-b055-2cca5f9c23fb`
- **参数名**: `SoAdIfTriggerTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the TriggerTransmit API or not. Value true means that the API is supported.

######## 3. SoAdIfTxConfirmation

- **UUID**: `ECUC:8e120498-e9dc-4049-9ad9-4637c25402cd`
- **参数名**: `SoAdIfTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the TxConfirmation API or not. Value true means that the API is supported.

######## 4. SoAdLocalIpAddrAssigmentChg

- **UUID**: `ECUC:9de9200d-13d9-4459-8f2c-0f928ebfcf1d`
- **参数名**: `SoAdLocalIpAddrAssigmentChg`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the LocalIpAddrAssigmentChg API or not. Value true means that the API is supported.

######## 5. SoAdSoConModeChg

- **UUID**: `ECUC:2851d043-899d-43c6-8c1d-cf6218cc7bd0`
- **参数名**: `SoAdSoConModeChg`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the SoConModeChg API or not. Value true means that the API is supported.

######## 6. SoAdTp

- **UUID**: `ECUC:2825d602-fc8e-4d64-a2c7-30226d4a826e`
- **参数名**: `SoAdTp`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the BSW module supports the TransportProtocol APIs or not. Value true means that the APIs are supported. A module can have both Communication Interface APIs and Transport Protocol APIs (e.g. the PduR module).

######## 7. SoAdUseCallerInfix

- **UUID**: `ECUC:ae620584-c765-4574-90e9-6f9c7690b6e5`
- **参数名**: `SoAdUseCallerInfix`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if SoAd shall use (TRUE) the infix "SoAd" when calling an upper layer module function or not (FALSE). E.g. if SoAdUseCallerInfix is TRUE for the upper layer "ABC" then SoAd will call ABC_SoAdIfRxIndication() otherwise SoAd would call ABC_IfRxIndication().

######## 8. SoAdUseTypeInfix

- **UUID**: `ECUC:103a7f7b-0839-4d90-ac0a-830925ad10ea`
- **参数名**: `SoAdUseTypeInfix`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if SoAd shall use (TRUE) the API type infix "Tp" or "If" when calling an upper layer module function or not (FALSE). E.g. if SoAdUseTypeInfix is TRUE for the upper layer "ABC" then SoAd will call ABC_IfRxIndication(), otherwise SoAd would call ABC_RxIndication().

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. SoAdBswModuleRef

- **UUID**: `ECUC:bc97b938-7b4a-4243-8833-22afec289625`
- **引用名**: `SoAdBswModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is a reference to one BSW module's configuration (i.e. not the ECUC parameter definition template).

##### 2. SoAdConfig

**容器属性**:

- **UUID**: `ECUC:3fef2e18-01c5-4810-ae65-27fba17d97c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR SoAd module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SoAdConfigurationId

- **UUID**: `ECUC:1f3edc22-25e0-42cc-a867-40214bc535e7`
- **参数名**: `SoAdConfigurationId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of the SoAd configuration.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. SoAdPduRoute

**容器属性**:

- **UUID**: `ECUC:db0b3473-ac6c-42ba-8d58-21770ad5d14f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRoute`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes the path of a PDU from an upper layer of the SoAd to the socket in the TCP/IP stack for transmission.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdTxPduId

- **UUID**: `ECUC:0607b193-60b3-4acf-8ca0-f903cc227bd7`
- **参数名**: `SoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Tx PDU ID of the PDU coming from the PDU Router.

######### ENUMERATION 类型参数

########## 1. SoAdTxUpperLayerType

- **UUID**: `ECUC:56642173-affc-4c54-b407-ea215fc4a9d8`
- **参数名**: `SoAdTxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple PduRoutes).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdTxPduRef

- **UUID**: `ECUC:c753c894-c1eb-47ee-88e7-6396ea183e05`
- **引用名**: `SoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SoAdPduRouteDest

**容器属性**:

- **UUID**: `ECUC:608916f0-a352-48d1-9911-cd629867e984`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRouteDest`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the PDU route destination.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SoAdTxPduHeaderId

- **UUID**: `ECUC:f9cd4c91-4e8f-404d-a6b9-1fa911afb222`
- **参数名**: `SoAdTxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID to be sent on the TCP/IP connection if the PDU header option is enabled.

########### ENUMERATION 类型参数

############ 1. SoAdTxUdpTriggerMode

- **UUID**: `ECUC:8a5d9e39-36fb-4b39-8c27-859278c3f153`
- **参数名**: `SoAdTxUdpTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRIGGER_ALWAYS` (来源: AUTOSAR_ECUC)
  - `TRIGGER_NEVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SoAdTxRoutingGroupRef

- **UUID**: `ECUC:1ffd982b-fc0d-4ce9-aab8-4b67e71bd8e7`
- **引用名**: `SoAdTxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

############ 2. SoAdTxSocketConnectionRef

- **UUID**: `ECUC:22ca0917-bfb5-45f5-9765-f859d37d0482`
- **引用名**: `SoAdTxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU is to be sent on, references the appropriate entry in the Socket Connection Table.

####### 2. SoAdPduRouteDest

**容器属性**:

- **UUID**: `ECUC:608916f0-a352-48d1-9911-cd629867e984`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRouteDest`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the PDU route destination.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdTxPduHeaderId

- **UUID**: `ECUC:f9cd4c91-4e8f-404d-a6b9-1fa911afb222`
- **参数名**: `SoAdTxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID to be sent on the TCP/IP connection if the PDU header option is enabled.

######### ENUMERATION 类型参数

########## 1. SoAdTxUdpTriggerMode

- **UUID**: `ECUC:8a5d9e39-36fb-4b39-8c27-859278c3f153`
- **参数名**: `SoAdTxUdpTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRIGGER_ALWAYS` (来源: AUTOSAR_ECUC)
  - `TRIGGER_NEVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdTxRoutingGroupRef

- **UUID**: `ECUC:1ffd982b-fc0d-4ce9-aab8-4b67e71bd8e7`
- **引用名**: `SoAdTxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

########## 2. SoAdTxSocketConnectionRef

- **UUID**: `ECUC:22ca0917-bfb5-45f5-9765-f859d37d0482`
- **引用名**: `SoAdTxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU is to be sent on, references the appropriate entry in the Socket Connection Table.

####### 3. SoAdRoutingGroup

**容器属性**:

- **UUID**: `ECUC:fc04d0a2-e032-46ec-b1f6-1951663947c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdRoutingGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container describes a specific routing group which can be enabled or disabled. A routing group consists of PDUs. Routing of PDUs can either be forwarding of PDUs from the upper layer to a TCP or UDP socket of the TCP/IP stack specified by a SoAdPduRoute or the other way around specified by a SoAdSocketRoute.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. SoAdRoutingGroupId

- **UUID**: `ECUC:c01186c2-1b38-46d0-a36a-cca2e2dc98e3`
- **参数名**: `SoAdRoutingGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique ID of Routing Group

######### BOOLEAN 类型参数

########## 1. SoAdRoutingGroupIsEnabledAtInit

- **UUID**: `ECUC:fb184258-ebc6-43ad-b6df-4bac46074bc2`
- **参数名**: `SoAdRoutingGroupIsEnabledAtInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true this routing group will be enabled after initializing the SoAd module (i.e. enabled in the SoAd_Init function).

########## 2. SoAdRoutingGroupTxTriggerable

- **UUID**: `ECUC:aaa3d81d-9664-4c66-b322-d06217a9a89d`
- **参数名**: `SoAdRoutingGroupTxTriggerable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the If-TxPDUs related to the PduRouteDest containers

####### 4. SoAdSocketConnectionGroup

**容器属性**:

- **UUID**: `ECUC:abae0f3b-aa69-47ae-82df-bac364d52b6c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnectionGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the configuration of a socket connection group, i.e. specifies the socket connections belonging to the group and the parameters which are common for all socket connections of the group. A socket connection specifies how data can be received and transmited via a TCP or UDP socket.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketFramePriority

- **UUID**: `ECUC:785737d3-b1bb-46f7-be70-a3a689d38251`
- **参数名**: `SoAdSocketFramePriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the priority of the Ethernet frame.

########## 2. SoAdSocketLocalPort

- **UUID**: `ECUC:c6e53314-62e5-4f81-8f47-3c5cb6a19260`
- **参数名**: `SoAdSocketLocalPort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local UDP or TCP port used for this connection.If this parameter set to 0 SoAd requests TcpIp to select an ephemeral port.

########## 3. SoAdSocketTpRxBufferMin

- **UUID**: `ECUC:f1daede7-ba0e-4dbc-9ee7-6c3e6299c67b`
- **参数名**: `SoAdSocketTpRxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data for the upper layer and PDU Header if used) the SoAd shall at least be able to buffer for data reception via each socket connection of the socket connection group and using an upper layer with TP.

######### BOOLEAN 类型参数

########## 1. SoAdPduHeaderEnable

- **UUID**: `ECUC:410309ba-cede-4382-895d-35b0025664f5`
- **参数名**: `SoAdPduHeaderEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables the transmission of the PDU header (ID, length) on this socket connection.

########## 2. SoAdResourceManagementEnable

- **UUID**: `ECUC:9d03a035-be38-49bb-9cb5-6c542059bffc`
- **参数名**: `SoAdResourceManagementEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables the resource management option for this socket.

########## 3. SoAdSocketAutomaticSoConSetup

- **UUID**: `ECUC:40c95585-89c4-4ca2-ae2d-5a0c639ea0c4`
- **参数名**: `SoAdSocketAutomaticSoConSetup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the setup of the socket connection shall be done automatically (TRUE) or manually (FALSE) via SoAd_OpenSoCon() and SoAd_CloseSoCon().

########## 4. SoAdSocketIpAddrAssignmentChgNotification

- **UUID**: `ECUC:4ceb0609-a4e0-4022-bb2c-63f13206cd82`
- **参数名**: `SoAdSocketIpAddrAssignmentChgNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the local IP address assignment change notification callback function of the upper layer shall be called if the assignment of the local IP address used by this socket connection changes.

########## 5. SoAdSocketMsgAcceptanceFilterEnabled

- **UUID**: `ECUC:f1edc6f3-aa71-429b-9005-d78fe8ff68d3`
- **参数名**: `SoAdSocketMsgAcceptanceFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the message acceptance filter is enabled (TRUE) or not (FALSE).

########## 6. SoAdSocketSoConModeChgNotification

- **UUID**: `ECUC:2e4db225-90bc-4a6c-9d2e-b1f84b63318b`
- **参数名**: `SoAdSocketSoConModeChgNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the SoCon mode change notification callback function of the upper layer shall be called in case of SoCon mode change.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SoAdSocketLocalAddressRef

- **UUID**: `ECUC:5f8d7d9a-ea26-4a66-b188-8f9a5d39e808`
- **引用名**: `SoAdSocketLocalAddressRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local IP address and interface used for this connection.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. SoAdSocketConnection

**容器属性**:

- **UUID**: `ECUC:e21ff4b2-9c1b-4704-aacb-498a1675c0ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the socket connection (Id and remote address information).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketId

- **UUID**: `ECUC:f4c911ee-b2ee-42a9-9193-e80a9e168aca`
- **参数名**: `SoAdSocketId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Socket connection identifier used as SoConId in the interaction with upper layers.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

############# STRING 类型参数

############## 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

######### 2. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

########### STRING 类型参数

############ 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

######### 3. SoAdSocketTcp

**容器属性**:

- **UUID**: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketTcp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketTcpTxQuota

- **UUID**: `ECUC:a8df0686-4cc6-4284-987d-e8e01d20d77f`
- **参数名**: `SoAdSocketTcpTxQuota`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket connection of this socket connection group.

########### BOOLEAN 类型参数

############ 1. SoAdSocketTcpImmediateTpTxConfirmation

- **UUID**: `ECUC:c6ad7d55-2e5d-49c0-9f7a-e42599a33a50`
- **参数名**: `SoAdSocketTcpImmediateTpTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit confirmation immediately after transmit has been accepted by TcpIp.

############ 2. SoAdSocketTcpInitiate

- **UUID**: `ECUC:544ba1ab-6419-42e8-99dc-635daba8c15f`
- **参数名**: `SoAdSocketTcpInitiate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.

############ 3. SoAdSocketTcpNoDelay

- **UUID**: `ECUC:babda4bd-27c8-4502-ad52-3b21483c2bb6`
- **参数名**: `SoAdSocketTcpNoDelay`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies not to use the congestion control mechanism for this connection. It will not be defined for UDP sockets.

######### 4. SoAdSocketUdp

**容器属性**:

- **UUID**: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketUdp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketnPduUdpTxBufferMin

- **UUID**: `ECUC:35773a86-d1bf-4d8b-82a4-5120276e4d33`
- **参数名**: `SoAdSocketnPduUdpTxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd shall be able to buffer for data transmission via this socket connection in case the UDP message shall be buffered for transmission of multiple PDUs per UDP.

########### BOOLEAN 类型参数

############ 1. SoAdSocketUdpListenOnly

- **UUID**: `ECUC:d290a4ee-dd54-4e7d-b4d2-1df95c069f5b`
- **参数名**: `SoAdSocketUdpListenOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the socket connection group is only used for reception (TRUE) or used for both reception and transmission (FALSE).

############ 2. SoAdSocketUdpRetryEnabled

- **UUID**: `ECUC:6b47fbd2-cfb4-443f-965f-de4558a44429`
- **参数名**: `SoAdSocketUdpRetryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if an UdpTxBuffer shall be used (TRUE) to retry an UDP transmission in case of TCPIP_E_ARP_CACHE_MISS or not (FALSE).

########### FLOAT 类型参数

############ 1. SoAdSocketUdpTriggerTimeout

- **UUID**: `ECUC:ca90e8f9-cc0d-49e9-bebb-c1b79a3c0ef5`
- **参数名**: `SoAdSocketUdpTriggerTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode = TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer is reset after each UDP transmission. This optional parameter is only relevant if a nPduUdpTxBuffer is used.

######### 5. SoAdSocketProtocol

**容器属性**:

- **UUID**: `ECUC:eb8a2965-1cce-423b-be4e-e617127d909f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SoAdSocketProtocol`
- **多重性**: [1..1]

**容器选择**:

- **SoAdSocketTcp**
  - UUID: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
  - 描述: Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.
- **SoAdSocketUdp**
  - UUID: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
  - 描述: Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

**容器描述**:

Specifies the transport protocol and transport protocol specific parameters used for the socket connections of the socket connection group.

####### 5. SoAdSocketConnection

**容器属性**:

- **UUID**: `ECUC:e21ff4b2-9c1b-4704-aacb-498a1675c0ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the socket connection (Id and remote address information).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketId

- **UUID**: `ECUC:f4c911ee-b2ee-42a9-9193-e80a9e168aca`
- **参数名**: `SoAdSocketId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Socket connection identifier used as SoConId in the interaction with upper layers.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

########### STRING 类型参数

############ 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

####### 6. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

######### STRING 类型参数

########## 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

####### 7. SoAdSocketTcp

**容器属性**:

- **UUID**: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketTcp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketTcpTxQuota

- **UUID**: `ECUC:a8df0686-4cc6-4284-987d-e8e01d20d77f`
- **参数名**: `SoAdSocketTcpTxQuota`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket connection of this socket connection group.

######### BOOLEAN 类型参数

########## 1. SoAdSocketTcpImmediateTpTxConfirmation

- **UUID**: `ECUC:c6ad7d55-2e5d-49c0-9f7a-e42599a33a50`
- **参数名**: `SoAdSocketTcpImmediateTpTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit confirmation immediately after transmit has been accepted by TcpIp.

########## 2. SoAdSocketTcpInitiate

- **UUID**: `ECUC:544ba1ab-6419-42e8-99dc-635daba8c15f`
- **参数名**: `SoAdSocketTcpInitiate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.

########## 3. SoAdSocketTcpNoDelay

- **UUID**: `ECUC:babda4bd-27c8-4502-ad52-3b21483c2bb6`
- **参数名**: `SoAdSocketTcpNoDelay`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies not to use the congestion control mechanism for this connection. It will not be defined for UDP sockets.

####### 8. SoAdSocketUdp

**容器属性**:

- **UUID**: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketUdp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketnPduUdpTxBufferMin

- **UUID**: `ECUC:35773a86-d1bf-4d8b-82a4-5120276e4d33`
- **参数名**: `SoAdSocketnPduUdpTxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd shall be able to buffer for data transmission via this socket connection in case the UDP message shall be buffered for transmission of multiple PDUs per UDP.

######### BOOLEAN 类型参数

########## 1. SoAdSocketUdpListenOnly

- **UUID**: `ECUC:d290a4ee-dd54-4e7d-b4d2-1df95c069f5b`
- **参数名**: `SoAdSocketUdpListenOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the socket connection group is only used for reception (TRUE) or used for both reception and transmission (FALSE).

########## 2. SoAdSocketUdpRetryEnabled

- **UUID**: `ECUC:6b47fbd2-cfb4-443f-965f-de4558a44429`
- **参数名**: `SoAdSocketUdpRetryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if an UdpTxBuffer shall be used (TRUE) to retry an UDP transmission in case of TCPIP_E_ARP_CACHE_MISS or not (FALSE).

######### FLOAT 类型参数

########## 1. SoAdSocketUdpTriggerTimeout

- **UUID**: `ECUC:ca90e8f9-cc0d-49e9-bebb-c1b79a3c0ef5`
- **参数名**: `SoAdSocketUdpTriggerTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode = TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer is reset after each UDP transmission. This optional parameter is only relevant if a nPduUdpTxBuffer is used.

####### 9. SoAdSocketRoute

**容器属性**:

- **UUID**: `ECUC:6d408df2-0d97-411f-bede-b1b3f2335c97`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRoute`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes the path of a PDU from a socket in the TCP/IP stack to an upper layer of the SoAd after reception in the TCP/IP Stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SoAdRxPduHeaderId

- **UUID**: `ECUC:e71a64bd-f0cd-471d-96c8-2b92f5751301`
- **参数名**: `SoAdRxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID contained in the packet received on the TCP/IP connection if the PDU header option is enabled.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdRxSocketConnectionRef

- **UUID**: `ECUC:f4f02f3d-d765-4a84-88ec-01a80b047fe0`
- **引用名**: `SoAdRxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU was received. This references an entry in the Socket Connection Table.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SoAdSocketRouteDest

**容器属性**:

- **UUID**: `ECUC:c9313315-2428-474e-bf2b-fa9f9491ab64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRouteDest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Describes the upper layer destination PDU for a message received on a TcpIp socket.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SoAdRxPduId

- **UUID**: `ECUC:a420c5fd-18c3-4bfb-96e8-9f12c650aef8`
- **参数名**: `SoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for a receive cancellation request from an upper layer of the SoAd.

########### ENUMERATION 类型参数

############ 1. SoAdRxUpperLayerType

- **UUID**: `ECUC:1ad3be2c-e898-4c78-a3e5-b9c54698e2ed`
- **参数名**: `SoAdRxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. SoAdRxPduRef

- **UUID**: `ECUC:7f29b096-bb12-495e-9d74-21c032008ada`
- **引用名**: `SoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

############ 2. SoAdRxRoutingGroupRef

- **UUID**: `ECUC:8a4e0666-fa03-4bb5-99fd-10c2bf83e9ed`
- **引用名**: `SoAdRxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

####### 10. SoAdSocketRouteDest

**容器属性**:

- **UUID**: `ECUC:c9313315-2428-474e-bf2b-fa9f9491ab64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRouteDest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Describes the upper layer destination PDU for a message received on a TcpIp socket.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdRxPduId

- **UUID**: `ECUC:a420c5fd-18c3-4bfb-96e8-9f12c650aef8`
- **参数名**: `SoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for a receive cancellation request from an upper layer of the SoAd.

######### ENUMERATION 类型参数

########## 1. SoAdRxUpperLayerType

- **UUID**: `ECUC:1ad3be2c-e898-4c78-a3e5-b9c54698e2ed`
- **参数名**: `SoAdRxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdRxPduRef

- **UUID**: `ECUC:7f29b096-bb12-495e-9d74-21c032008ada`
- **引用名**: `SoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

########## 2. SoAdRxRoutingGroupRef

- **UUID**: `ECUC:8a4e0666-fa03-4bb5-99fd-10c2bf83e9ed`
- **引用名**: `SoAdRxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

####### 11. SoAdSocketProtocol

**容器属性**:

- **UUID**: `ECUC:eb8a2965-1cce-423b-be4e-e617127d909f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SoAdSocketProtocol`
- **多重性**: [1..1]

**容器选择**:

- **SoAdSocketTcp**
  - UUID: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
  - 描述: Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.
- **SoAdSocketUdp**
  - UUID: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
  - 描述: Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

**容器描述**:

Specifies the transport protocol and transport protocol specific parameters used for the socket connections of the socket connection group.

##### 3. SoAdPduRoute

**容器属性**:

- **UUID**: `ECUC:db0b3473-ac6c-42ba-8d58-21770ad5d14f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRoute`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes the path of a PDU from an upper layer of the SoAd to the socket in the TCP/IP stack for transmission.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SoAdTxPduId

- **UUID**: `ECUC:0607b193-60b3-4acf-8ca0-f903cc227bd7`
- **参数名**: `SoAdTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Tx PDU ID of the PDU coming from the PDU Router.

####### ENUMERATION 类型参数

######## 1. SoAdTxUpperLayerType

- **UUID**: `ECUC:56642173-affc-4c54-b407-ea215fc4a9d8`
- **参数名**: `SoAdTxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple PduRoutes).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SoAdTxPduRef

- **UUID**: `ECUC:c753c894-c1eb-47ee-88e7-6396ea183e05`
- **引用名**: `SoAdTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SoAdPduRouteDest

**容器属性**:

- **UUID**: `ECUC:608916f0-a352-48d1-9911-cd629867e984`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRouteDest`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the PDU route destination.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdTxPduHeaderId

- **UUID**: `ECUC:f9cd4c91-4e8f-404d-a6b9-1fa911afb222`
- **参数名**: `SoAdTxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID to be sent on the TCP/IP connection if the PDU header option is enabled.

######### ENUMERATION 类型参数

########## 1. SoAdTxUdpTriggerMode

- **UUID**: `ECUC:8a5d9e39-36fb-4b39-8c27-859278c3f153`
- **参数名**: `SoAdTxUdpTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRIGGER_ALWAYS` (来源: AUTOSAR_ECUC)
  - `TRIGGER_NEVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdTxRoutingGroupRef

- **UUID**: `ECUC:1ffd982b-fc0d-4ce9-aab8-4b67e71bd8e7`
- **引用名**: `SoAdTxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

########## 2. SoAdTxSocketConnectionRef

- **UUID**: `ECUC:22ca0917-bfb5-45f5-9765-f859d37d0482`
- **引用名**: `SoAdTxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU is to be sent on, references the appropriate entry in the Socket Connection Table.

##### 4. SoAdPduRouteDest

**容器属性**:

- **UUID**: `ECUC:608916f0-a352-48d1-9911-cd629867e984`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdPduRouteDest`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the PDU route destination.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SoAdTxPduHeaderId

- **UUID**: `ECUC:f9cd4c91-4e8f-404d-a6b9-1fa911afb222`
- **参数名**: `SoAdTxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID to be sent on the TCP/IP connection if the PDU header option is enabled.

####### ENUMERATION 类型参数

######## 1. SoAdTxUdpTriggerMode

- **UUID**: `ECUC:8a5d9e39-36fb-4b39-8c27-859278c3f153`
- **参数名**: `SoAdTxUdpTriggerMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRIGGER_ALWAYS` (来源: AUTOSAR_ECUC)
  - `TRIGGER_NEVER` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a PDU triggers the transmission of the nPduUdpTxBuffer.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SoAdTxRoutingGroupRef

- **UUID**: `ECUC:1ffd982b-fc0d-4ce9-aab8-4b67e71bd8e7`
- **引用名**: `SoAdTxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

######## 2. SoAdTxSocketConnectionRef

- **UUID**: `ECUC:22ca0917-bfb5-45f5-9765-f859d37d0482`
- **引用名**: `SoAdTxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU is to be sent on, references the appropriate entry in the Socket Connection Table.

##### 5. SoAdRoutingGroup

**容器属性**:

- **UUID**: `ECUC:fc04d0a2-e032-46ec-b1f6-1951663947c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdRoutingGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Each container describes a specific routing group which can be enabled or disabled. A routing group consists of PDUs. Routing of PDUs can either be forwarding of PDUs from the upper layer to a TCP or UDP socket of the TCP/IP stack specified by a SoAdPduRoute or the other way around specified by a SoAdSocketRoute.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SoAdRoutingGroupId

- **UUID**: `ECUC:c01186c2-1b38-46d0-a36a-cca2e2dc98e3`
- **参数名**: `SoAdRoutingGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique ID of Routing Group

####### BOOLEAN 类型参数

######## 1. SoAdRoutingGroupIsEnabledAtInit

- **UUID**: `ECUC:fb184258-ebc6-43ad-b6df-4bac46074bc2`
- **参数名**: `SoAdRoutingGroupIsEnabledAtInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to true this routing group will be enabled after initializing the SoAd module (i.e. enabled in the SoAd_Init function).

######## 2. SoAdRoutingGroupTxTriggerable

- **UUID**: `ECUC:aaa3d81d-9664-4c66-b322-d06217a9a89d`
- **参数名**: `SoAdRoutingGroupTxTriggerable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the If-TxPDUs related to the PduRouteDest containers

##### 6. SoAdSocketConnectionGroup

**容器属性**:

- **UUID**: `ECUC:abae0f3b-aa69-47ae-82df-bac364d52b6c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnectionGroup`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the configuration of a socket connection group, i.e. specifies the socket connections belonging to the group and the parameters which are common for all socket connections of the group. A socket connection specifies how data can be received and transmited via a TCP or UDP socket.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. SoAdSocketFramePriority

- **UUID**: `ECUC:785737d3-b1bb-46f7-be70-a3a689d38251`
- **参数名**: `SoAdSocketFramePriority`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the priority of the Ethernet frame.

######## 2. SoAdSocketLocalPort

- **UUID**: `ECUC:c6e53314-62e5-4f81-8f47-3c5cb6a19260`
- **参数名**: `SoAdSocketLocalPort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local UDP or TCP port used for this connection.If this parameter set to 0 SoAd requests TcpIp to select an ephemeral port.

######## 3. SoAdSocketTpRxBufferMin

- **UUID**: `ECUC:f1daede7-ba0e-4dbc-9ee7-6c3e6299c67b`
- **参数名**: `SoAdSocketTpRxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data for the upper layer and PDU Header if used) the SoAd shall at least be able to buffer for data reception via each socket connection of the socket connection group and using an upper layer with TP.

####### BOOLEAN 类型参数

######## 1. SoAdPduHeaderEnable

- **UUID**: `ECUC:410309ba-cede-4382-895d-35b0025664f5`
- **参数名**: `SoAdPduHeaderEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables the transmission of the PDU header (ID, length) on this socket connection.

######## 2. SoAdResourceManagementEnable

- **UUID**: `ECUC:9d03a035-be38-49bb-9cb5-6c542059bffc`
- **参数名**: `SoAdResourceManagementEnable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables the resource management option for this socket.

######## 3. SoAdSocketAutomaticSoConSetup

- **UUID**: `ECUC:40c95585-89c4-4ca2-ae2d-5a0c639ea0c4`
- **参数名**: `SoAdSocketAutomaticSoConSetup`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the setup of the socket connection shall be done automatically (TRUE) or manually (FALSE) via SoAd_OpenSoCon() and SoAd_CloseSoCon().

######## 4. SoAdSocketIpAddrAssignmentChgNotification

- **UUID**: `ECUC:4ceb0609-a4e0-4022-bb2c-63f13206cd82`
- **参数名**: `SoAdSocketIpAddrAssignmentChgNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the local IP address assignment change notification callback function of the upper layer shall be called if the assignment of the local IP address used by this socket connection changes.

######## 5. SoAdSocketMsgAcceptanceFilterEnabled

- **UUID**: `ECUC:f1edc6f3-aa71-429b-9005-d78fe8ff68d3`
- **参数名**: `SoAdSocketMsgAcceptanceFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the message acceptance filter is enabled (TRUE) or not (FALSE).

######## 6. SoAdSocketSoConModeChgNotification

- **UUID**: `ECUC:2e4db225-90bc-4a6c-9d2e-b1f84b63318b`
- **参数名**: `SoAdSocketSoConModeChgNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the SoCon mode change notification callback function of the upper layer shall be called in case of SoCon mode change.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SoAdSocketLocalAddressRef

- **UUID**: `ECUC:5f8d7d9a-ea26-4a66-b188-8f9a5d39e808`
- **引用名**: `SoAdSocketLocalAddressRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Local IP address and interface used for this connection.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. SoAdSocketConnection

**容器属性**:

- **UUID**: `ECUC:e21ff4b2-9c1b-4704-aacb-498a1675c0ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the socket connection (Id and remote address information).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketId

- **UUID**: `ECUC:f4c911ee-b2ee-42a9-9193-e80a9e168aca`
- **参数名**: `SoAdSocketId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Socket connection identifier used as SoConId in the interaction with upper layers.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

########### STRING 类型参数

############ 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

####### 2. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

######### STRING 类型参数

########## 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

####### 3. SoAdSocketTcp

**容器属性**:

- **UUID**: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketTcp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketTcpTxQuota

- **UUID**: `ECUC:a8df0686-4cc6-4284-987d-e8e01d20d77f`
- **参数名**: `SoAdSocketTcpTxQuota`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket connection of this socket connection group.

######### BOOLEAN 类型参数

########## 1. SoAdSocketTcpImmediateTpTxConfirmation

- **UUID**: `ECUC:c6ad7d55-2e5d-49c0-9f7a-e42599a33a50`
- **参数名**: `SoAdSocketTcpImmediateTpTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit confirmation immediately after transmit has been accepted by TcpIp.

########## 2. SoAdSocketTcpInitiate

- **UUID**: `ECUC:544ba1ab-6419-42e8-99dc-635daba8c15f`
- **参数名**: `SoAdSocketTcpInitiate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.

########## 3. SoAdSocketTcpNoDelay

- **UUID**: `ECUC:babda4bd-27c8-4502-ad52-3b21483c2bb6`
- **参数名**: `SoAdSocketTcpNoDelay`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies not to use the congestion control mechanism for this connection. It will not be defined for UDP sockets.

####### 4. SoAdSocketUdp

**容器属性**:

- **UUID**: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketUdp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketnPduUdpTxBufferMin

- **UUID**: `ECUC:35773a86-d1bf-4d8b-82a4-5120276e4d33`
- **参数名**: `SoAdSocketnPduUdpTxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd shall be able to buffer for data transmission via this socket connection in case the UDP message shall be buffered for transmission of multiple PDUs per UDP.

######### BOOLEAN 类型参数

########## 1. SoAdSocketUdpListenOnly

- **UUID**: `ECUC:d290a4ee-dd54-4e7d-b4d2-1df95c069f5b`
- **参数名**: `SoAdSocketUdpListenOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the socket connection group is only used for reception (TRUE) or used for both reception and transmission (FALSE).

########## 2. SoAdSocketUdpRetryEnabled

- **UUID**: `ECUC:6b47fbd2-cfb4-443f-965f-de4558a44429`
- **参数名**: `SoAdSocketUdpRetryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if an UdpTxBuffer shall be used (TRUE) to retry an UDP transmission in case of TCPIP_E_ARP_CACHE_MISS or not (FALSE).

######### FLOAT 类型参数

########## 1. SoAdSocketUdpTriggerTimeout

- **UUID**: `ECUC:ca90e8f9-cc0d-49e9-bebb-c1b79a3c0ef5`
- **参数名**: `SoAdSocketUdpTriggerTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode = TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer is reset after each UDP transmission. This optional parameter is only relevant if a nPduUdpTxBuffer is used.

####### 5. SoAdSocketProtocol

**容器属性**:

- **UUID**: `ECUC:eb8a2965-1cce-423b-be4e-e617127d909f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SoAdSocketProtocol`
- **多重性**: [1..1]

**容器选择**:

- **SoAdSocketTcp**
  - UUID: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
  - 描述: Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.
- **SoAdSocketUdp**
  - UUID: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
  - 描述: Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

**容器描述**:

Specifies the transport protocol and transport protocol specific parameters used for the socket connections of the socket connection group.

##### 7. SoAdSocketConnection

**容器属性**:

- **UUID**: `ECUC:e21ff4b2-9c1b-4704-aacb-498a1675c0ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketConnection`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Specifies the socket connection (Id and remote address information).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SoAdSocketId

- **UUID**: `ECUC:f4c911ee-b2ee-42a9-9193-e80a9e168aca`
- **参数名**: `SoAdSocketId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Socket connection identifier used as SoConId in the interaction with upper layers.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

######### STRING 类型参数

########## 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

##### 8. SoAdSocketRemoteAddress

**容器属性**:

- **UUID**: `ECUC:61d6f4d9-7fe5-44a5-9c03-17ad0895a2f9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRemoteAddress`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Subcontainer of SoAdSocketConnection to specify the remote address (IP address and port) for a socket connection.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SoAdSocketRemotePort

- **UUID**: `ECUC:d92ba3b3-f3db-4249-877f-97905d97d603`
- **参数名**: `SoAdSocketRemotePort`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Remote UDP or TCP port used for this connection.

####### STRING 类型参数

######## 1. SoAdSocketRemoteIpAddress

- **UUID**: `ECUC:bb1fc885-6e6e-4cf5-9df0-d8ccbdbe059f`
- **参数名**: `SoAdSocketRemoteIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: IP address of remote node.

##### 9. SoAdSocketTcp

**容器属性**:

- **UUID**: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketTcp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SoAdSocketTcpTxQuota

- **UUID**: `ECUC:a8df0686-4cc6-4284-987d-e8e01d20d77f`
- **参数名**: `SoAdSocketTcpTxQuota`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum amout of bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd may queue for transmission via TCP at the TcpIp module for each socket connection of this socket connection group.

####### BOOLEAN 类型参数

######## 1. SoAdSocketTcpImmediateTpTxConfirmation

- **UUID**: `ECUC:c6ad7d55-2e5d-49c0-9f7a-e42599a33a50`
- **参数名**: `SoAdSocketTcpImmediateTpTxConfirmation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to FALSE, SoAd notifies the TP upper layer via transmit confirmation after a Tcp Ack has been received. If set to TRUE, SoAd notifies the TP upper layer via transmit confirmation immediately after transmit has been accepted by TcpIp.

######## 2. SoAdSocketTcpInitiate

- **UUID**: `ECUC:544ba1ab-6419-42e8-99dc-635daba8c15f`
- **参数名**: `SoAdSocketTcpInitiate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the initiator for this TCP connection. It will not be defined for UDP sockets.

######## 3. SoAdSocketTcpNoDelay

- **UUID**: `ECUC:babda4bd-27c8-4502-ad52-3b21483c2bb6`
- **参数名**: `SoAdSocketTcpNoDelay`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies not to use the congestion control mechanism for this connection. It will not be defined for UDP sockets.

##### 10. SoAdSocketUdp

**容器属性**:

- **UUID**: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketUdp`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SoAdSocketnPduUdpTxBufferMin

- **UUID**: `ECUC:35773a86-d1bf-4d8b-82a4-5120276e4d33`
- **参数名**: `SoAdSocketnPduUdpTxBufferMin`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the amout of data in bytes (PDU data provided by the upper layer and PDU Header if used) the SoAd shall be able to buffer for data transmission via this socket connection in case the UDP message shall be buffered for transmission of multiple PDUs per UDP.

####### BOOLEAN 类型参数

######## 1. SoAdSocketUdpListenOnly

- **UUID**: `ECUC:d290a4ee-dd54-4e7d-b4d2-1df95c069f5b`
- **参数名**: `SoAdSocketUdpListenOnly`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the socket connection group is only used for reception (TRUE) or used for both reception and transmission (FALSE).

######## 2. SoAdSocketUdpRetryEnabled

- **UUID**: `ECUC:6b47fbd2-cfb4-443f-965f-de4558a44429`
- **参数名**: `SoAdSocketUdpRetryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if an UdpTxBuffer shall be used (TRUE) to retry an UDP transmission in case of TCPIP_E_ARP_CACHE_MISS or not (FALSE).

####### FLOAT 类型参数

######## 1. SoAdSocketUdpTriggerTimeout

- **UUID**: `ECUC:ca90e8f9-cc0d-49e9-bebb-c1b79a3c0ef5`
- **参数名**: `SoAdSocketUdpTriggerTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the timeout in [s] a nPduUdpTxBuffer is waiting for a PDU with TriggerMode = TRIGGER_ALWAYS, i.e. when the timeout expires the nPduUdpTxBuffer is transmitted. Timer is reset after each UDP transmission. This optional parameter is only relevant if a nPduUdpTxBuffer is used.

##### 11. SoAdSocketRoute

**容器属性**:

- **UUID**: `ECUC:6d408df2-0d97-411f-bede-b1b3f2335c97`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRoute`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes the path of a PDU from a socket in the TCP/IP stack to an upper layer of the SoAd after reception in the TCP/IP Stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SoAdRxPduHeaderId

- **UUID**: `ECUC:e71a64bd-f0cd-471d-96c8-2b92f5751301`
- **参数名**: `SoAdRxPduHeaderId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967296]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID contained in the packet received on the TCP/IP connection if the PDU header option is enabled.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SoAdRxSocketConnectionRef

- **UUID**: `ECUC:f4f02f3d-d765-4a84-88ec-01a80b047fe0`
- **引用名**: `SoAdRxSocketConnectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SoAdSocketConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdSocketConnectionGroup/SoAdSocketConnection`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Connection on which the PDU was received. This references an entry in the Socket Connection Table.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SoAdSocketRouteDest

**容器属性**:

- **UUID**: `ECUC:c9313315-2428-474e-bf2b-fa9f9491ab64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRouteDest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Describes the upper layer destination PDU for a message received on a TcpIp socket.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SoAdRxPduId

- **UUID**: `ECUC:a420c5fd-18c3-4bfb-96e8-9f12c650aef8`
- **参数名**: `SoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for a receive cancellation request from an upper layer of the SoAd.

######### ENUMERATION 类型参数

########## 1. SoAdRxUpperLayerType

- **UUID**: `ECUC:1ad3be2c-e898-4c78-a3e5-b9c54698e2ed`
- **参数名**: `SoAdRxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. SoAdRxPduRef

- **UUID**: `ECUC:7f29b096-bb12-495e-9d74-21c032008ada`
- **引用名**: `SoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

########## 2. SoAdRxRoutingGroupRef

- **UUID**: `ECUC:8a4e0666-fa03-4bb5-99fd-10c2bf83e9ed`
- **引用名**: `SoAdRxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

##### 12. SoAdSocketRouteDest

**容器属性**:

- **UUID**: `ECUC:c9313315-2428-474e-bf2b-fa9f9491ab64`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdSocketRouteDest`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Describes the upper layer destination PDU for a message received on a TcpIp socket.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SoAdRxPduId

- **UUID**: `ECUC:a420c5fd-18c3-4bfb-96e8-9f12c650aef8`
- **参数名**: `SoAdRxPduId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This unique identifier is used for a receive cancellation request from an upper layer of the SoAd.

####### ENUMERATION 类型参数

######## 1. SoAdRxUpperLayerType

- **UUID**: `ECUC:1ad3be2c-e898-4c78-a3e5-b9c54698e2ed`
- **参数名**: `SoAdRxUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `IF` (来源: AUTOSAR_ECUC)
  - `TP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the upper layer interface type (must be "IF" in case of multiple RxPdus).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. SoAdRxPduRef

- **UUID**: `ECUC:7f29b096-bb12-495e-9d74-21c032008ada`
- **引用名**: `SoAdRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU structure

######## 2. SoAdRxRoutingGroupRef

- **UUID**: `ECUC:8a4e0666-fa03-4bb5-99fd-10c2bf83e9ed`
- **引用名**: `SoAdRxRoutingGroupRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SoAdRoutingGroup`
- **完整路径**: `/AUTOSAR/EcucDefs/SoAd/SoAdConfig/SoAdRoutingGroup`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the routing group.

##### 13. SoAdGeneral

**容器属性**:

- **UUID**: `ECUC:4202ade9-3a6c-48f5-a9dc-23b17eff1b56`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SoAdGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains all global configuration parameters of SoAd.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SoAdRoutingGroupMax

- **UUID**: `ECUC:c09a057f-1b6c-4158-be7d-a8be2c930896`
- **参数名**: `SoAdRoutingGroupMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum number of SoAd routing groups. Furthermore it defines the platform type used for RoutingGroupIdType. If SoAdRoutingGroupMax is not greater than 256, an uint8 is used,

######## 2. SoAdSoConMax

- **UUID**: `ECUC:0b9eb24e-bc16-469d-be91-0ac798b57ea6`
- **参数名**: `SoAdSoConMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum number of SoAd socket connections.

####### BOOLEAN 类型参数

######## 1. SoAdDevErrorDetect

- **UUID**: `ECUC:794cba6f-b434-4d3e-bbd0-964f43cbe9c3`
- **参数名**: `SoAdDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. SoAdIPv6AddressEnabled

- **UUID**: `ECUC:1476fc8f-53cd-449b-87fb-290eaf61abc6`
- **参数名**: `SoAdIPv6AddressEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows for increased memory allocation to store IPv6 addresses.

######## 3. SoAdVersionInfoApi

- **UUID**: `ECUC:e37f5bb1-2a02-48b6-8f8b-5bdabdd69153`
- **参数名**: `SoAdVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activates the SoAd_GetVersionInfo() API.

####### FLOAT 类型参数

######## 1. SoAdMainFunctionPeriod

- **UUID**: `ECUC:0d68aaf1-6ac6-4703-9f87-6ed9bc77fcb3`
- **参数名**: `SoAdMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Determines the frequency at which the SoAd_MainFunction() is called in [s].

##### 14. SoAdSocketProtocol

**容器属性**:

- **UUID**: `ECUC:eb8a2965-1cce-423b-be4e-e617127d909f`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SoAdSocketProtocol`
- **多重性**: [1..1]

**容器选择**:

- **SoAdSocketTcp**
  - UUID: `ECUC:2fd748e9-1c58-4419-a869-f1583dab6a51`
  - 描述: Specifies that TCP is used as transport protocol for the socket connection group and parameters only related to TCP socket connections.
- **SoAdSocketUdp**
  - UUID: `ECUC:7365929a-7420-4e93-b00a-6f1576bd11d9`
  - 描述: Specifies that UDP is used as transport protocol for the socket connection group and parameters only related to UDP socket connections.

**容器描述**:

Specifies the transport protocol and transport protocol specific parameters used for the socket connections of the socket connection group.

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

1. **SoAd**
