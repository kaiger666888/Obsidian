# IdsM

## 容器列表

### 1. IdsMConfiguration

**描述**: Configuration parameters of the module IdsM.

该容器没有参数。

### 2. IdsMBlockState

**描述**: Configuration of an IdsM blocking state used in the IdsMStateBlockFilter to suspend the collection
of security events.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMBlockStateID
  长名称: ''
  描述: This value specifies the identifier of this block state.
  默认值: ''
  最小值: 0
  最大值: 15
```

### 3. IdsMBufferConfiguration

**描述**: Configuration of the event buffers and context data buffers used by IdsM.

该容器没有参数。

### 4. IdsMContextDataBuffer

**描述**: Buffer that is reserved to store the context data of SEvs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMContextDataBufferSize
  长名称: ''
  描述: Size of the context data buffer in bytes.
  默认值: ''
  最小值: 1
  最大值: 1500
- 
  序号: 2
  名称: IdsMNumberOfContextDataBuffers
  长名称: ''
  描述: The number of buffers with the configured buffer size specified in IdsMContextDataBufferSize.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 5. IdsMEventBuffers

**描述**: Buffers used to store the SEvs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMNumberOfEventBuffers
  长名称: ''
  描述: The number of event buffers used to store the SEvs.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 6. IdsMEvent

**描述**: Configuration of the IdsM Event unit which is reported by a sensor and its parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMExternalEventId
  长名称: ''
  描述: The external security event ID which is reported to the sink.
  默认值: ''
  最小值: 0
  最大值: 65534
- 
  序号: 2
  名称: IdsMInternalEventId
  长名称: ''
  描述: Consecutive number used internally as an identifier by the IdsM module.
  默认值: 65535
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: IdsMReportingModeFilter
  长名称: ''
  描述: The reporting mode filter defines the level of detail of the reporting. Whether SEv should be
      dropped, forwarded with context data or forwarded without context data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IdsMSensorInstanceId
  长名称: ''
  描述: The instance ID of the sensor which reports security events to the IdsM.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: IdsMSinkDem
  长名称: ''
  描述: The QSEv will be sent to the Dem Module into a Security Event Memory (Sem) to persist it on
      the local ECU.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IdsMSinkIdsR
  长名称: ''
  描述: The QSEv will be sent to the IDS Reporter.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. IdsMServiceInterfaceOptions

**描述**: Adittional configuration parameters of a SEv when the sensor is a SW-C or application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMAdditionalParameterOption
  长名称: ''
  描述: In addition to the optional context data the Service Port Interface can be extended by the
      following parameters:
  默认值: None
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IdsMEventMaxContextDataSize
  长名称: ''
  描述: Maximum number of bytes used by the IdsM and the RTE when forwarding context data of the
      corresponding security event.
  默认值: 0
  最小值: 0
  最大值: 1500
```

### 8. IdsMFilterChain

**描述**: A filter chain is a combination of filters that affects one or more SEvs.

该容器没有参数。

### 9. IdsMBlockStateFilter

**描述**: This state filter drops SEvs if the current State reported by the BswM is in this state filter list.

该容器没有参数。

### 10. IdsMEventAggregationFilter

**描述**: All received events of a certain event ID that are received by this filter during a single
aggregation time interval are not forwarded immediately.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMContextDataSourceSelector
  长名称: ''
  描述: The resulting SEv from the aggregation filter contains the context data from one of the
      following two sources:
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IdsMEventAggregationTimeInterval
  长名称: ''
  描述: Length of the aggregation time interval (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: INF
```

### 11. IdsMEventThresholdFilter

**描述**: During each time interval "IdsMEventThresholdTimeInterval", the filter drops the first
"IdsMEventThresholdNumber - 1" SEvs and forwards all other incoming SEvs immediately until the end
of the time interval.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMEventThresholdNumber
  长名称: ''
  描述: This parameter assigns the threshold 'p' for each SEv ID affected by this threshold filter.
  默认值: ''
  最小值: 2
  最大值: 65535
- 
  序号: 2
  名称: IdsMEventThresholdTimeInterval
  长名称: ''
  描述: Length of the threshold time interval (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: INF
```

### 12. IdsMForwardEveryNthFilter

**描述**: Out of all incoming SEVs, drop all but every nth. Those will be forwarded without modification.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMNthParameter
  长名称: ''
  描述: For each SEv ID for which this filter is configured, this parameter assigns the appropriate n.
  默认值: ''
  最小值: 2
  最大值: 65535
```

### 13. IdsMPdus

**描述**: Configuration of the PDU references used to send the events data.

该容器没有参数。

### 14. IdsMIfTxPdu

**描述**: IF PDU used to transmit a QSEv via the PduR to the IdsR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMIfTxPduHandleId
  长名称: ''
  描述: IdsM does not use this parameter, content will be ignored.
  默认值: 0
  最小值: 0
  最大值: 0
```

### 15. IdsMTpTxPdu

**描述**: TP PDU used to transmit a QSEv via the PduR to the IdsR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMTpTxPduHandleId
  长名称: ''
  描述: IdsM does not use this parameter, content will be ignored.
  默认值: 0
  最小值: 0
  最大值: 0
```

### 16. IdsMGeneral

**描述**: General configuration parameters of IdsM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMDevErrorDetect
  长名称: ''
  描述: This parameter enables/disables the Development Error Detection and Notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IdsMDiagnosticSupport
  长名称: ''
  描述: Enables or disables the Dcm APIs which are used to read and write certain values of the IdsM
      module through the diagnostic communication manager.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IdsMInstanceId
  长名称: ''
  描述: The unique identifier of the sending IdsM instance.
  默认值: ''
  最小值: 0
  最大值: 1023
- 
  序号: 4
  名称: IdsMMainFunctionPeriod
  长名称: ''
  描述: The period between successive calls to the IdsM main function (as float in seconds).
  默认值: 0.01
  最小值: 0
  最大值: INF
- 
  序号: 5
  名称: IdsMSignatureGenerateResultLength
  长名称: ''
  描述: This parameter defines the length in bytes of the signature calculated by the crypto services.
      This parameter should be set when the IdsMSignatureSupport is enabled.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: IdsMSignatureSupport
  长名称: ''
  描述: This parameter enables/disables the functionality of sending messages to the network with a
      signature of encryption calculated by the crypto services.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IdsMTimestampOption
  长名称: ''
  描述: This parameter enables/disables the functionality of having a timestamp field as part of a
      QSEv and if the origin of the timestamp is from the AUTOSAR stack or from the
      application (custom timestamp).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IdsMVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function IdsM_GetVersionInfo() to get major, minor and
      patch version information of the module.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. IdsMGlobalRateLimitationFilters

**描述**: Global rate limitation filters for all SEvs.

该容器没有参数。

### 18. IdsMFilterEventRateLimitation

**描述**: For configurable time intervals of length "IdsMRateLimitationTimeInterval" this filter forwards all
the SEvs until reaching the limit "IdsMRateLimitationMaximumEvents".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMRateLimitationMaximumEvents
  长名称: ''
  描述: The maximum number of SEvs which are passed on by this filter in a single rate limitation time
      interval.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: IdsMRateLimitationTimeInterval
  长名称: ''
  描述: Time interval length of the event rate limitation filter (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: INF
```

### 19. IdsMFilterTrafficLimitation

**描述**: The traffic limitation filter forwards all the incoming SEvs until reaching the limit
"IdsMTrafficLimitationMaximumBytes".

#### 参数列表

```yaml
- 
  序号: 1
  名称: IdsMTrafficLimitationMaximumBytes
  长名称: ''
  描述: The maximum number of bytes to be sent out by the IdsM in a single traffic limitation time
      interval.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: IdsMTrafficLimitationTimeInterval
  长名称: ''
  描述: Length of the traffic limitation time interval (as float in seconds).
  默认值: ''
  最小值: 0
  最大值: INF
```

