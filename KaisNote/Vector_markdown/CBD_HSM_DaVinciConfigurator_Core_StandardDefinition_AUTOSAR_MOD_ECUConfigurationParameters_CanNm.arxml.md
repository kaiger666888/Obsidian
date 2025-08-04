# CanNm

## 模块描述

Configuration Parameters for the Can Nm module.

## 容器列表

### 1. CanNmGlobalConfig

**描述**: This container contains the global configuration parameter of the CanNm. The parameters and the
parameters of the sub containers shall be mapped to the C data type CanNm_ConfigType (for parameters
where it is possible) which is passed to the CanNm_Init function.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmBusLoadReductionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling busload reduction support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanNmBusSynchronizationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling bus synchronization support. This feature is required for
      gateway nodes only.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanNmComControlEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the Communication Control support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanNmComUserDataSupport
  长名称: ''
  描述: Enable/disable the user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanNmCoordinatorSyncSupport
  长名称: ''
  描述: Enables/disables the coordinator synchronisation support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanNmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanNmImmediateRestartEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the asynchronous transmission of a NM PDU upon
      bus-communication request in Prepare-Bus-Sleep mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanNmImmediateTxconfEnabled
  长名称: ''
  描述: Enable/disable the immediate tx confirmation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanNmMainFunctionPeriod
  长名称: ''
  描述: Call cycle in seconds of CanNm_MainFunction.
  默认值: ''
  最小值: 0.001
  最大值: 0.255
- 
  序号: 10
  名称: CanNmNodeDetectionEnabled
  长名称: ''
  描述: Precompile time switch to enable the node detection feature.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CanNmNumberOfChannels
  长名称: ''
  描述: Number of Can NM channels allowed within one ECU.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 12
  名称: CanNmPassiveModeEnabled
  长名称: ''
  描述: Pre-processor switch for enabling support of the Passive Mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: CanNmPduRxIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the PDU Rx Indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: CanNmPnEiraCalcEnabled
  长名称: ''
  描述: Specifies if CanNm calculates the PN request information for internal an external requests.
      (EIRA)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: CanNmPnResetTime
  长名称: ''
  描述: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of
      PN requests in the EIRA and in the ERA. The value shall be the same for every channel.
      Thus it is a global config parameter.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 16
  名称: CanNmRemoteSleepIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling remote sleep indication support. This feature is required
      for gateway nodes only.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: CanNmRepeatMsgIndEnabled
  长名称: ''
  描述: Enable/disable the notification that a RepeatMessageRequest bit has been received.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: CanNmStateChangeIndEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the CAN NM state change notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: CanNmUserDataEnabled
  长名称: ''
  描述: Pre-processor switch for enabling user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: CanNmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. CanNmChannelConfig

**描述**: This container contains the channel specific configuration parameter of the CanNm.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmAllNmMessagesKeepAwake
  长名称: ''
  描述: Specifies if CanNm drops irrelevant NM messages.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanNmBusLoadReductionActive
  长名称: ''
  描述: This parameter defines if bus load reduction for the respective NM channel is active or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanNmCarWakeUpBitPosition
  长名称: ''
  描述: Specifies the Bit position of the CWU within the NM-Message.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 4
  名称: CanNmCarWakeUpBytePosition
  长名称: ''
  描述: Specifies the Byte position of the CWU within the NM-Message.
  默认值: ''
  最小值: 2
  最大值: 7
- 
  序号: 5
  名称: CanNmCarWakeUpFilterEnabled
  长名称: ''
  描述: If CWU filtering is supported, only the CWU bit within the NM message with source node
      identifier CanNmCarWakeUpFilterNodeId is considered as CWU request.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanNmCarWakeUpFilterNodeId
  长名称: ''
  描述: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit
      within the NM message with source node identifier CanNmCarWakeUpFilterNodeId is
      considered as CWU request.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: CanNmCarWakeUpRxEnabled
  长名称: ''
  描述: Enables or disables support of CarWakeUp bit evaluation in received NM messages.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanNmImmediateNmCycleTime
  长名称: ''
  描述: Defines the immediate NM PDU cycle time in seconds which is used for
      CanNmImmediateNmTransmissions NM PDU transmissions. This parameter is only valid if
      CanNmImmediateNmTransmissions is greater one.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 9
  名称: CanNmImmediateNmTransmissions
  长名称: ''
  描述: Defines the number of immediate NM PDUs which shall be transmitted. If the value is zero no
      immediate NM PDUs are transmitted. The cycle time of immeditate NM PDUs is defined by
      CanNmImmediateNmCycleTime.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: CanNmMsgCycleOffset
  长名称: ''
  描述: Time offset in the periodic transmission node. It determines the start delay of the
      transmission. Specified in seconds.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 11
  名称: CanNmMsgCycleTime
  长名称: ''
  描述: Period of a NM-message in seconds. It determines the periodic rate in the "periodic
      transmission mode with bus load reduction" and is the basis for transmit scheduling in
      the "periodic transmission mode without bus load reduction".
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 12
  名称: CanNmMsgReducedTime
  长名称: ''
  描述: Node specific bus cycle time in the periodic transmission mode with bus load reduction.
      Specified in seconds.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 13
  名称: CanNmMsgTimeoutTime
  长名称: ''
  描述: Transmission Timeout of NM-message. If there is no transmission confirmation by the CAN
      Interface within this timeout, the CANNM module shall give an error notification.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 14
  名称: CanNmNodeId
  长名称: ''
  描述: Node identifier of local node.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: CanNmPduCbvPosition
  长名称: ''
  描述: Defines the position of the control bit vector within the NM PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: CanNmPduNidPosition
  长名称: ''
  描述: Defines the position of the source node identifier within the NM PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: CanNmPnEnabled
  长名称: ''
  描述: Enables or disables support of partial networking.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: CanNmPnEraCalcEnabled
  长名称: ''
  描述: Specifies if CanNm calculates the PN request information for external requests. (ERA)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: CanNmPnHandleMultipleNetworkRequests
  长名称: ''
  描述: false: CanNm_NetworkRequest is ignored in NO.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: CanNmRemoteSleepIndTime
  长名称: ''
  描述: Timeout for Remote Sleep Indication.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 21
  名称: CanNmRepeatMessageTime
  长名称: ''
  描述: Timeout for Repeat Message State.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 22
  名称: CanNmTimeoutTime
  长名称: ''
  描述: Network Timeout for NM-Messages.
  默认值: ''
  最小值: 0.002
  最大值: 65.535
- 
  序号: 23
  名称: CanNmUserDataLength
  长名称: ''
  描述: Defines the length of the user data contained in the NM PDU
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 24
  名称: CanNmWaitBusSleepTime
  长名称: ''
  描述: Timeout for bus calm down phase.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
```

### 3. CanNmRxPdu

**描述**: This container is used to configure the Rx PDU properties that are used for the CanNm Channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmRxPduId
  长名称: ''
  描述: This parameter defines the Rx PDU ID of the CanIf L-PDU range that is associated with this
      CanNmChannel instance.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. CanNmTxPdu

**描述**: This container contains the CanNmTxConfirmationPduId and the CanNmTxPduRef.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the CanNmTxPdu to the
      LowerLayer.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. CanNmUserDataTxPdu

**描述**: This optional container is used to configure the UserNm PDU. This container is only available if
CanNmComUserDataSupport is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmTxUserDataPduId
  长名称: ''
  描述: This parameter defines the Handle ID of the NM User Data I-PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. CanNmPnInfo

**描述**: PN information configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmPnInfoLength
  长名称: ''
  描述: Specifies the length of the PN request information in the NM message.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: CanNmPnInfoOffset
  长名称: ''
  描述: Specifies the offset of the PN request information in the NM message.
  默认值: 0
  最小值: 1
  最大值: 7
```

### 7. CanNmPnFilterMaskByte

**描述**: PN information configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanNmPnFilterMaskByteIndex
  长名称: ''
  描述: Specifies the offset of the PN request information in the NM message.
  默认值: ''
  最小值: 0
  最大值: 6
- 
  序号: 2
  名称: CanNmPnFilterMaskByteValue
  长名称: ''
  描述: Parameter to configure the filter mask byte.
  默认值: 0
  最小值: 0
  最大值: 255
```

