# Cdd

## 模块描述

The CDD module describes the minimal requirements that are necessary for the configuration of a CDD
with respect to the surrounding standardized BSW modules.

## 容器列表

### 1. CddComStackContribution

**描述**: Contribution of COM Stack modules.

该容器没有参数。

### 2. CddComIfUpperLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Device Driver that serves as the
UpperLayer of the Com Interface module.

该容器没有参数。

### 3. CddComIfUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. CddComIfUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddComIfHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
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

**描述**: Parameters that are necessary for the configuration of a Complex Device Driver that serves as the
LowerLayer of the Pdu Router module.

该容器没有参数。

### 10. CddPduRLowerLayerRxPdu

**描述**: This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRLowerLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. CddPduRLowerLayerTxPdu

**描述**: This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRLowerLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. CddPduRUpperLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Device Driver that serves as the
UpperLayer of the Pdu Router module.

该容器没有参数。

### 13. CddPduRUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRUpperLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. CddPduRUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddPduRUpperLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. CddSoAdUpperLayerContribution

**描述**: Parameters that are necessary for the configuration of a Complex Driver that serves as the
UpperLayer of the SoAd module.

该容器没有参数。

### 16. CddSoAdUpperLayerRxPdu

**描述**: This container specifies Rx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddSoAdUpperLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 17. CddSoAdUpperLayerTxPdu

**描述**: This container specifies Tx PDUs that are exchanged between the CDD and the standardized BSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CddSoAdUpperLayerHandleId
  长名称: ''
  描述: ECU wide unique, symbolic handle for the Pdu.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 18. CddEcucPartitionInteraction

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

