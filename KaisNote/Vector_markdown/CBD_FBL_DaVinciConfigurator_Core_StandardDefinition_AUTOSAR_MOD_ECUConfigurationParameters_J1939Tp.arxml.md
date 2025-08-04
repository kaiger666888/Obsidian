# J1939Tp

## 模块描述

Configuration of the J1939Tp (J1939 Transport Protocol) module.

## 容器列表

### 1. J1939TpConfiguration

**描述**: This container contains the configuration parameters and sub containers of the J1939Tp module that
define the communication paths. This container is a MultipleConfigurationContainer, i.e. this
container and its sub-containers exist once per configuration set.

该容器没有参数。

### 2. J1939TpDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be passed to the API
Dem_ReportErrorStatus. The EventId is taken from the referenced DemEventParameter's DemEventId
value.

该容器没有参数。

### 3. J1939TpRxChannel

**描述**: This container describes a reception channel of the J1939Tp module. One channel is used for all
N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF,
CMDT: DA != 0xFF).

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxDa
  长名称: ''
  描述: Destination address (DA) of this channel. This parameter is only required for channels with
      fixed DA which use N-PDUs with MetaData containing the DA.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: J1939TpRxProtocolType
  长名称: ''
  描述: Protocol type used by this channel. This parameter is only required for channels with fixed
      destination address.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: J1939TpRxSa
  长名称: ''
  描述: Source address (SA) of this channel. This parameter is only required for channels with fixed
      SA which use N-PDUs with MetaData.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 4
  名称: J1939TpRxCancellationSupport
  长名称: ''
  描述: Enable receive cancellation using the API J1939Tp_CancelReceive() for this channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: J1939TpRxDynamicBlockCalculation
  长名称: ''
  描述: Enable dynamic calculation of "number of packets that can be sent" value in TP.CM_CTS, based
      on the size of buffers in upper layers reported via StartOfReception and CopyRxData.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: J1939TpRxDynamicBufferRatio
  长名称: ''
  描述: |
    Percentage of available buffer that shall be used for retry.
    This parameter is only applicable when "J1939TpRxRetrySupport" and
    "J1939TpRxDynamicBlockCalculation" are enabled.
  默认值: 80
  最小值: 0
  最大值: 100
- 
  序号: 7
  名称: J1939TpRxPacketsPerBlock
  长名称: ''
  描述: Number of TP.DT frames the receiving J1939Tp module allows the sender to send before waiting
      for another TP.CM_CTS. This parameter is transmitted in the TP.CM_CTS frame, and is thus
      only relevant for reception of messages via CMDT. When J1939TpDynamicBlockCalculation is
      enabled, this parameter specifies a maximum for the calculated value. For further
      details on this parameter value see SAE J1939/21.
  默认值: 16
  最小值: 1
  最大值: 255
- 
  序号: 8
  名称: J1939TpRxRetrySupport
  长名称: ''
  描述: Enable support for triggering repetition of failed transmission using TP.CM_CTS with a packet
      number that has already been sent. Retransmission is triggered when a sequence number is
      missing or a timeout occurs during reception.
  默认值: false
  最小值: ''
  最大值: ''
```

### 4. J1939TpRxCmNPdu

**描述**: This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by
BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxCmNPduId
  长名称: ''
  描述: The N-PDU identifier used for communication with CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. J1939TpRxDtNPdu

**描述**: This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by
BAM and CMDT to transfer the contents of an N-SDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxDtNPduId
  长名称: ''
  描述: The N-PDU identifier used for communication with CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 6. J1939TpRxPg

**描述**: Parameter group received by the J1939 transport layer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxPgDynLength
  长名称: ''
  描述: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939TpRxPgPGN
  长名称: ''
  描述: Defines the PGN which is represented by the N-SDU.
  默认值: ''
  最小值: 0
  最大值: 262143
```

### 7. J1939TpRxDirectNPdu

**描述**: This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of
less that 8 bytes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxDirectNPduId
  长名称: ''
  描述: The N-PDU identifier used for communication with CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 8. J1939TpRxNSdu

**描述**: This container describes the parameters that are relevant for the reception of a specific N-SDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxNSduId
  长名称: ''
  描述: This is a unique identifier for a received N-SDU. This Id is used in the CancelReceive and
      ChangeParameter API call.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. J1939TpTxFcNPdu

**描述**: This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport
protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate
and final acknowledgement of received data and to abort the connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxFcNPduTxConfId
  长名称: ''
  描述: The N-PDU identifier used for Tx confirmation from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 10. J1939TpTxChannel

**描述**: This container describes a transmission channel of the J1939Tp module. One channel is used for all
N-SDUs that share the same source address (SA) and the same destination address (BAM: DA = 0xFF,
CMDT: DA != 0xFF).

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxDa
  长名称: ''
  描述: Destination address (DA) of this channel. This parameter is only required for channels with
      fixed DA which use N-PDUs with MetaData containing the DA.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: J1939TpTxProtocolType
  长名称: ''
  描述: Protocol type used by this channel. This parameter is only required for channels with fixed
      destination address.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: J1939TpTxSa
  长名称: ''
  描述: Source address (SA) of this channel. This parameter is only required for channels with fixed
      SA which use N-PDUs with MetaData.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 4
  名称: J1939TpTxCancellationSupport
  长名称: ''
  描述: Enable transmit cancellation using the API J1939Tp_CancelTransmit() for this channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: J1939TpTxDynamicBlockCalculation
  长名称: ''
  描述: Enable dynamic calculation of "maximum number of packets that can be sent" value in TP.CM_RTS,
      based on the available amount of data in upper layers reported via CopyTxData.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: J1939TpTxMaxPacketsPerBlock
  长名称: ''
  描述: Maximum number of TP.DT frames the transmitting J1939Tp module is ready to send before waiting
      for another TP.CM_CTS. This parameter is transmitted in the TP.CM_RTS frame, and is thus
      only relevant for transmission of messages via CMDT. When J1939TpDynamicBlockCalculation
      is enabled, this parameter specifies a maximum for the calculated value. For further
      details on this parameter value see SAE J1939/21.
  默认值: 255
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: J1939TpTxRetrySupport
  长名称: ''
  描述: Enable support for repetition of failed transmission using TP.CM_CTS with a packet number that
      has already been sent. Retransmission is handled via the retry feature of
      PduR_J1939TpCopyTxData.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. J1939TpRxFcNPdu

**描述**: This N-PDU represents the TP.CM frame that is used in reverse direction for a J1939 transport
protocol session using the CMDT protocol type. TP.CM in reverse direction is used for intermediate
and final acknowledgement of received data and to abort the connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpRxFcNPduId
  长名称: ''
  描述: The N-PDU identifier used for communication with CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. J1939TpTxCmNPdu

**描述**: This N-PDU represents the TP.CM frame of a J1939 transport protocol session. TP.CM is used both by
BAM and CMDT to initialize the connection. For CMDT, it is also used to abort the connection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxCmNPduTxConfId
  长名称: ''
  描述: The N-PDU identifier used for Tx confirmation from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. J1939TpTxDtNPdu

**描述**: This N-PDU represents the TP.DT frame of a J1939 transport protocol session. TP.DT is used both by
BAM and CMDT to transfer the contents of an N-SDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxDtNPduTxConfId
  长名称: ''
  描述: The N-PDU identifier used for Tx confirmation from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. J1939TpTxPg

**描述**: Parameter group transmitted by the J1939 transport layer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxPgDynLength
  长名称: ''
  描述: This flag is set to TRUE when the N-SDU refers to a PGN with variable length.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939TpTxPgPGN
  长名称: ''
  描述: Defines the PGN which is represented by the N-SDU.
  默认值: ''
  最小值: 0
  最大值: 262143
```

### 15. J1939TpTxDirectNPdu

**描述**: This N-PDU represents the short frame that is used for a dynamic length PGN when it has a length of
less that 8 bytes.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxDirectNPduTxConfId
  长名称: ''
  描述: The N-PDU identifier used for Tx confirmation from CanIf.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 16. J1939TpTxNSdu

**描述**: This container describes the parameters that are relevant for the transmission of a specific N-SDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpTxNSduId
  长名称: ''
  描述: The N-SDU identifier used for communication with PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 17. J1939TpGeneral

**描述**: This container describes the general configuration parameters of the J1939Tp  module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: J1939TpCancellationSupport
  长名称: ''
  描述: Enable transmit and receive cancellation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: J1939TpDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: J1939TpMainFunctionPeriod
  长名称: ''
  描述: Allow to configure the time for the MainFunction (in seconds).
  默认值: ''
  最小值: 0
  最大值: 0.255
- 
  序号: 4
  名称: J1939TpTxConfTimeout
  长名称: ''
  描述: Timeout in seconds for the CanIf Tx confirmation. After this time the J1939Tp assumes that an
      N-PDU could not be transmitted.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 5
  名称: J1939TpVersionInfoApi
  长名称: ''
  描述: The function J1939Tp_GetVersionInfo is configurable (On/Off) by this configuration parameter.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: J1939TpUserConfigurationFile
  长名称: ''
  描述: Path to user configuration file. The content of this file is included in J1939Tp_Cfg.h during
      generation.
  默认值: ''
  最小值: ''
  最大值: ''
```

