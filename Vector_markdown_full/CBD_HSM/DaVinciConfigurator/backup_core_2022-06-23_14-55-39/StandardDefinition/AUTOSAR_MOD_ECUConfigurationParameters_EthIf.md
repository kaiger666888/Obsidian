# EthIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:16

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthIf](#ethif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthIf

#### 基本信息

- **UUID**: `ECUC:37f208f2-5f1b-46d0-88ad-5a6d0ab35c0a`
- **模块名称**: `EthIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the EthIf (Ethernet Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. EthIfConfigSet

**容器属性**:

- **UUID**: `ECUC:2e80d7a0-8c5e-4418-90e5-7566219aa6e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfConfigSet`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: true

**容器描述**:

Collecting container for all parameters with post-build configuration classes.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. EthIfController

**容器属性**:

- **UUID**: `ECUC:b0742c53-b8e3-4b1f-90d5-44cf6cf0f904`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfController`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration of EthIfController.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EthIfCtrlIdx

- **UUID**: `ECUC:11f8c68f-cb6d-48f9-b8a6-b4f8cd0aa940`
- **参数名**: `EthIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the Ethernet Communication Controllers. Upper layer BSW modules and the EthIf itself use this index to identify a Ethernet CC.

########## 2. EthIfCtrlMtu

- **UUID**: `ECUC:5c7b376a-c30d-4dad-86e9-3d006d5eeeac`
- **参数名**: `EthIfCtrlMtu`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [64..9000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum transmission unit (MTU) of the EthIfCtrl in [bytes].

########## 3. EthIfVlanId

- **UUID**: `ECUC:3f77c980-3fb1-4f5c-b6d9-36dc500a86fb`
- **参数名**: `EthIfVlanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A virtual-LAN is identified by this attribute according to IEEE 802.1Q.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthIfPhysControllerRef

- **UUID**: `ECUC:569eb05a-1907-4b7d-b59f-6ee27ec7608f`
- **引用名**: `EthIfPhysControllerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet controller used for sending/receiving Ethernet frames and controlled by the EthIf mode management.

########## 2. EthIfTransceiverRef

- **UUID**: `ECUC:54c10002-0930-476d-8d0b-a178bf138d77`
- **引用名**: `EthIfTransceiverRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthTrcvConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet/EthTrcvConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet transceiver used to retrieve the link state and controlled by the EthIf mode management.

########## 3. EthIfSwitchRef

- **UUID**: `3e8e32f8-349f-414c-b96e-956eefb32fe3`
- **引用名**: `EthIfSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `EthIfSwitch`
- **完整路径**: `/MICROSAR/EthIf/EthIfConfigSet/EthIfSwitch`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet switch controlled by the EthIf mode management.

########## 4. EthIfSwitchPortGroupRef

- **UUID**: `4aba61f5-4b88-4ecc-8481-b1170158b690`
- **引用名**: `EthIfSwitchPortGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthIfSwitchPortGroup`
- **完整路径**: `/MICROSAR/EthIf/EthIfConfigSet/EthIfSwitchPortGroup`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### 2. EthIfFrameOwnerConfig

**容器属性**:

- **UUID**: `ECUC:37e0f750-2616-4d3f-81d1-086be3a639c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfFrameOwnerConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of Ethernet frame owner

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthIfFrameType

- **UUID**: `ECUC:9f885a46-fd04-4ac7-8a13-08dc4756902e`
- **参数名**: `EthIfFrameType`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the Ethernet frame type.

########## 2. EthIfOwner

- **UUID**: `ECUC:3182eb85-f911-4fa6-9999-22536204c451`
- **参数名**: `EthIfOwner`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the owner of an Ethernet frame type. The owner is a zero based index into the callback function configuration 'EthIfRxIndicationConfig'. I.e. an Ethernet frame of type IPv4 (0x800) at index 0 will call the first callback function configured in 'EthIfRxIndicationConfig'.

####### 3. EthIfRxIndicationConfig

**容器属性**:

- **UUID**: `ECUC:da2f1421-087a-40d5-b0bb-233f38c04fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfRxIndicationConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of receive callback functions.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. EthIfRxIndicationFunction

- **UUID**: `ECUC:9f914ccb-963f-40a4-855f-aedec4c921fb`
- **参数名**: `EthIfRxIndicationFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies receive indication callback function.

####### 4. EthIfTrcvLinkStateChgConfig

**容器属性**:

- **UUID**: `ECUC:d948a757-1808-40e8-8790-ada11854d9dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfTrcvLinkStateChgConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies link state change callback function

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. EthIfTrcvLinkStateChgFunction

- **UUID**: `ECUC:690388af-20c9-48dc-b8f7-2652cce939f7`
- **参数名**: `EthIfTrcvLinkStateChgFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies link state change callback function

####### 5. EthIfTxConfirmationConfig

**容器属性**:

- **UUID**: `ECUC:b423970d-2818-47ed-9d91-b62cbccc1f47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfTxConfirmationConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of transmit indication callback functions.

######## 参数配置

此容器包含 **1** 个参数：

######### FUNCTION-NAME 类型参数

########## 1. EthIfTxConfirmationFunction

- **UUID**: `ECUC:0066da3a-acae-4b4d-8d01-26abd02c73d1`
- **参数名**: `EthIfTxConfirmationFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies transmit indication callback function

####### 6. EthIfSwitch

**容器属性**:

- **UUID**: `efa31a4a-fc71-4292-8786-cd2eeed75ee2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfSwitch`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container is used to globally index all hardware switches that are used by the Ethernet Interface. The index may be used by upper layers like the DHCP server component as a unique identifier when calling a Ethernet Interface API. Besides the global index a reference to a hardware switch configuration container resides in this container.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EthIfSwitchIndex

- **UUID**: `32eb5e2b-a61d-4c9c-a2e8-cf5d6ed59fb5`
- **参数名**: `EthIfSwitchIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies a globally unique index for each hardware Ethernet Switch that is used by the Ethernet Interface. The index is zero-based and incremented by one for each hardware switch.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthIfEthSwtRef

- **UUID**: `71626864-79de-4c6a-8084-320a23b15185`
- **引用名**: `EthIfEthSwtRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Ethernet Switch configuration container.

##### 2. EthIfController

**容器属性**:

- **UUID**: `ECUC:b0742c53-b8e3-4b1f-90d5-44cf6cf0f904`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfController`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration of EthIfController.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. EthIfCtrlIdx

- **UUID**: `ECUC:11f8c68f-cb6d-48f9-b8a6-b4f8cd0aa940`
- **参数名**: `EthIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the Ethernet Communication Controllers. Upper layer BSW modules and the EthIf itself use this index to identify a Ethernet CC.

######## 2. EthIfCtrlMtu

- **UUID**: `ECUC:5c7b376a-c30d-4dad-86e9-3d006d5eeeac`
- **参数名**: `EthIfCtrlMtu`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [64..9000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum transmission unit (MTU) of the EthIfCtrl in [bytes].

######## 3. EthIfVlanId

- **UUID**: `ECUC:3f77c980-3fb1-4f5c-b6d9-36dc500a86fb`
- **参数名**: `EthIfVlanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: A virtual-LAN is identified by this attribute according to IEEE 802.1Q.

###### 引用关系

此容器包含 **4** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthIfPhysControllerRef

- **UUID**: `ECUC:569eb05a-1907-4b7d-b59f-6ee27ec7608f`
- **引用名**: `EthIfPhysControllerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet controller used for sending/receiving Ethernet frames and controlled by the EthIf mode management.

######## 2. EthIfTransceiverRef

- **UUID**: `ECUC:54c10002-0930-476d-8d0b-a178bf138d77`
- **引用名**: `EthIfTransceiverRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthTrcvConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet/EthTrcvConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet transceiver used to retrieve the link state and controlled by the EthIf mode management.

######## 3. EthIfSwitchRef

- **UUID**: `3e8e32f8-349f-414c-b96e-956eefb32fe3`
- **引用名**: `EthIfSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `EthIfSwitch`
- **完整路径**: `/MICROSAR/EthIf/EthIfConfigSet/EthIfSwitch`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Ethernet switch controlled by the EthIf mode management.

######## 4. EthIfSwitchPortGroupRef

- **UUID**: `4aba61f5-4b88-4ecc-8481-b1170158b690`
- **引用名**: `EthIfSwitchPortGroupRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EthIfSwitchPortGroup`
- **完整路径**: `/MICROSAR/EthIf/EthIfConfigSet/EthIfSwitchPortGroup`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

##### 3. EthIfFrameOwnerConfig

**容器属性**:

- **UUID**: `ECUC:37e0f750-2616-4d3f-81d1-086be3a639c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfFrameOwnerConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of Ethernet frame owner

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthIfFrameType

- **UUID**: `ECUC:9f885a46-fd04-4ac7-8a13-08dc4756902e`
- **参数名**: `EthIfFrameType`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the Ethernet frame type.

######## 2. EthIfOwner

- **UUID**: `ECUC:3182eb85-f911-4fa6-9999-22536204c451`
- **参数名**: `EthIfOwner`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the owner of an Ethernet frame type. The owner is a zero based index into the callback function configuration 'EthIfRxIndicationConfig'. I.e. an Ethernet frame of type IPv4 (0x800) at index 0 will call the first callback function configured in 'EthIfRxIndicationConfig'.

##### 4. EthIfRxIndicationConfig

**容器属性**:

- **UUID**: `ECUC:da2f1421-087a-40d5-b0bb-233f38c04fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfRxIndicationConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of receive callback functions.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. EthIfRxIndicationFunction

- **UUID**: `ECUC:9f914ccb-963f-40a4-855f-aedec4c921fb`
- **参数名**: `EthIfRxIndicationFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies receive indication callback function.

##### 5. EthIfTrcvLinkStateChgConfig

**容器属性**:

- **UUID**: `ECUC:d948a757-1808-40e8-8790-ada11854d9dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfTrcvLinkStateChgConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Specifies link state change callback function

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. EthIfTrcvLinkStateChgFunction

- **UUID**: `ECUC:690388af-20c9-48dc-b8f7-2652cce939f7`
- **参数名**: `EthIfTrcvLinkStateChgFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies link state change callback function

##### 6. EthIfTxConfirmationConfig

**容器属性**:

- **UUID**: `ECUC:b423970d-2818-47ed-9d91-b62cbccc1f47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfTxConfirmationConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Configuration of transmit indication callback functions.

###### 参数配置

此容器包含 **1** 个参数：

####### FUNCTION-NAME 类型参数

######## 1. EthIfTxConfirmationFunction

- **UUID**: `ECUC:0066da3a-acae-4b4d-8d01-26abd02c73d1`
- **参数名**: `EthIfTxConfirmationFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies transmit indication callback function

##### 7. EthIfSwitch

**容器属性**:

- **UUID**: `efa31a4a-fc71-4292-8786-cd2eeed75ee2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfSwitch`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container is used to globally index all hardware switches that are used by the Ethernet Interface. The index may be used by upper layers like the DHCP server component as a unique identifier when calling a Ethernet Interface API. Besides the global index a reference to a hardware switch configuration container resides in this container.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EthIfSwitchIndex

- **UUID**: `32eb5e2b-a61d-4c9c-a2e8-cf5d6ed59fb5`
- **参数名**: `EthIfSwitchIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies a globally unique index for each hardware Ethernet Switch that is used by the Ethernet Interface. The index is zero-based and incremented by one for each hardware switch.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthIfEthSwtRef

- **UUID**: `71626864-79de-4c6a-8084-320a23b15185`
- **引用名**: `EthIfEthSwtRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Ethernet Switch configuration container.

##### 8. EthIfGeneral

**容器属性**:

- **UUID**: `ECUC:6c8794b3-e72e-43f7-b296-4c01cf430dbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthIfGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the Ethernet Interface.

###### 参数配置

此容器包含 **15** 个参数：

####### INTEGER 类型参数

######## 1. EthIfMaxTrcvsTotal

- **UUID**: `ECUC:0fc1d4ae-0f92-43b8-bf65-4d1036eb0d9b`
- **参数名**: `EthIfMaxTrcvsTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the total number of transceivers.

######## 2. EthIfMaxTxBufsTotal

- **UUID**: `ECUC:a44750e3-3109-41f0-bee8-aa9994ce0a0a`
- **参数名**: `EthIfMaxTxBufsTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the total number of transmit buffers.

######## 3. EthIfRxIndicationIterations

- **UUID**: `ECUC:22700c8d-6b97-4d16-8111-31116560b83f`
- **参数名**: `EthIfRxIndicationIterations`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of Ethernet frames per Ethernet controller polled from the Ethernet driver within EthIf_MainFunctionRx.

######## 4. EthIfTrcvLinkStateChgMainReload

- **UUID**: `ECUC:2c506165-9e0f-4c80-aa09-1edc85118c86`
- **参数名**: `EthIfTrcvLinkStateChgMainReload`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the frequency of transceiver link state change checks in each

####### BOOLEAN 类型参数

######## 1. EthIfDevErrorDetect

- **UUID**: `ECUC:0749db1b-7fdd-4e28-92c7-b583b40e921f`
- **参数名**: `EthIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables development error detection.

######## 2. EthIfEnableRxInterrupt

- **UUID**: `ECUC:cd0c0315-e5ac-4c42-804e-04f5a8289812`
- **参数名**: `EthIfEnableRxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables receive interrupt.

######## 3. EthIfEnableTxInterrupt

- **UUID**: `ECUC:a3457b20-2449-49ad-99c5-69f0b70c5cc3`
- **参数名**: `EthIfEnableTxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables the transmit interrupt.

######## 4. EthIfGetBaudRate

- **UUID**: `ECUC:f8834dcb-ef9a-49da-a68f-954aa34117d2`
- **参数名**: `EthIfGetBaudRate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables GetBaudRate API.

######## 5. EthIfGetCounterState

- **UUID**: `ECUC:59d038be-b122-43b8-b1e1-1ff5a6cd34bc`
- **参数名**: `EthIfGetCounterState`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables GetCounterState API.

######## 6. EthIfStartAutoNegotiation

- **UUID**: `ECUC:6b03cae0-33a9-4658-bc68-c31d66ebc0f3`
- **参数名**: `EthIfStartAutoNegotiation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables StartAutoNegotiation API.

######## 7. EthIfVersionInfoApi

- **UUID**: `ECUC:70813955-bcf5-4158-9146-b95b832fa699`
- **参数名**: `EthIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API

######## 8. EthIfVersionInfoApiMacro

- **UUID**: `ECUC:8f788107-3d3e-4280-ae24-0ad29b191410`
- **参数名**: `EthIfVersionInfoApiMacro`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API macro implementation.

####### FLOAT 类型参数

######## 1. EthIfMainFunctionPeriod

- **UUID**: `ECUC:c1682f48-b9fb-4e01-8919-e43f11888af3`
- **参数名**: `EthIfMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period of main function EthIf_MainFunctionRx and EthIf_MainFunctionTx in seconds. Ethernet Interface does not require this information but the BSW scheduler.

######## 2. EthIfMainFunctionRxTimeout

- **UUID**: `ECUC:149a43e4-f4d8-4432-9fe7-083897e263d2`
- **参数名**: `EthIfMainFunctionRxTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in seconds after which the EthIf stops to receive frames in an EthIfMainFunctionRx period.

####### STRING 类型参数

######## 1. EthIfPublicCddHeaderFile

- **UUID**: `ECUC:78109fef-fa07-4bdb-a31f-ae95502bae04`
- **参数名**: `EthIfPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines header files for callback functions which shall be included in case of CDDs. Range of characters is 1.. 32.

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

1. **EthIf**
