# Com

## 模块描述

The Com provides a signal-based communication interface to the upper layer (in an AUTOSAR system
this is the Rte) which the Com couples with the PduR by packing and unpacking signals to and from
pdus.
The Com also allows for signal and pdu based routing.
#Communication
#AUTOSAR

## 容器列表

### 1. ComConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR COM module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComConfigurationId
  长名称: ''
  描述: This ID is returned by a call to Com_GetConfigurationId.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: ComDataMemSize
  长名称: ''
  描述: |
    Size of internal Com data in units of bytes (static memory allocation) - memory required by
    post-build configuration must be smaller than this constant. This parameter is needed only in
    case of post-build loadable implementation using static memory allocation.
    Note: This parameter is not used by the generator.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComMaxIPduCnt
  长名称: ''
  描述: |
    Maximum number of IPdus. This paramterer is needed only in case of post-build loadable
    implementtation using static memory allocation.
    Note: This parameter is not used by the generator.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 4
  名称: ComRxDeferredEventCacheSize
  长名称: ''
  描述: This parameter defines the size of the deferred event cache.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: ComRxDeferredNotificationCacheSize
  长名称: ''
  描述: |
    This parameter defines the max. number of ComSignal or ComSignalGroup notifications or invalid
    notifications, which will be cached during unpacking of all received deferred ComIPdus with
    closed Rx ISR lock.
    If the number of (invalid) notifications exceeds the configured cache size, the Rx ISR lock will
    temporarily be opened and all cached (invalid) notifications will be called.
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: ComRxImmediateNotificationCacheSize
  长名称: ''
  描述: |
    This parameter defines the max. number of ComSignal or ComSignalGroup notifications or invalid
    notifications, which will be cached during unpacking of a received immediate ComIPdu with closed
    Rx ISR lock.
    If the number of (invalid) notifications exceeds the configured cache size, the Rx ISR lock will
    temporarily be opened and all cached (invalid) notifications will be called.
  默认值: 1
  最小值: 0
  最大值: 65535
```

### 2. ComGwMapping

**描述**: Each GwMapping represents one signal routing relation handled by COM. A signal routing relation has
one source signal and can have multiple destination signals. COM is able to route signals and group
signals.

该容器没有参数。

### 3. ComGwSignal

**描述**: This choice container allows referring signals and group signals that have been configured
explicitly in the COM configuration.

该容器没有参数。

### 4. ComGwDestinationDescription

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
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComSignalInitValue
  长名称: ''
  描述: |
    Initial value for this signal. The default value is 0.
    
    Note: This container is not used.
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
  默认值: PENDING
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComUpdateBitPosition
  长名称: ''
  描述: |
    Bit position of update-bit inside I-PDU.
    
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. ComFilter

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's Filters.

Note: This container is not used.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: |
    The supported filter algorithms for signals/group signals are:
    - Always: This filter always evaluates to TRUE
    - Never: This filter always evaluates to FALSE
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: ALWAYS
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: |
    The specified mask is used for the filters:
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
  默认值: 18446744073709551615
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: |
    The specified max value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: |
    The specified min value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 5
  名称: ComFilterOffset
  长名称: ''
  描述: |
    The name of this attribute corresponds to the parameter name in the [17] specification of
    Reception Filtering.
    Note: This parameter is not used by the generator.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 6
  名称: ComFilterPeriod
  长名称: ''
  描述: |
    This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
    Note: This parameter is not used by the generator.
  默认值: 2
  最小值: 2
  最大值: 4294967295
- 
  序号: 7
  名称: ComFilterX
  长名称: ''
  描述: |
    The specified value X is used for the filters:
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
```

### 6. ComGwSignal

**描述**: This choice container allows referring signals and group signals that have been configured
explicitly in the COM configuration.

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
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: 0
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComSignalEndianness
  长名称: ''
  描述: Defines the endianness of the signal's network representation.
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComSignalLength
  长名称: ''
  描述: For ComSignalType UINT8_N this parameter specifies the length n in bytes. For ComSignalType
      UINT8_DYN it specifies the maximum length in bytes. For all other types this parameter
      shall be ignored.
  默认值: 0
  最小值: 0
  最大值: 4095
- 
  序号: 5
  名称: ComSignalType
  长名称: ''
  描述: |
    The AUTOSAR type of the signal. Whether or not the signal is signed or unsigned can be found by
    examining the value of this attribute.
    
    Note: This parameter is only evaluated for distinguishing between array based signal types
    (UINT8_N) and non array based signal types.
  默认值: BOOLEAN
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of update-bit inside I-PDU.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 8. ComIPdu

**描述**: I-PDU configuration of COM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduCallout
  长名称: ''
  描述: |
    This parameter defines the existence and the name of the I-PDUs callout function.
    For Rx I-PDUs the callout function is called in the context of Com_RxIndication(). For Tx I-PDUs
    the callout function is called before the transmission is triggered by COM.
    If the parameter is undefined no callout function will be called.
    The API prototype is generated to Com_Cbk.h and has to be implemented by the application.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComIPduDirection
  长名称: ''
  描述: The direction defines if this I-PDU and the contributing signals and signal groups are sent or
      received.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComIPduHandleId
  长名称: ''
  描述: |
    The numerical value used as the ID of this I-PDU.
    The ComIPduHandleId is required by the API calls to receive Rx I-PDUs from the PduR.
    For Tx-I-PDUs this handle Id is used by the PduR to confirm the transmission of the ComIPdu and
    for the APIs Com_TriggerTransmit() and Com_TriggerIPDUSend()
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: ComIPduSignalProcessing
  长名称: ''
  描述: |
    This option determines the call context and the point of time when the signal notification
    function is called.
    - IMMEDIATE: The notification function is called within Com_TxConfirmation() or
    Com_RxIndication(). Depending on the lower layer interface, this might be in interrupt context.
    - DEFERRED: The notification function is called on task level during the next call cycle of
    Com_MainFunctionRx() or Com_MainFunctionTx().
                          Please note that the signal data of a received I-PDU is not updated until
    the next call to Com_MainfunctionRx().
  默认值: DEFERRED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComIPduTriggerTransmitCallout
  长名称: ''
  描述: |
    This parameter defines the existence and the name of a trigger callout function for the
    corresponding I-PDU.
    The function is called in the context of Com_TriggerTransmit() before the data are copied to the
    lower layer.
    The prototype is generated to Com_Cbk.h and has to be implemented by the application.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComIPduType
  长名称: ''
  描述: |
    Defines the lower layer type that is used to transmit/received the I-PDU.
    Defines if this I-PDU is a normal I-PDU that can be sent unfragmented or if this is a large
    I-PDU that shall be sent via the Transport Protocol of the underlying bus.
    
    NORMAL: indicates that the I-PDU is sent/received unfragmented.
    TP: indicates that the I-PDU is send/received fragmented by a Transport Protocol.
  默认值: NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComIPduCancellationSupport
  长名称: ''
  描述: Defines for I-PDUs with ComIPduType TP: If the underlying TP-module supports RX and TX
      cancellation of ongoing requests.
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. ComTxIPdu

**描述**: Additional transmission related configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMinimumDelayTime
  长名称: ''
  描述: |
    Defines the Minimum Delay Time (MDT) between successive transmissions of this I-PDU.
    The MDT is independent of the possible different transmission modes. There is only one minimum
    delay time parameter for one I-PDU. The minimum delay timer is not reset by changing the
    transmission mode. Hence, it is not allowed to violate the minimum delay time by transmission
    mode changes.
    It is not possible to monitor the minimum delay time for I-PDUs that are requested using the
    Com_TriggerTransmit API.
    
    Note: The actual Minimum Delay Time is incremented by one ComTxTimeBase to ensure the minimum
    delay in case of late receiving Tx confirmations.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComGwRoutingTimeout
  长名称: ''
  描述: Maximum Time between two routing events before a timeout occurs.
  默认值: 0.05
  最小值: 0
  最大值: 3600
- 
  序号: 3
  名称: ComTxIPduClearUpdateBit
  长名称: ''
  描述: |
    Defines when the update bits shall be cleared.
    Transmit: clear update bit in PduR_ComTransmit() context
    TriggerTransmit: clear update bit in Com_TriggerTransmit() context
    Confirmation: The update-bits are cleared when the transmission of the I-PDU was confirmed.
  默认值: Transmit
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComTxIPduUnusedAreasDefault
  长名称: ''
  描述: |
    Byte pattern that is used to fill in unused bits within an I-PDU.
    The byte-pattern will be repeated throughout the I-PDU before any initial values or update-bits
    are applied.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: ComMetaDataDefault
  长名称: ''
  描述: |
    The AUTOSAR COM module uses default MetaData when not triggered by
    Com_TriggerIPDUSendWithMetaData.
    
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. ComTxModeFalse

**描述**: Defines the I-PDU transmit behavior if the transmission mode state of the I-PDU is evaluated to
false.

该容器没有参数。

### 11. ComTxMode

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComTxModeMode
  长名称: ''
  描述: |
    The transmission mode determines the Tx properties of the IPDU:
    - DIRECT: The message is transmitted in the next Com_MainFunctionTx() call after a trigger event
    occurred.
    - PERIODIC: The IPDU is transmitted with the specified cycle time (ComTxModeTimePeriod).
    - MIXED: Combines the transmission modes of CYCLIC and DIRECT.
    - NONE: COM does not transmit the I-PDU. The transmission must be triggered by the lower layer
    through Com_TriggerTransmit().
    All transmission modes, except NONE, maintain the Minimum Delay Time (ComTxIPduMinimumDelayTime)
    and delay a transmission if required.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComTxModeNumberOfRepetitions
  长名称: ''
  描述: |
    Defines how often the I-PDU shall be transmitted after a single transmission trigger event.
    For the transmission mode DIRECT and the event driven part of transmission mode MIXED.
    
    If the parameter is configured to '0' the transmission is requested once by a trigger-event.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComTxModeRepetitionPeriod
  长名称: ''
  描述: |
    Defines the repetition period of the repeated transmissions in case ComTxModeNumberOfRepetitions
    is configured to a value greater 0 and the ComTxModeMode is configured to DIRECT or MIXED.
    In case of the mixed transmission mode only the event driven part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: ComTxModeTimeOffset
  长名称: ''
  描述: |
    Defines the period between the start of the I-PDU by Com_IpduGroupControl and the first
    transmission request to the lower layer if ComTxModeMode is configured to PERIODIC or MIXED.
    In case of the mixed transmission mode only the periodic part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: ComTxModeTimePeriod
  长名称: ''
  描述: |
    Defines the cycle time of periodic transmission requests in case ComTxModeMode is configured to
    PERIODIC or MIXED.
    In case of the mixed transmission mode only the periodic part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
```

### 12. ComTxModeTrue

**描述**: Defines the I-PDU transmit behavior if the transmission mode state of the I-PDU is evaluated to
true.

该容器没有参数。

### 13. ComTxMode

**描述**: This container contains the configuration parameters of the AUTOSAR COM module's transmission modes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComTxModeMode
  长名称: ''
  描述: |
    The transmission mode determines the Tx properties of the I-PDU:
    - DIRECT: The message is transmitted in the next Com_MainFunctionTx() call after a trigger event
    occurred.
    - PERIODIC: The I-PDU is transmitted with the specified cycle time (ComTxModeTimePeriod).
    - MIXED: Combines the transmission modes of CYCLIC and DIRECT.
    - NONE: COM does not transmit the I-PDUs. The transmission must be triggered by the lower layer
    through Com_TriggerTransmit().
    All transmission modes, except NONE, maintain the Minimum Delay Time (ComTxIPduMinimumDelayTime)
    and delay a transmission if required.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComTxModeNumberOfRepetitions
  长名称: ''
  描述: |
    Defines how often the I-PDU shall be transmitted after a single transmission trigger event.
    For the transmission mode DIRECT and the event driven part of transmission mode MIXED.
    
    If the parameter is configured to '0' the transmission is requested once by a trigger event.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ComTxModeRepetitionPeriod
  长名称: ''
  描述: |
    Defines the repetition period of the repeated transmissions in case ComTxModeNumberOfRepetitions
    is configured to a value greater 0 and the ComTxModeMode is configured to DIRECT or MIXED.
    In case of the mixed transmission mode only the event driven part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 4
  名称: ComTxModeTimeOffset
  长名称: ''
  描述: |
    Defines the period between the start of the I-PDU by Com_IpduGroupControl and the first
    transmission request to the lower layer if ComTxModeMode is configured to PERIODIC or MIXED.
    In case of the mixed transmission mode only the periodic part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: ComTxModeTimePeriod
  长名称: ''
  描述: |
    Defines the cycle time of periodic transmission requests in case ComTxModeMode is configured to
    PERIODIC or MIXED.
    In case of the mixed transmission mode only the periodic part is affected.
  默认值: 0
  最小值: 0
  最大值: 3600
```

### 14. ComIPduCounter

**描述**: This optional container contains the configuration parameters of PDU Counter.

Note: This container is not used by the generator.

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
  默认值: 1
  最小值: 1
  最大值: 8
- 
  序号: 3
  名称: ComIPduCounterStartPosition
  长名称: ''
  描述: Position of PDU counter expressed in bits from start position of data content
  默认值: 0
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

### 15. ComIPduReplication

**描述**: This optional container contains the information needed for each I-PDU replicated.

Note: This container is not used by the generator.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduReplicationQuorum
  长名称: ''
  描述: The number of identical I-PDUs needed for successful voting.
  默认值: 1
  最小值: 1
  最大值: 3
```

### 16. ComIPduGroup

**描述**: Defines one I-PDU group that is used to enable and disable the reception and transmission of a COM
I-PDU. Typically there is for each communication channel at least one I-PDU group for Rx I-PDUs and
one I-PDU group for Tx I-PDUs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComIPduGroupHandleId
  长名称: ''
  描述: The numerical value used as the ID of this I-PDU Group .
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 17. ComSignal

**描述**: Defines one Signal transmitted or received by COM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: |
    Start position of the signal within the I-PDU.
    The interpretation of the bit position depends on the signal endianness:
    BIG_ENDIAN: bit position refers to the MSB of the signal.
    LITTLE_ENDIAN: bit position refers to the LSB of the signal.
    OPAQUE: bit position refers to bit 0 of the first byte similar to the little endian byte order.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: 8
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComDataInvalidAction
  长名称: ''
  描述: |
    This parameter defines the action performed upon reception of an invalid signal.
    
    NOTIFY: The configured invalid notification is called and further signal processing (like signal
    indication) is abandoned. In this case the invalid value is not stored to preserve the last
    valid received value.
    REPLACE: The last received value is replaced by the initial value. Normal signal processing
    including filtering and handling of notifications does not take place.
  默认值: NOTIFY
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComErrorNotification
  长名称: ''
  描述: |
    Defines the name and existence of the error notification function that is called in case of
    transmit errors
    The notification is called for not confirmed send requests, if the corresponding I-PDU group is
    getting stopped or the COM module is de-initialized.
    
    The error notification function is not available for receive signals.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComFirstTimeout
  长名称: ''
  描述: |
    Timeout time that is used for reception deadline monitoring immediately after start (or restart)
    of the deadline monitoring service.
    If the parameter is undefined or configured to 0, the signal reception is not monitored from the
    BSW initialization until the I-PDU is received for the first time.
    After the first reception ComTimeout will be used o monitor signal reception.
    
    For signals without a configured update-bit, an I-PDU based deadline monitoring is used. The
    first timeout time is evaluated as smallest first timeout time of all signals and signal groups
    without configured update-bit of the I-PDU
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 6
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: ComInvalidNotification
  长名称: ''
  描述: |
    Defines the name and existence of callback function that is called if the signal has been
    identified to be invalid.
    The notification is called if the invalid action is configured to 'NOTIFY' and an invalid value
    is received.
    
    The call context depends on the configured signal processing of the corresponding I-PDU.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComNotification
  长名称: ''
  描述: |
    Defines the name and existence of a callback function.
    The notification is called
    for Tx signals, if the transmission of the signal is confirmed,
    for Rx signals, if the signal is received.
    
    The call context depends on the configured signal processing of the corresponding I-PDU.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComRxDataTimeoutAction
  长名称: ''
  描述: |
    If this parameter is configured to 'REPLACE', the initial value is set for this signal if a
    timeout occurred.
    If this parameter is configured to 'NONE' or undefined, the last received value is maintained.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: ComSignalDataInvalidValue
  长名称: ''
  描述: |
    Defines the invalid value of the signal. The invalid value is a dedicated value that is
    transmitted in case the application cannot provide a valid value. The reception of an invalid
    signal value can trigger special invalid handling on receiver side.
    
    The interpretation of the configured value depends on ComSignalType setting:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. Possible values are "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComSignalEndianness
  长名称: ''
  描述: |
    Defines the endianness of the signal's network representation.
    OPAQUE indicates that no byte order conversion is performed (e.g. for byte arrays).
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComSignalInitValue
  长名称: ''
  描述: |
    Defines the Initial value of the signal.
    The value is set during initialization of the module and if the corresponding I-PDU group is
    getting started with parameter 'initialize' set to 'true'.
    
    The interpretation of the configured value depends on ComSignalType setting:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. Possible values are "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: ComSignalLength
  长名称: ''
  描述: Indicates the signal length in bytes for signals with data type UINT8_N.
  默认值: 0
  最小值: 0
  最大值: 4095
- 
  序号: 14
  名称: ComSignalType
  长名称: ''
  描述: Specifies the data type that is used by the application to receive or transmit the signal
      through the COM APIs.
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: ComTimeout
  长名称: ''
  描述: |
    Timeout time that is used for deadline monitoring.
    If the value is configured to '0' or undefined, the signal is not monitored.
    
    For signals without a configured update-bit, an I-PDU based deadline monitoring is used. The
    timeout time is evaluated as smallest timeout time of all signals and signal groups without
    configured update-bit of the I-PDU.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 16
  名称: ComTimeoutNotification
  长名称: ''
  描述: |
    Defines the name and existence of the callback function that is called, if a timeout for the
    signal is detected.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: ComTransferProperty
  长名称: ''
  描述: |
    The transfer behavior for the transmission mode DIRECT or MIXED when writing to the signal can
    either be
    - TRIGGERED: the transmission of the message is triggered if the signal is written regardless of
    the signal value
    - TRIGGERED_WITHOUT_REPETITION: the transmission of the message is triggered just once without a
    repetition
    - TRIGGERED_ON_CHANGE: the transmission of the message is triggered if the signal is written and
    the signal value has changed
    - TRIGGERED_ON_CHANGE_WITHOUT_REPETITION: the transmission of the message is triggered just once
    without a repetition
    - PENDING: writing to the signal does not cause direct transmission.
  默认值: PENDING
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of the update-bit inside the I-PDU.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 19
  名称: ComRxDataTimeoutSubstitutionValue
  长名称: ''
  描述: |
    If this parameter and the ComRxDataTimeoutAction is configured to 'REPLACE',
    the signal value will be set to the value of this parameter, if a timeout occurred.
    The interpretation of the configured value depends on ComSignalType setting:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. Possible values are "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: ComSignalAccess
  长名称: ''
  描述: |
    The parameter ComSignalAccess gives the Com generator the information whether a Signal access is
    needed or not.
    All Signals with ComSignalAccess != ACCESS_NOT_NEEDED can be accessed.
    All Signals with ComSignalAccess == ACCESS_NOT_NEEDED cannot be accessed.
    
    ACCESS_NOT_NEEDED                       The Signal will never be accessed.
    ACCESS_UNCLEAR                  It is unclear if the Signal will be accessed.
    ACCESS_NEEDED_BY_SWC_OR_COM     It is clear that the Signal access is needed, e.g. by COM. This
    state is set by a validator
    ACCESS_NEEDED_BY_OTHER                  The Signal access is declared as to be needed. This
    state is set by the user.
  默认值: ACCESS_UNCLEAR
  最小值: ''
  最大值: ''
```

### 18. ComFilter

**描述**: Defines the filter that is applied on transmit signals. The filter result of each signal is used to
determine the TxMode that shall be used for transmitting the I-PDU.
For receive signal the filter is used to determine whether the reception event is forwarded to the
application or not.

Signal only have a filter if the ComFilter container exists.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: |
    The supported filter algorithms for signals are:
    - Always: This filter always evaluates to TRUE
    - Never: This filter always evaluates to FALSE
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: NEVER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: |
    The specified mask is used for the filters:
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
  默认值: 18446744073709551615
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: |
    The specified max value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: |
    The specified min value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 5
  名称: ComFilterX
  长名称: ''
  描述: |
    The specified value X is used for the filters:
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 6
  名称: ComFilterOffset
  长名称: ''
  描述: |
    The name of this attribute corresponds to the parameter name in the [17] specification of
    Reception Filtering.
    
    Note: This parameter is not used by the generator.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 7
  名称: ComFilterPeriod
  长名称: ''
  描述: |
    This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
    
    Note: This parameter is not used by the generator.
  默认值: 2
  最小值: 2
  最大值: 4294967295
```

### 19. ComSignalGroup

**描述**: Defines a signal group. Signal groups are used to transmit or receive its included group signals
consistently.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComDataInvalidAction
  长名称: ''
  描述: |
    This parameter defines the action performed if at least one of the included signals is an
    invalid signal.
    
    NOTIFY: The configured invalid notification is called and further signal processing (like signal
    indication) is abandoned. In this case the invalid value is not stored to preserve the last
    valid received value.
    REPLACE: The last received values of all group signals are replaced by the initial values.
    Normal signal processing including filtering and handling of notifications does not take place.
  默认值: NOTIFY
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComSignalGroupArrayAccess
  长名称: ''
  描述: Defines whether the uint8-array based access shall be used for this ComSignalGroup.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComErrorNotification
  长名称: ''
  描述: |
    Defines the name and existence of the error notification function that is called in case of
    transmit errors
    The notification is called for not confirmed send requests, if the corresponding I-PDU group is
    getting stopped or the COM module is de-initialized.
    
    The error notification function is not available for receive signal groups.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComFirstTimeout
  长名称: ''
  描述: |
    Timeout time that is used for reception deadline monitoring immediately after start (or restart)
    of the deadline monitoring service.
    If the parameter is undefined or configured to 0, the signal group reception is not monitored
    from the BSW initialization until the I-PDU is received for the first time.
    After the first reception ComTimeout will be used o monitor signal group reception.
    
    For signal groups without a configured update-bit, an I-PDU based deadline monitoring is used.
    The first timeout time is evaluated as smallest first timeout time of all signals and signal
    groups without configured update-bit of the I-PDU.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: ComInvalidNotification
  长名称: ''
  描述: |
    Defines the name and existence of callback function that is called if the signal has been
    identified to be invalid.
    The notification is called if the invalid action is configured to 'NOTIFY' and an invalid value
    is received.
    
    The call context depends on the configured signal processing of the corresponding I-PDU.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComNotification
  长名称: ''
  描述: |
    Defines the name and existence of a callback function.
    The notification is called
    for Tx signal groups, if the transmission of the signal group is confirmed,
    for Rx signal groups, if the signal group is received.
    
    The call context depends on the configured signal processing of the corresponding I-PDU.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComRxDataTimeoutAction
  长名称: ''
  描述: |
    If this parameter is configured to 'REPLACE', the initial values of all group signals are set if
    a timeout occurred.
    If this parameter is configured to 'NONE' or undefined, the last received values are maintained.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComTimeout
  长名称: ''
  描述: |
    Timeout time that is used for deadline monitoring.
    If the value is configured to '0' or undefined, the signal group is not monitored.
    
    For signal groups without a configured update-bit, an I-PDU based deadline monitoring is used.
    The timeout time is evaluated as smallest timeout time of all signals and signal groups without
    configured update-bit of the I-PDU.
  默认值: 0
  最小值: 0
  最大值: 3600
- 
  序号: 10
  名称: ComTimeoutNotification
  长名称: ''
  描述: |
    Defines the name and existence of the callback function that is called, if a timeout for the
    signal group is detected.
    
    Notification functions that shall not be handled by the RTE must use a function name without the
    pre-fix 'Rte_'. The prototype will then be generated to the file 'Appl_Cbk.h' and has to be
    implemented by called module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComTransferProperty
  长名称: ''
  描述: |
    The transfer behavior for the transmission mode DIRECT or MIXED when writing to the signal group
    can either be
    - TRIGGERED: the transmission of the message is triggered if at least one group signal of signal
    group is written regardless of the group signal value
    - TRIGGERED_WITHOUT_REPETITION: the transmission of the message is triggered just once without a
    repetition
    - TRIGGERED_ON_CHANGE: the transmission of the message is triggered if at least one group signal
    of signal group is written and the group signal value has changed
    - TRIGGERED_ON_CHANGE_WITHOUT_REPETITION: the transmission of the message is triggered just once
    without a repetition
    - PENDING: writing to the signal group does not cause direct transmission.
    
    Note: If at least one group signal of the signal group has a defined transfer property not equal
    to PENDING, the transfer property of the signal group will be ignored and the trigger will be
    evaluated per group signal.
  默认值: PENDING
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComUpdateBitPosition
  长名称: ''
  描述: Bit position of the update-bit inside the I-PDU.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 13
  名称: ComSignalGroupAccess
  长名称: ''
  描述: |
    The parameter ComSignalGroupAccess gives the Com generator the information whether a SignalGroup
    access is needed or not.
    All Signals with ComSignalGroupAccess != ACCESS_NOT_NEEDED can be accessed.
    All Signals with ComSignalGroupAccess == ACCESS_NOT_NEEDED cannot be accessed.
    
    ACCESS_NOT_NEEDED                       The SignalGroup will never be accessed.
    ACCESS_UNCLEAR                  It is unclear if the SignalGroup will be accessed.
    ACCESS_NEEDED_BY_SWC_OR_COM     It is clear that the SignalGroup access is needed, e.g. by COM.
    This state is set by a validator
    ACCESS_NEEDED_BY_OTHER                  The SignalGroup access is declared as to be needed. This
    state is set by the user.
  默认值: ACCESS_UNCLEAR
  最小值: ''
  最大值: ''
```

### 20. ComGroupSignal

**描述**: Specifies a group signal that is included within the signal group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComBitPosition
  长名称: ''
  描述: |
    Starting position within the I-PDU (not in the shadow buffer).
    The interpretation of the bit position depends on the signal endianness:
    BIG_ENDIAN: bit position refers to the MSB.
    LITTLE_ENDIAN: bit position refers to the LSB.
    OPAQUE: bit position refers to bit0 of the first byte like in little endian byte order.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: ComBitSize
  长名称: ''
  描述: Size in bits, for non-array signal types.
  默认值: 8
  最小值: 0
  最大值: 64
- 
  序号: 3
  名称: ComHandleId
  长名称: ''
  描述: The numerical value used as the ID.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: ComSignalDataInvalidValue
  长名称: ''
  描述: |
    Defines the invalid value of the group signal. The invalid value is a dedicated value that is
    transmitted in case the application cannot provide a valid value. The reception of an invalid
    signal value can trigger special invalid handling on receiver side.
    
    The interpretation of the configured value depends on ComSignalType setting:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. Possible values are "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComSignalEndianness
  长名称: ''
  描述: |
    Defines the endianness of the group signal's network representation.
    OPAQUE indicates that no byte order conversion is performed (e.g. for byte arrays).
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComSignalInitValue
  长名称: ''
  描述: |
    Initial value for this signal.
    The value is set during initialization of the module and if the corresponding I-PDU group is
    getting started with parameter 'initialize' set to 'true'.
    
    Note: The interpretation of the configured string depends on ComSignalType:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. It can be one of "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComSignalLength
  长名称: ''
  描述: For ComSignalType UINT8_N this parameter specifies the length n in bytes. For ComSignalType
      UINT8_DYN it specifies the maximum length in bytes. For all other types this parameter
      shall be ignored.
  默认值: 0
  最小值: 0
  最大值: 4095
- 
  序号: 8
  名称: ComSignalType
  长名称: ''
  描述: Specifies the data type that is used by the application to receive or transmit the signal
      through the COM APIs.
  默认值: UINT8
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComTransferProperty
  长名称: ''
  描述: |
    The transfer behavior for the transmission mode DIRECT or MIXED when writing to the group signal
    can either be
    - TRIGGERED: the transmission of the message is triggered if the group signal is written
    regardless of the group signal value
    - TRIGGERED_WITHOUT_REPETITION: the transmission of the message is triggered just once without a
    repetition
    - TRIGGERED_ON_CHANGE: the transmission of the message is triggered if the group signal is
    written and the group signal value has changed
    - TRIGGERED_ON_CHANGE_WITHOUT_REPETITION: the transmission of the message is triggered just once
    without a repetition
    - PENDING: writing to the group signal does not cause direct transmission.
    
    Note: If all the transfer properties of the group signals of a signal group equals PENDING, the
    transfer property of the signal group will be evaluated for the group signals.
  默认值: PENDING
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: ComRxDataTimeoutSubstitutionValue
  长名称: ''
  描述: |
    If this parameter and the ComRxDataTimeoutAction is configured to 'REPLACE',
    the signal value will be set to the value of this parameter, if a timeout occurred.
    The interpretation of the configured value depends on ComSignalType setting:
    - UINT8, UINT16, UINT32, UINT64, SINT8, SINT16, SINT32, SINT64, FLOAT32, FLOAT64
    the string is interpreted as integer type ( ..., -2, -1, 0, 1, 2,...).
    - BOOLEAN
    the string is interpreted as boolean type. Possible values are "0", "1", "true", "false".
    - UINT8_N
    the string is interpreted as a decimal representation of the characters separated by blanks,
    e.g. "97 98 100" means a string "abd", where the char "a" is in byte 0 (lowest address), "b" is
    in byte 1, and "d" is in byte 2 (highest address).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComSignalAccess
  长名称: ''
  描述: |
    The parameter ComSignalAccess gives the Com generator the information whether a GroupSignal
    access is needed or not.
    All GroupSignals with ComSignalAccess != ACCESS_NOT_NEEDED can be accessed.
    All GroupSignals with ComSignalAccess == ACCESS_NOT_NEEDED cannot be accessed.
    
    ACCESS_NOT_NEEDED                       The GroupSignal will never be accessed.
    ACCESS_UNCLEAR                  It is unclear if the GroupSignal will be accessed.
    ACCESS_NEEDED_BY_SWC_OR_COM     It is clear that the GroupSignal access is needed, e.g. by COM.
    This state is set by a validator
    ACCESS_NEEDED_BY_OTHER                  The GroupSignal access is declared as to be needed. This
    state is set by the user.
  默认值: ACCESS_UNCLEAR
  最小值: ''
  最大值: ''
```

### 21. ComFilter

**描述**: Defines the filter that is applied on transmit signals. The filter result of each signal is used to
determine the TxMode that shall be used for transmitting the I-PDU.
For receive signal the filter is used to determine whether the reception event is forwarded to the
application or not.

Signal only have a filter if the ComFilter container exists.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComFilterAlgorithm
  长名称: ''
  描述: |
    The supported filter algorithms for group signals are:
    - Always: This filter always evaluates to TRUE
    - Never: This filter always evaluates to FALSE
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: NEVER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComFilterMask
  长名称: ''
  描述: |
    Only valid on sender side: The supported filter algorithms for Tx signals are:
    - None: The signal has no filter (Multiplicity of ComFilter)
    - Always: This filter always evaluates to TRUE
    - Never: This filter always evaluates to FALSE
    - MaskedNewDiffersMaskedOld: ((new & mask) != (old & mask))
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 18446744073709551615
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: ComFilterMax
  长名称: ''
  描述: |
    The specified max value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 4
  名称: ComFilterMin
  长名称: ''
  描述: |
    The specified min value is used for the filters:
    - NewIsOutside: ((new < min) || (max < new))
    - NewIsWithin: ((min <= new) && (new <= max))
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 5
  名称: ComFilterX
  长名称: ''
  描述: |
    The specified value X is used for the filters:
    - MaskedNewEqualsX:  ((new & mask) == x)
    - MaskedNewDiffersX:  ((new & mask) != x)
  默认值: 0
  最小值: -2147483648
  最大值: 4294967295
- 
  序号: 6
  名称: ComFilterOffset
  长名称: ''
  描述: |
    The name of this attribute corresponds to the parameter name in the [17] specification of
    Reception Filtering.
    
    Note: This parameter is not used by the generator.
  默认值: 0
  最小值: 0
  最大值: 4294967294
- 
  序号: 7
  名称: ComFilterPeriod
  长名称: ''
  描述: |
    This parameter defines the period of the ComFilterAlgorithm ONE_EVERY_N.
    
    Note: This parameter is not used by the generator.
  默认值: 2
  最小值: 2
  最大值: 4294967295
```

### 22. ComMainFunctionRx

**描述**: Each element of this container defines one instance of Com_MainFunctionRx.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMainRxTimeBase
  长名称: ''
  描述: The period between successive calls to according instance of Com_MainFunctionRx in seconds.
      This parameter is used by the COM generator to transform the values of the reception
      related timing configuration parameters of the COM module to internal counter values.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComMainFunctionRxHandleId
  长名称: ''
  描述: The numerical value used as the ID of this MainFunctionRx.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 23. ComMainFunctionTx

**描述**: Each element of this container defines one instance of Com_MainFunctionTx.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMainTxTimeBase
  长名称: ''
  描述: The period between successive calls to according instance of Com_MainFunctionTx in seconds.
      This parameter is used by the COM generator to transform the values of the transmission
      related timing configuration parameters of the COM module to internal counter values.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComMainFunctionTxHandleId
  长名称: ''
  描述: The numerical value used as the ID of this MainFunctionTx.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 24. ComMainFunctionRouteSignals

**描述**: Each element of this container defines one instance of Com_MainFunctionRouteSignals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComMainRouteSignalsTimeBase
  长名称: ''
  描述: The period between successive calls to according instance of Com_MainFunctionRouteSignals in
      seconds. This parameter is used by the COM generator to transform the values of the
      reception related timing configuration parameters of the COM module to internal counter
      values.
  默认值: 0.01
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: ComMainFunctionRouteSignalsHandleId
  长名称: ''
  描述: The numerical value used as the ID of this ComMainFunctionRouteSignals.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 25. ComSignalGatewayQueue

**描述**: Cross-partition queue is used to perform the routing between different partitions.

Each container consists of two unidirectional cross-partition queues from partition A to partition B
and vice versa.
It is possible to specify the queue size for each direction independently.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComCrossPartitionQueueSizeAtoB
  长名称: ''
  描述: Size of the cross-partition queue for communication from partition A to partition B.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: ComCrossPartitionQueueSizeBtoA
  长名称: ''
  描述: Size of the cross-partition queue for communication from partition B to partition A.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 26. ComDescriptionRoutingQueue

**描述**: Cross-partition queue is used to perform the routing between different partitions.

Each container consists of two unidirectional cross-partition queues from partition A to partition B
and vice versa.
It is possible to specify the queue size for each direction independently.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComCrossPartitionQueueSizeAtoB
  长名称: ''
  描述: Size of the cross-partition queue for communication from partition A to partition B.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: ComCrossPartitionQueueSizeBtoA
  长名称: ''
  描述: Size of the cross-partition queue for communication from partition B to partition A.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 27. ComGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComConfigurationUseDet
  长名称: ''
  描述: |
    If 'Development Error Detection' is enabled, all development errors are reported to the
    Development Error Tracer (DET). The errors are described in the technical reference.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
    are checked before function is executed.
    This attribute has to be enabled for safety projects where this component is mapped to an ASIL
    partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComEnableMDTForCyclicTransmission
  长名称: ''
  描述: Enables globally for the whole COM module the minimum delay time monitoring for cyclic and
      repeated transmissions (ComTxModeMode=PERIODIC or ComTxModeMode=MIXED for the cyclic
      transmissions, ComTxModeNumberOfRepetitions > 0 for repeated transmissions).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComEnableSignalGroupArrayApi
  长名称: ''
  描述: Activate/Deactivate the signal group array access APIs (Com_SendSignalGroupArray,
      Com_ReceiveSignalGroupArray).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComRetryFailedTransmitRequests
  长名称: ''
  描述: |
    If the feature is activated, the COM repeats transmission requests of a Tx I-PDU to the
    underlying layer if E_NOT_OK is returned.
    If the feature is deactivated, the COM will ignore all errors from the underlying communication
    layer as recommended by AUTOSAR.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComSupportedIPduGroups
  长名称: ''
  描述: Note: This parameter is not used by the generator.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: ComVersionInfoApi
  长名称: ''
  描述: Note: This parameter is not used by the generator.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComUserConfigFile
  长名称: ''
  描述: |
    Reference to an external user configuration file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: ComMetaDataSupport
  长名称: ''
  描述: Note: This parameter is not used by the generator.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: ComUserCbkHeaderFile
  长名称: ''
  描述: Defines the header files for callback functions which shall be included by the COM module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: ComDescriptionGateway
  长名称: ''
  描述: Activate/Deactivate the ComGwSourceDescription and ComGwDestinationDescription based Gateway.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComStrictRepetitionPeriod
  长名称: ''
  描述: |
    Defines how the ComTxModeRepetitionPeriod is affected by the ComMinimumDelayTime.
    If the feature is activated, the time between two transmits equals ComTxModeRepetitionPeriod
    (Autosar 4.0.3).
    If the feature is deactivated, the time between two transmits can be shorter than
    ComTxModeRepetitionPeriod if the first transmit is delayed by the ComMinimumDelayTime (Autosar
    4.1.3).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: ComMixedModePeriodicSuppression
  长名称: ''
  描述: Mixed transmission mode PDUs with repetitions: the periodic part is suppressed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: ComSignalGateway
  长名称: ''
  描述: |
    Define if SignalGateway shall be used and what kind of signal routing shall be used.
    
    NONE: No Signal Gateway shall be used.
    MINIMALSIGNALPROCESSING: Endianness conversion, sign extension, check of update bits, I-PDU
    callout, reset reception deadline monitoring for I-PDU based monitoring is performed, before any
    signal is routed to its destination (ASR Version 4.3).
    COMPLETESIGNALPROCESSING: Signal invalidation, reception filtering and replace action of
    signal-based deadline monitoring are performed in addition to the MINIMALSIGNALPROCESSING steps,
    before any signal is routed to its destination (ASR Version 4.2).
    The resulting value after the complete signal processing is routed to the destination.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: ComMultiPartition
  长名称: ''
  描述: Enabled, if multi-partition capabilities are used.
  默认值: false
  最小值: ''
  最大值: ''
```

### 28. ComGeneration

**描述**: Contains the generation configuration parameters of the module Com.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden. This debugging feature must not be used in production code!
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access. This debugging feature must
    not be used in production code!
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: ComOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    This debugging feature must not be used in production code!
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: ComOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    This debugging feature must not be used in production code!
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: ComReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: ComBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES.
    The difference between BITFIELD and BITMASKING depends on your compiler options and memory
    mapping.
    
    BOOLEAN: The datatype of boolean data is native boolean.
    Code: the code size is small.
    RAM: no change expected.
    ROM: the ROM size is large.
    Runtime: the runtime is fast.
    
    BITFIELD: The bitfield type is used and the compiler extracts the boolean data from structures.
    Code: the code size is larger than using BOOLEAN.
    RAM: no change expected.
    ROM: the ROM size is smaller than using BOOLEAN.
    Runtime: the runtime is larger than using BOOLEAN.
    
    BITMASKING: Generated Masks are used to extract the boolean data from structures.
    Code: the code size is larger than using BOOLEAN.
    RAM: no change expected.
    ROM: the ROM size is smaller than using BOOLEAN.
    Runtime: the runtime is larger than using BOOLEAN.
  默认值: BITFIELD
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: ComDeduplicateIndirectedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress 0:N relational ROM data in all
    CONFIG-CLASSES without increasing the runtime.
    This option can be used in lib builds and in postbuild configurations.
    
    TRUE: 0:N relational ROM data is compressed without decreasing the runtime.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: no change expected.
    
    FALSE: 0:N relational ROM data is not compressed.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: ComDataDeduplicationStrategy
  长名称: ''
  描述: |
    This parameter is used to deduplicate CONFIG-CLASS PRE-COMPILE  ROM data.
    
    NONE: The generated data is not deduplicated.
    
    WITHOUT_CAST: The data is deduplicated without using casts.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size can be minimized.
    Runtime: no change expected.
    
    WITH_CAST: The data is deduplicated using casts.
    Code: no change expected.
    RAM: no change expected.
    ROM: the ROM size can be minimized more than in DEDUPLICATE_CONST_DATA_WITHOUT_CAST.
    Runtime: no change expected.
  默认值: WITH_CAST
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: ComReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the negation operator in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the negation operator in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 9
  名称: ComReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 10
  名称: ComReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: ComReduceBoolDataByNumericalOperandStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM data deduplication mechaisms.
    A comparison with 0 is very efficient, but a numerical comparison with a value not 0 can be used
    to increase the ROM data compression rate.
    
    NONE: ROM data deduplications are switched off.
    Code: the code size is small.
    RAM: no change expected.
    ROM: the ROM size is large.
    Runtime: the runtime is fast.
    
    WITH_ZERO: ROM data deduplications can be applied with the value 0.
    Code: the code size is larger than using NONE
    RAM: no change expected.
    ROM: the ROM size is smaller than using NONE.
    Runtime: the runtime is larger than using NONE.
    
    WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical value.
    Code: the code size is larger than using NONE
    RAM: no change expected.
    ROM: the ROM size is smaller than using DEDUPLICATE_DATA_WITH_ZERO.
    Runtime: the runtime is larger than using NONE.
  默认值: WITH_ANY_VALUE
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: ComReduceNumericalDataByOffsetThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a constant offset.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the constant offset operation in the data
    access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the constant offset operation in the data
    access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 13
  名称: ComReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a sutraction with other ROM data.
    0: The optimization is not performed.
    >0: This is the threshold to activate the data optimization.
    
    Code: the code size is increased due to the usage of the operation in the data access.
    RAM: no change expected.
    ROM: the ROM size is minimized.
    Runtime: the runtime is increased due to the usage of the operation in the data access.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 14
  名称: ComReduceDataByStreaming
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE
    ROM data into a data type dependent stream.
    
    TRUE: generated const data is packed into a data type dependent stream.
    Code: no change expected.
    RAM: no change expected.
    ROM: configuration dependent smaller than with FALSE.
    Runtime: no change expected.
    
    FALSE: generated const data is not packed into a data type dependent stream.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: ComShortSymbols
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate shortened symbol names.
    
    FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant
    names.
    TRUE: symbol names are generated based on the MIP and a CRC32.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: ComInterfacesForDeactivatedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate bsw data interfaces for
    deactivated data elements. This is an advantage for the BSW developer to reduce the time to
    market with a development environment using auto completition and to investigate potential
    interfaces.
    
    FALSE: data interfaces are not generated if the data elementis deactivated.
    TRUE: data interfaces are generated as e.g. emty macros.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: ComReferringKeysInComments
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to generate referring keys in comments. This
    is an advantage for the developer to investigate indirections, but this feature reduces the
    overall readability of the generated data.
    
    FALSE: referring keys are not generated in comments.
    TRUE: referring keys are generated in comments.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: ComNumberOfElementsCommentThreshold
  长名称: ''
  描述: |
    This parameter defines the maximum number of elements up to which comments for iterable var data
    are printed.
    These comments contain the referable keys corresponding to the index.
    
    0:  No Comments are printed.
    >0: Comments are printed for var data, if the contained number of elements is less than the
    specified threshold.
    
  默认值: 1000
  最小值: 0
  最大值: 9223372036854775807
```

### 29. ComOptimization

**描述**: Contains parameters that can change the module runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ComTxProcessingISRLockThreshold
  长名称: ''
  描述: This parameter defines the maximum number of Tx PDUs which are processed for transmission
      under Tx ISR Locks.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: ComRxProcessingISRLockThreshold
  长名称: ''
  描述: This parameter defines the maximum number of Rx PDUs which are deferred processed under Rx ISR
      Locks.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 3
  名称: ComGatewayProcessingISRLockThreshold
  长名称: ''
  描述: This parameter defines the maximum number of Tx PDUs which are deferred processed under
      Gateway ISR Locks.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 4
  名称: ComGatewayDescriptionProcessingISRLockThreshold
  长名称: ''
  描述: This parameter defines the maximum number of deferred gateway descriptions, which are
      processed in under Gateway Description ISR Locks.
  默认值: 1
  最小值: 0
  最大值: 65534
- 
  序号: 5
  名称: ComIPduGroupISRLockThreshold
  长名称: ''
  描述: This parameter defines the maximum number of IPdus, which are started or stopped under
      IPduGroup ISR Locks.
  默认值: 1
  最小值: 0
  最大值: 65534
```

