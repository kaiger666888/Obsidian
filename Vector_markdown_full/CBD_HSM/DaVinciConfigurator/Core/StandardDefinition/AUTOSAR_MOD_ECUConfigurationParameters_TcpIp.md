# TcpIp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [TcpIp](#tcpip)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. TcpIp

#### 基本信息

- **UUID**: `ECUC:b86af44e-33ca-4ffc-addb-799de20df7b6`
- **模块名称**: `TcpIp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the TcpIp (TCP/IP stack) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.6.0

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **45** 个配置容器：

##### 1. TcpIpConfig

**容器属性**:

- **UUID**: `f39fb728-364a-4aa7-947c-263b3ac95468`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpConfig`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR TcpIp module.

###### 配置容器

本模块包含 **41** 个配置容器：

####### 1. TcpIpCtrl

**容器属性**:

- **UUID**: `fa0185ea-8bbc-4d6b-9fdd-569acd00f722`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrl`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the EthIf controller used for IP communication and TcpIp errors that shall be reported to DEM.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpFramePrioDefault

- **UUID**: `4a48e069-b06d-4378-999f-a6cbf5bdae16`
- **参数名**: `TcpIpIpFramePrioDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the default value for the frame priority used by all sockets.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpDhcpServerConfigRef

- **UUID**: `437632f9-fa1f-4d6a-b547-e284ab6a07ab`
- **引用名**: `TcpIpDhcpServerConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpServerConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpDhcpServerConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a TcpIpDhcpServerConfig which shall be used for this controller setting (VLAN).

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TcpIpEthIfCtrlRef

- **UUID**: `31ec8ab1-1bc4-46d2-b79f-3d2d345aaefc`
- **引用名**: `TcpIpEthIfCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to EthIf controller where the IP address shall be assigned.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. TcpIpCtrlDemEventParameterRefs

**容器属性**:

- **UUID**: `171d8e15-2221-4c34-97ee-fecd3dd4148c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrlDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpCtrl and specifies the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding TcpIp error occurs for communication on the EthIf Controller. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **4** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. TCPIP_E_CONNREFUSED

- **UUID**: `a1d84fdb-d29a-4cfd-ac49-d4a44677a60b`
- **引用名**: `TCPIP_E_CONNREFUSED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Connection refused” has occurred.

############ 2. TCPIP_E_HOSTUNREACH

- **UUID**: `f3780506-6517-4701-8785-46acedc4347f`
- **引用名**: `TCPIP_E_HOSTUNREACH`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "No route to host” has occurred.

############ 3. TCPIP_E_PACKETTOBIG

- **UUID**: `b42e0ca4-3ecf-4695-9272-38671b10ea3e`
- **引用名**: `TCPIP_E_PACKETTOBIG`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Path does not support frame size" has occurred.

############ 4. TCPIP_E_TIMEDOUT

- **UUID**: `42bd5b2a-fecc-46d2-b944-a7f725fe2c0f`
- **引用名**: `TCPIP_E_TIMEDOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Operation timed out” has occurred.

######### 2. TcpIpIpV4Ctrl

**容器属性**:

- **UUID**: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 4 (IPv4) instance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpTypeOfServiceDefault

- **UUID**: `ae037c79-b220-4a64-9345-7b7ee8a5d1fc`
- **参数名**: `TcpIpIpTypeOfServiceDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Type of Service" field of the IPv4 header in outgoing packets on this IP controller.

############ 2. TcpIpIpCtrlIdx

- **UUID**: `2d481e8c-7607-4368-bbd2-60ab601b3643`
- **参数名**: `TcpIpIpCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv4 controller index (calculated automatically)

############ 3. TcpIpIpDefaultTtl

- **UUID**: `9b3a7947-c7a7-46db-982c-440fab0e0884`
- **参数名**: `TcpIpIpDefaultTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Time to Live" field of the IPv4 header in outgoing packets on this IP controller.

########## 引用关系

此容器包含 **5** 个引用：

########### REFERENCE 类型引用

############ 1. TcpIpArpConfigRef

- **UUID**: `7bd8c38e-2a76-40f0-97d5-68397b972d43`
- **引用名**: `TcpIpArpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpArpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpArpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to ARP configuration for this IPv4 instance.

############ 2. TcpIpAutoIpConfigRef

- **UUID**: `464b79fb-c0e5-42fc-9237-68c9ebac4fea`
- **引用名**: `TcpIpAutoIpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpAutoIpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpAutoIpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to AutoIp configuration for this IPv4 instance.

############ 3. TcpIpDhcpConfigRef

- **UUID**: `71225b07-2bf6-4aec-8332-fbe97401610f`
- **引用名**: `TcpIpDhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpDhcpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCP configuration for this IPv4 instance.

############ 4. TcpIpFragmentationConfigRef

- **UUID**: `1082db5e-3319-4ece-961a-2bc452de93ed`
- **引用名**: `TcpIpFragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpFragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpIpFragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Fragmentation configuration for this IPv4 instance.

############ 5. TcpIpStaticArpTableRef

- **UUID**: `7cae9e88-93a6-4ebf-87c1-b84a6b6bc333`
- **引用名**: `TcpIpStaticArpTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpStaticArpTable`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpStaticArpTable`
- **来源**: Vector Informatik
- **描述**: Reference to a static ARP table that shall be used for this controller.

######### 3. TcpIpIpV6Ctrl

**容器属性**:

- **UUID**: `739c0200-ae9c-42da-8178-469e4380cfe7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 6 (IPv6) instance.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6DefaultHopLimit

- **UUID**: `97eff9a8-3b09-4983-bb0c-15ed7584624a`
- **参数名**: `TcpIpIpV6DefaultHopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default Hop Limit for outgoing IPv6 packets. If "Allow Hop Limit Reconfiguration" is checked, the value may be reconfigured based on received Router Advertisements according to [RFC4861 6.3.4. Processing Received Router Advertisements].

############ 2. TcpIpIpV6DefaultTrafficClass

- **UUID**: `8b7ee167-db6d-4482-9ed1-0bc056c6a7df`
- **参数名**: `TcpIpIpV6DefaultTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'Traffic Class' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

############ 3. TcpIpIpV6DefaultFlowLabel

- **UUID**: `00a48c96-3ca4-4fbb-80fd-73a5a9a4cf19`
- **参数名**: `TcpIpIpV6DefaultFlowLabel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'FlowLabel' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

############ 4. TcpIpIpV6CtrlIdx

- **UUID**: `d067c0c6-3daf-4a64-97d4-b7abfe991021`
- **参数名**: `TcpIpIpV6CtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv6 controller index (calculated automatically)

########## 引用关系

此容器包含 **5** 个引用：

########### REFERENCE 类型引用

############ 1. TcpIpIpV6DhcpConfigRef

- **UUID**: `73944cf1-1420-4f8a-8fa7-8bfa1501dd96`
- **引用名**: `TcpIpIpV6DhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpV6Config`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpDhcpV6Config`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCPv6 configuration.

############ 2. TcpIpIpV6FragmentationConfigRef

- **UUID**: `6c6538e3-478e-448a-9603-4405e9e6eb2a`
- **引用名**: `TcpIpIpV6FragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6FragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpIpV6FragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to IPv6 Fragmentation Configuration.

############ 3. TcpIpIpV6NdpConfigRef

- **UUID**: `71a3d2ba-aefa-4d9c-b7e4-55ffc06e4812`
- **引用名**: `TcpIpIpV6NdpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpNdpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Neighbor Discovery Protocol Configuration.

############ 4. TcpIpIpV6MldConfigRef

- **UUID**: `63245d91-769a-4507-86d1-ae901e82ec6b`
- **引用名**: `TcpIpIpV6MldConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6MldConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6MldConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Multicast Listener Discovery version 2 Configuration.
If no reference is set, MLDv2 [RFC3810] is disabled on this IpV6 instance.
(Multiple IpV6 instances may use the same configuration container but will operate independently)

############ 5. TcpIpIpV6PrivExtConfigRef

- **UUID**: `7659b8c3-9f71-4660-8393-f65b47df0891`
- **引用名**: `TcpIpIpV6PrivExtConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6PrivExtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6PrivExtConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Privacy Extensions Configuration.
If no reference is set, Privacy Extensions [RFC4941] are disabled on this IpV6 instance,
(Multiple IpV6 instances may use the same configuration container but will operate independently)

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

############# BOOLEAN 类型参数

############## 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

############# FLOAT 类型参数

############## 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

######### 4. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

########### BOOLEAN 类型参数

############ 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

########### FLOAT 类型参数

############ 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

######### 5. TcpIpIpVXCtrl

**容器属性**:

- **UUID**: `c7454466-eafa-4093-9930-19ededbf3a4e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `TcpIpIpVXCtrl`
- **多重性**: [1..1]

**容器选择**:

- **TcpIpIpV4Ctrl**
  - UUID: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
  - 描述: Specifies an Internet Protocol version 4 (IPv4) instance.
- **TcpIpIpV6Ctrl**
  - UUID: `739c0200-ae9c-42da-8178-469e4380cfe7`
  - 描述: Specifies an Internet Protocol version 6 (IPv6) instance.
- **TcpIpIpV6MtuConfig**
  - UUID: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
  - 描述: This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

**容器描述**:

Specifies whether this controller is an Internet Protocol version 4 (IPv4) or Internet Protocol version 6 (IPv4) instance.

####### 2. TcpIpCtrlDemEventParameterRefs

**容器属性**:

- **UUID**: `171d8e15-2221-4c34-97ee-fecd3dd4148c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrlDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpCtrl and specifies the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding TcpIp error occurs for communication on the EthIf Controller. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TCPIP_E_CONNREFUSED

- **UUID**: `a1d84fdb-d29a-4cfd-ac49-d4a44677a60b`
- **引用名**: `TCPIP_E_CONNREFUSED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Connection refused” has occurred.

########## 2. TCPIP_E_HOSTUNREACH

- **UUID**: `f3780506-6517-4701-8785-46acedc4347f`
- **引用名**: `TCPIP_E_HOSTUNREACH`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "No route to host” has occurred.

########## 3. TCPIP_E_PACKETTOBIG

- **UUID**: `b42e0ca4-3ecf-4695-9272-38671b10ea3e`
- **引用名**: `TCPIP_E_PACKETTOBIG`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Path does not support frame size" has occurred.

########## 4. TCPIP_E_TIMEDOUT

- **UUID**: `42bd5b2a-fecc-46d2-b944-a7f725fe2c0f`
- **引用名**: `TCPIP_E_TIMEDOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Operation timed out” has occurred.

####### 3. TcpIpIpV4Ctrl

**容器属性**:

- **UUID**: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 4 (IPv4) instance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpTypeOfServiceDefault

- **UUID**: `ae037c79-b220-4a64-9345-7b7ee8a5d1fc`
- **参数名**: `TcpIpIpTypeOfServiceDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Type of Service" field of the IPv4 header in outgoing packets on this IP controller.

########## 2. TcpIpIpCtrlIdx

- **UUID**: `2d481e8c-7607-4368-bbd2-60ab601b3643`
- **参数名**: `TcpIpIpCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv4 controller index (calculated automatically)

########## 3. TcpIpIpDefaultTtl

- **UUID**: `9b3a7947-c7a7-46db-982c-440fab0e0884`
- **参数名**: `TcpIpIpDefaultTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Time to Live" field of the IPv4 header in outgoing packets on this IP controller.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpArpConfigRef

- **UUID**: `7bd8c38e-2a76-40f0-97d5-68397b972d43`
- **引用名**: `TcpIpArpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpArpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpArpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to ARP configuration for this IPv4 instance.

########## 2. TcpIpAutoIpConfigRef

- **UUID**: `464b79fb-c0e5-42fc-9237-68c9ebac4fea`
- **引用名**: `TcpIpAutoIpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpAutoIpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpAutoIpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to AutoIp configuration for this IPv4 instance.

########## 3. TcpIpDhcpConfigRef

- **UUID**: `71225b07-2bf6-4aec-8332-fbe97401610f`
- **引用名**: `TcpIpDhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpDhcpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCP configuration for this IPv4 instance.

########## 4. TcpIpFragmentationConfigRef

- **UUID**: `1082db5e-3319-4ece-961a-2bc452de93ed`
- **引用名**: `TcpIpFragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpFragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpIpFragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Fragmentation configuration for this IPv4 instance.

########## 5. TcpIpStaticArpTableRef

- **UUID**: `7cae9e88-93a6-4ebf-87c1-b84a6b6bc333`
- **引用名**: `TcpIpStaticArpTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpStaticArpTable`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpStaticArpTable`
- **来源**: Vector Informatik
- **描述**: Reference to a static ARP table that shall be used for this controller.

####### 4. TcpIpIpV6Ctrl

**容器属性**:

- **UUID**: `739c0200-ae9c-42da-8178-469e4380cfe7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 6 (IPv6) instance.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6DefaultHopLimit

- **UUID**: `97eff9a8-3b09-4983-bb0c-15ed7584624a`
- **参数名**: `TcpIpIpV6DefaultHopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default Hop Limit for outgoing IPv6 packets. If "Allow Hop Limit Reconfiguration" is checked, the value may be reconfigured based on received Router Advertisements according to [RFC4861 6.3.4. Processing Received Router Advertisements].

########## 2. TcpIpIpV6DefaultTrafficClass

- **UUID**: `8b7ee167-db6d-4482-9ed1-0bc056c6a7df`
- **参数名**: `TcpIpIpV6DefaultTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'Traffic Class' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

########## 3. TcpIpIpV6DefaultFlowLabel

- **UUID**: `00a48c96-3ca4-4fbb-80fd-73a5a9a4cf19`
- **参数名**: `TcpIpIpV6DefaultFlowLabel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'FlowLabel' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

########## 4. TcpIpIpV6CtrlIdx

- **UUID**: `d067c0c6-3daf-4a64-97d4-b7abfe991021`
- **参数名**: `TcpIpIpV6CtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv6 controller index (calculated automatically)

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpIpV6DhcpConfigRef

- **UUID**: `73944cf1-1420-4f8a-8fa7-8bfa1501dd96`
- **引用名**: `TcpIpIpV6DhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpV6Config`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpDhcpV6Config`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCPv6 configuration.

########## 2. TcpIpIpV6FragmentationConfigRef

- **UUID**: `6c6538e3-478e-448a-9603-4405e9e6eb2a`
- **引用名**: `TcpIpIpV6FragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6FragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpIpV6FragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to IPv6 Fragmentation Configuration.

########## 3. TcpIpIpV6NdpConfigRef

- **UUID**: `71a3d2ba-aefa-4d9c-b7e4-55ffc06e4812`
- **引用名**: `TcpIpIpV6NdpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpNdpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Neighbor Discovery Protocol Configuration.

########## 4. TcpIpIpV6MldConfigRef

- **UUID**: `63245d91-769a-4507-86d1-ae901e82ec6b`
- **引用名**: `TcpIpIpV6MldConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6MldConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6MldConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Multicast Listener Discovery version 2 Configuration.
If no reference is set, MLDv2 [RFC3810] is disabled on this IpV6 instance.
(Multiple IpV6 instances may use the same configuration container but will operate independently)

########## 5. TcpIpIpV6PrivExtConfigRef

- **UUID**: `7659b8c3-9f71-4660-8393-f65b47df0891`
- **引用名**: `TcpIpIpV6PrivExtConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6PrivExtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6PrivExtConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Privacy Extensions Configuration.
If no reference is set, Privacy Extensions [RFC4941] are disabled on this IpV6 instance,
(Multiple IpV6 instances may use the same configuration container but will operate independently)

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

########### BOOLEAN 类型参数

############ 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

########### FLOAT 类型参数

############ 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

####### 5. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

######### BOOLEAN 类型参数

########## 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

######### FLOAT 类型参数

########## 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

####### 6. TcpIpDhcpServerConfig

**容器属性**:

- **UUID**: `1dd0738d-1fce-4b7e-9a36-0d578df47e44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpServerConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCP Server sub-module.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpNetmask

- **UUID**: `cf95c447-31eb-42c5-8d31-7375534ea05c`
- **参数名**: `TcpIpDhcpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

########## 2. TcpIpDhcpMaxClientIdLen

- **UUID**: `b9118591-7d3b-4f97-b77b-7e565a418b4d`
- **参数名**: `TcpIpDhcpMaxClientIdLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [6..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maxumin length of a DHCP client identifier.
A client identifier may be either the value of the 'chaddr' filed in the DHCP message header or the content of the client identifier option [RFC2132 9.14. Client-identifier]. A client identifer may be up to 255 bytes long but usually the client MAC address is used as client identifer. This value should be at least set to 7 in order to store the type (1 byte) and the address value (6 bytes).

######### FLOAT 类型参数

########## 1. TcpIpDhcpOfferValidTime

- **UUID**: `4422c6da-00d4-435e-9ef7-20d13c131a87`
- **参数名**: `TcpIpDhcpOfferValidTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

########## 2. TcpIpDhcpLeaseTimeMax

- **UUID**: `37fa2a4f-6c70-407e-917b-cc620d105ba3`
- **参数名**: `TcpIpDhcpLeaseTimeMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum lease time. If a client requests a longer lease time the server will use this maximum value instead.
If this parameter does not exists the maximum lease time is infinite.

########## 3. TcpIpDhcpLeaseTimeMin

- **UUID**: `7a6fe8d0-d21d-467b-9df4-68dfcca3b33f`
- **参数名**: `TcpIpDhcpLeaseTimeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum lease time. If a client requests a shorter lease time the server will use this minimum value instead.

########## 4. TcpIpDhcpLeaseTimeDefault

- **UUID**: `b959d8fa-3d4e-4d6a-9a81-3b1f9fa5dc62`
- **参数名**: `TcpIpDhcpLeaseTimeDefault`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default lease time that is used if a client does not has requested a specific lease time.
If this parameter does not exist the maximum lease time will be used as default.

######### STRING 类型参数

########## 1. TcpIpDhcpDefaultRouter

- **UUID**: `5b4fc04d-1532-4f96-8c22-eb13042061d7`
- **参数名**: `TcpIpDhcpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway).

########## 2. TcpIpDhcpGetPortMacAddrFunctionInclude

- **UUID**: `4a125b98-6fa9-4a6a-9f68-616a8bc11896`
- **参数名**: `TcpIpDhcpGetPortMacAddrFunctionInclude`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 默认值: `EthIf.h`
  - 最小长度: 3
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of a header file that contains the declaration of the function defined in TcpIpGetPortMacAddrFunctionName.

########## 3. TcpIpDhcpHostname

- **UUID**: `705720e0-fa08-4af9-8906-ebc82af1fbfd`
- **参数名**: `TcpIpDhcpHostname`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 64
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the value of the DHCP server name that will be sent in the 'sname' field of outgoing DHCPOFFER, DHCPACK and DHCPNAK messages.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpDhcpGetPortMacAddrFunctionName

- **UUID**: `424b3df9-06a9-46be-9180-4fb53fa404fd`
- **参数名**: `TcpIpDhcpGetPortMacAddrFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **函数变体**:
  - 默认值: `EthIf_GetPortMacAddr`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of a function that will be called in order to map a client link-layer (MAC) address to a switch index and port index.
The valid address assignment configurations for a client are selected based on these values.

The function must have the following signature:
Std_ReturnType [TcpIpGetPortMacAddrFunctionName](uint8* MacAddrPtr, uint8* SwitchIdxPtr, uint8* PortIdxPtr)

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TcpIpDhcpEthIfSwitchRef

- **UUID**: `bd17f471-6149-4c36-ab4f-beb071214cee`
- **引用名**: `TcpIpDhcpEthIfSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthIfSwitch`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfSwitch`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to EthIfSwitch representation.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpDhcpAddressAssignment

**容器属性**:

- **UUID**: `5659caac-1d3e-4763-9796-197a6c159b98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpAddressAssignment`
- **多重性**: [0..infinite]

**容器描述**:

Defines a Ethernet Switch port based IP address assignment.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpDhcpAddressLowerBound

- **UUID**: `547e9d46-173e-4371-a642-fc5dc2268763`
- **参数名**: `TcpIpDhcpAddressLowerBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The lower bound IP address which shall be assigned.

############ 2. TcpIpDhcpAddressUpperBound

- **UUID**: `e0134c3a-8251-4782-8a0b-01d2f17258ef`
- **参数名**: `TcpIpDhcpAddressUpperBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The upper bound IP address which shall be assigned.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. TcpIpDhcpSwitchPortRef

- **UUID**: `b4056ffe-3212-451b-a5e6-010d2a06491e`
- **引用名**: `TcpIpDhcpSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Ethernet Switch port.

############ 2. TcpIpDhcpLocalAddrRef

- **UUID**: `65bba8ea-a57a-4066-87ef-3728b0abf66f`
- **引用名**: `TcpIpDhcpLocalAddrRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a TcpIp local address on which this address assignment configuration shall be active. This reference specifies the interface/VLAN this address assignment shall be valid for.

####### 7. TcpIpDhcpAddressAssignment

**容器属性**:

- **UUID**: `5659caac-1d3e-4763-9796-197a6c159b98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpAddressAssignment`
- **多重性**: [0..infinite]

**容器描述**:

Defines a Ethernet Switch port based IP address assignment.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpDhcpAddressLowerBound

- **UUID**: `547e9d46-173e-4371-a642-fc5dc2268763`
- **参数名**: `TcpIpDhcpAddressLowerBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The lower bound IP address which shall be assigned.

########## 2. TcpIpDhcpAddressUpperBound

- **UUID**: `e0134c3a-8251-4782-8a0b-01d2f17258ef`
- **参数名**: `TcpIpDhcpAddressUpperBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The upper bound IP address which shall be assigned.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TcpIpDhcpSwitchPortRef

- **UUID**: `b4056ffe-3212-451b-a5e6-010d2a06491e`
- **引用名**: `TcpIpDhcpSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Ethernet Switch port.

########## 2. TcpIpDhcpLocalAddrRef

- **UUID**: `65bba8ea-a57a-4066-87ef-3728b0abf66f`
- **引用名**: `TcpIpDhcpLocalAddrRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a TcpIp local address on which this address assignment configuration shall be active. This reference specifies the interface/VLAN this address assignment shall be valid for.

####### 8. TcpIpIpConfig

**容器属性**:

- **UUID**: `e6111133-72b5-492f-b012-f8f1370587a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IP (Internet Protocol) sub-module

######## 配置容器

本模块包含 **20** 个配置容器：

######### 1. TcpIpIpV4Config

**容器属性**:

- **UUID**: `61db77db-188c-4120-bd67-39c656db06b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv4 (Internet Protocol version 4) sub-module.

########## 配置容器

本模块包含 **8** 个配置容器：

########### 1. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

############## 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

############# BOOLEAN 类型参数

############## 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

############# FLOAT 类型参数

############## 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

############## 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

############## 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

########### 2. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

############## 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

############## 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

############# FLOAT 类型参数

############## 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

############## 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

############## 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

############## 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

############## 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

############## 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

############## 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

############## 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

########### 3. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############# BOOLEAN 类型参数

############## 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############# FLOAT 类型参数

############## 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############## 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### 4. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

############## 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

############## 参数配置

此容器包含 **2** 个参数：

############### STRING 类型参数

################ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

############### FUNCTION-NAME 类型参数

################ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########### 5. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########### 6. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

############## 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

############# BOOLEAN 类型参数

############## 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

############# FLOAT 类型参数

############## 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

########### 7. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

############## 参数配置

此容器包含 **2** 个参数：

############### STRING 类型参数

################ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

################ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

########### 8. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

######### 2. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

############ 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

########### BOOLEAN 类型参数

############ 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

########### FLOAT 类型参数

############ 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

############ 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

############ 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

######### 3. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

############ 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

############ 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

########### FLOAT 类型参数

############ 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

############ 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

############ 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

############ 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

############ 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

############ 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

############ 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

############ 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

######### 4. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### 5. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

############ 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 6. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 7. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

############ 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

########### BOOLEAN 类型参数

############ 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

########### FLOAT 类型参数

############ 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

######### 8. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

######### 9. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

######### 10. TcpIpIpV6Config

**容器属性**:

- **UUID**: `852b8696-f018-4f10-a8d4-8705bd6fb938`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv6 (Internet Protocol version 6) sub-module.

########## 配置容器

本模块包含 **10** 个配置容器：

########### 1. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

############ 参数配置

此容器包含 **12** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

############# BOOLEAN 类型参数

############## 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

############## 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

############## 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

############## 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

############# FLOAT 类型参数

############## 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############## 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

############## 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############## 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

############## 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############## 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

############## 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

########### 2. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

############ 参数配置

此容器包含 **8** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

############## 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

############## 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

############# BOOLEAN 类型参数

############## 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

############## 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

############## 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

############## 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

############## 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

############## 参数配置

此容器包含 **4** 个参数：

############### STRING 类型参数

################ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

############### FUNCTION-NAME 类型参数

################ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

################ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

################ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

########### 3. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

########### 4. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

############## 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

############## 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

############## 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

############## 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

############# FLOAT 类型参数

############## 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

########### 5. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

############ 参数配置

此容器包含 **2** 个参数：

############# BOOLEAN 类型参数

############## 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

############## 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

############ 配置容器

本模块包含 **5** 个配置容器：

############# 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

############## 参数配置

此容器包含 **14** 个参数：

############### INTEGER 类型参数

################ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

################ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

################ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

################ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

################ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

############### BOOLEAN 类型参数

################ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

################ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

################ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

################ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

################ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

################ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############### FLOAT 类型参数

################ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

################ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

################ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

############# 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

############## 参数配置

此容器包含 **11** 个参数：

############### INTEGER 类型参数

################ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

################ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

################ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

################ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

############### BOOLEAN 类型参数

################ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

################ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

################ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

################ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

################ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

############### FLOAT 类型参数

################ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

################ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

############# 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

############## 参数配置

此容器包含 **6** 个参数：

############### INTEGER 类型参数

################ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

############### BOOLEAN 类型参数

################ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

################ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

############### FLOAT 类型参数

################ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

################ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

################ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

############# 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

############## 参数配置

此容器包含 **9** 个参数：

############### INTEGER 类型参数

################ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

################ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

################ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

################ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

################ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

################ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

############### FLOAT 类型参数

################ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

################ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

################ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

############# 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

############## 参数配置

此容器包含 **7** 个参数：

############### INTEGER 类型参数

################ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

################ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

############### BOOLEAN 类型参数

################ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

############### FLOAT 类型参数

################ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

################ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

################ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

################ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

########### 6. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

############ 参数配置

此容器包含 **14** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############# FLOAT 类型参数

############## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

########### 7. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

############# FLOAT 类型参数

############## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

########### 8. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

############# FLOAT 类型参数

############## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

########### 9. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

############ 参数配置

此容器包含 **9** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

############# FLOAT 类型参数

############## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

########### 10. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

############# BOOLEAN 类型参数

############## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

############# FLOAT 类型参数

############## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

######### 11. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

############ 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

############ 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

############ 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

############ 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

############ 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

############ 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

######### 12. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

############ 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

############ 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

########### BOOLEAN 类型参数

############ 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

############ 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

############ 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

############ 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

############ 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 13. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 14. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

############ 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

############ 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

############ 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

############ 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

########### FLOAT 类型参数

############ 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

######### 15. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

############ 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

############ 参数配置

此容器包含 **14** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############# FLOAT 类型参数

############## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

########### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

############# FLOAT 类型参数

############## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

########### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

############# FLOAT 类型参数

############## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

########### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

############ 参数配置

此容器包含 **9** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

############# FLOAT 类型参数

############## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

########### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

############# BOOLEAN 类型参数

############## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

############# FLOAT 类型参数

############## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

######### 16. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 17. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 18. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 19. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 20. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 9. TcpIpIpV4Config

**容器属性**:

- **UUID**: `61db77db-188c-4120-bd67-39c656db06b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv4 (Internet Protocol version 4) sub-module.

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

############ 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

########### BOOLEAN 类型参数

############ 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

########### FLOAT 类型参数

############ 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

############ 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

############ 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

######### 2. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

############ 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

############ 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

########### FLOAT 类型参数

############ 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

############ 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

############ 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

############ 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

############ 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

############ 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

############ 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

############ 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

######### 3. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### 4. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

############ 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 5. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 6. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

############ 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

########### BOOLEAN 类型参数

############ 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

########### FLOAT 类型参数

############ 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

######### 7. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

######### 8. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 10. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

########## 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

######### BOOLEAN 类型参数

########## 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

######### FLOAT 类型参数

########## 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

########## 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

########## 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

####### 11. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

########## 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

########## 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

######### FLOAT 类型参数

########## 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

########## 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

########## 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

########## 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

########## 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

########## 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

########## 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

########## 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

####### 12. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

####### 13. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

########## 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 14. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 15. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

########## 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

######### BOOLEAN 类型参数

########## 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

######### FLOAT 类型参数

########## 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

####### 16. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 17. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

########## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 18. TcpIpIpV6Config

**容器属性**:

- **UUID**: `852b8696-f018-4f10-a8d4-8705bd6fb938`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv6 (Internet Protocol version 6) sub-module.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

############ 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

############ 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

############ 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

############ 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

############ 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

############ 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

######### 2. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

############ 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

############ 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

########### BOOLEAN 类型参数

############ 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

############ 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

############ 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

############ 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

############ 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 3. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 4. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

############ 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

############ 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

############ 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

############ 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

########### FLOAT 类型参数

############ 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

######### 5. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

############ 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

############ 参数配置

此容器包含 **14** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############# FLOAT 类型参数

############## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

########### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

############# FLOAT 类型参数

############## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

########### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

############# FLOAT 类型参数

############## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

########### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

############ 参数配置

此容器包含 **9** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

############# FLOAT 类型参数

############## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

########### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

############# BOOLEAN 类型参数

############## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

############# FLOAT 类型参数

############## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

######### 6. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 7. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 8. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 9. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 10. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 19. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

########## 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

########## 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

########## 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

########## 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

########## 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

########## 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

####### 20. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

########## 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

########## 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

######### BOOLEAN 类型参数

########## 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

########## 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

########## 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

########## 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

########## 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 21. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

########## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 22. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

########## 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

########## 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

########## 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

########## 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

######### FLOAT 类型参数

########## 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

####### 23. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

########## 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 24. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

######## 参数配置

此容器包含 **14** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

########## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

########## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

########## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

########## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

########## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

########## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

########## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######### FLOAT 类型参数

########## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

########## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

########## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

####### 25. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

########## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

########## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

########## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

########## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

########## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

########## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

########## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

######### FLOAT 类型参数

########## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

########## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

####### 26. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

########## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

######### FLOAT 类型参数

########## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

########## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

########## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

####### 27. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

########## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

########## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

########## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

########## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

########## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

######### FLOAT 类型参数

########## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

########## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

########## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

####### 28. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

########## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

######### BOOLEAN 类型参数

########## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

######### FLOAT 类型参数

########## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

########## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 29. TcpIpLocalAddr

**容器属性**:

- **UUID**: `ef12f5ca-593f-4f49-a4f3-244a2800e58c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpLocalAddr`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the local IP (Internet Protocol) addresses used for IP communication.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAddrId

- **UUID**: `67a403fe-2f00-4519-8e5b-379d56bd44ed`
- **参数名**: `TcpIpAddrId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IP address table identifier assigned by TCP/IP stack.

######### BOOLEAN 类型参数

########## 1. TcpIpIpAddrReceiveAllNotConfiguredMulticasts

- **UUID**: `4fb9b00e-4c71-4f97-8bdc-9949cf83e0bc`
- **参数名**: `TcpIpIpAddrReceiveAllNotConfiguredMulticasts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether an address of type "AutoSelect_Broadcast" shall also be used to receive multicasts that have not been configured individually by addresses of type "Multicast".

Note: If this parameter is set, the IPv4 will configure the EthIf to accept all multicast packets on the corresponsing controller.

This parameter is only valid for an "AutoSelect_Broadcast" address.

######### ENUMERATION 类型参数

########## 1. TcpIpAddressType

- **UUID**: `189afa14-e5b0-422c-a75d-5ca1931f82c5`
- **参数名**: `TcpIpAddressType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_MULTICAST` (来源: AUTOSAR_ECUC)
  - `TCPIP_UNICAST` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV4_BROADCAST` (来源: Vector Informatik)
- **描述**: Address type.

########## 2. TcpIpDomainType

- **UUID**: `a73ae771-25bc-45c2-a02a-e2a2bb7c03d4`
- **参数名**: `TcpIpDomainType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AF_INET` (来源: AUTOSAR_ECUC)
  - `TCPIP_AF_INET6` (来源: AUTOSAR_ECUC)
- **描述**: Address family.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpCtrlRef

- **UUID**: `ed62a943-284f-469c-b777-22bf770e733f`
- **引用名**: `TcpIpCtrlRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpCtrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a TcpIpCtrl specifying the EthIf Controller where the IP address shall be assigned and DEM errors that shall be reported in case of an error on this controller.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. TcpIpAddrAssignment

**容器属性**:

- **UUID**: `8a900823-fc2e-4026-8b31-b66af24a31ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAddrAssignment`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies the assignment policy for the IP address.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpAssignmentPriority

- **UUID**: `66ec827e-8e41-446a-b7d6-b649b6bc0f91`
- **参数名**: `TcpIpAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority of assignment (1 is highest). If a new address from an assignment method with a higher priority is available, it overwrites the IP address previously assigned by an assignment method with a lower priority.

########### ENUMERATION 类型参数

############ 1. TcpIpAssignmentLifetime

- **UUID**: `3cdbb6d1-db4a-4a6b-860c-0073d9c5ae3c`
- **参数名**: `TcpIpAssignmentLifetime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TCPIP_FORGET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_FORGET` (来源: AUTOSAR_ECUC)
  - `TCPIP_STORE` (来源: AUTOSAR_ECUC)
- **描述**: Defines the lifetime of a dynamically fetched IP address.

############ 2. TcpIpAssignmentMethod

- **UUID**: `257a8813-f676-4382-a53d-1172d38d5040`
- **参数名**: `TcpIpAssignmentMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_DHCP` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV6_ROUTER` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL_DOIP` (来源: AUTOSAR_ECUC)
  - `TCPIP_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Method of address assignment

############ 3. TcpIpAssignmentTrigger

- **UUID**: `9286b86a-91cf-4520-b9d2-c73af6504f7f`
- **参数名**: `TcpIpAssignmentTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AUTOMATIC` (来源: AUTOSAR_ECUC)
  - `TCPIP_MANUAL` (来源: AUTOSAR_ECUC)
- **描述**: Trigger of address assignment.

######### 2. TcpIpStaticIpAddressConfig

**容器属性**:

- **UUID**: `8d6861de-7c37-4128-8e83-97af7acb2387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticIpAddressConfig`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies a static IP address including directly related parameters.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNetmask

- **UUID**: `a6bc4b11-58fc-4968-9d60-324b5954ebfa`
- **参数名**: `TcpIpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

########### BOOLEAN 类型参数

############ 1. TcpIpRequestIpAddrAssignmentEnabled

- **UUID**: `4f690c9f-ec8c-4cfb-84fd-80be392391ed`
- **参数名**: `TcpIpRequestIpAddrAssignmentEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this ip address can be changed during runtime via the TcpIp_RequestIpAddrAssignment() API.

########### STRING 类型参数

############ 1. TcpIpDefaultRouter

- **UUID**: `e9069409-5fee-4e28-a2d8-c191e558b754`
- **参数名**: `TcpIpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway)

############ 2. TcpIpStaticIpAddress

- **UUID**: `3b8a3709-2c5c-494d-b0a1-7172a6742b4a`
- **参数名**: `TcpIpStaticIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Static IP Address.

####### 30. TcpIpAddrAssignment

**容器属性**:

- **UUID**: `8a900823-fc2e-4026-8b31-b66af24a31ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAddrAssignment`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies the assignment policy for the IP address.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAssignmentPriority

- **UUID**: `66ec827e-8e41-446a-b7d6-b649b6bc0f91`
- **参数名**: `TcpIpAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority of assignment (1 is highest). If a new address from an assignment method with a higher priority is available, it overwrites the IP address previously assigned by an assignment method with a lower priority.

######### ENUMERATION 类型参数

########## 1. TcpIpAssignmentLifetime

- **UUID**: `3cdbb6d1-db4a-4a6b-860c-0073d9c5ae3c`
- **参数名**: `TcpIpAssignmentLifetime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TCPIP_FORGET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_FORGET` (来源: AUTOSAR_ECUC)
  - `TCPIP_STORE` (来源: AUTOSAR_ECUC)
- **描述**: Defines the lifetime of a dynamically fetched IP address.

########## 2. TcpIpAssignmentMethod

- **UUID**: `257a8813-f676-4382-a53d-1172d38d5040`
- **参数名**: `TcpIpAssignmentMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_DHCP` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV6_ROUTER` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL_DOIP` (来源: AUTOSAR_ECUC)
  - `TCPIP_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Method of address assignment

########## 3. TcpIpAssignmentTrigger

- **UUID**: `9286b86a-91cf-4520-b9d2-c73af6504f7f`
- **参数名**: `TcpIpAssignmentTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AUTOMATIC` (来源: AUTOSAR_ECUC)
  - `TCPIP_MANUAL` (来源: AUTOSAR_ECUC)
- **描述**: Trigger of address assignment.

####### 31. TcpIpStaticIpAddressConfig

**容器属性**:

- **UUID**: `8d6861de-7c37-4128-8e83-97af7acb2387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticIpAddressConfig`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies a static IP address including directly related parameters.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNetmask

- **UUID**: `a6bc4b11-58fc-4968-9d60-324b5954ebfa`
- **参数名**: `TcpIpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

######### BOOLEAN 类型参数

########## 1. TcpIpRequestIpAddrAssignmentEnabled

- **UUID**: `4f690c9f-ec8c-4cfb-84fd-80be392391ed`
- **参数名**: `TcpIpRequestIpAddrAssignmentEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this ip address can be changed during runtime via the TcpIp_RequestIpAddrAssignment() API.

######### STRING 类型参数

########## 1. TcpIpDefaultRouter

- **UUID**: `e9069409-5fee-4e28-a2d8-c191e558b754`
- **参数名**: `TcpIpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway)

########## 2. TcpIpStaticIpAddress

- **UUID**: `3b8a3709-2c5c-494d-b0a1-7172a6742b4a`
- **参数名**: `TcpIpStaticIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Static IP Address.

####### 32. TcpIpNvmBlock

**容器属性**:

- **UUID**: `c2bb41c1-4935-4e1b-acf0-3f595c89ea1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNvmBlock`
- **多重性**: [0..1]

**容器描述**:

Configuration of optional usage of Nvm in case the TcpIp module requires non volatile memory in the Ecu to store information (e.g. IP Address received via DHCP and shall be stored).

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TcpIpNvmBlockDescriptorRef

- **UUID**: `0a0315fb-fe9b-4da2-9061-5621026cea95`
- **引用名**: `TcpIpNvmBlockDescriptorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

####### 33. TcpIpPhysAddrConfig

**容器属性**:

- **UUID**: `8bbfae3c-9972-402f-be2e-de6fa989972d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the physical address configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpPhysAddrChgHandler

**容器属性**:

- **UUID**: `4f251a1a-c10a-44b0-9224-bba3315cb450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrChgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpPhysAddrConfig and

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpPhysAddrChgHandlerHeaderFileName

- **UUID**: `89044b9e-f193-4d7b-9400-c91fa361e7cc`
- **参数名**: `TcpIpPhysAddrChgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the physical address change handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpPhysAddrChgHandlerName

- **UUID**: `db36425a-74a7-4c3e-9689-670d428eec1e`
- **参数名**: `TcpIpPhysAddrChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the physical address change function <Up>_PhysAddrTableChg.

####### 34. TcpIpPhysAddrChgHandler

**容器属性**:

- **UUID**: `4f251a1a-c10a-44b0-9224-bba3315cb450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrChgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpPhysAddrConfig and

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpPhysAddrChgHandlerHeaderFileName

- **UUID**: `89044b9e-f193-4d7b-9400-c91fa361e7cc`
- **参数名**: `TcpIpPhysAddrChgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the physical address change handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpPhysAddrChgHandlerName

- **UUID**: `db36425a-74a7-4c3e-9689-670d428eec1e`
- **参数名**: `TcpIpPhysAddrChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the physical address change function <Up>_PhysAddrTableChg.

####### 35. TcpIpSocketOwnerConfig

**容器属性**:

- **UUID**: `99b3e3b9-ff4a-47ac-9850-604c41875ccd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwnerConfig`
- **多重性**: [1..1]

**容器描述**:

Specifies the upper layer modules of TcpIp using the socket API.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpSocketOwner

**容器属性**:

- **UUID**: `070f0e68-8e85-4d70-b307-3bd24911fb0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwner`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpSocketOwnerConfig and specifies an upper layer of TcpIp that uses the socket API.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpSocketOwnerId

- **UUID**: `db654543-ffed-44ce-808f-292703b2c45a`
- **参数名**: `TcpIpSocketOwnerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ID of the socket user.
(auto calculated)

############ 2. TcpIpSocketOwnerTcpListenSocketMax

- **UUID**: `298c361b-29ce-4c1a-899f-76dc9a25463f`
- **参数名**: `TcpIpSocketOwnerTcpListenSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of TCP listen sockets this socket owner will use simultaneously

########### STRING 类型参数

############ 1. TcpIpSocketOwnerCopyTxDataName

- **UUID**: `31e19519-a2af-4071-8f98-9972932efd76`
- **参数名**: `TcpIpSocketOwnerCopyTxDataName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_CopyTxData> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 2. TcpIpSocketOwnerHeaderFileName

- **UUID**: `fd702bd9-4515-4c7e-9cbf-e8ca95106f95`
- **参数名**: `TcpIpSocketOwnerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the name of the header file containing the definition of the TcpIpSocketOwner module functions. The header file name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 3. TcpIpSocketOwnerLocalIpAddrAssignmentChgName

- **UUID**: `db9ec507-2c81-4399-9f7f-511e0a9801f7`
- **参数名**: `TcpIpSocketOwnerLocalIpAddrAssignmentChgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_LocalIpAddrAssignmentChg> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 4. TcpIpSocketOwnerRxIndicationName

- **UUID**: `18f65b8d-9e74-4011-bf73-e2585e57113f`
- **参数名**: `TcpIpSocketOwnerRxIndicationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_RxIndication> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 5. TcpIpSocketOwnerTcpAcceptedName

- **UUID**: `d3202b67-8321-46cf-832a-12ddcce6eaf6`
- **参数名**: `TcpIpSocketOwnerTcpAcceptedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpAccepted> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 6. TcpIpSocketOwnerTcpConnectedName

- **UUID**: `ea3021c1-8c38-4af8-b85a-f9bcbcabf73c`
- **参数名**: `TcpIpSocketOwnerTcpConnectedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpConnected> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 7. TcpIpSocketOwnerTxConfirmationName

- **UUID**: `c43a4af8-4317-45e1-9350-d618f4a01d9a`
- **参数名**: `TcpIpSocketOwnerTxConfirmationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TxConfirmation> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

############ 8. TcpIpSocketOwnerTcpIpEventName

- **UUID**: `877fae0f-7cf2-4285-b5fb-e784076dc319`
- **参数名**: `TcpIpSocketOwnerTcpIpEventName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the function called for a TCP/IP event on related sockets.The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########### ENUMERATION 类型参数

############ 1. TcpIpSocketOwnerUpperLayerType

- **UUID**: `8227b25a-6ce0-403f-9cc5-8274e6fe05d7`
- **参数名**: `TcpIpSocketOwnerUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `SOAD` (来源: AUTOSAR_ECUC)
  - `DHCPV4_SERVER` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of the upper layer module.

####### 36. TcpIpSocketOwner

**容器属性**:

- **UUID**: `070f0e68-8e85-4d70-b307-3bd24911fb0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwner`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpSocketOwnerConfig and specifies an upper layer of TcpIp that uses the socket API.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpSocketOwnerId

- **UUID**: `db654543-ffed-44ce-808f-292703b2c45a`
- **参数名**: `TcpIpSocketOwnerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ID of the socket user.
(auto calculated)

########## 2. TcpIpSocketOwnerTcpListenSocketMax

- **UUID**: `298c361b-29ce-4c1a-899f-76dc9a25463f`
- **参数名**: `TcpIpSocketOwnerTcpListenSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of TCP listen sockets this socket owner will use simultaneously

######### STRING 类型参数

########## 1. TcpIpSocketOwnerCopyTxDataName

- **UUID**: `31e19519-a2af-4071-8f98-9972932efd76`
- **参数名**: `TcpIpSocketOwnerCopyTxDataName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_CopyTxData> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 2. TcpIpSocketOwnerHeaderFileName

- **UUID**: `fd702bd9-4515-4c7e-9cbf-e8ca95106f95`
- **参数名**: `TcpIpSocketOwnerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the name of the header file containing the definition of the TcpIpSocketOwner module functions. The header file name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 3. TcpIpSocketOwnerLocalIpAddrAssignmentChgName

- **UUID**: `db9ec507-2c81-4399-9f7f-511e0a9801f7`
- **参数名**: `TcpIpSocketOwnerLocalIpAddrAssignmentChgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_LocalIpAddrAssignmentChg> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 4. TcpIpSocketOwnerRxIndicationName

- **UUID**: `18f65b8d-9e74-4011-bf73-e2585e57113f`
- **参数名**: `TcpIpSocketOwnerRxIndicationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_RxIndication> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 5. TcpIpSocketOwnerTcpAcceptedName

- **UUID**: `d3202b67-8321-46cf-832a-12ddcce6eaf6`
- **参数名**: `TcpIpSocketOwnerTcpAcceptedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpAccepted> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 6. TcpIpSocketOwnerTcpConnectedName

- **UUID**: `ea3021c1-8c38-4af8-b85a-f9bcbcabf73c`
- **参数名**: `TcpIpSocketOwnerTcpConnectedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpConnected> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 7. TcpIpSocketOwnerTxConfirmationName

- **UUID**: `c43a4af8-4317-45e1-9350-d618f4a01d9a`
- **参数名**: `TcpIpSocketOwnerTxConfirmationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TxConfirmation> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 8. TcpIpSocketOwnerTcpIpEventName

- **UUID**: `877fae0f-7cf2-4285-b5fb-e784076dc319`
- **参数名**: `TcpIpSocketOwnerTcpIpEventName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the function called for a TCP/IP event on related sockets.The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######### ENUMERATION 类型参数

########## 1. TcpIpSocketOwnerUpperLayerType

- **UUID**: `8227b25a-6ce0-403f-9cc5-8274e6fe05d7`
- **参数名**: `TcpIpSocketOwnerUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `SOAD` (来源: AUTOSAR_ECUC)
  - `DHCPV4_SERVER` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of the upper layer module.

####### 37. TcpIpTcpConfig

**容器属性**:

- **UUID**: `cf13f3bf-480e-4446-882f-7ca705d7e778`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the TCP (Transmission Control Protocol) sub-module.

######## 参数配置

此容器包含 **33** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpTcpKeepAliveProbesMax

- **UUID**: `e46e8e8c-03a0-4351-95b5-6e439d335c97`
- **参数名**: `TcpIpTcpKeepAliveProbesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP Keep Alive is retransmitted before the connection is closed.

########## 2. TcpIpTcpMaxRtx

- **UUID**: `e59720fc-d0bf-4999-bbdd-416170936ec0`
- **参数名**: `TcpIpTcpMaxRtx`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP segment is retransmitted before the TCP connection is closed. This parameter is only valid if TcpIpTcpRetransmissionTimeout is configured.

########## 3. TcpIpTcpReceiveWindowMax

- **UUID**: `cf0da76e-545f-4ce4-b55b-02ac907f9720`
- **参数名**: `TcpIpTcpReceiveWindowMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default value of maximum receive window in bytes.

########## 4. TcpIpTcpSynMaxRtx

- **UUID**: `e67e8d63-0387-42a3-b930-e03c65021b6d`
- **参数名**: `TcpIpTcpSynMaxRtx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP SYN is retransmitted.

########## 5. TcpIpTcpTtl

- **UUID**: `55e70307-5151-4dcf-8e15-b480d1770986`
- **参数名**: `TcpIpTcpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing TCP packets.

########## 6. TcpIpTcpMaxNumOooSegsPerSocket

- **UUID**: `95f52997-c21f-4b88-9388-e72b551789ba`
- **参数名**: `TcpIpTcpMaxNumOooSegsPerSocket`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the maximum number of out of order control elements that can be allocated for one TCP socket during runtime.

RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

########## 7. TcpIpTcpAvgNumOooSegsPerSocket

- **UUID**: `0eb963a8-8b67-4bca-91c0-d1befc3b14dc`
- **参数名**: `TcpIpTcpAvgNumOooSegsPerSocket`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the number of out of order control elements per TCP socket.

The elements are grouped into a pool shared by all TCP sockets.
A TCP socket is allowed to allocate as much elements as specified by 'TcpIpTcpMaxNumOooSegsPerSocket'.

RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

########## 8. TcpIpTcpTxResetQueueSize

- **UUID**: `a4c3705c-875e-41d0-8c45-c4f476d64000`
- **参数名**: `TcpIpTcpTxResetQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [0..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the amount of entries reserved for the Tx Reset Queue.

Note:
The Reset Queue is shared by all TCP Sockets.

########## 9. TcpIpTcpTxRetryQueueSize

- **UUID**: `c048dbcf-ba87-40a6-995e-d379c4f2f9ac`
- **参数名**: `TcpIpTcpTxRetryQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [0..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the average amount of entries allocated for the Tx Retry Queue of one TCP Socket.

Note:
The Retry Queues are grouped in a pool shared by all TCP Sockets. Therefore a Socket may have less entries available as specified.

######### BOOLEAN 类型参数

########## 1. TcpIpTcpCongestionAvoidanceEnabled

- **UUID**: `fbb74212-5c12-4483-abb4-019016ad3d2a`
- **参数名**: `TcpIpTcpCongestionAvoidanceEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP congestion avoidance algorithm according to IETF RFC 5681.

########## 2. TcpIpTcpFastRecoveryEnabled

- **UUID**: `c157243f-6ad5-418e-92f7-37ed6b060c7d`
- **参数名**: `TcpIpTcpFastRecoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP Fast Recovery according to IETF RFC 5681.

########## 3. TcpIpTcpFastRetransmitEnabled

- **UUID**: `313f0b44-0a1c-4541-8217-79e4fc1ac81e`
- **参数名**: `TcpIpTcpFastRetransmitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP Fast Retransmission according to IETF RFC 5681.

########## 4. TcpIpTcpKeepAliveEnabled

- **UUID**: `232c5c88-2a34-4da7-ad35-740cad99d841`
- **参数名**: `TcpIpTcpKeepAliveEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) TCP Keep Alive Probes according to IETF RFC 1122 chapter 4.2.3.6

########## 5. TcpIpTcpNagleEnabled

- **UUID**: `1f7a5768-fe1b-4c4b-81b0-338cf540cbcc`
- **参数名**: `TcpIpTcpNagleEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Nagle’s algorithm according to IETF RFC 896. If enabled the Nagle’s algorithm is activated per default for all TCP sockets, but can be deactivated via TcpIp_ChangeParameter() API.

########## 6. TcpIpTcpSlowStartEnabled

- **UUID**: `b65d3ad7-a9dd-4a1d-9ab6-99a820b722ce`
- **参数名**: `TcpIpTcpSlowStartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP slow start algorithm according to IETF RFC 5681.

########## 7. TcpIpTcpEnableDiagReadAckSeqNum

- **UUID**: `648a1543-f1c2-4b09-a785-e95cf482c1bf`
- **参数名**: `TcpIpTcpEnableDiagReadAckSeqNum`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable reading of current TCP sequence number and acknowledgement number for a specified socket.

########## 8. TcpIpTcpSackOptionSupport

- **UUID**: `b1ae3760-7dff-4558-93ec-c14ba1f829a8`
- **参数名**: `TcpIpTcpSackOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the TCP option 'selective acknowlagement' is enabled.
[RFC 2018]

RESTRICTIONS: 'TcpSackOptionSupport' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

########## 9. TcpIpTcpUserTimeoutOptionSupport

- **UUID**: `d7170237-f65e-442b-882a-cc5c8e010d35`
- **参数名**: `TcpIpTcpUserTimeoutOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the User Timeout Option of TCP is enabled.

########## 10. TcpIpTcpTimeStampOptionSupport

- **UUID**: `9bdfc8a2-b42b-4b26-8ddc-871fea60607a`
- **参数名**: `TcpIpTcpTimeStampOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the Timestamp Option of TCP is enabled.

########## 11. TcpIpTcpOutOfOrderRxSupport

- **UUID**: `fe72aa01-e5dc-4492-bb66-b038c8f6a3e7`
- **参数名**: `TcpIpTcpOutOfOrderRxSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the reception of out of order TCP segments is supported.

######### FLOAT 类型参数

########## 1. TcpIpTcpFinWait2Timeout

- **UUID**: `f47ac90d-f6b7-45bd-9e3d-62e895e359cd`
- **参数名**: `TcpIpTcpFinWait2Timeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] to receive a FIN from the remote node (after this node has initiated connection termination), i.e. maximum time waiting in FINWAIT-2 for a connection termination request from the remote TCP.

########## 2. TcpIpTcpKeepAliveInterval

- **UUID**: `9763d9aa-9ee6-4a34-a63f-1176847a01a7`
- **参数名**: `TcpIpTcpKeepAliveInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the interval in [s] between subsequent keepalive probes.

########## 3. TcpIpTcpKeepAliveTime

- **UUID**: `221739f6-e136-448b-ac38-e6d782db2b07`
- **参数名**: `TcpIpTcpKeepAliveTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the time in [s] between the last data packet sent (simple ACKs are not considered data) and the first keepalive probe. Note: Setting this configuration parameter to a value smaller or equal to the value of TcpIpMainFunctionPeriod results in the transmission of keep alive probes within every MainFunction cycle.

########## 4. TcpIpTcpMsl

- **UUID**: `f9cbef19-c89e-4956-a226-61f33ec7654e`
- **参数名**: `TcpIpTcpMsl`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `120`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum segment lifetime in [s].

########## 5. TcpIpTcpRetransmissionTimeout

- **UUID**: `fd9d758d-c2d8-487f-bd0b-b3d76f04c987`
- **参数名**: `TcpIpTcpRetransmissionTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0.001..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] before an unacknowledged TCP segment is sent again.

########## 6. TcpIpTcpSynReceivedTimeout

- **UUID**: `00286551-808e-403e-aa93-7f79b4153ce1`
- **参数名**: `TcpIpTcpSynReceivedTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] to complete a remotely initiated TCP connection establishment, i.e. maximum time waiting in SYN-RECEIVED for a confirming connection request acknowledgment after having both received and sent a connection request.

########## 7. TcpIpTcpUserTimeoutDef

- **UUID**: `6c7d23b6-e5ce-41ca-bf9f-0b119b979986`
- **参数名**: `TcpIpTcpUserTimeoutDef`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default value for User Timeout.
(default: 20s)
(time transmitted data may stay un-acknowlaged)

RESTRICTION: Value of 'TcpUserTimeoutDef' has to be in the range defined by 'TcpUserTimeoutMin' and 'TcpUserTimeoutMax'.

########## 8. TcpIpTcpUserTimeoutMax

- **UUID**: `97fe9a77-ec91-4c59-82ff-ad63abe5d901`
- **参数名**: `TcpIpTcpUserTimeoutMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `300`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the maximum value for User Timeout.
(default: 300s)

RESTRICTION: Value of 'TcpUserTimeoutMax' has to be greater than 'TcpUserTimeoutMin' and greater than or equal to 'TcpUserTimeoutDef'.

########## 9. TcpIpTcpUserTimeoutMin

- **UUID**: `4074990f-5fd9-4775-937c-7368a2197ef7`
- **参数名**: `TcpIpTcpUserTimeoutMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..5000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum value for User Timeout.
(default: 5s)
RFC 1122 defines it to 100 seconds (3 minutes for SYN segments).

RESTRICTION: Value of 'TcpUserTimeoutMin' has to be smaller than 'TcpUserTimeoutMax' and smaller than or equal to 'TcpUserTimeoutDef'.

########## 10. TcpIpTcpTxRetryIntMaxTime

- **UUID**: `5e7b53e8-7aa8-4856-a259-f03a647f18f1`
- **参数名**: `TcpIpTcpTxRetryIntMaxTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [10..60]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound of the time interval, in which the retransmittion of a not acknowledged TCP packet is triggered.

########## 11. TcpIpTcpTxRetryIntMinTime

- **UUID**: `49e579c0-d498-449a-a506-ffeb836de633`
- **参数名**: `TcpIpTcpTxRetryIntMinTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.1..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound of the time interval, in which the retransmittion of a not acknowledged TCP packet is triggered.

########## 12. TcpIpTcpNagleTimeout

- **UUID**: `86d734b0-dfe6-468f-8cec-273ea4454e57`
- **参数名**: `TcpIpTcpNagleTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the timeout for Nagle algorithm,

Note:
Value must be a multiple of Main Function Period

RESTRICTIONS: 'TcpNagleTimeoutMsec' is only available, if 'TcpEnableNagle' is enabled.

########## 13. TcpIpTcpIdleTimeout

- **UUID**: `5880ffe0-2131-4be8-a4fc-596de5501492`
- **参数名**: `TcpIpTcpIdleTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the TCP idle timeout (must be bigger than MSL timeout)

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpTcpSocketBuffer

**容器属性**:

- **UUID**: `1109a158-037d-4a0d-afbe-dceded4de7aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpSocketBuffer`
- **多重性**: [1..infinite]

**容器描述**:

This container includes the rx and tx buffer configuration of a TCP socket. 
The number of available socket handles will be the sum of all TCP rx and tx buffer configurations and the number of all TCP listen sockets.

Note: rx and tx buffers are not bound to a specific socket handle. 
The buffers are shared between all users and must be allocated to a socket during runtime via the TcpIp_ChangeParameter() API.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpTcpSocketRxBufferSize

- **UUID**: `ad411939-2b30-425f-a1f7-60d953202e96`
- **参数名**: `TcpIpTcpSocketRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a RX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

############ 2. TcpIpTcpSocketTxBufferSize

- **UUID**: `036a1a56-15d7-4b4f-9b0c-81a782c48b2a`
- **参数名**: `TcpIpTcpSocketTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a TX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

####### 38. TcpIpTcpSocketBuffer

**容器属性**:

- **UUID**: `1109a158-037d-4a0d-afbe-dceded4de7aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpSocketBuffer`
- **多重性**: [1..infinite]

**容器描述**:

This container includes the rx and tx buffer configuration of a TCP socket. 
The number of available socket handles will be the sum of all TCP rx and tx buffer configurations and the number of all TCP listen sockets.

Note: rx and tx buffers are not bound to a specific socket handle. 
The buffers are shared between all users and must be allocated to a socket during runtime via the TcpIp_ChangeParameter() API.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpTcpSocketRxBufferSize

- **UUID**: `ad411939-2b30-425f-a1f7-60d953202e96`
- **参数名**: `TcpIpTcpSocketRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a RX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

########## 2. TcpIpTcpSocketTxBufferSize

- **UUID**: `036a1a56-15d7-4b4f-9b0c-81a782c48b2a`
- **参数名**: `TcpIpTcpSocketTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a TX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

####### 39. TcpIpUdpConfig

**容器属性**:

- **UUID**: `18648ba8-01de-4125-806b-c826fe615aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specifies the configuration parameters of the UDP (User Datagram Protocol) sub-module

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpUdpTtl

- **UUID**: `600fcc21-1028-4ed2-8de4-6cca16b1cb48`
- **参数名**: `TcpIpUdpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing UDP packets.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpUdpTxReqList

**容器属性**:

- **UUID**: `16114d8f-6758-4001-9821-5a0acc0c08a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpTxReqList`
- **多重性**: [0..infinite]

**容器描述**:

This container includes configuration parameters of a UDP TX request list that can be attached to a UDP socket handle via TcpIp_ChangeParameter() during runtime.

A UDP socket only needs a TX request list if a TxConfirmation is required by the upper layer.

Note: A UDP tx request list is shared between all UDP sockets but can only be used for one socket at a time. If multiple sockets with the same request list size shall be used simultaneously, multiple request lists of the same size have to be configured.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpUdpTxReqListSize

- **UUID**: `6b572316-8596-4a09-8d9e-8e2bc755bbc4`
- **参数名**: `TcpIpUdpTxReqListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of entries in the UDP TX request list.

####### 40. TcpIpUdpTxReqList

**容器属性**:

- **UUID**: `16114d8f-6758-4001-9821-5a0acc0c08a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpTxReqList`
- **多重性**: [0..infinite]

**容器描述**:

This container includes configuration parameters of a UDP TX request list that can be attached to a UDP socket handle via TcpIp_ChangeParameter() during runtime.

A UDP socket only needs a TX request list if a TxConfirmation is required by the upper layer.

Note: A UDP tx request list is shared between all UDP sockets but can only be used for one socket at a time. If multiple sockets with the same request list size shall be used simultaneously, multiple request lists of the same size have to be configured.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpUdpTxReqListSize

- **UUID**: `6b572316-8596-4a09-8d9e-8e2bc755bbc4`
- **参数名**: `TcpIpUdpTxReqListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of entries in the UDP TX request list.

####### 41. TcpIpIpVXCtrl

**容器属性**:

- **UUID**: `c7454466-eafa-4093-9930-19ededbf3a4e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `TcpIpIpVXCtrl`
- **多重性**: [1..1]

**容器选择**:

- **TcpIpIpV4Ctrl**
  - UUID: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
  - 描述: Specifies an Internet Protocol version 4 (IPv4) instance.
- **TcpIpIpV6Ctrl**
  - UUID: `739c0200-ae9c-42da-8178-469e4380cfe7`
  - 描述: Specifies an Internet Protocol version 6 (IPv6) instance.
- **TcpIpIpV6MtuConfig**
  - UUID: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
  - 描述: This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

**容器描述**:

Specifies whether this controller is an Internet Protocol version 4 (IPv4) or Internet Protocol version 6 (IPv4) instance.

##### 2. TcpIpCtrl

**容器属性**:

- **UUID**: `fa0185ea-8bbc-4d6b-9fdd-569acd00f722`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrl`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the EthIf controller used for IP communication and TcpIp errors that shall be reported to DEM.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpFramePrioDefault

- **UUID**: `4a48e069-b06d-4378-999f-a6cbf5bdae16`
- **参数名**: `TcpIpIpFramePrioDefault`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the default value for the frame priority used by all sockets.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpDhcpServerConfigRef

- **UUID**: `437632f9-fa1f-4d6a-b547-e284ab6a07ab`
- **引用名**: `TcpIpDhcpServerConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpServerConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpDhcpServerConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a TcpIpDhcpServerConfig which shall be used for this controller setting (VLAN).

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. TcpIpEthIfCtrlRef

- **UUID**: `31ec8ab1-1bc4-46d2-b79f-3d2d345aaefc`
- **引用名**: `TcpIpEthIfCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to EthIf controller where the IP address shall be assigned.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. TcpIpCtrlDemEventParameterRefs

**容器属性**:

- **UUID**: `171d8e15-2221-4c34-97ee-fecd3dd4148c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrlDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpCtrl and specifies the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding TcpIp error occurs for communication on the EthIf Controller. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TCPIP_E_CONNREFUSED

- **UUID**: `a1d84fdb-d29a-4cfd-ac49-d4a44677a60b`
- **引用名**: `TCPIP_E_CONNREFUSED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Connection refused” has occurred.

########## 2. TCPIP_E_HOSTUNREACH

- **UUID**: `f3780506-6517-4701-8785-46acedc4347f`
- **引用名**: `TCPIP_E_HOSTUNREACH`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "No route to host” has occurred.

########## 3. TCPIP_E_PACKETTOBIG

- **UUID**: `b42e0ca4-3ecf-4695-9272-38671b10ea3e`
- **引用名**: `TCPIP_E_PACKETTOBIG`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Path does not support frame size" has occurred.

########## 4. TCPIP_E_TIMEDOUT

- **UUID**: `42bd5b2a-fecc-46d2-b944-a7f725fe2c0f`
- **引用名**: `TCPIP_E_TIMEDOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Operation timed out” has occurred.

####### 2. TcpIpIpV4Ctrl

**容器属性**:

- **UUID**: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 4 (IPv4) instance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpTypeOfServiceDefault

- **UUID**: `ae037c79-b220-4a64-9345-7b7ee8a5d1fc`
- **参数名**: `TcpIpIpTypeOfServiceDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Type of Service" field of the IPv4 header in outgoing packets on this IP controller.

########## 2. TcpIpIpCtrlIdx

- **UUID**: `2d481e8c-7607-4368-bbd2-60ab601b3643`
- **参数名**: `TcpIpIpCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv4 controller index (calculated automatically)

########## 3. TcpIpIpDefaultTtl

- **UUID**: `9b3a7947-c7a7-46db-982c-440fab0e0884`
- **参数名**: `TcpIpIpDefaultTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Time to Live" field of the IPv4 header in outgoing packets on this IP controller.

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpArpConfigRef

- **UUID**: `7bd8c38e-2a76-40f0-97d5-68397b972d43`
- **引用名**: `TcpIpArpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpArpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpArpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to ARP configuration for this IPv4 instance.

########## 2. TcpIpAutoIpConfigRef

- **UUID**: `464b79fb-c0e5-42fc-9237-68c9ebac4fea`
- **引用名**: `TcpIpAutoIpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpAutoIpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpAutoIpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to AutoIp configuration for this IPv4 instance.

########## 3. TcpIpDhcpConfigRef

- **UUID**: `71225b07-2bf6-4aec-8332-fbe97401610f`
- **引用名**: `TcpIpDhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpDhcpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCP configuration for this IPv4 instance.

########## 4. TcpIpFragmentationConfigRef

- **UUID**: `1082db5e-3319-4ece-961a-2bc452de93ed`
- **引用名**: `TcpIpFragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpFragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpIpFragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Fragmentation configuration for this IPv4 instance.

########## 5. TcpIpStaticArpTableRef

- **UUID**: `7cae9e88-93a6-4ebf-87c1-b84a6b6bc333`
- **引用名**: `TcpIpStaticArpTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpStaticArpTable`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpStaticArpTable`
- **来源**: Vector Informatik
- **描述**: Reference to a static ARP table that shall be used for this controller.

####### 3. TcpIpIpV6Ctrl

**容器属性**:

- **UUID**: `739c0200-ae9c-42da-8178-469e4380cfe7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 6 (IPv6) instance.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6DefaultHopLimit

- **UUID**: `97eff9a8-3b09-4983-bb0c-15ed7584624a`
- **参数名**: `TcpIpIpV6DefaultHopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default Hop Limit for outgoing IPv6 packets. If "Allow Hop Limit Reconfiguration" is checked, the value may be reconfigured based on received Router Advertisements according to [RFC4861 6.3.4. Processing Received Router Advertisements].

########## 2. TcpIpIpV6DefaultTrafficClass

- **UUID**: `8b7ee167-db6d-4482-9ed1-0bc056c6a7df`
- **参数名**: `TcpIpIpV6DefaultTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'Traffic Class' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

########## 3. TcpIpIpV6DefaultFlowLabel

- **UUID**: `00a48c96-3ca4-4fbb-80fd-73a5a9a4cf19`
- **参数名**: `TcpIpIpV6DefaultFlowLabel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'FlowLabel' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

########## 4. TcpIpIpV6CtrlIdx

- **UUID**: `d067c0c6-3daf-4a64-97d4-b7abfe991021`
- **参数名**: `TcpIpIpV6CtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv6 controller index (calculated automatically)

######## 引用关系

此容器包含 **5** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpIpV6DhcpConfigRef

- **UUID**: `73944cf1-1420-4f8a-8fa7-8bfa1501dd96`
- **引用名**: `TcpIpIpV6DhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpV6Config`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpDhcpV6Config`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCPv6 configuration.

########## 2. TcpIpIpV6FragmentationConfigRef

- **UUID**: `6c6538e3-478e-448a-9603-4405e9e6eb2a`
- **引用名**: `TcpIpIpV6FragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6FragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpIpV6FragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to IPv6 Fragmentation Configuration.

########## 3. TcpIpIpV6NdpConfigRef

- **UUID**: `71a3d2ba-aefa-4d9c-b7e4-55ffc06e4812`
- **引用名**: `TcpIpIpV6NdpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpNdpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Neighbor Discovery Protocol Configuration.

########## 4. TcpIpIpV6MldConfigRef

- **UUID**: `63245d91-769a-4507-86d1-ae901e82ec6b`
- **引用名**: `TcpIpIpV6MldConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6MldConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6MldConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Multicast Listener Discovery version 2 Configuration.
If no reference is set, MLDv2 [RFC3810] is disabled on this IpV6 instance.
(Multiple IpV6 instances may use the same configuration container but will operate independently)

########## 5. TcpIpIpV6PrivExtConfigRef

- **UUID**: `7659b8c3-9f71-4660-8393-f65b47df0891`
- **引用名**: `TcpIpIpV6PrivExtConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6PrivExtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6PrivExtConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Privacy Extensions Configuration.
If no reference is set, Privacy Extensions [RFC4941] are disabled on this IpV6 instance,
(Multiple IpV6 instances may use the same configuration container but will operate independently)

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

########### BOOLEAN 类型参数

############ 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

########### FLOAT 类型参数

############ 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

####### 4. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

######### BOOLEAN 类型参数

########## 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

######### FLOAT 类型参数

########## 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

####### 5. TcpIpIpVXCtrl

**容器属性**:

- **UUID**: `c7454466-eafa-4093-9930-19ededbf3a4e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `TcpIpIpVXCtrl`
- **多重性**: [1..1]

**容器选择**:

- **TcpIpIpV4Ctrl**
  - UUID: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
  - 描述: Specifies an Internet Protocol version 4 (IPv4) instance.
- **TcpIpIpV6Ctrl**
  - UUID: `739c0200-ae9c-42da-8178-469e4380cfe7`
  - 描述: Specifies an Internet Protocol version 6 (IPv6) instance.
- **TcpIpIpV6MtuConfig**
  - UUID: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
  - 描述: This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

**容器描述**:

Specifies whether this controller is an Internet Protocol version 4 (IPv4) or Internet Protocol version 6 (IPv4) instance.

##### 3. TcpIpCtrlDemEventParameterRefs

**容器属性**:

- **UUID**: `171d8e15-2221-4c34-97ee-fecd3dd4148c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpCtrlDemEventParameterRefs`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpCtrl and specifies the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding TcpIp error occurs for communication on the EthIf Controller. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **4** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. TCPIP_E_CONNREFUSED

- **UUID**: `a1d84fdb-d29a-4cfd-ac49-d4a44677a60b`
- **引用名**: `TCPIP_E_CONNREFUSED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Connection refused” has occurred.

######## 2. TCPIP_E_HOSTUNREACH

- **UUID**: `f3780506-6517-4701-8785-46acedc4347f`
- **引用名**: `TCPIP_E_HOSTUNREACH`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "No route to host” has occurred.

######## 3. TCPIP_E_PACKETTOBIG

- **UUID**: `b42e0ca4-3ecf-4695-9272-38671b10ea3e`
- **引用名**: `TCPIP_E_PACKETTOBIG`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Path does not support frame size" has occurred.

######## 4. TCPIP_E_TIMEDOUT

- **UUID**: `42bd5b2a-fecc-46d2-b944-a7f725fe2c0f`
- **引用名**: `TCPIP_E_TIMEDOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Operation timed out” has occurred.

##### 4. TcpIpIpV4Ctrl

**容器属性**:

- **UUID**: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 4 (IPv4) instance.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpTypeOfServiceDefault

- **UUID**: `ae037c79-b220-4a64-9345-7b7ee8a5d1fc`
- **参数名**: `TcpIpIpTypeOfServiceDefault`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Type of Service" field of the IPv4 header in outgoing packets on this IP controller.

######## 2. TcpIpIpCtrlIdx

- **UUID**: `2d481e8c-7607-4368-bbd2-60ab601b3643`
- **参数名**: `TcpIpIpCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv4 controller index (calculated automatically)

######## 3. TcpIpIpDefaultTtl

- **UUID**: `9b3a7947-c7a7-46db-982c-440fab0e0884`
- **参数名**: `TcpIpIpDefaultTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default for the "Time to Live" field of the IPv4 header in outgoing packets on this IP controller.

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpArpConfigRef

- **UUID**: `7bd8c38e-2a76-40f0-97d5-68397b972d43`
- **引用名**: `TcpIpArpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpArpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpArpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to ARP configuration for this IPv4 instance.

######## 2. TcpIpAutoIpConfigRef

- **UUID**: `464b79fb-c0e5-42fc-9237-68c9ebac4fea`
- **引用名**: `TcpIpAutoIpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpAutoIpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpAutoIpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to AutoIp configuration for this IPv4 instance.

######## 3. TcpIpDhcpConfigRef

- **UUID**: `71225b07-2bf6-4aec-8332-fbe97401610f`
- **引用名**: `TcpIpDhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpDhcpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCP configuration for this IPv4 instance.

######## 4. TcpIpFragmentationConfigRef

- **UUID**: `1082db5e-3319-4ece-961a-2bc452de93ed`
- **引用名**: `TcpIpFragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpFragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpIpFragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Fragmentation configuration for this IPv4 instance.

######## 5. TcpIpStaticArpTableRef

- **UUID**: `7cae9e88-93a6-4ebf-87c1-b84a6b6bc333`
- **引用名**: `TcpIpStaticArpTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpStaticArpTable`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV4Config/TcpIpStaticArpTable`
- **来源**: Vector Informatik
- **描述**: Reference to a static ARP table that shall be used for this controller.

##### 5. TcpIpIpV6Ctrl

**容器属性**:

- **UUID**: `739c0200-ae9c-42da-8178-469e4380cfe7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Ctrl`
- **多重性**: [0..1]

**容器描述**:

Specifies an Internet Protocol version 6 (IPv6) instance.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpV6DefaultHopLimit

- **UUID**: `97eff9a8-3b09-4983-bb0c-15ed7584624a`
- **参数名**: `TcpIpIpV6DefaultHopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default Hop Limit for outgoing IPv6 packets. If "Allow Hop Limit Reconfiguration" is checked, the value may be reconfigured based on received Router Advertisements according to [RFC4861 6.3.4. Processing Received Router Advertisements].

######## 2. TcpIpIpV6DefaultTrafficClass

- **UUID**: `8b7ee167-db6d-4482-9ed1-0bc056c6a7df`
- **参数名**: `TcpIpIpV6DefaultTrafficClass`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'Traffic Class' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

######## 3. TcpIpIpV6DefaultFlowLabel

- **UUID**: `00a48c96-3ca4-4fbb-80fd-73a5a9a4cf19`
- **参数名**: `TcpIpIpV6DefaultFlowLabel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1048575]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default 'FlowLabel' set in the IPv6 header of outgoing packets of this controller.
This value may be changed to a socket specific value during runtime.

######## 4. TcpIpIpV6CtrlIdx

- **UUID**: `d067c0c6-3daf-4a64-97d4-b7abfe991021`
- **参数名**: `TcpIpIpV6CtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: true
- **描述**: IPv6 controller index (calculated automatically)

###### 引用关系

此容器包含 **5** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpIpV6DhcpConfigRef

- **UUID**: `73944cf1-1420-4f8a-8fa7-8bfa1501dd96`
- **引用名**: `TcpIpIpV6DhcpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpDhcpV6Config`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpDhcpV6Config`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to DHCPv6 configuration.

######## 2. TcpIpIpV6FragmentationConfigRef

- **UUID**: `6c6538e3-478e-448a-9603-4405e9e6eb2a`
- **引用名**: `TcpIpIpV6FragmentationConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6FragmentationConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpIpV6FragmentationConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to IPv6 Fragmentation Configuration.

######## 3. TcpIpIpV6NdpConfigRef

- **UUID**: `71a3d2ba-aefa-4d9c-b7e4-55ffc06e4812`
- **引用名**: `TcpIpIpV6NdpConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpNdpConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Neighbor Discovery Protocol Configuration.

######## 4. TcpIpIpV6MldConfigRef

- **UUID**: `63245d91-769a-4507-86d1-ae901e82ec6b`
- **引用名**: `TcpIpIpV6MldConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6MldConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6MldConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Multicast Listener Discovery version 2 Configuration.
If no reference is set, MLDv2 [RFC3810] is disabled on this IpV6 instance.
(Multiple IpV6 instances may use the same configuration container but will operate independently)

######## 5. TcpIpIpV6PrivExtConfigRef

- **UUID**: `7659b8c3-9f71-4660-8393-f65b47df0891`
- **引用名**: `TcpIpIpV6PrivExtConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6PrivExtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpIpConfig/TcpIpIpV6Config/TcpIpNdpConfig/TcpIpIpV6PrivExtConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to Privacy Extensions Configuration.
If no reference is set, Privacy Extensions [RFC4941] are disabled on this IpV6 instance,
(Multiple IpV6 instances may use the same configuration container but will operate independently)

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

######### BOOLEAN 类型参数

########## 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

######### FLOAT 类型参数

########## 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

##### 6. TcpIpIpV6MtuConfig

**容器属性**:

- **UUID**: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MtuConfig`
- **多重性**: [1..1]

**容器描述**:

This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpV6DefaultMtuSize

- **UUID**: `6d215459-127b-4424-bad3-4d3d84d37f2c`
- **参数名**: `TcpIpIpV6DefaultMtuSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1500`
- **取值范围**: [1280..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum Transmission Unit (MTU) of the link.

####### BOOLEAN 类型参数

######## 1. TcpIpIpV6PathMtuEnabled

- **UUID**: `16a113dc-b8c7-4c10-ba8c-6308a25f4353`
- **参数名**: `TcpIpIpV6PathMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the IPv6 processes incoming ICMPv6 "Packet Too Big" messages and stores a MTU value for each destination address.

####### FLOAT 类型参数

######## 1. TcpIpIpV6PathMtuTimeout

- **UUID**: `eaccd3b1-bd1c-4fb4-8409-af69dcd3206a`
- **参数名**: `TcpIpIpV6PathMtuTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..86400]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this value is >0 the IpV6 will reset the MTU value stored for each destination after n seconds.

##### 7. TcpIpDhcpServerConfig

**容器属性**:

- **UUID**: `1dd0738d-1fce-4b7e-9a36-0d578df47e44`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpServerConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCP Server sub-module.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpDhcpNetmask

- **UUID**: `cf95c447-31eb-42c5-8d31-7375534ea05c`
- **参数名**: `TcpIpDhcpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `24`
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

######## 2. TcpIpDhcpMaxClientIdLen

- **UUID**: `b9118591-7d3b-4f97-b77b-7e565a418b4d`
- **参数名**: `TcpIpDhcpMaxClientIdLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [6..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maxumin length of a DHCP client identifier.
A client identifier may be either the value of the 'chaddr' filed in the DHCP message header or the content of the client identifier option [RFC2132 9.14. Client-identifier]. A client identifer may be up to 255 bytes long but usually the client MAC address is used as client identifer. This value should be at least set to 7 in order to store the type (1 byte) and the address value (6 bytes).

####### FLOAT 类型参数

######## 1. TcpIpDhcpOfferValidTime

- **UUID**: `4422c6da-00d4-435e-9ef7-20d13c131a87`
- **参数名**: `TcpIpDhcpOfferValidTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE

######## 2. TcpIpDhcpLeaseTimeMax

- **UUID**: `37fa2a4f-6c70-407e-917b-cc620d105ba3`
- **参数名**: `TcpIpDhcpLeaseTimeMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum lease time. If a client requests a longer lease time the server will use this maximum value instead.
If this parameter does not exists the maximum lease time is infinite.

######## 3. TcpIpDhcpLeaseTimeMin

- **UUID**: `7a6fe8d0-d21d-467b-9df4-68dfcca3b33f`
- **参数名**: `TcpIpDhcpLeaseTimeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum lease time. If a client requests a shorter lease time the server will use this minimum value instead.

######## 4. TcpIpDhcpLeaseTimeDefault

- **UUID**: `b959d8fa-3d4e-4d6a-9a81-3b1f9fa5dc62`
- **参数名**: `TcpIpDhcpLeaseTimeDefault`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `4294967295`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default lease time that is used if a client does not has requested a specific lease time.
If this parameter does not exist the maximum lease time will be used as default.

####### STRING 类型参数

######## 1. TcpIpDhcpDefaultRouter

- **UUID**: `5b4fc04d-1532-4f96-8c22-eb13042061d7`
- **参数名**: `TcpIpDhcpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway).

######## 2. TcpIpDhcpGetPortMacAddrFunctionInclude

- **UUID**: `4a125b98-6fa9-4a6a-9f68-616a8bc11896`
- **参数名**: `TcpIpDhcpGetPortMacAddrFunctionInclude`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 默认值: `EthIf.h`
  - 最小长度: 3
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of a header file that contains the declaration of the function defined in TcpIpGetPortMacAddrFunctionName.

######## 3. TcpIpDhcpHostname

- **UUID**: `705720e0-fa08-4af9-8906-ebc82af1fbfd`
- **参数名**: `TcpIpDhcpHostname`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 64
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the value of the DHCP server name that will be sent in the 'sname' field of outgoing DHCPOFFER, DHCPACK and DHCPNAK messages.

####### FUNCTION-NAME 类型参数

######## 1. TcpIpDhcpGetPortMacAddrFunctionName

- **UUID**: `424b3df9-06a9-46be-9180-4fb53fa404fd`
- **参数名**: `TcpIpDhcpGetPortMacAddrFunctionName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **函数变体**:
  - 默认值: `EthIf_GetPortMacAddr`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of a function that will be called in order to map a client link-layer (MAC) address to a switch index and port index.
The valid address assignment configurations for a client are selected based on these values.

The function must have the following signature:
Std_ReturnType [TcpIpGetPortMacAddrFunctionName](uint8* MacAddrPtr, uint8* SwitchIdxPtr, uint8* PortIdxPtr)

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. TcpIpDhcpEthIfSwitchRef

- **UUID**: `bd17f471-6149-4c36-ab4f-beb071214cee`
- **引用名**: `TcpIpDhcpEthIfSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthIfSwitch`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfSwitch`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to EthIfSwitch representation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpDhcpAddressAssignment

**容器属性**:

- **UUID**: `5659caac-1d3e-4763-9796-197a6c159b98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpAddressAssignment`
- **多重性**: [0..infinite]

**容器描述**:

Defines a Ethernet Switch port based IP address assignment.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpDhcpAddressLowerBound

- **UUID**: `547e9d46-173e-4371-a642-fc5dc2268763`
- **参数名**: `TcpIpDhcpAddressLowerBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The lower bound IP address which shall be assigned.

########## 2. TcpIpDhcpAddressUpperBound

- **UUID**: `e0134c3a-8251-4782-8a0b-01d2f17258ef`
- **参数名**: `TcpIpDhcpAddressUpperBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The upper bound IP address which shall be assigned.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. TcpIpDhcpSwitchPortRef

- **UUID**: `b4056ffe-3212-451b-a5e6-010d2a06491e`
- **引用名**: `TcpIpDhcpSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Ethernet Switch port.

########## 2. TcpIpDhcpLocalAddrRef

- **UUID**: `65bba8ea-a57a-4066-87ef-3728b0abf66f`
- **引用名**: `TcpIpDhcpLocalAddrRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a TcpIp local address on which this address assignment configuration shall be active. This reference specifies the interface/VLAN this address assignment shall be valid for.

##### 8. TcpIpDhcpAddressAssignment

**容器属性**:

- **UUID**: `5659caac-1d3e-4763-9796-197a6c159b98`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpAddressAssignment`
- **多重性**: [0..infinite]

**容器描述**:

Defines a Ethernet Switch port based IP address assignment.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. TcpIpDhcpAddressLowerBound

- **UUID**: `547e9d46-173e-4371-a642-fc5dc2268763`
- **参数名**: `TcpIpDhcpAddressLowerBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The lower bound IP address which shall be assigned.

######## 2. TcpIpDhcpAddressUpperBound

- **UUID**: `e0134c3a-8251-4782-8a0b-01d2f17258ef`
- **参数名**: `TcpIpDhcpAddressUpperBound`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The upper bound IP address which shall be assigned.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. TcpIpDhcpSwitchPortRef

- **UUID**: `b4056ffe-3212-451b-a5e6-010d2a06491e`
- **引用名**: `TcpIpDhcpSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to Ethernet Switch port.

######## 2. TcpIpDhcpLocalAddrRef

- **UUID**: `65bba8ea-a57a-4066-87ef-3728b0abf66f`
- **引用名**: `TcpIpDhcpLocalAddrRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpLocalAddr`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpLocalAddr`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a TcpIp local address on which this address assignment configuration shall be active. This reference specifies the interface/VLAN this address assignment shall be valid for.

##### 9. TcpIpIpConfig

**容器属性**:

- **UUID**: `e6111133-72b5-492f-b012-f8f1370587a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IP (Internet Protocol) sub-module

###### 配置容器

本模块包含 **20** 个配置容器：

####### 1. TcpIpIpV4Config

**容器属性**:

- **UUID**: `61db77db-188c-4120-bd67-39c656db06b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv4 (Internet Protocol version 4) sub-module.

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

############ 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

########### BOOLEAN 类型参数

############ 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

########### FLOAT 类型参数

############ 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

############ 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

############ 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

######### 2. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

############ 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

############ 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

########### FLOAT 类型参数

############ 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

############ 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

############ 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

############ 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

############ 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

############ 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

############ 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

############ 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

######### 3. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

############ 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### 4. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

############ 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 5. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######### 6. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

############ 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

########### BOOLEAN 类型参数

############ 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

########### FLOAT 类型参数

############ 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

######### 7. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

######### 8. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 2. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

########## 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

######### BOOLEAN 类型参数

########## 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

######### FLOAT 类型参数

########## 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

########## 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

########## 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

####### 3. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

########## 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

########## 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

######### FLOAT 类型参数

########## 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

########## 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

########## 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

########## 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

########## 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

########## 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

########## 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

########## 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

####### 4. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

####### 5. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

########## 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 6. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 7. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

########## 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

######### BOOLEAN 类型参数

########## 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

######### FLOAT 类型参数

########## 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

####### 8. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 9. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

########## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 10. TcpIpIpV6Config

**容器属性**:

- **UUID**: `852b8696-f018-4f10-a8d4-8705bd6fb938`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv6 (Internet Protocol version 6) sub-module.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

########## 参数配置

此容器包含 **12** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

########### BOOLEAN 类型参数

############ 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

############ 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

############ 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

############ 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

########### FLOAT 类型参数

############ 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

############ 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

############ 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

############ 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

############ 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

######### 2. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

############ 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

############ 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

########### BOOLEAN 类型参数

############ 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

############ 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

############ 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

############ 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

############ 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

############# FUNCTION-NAME 类型参数

############## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 3. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

######### 4. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

############ 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

############ 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

############ 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

############ 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

########### FLOAT 类型参数

############ 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

######### 5. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

############ 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

########## 配置容器

本模块包含 **5** 个配置容器：

########### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

############ 参数配置

此容器包含 **14** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############# FLOAT 类型参数

############## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

########### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

############ 参数配置

此容器包含 **11** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

############# FLOAT 类型参数

############## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

########### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

############ 参数配置

此容器包含 **6** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

############# BOOLEAN 类型参数

############## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

############# FLOAT 类型参数

############## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

########### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

############ 参数配置

此容器包含 **9** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

############# FLOAT 类型参数

############## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

########### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

############ 参数配置

此容器包含 **7** 个参数：

############# INTEGER 类型参数

############## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

############# BOOLEAN 类型参数

############## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

############# FLOAT 类型参数

############## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

######### 6. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 7. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 8. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 9. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 10. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 11. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

########## 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

########## 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

########## 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

########## 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

########## 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

########## 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

####### 12. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

########## 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

########## 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

######### BOOLEAN 类型参数

########## 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

########## 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

########## 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

########## 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

########## 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 13. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

########## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 14. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

########## 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

########## 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

########## 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

########## 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

######### FLOAT 类型参数

########## 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

####### 15. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

########## 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 16. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

######## 参数配置

此容器包含 **14** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

########## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

########## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

########## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

########## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

########## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

########## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

########## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######### FLOAT 类型参数

########## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

########## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

########## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

####### 17. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

########## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

########## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

########## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

########## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

########## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

########## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

########## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

######### FLOAT 类型参数

########## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

########## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

####### 18. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

########## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

######### FLOAT 类型参数

########## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

########## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

########## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

####### 19. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

########## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

########## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

########## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

########## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

########## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

######### FLOAT 类型参数

########## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

########## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

########## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

####### 20. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

########## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

######### BOOLEAN 类型参数

########## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

######### FLOAT 类型参数

########## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

########## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

##### 10. TcpIpIpV4Config

**容器属性**:

- **UUID**: `61db77db-188c-4120-bd67-39c656db06b6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv4 (Internet Protocol version 4) sub-module.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

########## 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

######### BOOLEAN 类型参数

########## 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

######### FLOAT 类型参数

########## 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

########## 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

########## 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

####### 2. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

########## 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

########## 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

######### FLOAT 类型参数

########## 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

########## 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

########## 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

########## 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

########## 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

########## 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

########## 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

########## 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

####### 3. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

########## 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

####### 4. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

########## 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 5. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

####### 6. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

########## 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

######### BOOLEAN 类型参数

########## 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

######### FLOAT 类型参数

########## 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

####### 7. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

############ 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

####### 8. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

########## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

##### 11. TcpIpArpConfig

**容器属性**:

- **UUID**: `fe9d3070-ccfd-4031-be09-b9e09b2ec078`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpArpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the ARP (Address Resolution Protocol) sub-module.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpArpNumGratuitousARPonStartup

- **UUID**: `e99492da-2582-4561-8c35-86563f0bf0cf`
- **参数名**: `TcpIpArpNumGratuitousARPonStartup`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the number of gratuitous ARP replies which shall be sent on assignment of a new IP address.

######## 2. TcpIpArpTableSizeMax

- **UUID**: `eb74e38d-a4f4-4114-a180-4a877e9246ed`
- **参数名**: `TcpIpArpTableSizeMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the ARP table.

####### BOOLEAN 类型参数

######## 1. TcpIpArpPacketQueueEnabled

- **UUID**: `c025e5a6-8787-43bb-a5fd-58e892dd5dbb`
- **参数名**: `TcpIpArpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of the ARP Packet Queue according to IETF RFC 1122, section 2.3.2.2.

####### FLOAT 类型参数

######## 1. TcpIpArpTableEntryTimeout

- **UUID**: `01629e6e-ce4b-47e1-8c4e-44558e37fbf3`
- **参数名**: `TcpIpArpTableEntryTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in seconds after which an unused ARP entry is removed.

######## 2. TcpIpArpRetryTime

- **UUID**: `05e03ab6-7476-4357-81fb-91eb84721232`
- **参数名**: `TcpIpArpRetryTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time for an ARP resolution.
If no answer has been received before this time has expired, ARP resolution is canceled.

######## 3. TcpIpArpRetryInterval

- **UUID**: `3b30286b-e8df-4c4b-82df-c0f1e85a79a6`
- **参数名**: `TcpIpArpRetryInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ARP retry interval.

##### 12. TcpIpAutoIpConfig

**容器属性**:

- **UUID**: `e570ea6b-48e1-4f68-a688-782b3747b985`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAutoIpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the Auto-IP (automatic private IP addressing) sub-module.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpAutoIpProbeNum

- **UUID**: `def0d6ec-df9b-48f2-82a3-de657abed824`
- **参数名**: `TcpIpAutoIpProbeNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of probe packets (RFC standard: 3)

######## 2. TcpIpAutoIpAnnounceNum

- **UUID**: `7f35a4de-41d5-4496-814e-7757af22af73`
- **参数名**: `TcpIpAutoIpAnnounceNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of announcement packets (RFC standard: 2)

######## 3. TcpIpAutoIpMaxConflicts

- **UUID**: `39ea80bc-b6bf-471d-b526-179002f31b71`
- **参数名**: `TcpIpAutoIpMaxConflicts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of conflicts before rate limiting (RFC standard: 10)

If the specified number of conflicts has been reached new address configurations attempts are rate limited by "Rate Limit Interval".

####### FLOAT 类型参数

######## 1. TcpIpAutoIpInitTimeout

- **UUID**: `3bb4d309-a0d2-4f6c-be82-a2a3535c7b12`
- **参数名**: `TcpIpAutoIpInitTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The time Auto-IP waits at startup, before beginning with ARP probing. This delay is used to give DHCP time to acquire a lease in case a DHCP server is present.

######## 2. TcpIpAutoIpProbeMin

- **UUID**: `2c2bc815-1386-41ef-85f3-a191f5264d3b`
- **参数名**: `TcpIpAutoIpProbeMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between probe messages (RFC standard: 1s)

######## 3. TcpIpAutoIpProbeMax

- **UUID**: `0bd6f823-4d44-4fa0-b399-6f647e2dd5d1`
- **参数名**: `TcpIpAutoIpProbeMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.6`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum delay between probe messages (RFC standard: 2s)

######## 4. TcpIpAutoIpAnnounceWait

- **UUID**: `a20e2884-e567-4d08-81f3-c64fa2b790de`
- **参数名**: `TcpIpAutoIpAnnounceWait`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay before the first announcement message (RFC standard: 2s)

######## 5. TcpIpAutoIpAnnounceInterval

- **UUID**: `54d0c603-0468-499f-93fe-7c1c4f92cb64`
- **参数名**: `TcpIpAutoIpAnnounceInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the interval between announcement packets (RFC standard: 2s)

######## 6. TcpIpAutoIpRateLimitInterval

- **UUID**: `bc1933d2-caa9-4b37-aa99-a2a370e42af4`
- **参数名**: `TcpIpAutoIpRateLimitInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the delay between successive address configuration attempts when rate limiting is active (RFC standard: 60s)

see "Max Number Of Conflicts"

######## 7. TcpIpAutoIpDefendInterval

- **UUID**: `7e717fac-5458-4c75-b9f1-fa2cbd7507ae`
- **参数名**: `TcpIpAutoIpDefendInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum interval between defensive ARPs (RFC standard: 10s)

######## 8. TcpIpAutoIpProbeWaitMax

- **UUID**: `e9ca4abc-cffe-4c3b-915b-7e85fae3a879`
- **参数名**: `TcpIpAutoIpProbeWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum initial random delay before the first probe message is sent. (RFC standard: 1s)

##### 13. TcpIpDhcpConfig

**容器属性**:

- **UUID**: `095c9a8d-524a-4106-9333-e602351abb95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv4.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpDhcpV4DiscoverMaxNum

- **UUID**: `0fe484ba-c5f1-4f35-9818-f0ab34b26350`
- **参数名**: `TcpIpDhcpV4DiscoverMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of DISCOVER messages

RESTRICTIONS: 'DhcpV4DiscoverMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 2. TcpIpDhcpV4RequestMaxNum

- **UUID**: `7d39e724-68ba-42cd-b582-21c1cddd35d1`
- **参数名**: `TcpIpDhcpV4RequestMaxNum`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of REQUEST messages

RESTRICTIONS: 'DhcpV4RequestMaxNum' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 3. TcpIpDhcpV4HostNameLenMax

- **UUID**: `5a76a881-b0af-417a-8b51-145a437ccf70`
- **参数名**: `TcpIpDhcpV4HostNameLenMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum support Host name length [byte]

RESTRICTIONS: 'DhcpV4HostNameLenMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

####### BOOLEAN 类型参数

######## 1. TcpIpDhcpV4RestartOnFail

- **UUID**: `76424154-e781-4344-a7a3-3fbb524f364b`
- **参数名**: `TcpIpDhcpV4RestartOnFail`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Restart the DHCP address assignment process if a used address lease times out and no lease update could be obtained. After the lease expires either the DHCP process is restarted or the process will be stopped completely (no new address assignment).

RESTRICTIONS: 'TcpIpDhcpV4RestartOnFail' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

####### FLOAT 类型参数

######## 1. TcpIpDhcpV4InitWaitMin

- **UUID**: `896ae055-c47b-4dfa-90c8-4cdf02d43266`
- **参数名**: `TcpIpDhcpV4InitWaitMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum initial delay for DISCOVER (RFC standard: 1s)

RESTRICTIONS: 'DhcpV4InitWaitMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 2. TcpIpDhcpV4InitWaitMax

- **UUID**: `5b13dc86-60dd-44e6-9acb-2be106995879`
- **参数名**: `TcpIpDhcpV4InitWaitMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `800`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum initial delay for DISCOVER (RFC standard: 10s)

RESTRICTIONS: 'DhcpV4InitWaitMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 3. TcpIpDhcpV4DiscoverIntervalMin

- **UUID**: `79231d1e-6638-4b1f-80a3-e16969a3cc99`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 4. TcpIpDhcpV4DiscoverIntervalMax

- **UUID**: `79f3f297-5db3-4af3-a939-75cca6154823`
- **参数名**: `TcpIpDhcpV4DiscoverIntervalMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum DISCOVER interval

RESTRICTIONS: 'DhcpV4DiscoverIntervalMax' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 5. TcpIpDhcpV4RequestInterval

- **UUID**: `38c28c76-f7a9-40f7-90e3-bdf60ff4c5b2`
- **参数名**: `TcpIpDhcpV4RequestInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: REQUEST interval

RESTRICTIONS: 'DhcpV4RequestInterval' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 6. TcpIpDhcpV4RenewIntervalMin

- **UUID**: `25fff6c2-1755-4f5a-ae23-a17870a41125`
- **参数名**: `TcpIpDhcpV4RenewIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Renew interval

RESTRICTIONS: 'DhcpV4RenewIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

######## 7. TcpIpDhcpV4RebindIntervalMin

- **UUID**: `0822ef67-ef53-4ce9-8656-0f15bbe31e79`
- **参数名**: `TcpIpDhcpV4RebindIntervalMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Minimum Rebind interval

RESTRICTIONS: 'DhcpV4RebindIntervalMin' is only available, if 'TcpIpEnableDhcpV4' is set to 'true'.

##### 14. TcpIpIcmpConfig

**容器属性**:

- **UUID**: `d31d6c5a-9ded-4e18-8ac5-8089905127d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the ICMP (Internet Control Message Protocol) sub-module.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIcmpTtl

- **UUID**: `d36dcbb7-c3e5-433c-b754-837aa8e07f12`
- **参数名**: `TcpIpIcmpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing ICMP packets.

######## 2. TcpIpIcmpEchoReplyMaxLen

- **UUID**: `5e6f24a6-fd84-4fe9-bcaa-58db98994587`
- **参数名**: `TcpIpIcmpEchoReplyMaxLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32767]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum payload length of an Echo Reply.
If an Echo Request contains more data the payload of the response will be truncated.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

##### 15. TcpIpIcmpMsgHandler

**容器属性**:

- **UUID**: `dfb89cc6-613b-4806-bb49-f1f35982290b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpMsgHandler`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMP message handler.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. TcpIpIcmpMsgHandlerHeaderFileName

- **UUID**: `d726ddfc-319c-47ab-9626-486a7ab2c513`
- **参数名**: `TcpIpIcmpMsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMP message handler function.

####### FUNCTION-NAME 类型参数

######## 1. TcpIpIcmpMsgHandlerName

- **UUID**: `4d40c565-f7da-4939-931a-75a589e487c7`
- **参数名**: `TcpIpIcmpMsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

##### 16. TcpIpIpFragmentationConfig

**容器属性**:

- **UUID**: `d3a8de10-ba6d-496f-83a9-cfaf937119d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpFragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv4 packet fragmentation/reassembly.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpNumFragments

- **UUID**: `6c5f7d62-30c7-4f61-bc7f-8958970e834b`
- **参数名**: `TcpIpIpNumFragments`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of IP fragments per datagram.

######## 2. TcpIpIpNumReassDgrams

- **UUID**: `b350d840-7805-4c26-84ad-2b946c8f0674`
- **参数名**: `TcpIpIpNumReassDgrams`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `3`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of fragmented IP datagrams that can be reassembled in parallel.

####### BOOLEAN 类型参数

######## 1. TcpIpIpFragmentationRxEnabled

- **UUID**: `f843b808-19d8-4696-a17c-c72881b9a7d7`
- **参数名**: `TcpIpIpFragmentationRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support for reassembling of incoming datagrams that are fragmented according to IETF RFC 815 (IP Datagram Reassembly Algorithms).

####### FLOAT 类型参数

######## 1. TcpIpIpReassTimeout

- **UUID**: `07836198-3f49-448b-ba7c-b1d4ad129a9d`
- **参数名**: `TcpIpIpReassTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the timeout in [s] after which an incomplete datagram gets discarded.

##### 17. TcpIpStaticArpTable

**容器属性**:

- **UUID**: `962cc953-240c-4e88-abff-b17c7bdd0c55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpTable`
- **多重性**: [0..infinite]

**容器描述**:

This container includes one or more static ARP table entries.
It may be referenced by multiple IpV4CtrlConfig containers if they shall use the same static ARP table.
The static ARP table is stored into the ROM and cannot be overwritten during runtime.
IP instances using this static ARP table will never send ARP requests for the configured addresses.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

########## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

##### 18. TcpIpStaticArpEntry

**容器属性**:

- **UUID**: `a768cd34-9ec8-48a0-80df-89635ce68e08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticArpEntry`
- **多重性**: [1..infinite]

**容器描述**:

This container includes a static IP address to physical address mapping.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. TcpIpStaticArpEntryIpAddr

- **UUID**: `f1ceebbd-85f7-4df7-b9c6-a8c7cb024d5d`
- **参数名**: `TcpIpStaticArpEntryIpAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 15
  - 最小长度: 7
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the IP address that shall be statically mapped to the physical address defined in IpV4StaticArpEntryPhysAddr

######## 2. TcpIpStaticArpEntryPhysAddr

- **UUID**: `b0e5ab81-c88d-491f-8a24-870389090458`
- **参数名**: `TcpIpStaticArpEntryPhysAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the physical address that shall be used for outgoing packets to the IP address specified in IpV4StaticArpEntryIpAddr

##### 19. TcpIpIpV6Config

**容器属性**:

- **UUID**: `852b8696-f018-4f10-a8d4-8705bd6fb938`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6Config`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the IPv6 (Internet Protocol version 6) sub-module.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

######## 参数配置

此容器包含 **12** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

########## 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

########## 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

########## 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

######### FLOAT 类型参数

########## 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

########## 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

########## 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

########## 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

########## 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

####### 2. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

########## 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

########## 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

######### BOOLEAN 类型参数

########## 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

########## 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

########## 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

########## 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

########## 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

########### FUNCTION-NAME 类型参数

############ 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

############ 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

############ 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 3. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

########## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

####### 4. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

########## 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

########## 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

########## 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

########## 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

######### FLOAT 类型参数

########## 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

####### 5. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

########## 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

########## 参数配置

此容器包含 **14** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

############ 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

############ 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

############ 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

############ 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

############ 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

############ 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

############ 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

############ 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########### FLOAT 类型参数

############ 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

############ 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

############ 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

######### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

########## 参数配置

此容器包含 **11** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

############ 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

############ 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

############ 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

############ 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

############ 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

############ 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

############ 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

########### FLOAT 类型参数

############ 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

############ 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

######### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

########### BOOLEAN 类型参数

############ 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

############ 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

########### FLOAT 类型参数

############ 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

############ 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

############ 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

######### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

############ 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

############ 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

############ 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

############ 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

############ 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

########### FLOAT 类型参数

############ 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

############ 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

############ 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

######### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

############ 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

########### BOOLEAN 类型参数

############ 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

########### FLOAT 类型参数

############ 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

############ 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

############ 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

####### 6. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

######## 参数配置

此容器包含 **14** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

########## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

########## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

########## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

########## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

########## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

########## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

########## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######### FLOAT 类型参数

########## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

########## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

########## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

####### 7. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

########## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

########## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

########## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

########## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

########## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

########## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

########## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

######### FLOAT 类型参数

########## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

########## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

####### 8. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

########## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

######### FLOAT 类型参数

########## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

########## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

########## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

####### 9. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

########## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

########## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

########## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

########## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

########## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

######### FLOAT 类型参数

########## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

########## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

########## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

####### 10. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

########## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

######### BOOLEAN 类型参数

########## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

######### FLOAT 类型参数

########## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

########## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

##### 20. TcpIpDhcpV6Config

**容器属性**:

- **UUID**: `5f7f6e81-f441-40f0-9fc5-c4c72eb6dba7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpDhcpV6Config`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of the DHCPv6.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpDhcpV6TxMsgBufferLen

- **UUID**: `635352f8-face-4394-b1b6-fe8f001d2539`
- **参数名**: `TcpIpDhcpV6TxMsgBufferLen`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [64..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of the buffer for outgoing DHCPv6 messages. The size of a DHCPv6 message depends on the number and length of options included in it.

####### BOOLEAN 类型参数

######## 1. TcpIpDhcpV6RandomizeTimeouts

- **UUID**: `9ca84df5-a99c-4f88-b7a7-1df6f6c2c87d`
- **参数名**: `TcpIpDhcpV6RandomizeTimeouts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use randomization factor for computing retransmission timeouts.

"Each of the computations of a new RT include a randomization factor (RAND), which is a random number chosen with a uniform distribution between -0.1 and +0.1. The randomization factor is included to minimize synchronization of messages transmitted by DHCP clients."

[RFC3315 14. Reliability of Client Initiated Message Exchanges]

######## 2. TcpIpDhcpV6UseFirstValidAdv

- **UUID**: `11deef79-8a1d-4657-8309-bdf40845b846`
- **参数名**: `TcpIpDhcpV6UseFirstValidAdv`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the Dhcp will not wait for other advertise messages if a valid one has been received but the preference is less than 255.

"A client MUST collect Advertise messages for the first RT seconds, unless it receives an Advertise message with a preference value of 255"

[RFC3315 17.1.2. Transmission of Solicit Messages]

######## 3. TcpIpDhcpV6Rfc3646DomainListOptEnabled

- **UUID**: `21e6a08b-1dcd-424a-a305-49fedcd87aaf`
- **参数名**: `TcpIpDhcpV6Rfc3646DomainListOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns search lists contained in DOMAIN_LIST options of received DHCPv6 Reply messages.

[RFC3646 4. Domain Search List option]

Requires Dns Component.

######## 4. TcpIpDhcpV6Rfc3646DnsServersOptEnabled

- **UUID**: `23292d42-0474-4fb4-adc4-83a276342dd6`
- **参数名**: `TcpIpDhcpV6Rfc3646DnsServersOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled the DhcpV6 will notify the Dns of dns server addresses contained in DNS_SERVERS options of received DHCPv6 Reply messages.

[RFC3646 3. DNS Recursive Name Server option]

Requires Dns Component.

####### FLOAT 类型参数

######## 1. TcpIpDhcpV6CnfDelayMax

- **UUID**: `14b41014-748f-4bbc-98d4-cc57574a0da2`
- **参数名**: `TcpIpDhcpV6CnfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Confirm message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

######## 2. TcpIpDhcpV6CnfDelayMin

- **UUID**: `0d90a415-ff8a-430c-a2db-6ac88d6481dd`
- **参数名**: `TcpIpDhcpV6CnfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Confirm message will be sent.

######## 3. TcpIpDhcpV6InfDelayMax

- **UUID**: `b038737f-723b-4b4b-a9a8-aeb6e3ed65bc`
- **参数名**: `TcpIpDhcpV6InfDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Information Request message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

######## 4. TcpIpDhcpV6InfDelayMin

- **UUID**: `bc9bca3e-5f34-4db1-975f-fbc1d0a60b34`
- **参数名**: `TcpIpDhcpV6InfDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Information Request message will be sent.

######## 5. TcpIpDhcpV6SolDelayMax

- **UUID**: `9d7f93e6-cbff-4cab-9bd2-f2889df7a334`
- **参数名**: `TcpIpDhcpV6SolDelayMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay (s) before sending the first Solicit message. If this value is bigger than the previous minimum delay value a random delay will be chosen from the interval.

######## 6. TcpIpDhcpV6SolDelayMin

- **UUID**: `0aee8c0b-742b-4547-ac3e-69fc383fbe4e`
- **参数名**: `TcpIpDhcpV6SolDelayMin`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum delay (s) before the first Solicit message will be sent.

######## 7. TcpIpDhcpV6ClientIdTime

- **UUID**: `09f2980f-1926-4d47-a909-7f477089cbc9`
- **参数名**: `TcpIpDhcpV6ClientIdTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time value used to build the DHCP Unique Identifier (DUID) of the client.

The Identifier of the client will be built from this time value and the link-layer address of this node.

"The time value is the time that the DUID is generated represented in seconds since midnight (UTC), January 1, 2000, modulo 2^32."

[RFC3315 9.2. DUID Based on Link-layer Address Plus Time [DUID-LLT]]

##### 21. TcpIpIcmpV6Config

**容器属性**:

- **UUID**: `46a4dd20-d4d4-44c5-9bc5-624ea7e7edf1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6Config`
- **多重性**: [1..1]

**容器描述**:

Specifies the configuration parameters of the ICMPv6 (Internet Control Message Protocol for IPv6) sub-module.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIcmpV6EchoDataBufferSize

- **UUID**: `b36675e5-699a-4ac0-b29d-fc9bcae8534f`
- **参数名**: `TcpIpIcmpV6EchoDataBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..1452]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configure the maximum amount of arbitrary data that will be sent back to the sender of an echo request. If the arbitrary data of an incoming echo request is bigger than configured here, the response payload will be truncated.

######## 2. TcpIpIcmpV6HopLimit

- **UUID**: `eec28e79-7517-4f58-94ba-1ad1b8ba07c7`
- **参数名**: `TcpIpIcmpV6HopLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Hop-Limit value of outgoing ICMPv6 packets.

######## 3. TcpIpIcmpV6TxMessageBufferSize

- **UUID**: `bc7714eb-33f6-4064-8717-8c47f95051e7`
- **参数名**: `TcpIpIcmpV6TxMessageBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [48..1280]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of outgoing ICMPv6 messages.
This value should be 1280 if IpV6EnableIcmpErrMsgs is enabled.
If the value is smaller the Original Packet payload in ICMPv6 Error messages will be truncated.

####### BOOLEAN 类型参数

######## 1. TcpIpIcmpV6EchoReplyEnabled

- **UUID**: `f467b05d-b327-4a56-9eac-a7bc29ae0479`
- **参数名**: `TcpIpIcmpV6EchoReplyEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled, the stack will respond to incoming ICMPv6 Echo Requests (Pings).

######## 2. TcpIpIcmpV6MsgDestinationUnreachableEnabled

- **UUID**: `0e915275-a801-414b-85ff-e4c1948dbc97`
- **参数名**: `TcpIpIcmpV6MsgDestinationUnreachableEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Dis/Enables transmission of Destination Unreachable Messages

######## 3. TcpIpIcmpV6MsgParameterProblemEnabled

- **UUID**: `ea3c1229-fd7f-43fe-aa93-117f8655f428`
- **参数名**: `TcpIpIcmpV6MsgParameterProblemEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled an ICMPv6 parameter problem message will be sent if a received packet has been dropped due to unknown options or headers that are found in the packet.

######## 4. TcpIpIcmpV6EchoRequestApiEnabled

- **UUID**: `66401d45-ee93-4afe-ab27-ed2be9abff95`
- **参数名**: `TcpIpIcmpV6EchoRequestApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the API function IpV6_Icmp_TxEchoRequest() is available. This function can be used to send outgoing Echo Requests (Pings) to other Hosts.

Note: This function is for debugging purposes only. Incoming Echo Replies are currently not handled by the ICMPv6.

######## 5. TcpIpIcmpV6ErrorMessagesEnabled

- **UUID**: `abfa5045-770f-40bf-8752-618c3b76f437`
- **参数名**: `TcpIpIcmpV6ErrorMessagesEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether ICMPv6 Error Messages will be sent as specified in [RFC4443].

[RFC4443 3.2. Packet Too Big Message]
[RFC4443 3.3. Time Exceeded Message]
[RFC4443 3.4. Parameter Problem Message]

If disabled, no ICMPv6 Error Messages will be sent

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

########## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

########## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

##### 22. TcpIpIcmpV6MsgHandler

**容器属性**:

- **UUID**: `a7814f65-8b08-4b6f-a254-e74d836e432f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIcmpV6MsgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpIcmpConfig and specifies the configuration parameters for the ICMPv6 message handler.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. TcpIpIcmpV6MsgHandlerHeaderFileName

- **UUID**: `9493c1bf-918c-486c-963f-1a7485740adf`
- **参数名**: `TcpIpIcmpV6MsgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the ICMPv6 message handler function.

####### FUNCTION-NAME 类型参数

######## 1. TcpIpIcmpV6MsgHandlerName

- **UUID**: `c392dd9f-e48a-43de-96e9-dce3ecd00dba`
- **参数名**: `TcpIpIcmpV6MsgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the ICMP message handler function <User_IcmpMsgHandler>.

######## 2. TcpIpIcmpV6MaxPayloadLenChgHandlerName

- **UUID**: `5e39b3b4-d74c-474b-8675-228cb905a0f4`
- **参数名**: `TcpIpIcmpV6MaxPayloadLenChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when the maximum payload length, that fits into one IPv6 packet, changes due to MTU limitations on the path to a specific destination.

see [RFC1981 Path MTU Discovery for IP version 6]

Callback function signature: void Cbk_Name(uint8 CtrlIdx, const IpBase_SockAddrType DstAddrPtr, uint16 Mtu)

For reasons of efficiency at least the callback "TcpIp_Cbk_VPathMtuChg" of "TcpIp_Cbk.h" should be configured here in order to avoid that TCP transmits packets that need to be fragmented by the IP layer.

######## 3. TcpIpIcmpV6IndAddrListReceivedHandlerName

- **UUID**: `526b7403-d881-445b-be07-35f71cb61391`
- **参数名**: `TcpIpIcmpV6IndAddrListReceivedHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a function that will be called when an Inverse Neighbor Discovery Solicitation or Advertisement with an Address List Option [RFC3122] is received.

Callback function signature: void Cbk_Name(uint8 CtrlIdx, IPV6_P2C(Eth_PhysAddrType) RemoteLLAddrPtr, IPV6_P2C(IpV6_AddrType) AddrListPtr, uint8 AddrCount);

##### 23. TcpIpIpV6FragmentationConfig

**容器属性**:

- **UUID**: `9a9db678-2190-4606-a8c1-8be8a0efba94`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6FragmentationConfig`
- **多重性**: [0..infinite]

**容器描述**:

Specifies the configuration parameters of IPv6 packet fragmentation/reassembly.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpIpV6ReassemblyBufferCount

- **UUID**: `5d040239-ec67-4a1a-8d33-ff96f8626ef1`
- **参数名**: `TcpIpIpV6ReassemblyBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of buffers that can be used for fragment reassembly. In case of a reassembly error or if not all fragments are received in time this buffer will be blocked until the specified "Fragment Reassembly Timeout" has been exceeded.

######## 2. TcpIpIpV6ReassemblyBufferSize

- **UUID**: `5909005a-0115-4e2c-a207-dea162d33528`
- **参数名**: `TcpIpIpV6ReassemblyBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 5. Packet Size Issues]

######## 3. TcpIpIpV6ReassemblySegmentCount

- **UUID**: `aefaa68f-2dd8-4e1a-a9af-4139effa2258`
- **参数名**: `TcpIpIpV6ReassemblySegmentCount`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the maximum number of consecutive data segments that can be managed in each reassembly buffer. If all fragments are received in order, only one segment will be needed.

######## 4. TcpIpIpV6TxFragmentBufferCount

- **UUID**: `e982f80e-cf78-46b6-87b2-1419207a9f9c`
- **参数名**: `TcpIpIpV6TxFragmentBufferCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: These buffers will be used if the IpV6 receives packets from the upper layer that do not fit into the MTU and thus must be fragmented.

######## 5. TcpIpIpV6TxFragmentBufferSize

- **UUID**: `d59e41e1-d3a7-4ebc-852a-a8df995b9f34`
- **参数名**: `TcpIpIpV6TxFragmentBufferSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1500`
- **取值范围**: [1500..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of each fragment tx buffer in bytes

####### FLOAT 类型参数

######## 1. TcpIpIpV6ReassemblyTimeout

- **UUID**: `a08567cf-0653-4778-8374-f7d8e2e5b9fd`
- **参数名**: `TcpIpIpV6ReassemblyTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0.001..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: [RFC2460 4.5 Fragment Header]

##### 24. TcpIpNdpConfig

**容器属性**:

- **UUID**: `5c419794-dad8-4742-aacf-19f3fbe10fd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpConfig`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the configuration parameters of the Neighbor Discovery Protocol for IPv6

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. TcpIpNdpRfc6106DnsslOptEnabled

- **UUID**: `a27f2540-ca40-4cb8-91f9-cb3140b7ad99`
- **参数名**: `TcpIpNdpRfc6106DnsslOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of domain names of DNS suffixes contained in DNSSL options of received Router Advertisements.

[RFC6106 5.2. DNS Search List Option]

######## 2. TcpIpNdpRfc6106RdnssOptEnabled

- **UUID**: `da20026f-8187-4d37-b13e-8be3d8dd0d9e`
- **参数名**: `TcpIpNdpRfc6106RdnssOptEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will notify the DNS of dns server adresses contained in RDNS options of received Router Advertisements.

[RFC6106 5.1. Recursive DNS Server Option]

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

######## 参数配置

此容器包含 **14** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

########## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

########## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

########## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

########## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

########## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

########## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

########## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

########## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######### FLOAT 类型参数

########## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

########## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

########## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

####### 2. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

########## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

########## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

########## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

########## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

########## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

########## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

########## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

######### FLOAT 类型参数

########## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

########## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

####### 3. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

######### BOOLEAN 类型参数

########## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

########## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

######### FLOAT 类型参数

########## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

########## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

########## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

####### 4. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

########## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

########## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

########## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

########## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

########## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

######### FLOAT 类型参数

########## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

########## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

########## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

####### 5. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

########## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

######### BOOLEAN 类型参数

########## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

######### FLOAT 类型参数

########## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

########## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

########## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

##### 25. TcpIpNdpArNudConfig

**容器属性**:

- **UUID**: `6721979b-d7d3-417d-88b2-432d2320e0a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpArNudConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Address Resolution and Neighbor Unreachability Detection.

###### 参数配置

此容器包含 **14** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpNdpMaxNeighborCacheSize

- **UUID**: `ca7fe087-4682-452e-807e-c3a08c7a7cf1`
- **参数名**: `TcpIpNdpMaxNeighborCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the neighbor cache.

######## 2. TcpIpNdpMaxRandomFactor

- **UUID**: `d4ca1f2c-720d-411e-ab60-c86d557c9557`
- **参数名**: `TcpIpNdpMaxRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum random factor used for randomization

######## 3. TcpIpNdpMinRandomFactor

- **UUID**: `4753de2b-8168-4026-b2ff-804c1b79ccdc`
- **参数名**: `TcpIpNdpMinRandomFactor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Minimum random factor used for randomization

######## 4. TcpIpNdpNumMulticastSolicitations

- **UUID**: `cb9c4e2a-d2db-40f9-83e6-c952b1524b8b`
- **参数名**: `TcpIpNdpNumMulticastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of multicast solicitations that will be sent when performing address resolution.

######## 5. TcpIpNdpNumUnicastSolicitations

- **UUID**: `87799990-5fbe-4566-a4d1-fd713ff5a283`
- **参数名**: `TcpIpNdpNumUnicastSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of unicast solicitations that will be sent when performig Neighbor Unreachability Detection.

####### BOOLEAN 类型参数

######## 1. TcpIpNdpNeighborUnreachabilityDetectionEnabled

- **UUID**: `aa7cc7f9-c894-4273-9873-8699c1b1e526`
- **参数名**: `TcpIpNdpNeighborUnreachabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Neighbor Unreachability Detection is used to remove unused entries from the neighbor cache. This feature is a basic feature of NDP and should be turned on.

######## 2. TcpIpNdpPacketQueueEnabled

- **UUID**: `5b480a6d-7885-4940-ac6b-bc573c5c8943`
- **参数名**: `TcpIpNdpPacketQueueEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of a NDP Packet Queue according to IETF RFC 4861, section 7.2.2.

######## 3. TcpIpNdpRandomReachableTimeEnabled

- **UUID**: `dae601b8-5cfc-4dd4-99bb-c6eae1c5aa90`
- **参数名**: `TcpIpNdpRandomReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the value of ReachableTime will be multiplied with a random value between MIN_RANDOM_FACTOR and MAX_RANDOM_FACTOR in order to prevent multiple nodes from transmitting at exactly the same time

######## 4. TcpIpNdpInverseNaEnabled

- **UUID**: `8c81e7cf-ab55-47a2-ab38-27fdda22df4b`
- **参数名**: `TcpIpNdpInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are processed or silently discarded.
This also enables the API IpV6_Ndp_SendInverseSolicitation().

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled no Inverse Neighbor Solicitations can be sent and received Inverse Neighbor Advertisements will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######## 5. TcpIpNdpInverseNsEnabled

- **UUID**: `ad52eedc-11a4-4e4a-ad55-b82d98ba116c`
- **参数名**: `TcpIpNdpInverseNsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether Inverse Neighbor Advertisements are sent in response to received Inverse Neighbor Solicitations.

Use "User Callback Configuration" to configure a callback function that handles received Address Lists.

If disabled received Inverse Neighbor Solicitations will be silently ignored.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

######## 6. TcpIpNdpNeighborCacheUpdateByInverseNaEnabled

- **UUID**: `752b17eb-edf2-4c01-b21e-70732a4556c5`
- **参数名**: `TcpIpNdpNeighborCacheUpdateByInverseNaEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the Neighbor Cache will be updated with information from received Inverse Neighbor Advertisements.

[RFC3122 4.2.2 Processing Inverse Neighbor Advertisement Messages]

####### FLOAT 类型参数

######## 1. TcpIpNdpDefaultReachableTime

- **UUID**: `0b691f1a-ffb8-4bb3-a985-6dd9cb517d7e`
- **参数名**: `TcpIpNdpDefaultReachableTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..120]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configuration of the ReachableTime (s) specified in [RFC4861 6.3.2. Host Variables].

######## 2. TcpIpNdpDefaultRetransTimer

- **UUID**: `0e7c1a2a-d5a8-4861-9502-7ec78a4f7004`
- **参数名**: `TcpIpNdpDefaultRetransTimer`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Configures the default value (s) for the RetransTimer variable specified in [RFC4861 6.3.2. Host Variables].

######## 3. TcpIpNdpDelayFirstProbeTime

- **UUID**: `4415dfcf-ca74-4e38-bb2b-f299de4c1a07`
- **参数名**: `TcpIpNdpDelayFirstProbeTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Delay before sending the first NUD probe in (s).

##### 26. TcpIpNdpPrefixRouterDiscoveryConfig

**容器属性**:

- **UUID**: `d4f8ca7e-57f3-41ca-adb8-e310706bbb1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpPrefixRouterDiscoveryConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for NDP Prefix and Router Discovery.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpNdpDefaultRouterListSize

- **UUID**: `038358c8-5751-461d-bc16-4968fbae9fd3`
- **参数名**: `TcpIpNdpDefaultRouterListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [2..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of default router entries.

######## 2. TcpIpNdpDestinationCacheSize

- **UUID**: `7e4351eb-50b0-4f79-8cf5-875c3b0920cc`
- **参数名**: `TcpIpNdpDestinationCacheSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the destination cache.

######## 3. TcpIpNdpMaxRtrSolicitations

- **UUID**: `68f10eb3-b089-4b73-85ca-7dc45ecdb43f`
- **参数名**: `TcpIpNdpMaxRtrSolicitations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of Router Solicitations that will be sent before the first Router Advertisement has been received.

######## 4. TcpIpNdpPrefixListSize

- **UUID**: `f2fb15a1-12db-408b-b3af-986ee1ba55a3`
- **参数名**: `TcpIpNdpPrefixListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of entries in the on-link prefix list.

####### BOOLEAN 类型参数

######## 1. TcpIpNdpDynamicHopLimitEnabled

- **UUID**: `dba1de79-d34f-4a46-856d-55de58f15b2d`
- **参数名**: `TcpIpNdpDynamicHopLimitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default hop limit may be reconfigured based on received Router Advertisements.

######## 2. TcpIpNdpDynamicMtuEnabled

- **UUID**: `2112e1c0-6998-4d65-a691-5b0528648b4f`
- **参数名**: `TcpIpNdpDynamicMtuEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Allow dynamic reconfiguration of link MTU via Router Advertisements.

######## 3. TcpIpNdpDynamicReachableTimeEnabled

- **UUID**: `92b93b2c-9e22-4dfd-8549-b14ffc0b7151`
- **参数名**: `TcpIpNdpDynamicReachableTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Reachable Time value may be reconfigured based on received Router Advertisements.

######## 4. TcpIpNdpDynamicRetransTimeEnabled

- **UUID**: `3024653e-6fa5-4670-8957-ab2d567ae9d7`
- **参数名**: `TcpIpNdpDynamicRetransTimeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the default Retransmit Timer value may be reconfigured based on received Router Advertisements.

######## 5. TcpIpNdpRndRtrSolicitationDelayEnabled

- **UUID**: `44bf4182-733b-4bbf-9a1c-9b7e4fa911d5`
- **参数名**: `TcpIpNdpRndRtrSolicitationDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled the first router solicitation will be delayed randomly from [0...MAX_RTR_SOLICITATION_DELAY]. Otherwise the first router solicitation will be sent after exactly MAX_RTR_SOLICITATION_DELAY milliseconds.

####### FLOAT 类型参数

######## 1. TcpIpNdpMaxRtrSolicitationDelay

- **UUID**: `f4956d66-3569-432c-be99-392231d54cda`
- **参数名**: `TcpIpNdpMaxRtrSolicitationDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum delay before the first Router Solicitation will be sent after interface initialization in (s).

######## 2. TcpIpNdpRtrSolicitationInterval

- **UUID**: `96d7e9d6-ee3e-4ce6-aa79-ff4607b07c36`
- **参数名**: `TcpIpNdpRtrSolicitationInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0.001..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Interval between consecutive Router Solicitations in (s).

##### 27. TcpIpNdpSlaacConfig

**容器属性**:

- **UUID**: `90d9871b-fc6b-4427-8819-7b24868d4fa4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNdpSlaacConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters for StateLess Address AutoConfiguration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpNdpSlaacDadNumberOfTransmissions

- **UUID**: `405e7fe8-66bf-4f88-baf7-63e6f560cf3b`
- **参数名**: `TcpIpNdpSlaacDadNumberOfTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of Neighbor Solicitations that have to be unanswered in order to set an autoconfigurated address to PREFERRED (usable) state.

####### BOOLEAN 类型参数

######## 1. TcpIpNdpSlaacDelayEnabled

- **UUID**: `4f1b0629-037e-4c35-b798-41ebeac82379`
- **参数名**: `TcpIpNdpSlaacDelayEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If enabled transmission of the first DAD Neighbor Solicitation will be delayed by a random value from [0...MAX_DAD_DELAY].

######## 2. TcpIpNdpSlaacOptimisticDadEnabled

- **UUID**: `2395a7d0-5677-4844-b4c6-c74a423ac6d4`
- **参数名**: `TcpIpNdpSlaacOptimisticDadEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enable Optimistic Duplicate Address Detection (DAD) according to RFC4429.

####### FLOAT 类型参数

######## 1. TcpIpNdpSlaacDadRetransmissionDelay

- **UUID**: `be24e378-7ad5-43ac-91a7-7bb6cf7b9ba5`
- **参数名**: `TcpIpNdpSlaacDadRetransmissionDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the maximum value for the address configuration delay (s).

######## 2. TcpIpNdpSlaacMinLifetime

- **UUID**: `b4af1aed-70df-4f32-a0b8-e7e4ca538508`
- **参数名**: `TcpIpNdpSlaacMinLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [10..120000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum valid Lifetime for addresses configured via Stateless Address Autoconfiguration.

[RFC4862 5.5.3. e]

RFC Default: 7200sec (2hrs)

######## 3. TcpIpNdpSlaacMaxDelay

- **UUID**: `5c3659c3-d82d-4c21-a67a-80160b15aba4`
- **参数名**: `TcpIpNdpSlaacMaxDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum value for the address configuration delay.

According to [RFC4861 5.4.2. Sending Neighbor Solicitation Messages] this value should be the same as MAX_RTR_SOLICITATION_DELAY.

RFC Default: "MAX_RTR_SOLICITATION_DELAY" = 1000 milliseconds

##### 28. TcpIpIpV6MldConfig

**容器属性**:

- **UUID**: `1753a324-ce21-4c2b-9384-c864dc1fda18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6MldConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Multicast Listener Discovery Version 2 (MLDv2) for IPv6.

See [RFC3810 Multicast Listener Discovery Version 2 (MLDv2) for IPv6]

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpMldIfStatePoolSize

- **UUID**: `a887b3ac-c946-42b9-b5ba-83088808ab03`
- **参数名**: `TcpIpMldIfStatePoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast addresses the IpV6 instance can listen to.

######## 2. TcpIpMldSrcAddrPoolSize

- **UUID**: `0b3c6e70-b5e7-4562-a7bd-063bb8328423`
- **参数名**: `TcpIpMldSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of source addresses that can be stored for all socket-based multicast memberships.

If multicast packets shall only be received if they have been sent from specific source addresses each of these addresses requires an entry in this pool.

######## 3. TcpIpMldSocketMembershipPoolSize

- **UUID**: `8eb3ca21-009e-49b3-af13-0c324a07a77d`
- **参数名**: `TcpIpMldSocketMembershipPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of multicast memberships that can be managed via the IpV6_MulticastListen() API. All sockets share the same membership pool. Each multicast address can apper at most once for each socket.

Maximum: IpV6MldIfStatePoolSize * number of sockets (all socket are member of all multicast groups)
Minimum: IpV6MldIfStatePoolSize * 1 (exactly one socket is member of each multicast address group)

######## 4. TcpIpMldIfStateSrcAddrPoolSize

- **UUID**: `a7578eb7-1626-4371-b385-c4d2de78446e`
- **参数名**: `TcpIpMldIfStateSrcAddrPoolSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `16`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the total number of all source addresses for all multicast addresses.

This value may be less than IpV6MldSrcAddrPoolSize if multiple sockets only need multicast packets from the same source addresses.

######## 5. TcpIpMldRobustness

- **UUID**: `3a24a09e-4b30-42a5-883f-877b90be1ca4`
- **参数名**: `TcpIpMldRobustness`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the [Robustness Variable] which is defined in [RFC3810 9.1. Robustness Variable].

"MLD is robust to [Robustness Variable] - 1 packet losses. The value of the Robustness Variable MUST NOT be zero, and SHOULD NOT be one. Default value: 2."

######## 6. TcpIpMldMaxReportMsgSize

- **UUID**: `b7abc977-d3f0-4426-914f-1cef4ffefc5a`
- **参数名**: `TcpIpMldMaxReportMsgSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1280`
- **取值范围**: [76..1500]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum size of a MLDv2 Report message inclusive the IPv6 header (40 bytes) and the Hop-by-Hop header (8 bytes).
This value directly depends on the Ethernet Tx buffer size. (No extra buffer will be allocated.)

####### FLOAT 类型参数

######## 1. TcpIpMldV1QuerierPresentTimeout

- **UUID**: `4565fd23-af62-4d5c-a652-ff64c87b85a6`
- **参数名**: `TcpIpMldV1QuerierPresentTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5000`
- **取值范围**: [1..600000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the value of the "Older Version Querier Present Timeout" Variable.

See [RFC3810 9.12. Older Version Querier Present Timeout]

"This value MUST be ([Robustness Variable] times ([Query Interval]) plus (one half of [Query Response Interval])."

######## 2. TcpIpMldMinUnsolicitedReportInt

- **UUID**: `031f0bde-762d-4719-9434-73d504aa287f`
- **参数名**: `TcpIpMldMinUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound for the randomized Unsolicited Report Interval.

If this value equals IpV6MldMaxUnsolicitedReportInt the interval will be fixed.

RFC Default: 0

See: IpV6MldMaxUnsolicitedReportInt

######## 3. TcpIpMldMaxUnsolicitedReportInt

- **UUID**: `e2a3d82e-0340-4455-9452-512cb590e300`
- **参数名**: `TcpIpMldMaxUnsolicitedReportInt`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1000`
- **取值范围**: [0..100000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the randomized Unsolicited Report Interval.

"The Unsolicited Report Interval is the time between repetitions of a node's initial report of interest in a multicast address." [RFC3810 9.11. Unsolicited Report Interval]

RFC Default: 1 second.

"To cover the possibility of the State Change Report being missed by one or more multicast routers, [Robustness Variable] - 1 retransmissions are scheduled, through a Retransmission Timer, at intervals chosen at random from the range (0, [Unsolicited Report Interval])." [RFC3810 6.1. Action on Change of Per-Interface State]

##### 29. TcpIpIpV6PrivExtConfig

**容器属性**:

- **UUID**: `0acaae98-4d88-463e-bdd7-5b0db9f7e45c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6PrivExtConfig`
- **多重性**: [0..1]

**容器描述**:

This container includes configuration parameters for the Privacy Extensions for Stateless Address Autoconfiguration in IPv6.

See [RFC4941 Privacy Extensions for Stateless Address Autoconfiguration in IPv6]

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpPrivExtTempIdGenRetries

- **UUID**: `00bb35ee-e901-44d6-b352-9567a528fece`
- **参数名**: `TcpIpPrivExtTempIdGenRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of times the node shall retry to generate an unique interface identifier for a temporary address.

If an unique identifier could not be generated after the specified number of retries, there will be no temporary address available.

RFC Default: 3
[RFC4941 5. Defined Constants]
[RFC4941 3.3. Generating Temporary Addresses / 7.]

######## 2. TcpIpPrivExtMaxTempAddrs

- **UUID**: `f4dbe358-6c0e-4576-8494-0784b66d3ab0`
- **参数名**: `TcpIpPrivExtMaxTempAddrs`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of temporary addresses that can be configured at the same time.

This should be at least 2 times the number of golbal prefixes advertised by routers.

####### BOOLEAN 类型参数

######## 1. TcpIpPrivExtUseOnLinkPrefixes

- **UUID**: `3f0fe9a1-5685-4d71-951f-058117c55aba`
- **参数名**: `TcpIpPrivExtUseOnLinkPrefixes`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will generate temporary addresses for prefixes marked as on-link in received Router Advertisements. Normally temporary addresses are only created for prefixes that are not marked as on-link.

####### FLOAT 类型参数

######## 1. TcpIpPrivExtTempValidLifetime

- **UUID**: `5cbf1a31-38db-4659-8366-325c0fe6d6c1`
- **参数名**: `TcpIpPrivExtTempValidLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `604800`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is valid.

RFC Default: 604800s (1 week)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

######## 2. TcpIpPrivExtTempPreferredLifetime

- **UUID**: `95293de4-1964-4a6b-a546-82104ff7aaf7`
- **参数名**: `TcpIpPrivExtTempPreferredLifetime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `86400`
- **取值范围**: [0..4294967]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum time a temporary address is preferred.

RFC Default: 86400s (1 day)
[RFC4941 5. Defined Constants]

[RFC4941 3.3. Generating Temporary Addresses / 1.]

######## 3. TcpIpPrivExtRegenAdvance

- **UUID**: `932d705f-7ca5-4ac1-a253-d5ba7bd13f84`
- **参数名**: `TcpIpPrivExtRegenAdvance`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A new temporary addresses is generated RegenAdvance time units before its predecessor gets deprecated.

RFC Default: 5s
[RFC4941 5. Defined Constants]

"To ensure that a preferred temporary address is always available, a new temporary address SHOULD be regenerated slightly before its predecessor is deprecated. This is to allow sufficient time to avoid race conditions in the case where generating a new temporary address is not instantaneous, such as when duplicate address detection must be run. The node SHOULD start the address regeneration process REGEN_ADVANCE time units before a temporary address would actually be deprecated."
[RFC4941 3.4. Expiration of Temporary Addresses]

######## 4. TcpIpPrivExtMaxDesyncFactor

- **UUID**: `0b3a3466-d2ee-49d1-96e3-6fcb8d21ec35`
- **参数名**: `TcpIpPrivExtMaxDesyncFactor`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `600`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound for the random value DESYNC_FACTOR.

RFC Default: 600s (10 minutes)
[RFC4941 5. Defined Constants]

"The value DESYNC_FACTOR is a random value (different for each client) that ensures that clients don't synchronize with each other and generate new addresses at exactly thesame time."
[RFC4941 3.5. Regeneration of Randomized Interface Identifiers]

##### 30. TcpIpLocalAddr

**容器属性**:

- **UUID**: `ef12f5ca-593f-4f49-a4f3-244a2800e58c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpLocalAddr`
- **多重性**: [1..infinite]

**容器描述**:

Specifies the local IP (Internet Protocol) addresses used for IP communication.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpAddrId

- **UUID**: `67a403fe-2f00-4519-8e5b-379d56bd44ed`
- **参数名**: `TcpIpAddrId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: IP address table identifier assigned by TCP/IP stack.

####### BOOLEAN 类型参数

######## 1. TcpIpIpAddrReceiveAllNotConfiguredMulticasts

- **UUID**: `4fb9b00e-4c71-4f97-8bdc-9949cf83e0bc`
- **参数名**: `TcpIpIpAddrReceiveAllNotConfiguredMulticasts`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether an address of type "AutoSelect_Broadcast" shall also be used to receive multicasts that have not been configured individually by addresses of type "Multicast".

Note: If this parameter is set, the IPv4 will configure the EthIf to accept all multicast packets on the corresponsing controller.

This parameter is only valid for an "AutoSelect_Broadcast" address.

####### ENUMERATION 类型参数

######## 1. TcpIpAddressType

- **UUID**: `189afa14-e5b0-422c-a75d-5ca1931f82c5`
- **参数名**: `TcpIpAddressType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_MULTICAST` (来源: AUTOSAR_ECUC)
  - `TCPIP_UNICAST` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV4_BROADCAST` (来源: Vector Informatik)
- **描述**: Address type.

######## 2. TcpIpDomainType

- **UUID**: `a73ae771-25bc-45c2-a02a-e2a2bb7c03d4`
- **参数名**: `TcpIpDomainType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AF_INET` (来源: AUTOSAR_ECUC)
  - `TCPIP_AF_INET6` (来源: AUTOSAR_ECUC)
- **描述**: Address family.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpCtrlRef

- **UUID**: `ed62a943-284f-469c-b777-22bf770e733f`
- **引用名**: `TcpIpCtrlRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `TcpIpCtrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a TcpIpCtrl specifying the EthIf Controller where the IP address shall be assigned and DEM errors that shall be reported in case of an error on this controller.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. TcpIpAddrAssignment

**容器属性**:

- **UUID**: `8a900823-fc2e-4026-8b31-b66af24a31ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAddrAssignment`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies the assignment policy for the IP address.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpAssignmentPriority

- **UUID**: `66ec827e-8e41-446a-b7d6-b649b6bc0f91`
- **参数名**: `TcpIpAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority of assignment (1 is highest). If a new address from an assignment method with a higher priority is available, it overwrites the IP address previously assigned by an assignment method with a lower priority.

######### ENUMERATION 类型参数

########## 1. TcpIpAssignmentLifetime

- **UUID**: `3cdbb6d1-db4a-4a6b-860c-0073d9c5ae3c`
- **参数名**: `TcpIpAssignmentLifetime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TCPIP_FORGET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_FORGET` (来源: AUTOSAR_ECUC)
  - `TCPIP_STORE` (来源: AUTOSAR_ECUC)
- **描述**: Defines the lifetime of a dynamically fetched IP address.

########## 2. TcpIpAssignmentMethod

- **UUID**: `257a8813-f676-4382-a53d-1172d38d5040`
- **参数名**: `TcpIpAssignmentMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_DHCP` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV6_ROUTER` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL_DOIP` (来源: AUTOSAR_ECUC)
  - `TCPIP_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Method of address assignment

########## 3. TcpIpAssignmentTrigger

- **UUID**: `9286b86a-91cf-4520-b9d2-c73af6504f7f`
- **参数名**: `TcpIpAssignmentTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AUTOMATIC` (来源: AUTOSAR_ECUC)
  - `TCPIP_MANUAL` (来源: AUTOSAR_ECUC)
- **描述**: Trigger of address assignment.

####### 2. TcpIpStaticIpAddressConfig

**容器属性**:

- **UUID**: `8d6861de-7c37-4128-8e83-97af7acb2387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticIpAddressConfig`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies a static IP address including directly related parameters.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpNetmask

- **UUID**: `a6bc4b11-58fc-4968-9d60-324b5954ebfa`
- **参数名**: `TcpIpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

######### BOOLEAN 类型参数

########## 1. TcpIpRequestIpAddrAssignmentEnabled

- **UUID**: `4f690c9f-ec8c-4cfb-84fd-80be392391ed`
- **参数名**: `TcpIpRequestIpAddrAssignmentEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this ip address can be changed during runtime via the TcpIp_RequestIpAddrAssignment() API.

######### STRING 类型参数

########## 1. TcpIpDefaultRouter

- **UUID**: `e9069409-5fee-4e28-a2d8-c191e558b754`
- **参数名**: `TcpIpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway)

########## 2. TcpIpStaticIpAddress

- **UUID**: `3b8a3709-2c5c-494d-b0a1-7172a6742b4a`
- **参数名**: `TcpIpStaticIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Static IP Address.

##### 31. TcpIpAddrAssignment

**容器属性**:

- **UUID**: `8a900823-fc2e-4026-8b31-b66af24a31ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpAddrAssignment`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies the assignment policy for the IP address.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpAssignmentPriority

- **UUID**: `66ec827e-8e41-446a-b7d6-b649b6bc0f91`
- **参数名**: `TcpIpAssignmentPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..3]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Priority of assignment (1 is highest). If a new address from an assignment method with a higher priority is available, it overwrites the IP address previously assigned by an assignment method with a lower priority.

####### ENUMERATION 类型参数

######## 1. TcpIpAssignmentLifetime

- **UUID**: `3cdbb6d1-db4a-4a6b-860c-0073d9c5ae3c`
- **参数名**: `TcpIpAssignmentLifetime`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `TCPIP_FORGET`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_FORGET` (来源: AUTOSAR_ECUC)
  - `TCPIP_STORE` (来源: AUTOSAR_ECUC)
- **描述**: Defines the lifetime of a dynamically fetched IP address.

######## 2. TcpIpAssignmentMethod

- **UUID**: `257a8813-f676-4382-a53d-1172d38d5040`
- **参数名**: `TcpIpAssignmentMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_DHCP` (来源: AUTOSAR_ECUC)
  - `TCPIP_IPV6_ROUTER` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL` (来源: AUTOSAR_ECUC)
  - `TCPIP_LINKLOCAL_DOIP` (来源: AUTOSAR_ECUC)
  - `TCPIP_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Method of address assignment

######## 3. TcpIpAssignmentTrigger

- **UUID**: `9286b86a-91cf-4520-b9d2-c73af6504f7f`
- **参数名**: `TcpIpAssignmentTrigger`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TCPIP_AUTOMATIC` (来源: AUTOSAR_ECUC)
  - `TCPIP_MANUAL` (来源: AUTOSAR_ECUC)
- **描述**: Trigger of address assignment.

##### 32. TcpIpStaticIpAddressConfig

**容器属性**:

- **UUID**: `8d6861de-7c37-4128-8e83-97af7acb2387`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpStaticIpAddressConfig`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpLocalAddr and specifies a static IP address including directly related parameters.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpNetmask

- **UUID**: `a6bc4b11-58fc-4968-9d60-324b5954ebfa`
- **参数名**: `TcpIpNetmask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..128]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Network mask of IPv4 address or address prefix of IPv6 address in CIDR Notation, i.e. decimal value between 0 and 32 (IPv4) or 0 and 128 (IPv6) that describes the number of significant bits defining the network number or prefix of an IP address.

####### BOOLEAN 类型参数

######## 1. TcpIpRequestIpAddrAssignmentEnabled

- **UUID**: `4f690c9f-ec8c-4cfb-84fd-80be392391ed`
- **参数名**: `TcpIpRequestIpAddrAssignmentEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if this ip address can be changed during runtime via the TcpIp_RequestIpAddrAssignment() API.

####### STRING 类型参数

######## 1. TcpIpDefaultRouter

- **UUID**: `e9069409-5fee-4e28-a2d8-c191e558b754`
- **参数名**: `TcpIpDefaultRouter`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: IP address of default router (gateway)

######## 2. TcpIpStaticIpAddress

- **UUID**: `3b8a3709-2c5c-494d-b0a1-7172a6742b4a`
- **参数名**: `TcpIpStaticIpAddress`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Static IP Address.

##### 33. TcpIpNvmBlock

**容器属性**:

- **UUID**: `c2bb41c1-4935-4e1b-acf0-3f595c89ea1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpNvmBlock`
- **多重性**: [0..1]

**容器描述**:

Configuration of optional usage of Nvm in case the TcpIp module requires non volatile memory in the Ecu to store information (e.g. IP Address received via DHCP and shall be stored).

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. TcpIpNvmBlockDescriptorRef

- **UUID**: `0a0315fb-fe9b-4da2-9061-5621026cea95`
- **引用名**: `TcpIpNvmBlockDescriptorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `NvMBlockDescriptor`
- **完整路径**: `/AUTOSAR/EcucDefs/NvM/NvMBlockDescriptor`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to the Nvm block description in the Nvm module configuration.

##### 34. TcpIpPhysAddrConfig

**容器属性**:

- **UUID**: `8bbfae3c-9972-402f-be2e-de6fa989972d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the physical address configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpPhysAddrChgHandler

**容器属性**:

- **UUID**: `4f251a1a-c10a-44b0-9224-bba3315cb450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrChgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpPhysAddrConfig and

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. TcpIpPhysAddrChgHandlerHeaderFileName

- **UUID**: `89044b9e-f193-4d7b-9400-c91fa361e7cc`
- **参数名**: `TcpIpPhysAddrChgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the physical address change handler function.

######### FUNCTION-NAME 类型参数

########## 1. TcpIpPhysAddrChgHandlerName

- **UUID**: `db36425a-74a7-4c3e-9689-670d428eec1e`
- **参数名**: `TcpIpPhysAddrChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the physical address change function <Up>_PhysAddrTableChg.

##### 35. TcpIpPhysAddrChgHandler

**容器属性**:

- **UUID**: `4f251a1a-c10a-44b0-9224-bba3315cb450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpPhysAddrChgHandler`
- **多重性**: [0..1]

**容器描述**:

This container is a subcontainer of TcpIpPhysAddrConfig and

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. TcpIpPhysAddrChgHandlerHeaderFileName

- **UUID**: `89044b9e-f193-4d7b-9400-c91fa361e7cc`
- **参数名**: `TcpIpPhysAddrChgHandlerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: This parameter specifies the name of the header file containing the definition of the physical address change handler function.

####### FUNCTION-NAME 类型参数

######## 1. TcpIpPhysAddrChgHandlerName

- **UUID**: `db36425a-74a7-4c3e-9689-670d428eec1e`
- **参数名**: `TcpIpPhysAddrChgHandlerName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the physical address change function <Up>_PhysAddrTableChg.

##### 36. TcpIpSocketOwnerConfig

**容器属性**:

- **UUID**: `99b3e3b9-ff4a-47ac-9850-604c41875ccd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwnerConfig`
- **多重性**: [1..1]

**容器描述**:

Specifies the upper layer modules of TcpIp using the socket API.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpSocketOwner

**容器属性**:

- **UUID**: `070f0e68-8e85-4d70-b307-3bd24911fb0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwner`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpSocketOwnerConfig and specifies an upper layer of TcpIp that uses the socket API.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpSocketOwnerId

- **UUID**: `db654543-ffed-44ce-808f-292703b2c45a`
- **参数名**: `TcpIpSocketOwnerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ID of the socket user.
(auto calculated)

########## 2. TcpIpSocketOwnerTcpListenSocketMax

- **UUID**: `298c361b-29ce-4c1a-899f-76dc9a25463f`
- **参数名**: `TcpIpSocketOwnerTcpListenSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of TCP listen sockets this socket owner will use simultaneously

######### STRING 类型参数

########## 1. TcpIpSocketOwnerCopyTxDataName

- **UUID**: `31e19519-a2af-4071-8f98-9972932efd76`
- **参数名**: `TcpIpSocketOwnerCopyTxDataName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_CopyTxData> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 2. TcpIpSocketOwnerHeaderFileName

- **UUID**: `fd702bd9-4515-4c7e-9cbf-e8ca95106f95`
- **参数名**: `TcpIpSocketOwnerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the name of the header file containing the definition of the TcpIpSocketOwner module functions. The header file name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 3. TcpIpSocketOwnerLocalIpAddrAssignmentChgName

- **UUID**: `db9ec507-2c81-4399-9f7f-511e0a9801f7`
- **参数名**: `TcpIpSocketOwnerLocalIpAddrAssignmentChgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_LocalIpAddrAssignmentChg> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 4. TcpIpSocketOwnerRxIndicationName

- **UUID**: `18f65b8d-9e74-4011-bf73-e2585e57113f`
- **参数名**: `TcpIpSocketOwnerRxIndicationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_RxIndication> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 5. TcpIpSocketOwnerTcpAcceptedName

- **UUID**: `d3202b67-8321-46cf-832a-12ddcce6eaf6`
- **参数名**: `TcpIpSocketOwnerTcpAcceptedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpAccepted> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 6. TcpIpSocketOwnerTcpConnectedName

- **UUID**: `ea3021c1-8c38-4af8-b85a-f9bcbcabf73c`
- **参数名**: `TcpIpSocketOwnerTcpConnectedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpConnected> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 7. TcpIpSocketOwnerTxConfirmationName

- **UUID**: `c43a4af8-4317-45e1-9350-d618f4a01d9a`
- **参数名**: `TcpIpSocketOwnerTxConfirmationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TxConfirmation> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

########## 8. TcpIpSocketOwnerTcpIpEventName

- **UUID**: `877fae0f-7cf2-4285-b5fb-e784076dc319`
- **参数名**: `TcpIpSocketOwnerTcpIpEventName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the function called for a TCP/IP event on related sockets.The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######### ENUMERATION 类型参数

########## 1. TcpIpSocketOwnerUpperLayerType

- **UUID**: `8227b25a-6ce0-403f-9cc5-8274e6fe05d7`
- **参数名**: `TcpIpSocketOwnerUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `SOAD` (来源: AUTOSAR_ECUC)
  - `DHCPV4_SERVER` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of the upper layer module.

##### 37. TcpIpSocketOwner

**容器属性**:

- **UUID**: `070f0e68-8e85-4d70-b307-3bd24911fb0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpSocketOwner`
- **多重性**: [1..infinite]

**容器描述**:

This container is a subcontainer of TcpIpSocketOwnerConfig and specifies an upper layer of TcpIp that uses the socket API.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpSocketOwnerId

- **UUID**: `db654543-ffed-44ce-808f-292703b2c45a`
- **参数名**: `TcpIpSocketOwnerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the ID of the socket user.
(auto calculated)

######## 2. TcpIpSocketOwnerTcpListenSocketMax

- **UUID**: `298c361b-29ce-4c1a-899f-76dc9a25463f`
- **参数名**: `TcpIpSocketOwnerTcpListenSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of TCP listen sockets this socket owner will use simultaneously

####### STRING 类型参数

######## 1. TcpIpSocketOwnerCopyTxDataName

- **UUID**: `31e19519-a2af-4071-8f98-9972932efd76`
- **参数名**: `TcpIpSocketOwnerCopyTxDataName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_CopyTxData> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 2. TcpIpSocketOwnerHeaderFileName

- **UUID**: `fd702bd9-4515-4c7e-9cbf-e8ca95106f95`
- **参数名**: `TcpIpSocketOwnerHeaderFileName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter specifies the name of the header file containing the definition of the TcpIpSocketOwner module functions. The header file name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 3. TcpIpSocketOwnerLocalIpAddrAssignmentChgName

- **UUID**: `db9ec507-2c81-4399-9f7f-511e0a9801f7`
- **参数名**: `TcpIpSocketOwnerLocalIpAddrAssignmentChgName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_LocalIpAddrAssignmentChg> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 4. TcpIpSocketOwnerRxIndicationName

- **UUID**: `18f65b8d-9e74-4011-bf73-e2585e57113f`
- **参数名**: `TcpIpSocketOwnerRxIndicationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_RxIndication> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 5. TcpIpSocketOwnerTcpAcceptedName

- **UUID**: `d3202b67-8321-46cf-832a-12ddcce6eaf6`
- **参数名**: `TcpIpSocketOwnerTcpAcceptedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpAccepted> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 6. TcpIpSocketOwnerTcpConnectedName

- **UUID**: `ea3021c1-8c38-4af8-b85a-f9bcbcabf73c`
- **参数名**: `TcpIpSocketOwnerTcpConnectedName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TcpConnected> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 7. TcpIpSocketOwnerTxConfirmationName

- **UUID**: `c43a4af8-4317-45e1-9350-d618f4a01d9a`
- **参数名**: `TcpIpSocketOwnerTxConfirmationName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the name of the <Up_TxConfirmation> function of the TcpIpSocketOwner module. The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

######## 8. TcpIpSocketOwnerTcpIpEventName

- **UUID**: `877fae0f-7cf2-4285-b5fb-e784076dc319`
- **参数名**: `TcpIpSocketOwnerTcpIpEventName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the function called for a TCP/IP event on related sockets.The function name shall only be configurable if TcpIpSocketOwnerUpperLayerType is set to CDD.

####### ENUMERATION 类型参数

######## 1. TcpIpSocketOwnerUpperLayerType

- **UUID**: `8227b25a-6ce0-403f-9cc5-8274e6fe05d7`
- **参数名**: `TcpIpSocketOwnerUpperLayerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `SOAD` (来源: AUTOSAR_ECUC)
  - `DHCPV4_SERVER` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of the upper layer module.

##### 38. TcpIpTcpConfig

**容器属性**:

- **UUID**: `cf13f3bf-480e-4446-882f-7ca705d7e778`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpConfig`
- **多重性**: [0..1]

**容器描述**:

Specifies the configuration parameters of the TCP (Transmission Control Protocol) sub-module.

###### 参数配置

此容器包含 **33** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpTcpKeepAliveProbesMax

- **UUID**: `e46e8e8c-03a0-4351-95b5-6e439d335c97`
- **参数名**: `TcpIpTcpKeepAliveProbesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP Keep Alive is retransmitted before the connection is closed.

######## 2. TcpIpTcpMaxRtx

- **UUID**: `e59720fc-d0bf-4999-bbdd-416170936ec0`
- **参数名**: `TcpIpTcpMaxRtx`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP segment is retransmitted before the TCP connection is closed. This parameter is only valid if TcpIpTcpRetransmissionTimeout is configured.

######## 3. TcpIpTcpReceiveWindowMax

- **UUID**: `cf0da76e-545f-4ce4-b55b-02ac907f9720`
- **参数名**: `TcpIpTcpReceiveWindowMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default value of maximum receive window in bytes.

######## 4. TcpIpTcpSynMaxRtx

- **UUID**: `e67e8d63-0387-42a3-b930-e03c65021b6d`
- **参数名**: `TcpIpTcpSynMaxRtx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `255`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of times that a TCP SYN is retransmitted.

######## 5. TcpIpTcpTtl

- **UUID**: `55e70307-5151-4dcf-8e15-b480d1770986`
- **参数名**: `TcpIpTcpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing TCP packets.

######## 6. TcpIpTcpMaxNumOooSegsPerSocket

- **UUID**: `95f52997-c21f-4b88-9388-e72b551789ba`
- **参数名**: `TcpIpTcpMaxNumOooSegsPerSocket`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the maximum number of out of order control elements that can be allocated for one TCP socket during runtime.

RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

######## 7. TcpIpTcpAvgNumOooSegsPerSocket

- **UUID**: `0eb963a8-8b67-4bca-91c0-d1befc3b14dc`
- **参数名**: `TcpIpTcpAvgNumOooSegsPerSocket`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [1..254]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the number of out of order control elements per TCP socket.

The elements are grouped into a pool shared by all TCP sockets.
A TCP socket is allowed to allocate as much elements as specified by 'TcpIpTcpMaxNumOooSegsPerSocket'.

RESTRICTIONS: 'TcpAvgNumOooSegsPerSocket' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

######## 8. TcpIpTcpTxResetQueueSize

- **UUID**: `a4c3705c-875e-41d0-8c45-c4f476d64000`
- **参数名**: `TcpIpTcpTxResetQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [0..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the amount of entries reserved for the Tx Reset Queue.

Note:
The Reset Queue is shared by all TCP Sockets.

######## 9. TcpIpTcpTxRetryQueueSize

- **UUID**: `c048dbcf-ba87-40a6-995e-d379c4f2f9ac`
- **参数名**: `TcpIpTcpTxRetryQueueSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10`
- **取值范围**: [0..127]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the average amount of entries allocated for the Tx Retry Queue of one TCP Socket.

Note:
The Retry Queues are grouped in a pool shared by all TCP Sockets. Therefore a Socket may have less entries available as specified.

####### BOOLEAN 类型参数

######## 1. TcpIpTcpCongestionAvoidanceEnabled

- **UUID**: `fbb74212-5c12-4483-abb4-019016ad3d2a`
- **参数名**: `TcpIpTcpCongestionAvoidanceEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP congestion avoidance algorithm according to IETF RFC 5681.

######## 2. TcpIpTcpFastRecoveryEnabled

- **UUID**: `c157243f-6ad5-418e-92f7-37ed6b060c7d`
- **参数名**: `TcpIpTcpFastRecoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP Fast Recovery according to IETF RFC 5681.

######## 3. TcpIpTcpFastRetransmitEnabled

- **UUID**: `313f0b44-0a1c-4541-8217-79e4fc1ac81e`
- **参数名**: `TcpIpTcpFastRetransmitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP Fast Retransmission according to IETF RFC 5681.

######## 4. TcpIpTcpKeepAliveEnabled

- **UUID**: `232c5c88-2a34-4da7-ad35-740cad99d841`
- **参数名**: `TcpIpTcpKeepAliveEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) TCP Keep Alive Probes according to IETF RFC 1122 chapter 4.2.3.6

######## 5. TcpIpTcpNagleEnabled

- **UUID**: `1f7a5768-fe1b-4c4b-81b0-338cf540cbcc`
- **参数名**: `TcpIpTcpNagleEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Nagle’s algorithm according to IETF RFC 896. If enabled the Nagle’s algorithm is activated per default for all TCP sockets, but can be deactivated via TcpIp_ChangeParameter() API.

######## 6. TcpIpTcpSlowStartEnabled

- **UUID**: `b65d3ad7-a9dd-4a1d-9ab6-99a820b722ce`
- **参数名**: `TcpIpTcpSlowStartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of TCP slow start algorithm according to IETF RFC 5681.

######## 7. TcpIpTcpEnableDiagReadAckSeqNum

- **UUID**: `648a1543-f1c2-4b09-a785-e95cf482c1bf`
- **参数名**: `TcpIpTcpEnableDiagReadAckSeqNum`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable reading of current TCP sequence number and acknowledgement number for a specified socket.

######## 8. TcpIpTcpSackOptionSupport

- **UUID**: `b1ae3760-7dff-4558-93ec-c14ba1f829a8`
- **参数名**: `TcpIpTcpSackOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the TCP option 'selective acknowlagement' is enabled.
[RFC 2018]

RESTRICTIONS: 'TcpSackOptionSupport' is only available, if 'TcpOutOfOrderRxSupport' is set to 'true'.

######## 9. TcpIpTcpUserTimeoutOptionSupport

- **UUID**: `d7170237-f65e-442b-882a-cc5c8e010d35`
- **参数名**: `TcpIpTcpUserTimeoutOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the User Timeout Option of TCP is enabled.

######## 10. TcpIpTcpTimeStampOptionSupport

- **UUID**: `9bdfc8a2-b42b-4b26-8ddc-871fea60607a`
- **参数名**: `TcpIpTcpTimeStampOptionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the Timestamp Option of TCP is enabled.

######## 11. TcpIpTcpOutOfOrderRxSupport

- **UUID**: `fe72aa01-e5dc-4492-bb66-b038c8f6a3e7`
- **参数名**: `TcpIpTcpOutOfOrderRxSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the reception of out of order TCP segments is supported.

####### FLOAT 类型参数

######## 1. TcpIpTcpFinWait2Timeout

- **UUID**: `f47ac90d-f6b7-45bd-9e3d-62e895e359cd`
- **参数名**: `TcpIpTcpFinWait2Timeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] to receive a FIN from the remote node (after this node has initiated connection termination), i.e. maximum time waiting in FINWAIT-2 for a connection termination request from the remote TCP.

######## 2. TcpIpTcpKeepAliveInterval

- **UUID**: `9763d9aa-9ee6-4a34-a63f-1176847a01a7`
- **参数名**: `TcpIpTcpKeepAliveInterval`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the interval in [s] between subsequent keepalive probes.

######## 3. TcpIpTcpKeepAliveTime

- **UUID**: `221739f6-e136-448b-ac38-e6d782db2b07`
- **参数名**: `TcpIpTcpKeepAliveTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `7200`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Specifies the time in [s] between the last data packet sent (simple ACKs are not considered data) and the first keepalive probe. Note: Setting this configuration parameter to a value smaller or equal to the value of TcpIpMainFunctionPeriod results in the transmission of keep alive probes within every MainFunction cycle.

######## 4. TcpIpTcpMsl

- **UUID**: `f9cbef19-c89e-4956-a226-61f33ec7654e`
- **参数名**: `TcpIpTcpMsl`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `120`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum segment lifetime in [s].

######## 5. TcpIpTcpRetransmissionTimeout

- **UUID**: `fd9d758d-c2d8-487f-bd0b-b3d76f04c987`
- **参数名**: `TcpIpTcpRetransmissionTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0.001..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] before an unacknowledged TCP segment is sent again.

######## 6. TcpIpTcpSynReceivedTimeout

- **UUID**: `00286551-808e-403e-aa93-7f79b4153ce1`
- **参数名**: `TcpIpTcpSynReceivedTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timeout in [s] to complete a remotely initiated TCP connection establishment, i.e. maximum time waiting in SYN-RECEIVED for a confirming connection request acknowledgment after having both received and sent a connection request.

######## 7. TcpIpTcpUserTimeoutDef

- **UUID**: `6c7d23b6-e5ce-41ca-bf9f-0b119b979986`
- **参数名**: `TcpIpTcpUserTimeoutDef`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `20`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the default value for User Timeout.
(default: 20s)
(time transmitted data may stay un-acknowlaged)

RESTRICTION: Value of 'TcpUserTimeoutDef' has to be in the range defined by 'TcpUserTimeoutMin' and 'TcpUserTimeoutMax'.

######## 8. TcpIpTcpUserTimeoutMax

- **UUID**: `97fe9a77-ec91-4c59-82ff-ad63abe5d901`
- **参数名**: `TcpIpTcpUserTimeoutMax`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `300`
- **取值范围**: [0..10000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the maximum value for User Timeout.
(default: 300s)

RESTRICTION: Value of 'TcpUserTimeoutMax' has to be greater than 'TcpUserTimeoutMin' and greater than or equal to 'TcpUserTimeoutDef'.

######## 9. TcpIpTcpUserTimeoutMin

- **UUID**: `4074990f-5fd9-4775-937c-7368a2197ef7`
- **参数名**: `TcpIpTcpUserTimeoutMin`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `5`
- **取值范围**: [0..5000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the minimum value for User Timeout.
(default: 5s)
RFC 1122 defines it to 100 seconds (3 minutes for SYN segments).

RESTRICTION: Value of 'TcpUserTimeoutMin' has to be smaller than 'TcpUserTimeoutMax' and smaller than or equal to 'TcpUserTimeoutDef'.

######## 10. TcpIpTcpTxRetryIntMaxTime

- **UUID**: `5e7b53e8-7aa8-4856-a259-f03a647f18f1`
- **参数名**: `TcpIpTcpTxRetryIntMaxTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [10..60]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the upper bound of the time interval, in which the retransmittion of a not acknowledged TCP packet is triggered.

######## 11. TcpIpTcpTxRetryIntMinTime

- **UUID**: `49e579c0-d498-449a-a506-ffeb836de633`
- **参数名**: `TcpIpTcpTxRetryIntMinTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.1..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the lower bound of the time interval, in which the retransmittion of a not acknowledged TCP packet is triggered.

######## 12. TcpIpTcpNagleTimeout

- **UUID**: `86d734b0-dfe6-468f-8cec-273ea4454e57`
- **参数名**: `TcpIpTcpNagleTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the timeout for Nagle algorithm,

Note:
Value must be a multiple of Main Function Period

RESTRICTIONS: 'TcpNagleTimeoutMsec' is only available, if 'TcpEnableNagle' is enabled.

######## 13. TcpIpTcpIdleTimeout

- **UUID**: `5880ffe0-2131-4be8-a4fc-596de5501492`
- **参数名**: `TcpIpTcpIdleTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the TCP idle timeout (must be bigger than MSL timeout)

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpTcpSocketBuffer

**容器属性**:

- **UUID**: `1109a158-037d-4a0d-afbe-dceded4de7aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpSocketBuffer`
- **多重性**: [1..infinite]

**容器描述**:

This container includes the rx and tx buffer configuration of a TCP socket. 
The number of available socket handles will be the sum of all TCP rx and tx buffer configurations and the number of all TCP listen sockets.

Note: rx and tx buffers are not bound to a specific socket handle. 
The buffers are shared between all users and must be allocated to a socket during runtime via the TcpIp_ChangeParameter() API.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpTcpSocketRxBufferSize

- **UUID**: `ad411939-2b30-425f-a1f7-60d953202e96`
- **参数名**: `TcpIpTcpSocketRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a RX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

########## 2. TcpIpTcpSocketTxBufferSize

- **UUID**: `036a1a56-15d7-4b4f-9b0c-81a782c48b2a`
- **参数名**: `TcpIpTcpSocketTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a TX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

##### 39. TcpIpTcpSocketBuffer

**容器属性**:

- **UUID**: `1109a158-037d-4a0d-afbe-dceded4de7aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpTcpSocketBuffer`
- **多重性**: [1..infinite]

**容器描述**:

This container includes the rx and tx buffer configuration of a TCP socket. 
The number of available socket handles will be the sum of all TCP rx and tx buffer configurations and the number of all TCP listen sockets.

Note: rx and tx buffers are not bound to a specific socket handle. 
The buffers are shared between all users and must be allocated to a socket during runtime via the TcpIp_ChangeParameter() API.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpTcpSocketRxBufferSize

- **UUID**: `ad411939-2b30-425f-a1f7-60d953202e96`
- **参数名**: `TcpIpTcpSocketRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a RX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

######## 2. TcpIpTcpSocketTxBufferSize

- **UUID**: `036a1a56-15d7-4b4f-9b0c-81a782c48b2a`
- **参数名**: `TcpIpTcpSocketTxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `512`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the size of a TX buffer segment that can be allocated to a TCP socket handle via the TcpIp_ChangeParameter() API during runtime.

Note: A buffer segment is shared between all TCP sockets but can only be used for one socket at a time. If multiple sockets with the same buffer size shall be used simultaneously, multiple buffer segments of the same size have to be configured.

##### 40. TcpIpUdpConfig

**容器属性**:

- **UUID**: `18648ba8-01de-4125-806b-c826fe615aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpConfig`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Specifies the configuration parameters of the UDP (User Datagram Protocol) sub-module

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpUdpTtl

- **UUID**: `600fcc21-1028-4ed2-8de4-6cca16b1cb48`
- **参数名**: `TcpIpUdpTtl`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Default Time-to-live value of outgoing UDP packets.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. TcpIpUdpTxReqList

**容器属性**:

- **UUID**: `16114d8f-6758-4001-9821-5a0acc0c08a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpTxReqList`
- **多重性**: [0..infinite]

**容器描述**:

This container includes configuration parameters of a UDP TX request list that can be attached to a UDP socket handle via TcpIp_ChangeParameter() during runtime.

A UDP socket only needs a TX request list if a TxConfirmation is required by the upper layer.

Note: A UDP tx request list is shared between all UDP sockets but can only be used for one socket at a time. If multiple sockets with the same request list size shall be used simultaneously, multiple request lists of the same size have to be configured.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpUdpTxReqListSize

- **UUID**: `6b572316-8596-4a09-8d9e-8e2bc755bbc4`
- **参数名**: `TcpIpUdpTxReqListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of entries in the UDP TX request list.

##### 41. TcpIpUdpTxReqList

**容器属性**:

- **UUID**: `16114d8f-6758-4001-9821-5a0acc0c08a0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpUdpTxReqList`
- **多重性**: [0..infinite]

**容器描述**:

This container includes configuration parameters of a UDP TX request list that can be attached to a UDP socket handle via TcpIp_ChangeParameter() during runtime.

A UDP socket only needs a TX request list if a TxConfirmation is required by the upper layer.

Note: A UDP tx request list is shared between all UDP sockets but can only be used for one socket at a time. If multiple sockets with the same request list size shall be used simultaneously, multiple request lists of the same size have to be configured.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpUdpTxReqListSize

- **UUID**: `6b572316-8596-4a09-8d9e-8e2bc755bbc4`
- **参数名**: `TcpIpUdpTxReqListSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of entries in the UDP TX request list.

##### 42. TcpIpGeneral

**容器属性**:

- **UUID**: `6673e254-b33c-4042-8147-65caec2bd8d5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpGeneral`
- **多重性**: [1..1]

**容器描述**:

This container is a subcontainer of TcpIp and specifies the general configuration parameters of the TCP/IP stack.

###### 参数配置

此容器包含 **15** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpBufferMemory

- **UUID**: `b781b6e7-e035-4982-b2d7-d628f6cea806`
- **参数名**: `TcpIpBufferMemory`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Memory size in bytes reserved for TCP/IP buffers.

######## 2. TcpIpTcpSocketMax

- **UUID**: `5052dd39-53ff-4260-9595-af06ff321a82`
- **参数名**: `TcpIpTcpSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of TCP sockets

######## 3. TcpIpUdpSocketMax

- **UUID**: `16aa4ed5-1dfa-481f-af54-ec13ab44acea`
- **参数名**: `TcpIpUdpSocketMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of UDP sockets.

####### BOOLEAN 类型参数

######## 1. TcpIpDevErrorDetect

- **UUID**: `29def85d-ccf9-4ce5-9fd1-71420fbe0af5`
- **参数名**: `TcpIpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If true then TCP/IP will enable the error-reporting to the Development Error Tracer (DET).

######## 2. TcpIpDhcpServerEnabled

- **UUID**: `e31cb094-7dfd-4525-b55a-7c2fd8ec2f30`
- **参数名**: `TcpIpDhcpServerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the DHCPv4 (Dynamic Host Configuration Protocol) Server.

######## 3. TcpIpResetIpAssignmentApi

- **UUID**: `4fe73b9c-64aa-483a-a991-27f3f0a1d19f`
- **参数名**: `TcpIpResetIpAssignmentApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables/disables the API TcpIp_ResetIpAssignment of a DHCP-client.

######## 4. TcpIpTcpEnabled

- **UUID**: `123aba43-d0b3-4161-9b93-a1c34709f253`
- **参数名**: `TcpIpTcpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disabled (FALSE) support of TCP (Transmission Control Protocol).

######## 5. TcpIpUdpEnabled

- **UUID**: `8125010f-be32-40b7-8b88-4a9508d987b8`
- **参数名**: `TcpIpUdpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disabled (FALSE) support of UDP (User Datagram Protocol)

######## 6. TcpIpVersionInfoApi

- **UUID**: `4905db7c-a3a7-42bd-9515-8be12acc66e9`
- **参数名**: `TcpIpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If true the TcpIp_GetVersionInfo API is available.

######## 7. TcpIpDiagExtensionsEnabled

- **UUID**: `c034b5ce-3bc4-4168-b025-3c6d4ba81355`
- **参数名**: `TcpIpDiagExtensionsEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable diagnostic read access to several parameters. For some parameters read access has to be enabled separately.

Read features can be located at TcpIp_General or at the different sub-components.

####### FLOAT 类型参数

######## 1. TcpIpMainFunctionPeriod

- **UUID**: `e8bf6bc1-c28e-48eb-a3f3-4c1a0d7c27eb`
- **参数名**: `TcpIpMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0.0001..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Period of TcpIp_MainFunction in [s].

####### STRING 类型参数

######## 1. TcpIpUserConfigFile

- **UUID**: `c3e602e5-340e-4866-b08b-f7b733420e6d`
- **参数名**: `TcpIpUserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 2. TcpIpRandNoFctIncludeFile

- **UUID**: `d2a005e3-0f86-4538-ab23-342c369180df`
- **参数名**: `TcpIpRandNoFctIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 默认值: `Appl_Rand.h`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the header file holding the declaration of the random number generation function defined in 'TcpIpRandNoFct'.

####### ENUMERATION 类型参数

######## 1. TcpIpScalabilityClass

- **UUID**: `b72e0af6-f289-4eaf-842f-b5377b870ba2`
- **参数名**: `TcpIpScalabilityClass`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SC1`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `SC1` (来源: AUTOSAR_ECUC)
  - `SC2` (来源: AUTOSAR_ECUC)
  - `SC3` (来源: AUTOSAR_ECUC)
- **描述**: In order to customize the TcpIp Stack to the specific needs of the user it can be scaled according to the scalability classes.

####### FUNCTION-NAME 类型参数

######## 1. TcpIpRandNoFct

- **UUID**: `8e2b0fe2-3b9b-4e84-9a87-1605d12b0e2b`
- **参数名**: `TcpIpRandNoFct`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **函数变体**:
  - 默认值: `Appl_Crypto_GetRandNo`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the function called for the random number generation.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. TcpIpIpV4General

**容器属性**:

- **UUID**: `c1ca44c6-906c-422b-bee7-93600afcade7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4General`
- **多重性**: [1..1]

**容器描述**:

This container is a subcontainer of TcpIp and specifies the general configuration parameters of the TCP/IP stack for IPv4

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpLocalAddrIpv4EntriesMax

- **UUID**: `129ee98f-fe2d-4b09-942d-1d7b215073e5`
- **参数名**: `TcpIpLocalAddrIpv4EntriesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of LocalAddr table entries for IPv4.

######### BOOLEAN 类型参数

########## 1. TcpIpArpEnabled

- **UUID**: `9faa203f-6fdc-4b9e-a29a-ed423fe70e2a`
- **参数名**: `TcpIpArpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of ARP (Address Resolution Protocol).

########## 2. TcpIpAutoIpEnabled

- **UUID**: `711cad52-6e74-4cbd-9658-722e3bb6fb8b`
- **参数名**: `TcpIpAutoIpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the Auto-IP (automatic private IP addressing) sub-module.

########## 3. TcpIpDhcpClientEnabled

- **UUID**: `45110993-4b87-429e-9f19-bef9604954fa`
- **参数名**: `TcpIpDhcpClientEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the DHCP (Dynamic Host Configuration Protocol) Client.

########## 4. TcpIpIcmpEnabled

- **UUID**: `6b6fcd2a-09aa-463a-9c29-d3e76b7c3114`
- **参数名**: `TcpIpIcmpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disabled (FALSE) support of ICMP (Internet Control Message Protocol).

########## 5. TcpIpIpV4Enabled

- **UUID**: `6ed21325-4a2e-4a3f-ac20-71da2bd39dba`
- **参数名**: `TcpIpIpV4Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of IPv4 (Internet Protocol version 4).

########## 6. TcpIpPathMtuDiscoveryEnabled

- **UUID**: `876cae05-7a32-4b40-8cf1-bc7420800abf`
- **参数名**: `TcpIpPathMtuDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the discovery of the maximum transmission unit on a path according to IETF RfC 1191.

######### STRING 类型参数

########## 1. TcpIpIpV4UserConfigFile

- **UUID**: `f1f49b49-7ac0-48ac-9cf8-4433b9f19577`
- **参数名**: `TcpIpIpV4UserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpIpV4DefaultCtrl

- **UUID**: `ee6e9521-72d3-47eb-8fca-bb1f0172f660`
- **引用名**: `TcpIpIpV4DefaultCtrl`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV4Ctrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl/TcpIpIpVXCtrl/TcpIpIpV4Ctrl`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the default controller for messages not directed to own subnet(s)

####### 2. TcpIpIpV6General

**容器属性**:

- **UUID**: `0f963339-d6f3-4a29-b8c8-d26a8e21e09a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6General`
- **多重性**: [1..1]

**容器描述**:

This container is a subcontainer of TcpIp and specifies the general configuration parameters of the TCP/IP stack for IPv6.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. TcpIpLocalAddrIpv6EntriesMax

- **UUID**: `8ed02751-16d5-4506-9d6f-c3e7eccbb538`
- **参数名**: `TcpIpLocalAddrIpv6EntriesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of LocalAddr table entries for IPv6.

######### BOOLEAN 类型参数

########## 1. TcpIpDhcpV6ClientEnabled

- **UUID**: `d767476e-8e17-4452-a45b-8b670228026c`
- **参数名**: `TcpIpDhcpV6ClientEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the DHCPv6 (Dynamic Host Configuration Protocol for IPv6) Client.

########## 2. TcpIpIpV6Enabled

- **UUID**: `7785577e-7bae-4091-a6ec-53e6cde4f694`
- **参数名**: `TcpIpIpV6Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of IPv6 (Internet Protocol version 6).

########## 3. TcpIpIpV6PathMtuDiscoveryEnabled

- **UUID**: `3cc9b9c9-ac53-4031-9962-7ce25f9e3120`
- **参数名**: `TcpIpIpV6PathMtuDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) Path MTU Discovery support for IPv6 according to IETF RFC 1981.

########## 4. TcpIpNdpAddressResolutionUnrechabilityDetectionEnabled

- **UUID**: `68a2e40c-4b38-461e-9401-851ad86d1a02`
- **参数名**: `TcpIpNdpAddressResolutionUnrechabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Address Resoultion and Neighbor Unreachability Detetion via NDP.

########## 5. TcpIpNdpPrefixAndRouterDiscoveryEnabled

- **UUID**: `37c8adfc-25e1-43ef-a3bf-bc618a6eb5c7`
- **参数名**: `TcpIpNdpPrefixAndRouterDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Prefix and Router Discovery via NDP.

########## 6. TcpIpIpV6EthIfUpdatePhysAddrFilterApiEnabled

- **UUID**: `bc9cc465-c5a3-4186-9bc8-b45358cb31a3`
- **参数名**: `TcpIpIpV6EthIfUpdatePhysAddrFilterApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will call EthIf_SetPhysAddrFilter() in order to configure the ethernet group address Rx filter.

Since the IPv6 Neighbor Discovery Protocol uses ethernet link-layer multicasts, the controller must be configured to accept received ethernet multicast IPv6 packets.

If the controller is in promiscuous mode or statically configured to accept all neccessary multicasts, this parameter can be disabled in order to avoid superfluous calls to the EthIf API.

########## 7. TcpIpIpV6SetTrafficClassAndFlowLabelApiEnabled

- **UUID**: `bccbc7fa-254c-4b08-ad6a-e87ce0e32f8a`
- **参数名**: `TcpIpIpV6SetTrafficClassAndFlowLabelApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 provides the IpV6_SetTrafficClass() and IpV6_SetFlowLabel() APIs to change the Traffic Class octet of the IPv6 header for outgoing packets.

If enabled the value can be set on a per-socket basis during runtime.
The default values for the Traffic Class and the Flow Label for all outgoing packets are controller specific and are configured by the IpV6DefaultTrafficClass and IpV6DefaultFlowLabel parameters.

[RFC2460 3. IPv6 Header Format]
[RFC2460 7. Traffic Classes]

see also [RFC2474 3. Differentiated Services Field Definition]

########## 8. TcpIpIpV6ExtendedDestAddrValidationEnabled

- **UUID**: `cc6401f0-003a-4e1d-aa53-072cd7cc557d`
- **参数名**: `TcpIpIpV6ExtendedDestAddrValidationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will check the destination address every time IpV6_ProvideTxBuffer() is called. 
If disabled the user should call IpV6_IsValidDestinationAddr() before IpV6_ProvideTxBuffer() is called the first time with a specific destination address.

########## 9. TcpIpIpV6CacheLookupOptimizationEnabled

- **UUID**: `cd4d574e-1ea1-4e6a-bfd0-0fa2ef3cd0ba`
- **参数名**: `TcpIpIpV6CacheLookupOptimizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether lookups in internal IpV6 data structures shall be optimized.

If enabled the last lookup result is stored and reused for the next lookup.
Disabling this feature will save some bytes in RAM and ROM but reduce performance.

######### STRING 类型参数

########## 1. TcpIpIpV6UserConfigFile

- **UUID**: `9b239a40-6859-45d0-a49c-70f7c788f755`
- **参数名**: `TcpIpIpV6UserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code (in IpV6_Cfg.h).

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. TcpIpIpV6DefaultCtrl

- **UUID**: `18479c9f-51b2-40ad-a00b-dcca1fb7667c`
- **引用名**: `TcpIpIpV6DefaultCtrl`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6Ctrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl/TcpIpIpVXCtrl/TcpIpIpV6Ctrl`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the IpV6 controller instance to which this address shall be assigned.

##### 43. TcpIpIpV4General

**容器属性**:

- **UUID**: `c1ca44c6-906c-422b-bee7-93600afcade7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV4General`
- **多重性**: [1..1]

**容器描述**:

This container is a subcontainer of TcpIp and specifies the general configuration parameters of the TCP/IP stack for IPv4

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpLocalAddrIpv4EntriesMax

- **UUID**: `129ee98f-fe2d-4b09-942d-1d7b215073e5`
- **参数名**: `TcpIpLocalAddrIpv4EntriesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of LocalAddr table entries for IPv4.

####### BOOLEAN 类型参数

######## 1. TcpIpArpEnabled

- **UUID**: `9faa203f-6fdc-4b9e-a29a-ed423fe70e2a`
- **参数名**: `TcpIpArpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of ARP (Address Resolution Protocol).

######## 2. TcpIpAutoIpEnabled

- **UUID**: `711cad52-6e74-4cbd-9658-722e3bb6fb8b`
- **参数名**: `TcpIpAutoIpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the Auto-IP (automatic private IP addressing) sub-module.

######## 3. TcpIpDhcpClientEnabled

- **UUID**: `45110993-4b87-429e-9f19-bef9604954fa`
- **参数名**: `TcpIpDhcpClientEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the DHCP (Dynamic Host Configuration Protocol) Client.

######## 4. TcpIpIcmpEnabled

- **UUID**: `6b6fcd2a-09aa-463a-9c29-d3e76b7c3114`
- **参数名**: `TcpIpIcmpEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disabled (FALSE) support of ICMP (Internet Control Message Protocol).

######## 5. TcpIpIpV4Enabled

- **UUID**: `6ed21325-4a2e-4a3f-ac20-71da2bd39dba`
- **参数名**: `TcpIpIpV4Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of IPv4 (Internet Protocol version 4).

######## 6. TcpIpPathMtuDiscoveryEnabled

- **UUID**: `876cae05-7a32-4b40-8cf1-bc7420800abf`
- **参数名**: `TcpIpPathMtuDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the discovery of the maximum transmission unit on a path according to IETF RfC 1191.

####### STRING 类型参数

######## 1. TcpIpIpV4UserConfigFile

- **UUID**: `f1f49b49-7ac0-48ac-9cf8-4433b9f19577`
- **参数名**: `TcpIpIpV4UserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpIpV4DefaultCtrl

- **UUID**: `ee6e9521-72d3-47eb-8fca-bb1f0172f660`
- **引用名**: `TcpIpIpV4DefaultCtrl`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV4Ctrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl/TcpIpIpVXCtrl/TcpIpIpV4Ctrl`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the default controller for messages not directed to own subnet(s)

##### 44. TcpIpIpV6General

**容器属性**:

- **UUID**: `0f963339-d6f3-4a29-b8c8-d26a8e21e09a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `TcpIpIpV6General`
- **多重性**: [1..1]

**容器描述**:

This container is a subcontainer of TcpIp and specifies the general configuration parameters of the TCP/IP stack for IPv6.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. TcpIpLocalAddrIpv6EntriesMax

- **UUID**: `8ed02751-16d5-4506-9d6f-c3e7eccbb538`
- **参数名**: `TcpIpLocalAddrIpv6EntriesMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Maximum number of LocalAddr table entries for IPv6.

####### BOOLEAN 类型参数

######## 1. TcpIpDhcpV6ClientEnabled

- **UUID**: `d767476e-8e17-4452-a45b-8b670228026c`
- **参数名**: `TcpIpDhcpV6ClientEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) the DHCPv6 (Dynamic Host Configuration Protocol for IPv6) Client.

######## 2. TcpIpIpV6Enabled

- **UUID**: `7785577e-7bae-4091-a6ec-53e6cde4f694`
- **参数名**: `TcpIpIpV6Enabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of IPv6 (Internet Protocol version 6).

######## 3. TcpIpIpV6PathMtuDiscoveryEnabled

- **UUID**: `3cc9b9c9-ac53-4031-9962-7ce25f9e3120`
- **参数名**: `TcpIpIpV6PathMtuDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) Path MTU Discovery support for IPv6 according to IETF RFC 1981.

######## 4. TcpIpNdpAddressResolutionUnrechabilityDetectionEnabled

- **UUID**: `68a2e40c-4b38-461e-9401-851ad86d1a02`
- **参数名**: `TcpIpNdpAddressResolutionUnrechabilityDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Address Resoultion and Neighbor Unreachability Detetion via NDP.

######## 5. TcpIpNdpPrefixAndRouterDiscoveryEnabled

- **UUID**: `37c8adfc-25e1-43ef-a3bf-bc618a6eb5c7`
- **参数名**: `TcpIpNdpPrefixAndRouterDiscoveryEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Enables (TRUE) or disables (FALSE) support of Prefix and Router Discovery via NDP.

######## 6. TcpIpIpV6EthIfUpdatePhysAddrFilterApiEnabled

- **UUID**: `bc9cc465-c5a3-4186-9bc8-b45358cb31a3`
- **参数名**: `TcpIpIpV6EthIfUpdatePhysAddrFilterApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will call EthIf_SetPhysAddrFilter() in order to configure the ethernet group address Rx filter.

Since the IPv6 Neighbor Discovery Protocol uses ethernet link-layer multicasts, the controller must be configured to accept received ethernet multicast IPv6 packets.

If the controller is in promiscuous mode or statically configured to accept all neccessary multicasts, this parameter can be disabled in order to avoid superfluous calls to the EthIf API.

######## 7. TcpIpIpV6SetTrafficClassAndFlowLabelApiEnabled

- **UUID**: `bccbc7fa-254c-4b08-ad6a-e87ce0e32f8a`
- **参数名**: `TcpIpIpV6SetTrafficClassAndFlowLabelApiEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 provides the IpV6_SetTrafficClass() and IpV6_SetFlowLabel() APIs to change the Traffic Class octet of the IPv6 header for outgoing packets.

If enabled the value can be set on a per-socket basis during runtime.
The default values for the Traffic Class and the Flow Label for all outgoing packets are controller specific and are configured by the IpV6DefaultTrafficClass and IpV6DefaultFlowLabel parameters.

[RFC2460 3. IPv6 Header Format]
[RFC2460 7. Traffic Classes]

see also [RFC2474 3. Differentiated Services Field Definition]

######## 8. TcpIpIpV6ExtendedDestAddrValidationEnabled

- **UUID**: `cc6401f0-003a-4e1d-aa53-072cd7cc557d`
- **参数名**: `TcpIpIpV6ExtendedDestAddrValidationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the IpV6 will check the destination address every time IpV6_ProvideTxBuffer() is called. 
If disabled the user should call IpV6_IsValidDestinationAddr() before IpV6_ProvideTxBuffer() is called the first time with a specific destination address.

######## 9. TcpIpIpV6CacheLookupOptimizationEnabled

- **UUID**: `cd4d574e-1ea1-4e6a-bfd0-0fa2ef3cd0ba`
- **参数名**: `TcpIpIpV6CacheLookupOptimizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether lookups in internal IpV6 data structures shall be optimized.

If enabled the last lookup result is stored and reused for the next lookup.
Disabling this feature will save some bytes in RAM and ROM but reduce performance.

####### STRING 类型参数

######## 1. TcpIpIpV6UserConfigFile

- **UUID**: `9b239a40-6859-45d0-a49c-70f7c788f755`
- **参数名**: `TcpIpIpV6UserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code (in IpV6_Cfg.h).

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. TcpIpIpV6DefaultCtrl

- **UUID**: `18479c9f-51b2-40ad-a00b-dcca1fb7667c`
- **引用名**: `TcpIpIpV6DefaultCtrl`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `TcpIpIpV6Ctrl`
- **完整路径**: `/AUTOSAR/EcucDefs/TcpIp/TcpIpConfig/TcpIpCtrl/TcpIpIpVXCtrl/TcpIpIpV6Ctrl`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the IpV6 controller instance to which this address shall be assigned.

##### 45. TcpIpIpVXCtrl

**容器属性**:

- **UUID**: `c7454466-eafa-4093-9930-19ededbf3a4e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `TcpIpIpVXCtrl`
- **多重性**: [1..1]

**容器选择**:

- **TcpIpIpV4Ctrl**
  - UUID: `2ab7ecbc-88ed-4c6b-87c3-3341fc476534`
  - 描述: Specifies an Internet Protocol version 4 (IPv4) instance.
- **TcpIpIpV6Ctrl**
  - UUID: `739c0200-ae9c-42da-8178-469e4380cfe7`
  - 描述: Specifies an Internet Protocol version 6 (IPv6) instance.
- **TcpIpIpV6MtuConfig**
  - UUID: `8123f92e-015e-40c8-afc5-e6f1cbd85228`
  - 描述: This container specifies the Maximum Transmission Unit parameters for this IPv6 instance.

**容器描述**:

Specifies whether this controller is an Internet Protocol version 4 (IPv4) or Internet Protocol version 6 (IPv4) instance.

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

1. **TcpIp**
