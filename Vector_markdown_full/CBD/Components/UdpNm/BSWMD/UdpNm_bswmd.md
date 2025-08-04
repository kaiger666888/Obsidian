# UdpNm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [UdpNm](#udpnm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-1-1.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. UdpNm

#### 基本信息

- **UUID**: `22381f8a-f5e6-4afc-92e2-c3625b5ffa79`
- **模块名称**: `UdpNm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-SELECTABLE
  - VARIANT-POST-BUILD-LOADABLE

#### 模块描述

Ethernet Network Management (Udp). The UdpNm is a hardware independent protocol that can only be used on ETH. Its main purpose is to coordinate the transition between normal operation and bus-sleep mode of the network. #ModeManagement #NetworkManagement #Shutdown

#### 版本历史

共有 **20** 个版本记录：

##### 1. 版本 2.00.00

- **状态**: beta
- **发布日期**: 2013-05-21
- **发布者**: vismha

**变更内容**:

##### 2. 版本 2.01.00

- **状态**: beta
- **发布日期**: 2013-11-11T02:57:23+01:00
- **发布者**: vismha

**变更内容**:

##### 3. 版本 2.01.01

- **状态**: released
- **发布日期**: 2014-06-17T02:46:21+02:00
- **发布者**: vismha

**变更内容**:

##### 4. 版本 2.01.02

- **状态**: released
- **发布日期**: 2014-10-10T09:14:20+02:00
- **发布者**: vismha

**变更内容**:

##### 5. 版本 2.01.03

- **状态**: released
- **发布日期**: 2015-08-04T03:38:48+02:00
- **发布者**: vismha

**变更内容**:

##### 6. 版本 2.01.04

- **状态**: released
- **发布日期**: 2015-11-02T10:17:31+01:00
- **发布者**: vismha

**变更内容**:

##### 7. 版本 3.00.00

- **状态**: released
- **发布日期**: 2015-11-26T09:54:32+01:00
- **发布者**: vismha

**变更内容**:

##### 8. 版本 3.00.01

- **状态**: released
- **发布日期**: 2016-02-12T08:59:04+01:00
- **发布者**: visfdn

**变更内容**:

##### 9. 版本 3.01.00

- **状态**: released
- **发布日期**: 2016-02-12T02:07:03+01:00
- **发布者**: visfdn

**变更内容**:

##### 10. 版本 3.02.00

- **状态**: released
- **发布日期**: 2016-08-03T10:38:25+02:00
- **发布者**: vissrk

**变更内容**:

##### 11. 版本 3.02.01

- **状态**: released
- **发布日期**: 2016-11-25T02:39:48+01:00
- **发布者**: vissrk

**变更内容**:

##### 12. 版本 3.02.02

- **状态**: released
- **发布日期**: 2017-02-16T04:22:16+01:00
- **发布者**: vissrk

**变更内容**:

##### 13. 版本 3.03.00

- **状态**: released
- **发布日期**: 2017-10-23T10:36:18+02:00
- **发布者**: vislsi

**变更内容**:

##### 14. 版本 3.03.01

- **状态**: released
- **发布日期**: 2018-01-16T13:21:49+01:00
- **发布者**: vissrk

**变更内容**:

##### 15. 版本 4.00.00

- **状态**: released
- **发布日期**: 2016-09-02T12:56:10+02:00
- **发布者**: vissrk, vispkn

**变更内容**:

##### 16. 版本 5.00.00

- **状态**: released
- **发布日期**: 2019-04-01T13:40:37+02:00
- **发布者**: vispkn

**变更内容**:

##### 17. 版本 6.00.00

- **状态**: released
- **发布日期**: 2021-09-27T12:50:42+02:00
- **发布者**: vispkn

**变更内容**:

##### 18. 版本 6.01.00

- **状态**: released
- **发布日期**: 2022-02-08T15:12:49+01:00
- **发布者**: vispkn

**变更内容**:

##### 19. 版本 6.01.01

- **状态**: released
- **发布日期**: 2022-06-10T09:18:46+02:00
- **发布者**: vispkn

**变更内容**:

##### 20. 版本 7.00.00

- **状态**: released
- **发布日期**: 2023-09-25T10:53:20+02:00
- **发布者**: vissrk

**变更内容**:

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. UdpNmGlobalConfig

**容器属性**:

- **UUID**: `55ae9818-bb5d-414a-81b7-4833b760fb65`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmGlobalConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Global configuration parameters of the UdpNm.

###### 参数配置

此容器包含 **27** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmNumberOfChannels

- **UUID**: `a112b204-9728-41d5-b79a-40f626a269c6`
- **参数名**: `UdpNmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

######## 2. UdpNmCoordinatorId

- **UUID**: `de56e115-1add-40d5-8faf-3c2f4873713b`
- **参数名**: `UdpNmCoordinatorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..3]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

####### BOOLEAN 类型参数

######## 1. UdpNmBusSynchronizationEnabled

- **UUID**: `d935751f-601e-47bf-9335-142c46f46ba7`
- **参数名**: `UdpNmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the bus synchronization support is enabled. This feature is required for gateway nodes only.

This option allows the transmission of an asynchronous NM message at any time within Network Mode. This may be required for the synchronized shutdown of networks. Therefore this option is usually only enabled in gateways.


RESTRICTIONS: This parameter is derived from NmBusSynchronizationEnabled. This parameter is only relevant if UdpNmPassiveModeEnabled == false.

######## 2. UdpNmComControlEnabled

- **UUID**: `9a328735-2cec-43af-8dc9-e718652968ab`
- **参数名**: `UdpNmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the Communication Control support is enabled.
If this option is enabled two additional APIs are available that can either enable or disable the transmission of Network Management messages in the Normal Operation state. While the transmission is disabled the network cannot be released.

RESTRICTIONS: Derived from NmComControlEnabled.
If this global parameter is enabled, at least one channel configuration must have this parameter enabled. If this parameter is disabled, all channel configurations must have this parameter disabled.
/MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmComControlEnabled.

######## 3. UdpNmComUserDataSupport

- **UUID**: `71c5b397-6fee-4212-9a7e-d448616d7174`
- **参数名**: `UdpNmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the user data handling by a PDU handled within an upper layer is supported.

######## 4. UdpNmCoordinatorSyncSupport

- **UUID**: `7e98e625-d170-48e5-bb1f-59a45928a2ab`
- **参数名**: `UdpNmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the coordinator synchronization support is enabled.

######## 5. UdpNmDevErrorDetect

- **UUID**: `b8ea26be-d4c5-415c-b424-1087e42ba49f`
- **参数名**: `UdpNmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.
If it is enabled development errors are reported to the Development Error Tracer (Det).
The following development errors are reported: 
- service call without intialization of network management
- service call with invalid channel handle
- service call with invalid PDU ID
- reception of an NM PDU in Bus Sleep Mode
- network timeout (i.e. the network management timoeut timer has timed out in Repeat Message State or Normal Operation State)
- null pointer has been passed as argument

######## 6. UdpNmImmediateRestartEnabled

- **UUID**: `eac63955-4fd8-44ba-b97b-447fc383151b`
- **参数名**: `UdpNmImmediateRestartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the asynchronous transmission of an NM PDU upon bus-communication request in Prepare-Bus-Sleep mode is enabled.
Enabling this option may lead to a burst of NM messages if all nodes get a bus-communication request approximately at the same time.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled is False
If this global parameter is enabled, at least one channel configuration must have this parameter enabled. If this parameter is disabled, all channel configurations must have this parameter disabled.
/MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmImmediateRestartEnabled.

######## 7. UdpNmNodeDetectionEnabled

- **UUID**: `675990bd-c0c6-4eea-ab71-bd9881ba86ce`
- **参数名**: `UdpNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the node detection feature is enabled.
If a Tester is present in the network, 'UdpNmNodeDetectionEnabled' offers the opportunity to detect all present network nodes.


RESTRICTIONS: Derived from NmNodeDetectionEnabled.
This parameter is only relevant if UdpNmPassiveModeEnabled is false.
This parameter is only valid if UdpNmPduNidPosition is not UDPNM_PDU_OFF for at least one channel.

If this global parameter is enabled, at least one channel configuration must have this parameter enabled. If this parameter is disabled, all channel configurations must have this parameter disabled.
/MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmNodeDetectionEnabled.

######## 8. UdpNmNodeIdEnabled

- **UUID**: `c17c8173-6338-48f1-93e7-6fddca9e7024`
- **参数名**: `UdpNmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter specifies if the Node ID is enabled.

Parameters value is derived from configuration parameter NmNodeIdEnabled.

RESTRICTIONS:If this global parameter is enabled, at least one channel configuration must have this parameter enabled. If this parameter is disabled, all channel configurations must have this parameter disabled.
/MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmNodeIdEnabled.

######## 9. UdpNmPassiveModeEnabled

- **UUID**: `59d6f093-d286-4dee-bc48-e135455d49a2`
- **参数名**: `UdpNmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the Passive Mode is supported.
If this option is set, the node is not able to send NM messages. This option can be used for nodes that do not require to keep the bus awake.

RESTRICTIONS: Needs to have the same value as 'NmPassiveModeEnabled' for all UdpNm channels.

######## 10. UdpNmPduRxIndicationEnabled

- **UUID**: `0ad60ecb-d5d6-4af7-879d-7b592a9d189e`
- **参数名**: `UdpNmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the PDU Rx Indication is called.
If this option is enabled a callback function for every received PDU will be triggered.


RESTRICTIONS: Derived from 'NmPduRxIndicationEnabled'.

######## 11. UdpNmPnEiraCalcEnabled

- **UUID**: `e03a8ae3-0f6f-45d1-9459-c2bb25929b8b`
- **参数名**: `UdpNmPnEiraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm calculates the PN request information for internal and external requests. (EIRA)
                    
true: PN request are calculated
false: PN request are not calculated

######## 12. UdpNmRemoteSleepIndEnabled

- **UUID**: `9c98a328-1a16-4695-b544-c1b3a4318ab1`
- **参数名**: `UdpNmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the remote sleep indication support is enabled. This feature is required for gateway nodes only.
'UdpNmRemoteSleepIndEnabled' is used in gateways to detect when the synchronized shutdown of networks has to be carried out.
It comprises Remote Sleep Indication, Remote Sleep Cancelation and checking of the Remote Sleep Indication State.

Remote Sleep Indication is notified when your network node is the only one in the whole network that requests bus-communication for 'UdpNmRemoteSleepIndTime'.
Remote Sleep Cancelation is notified if any other network node requires the communication bus while Remote Sleep Indication takes place in your network node.


RESTRICTIONS: Derived from NmRemoteSleepIndEnabled.
This parameter is only relevant if UdpNmPassiveModeEnabled is false.

######## 13. UdpNmRepeatMsgIndEnabled

- **UUID**: `bab82850-098b-457b-824f-c4785e2a7f75`
- **参数名**: `UdpNmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the notification that a RepeatMessageRequest bit has been received is enabled.

This option enables a callback to the NM Interface whenever a state change due to a repeat message request or a repeat message bit occurs.



RESTRICTIONS: If (UdpNmNodeDetectionEnabled == false) then (UdpNmRepeatMsgIndEnabled = false). Derived from 'NmRepeatMsgIndEnabled'.

If this global parameter is enabled, at least one channel configuration must have this parameter enabled. If this parameter is disabled, all channel configurations must have this parameter disabled.
/MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmChannelConfig/UdpNmRepeatMsgIndEnabled.

######## 14. UdpNmStateChangeIndEnabled

- **UUID**: `a9d6688a-21c3-4fe6-bd8f-3701c0a8ef23`
- **参数名**: `UdpNmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the UdpNm state change notification is enabled.
This option allows to track every change in the NM state machine by the means of a callback function triggered on every state change.



RESTRICTIONS: Derived from 'NmStateChangeIndEnabled'.

######## 15. UdpNmUserDataEnabled

- **UUID**: `f20a7033-8a95-4fb0-8343-1fd74897e221`
- **参数名**: `UdpNmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the user data support is enabled.
This option provides read and write access to the user data. Location of user data in the NM message depends on the message configuration.



RESTRICTIONS: Derived from 'NmUserDataEnabled'.

######## 16. UdpNmVersionInfoApi

- **UUID**: `1bd97b5c-a8ac-4a3d-9d29-374501c30174`
- **参数名**: `UdpNmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter enables/disables the function UdpNm_GetVersionInfo() to get major, minor and patch version information.

######## 17. UdpNmRuntimeMeasurementSupport

- **UUID**: `fc6535ba-8c32-4712-ae0e-a1e846c6c307`
- **参数名**: `UdpNmRuntimeMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if runtime measurement points are added to the BSW module code and to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality.
Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

######## 18. UdpNmSafeBswChecks

- **UUID**: `9e98130a-c44c-4bb5-a982-3039df2cdbde`
- **参数名**: `UdpNmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 19. UdpNmRuntimeErrorReport

- **UUID**: `f535c392-e5c1-47c5-b72a-e90cd82c5bb5`
- **参数名**: `UdpNmRuntimeErrorReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Selects if runtime errors are reported.

######## 20. UdpNmCoordinatorEnabled

- **UUID**: `84b0695f-ed4c-46a5-90ba-bbc48fa0f20c`
- **参数名**: `UdpNmCoordinatorEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

######## 21. UdpNmPnSyncShutdownErrorReactionEnabled

- **UUID**: `b9acde05-16fb-4e5e-a0d9-b41d8f8f6a5c`
- **参数名**: `UdpNmPnSyncShutdownErrorReactionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Pre-processor switch for enabling reaction, if a top-level PNC coordinator received a PN shutdown message on a NM-channel which refer to a ComM channel that is actively coordinated by a PNC gateway.

####### FLOAT 类型参数

######## 1. UdpNmPnResetTime

- **UUID**: `ec689076-e47a-4e53-8f50-59fc2cc4edfe`
- **参数名**: `UdpNmPnResetTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of PN requests in the EIRA and in the ERA. The value shall be the same for every channel. Thus it is a global config parameter.

######## 2. UdpNmPnShutdownMessageRetransmissionDuration

- **UUID**: `2e0acfc1-0f95-4c72-80a3-5adb5c7ecac2`
- **参数名**: `UdpNmPnShutdownMessageRetransmissionDuration`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies the duration in msec of retransmission phase of a PN shutdown message. A retransmission shall be performed per affected NM channel, as long as the PN shutdown message could not be successfully sent and the retransmission timer is running. The value shall be a multiple integral of UdpNmMainFunctionPeriod.

######## 3. UdpNmPnShutdownMessageTimeoutTime

- **UUID**: `b77f7842-8f31-4d05-b5ab-1468b1848b49`
- **参数名**: `UdpNmPnShutdownMessageTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This message timeout time is only relevant if the feature UdpNmSynchronizedPncShutdownEnabled is enabled.

This parameter specifies the timeout time that is waited for a TxConfirmation of the transmitted PNSR message until a retry is performed.

Note: This time must be smaller than the UdpNmPnShutdownMessageRetransmissionDuration.

####### STRING 类型参数

######## 1. UdpNmUserConfigFile

- **UUID**: `c9662a71-72c0-4e21-8201-f1afaf0f8bf1`
- **参数名**: `UdpNmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to an external text file that will be included during generation to UdpNm_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmPnEiraRxNSduRef

- **UUID**: `367d8579-5291-49cd-b2ba-8f2738099f51`
- **引用名**: `UdpNmPnEiraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to a Pdu in the COM-Stack. Only one SduRef is required for UdpNm because the EIRA is the aggregation over all Ethernet Channels.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. UdpNmChannelConfig

**容器属性**:

- **UUID**: `c024afe1-cd82-41d8-b750-2d6aabf37412`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmChannelConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the channel specific configuration parameter of the UdpNm.

######## 参数配置

此容器包含 **33** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmNodeId

- **UUID**: `8e0cd2be-398b-4103-8620-5e002b1d334b`
- **参数名**: `UdpNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the node identifier of local node.

The 'NodeId' is transmitted within the network management message if UdpNmPduNidPosition != UDPNM_PDU_OFF)

The node identifier is used for the detection of present nodes and can be read by the application at any time.

Note: This value is transmitted within the NM message.

########## 2. UdpNmPduLength

- **UUID**: `63f48c13-fd3c-4239-9773-7b2a476520fb`
- **参数名**: `UdpNmPduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the length of the NM PDU.

The value is auto-calculated dependent on 'UdpNmPduCbvPosition', 'UdpNmPduNidPosition' and 'UdpNmUserDataLength'.

According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like specified in AUTOSAR SWS (last released version 4.2.2). Therefore it is possible to use PDUs larger than 8 Byte.

########## 3. UdpNmUserDataLength

- **UUID**: `51b917dd-4885-4326-9815-a059af9154cf`
- **参数名**: `UdpNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the length of the user data contained in the NM PDU.

According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like specified in AUTOSAR SWS (last released version 4.2.2). Therefore the User Data Length is extended in line with the extension of the PDU Length.

########## 4. UdpNmImmediateNmTransmissions

- **UUID**: `dec4a6bf-1161-44af-8048-66ccc86e3212`
- **参数名**: `UdpNmImmediateNmTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the number of immediate NM PDUs which shall be transmitted. If the value is zero no immediate NM PDUs are transmitted. The cycle time of immediate NM PDUs is defined by UdpNmImmediateNmCycleTime.

########## 5. UdpNmCarWakeUpBitPosition

- **UUID**: `bd4111f3-cc3d-43bf-918f-36474d481760`
- **参数名**: `UdpNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter specifies the Bit position of the Car Wake-Up Bit within the NM-PDU.

Note that this parameter has to be set to a value between 0 and 7.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

########## 6. UdpNmCarWakeUpBytePosition

- **UUID**: `ae83bc0d-b665-409f-97d3-19a0adf066a8`
- **参数名**: `UdpNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter specifies the Byte position of the Car Wake-Up Bit within the NM-PDU.

Note that this parameter has to be set to a valid byte position within the user data of the NM PDU.
If this setting is set to '0', the first byte of the NM PDU (not necessarily the first user data byte) is referred.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

########## 7. UdpNmCarWakeUpFilterNodeId

- **UUID**: `4ea9ed83-cfc7-4ac4-8abf-f6df43395cc8`
- **参数名**: `UdpNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the source node identifier for Car Wake-Up filtering. If Car Wake-Up filtering is supported, only the Car Wake-Up bit within the NM message with source node identifier 'UdpNmCarWakeUpFilterNodeId' is considered as Car Wake-Up request.

Note that this parameter has to be set to a value between 0x00 and 0xFF.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpFilterEnabled == True)

######### BOOLEAN 类型参数

########## 1. UdpNmPnEnabled

- **UUID**: `1d5bd864-8005-4e29-beeb-70c7cd2887ec`
- **参数名**: `UdpNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

false: Partial networking is not supported 
true: Partial networking supported

########## 2. UdpNmPnEraCalcEnabled

- **UUID**: `b84ea805-40cb-45fc-8893-0f336f32911f`
- **参数名**: `UdpNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm calculates the PN request information for external requests. (ERA)

false: PN request information for external requests is not calculated.
true: PN request information for external requests is calculated.

########## 3. UdpNmPnHandleMultipleNetworkRequests

- **UUID**: `ccb12947-d2cc-4597-839c-3e601c62305a`
- **参数名**: `UdpNmPnHandleMultipleNetworkRequests`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines whether UdpNm_NetworkRequest calls have an effect in Network Mode. If disabled UdpNm_NetworkRequest is ignored in Network Mode. If enabled UdpNm_NetworkRequest triggers a change from Network Mode to Repeat Message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPnEnabled == True)

########## 4. UdpNmAllNmMessagesKeepAwake

- **UUID**: `5dd9af87-0b59-4d4f-9f5b-3ba783e77c25`
- **参数名**: `UdpNmAllNmMessagesKeepAwake`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm drops irrelevant NM PDUs.

false: Only NM PDUs with a PNI bit = true and containing a PN request for this ECU triggers the standard RX indication handling 
true: Every NM PDU triggers the standard RX indication handling

RESTRICTIONS: This parameter is only relevant if UdpNmPnEnabled == True

########## 5. UdpNmCarWakeUpFilterEnabled

- **UUID**: `dee5e183-1657-46eb-ae68-6825a4eba8aa`
- **参数名**: `UdpNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if Car Wake-Up filtering is supported. Then only the Car Wake-Up bit within the NM message with source node identifier 'UdpNmCarWakeUpFilterNodeId' is considered as Car Wake-Up request.

false: Car Wake-up filtering is not supported
true: Car Wake-up filtering is supported

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

########## 6. UdpNmCarWakeUpRxEnabled

- **UUID**: `eeedb3bb-862a-429c-b053-c1f704acca89`
- **参数名**: `UdpNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if support of Car Wake-Up bit evaluation in received NM PDUs is enabled.
												
false: Car Wake-up is not supported
true: Car Wake-up is supported

########## 7. UdpNmActiveWakeupBitEnabled

- **UUID**: `f146949f-653e-4f03-aa9c-363827f24cec`
- **参数名**: `UdpNmActiveWakeupBitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the active wakeup bit is set in the CBV for this channel.

########## 8. UdpNmNodeIdEnabled

- **UUID**: `f2de1ce7-5dfb-4337-9ddc-d95b78b1231c`
- **参数名**: `UdpNmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter enables the source node identifier on the selected channel.
This option provides read access to the local node identifier and to the node identifier received in the last NM message.

RESTRICTIONS: If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled is disabled, this parameter must be disabled.

########## 9. UdpNmNodeDetectionEnabled

- **UUID**: `0013c174-d312-418d-a0c9-f6a811e4a97e`
- **参数名**: `UdpNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the node detection feature is enabled per channel.
If a Tester is present in the network 'UdpNmNodeDetectionEnabled' offers the opportunity to detect all present network nodes.


RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is false.
The feature can only be used on a channel if UdpNmPduNidPosition is not equal to UDPNM_PDU_OFF.
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled is disabled, this parameter must be disabled.

########## 10. UdpNmComControlEnabled

- **UUID**: `c2618c28-1f9e-44ac-8f03-ea10ea83d2c3`
- **参数名**: `UdpNmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the Communication Control support is enabled per channel.
If this option is enabled two additional APIs are available that can either enable or disable the transmission of Network Management messages in the Normal Operation state. While the transmission is disabled the network cannot be released.

RESTRICTIONS: If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled is disabled, this parameter must be disabled.

########## 11. UdpNmImmediateRestartEnabled

- **UUID**: `0709eaf9-6c7e-4374-8d57-bbaad1e8dd9a`
- **参数名**: `UdpNmImmediateRestartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the asynchronous transmission of an NM PDU upon bus-communication request in Prepare-Bus-Sleep mode is enabled per channel.
Enabling this option may lead to a burst of NM messages if all Nodes get a bus-communication request approximately at the same time.

RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is False
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled is disabled, this parameter must be disabled.

########## 12. UdpNmRepeatMsgIndEnabled

- **UUID**: `87a65acf-6ffd-4597-8ca9-7b64a2e4e879`
- **参数名**: `UdpNmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the notification that a RepeatMessageRequest bit has been received is enabled per channel.

This option enables a callback to the NM Interface whenever a state change due to a repeat message request or a repeat message bit occurs.


RESTRICTIONS: If (UdpNmNodeDetectionEnabled == false) then (UdpNmRepeatMsgIndEnabled = false).
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled is disabled, this parameter must be disabled.

########## 13. UdpNmRetryFirstMessageRequest

- **UUID**: `400ae136-28c1-4185-be54-2dcca3495465`
- **参数名**: `UdpNmRetryFirstMessageRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This pararmeter specifies if first message request in UdpNm is repeated until accepted by the SoAd.

RESTRICTION:
UdpNmRetryFirstMessageRequest = false if UdpNmPassiveModeEnabled == true

########## 14. UdpNmCriBitAlwaysEnabled

- **UUID**: `e06693fb-f3ea-4b34-972f-f22101ac3ab2`
- **参数名**: `UdpNmCriBitAlwaysEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When this feature is enabled, the CRI bit in the CBV byte is always enabled. Regardless of the configured Partial Network setting.

Note: The CRI bit is responsible to display if the current message contains PN info bytes and is usually only set if Partial Network is enabled.

########## 15. UdpNmSynchronizedPncShutdownEnabled

- **UUID**: `894964a0-35a1-46ca-8714-40ab128f703d`
- **参数名**: `UdpNmSynchronizedPncShutdownEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm handle PN shutdown messages to support a synchronized PNC shutdown across a PN topology. This is only used for ECUs in the role of a top-level PNC coordinator or intermediate PNC coordinator. Thus, the PNC gateway functionality is enabled and therefore ERA calculation is used.

FALSE: synchronized PNC shutdown is disabled
TRUE: synchronized PNC shutdown is enabled

######### FLOAT 类型参数

########## 1. UdpNmMainFunctionPeriod

- **UUID**: `8ff2b257-a56b-41b7-9b01-b9e062c9f7de`
- **参数名**: `UdpNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the period for the calls of UdpNm_MainFunction for this channel.

########## 2. UdpNmMsgCycleOffset

- **UUID**: `195e2fb7-4458-43b1-bfbe-2e4aca46dd0f`
- **参数名**: `UdpNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the offset in the periodic transmission node. It determines the start delay of the transmission.
Whenever the transmission of network management messages is started, the transmission start is delayed by this value.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

########## 3. UdpNmMsgCycleTime

- **UUID**: `6bcb71b2-27f7-4173-bbe2-9103b2cc4268`
- **参数名**: `UdpNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the period of a NM PDU. It determines the periodic rate and is the basis for transmit scheduling.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

########## 4. UdpNmMsgTimeoutTime

- **UUID**: `453fb7bc-7993-4758-ba61-b0b109c468a6`
- **参数名**: `UdpNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.06`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the transmission timeout of NM PDUs. If there is no transmission confirmation by the SoAd within this timeout, the UdpNm module shall give an error notification.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False). It should be a multiple of UdpNmMainFunctionPeriod and smaller than UdpNmMsgCycleTime.

########## 5. UdpNmRemoteSleepIndTime

- **UUID**: `2c90da0e-d825-4c94-be09-ae3e34a625fc`
- **参数名**: `UdpNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for Remote Sleep Indication.

Remote Sleep Indication is notified when the network node of the own ECU is the only one in the whole network that requests bus communication for this timing value.

Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of NM-Messages that are normally sent before Remote Sleep Indication is detected. 
The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the Remote Sleep Indication procedure. 

RESTRICTIONS: This parameter is only relevant if (UdpNmRemoteSleepIndEnabled == True)
If (UdpNmRemoteSleepIndEnabled == True) then (UdpNmRemoteSleepIndTime > 0)

########## 6. UdpNmRepeatMessageTime

- **UUID**: `6318692b-2cae-43ef-b442-416b31ba2a2e`
- **参数名**: `UdpNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for Repeat Message State.
It defines how long the NM shall stay in the Repeat Message State. Within Repeat Message State the NM messages are always transmitted cyclically.

Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of NM-Messages that are normally sent in the Repeat Message State. 
The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the node detection procedure.
The value 0 denotes that no Repeat Message State is configured. It means that Repeat Message State is transient what implicates that it is left immediately after entrance and in result, no start-up stability is guaranteed and no node detection procedure is possible.

If UdpNmPassiveModeEnabled == True, then a value of UdpNmRepeatMessageTime = 0 is forced.

########## 7. UdpNmTimeoutTime

- **UUID**: `062ced88-152e-452b-b9db-614fa1590266`
- **参数名**: `UdpNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.002..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the Network Timeout for the reception and transmission of network management messages.
If in Network Mode (Repeat Message State, Normal Operation State or Ready Sleep State) your network node does not require the communication bus anymore and no more NM messages are received within this time 'Prepare Bus-Sleep' is entered.

It shall be equal for all nodes in the cluster. It shall be greater than 'UdpNmMsgCycleTime'.
Typically it should be equal to n * UdpNmMsgCycleTime, where n denotes the number of NM-Message cycle times in the Ready Sleep State before transition into the Bus-Sleep Mode is initiated. The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the coordination algorithm.

########## 8. UdpNmWaitBusSleepTime

- **UUID**: `01f916cb-395d-4881-9ca8-73f31b757485`
- **参数名**: `UdpNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.75`
- **取值范围**: [0.001..4294967.295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for bus calm down phase (Prepare Bus-Sleep Mode).
The bus calm down period is a safety zone between bus-communication of application messages and shutdown of the communication bus.

It shall be equal for all nodes in the cluster. It shall be long enough to make all Tx-buffers empty.

########## 9. UdpNmImmediateNmCycleTime

- **UUID**: `a0834197-ac16-408e-ab79-19c8facad750`
- **参数名**: `UdpNmImmediateNmCycleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the immediate NM PDU cycle time which is used for 'UdpNmImmediateNmTransmissions' NM PDU transmissions. This parameter is only valid if 'UdpNmImmediateNmTransmissions' is greater than one.

######### ENUMERATION 类型参数

########## 1. UdpNmPduCbvPosition

- **UUID**: `f7e21e13-dc85-4e9b-b3f7-443fc9f5d982`
- **参数名**: `UdpNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UDPNM_PDU_OFF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the position of the control bit vector within the NM PDU.
The value of the parameter represents the location of the control bit vector in the NM PDU (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the Control Bit Vector is not part of the NM PDU).

RESTRICTIONS: If (UdpNmPduCbvPosition != UDPNM_PDU_OFF) then (UdpNmPduCbvPosition != UdpNmPduNidPosition) and (UdpNmPduLength >= UdpNmPduCbvPosition).
If (UdpNmPduNidPosition == UDPNM_PDU_OFF) then (UdpNmPduCbvPosition != UDPNM_PDU_BYTE_1).

########## 2. UdpNmPduNidPosition

- **UUID**: `85aa8ef7-7d44-4a0c-9d90-584305bbc295`
- **参数名**: `UdpNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UDPNM_PDU_OFF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the position of the source node identifier within the NM PDU.
The value of the parameter represents the location of the source node identifier in the NM PDU (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the source node identifier is not part of the NM PDU).

RESTRICTIONS: If (UdpNmPduNidPosition != UDPNM_PDU_OFF) then (UdpNmPduNidPosition != UdpNmPduCbvPosition) and (UdpNmPduLength >= UdpNmPduNidPosition).
If (UdpNmPduCbvPosition == UDPNM_PDU_OFF) then (UdpNmPduNidPosition != UDPNM_PDU_BYTE_1).

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmPnEraRxNSduRef

- **UUID**: `7acc9b5a-a452-432f-9bec-c82a0da3a298`
- **引用名**: `UdpNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to a Pdu in the COM-Stack. The SduRef is required for every UdpNm Channel, because ERA is reported per channel.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. UdpNmComMNetworkHandleRef

- **UUID**: `25348c3e-db73-4cff-8852-de2cb0143486`
- **引用名**: `UdpNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to the unique channel defined by the ComMChannel. It provides access to the unique channel index value in ComMChannelId.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. UdpNmRxPdu

**容器属性**:

- **UUID**: `f5578415-ef15-47d5-ae00-8211f6c0f381`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Rx PDU properties that are used for the UdpNm Channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmRxPduId

- **UUID**: `1aeb86b5-ace5-4083-a2e1-0fe52794b49d`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmRxPduRef

- **UUID**: `e928525d-e21a-48cd-b4c4-1967a628d229`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

######### 2. UdpNmTxPdu

**容器属性**:

- **UUID**: `4a509b81-4a24-42a6-b845-5d237e56eca0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Tx PDU properties that are used for the UdpNm Channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmTxConfirmationPduId

- **UUID**: `b8d58a6f-11e8-49ad-99d5-92cd1d9318ee`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmTxPduRef

- **UUID**: `89e41478-3cca-41dc-b214-3bb03598524f`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

######### 3. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `e6a224d0-eb57-44ee-9256-2bed9bf47d27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmTxUserDataPduId

- **UUID**: `6dfce2e0-3abc-4f83-8c7a-caa405658100`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

########### BOOLEAN 类型参数

############ 1. UdpNmAllowTriggeredMsgTransmission

- **UUID**: `7d4e88c7-90ce-48d9-aaab-5c84c6cff2f9`
- **参数名**: `UdpNmAllowTriggeredMsgTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if changes written to the User Data Pdu triggers an immediate transmission of the NM message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. UdpNmTxUserDataPduRef

- **UUID**: `59fad910-8b9b-425e-88cd-75d9c282bab1`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

####### 2. UdpNmRxPdu

**容器属性**:

- **UUID**: `f5578415-ef15-47d5-ae00-8211f6c0f381`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Rx PDU properties that are used for the UdpNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmRxPduId

- **UUID**: `1aeb86b5-ace5-4083-a2e1-0fe52794b49d`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmRxPduRef

- **UUID**: `e928525d-e21a-48cd-b4c4-1967a628d229`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 3. UdpNmTxPdu

**容器属性**:

- **UUID**: `4a509b81-4a24-42a6-b845-5d237e56eca0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Tx PDU properties that are used for the UdpNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxConfirmationPduId

- **UUID**: `b8d58a6f-11e8-49ad-99d5-92cd1d9318ee`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxPduRef

- **UUID**: `89e41478-3cca-41dc-b214-3bb03598524f`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

####### 4. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `e6a224d0-eb57-44ee-9256-2bed9bf47d27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxUserDataPduId

- **UUID**: `6dfce2e0-3abc-4f83-8c7a-caa405658100`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

######### BOOLEAN 类型参数

########## 1. UdpNmAllowTriggeredMsgTransmission

- **UUID**: `7d4e88c7-90ce-48d9-aaab-5c84c6cff2f9`
- **参数名**: `UdpNmAllowTriggeredMsgTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if changes written to the User Data Pdu triggers an immediate transmission of the NM message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxUserDataPduRef

- **UUID**: `59fad910-8b9b-425e-88cd-75d9c282bab1`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

####### 5. UdpNmPnInfo

**容器属性**:

- **UUID**: `e2904c70-1684-4273-9fef-553007c95b4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnInfo`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN information configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmPnInfoLength

- **UUID**: `3000c78a-b8c6-44ef-b14e-d2f7d3e73dd1`
- **参数名**: `UdpNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies the length of the PN request information in the NM message.

Note that this parameter has to be set to a value less or equal to user data length.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
This parameter cannot be edited directly in DaVinci Configurator. To change its value, add or remove UdpNmPnFilterMaskByte containers.

########## 2. UdpNmPnInfoOffset

- **UUID**: `3998dc32-a90e-45ed-8346-ecd1da90c273`
- **参数名**: `UdpNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

Note that this parameter has to be set to a valid byte position within the user data of the NM PDU.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. UdpNmPnFilterMaskByte

**容器属性**:

- **UUID**: `b7e2d735-d1de-484b-841c-999975036d55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnFilterMaskByte`
- **多重性**: [0..63]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN filter mask configuration.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. UdpNmPnFilterMaskByteIndex

- **UUID**: `97e63f13-6ec0-4ae3-81ee-6f616e026b33`
- **参数名**: `UdpNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..62]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

############ 2. UdpNmPnFilterMaskByteValue

- **UUID**: `38a4b673-b076-43ed-a543-9f498f6b76ee`
- **参数名**: `UdpNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the filter mask byte.
This parameter defines the value of the mask byte which is used for the filter algorithm for relevant NM messages.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

####### 6. UdpNmPnFilterMaskByte

**容器属性**:

- **UUID**: `b7e2d735-d1de-484b-841c-999975036d55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnFilterMaskByte`
- **多重性**: [0..63]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN filter mask configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmPnFilterMaskByteIndex

- **UUID**: `97e63f13-6ec0-4ae3-81ee-6f616e026b33`
- **参数名**: `UdpNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..62]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

########## 2. UdpNmPnFilterMaskByteValue

- **UUID**: `38a4b673-b076-43ed-a543-9f498f6b76ee`
- **参数名**: `UdpNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the filter mask byte.
This parameter defines the value of the mask byte which is used for the filter algorithm for relevant NM messages.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

####### 7. UdpNmGeneration

**容器属性**:

- **UUID**: `72833978-d652-4098-b59b-2ac364524fb8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false
- **需要索引**: false

**容器描述**:

Contains the generation configuration parameters of the module UdpNm.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. UdpNmOutOfBoundsWriteSanitizer

- **UUID**: `0457481c-32d3-4fac-b077-c2491652a03c`
- **参数名**: `UdpNmOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 2. UdpNmOutOfBoundsReadSanitizer

- **UUID**: `e4442d5a-ef7e-486e-921f-8765d937e86d`
- **参数名**: `UdpNmOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 3. UdpNmInterfacesForDeactivatedData

- **UUID**: `ffe8a4d4-1d5c-471d-b0ef-eeca24c6e443`
- **参数名**: `UdpNmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

####### 8. UdpNmDemEventParameterRefs

**容器属性**:

- **UUID**: `8224c7a5-bcc9-46c8-bab7-bc850b838573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

not used

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. UDPNM_E_NETWORK_TIMEOUT

- **UUID**: `8cd403cc-312e-4b23-98f9-d0739fada14c`
- **引用名**: `UDPNM_E_NETWORK_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

########## 2. UDPNM_E_TCPIP_TRANSMIT_ERROR

- **UUID**: `11be4b2e-1d18-4c6d-9065-39c6c6c93212`
- **引用名**: `UDPNM_E_TCPIP_TRANSMIT_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

##### 2. UdpNmChannelConfig

**容器属性**:

- **UUID**: `c024afe1-cd82-41d8-b750-2d6aabf37412`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmChannelConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the channel specific configuration parameter of the UdpNm.

###### 参数配置

此容器包含 **33** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmNodeId

- **UUID**: `8e0cd2be-398b-4103-8620-5e002b1d334b`
- **参数名**: `UdpNmNodeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the node identifier of local node.

The 'NodeId' is transmitted within the network management message if UdpNmPduNidPosition != UDPNM_PDU_OFF)

The node identifier is used for the detection of present nodes and can be read by the application at any time.

Note: This value is transmitted within the NM message.

######## 2. UdpNmPduLength

- **UUID**: `63f48c13-fd3c-4239-9773-7b2a476520fb`
- **参数名**: `UdpNmPduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the length of the NM PDU.

The value is auto-calculated dependent on 'UdpNmPduCbvPosition', 'UdpNmPduNidPosition' and 'UdpNmUserDataLength'.

According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like specified in AUTOSAR SWS (last released version 4.2.2). Therefore it is possible to use PDUs larger than 8 Byte.

######## 3. UdpNmUserDataLength

- **UUID**: `51b917dd-4885-4326-9815-a059af9154cf`
- **参数名**: `UdpNmUserDataLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the length of the user data contained in the NM PDU.

According to AUTOSAR RfC 70333 the PDU Length shall not be restricted to 8 Byte anymore like specified in AUTOSAR SWS (last released version 4.2.2). Therefore the User Data Length is extended in line with the extension of the PDU Length.

######## 4. UdpNmImmediateNmTransmissions

- **UUID**: `dec4a6bf-1161-44af-8048-66ccc86e3212`
- **参数名**: `UdpNmImmediateNmTransmissions`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the number of immediate NM PDUs which shall be transmitted. If the value is zero no immediate NM PDUs are transmitted. The cycle time of immediate NM PDUs is defined by UdpNmImmediateNmCycleTime.

######## 5. UdpNmCarWakeUpBitPosition

- **UUID**: `bd4111f3-cc3d-43bf-918f-36474d481760`
- **参数名**: `UdpNmCarWakeUpBitPosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter specifies the Bit position of the Car Wake-Up Bit within the NM-PDU.

Note that this parameter has to be set to a value between 0 and 7.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

######## 6. UdpNmCarWakeUpBytePosition

- **UUID**: `ae83bc0d-b665-409f-97d3-19a0adf066a8`
- **参数名**: `UdpNmCarWakeUpBytePosition`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter specifies the Byte position of the Car Wake-Up Bit within the NM-PDU.

Note that this parameter has to be set to a valid byte position within the user data of the NM PDU.
If this setting is set to '0', the first byte of the NM PDU (not necessarily the first user data byte) is referred.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

######## 7. UdpNmCarWakeUpFilterNodeId

- **UUID**: `4ea9ed83-cfc7-4ac4-8abf-f6df43395cc8`
- **参数名**: `UdpNmCarWakeUpFilterNodeId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the source node identifier for Car Wake-Up filtering. If Car Wake-Up filtering is supported, only the Car Wake-Up bit within the NM message with source node identifier 'UdpNmCarWakeUpFilterNodeId' is considered as Car Wake-Up request.

Note that this parameter has to be set to a value between 0x00 and 0xFF.

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpFilterEnabled == True)

####### BOOLEAN 类型参数

######## 1. UdpNmPnEnabled

- **UUID**: `1d5bd864-8005-4e29-beeb-70c7cd2887ec`
- **参数名**: `UdpNmPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables or disables support of partial networking.

false: Partial networking is not supported 
true: Partial networking supported

######## 2. UdpNmPnEraCalcEnabled

- **UUID**: `b84ea805-40cb-45fc-8893-0f336f32911f`
- **参数名**: `UdpNmPnEraCalcEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm calculates the PN request information for external requests. (ERA)

false: PN request information for external requests is not calculated.
true: PN request information for external requests is calculated.

######## 3. UdpNmPnHandleMultipleNetworkRequests

- **UUID**: `ccb12947-d2cc-4597-839c-3e601c62305a`
- **参数名**: `UdpNmPnHandleMultipleNetworkRequests`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines whether UdpNm_NetworkRequest calls have an effect in Network Mode. If disabled UdpNm_NetworkRequest is ignored in Network Mode. If enabled UdpNm_NetworkRequest triggers a change from Network Mode to Repeat Message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPnEnabled == True)

######## 4. UdpNmAllNmMessagesKeepAwake

- **UUID**: `5dd9af87-0b59-4d4f-9f5b-3ba783e77c25`
- **参数名**: `UdpNmAllNmMessagesKeepAwake`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm drops irrelevant NM PDUs.

false: Only NM PDUs with a PNI bit = true and containing a PN request for this ECU triggers the standard RX indication handling 
true: Every NM PDU triggers the standard RX indication handling

RESTRICTIONS: This parameter is only relevant if UdpNmPnEnabled == True

######## 5. UdpNmCarWakeUpFilterEnabled

- **UUID**: `dee5e183-1657-46eb-ae68-6825a4eba8aa`
- **参数名**: `UdpNmCarWakeUpFilterEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if Car Wake-Up filtering is supported. Then only the Car Wake-Up bit within the NM message with source node identifier 'UdpNmCarWakeUpFilterNodeId' is considered as Car Wake-Up request.

false: Car Wake-up filtering is not supported
true: Car Wake-up filtering is supported

RESTRICTIONS: This parameter is only relevant if (UdpNmCarWakeUpRxEnabled == True)

######## 6. UdpNmCarWakeUpRxEnabled

- **UUID**: `eeedb3bb-862a-429c-b053-c1f704acca89`
- **参数名**: `UdpNmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if support of Car Wake-Up bit evaluation in received NM PDUs is enabled.
												
false: Car Wake-up is not supported
true: Car Wake-up is supported

######## 7. UdpNmActiveWakeupBitEnabled

- **UUID**: `f146949f-653e-4f03-aa9c-363827f24cec`
- **参数名**: `UdpNmActiveWakeupBitEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the active wakeup bit is set in the CBV for this channel.

######## 8. UdpNmNodeIdEnabled

- **UUID**: `f2de1ce7-5dfb-4337-9ddc-d95b78b1231c`
- **参数名**: `UdpNmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter enables the source node identifier on the selected channel.
This option provides read access to the local node identifier and to the node identifier received in the last NM message.

RESTRICTIONS: If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeIdEnabled is disabled, this parameter must be disabled.

######## 9. UdpNmNodeDetectionEnabled

- **UUID**: `0013c174-d312-418d-a0c9-f6a811e4a97e`
- **参数名**: `UdpNmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the node detection feature is enabled per channel.
If a Tester is present in the network 'UdpNmNodeDetectionEnabled' offers the opportunity to detect all present network nodes.


RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is false.
The feature can only be used on a channel if UdpNmPduNidPosition is not equal to UDPNM_PDU_OFF.
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmNodeDetectionEnabled is disabled, this parameter must be disabled.

######## 10. UdpNmComControlEnabled

- **UUID**: `c2618c28-1f9e-44ac-8f03-ea10ea83d2c3`
- **参数名**: `UdpNmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the Communication Control support is enabled per channel.
If this option is enabled two additional APIs are available that can either enable or disable the transmission of Network Management messages in the Normal Operation state. While the transmission is disabled the network cannot be released.

RESTRICTIONS: If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmComControlEnabled is disabled, this parameter must be disabled.

######## 11. UdpNmImmediateRestartEnabled

- **UUID**: `0709eaf9-6c7e-4374-8d57-bbaad1e8dd9a`
- **参数名**: `UdpNmImmediateRestartEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the asynchronous transmission of an NM PDU upon bus-communication request in Prepare-Bus-Sleep mode is enabled per channel.
Enabling this option may lead to a burst of NM messages if all Nodes get a bus-communication request approximately at the same time.

RESTRICTIONS: This parameter is only relevant if 'UdpNmPassiveModeEnabled' is False
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmImmediateRestartEnabled is disabled, this parameter must be disabled.

######## 12. UdpNmRepeatMsgIndEnabled

- **UUID**: `87a65acf-6ffd-4597-8ca9-7b64a2e4e879`
- **参数名**: `UdpNmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines if the notification that a RepeatMessageRequest bit has been received is enabled per channel.

This option enables a callback to the NM Interface whenever a state change due to a repeat message request or a repeat message bit occurs.


RESTRICTIONS: If (UdpNmNodeDetectionEnabled == false) then (UdpNmRepeatMsgIndEnabled = false).
If this parameter is enabled, the global parameter /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled must be enabled.
If /MICROSAR/UdpNm/UdpNmGlobalConfig/UdpNmRepeatMsgIndEnabled is disabled, this parameter must be disabled.

######## 13. UdpNmRetryFirstMessageRequest

- **UUID**: `400ae136-28c1-4185-be54-2dcca3495465`
- **参数名**: `UdpNmRetryFirstMessageRequest`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This pararmeter specifies if first message request in UdpNm is repeated until accepted by the SoAd.

RESTRICTION:
UdpNmRetryFirstMessageRequest = false if UdpNmPassiveModeEnabled == true

######## 14. UdpNmCriBitAlwaysEnabled

- **UUID**: `e06693fb-f3ea-4b34-972f-f22101ac3ab2`
- **参数名**: `UdpNmCriBitAlwaysEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: When this feature is enabled, the CRI bit in the CBV byte is always enabled. Regardless of the configured Partial Network setting.

Note: The CRI bit is responsible to display if the current message contains PN info bytes and is usually only set if Partial Network is enabled.

######## 15. UdpNmSynchronizedPncShutdownEnabled

- **UUID**: `894964a0-35a1-46ca-8714-40ab128f703d`
- **参数名**: `UdpNmSynchronizedPncShutdownEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies if UdpNm handle PN shutdown messages to support a synchronized PNC shutdown across a PN topology. This is only used for ECUs in the role of a top-level PNC coordinator or intermediate PNC coordinator. Thus, the PNC gateway functionality is enabled and therefore ERA calculation is used.

FALSE: synchronized PNC shutdown is disabled
TRUE: synchronized PNC shutdown is enabled

####### FLOAT 类型参数

######## 1. UdpNmMainFunctionPeriod

- **UUID**: `8ff2b257-a56b-41b7-9b01-b9e062c9f7de`
- **参数名**: `UdpNmMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the period for the calls of UdpNm_MainFunction for this channel.

######## 2. UdpNmMsgCycleOffset

- **UUID**: `195e2fb7-4458-43b1-bfbe-2e4aca46dd0f`
- **参数名**: `UdpNmMsgCycleOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the offset in the periodic transmission node. It determines the start delay of the transmission.
Whenever the transmission of network management messages is started, the transmission start is delayed by this value.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

######## 3. UdpNmMsgCycleTime

- **UUID**: `6bcb71b2-27f7-4173-bbe2-9103b2cc4268`
- **参数名**: `UdpNmMsgCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the period of a NM PDU. It determines the periodic rate and is the basis for transmit scheduling.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

######## 4. UdpNmMsgTimeoutTime

- **UUID**: `453fb7bc-7993-4758-ba61-b0b109c468a6`
- **参数名**: `UdpNmMsgTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.06`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the transmission timeout of NM PDUs. If there is no transmission confirmation by the SoAd within this timeout, the UdpNm module shall give an error notification.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False). It should be a multiple of UdpNmMainFunctionPeriod and smaller than UdpNmMsgCycleTime.

######## 5. UdpNmRemoteSleepIndTime

- **UUID**: `2c90da0e-d825-4c94-be09-ae3e34a625fc`
- **参数名**: `UdpNmRemoteSleepIndTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for Remote Sleep Indication.

Remote Sleep Indication is notified when the network node of the own ECU is the only one in the whole network that requests bus communication for this timing value.

Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of NM-Messages that are normally sent before Remote Sleep Indication is detected. 
The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the Remote Sleep Indication procedure. 

RESTRICTIONS: This parameter is only relevant if (UdpNmRemoteSleepIndEnabled == True)
If (UdpNmRemoteSleepIndEnabled == True) then (UdpNmRemoteSleepIndTime > 0)

######## 6. UdpNmRepeatMessageTime

- **UUID**: `6318692b-2cae-43ef-b442-416b31ba2a2e`
- **参数名**: `UdpNmRepeatMessageTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.4`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for Repeat Message State.
It defines how long the NM shall stay in the Repeat Message State. Within Repeat Message State the NM messages are always transmitted cyclically.

Typically it should be equal to: n * UdpNmMsgCycleTime, where n denotes the number of NM-Messages that are normally sent in the Repeat Message State. 
The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the node detection procedure.
The value 0 denotes that no Repeat Message State is configured. It means that Repeat Message State is transient what implicates that it is left immediately after entrance and in result, no start-up stability is guaranteed and no node detection procedure is possible.

If UdpNmPassiveModeEnabled == True, then a value of UdpNmRepeatMessageTime = 0 is forced.

######## 7. UdpNmTimeoutTime

- **UUID**: `062ced88-152e-452b-b9db-614fa1590266`
- **参数名**: `UdpNmTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0.002..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the Network Timeout for the reception and transmission of network management messages.
If in Network Mode (Repeat Message State, Normal Operation State or Ready Sleep State) your network node does not require the communication bus anymore and no more NM messages are received within this time 'Prepare Bus-Sleep' is entered.

It shall be equal for all nodes in the cluster. It shall be greater than 'UdpNmMsgCycleTime'.
Typically it should be equal to n * UdpNmMsgCycleTime, where n denotes the number of NM-Message cycle times in the Ready Sleep State before transition into the Bus-Sleep Mode is initiated. The value of n decremented by one determines the amount of lost NM-Messages that can be tolerated by the coordination algorithm.

######## 8. UdpNmWaitBusSleepTime

- **UUID**: `01f916cb-395d-4881-9ca8-73f31b757485`
- **参数名**: `UdpNmWaitBusSleepTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.75`
- **取值范围**: [0.001..4294967.295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the timeout for bus calm down phase (Prepare Bus-Sleep Mode).
The bus calm down period is a safety zone between bus-communication of application messages and shutdown of the communication bus.

It shall be equal for all nodes in the cluster. It shall be long enough to make all Tx-buffers empty.

######## 9. UdpNmImmediateNmCycleTime

- **UUID**: `a0834197-ac16-408e-ab79-19c8facad750`
- **参数名**: `UdpNmImmediateNmCycleTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..65.535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the immediate NM PDU cycle time which is used for 'UdpNmImmediateNmTransmissions' NM PDU transmissions. This parameter is only valid if 'UdpNmImmediateNmTransmissions' is greater than one.

####### ENUMERATION 类型参数

######## 1. UdpNmPduCbvPosition

- **UUID**: `f7e21e13-dc85-4e9b-b3f7-443fc9f5d982`
- **参数名**: `UdpNmPduCbvPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UDPNM_PDU_OFF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the position of the control bit vector within the NM PDU.
The value of the parameter represents the location of the control bit vector in the NM PDU (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the Control Bit Vector is not part of the NM PDU).

RESTRICTIONS: If (UdpNmPduCbvPosition != UDPNM_PDU_OFF) then (UdpNmPduCbvPosition != UdpNmPduNidPosition) and (UdpNmPduLength >= UdpNmPduCbvPosition).
If (UdpNmPduNidPosition == UDPNM_PDU_OFF) then (UdpNmPduCbvPosition != UDPNM_PDU_BYTE_1).

######## 2. UdpNmPduNidPosition

- **UUID**: `85aa8ef7-7d44-4a0c-9d90-584305bbc295`
- **参数名**: `UdpNmPduNidPosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `UDPNM_PDU_OFF`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `UDPNM_PDU_BYTE_0` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_BYTE_1` (来源: AUTOSAR_ECUC)
  - `UDPNM_PDU_OFF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This value specifies the position of the source node identifier within the NM PDU.
The value of the parameter represents the location of the source node identifier in the NM PDU (UDPNM_PDU_BYTE_0 means byte 0, UDPNM_PDU_BYTE_1 means byte 1, UDPNM_PDU_OFF means that the source node identifier is not part of the NM PDU).

RESTRICTIONS: If (UdpNmPduNidPosition != UDPNM_PDU_OFF) then (UdpNmPduNidPosition != UdpNmPduCbvPosition) and (UdpNmPduLength >= UdpNmPduNidPosition).
If (UdpNmPduCbvPosition == UDPNM_PDU_OFF) then (UdpNmPduNidPosition != UDPNM_PDU_BYTE_1).

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmPnEraRxNSduRef

- **UUID**: `7acc9b5a-a452-432f-9bec-c82a0da3a298`
- **引用名**: `UdpNmPnEraRxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to a Pdu in the COM-Stack. The SduRef is required for every UdpNm Channel, because ERA is reported per channel.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. UdpNmComMNetworkHandleRef

- **UUID**: `25348c3e-db73-4cff-8852-de2cb0143486`
- **引用名**: `UdpNmComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Reference to the unique channel defined by the ComMChannel. It provides access to the unique channel index value in ComMChannelId.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. UdpNmRxPdu

**容器属性**:

- **UUID**: `f5578415-ef15-47d5-ae00-8211f6c0f381`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Rx PDU properties that are used for the UdpNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmRxPduId

- **UUID**: `1aeb86b5-ace5-4083-a2e1-0fe52794b49d`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmRxPduRef

- **UUID**: `e928525d-e21a-48cd-b4c4-1967a628d229`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

####### 2. UdpNmTxPdu

**容器属性**:

- **UUID**: `4a509b81-4a24-42a6-b845-5d237e56eca0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Tx PDU properties that are used for the UdpNm Channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxConfirmationPduId

- **UUID**: `b8d58a6f-11e8-49ad-99d5-92cd1d9318ee`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxPduRef

- **UUID**: `89e41478-3cca-41dc-b214-3bb03598524f`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

####### 3. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `e6a224d0-eb57-44ee-9256-2bed9bf47d27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmTxUserDataPduId

- **UUID**: `6dfce2e0-3abc-4f83-8c7a-caa405658100`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

######### BOOLEAN 类型参数

########## 1. UdpNmAllowTriggeredMsgTransmission

- **UUID**: `7d4e88c7-90ce-48d9-aaab-5c84c6cff2f9`
- **参数名**: `UdpNmAllowTriggeredMsgTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if changes written to the User Data Pdu triggers an immediate transmission of the NM message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. UdpNmTxUserDataPduRef

- **UUID**: `59fad910-8b9b-425e-88cd-75d9c282bab1`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

##### 3. UdpNmRxPdu

**容器属性**:

- **UUID**: `f5578415-ef15-47d5-ae00-8211f6c0f381`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmRxPdu`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Rx PDU properties that are used for the UdpNm Channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmRxPduId

- **UUID**: `1aeb86b5-ace5-4083-a2e1-0fe52794b49d`
- **参数名**: `UdpNmRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: ID of the RxPdu that will be used by a RxIndication of the lower layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmRxPduRef

- **UUID**: `e928525d-e21a-48cd-b4c4-1967a628d229`
- **引用名**: `UdpNmRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

##### 4. UdpNmTxPdu

**容器属性**:

- **UUID**: `4a509b81-4a24-42a6-b845-5d237e56eca0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration of Tx PDU properties that are used for the UdpNm Channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmTxConfirmationPduId

- **UUID**: `b8d58a6f-11e8-49ad-99d5-92cd1d9318ee`
- **参数名**: `UdpNmTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmTxPduRef

- **UUID**: `89e41478-3cca-41dc-b214-3bb03598524f`
- **引用名**: `UdpNmTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The reference to a PDU in the global PDU structure described in the AUTOSAR ECU Configuration Specification. This reference will be used by the UdpNm module to derive the PDU Id.

RESTRICTIONS: This parameter is only relevant if UdpNmPassiveModeEnabled = False.

##### 5. UdpNmUserDataTxPdu

**容器属性**:

- **UUID**: `e6a224d0-eb57-44ee-9256-2bed9bf47d27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmUserDataTxPdu`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This optional container is used to configure the UserNm PDU. This container is only available if UdpNmComUserDataSupport is enabled.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmTxUserDataPduId

- **UUID**: `6dfce2e0-3abc-4f83-8c7a-caa405658100`
- **参数名**: `UdpNmTxUserDataPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter defines the Handle ID of the NM User Data I-PDU.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

####### BOOLEAN 类型参数

######## 1. UdpNmAllowTriggeredMsgTransmission

- **UUID**: `7d4e88c7-90ce-48d9-aaab-5c84c6cff2f9`
- **参数名**: `UdpNmAllowTriggeredMsgTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if changes written to the User Data Pdu triggers an immediate transmission of the NM message.

RESTRICTIONS: This parameter is only relevant if (UdpNmPassiveModeEnabled == False)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. UdpNmTxUserDataPduRef

- **UUID**: `59fad910-8b9b-425e-88cd-75d9c282bab1`
- **引用名**: `UdpNmTxUserDataPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the NM User Data I-PDU in the global PDU collection.

RESTRICTIONS: This parameter is only relevant if UdpNmComUserDataSupport = True.

##### 6. UdpNmPnInfo

**容器属性**:

- **UUID**: `e2904c70-1684-4273-9fef-553007c95b4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnInfo`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN information configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmPnInfoLength

- **UUID**: `3000c78a-b8c6-44ef-b14e-d2f7d3e73dd1`
- **参数名**: `UdpNmPnInfoLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: Specifies the length of the PN request information in the NM message.

Note that this parameter has to be set to a value less or equal to user data length.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.
This parameter cannot be edited directly in DaVinci Configurator. To change its value, add or remove UdpNmPnFilterMaskByte containers.

######## 2. UdpNmPnInfoOffset

- **UUID**: `3998dc32-a90e-45ed-8346-ecd1da90c273`
- **参数名**: `UdpNmPnInfoOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..63]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

Note that this parameter has to be set to a valid byte position within the user data of the NM PDU.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. UdpNmPnFilterMaskByte

**容器属性**:

- **UUID**: `b7e2d735-d1de-484b-841c-999975036d55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnFilterMaskByte`
- **多重性**: [0..63]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN filter mask configuration.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. UdpNmPnFilterMaskByteIndex

- **UUID**: `97e63f13-6ec0-4ae3-81ee-6f616e026b33`
- **参数名**: `UdpNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..62]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

########## 2. UdpNmPnFilterMaskByteValue

- **UUID**: `38a4b673-b076-43ed-a543-9f498f6b76ee`
- **参数名**: `UdpNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the filter mask byte.
This parameter defines the value of the mask byte which is used for the filter algorithm for relevant NM messages.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

##### 7. UdpNmPnFilterMaskByte

**容器属性**:

- **UUID**: `b7e2d735-d1de-484b-841c-999975036d55`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmPnFilterMaskByte`
- **多重性**: [0..63]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This container includes the PN filter mask configuration.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. UdpNmPnFilterMaskByteIndex

- **UUID**: `97e63f13-6ec0-4ae3-81ee-6f616e026b33`
- **参数名**: `UdpNmPnFilterMaskByteIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..62]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the offset of the PN request information in the NM message.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

######## 2. UdpNmPnFilterMaskByteValue

- **UUID**: `38a4b673-b076-43ed-a543-9f498f6b76ee`
- **参数名**: `UdpNmPnFilterMaskByteValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the filter mask byte.
This parameter defines the value of the mask byte which is used for the filter algorithm for relevant NM messages.

RESTRICTIONS: This parameter is only valid if (UdpNmPnEnabled == True) for at least one channel.

##### 8. UdpNmGeneration

**容器属性**:

- **UUID**: `72833978-d652-4098-b59b-2ac364524fb8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false
- **需要索引**: false

**容器描述**:

Contains the generation configuration parameters of the module UdpNm.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. UdpNmOutOfBoundsWriteSanitizer

- **UUID**: `0457481c-32d3-4fac-b077-c2491652a03c`
- **参数名**: `UdpNmOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. UdpNmOutOfBoundsReadSanitizer

- **UUID**: `e4442d5a-ef7e-486e-921f-8765d937e86d`
- **参数名**: `UdpNmOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. UdpNmInterfacesForDeactivatedData

- **UUID**: `ffe8a4d4-1d5c-471d-b0ef-eeca24c6e443`
- **参数名**: `UdpNmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

##### 9. UdpNmDemEventParameterRefs

**容器属性**:

- **UUID**: `8224c7a5-bcc9-46c8-bab7-bc850b838573`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `UdpNmDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

not used

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. UDPNM_E_NETWORK_TIMEOUT

- **UUID**: `8cd403cc-312e-4b23-98f9-d0739fada14c`
- **引用名**: `UDPNM_E_NETWORK_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

######## 2. UDPNM_E_TCPIP_TRANSMIT_ERROR

- **UUID**: `11be4b2e-1d18-4c6d-9065-39c6c6c93212`
- **引用名**: `UDPNM_E_TCPIP_TRANSMIT_ERROR`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
- **描述**: not used

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **UdpNm**

##### BSW-IMPLEMENTATION 类型元素

1. **UdpNm_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **UdpNm_Pre**
2. **UdpNm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. UdpNm_Impl

- **UUID**: `a0e9b114-469d-41cf-9486-861f0d36eaf1`
- **实现名称**: `UdpNm_Impl`
- **编程语言**: C
- **软件版本**: 7.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.01.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. UdpNm_Pre

- **UUID**: `56e1cb95-7d8f-46ba-b26b-35d13bb591ea`
- **配置名称**: `UdpNm_Pre`
- **定义引用**: `/MICROSAR/UdpNm`

### 2. UdpNm_Rec

- **UUID**: `0f855377-255e-491b-a0d5-6a1c5037ca79`
- **配置名称**: `UdpNm_Rec`
- **定义引用**: `/MICROSAR/UdpNm`
