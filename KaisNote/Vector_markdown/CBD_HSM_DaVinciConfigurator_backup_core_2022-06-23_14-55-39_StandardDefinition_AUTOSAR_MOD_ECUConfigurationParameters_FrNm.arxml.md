# FrNm

## 模块描述

The Flexray Nm module

## 容器列表

### 1. FrNmChannelConfig

**描述**: This container contains the configuration parameters for all FlexRay NM channels.

该容器没有参数。

### 2. FrNmChannel

**描述**: This container contains the configuration parameters for a FlexRay NM Channel.

该容器没有参数。

### 3. FrNmChannelIdentifiers

**描述**: This container contains instance specific identifiers related to the respective FlexRay Channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmCarWakeUpBitPosition
  长名称: ''
  描述: Specifies the Bit position of the CWU within the NM-Message.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: FrNmCarWakeUpBytePosition
  长名称: ''
  描述: Specifies the Byte position of the CWU within the NM-Message.
  默认值: ''
  最小值: 2
  最大值: 7
- 
  序号: 3
  名称: FrNmCarWakeUpFilterEnabled
  长名称: ''
  描述: If CWU filtering is supported, only the CWU bit within the NM message with source node
      identifier
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrNmCarWakeUpFilterNodeId
  长名称: ''
  描述: Source node identifier for CWU filtering. If CWU filtering is supported, only the CWU bit
      within the NM
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: FrNmCarWakeUpRxEnabled
  长名称: ''
  描述: Enables or disables support of CarWakeUp bit evaluation in received NM messages.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrNmControlBitVectorActive
  长名称: ''
  描述: This parameter is used to activate or deactivate the control bit vector support for a Fr Nm
      Channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrNmNodeId
  长名称: ''
  描述: NM node identifier configured for the respective FlexRay Channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: FrNmPduScheduleVariant
  长名称: ''
  描述: This parameter defines the PDU scheduling variant that should be used for this channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FrNmPnEnabled
  长名称: ''
  描述: Enables or disables support of partial networking.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FrNmPnEraCalcEnabled
  长名称: ''
  描述: Specifies if FrNm calculates the PN request information for external requests. (ERA)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FrNmRepeatMessageBitActive
  长名称: ''
  描述: This parameter is used to activate or deactivate the repeat message bit support for a Fr Nm
      Channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FrNmSynchronizationPointEnabled
  长名称: ''
  描述: This parameter defines if this channel shall provide the synchronization point indication to
      the NM Interface.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FrNmRxPdu

**描述**: This container describes the FlexRay NM RX PDU:s.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmRxPduContainsData
  长名称: ''
  描述: This parameted defines if the PDU contains NM Data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrNmRxPduContainsVote
  长名称: ''
  描述: This parameted defines if the PDU contains NM Vote information.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrNmRxPduId
  长名称: ''
  描述: PDU identifier configured for the respective FlexRay Channel.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. FrNmTxPdu

**描述**: This container describes the FlexRay NM TX PDU:s.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the FrNmTxPdu to the
      LowerLayer.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: FrNmTxPduContainsData
  长名称: ''
  描述: This parameted defines if the PDU contains NM Data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrNmTxPduContainsVote
  长名称: ''
  描述: This parameted defines if the PDU contains NM Vote information.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. FrNmUserDataTxPdu

**描述**: This optional container is used to configure the UserNm PDU. This container is only available if
FrNmComUserDataSupport is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmTxUserDataPduId
  长名称: ''
  描述: This parameter defines the Handle ID of the NM User Data I-PDU.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. FrNmChannelTiming

**描述**: This container contains instance-specific timing related to the respective FlexRay  Channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmDataCycle
  长名称: ''
  描述: Number of FlexRay Schedule Cycles needed to transmit the NM Data of all ECUs on the FlexRay
      bus
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrNmMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the processing cycle of the main function of FrNm module in seconds.
  默认值: ''
  最小值: 0.001
  最大值: 0.02
- 
  序号: 3
  名称: FrNmMsgTimeoutTime
  长名称: ''
  描述: Timeout  of a NM-message. It determines in seconds how long the NM shall wait with
      notification of transmission failure while communication errors occur on the bus.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 4
  名称: FrNmReadySleepCnt
  长名称: ''
  描述: Numbers of repetitions in the ready sleep state before NM switches to bus sleep mode.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: FrNmRemoteSleepIndTime
  长名称: ''
  描述: Timeout for Remote Sleep Indication. It defines the time in seconds how long it shall take to
      recognize that all other nodes are ready to sleep.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 6
  名称: FrNmRepeatMessageTime
  长名称: ''
  描述: Timeout for Repeat Message State. Defines the time in seconds how long the NM shall stay in
      the Repeat Message State.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 7
  名称: FrNmRepetitionCycle
  长名称: ''
  描述: Number of Flexray Schedule Cycles used to repeat the transmission of the Nm vote of all ECUs
      on the Flexray Bus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrNmSyncLossTimer
  长名称: ''
  描述: Initial value for the SyncLossTimer in seconds.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: FrNmVoteInhibitionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the inhibition of vote changes from the next-to-last
      repetition cycle to the last repetition cycle before the Ready Sleep Counter expires.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FrNmVotingCycle
  长名称: ''
  描述: Number of FlexRay Schedule Cycles needed to transmit the Nm vote of all ECUs on the FlexRay
      Bus.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. FrNmGlobalConfig

**描述**: This container contains all global configuration parameters for the FrNm module.

该容器没有参数。

### 9. FrNmGlobalConstants

**描述**: This container contains module constants related to the FlexRay NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmNumberOfClusters
  长名称: ''
  描述: Number of AUTOSAR FR NM clusters allowed within one ECU.
  默认值: ''
  最小值: 1
  最大值: 255
```

### 10. FrNmGlobalFeatures

**描述**: This container contains module features related to the FlexRay NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmBusSynchronizationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the bus synchronisation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrNmComUserDataSupport
  长名称: ''
  描述: Enable/disable the user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrNmControlBitVectorEnabled
  长名称: ''
  描述: Pre-processor switch for enabling control bit vector support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrNmCoordinatorSyncSupport
  长名称: ''
  描述: Enables/disables the coordinator synchronisation support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrNmCycleCounterEmulation
  长名称: ''
  描述: Pre-processor switch for enabling the cycle counter emulation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrNmDualChannelPduEnable
  长名称: ''
  描述: Pre-processor switch for enabling the support of dual channel transmission and reception of NM
      messages.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrNmHwVoteEnable
  长名称: ''
  描述: Pre-processor switch for enabling the processing of FlexRay Hardware aggregated NM-Votes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrNmNodeDetectionEnabled
  长名称: ''
  描述: Pre-processor switch for enabling node detection support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FrNmPassiveModeEnabled
  长名称: ''
  描述: Pre-processor switch for enabling Passive Mode Configuration support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FrNmPduRxIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling PDU reception indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FrNmPnEiraCalcEnabled
  长名称: ''
  描述: Specifies if FrNm calculates the PN request information for internal an external requests.
      (EIRA)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FrNmPnResetTime
  长名称: ''
  描述: Specifies the runtime of the reset timer in seconds. This reset time is valid for the reset of
      PN requests in the EIRA and in the ERA. The value shall be the same for every channel.
      Thus it is a global config parameter.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 13
  名称: FrNmRemoteSleepIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling remote sleep indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: FrNmRepeatMessageBitEnabled
  长名称: ''
  描述: Pre-processor switch for enabling the repeat message bit support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FrNmSourceNodeIdentifierEnabled
  长名称: ''
  描述: Pre-processor switch for enabling SourceNodeIdentifier support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: FrNmStateChangeIndicationEnabled
  长名称: ''
  描述: Pre-processor switch for enabling state change indication.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: FrNmUserDataEnabled
  长名称: ''
  描述: Pre-processor switch for enabling user data support.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: FrNmVotingNextToLastRepetitionCycleDisable
  长名称: ''
  描述: Pre-processor switch for disabling vote changes in the last two
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. FrNmPnInfo

**描述**: PN information configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmPnInfoLength
  长名称: ''
  描述: Specifies the length of the PN request information in the NM message.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: FrNmPnInfoOffset
  长名称: ''
  描述: Specifies the offset of the PN request information in the NM message.
  默认值: 0
  最小值: 1
  最大值: 7
```

### 12. FrNmPnFilterMaskByte

**描述**: Filter mask byte configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmPnFilterMaskByteIndex
  长名称: ''
  描述: Index of the filter mask byte. Specifies the position within the filter mask byte array.
  默认值: ''
  最小值: 0
  最大值: 6
- 
  序号: 2
  名称: FrNmPnFilterMaskByteValue
  长名称: ''
  描述: Parameter to configure the filter mask byte.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 13. FrNmGlobalProperties

**描述**: This container contains module properties related to the FlexRay NM functionality.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrNmDevErrorDetect
  长名称: ''
  描述: Pre-processor switch for enabling development error detection
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrNmMainAcrossFrCycle
  长名称: ''
  描述: Parameter describing if the execution of FrNm_Main function crosses the FlexRay cycle boundary
      or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrNmVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: ''
  最小值: ''
  最大值: ''
```

