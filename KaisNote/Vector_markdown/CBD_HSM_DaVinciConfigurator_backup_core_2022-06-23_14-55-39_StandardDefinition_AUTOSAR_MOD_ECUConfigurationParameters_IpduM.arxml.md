# IpduM

## 模块描述

Configuration of the IpduM (Ipdu Multiplexer) module.

## 容器列表

### 1. IpduMConfig

**描述**: This container contains the sub containers of the IpduM module. The IpduMTxPathway subcontainer
includes information about sent I-PDUs. The IpduMRxPathway includes information about received
I-PDUs.

该容器没有参数。

### 2. IpduMRxPathway

**描述**: Contains the configuration parameters received I-PDUs by the IpduM module.

该容器没有参数。

### 3. IpduMRxIndication

**描述**: Contains the configuration for incoming RxIndication calls.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMByteOrder
  长名称: ''
  描述: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for
      the selectorField within the MultiplexedPdu.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMRxHandleId
  长名称: ''
  描述: This is the I-PDU ID of the incoming I-PDU. If an incoming RxIndication's I-PDU ID matches
      this value then it is unpacked according to the specification in this container.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. IpduMRxDynamicPart

**描述**: This container contains the configuration for the dynamic part of incoming RxIndication calls. When
an incoming received I-PDU's selector field matches the IpduM_Selector_Value, the new outgoing I-PDU
for the dynamic part is constructed as defined by the segments of this container and sent out with
the I-PDU ID referenced by IpduMOutgoingDynamicPduRef.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMRxSelectorValue
  长名称: ''
  描述: This is the selector value that this container refers to.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 5. IpduMSegment

**描述**: This contains the location and the length of a segment. A segment must fit inside the I-PDU. The
segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same
position in the destination I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 6. IpduMRxStaticPart

**描述**: This container contains the configuration for the static part of incoming RxIndication calls. On
reception, the new outgoing I-PDU for the static part is constructed as defined by the segments of
this container and sent out with the I-PDU ID referenced by IpduMOutgoingStaticPduRef.

该容器没有参数。

### 7. IpduMSegment

**描述**: This contains the location and the length of a segment. A segment must fit inside the I-PDU. The
segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same
position in the destination I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 8. IpduMSelectorFieldPosition

**描述**: This contains the location and the length of the selector field.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSelectorFieldLength
  长名称: ''
  描述: Length of the selector field in bits.
  默认值: ''
  最小值: 1
  最大值: 8
- 
  序号: 2
  名称: IpduMSelectorFieldPosition
  长名称: ''
  描述: Selector field bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 9. IpduMTxPathway

**描述**: Contains the configuration parameters transmitted I-PDUs by the IpduM module.

该容器没有参数。

### 10. IpduMTxRequest

**描述**: This is used to specify the configuration for Transmit requests.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMByteOrder
  长名称: ''
  描述: This parameter defines the ByteOrder for all IpduMSegments (static and dynamic part) and for
      the selectorField within the MultiplexedPdu.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMIPduUnusedAreasDefault
  长名称: ''
  描述: IpduM module fills not used areas of an I-PDU with this bit-pattern
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IpduMTxConfirmationPduId
  长名称: ''
  描述: The handle Id to be used by the PduR to confirm the transmission of this Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: IpduMTxConfirmationTimeout
  长名称: ''
  描述: This timeout (in seconds) defines the timeout period for monitoring the reception of the
      TxConfirmation.
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 5
  名称: IpduMTxTriggerMode
  长名称: ''
  描述: Selects whether to send the multiplexed I-PDU immediately or at some later date.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. IpduMSelectorFieldPosition

**描述**: This contains the location and the length of the selector field.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSelectorFieldLength
  长名称: ''
  描述: Length of the selector field in bits.
  默认值: ''
  最小值: 1
  最大值: 8
- 
  序号: 2
  名称: IpduMSelectorFieldPosition
  长名称: ''
  描述: Selector field bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 12. IpduMTxDynamicPart

**描述**: Configuration parameters for an instance of a TxRequest call into the IpduM. When a Tx Request with
the IpduMTxDynamicHandleId is received by the IpduM, all segments as defined by this container are
copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This
container is used by the dynamic part of a TxRequest configuration. Therefore, for each outgoing
I-PDU there will be one instance of this container for the dynamic part.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMJitUpdate
  长名称: ''
  描述: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of
      the PduR.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMTxDynamicConfirmation
  长名称: ''
  描述: A transmit request can be confirmed by the lower layer. If this parameter is set to true a
      confirmation of the I-PDU in COM representing the dynamic part is generated.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMTxDynamicHandleId
  长名称: ''
  描述: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the
      bits fields (see IpduMSegment) are copied and the IpduMTxTriggerMode is honored.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. IpduMSegment

**描述**: This contains the location and the length of a segment. A segment must fit inside the I-PDU. The
segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same
position in the destination I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 14. IpduMTxStaticPart

**描述**: Configuration parameters for an instance of a Tx_Request call into the IpduM. When a Tx Request with
the IpduMTxStaticHandleId is received by the IpduM, all segments as defined by this container are
copied from the incoming I-PDU into the outgoing I-PDU buffer and then the send mode honoured. This
container is used for the static part of a TxRequest configuration. Therefore, for each outgoing
I-PDU there will be one instance of this container for the static part if it exists.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMJitUpdate
  长名称: ''
  描述: If configured to true fetch the data of this part Just-In-Time via the triggerTransmit API of
      the PduR.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IpduMTxStaticConfirmation
  长名称: ''
  描述: A transmit request can be confirmed by the lower layer. If this parameter is set to true a
      confirmation of the I-PDU in COM representing the static part is generated.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMTxStaticHandleId
  长名称: ''
  描述: This is an incoming handle id. When the handle of an incoming Tx Request matches this, the
      segments are copied (IPduMSegment) and the IpduMTxTriggerMode is honored.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. IpduMSegment

**描述**: This contains the location and the length of a segment. A segment must fit inside the I-PDU. The
segment in the source I-PDU that is located at the IpduMSegmentPosition is copied to the same
position in the destination I-PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMSegmentLength
  长名称: ''
  描述: Length of the segment in bits.
  默认值: ''
  最小值: 1
  最大值: 2032
- 
  序号: 2
  名称: IpduMSegmentPosition
  长名称: ''
  描述: Segments bit position in the multiplexed Pdu.
  默认值: ''
  最小值: 0
  最大值: 2031
```

### 16. IpduMGeneral

**描述**: Contains the general configuration parameters of IpduM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMConfigurationTimeBase
  长名称: ''
  描述: The cycle time with which IpduM_MainFunction should  be invoked (in seconds).
  默认值: ''
  最小值: 0
  最大值: 3600
- 
  序号: 2
  名称: IpduMDevErrorDetect
  长名称: ''
  描述: Active/Deactivate the detection of development errors, for production code this parameter has
      to be False.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IpduMStaticPartExists
  长名称: ''
  描述: This is to allow optimizations in the case the IpduM will never be used with a static part.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IpduMVersionInfoApi
  长名称: ''
  描述: Active/Deactivate the version information API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. IpduMPublishedInformation

**描述**: Additional published parameters not covered by

#### 参数列表

```yaml
- 
  序号: 1
  名称: IpduMRxDirectComInvocation
  长名称: ''
  描述: If set to TRUE the COM invocation optimization as defined in
  默认值: ''
  最小值: ''
  最大值: ''
```

