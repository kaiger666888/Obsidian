# Com

## 模块描述

Configuration of the AUTOSAR COM module.

## 容器列表

### 1. ComConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR COM module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComConfigurationId
  长名称: ''
  描述: This ID is returned by a call to Com_GetConfigurationId.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 2. ComGwMapping

该容器没有参数。

### 3. ComGwDestinationDescription

**描述**: Description of a gateway destination. This container allows defining a gateway destination without
the configuration of a complete COM signal. This allows adding / changing gateway relations post
build without the configuration of new signals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not
      in the shadow buffer. If the endianness conversion is configured to Opaque the parameter
      ComBitPosition shall define the bit0 of the first byte like in little endian byte order
  默认值: ''
  最小值: 0
  最大值: 2031
- 
  序号: 2
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComSignalInitValue
  长名称: ''
  描述: Initial value for this signal. The default value is 0.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComTransferProperty
  长名称: ''
  描述: Defines if a write access to this signal can trigger the transmission of the corresponding
      I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the
      corresponding I-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of update-bit inside I-PDU.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 4. ComFilter

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's Filters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: The range of values is specified in the [17] specification, chapter 2.2.2, Reception
      Filtering.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 5
  名称: ComFilterOffset
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: ComFilterPeriod
  长名称: ''
  描述: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 7
  名称: ComFilterX
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 5. ComGwSignal

**描述**: This container allows specifying a gateway source or destination respectively with a reference to a
ComSignal, a ComGroupSignal or a ComSignalGroup.

该容器没有参数。

### 6. ComGwSignal

**描述**: This container allows specifying a gateway source or destination respectively with a reference to a
ComSignal, a ComGroupSignal or a ComSignalGroup.

该容器没有参数。

### 7. ComGwSourceDescription

**描述**: Description of a gateway source. This container allows defining a gateway source without the
configuration of a complete COM signal. This allows adding / changing gateway relations post build
without the configuration of new signals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not
      in the shadow buffer. If the endianness conversion is configured to Opaque the parameter
      ComBitPosition shall define the bit0 of the first byte like in little endian byte order
  默认值: ''
  最小值: 0
  最大值: 2031
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComSignalLength
  长名称: ''
  描述: Description:
  默认值: ''
  最小值: 0
  最大值: 4095
- 
  序号: 5
  名称: ComSignalType
  长名称: ''
  描述: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found
      by examining the value of this attribute.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of update-bit inside I-PDU.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 8. ComIPdu

**描述**: Contains the configuration parameters of the AUTOSAR COM module's I-PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduCallout
  长名称: ''
  描述: This parameter defines the existence and the name of a callout function for the corresponding
      I-PDU. If this parameter is omitted no I-PDU callout shall take place for the
      corresponding I-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComIPduCancellationSupport
  长名称: ''
  描述: Defines for I-PDUs with ComIPduType NORMAL:
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComIPduDirection
  长名称: ''
  描述: The direction defines if this I-PDU, and therefore the contributing signals and signal groups,
      shall be sent or received.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComIPduHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU. The ComIPduHandleId is required by the API
      calls to receive I-PDUs from the PduR (ComIP-duDirection: Receive). For Tx-I-PDUs
      (ComIPduDirection: Send) this handle Id is used by the PduR to confirm the transmission
      of the ComIPdu. In case no Tx-Confirmation is configured for a Tx-I-PDU, the
      ComIPduHandleId is not used.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: ComIPduSignalProcessing
  长名称: ''
  描述: For the definition of the two modes Immediate and Deferred.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComIPduTriggerTransmitCallout
  长名称: ''
  描述: If there is a trigger transmit callout defined for this I-PDU this parameter contains the name
      of the callout function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComIPduType
  长名称: ''
  描述: Defines if this I-PDU is a normal I-PDU that can be sent unfragmented or if this is a large
      I-PDU that shall be sent via the Transport Protocol of the underlying bus.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. ComIPduCounter

**描述**: This optional container contains the configuration parameters of PDU Counter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduCounterErrorNotification
  长名称: ''
  描述: Name of Com_CbkCounterErr callback function to be called. If this
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComIPduCounterSize
  长名称: ''
  描述: Size of PDU Counter expressed in bits
  默认值: ''
  最小值: 1
  最大值: 8
- 
  序号: 3
  名称: ComIPduCounterStartPosition
  长名称: ''
  描述: Position of PDU counter expressed in bits from start position of data content
  默认值: ''
  最小值: 0
  最大值: 2031
- 
  序号: 4
  名称: ComIPduCounterThreshold
  长名称: ''
  描述: Threshold value of I-PDU counter algorithm, see COM590.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 10. ComIPduReplication

**描述**: This optional container contains the information needed for each I-PDU replicated.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduReplicationQuorum
  长名称: ''
  描述: The number of identical I-PDUs needed for successful voting.
  默认值: ''
  最小值: 1
  最大值: 3
```

### 11. ComTxIPdu

**描述**: This container contains additional transmission related configuration parameters of the AUTOSAR COM
module's I-PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMinimumDelayTime
  长名称: ''
  描述: Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU in
      seconds. The MDT is independent of the possible different transmission modes. There is
      only one minimum delay time parameter for one I-PDU. The minimum delay timer is not
      reset by changing the transmission mode. Hence, it is not allowed to violate the minimum
      delay time by transmission mode changes. It is not possible to monitor the minimum delay
      time for I-PDUs that are requested using the Com_TriggerTransmit API.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComTxIPduClearUpdateBit
  长名称: ''
  描述: Defines when the update-bits of signals or signal groups, contained in this I-PDU, will be
      cleared.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComTxIPduUnusedAreasDefault
  长名称: ''
  描述: The AUTOSAR COM module fills not used areas of an I-PDU with this byte pattern. This attribute
      is mandatory to avoid undefined behaviour. This byte-pattern will be repeated throughout
      the I-PDU before any init-values or update-bits were set.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 12. ComTxModeFalse

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes
in the case the ComFilter evaluates to false.

该容器没有参数。

### 13. ComTxMode

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComTxModeMode
  长名称: ''
  描述: The available transmission modes described in [18] shall be extended by the additional mode
      None.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComTxModeNumberOfRepetitions
  长名称: ''
  描述: Defines the number of repetitions for the transmission mode DIRECT and the event driven part
      of transmission mode MIXED.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComTxModeRepetitionPeriod
  长名称: ''
  描述: Defines the repetition period in seconds of the multiple transmissions in case
      ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is
      configured to DIRECT or MIXED. In case of the mixed transmission mode only the event
      driven part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: ComTxModeTimeOffset
  长名称: ''
  描述: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the
      first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In
      case of the mixed transmission mode only the periodic part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: ComTxModeTimePeriod
  长名称: ''
  描述: Defines the repetition period in seconds of the periodic transmission requests in case
      ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode
      only the periodic part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
```

### 14. ComTxModeTrue

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes
in the case the ComFilter evaluates to true.

该容器没有参数。

### 15. ComTxMode

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComTxModeMode
  长名称: ''
  描述: The available transmission modes described in [18] shall be extended by the additional mode
      None.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComTxModeNumberOfRepetitions
  长名称: ''
  描述: Defines the number of repetitions for the transmission mode DIRECT and the event driven part
      of transmission mode MIXED.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComTxModeRepetitionPeriod
  长名称: ''
  描述: Defines the repetition period in seconds of the multiple transmissions in case
      ComTxModeNumberOfRepetitions is configured greater than 1 and ComTxModeMode is
      configured to DIRECT or MIXED. In case of the mixed transmission mode only the event
      driven part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: ComTxModeTimeOffset
  长名称: ''
  描述: Defines the period in seconds between the start of the I-PDU by Com_IpduGroupControl and the
      first transmission request in case ComTxModeMode is configured to PERIODIC or MIXED. In
      case of the mixed transmission mode only the periodic part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: ComTxModeTimePeriod
  长名称: ''
  描述: Defines the repetition period in seconds of the periodic transmission requests in case
      ComTxModeMode is configured to PERIODIC or MIXED. In case of the mixed transmission mode
      only the periodic part is affected.
  默认值: ''
  最小值: 0
  最大值: 3600
```

### 16. ComIPduGroup

**描述**: Contains the configuration parameters of the AUTOSAR COM module's I-PDU groups.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduGroupHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU Group .
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 17. ComSignal

**描述**: Contains the configuration parameters of the AUTOSAR COM module's signals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not
      in the shadow buffer. If the endianness conversion is configured to Opaque the parameter
      ComBitPosition shall define the bit0 of the first byte like in little endian byte order
  默认值: ''
  最小值: 0
  最大值: 2031
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComDataInvalidAction
  长名称: ''
  描述: This parameter defines the action performed upon reception of an invalid signal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComErrorNotification
  长名称: ''
  描述: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComFirstTimeout
  长名称: ''
  描述: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is
      used immediately after start (or restart) of the deadline monitoring service. The
      timeout period of the successive periods is configured by COM263_Conf.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 6
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: ComInvalidNotification
  长名称: ''
  描述: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the
      function which notifies the RTE about the reception of an invalidated signal/ signal
      group. Only applicable if ComDataInvalidAction is configured to NOTIFY.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComNotification
  长名称: ''
  描述: On sender side: Name of Com_CbkTxAck callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComRxDataTimeoutAction
  长名称: ''
  描述: This parameter defines the action performed upon expiration of the  reception deadline
      monitoring timer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: ComSignalDataInvalidValue
  长名称: ''
  描述: Defines the data invalid value of the signal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComSignalInitValue
  长名称: ''
  描述: Initial value for this signal. The default value is 0.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: ComSignalLength
  长名称: ''
  描述: Description:
  默认值: ''
  最小值: 0
  最大值: 4095
- 
  序号: 14
  名称: ComSignalType
  长名称: ''
  描述: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found
      by examining the value of this attribute.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: ComTimeout
  长名称: ''
  描述: Defines the length of the deadline monitoring timeout period in seconds. The period for the
      first timeout period can be configured separately by COM183_Conf.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 16
  名称: ComTimeoutNotification
  长名称: ''
  描述: On sender side: Name of Com_CbkTxTOut callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: ComTransferProperty
  长名称: ''
  描述: Defines if a write access to this signal can trigger the transmission of the corresponding
      I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the
      corresponding I-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of update-bit inside I-PDU.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 18. ComFilter

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's Filters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: The range of values is specified in the [17] specification, chapter 2.2.2, Reception
      Filtering.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 5
  名称: ComFilterOffset
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: ComFilterPeriod
  长名称: ''
  描述: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 7
  名称: ComFilterX
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 19. ComSignalGroup

**描述**: Contains the configuration parameters of the AUTOSAR COM module's signal groups.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComDataInvalidAction
  长名称: ''
  描述: This parameter defines the action performed upon reception of an invalid signal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComErrorNotification
  长名称: ''
  描述: Only valid on sender side: Name of Com_CbkTxErr callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComFirstTimeout
  长名称: ''
  描述: Defines the length of the first deadline monitoring timeout period in seconds. This timeout is
      used immediately after start (or restart) of the deadline monitoring service. The
      timeout period of the successive periods is configured by COM263_Conf.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: ComInvalidNotification
  长名称: ''
  描述: Only valid on receiver side: Name of Com_CbkInv callback function to be called. Name of the
      function which notifies the RTE about the reception of an invalidated signal/ signal
      group. Only applicable if ComDataInvalidAction is configured to NOTIFY.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComNotification
  长名称: ''
  描述: On sender side: Name of Com_CbkTxAck callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComRxDataTimeoutAction
  长名称: ''
  描述: This parameter defines the action performed upon expiration of the  reception deadline
      monitoring timer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComTimeout
  长名称: ''
  描述: Defines the length of the deadline monitoring timeout period in seconds. The period for the
      first timeout period can be configured separately by COM183_Conf.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 9
  名称: ComTimeoutNotification
  长名称: ''
  描述: On sender side: Name of Com_CbkTxTOut callback function to be called.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: ComTransferProperty
  长名称: ''
  描述: Defines if a write access to this signal can trigger the transmission of the corresponding
      I-PDU. If the I-PDU is triggered, depends also on the transmission mode of the
      corresponding I-PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of update-bit inside I-PDU.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 20. ComGroupSignal

**描述**: This container contains the configuration parameters of group signals. I.e. signals that are
included within a signal group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: Starting position within the I-PDU. This parameter refers to the position in the I-PDU and not
      in the shadow buffer. If the endianness conversion is configured to Opaque the parameter
      ComBitPosition shall define the bit0 of the first byte like in little endian byte order
  默认值: ''
  最小值: 0
  最大值: 2031
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: ''
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: ComSignalDataInvalidValue
  长名称: ''
  描述: Defines the data invalid value of the signal.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComSignalInitValue
  长名称: ''
  描述: Initial value for this signal. The default value is 0.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComSignalLength
  长名称: ''
  描述: Description:
  默认值: ''
  最小值: 0
  最大值: 4095
- 
  序号: 8
  名称: ComSignalType
  长名称: ''
  描述: The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found
      by examining the value of this attribute.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComTransferProperty
  长名称: ''
  描述: Optionally defines whether this group signal shall contribute to the TRIGGERED_ON_CHANGE
      transfer property of the signal group. If at least one  group signal of a signal group
      has the "ComTransferProperty" configured all other group signals of that signal group
      shall have the attribute configured as well.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. ComFilter

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's Filters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: The range of values is specified in the [17] specification, chapter 2.2.2, Reception
      Filtering.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 5
  名称: ComFilterOffset
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: ComFilterPeriod
  长名称: ''
  描述: This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 7
  名称: ComFilterX
  长名称: ''
  描述: The name of this attribute corresponds to the parameter name in the [17] specification of
      Reception Filtering.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 22. ComTimeBase

**描述**: Contains the timebase parameters for Tx, Rx and routing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComGwTimeBase
  长名称: ''
  描述: The period between successive calls to Com_MainFunctionRouteSignals in seconds. This parameter
      may be used by the COM generator to transform the values of the signal gateway related
      timing configuration parameters of the COM module to internal implementation specific
      counter or tick values. The COM module's internal timing handling is implementation
      specific.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComRxTimeBase
  长名称: ''
  描述: The period between successive calls to Com_MainFunctionRx in seconds. This parameter may be
      used by the COM generator to transform the values of the reception related timing
      configuration parameters of the COM module to internal implementation specific counter
      or tick values. The COM module's internal timing handling is implementation specific.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 3
  名称: ComTxTimeBase
  长名称: ''
  描述: The period between successive calls to Com_MainFunctionTx in seconds. This parameter may be
      used by the COM generator to transform the values of the transmission related timing
      configuration parameters of the COM module to internal implementation specific counter
      or tick values. The COM module's internal timing handling is implementation specific.
  默认值: ''
  最小值: 0
  最大值: 3600
```

### 23. ComGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComConfigurationUseDet
  长名称: ''
  描述: The error hook shall contain code to call the Det.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComEnableMDTForCyclicTransmission
  长名称: ''
  描述: Enables globally for the whole Com module the minimum delay time monitoring for cyclic and
      repeated transmissions (ComTxModeMode=PERIODIC or ComTxModeMode=MIXED for the cyclic
      transmissions, ComTxModeNumberOfRepetitions > 0 for repeated transmissions).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComRetryFailedTransmitRequests
  长名称: ''
  描述: If this Parameter is set to true, retry of failed transmission requests is enabled. If this
      Parameter is not present, the default value is assumed.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComSupportedIPduGroups
  长名称: ''
  描述: Defines the maximum number of supported I-PDU groups.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: ComVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API (Com_GetVersionInfo).
  默认值: ''
  最小值: ''
  最大值: ''
```

