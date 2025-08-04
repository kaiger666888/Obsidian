# Nm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:23

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Nm](#nm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Nm

#### 基本信息

- **UUID**: `9a8e0bc9-60f8-4ecc-8412-3abf411cb25e`
- **模块名称**: `Nm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Network Management Interface (NmIf). The NmIf acts as an adaption layer between AUTOSAR BSW module ComM and the AUTOSAR BSW bus-specific network management modules (e.g. CanNm). The NmIf also provides a coordination algorithm to perform a synchronous shutdown handling of several connected networks and/or multiple BusNms on one channel.
#Interface #forwarding #NetworkManagement #ModeManagement #Shutdown #NM #BusSleep
#AUTOSAR

#### 版本历史

共有 **27** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2011-02-03T13:05:50+01:00
- **发布者**: vismdr

**变更内容**:

##### 2. 版本 2.00.00

- **状态**: released
- **发布日期**: 2012-04-16T09:56:45+02:00
- **发布者**: vismdr, visrpp

**变更内容**:

##### 3. 版本 2.00.01

- **状态**: released
- **发布日期**: 2012-11-08T10:01:47+01:00
- **发布者**: vismdr

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2013-03-04T09:16:44+01:00
- **发布者**: vismdr

**变更内容**:

##### 5. 版本 3.00.00

- **状态**: released
- **发布日期**: 2013-07-01T08:07:41+02:00
- **发布者**: vismdr

**变更内容**:

##### 6. 版本 3.01.00

- **状态**: released
- **发布日期**: 2013-11-05T08:47:28+01:00
- **发布者**: vismdr

**变更内容**:

##### 7. 版本 4.00.00

- **状态**: released
- **发布日期**: 2013-11-18T08:37:16+01:00
- **发布者**: vissrk

**变更内容**:

##### 8. 版本 5.00.00

- **状态**: released
- **发布日期**: 2014-07-09T06:00:14+02:00
- **发布者**: vismdr

**变更内容**:

##### 9. 版本 6.00.00

- **状态**: released
- **发布日期**: 2014-12-03T10:01:07+01:00
- **发布者**: vismdr

**变更内容**:

##### 10. 版本 7.00.00

- **状态**: released
- **发布日期**: 2014-12-03T10:05:25+01:00
- **发布者**: vismdr

**变更内容**:

##### 11. 版本 8.00.00

- **状态**: released
- **发布日期**: 2015-09-08T11:40:14+02:00
- **发布者**: visgle

**变更内容**:

##### 12. 版本 8.00.01

- **状态**: released
- **发布日期**: 2016-02-01T10:16:04+01:00
- **发布者**: vismdr

**变更内容**:

##### 13. 版本 9.00.00

- **状态**: released
- **发布日期**: 2016-03-03T08:55:26+01:00
- **发布者**: vismdr

**变更内容**:

##### 14. 版本 10.00.00

- **状态**: released
- **发布日期**: 2016-05-11T08:07:13+02:00
- **发布者**: vismdr

**变更内容**:

##### 15. 版本 10.01.00

- **状态**: released
- **发布日期**: 2017-01-13T11:30:51+01:00
- **发布者**: visgle

**变更内容**:

##### 16. 版本 11.00.00

- **状态**: released
- **发布日期**: 2017-11-14T12:02:32+01:00
- **发布者**: visgle

**变更内容**:

##### 17. 版本 11.00.01

- **状态**: released
- **发布日期**: 2018-03-20T11:56:07+01:00
- **发布者**: visgle

**变更内容**:

##### 18. 版本 12.00.00

- **状态**: released
- **发布日期**: 2018-09-10T03:18:52+02:00
- **发布者**: vispkn

**变更内容**:

##### 19. 版本 13.00.00

- **状态**: released
- **发布日期**: 2019-03-25T10:46:02+01:00
- **发布者**: visgle

**变更内容**:

##### 20. 版本 14.00.00

- **状态**: released
- **发布日期**: 2020-03-27T14:37:05+01:00
- **发布者**: vispps

**变更内容**:

##### 21. 版本 14.01.00

- **状态**: released
- **发布日期**: 2021-09-13T09:27:37+02:00
- **发布者**: vispps

**变更内容**:

##### 22. 版本 15.00.00

- **状态**: released
- **发布日期**: 2021-11-08T15:31:09+01:00
- **发布者**: vispps

**变更内容**:

##### 23. 版本 15.01.00

- **状态**: released
- **发布日期**: 2022-01-12T13:47:21+01:00
- **发布者**: vispps

**变更内容**:

##### 24. 版本 16.00.00

- **状态**: released
- **发布日期**: 2022-04-26T10:31:46+02:00
- **发布者**: vispps

**变更内容**:

##### 25. 版本 16.00.01

- **状态**: released
- **发布日期**: 2022-08-12T08:36:32+02:00
- **发布者**: vispps

**变更内容**:

##### 26. 版本 17.00.00

- **状态**: released
- **发布日期**: 2023-05-26T16:32:37+02:00
- **发布者**: smarcelin

**变更内容**:

##### 27. 版本 18.00.00

- **状态**: released
- **发布日期**: 2023-09-26T11:34:05+02:00
- **发布者**: smarcelin

**变更内容**:

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. NmChannelConfig

**容器属性**:

- **UUID**: `a34010af-e386-406e-850b-47ba4847f803`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmChannelConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container represents the configuration of one Network Management channel.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. NmChannelId

- **UUID**: `2ec05e4a-3d24-4759-b8ac-0f804ce21376`
- **参数名**: `NmChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Handle ID of the NM channel. The value shall be the same as the ComMChannelId of the ComMChannel referenced by NmComMChannelRef. The value of this parameter is calculated automatically at validation time.
										
Implementation Type: NetworkHandleType

######## 2. NmCoordClusterIndex

- **UUID**: `5f615eff-6488-45de-9ee3-9cf08999eaec`
- **参数名**: `NmCoordClusterIndex`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies to which coordination cluster a bus belongs. If this parameter is undefined for a channel, the corresponding bus does not belong to an NM coordination cluster.

An NM coordination cluster is a group of networks/busses/channels that shall be shut down synchronously. Each NM coordination cluster requires at least two channels that need to be shut down synchronously.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

####### BOOLEAN 类型参数

######## 1. NmActiveCoordinator

- **UUID**: `bbab4661-e3ae-442a-8366-2d682bb30e15`
- **参数名**: `NmActiveCoordinator`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter indicates whether a NM Coordinator is an active gateway (NmActiveCoordinator = TRUE) or a passive.

An active coordinator is the node on the channel that is the last one that withdraws its network request. That means that it waits until all other nodes have indicated readiness to sleep and it waits for all other channels in the coordinator cluster for being ready to sleep until it indicates readiness to sleep itself.

A passive coordinator is a node on the channel that is not the last one that withdraws its network request. Instead, the request is withdrawn when all channels in the coordinator cluster are ready to sleep and the own node is ready to sleep on the channel.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined. This parameter needs to be set to true if 'NmCoordinatorSyncSupport' is OFF.

######## 2. NmChannelSleepMaster

- **UUID**: `1de5f30d-f10e-40ac-a999-2f9790658323`
- **参数名**: `NmChannelSleepMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be set to indicate if the readiness to sleep of this network can be absolutely decided by the local node only and that no other nodes can oppose that decision.
I.e. if this parameter is set to TRUE, the NM coordinator considers that the bus is ready to sleep at all times and shall not evaluate the remote sleep indication status. If this parameter is set to FALSE, the NM Coordinator evaluates the remote sleep indication status to decide whether the bus is ready to sleep or not.

If a Generic BusNm is used that is not able to determine the 'Remote Sleep' State and/or all other nodes are always ready to sleep, consider setting this value to true and also consider setting the NmGenericBusNmChannelSleepMaster switch to TRUE.
The setting for an AUTOSAR Standard BusNm is considered as
- TRUE for J1939Nm
- FALSE for all other BusNms (CanNm, FrNm, LinNm, UdpNm)

This parameter must not be set to TRUE if other nodes need to keep this node awake althrough the own node is ready to sleep.

This parameter needs to be turned ON, if NmGenericBusNmChannelSleepMaster is TRUE for at least one Generic BusNm on this channel.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined.

######## 3. NmPassiveModeEnabled

- **UUID**: `7d410193-576f-49b1-a988-95a2cb7a2360`
- **参数名**: `NmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If set to TRUE the passive mode of the network is enabled. Passive nodes are not able to send NM PDUs and therefore cannot keep the network awake. Passive nodes can however be woken up by the network by receiving the NM PDUs of other ECUs.
If set to FALSE, the ECU will be able to keep the network awake by transmitting own NM PDUs.

Restrictions: This parameter is not allowed to be defined in NmChannelConfig, if it is defined in NmGlobalFeatures.

######## 4. NmStateReportEnabled

- **UUID**: `5b3ca5e1-28ec-45bb-9f39-bac7620cb49e`
- **参数名**: `NmStateReportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this feature is enabled the Nm module will write state transition information into the Com Signal provided by 'NmStateReportSignalRef'. Most likely, the signal is inside the NM User Data TX PDU of the BusNm.
										
false: No NM State is written into the Com Signal.
true: The NM State is written into the Com Signal.

If enabled, the referenced signal will contain the last state transition of the BusNm. This can be one of the following values:
NM_RM_BSM (1): The last state transition has been from Bus Sleep to Repeat Message
NM_RM_PBSM (2): The last state transition has been from Prepare Bus Sleep to Repeat Message
NM_NO_RM (4) : The last state transition has been from Repeat Message to Normal Operation
NM_NO_RS (8): The last state transition has been from Ready Sleep to Normal Operation
NM_RM_RS (16): The last state transition has been from Ready Sleep to Repeat Message
NM_RM_NO (32): The last state transition has been from Normal Operation to Repeat Message

######## 5. NmSynchronizingNetwork

- **UUID**: `9151fecc-57e9-4230-8cfe-d1727a0fa9d0`
- **参数名**: `NmSynchronizingNetwork`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If this parameter is true the network is a synchronizing network for the NM coordination cluster which it belongs to. A synchronizing network is a network where the NM message is usually sent in a static time pattern and an NM message cannot be sent asynchronously due to the restrictions of the underlying bus type (e.g. FrNm) or due to the restrictions of the NM algorithm (e.g. OSEK NM).
If enabled, the network is expected to call Nm_SynchronizationPoint() at regular intervals.
Otherwise, the NM coordinator does not wait for Nm_SynchronizationPoint() calls.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined. This parameter can only be set to TRUE if all channels in the NM Coordination Cluster are actively coordinated, i.e. 'NmActiveCoordinator' is TRUE.

####### FLOAT 类型参数

######## 1. NmShutdownDelayTimer

- **UUID**: `14b10358-c8e7-4cf8-9967-8adf1552d73b`
- **参数名**: `NmShutdownDelayTimer`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter not used as the value is determined automatically by the code generator.

The Shutdown Delay Timer is started by the NM Coordinator on an actively coordinated channel when readiness for sleep is recognized on all channels in an NM coordination cluster. When the timer is elapsed, the Network Request is withdrawn on the BusNm.

######## 2. NmGlobalCoordinatorTimeAllNmOsekInNormal

- **UUID**: `8d323b08-1ec2-4549-9cc9-66204f0992d9`
- **参数名**: `NmGlobalCoordinatorTimeAllNmOsekInNormal`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster if all channels equipped with NmOsek are in the NMNormal state, i,e. not in NMLimpHome.
This time indicates to the NM coordinator how long it takes to shut down all NM coordinated channels on all ECUs in the vehicle networks. This is not a hard upper limit, since there may be slight time differences due to NM algorithms, call cycles of functions, etc.

For minimum values, refer to the description of NmGlobalCoordinatorTime in the NmGlobalFeatures container.
The only exception for NmOsek channels is that instead of NmGenericBusNmShutdownTime, the result of (NmGenericBusNmShutdownTime - (NmOsekErrorWaitBusSleepTime - NmOsekWaitBusSleepTime)) is used as BusNm shutdown time.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and NmOsekWaitBusSleepExtensions is TRUE.
This parameter shall only be defined if and only if the parameter is relevant AND NmSynchronizingNetwork is turned ON.
Note: this parameter is automatically calculated.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. NmComMChannelRef

- **UUID**: `1e33bc7a-8890-4661-9780-0584feace0ca`
- **引用名**: `NmComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - LINK: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComM channel that is handled by the Nm channel.

######## 2. NmStateReportSignalRef

- **UUID**: `df2aafea-ff82-413e-86f3-8947e9eb49ff`
- **引用名**: `NmStateReportSignalRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the signal that is used to write the Network Management State information to. The signal is usually part of the NM User Data TX PDU.

Restrictions: Only relevant if 'NmStateReportEnabled' is TRUE.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. NmGenericBusNmConfig

**容器属性**:

- **UUID**: `ad78d002-6921-4757-bf7e-57d502dbf8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGenericBusNmConfig`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Choose this container if the underlying BusNm is a Complex Device Driver with a Generic BusNm Interface.

######## 参数配置

此容器包含 **4** 个参数：

######### BOOLEAN 类型参数

########## 1. NmGenericBusNmChannelSleepMaster

- **UUID**: `33bbc656-a5e4-4eca-9935-d1b811ce6107`
- **参数名**: `NmGenericBusNmChannelSleepMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be set to indicate if the readiness to sleep of the NM algorithm for this Generic BusNm can be absolutely decided by the local node only and that no other nodes can oppose that decision.
I.e. if this parameter is set to TRUE, the NM coordinator considers that the BusNm is ready to sleep at all times and shall not evaluate the remote sleep indication status. If this parameter is set to FALSE, the NM Coordinator evaluates the remote sleep indication status to decide whether the BusNm is ready to sleep or not.

Set this parameter to TRUE if this GenericBusNm does not provide the 'Remote Sleep' status (i.e. it cannot determine whether the other nodes are ready to sleep) and/or if the own node can completely decide on its own that the other nodes are ready to sleep.
This parameter must not be set to TRUE if other nodes need to keep this node awake althrough the own node is ready to sleep.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and 'NmChannelSleepMaster' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined.

######### FLOAT 类型参数

########## 1. NmGenericBusNmShutdownTime

- **UUID**: `149f0f50-3938-4935-b9d3-cf22a9971c27`
- **参数名**: `NmGenericBusNmShutdownTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time the generic BusNm needs to shut down the channel.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined.

######### STRING 类型参数

########## 1. NmGenericBusNmPrefix

- **UUID**: `7e8f3ecc-c2c4-42a1-a1e5-c8871939a3c2`
- **参数名**: `NmGenericBusNmPrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the short name of the lower layer Nm used as <BusNm> prefix. The name is used to determine the function names of the APIs provided by the Generic BusNm that are called by Nm. 
This string will used for the module prefix in front of the "_" character in the API call name.

######### FUNCTION-NAME 类型参数

########## 1. NmGenericBusNmPduRxIndication

- **UUID**: `4d0646da-7c89-4421-b7dc-88f6b5feae8d`
- **参数名**: `NmGenericBusNmPduRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function called to notify the reception of a NmPdu.
This function can be used to distinguish between each BusNm on the same channel by using different identifiers for each BusNm.
It is not necessary to configure the function if there is only one BusNm on the channel. The NmPduReceiveIndCallback can be used as an alternative for this purpose.
Function prototype:
FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC) nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)

This function can be implemented by the Application, but it can also be used by BswM as a mode request port.

Example:
In a setup with two channels, one of them equipped with one Generic BusNm, the other one equipped with another Generic BusNm, there is no distinction required between the BusNms, because the Network Handle parameter is different for each channel.
Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However, this type of notification cannot be realized in BswM.
If a mode request port in BswM is required, define this parameter to a function name that BswM shall implement and configure.

Another example:
In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the provided Network Handle is the same.
Therefore, for a distinction, define this parameter to a certain value for NmOsek and the NmStandardBusNmPduRxIndication for the CanNm to a certain value.

####### 2. NmStandardBusNmConfig

**容器属性**:

- **UUID**: `2e1ead3a-0ed5-4b0a-8b2e-0c462eb56cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmStandardBusNmConfig`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Choose this container if the underlying BusNm is an AUTOSAR standard BusNm.

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. NmStandardBusType

- **UUID**: `092a4659-36dd-4551-8fbe-bb81ed912a77`
- **参数名**: `NmStandardBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NM_BUSNM_CANNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_FRNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_J1939NM` (来源: Vector Informatik)
  - `NM_BUSNM_LINNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_UDPNM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type for standard AUTOSAR <BusNm>s and is used to determine which APIs are to be called by the Nm module.

NOTE: The BusNm for Ethernet is UdpNm.

######### FUNCTION-NAME 类型参数

########## 1. NmStandardBusNmPduRxIndication

- **UUID**: `8ec0b024-17cd-4d68-91df-d85f89f2e92a`
- **参数名**: `NmStandardBusNmPduRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function called to notify the reception of a NmPdu.
This function can be used to distinguish between each BusNm on the same channel by using different identifiers for each BusNm.
It is not necessary to configure the function if there is only one BusNm on the channel. The NmPduReceiveIndCallback can be used as an alternative for this purpose.
Function prototype:
FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC) nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)

This function can be implemented by the Application, but it can also be used by BswM as a mode request port.

Example:
In a setup with two channels, one of them equipped with CanNm, the other one equipped with FrNm, there is no distinction required between the BusNms, because the Network Handle parameter is different for each channel.
Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However, this type of notification cannot be realized in BswM.
If a mode request port in BswM is required, define this parameter to a function name that BswM shall implement and configure.

Another example:
In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the provided Network Handle is the same.
Therefore, for a distinction, define this parameter to a certain value for CanNm and the NmGenericBusNmPduRxIndication for the NmOsek to a certain value.

RESTRICTIONS: This parameter cannot be defined if NmStandardBusType equals to NM_BUSNM_J1939NM or equals to NM_BUSNM_LINNM.

####### 3. NmBusType

**容器属性**:

- **UUID**: `ae05e2e7-4c80-43b8-86e9-54ac44fbd11e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NmBusType`
- **多重性**: [1..255]
- **构建后可变**: false

**容器选择**:

- **NmGenericBusNmConfig**
  - UUID: `ad78d002-6921-4757-bf7e-57d502dbf8cc`
  - 描述: Choose this container if the underlying BusNm is a Complex Device Driver with a Generic BusNm Interface.
- **NmStandardBusNmConfig**
  - UUID: `2e1ead3a-0ed5-4b0a-8b2e-0c462eb56cfc`
  - 描述: Choose this container if the underlying BusNm is an AUTOSAR standard BusNm.

**容器描述**:

This choice container determines the underlying BusNm for this channel.

If this container exists multiple times, this means that there are multiple BusNms on this channel.

RESTRICTIONS: The multiplicity of this container is only allowed to be greater than one if the underlying bus system is CAN.

##### 2. NmGenericBusNmConfig

**容器属性**:

- **UUID**: `ad78d002-6921-4757-bf7e-57d502dbf8cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGenericBusNmConfig`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Choose this container if the underlying BusNm is a Complex Device Driver with a Generic BusNm Interface.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. NmGenericBusNmChannelSleepMaster

- **UUID**: `33bbc656-a5e4-4eca-9935-d1b811ce6107`
- **参数名**: `NmGenericBusNmChannelSleepMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter shall be set to indicate if the readiness to sleep of the NM algorithm for this Generic BusNm can be absolutely decided by the local node only and that no other nodes can oppose that decision.
I.e. if this parameter is set to TRUE, the NM coordinator considers that the BusNm is ready to sleep at all times and shall not evaluate the remote sleep indication status. If this parameter is set to FALSE, the NM Coordinator evaluates the remote sleep indication status to decide whether the BusNm is ready to sleep or not.

Set this parameter to TRUE if this GenericBusNm does not provide the 'Remote Sleep' status (i.e. it cannot determine whether the other nodes are ready to sleep) and/or if the own node can completely decide on its own that the other nodes are ready to sleep.
This parameter must not be set to TRUE if other nodes need to keep this node awake althrough the own node is ready to sleep.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and 'NmChannelSleepMaster' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined.

####### FLOAT 类型参数

######## 1. NmGenericBusNmShutdownTime

- **UUID**: `149f0f50-3938-4935-b9d3-cf22a9971c27`
- **参数名**: `NmGenericBusNmShutdownTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the time the generic BusNm needs to shut down the channel.

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE. This parameter is only valid if 'NmCoordClusterIndex' is defined.

####### STRING 类型参数

######## 1. NmGenericBusNmPrefix

- **UUID**: `7e8f3ecc-c2c4-42a1-a1e5-c8871939a3c2`
- **参数名**: `NmGenericBusNmPrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the short name of the lower layer Nm used as <BusNm> prefix. The name is used to determine the function names of the APIs provided by the Generic BusNm that are called by Nm. 
This string will used for the module prefix in front of the "_" character in the API call name.

####### FUNCTION-NAME 类型参数

######## 1. NmGenericBusNmPduRxIndication

- **UUID**: `4d0646da-7c89-4421-b7dc-88f6b5feae8d`
- **参数名**: `NmGenericBusNmPduRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function called to notify the reception of a NmPdu.
This function can be used to distinguish between each BusNm on the same channel by using different identifiers for each BusNm.
It is not necessary to configure the function if there is only one BusNm on the channel. The NmPduReceiveIndCallback can be used as an alternative for this purpose.
Function prototype:
FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC) nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)

This function can be implemented by the Application, but it can also be used by BswM as a mode request port.

Example:
In a setup with two channels, one of them equipped with one Generic BusNm, the other one equipped with another Generic BusNm, there is no distinction required between the BusNms, because the Network Handle parameter is different for each channel.
Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However, this type of notification cannot be realized in BswM.
If a mode request port in BswM is required, define this parameter to a function name that BswM shall implement and configure.

Another example:
In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the provided Network Handle is the same.
Therefore, for a distinction, define this parameter to a certain value for NmOsek and the NmStandardBusNmPduRxIndication for the CanNm to a certain value.

##### 3. NmStandardBusNmConfig

**容器属性**:

- **UUID**: `2e1ead3a-0ed5-4b0a-8b2e-0c462eb56cfc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmStandardBusNmConfig`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Choose this container if the underlying BusNm is an AUTOSAR standard BusNm.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. NmStandardBusType

- **UUID**: `092a4659-36dd-4551-8fbe-bb81ed912a77`
- **参数名**: `NmStandardBusType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NM_BUSNM_CANNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_FRNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_J1939NM` (来源: Vector Informatik)
  - `NM_BUSNM_LINNM` (来源: AUTOSAR_ECUC)
  - `NM_BUSNM_UDPNM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the bus type for standard AUTOSAR <BusNm>s and is used to determine which APIs are to be called by the Nm module.

NOTE: The BusNm for Ethernet is UdpNm.

####### FUNCTION-NAME 类型参数

######## 1. NmStandardBusNmPduRxIndication

- **UUID**: `8ec0b024-17cd-4d68-91df-d85f89f2e92a`
- **参数名**: `NmStandardBusNmPduRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Function called to notify the reception of a NmPdu.
This function can be used to distinguish between each BusNm on the same channel by using different identifiers for each BusNm.
It is not necessary to configure the function if there is only one BusNm on the channel. The NmPduReceiveIndCallback can be used as an alternative for this purpose.
Function prototype:
FUNC(void, <MODULE_NAME>_CODE)<FunctionName>(CONST(NetworkHandleType, AUTOMATIC) nmNetworkHandle, P2CONST(PduInfoType, AUTOMATIC, AUTOMATIC) pduInfo)

This function can be implemented by the Application, but it can also be used by BswM as a mode request port.

Example:
In a setup with two channels, one of them equipped with CanNm, the other one equipped with FrNm, there is no distinction required between the BusNms, because the Network Handle parameter is different for each channel.
Therefore it suffices to use NmPduRxIndicationEnabled with NmPduReceiveIndCallback. However, this type of notification cannot be realized in BswM.
If a mode request port in BswM is required, define this parameter to a function name that BswM shall implement and configure.

Another example:
In a setup with one channel equipped with CanNm and NmOsek on the same channel, a distinction of which BusNm has received a NM PDU cannot be made by the NmPduReceiveIndCallback, since the provided Network Handle is the same.
Therefore, for a distinction, define this parameter to a certain value for CanNm and the NmGenericBusNmPduRxIndication for the NmOsek to a certain value.

RESTRICTIONS: This parameter cannot be defined if NmStandardBusType equals to NM_BUSNM_J1939NM or equals to NM_BUSNM_LINNM.

##### 4. NmGlobalConfig

**容器属性**:

- **UUID**: `3c405fea-52ba-41fe-b676-310f20a4bc83`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the NM module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. NmEcucPartitionRef

- **UUID**: `72b44a3c-6237-497a-b417-d426ac68edeb`
- **引用名**: `NmEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to EcuCPartition, where Nm module is assigned to.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. NmGlobalConstants

**容器属性**:

- **UUID**: `a7ad00d4-c902-42aa-8fbc-afa568036a6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConstants`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module constants related to the NM functionality.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. NmNumberOfChannels

- **UUID**: `66261fb4-974b-4b8e-b478-58cff3c8cceb`
- **参数名**: `NmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of logical Nm channels the ECU shall handle.
Parameter not used as the value is determined through the number of NmChannelConfig containers by the code generator.

####### 2. NmGlobalFeatures

**容器属性**:

- **UUID**: `1f5436d6-3f33-450b-8ef3-28daa1d81090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalFeatures`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module features related to the NM functionality.

######## 参数配置

此容器包含 **30** 个参数：

######### BOOLEAN 类型参数

########## 1. NmBusSynchronizationEnabled

- **UUID**: `4fc94752-655c-4c9f-a182-9ad4c543b214`
- **参数名**: `NmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled, the bus synchronization support of the <BusNm>s is turned ON. This parameter needs to be enabled if the NM Coordinator is used on this ECU.
Bus Synchronization permits an asynchronous message transmission for BusNms that support this feature (e.g. CanNm, UdpNm). This feature is required for the NM Coordinator to send the last NM message on the Bus that is responsible for restarting the Timeout Timer in the BusNm.

Restrictions: This parameter is only valid if it has the same value as 'NmCoordinatorSupportEnabled'.

########## 2. NmCarWakeUpRxEnabled

- **UUID**: `1fd5c47b-4ed5-4439-839b-672463201b95`
- **参数名**: `NmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables or disables Car Wake-Up detection.
If this option is enabled the Nm reports a detected Car Wake-Up in a received NM message to an upper layer (e.g. Complex Device Driver/Application) by calling the function given in 'NmCarWakeUpCallback'.

false: Car Wake-up is not supported.
true: Car Wake-up is supported.

It is completely application-specific how to react on this event. This can for instance be used for wake-up forwardings, so that all ComM users assigned to communication channels have to request FULL COMMUNICATION if this event occurs.

########## 3. NmComControlEnabled

- **UUID**: `0b15e8c3-5bdd-47b3-b071-f3a22bd97dce`
- **参数名**: `NmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If this option is enabled an additional API (CanNm_DisableCommunication(), CanNm_EnableCommunication()) is available that allows to enable and disable the transmission of NM PDUs at run-time while the NM is in the Normal Operation State. While the transmission is disabled the network cannot be released which implies that the network cannot be shut down.

Enable this feature in order to support ISO 14229 Communication Control Service $28.

########## 4. NmComUserDataSupport

- **UUID**: `ad0bff72-2080-4d09-af38-5e263e77adf7`
- **参数名**: `NmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled NM user data that is transmitted inside the NM PDU is determined through the contents of the COM I-PDU configured as NM User Data TX PDU inside the BusNm. The User Data of NM TX messages are handled as standard COM Signals and can be set by the application. The API Nm_SetUserData is not available.
If disabled NM user data that is transmitted inside the NM PDU can be set by the API Nm_SetUserData.

The NM user data in received NM PDUs is not handled by this feature and can be determined via Nm_GetUserData() and/or Nm_GetPduData().

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

########## 5. NmCoordinatorSupportEnabled

- **UUID**: `cf5ccea2-35a7-4353-9555-ffe4977dd442`
- **参数名**: `NmCoordinatorSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled the NM module allows the coordinated shutdown for all synchronized channels of the node. All synchronized channels are kept awake until the readiness to sleep is reached on all coordinated channels in one NM Coordination Cluster. Supported Network Managements are CANNM, FRNM, LINNM, UDPNM and Generic BusNms. J1939NM is not supported.
If disabled and a coordinated shutdown is required, the ComM users can be used inside the application.
If wake-up coordination is required, the 'Synchronous Wake-up' feature in ComM can be used and the coordination of different channels can be implemented by the application using ComM users.

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmCoordinatorSupportEnabled' is set to TRUE, then 'NmRemoteSleepIndEnabled' and 'NmBusSynchronizationEnabled' have to be TRUE.

########## 6. NmNodeDetectionEnabled

- **UUID**: `c3c2dc8b-1f06-44c3-9103-70b4664ff91b`
- **参数名**: `NmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If this feature is enabled on all nodes of a network other ECUs or a tester have the opportunity to detect all present active network nodes of a network.
The node that transmit an NM PDU with the 'Repeat Message Bit' set to 1, initiates the node detection. This can be realized by a Nm_RepeatMessageRequest() function call. This node and all nodes that receive this message return back to the 'Repeat Message' state so that their NM PDUs can be seen on the bus.
The function Nm_GetNodeIdentifier() returns the Node Identifier of the most recently received NM PDU. This function may be called in the context of Nm_PduRxIndication() and its configured callback function in 'NmPduReceiveIndCallback'.
Thus the algorithm for node detection can be realized by the application or by a Complex Device Driver.
Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmNodeDetectionEnabled' is set to TRUE, then 'NmNodeIdEnabled' has to be TRUE.

########## 7. NmNodeIdEnabled

- **UUID**: `4a0ffad6-d3df-4eed-ae27-19083eacd62a`
- **参数名**: `NmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This option provides read access to the local node identifier and to the node identifier received in the last NM message. Also, the own node identifier is transmitted in the NM PDU.
The following APIs are provided if the option is enabled:
- Nm_GetPduData() to receive the whole data bytes of the most recently received NM PDU.
- Nm_GetNodeIdentifier() to receive the Node Identifier byte of the most recently received NM PDU
- Nm_GetLocalNodeIdentifier() to receive the Node Identifier byte of own NM TX PDU

########## 8. NmPduRxIndicationEnabled

- **UUID**: `7e17dda4-81d5-4c6d-8e15-6541f45af9f3`
- **参数名**: `NmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled a callback function for every received NM PDU will be triggered.
The name of the callback function is configurable by the parameter 'NmPduReceiveIndCallback'. The function provided by this parameter can be implemented in the Application or in a Complex Device Driver.
The function Nm_GetPduData() may be used to access the data bytes (payload) of the received NM PDU. In order to use this function, the settings 'NmNodeIdEnabled' and/or 'NmUserDataEnabled' must be turned ON.

########## 9. NmRemoteSleepIndEnabled

- **UUID**: `b02e4442-55bb-4637-8d2b-ffba5d6ff1d9`
- **参数名**: `NmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable this feature in gateways (e.g. if NM coordinator is used) to allow the remote sleep detection. 'Remote Sleep' is a state of the network where all other nodes have indicated their readiness to sleep (e.g. in AUTOSAR Standard BusNms due to the absence of the NM PDU/negative votes).
This switch needs to be enabled if the synchronized shutdown of networks has to be carried out.
It comprises Remote Sleep Indication, Remote Sleep Cancellation and checking of the Remote Sleep Indication State.
If the feature is enabled, the following behavior is activated: Remote Sleep Indication is notified to the Nm module when your network node is the only one in the whole network that requests bus-communication for 'Remote Sleep Indication Time'.
Remote Sleep Cancellation is notified if any other network node requires the communication bus while Remote Sleep Indication takes place in your network node.
The Remote Sleep Status can be determined via the API Nm_CheckRemoteSleepIndication().
Optionally, an upper layer (e.g. Complex Device Driver, Application) can be notified by callback function calls about a Remote Sleep Indication and a remote Sleep Cancellation using the functions configured in 'NmRemoteSleepIndCallback' and 'NmRemoteSleepCancelCallback'.
If disabled, the above mentioned notifications do not happen and the API Nm_CheckRemoteSleepIndication is not available.
This feature is required for NM Coordinator nodes.

												

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

########## 10. NmRepeatMsgIndEnabled

- **UUID**: `441e3865-1625-41bb-962e-c54e6156a72c`
- **参数名**: `NmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled the ECU can request the transmission of NM messages from other nodes in order to detect which nodes are present in the network. To request this functionality the API Nm_RepeatMessageRequest() has to be called. Activated nodes can then be detected by the Application/by a Complex Device Driver through the API Nm_GetNodeIdentifier() that is enabled by 'NmNodeIdEnabled'. This API determines the Node Identifier of the most recently received NM PDU.

Restrictions: If 'NmRepeatMsgIndEnabled' is set to TRUE, then 'NmNodeDetectionEnabled' has to be TRUE.

########## 11. NmStateChangeIndEnabled

- **UUID**: `78310111-6b10-4a75-805b-b7e9ae8e6911`
- **参数名**: `NmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled every change in the NM state machine in the BusNm is reported as a function call to  Nm_StateChangeNotification(). This state change indication can be forwarded to an upper layer (e.g. Complex Device Driver, Application) using the function configured in 'NmStateChangeIndCallback'.

########## 12. NmUserDataEnabled

- **UUID**: `29e340c8-86e8-4369-b9b9-dd3f2f7a95e5`
- **参数名**: `NmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables read and write access to the user data of NM PDUs. The location of user data in the NM message depends on the message configuration.
If enabled, the NM user data can be read from the most recently received NM PDU through the APIs:
- Nm_GetUserData(): determines a pointer to the first user data byte.
- Nm_GetPduData(): determines a pointer to the first byte of the NM PDU.
If 'NmComUserDataSupport' is not enabled, the NM User Data Bytes can also be changed through the API:
- Nm_SetUserData().

########## 13. NmMacroLayerEnabled

- **UUID**: `5b8ff026-da7d-461e-aeb9-1e57659f4072`
- **参数名**: `NmMacroLayerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled, this option can be used to minimize the NM resource consumption ROM, RAM and runtime in case 'NmCoordinatorSupportEnabled' is FALSE and in case only one type of BusNm is used.
If disabled all NM options and features are available.

########## 14. NmCoordinatorSyncSupport

- **UUID**: `c78ae930-346b-4cb1-ba8d-1076e74cc108`
- **参数名**: `NmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the coordinator synchronization support.
If enabled, there can be active and passive coordinators. To allow synchronization between multiple coordinators, the NM PDU also contains a 'Sleep Ready' bit. For the difference of an active and a passive coordinator, see also the description of the 'NmActiveCoordinator' parameter.
If disabled, only active coordinators can be used and the 'Sleep Ready' bit in the NM PDU is not available.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

########## 15. NmRuntimeMeasurementSupport

- **UUID**: `cf86e1e6-4076-4705-9bad-dd3b53c210e8`
- **参数名**: `NmRuntimeMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines if runtime measurement points are added to the BSW module code and to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality.
Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

########## 16. NmPassiveModeEnabled

- **UUID**: `b85324c6-2b6e-4550-b6a3-d549623308b6`
- **参数名**: `NmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to TRUE the passive mode of all networks is enabled. Passive nodes are not able to send NM PDUs and therefore cannot keep the network awake. Passive nodes can however be woken up by the network by receiving the NM PDUs of other ECUs.
If set to FALSE, the ECU will be able to keep the network awake by transmitting own NM PDUs. The functions Nm_NetworkRequest() and Nm_NetworkRelease() will be available.
If set to TRUE, the ECU will not be able to keep all networks awake by transmitting own NM PDUs. The functions Nm_NetworkRequest() and Nm_NetworkRelease() will not be available.
If this parameter is not defined, the NmPassiveModeEnabled switch needs to be defined in each NmChannelConfig. This way, Passive Mode can be set individually for each network.

Restrictions: This parameter is only valid if 'NmPassiveModeEnabled' is not defined in every NmChannelConfig.

########## 17. NmCoordinatorRequestChannelsInBusSleep

- **UUID**: `fde39b79-cadd-45b9-8e99-cfbb33f2089f`
- **参数名**: `NmCoordinatorRequestChannelsInBusSleep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the support to request channels that are in Bus Sleep Mode.
If enabled, channels that belong to a coordination cluster are also requested (BusNm_NetworkRequest() call) if they are in Bus Sleep Mode if there is any reason to abort the coordinated shutdown.
If disabled, only those channels are requested that are not in Bus Sleep mode if there is any reason to abort the coordinated shutdown.

This behavior can be used to have an alternative to 'Synchronous Wake-up' at ComM that requests only the channels that belong to a coordination cluster.
 
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

########## 18. NmBusNmSpecificPduRxIndicationEnabled

- **UUID**: `f19a2333-75ba-45d4-a820-5dbb1d0ba7d4`
- **参数名**: `NmBusNmSpecificPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the generation of a BusNm specific callback that shall be called by the BusNm upon reception of the RxNmPdu.

The BusNm shall call this function instead of Nm_PduRxIndication to have a distinction between the BusNm if there are multiple BusNm on one channel.
However, Nm_PduRxIndication() can also be called instead of the specific BusNm Pdu RxIndication.

BusNm shall not call both functions. 

RESTRICTIONS:
The functions are generated only for CAN channels.

########## 19. NmCoordinatorPassiveStartUpForwarding

- **UUID**: `044f74b1-5e9b-4ae3-8c5a-7a3e1d6237d5`
- **参数名**: `NmCoordinatorPassiveStartUpForwarding`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the direct call of BusNm_PassiveStartUp when calling Nm_PassiveStartUp.

If enabled, the algorithm of the coordinator has a special handling in which the call of Nm_PassiveStartUp leads always to a BusNm_PassiveStartUp. Shortly after, the coordinator algorithm will call BusNm_NetworkRequest

Use this switch if the active wake up bit is used.

########## 20. NmSynchronizedPncShutdownEnabled

- **UUID**: `da2bde21-a658-4c1b-bc42-41b66e44927a`
- **参数名**: `NmSynchronizedPncShutdownEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables or disables support of synchronized PNC shutdown.

FALSE: synchronized PNC shutdown is disabled. This is the default setting. 

TRUE: synchronized PNC shutdown is enabled.

Dependencies: 
This feature can only be enabled for ECUs in the role of a Top-Level-PNC-Coordinator (TLPC) or an intermediate PNC coordinator. It cannot be enabled for subordinated (or leaf) nodes.
This feature can only be enabled if NmCoordinatorSupportEnabled is deactivated.

######### FLOAT 类型参数

########## 1. NmGlobalCoordinatorTime

- **UUID**: `7225cfb2-35e4-496c-9cdb-7d1e6af2677b`
- **参数名**: `NmGlobalCoordinatorTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967.295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.
This time indicates to the NM coordinator how long it takes to shut down all NM coordinated channels on all ECUs in the vehicle networks. This is not a hard upper limit, since there may be slight time differences due to NM algorithms, call cycles of functions, etc.
The minimum value of this parameter is given as the maximum of:
CanNmWaitBusSleepTime + CanNmTimeoutTime for all coordinated CAN NM channels
((FrNmReadySleepCnt + 1) * FrNmRepetitionCycle * FrCycleTime for all coordinated FR NM channels
0 for all coordinated LIN NM channels
UdpNmWaitBusSleepTime + UdpNmTimeoutTime for all coordinated UDP NM channels
NmGenericBusNmShutdownTime for all coordinated channels with a Generic BusNmIf this parameter is not defined, the minimum value as given above is calculated and used for code generation.

Note: This includes connections to coordinators across multiple networks.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

########## 2. NmSynchronizationTimeoutTime

- **UUID**: `774e090f-4907-4243-81d5-6a631b523e03`
- **参数名**: `NmSynchronizationTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum waiting time for a synchronization point. After this time, NM coordinator will continue the shutdown even if no synchronization point has appeared. If the time is set to 0, the NM module will not force any shutdown without a synchronization point.
A 'synchronization point' in this context is a notification that the BusNm has reached a state where usually the NM message is being sent or another NM algorithm-specific event has occurred that is relevant for the shutdown timing. See also the description of the parameter 'NmSynchronizingNetwork'.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and at least one channel is a synchronizing network.

######### STRING 类型参数

########## 1. NmCallbacksPrototypeHeader

- **UUID**: `94039f03-2c75-47cc-8b4e-1b75eb76db2c`
- **参数名**: `NmCallbacksPrototypeHeader`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If any of the configurable callback functions in the Nm is used the name of the header file providing the callback prototypes has to be defined here.
A header file is required for the following callback APIs: State Change Notification, Remote Sleep Indication, Remote Sleep Cancellation, Pdu Receive Indication, Repeat Message Indication, Tx Timeout Error Notification and/or Car Wakeup Indication.

######### FUNCTION-NAME 类型参数

########## 1. NmCarWakeUpCallback

- **UUID**: `9be96d22-4e23-464e-ab76-17f2ce32a421`
- **参数名**: `NmCarWakeUpCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Callback function that is called if the BusNm has detected the Car Wake-up Bit being set to 1 in the NM message (indicated by a function call of Nm_CarWakeUpIndication()).

Restrictions: Only relevant if 'NmCarWakeUpRxEnabled' is TRUE

########## 2. NmStateChangeIndCallback

- **UUID**: `3320a315-736c-4a54-81e0-a725582b9fea`
- **参数名**: `NmStateChangeIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the callback function that shall be invoked in case of NM state changes. The function is only called if 'NmStateChangeIndEnabled' has been enabled.

########## 3. NmRemoteSleepIndCallback

- **UUID**: `2e7b83d1-46cd-48a6-9842-9073726edfc0`
- **参数名**: `NmRemoteSleepIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the remote sleep indication callback. The function is only called if 'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be made.
The indication will be called when the own node has detected that all other nodes are ready to sleep.

########## 4. NmRemoteSleepCancelCallback

- **UUID**: `bd1445a8-2f68-492b-a2b5-c1fa68194a60`
- **参数名**: `NmRemoteSleepCancelCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the remote sleep cancellation indication callback. The function is only called if 'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be made.
The cancellation indication will be called when the own node has detected that it is not the only node that is ready to sleep.

########## 5. NmPduReceiveIndCallback

- **UUID**: `82f83e42-59bf-43a9-bf9d-33e54d87f354`
- **参数名**: `NmPduReceiveIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If 'NmPduRxIndicationEnabled' is enabled, the configured callback function will be invoked to notify an upper layer (e.g. Complex Device Driver, Application) about the reception of an NM PDU.

########## 6. NmRepeatMessageIndCallback

- **UUID**: `8b5f37c8-1639-4159-a5ac-eded356b3621`
- **参数名**: `NmRepeatMessageIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If 'NmRepeatMsgIndEnabled' is enabled, the configured callback function will be invoked to notify an upper layer (e.g. Complex Device Driver, Application) upon the state transition to Repeat Message due to a Repeat Message Request issued by any node. The repeat message state will be entered and executed by the NM module independently of the configured callback function. Note that entering Repeat Message will not always be notified, only if it has been entered because of a Repeat Message Request. If an upper layer shall always be notified about a state transition, for instance to Repeat Message, it is recommended to use the 'NmStateChangeIndEnabled' setting in combination with a configured callback function in the parameter 'NmStateChangeIndCallback'.

########## 7. NmTxTimeoutErrorCallback

- **UUID**: `8a2f6c31-17c8-47c6-a21b-4b798eb89140`
- **参数名**: `NmTxTimeoutErrorCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If a function name is configured the configured callback function will be invoked if the transmission of a NM PDU has failed due to a TX timeout. The notification may be used by an upper layer (e.g. Complex Device Driver) for error reporting.

Restrictions: This parameter is only relevant if at least one channel is not passive or CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

####### 3. NmGlobalProperties

**容器属性**:

- **UUID**: `da6dc8cd-7161-4c69-90b2-f7090f5c1589`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalProperties`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module properties related to the NM functionality.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. NmDevErrorDetect

- **UUID**: `5419aa68-c663-42ed-9555-607e3701c305`
- **参数名**: `NmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

########## 2. NmVersionInfoApi

- **UUID**: `adcc5aca-74e7-4f62-a7c4-e2db3cce4859`
- **参数名**: `NmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables the function Nm_GetVersionInfo() to get major, minor and patch version information.

########## 3. NmSafeBswChecks

- **UUID**: `22824d89-5d85-4ff0-8b4f-05bdd8c9dab8`
- **参数名**: `NmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######### FLOAT 类型参数

########## 1. NmCycletimeMainFunction

- **UUID**: `dceae664-96d4-4a36-8464-d9c745de1b2f`
- **参数名**: `NmCycletimeMainFunction`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The period between successive calls to the NM Main Function (Nm_MainFunction()).

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

######### STRING 类型参数

########## 1. NmUserConfigFile

- **UUID**: `c041b2bf-52b8-41bb-8b23-7ac3f94c93fe`
- **参数名**: `NmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

####### 4. NmGeneration

**容器属性**:

- **UUID**: `f32b77b9-868f-4982-9340-5ada81674eb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module Nm.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. NmOutOfBoundsWriteSanitizer

- **UUID**: `5518dfb6-b266-4538-8967-ef486355bfbf`
- **参数名**: `NmOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 2. NmOutOfBoundsReadSanitizer

- **UUID**: `55334441-78d5-4cea-90f8-814ef979a1a1`
- **参数名**: `NmOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 3. NmShortSymbols

- **UUID**: `de06d416-a90e-4b77-a706-0f10ad03fa12`
- **参数名**: `NmShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

########## 4. NmInterfacesForDeactivatedData

- **UUID**: `7e017510-dd21-4a63-93de-55fc0fc8429f`
- **参数名**: `NmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

########## 5. NmReferringKeysInComments

- **UUID**: `65615d86-c377-4c65-a7b5-5f76f8273c8a`
- **参数名**: `NmReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

##### 5. NmGlobalConstants

**容器属性**:

- **UUID**: `a7ad00d4-c902-42aa-8fbc-afa568036a6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalConstants`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module constants related to the NM functionality.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. NmNumberOfChannels

- **UUID**: `66261fb4-974b-4b8e-b478-58cff3c8cceb`
- **参数名**: `NmNumberOfChannels`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the number of logical Nm channels the ECU shall handle.
Parameter not used as the value is determined through the number of NmChannelConfig containers by the code generator.

##### 6. NmGlobalFeatures

**容器属性**:

- **UUID**: `1f5436d6-3f33-450b-8ef3-28daa1d81090`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalFeatures`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module features related to the NM functionality.

###### 参数配置

此容器包含 **30** 个参数：

####### BOOLEAN 类型参数

######## 1. NmBusSynchronizationEnabled

- **UUID**: `4fc94752-655c-4c9f-a182-9ad4c543b214`
- **参数名**: `NmBusSynchronizationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled, the bus synchronization support of the <BusNm>s is turned ON. This parameter needs to be enabled if the NM Coordinator is used on this ECU.
Bus Synchronization permits an asynchronous message transmission for BusNms that support this feature (e.g. CanNm, UdpNm). This feature is required for the NM Coordinator to send the last NM message on the Bus that is responsible for restarting the Timeout Timer in the BusNm.

Restrictions: This parameter is only valid if it has the same value as 'NmCoordinatorSupportEnabled'.

######## 2. NmCarWakeUpRxEnabled

- **UUID**: `1fd5c47b-4ed5-4439-839b-672463201b95`
- **参数名**: `NmCarWakeUpRxEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables or disables Car Wake-Up detection.
If this option is enabled the Nm reports a detected Car Wake-Up in a received NM message to an upper layer (e.g. Complex Device Driver/Application) by calling the function given in 'NmCarWakeUpCallback'.

false: Car Wake-up is not supported.
true: Car Wake-up is supported.

It is completely application-specific how to react on this event. This can for instance be used for wake-up forwardings, so that all ComM users assigned to communication channels have to request FULL COMMUNICATION if this event occurs.

######## 3. NmComControlEnabled

- **UUID**: `0b15e8c3-5bdd-47b3-b071-f3a22bd97dce`
- **参数名**: `NmComControlEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If this option is enabled an additional API (CanNm_DisableCommunication(), CanNm_EnableCommunication()) is available that allows to enable and disable the transmission of NM PDUs at run-time while the NM is in the Normal Operation State. While the transmission is disabled the network cannot be released which implies that the network cannot be shut down.

Enable this feature in order to support ISO 14229 Communication Control Service $28.

######## 4. NmComUserDataSupport

- **UUID**: `ad0bff72-2080-4d09-af38-5e263e77adf7`
- **参数名**: `NmComUserDataSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled NM user data that is transmitted inside the NM PDU is determined through the contents of the COM I-PDU configured as NM User Data TX PDU inside the BusNm. The User Data of NM TX messages are handled as standard COM Signals and can be set by the application. The API Nm_SetUserData is not available.
If disabled NM user data that is transmitted inside the NM PDU can be set by the API Nm_SetUserData.

The NM user data in received NM PDUs is not handled by this feature and can be determined via Nm_GetUserData() and/or Nm_GetPduData().

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

######## 5. NmCoordinatorSupportEnabled

- **UUID**: `cf5ccea2-35a7-4353-9555-ffe4977dd442`
- **参数名**: `NmCoordinatorSupportEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled the NM module allows the coordinated shutdown for all synchronized channels of the node. All synchronized channels are kept awake until the readiness to sleep is reached on all coordinated channels in one NM Coordination Cluster. Supported Network Managements are CANNM, FRNM, LINNM, UDPNM and Generic BusNms. J1939NM is not supported.
If disabled and a coordinated shutdown is required, the ComM users can be used inside the application.
If wake-up coordination is required, the 'Synchronous Wake-up' feature in ComM can be used and the coordination of different channels can be implemented by the application using ComM users.

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmCoordinatorSupportEnabled' is set to TRUE, then 'NmRemoteSleepIndEnabled' and 'NmBusSynchronizationEnabled' have to be TRUE.

######## 6. NmNodeDetectionEnabled

- **UUID**: `c3c2dc8b-1f06-44c3-9103-70b4664ff91b`
- **参数名**: `NmNodeDetectionEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If this feature is enabled on all nodes of a network other ECUs or a tester have the opportunity to detect all present active network nodes of a network.
The node that transmit an NM PDU with the 'Repeat Message Bit' set to 1, initiates the node detection. This can be realized by a Nm_RepeatMessageRequest() function call. This node and all nodes that receive this message return back to the 'Repeat Message' state so that their NM PDUs can be seen on the bus.
The function Nm_GetNodeIdentifier() returns the Node Identifier of the most recently received NM PDU. This function may be called in the context of Nm_PduRxIndication() and its configured callback function in 'NmPduReceiveIndCallback'.
Thus the algorithm for node detection can be realized by the application or by a Complex Device Driver.
Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE. If 'NmNodeDetectionEnabled' is set to TRUE, then 'NmNodeIdEnabled' has to be TRUE.

######## 7. NmNodeIdEnabled

- **UUID**: `4a0ffad6-d3df-4eed-ae27-19083eacd62a`
- **参数名**: `NmNodeIdEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This option provides read access to the local node identifier and to the node identifier received in the last NM message. Also, the own node identifier is transmitted in the NM PDU.
The following APIs are provided if the option is enabled:
- Nm_GetPduData() to receive the whole data bytes of the most recently received NM PDU.
- Nm_GetNodeIdentifier() to receive the Node Identifier byte of the most recently received NM PDU
- Nm_GetLocalNodeIdentifier() to receive the Node Identifier byte of own NM TX PDU

######## 8. NmPduRxIndicationEnabled

- **UUID**: `7e17dda4-81d5-4c6d-8e15-6541f45af9f3`
- **参数名**: `NmPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled a callback function for every received NM PDU will be triggered.
The name of the callback function is configurable by the parameter 'NmPduReceiveIndCallback'. The function provided by this parameter can be implemented in the Application or in a Complex Device Driver.
The function Nm_GetPduData() may be used to access the data bytes (payload) of the received NM PDU. In order to use this function, the settings 'NmNodeIdEnabled' and/or 'NmUserDataEnabled' must be turned ON.

######## 9. NmRemoteSleepIndEnabled

- **UUID**: `b02e4442-55bb-4637-8d2b-ffba5d6ff1d9`
- **参数名**: `NmRemoteSleepIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable this feature in gateways (e.g. if NM coordinator is used) to allow the remote sleep detection. 'Remote Sleep' is a state of the network where all other nodes have indicated their readiness to sleep (e.g. in AUTOSAR Standard BusNms due to the absence of the NM PDU/negative votes).
This switch needs to be enabled if the synchronized shutdown of networks has to be carried out.
It comprises Remote Sleep Indication, Remote Sleep Cancellation and checking of the Remote Sleep Indication State.
If the feature is enabled, the following behavior is activated: Remote Sleep Indication is notified to the Nm module when your network node is the only one in the whole network that requests bus-communication for 'Remote Sleep Indication Time'.
Remote Sleep Cancellation is notified if any other network node requires the communication bus while Remote Sleep Indication takes place in your network node.
The Remote Sleep Status can be determined via the API Nm_CheckRemoteSleepIndication().
Optionally, an upper layer (e.g. Complex Device Driver, Application) can be notified by callback function calls about a Remote Sleep Indication and a remote Sleep Cancellation using the functions configured in 'NmRemoteSleepIndCallback' and 'NmRemoteSleepCancelCallback'.
If disabled, the above mentioned notifications do not happen and the API Nm_CheckRemoteSleepIndication is not available.
This feature is required for NM Coordinator nodes.

												

Restrictions: This parameter is only relevant if at least one channel is not passive or the CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

######## 10. NmRepeatMsgIndEnabled

- **UUID**: `441e3865-1625-41bb-962e-c54e6156a72c`
- **参数名**: `NmRepeatMsgIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled the ECU can request the transmission of NM messages from other nodes in order to detect which nodes are present in the network. To request this functionality the API Nm_RepeatMessageRequest() has to be called. Activated nodes can then be detected by the Application/by a Complex Device Driver through the API Nm_GetNodeIdentifier() that is enabled by 'NmNodeIdEnabled'. This API determines the Node Identifier of the most recently received NM PDU.

Restrictions: If 'NmRepeatMsgIndEnabled' is set to TRUE, then 'NmNodeDetectionEnabled' has to be TRUE.

######## 11. NmStateChangeIndEnabled

- **UUID**: `78310111-6b10-4a75-805b-b7e9ae8e6911`
- **参数名**: `NmStateChangeIndEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled every change in the NM state machine in the BusNm is reported as a function call to  Nm_StateChangeNotification(). This state change indication can be forwarded to an upper layer (e.g. Complex Device Driver, Application) using the function configured in 'NmStateChangeIndCallback'.

######## 12. NmUserDataEnabled

- **UUID**: `29e340c8-86e8-4369-b9b9-dd3f2f7a95e5`
- **参数名**: `NmUserDataEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables read and write access to the user data of NM PDUs. The location of user data in the NM message depends on the message configuration.
If enabled, the NM user data can be read from the most recently received NM PDU through the APIs:
- Nm_GetUserData(): determines a pointer to the first user data byte.
- Nm_GetPduData(): determines a pointer to the first byte of the NM PDU.
If 'NmComUserDataSupport' is not enabled, the NM User Data Bytes can also be changed through the API:
- Nm_SetUserData().

######## 13. NmMacroLayerEnabled

- **UUID**: `5b8ff026-da7d-461e-aeb9-1e57659f4072`
- **参数名**: `NmMacroLayerEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If enabled, this option can be used to minimize the NM resource consumption ROM, RAM and runtime in case 'NmCoordinatorSupportEnabled' is FALSE and in case only one type of BusNm is used.
If disabled all NM options and features are available.

######## 14. NmCoordinatorSyncSupport

- **UUID**: `c78ae930-346b-4cb1-ba8d-1076e74cc108`
- **参数名**: `NmCoordinatorSyncSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the coordinator synchronization support.
If enabled, there can be active and passive coordinators. To allow synchronization between multiple coordinators, the NM PDU also contains a 'Sleep Ready' bit. For the difference of an active and a passive coordinator, see also the description of the 'NmActiveCoordinator' parameter.
If disabled, only active coordinators can be used and the 'Sleep Ready' bit in the NM PDU is not available.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

######## 15. NmRuntimeMeasurementSupport

- **UUID**: `cf86e1e6-4076-4705-9bad-dd3b53c210e8`
- **参数名**: `NmRuntimeMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines if runtime measurement points are added to the BSW module code and to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality.
Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

######## 16. NmPassiveModeEnabled

- **UUID**: `b85324c6-2b6e-4550-b6a3-d549623308b6`
- **参数名**: `NmPassiveModeEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to TRUE the passive mode of all networks is enabled. Passive nodes are not able to send NM PDUs and therefore cannot keep the network awake. Passive nodes can however be woken up by the network by receiving the NM PDUs of other ECUs.
If set to FALSE, the ECU will be able to keep the network awake by transmitting own NM PDUs. The functions Nm_NetworkRequest() and Nm_NetworkRelease() will be available.
If set to TRUE, the ECU will not be able to keep all networks awake by transmitting own NM PDUs. The functions Nm_NetworkRequest() and Nm_NetworkRelease() will not be available.
If this parameter is not defined, the NmPassiveModeEnabled switch needs to be defined in each NmChannelConfig. This way, Passive Mode can be set individually for each network.

Restrictions: This parameter is only valid if 'NmPassiveModeEnabled' is not defined in every NmChannelConfig.

######## 17. NmCoordinatorRequestChannelsInBusSleep

- **UUID**: `fde39b79-cadd-45b9-8e99-cfbb33f2089f`
- **参数名**: `NmCoordinatorRequestChannelsInBusSleep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the support to request channels that are in Bus Sleep Mode.
If enabled, channels that belong to a coordination cluster are also requested (BusNm_NetworkRequest() call) if they are in Bus Sleep Mode if there is any reason to abort the coordinated shutdown.
If disabled, only those channels are requested that are not in Bus Sleep mode if there is any reason to abort the coordinated shutdown.

This behavior can be used to have an alternative to 'Synchronous Wake-up' at ComM that requests only the channels that belong to a coordination cluster.
 
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

######## 18. NmBusNmSpecificPduRxIndicationEnabled

- **UUID**: `f19a2333-75ba-45d4-a820-5dbb1d0ba7d4`
- **参数名**: `NmBusNmSpecificPduRxIndicationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the generation of a BusNm specific callback that shall be called by the BusNm upon reception of the RxNmPdu.

The BusNm shall call this function instead of Nm_PduRxIndication to have a distinction between the BusNm if there are multiple BusNm on one channel.
However, Nm_PduRxIndication() can also be called instead of the specific BusNm Pdu RxIndication.

BusNm shall not call both functions. 

RESTRICTIONS:
The functions are generated only for CAN channels.

######## 19. NmCoordinatorPassiveStartUpForwarding

- **UUID**: `044f74b1-5e9b-4ae3-8c5a-7a3e1d6237d5`
- **参数名**: `NmCoordinatorPassiveStartUpForwarding`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables/disables the direct call of BusNm_PassiveStartUp when calling Nm_PassiveStartUp.

If enabled, the algorithm of the coordinator has a special handling in which the call of Nm_PassiveStartUp leads always to a BusNm_PassiveStartUp. Shortly after, the coordinator algorithm will call BusNm_NetworkRequest

Use this switch if the active wake up bit is used.

######## 20. NmSynchronizedPncShutdownEnabled

- **UUID**: `da2bde21-a658-4c1b-bc42-41b66e44927a`
- **参数名**: `NmSynchronizedPncShutdownEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enables or disables support of synchronized PNC shutdown.

FALSE: synchronized PNC shutdown is disabled. This is the default setting. 

TRUE: synchronized PNC shutdown is enabled.

Dependencies: 
This feature can only be enabled for ECUs in the role of a Top-Level-PNC-Coordinator (TLPC) or an intermediate PNC coordinator. It cannot be enabled for subordinated (or leaf) nodes.
This feature can only be enabled if NmCoordinatorSupportEnabled is deactivated.

####### FLOAT 类型参数

######## 1. NmGlobalCoordinatorTime

- **UUID**: `7225cfb2-35e4-496c-9cdb-7d1e6af2677b`
- **参数名**: `NmGlobalCoordinatorTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967.295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the maximum shutdown time of a connected and coordinated NM-Cluster.
This time indicates to the NM coordinator how long it takes to shut down all NM coordinated channels on all ECUs in the vehicle networks. This is not a hard upper limit, since there may be slight time differences due to NM algorithms, call cycles of functions, etc.
The minimum value of this parameter is given as the maximum of:
CanNmWaitBusSleepTime + CanNmTimeoutTime for all coordinated CAN NM channels
((FrNmReadySleepCnt + 1) * FrNmRepetitionCycle * FrCycleTime for all coordinated FR NM channels
0 for all coordinated LIN NM channels
UdpNmWaitBusSleepTime + UdpNmTimeoutTime for all coordinated UDP NM channels
NmGenericBusNmShutdownTime for all coordinated channels with a Generic BusNmIf this parameter is not defined, the minimum value as given above is calculated and used for code generation.

Note: This includes connections to coordinators across multiple networks.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

######## 2. NmSynchronizationTimeoutTime

- **UUID**: `774e090f-4907-4243-81d5-6a631b523e03`
- **参数名**: `NmSynchronizationTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the maximum waiting time for a synchronization point. After this time, NM coordinator will continue the shutdown even if no synchronization point has appeared. If the time is set to 0, the NM module will not force any shutdown without a synchronization point.
A 'synchronization point' in this context is a notification that the BusNm has reached a state where usually the NM message is being sent or another NM algorithm-specific event has occurred that is relevant for the shutdown timing. See also the description of the parameter 'NmSynchronizingNetwork'.
Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE and at least one channel is a synchronizing network.

####### STRING 类型参数

######## 1. NmCallbacksPrototypeHeader

- **UUID**: `94039f03-2c75-47cc-8b4e-1b75eb76db2c`
- **参数名**: `NmCallbacksPrototypeHeader`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If any of the configurable callback functions in the Nm is used the name of the header file providing the callback prototypes has to be defined here.
A header file is required for the following callback APIs: State Change Notification, Remote Sleep Indication, Remote Sleep Cancellation, Pdu Receive Indication, Repeat Message Indication, Tx Timeout Error Notification and/or Car Wakeup Indication.

####### FUNCTION-NAME 类型参数

######## 1. NmCarWakeUpCallback

- **UUID**: `9be96d22-4e23-464e-ab76-17f2ce32a421`
- **参数名**: `NmCarWakeUpCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Callback function that is called if the BusNm has detected the Car Wake-up Bit being set to 1 in the NM message (indicated by a function call of Nm_CarWakeUpIndication()).

Restrictions: Only relevant if 'NmCarWakeUpRxEnabled' is TRUE

######## 2. NmStateChangeIndCallback

- **UUID**: `3320a315-736c-4a54-81e0-a725582b9fea`
- **参数名**: `NmStateChangeIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the callback function that shall be invoked in case of NM state changes. The function is only called if 'NmStateChangeIndEnabled' has been enabled.

######## 3. NmRemoteSleepIndCallback

- **UUID**: `2e7b83d1-46cd-48a6-9842-9073726edfc0`
- **参数名**: `NmRemoteSleepIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the remote sleep indication callback. The function is only called if 'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be made.
The indication will be called when the own node has detected that all other nodes are ready to sleep.

######## 4. NmRemoteSleepCancelCallback

- **UUID**: `bd1445a8-2f68-492b-a2b5-c1fa68194a60`
- **参数名**: `NmRemoteSleepCancelCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Define the remote sleep cancellation indication callback. The function is only called if 'NmRemoteSleepIndEnabled' has been enabled. If no function name is defined, no API call will be made.
The cancellation indication will be called when the own node has detected that it is not the only node that is ready to sleep.

######## 5. NmPduReceiveIndCallback

- **UUID**: `82f83e42-59bf-43a9-bf9d-33e54d87f354`
- **参数名**: `NmPduReceiveIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If 'NmPduRxIndicationEnabled' is enabled, the configured callback function will be invoked to notify an upper layer (e.g. Complex Device Driver, Application) about the reception of an NM PDU.

######## 6. NmRepeatMessageIndCallback

- **UUID**: `8b5f37c8-1639-4159-a5ac-eded356b3621`
- **参数名**: `NmRepeatMessageIndCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If 'NmRepeatMsgIndEnabled' is enabled, the configured callback function will be invoked to notify an upper layer (e.g. Complex Device Driver, Application) upon the state transition to Repeat Message due to a Repeat Message Request issued by any node. The repeat message state will be entered and executed by the NM module independently of the configured callback function. Note that entering Repeat Message will not always be notified, only if it has been entered because of a Repeat Message Request. If an upper layer shall always be notified about a state transition, for instance to Repeat Message, it is recommended to use the 'NmStateChangeIndEnabled' setting in combination with a configured callback function in the parameter 'NmStateChangeIndCallback'.

######## 7. NmTxTimeoutErrorCallback

- **UUID**: `8a2f6c31-17c8-47c6-a21b-4b798eb89140`
- **参数名**: `NmTxTimeoutErrorCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If a function name is configured the configured callback function will be invoked if the transmission of a NM PDU has failed due to a TX timeout. The notification may be used by an upper layer (e.g. Complex Device Driver) for error reporting.

Restrictions: This parameter is only relevant if at least one channel is not passive or CONFIG-VARIANT is not VARIANT-PRE-COMPILE.

##### 7. NmGlobalProperties

**容器属性**:

- **UUID**: `da6dc8cd-7161-4c69-90b2-f7090f5c1589`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGlobalProperties`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains module properties related to the NM functionality.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. NmDevErrorDetect

- **UUID**: `5419aa68-c663-42ed-9555-607e3701c305`
- **参数名**: `NmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. NmVersionInfoApi

- **UUID**: `adcc5aca-74e7-4f62-a7c4-e2db3cce4859`
- **参数名**: `NmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables the function Nm_GetVersionInfo() to get major, minor and patch version information.

######## 3. NmSafeBswChecks

- **UUID**: `22824d89-5d85-4ff0-8b4f-05bdd8c9dab8`
- **参数名**: `NmSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. NmCycletimeMainFunction

- **UUID**: `dceae664-96d4-4a36-8464-d9c745de1b2f`
- **参数名**: `NmCycletimeMainFunction`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The period between successive calls to the NM Main Function (Nm_MainFunction()).

Restrictions: This parameter is only relevant if 'NmCoordinatorSupportEnabled' is TRUE.

####### STRING 类型参数

######## 1. NmUserConfigFile

- **UUID**: `c041b2bf-52b8-41bb-8b23-7ac3f94c93fe`
- **参数名**: `NmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

##### 8. NmGeneration

**容器属性**:

- **UUID**: `f32b77b9-868f-4982-9340-5ada81674eb5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `NmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module Nm.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. NmOutOfBoundsWriteSanitizer

- **UUID**: `5518dfb6-b266-4538-8967-ef486355bfbf`
- **参数名**: `NmOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. NmOutOfBoundsReadSanitizer

- **UUID**: `55334441-78d5-4cea-90f8-814ef979a1a1`
- **参数名**: `NmOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. NmShortSymbols

- **UUID**: `de06d416-a90e-4b77-a706-0f10ad03fa12`
- **参数名**: `NmShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 4. NmInterfacesForDeactivatedData

- **UUID**: `7e017510-dd21-4a63-93de-55fc0fc8429f`
- **参数名**: `NmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 5. NmReferringKeysInComments

- **UUID**: `65615d86-c377-4c65-a7b5-5f76f8273c8a`
- **参数名**: `NmReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

##### 9. NmBusType

**容器属性**:

- **UUID**: `ae05e2e7-4c80-43b8-86e9-54ac44fbd11e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `NmBusType`
- **多重性**: [1..255]
- **构建后可变**: false

**容器选择**:

- **NmGenericBusNmConfig**
  - UUID: `ad78d002-6921-4757-bf7e-57d502dbf8cc`
  - 描述: Choose this container if the underlying BusNm is a Complex Device Driver with a Generic BusNm Interface.
- **NmStandardBusNmConfig**
  - UUID: `2e1ead3a-0ed5-4b0a-8b2e-0c462eb56cfc`
  - 描述: Choose this container if the underlying BusNm is an AUTOSAR standard BusNm.

**容器描述**:

This choice container determines the underlying BusNm for this channel.

If this container exists multiple times, this means that there are multiple BusNms on this channel.

RESTRICTIONS: The multiplicity of this container is only allowed to be greater than one if the underlying bus system is CAN.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Nm_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Nm**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Nm_Pre**
2. **Nm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Nm_Impl

- **UUID**: `10e1d426-5838-4dbc-827a-9f03994ff3ed`
- **实现名称**: `Nm_Impl`
- **编程语言**: C
- **软件版本**: 18.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Nm_Pre

- **UUID**: `DCE:78dff519-7e10-4ff0-9e04-3fa17d9ad19f`
- **配置名称**: `Nm_Pre`
- **定义引用**: `/MICROSAR/Nm`

### 2. Nm_Rec

- **UUID**: `DCE:7b32bc44-023a-4d34-bcbf-bfa64a6fb21a`
- **配置名称**: `Nm_Rec`
- **定义引用**: `/MICROSAR/Nm`
