# Dcm

## 模块描述

Configuration of the Dcm (Diagnostic Communications Manager) module.

## 容器列表

### 1. DcmConfigSet

**描述**: This container contains the configuration parameters and sub containers of the DCM module supporting
multiple configuration sets.

该容器没有参数。

### 2. DcmDsd

**描述**: These parameters apply to Diagnostic Service Dispatcher. All parameters for all service dispatchers
are included in this one configuration container.

该容器没有参数。

### 3. DcmDsdServiceTable

**描述**: This container contains the configuration (DSD parameters) for Service Identifier Table.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDsdSidTabId
  长名称: ''
  描述: Due the fact of using one or more service tables the member of the Service Identifier Table
      includes a unique id for the Service Identifier Table.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. DcmDsdService

**描述**: This container contains the configuration (DSD parameters) for Service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDsdSidTabFnc
  长名称: ''
  描述: Callback function of the ECU Supplier specific component for the particular
      DcmDsdSidTabServiceId.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDsdSidTabServiceId
  长名称: ''
  描述: Id of the Service identifier.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DcmDsdSidTabSubfuncAvail
  长名称: ''
  描述: Information whether the DcmDsdSidTabServiceId includes Sub functions or not. Used for the
      Handling of "suppressPosRspMsgIndicationBit" ISO14229-1 can be referenced here, as this
      specification gives fix definition, if an SID includes Subfunction or not.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. DcmDsdSubService

**描述**: This container contains the configuration (DSD parameters) for SubServices. This configuration is
available only for services having Subfunction: this container exists only if parameter
DcmDsdSidTabSubfuncAvail, of this service, is set to TRUE and the parameter DcmDsdSidTabFnc is not
existing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDsdSubServiceFnc
  长名称: ''
  描述: Callback function of the ECU Supplier specific component. This parameter is related to the
      interface <Module>_<DiagnosticService>_<SubService>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDsdSubServiceId
  长名称: ''
  描述: Id of the SubService identifier. The possible Subfunction parameter value are predefined in
      the ISO 14229-1 and ISO 15031-5.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. DcmDsl

**描述**: These parameters apply to a Diagnostic Session Layer. There may be a parameter set (DSL
Configuration) per protocol.

该容器没有参数。

### 7. DcmDslBuffer

**描述**: This container contains the configuration (parameters) for the diagnostic buffer.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslBufferSize
  长名称: ''
  描述: Size of Diagnostic Buffer (in Bytes)
  默认值: ''
  最小值: 8
  最大值: 4294967294
```

### 8. DcmDslCallbackDCMRequestService

**描述**: The name of this container is used to define the name of the R-Port through which the DCM access the
interface CallbackDCMRequestServices.

该容器没有参数。

### 9. DcmDslDiagResp

**描述**: This container contains the configuration (parameters) for the ResponsePending handling

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslDiagRespMaxNumRespPend
  长名称: ''
  描述: Maximum number of negative responses with response code 0x78
      (requestCorrectlyReceived-ResponsePending) allowed per request. DCM will send a negative
      response with response code 0x10                 (generalReject), in case the limit
      value gets reached.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDslDiagRespOnSecondDeclinedRequest
  长名称: ''
  描述: Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to
      priority assessment).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. DcmDslProtocol

**描述**: This container contains the configuration (parameters) for the protocol configuration (for each
protocol) The following parameters needs to be configured per protocol.

该容器没有参数。

### 11. DcmDslProtocolRow

**描述**: Definition of a single Row of configuration for the protocol configuration (for each protocol)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolEndiannessConvEnabled
  长名称: ''
  描述: Enables /disables the endianness conversion, per diagnostic
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslProtocolID
  长名称: ''
  描述: The diagnostic protocol type for the DCM DSL protocol that is being configured.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDslProtocolIsParallelExecutab
  长名称: ''
  描述: Enables the parallel processing of ROE or Periodic Transmission protocol. Only these both
      protocols are allowed to run in parallel to normal protocol (UDS, OBD).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDslProtocolPreemptTimeout
  长名称: ''
  描述: This is the value for the timeout (in milliseconds) of preempting protocol until protocol
      needs to be started.
  默认值: ''
  最小值: 0
  最大值: 1000
- 
  序号: 5
  名称: DcmDslProtocolPriority
  长名称: ''
  描述: The SWS for DCM defines this item as uint8. This is the protocol priority that is used during
      protocol preemption handling.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DcmDslProtocolTransType
  长名称: ''
  描述: Selects the transmission type for protocol.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmSendRespPendOnTransToBoot
  长名称: ''
  描述: Parameter specifying if the ECU should send a NRC 0x78 (response pending) before transitioning
      to the bootloader (parameter set to TRUE) or if the transition shall be initiated
      without sending NRC 0x78 (parameter set to FALSE).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmTimStrP2ServerAdjust
  长名称: ''
  描述: This parameter is used to gurantee that the DCM response is available on the bus before
      reaching P2.This parameter value in milliseconds has to be configured as a multiple of
      DcmTaskTime and is minimum in the timing handling of P2.
  默认值: ''
  最小值: 0
  最大值: 1000
- 
  序号: 9
  名称: DcmTimStrP2StarServerAdjust
  长名称: ''
  描述: This parameter is used to gurantee that the DCM response is available on the bus before
      reaching P2*.This parameter value in milliseconds has to be configured as multiple of
      DcmTaskTime and is minimum in the timing handling of P2*.
  默认值: ''
  最小值: 0
  最大值: 5000
```

### 12. DcmDslMainConnection

**描述**: This container contains configuration for Diagnostic Main Connection

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolRxTesterSourceAddr
  长名称: ''
  描述: Tester source address uniquely describes a client and will be used e.g. within
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 13. DcmDslProtocolRx

**描述**: This container contains the configuration (parameters) for the protocol configuration of RX channel
(for each protocol)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslProtocolRxAddrType
  长名称: ''
  描述: Declares the communication type of this DCM_PROTOCOL_DCMRXPDUID.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDslProtocolRxChannelId
  长名称: ''
  描述: Channel Identifier associated to the received Pdu.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DcmDslProtocolRxPduId
  长名称: ''
  描述: DcmRxPduId value for reception of requests.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 14. DcmDslProtocolTx

**描述**: This container contains the configuration (parameters) for the protocol configuration of TX channel
(for each protocol)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the DcmDsProtocolTxPdu
      to the LowerLayer.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 15. DcmDslPeriodicTransmission

**描述**: This container contains the configuration (parameters) for Periodic Transmission service.

该容器没有参数。

### 16. DcmDslPeriodicConnection

**描述**: Holding the TxPduId configuration for PeriodicTransmission.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslPeriodicTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the DcmDslPeriodicTxPdu
      to the LowerLayer.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 17. DcmDslResponseOnEvent

**描述**: This container contains the configuration (parameters) for ResponseOnEvent service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDslRoeTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the Lower Layer to confirm the transmission of the DcmDslRoeTxPdu to
      the LowerLayer.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 18. DcmDslServiceRequestManufacturerNotification

**描述**: The name of this container is used to define the name of the R-Port through which the DCM accesses
the interface ServiceRequestNotification.

该容器没有参数。

### 19. DcmDslServiceRequestSupplierNotification

**描述**: The name of this container is used to define the name of the R-Port through which the DCM accesses
the interface ServiceRequestNotification.

该容器没有参数。

### 20. DcmDsp

**描述**: These parameters apply to Diagnostic Service Processing. There will always be one set of these
parameters per DCM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMaxDidToRead
  长名称: ''
  描述: Indicates the maximum allowed DIDs in a single "ReadDataByIdentifier" request.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspPowerDownTime
  长名称: ''
  描述: This parameter indicates to the client the minimum time of the  stand-by sequence the server
      will remain in the power-down sequence.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 21. DcmDspComControl

该容器没有参数。

### 22. DcmDspComControlAllChannel

**描述**: Collection of ComM channels which shall be controlled if all networks are addressed.

该容器没有参数。

### 23. DcmDspComControlSetting

**描述**: Provide the configuration of the Communication control.

该容器没有参数。

### 24. DcmDspComControlSpecificChannel

**描述**: Assigns subnet number to ComM channel which will be controlled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSubnetNumber
  长名称: ''
  描述: Subnet Number which controls the specific ComMChannel.
  默认值: ''
  最小值: 1
  最大值: 14
```

### 25. DcmDspControlDTCSetting

**描述**: Provide the configuration of the ControlDTCSetting mechanism.

该容器没有参数。

### 26. DcmDspData

**描述**: This container contains the configuration (parameters) of a Data belonging to a DID

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDataConditionCheckReadFnc
  长名称: ''
  描述: Function name to demand application if the conditions (e.g. System state) to read the DID are
      correct. (ConditionCheckRead-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDataEcuSignal
  长名称: ''
  描述: Function name to control the access to a certain ECU Signal by the DCM.
      (IoHwAb_Dcm_<EcuSignalName>-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspDataFreezeCurrentStateFnc
  长名称: ''
  描述: Function name to request to application to freeze the current state of an IOControl.
      (FreezeCurrentState-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspDataGetScalingInfoFnc
  长名称: ''
  描述: Function name to request to application the scaling information of the DID.
      (GetScalingInformation-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDspDataReadDataLengthFnc
  长名称: ''
  描述: Function name to request from application the data length of a DID. (ReadDataLength-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmDspDataReadEcuSignal
  长名称: ''
  描述: Function name for read access to a certain ECU Signal by the DCM.
      (IoHwAb_Dcm_Read<EcuSignalName>-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDspDataReadFnc
  长名称: ''
  描述: Function name to request from application the data value of a DID. (ReadData-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmDspDataResetToDefaultFnc
  长名称: ''
  描述: Function name to request to application to reset an IOControl to default value.
      (ResetToDefault-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspDataReturnControlToEcuFnc
  长名称: ''
  描述: Function name to request to application to return control to ECU of an IOControl.
      (ReturnControlToECU-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DcmDspDataShortTermAdjustmentFnc
  长名称: ''
  描述: Function name to request to application to adjuste the IO signal.
      (ShortTermAdjustment-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DcmDspDataSize
  长名称: ''
  描述: Length of data in bits associated to the Data. If Data has variable datalength, that
      corresponds to the maximum datalength.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 12
  名称: DcmDspDataType
  长名称: ''
  描述: Provide the data type of Data belonging to a DID.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DcmDspDataUsePort
  长名称: ''
  描述: Define wich interface shall be used to access the data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DcmDspDataWriteFnc
  长名称: ''
  描述: Function name to request application to write the data value of a DID. (WriteData-function).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 27. DcmDspDataInfo

**描述**: This container contains the configuration (parameters) of a Data

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDataFixedLength
  长名称: ''
  描述: Indicates if the datalength of the Data is fixed
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDataScalingInfoSize
  长名称: ''
  描述: If Scaling information service is available for this Data, it provides the size of the scaling
      information.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 28. DcmDspDid

**描述**: This container contains the configuration (parameters) of the DID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidIdentifier
  长名称: ''
  描述: 2 byte Identifier of the DID
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspDidRoeQueueEnabled
  长名称: ''
  描述: If set to TRUE, the ROE queue mechanism will be used in case of ROE OnChangeOfDataIdentifier
      on this DID.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspDidUsed
  长名称: ''
  描述: Allow to activate or deactivate the usage of a DID, for multi  purpose ECUs
  默认值: ''
  最小值: ''
  最大值: ''
```

### 29. DcmDspDidExtRoe

**描述**: Provide information to manage a responseOnEvent  request on this DID externally. If this container
doesn't exist, an ROE event on this DID will be managed internally.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidRoeActivateFnc
  长名称: ''
  描述: Function name to activate/deactivate an ROE event managed externally. Only relevant if
      DcmDspDataUsePort== USE_DATA_SYNCH_FNC or USE_DATA_ASYNCH_FNC. This parameter is related
      to the interface xxx_ActivateEvent.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDidRoeEventId
  长名称: ''
  描述: EventId to be used within Apis  Dcm_TriggerOnEvent() and xxx_ActivateEvent()
  默认值: ''
  最小值: 0
  最大值: 255
```

### 30. DcmDspDidSignal

**描述**: This container defines the reference to 1 DcmDspData container and position relevant for this DID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidDataPos
  长名称: ''
  描述: Defines the position of the data defined by DcmDspDidDataRef reference to DcmDspData container
      in the DID.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 31. DcmDspDidInfo

**描述**: This container contains the configuration (parameters) of the DID's Info

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidDynamicallyDefined
  长名称: ''
  描述: Indicates if this DID can be dynamically defined
  默认值: ''
  最小值: ''
  最大值: ''
```

### 32. DcmDspDidAccess

**描述**: This container contains the configuration (parameters) of the DID access

该容器没有参数。

### 33. DcmDspDidControl

**描述**: This container contains the configuration (parameters) of the DID control.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidFreezeCurrentState
  长名称: ''
  描述: <b>This indicates the presence of "FreezeCurrentState".</b>
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDidResetToDefault
  长名称: ''
  描述: <b>This indicates the presence of "ResetToDefault".</b>
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspDidReturnControlToEcu
  长名称: ''
  描述: <b>This indicates the presence of "ReturnControlToEcu".</b>
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspDidShortTermAdjustment
  长名称: ''
  描述: This indicates the presence of "ShortTermAdjustment".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 34. DcmDspDidRead

**描述**: This container contains the configuration (parameters) of the DID read.

该容器没有参数。

### 35. DcmDspDidWrite

**描述**: This container contains the configuration (parameters) of the DID write.

该容器没有参数。

### 36. DcmDspDidRange

**描述**: This container defines the DID Range

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspDidRangeHasGaps
  长名称: ''
  描述: Parameter specifying if there are gaps in the DID range (parameter set to TRUE) or not
      (parameter set to FALSE)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspDidRangeIdentifierLowerLimit
  长名称: ''
  描述: Lower limit of DID range.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspDidRangeIdentifierUpperLimit
  长名称: ''
  描述: Upper limit of DID range.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: DcmDspDidRangeIsDidAvailableFnc
  长名称: ''
  描述: Function name to request from application if a specific DID is available within the range or
      not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmDspDidRangeMaxDataLength
  长名称: ''
  描述: Maximum data length in bytes
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: DcmDspDidRangeReadDidFnc
  长名称: ''
  描述: Function name to request from application the data range value of a DID.(ReadData-function).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDspDidRangeUsePort
  长名称: ''
  描述: When the parameter DcmDspDidRangeUsePort is set to true the DCM will access the Data using an
      R-Port requiring a PortInteface DataServices_DIDRange. In that case,
      DcmDspDidRangeIsDidAvailableFnc, DcmDspDidRangeReadDidFnc and DcmDspDidRangeWriteDidFnc
      are ignored and the RTE APIs are used. When the parameter DcmDspDidRangeUsePort is
      false, the DCM calls the functions defined in DcmDspDidRangeIsDidAvailableFnc,
      DcmDspDidRangeReadDidFnc and DcmDspDidRangeWriteDidFnc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmDspDidRangeWriteDidFnc
  长名称: ''
  描述: Function name to request application to write the data range value of a
      DID.(WriteData-function).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 37. DcmDspMemory

**描述**: This container contains the configuration of the memory access.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspUseMemoryId
  长名称: ''
  描述: If this parameter is set to false, the DCM will not use MemoryIdentifier parameter.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 38. DcmDspMemoryIdInfo

**描述**: Provides the value of memory identifier used to select the desired memory device

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspMemoryIdValue
  长名称: ''
  描述: Value of the memory device identifer used. This parameter is only relevant if the memory Id
      parameter use is enabled. (DcmDspUseMemoryId = TRUE)
  默认值: ''
  最小值: 0
  最大值: 255
```

### 39. DcmDspReadMemoryRangeInfo

**描述**: Provides the range of memory address allowed for reading

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspReadMemoryRangeHigh
  长名称: ''
  描述: High memory address of a range allowed for reading
  默认值: ''
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: DcmDspReadMemoryRangeLow
  长名称: ''
  描述: Low memory address of a range allowed for reading
  默认值: ''
  最小值: 0
  最大值: 4294967294
```

### 40. DcmDspWriteMemoryRangeInfo

**描述**: Provides the range of memory address allowed for writting.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspWriteMemoryRangeHigh
  长名称: ''
  描述: High memory address of a range allowed for writting.
  默认值: ''
  最小值: 0
  最大值: 4294967294
- 
  序号: 2
  名称: DcmDspWriteMemoryRangeLow
  长名称: ''
  描述: Low memory address of a range allowed for writting
  默认值: ''
  最小值: 0
  最大值: 4294967294
```

### 41. DcmDspPid

**描述**: This container defines the availability of a PID to the DCM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidIdentifier
  长名称: ''
  描述: 1 byte Identifier of the PID
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspPidService
  长名称: ''
  描述: Allow to indicate if this PID is used for service $01 or/and $02.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspPidSize
  长名称: ''
  描述: Length of the PID in byte.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DcmDspPidUsed
  长名称: ''
  描述: Allow to activate or deactivate the usage of a PID, for multi  purpose ECUs
  默认值: ''
  最小值: ''
  最大值: ''
```

### 42. DcmDspPidData

**描述**: This container defines the parameter for a Signal in the PID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataPos
  长名称: ''
  描述: This is the position in bit of the PID structure and will not start at position 0 in case a
      support information is availabe (for bit-mapped PIDs).
  默认值: ''
  最小值: 0
  最大值: 2040
- 
  序号: 2
  名称: DcmDspPidDataSize
  长名称: ''
  描述: Length of data associated to the PID in bit.
  默认值: ''
  最小值: 0
  最大值: 2040
```

### 43. DcmDspPidDataSupportInfo

**描述**: This container defines the supported information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataSupportInfoBit
  长名称: ''
  描述: referenced Bit of the SupportInfo
  默认值: ''
  最小值: 0
  最大值: 255
```

### 44. DcmDspPidService01

**描述**: Contains specific configuration parameter of PID for service $01. This container exists only if
DcmDspPidService is set to DCM_SERVICE_01 or DCM_SERVICE_01_02.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidDataReadFnc
  长名称: ''
  描述: Function name for reading PID data value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspPidDataUsePort
  长名称: ''
  描述: If this parameter is set to USE_DATA_SYNCH_FNC, the DCM will use the function defined in
      DcmDspPidDataReadFnc to get the PID data value.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 45. DcmDspPidService02

**描述**: Contains specific configuration parameter of PID for service $02. This container exists only if
DcmDspPidService is set to DCM_SERVICE_02 or DCM_SERVICE_01_02.

该容器没有参数。

### 46. DcmDspPidSupportInfo

**描述**: This container defines the support information (typically byte A) to declare the usability of the
data bytes within the so-called bit-mapped PIDs (e.g. PID$68).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspPidSupportInfoLen
  长名称: ''
  描述: Length of the supported information in bytes.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspPidSupportInfoPos
  长名称: ''
  描述: Position of the supported information in bytes.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 47. DcmDspRequestControl

**描述**: This container contains the configuration (parameters) of the "Request control of on-board system,
test or component" service (Service $08).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRequestControlInBufferSize
  长名称: ''
  描述: ''
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: DcmDspRequestControlOutBufferSize
  长名称: ''
  描述: ''
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: DcmDspRequestControlTestId
  长名称: ''
  描述: Test Id for Service $08
  默认值: ''
  最小值: 0
  最大值: 255
```

### 48. DcmDspRoe

**描述**: Provide the configuration of the ResponseOnEvent mechanism.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoeBufSize
  长名称: ''
  描述: Size of the buffer used to managed internally the subservice OnChangeOfDataIdentifier of
      ResponseOnEvent Service.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoeInitFnc
  长名称: ''
  描述: Function name to initialize an ROE event managed externally.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspRoeInitOnDSC
  长名称: ''
  描述: If set to TRUE the ROE functionality is re-initialized on reception of service
      DiagnosticSessionControl.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoeInterMessageTime
  长名称: ''
  描述: Provide the minimum time in ms between two transmissions of ROE event. It is used for the
      delay between two different consecutive Roe transmissions and between two transmissions
      of the retry mechanism.
  默认值: ''
  最小值: 0
  最大值: 5000
- 
  序号: 5
  名称: DcmDspRoeMaxEventLength
  长名称: ''
  描述: Provide the max size in byte of an ROE message that will be stored in the ROE transmission
      queue.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DcmDspRoeMaxNumberOfRetry
  长名称: ''
  描述: Provide the max number of re-transmission of an ROE event in case of transmission failure.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: DcmDspRoeMaxQueueLength
  长名称: ''
  描述: Provide the max number of element in the ROE transmission queue.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 8
  名称: DcmDspRoeQueueEnabled
  长名称: ''
  描述: If set to TRUE, the ROE queue mechanism is enabled on DCM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspRoeStopFnc
  长名称: ''
  描述: Function name to stop an ROE event managed externally.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 49. DcmDspRoutine

**描述**: This container contains the configuration (parameters) for Routines

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRequestResultsRoutineFnc
  长名称: ''
  描述: Function name for request to application the results of a routine.
      (Routine_RequestResults-function)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspRequestResultsRoutineSupported
  长名称: ''
  描述: Indicates if the optional requestRoutineResults in the RoutineControl is supported
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspRoutineFixedLength
  长名称: ''
  描述: Indicates if the datalength of the optional record in the RoutineControl request and response
      is fixed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmDspRoutineIdentifier
  长名称: ''
  描述: 2 bytes Identifier of the RID
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DcmDspRoutineUsePort
  长名称: ''
  描述: If this parameter is set to true, the DCM uses a port requiring a PortInterface
      RoutineServices_<ROUTINENAME>.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DcmDspRoutineUsed
  长名称: ''
  描述: Allow to activate or deactivate the usage of a Routine, for multi  purpose ECUs
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DcmDspStartRoutineFnc
  长名称: ''
  描述: Function name for request to application to start a routine. (Routine_Start-function)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DcmDspStopRoutineFnc
  长名称: ''
  描述: Function name for request to application to stop a routine. (Routine_Stop-function)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DcmDspStopRoutineSupported
  长名称: ''
  描述: Indicates if the optional stopRoutine in the RoutineControl is supported
  默认值: ''
  最小值: ''
  最大值: ''
```

### 50. DcmDspRoutineInfo

**描述**: This container contains the configuration (parameters) for Routine's Info.

该容器没有参数。

### 51. DcmDspRoutineAuthorization

**描述**: This container contains the configuration (parameters) for the Routine Authorization.

该容器没有参数。

### 52. DcmDspRoutineRequestResOut

**描述**: Provide description of output parameter of RequestResult subservice for RoutineControl service.

该容器没有参数。

### 53. DcmDspRoutineRequestResOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: Provide the length in bits of the signal in the RoutineControl request/response
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: Provide the position of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: Provide the type of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 54. DcmDspRoutineStopIn

**描述**: Provide description of input parameter of Stop subservice for RoutineControl service.

该容器没有参数。

### 55. DcmDspRoutineStopInSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: Provide the length in bits of the signal in the RoutineControl request/response
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: Provide the position of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: Provide the type of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 56. DcmDspRoutineStopOut

**描述**: Provide description of output parameter of Stop subservice for RoutineControl service.

该容器没有参数。

### 57. DcmDspRoutineStopOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: Provide the length in bits of the signal in the RoutineControl request/response
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: Provide the position of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: Provide the type of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 58. DcmDspStartRoutineIn

**描述**: Provide description of input parameter of Start subservice for RoutineControl service

该容器没有参数。

### 59. DcmDspStartRoutineInSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: Provide the length in bits of the signal in the RoutineControl request/response
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: Provide the position of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: Provide the type of the signal in the RoutineControl  request/response.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 60. DcmDspStartRoutineOut

**描述**: Provide description of output parameter of Start subservice for RoutineControl service.

该容器没有参数。

### 61. DcmDspStartRoutineOutSignal

**描述**: Provide description of a routine signal used in RoutineControl service.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspRoutineSignalLength
  长名称: ''
  描述: Provide the length in bits of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DcmDspRoutineSignalPos
  长名称: ''
  描述: Provide the position of the signal in the RoutineControl request/response.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DcmDspRoutineSignalType
  长名称: ''
  描述: Provide the type of the signal in the RoutineControl  request/response.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 62. DcmDspSecurity

**描述**: This container contains the configuration ( DSP parameter) for security level configuration (per
security level)

该容器没有参数。

### 63. DcmDspSecurityRow

**描述**: Definition of a single Row of configuration for security level configuration (per security level)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSecurityADRSize
  长名称: ''
  描述: Size of the AccessDataRecord used in GetSeed
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: DcmDspSecurityDelayTime
  长名称: ''
  描述: Delay time after failed security access (in ms). This is started after
      DcmDspSecurityNumAttDelay number of failed security accesses.
  默认值: ''
  最小值: 0
  最大值: 20000
- 
  序号: 3
  名称: DcmDspSecurityDelayTimeOnBoot
  长名称: ''
  描述: Start delay timer on power on (in ms)
  默认值: ''
  最小值: 0
  最大值: 20000
- 
  序号: 4
  名称: DcmDspSecurityKeySize
  长名称: ''
  描述: size of the security key (in Bytes).
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 5
  名称: DcmDspSecurityLevel
  长名称: ''
  描述: Value of Security level.
  默认值: ''
  最小值: 1
  最大值: 63
- 
  序号: 6
  名称: DcmDspSecurityNumAttDelay
  长名称: ''
  描述: Number of failed security accesses after which the delay time is activated
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: DcmDspSecuritySeedSize
  长名称: ''
  描述: size of the security seed (in Bytes).
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 64. DcmDspSession

**描述**: This container contains the configuration ( DSP parameter) session control configuration (per
session control)

该容器没有参数。

### 65. DcmDspSessionRow

**描述**: Definition of a single Row of session control configuration (per session control)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspSessionForBoot
  长名称: ''
  描述: This parameter defines whether this diagnostic session allows to jump to Bootloader (OEM
      Bootloader or System Supplier Bootloader). If this diagnostic session doesn't allow to
      jump to Bootloader the value DCM_NO_BOOT shall be chosen.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmDspSessionLevel
  长名称: ''
  描述: Value of the Session control. The symbolicName represents the Name of the Session
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DcmDspSessionP2ServerMax
  长名称: ''
  描述: This is the session value for P2ServerMax in milliseconds (per Session Control).
  默认值: ''
  最小值: 0
  最大值: 1000
- 
  序号: 4
  名称: DcmDspSessionP2StarServerMax
  长名称: ''
  描述: This is the session value for P2*ServerMax in milliseconds (per Session Control).
  默认值: ''
  最小值: 0
  最大值: 100000
```

### 66. DcmDspTestResultByObdmid

**描述**: This container contains the configuration (parameters) of the "Request on-board monitoring test
results" service (Service $06).

该容器没有参数。

### 67. DcmDspTestResultObdmidTid

**描述**: This container contains the configuration (parameters) of a OBDMID and the assigned TIDs for the
"Request on-board monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultObdmid
  长名称: ''
  描述: OBDMID for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
```

### 68. DcmDspTestResultObdmidTids

**描述**: This container contains the configuration (parameters) of the TIDs belonging to the OBDMID for the
"Request on-board monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultObdmidTidUaSid
  长名称: ''
  描述: Unit And Scaling ID for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
```

### 69. DcmDspTestResultTid

**描述**: This container contains the configuration (parameters) of a single TID for the "Request on-board
monitoring test results" service (Service $06).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspTestResultTestId
  长名称: ''
  描述: Test Id for Service $06
  默认值: ''
  最小值: 0
  最大值: 255
```

### 70. DcmDspVehInfo

**描述**: This container contains the configuration (parameters) of the "Request vehicle information service"
(service $09).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspVehInfoInfoType
  长名称: ''
  描述: value of InfoType.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 71. DcmDspVehInfoData

**描述**: Data Item of an InfoType; post-fix of the port interface name.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDspVehInfoDataOrder
  长名称: ''
  描述: Defines the order of the data item in the InfoType; values: 0..255; first data item having the
      order number 0; the next 1 and so on.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DcmDspVehInfoDataReadFnc
  长名称: ''
  描述: Function name for reading InfoType data item.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmDspVehInfoDataSize
  长名称: ''
  描述: Size in bytes of the InfoType data item.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DcmDspVehInfoDataUsePort
  长名称: ''
  描述: When the parameter DcmDspVehInfoUsePort is set to true the DCM will access the Data using an
      R-Port requiring a PortInteface InfotypeServices_<VEHINFODATA>. The R-Port is named
  默认值: ''
  最小值: ''
  最大值: ''
```

### 72. DcmGeneral

**描述**: This container contains the configuration (parameters) for Component wide parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmDevErrorDetect
  长名称: ''
  描述: Preprocessor switch to enable or disable the Development Error Detection (DET) mechanism.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmRequestManufacturerNotificationEnabled
  长名称: ''
  描述: Allows to enable or disable the requested notification mechanism for the Manufacturer.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DcmRequestSupplierNotificationEnabled
  长名称: ''
  描述: Allows to enable or disable the requested notification mechanism for the Supplier.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DcmRespondAllRequest
  长名称: ''
  描述: If set to FALSE the DCM will not respond to diagnostic request  that contains a service ID
      which is in the range from 0x40 to 0x7F or in the  range from 0xC0 to 0xFF (Response
      IDs).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DcmTaskTime
  长名称: ''
  描述: Allow to configure the time for the periodic cyclic task. Please note: This configuration
      value shall be equal to the value in the ScheduleManager module.
  默认值: ''
  最小值: 0
  最大值: 100
- 
  序号: 6
  名称: DcmVersionInfoApi
  长名称: ''
  描述: Preprocessor switch to enable or disable the output Version info of the functionality.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 73. DcmPageBufferCfg

**描述**: This container contains the configuration (parameters) for Page Buffer handling

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmPagedBufferEnabled
  长名称: ''
  描述: Allow to enable or disable the Page buffer mechanism.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmPagedBufferTimeout
  长名称: ''
  描述: Allow to configure the Timeout (in ms) towards the application for filling the next page.
  默认值: ''
  最小值: 0
  最大值: 1000
```

### 74. DcmProcessingConditions

**描述**: This container contains the configuration ( DSP parameter) for mode arbitration functionality of the
Dcm

该容器没有参数。

### 75. DcmModeCondition

**描述**: This container contains the configuration of a mode condition which can be used as argument in
DcmModeRules.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmConditionType
  长名称: ''
  描述: This parameter specifies what kind of comparison that is made for the evaluation of the mode
      condition.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 76. DcmModeRule

**描述**: This container contains the configuration of a mode rule which represents a logical expression with
DcmModeCondistions or other DcmModeRules as arguments.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DcmLogicalOperator
  长名称: ''
  描述: This parameter specifies the logical operator to be used in the logical expression. If the
      expression only consists of a single condition this parameter shall not be used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DcmModeRuleNrcValue
  长名称: ''
  描述: Optional parameter which defines the NRC to be sent in case the mode rule condition is not
      valid.
  默认值: ''
  最小值: 0
  最大值: 255
```

