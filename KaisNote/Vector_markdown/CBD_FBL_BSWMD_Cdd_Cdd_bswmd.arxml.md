# Cdd

## 模块描述

The CDD module describes the minimal requirements that are necessary for the configuration of a
Complex Driver with access to the MICROSAR communication stack.

## 容器列表

### 1. CddComStackContribution

**描述**: Contribution of COM Stack modules.

该容器没有参数。

### 2. CddComIfUpperLayerContribution

**描述**: This container collects parameters for the configuration of a Complex Driver that serves as the
UpperLayer of a Com Interface module (e.g. CanIf, FrIf).

该容器没有参数。

### 3. CddComIfUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are received by the CDD through communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 4. CddComIfUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are transmitted by the CDD through communication stack.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. CddComMLowerLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Device Driver that serves as the
LowerLayer of the Communication Manager module.

该容器没有参数。

### 6. CddComMLowerLayerChannel

**描述**: This container contains the network specific parameters.

该容器没有参数。

### 7. CddGenericNmLowerLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Device Driver that serves as the
LowerLayer of the Generic NM module.

该容器没有参数。

### 8. CddGenericNmLowerLayerChannel

**描述**: NM Channel specific configuration parameters.

该容器没有参数。

### 9. CddPduRLowerLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Driver that serves as the
LowerLayer of the Pdu Router module.

该容器没有参数。

### 10. CddPduRLowerLayerRxPdu

**描述**: Rx PDU that is received by the Complex Driver and forwarded to the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRLowerLayerHandleId
  长名称: PduR Lower Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 11. CddPduRLowerLayerTxPdu

**描述**: Tx PDU that is received by the Complex Driver from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRLowerLayerHandleId
  长名称: PduR Lower Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 12. CddPduRUpperLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Driver that serves as the
UpperLayer of the Pdu Router module.

该容器没有参数。

### 13. CddPduRUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are received by the Complex Driver from the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRUpperLayerHandleId
  长名称: PduR Upper Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 14. CddPduRUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are transmitted from the Complex Driver to the PduR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRUpperLayerHandleId
  长名称: PduR Upper Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 15. CddJ1939RmContribution

**描述**: This container collects parameters for the configuration of a Complex Driver that serves as
UpperLayer of the J1939Rm module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddJ1939RmRequestIndication
  长名称: ''
  描述: |
    Enables the J1939Rm RequestIndication for this CDD. The RequestIndication provides information
    about a received J1939 RQST message which affects a J1939Rm user that references this CDD.
    
    Prototype of the RequestIndication:
    void <Cdd>_RequestIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn, uint8
    sourceAddress, uint8 destAddress, uint8 priority)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CddJ1939RmAckIndication
  长名称: ''
  描述: |
    Enables the J1939Rm AckIndication for this CDD. The AckIndication provides information about a
    received J1939 ACKM message which affects a J1939Rm user that references this CDD.
    
    Prototype of the AckIndication:
    void <Cdd>_AckIndication(uint8 node, NetworkHandleType channel, uint32 ackPgn, uint8 ackCode,
    uint8 ackAddress, uint8 sourceAddress, uint8 priority)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CddJ1939RmRequestTimeoutIndication
  长名称: ''
  描述: |
    Enables the J1939Rm RequestTimeoutIndication for this CDD. The RequestTimeoutIndication is
    called after time out of a transmitted J1939 RQST message.
    
    Prototype of the AckIndication:
    void <Cdd>_RequestTimeoutIndication(uint8 node, NetworkHandleType channel, uint32 requestedPgn,
    uint8 destAddress)
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. CddSoAdUpperLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Driver that serves as the
UpperLayer of the SoAd module.

该容器没有参数。

### 17. CddSoAdUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRApiType
  长名称: Api Type
  描述: This parameter configures the type of the CDD interface (IF/TP)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CddSoAdUpperLayerHandleId
  长名称: SoAd Upper Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 18. CddSoAdUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRApiType
  长名称: Api Type
  描述: This parameter configures the type of the CDD interface (IF/TP)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CddSoAdUpperLayerHandleId
  长名称: SoAd Upper Layer Handle Id
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 19. CddEcucPartitionInteraction

**描述**: This optional container holds the partition interaction configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPartitionStoppedFunctionName
  长名称: ''
  描述: Function name to be called when the partition which is triggering the complex driver is
      stopped.
  默认值: ''
  最小值: ''
  最大值: ''
```

