# PduR

## 模块描述

Configuration of the PduR (PDU Router) module.

## 容器列表

### 1. PduRBswModules

**描述**: Each container describes a specific BSW module (upper/CDD/lower/IpduM) that the PDU Router shall
interface to.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRCancelReceive
  长名称: ''
  描述: Specifies if the Transport protocol module supports the CancelReceive API or not. Value true
      the API is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRCancelTransmit
  长名称: ''
  描述: Specifies if the BSW module supports the CancelTransmit API or not. Value true the API is
      supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PduRChangeParameterRequestApi
  长名称: ''
  描述: This parameter, if set to true, enables the PduR_<Up>ChangeParameterRequest Api for this
      Module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PduRCommunicationInterface
  长名称: ''
  描述: Specifies if the BSW module supports the Communication Interface APIs or not. Value true the
      APIs are supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PduRLowerModule
  长名称: ''
  描述: The PduRLowerModule will decide who will call the APIs and who will implement the APIs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PduRRetransmission
  长名称: ''
  描述: If set to true this means that the destination transport protocol module will use the
      retransmission feature. This parameter might be set to false if the retransmission
      feature is not used, even though the destination transport protocol is supporting it.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PduRTransportProtocol
  长名称: ''
  描述: The PDU Router module shall use the API parameters specified for transport protocol interface.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PduRTriggertransmit
  长名称: ''
  描述: Specifies if the BSW module supports the TriggerTransmit API or not. Value true the API is
      supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PduRTxConfirmation
  长名称: ''
  描述: Specifies if the BSW module supports the TxConfirmation API or not. Value true the API is
      supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: PduRUpperModule
  长名称: ''
  描述: The PduRUpperModule will decide who will call the APIs and who will implement the APIs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: PduRUseTag
  长名称: ''
  描述: This parameter, if set to true, enables the usage of the tag (<up>) in the following API
      calls:
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. PduRGeneral

**描述**: This container is a subcontainer of PduR and specifies the general configuration parameters of the
PDU Router.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDevErrorDetect
  长名称: ''
  描述: If true then PDU Router will enable the error-reporting to the Development Error Tracer (DET).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRVersionInfoApi
  长名称: ''
  描述: If true the PduR_GetVersionInfo API is available.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PduRZeroCostOperation
  长名称: ''
  描述: If set the PduR configuration generator will report an error if zero-cost-operation cannot be
      fulfilled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. PduRRoutingTables

**描述**: Represents one table of routing paths.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRConfigurationId
  长名称: ''
  描述: Identification of the configuration of the PduR configuration. This identification can be read
      using the PduR API.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. PduRRoutingPathGroup

**描述**: This container groups routing path destinations. Destinations are used instead of routing paths
since a routing path can be 1:n. It is desirable to be able to enable/disable a specific bus (i.e. a
destination) rather than a routing path. Of course it is possible to create groups that covers
specific routing paths as well.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRIsEnabledAtInit
  长名称: ''
  描述: If set to true this routing path group will be enabled after initializing the PDU Router
      module (i.e. enabled in the PduR_Init function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRRoutingPathGroupId
  长名称: ''
  描述: Identification of the routing group.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. PduRRoutingTable

**描述**: Represents one container of routing paths. Each container is either minimum routing or not.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRIsMinimumRouting
  长名称: ''
  描述: Specifies if the container contains routing paths that are of the type minimum routing or not.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. PduRRoutingPath

**描述**: This container is a subcontainer of PduRRoutingTable and specifies the routing path of a PDU.

该容器没有参数。

### 7. PduRDestPdu

**描述**: This container is a subcontainer of PduRRoutingPath and specifies one destination for the PDU to be
routed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDestPduDataProvision
  长名称: ''
  描述: Specifies how data are provided: direct (as part of the Transmit call) or via the
      TriggerTransmit callback function. Only required for non-TP I-PDUs (local and
      gatewayed).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PduRDestPduHandleId
  长名称: ''
  描述: PDU identifier assigned by PDU Router. Used by communication interface and transport protocol
      modules for confirmation.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: PduRTpThreshold
  长名称: ''
  描述: Defines the number of bytes which shall be received before transmission on the destination bus
      may start. Only required for routing-on-the-fly TP gateway PDUs. The threshold shall not
      be larger than the length of the related TP Buffer.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: PduRTransmissionConfirmation
  长名称: ''
  描述: This parameter is only for communication interfaces. Transport protocol modules will always
      call the TxConfirmation function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. PduRDefaultValue

**描述**: Specifies the default value of the I-PDU. Only required for gateway operation and if at least one
PDU specified by PduRDestPdu uses TriggerTransmit Data provision.

该容器没有参数。

### 9. PduRDefaultValueElement

**描述**: Each value element is represented by the element and the position in an array.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRDefaultValueElement
  长名称: ''
  描述: The default value consists of a number of elements. Each element is one byte long and the
      number of elements is specified by SduLength. The position of this parameter in the
      container is specified by the PduRElementBytePosition parameter.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: PduRDefaultValueElementBytePosition
  长名称: ''
  描述: This parameter specifies the byte position of the element within the default value
  默认值: ''
  最小值: 0
  最大值: 255
```

### 10. PduRSrcPdu

**描述**: This container is a subcontainer of PduRRoutingPath and specifies the source of the PDU to be
routed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRSourcePduHandleId
  长名称: ''
  描述: PDU identifier assigned by PDU Router.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 11. PduRTpBufferTable

**描述**: This container will specify the needed buffers for gatewaying using TP. It is not connected to the
specific routing path destination to allow a more efficient buffer handling.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRMaxTpBufferNumber
  长名称: ''
  描述: maximum number of TP buffers.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. PduRTpBuffer

**描述**: Specifies a buffer used for gatwaying through TP.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRTpBufferLength
  长名称: ''
  描述: Length of the TP buffer in number of bytes
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 13. PduRTxBufferTable

**描述**: This container will specify the needed buffers for gatewaying using communication interface. It not
defined per routing path to allow reusage of buffers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRMaxTxBufferNumber
  长名称: ''
  描述: maximum number of Tx buffers.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. PduRTxBuffer

**描述**: Specifies a buffer used for gatwaying through communication interface.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PduRPduMaxLength
  长名称: ''
  描述: Length of the Tx buffer in number of bytes.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: PduRTxBufferDepth
  长名称: ''
  描述: Number of Pdus that can be stored in the buffer. If value is 1 then the buffer semantic is
      "last is best". If the value is greater then 1 then the buffer semnatic is a FiFo.
  默认值: ''
  最小值: 1
  最大值: 255
```

