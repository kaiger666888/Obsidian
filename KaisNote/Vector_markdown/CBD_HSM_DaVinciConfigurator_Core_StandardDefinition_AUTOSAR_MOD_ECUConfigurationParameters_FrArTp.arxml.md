# FrArTp

## 模块描述

Configuration of the FrArTp (FlexRay Transport Protocol) module.

## 容器列表

### 1. FrArTpGeneral

**描述**: This container contains the general configuration (parameters) of the FlexRay TP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpChanNum
  长名称: ''
  描述: Preprocessor switch for defining the number of concurrent channels the module supports. Up to
      32 channels shall be definable here.
  默认值: ''
  最小值: 1
  最大值: 32
- 
  序号: 2
  名称: FrArTpDevErrorDetect
  长名称: ''
  描述: Preprocessor switch for enabling development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrArTpHaveAckRt
  长名称: ''
  描述: Preprocessor switch for enabling the Acknowledgement and retry mechanisms.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FrArTpHaveGrpSeg
  长名称: ''
  描述: Preprocessor switch for enabling segmentation of 1:n messages.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FrArTpHaveLm
  长名称: ''
  描述: Preprocessor switch for enabling the mechanism for message longer than allowed by.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrArTpHaveTc
  长名称: ''
  描述: Preprocessor switch for enabling Transmit Cancellation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrArTpMainFuncCycle
  长名称: ''
  描述: This parameter contains the calling period of the TPs Main Function. The parameter is
      specified in seconds.
  默认值: ''
  最小值: 0
  最大值: 1.024
- 
  序号: 8
  名称: FrArTpVersionInfoApi
  长名称: ''
  描述: Preprocessor switch for enabling the Version info API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. FrArTpMultipleConfig

**描述**: This container holds one or several multiple configuration sets.

该容器没有参数。

### 3. FrArTpChannel

**描述**: This container contains the configuration (parameters) of one FlexRay TP channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpAckType
  长名称: ''
  描述: This parameter defines the type of acknowledgement which is used for the specific channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrArTpAdrType
  长名称: ''
  描述: This parameter states the addressing type this connection has. The meanings of the values are
      one byte and two byte.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrArTpChannelId
  长名称: ''
  描述: The Id of the channel.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: FrArTpConNum
  长名称: ''
  描述: This parameter states the number of connections used in this channel. At least 256 shall be
      configurable here.
  默认值: ''
  最小值: 0
  最大值: 65536
- 
  序号: 5
  名称: FrArTpGrpSeg
  长名称: ''
  描述: Here can be specified, whether segmentation within a 1:n connection is allowed or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FrArTpLm
  长名称: ''
  描述: This specifies the maximum message length for the particular channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrArTpMaxAr
  长名称: ''
  描述: This parameter defines the maximum number of trying to send a frame when a TIMEOUT AR occurs
      (depending on whether retry is configured).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: FrArTpMaxAs
  长名称: ''
  描述: This parameter defines the maximum number of trying t osend a frame when a TIMEOUT AS occurs
      (depending on whether retry is configured)
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: FrArTpMaxBs
  长名称: ''
  描述: This parameter defines number of consecutive CFs between two FCs (block size). Valid values
      are 1 .. 16 when retry is activated, and 0 .. 255 otherwise.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: FrArTpMaxBufReq
  长名称: ''
  描述: This parameter defines the maximum number of times the FrArTp should send a wait frame FC(WT).
      It is also used to limit the number of retries for PduR_FrArTpCopyTxData and
      PduR_FrArTpCopyRxData when no timer is active.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: FrArTpMaxFrIf
  长名称: ''
  描述: This parameter defines the maximum number of trying to send a frame when the FrIf returns an
      error.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: FrArTpMaxRn
  长名称: ''
  描述: This parameter defines the maximum number of retries (if retry is configured for the
      particular channel).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: FrArTpStMin
  长名称: ''
  描述: This parameter defines the minimum amount of time between two succeeding CFs in seconds. Valid
      values are 0, 100µs, 200µs .. 900µs, 1ms, 2ms .. 127ms. The value can be changed at
      runtime using the FrArTp_ChangeParameter interface.
  默认值: ''
  最小值: 0
  最大值: 1
- 
  序号: 14
  名称: FrArTpTc
  长名称: ''
  描述: With this switch Transmit Cancellation can be turned on or off for this channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FrArTpTimeBr
  长名称: ''
  描述: This parameter defines the time in seconds between receiving the last CF of a block or an FF-x
      (or SF-x) and sending out an FC or AF.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 16
  名称: FrArTpTimeBuffer
  长名称: ''
  描述: This parameter defines the time in seconds of waiting for the next try (if retry is activated)
      to get a Tx or Rx buffer.
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 17
  名称: FrArTpTimeCs
  长名称: ''
  描述: This parameter defines the time in seconds between the sending of two consecutive CFs or
      between reception of an FC or AF and sending of the next CF . It is obvious that
      FRARTP_TIME_CS + FRARTP_TIMEOUT_AS < FRARTP_TIMEOUT_CR must hold (because the
      transmission duration on the bus has also to be considered). This parameter is defined
      in ISO 15765-2. It is contained in the configuration as a performance requirement.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 18
  名称: FrArTpTimeFrIf
  长名称: ''
  描述: This parameter defines the time in seconds of waiting for the next try (if retry is activated)
      to send via FrIf_Transmit.
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 19
  名称: FrArTpTimeoutAr
  长名称: ''
  描述: This parameter states the timeout in seconds between the PDU transmit request of the Transport
      Layer to the FlexRay Interface and the corresponding confirmation of the FlexRay
      Interface on the receiver side (for FC or AF).
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 20
  名称: FrArTpTimeoutAs
  长名称: ''
  描述: This parameter states the timeout in seconds between the PDU transmit request for the first
      PDU of the group used in the current connection of the Transport Layer to the FlexRay
      Interface and the corresponding confirmation of the FlexRay Interface (when having sent
      the last PDU of the
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 21
  名称: FrArTpTimeoutBs
  长名称: ''
  描述: This parameter defines the timeout in seconds for waiting for an FC or AF on the sender side
      in a 1:1 connection.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 22
  名称: FrArTpTimeoutCr
  长名称: ''
  描述: This parameter defines the timeout value in seconds for waiting for a CF or FF-x (in case of
      retry) after receiving the last CF or after sending an FC or AF on the receiver side.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 23
  名称: FrArTpUsePduFc
  长名称: ''
  描述: This switch defines, whether within this channel the dedicated FC/ACK PDU (FrArTpPduFc) shall
      be used or not. If this is not used FC / ACK frames are sent using the normal IDs,
      otherwise only FrArTpPduFc shall be used for sending / receiving FC / ACK frames.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. FrArTpConnection

**描述**: This container contains the configuration (parameters) of one FlexRay TP connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpLa
  长名称: ''
  描述: This parameter defines the Local Address for the respective connection.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: FrArTpMultRec
  长名称: ''
  描述: This parameter defines, whether this connection is an 1:1 ('false') or an 1:n ('true')
      connection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrArTpRa
  长名称: ''
  描述: This parameter defines the Remote Address for the respective connection.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. FrArTpRxSdu

**描述**: Describes the Rx SDU

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpSduRxId
  长名称: ''
  描述: This is a unique identifier for a received message. This Id is used in the CancelReceive API
      call.
  默认值: ''
  最小值: 0
  最大值: 65536
```

### 6. FrArTpTxSdu

**描述**: Describes the Tx SDU

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpSduTxId
  长名称: ''
  描述: This is a unique identifier for a received or a to be transmitted message. With this (and by
      means of e.g. a lookup table) the PDU Router can route the message appropriately without
      dealing with the particularities of the Transport Layer. This parameter can also be seen
      as the identifier of a connection.
  默认值: ''
  最小值: 0
  最大值: 65536
```

### 7. FrArTpPdu

**描述**: Container to hold the PDU parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpPduDirection
  长名称: ''
  描述: This parameter defines the direction of the PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrArTpPduId
  长名称: ''
  描述: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the
      Transport Layer Frames of this channel should be transmitted.
  默认值: ''
  最小值: 0
  最大值: 65536
```

### 8. FrArTpPduFc

**描述**: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the Transport
Layer Flow Control and Acknowledgement Frames of this channel should be transmitted.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrArTpPduFcDirection
  长名称: ''
  描述: This parameter defines the direction of the PDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrArTpPduFcId
  长名称: ''
  描述: This is the identifier of the FlexRay Interface PDUs (Fr N-PDU, Fr L-SDU) in which the
      Transport Layer Flow Control and Acknowledgement Frames of this channel should be
      transmitted.
  默认值: ''
  最小值: 0
  最大值: 65536
```

