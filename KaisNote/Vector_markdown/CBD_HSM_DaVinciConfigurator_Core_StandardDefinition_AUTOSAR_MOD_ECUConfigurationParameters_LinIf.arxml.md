# LinIf

## 模块描述

Configuration of the LinIf (LIN Interface) module.

## 容器列表

### 1. LinIfGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfCancelTransmitSupported
  长名称: ''
  描述: Global Pre-Compile Switch to reliably prevent the generation of the dummy LinIf_CancelTransmit
      API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIfDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinIfMultipleDriversSupported
  长名称: ''
  描述: States if multiple drivers are included in the LIN Interface or not. The reason for this
      parameter is to reduce the size of LIN Interface if multiple drivers are not used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinIfMultipleTrcvDriverSupported
  长名称: ''
  描述: States if multiple transceiver drivers are included in the LIN Interface or not. The reason
      for this parameter is to reduce the size of LIN Interface if multiple transceiver
      drivers are not used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: LinIfNcOptionalRequestSupported
  长名称: ''
  描述: States if the node configuration commands Assign NAD and Conditional Change NAD are supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: LinIfPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs. Range of
      characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: LinIfTpSupported
  长名称: ''
  描述: States if the TP is included in the LIN Interface or not. The reason for this parameter is to
      reduce the size of LIN Interface if the TP is not used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: LinIfTrcvDriverSupported
  长名称: ''
  描述: States if transceiver drivers are included in the LIN Interface or not. The reason for this
      parameter is to reduce the size of LIN Interface if transceiver drivers are not used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: LinIfVersionInfoApi
  长名称: ''
  描述: Switches the LinIf_GetVersionInfo function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. LinIfGlobalConfig

**描述**: This container contains the global configuration parameter of the LinIf.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfTimeBase
  长名称: ''
  描述: The delay between processing two frames is a multiple of the LIN Interface time-base in
      seconds.
  默认值: ''
  最小值: 0
  最大值: 0.255
```

### 3. LinIfChannel

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfChannelId
  长名称: ''
  描述: This parameter holds the unique channel index value. The value shall be the same as the
      ComMChannelId of the ComMChannel referenced by LinIfComMNetworkHandleRef.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: LinIfGotoSleepConfirmationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the confirmation of the goto-sleep
      command shall be sent.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinIfScheduleRequestConfirmationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the confirmation of the
      successfully performed schedule table change.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinIfStartupState
  长名称: ''
  描述: Defines the state of each LIN channel after startup
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: LinIfWakeupConfirmationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the confirmation of the wake-up
      shall be sent.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. LinIfFrame

**描述**: Generic container for all types of LIN frames. The shortName of this container is used as
LinIfFrameName.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfChecksumType
  长名称: ''
  描述: Type of checksum that the frame is using.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIfFrameType
  长名称: ''
  描述: Type of frame that is described (e.g. sporadic frame).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinIfLength
  长名称: ''
  描述: Length of the LIN SDU in bytes.
  默认值: ''
  最小值: 1
  最大值: 8
- 
  序号: 4
  名称: LinIfPid
  长名称: ''
  描述: Protected ID of the LIN frame. There is no reason to calculate the Parity in run-time.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 5. LinIfFixedFrameSdu

**描述**: In case this is a fixed frame this is the SDU (response).

该容器没有参数。

### 6. LinIfFixedFrameSduByte

**描述**: This container represents a byte within the 8 byte array.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfFixedFrameSduBytePos
  长名称: ''
  描述: Index of the Byte in the SDU (response) 8 byte array.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: LinIfFixedFrameSduByteVal
  长名称: ''
  描述: Byte value in the SDU (response) 8-byte array.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 7. LinIfInternalPdu

**描述**: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

该容器没有参数。

### 8. LinIfRxPdu

**描述**: represents a received PDU/frame

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfRxIndicationUL
  长名称: ''
  描述: This parameter defines the name of the <User_RxIndication>. This parameter depends on the
      parameter LinIfUserRxIndicationUL.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIfUserRxIndicationUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the indication of the successfully
      received LINRXPDUID has to be routed via <User_RxIndication>.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. LinIfSlaveToSlavePdu

**描述**: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the
response.

该容器没有参数。

### 10. LinIfTxPdu

**描述**: represents a transmitted PDU/frame

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfTxConfirmationUL
  长名称: ''
  描述: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the
      parameter LinIfUserTxUL.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIfTxPduId
  长名称: ''
  描述: Identifier of the Pdu for the upper layer.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: LinIfTxTriggerTransmitUL
  长名称: ''
  描述: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the
      parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the
      <User_TriggerTransmit> is fixed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinIfUserTxUL
  长名称: ''
  描述: This parameter defines the upper layer (UL) module to which the trigger of the transmitted
      LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully
      transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. LinIfSubstitutionFrames

**描述**: List of unconditional Frames that can be sent in a sporadic Frame slot.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfFramePriority
  长名称: ''
  描述: Priority of an unconditional frame if used as a sporadic frame.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 12. LinIfMaster

**描述**: Each Master can only be connected to one physical channel. This could be compared to the Node
parameter in a LDF file.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfClusterTimeBase
  长名称: ''
  描述: Defines a time-base for one LIN cluster in seconds (normally 0.002, 0.005 or 0.010s).
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 2
  名称: LinIfJitter
  长名称: ''
  描述: The jitter specifies the differences between the maximum and minimum delay from time base tick
      to the header sending start point in seconds.
  默认值: ''
  最小值: 0
  最大值: 0.255
```

### 13. LinIfScheduleTable

**描述**: Describes a schedule table. Each LinIfChannel may have several schedule tables. Each schedule table
can only be connected to one channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfResumePosition
  长名称: ''
  描述: Defines, where a schedule table shall be proceeded in case if it has been interrupted by a
      RUN-ONCE table.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: LinIfRunMode
  长名称: ''
  描述: The schedule table can be executed in two different modes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: LinIfScheduleMode
  长名称: ''
  描述: The schedule table can be executed in three different modes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinIfScheduleTableIndex
  长名称: ''
  描述: This is the unique index used by upper layers to identify a schedule. Note that the
      NULL_SCHEDULE for each channel has index 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: LinIfScheduleTableName
  长名称: ''
  描述: Optional schedule name used to cross-reference with a LDF. This parameter shall always be
      accompanied by LIN_IF_SCHEDULE_INDEX.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. LinIfEntry

**描述**: Describes an entry in the schedule table (also known as Frame Slot).

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfDelay
  长名称: ''
  描述: Delay to next entry in schedule table in seconds.
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 2
  名称: LinIfEntryIndex
  长名称: ''
  描述: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table
      is 0.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 15. LinIfSlave

**描述**: The Node attributes of the Slaves are provided with these parameter. The ShortName of this container
is used as LinIfNodeName.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfConfiguredNad
  长名称: ''
  描述: Definition of the initial node address
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: LinIfFunctionId
  长名称: ''
  描述: LIN function ID
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: LinIfProtocolVersion
  长名称: ''
  描述: Defines the LIN Protocol version which is used by the slave.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: LinIfSupplierId
  长名称: ''
  描述: LIN Supplier ID
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: LinIfVariant
  长名称: ''
  描述: Specifies the Variant ID
  默认值: ''
  最小值: 0
  最大值: 255
```

### 16. LinIfTransceiverDrvConfig

**描述**: This container contains the configuration (parameters) of all addressed LIN transceivers by each
underlying LIN Transceiver Driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: LinIfTrcvWakeupNotification
  长名称: ''
  描述: Selects whether wakeup indication notification is supported.
  默认值: false
  最小值: ''
  最大值: ''
```

