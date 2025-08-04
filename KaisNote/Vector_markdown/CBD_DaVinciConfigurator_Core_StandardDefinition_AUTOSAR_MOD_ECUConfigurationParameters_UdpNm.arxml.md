# UdpNm

## 容器列表

### 1. UdpNmGlobalConfig

**描述**: This container contains all global configuration parameters of UDP NM configured from the NM Module
perspective.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmBusSynchronizationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling bus synchronization support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: UdpNmComControlEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Communication Control support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: UdpNmComUserDataSupport
  长名称: ''
  描述: Enable/disable the user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: UdpNmCoordinatorEnabled
  长名称: ''
  描述: Enable/disable the NM Coordination algorithm to being able to initiate the synchronization
      algorithm.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: UdpNmCoordinatorId
  长名称: ''
  描述: Set the NM coordination ID for this gateway.
  默认值: ''
  最小值: 0
  最大值: 3
- 
  序号: 6
  名称: UdpNmCoordinatorSyncSupport
  长名称: ''
  描述: Enables/disables the coordinator synchronisation support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: UdpNmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: UdpNmImmediateRestartEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the asynchronous transmission of a NM PACKET upon
      bus-communication request in Prepare-Bus-Sleep mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: UdpNmNodeDetectionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the node detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: UdpNmNodeIdEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the source node identifier.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UdpNmNumberOfChannels
  长名称: ''
  描述: Number of NM channels allowed within one ECU.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 12
  名称: UdpNmPassiveModeEnabled
  长名称: ''
  描述: Pre-processor switch for enabling support of the Passive Mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: UdpNmPduRxIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the PDU Rx Indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: UdpNmPnEiraCalcEnabled
  长名称: ''
  描述: Specifies if UdpNm calculates the PN request information for internal and external requests.
      (EIRA) true: PN request are calculated
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: UdpNmPnResetTime
  长名称: ''
  描述: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of
      PN requests in the EIRA and in the ERA. The value shall be the same for every channel.
      Thus it is a global config parameter.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 16
  名称: UdpNmRemoteSleepIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling remote sleep indication support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: UdpNmRepeatMsgIndEnabled
  长名称: ''
  描述: Enable/disable the notification that a RepeatMessageRequest bit has been received.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: UdpNmStateChangeIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the UDP NM state change notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: UdpNmUserDataEnabled
  长名称: ''
  描述: Pre-processor switch for enabling user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: UdpNmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. UdpNmChannelConfig

**描述**: This container contains the channel-specific configuration parameters of the UdpNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmMainFunctionPeriod
  长名称: ''
  描述: Call cycle of UdpNm_MainFunction_x for the respective instance in [s].
  默认值: ''
  最小值: 0.001
  最大值: 0.255
- 
  序号: 2
  名称: UdpNmMsgCycleOffset
  长名称: ''
  描述: Time offset in the periodic transmission node. It determines the start delay of the
      transmission.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 3
  名称: UdpNmMsgCycleTime
  长名称: ''
  描述: Period of a NM-message. It determines the periodic rate and is the basis for transmit
      scheduling.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 4
  名称: UdpNmMsgTimeoutTime
  长名称: ''
  描述: Transmission Timout of NM-message. If there is no transmission confirmation by the UDP
      Interface within this timeout, the UDPNM module shall gibe an error notification.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 5
  名称: UdpNmNodeId
  长名称: ''
  描述: Node identifier of local node.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: UdpNmPduCbvPosition
  长名称: ''
  描述: Defines the position of the control bit vector within the NM PACKET.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: UdpNmPduLength
  长名称: ''
  描述: Defines the length of the NM PACKET in bytes.
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 8
  名称: UdpNmPduNidPosition
  长名称: ''
  描述: Defines the position of the source node identifier within the NM PACKET.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: UdpNmPnEnabled
  长名称: ''
  描述: Enables or disables support of partial networking.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: UdpNmPnEraCalcEnabled
  长名称: ''
  描述: Specifies if UdpNm calculates the PN request information for external requests. (ERA)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UdpNmPnHandleMultipleNetworkRequests
  长名称: ''
  描述: false: UdpNm_NetworkRequest is ignored in NO.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: UdpNmRemoteSleepIndTime
  长名称: ''
  描述: Timeout for Remote Sleep Indication.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 13
  名称: UdpNmRepeatMessageTime
  长名称: ''
  描述: Timeout for Repeat Message State.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 14
  名称: UdpNmTimeoutTime
  长名称: ''
  描述: Network Timeout for NM packets.
  默认值: ''
  最小值: 0.002
  最大值: 65.535
- 
  序号: 15
  名称: UdpNmUserDataLength
  长名称: ''
  描述: Defines the length of the user data contained in the NM PACKET.
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 16
  名称: UdpNmWaitBusSleepTime
  长名称: ''
  描述: Timeout for bus calm down phase.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
```

### 3. UdpNmRxPdu

**描述**: This container describes the UdpNm RX PDU's.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmRxPduId
  长名称: ''
  描述: ID of the RxPdu that will be used by a RxIndication of the lower layer.
  默认值: ''
  最小值: 0
  最大值: 4294967296
```

### 4. UdpNmTxPdu

**描述**: This container describes the UdpNm TX PDU's.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmTxConfirmationPduId
  长名称: ''
  描述: Id of the TxPdu that will be used by a TxConfirmation from the lower layer.
  默认值: ''
  最小值: 0
  最大值: 4294967296
```

### 5. UdpNmUserDataTxPdu

**描述**: This optional container is used to configure the UserNm PDU. This container is only available if
UdpNmComUserDataSupport is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmTxUserDataPduId
  长名称: ''
  描述: This parameter defines the Handle ID of the NM User Data I-PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. UdpNmDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 7. UdpNmPnInfo

**描述**: PN information configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmPnInfoLength
  长名称: ''
  描述: Specifies the length of the PN request information in the NM message.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: UdpNmPnInfoOffset
  长名称: ''
  描述: Specifies the offset of the PN request information in the NM message.
  默认值: 0
  最小值: 1
  最大值: 7
```

### 8. UdpNmPnFilterMaskByte

**描述**: PN information configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: UdpNmPnFilterMaskByteIndex
  长名称: ''
  描述: Specifies the offset of the PN request information in the NM message.
  默认值: ''
  最小值: 0
  最大值: 6
- 
  序号: 2
  名称: UdpNmPnFilterMaskByteValue
  长名称: ''
  描述: Parameter to configure the filter mask byte.
  默认值: 0
  最小值: 0
  最大值: 255
```

