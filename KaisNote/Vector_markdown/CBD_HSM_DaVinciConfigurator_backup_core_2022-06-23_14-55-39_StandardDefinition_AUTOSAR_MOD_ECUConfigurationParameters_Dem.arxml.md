# Dem

## 模块描述

Configuration of the Dem (Diagnostic Event Manager) module.

## 容器列表

### 1. DemConfigSet

**描述**: This container contains the configuration parameters and sub containers of the Dem module supporting
multiple configuration sets. This container is a MultipleConfigurationContainer, i.e. this container
and its sub-containers exist once per configuration set.

该容器没有参数。

### 2. DemDTCClass

**描述**: This container contains the configuration (parameters) for DTCClass.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDTCFunctionalUnit
  长名称: ''
  描述: DTCFuncitonalUnit is a 1-byte value which identifies the corresponding basic vehicle / system
      function which reports the DTC. This parameter is necessary for the report of severity
      information.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemDTCSeverity
  长名称: ''
  描述: DTC severity according to ISO 14229-1. This parameter depends on the automotive manufacturer.
  默认值: DEM_DTC_SEV_NO_SEVERITY
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemImmediateNvStorage
  长名称: ''
  描述: Switch to enable immediate storage triggering of an according event memory entriy persistently
      to NVRAM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemJ1939DTC
  长名称: ''
  描述: Unique Diagnostic Trouble Code value for J1939 (consiting of SPN and FMI)
  默认值: ''
  最小值: 1
  最大值: 16777214
- 
  序号: 5
  名称: DemObdDTC
  长名称: ''
  描述: Unique Diagnostic Trouble Code value for OBD
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DemUdsDTC
  长名称: ''
  描述: Unique Diagnostic Trouble Code value for UDS
  默认值: ''
  最小值: 1
  最大值: 16777214
```

### 3. DemCallbackInitMForF

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackInitMForFFnc
  长名称: ''
  描述: Function name of prototype "InitMonitorForFunction".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. DemDtr

**描述**: This container holds the configuration of one individual DTR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDtrCompuDenominator0
  长名称: ''
  描述: Part of the conversion between the binary representation and the physical meaning analogous to
      the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1
      denominator coefficient in the direction compuInternalToPhys.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemDtrCompuNumerator0
  长名称: ''
  描述: Part of the conversion between the binary representation and the physical meaning analogous to
      the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1
      denominator coefficient in the direction compuInternalToPhys.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemDtrCompuNumerator1
  长名称: ''
  描述: Part of the conversion between the binary representation and the physical meaning analogous to
      the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1
      denominator coefficient in the direction compuInternalToPhys.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemDtrId
  长名称: ''
  描述: The index identifier value assigned to this DTR. The value is generated during the Dem
      configuration process.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DemDtrMid
  长名称: ''
  描述: The OBDMID of the DTR.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DemDtrTid
  长名称: ''
  描述: The OBDTID of the DTR.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: DemDtrUasid
  长名称: ''
  描述: The UaSId the DTR data shall be scaled to, and reported together with the rescaled DTR data.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: DemDtrUpdateKind
  长名称: ''
  描述: Update conditions applied by the Dem to reports of DTR values. Only supported if a related
      Event is configured. If no related Event is configured, the Dem behaves as if
      DemDtrUpdateKind is configured to "DEM_DTR_UPDATE_ALWAYS".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. DemEventParameter

**描述**: This container contains the configuration (parameters) for events.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemEventAvailable
  长名称: ''
  描述: This parameter configures an Event as unavailable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemEventId
  长名称: ''
  描述: Unique identifier of a diagnostic event.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: DemEventKind
  长名称: ''
  描述: This parameter is used to distinguish between SW-C and BSW events. SW-C events are reported by
      Dem_SetEventStatus API and BSW events are reported by Dem_ReportErrorStatus API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemMaxNumberFreezeFrameRecords
  长名称: ''
  描述: This parameter defines the number of according freeze frame records, which can maximal be
      stored for this event. Therefore all these freeze frame records have the same freeze
      frame class.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. DemCallbackClearEventAllowed

**描述**: The presence of this container indicates that the Dem has access to a "ClearEventAllowed" callback.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackClearEventAllowedFnc
  长名称: ''
  描述: Function name of prototype "ClearEventAllowed".
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemClearEventAllowedBehavior
  长名称: ''
  描述: Defines the resulting UDS status byte for the related event, which must not be cleared
      according to the ClearEventAllowed callback.
  默认值: DEM_NO_STATUS_BYTE_CHANGE
  最小值: ''
  最大值: ''
```

### 7. DemCallbackEventDataChanged

**描述**: The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackEventDataChangedFnc
  长名称: ''
  描述: Function name of prototype "EventDataChanged"
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. DemCallbackEventStatusChanged

**描述**: The presence of this container indicates, that the Dem has access to an "EventStatusChanged"
callback, which the Dem will call to notify other components about the change in the status of an
event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackEventStatusChangedFnc
  长名称: ''
  描述: Function name of prototype "EventStatusChanged"
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. DemCallbackInitMForE

**描述**: The presence of this container indicates, that the Dem has access to an "InitMonitorForEvent"
callback, which the Dem will call to initialize a monitor.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackInitMForEFnc
  长名称: ''
  描述: Function name of prototype "InitMonitorForEvent".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. DemEventClass

**描述**: This container contains the configuration (parameters) for EventClass

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemAgingAllowed
  长名称: ''
  描述: Switch to allow aging/unlearning of the event or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemAgingCycleCounterThreshold
  长名称: ''
  描述: Number of aging cycles needed to unlearn/delete the event.
  默认值: ''
  最小值: 1
  最大值: 256
- 
  序号: 3
  名称: DemConsiderPtoStatus
  长名称: ''
  描述: This parameter is TRUE, when the event is affected by the Dem PTO handling.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemEventDestination
  长名称: ''
  描述: The event destination assigns events to none, one or multiple origins.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemEventFailureCycleCounterThreshold
  长名称: ''
  描述: Defines the number of failure cycles for the event based fault confirmation.
  默认值: ''
  最小值: 1
  最大值: 256
- 
  序号: 6
  名称: DemEventMemoryEntryFdcThresholdStorageValue
  长名称: ''
  描述: Threshold to allocate an event memory entry and to capture the Freeze Frame.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: DemEventOBDReadinessGroup
  长名称: ''
  描述: This parameter specifies the Event OBD Readiness group for PID $01 and PID $41 computation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemEventPriority
  长名称: ''
  描述: Priority of the event, in view of full event buffer.
  默认值: ''
  最小值: 1
  最大值: 256
- 
  序号: 9
  名称: DemEventSignificance
  长名称: ''
  描述: Significance of the event, which indicates additional information concerning fault
      classification and resolution.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemFFPrestorageSupported
  长名称: ''
  描述: If this parameter is set to true, then the Prestorage of FreezeFrames is supported by the
      assigned event. This parameter is useful to calculate the buffer size.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. DemDebounceCounterBased

**描述**: This container contains the configuration (parameters) for counter based debouncing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDebounceBehavior
  长名称: ''
  描述: This parameter defines how the event debounce algorithm will behave, if a related enable
      condition is not fulfilled or ControlDTCSetting of the related event is disabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemDebounceCounterDecrementStepSize
  长名称: ''
  描述: Defines the step size for decrementation of the internal debounce counter (PREPASSED).
  默认值: ''
  最小值: 1
  最大值: 32768
- 
  序号: 3
  名称: DemDebounceCounterFailedThreshold
  长名称: ''
  描述: Defines the value of the internal debounce counter, which indicates the failed status.
  默认值: ''
  最小值: 1
  最大值: 32767
- 
  序号: 4
  名称: DemDebounceCounterIncrementStepSize
  长名称: ''
  描述: Defines the step size for incrementation of the internal debounce counter (PREFAILED).
  默认值: ''
  最小值: 1
  最大值: 32767
- 
  序号: 5
  名称: DemDebounceCounterJumpDown
  长名称: ''
  描述: Switch for the activation of Jump-Down.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemDebounceCounterJumpDownValue
  长名称: ''
  描述: Jump-Down value of the internal debounce counter which is taken as initialization value for
      the counter when the respective step-down occurs.
  默认值: 0
  最小值: -32768
  最大值: 32767
- 
  序号: 7
  名称: DemDebounceCounterJumpUp
  长名称: ''
  描述: Switch for the activation of Jump-Up.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemDebounceCounterJumpUpValue
  长名称: ''
  描述: Jump-Up value of the internal debounce counter which is taken as initialization value for the
      counter when the respective step-up occurs.
  默认值: 0
  最小值: -32768
  最大值: 32767
- 
  序号: 9
  名称: DemDebounceCounterPassedThreshold
  长名称: ''
  描述: Defines the value of the internal debounce counter, which indicates the passed status.
  默认值: ''
  最小值: -32768
  最大值: -1
- 
  序号: 10
  名称: DemDebounceCounterStorage
  长名称: ''
  描述: Switch to store the debounce counter value non-volatile or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. DemDebounceMonitorInternal

**描述**: This container contains the configuration (parameters) for monitor internal debouncing.

该容器没有参数。

### 13. DemCallbackGetFDC

**描述**: The presence of this container indicates, that the Dem has access to a "GetFaultDetectionCounter"
callback, which the Dem will call to obtain the value of the fault detection counter.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackGetFDCFnc
  长名称: ''
  描述: Function name of prototype "GetFaultDetectionCounter".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. DemDebounceTimeBase

**描述**: This container contains the configuration (parameters) for time based debouncing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDebounceBehavior
  长名称: ''
  描述: This parameter defines how the event debounce algorithm will
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemDebounceTimeFailedThreshold
  长名称: ''
  描述: Defines the time out duration for "Event Failed" qualification.
  默认值: ''
  最小值: 0.001
  最大值: 3600
- 
  序号: 3
  名称: DemDebounceTimePassedThreshold
  长名称: ''
  描述: Defines the time out duration for "Event Passed" qualification.
  默认值: ''
  最小值: 0.001
  最大值: 3600
```

### 15. DemIndicatorAttribute

**描述**: This container contains the event specific configuration of Indicators.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIndicatorBehaviour
  长名称: ''
  描述: Behaviour of the linked indicator
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemIndicatorFailureCycleCounterThreshold
  长名称: ''
  描述: Defines the number of failure cycles for the WarningIndicatorOnCriteria.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DemIndicatorFailureCycleSource
  长名称: ''
  描述: This parameter defines, which failure cycle is used for the WarningIndicatorOnCriteria
      handling.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemIndicatorHealingCycleCounterThreshold
  长名称: ''
  描述: Defines the number of healing cycles for the WarningIndicatorOffCriteria.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 16. DemJ1939NodeAddress

**描述**: Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

该容器没有参数。

### 17. DemPidClass

**描述**: This container contains the different PIDs for the single global OBD relevant freeze frame class. It
is assembled out of one or several data elements.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemPidIdentifier
  长名称: ''
  描述: identifier of the PID
  默认值: ''
  最小值: 0
  最大值: 255
```

### 18. DemPidDataElement

**描述**: This container contains the different data elements contained in the specific PID.

该容器没有参数。

### 19. DemGeneral

**描述**: This container contains the configuration (parameters) of the BSW Dem

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemAgingCycleCounterProcessing
  长名称: ''
  描述: This configuration switch defines, whether the aging counter is calculated Dem-internally or
      provided via Dem_SetAgingCycleCounterValue.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemAgingRequieresTestedCycle
  长名称: ''
  描述: Defines if the aging cycle counter is processed every aging cycles or if only tested aging
      cycle are considered.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemAvailabilitySupport
  长名称: ''
  描述: This configuration switch defines, whether support for availability is enabled or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemBswErrorBufferSize
  长名称: ''
  描述: Maximum number of elements in buffer for handling of BSW errors (ref. to Dem107).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: DemClearDTCBehavior
  长名称: ''
  描述: Defines the clearing process of diagnostic information for volatile and non-volatile memory
      and the positive response handling for the Dcm module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemClearDTCLimitation
  长名称: ''
  描述: Defines the supported Dem_<...>ClearDTC API scope.
  默认值: DEM_ALL_SUPPORTED_DTCS
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemDataElementDefaultEndianness
  长名称: ''
  描述: Defines the default endianness of the data belonging to a data element which is applicable if
      the DemExternalSRDataElementClass does not define a endianness.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemDebounceCounterBasedSupport
  长名称: ''
  描述: This configuration switch defines, whether support for counter based debouncing is enabled or
      not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemDebounceTimeBasedSupport
  长名称: ''
  描述: This configuration switch defines, whether support for time based debouncing is enabled or
      not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemDevErrorDetect
  长名称: ''
  描述: Activate/Deactivate the Development Error Detection and Notification.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DemDtcStatusAvailabilityMask
  长名称: ''
  描述: Mask for the supported DTC status bits by the Dem. This mask is used by UDS service 0x19.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: DemEnableConditionSupport
  长名称: ''
  描述: This configuration switch defines, whether support for enable conditions is enabled or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DemEventCombinationSupport
  长名称: ''
  描述: This parameter defines the type of event combination supported by the Dem.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DemEventDisplacementStrategy
  长名称: ''
  描述: This configuration switch defines, whether support for event displacement is enabled or not,
      and which displacement strategy is followed.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DemEventMemoryEntryStorageTrigger
  长名称: ''
  描述: Configures the primary trigger to allocate an event memory entry.
  默认值: DEM_STORAGE_ON_TEST_FAILED
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DemExtendedDataCapture
  长名称: ''
  描述: This parameter defines the point in time, when the extended data collection is done for the
      initial event memory entry.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DemFreezeFrameCapture
  长名称: ''
  描述: This parameter defines the point in time, when the freeze frame data collection is done for
      the initial event memory entry.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DemGeneralInterfaceSupport
  长名称: ''
  描述: The interfaces GeneralEvtInfo, GeneralCallbackEventDataChanged and
      GeneralCallbackEventStatusChange are provided if DemGeneralInterfaceSupport is equal to
      true.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: DemHeaderFileInclusion
  长名称: ''
  描述: Name of the header file(s) to be included by the Dem module containing the used C-callback
      declarations.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DemImmediateNvStorageLimit
  长名称: ''
  描述: This parameter defines the maximum number of occurrences, a specific event memory entry is
      allowed, to be stored in NVRAM immediately (refer to DemImmediateNvStorage).
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 21
  名称: DemMaxNumberEventEntryMirror
  长名称: ''
  描述: Maximum number of events which can be stored in the mirror memory
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: DemMaxNumberEventEntryPermanent
  长名称: ''
  描述: Maximum number of events which can be stored in the permanent memory.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: DemMaxNumberEventEntryPrimary
  长名称: ''
  描述: Maximum number of events which can be stored in the primary memory
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 24
  名称: DemMaxNumberEventEntrySecondary
  长名称: ''
  描述: Maximum number of events which can be stored in the secondary memory
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 25
  名称: DemMaxNumberPrestoredFF
  长名称: ''
  描述: Defines the maximum number for prestored freeze frames.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 26
  名称: DemOBDSupport
  长名称: ''
  描述: This configuration switch defines OBD support and kind of OBD ECU.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: DemOccurrenceCounterProcessing
  长名称: ''
  描述: This configuration switch defines the consideration of the fault confirmation process for the
      occurrence counter. For OBD and mixed systems (OBD/non OBD, refer to DemOBDSupport)
      configuration switch shall always set to DEM_PROCESS_OCCCTR_TF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: DemOperationCycleProcessing
  长名称: ''
  描述: This configuration switch defines, whether the operation cycles are triggered by
      DEM_CYCLE_STATE_START or collecting an external counter value, which results in
      respective state changes.
  默认值: DEM_PROCESS_OPCYC_STATE
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: DemOperationCycleStatusStorage
  长名称: ''
  描述: Defines if the operation cycle state is available over the power cycle (stored non-volatile)
      or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: DemPTOSupport
  长名称: ''
  描述: This configuration switch defines, whether PTO support (and therefore PID $1E support) is
      enabled or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: DemResetConfirmedBitOnOverflow
  长名称: ''
  描述: This configuration switch defines, whether the confirmed bit is reset or not while an event
      memory entry will be displaced.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: DemStatusBitHandlingTestFailedSinceLastClear
  长名称: ''
  描述: This configuration switch defines, whether the aging and displacement mechanism shall be
      applied to the "TestFailedSinceLastClear" status bits.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: DemStatusBitStorageTestFailed
  长名称: ''
  描述: Activate/Deactivate the permanent storage of the "TestFailed" status bits.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: DemStorageConditionSupport
  长名称: ''
  描述: This configuration switch defines, whether support for storage conditions is enabled or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 35
  名称: DemSuppressionSupport
  长名称: ''
  描述: This configuration switch defines, whether support for suppression is enabled or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: DemTaskTime
  长名称: ''
  描述: Allow to configure the time for the periodic cyclic task. Please note: This configuration
      value shall be equal to the value in the Basic Software Scheduler configuration of the
      RTE module.
  默认值: ''
  最小值: 0.001
  最大值: 0.1
- 
  序号: 37
  名称: DemTriggerDcmReports
  长名称: ''
  描述: Activate/Deactivate the notification to the Diagnostic Communication Manager for ROE
      processing.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: DemTriggerDltReports
  长名称: ''
  描述: Activate/Deactivate the notification to the Diagnostic Log and Trace.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 39
  名称: DemTriggerFiMReports
  长名称: ''
  描述: Activate/Deactivate the notification to the Function Inhibition Manager.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: DemTriggerMonitorInitBeforeClearOk
  长名称: ''
  描述: Defines if the monitor re-initialization has to be triggered before or after the Dem module
      returns DEM_CLEAR_OK.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: DemTypeOfDTCSupported
  长名称: ''
  描述: This parameter defines the format returned by Dem_DcmGetTranslationType and does not relate
      to/influence the supported Dem functionality.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: DemTypeOfFreezeFrameRecordNumeration
  长名称: ''
  描述: This parameter defines the type of assigning freeze frame record numbers for event-specific
      freeze frame records.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 43
  名称: DemVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 20. DemAgingCycle

**描述**: Note that this container definition does not explicitly define a symbolic name parameter. Instead,
the short name of the container will be used in the Ecu Configuration Description to specify the
symbolic name of the aging cycle name. These aging cycles are reported via API
Dem_SetAgingCycleState only.

该容器没有参数。

### 21. DemCallbackDTCStatusChanged

**描述**: The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback,
which the Dem will call to notify other components about the change in the status of a DTC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackDTCStatusChangedFnc
  长名称: ''
  描述: Function name of prototype "DTCStatusChanged".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 22. DemExternalCSDataElementClass

**描述**: This container contains the configuration (parameters) for an external client/server based data
element class.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataElementDataSize
  长名称: ''
  描述: Defines the size of the data element in bytes.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemDataElementReadFnc
  长名称: ''
  描述: In case of DemDataElementUsePort is false, this parameter defines the prototype of the C
      function "ReadDataElement" used to get the according value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemDataElementUsePort
  长名称: ''
  描述: If the parameter is set to True, a R-Port is generated, to obtain the data element (interface
      DataServices_<SyncDataElement>).
  默认值: ''
  最小值: ''
  最大值: ''
```

### 23. DemExternalSRDataElementClass

**描述**: This container contains the configuration (parameters) for an external sender/receiver based data
element class. It defines, how the Dem can obtain the value of the data element from a SW-C, by
using a sender/receiver port.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataElementDataSize
  长名称: ''
  描述: Defines the size of the data element in bits.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemDataElementDataType
  长名称: ''
  描述: Provide the implementation data type of data belonging to a external data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemDataElementEndianness
  长名称: ''
  描述: Defines the endianness of the data belonging to an external data.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 24. DemAlternativeDataInterface

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of a VariableDataPrototoype in a DataInterface.

该容器没有参数。

### 25. DemAlternativeDataProps

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of ECU configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataTypeCategory
  长名称: ''
  描述: Data category of the alternative Diagnosis Representation.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 26. DemLinearScale

**描述**: This container contains the configuration (parameters) of an linear scale of the alternative
Diagnosis Representation.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataLowerRange
  长名称: ''
  描述: Lower Range for this scale of the data in the alternative Diagnosis Representation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemDiagnosisRepresentationDataOffset
  长名称: ''
  描述: Data offset of the alternative Diagnosis Representation for this scale.
  默认值: 0
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: DemDiagnosisRepresentationDataResolution
  长名称: ''
  描述: Data resolution of the alternative Diagnosis Representation for this scale.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: DemDiagnosisRepresentationDataUpperRange
  长名称: ''
  描述: Upper Range for this scale of the data in the alternative Diagnosis Representation.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 27. DemTextTableMapping

**描述**: This container contains the configuration (parameters) of the mapping a DataPrototype typed by
AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataValue
  长名称: ''
  描述: The data value in the diagnosis representation.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: DemInternalDataValue
  长名称: ''
  描述: The ECU internal data value.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 28. DemAlternativeDataType

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of an ApplicationDataType.

该容器没有参数。

### 29. DemTextTableMapping

**描述**: This container contains the configuration (parameters) of the mapping a DataPrototype typed by
AutosarDataType that refer to a CompuMethods of category TEXTTABLE or  SCALE_LINEAR_AND_TEXTTABLE.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataValue
  长名称: ''
  描述: The data value in the diagnosis representation.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: DemInternalDataValue
  长名称: ''
  描述: The ECU internal data value.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 30. DemDataElementInstance

**描述**: Instance Reference to the primitive data in a port  where the data element is typed with an
ApplicationPrimitveDataType or an ImplementationDataType.

该容器没有参数。

### 31. DemSubElementInDataElementInstance

**描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the
data element is typed with an ApplicationCompositeDataType.

该容器没有参数。

### 32. DemSubElementInImplDataElementInstance

**描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the
data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.

该容器没有参数。

### 33. DemInternalDataElementClass

**描述**: This container contains the configuration (parameters) for an internal data element class.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataElementDataSize
  长名称: ''
  描述: Defines the size of the data element in bytes.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemInternalDataElement
  长名称: ''
  描述: This parameter defines the Dem-internal data value, which is mapped to the data element.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 34. DemDidClass

**描述**: This container contains the configuration (parameters) for a data Id class. It is assembled out of
one or several data elements.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDidIdentifier
  长名称: ''
  描述: Identifier of the Data ID.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 35. DemEnableCondition

**描述**: This container contains the configuration (parameters) for enable conditions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemEnableConditionId
  长名称: ''
  描述: Defines a unique enable condition Id.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemEnableConditionStatus
  长名称: ''
  描述: Defines the initial status for enable or disable of acceptance of event reports of a
      diagnostic event.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 36. DemEnableConditionGroup

**描述**: This container contains the configuration (parameters) for enable condition groups.

该容器没有参数。

### 37. DemExtendedDataClass

**描述**: This class contains the combinations of extended data records for an extended data class.

该容器没有参数。

### 38. DemExtendedDataRecordClass

**描述**: This container contains the configuration (parameters) for an extended data record class.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemExtendedDataRecordNumber
  长名称: ''
  描述: This configuration parameter specifies an unique identifier for an extended data record.
  默认值: ''
  最小值: 0
  最大值: 253
- 
  序号: 2
  名称: DemExtendedDataRecordTrigger
  长名称: ''
  描述: Configures the primary trigger to allocate an event memory entry.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemExtendedDataRecordUpdate
  长名称: ''
  描述: This extended data record is captured if the configured trigger condition in
      "DemExtendedDataRecordTrigger" is fulfilled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 39. DemFreezeFrameClass

**描述**: This container contains the combinations of DIDs for a non OBD relevant freeze frame class.

该容器没有参数。

### 40. DemFreezeFrameRecNumClass

**描述**: This container contains a list of dedicated, different freeze frame record numbers assigned to an
event. The order of record numbers in this list is assigned to the chronological order of the
according freeze frame records.

该容器没有参数。

### 41. DemFreezeFrameRecordClass

**描述**: This container contains a list of dedicated, different freeze frame record numbers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemFreezeFrameRecordNumber
  长名称: ''
  描述: This parameter defines a record number for a freeze frame record. This record number is unique
      per freeze frame record number class.
  默认值: ''
  最小值: 1
  最大值: 254
- 
  序号: 2
  名称: DemFreezeFrameRecordTrigger
  长名称: ''
  描述: Configures the primary trigger to allocate an event memory entry.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemFreezeFrameRecordUpdate
  长名称: ''
  描述: This parameter defines the case, when the freeze frame record is stored/updated.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 42. DemGeneralJ1939

**描述**: This container contains the general J1939-specific configuration (parameters) of the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemJ1939ClearDtcSupport
  长名称: ''
  描述: This configuration switch defines whether clearing J1939 DTCs (DM3 und DM11) is supported or
      not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemJ1939Dm31Support
  长名称: ''
  描述: This configuration switch defines whether J1939 DM31 is supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemJ1939ExpandedFreezeFrameSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 expanded freeze frames are supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemJ1939FreezeFrameSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 freeze frames are supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemJ1939RatioSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 performance ratios are supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemJ1939Readiness1Support
  长名称: ''
  描述: This configuration switch defines whether J1939 diagnostic readiness 1 is supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemJ1939Readiness2Support
  长名称: ''
  描述: This configuration switch defines whether J1939 diagnostic readiness 2 is supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemJ1939Readiness3Support
  长名称: ''
  描述: This configuration switch defines whether J1939 diagnostic readiness 3 is supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemJ1939ReadingDtcSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 DTC readout is supported or not.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 43. DemCallbackJ1939DTCStatusChanged

**描述**: The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback,
which the Dem will call to notify other components about the change in the status of a DTC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackDTCStatusChangedFnc
  长名称: ''
  描述: Function name of prototype "DTCStatusChanged".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 44. DemJ1939FreezeFrameClass

**描述**: This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

该容器没有参数。

### 45. DemSPNClass

**描述**: This container contains the configuration (parameters) for a SPN.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemSPNId
  长名称: ''
  描述: Suspect parameter number
  默认值: ''
  最小值: 0
  最大值: 524287
```

### 46. DemGeneralOBD

**描述**: This container contains the general OBD-specific configuration (parameters) of the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemOBDCentralizedPID21Handling
  长名称: ''
  描述: Switch to enable the centralized handling of PID $21.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemOBDCentralizedPID31Handling
  长名称: ''
  描述: Switch to enable the centralized handling of PID $31.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemOBDCompliancy
  长名称: ''
  描述: Configuration value to define  the appropriate value to PID$1C "OBD requirements to which
      vehicle or engine is certified." according to the respective standards, e.g. OBD, OBDII,
      JOBD etc.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DemOBDDestinationOfEvents
  长名称: ''
  描述: The destination of events assigns where the OBD events shall be stored.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemOBDEventDisplacement
  长名称: ''
  描述: Activate/Deactivate a different displacement behavior for OBD events.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 47. DemCallbackOBDDTCStatusChanged

**描述**: The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback,
which the Dem will call to notify other components about the change in the status of a DTC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackDTCStatusChangedFnc
  长名称: ''
  描述: Function name of prototype "DTCStatusChanged".
  默认值: ''
  最小值: ''
  最大值: ''
```

### 48. DemGroupOfDTC

**描述**: This container contains the configuration (parameters) for DTC groups.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemGroupDTCs
  长名称: ''
  描述: DTC value of the selected group of DTC
  默认值: ''
  最小值: 0
  最大值: 16777214
```

### 49. DemIndicator

**描述**: This container contains the configuration (parameters) for Indicators.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIndicatorID
  长名称: ''
  描述: Unique identifier of an indicator.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 50. DemNvRamBlockId

**描述**: This container contains the configuration (parameters) for a non-volatile memory block, which is
used from the Dem. If no permanent storage of event memory entries is required, no block needs to be
configured.

该容器没有参数。

### 51. DemOperationCycle

**描述**: Note that this container definition does not explicitly define a symbolic name parameter. Instead,
the short name of the container will be used in the Ecu Configuration Description to specify the
symbolic name of the operation cycle name.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemOperationCycleAutomaticEnd
  长名称: ''
  描述: If DemOperationCycleAutomaticEnd is configured to TRUE, Dem shall automatically end the
      driving cycle at either Dem_Shutdown() or Dem_Init().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemOperationCycleAutostart
  长名称: ''
  描述: The autostart property defines if the operation cycles is automatically (re-)started during
      Dem_PreInit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemOperationCycleType
  长名称: ''
  描述: Operation cycles types for the Dem to be supported by cycle-state APIs.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 52. DemRatio

**描述**: This container contains the OBD-specific in-use-monitor performance ratio configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIUMPRDenGroup
  长名称: ''
  描述: This parameter specifies the assigned denominator type which is applied in addition to the
      General Denominator conditions.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemIUMPRGroup
  长名称: ''
  描述: This parameter specifies the assigned IUMPR group of the ratio Id.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemRatioId
  长名称: ''
  描述: Defines a unique ratio Id.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: DemRatioKind
  长名称: ''
  描述: This parameter defines whether the ratio will be calculated API or observer based.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 53. DemStorageCondition

**描述**: This container contains the configuration (parameters) for storage conditions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemStorageConditionId
  长名称: ''
  描述: Defines a unique storage condition Id. This parameter should not be changeable by user,
      because the Id should be generated by Dem itself to prevent gaps and multiple use of an
      Id. The storage conditions should be sequentially ordered beginning with 0 and no gaps
      in between.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemStorageConditionStatus
  长名称: ''
  描述: Defines the initial status for enable or disable of storage of a diagnostic event.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 54. DemStorageConditionGroup

**描述**: This container contains the configuration (parameters) for storage condition groups.

该容器没有参数。

### 55. DemClient

**描述**: This container contains possible clients that are using the Dem APIs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemClientId
  长名称: ''
  描述: Defines a unique identifier for a Dem client. This number is used by this client in the
      ClientID parameter in all API with this parameter.
  默认值: ''
  最小值: 0
  最大值: 255
```

