# Fr

## 模块描述

Configuration of the Fr (FlexRay driver) module.

## 容器列表

### 1. FrGeneral

**描述**: General configuration (parameters) of the FlexRay Driver module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrBufferReconfig
  长名称: ''
  描述: Enables or disables buffer reconfiguration at runtime.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrCtrlTestCount
  长名称: ''
  描述: Maxmimum number of iterations the FlexRay controller hardware test is performed during
      controller initialization.
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: FrDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: FrNumCtrlSupported
  长名称: ''
  描述: Determines the maximum number of communication controllers that the driver supports.
  默认值: ''
  最小值: 1
  最大值: 256
- 
  序号: 6
  名称: FrRxStringentCheck
  长名称: ''
  描述: If stringent check is enabled (true), received frames are only
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrRxStringentLengthCheck
  长名称: ''
  描述: If stringent check is enabled (true), received frames are only
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrVersionInfoApi
  长名称: ''
  描述: Enables/disables the existence of the Fr_GetVersionInfo API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. FrMultipleConfiguration

**描述**: Configuration of the individual controllers.

该容器没有参数。

### 3. FrController

**描述**: Configuration of the individual controller.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrCtrlIdx
  长名称: ''
  描述: Determines index of CC within Fr.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: FrPAllowHaltDueToClock
  长名称: ''
  描述: Boolean flag that controls the transition to the POC:halt state due to a clock synchronization
      errors. If set to true, the CC is allowed to transition to POC:halt. If set to false,
      the CC will not transition to the POC:halt state but will enter or remain in the
      POC:normal passive state (self healing would still be possible)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrPAllowPassiveToActive
  长名称: ''
  描述: Number of consecutive even/odd cycle pairs that must have valid clock correction terms before
      the CC will be allowed to transition from the POC:normal passive state to POC:normal
      active state. If set to zero, the CC is not allowed to transition from POC:normal
      passive to POC:normal active
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 4
  名称: FrPChannels
  长名称: ''
  描述: Channels to which the node is connected.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrPClusterDriftDamping
  长名称: ''
  描述: Local cluster drift damping factor used for rate correction [Microticks].
  默认值: ''
  最小值: 0
  最大值: 20
- 
  序号: 6
  名称: FrPDecodingCorrection
  长名称: ''
  描述: Value used by the receiver to calculate the difference between primary time reference point
      and secondary time reference point [Microticks].
  默认值: ''
  最小值: 12
  最大值: 143
- 
  序号: 7
  名称: FrPDelayCompensationA
  长名称: ''
  描述: Value used to compensate for reception delays on the indicated channel. This covers assumed
      propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to
      0.05us [Microticks].
  默认值: ''
  最小值: 0
  最大值: 211
- 
  序号: 8
  名称: FrPDelayCompensationB
  长名称: ''
  描述: Value used to compensate for reception delays on the indicated channel. This covers assumed
      propagation delay up to cPropagationDelayMax for microticks in the range of 0.0125us to
      0.05us [Microticks].
  默认值: ''
  最小值: 0
  最大值: 211
- 
  序号: 9
  名称: FrPExternalSync
  长名称: ''
  描述: Flag indicating whether the node is externally synchronized (operating as time gateway sink in
      an TT-E cluster) or locally synchronized.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FrPFallBackInternal
  长名称: ''
  描述: Flag indicating whether a time gateway sink node will switch to local clock operation when
      synchronization with the time gateway source node is lost (FrPFallBackInternal = true)
      or will instead go to POC:ready (FrPFallBackInternal =false).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FrPKeySlotId
  长名称: ''
  描述: ID of the key slot, i.e., the slot used to transmit the startup frame, sync frame, or
      designated key slot frame. If this parameter is set to zero the node does not have a key
      slot.
  默认值: ''
  最小值: 0
  最大值: 1023
- 
  序号: 12
  名称: FrPKeySlotOnlyEnabled
  长名称: ''
  描述: Flag indicating whether or not the node shall enter key slot only mode following startup.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: FrPKeySlotUsedForStartup
  长名称: ''
  描述: Flag indicating whether the key slot is used to transmit a startup frame.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: FrPKeySlotUsedForSync
  长名称: ''
  描述: Flag indicating whether the key slot is used to transmit a sync frame.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FrPLatestTx
  长名称: ''
  描述: Number of the last minislot in which a frame transmission can start in the dynamic segment.
  默认值: ''
  最小值: 0
  最大值: 7988
- 
  序号: 16
  名称: FrPMacroInitialOffsetA
  长名称: ''
  描述: Integer number of macroticks between the static slot boundary and the following macrotick
      boundary of the secondary time reference point based on the nominal macrotick duration
      [Macroticks].
  默认值: ''
  最小值: 2
  最大值: 68
- 
  序号: 17
  名称: FrPMacroInitialOffsetB
  长名称: ''
  描述: Integer number of macroticks between the static slot boundary and the following macrotick
      boundary of the secondary time reference point based on the nominal macrotick duration
      [Macroticks].
  默认值: ''
  最小值: 2
  最大值: 68
- 
  序号: 18
  名称: FrPMicroInitialOffsetA
  长名称: ''
  描述: Number of microticks between the secondary time reference point
  默认值: ''
  最小值: 0
  最大值: 239
- 
  序号: 19
  名称: FrPMicroInitialOffsetB
  长名称: ''
  描述: Number of microticks between the secondary time reference point
  默认值: ''
  最小值: 0
  最大值: 239
- 
  序号: 20
  名称: FrPMicroPerCycle
  长名称: ''
  描述: Nominal number of microticks in the communication cycle of the local node. If nodes have
      different microtick durations this number will differ from node to node [Microticks].
  默认值: ''
  最小值: 640
  最大值: 1280000
- 
  序号: 21
  名称: FrPNmVectorEarlyUpdate
  长名称: ''
  描述: Flag indicating when the update of the Network Management Vector
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: FrPOffsetCorrectionOut
  长名称: ''
  描述: Magnitude of the maximum permissible offset correction value [Microticks]. Remark: Upper limit
      15567 for FlexRay Protocol 2.1 Rev A compliance. Remark: Lower limit 15 for FlexRay
      Protocol 3.0 compliance.
  默认值: ''
  最小值: 13
  最大值: 16082
- 
  序号: 23
  名称: FrPOffsetCorrectionStart
  长名称: ''
  描述: Start of the offset correction phase within the NIT, expressed as the number of macroticks
      from the start of cycle [Macroticks].
  默认值: ''
  最小值: 7
  最大值: 15999
- 
  序号: 24
  名称: FrPPayloadLengthDynMax
  长名称: ''
  描述: Maximum payload length for dynamic frames [16 bit words].
  默认值: ''
  最小值: 0
  最大值: 127
- 
  序号: 25
  名称: FrPRateCorrectionOut
  长名称: ''
  描述: Magnitude of the maximum permissible rate correction value and the maximum drift offset
      between two nodes operating with unsynchronized clocks for one communication cycle
      [Microticks].
  默认值: ''
  最小值: 2
  最大值: 3846
- 
  序号: 26
  名称: FrPSamplesPerMicrotick
  长名称: ''
  描述: Number of samples per microtick. Remark: Allowed range N1SAMPLES, N2SAMPLES for FlexRay
      Protocol 3.0 compliance.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: FrPSecondKeySlotId
  长名称: ''
  描述: ID of the second key slot, in which a second startup frame shall be sent when operating as a
      coldstart node in a TT-L or TT-D cluster. If this parameter is set to zero the node does
      not have a second key slot.
  默认值: ''
  最小值: 0
  最大值: 1023
- 
  序号: 28
  名称: FrPTwoKeySlotMode
  长名称: ''
  描述: Flag indicating whether node operates as a coldstart node in a TT-E or TT-L cluster.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: FrPWakeupChannel
  长名称: ''
  描述: Channel used by the node to send a wakeup pattern.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: FrPWakeupPattern
  长名称: ''
  描述: Number of repetitions of the wakeup symbol that are combined to form a wakeup pattern when the
      node enters the POC:wakeup send state.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 31
  名称: FrPdAcceptedStartupRange
  长名称: ''
  描述: Expanded range of measured clock deviation allowed for startup frames during integration
      [Microticks].
  默认值: ''
  最小值: 0
  最大值: 2743
- 
  序号: 32
  名称: FrPdListenTimeout
  长名称: ''
  描述: Value for the startup listen timeout and wakeup listen timeout. Although this is a node local
      parameter, the real time equivalent of this value should be the same for all nodes in
      the cluster [Microticks].
  默认值: ''
  最小值: 1284
  最大值: 2567692
- 
  序号: 33
  名称: FrPdMicrotick
  长名称: ''
  描述: Duration of a microtick.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FrAbsoluteTimer

**描述**: Specifies the absolute timer configuration parameters of the Fr.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrAbsTimerIdx
  长名称: ''
  描述: Contains the index of an absolute timer contained in Fr on a certain FlexRay CC.
  默认值: ''
  最小值: 0
  最大值: 254
```

### 5. FrControllerDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 6. FrFifo

**描述**: One First In First Out (FIFO) queued receive structure, defining the admittance criteria to the
FIFO, and mandating the ability to admit messages into the FIFO based on Message Id filtering
criteria.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrAdmitWithoutMessageId
  长名称: ''
  描述: Determines whether or not frames received in the dynamic segment that don't contain a message
      ID will be admitted into the FIFO.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrBaseCycle
  长名称: ''
  描述: FIFO cycle counter acceptance criteria.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 3
  名称: FrChannels
  长名称: ''
  描述: FIFO channel admittance criteria.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrCycleRepetition
  长名称: ''
  描述: FIFO cylce counter acceptance criteria. Valid values are  1,2,4,5,8,10,16,20,32,40,50,64.
  默认值: ''
  最小值: 1
  最大值: 64
- 
  序号: 5
  名称: FrFifoDepth
  长名称: ''
  描述: Fifo Depth.
  默认值: ''
  最小值: 1
  最大值: 2048
- 
  序号: 6
  名称: FrMsgIdMask
  长名称: ''
  描述: FIFO message identifier acceptance criteria (Mask filter).
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: FrMsgIdMatch
  长名称: ''
  描述: FIFO message identifier acceptance criteria (Match filter).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. FrRange

**描述**: FIFO Frame Id range acceptance criteria.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrRangeMax
  长名称: ''
  描述: Last FrameId of this range that will be accepted by the FIFO.
  默认值: ''
  最小值: 0
  最大值: 2047
- 
  序号: 2
  名称: FrRangeMin
  长名称: ''
  描述: First FrameId of this range that will be accepted by the FIFO.
  默认值: ''
  最小值: 0
  最大值: 2047
```

