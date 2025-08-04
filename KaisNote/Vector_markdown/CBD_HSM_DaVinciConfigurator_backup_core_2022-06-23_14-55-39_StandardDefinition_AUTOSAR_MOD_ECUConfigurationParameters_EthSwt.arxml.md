# EthSwt

## 模块描述

Configuration of the EthSwt (Ethernet Switch Driver) module.

## 容器列表

### 1. EthSwtConfig

**描述**: Configuration of one Ethernet Switch.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtIdx
  长名称: ''
  描述: Specifies the instance ID of the configured Ethernet Switch.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 2. EthSwtDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 3. EthSwtNvm

**描述**: Configuration of one Ethernet Switch Nvm usage in case the module requires non volatile memory in
the Ecu to store switch configuration.

该容器没有参数。

### 4. EthSwtPort

**描述**: Configuration of one Ethernet Switch Port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortEnableLinkDownCallback
  长名称: ''
  描述: Enables the callback <User>_LinkDown for this EthSwtPort if an IEEE802.1X link loss is
      detected.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthSwtPortIdx
  长名称: ''
  描述: Specifies the instance ID of the configured Ethernet Switch Port.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: EthSwtPortPhysicalLayerType
  长名称: ''
  描述: Defines the physical layer type on this EthSwtPort.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthSwtPortPredefinedMacAddresses
  长名称: ''
  描述: Specifies a list of 48-bit physical addresses (MAC addresses) which can be reached via this
      port in network byte order.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthSwtPortSpeed
  长名称: ''
  描述: Defines the communication speed in Mbit per second on this EthSwtPort in case no
      EthSwtPortTrcvRef is defined.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. EthSwtPortEgress

**描述**: Configuration of one Ethernet Switch Port Egress behavior.

该容器没有参数。

### 6. EthSwtPortFifo

**描述**: Represents a Fifo in the egress port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortFifoTrafficClassAssignment
  长名称: ''
  描述: Defines which traffic classes are assigned to this Fifo.
  默认值: ''
  最小值: 0
  最大值: 7
```

### 7. EthSwtPortScheduler

**描述**: Represents a Scheduler in the egress port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortSchedulerAlgorithm
  长名称: ''
  描述: Defines the scheduler algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. EthSwtPortSchedulerPredecessor

**描述**: Defines an ordered list of predecessors for this scheduler.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortSchedulerPredecessorOrder
  长名称: ''
  描述: Defines the order of the scheduler predecessors.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 9. EthSwtPortShaper

**描述**: Represents a Shaper in the egress port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortShaperIdleSlope
  长名称: ''
  描述: Defines the increase of credit in bits per second for the AVB shaper.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 10. EthSwtPortVlanForwarding

**描述**: Defines how messages with a specific VLAN Id shall be handled at this egress port wrt. their VLAN
Id.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortVlanDefaultPriority
  长名称: ''
  描述: Determines the standard output-priority outgoing messages will be tagged with.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthSwtPortVlanForwardingId
  长名称: ''
  描述: Determines the VLAN Id the VlanForwarding shall apply to.
  默认值: ''
  最小值: 1
  最大值: 4094
- 
  序号: 3
  名称: EthSwtPortVlanForwardingType
  长名称: ''
  描述: Defines how the message with a specific VLAN Id shall be handled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. EthSwtPortIngress

**描述**: Configuration of one Ethernet Switch Port ingress behavior.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPortIngressVlanModification
  长名称: ''
  描述: If this parameter is defined all messages which arrive at this ingress port will be tagged
      with this VLAN Id. This tagging happen also if the arriving message already has a VLAN
      Id, it will be overwritten by the defined one.
  默认值: ''
  最小值: 1
  最大值: 4094
- 
  序号: 2
  名称: EthSwtPortTrafficClassAssignment
  长名称: ''
  描述: If this parameter is defined all arriving messages at this ingress port shall be assigned this
      traffic class.
  默认值: ''
  最小值: 0
  最大值: 7
```

### 12. EthSwtPriorityRegeneration

**描述**: Defines a priority regeneration where the EthSwtPriorityRegenerationIngressPriority is replaced by
EthSwtPriorityRegenerationRegeneratedPriority.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPriorityRegenerationIngressPriority
  长名称: ''
  描述: Message priority of the incoming message.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthSwtPriorityRegenerationRegeneratedPriority
  长名称: ''
  描述: Message priority the incoming message will be tagged with.
  默认值: ''
  最小值: 0
  最大值: 7
```

### 13. EthSwtPriorityTrafficClassAssignment

**描述**: Defines a priority based traffic class assignment. All messages with a specific priority
(EthSwtPriorityTrafficClassAssignmentPriority) arriving at this ingress port or, if enabled
regenerated priorities (EthSwtPriorityRegeneration), shall be assigned to a traffic class
(EthSwtPriorityTrafficClassAssignmentTrafficClass).

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtPriorityTrafficClassAssignmentPriority
  长名称: ''
  描述: Message priority.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: EthSwtPriorityTrafficClassAssignmentTrafficClass
  长名称: ''
  描述: Traffic Class value.
  默认值: ''
  最小值: 0
  最大值: 7
```

### 14. EthSwtSpi

**描述**: Configuration of one Ethernet Switch SPI access (if SPI is used).

该容器没有参数。

### 15. EthSwtSpiSequence

**描述**: Container gives EthSwt driver information about one SPI sequence.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtSpiAccessSynchronous
  长名称: ''
  描述: This parameter is used to define whether the access to the Spi sequence is synchronous or
      asynchronous.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. EthSwtGeneral

**描述**: General configuration of Ethernet Switch Driver module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EthSwtDevErrorDetect
  长名称: ''
  描述: Enables / Disables development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EthSwtEnableVlanApi
  长名称: ''
  描述: Enables / Disables EthSwt_EnableVLAN API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EthSwtGetArlTableApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetArlTable API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EthSwtGetBufferLevelApi
  长名称: ''
  描述: Enables / Disables API to fetch the switch buffer utilization.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EthSwtGetDropCountApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetDropCount API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EthSwtGetEtherStatsApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetEtherStats API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EthSwtGetMacLearningModeApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetMacLearningMode API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EthSwtGetPortMacAddrApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetPortMacAddr API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EthSwtGetSwitchRegApi
  长名称: ''
  描述: Enables / Disables EthSwt_GetSwitchReg API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EthSwtIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: EthSwtLinkDownUser
  长名称: ''
  描述: Defines the <User> function name for the <User>_LinkDown callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: EthSwtLinkUpUser
  长名称: ''
  描述: Defines the <User> function name for the <User>_LinkUp callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EthSwtPersistentConfigurationResult
  长名称: ''
  描述: Enables / Disables the callback API <User>_PersistentConfigurationResult.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: EthSwtPersistentConfigurationResultUser
  长名称: ''
  描述: Defines the <User> function name for the <User>_PersistentConfigurationResult callback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: EthSwtPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: EthSwtReadTrcvRegisterApi
  长名称: ''
  描述: Enables / Disables EthSwt_ReadTrcvRegister API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: EthSwtResetConfigurationApi
  长名称: ''
  描述: Enables / Disables EthSwt_ResetConfiguration API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: EthSwtSetMacLearningModeApi
  长名称: ''
  描述: Enables / Disables EthSwt_SetMacLearningMode API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: EthSwtSetSwitchRegApi
  长名称: ''
  描述: Enables / Disables EthSwt_SetSwitchReg API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: EthSwtStoreConfigurationApi
  长名称: ''
  描述: Enables / Disables EthSwt_StoreConfiguration API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: EthSwtVersionInfoApi
  长名称: ''
  描述: Enables / Disables version info API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: EthSwtWriteTrcvRegisterApi
  长名称: ''
  描述: Enables / Disables EthSwt_WriteTrcvRegister API.
  默认值: ''
  最小值: ''
  最大值: ''
```

