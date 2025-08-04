# Mirror

## 模块描述

Configuration of the Bus Mirroring module.

## 容器列表

### 1. MirrorConfigSet

**描述**: Contains the configuration parameters and sub containers of the Bus Mirroring module.

该容器没有参数。

### 2. MirrorDestNetworkCan

**描述**: Destination bus representing a CAN network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestQueueSize
  长名称: ''
  描述: Number of frames that can be stored in the output queue for the destination bus.
  默认值: 20
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: MirrorStatusCanId
  长名称: ''
  描述: CAN ID of the CAN status frame.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 3. MirrorDestPdu

**描述**: I-PDU used for transmission of the mirrored frames on the destination bus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestPduId
  长名称: ''
  描述: I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestPduUsesTriggerTransmit
  长名称: ''
  描述: Switches transmission via TriggerTransmit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. MirrorDestNetworkCdd

**描述**: Destination bus representing a user defined network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestQueueSize
  长名称: ''
  描述: Number of frames that can be stored in the output queue for the destination bus.
  默认值: 20
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestTransmissionDeadline
  长名称: ''
  描述: Time in seconds after which the collection of source frames into the destination frame stopped
      and  the frame is sent at the latest.
  默认值: 0.1
  最小值: 0.001
  最大值: 0.655
- 
  序号: 3
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 5. MirrorDestPdu

**描述**: I-PDU used for transmission of the mirrored frames on the destination bus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestPduId
  长名称: ''
  描述: I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestPduUsesTriggerTransmit
  长名称: ''
  描述: Switches transmission via TriggerTransmit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. MirrorDestNetworkFlexRay

**描述**: Destination bus representing a FlexRay network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestQueueSize
  长名称: ''
  描述: Number of frames that can be stored in the output queue for the destination bus.
  默认值: 20
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestTransmissionDeadline
  长名称: ''
  描述: Time in seconds after which the collection of source frames into the destination frame stopped
      and  the frame is sent at the latest.
  默认值: 0.1
  最小值: 0.001
  最大值: 0.655
- 
  序号: 3
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 7. MirrorDestPdu

**描述**: I-PDU used for transmission of the mirrored frames on the destination bus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestPduId
  长名称: ''
  描述: I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestPduUsesTriggerTransmit
  长名称: ''
  描述: Switches transmission via TriggerTransmit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. MirrorDestNetworkIp

**描述**: Destination bus representing an IP network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestQueueSize
  长名称: ''
  描述: Number of frames that can be stored in the output queue for the destination bus.
  默认值: 20
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestTransmissionDeadline
  长名称: ''
  描述: Time in seconds after which the collection of source frames into the destination frame stopped
      and  the frame is sent at the latest.
  默认值: 0.1
  最小值: 0.001
  最大值: 0.655
- 
  序号: 3
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 9. MirrorDestPdu

**描述**: I-PDU used for transmission of the mirrored frames on the destination bus.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDestPduId
  长名称: ''
  描述: I-PDU identifier used for TxConfirmation from PduR.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: MirrorDestPduUsesTriggerTransmit
  长名称: ''
  描述: Switches transmission via TriggerTransmit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. MirrorSourceNetworkCan

**描述**: Source bus representing a CAN network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: MirrorSourceMaxDynamicFilters
  长名称: ''
  描述: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().
  默认值: 5
  最小值: 0
  最大值: 255
```

### 11. MirrorSourceCanMaskBasedIdMapping

**描述**: Rule for remapping a set of CAN IDs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceCanMaskBasedIdMappingDestBaseId
  长名称: ''
  描述: Base ID merged with the masked parts of the original CAN ID to form the mapped CAN ID.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: MirrorSourceCanMaskBasedIdMappingSourceCanIdCode
  长名称: ''
  描述: Value to match masked original CAN IDs.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: MirrorSourceCanMaskBasedIdMappingSourceCanIdMask
  长名称: ''
  描述: Mask applied to original CAN IDs before comparison.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 12. MirrorSourceCanSingleIdMapping

**描述**: Rule for remapping a single CAN ID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceCanSingleIdMappingDestCanId
  长名称: ''
  描述: Mapped CAN ID.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: MirrorSourceCanSingleIdMappingSourceCanId
  长名称: ''
  描述: Original CAN ID.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 13. MirrorSourceNetworkFlexRay

**描述**: Source bus representing a FlexRay network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: MirrorSourceMaxDynamicFilters
  长名称: ''
  描述: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().
  默认值: 5
  最小值: 0
  最大值: 255
```

### 14. MirrorSourceFlexRayFilter

**描述**: Pre-configured filter for FlexRay frames.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceFlexRayFilterChannelAssignment
  长名称: ''
  描述: FlexRay channels accepted by the filter.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MirrorSourceFlexRayFilterCycleRepetition
  长名称: ''
  描述: Cycle repetition of accepted cycles.
  默认值: ''
  最小值: 1
  最大值: 64
- 
  序号: 3
  名称: MirrorSourceFlexRayFilterId
  长名称: ''
  描述: Unique identifier of the pre-configured FlexRay filter.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: MirrorSourceFlexRayFilterLowerBaseCycle
  长名称: ''
  描述: Lowest base cycle number that is accepted by the filter.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 5
  名称: MirrorSourceFlexRayFilterLowerSlot
  长名称: ''
  描述: Lowest slot ID that is accepted by the filter.
  默认值: ''
  最小值: 1
  最大值: 2047
- 
  序号: 6
  名称: MirrorSourceFlexRayFilterUpperBaseCycle
  长名称: ''
  描述: Highest base cycle number that is accepted by the filter.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 7
  名称: MirrorSourceFlexRayFilterUpperSlot
  长名称: ''
  描述: Highest slot ID that is accepted by the filter.
  默认值: ''
  最小值: 1
  最大值: 2047
```

### 15. MirrorSourceNetworkLin

**描述**: Source bus representing a LIN network.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorNetworkId
  长名称: ''
  描述: Network ID of the bus.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: MirrorSourceLinToCanBaseId
  长名称: ''
  描述: Base ID merged with the LIN frame ID to form the CAN ID.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: MirrorSourceMaxDynamicFilters
  长名称: ''
  描述: Maximum number of filters that can be dynamically added using Mirror_AddXxxFilter().
  默认值: 5
  最小值: 0
  最大值: 255
```

### 16. MirrorSourceLinFilterMask

**描述**: Pre-configured mask based filter for LIN frames.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceLinFilterId
  长名称: ''
  描述: Unique identifier of the pre-configured LIN filter.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: MirrorSourceLinFilterLinIdCode
  长名称: ''
  描述: Value to match masked frame IDs.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 3
  名称: MirrorSourceLinFilterLinIdMask
  长名称: ''
  描述: Mask applied to frame IDs before comparison.
  默认值: ''
  最小值: 0
  最大值: 63
```

### 17. MirrorSourceLinFilterRange

**描述**: Pre-configured range filter for LIN frames.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceLinFilterId
  长名称: ''
  描述: Unique identifier of the pre-configured LIN filter.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: MirrorSourceLinFilterLower
  长名称: ''
  描述: Lowest frame ID that is accepted by the filter.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 3
  名称: MirrorSourceLinFilterUpper
  长名称: ''
  描述: Highest frame ID that is accepted by the filter.
  默认值: ''
  最小值: 0
  最大值: 63
```

### 18. MirrorSourceLinToCanIdMapping

**描述**: Rule for mapping a LIN frame ID to a special CAN ID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorSourceLinToCanIdMappingCanId
  长名称: ''
  描述: CAN ID which lies outside of the range mapping.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: MirrorSourceLinToCanIdMappingLinId
  长名称: ''
  描述: Frame ID which is excluded from the range mapping.
  默认值: ''
  最小值: 0
  最大值: 63
```

### 19. MirrorGeneral

**描述**: Contains the general configuration parameters of the module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MirrorDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MirrorMainFunctionPeriod
  长名称: ''
  描述: Execution cycle of Mirror_MainFunction() in seconds.
  默认值: 0.05
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: MirrorVersionInfoApi
  长名称: ''
  描述: Pre-processor switch for enabling version info API support.
  默认值: false
  最小值: ''
  最大值: ''
```

