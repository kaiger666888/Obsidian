# FrIf

## 模块描述

Configuration of the FrIf (FlexRay Interface) module.

## 容器列表

### 1. FrIfConfig

**描述**: Configuration of the FlexRay Interface. This container is a MultipleConfigurationContainer, i.e.
this container and its sub-containers exist once per configuration set.

该容器没有参数。

### 2. FrIfCluster

**描述**: This container specifies a FrIf Cluster and all related data which is required to enable
communication of the Cluster. A Cluster may consist of more than one Controller.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfClstIdx
  长名称: ''
  描述: This parameter provides a zero-based consecutive index of the FlexRay Clusters. Upper layer
      BSW modules and the FrIf itself use this index to identify a FlexRay Cluster.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 2
  名称: FrIfDetectNITError
  长名称: ''
  描述: Indicates whether NIT error status of each cluster shall be detected or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrIfGChannels
  长名称: ''
  描述: The channels that are used by the cluster.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrIfGColdStartAttempts
  长名称: ''
  描述: Maximum number of times a node in the cluster is permitted to attempt to start the cluster by
      initiating schedule synchronization
  默认值: ''
  最小值: 2
  最大值: 31
- 
  序号: 5
  名称: FrIfGCycleCountMax
  长名称: ''
  描述: Maximum cycle counter value in a given cluster.
  默认值: ''
  最小值: 7
  最大值: 63
- 
  序号: 6
  名称: FrIfGListenNoise
  长名称: ''
  描述: Upper limit for the start up listen timeout and wake up listen timeout in the presence of
      noise. It is used as a multiplier of the node
  默认值: ''
  最小值: 2
  最大值: 16
- 
  序号: 7
  名称: FrIfGMacroPerCycle
  长名称: ''
  描述: Number of macroticks in a communication cycle.
  默认值: ''
  最小值: 8
  最大值: 16000
- 
  序号: 8
  名称: FrIfGMaxWithoutClockCorrectFatal
  长名称: ''
  描述: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of
      consecutive even/odd Cycle pairs with missing clock correction terms that will cause the
      protocol to transition from the POC:normal active or POC:normal passive state into the
      POC:halt state. [Even/odd cycle pairs].
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 9
  名称: FrIfGMaxWithoutClockCorrectPassive
  长名称: ''
  描述: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of
      consecutive even/odd Cycle pairs with missing clock correction terms that will cause the
      protocol to transition from the POC:normal active state to the POC:normal passive state.
      [Even/Odd cycle pairs]
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 10
  名称: FrIfGNetworkManagementVectorLength
  长名称: ''
  描述: Length of the Network Management vector in a cluster [bytes]
  默认值: ''
  最小值: 0
  最大值: 12
- 
  序号: 11
  名称: FrIfGNumberOfMinislots
  长名称: ''
  描述: Number of minislots in the dynamic segment
  默认值: ''
  最小值: 0
  最大值: 7988
- 
  序号: 12
  名称: FrIfGNumberOfStaticSlots
  长名称: ''
  描述: Number of static slots in the static segment
  默认值: ''
  最小值: 2
  最大值: 1023
- 
  序号: 13
  名称: FrIfGPayloadLengthStatic
  长名称: ''
  描述: Payload length of a static frame [16 bit words]
  默认值: ''
  最小值: 0
  最大值: 127
- 
  序号: 14
  名称: FrIfGSyncFrameIDCountMax
  长名称: ''
  描述: Maximum number of distinct syncframe identifiers present in a  given cluster. This parameter
      maps to FlexRay Protocol 2.1 Rev. A parameter gSyncNodeMax.
  默认值: ''
  最小值: 2
  最大值: 15
- 
  序号: 15
  名称: FrIfGdActionPointOffset
  长名称: ''
  描述: Number of macroticks the action point is offset from the beginning of a static slot.
  默认值: ''
  最小值: 1
  最大值: 63
- 
  序号: 16
  名称: FrIfGdBit
  长名称: ''
  描述: Nominal bit time in seconds
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: FrIfGdCasRxLowMax
  长名称: ''
  描述: Upper limit of the CAS acceptance windows [gdBit]
  默认值: ''
  最小值: 28
  最大值: 254
- 
  序号: 18
  名称: FrIfGdCycle
  长名称: ''
  描述: Length of the cycle, expressed in [s]
  默认值: ''
  最小值: 2.4E-5
  最大值: 0.016
- 
  序号: 19
  名称: FrIfGdDynamicSlotIdlePhase
  长名称: ''
  描述: Duration of the idle phase within a dynamic slot [Minislots].
  默认值: ''
  最小值: 0
  最大值: 2
- 
  序号: 20
  名称: FrIfGdIgnoreAfterTx
  长名称: ''
  描述: Duration for which the bitstrobing is paused after transmission [gdBit].
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 21
  名称: FrIfGdMacrotick
  长名称: ''
  描述: Duration of the cluster wide nominal macrotick, expressed in s
  默认值: ''
  最小值: 1E-6
  最大值: 6E-6
- 
  序号: 22
  名称: FrIfGdMiniSlotActionPointOffset
  长名称: ''
  描述: Number of Macroticks the Minislot action point is offset from the beginning of a Minislot
      [Macroticks].
  默认值: ''
  最小值: 1
  最大值: 31
- 
  序号: 23
  名称: FrIfGdMinislot
  长名称: ''
  描述: Duration of a minislot [Macroticks]
  默认值: ''
  最小值: 2
  最大值: 63
- 
  序号: 24
  名称: FrIfGdNit
  长名称: ''
  描述: Duration of the Network Idle Time [Macroticks]
  默认值: ''
  最小值: 2
  最大值: 15978
- 
  序号: 25
  名称: FrIfGdSampleClockPeriod
  长名称: ''
  描述: Sample clock period
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: FrIfGdStaticSlot
  长名称: ''
  描述: Duration of a static slot [Macroticks].
  默认值: ''
  最小值: 3
  最大值: 664
- 
  序号: 27
  名称: FrIfGdSymbolWindow
  长名称: ''
  描述: Duration of the symbol window [Macroticks].
  默认值: ''
  最小值: 0
  最大值: 162
- 
  序号: 28
  名称: FrIfGdSymbolWindowActionPointOffset
  长名称: ''
  描述: Number of macroticks the action point offset is from the beginning of the symbol window
      [Macroticks].
  默认值: ''
  最小值: 1
  最大值: 63
- 
  序号: 29
  名称: FrIfGdTSSTransmitter
  长名称: ''
  描述: Number of bits in the Transmission Start Sequence [gdBits].
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 30
  名称: FrIfGdWakeupRxIdle
  长名称: ''
  描述: Number of bits used by the node to test the duration of the 'idle' or HIGH phase of a received
      wakeup [gdBit]. Remarks: This parameter maps to FlexRay Protocol 2.1 Rev. A parameter
      gdWakeupSymbolRxIdle. Lower limit 14 for FlexRay Protocol 2.1 Rev. A compliance.
  默认值: ''
  最小值: 8
  最大值: 59
- 
  序号: 31
  名称: FrIfGdWakeupRxLow
  长名称: ''
  描述: Number of bits used by the node to test the duration of the LOW phase of a received wakeup
      [gdBit].
  默认值: ''
  最小值: 8
  最大值: 59
- 
  序号: 32
  名称: FrIfGdWakeupRxWindow
  长名称: ''
  描述: The size of the window used to detect wakeups [gdBit].
  默认值: ''
  最小值: 76
  最大值: 485
- 
  序号: 33
  名称: FrIfGdWakeupTxActive
  长名称: ''
  描述: Number of bits used by the node to transmit the LOW phase of awakeup symbol and  the HIGH and
      LOW phases of a WUDOP [gdBit].
  默认值: ''
  最小值: 15
  最大值: 60
- 
  序号: 34
  名称: FrIfGdWakeupTxIdle
  长名称: ''
  描述: Number of bits used by the node to transmit the 'idle' part of a
  默认值: ''
  最小值: 45
  最大值: 180
- 
  序号: 35
  名称: FrIfMainFunctionPeriod
  长名称: ''
  描述: The execution cycle of the FrIf_MainFunction_<cluster>() in seconds. The FrIf does not require
      this information but the BSW scheduler, which invokes the cluster main functions, needs
      it in order to plan its tasks.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 36
  名称: FrIfMaxIsrDelay
  长名称: ''
  描述: The maximum delay in macroticks the FrIf_JoblistExec_<cluster>() function is processed after
      the absolute timer interrupt was triggered.
  默认值: ''
  最小值: 0
  最大值: 10240000
- 
  序号: 37
  名称: FrIfSafetyMargin
  长名称: ''
  描述: Additional timespan in macroticks which takes jitter into account to be able to set the
      JobListPointer to the next possible job which can be executed in case the FlexRay Job
      List Execution Function has be resynchronized.
  默认值: ''
  最小值: 0
  最大值: 10240000
```

### 3. FrIfClusterDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. FrIfController

**描述**: This container contains the configuration of FlexRay CC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfCtrlIdx
  长名称: ''
  描述: This parameter provides a zero-based consecutive index of the FlexRay Communication
      Controllers. Upper layer BSW modules and the FrIf itself use this index to identify a
      FlexRay CC.
  默认值: ''
  最小值: 0
  最大值: 31
```

### 5. FrIfFrameTriggering

**描述**: A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference
to the Frame Construction Plan.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfAllowDynamicLSduLength
  长名称: ''
  描述: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the
      related CC buffer has to be reconfigured for the actual length and Header-CRC before
      transmission of the L-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrIfAlwaysTransmit
  长名称: ''
  描述: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this
      L-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrIfBaseCycle
  长名称: ''
  描述: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 4
  名称: FrIfChannel
  长名称: ''
  描述: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrIfCycleRepetition
  长名称: ''
  描述: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..
  默认值: ''
  最小值: 1
  最大值: 64
- 
  序号: 6
  名称: FrIfLSduLength
  长名称: ''
  描述: The payload length of the Frame is given here. This parameter is required for validation if
      configured PDUs and update information fits into the Frame at configuration time
      [bytes].
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 7
  名称: FrIfMessageId
  长名称: ''
  描述: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted
      in the
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: FrIfPayloadPreamble
  长名称: ''
  描述: Switching the Payload Preamble bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FrIfSlotId
  长名称: ''
  描述: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.
  默认值: ''
  最小值: 1
  最大值: 2047
```

### 6. FrIfFrameTriggeringDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 7. FrIfLPdu

**描述**: Reference to a L-PDU index

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfLPduIdx
  长名称: ''
  描述: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay
      Driver.
  默认值: ''
  最小值: 0
  最大值: 4095
- 
  序号: 2
  名称: FrIfReconfigurable
  长名称: ''
  描述: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means
      that this LPdu can be assigned to a different FrameTriggering at runtime. However, this
      reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be
      reconfigured.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. FrIfTransceiver

**描述**: Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a
Controller-Transceiver assignment.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfClusterChannel
  长名称: ''
  描述: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the
      Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A
      == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. FrIfJobList

**描述**: This container specifies a list of all FlexRay Jobs of the Cluster to be performed by
FrIf_JobListExec_<ClstIdx>().

该容器没有参数。

### 10. FrIfJob

**描述**: A job may contain more than one operation that are executed at a specific point in time.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfCycle
  长名称: ''
  描述: The FlexRay Cycle in which the communication operation will execute this job
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 2
  名称: FrIfMacrotick
  长名称: ''
  描述: Macrotick offset in the Cycle [Macrotick]
  默认值: ''
  最小值: 0
  最大值: 10240000
```

### 11. FrIfCommunicationOperation

**描述**: A separate operation which is part of a FlexRay Job and defines what type of action is executed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfCommunicationAction
  长名称: ''
  描述: The action to be performed in the FlexRay Operation
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrIfCommunicationOperationIdx
  长名称: ''
  描述: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values
      and thus defines the order of the FlexRay Communication Operation in the respective
      FlexRay Communication Job.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: FrIfRxComOpMaxLoop
  长名称: ''
  描述: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a
      FIFO).
  默认值: ''
  最小值: 1
  最大值: 512
```

### 12. FrIfFrameStructure

**描述**: The Frame structure specifies a Construction Plan how a Frame is assembled with PDUs and their
respective Update-Bits.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfByteOrder
  长名称: ''
  描述: This parameter defines the ByteOrder of all Pdus that are mapped into the Frame.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. FrIfPdusInFrame

**描述**: This container holds all the information about a PDU in a FlexRay Frame.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfPduOffset
  长名称: ''
  描述: The value specifies the offset of the PDU within the Frame [bytes].
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: FrIfPduUpdateBitOffset
  长名称: ''
  描述: This value specifies where the PDU's Update-Bit is stored in the Frame (bit location of PDU's
      Update-Bit in the FlexRay Frame).
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 14. FrIfPdu

**描述**: Contains PDU information. A PDU may be either a transmission PDU or a reception PDU.

该容器没有参数。

### 15. FrIfRxPdu

**描述**: Receive PDU

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfRxIndicationName
  长名称: ''
  描述: This parameter defines the name of the <User_RxIndication>. This parameter depends on the
      parameter FRIF_USERRXINDICATION_UL. If FRIF_USERRXINDICATION_UL equals FR_TP, FR_NM,
      PDUR or XCP, the name of the <User_RxIndication> is fixed. If FRIF_USERRXINDICATION_UL
      equals CDD, the name of the <User_RxIndication> is selectable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrIfUserRxIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the indication of the successfully
      received FRIFRXPDU has to be routed via <User_RxIndication>. This <User_RxIndication>
      has to be invoked when the indication of the configured FRIFRXPDU will be received by a
      Rx indication event from the FR Driver module. If no upper layer (UL) module is
      configured, no <User_RxIndication> has to be called in case of a Rx indication event of
      the FRIFRXPDU from the FR Driver module.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. FrIfTxPdu

**描述**: This container specifies transmission PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfConfirm
  长名称: ''
  描述: Defines whether the transmission of a PDU should be checked and confirmed to the PDU owning
      BSW module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrIfCounterLimit
  长名称: ''
  描述: This value states the maximum number of indication of ready PDU data to the FrIf (i.e. maximum
      number of invocations of FrIf_Transmit) without an intermediate transmission of the PDU.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 3
  名称: FrIfImmediate
  长名称: ''
  描述: Defines whether the PDU is transmitted immediate or decoupled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrIfNoneMode
  长名称: ''
  描述: Using the "None-Mode" which means that there is no API FrIf_Transmit call of the upper layer
      for this PDU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrIfTxConfirmationName
  长名称: ''
  描述: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the
      parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of
      the <User_TxConfirmation> is fixed. If FrIfUserTxUL equals CDD, the name of the
      <User_TxConfirmation> is selectable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrIfTxPduId
  长名称: ''
  描述: The global PDU identifier, which has to be used by the upper layer BSW module. The identifier
      has to be zero based and consecutive.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: FrIfUserTriggerTransmitName
  长名称: ''
  描述: This parameter defines the name of the <User_TriggerTransmit>. This parameter depends on the
      parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of
      the <User_TriggerTransmit> is fixed. If FrIfUserTxUL equals CDD, the name of the
      <User_TriggerTransmit> is selectable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrIfUserTxUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the trigger of the to be
      transmitted FRIFTXPDUID (via the <User_TriggerTransmit>) or the confirmation of the
      successfully transmitted FRIFTXPDUID has to be routed (via the <User_TxConfirmation>).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. FrIfGeneral

**描述**: This container contains the general configuration parameters of the FlexRay Interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrIfAbsTimerIdx
  长名称: ''
  描述: Maximum number of supported absolut timers.
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 2
  名称: FrIfAllSlotsSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable of switching from
      key-slot / single-slot mode to all slot mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrIfCancelTransmitSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to request the cancellation of the
      I-PDU transmission to FrDrv.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrIfDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification on or off
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrIfDisableLPduSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to disables the hardware resource of a
      LPdu for transmission/reception.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrIfDisableTransceiverBranchSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to disable branches of an active star.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrIfEnableTransceiverBranchSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable branches of an active star.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrIfGetClockCorrectionSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable of polling the
      FlexRay Driver to getting CC clock correction values.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FrIfGetGetChannelStatusSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable of polling the
      FlexRay Driver to getting error information about the FlexRay communications bus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FrIfGetNmVectorSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to request the FlexRay hardware
      NMVector.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FrIfGetNumOfStartupFramesSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable of polling the
      FlexRay Driver for the actual number of received startup frames on the bus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FrIfGetSyncFrameListSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable of polling the
      FlexRay Driver to getting a list of actual received sync frames.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: FrIfGetTransceiverErrorSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to get the FlexRay Transceiver errors
      by calling the FlexRay Transceiver module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: FrIfGetWakeupRxStatusSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to get the wakeup received information
      from the FlexRay controller.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FrIfNumClstSupported
  长名称: ''
  描述: Maximum number of FlexRay Clusters that the FlexRay Interface supports.
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 16
  名称: FrIfNumCtrlSupported
  长名称: ''
  描述: Maximum number of FlexRay CCs that the FlexRay Interface supports
  默认值: ''
  最小值: 1
  最大值: 15
- 
  序号: 17
  名称: FrIfPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs. Range of
      characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: FrIfReadCCConfigApi
  长名称: ''
  描述: Configuration parameter to enable/disable the optional FrIf_ReadCCConfig API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: FrIfReconfigLPduSupport
  长名称: ''
  描述: Configuration parameter to enable/disable FrIf support to enable/disable the reconfiguration
      of a given LPdu according to the parameters (FrameId, Channel, CycleRepetition,
      CycleOffset, PayloadLength, HeaderCRC) at runtime.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: FrIfUnusedBitValue
  长名称: ''
  描述: Set unused bits to a defined value.
  默认值: ''
  最小值: 0
  最大值: 1
- 
  序号: 21
  名称: FrIfVersionInfoApi
  长名称: ''
  描述: Enables/disables the existence of the FrIf_GetVersionInfo() API service
  默认值: ''
  最小值: ''
  最大值: ''
```

