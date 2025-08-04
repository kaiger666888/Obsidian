# FrTp

## 模块描述

Configuration of the FlexRay Transport Protocol module according to ISO 10681-2.

## 容器列表

### 1. FrTpGeneral

**描述**: This container contains the general configuration parameters of the FlexRay Transport Protocol
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpAckRt
  长名称: ''
  描述: Preprocessor switch for enabling the Acknowledgement and retry mechanisms.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTpChanNum
  长名称: ''
  描述: Preprocessor switch for defining the number of concurrent channels the module supports. Up to
      32 channels shall be definable here.
  默认值: ''
  最小值: 1
  最大值: 32
- 
  序号: 3
  名称: FrTpChangeParamApi
  长名称: ''
  描述: Preprocessor switch for enabling the API to change FrTp communication
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrTpDevErrorDetect
  长名称: ''
  描述: Preprocessor switch for enabling development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrTpFullDuplexEnable
  长名称: ''
  描述: Preprocessor switch for enabling full duplex mechanisms for all channels.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrTpMainFuncCycle
  长名称: ''
  描述: This parameter contains the calling period of the TPs Main Function. The parameter is
      specified in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: FrTpTransmitCancellation
  长名称: ''
  描述: Preprocessor switch for enabling Transmit Cancellation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrTpUnknownMsgLength
  长名称: ''
  描述: Preprocessor switch to support data transfer with unknown message length.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FrTpVersionInfoApi
  长名称: ''
  描述: Preprocessor switch for enabling the Version info API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. FrTpMultipleConfig

**描述**: This container holds one or several multiple configuration sets.

该容器没有参数。

### 3. FrTpConnection

**描述**: This container contains the connection specific parameters to transfer N-PDUs via FlexRay TP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpBandwidthLimitation
  长名称: ''
  描述: This parameter indicates wheather the connection requires a  bandwidth limitation or not. If
      FrTpBandwidthLimitation=True the sender shall send a StartFrame always on the first PDU
      of a PDU-Pool.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTpLa
  长名称: ''
  描述: This parameter defines the Local Address for the respective connection. When the local
      instance is the sender, this is the Source Address within the TP frame. When the local
      instance is the receiver, this is the Target Address within the TP frame.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: FrTpMultipleReceiverCon
  长名称: ''
  描述: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true')
      connection. If data segmentation is required this parameter is used to check whether
      segmentation is possible or not. If the connection is 1:n segmentation is not possible
      and an error will occur.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrTpRa
  长名称: ''
  描述: This parameter defines the Remote Address for the respective connection. When the local
      instance is the sender, this is the Target Address within the TP frame. When the local
      instance is the receiver, this is the Source Address within the TP frame.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. FrTpRxSdu

**描述**: This parameter defines the Rx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data
transfer (inter-module communication) between FrTp and PDUR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpRxSduId
  长名称: ''
  描述: This unique identifier is used for change parameter request or receive cancellation from PduR
      to FrTp.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. FrTpTxSdu

**描述**: This parameter defines the Tx Service Data Unit Identifier (Sdu Id) which uniquely identifies a data
transfer (inter-module communication) between FrTp and PDUR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpTxSduId
  长名称: ''
  描述: This is a unique identifier for a to be transmitted message from the PduR to the FrTp.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. FrTpConnectionControl

**描述**: This container contains the configuration parameters to control a FlexRay TP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpAckType
  长名称: ''
  描述: This parameter defines the type of acknowledgement which is used for the specific channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTpMaxAr
  长名称: ''
  描述: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: FrTpMaxAs
  长名称: ''
  描述: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AS occurs.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: FrTpMaxBufferSize
  长名称: ''
  描述: Limits the maximal buffer size the FrTp can choose in order to limit the amount of Tx buffer
      that will be requested at the sender side in a segmented transfer.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: FrTpMaxFCWait
  长名称: ''
  描述: This parameter defines the maximum number of FlowControl N-PDUs with FlowState "WAIT"
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: FrTpMaxFrIf
  长名称: ''
  描述: This parameter defines the maximum number of trying to send a frame when the FrIf returns an
      error.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: FrTpMaxNbrOfNPduPerCycle
  长名称: ''
  描述: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control
      (BC)". It limits the number of N-Pdus the sender is allowed to transmit within a FlexRay
      cycle.
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 8
  名称: FrTpMaxRn
  长名称: ''
  描述: This parameter defines the maximum number of retries (if retry is configured).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: FrTpSCexp
  长名称: ''
  描述: This parameter is part of the ISO 10681-2 protocol's FlowControl parameter "Bandwidth Control
      (BC)". It represents the exponent to calculate the minimum number of "Separation Cycles"
      the sender has to wait for the next transmission of an FrTp N-Pdu.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 10
  名称: FrTpTimeBr
  长名称: ''
  描述: This parameter defines the time in seconds the FrTp requires to transmit a corresponding
      FlowControl Frame. According to ISO 10681-2 this parameter is a performance requirement.
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 11
  名称: FrTpTimeBuffer
  长名称: ''
  描述: This parameter defines the time in seconds of waiting for the next try to get a Tx or Rx
      buffer.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 12
  名称: FrTpTimeFrIf
  长名称: ''
  描述: This parameter defines the time in seconds of waiting for the next try (if retry is activated)
      to send via FrIf_Transmit.
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 13
  名称: FrTpTimeoutAr
  长名称: ''
  描述: This parameter states the timeout in seconds between the PDU transmit request of the Transport
      Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay
      Interface on the receiver side (for FC or AF).
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 14
  名称: FrTpTimeoutAs
  长名称: ''
  描述: This parameter specifies the timeout in seconds the FrIf shall confirm a transmitted Pdu to
      the FrTp.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 15
  名称: FrTpTimeoutBs
  长名称: ''
  描述: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side
      in a 1:1 connection.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 16
  名称: FrTpTimeoutCr
  长名称: ''
  描述: This parameter defines the timeout value in seconds a receiver is waiting for a CF or a LF.
  默认值: ''
  最小值: 0
  最大值: 65.535
```

### 7. FrTpRxPduPool

**描述**: This container contains all Pdus that are assigned to that Pdu Pool.

该容器没有参数。

### 8. FrTpRxPdu

**描述**: Container to hold the PDU parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpRxPduId
  长名称: ''
  描述: This is a unique identifier for a received message which is forwarded from the FrIf to the
      FrTp.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. FrTpTxPduPool

**描述**: This container contains all Pdus that are assigned to that Pdu Pool.

该容器没有参数。

### 10. FrTpTxPdu

**描述**: Container to hold the PDU parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTpTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the FrIf to confirm the transmission of the FrTpTxPdu to the FrIf
      module.
  默认值: ''
  最小值: 0
  最大值: 65535
```

