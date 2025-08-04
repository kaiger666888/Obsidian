# CanTp

## 模块描述

Configuration of the CanTp (CAN Transport Protocol) module.

## 容器列表

### 1. CanTpConfig

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR CanTp module.
This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist
once per configuration set.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpMainFunctionPeriod
  长名称: ''
  描述: Allow to configure the time for the MainFunction (as float in seconds). Please note: This
      period shall be the same as call cycle time of the periodic task were CanTp Main
      function is called.
  默认值: ''
  最小值: 0
  最大值: 0.255
```

### 2. CanTpChannel

**描述**: This container contains the configuration parameters of the CanTp channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpChannelMode
  长名称: ''
  描述: The CAN Transport Layer supports half and full duplex channel modes.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. CanTpRxNSdu

**描述**: The following parameters needs to be configured for each CAN N-SDU that the CanTp module receives
via the CanTpChannel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpBs
  长名称: ''
  描述: Sets the number of N-PDUs the CanTp receiver allows the sender to send, before waiting for an
      authorization to continue transmission of the following N-PDUs.For further details on
      this parameter value see ISO 15765-2 specification.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanTpNar
  长名称: ''
  描述: Value in seconds of the N_Ar timeout. N_Ar is the time for transmission of a CAN frame (any
      N_PDU) on the receiver side.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: CanTpNbr
  长名称: ''
  描述: Value in seconds of the performance requirement for (N_Br + N_Ar). N_Br is the elapsed time
      between the receiving indication of a FF or CF or the transmit confirmation of a FC,
      until the transmit request of the next FC.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: CanTpNcr
  长名称: ''
  描述: Value in seconds of the N_Cr timeout. N_Cr is the time until reception of the next Consecutive
      Frame N_PDU.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 5
  名称: CanTpRxAddressingFormat
  长名称: ''
  描述: Declares which communication addressing mode is supported for this Rx N-SDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanTpRxDl
  长名称: ''
  描述: Data Length Code of this RxNsdu. In case of variable message length, this value indicates the
      minimum data length.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: CanTpRxNSduId
  长名称: ''
  描述: Unique identifier user by the upper layer to call CanTp_CancelReceive, CanTp_ChangeParameter
      and CanTp_ReadParameter.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: CanTpRxPaddingActivation
  长名称: ''
  描述: Defines if the receive frame uses padding or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanTpRxTaType
  长名称: ''
  描述: Declares the communication type of this Rx N-SDU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: CanTpRxWftMax
  长名称: ''
  描述: This parameter indicates how many Flow Control wait N-PDUs can be consecutively transmitted by
      the receiver. It is local to the node and is not transmitted inside the FC protocol data
      unit.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 11
  名称: CanTpSTmin
  长名称: ''
  描述: Sets the duration of the minimum time the CanTp sender shall wait between the transmissions of
      two CF N-PDUs.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 4. CanTpNAe

**描述**: Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to
CanTpMixed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNAe
  长名称: ''
  描述: If an RxNsdu or a TxNsdu is configured for mixed addressing
  默认值: ''
  最小值: 0
  最大值: 255
```

### 5. CanTpNSa

**描述**: Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to
CanTpExtended.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNSa
  长名称: ''
  描述: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains
      the transport protocol source address's value.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. CanTpNTa

**描述**: The following parameters need to be configured for each RxNsdu or TxNsdu with the
CanTpAddressingFormat set to CanTpExtended.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNTa
  长名称: ''
  描述: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains
      the transport protocol target address's value.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 7. CanTpRxNPdu

**描述**: Used for grouping of the ID of a PDU and the Reference to a PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpRxNPduId
  长名称: ''
  描述: The N-PDU identifier attached to the RxNsdu is identified by CanTpRxNSduId.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 8. CanTpTxFcNPdu

**描述**: Used for grouping of the ID of a PDU and the Reference to a PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpTxFcNPduConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxFcNPdu to the
      CanIf module.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. CanTpTxNSdu

**描述**: The following parameters needs to be configured for each CAN N-SDU that the CanTp module transmits
via the CanTpChannel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNas
  长名称: ''
  描述: Value in second of the N_As timeout. N_As is the time for transmission of a CAN frame (any
      N_PDU) on the part of the sender.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: CanTpNbs
  长名称: ''
  描述: Value in seconds of the N_Bs timeout. N_Bs is the time of transmission until reception of the
      next Flow Control N_PDU.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: CanTpNcs
  长名称: ''
  描述: Value in seconds of the performance requirement of (N_Cs + N_As). N_Cs is the time which
      elapses between the transmit request of a CF N-PDU until the transmit request of the
      next CF N-PDU.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: CanTpTc
  长名称: ''
  描述: switch for enabling Transmit Cancellation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanTpTxAddressingFormat
  长名称: ''
  描述: Declares which communication addressing format is supported for this TxNsdu.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanTpTxDl
  长名称: ''
  描述: Data Length Code of this TxNsdu. In case of variable length message, this value indicates the
      minimum data length.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: CanTpTxNSduId
  长名称: ''
  描述: Unique identifier to a structure that contains all useful information to process the
      transmission of a TxNsdu.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: CanTpTxPaddingActivation
  长名称: ''
  描述: Defines if the transmit frame use padding or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanTpTxTaType
  长名称: ''
  描述: Declares the communication type of this TxNsdu.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. CanTpNAe

**描述**: Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to
CanTpMixed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNAe
  长名称: ''
  描述: If an RxNsdu or a TxNsdu is configured for mixed addressing
  默认值: ''
  最小值: 0
  最大值: 255
```

### 11. CanTpNSa

**描述**: Contains the parameters needed to configure each RxNSdu or TxNSdu with CanTpAddressingFormat set to
CanTpExtended.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNSa
  长名称: ''
  描述: If an RxNSdu or a TxNSdu is configured for extended addressing format, this parameter contains
      the transport protocol source address's value.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 12. CanTpNTa

**描述**: The following parameters need to be configured for each RxNsdu or TxNsdu with the
CanTpAddressingFormat set to CanTpExtended.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpNTa
  长名称: ''
  描述: If an RxNsdu or a TxNsdu is configured for extended addressing format, this parameter contains
      the transport protocol target address's value.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 13. CanTpRxFcNPdu

**描述**: Used for grouping of the ID of a PDU and the Reference to a PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpRxFcNPduId
  长名称: ''
  描述: N-PDU identifier attached to the FC N-PDU of this TxNsdu identified by CanTpTxNSduId.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. CanTpTxNPdu

**描述**: Used for grouping of the ID of a PDU and the Reference to a PDU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpTxNPduConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the CanIf to confirm the transmission of the CanTpTxNPdu to the CanIf
      module.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. CanTpGeneral

**描述**: This container contains the general configuration parameters of the CanTp module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTpChangeParameterApi
  长名称: ''
  描述: This parameter, if set to true, enables the CanTp_ChangeParameterRequest Api for this Module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanTpDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanTpPaddingByte
  长名称: ''
  描述: Used for the initialization of unused bytes with a certain value
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: CanTpReadParameterApi
  长名称: ''
  描述: This parameter, if set to true, enables the CanTp_ReadParameterApi for this module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanTpVersionInfoApi
  长名称: ''
  描述: The function CanTp_GetVersionInfo is configurable (On/Off) by this configuration parameter.
  默认值: ''
  最小值: ''
  最大值: ''
```

