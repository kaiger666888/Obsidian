# DoIPInt

## 模块描述

The Diagnostic over IP for vehicle internal communication (DoIPInt) module implements a transport
protocol for diagnostic data over the Internet Protocol. It is derived from the DoIP module
according to ISO Standard 13400 and adapted to fit the vehicle internal communication needs.
#Ethernet #Diag
#Vector

## 容器列表

### 1. DoIPIntConfigSet

**描述**: This container contains the configuration parameters and sub containers of the DoIPInt module.

该容器没有参数。

### 2. DoIPIntChannel

**描述**: This container includes the configuration to describe the link to the upper layer PDUR module,

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntChannelId
  长名称: ''
  描述: This parameter defines the Channel ID required for API calls using channels (e.g.
      DoIPInt_OverwriteLogicalAddresses()).
  默认值: 0
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: DoIPIntChannelReadyNotification
  长名称: ''
  描述: |
    This parameter defines whether this channel is related to the channel ready notification.
    true:   BswM is notified when a TCP connection establishment succeeded.
    false:  BswM is not notified.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. DoIPIntPduRRxPdu

**描述**: This container contains the Rx Pdu for the channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntPduRRxPduId
  长名称: PduR Rx Pdu Id
  描述: This parameter defines the Pdu ID required for  the TP API calls. (e.g.
      DoIPInt_TpCancelReceive()) to handle reception to PDUR.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 4. DoIPIntPduRTxPdu

**描述**: This container contains the Tx Pdu for the channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntPduRTxPduId
  长名称: PduR Tx Pdu Id
  描述: This parameter defines the Pdu ID required for the TP and IF API calls. (e.g.
      DoIPInt_TpTransmit()) to send data from PDUR.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DoIPIntPduType
  长名称: ''
  描述: |
    This parameter defines the API Type to use for communication with PduR.
    DOIPINT_IFPDU for UUDT messages,
    DOIPINT_TPPDU for all other diagnostic messages.
  默认值: DOIPINT_TPPDU
  最小值: ''
  最大值: ''
```

### 5. DoIPIntConnections

**描述**: This container contains the connections to the lower layer SOAD module.

该容器没有参数。

### 6. DoIPIntClientConnection

**描述**: This container includes the connection configuration to the lower layer SOAD module for TCP client
connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntClientConnectionId
  长名称: ''
  描述: This parameter gives a unique identifier for client and server connections required for API
      calls using connections (e.g. DoIPInt_CloseConnection(),
      DoIPInt_TransmitOemSpecificPayloadType()).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. DoIPIntClientSoAdRxPdu

**描述**: This container contains the Rx Pdu for the TCP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntClientSoAdRxPduId
  长名称: Client SoAd Rx Pdu Id
  描述: This parameter defines the Pdu ID required for  the TP API calls. (e.g.
      DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 8. DoIPIntClientSoAdTxPdu

**描述**: This container contains the Tx Pdu for the TCP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntClientSoAdTxPduId
  长名称: Client SoAd Tx Pdu Id
  描述: This parameter defines the Pdu ID required for  the TP API calls. (e.g.
      DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 9. DoIPIntServerConnection

**描述**: This container includes the connection configuration to the lower layer SOAD module for TCP server
connections.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntServerConnectionId
  长名称: ''
  描述: This parameter gives a unique identifier for client and server connections required for API
      calls using connections (e.g. DoIPInt_CloseConnection(),
      DoIPInt_TransmitOemSpecificPayloadType()).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 10. DoIPIntServerSoAdRxPdu

**描述**: This container contains the Rx Pdu for the TCP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntServerSoAdRxPduId
  长名称: Server SoAd Rx Pdu Id
  描述: This parameter defines the Pdu ID required for  the TP API calls. (e.g.
      DoIPInt_SoAdTpRxIndication()) to receive TCP data from SOAD.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 11. DoIPIntServerSoAdTxPdu

**描述**: This container contains the Tx Pdu for the TCP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntServerSoAdTxPduId
  长名称: Server SoAd Tx Pdu Id
  描述: This parameter defines the Pdu ID required for  the TP API calls. (e.g.
      DoIPInt_SoAdTpTxConfirmation()) to confirm TCP data from SOAD.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 12. DoIPIntRemoteAddress

**描述**: This container defines the logical remote address which is used in the diagnostic messages (e.g. as
target address in case of transmission).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntRemoteAddressValue
  长名称: ''
  描述: This parameter defines the logical remote address which is sent within diagnostic messages.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. DoIPIntLocalAddress

**描述**: This container defines the logical local address which is used in the diagnostic messages (e.g. as
source address in case of transmission).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntLocalAddressValue
  长名称: ''
  描述: This parameter defines the logical local address which is sent within diagnostic messages.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. DoIPIntOemPayload

**描述**: This container defines parameter (Tx/Rx buffer and callback configuration) for OEM payload type
messages.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntOemPayloadRxCallback
  长名称: ''
  描述: |
    This parameter defines a callback function to forward received manufacturer-specific payload
    types to a user via <User>_DoIPIntReceiveOemSpecificPayloadType.
    
    Note: In case no DoIPIntOemPayloadRxBuffer is configured which can be used for a connection no
    reception of OEM specific messages is supported on this connection and the reception of the
    message is skipped.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 15. DoIPIntOemPayloadTxBuffer

**描述**: This container provides parameter to configure a Tx buffer which is used for messages with OEM
payload type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntOemPayloadTxBufferSize
  长名称: ''
  描述: This parameter defines the size of the Tx buffer for OEM payload type.
  默认值: 1500
  最小值: 1
  最大值: 65535
```

### 16. DoIPIntOemPayloadRxBuffer

**描述**: This container provides parameter to configure an Rx buffer which is used for messages with OEM
payload type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntOemPayloadRxBufferSize
  长名称: ''
  描述: This parameter defines the size of the Rx buffer for OEM payload type.
  默认值: 1500
  最小值: 1
  最大值: 65535
```

### 17. DoIPIntGeneral

**描述**: This container contains general configuration parameters of the DoIPInt module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true: Development error detection is enabled.
    false: Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPIntSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DoIPIntMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the main function call period.
  默认值: 0.005
  最小值: 0
  最大值: 0.1
- 
  序号: 4
  名称: DoIPIntVersionInfoApi
  长名称: Version Info API
  描述: This parameter activates/deactivates the DoIP_GetVersionInfo() API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DoIPIntUserConfigFile
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
  序号: 6
  名称: DoIPIntTxProcessLimit
  长名称: ''
  描述: |
    This parameter specifies how many transmission requests are processed in one main function
    cycle.
    A value greater than 1 is only applicable if multiple transmission requests can be processed by
    SoAd (SoAdTxTpOptimized enabled).
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: DoIPIntRxRetryTimeout
  长名称: ''
  描述: |
    This parameter specifies the retry timeout which is used in two different reception contexts.
    1. In case reception to user fails (PduR_DoIPIntTpStartOfReception() API).
    The module retries the reception until the timeout elapses. The message is dropped as soon as
    the timeout has elapsed.
    2. In case all applicable OEM specific reception buffers are currently in use.
    The module retries getting a buffer until the timeout elapses. The message is dropped as soon as
    the timeout has elapsed.
  默认值: 0.2
  最小值: 0.05
  最大值: 5
- 
  序号: 8
  名称: DoIPIntTxQueueSize
  长名称: ''
  描述: |
    This parameter specifies the maximum size of the transmission queue per connection.
    The transmission queue stores the number of parallel transmission requests on a connection.
    This parameter does not apply to a connection with a smaller number of DoIPIntChannels than the
    value specified by this parameter. In this case the number of DoIPIntChannels equals the size of
    the transmission queue.
  默认值: 16
  最小值: 1
  最大值: 65535
- 
  序号: 9
  名称: DoIPIntHeaderStructure
  长名称: ''
  描述: |
    This parameter specifies the header structure which is expected on reception and used on
    transmission.
    
    ISO: Version | Inv. Version | Payload Type | Payload Length | Src. Address | Tgt. Address | User
    Data
    LIGHT: Src. Address | Tgt. Address | Payload Length | User Data
  默认值: ISO
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DoIPIntIfPayloadType
  长名称: ''
  描述: |
    This parameter specifies which payload type shall be used for IF-PDUs.
    This parameter is only applicable if an IF-PDU is configured and if ISO is used as
    DoIPIntHeaderStructure.
    
  默认值: 32769
  最小值: 0
  最大值: 65535
- 
  序号: 11
  名称: DoIPIntApplicationHeaderFileInclusion
  长名称: ''
  描述: |
    This parameter defines a list of header files to be included containing application specific
    functionality (e.g. for DoIPIntOemPayloadRxCallback configuration).
    These header files are included in the SoAd_Lcfg.c file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DoIPIntProtocolVersion
  长名称: ''
  描述: |
    This value specifies the DoIP protocol version used in the generic DoIP header. The valid range
    of this parameter is defined by the always latest release of ISO 13400-2 and can be extended
    with every new release of the ISO document. As example a value of 0x03 defines the ISO
    13400-2:2019 release.
    
    Note: The version 0xFF should not be used as it is the default protocol version of the ISO.
  默认值: 3
  最小值: 2
  最大值: 255
```

### 18. DoIPIntGeneration

**描述**: This container contains parameters to change general generation behavior.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntOutOfBoundsWriteProtectionStrategy
  长名称: ''
  描述: |
    This parameter is used to configure a strategy to protect the code to write out of bounds.
    
    NONE: no protection strategy is generated in the data access.
    INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate
    mask. The advantage is the speed of the data access, but own data elements at other indexes of
    the same variable can be overridden.
    INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that
    values are never written to incorrect indexes of the data access.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPIntOutOfBoundsWriteSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds write problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DoIPIntOutOfBoundsReadSanitizer
  长名称: ''
  描述: |
    This parameter activates/deactivates the generation of runtime checks which call a DET error
    notification function to find easily out of bounds read problems.
    
    FALSE:  no checks are generated in the data access.
    TRUE: the data access is enriched with DET checks to validate indexes.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DoIPIntReduceConstantData2Define
  长名称: Reduce Constant Data To a Define
  描述: |
    This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM
    arrays as constant define.
    
    FALSE: ROM arrays are generated as data even if all values are identical.
    TRUE: ROM arrays are generated as constant define if all values are identical.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DoIPIntBoolDataInArrayOfStructStrategy
  长名称: ''
  描述: |
    This parameter is used to tailor the usage of boolean data in structures in all CONFIG-CLASSES
    ROM data. The difference between BITFIELD and BITMASKING depends on your compiler options and
    memory mapping.
    
    BOOLEAN: the datatype of boolean data is native boolean.
    BITFIELD: the bitfield type is used and the compiler extracts the boolean data from structures.
    BITMASKING: generated masks are used to extract the boolean data from structures.
  默认值: BITMASKING
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DoIPIntDeduplicateIndirectedData
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress 0:N relational ROM data in all
    CONFIG-CLASSES without increasing the runtime.
    
    FALSE: 0:N relational ROM data is not compressed.
    TRUE: 0:N relational ROM data is compressed without increasing the runtime.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DoIPIntDataDeduplicationStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the the deduplication of CONFIG-CLASS PRE-COMPILE  ROM data.
    
    NONE: The generated data is not deduplicated.
    DEDUPLICATE_CONST_DATA_WITHOUT_CAST: The data is deduplicated without using casts.
    DEDUPLICATE_CONST_DATA_WITH_CAST: The data is deduplicated using casts.
  默认值: DEDUPLICATE_CONST_DATA_WITH_CAST
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DoIPIntReduceBoolDataByNegationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using the negation operator.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 9
  名称: DoIPIntReduceBoolDataByNumericalComparisonThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using numerical comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 10
  名称: DoIPIntReduceBoolDataByNumericalRelationThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE
    ROM data by using relational comparison with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: DoIPIntReduceBoolDataByNumericalOperandStrategy
  长名称: ''
  描述: |
    This parameter is used to taylor the CONFIG-CLASS PRE-COMPILE ROM bool data with number
    deduplication mechanisms. A comparison with 0 is very efficient, but a numerical comparison with
    a value not 0 can be used to increase the ROM data compression rate.
    
    NONE: ROM data deduplications are switched off.
    DEDUPLICATE_DATA_WITH_ZERO: ROM data deduplications can be applied with the value 0.
    DEDUPLICATE_DATA_WITH_ANY_VALUE: ROM data deduplications can be applied with any numerical
    value.
  默认值: DEDUPLICATE_DATA_WITH_ANY_VALUE
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DoIPIntReduceNumericalDataByOffsetThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a constant offset.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 13
  名称: DoIPIntReduceNumericalDataByArraySubtractionThreshold
  长名称: ''
  描述: |
    This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS
    PRE-COMPILE ROM data by using a subtraction with other ROM data.
    
    0: The optimization is deactivated.
    >0: If the number of deduplicateable elements is greater than this threshold the data
    optimization can be performed.
  默认值: 2
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 14
  名称: DoIPIntShortSymbols
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
  序号: 15
  名称: DoIPIntInterfacesForDeactivatedData
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
  序号: 16
  名称: DoIPIntReferringKeysInComments
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
```

### 19. DoIPIntEventCallback

**描述**: This container provides parameter to configure an event callback and all its related parameter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DoIPIntEventCallback
  长名称: ''
  描述: This parameter defines a callback function to report events via <User>_DoIPIntEvent.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DoIPIntEventMaxUserDataLength
  长名称: ''
  描述: This parameter defines the maximum user data length that shall be forwarded inisde the
      configured event callback function.
  默认值: 0
  最小值: 0
  最大值: 65535
```

