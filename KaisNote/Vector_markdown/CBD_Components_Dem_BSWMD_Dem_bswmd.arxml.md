# Dem

## 模块描述

Diagnostic Event Manager (DEM). Processes and stores diagnostic events and associated environmental
data. Provides the fault information to communication managers and SWCs.
#Diag #Diagnostics #UDS #OBD #WWHOBD
#AUTOSAR #ServiceComponent

## 容器列表

### 1. DemConfigSet

**描述**: This container groups the Diagnostic Monitor configuration setup. One such data set can be activated
during initialization in case of multiple configuration sets.

Currently only one configuration set is supported.

该容器没有参数。

### 2. DemDTCClass

**描述**: This container groups configuration options relating to the Diagnostic Trouble code (DTC) of a
monitor.

It is only valid if actually used by a monitor (see DemConfigSet/DemEventParameter/DemDTCClassRef).
Unused DTCClass containers are ignored.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDTCFunctionalUnit
  长名称: ''
  描述: |
    A 1-byte value which identifies the corresponding basic vehicle / system function which monitors
    this DTC.
    
    This parameter is necessary for the report of severity information and will be returned in UDS
    services $19 08 and  $19 09. If these services are not used, this parameter serves no use at
    all.
    This parameter has no further influence on the function of the Dem.
    If this parameter is not configured the value 0 is substituted, as required by AUTOSAR 4.3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemDTCSeverity
  长名称: ''
  描述: |
    DTC severity
    A missing configuration value (or parameter) is interpreted as NO_SEVERITY.
    
    The DTCSeverity byte according to ISO 14229-1 and J1979-2 consists of DTC severity and DTC class
    information (refer to DemWWHOBDDTCClass or DemOBDONUDSDTCClass) and is reported by UDS service
    $19 09 and can serve as a filter parameter for UDS services $19 07, $19 08, $19 42.
    
    This parameter has no further influence on the function of the Dem.
  默认值: DEM_DTC_SEV_NO_SEVERITY
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemImmediateNvStorage
  长名称: ''
  描述: |
    Select the write strategy for non-volatile storage of DTC related data.
    
    If enabled, environmental data for this DTC will be written to NV backing storage when it is
    stored or updated.
    If disabled, environmental data for this DTC will be persisted during shutdown.
    
    See also description of related parameters Dem/DemGeneral/DemImmediateNvStorageSupport and
    Dem/DemGeneral/DemImmediateNvStorageLimit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemJ1939DTC
  长名称: ''
  描述: |
    Unique Diagnostic Trouble Code value for J1939 (consisting of SPN and FMI).
    The Dem expects the SPN and FMI values of the J1939DTC to be configured
    according to the J1939 standard.
    
    For calculation of the SPN  the Dem uses Conversion Method 4 from SAE J1939-73 Specification.
  默认值: ''
  最小值: 1
  最大值: 16777214
- 
  序号: 5
  名称: DemObdDTC
  长名称: OBD II DTC
  描述: |
    Unique Diagnostic Trouble Code value for OBD II.
    
    This parameter is only valid if OBD II is supported (DemGeneral/DemOBDSupport == true and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_OBDII)
    If a DTC is OBD II relevant (i.e. has this DTC number configured) certain legislated
    restrictions apply to the DTC configuration. Please refer to the OBD legislation.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: DemUdsDTC
  长名称: ''
  描述: Unique Diagnostic Trouble Code value for UDS (DTC number).
  默认值: ''
  最小值: 1
  最大值: 16777214
- 
  序号: 7
  名称: DemWWHOBDDTCClass
  长名称: WWH OBD DTC Class
  描述: |
    CLASS_A: If a DTC with this class occur, it is assumed that the OBD threshold limits (OTL) are
    exceeded.
    CLASS_B1: A DTC with this class has the potential to lead to emissions above the OBD threshold
    limits.
    CLASS_B2: The malfunction is assumed to influence the emissions but not in a level exceeding the
    OBD threshold limits.
    CLASS_C: The DTC is assumed to influence the emissions but not in a level above the regulated
    emission limits.
    CLASS_NOCLASS: The DTC does not influence the emissions.
    
    Together with DemDTCSeverity, the DTC class forms the DTC severity byte according to ISO
    14229-1.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemFunctionalGroupIdentifier
  长名称: ''
  描述: |
    The identifier of the corresponding functional system group.
    Currently only support the identifier 0x33 for emissions-system group.
    
    
    If OBD II is supported (DemGeneral/DemOBDSupport == true and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_OBDII),
    this parameter is automatically derived from Dem/DemConfigSet/DemDTCClass/DemObdDTC and shall
    not be configured manually.
    
    If WWHOBD is supported (DemGeneral/DemOBDSupport == true and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_WWHOBD),
    this parameter is automatically derived from Dem/DemConfigSet/DemDTCClass/DemWWHOBDDTCClass and
    the Dem/DemConfigSet/DemEventParameter/DemOBDFreezeFrameClassRef of the referenced event and
    shall not be configured manually.
    
    If OBDonUDS is supported (DemGeneral/DemOBDSupport == true and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_OBD_ON_UDS),
    this parameter is not derived and must be configured manually.
    
    If ZEVonUDS is supported (DemGeneral/DemOBDSupport == true and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_ZEV_ON_UDS),
    this parameter is not derived and must be configured manually.
  默认值: 51
  最小值: 51
  最大值: 51
- 
  序号: 9
  名称: DemOBDONUDSDTCClass
  长名称: OBD on UDS DTC Class
  描述: |
    This parameter is only relevant for OBDonUDS and ZEVonUDS.
    Together with DemDTCSeverity, the DTC class forms the DTC severity byte according to ISO
    14229-1, J1979-2 and J1979-3.
    
    OBDonUDS:
    DTC Class to classify the emission severity of a DTC according to SAE J1979-2.
    
    
    A DTC with Class 0 does not influence the emissions.
    
    ZEVonUDS:
    DTCClass_1 (ZEV Propulsion related DTC) according to SAE J1979-3.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemObdDTC3Byte
  长名称: OBD on UDS 3 Byte DTC
  描述: |
    This parameter is only relevant for OBDonUDS.
    
    3 Byte OBD DTC value that is used for the UDS Diagnostic Trouble Code (DTC). The value is
    defining a DTC based on SAE J2012.
    
    This parameter is only considered when UDS and OBD DTC handling is separated
    (DemGeneral/DemOBDSupport == true, DemGeneral/DemGeneralOBD/DemSupportedObdUdsDtcSeparation ==
    true and DemGeneral/DemGeneralOBD/DemOBDLegislation == DEM_OBD_LEGISLATION_OBD_ON_UDS).
  默认值: ''
  最小值: 256
  最大值: 16777214
```

### 3. DemCallbackInitMForF

**描述**: The presence of this container sets up an initialization function (InitMonitorForFunction) for this
DTC.
The Dem will call this function each time the related DTC is cleared, or the operation (monitoring)
cycle of the related monitor restarts.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackInitMForFFnc'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackInitMForFFnc
  长名称: Callback InitMonitorForFunction Function
  描述: |
    Function name of an InitMonitorForFunction callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. DemDtrs

**描述**: This container holds the configuration of DTRs collection.

该容器没有参数。

### 5. DemDtr

**描述**: This container holds the configuration of one individual DTR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDtrCompuDenominator0
  长名称: ''
  描述: |
    Part of the conversion between the binary representation and the physical meaning analogous to
    the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator
    coefficient in the direction compuInternalToPhys.
    
    The value must be greater than 0.
    
    In detail, the conversion of x (= old Value) to y (= new value) is given by
    
       y = (A*x + B)/C,
    
    where
    A = DemDtrCumpuNumerator1,
    B = DemDtrCompuNumerator0,
    C = DemDtrCompuDenominator0 (= this parameter).
    
  默认值: 1
  最小值: 0
  最大值: 3.4028235E+38
- 
  序号: 2
  名称: DemDtrCompuNumerator0
  长名称: ''
  描述: |
    Part of the conversion between the binary representation and the physical meaning analogous to
    the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator
    coefficient in the direction compuInternalToPhys.
    
    In detail, the conversion of x (= old Value) to y (= new value) is given by
    
       y = (A*x + B)/C,
    
    where
    A = DemDtrCumpuNumerator1,
    B = DemDtrCompuNumerator0 (= this parameter),
    C = DemDtrCompuDenominator0.
    
  默认值: 0
  最小值: -3.4028235E+38
  最大值: 3.4028235E+38
- 
  序号: 3
  名称: DemDtrCompuNumerator1
  长名称: ''
  描述: |
    Part of the conversion between the binary representation and the physical meaning analogous to
    the SW-C Template conversion CompuRationalCoeffs with 2 numerator coefficients and 1 denominator
    coefficient in the direction compuInternalToPhys.
    
    The value must be greater than 0.
    
    In detail, the conversion of x (= old Value) to y (= new value) is given by
    
       y = (A*x + B)/C,
    
    where
    A = DemDtrCumpuNumerator1 (= this parameter),
    B = DemDtrCompuNumerator0,
    C = DemDtrCompuDenominator0.
    
  默认值: 1
  最小值: 0
  最大值: 3.4028235E+38
- 
  序号: 4
  名称: DemDtrId
  长名称: ''
  描述: The index identifier value assigned to this DTR. The value is generated during the Dem
      configuration process.
  默认值: 65535
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DemDtrMid
  长名称: ''
  描述: |
    The OBDMID of the DTR.
    
    The values 0x00, 0x20, 0x40, 0x60, 0x80, 0xA0, 0xC0, 0xE0 are reserved.
  默认值: ''
  最小值: 1
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
  描述: |
    Update conditions applied by the Dem to reports of DTR values.
    
    DEM_DTR_UPDATE_ALWAYS: The reported DTR values are always processed.
    
    DEM_DTR_UPDATE_STEADY: The reported DTR values are only processed, if the enable and storage
    conditions of the event referenced by DemDtrEventRef are fulfilled and the DTR values are
    consistent with the current event status of this event. This value can therefore only take
    effect if an event is referenced. If no event is referenced, the Dem behaves as if
    DemDtrUpdateKind is configured to DEM_DTR_UPDATE_ALWAYS.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. DemEventParameter

**描述**: This container contains the configuration of diagnostic events. These represent monitors and can be
mapped onto a DTC.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemEventAvailable
  长名称: Event Available By Default
  描述: |
    This parameter has only an effect when
    /Dem/DemGeneral/DemPostbuild/DemEventAvailableDefaultSupport is enabled.
    If this parameter is set to true, the event will be considered as available during
    initialization.
    If this parameter is set to false, the event will be considered as unavailable during
    initialization
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemEventId
  长名称: ''
  描述: |
    Internal identifier of a diagnostic event.
    
    This number is calculated internally and shall not be configured manually. This parameter is
    only available to publish the result of this calculation.
    Applications using Dem APIs must not rely on the value of this parameter. Instead, they must use
    the symbolic constant (SymbolicNameValue) DemConf_DemEventParameter_{SHORT-NAME}.
  默认值: 65535
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: DemEventKind
  长名称: ''
  描述: |
    This parameter is used to distinguish between SW-C and BSW events.
    
    SW-C events are reported through the RTE port interface DiagnosticMonitor, operation
    SetEventStatus.
    BSW events are reported by C-API Dem_SetEventStatus.
  默认值: DEM_EVENT_KIND_SWC
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemMaxNumberFreezeFrameRecords
  长名称: Max Number FreezeFrameRecords
  描述: |
    This parameter defines the number of snapshot records which can be stored for this event.
    
    The parameter will be mandatory, if the snapshot numbers are CALCULATED (refer to
    DemTypeOfFreezeFrameRecordNumeration of DemPrimaryMemory or DemUserDefinedMemory referenced by
    the event) and a FreezeFrame is configured for this DemEventParameter (see
    DemFreezeFrameClassRef).
    
    For configured record numbers this value has no meaning and should be removed.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: DemEventAvailableInVariant
  长名称: ''
  描述: |
    This parameter configures the event's availability in the variant.
    If this parameter is set to false for a specific variant, this event is not available at all in
    this variant.
    If this parameter is set to true, the event is available for the current variant.
    
    With Postbuild-Selectable setting not supported, this parameter will be set to true and shall
    not be changed manually.
    If the parameter is changed to false, the event will not be available at all, like it is not
    configured.
    
    If this parameter set to false, even though the switch DEM_CFG_SUPPORT_EVENTAVAILABLE
    (/Dem/DemGeneral/DemAvailabilitySupport) is enabled, changing the availability of events at
    runtime is not possible.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemEventLatchTestFailed
  长名称: Event Latch TestFailed
  描述: |
    Switch to block TestPassed results for a qualified event.
    
    See DemGeneral/DemLatchTestFailedBehavior for the effect of this switch.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemEventCreateInfoPort
  长名称: ''
  描述: |
    Activate/deactivate the creation of the DiagnosticInfo port for the event.
    
    If this parameter is enabled, the interface DiagnosticInfo is provided for the event.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemEventRecoverableInSameOperationCycle
  长名称: ''
  描述: |
    Not supported.
    Please use the following parameters to configure the desired behavior
    
    DemEventRecoverableInSameOperationCycle = TRUE:
    DemEventLatchTestFailed = FALSE
    
    DemEventRecoverableInSameOperationCycle = FALSE:
    DemEventLatchTestFailed = TRUE
    AND
    DemGeneral/DemLatchTestFailedBehavior = DEM_LATCH_ONLY_THIS_CYCLE
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. DemCallbackClearEventAllowed

**描述**: The presence of this container sets up a callout function 'ClearEventAllowed' for this DTC. The Dem
will call this function each time the related DTC is about to be cleared by an external tool. (API
Dem_ClearDTC, usually only called by Dcm).

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackClearEventAllowedFnc'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackClearEventAllowedFnc
  长名称: Callback ClearEventAllowed Function
  描述: |
    Function name of a 'ClearEventAllowed' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemClearEventAllowedBehavior
  长名称: ''
  描述: |
    Defines the resulting UDS status byte for the related event, which must not be cleared according
    to the ClearEventAllowed callback.
    (not supported)
  默认值: DEM_NO_STATUS_BYTE_CHANGE
  最小值: ''
  最大值: ''
```

### 8. DemCallbackEventDataChanged

**描述**: The presence of this container sets up a callout function 'EventDataChanged' for this DTC. The Dem
will call this function each time the stored data (extended record, snapshot record) has changed.

Please note, data elements can be mapped to internal data. This callback is NOT called if such data
changes, only if the stored data record is modified due to a new event report.
Example: If an extended record is mapped to the fault detection counter, this API is not called each
time the FDC changes even though a diagnostic service $19 06 would indeed return different data.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackEventDataChangedFnc'.
The presence of this container indicates that the Dem has access to an "EventDataChanged" callback.

This container is ignored, if parameter DemGeneral/DemTriggerEventDataChangedCallback exists and has
value False.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackEventDataChangedFnc
  长名称: Callback EventDataChanged Function
  描述: |
    Function name of a 'EventDataChanged' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. DemCallbackEventStatusChanged

**描述**: The presence of this container sets up a callout function 'EventStatusChanged' for this DTC. The Dem
will call this function each time the event status changes.

Please note, the event status is independent of the DTC status availability mask
(DemGeneral/DemDtcStatusAvailabilityMask). All transitions of status bits will be reported.
Attention: Due to preemption it is possible that event status changes are reported in the wrong
order. This is no issue if the Dem_Mainfunction is mapped to a non-preemptive task.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackEventStatusChangedFnc'.

This container is ignored, if parameter DemGeneral/DemTriggerEventStatusChangedCallback exists and
has value False.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackEventStatusChangedFnc
  长名称: Callback EventStatusChanged Function
  描述: |
    Function name of an 'EventStatusChanged' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. DemCallbackInitMForE

**描述**: The presence of this container sets up an initialization function 'InitMonitorForEvent' for this
Event. The Dem will call this function each time this event is cleared, or the operation
(monitoring) cycle restarts (see ./DemEventClass/DemOperationCycleRef).
Using parameter DemTriggerMonitorInitForEnableConditions with value'true', this function will also
be called if an enable condition or ControlDTC ($85 01) re-activates this event.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackInitMForFFnc'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackInitMForEFnc
  长名称: Callback InitMonitorForEvent Function
  描述: |
    Function name of a 'InitMonitorForEvent' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. DemEventClass

**描述**: This container contains further configuration parameters for the event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemAgingAllowed
  长名称: ''
  描述: |
    Switch to allow aging/unlearning of the event.
    
    If aging is supported, a valid aging cycle must be referenced (see DemAgingCycleRef) and a valid
    number of aging cycles must be set (see DemAgingCycleCounterThreshold).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemAgingCycleCounterThreshold
  长名称: AgingCycle Counter Threshold
  描述: |
    Number of aging cycles needed to unlearn/delete the event.
    
    A value of 0 means, the event is aged immediately with a passed event status.
    A value of 1 means the event is aged at the end of the current aging cycle (if the event is
    passive at that moment).
    Larger values represent the n-th cycle e.g. 2 is the next, 3 the cycle after the next etc.
    
    If this parameter is missing:
    - If aging allowed is set to true (refer to DemAgingAllowed), this value defaults to 0.
    - If aging allowed is set to false, this value defaults to 255.
    
    If aging allowed is set to false the value is still used as upper limit for the aging counter,
    given that the aging counter behavior (refer to Dem/DemGeneral/DemAgingCounterBehavior) is set
    to DEM_AGING_COUNT_ALWAYS. In this case the value is also used as initial value for the inverted
    aging counter.
    If the aging counter behavior is set to DEM_AGING_COUNT_ONLY_AGEABLE, this value is reported for
    the inverted aging counter, but has no effect for the incrementing aging counter (with aging
    allowed set to false).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DemConsiderPtoStatus
  长名称: ''
  描述: This parameter is TRUE, when the event is affected by the Dem PTO handling.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemEventFailureCycleCounterThreshold
  长名称: Event FailureCycleCounter Threshold
  描述: |
    Number of operation cycles needed to confirm the event.
    
    When the parameter is missing or has the value 0, use the standard UDS behavior of confirming
    the event (ConfirmedDTC status bit becomes set) with the first qualified FAILED result.
    A value of 1 means the event becomes confirmed if it fails again in the next operation cycle.
    Larger values represent confirmation in the n-th cycle e.g. 2 is confirmation in cycle after the
    next cycle, etc.
    
    All DTCs, that are in the same MIL Group, must have the same threshold value (refer to parameter
    /Dem/DemGeneral/DemMILGroup).
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 5
  名称: DemEventMemoryEntryFdcThresholdStorageValue
  长名称: ''
  描述: |
    Threshold to allocate an event memory entry and to capture the Freeze Frame.
    (Not supported - please use
    /DemConfigSet/DemDebounceTimeBasedClass/DemTimeBasedFdcThresholdStorageValue
    or
    DemConfigSet/DemDebounceCounterBasedClass/DemCounterBasedFdcThresholdStorageValue
    instead.)
    
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DemEventOBDReadinessGroup
  长名称: ''
  描述: |
    Select the Event OBD Readiness group.
    
    This parameter is only needed if OBD support is enabled (see DemGeneral/DemOBDSupport).
    The parameter is needed for PID $01, PID $F501, PID $41, J1939 diagnostic readiness 1 and 3
    computation and to classify faults according to OBD requirements (e.g. OBD freeze frame related
    to misfire or fuel system faults can displace other freeze frames).
    
    The different values for this parameter are described in the Dem AUTOSAR SWS. In addition to the
    Readiness groups described there, the following groups are supported for spark and compression
    engines:
    - DEM_OBD_RDY_EGHSENS: Exhaust gas sensor heater monitoring
    - DEM_OBD_RDY_CSAS: Cold start aid system monitoring.
  默认值: DEM_OBD_RDY_NONE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemEventPriority
  长名称: ''
  描述: |
    Set the priority of the event.
    
    A lower number represent higher priority. Same level priority is allowed.
    This value influences the event displacement in case the respective memory is completely filled
    at the time of event confirmation.
    Lower priority events will never displace higher priority events. Equal priority events will
    displace passive entries.
    
    This parameter only has an effect if event displacement is supported (see
    DemGeneral/DemEventDisplacementSupport).
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 8
  名称: DemEventSignificance
  长名称: ''
  描述: |
    Significance of the event, which indicates additional information concerning fault
    classification and resolution.
    
    This value can optionally be selected to be reported as event data (e.g. as data element inside
    an extended data record).
    It has no further effect on the Dem.
  默认值: DEM_EVENT_SIGNIFICANCE_FAULT
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemFFPrestorageSupported
  长名称: FreezeFrame Prestorage Supported
  描述: |
    Select the event for prestorage support.
    
    Only events with this flag enabled may request data prestorage (Port interface
    DiagnosticMonitor, operation PrestoreFreezeFrame).
    
    This parameter only has an effect if prestorage is enabled (see
    DemGeneral/DemMaxNumberPrestoredFF).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemOBDVisibilityDelayedUntilDcyQualification
  长名称: ''
  描述: |
    This parameter defines when the ConfirmedDTC and the WarningIndicatorRequested status bits of an
    OBD relevant event become externally visible. Depending on the configuration, permanent DTC and
    the OBD FreezeFrame of the event are also only externally visible after the related status bit
    becomes externally visible.
    If this parameter is enabled, the two status bits are not visible before the OBD driving cycle
    is qualified.
    If this parameter is disabled, the two status bits are visible without the need for a qualified
    driving cycle.
    
    If this parameter is missing, the Dem will handle the visibility of the two status bits
    according to the settings of
    Dem/DemConfigSet/DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold:
    If DemEventFailureCycleCounterThreshold is 0, the value of
    DemOBDVisibilityDelayedUntilDcyQualification is assumed as disabled.
    If DemEventFailureCycleCounterThreshold is > 0, the value of
    DemOBDVisibilityDelayedUntilDcyQualification is assumed as enabled.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 12. DemIndicatorAttribute

**描述**: This container maps the event to a list of indicators which can be enabled due to the event failing.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIndicatorBehaviour
  长名称: ''
  描述: Select how the referenced indicator will react on this event (Blink, continuous light,
      application decides)
  默认值: DEM_INDICATOR_CONTINUOUS
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemIndicatorFailureCycleCounterThreshold
  长名称: Indicator FailureCycle Counter Threshold
  描述: |
    Number of continuous failed cycles until the indicator is enabled.
    
    This parameter is only valid if DemIndicatorFailureCycleSource is set to INDICATOR, so this
    parameter is effectively not supported.
    All DTCs, that are in the same MIL Group, must have the same threshold value (refer to parameter
    /Dem/DemGeneral/DemMILGroup).
    
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DemIndicatorFailureCycleSource
  长名称: Indicator FailureCycle Source
  描述: |
    Select if the indicator is enabled as defined by the event status, or if the indicator requires
    a different set of event status bits to determine indicator state.
    
    This feature is required if an indicator is not enabled together with the event confirmation,
    but e.g. uses a different cycle or confirmation threshold.
    
    This parameter is currently not supported and is assumed to be set to 'DEM_FAILURE_CYCLE_EVENT'
  默认值: DEM_FAILURE_CYCLE_EVENT
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemIndicatorHealingCycleCounterThreshold
  长名称: Indicator HealingCycle Counter Threshold
  描述: |
    Defines the number of consecutive cycles in which the event has been tested passed, and not
    tested failed until this indicator heals.
    
    Currently it is only supported to set the same value for each indicator attached to this event.
  默认值: 3
  最小值: 0
  最大值: 255
```

### 13. DemDebounceCounterBased

**描述**: Counter based debouncing will increment a counter with each Prefailed result, and decrement the
counter with each Prepassed result.
A qualified 'Passed' or 'Failed' result will be generated when a given threshold value is reached.

This debouncing type is ideal for cyclic monitors that generate a monitoring result regularly since
it involves little overhead.

The debounce value is mapped to a faultdetection count (FDC) as such:
If the Failed threshould is reached, FDC is 127.
If the DebounceCounter is 0, FDC is 0.
If the Passed threshold is reached, FDC is -128.
Values between 0 and the threshold values are linearly mapped to 1..126 respectively -1..-127.

该容器没有参数。

### 14. DemDebounceMonitorInternal

**描述**: Monitor internal debouncing is used for monitors that implement the debouncing themselves, and only
report qualified results (PASSED/FAILED) to the Dem.

In order to implement the diagnostic services that report the fault detection counter, a callout
function is required.

该容器没有参数。

### 15. DemCallbackGetFDC

**描述**: This container sets up the callout function 'DemCallbackGetFDC' for this Event. The Dem will call
this function each time the value of the fault detection counter is needed, e.g. requested by the
Dcm.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackGetFDCFnc'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackGetFDCFnc
  长名称: Callback GetFaultDetectionCounter Function
  描述: |
    Function name of a 'DemCallbackGetFDC' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 16. DemDebounceTimeBased

**描述**: Time based debouncing will use a timer started in either passed or failed direction with an
unqualified result.
The timer is not restarted in case it is already running, unless a direction change is detected -
e.g. after a PrePassed result the next PrePassed result will not restart the timer, a following
PreFailed will stop the passed timer and start the failed timer.

Timer supervision incurs a substantial runtime and RAM overhead compared to counter based denouncing
and should be used sparingly.

The debounce value is mapped to a faultdetection count as such:
If the Failed time is reached, FDC is 127.
If no timer is running (and no qualified result has been reached), FDC is 0.
If the Passed time is reached, FDC is -128.
If the timer is currently running in either direction, the timer is linearly mapped to 1..126
respectively -1..-127.

该容器没有参数。

### 17. DemJ1939NodeAddress

**描述**: Contains the parameters for the support of a logical J1939 node (identified by an ECU address).

该容器没有参数。

### 18. DemPidClass

**描述**: Only relevant for OBD II.
These containers represent the different PIDs stored in the single global OBD relevant freeze frame.

Each PID consists of one or several data elements.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemPidIdentifier
  长名称: PID Identifier
  描述: PID Identifier as requested in Mode $02
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemSPNId
  长名称: ''
  描述: |
    Suspect parameter number.
    
    Must be configured  if OBDII is supported and DemJ1939ExpandedFreezeFrameSupport is enabled.
  默认值: ''
  最小值: 0
  最大值: 524287
```

### 19. DemPidDataElement

**描述**: These containers are used to reference the different data elements contained in the specific PID.

该容器没有参数。

### 20. DemDTCAttributes

**描述**: This container contains the configuration (parameters) for
DemDTCAttributes.

该容器没有参数。

### 21. DemMultiEventTriggering

**描述**: Configures an event that will trigger other events whenever the event is reported.

该容器没有参数。

### 22. DemDebounceCounterBasedClass

**描述**: Inside this container the parameters for the debouncing of counter based debouncing are configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDebounceCounterIncrementStepSize
  长名称: DebounceCounter Increment Step Size
  描述: The debounce counter will be incremented by this amount with each PREFAILED monitor result.
  默认值: 1
  最小值: 1
  最大值: 32767
- 
  序号: 2
  名称: DemDebounceCounterDecrementStepSize
  长名称: DebounceCounter Decrement Step Size
  描述: |
    The debounce counter will be decremented by this amount with each PREPASSED monitor result.
    
    Note: The value is subtracted, so it must be positive.
  默认值: 1
  最小值: 1
  最大值: 32768
- 
  序号: 3
  名称: DemDebounceCounterFailedThreshold
  长名称: DebounceCounter Failed Threshold
  描述: If a PREFAILED monitor result increments the debounce counter to(or above) this value, a
      qualified FAILED result is generated.
  默认值: 127
  最小值: 1
  最大值: 32767
- 
  序号: 4
  名称: DemDebounceCounterPassedThreshold
  长名称: DebounceCounter Passed Threshold
  描述: If a PREPASSED monitor result decrements the debounce counter to (or below) this value, a
      qualified PASSED result is generated.
  默认值: -128
  最小值: -32768
  最大值: -1
- 
  序号: 5
  名称: DemDebounceCounterJumpUp
  长名称: DebounceCounter Jump Up
  描述: |
    Select the jump up behavior.
    
    If enabled, the debounce counter is set to the value of DemDebounceCounterJumpUpValue before
    incrementing, unless the counter already is larger.
    This can be used to achieve constant times for a qualified FAILED result.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemDebounceCounterJumpDown
  长名称: DebounceCounter Jump Down
  描述: |
    Select the jump down behavior.
    
    If enabled, the debounce counter is set to the value of DemDebounceCounterJumpDownValue before
    decrementing, unless the counter already is smaller.
    This can be used to achieve constant times for a qualified PASSED result.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemDebounceCounterJumpDownValue
  长名称: DebounceCounter Jump Down Value
  描述: |
    This is the debounce counter value set if a 'JumpDown' is triggered.
    
    This parameter is used only if DemDebounceCounterJumpDown is enabled.
  默认值: 0
  最小值: -32768
  最大值: 32767
- 
  序号: 8
  名称: DemDebounceBehavior
  长名称: Debounce Behavior
  描述: |
    This parameter defines how the event debounce algorithm will behave, if a related enable
    condition is not fulfilled or ControlDTCSetting of the related event is disabled.
    
    FREEZE: The FDC will continue at the current value when enable conditions / ControlDTCSetting
    allow event reports again.
    RESET: The FDC will revert to 0. See also (DemGeneral/DemResetDebounceBehavior)
  默认值: DEM_DEBOUNCE_FREEZE
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemDebounceCounterStorage
  长名称: Debounce Counter Storage
  描述: |
    Switch to store the debounce counter value non-volatile or not.
    
    When activating this feature, the configuration needs an additional NV-RAM block with
    DemNvRamBlockIdType "DEM_NVBLOCK_DEBOUNCE".
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemCounterBasedFdcThresholdStorageValue
  长名称: Counter Based Fdc Threshold Storage Value
  描述: |
    If a PREFAILED monitor result increments the debounce counter to (or above) this value, a FDC
    TRIP result is generated.
    
    This value has to be less or equal to DemDebounceCounterFailedThreshold.
    
    This parameter is only relevant if data is stored at a time where the DTC fault detection
    counter passes a threshold lower than the failed threshold, or if parameter
    Dem/DemGeneral/DemSupportExtendedFiM is available and enabled.
  默认值: 127
  最小值: 1
  最大值: 32767
- 
  序号: 11
  名称: DemDebounceCounterJumpUpValue
  长名称: DebounceCounter Jump Up Value
  描述: |
    This is the debounce counter value which is set if a 'JumpUp' is triggered.
    Usually this is set to 0 as shown in ISO14229.
    
    This parameter is used only if DemDebounceCounterJumpUp is enabled.
  默认值: 0
  最小值: -32768
  最大值: 32767
- 
  序号: 12
  名称: DemDebounceContinuous
  长名称: Debounce Continuous
  描述: |
    This parameter defines whether the event debounce algorithm will continue counting while enable
    conditions are not fulfilled / ControlDTCSetting is disabled.
    To prevent the event from qualifying after the enable conditions become enabled /
    ControlDTCSetting is enabled again, it is recommended to set DemDebounceBehavior to
    DEM_DEBOUNCE_RESET if this option is used.
  默认值: false
  最小值: ''
  最大值: ''
```

### 23. DemDebounceTimeBasedClass

**描述**: Inside this container the parameters for the debouncing of time based debouncing are configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDebounceTimeFailedThreshold
  长名称: DebounceTime Failed Threshold
  描述: |
    Time after a PreFailed report, after which a qualified FAILED result is generated.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a diffenent unit.
  默认值: ''
  最小值: 0.001
  最大值: 3600
- 
  序号: 2
  名称: DemDebounceTimePassedThreshold
  长名称: DebounceTime Passed Threshold
  描述: |
    Time after a PrePassed report, after which a qualified PASSED result is generated.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a diffenent unit.
  默认值: ''
  最小值: 0.001
  最大值: 3600
- 
  序号: 3
  名称: DemDebounceBehavior
  长名称: Debounce Behavior
  描述: |
    This parameter defines how the event debounce algorithm will behave, if a related enable
    condition is not fulfilled or ControlDTCSetting of the related event is disabled.
    
    FREEZE: The debounce timer will pause while enable conditions are not active. To continue,
    report prepassed/prefailed after the enableconditions are fulfilled / ControlDTCSetting is
    enabled
    RESET: The FDC will revert to 0. See also (DemGeneral/DemResetDebounceBehavior)
  默认值: DEM_DEBOUNCE_FREEZE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemTimeBasedFdcThresholdStorageValue
  长名称: Time Based Fdc Threshold Storage Value
  描述: |
    If a monitor fails for this time, a FDC TRIP result is generated.
    
    This value has to be less than or equal to DemDebounceTimeFailedThreshold.
    
    This parameter is only relevant if data is stored at a time where the DTC fault detection
    counter passes a threshold lower than the failed threshold, or if parameter
    Dem/DemGeneral/DemSupportExtendedFiM is available and enabled.
  默认值: ''
  最小值: 0.001
  最大值: 3600
- 
  序号: 5
  名称: DemDebounceContinuous
  长名称: Debounce Continuous
  描述: |
    This parameter defines whether the event debounce algorithm will continue counting while enable
    conditions are not fulfilled / ControlDTCSetting is disabled.
    To prevent the event from qualifying after the enable conditions become enabled /
    ControlDTCSetting is enabled again, it is recommended to set DemDebounceBehavior to
    DEM_DEBOUNCE_RESET if this option is used.
    If DemDebounceBehavior is set to DEM_DEBOUNCE_FREEZE, an active debounce timer is paused, but
    the timer can be re-started while enable conditions are inactive.
  默认值: false
  最小值: ''
  最大值: ''
```

### 24. DemGeneral

**描述**: This container groups the constant configuration options, e.g. options that can not have different
values in multiple configurations.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemAgingCycleCounterProcessing
  长名称: AgingCycle Counter Processing
  描述: |
    This parameter is obsolete and ignored, since no DemAgingCycle is supported.
    The same functionality can be achieved with operation cycles.
  默认值: DEM_PROCESS_AGINGCTR_INTERN
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemAgingRequieresTestedCycle
  长名称: ''
  描述: |
    Defines if the aging cycle counter is processed every aging cycles or if only tested aging cycle
    are considered.
    (Not supported, please use DemGeneral/DemAgingBehavior instead)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemAvailabilitySupport
  长名称: ''
  描述: |
    This configuration switch defines, whether support for runtime configuration of the availability
    of events is enabled or not. If enabled, a corresponding API for switching availability of
    events at runtime is provided.
    
  默认值: DEM_NO_AVAILABILITY
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemAvailabilityStorage
  长名称: ''
  描述: |
    This configuration switch defines, whether runtime changes of the event's availability are
    persisted in NVRAM.
    
    If this option is disabled, changing the event availability is not persisted and API
    Dem_SetEventAvailable() will work as described in the AUTOSAR SWS.
    
    When activating this feature, the configuration needs an additional NV-RAM block with
    DemNvRamBlockIdType "DEM_NVBLOCK_AVAILABILITY".
    The referenced NV block must be configured to hold the configured number of DemEventParameter
    containers + 1, divided by 8, fraction rounded up to integer.
    Enabling this option will prevent API Dem_SetEventAvailable() from working before Dem_Init(), as
    the NV data must be restored first.
    
    If this option is enabled, you also need DemGeneral/DemAvailabilitySupport == TRUE - otherwise
    the availability is not persisted in NVRAM.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemBswErrorBufferSize
  长名称: BswError Buffer Size
  描述: |
    Dem processing queue size.
    (This parameter is no longer supported. The number of events, which can be queued, is not
    limited to this parameter value.)
    
    The Dem will process qualified events (Failed/Passed) during the next task cycle. This value
    specifies how many events can be queued.
    When this queue overflows you will not lose reports, but the surplus events are not processed in
    reporting order. Also run-time is greately increased as surplus events need to be searched for
    the pending event change.
    
    A sufficient queue size can not be deduced from the Dem configuration, you need to analyze how
    your system reports events:
    set the size to the maximum amount of monitors that may report a qualified result (e.g. finish
    debouncing) during a single task cycle of the Dem.
    
    With queue overflow the run time of the Dem_MainFunction can spike, so you need to verify its
    run-time does not exceed your system limit (e.g. causes a task overflow) when the maximum amount
    of your monitors qualify at the same time.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DemClearDTCBehavior
  长名称: ClearDTC Behavior
  描述: |
    Select the point in time a clear DTC request will result in a positive response from the Dcm.
    
    VOLATILE: The Dem will clear all DTCs in RAM before the API Dem_ClearDTC returns a final result
    to the Dcm. If power is cut right after that and your ECU does not allow for a controlled shut
    down in that case, DTCs will still be visible after the ECU restarts.
    
    NONVOLATILE_TRIGGER: ClearDTC will return a final result after the NvM has been informed about
    the modification. This setting is not supported by this implementation.
    
    NONVOLATILE_FINISH: ClearDTC will return a final result only after the NvM has finished
    persisting the cleared state of DTCs. Depending on your NV system this can result in several
    seconds of NRC $78 - response pending. On the upside, if power is cut after the positive
    response, all DTCs remain cleared.
  默认值: DEM_CLRRESP_VOLATILE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemClearDTCLimitation
  长名称: ''
  描述: |
    Defines the supported Dem_{...}ClearDTC API scope.
    
    ALL_SUPPORTED_DTCS: The API accepts all supported DTC values, as well as all DTC values which
    are configured in DemGroupDTCs and DEM_DTC_GROUP_ALL_DTCS (default).
    
    ONLY_CLEAR_ALL_DTCS: The API accepts ClearAllDTCs only (DTC Group 0xFFFFFF).
    
    ONLY_CLEAR_OBDII_AND_ALL_DTCS: The API accepts ClearAllDTCs only (DTC Groups 0x000000, 0xFFFFFF)
    in OBDII configuration variants.
    
    ONLY_CLEAR_SINGLE_AND_ALL_DTCS: The API accepts DTC numbers and ClearAllDTCs (DTC Group,
    0xFFFFFF).
    
    ONLY_CLEAR_EMISSIONS_SYSTEM_GROUP_AND_ALL_DTCS: The API accepts ClearAllDTCs only (DTC Groups
    0xFFFF33, 0xFFFFFF) in WWHOBD, OBD on UDS and ZEV on UDS configuration variants.
    
  默认值: DEM_ALL_SUPPORTED_DTCS
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemDataElementDefaultEndianness
  长名称: ''
  描述: |
    Defines the default endianness of the data belonging to a data element which is applicable if
    the DemExternalSRDataElementClass does not define a endianness.
    (not supported)
  默认值: LITTLE_ENDIAN
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemDebounceCounterBasedSupport
  长名称: Debounce CounterBased Support
  描述: |
    This configuration switch defines, whether support for counter based debouncing is enabled or
    not (see
    DemConfigSet/DemEventParameter/DemDebounceAlgorithmClass/DemDebounceCounterBased/DemDebounceCounterBasedClassRef).
    
    If events are configured to use counter based debouncing, this option must be enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemDebounceTimeBasedSupport
  长名称: Debounce TimeBased Support
  描述: |
    This configuration switch defines, whether support for time based debouncing is enabled or not
    (see
    DemConfigSet/DemEventParameter/DemDebounceAlgorithmClass/DemDebounceTimeBased/DemDebounceTimeBasedClassRef).
    
    If events are configured to use timer based debouncing, this option must be enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DemDevErrorDetect
  长名称: Development Error Detect
  描述: |
    Activate/Deactivate the Development Error Detection and Notification.
    
    If this option is enabled, integration errors are reported to the DET module (e.g. calling APIs
    with invalid arguments that would cause a malfunction of the Dem module).
    In a production system this option can be disabled as all code should be tested to correctly use
    the Dem API.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DemDtcStatusAvailabilityMask
  长名称: DTC StatusAvailabilityMask
  描述: |
    Mask for the supported DTC status bits of the Dem. This mask is used by UDS service 0x19.
    
    Internally, all status bits are supported as required by the Dem specification. This internal
    status byte is used e.g. for internal event notification callout functions.
    Externally, all status bits are ANDed with this mask, e.g. for diagnostic services like 0x19 or
    DTC status change notifications.
    This mask is also reported as status availability mask in the respective 0x19 subfunctions.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: DemEnableConditionSupport
  长名称: EnableCondition Support
  描述: |
    This configuration switch defines, whether support for enable conditions is enabled or not.
    
    If enable conditions are set up for events
    (DemConfigSet/DemEventParameter/DemEventClass/DemEnableConditionGroupRef) this option must be
    enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: DemEventCombinationSupport
  长名称: ''
  描述: |
    Merge several events to one specific DTC and a combined UDS DTC status byte.
    
    DISABLED: No event combination is supported.
    
    TYPE1: Multiple events can be combined to a single DTC. The events are combined on storage as
    specified in AUTOSAR.
    
    TYPE2: Multiple events can be combined to a single DTC. The events are combined on retrieval as
    specified in AUTOSAR.
    
    TYPE3: This type of event combination is only relevant if OBDonUDS is supported in at least one
    configuration variant.
    For configuration variants without OBDonUDS support:
    - The behavior of all DTCs corresponds to event combination TYPE1.
    
    For configuration variants with OBDonUDS support:
    - The calculation of the DTC status of OBD relevant DTCs deviates from TYPE1. It corresponds to
    the behavior specified in the Digital Annex of SAE J1979.
    - The behavior of DTCs that are not OBD relevant still corresponds to TYPE1.
    
    
  默认值: DEM_EVCOMB_DISABLED
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DemEventDisplacementStrategy
  长名称: ''
  描述: |
    This configuration switch is back-ported from AR4.1.1 and specifies the event displacement when
    the event memory is currently filled completely.
    It replaces the AR4.0.3 parameter DemEventDisplacementSupport.
    
    Please note, the DTC selected by the displacement algorithm is only displaced if it is a better
    match than the new DTC that has to be entered into the memory.
    If the new DTC is the better match, or no matching DTCs are found in the event memory, the
    fall-back strategy DemEventDisplacementFallbackStrategy is implemented.
    
    NONE: No displacement.
    If the event memory is filled, a new event will always be displaced immediately.
    Please note, the only supported fall-back strategy for this case is DISCARD_NEW_EVENT.
    
    PRIO_OCC: Displacement is active.
    If the event memory is filled, the DTC(s) with lowest priority are selected.
    If multiple DTCs share this lowest priority, the oldest is selected.
    
    FULL: Displacement is active.
    If the event memory is filled, the DTC(s) with the lowest priority are selected.
    If multiple DTCs share this lowest priority, the oldest passive DTC is selected.
    If no passive DTCs are among the lowest priority list, the oldest active, but untested DTC is
    selected.
    
    LEGACY_403: Vector extension that corresponds to the displacement behavior defined in Autosar
    4.0.3.
    If the event memory is filled, the DTC(s) with the lowest priority are selected.
    If multiple DTCs share this lowest priority, the oldest passive DTC is selected.
    
  默认值: DEM_DISPLACEMENT_LEGACY_403
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DemExtendedDataCapture
  长名称: ExtendedData Capture
  描述: |
    This parameter defines the point in time, when the extended data collection is done.
    
    TESTFAILED: The data is collected directly in the context of the SetEventStatus call. This
    option is not supported.
    
    MEMORY_STORAGE: The data is collected during the next Dem task cycle, in case a memory entry can
    be created for the DTC (see DemEventDisplacementSupport)
  默认值: DEM_TRIGGER_EVENT_MEMORY_STORAGE
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DemExtendedDataVisibility
  长名称: ExtendedData Visibility
  描述: |
    This parameter defines the point in time when extended data will be reported in diagnostic
    response messages.
    
    This parameter affects extended data records that consist solely of statistical data which is by
    its nature at any time available, see DemInternalDataElement.
    
    Using this parameter allows to reduce visibility of such extended data records until the DTC is
    actually stored.
    
    ALL_DTC: The data is reported independent of an existing memory entry.
    
    STOREDONLY: The data is reported only if a memory entry exists for the reported DTC.
    
    Example: The current fault detection counter exists at any time for all DTCs. If this parameter
    is set to ALL_DTC, service 19 06 will report the value of the FDC for DTCs that are not
    currently stored.
    If this parameter is set to STOREDONLY, Dcm will instead send a positive response without any
    content for those DTCs.
  默认值: DEM_VISIBILITY_ALL_DTC
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DemFreezeFrameCapture
  长名称: FreezeFrame Capture
  描述: |
    This parameter defines the point in time, when the freeze frame data collection is done.
    
    TESTFAILED: The data is collected directly in the context of the SetEventStatus call. This
    option is not supported.
    
    MEMORY_STORAGE: The data is collected during the next Dem task cycle, in case a memory entry can
    be created for the DTC (see DemEventDisplacementSupport).
  默认值: DEM_TRIGGER_EVENT_MEMORY_STORAGE
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: DemGeneralInterfaceSupport
  长名称: ''
  描述: |
    The interfaces GeneralEvtInfo, GeneralCallbackEventDataChanged and
    GeneralCallbackEventStatusChange are provided if DemGeneralInterfaceSupport is equal to true.
    (Not supported, please use
    - DemGeneral/DemGeneralDiagnosticInfoSupport,
    - DemGeneral/DemTriggerGlobalEventDataChangedCallback,
    - DemGeneral/DemTriggerGlobalEventStatusChangedCallback
    instead.)
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DemHeaderFileInclusion
  长名称: HeaderFile Inclusion
  描述: |
    Name of the header file(s) to be included by the Dem module containing the used C-callback
    declarations.
    
    The different callout configurations allow to specify a C-Callback instead of a port interface.
    If you choose so, you need to add a header file here with the appropriate declaration of the
    function.
    see DemConfigSet/DemDTCClass/DemCallbackInitMForF/DemCallbackInitMForFFnc,
    see DemConfigSet/DemEventParameter/DemCallbackClearEventAllowed/DemCallbackClearEventAllowedFnc,
    see DemConfigSet/DemEventParameter/DemCallbackEventDataChanged/DemCallbackEventDataChangedFnc,
    see
    DemConfigSet/DemEventParameter/DemCallbackEventStatusChanged/DemCallbackEventStatusChangedFnc,
    see DemConfigSet/DemEventParameter/DemCallbackInitMForE/DemCallbackInitMForEFnc,
    see
    DemConfigSet/DemEventParameter/DemDebounceAlgorithmClass/DemDebounceMonitorInternal/DemCallbackGetFDC/DemCallbackGetFDCFnc,
    see DemGeneral/DemCallbackDTCStatusChanged/DemCallbackDTCStatusChangedFnc,
    see DemGeneral/DemDataClass/DemDataElementReadFnc,
    see DemGeneral/DemEventMemorySet/DemClearDTCNotification/DemClearDtcNotificationFnc.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: DemImmediateNvStorageLimit
  长名称: ImmediateNvStorage Limit
  描述: |
    This parameter defines a limit for the number of immediate write accesses to the non-volatile
    memory.
    This option is only relevant if immediate NV storage is used for DTCs (see
    DemGeneral/DemImmediateNvStorageSupport and DemConfigSet/DemDTCClass/DemImmediateNvStorage).
    
    If configured the non-volatile immediate storage for a DTC is only triggered until the
    OccurenceCounter reaches the configured value.
    Note that the number of immediate write accesses for a DTC can be higher than the configured
    value (for detailed description see Technical Reference).
    
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 22
  名称: DemMaxNumberEventEntryMirror
  长名称: ''
  描述: |
    Maximum number of events which can be stored in the mirror memory.
    
    The mirror memory is currently not supported, so this value should be set to 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: DemMaxNumberEventEntryOBDFreezeFrame
  长名称: Max Number Event Entry OBD FreezeFrame
  描述: |
    Maximum number of events which can concurrently store an OBD II or OBDonUDS Freeze Frame.
    With WWH OBD each memory entry stores an OBD Freeze Frame, so this parameter is ignored.
    OBD Freeze Frame memory is only available if OBD II or OBDonUDS is supported.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: DemMaxNumberEventEntryPermanent
  长名称: ''
  描述: |
    Maximum number of events which can be stored in the permanent memory.
    
    Permanent memory is available in case that MIL is supported and either OBD II or OBD on UDS or
    Permanent for WWH-OBD is supported (see DemOBDSupport, DemOBDLegislation, DemMILIndicatorRef and
    DemOBDPermanentForWWHOBD).
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 25
  名称: DemMaxNumberPrestoredFF
  长名称: ''
  描述: Defines the maximum number for prestored freeze frames.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 26
  名称: DemOBDSupport
  长名称: ''
  描述: |
    DEM_OBD_NO_OBD_SUPPORT: OBD support is disabled, the DEM operates in UDS mode.
    
    DEP_SEC_ECU: OBD support is enabled, the DEM operates in secondary/dependent ECU mode. (not
    supported)
    
    PRIMARY_ECU: OBD support is enabled, the DEM operates in primary ECU mode.
    
    MASTER_ECU: OBD support is enabled, the DEM operates in master ECU mode. (not supported)
    
    If OBD support is NOT disabled, use parameter Dem/DemGeneral/DemGeneralOBD/DemOBDLegislation to
    choose either OBD II or WWH-OBD or OBDonUDS or ZEVonUDS support.
    If OBD support is disabled, all configured OBD relevant parameters (e.g. the parameters in
    Dem/DemGeneral/DemGeneralOBD) are ignored.
  默认值: DEM_OBD_NO_OBD_SUPPORT
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: DemOccurrenceCounterProcessing
  长名称: OccurrenceCounter Processing
  描述: |
    The occurrence counter is incremented each time the event status transitions from 'passed' to
    'failed'.
    
    TF (TestFailed) : The counter is incremented each time.
    
    CDTC (Confirmed): The counter is incremented only after the event is confirmed - Effectively the
    counter starts incrementing after N cycles (see
    DemConfigSet/DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold).
  默认值: DEM_PROCESS_OCCCTR_TF
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: DemOperationCycleProcessing
  长名称: OperationCycle Processing
  描述: |
    This parameter is obsolete since the option DEM_PROCESS_OPCYC_COUNTER is not longer supported by
    AUTOSAR.
    
    OPCYC_STATE: Cycles are reported by SetOperationCycleState(Start/Stop) and the Dem counts the
    cycles internally.
    
    OPCYC_COUNTER: Cycles are counted externally. The current count is reported to the Dem by
    SetOperationCycleCounter.
    
    Only OPCYC_STATE is supported at the moment.
  默认值: DEM_PROCESS_OPCYC_STATE
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: DemOperationCycleStatusStorage
  长名称: OperationCycle Status Storage
  描述: |
    Defines if the operation cycle state is available over the power cycle (stored non-volatile) or
    not.
    
    If this value is disabled, operation cycles are considered 'stopped' at the time of Dem_Init.
    Cycles must be started first to allow monitor reports to be processed, but starting a cycle
    involves event status changes.
    So if you have operation cycles that are longer than the power cycle of your ECU, you need to
    enable this option.
    
    This parameter is only valid if DemOperationCycleProcessing is set to OPCYC_STATE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: DemPTOSupport
  长名称: ''
  描述: |
    This configuration switch defines, whether PTO support (and therefore PID $1E support) is
    enabled or not.
    
    This parameter is not supported. Use parameter
    /Dem/DemConfigSet/DemEventParameter/DemEventClass/DemConsiderPtoStatus to configure an event as
    affected by PTO and activate the Dem PTO handling.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: DemResetConfirmedBitOnOverflow
  长名称: Status Bit ConfirmedDTC Reset on Overflow
  描述: |
    This configuration switch defines, whether the ConfirmedDTC UDS status bit is reset or not when
    an event memory entry will be displaced.
    
    If enabled, a DTC will immediately 'age', i.e. lose its ConfirmedDTC bit if it is displaced.
    
    If disabled, a DTC will stop aging on displacement. Its ConfirmedDTC status bit will stay active
    until the DTC can allocate a new aging counter, at which point the aging process will start from
    the beginning. Alternatively, ClearDTC will also clear such a DTC.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: DemStatusBitHandlingTestFailedSinceLastClear
  长名称: Status Bit TestFailedSinceLastClear Handling
  描述: |
    This configuration switch defines whether the aging and displacement mechanism shall be applied
    to the "TestFailedSinceLastClear" status bits.
    
    AGING_AND_DISPLACEMENT: The status bit 'TestFailedSinceLastClear' is only set if an event can be
    enteren into its event memory. (In case the event is not mapped to any destination it is never
    set!) The status bit is reset due to aging, clearing and displacement of the memory entry.
    
    NORMAL: The status bit 'TestFailedSinceLastClear' set for all events, irrespective of successful
    allocation of an event memory entry. It is reset to 0 only when the event is cleared.
    
    AGING: The status bit 'TestFailedSinceLastClear' set for all events, irrespective of successful
    allocation of an event memory entry. It is reset to 0 when the event ages, or is cleared.
    
  默认值: DEM_STATUS_BIT_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: DemStatusBitStorageTestFailed
  长名称: Status Bit TestFailed Storage
  描述: |
    Activate/Deactivate the permanent storage of the "TestFailed" status bits.
    
    If disabled, the TestFailed bit is reset during initilization.
    Please note that this does not suffice to start aging of the event.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: DemStorageConditionSupport
  长名称: StorageCondition Support
  描述: |
    This configuration switch defines, whether support for storage conditions is enabled or not.
    
    If storage conditions are set up for events
    (DemConfigSet/DemEventParameter/DemEventClass/DemStorageConditionGroupRef) this option must be
    enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 35
  名称: DemSuppressionSupport
  长名称: ''
  描述: |
    This configuration switch defines, whether support for suppression is enabled or not.
    According AUTOSAR 4.3, this DEM implementation only supports the suppression by DTC, not the
    suppression by Event.
    
    DTC_SUPPRESSION: Support suppression by DTC.
    
    EVENT_AND_DTC_SUPPRESSION: Support suppression by Event and DTC.
    Equivalent to DTC_SUPPRESSION, as  suppression by Event is not supported.
    
    EVENT_SUPPRESSION: Support suppression by Event.
    Equivalent to NO_SUPPRESSION, as  suppression by Event is not supported.
    
    NO_SUPPRESSION: Suppression is not supported.
    
  默认值: DEM_NO_SUPPRESSION
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: DemTaskTime
  长名称: ''
  描述: |
    Allow to configure the time for the periodic cyclic task.
    
    This value is used to set up the Dem Service-Description and BSW scheduler. This time is also
    used as time base in case time based debouncing is supported (see DemDebounceTimeBasedSupport,
    DemConfigSet/DemEventParameter/DemDebounceAlgorithmClass/DemDebounceTimeBased/DemDebounceTimeBasedClassRef).
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a diffenent unit.
  默认值: 0.01
  最小值: 0.001
  最大值: 0.1
- 
  序号: 37
  名称: DemTriggerDcmReports
  长名称: ''
  描述: |
    If enabled, the Dcm module is notified about DTC status changes in primary memory.
    Status changes caused by Dem_<...>ClearDTC do not trigger this callback. Notifications must be
    enabled using API Dem_DcmControlDTCStatusChangedNotification.
    
    For ASR4.0.3 compatible behavior, disable this option, and configure the Dcm trigger function in
    parameter 'DemCallbackDTCStatusChangedFnc'.
    
    This is required to implement RoE - OnDTCChange supervision, please refer to the Dcm
    configuration for details.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: DemTriggerDltReports
  长名称: ''
  描述: Activate/Deactivate the notification to the Diagnostic Log and Trace.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 39
  名称: DemTriggerFiMReports
  长名称: Trigger FiM Reports
  描述: |
    Activate/Deactivate the notification to the Function Inhibition Manager.
    
    This option must be enabled if the FiM requires monitor status change notification (see
    FiM/FiMGeneral/FiMEventUpdateTriggeredByDem).
    It enables MonitorStatusChange and FiM_DemInit according AR4.3.0.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: DemTriggerFiMReportsExtended
  长名称: Trigger FiM Reports (Extended)
  描述: |
    Activate/Deactivate the notification to the Function Inhibition Manager.
    
    This option must be enabled if the FiM requires event status change notification.
    It is used for Vector FiM's OBD extension, and also provides backward compatibility for older
    FiM version (ASR 4.2 and older)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: DemTriggerMonitorInitBeforeClearOk
  长名称: Trigger MonitorInit Before Clear Ok
  描述: |
    Defines if the monitor re-initialization has to be triggered before or after the Dem module
    returns DEM_CLEAR_OK.
    
    This option is not supported.
    InitMonitor callbacks are always triggered during the clear operation, and have completed before
    the final result is returned to the Dcm.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: DemTriggerMonitorInitForEnableConditions
  长名称: Trigger MonitorInit For Enable Conditions
  描述: |
    Defines if the monitor re-initialization is triggered when enable conditions re-activate a
    disabled monitor
    This option requires AR4.1.2 API compatibility.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 43
  名称: DemTypeOfDTCSupported
  长名称: ''
  描述: |
    This parameter defines the format returned by Dem_GetTranslationType and does not relate
    to/influence the supported Dem functionality.
    
    Its value is returned by some of the $19 services.
    
    ISO11992_4: ISO11992-4 DTC format.
    
    ISO14229_1: ISO14229-1 DTC format.
    
    ISO15031_6: ISO15031-6 DTC format/SAE J2012-DA_DTCFormat_00 DTC format.
    
    SAEJ1939_73: SAEJ1939-73 DTC format.
    
    J2012DA_FORMAT_04: SAE_J2012-DA_DTCFormat_04 DTC format.
  默认值: DEM_DTC_TRANSLATION_ISO14229_1
  最小值: ''
  最大值: ''
- 
  序号: 44
  名称: DemVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 45
  名称: DemBswApiVersion
  长名称: ''
  描述: |
    Specifies the AUTOSAR version of the integrated BSW stack API that Dem shall be able to interact
    with.
    
    This setting will modify the symbolic names, that are offered by the DEM and used by other BSW
    modules.
    See the additional parameters for the reverse (the DEM uses a symbolic name that is offered by
    another module): DemGeneral/DemBswApiVersionNvM, DemGeneral/DemBswApiVersionFiM.
    
    API_4_XX_XX: The DEM offers only symbolic names according the definition of AUTOSAR 4 for
    interaction with other BSW modules.
    
    API_3_XX_XX: The DEM creates additional symbolic names according the definition of AUTOSAR 3 for
    interaction with other BSW modules:
    The DEM itself will offer additional symbolic names (that may be used by AUTOSAR 3 BSW modules)
    for:
    - DemAgingCycle identifier
    - DemEnableConditionId
    - DemEventId
    - DemGroupDTCs
    - DemIndicatorID
    - DemMILGroup identifier
    - DemOperationCycle identifier
    - DemStorageConditionId
    
  默认值: DEM_BSW_API_4_XX_XX
  最小值: ''
  最大值: ''
- 
  序号: 46
  名称: DemBswApiVersionNvM
  长名称: Bsw Api Version NvM
  描述: |
    Specifies the AUTOSAR version of the integrated NvM API that Dem shall be able to interact with.
    
    Switches Dem interaction to the corresponding AUTOSAR version of NvM
    (DemNvRamBlockIdRef->NvMBlockDescriptor).
    
    API_4_XX_XX: The DEM uses symbolic names according the definition of AUTOSAR 4 for interaction
    with the NvM module. This is the default.
    
    API_3_XX_XX: The DEM uses symbolic names according the definition of AUTOSAR 3 for interaction
    with the NvM module. Use this setting when the NvM offers its symbolic names only according the
    AUTOSAR 3 naming convention (for example AUTOSAR 3 "NvM_DemAdminDataBlock" vs. AUTOSAR 4
    "NvMConf_NvMBlockDescriptor_DemAdminDataBlock").
    
  默认值: DEM_BSW_API_4_XX_XX
  最小值: ''
  最大值: ''
- 
  序号: 47
  名称: DemBswApiVersionFiM
  长名称: Bsw Api Version FiM
  描述: |
    Specifies the AUTOSAR version of the integrated FiM API that Dem shall be able to interact with.
    
    Switches Dem interaction to the corresponding AUTOSAR version of FiM (DemFunctionIdRef->FiMFID,
    DemSecondaryFunctionIdRef->FiMFID, DemIgnitionCycleFunctionIdRef->FiMFID).
    
    API_4_XX_XX: The DEM uses symbolic names according the definition of AUTOSAR 4 for interaction
    with the FiM module. This is the default.
    
    API_3_XX_XX: The DEM uses symbolic names according the definition of AUTOSAR 3 for interaction
    with the FiM module. Use this setting when the FiM offers its symbolic names only according the
    AUTOSAR 3 naming convention (for example AUTOSAR 3 "FiM_FiMFID_001" vs. AUTOSAR 4
    "FiMConf_FiMFID_FiMFID_001").
    
  默认值: DEM_BSW_API_4_XX_XX
  最小值: ''
  最大值: ''
- 
  序号: 48
  名称: DemAgingAfterHealing
  长名称: ''
  描述: |
    This parameter selects how aging and healing interact.
    
    DEM_AGING_WHILE_HEALING will allow events that meet the configured aging criteria
    (DemAgingBehavior) to start aging.
    In theory, this could mean that events can age while they still request an indicator. Use well
    defined operation cycles to avoid this effect, i.e. aging cycles should not complete faster than
    operation cycles.
    
    DEM_AGING_AFTER_HEALING will allow aging only after the event has finished healing, i.e. after
    resetting the warningIndicatorRequested status bit. This setting only has an effect on events
    with an indicators. This is the behavior defined by the AUTOSAR standard.
    
    DEM_AGING_AFTER_HEALING_ALL_DTC behaves like DEM_AGING_AFTER_HEALING, but extends the healing
    process to events without indicator. I.e. even though the events do not set the WIR bit, they
    will only start aging after they would have reset it. This way, both events with and without
    indicators age after the same amount of cycles.
    
    Events configured to use the MIL will always behave according to DEM_AGING_AFTER_HEALING.
  默认值: DEM_AGING_WHILE_HEALING
  最小值: ''
  最大值: ''
- 
  序号: 49
  名称: DemAgingBehavior
  长名称: ''
  描述: |
    This parameter selects the algorithm for the aging of the events.
    
    AGING_TYPE_1: Initial trigger to start the aging is the test result PASSED.
    The aging counter is incremented at the end of the aging cycle.
    Events with DemAgingCycleCounterThreshold == 0 will age with the PASSED test result.
    
    AGING_TYPE_2: Initial trigger to start the aging is the end of operation cycle if the event was
    tested PASSED and was never tested FAILED in this cycle.
    The aging counter is incremented at the end of the aging cycle.
    Events with DemAgingCycleCounterThreshold == 0 will age at the end of the operation cycle if the
    event was tested PASSED and was not tested FAILED in this cycle.
    
    AGING_TYPE_3: Initial trigger to start the aging is the end of operation cycle if the event was
    tested PASSED and was never tested FAILED in this cycle.
    The aging counter is incremented at the end of the aging cycle if the event was tested PASSED
    and was never tested FAILED in this cycle.
    Events with DemAgingCycleCounterThreshold == 0 will age at the end of the operation cycle if the
    event was tested PASSED and was not tested FAILED in this cycle.
    
    AGING_TYPE_4: Initial trigger to start the aging is the test result PASSED.
    The aging counter is incremented at the end of the aging cycle if the event was tested PASSED.
    Events with DemAgingCycleCounterThreshold == 0 will age with the PASSED test result.
    
    AGING_TYPE_5: Initial trigger to start the aging is the end of operation cycle if the event was
    tested PASSED and was never tested FAILED in this cycle.
    The aging counter is incremented at the end of the aging cycle if the event was tested PASSED
    and was never tested FAILED in this cycle.
    Events with DemAgingCycleCounterThreshold == 0 will age with the PASSED test result, if the
    event was not tested FAILED in this cycle.
    
    AGING_TYPE_6: Initial trigger to start the aging is the test result PASSED, if the event was
    never tested FAILED in this cycle.
    The aging counter is incremented at the end of the aging cycle if the event was tested PASSED
    and was never tested FAILED in this cycle.
    Events with DemAgingCycleCounterThreshold == 0 will age with the PASSED test result.
    
  默认值: DEM_AGING_TYPE_1
  最小值: ''
  最大值: ''
- 
  序号: 50
  名称: DemAgingCounterBehavior
  长名称: ''
  描述: |
    Control whether an aging counter is incremented / decremented for events that do not support
    aging (refer to DemAgingAllowed).
    
    DEM_AGING_COUNT_ALWAYS: The aging counter is incremented/decremented for every event. If an
    event does not support aging (DemAgingAllowed is set to false), its incrementing aging counter
    latches at aging cycle counter threshold and decrementing aging counters stops at 0.
    
    DEM_AGING_COUNT_ONLY_AGEABLE: The aging counter is incremented/decremented only for events
    supporting aging. If an event does not support aging, incrementing aging counters remain at 0,
    decrementing aging counters remain at the aging cycle counter threshold value.
  默认值: DEM_AGING_COUNT_ALWAYS
  最小值: ''
  最大值: ''
- 
  序号: 51
  名称: DemAgingCounterReporting
  长名称: ''
  描述: |
    This parameter changes how the aging counter is reported in an extended record.
    
    AGING_NORMAL_REPORTING:
    The counter is reported as defined by the internal data element (UPCOUNT/DOWNCOUNT)
    
    AGING_ZERO_AS_ONE_REPORTING:
    For upward counting, the counter value 0x00 is reported as value 0x01 in the cycle where aging
    is started.
    This has no effect on downward counting and on events with aging cycle counter threshold 0.
  默认值: DEM_AGING_NORMAL_REPORTING
  最小值: ''
  最大值: ''
- 
  序号: 52
  名称: DemAgingRetainEnvironmentalData
  长名称: ''
  描述: |
    If this option is enabled, environmental data stored with a DTC is not deleted on aging.
    
    This includes snapshot data and extended data records.
    The data is reported for UDS services as if the DTC was still confirmed, although Bit3 is not
    set anymore in the DTC status byte.
    Aged event entries will be treated as empty as far as displacment is concerned, even if DTC
    displacement is deactivated by DemEventDisplacementStategy.
    
    If this option is disabled, event memory entries including all stored data are cleared on aging.
    This setting corresponds to the behavior defined by AUTOSAR.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 53
  名称: DemClearDTCRuntimeLimit
  长名称: ClearDTC Runtime Limit
  描述: |
    If this parameter exists, ClearDTC will not clear more than this amount of DTCs at once.
    
    This parameter can be used to reduce the run time of the Dem_MainFunction during ClearDTC.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 54
  名称: DemCompiledConfigId
  长名称: ''
  描述: |
    Change this value to force the Dem to clear all NV data on next initialization (startup).
    
    This is useful if the flash eeprom emulation is not cleared during flashing of a new software
    version.
    When this parameter is missing, the value 0 is assumed.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 55
  名称: DemCompiledPostbuildCrc
  长名称: ''
  描述: |
    This parameter contains a variant specific checksum (CRC) over all postbuiild-changeable
    configuration items. This value is internally used to detect changes in the configuration.
    
    The non-volatile stored data is always configuration specific. Reading the NvData with a
    different configuration will give a new interpretation to that binary data, that is usually
    wrong. So with configuration changes the DEM shall typically discard the previous NvData.
    
    In mode AUTOMATIC (see parameter DemCompiledPostbuildCrcMode) the DaVinci Configurator5 will
    automatically evaluate a checksum over the relevant data, that will differ between incompatible
    configurations.
    
    In mode MANUAL the user himself is responsible to use different values for incompatible
    configurations.
    
    Generally: a value here, that is different from the previous value (that was used when storing
    the non-volatile data) will cause the DEM to discard the previously stored NvData.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 56
  名称: DemCompiledPostbuildCrcMode
  长名称: ''
  描述: |
    Switch the mode for the calculation of the variant specific checksum (CRC) over all
    postbuiild-changeable configuration items.
    See parameter DemCompiledPostbuildCrc.
    
    AUTOMATIC: the DaVinci Configurator5 calculates the checksum value
    
    MANUAL: the user defines the checksum - use this setting only when the NvData shall not be
    cleared with a configuration change. Take care to manually change the checksum when the stored
    non-volatile data becomes incompatible to the current configuration.
  默认值: DEM_POSTBUILD_CRC_AUTOMATIC
  最小值: ''
  最大值: ''
- 
  序号: 57
  名称: DemDcmSupport
  长名称: ''
  描述: |
    When this parameter is missing, the Dem assumes the Dcm being configured (that means you use a
    standard AUTOSAR stack).
    
    If the parameter exists with value FALSE there is no Dcm module in the system: the Dem doesn't
    offer the APIs defined in file "Dem_Dcm.h" any more, and it does not offer the Dcm port
    interfaces. Use this setting when your ECU doesn't implement UDS diagnostic services. A J1939Dcm
    in system will then still offer J1939 diagnostic services.
    
    If the parameter exists with value TRUE (or is missing) the standard Dem behaviour and APIs are
    available.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 58
  名称: DemDebounceTimeLowResThreshold
  长名称: TimeBased Debouncing - LowRes Timer Threshold
  描述: |
    Largest time duration (excl.) for using the high resolution timer.
    
    To reduce CPU load and reduce configuration code size, the feature Time Base Debounce can use 2
    different timers: the high resolution timer will tick with the configured DemTaskTime (typ.
    10ms), the additional low resolution timer will tick with 150ms.
    
    This configuration value defines the min. debounce time for an event to be handled by the
    low-res timer. Default: 5s
    
    Refer to configuration values DemDebounceTimeFailedThreshold and DemDebounceTimePassedThreshold
    of each event:
    - if both time values of an event are lower than the threshold (typ. 5s), the event's debounce
    is using the high-res timer with a jitter of DemTaskTime (typ. 10ms);
    - otherwise the debounce algorithms are using the low-res timer (with a jitter of 150ms) and a
    reduced CPU load.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the GUI will convert the value when using a diffenent unit.
  默认值: 5
  最小值: 0.15
  最大值: 3600
- 
  序号: 59
  名称: DemEvMemOverflowIndicationSupport
  长名称: EventMemory Overflow Indication Support
  描述: |
    Provide the Port-Interface EvMemOverflowIndication.
    
    If this parameter is disabled, the Dem will not provide the port interface or the C functions to
    read the overflow status of the event memories.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 60
  名称: DemEventDisplacementFallbackStrategy
  长名称: ''
  描述: |
    Fallback strategy for event displacement:
    
    DISCARD_NEW_EVENT:
    Standard behavior defined by AUTOSAR. In case no candidate for displacement is found, a new
    event is silently discarded.
    
    DISPLACE_OLDEST_EVENT:
    In case no better candidate for displacement can be found, the oldest event is displaced
    unconditionally.
    Note: Active OBD DTCs are not affected from this configuration.
    
  默认值: DEM_FALLBACK_DISCARD_NEW_EVENT
  最小值: ''
  最大值: ''
- 
  序号: 61
  名称: DemGeneralCallbackMonitorStatusChangedFnc
  长名称: General Callback MonitorStatus Changed Fnc
  描述: |
    Function name of prototype "<Module>_DemTriggerOnMonitorStatus".
    
    If configured, the DEM will call this function with each MonitorStatus change of an event.
    The function's signature is:
    void NN_DemTriggerOnMonitorStatus( Dem_EventIdType EventId );
    
    For FiM monitor status notification, use the configuration parameter
    DemGeneral/DemTriggerFiMReports.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 62
  名称: DemGeneralDiagnosticInfoSupport
  长名称: General DiagnosticInfo Support
  描述: Provide the Port-Interface GeneralDiagnosticInfo.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 63
  名称: DemImmediateNvStorageSupport
  长名称: ImmediateNvStorage Support
  描述: |
    TRUE: For all DTCs for which DemConfigSet/DemDTCClass/DemImmediateNvStorage parameter is
    enabled, environmental data is stored immediately in NvRam.
    Independent of the value of DemConfigSet/DemDTCClass/DemImmediateNvStorage OBD relevant data
    (OBD freeze frames and permanent DTCs) is always synchronized to NvRAM immediately.
    
    FALSE or when this parameter is missing: If at least one of the following conditions is
    fulfilled, the feature will be switched on (same behavior as TRUE):
    - at least one of the DemConfigSet/DemDTCClass/DemImmediateNvStorage parameters is enabled
    -  DemGeneral/DemNvSynchronizeSupport is set to TRUE
    -  DemGeneral/DemClearDTCBehavior is set to DEM_CLRRESP_NONVOLATILE_FINISH
    Otherwise the feature is disabled.
    
    Note: Immediate storage of other data (e.g., event status, IUMPR, DTR) than environmental data
    is not triggered by enabling this option.
    For more details regarding NvRAM synchronization see chapters 'NVRAM Write Frequency' in
    Technical Reference and Addendum for OBD.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 64
  名称: DemJ1939Support
  长名称: ''
  描述: |
    Globally activate the support for J1939.
    
    If this feature is active, the configuration of J1939 in container DemGeneral/DemGeneralJ1939 is
    mandatory.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 65
  名称: DemMemoryBlockDistribution
  长名称: ''
  描述: This parameter has no effect
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 66
  名称: DemMultipleTripSupport
  长名称: ''
  描述: |
    FALSE: Multitrip behavior is not allowed for any event.
    DemConfigSet/DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold has to be 0 or
    1.
    TRUE:  Multitrip behavior is possible, but not mandatory, i.e. confirmation handling is still
    according to the settings of
    DemConfigSet/DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold. Trip counter
    information is  available for all events.
    
    Example: If all events have a single trip behavior, enabling MultipleTripSupport  may be useful
    for configuration variants, e.g. to calibrate a different value for
    DemEventFailureCycleCounterThreshold later.
    When this parameter is missing, the Dem will select the confirmation handling according to the
    settings of DemConfigSet/DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold or
    DemConfigSet/DemEventParameter/DemEventClass/DemIndicatorAttribute/DemIndicatorHealingCycleCounterThreshold.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 67
  名称: DemNvSynchronizeSupport
  长名称: ''
  描述: |
    Provides API Dem_RequestNvSynchronization.
    
    If this option is enabled, API Dem_RequestNvSynchronization is provided which can be used to
    request full NV synchronization. For SWC, the API is available as operation SynchronizeNvData in
    port interface DemServices.
    
    Use this API in case the AUTOSAR defined synchronization points do not suffice for your project.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 68
  名称: DemPendingDtcProcessing
  长名称: Status Bit PendingDTC Processing
  描述: |
    Select behavior of PendingDTC status bit.
    
    STOREDONLY: Set the status bit2 (PendingDTC) only if a memory entry could be allocated
    successfully. With this setting the status bit PendingDTC is also reset when the event is
    displaced from memory.
    
    ALL_DTC: Set the status bit2 (PendingDTC) independently from successful event storage. With this
    setting the status bit PendingDTC is not modified in case the DTC is displaced from memory.
    
  默认值: DEM_PROCESS_PDTC_STOREDONLY
  最小值: ''
  最大值: ''
- 
  序号: 69
  名称: DemResetDebounceBehavior
  长名称: ''
  描述: |
    Controls which enable condition group transition leads to a reset/freeze of the debouncing
    behaviour, either with the state trasition to enabled or disabled.
    
    DEM_RESET_DEBOUNCE_ON_DISABLE_ENABLE_CONDITIONS
    Reset/freeze the debouncing values when the events preconditions are no longer fulfilled.
    
    DEM_RESET_DEBOUNCE_ON_ENABLE_ENABLE_CONDITIONS
    Reset/freeze the debouncing values when the events preconditions return to fulfilled state,
    after they had been unfulfilled.
    However, if /Dem/DemConfigSet/DemDebounceTimeBasedClass/DemDebounceContinuous == FALSE, then the
    debounce value is frozen,  when the events preconditions are no longer fulfilled.
  默认值: DEM_RESET_DEBOUNCE_ON_DISABLE_ENABLE_CONDITIONS
  最小值: ''
  最大值: ''
- 
  序号: 70
  名称: DemResetTestFailedOnOperationCycleStart
  长名称: Reset TestFailed on OperationCycle Start
  描述: |
    If this option is enabled, (re)starting an operation cycle also resets the TestFailed bit of
    events using the cycle as operation cycle.
    This is not counted as a qualified test result.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 71
  名称: DemRetryStorageSupport
  长名称: ''
  描述: |
    When enabled, the Dem will retry to store events that could not be stored; e.g. due to missing
    storage conditions, or filled up event memory.
    An attempt to store is triggered for FAILED DTCs (Bit0 set) with every PRE_FAILED report (while
    the FDC is at 128) or FAILED report.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 72
  名称: DemSafeBswChecks
  长名称: SafeBSW Checks
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. By default, this parameter is enabled. For
      projects where this component is not mapped to an ASIL partition, this parameter could
      be disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 73
  名称: DemTriggerControlDTCSetting
  长名称: Trigger ControlDTCSetting
  描述: |
    The application is triggered if diagnostic service 0x85 - ControlDtcSetting is processed in DEM.
    In case the ECU does not support an RTE (DemUseRte == False), the Dem calls function
    Appl_Dem_CBControlDTCSetting_ControlDTCSettingChanged, which must be supplied by the application
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 74
  名称: DemTriggerDtcStatusChangedCallback
  长名称: Trigger DtcStatusChanged Callback
  描述: |
    Globally disable DTC status notifications.
    
    You can use this parameter to suppress all dtc status notification callbacks, usually because
    none are used in the first place.
    You can also use this parameter as a temporary measure to allow compilation until all
    notification callouts are actually available.
    
    If you want notifications, it is recommended to remove the parameter completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 75
  名称: DemTriggerEventDataChangedCallback
  长名称: Trigger EventDataChanged Callback
  描述: |
    Globally disable DTC data change notifications.
    
    You can use this parameter to suppress all data change notification callbacks, usually because
    none are used in the first place.
    You can also use this parameter as a temporary measure to allow compilation until all
    notification callouts are actually available.
    
    If you want notifications, it is recommended to remove the parameter completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 76
  名称: DemTriggerEventStatusChangedCallback
  长名称: Trigger EventStatusChanged Callback
  描述: |
    Globally disable event status notifications.
    
    You can use this parameter to suppress all event status notification callbacks, usually because
    none are used in the first place.
    You can also use this parameter as a temporary measure to allow compilation until all
    notification callouts are actually available.
    
    If you want notifications, it is recommended to remove the parameter completely.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 77
  名称: DemTriggerGlobalEventDataChangedCallback
  长名称: Trigger GlobalEventDataChanged Callback
  描述: |
    If this parameter exists, you can explicitly control if the Dem requires the port interface
    'GlobalEventDataChanged' (set: True) or not (set: False).
    It is used as a 'one for all' callout in case event data changes.
    
    If this parameter is missing (not set), the global interface is always required in addition to
    any DemConfigSet/DemEventParameter/DemCallbackEventDataChanged callout as demanded by AUTOSAR.
    
    This parameter here is irrelevant, if parameter DemGeneral/DemTriggerEventDataChangedCallback
    exists and has value False.
    
    In case the ECU does not support an RTE (DemUseRte == False), the Dem calls function
    Appl_Dem_GeneralCBDataEvt_EventDataChanged, which must be supplied by the application.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 78
  名称: DemTriggerGlobalEventStatusChangedCallback
  长名称: Trigger GlobalEventStatusChanged Callback
  描述: |
    If this parameter exists, you can explicitly control if the port interface
    'GlobalEventStatusChanged' will be required (set: True) or not (set: False) by the Dem.
    It is used as a 'one for all' callout in case event status changes.
    
    If this parameter is missing (not set), the global interface is always required in addition to
    any DemConfigSet/DemEventParameter/DemCallbackEventStatusChanged callout as demanded by AUTOSAR.
    
    This parameter here is irrelevant, if parameter DemGeneral/DemTriggerEventStatusChangedCallback
    exists and has value False.
    
    In case the ECU does not support an RTE (DemUseRte == False), the Dem calls function
    Appl_Dem_GeneralCBStatusEvt_EventStatusChanged, which must be supplied by the application.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 79
  名称: DemUseMemcopyMacros
  长名称: ''
  描述: |
    Control use of VStdLib.
    
    If this switch is enabled, the Dem implementation uses macro implementations for memcopy and
    memset routines.
    
    These macros can be defined within a user config file (see DemUserConfigFile) if so desired:
    #define Dem_MemCpy_Macro(dst, src, len) /* some implementation */
    #define Dem_MemSet_Macro(dst, val, len) /* some implementation */
    If no definition is given by user config file, the Dem automatically uses a default
    implementation.
    
    If the switch is disabled, VStdLib is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 80
  名称: DemUseNvm
  长名称: ''
  描述: |
    When this parameter is missing, the Dem will determine if it uses nonvolatile memory blocks
    based on the configuration of DemNvRamBlockId containers.
    If the configuration of the containers is incorrect, NvM usage will be deactivated which is also
    indicated by a warning during generation.
    If the configuration of the containers is correct, NvM usage will be active.
    
    If NvM usage is deactivated, the Dem will not report modified blocks to the NvM and will run
    completely from RAM mirrors without persistence. All features concerning NV memory will not be
    available.
    
    If the parameter exists, you can control manually if NvM usage is active.
    This can be useful in early integration phases where you have not yet completely set up the NvM
    but still need the Dem for production error reporting of the communication stack.
    Creating and manually setting this parameter is discouraged in production ECUs, i.e., the
    parameter should not exist in production ECUs. It is expected that the NvM shall be set up
    completely for production and the configuration of DemNvRamBlockId containers is correct.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 81
  名称: DemUseRte
  长名称: ''
  描述: |
    Set to FALSE to disable the usage of RTE callbacks.
    
    If disabled, all callouts are replaced by direct function calls. This is supported only for ECUs
    with neither RTE nor BRE.
    If the ECU uses an RTE or BRE, this option must be enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 82
  名称: DemUserConfigFile
  长名称: User Configuration File
  描述: |
    Path to an external user configuration file used by the DaVinci Configurator 5 generation tool.
    
    If you want to overwrite some of the settings in the generated configuration file (Dem_Cfg.h),
    you can specify a path to a user defined configuration file. The user defined configuration file
    will be included at the end of the generated preprocessor switches. Definitions in the user
    defined configuration file can overwrite definitions in the generated configuration file.
    
    To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such
    sequence is replaced by the content of the related environment variable "var".
    Additionally you can use following predefined sequences:
    $(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
    $(EcuProjectName) Name of the project defined in the loaded *.dpa file.
    $(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files
    $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
    $(EcucFolder) Parent directory of $(EcucFile).
    $(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
    $(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting
    "Root Target Folder" of Configurator 5.
    $(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
    $(cwd) Current working directory when starting Configurator 5.
    
    RESTRICTIONS: Not all of the settings can be overwritten simply by triggering the preprocessor
    switch. Some of the options are complex and the code generator generates less or more code
    depending on the setting.
    
    USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 83
  名称: DemUserConfigFilePost
  长名称: User Configuration File - Late Inclusion
  描述: |
    Path to an external user configuration file used by the DaVinci Configurator 5 generation tool.
    
    If you want to overwrite some of the settings in the generated configuration file (Dem_LCfg.h),
    you can specify a path to a user defined configuration file. The user defined configuration file
    will be included at the end of the file. Definitions in the user defined configuration file can
    overwrite definitions in the generated configuration file.
    
    To specify the file name, you can use "$(var)" sequence(s) in the specified path. Each such
    sequence is replaced by the content of the related environment variable "var".
    Additionally you can use following predefined sequences:
    $(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
    $(EcuProjectName) Name of the project defined in the loaded *.dpa file.
    $(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files
    $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
    $(EcucFolder) Parent directory of $(EcucFile).
    $(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
    $(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting
    "Root Target Folder" of Configurator 5.
    $(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.
    $(cwd) Current working directory when starting Configurator 5.
    
    RESTRICTIONS: Usually it is sufficient to use only the DemUserConfigFile. This option should be
    only used with extreme caution.
    
    USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 84
  名称: DemUserControlledWirBehavior
  长名称: Status Bit WarningIndicatorRequest User Controlled Behavior
  描述: |
    This setting has effect only when DemUserControlledWirSupport == True. (Status Bit
    WarningIndicatorRequest User Controlled == True)
    
    DISABLED_DURING_CONTROLDTCSETTING: The API Dem_SetWIRStatus will return E_NOT_OK while
    ControlDTCSetting has disabled DTC storage.
    
    ENABLED_DURING_CONTROLDTCSETTING
    Dem_SetWIRStatus will process changes while ControlDTCSetting has disabled DTC storage.
  默认值: DEM_ENABLED_DURING_CONTROLDTCSETTING
  最小值: ''
  最大值: ''
- 
  序号: 85
  名称: DemUserDefinedCompareAndSwap
  长名称: ''
  描述: |
    Implement and use a hardware optimized ApplDem_SyncCompareAndSwap() function.
    
    The API ApplDem_SyncCompareAndSwap(uint32* AddressPtr, uint32 OldValue, uint32 NewValue)
    performs an atomic compare and swap of memory contents.
    If disabled, the DEM uses an internal implementation, that needs the critical section
    'CrossCoreComm'.
    If enabled, the DEM uses an external implementation.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 86
  名称: DemUserControlledWirSupport
  长名称: Status Bit WarningIndicatorRequest User Controlled
  描述: |
    Activate the external modifiability of the WarningIndicatorRequest Status Bit.
    
    If this option is enabled, the API Dem_SetWIRStatus is provided, which allows the user to
    override the current WarningIndicatorRequest Bit of the DTC status.
    Additionally, the API Dem_GetWIRStatus can be used the read the current override status (WIR
    controlled / not controlled by user).
    
    If this option is disabled, overriding the WarningIndicatorRequest Bit is deactivated, and the
    APIs Dem_SetWIRStatus and Dem_GetWIRStatus are not available.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 87
  名称: DemWarningIndicatorRequestedProcessing
  长名称: Status Bit WarningIndicatorRequested Processing
  描述: |
    Select behavior of WarningIndicatorRequested status bit.
    
    STOREDONLY: Set the status bit7 (WarningIndicatorRequested) only if a memory entry could be
    allocated successfully.
    
    ALL_DTC: Set the status bit7 (WarningIndicatorRequested) independently from successful event
    storage.
    
    Independent of the selected behavior the status bit 7 is not cleared due to displacement.
    
    
  默认值: DEM_PROCESS_WIR_STOREDONLY
  最小值: ''
  最大值: ''
- 
  序号: 88
  名称: DemUseMultiPartitionFiM
  长名称: Use Multi Partition FiM
  描述: |
    This configuration switch defines, whether a Multi Partition FiM is used.
    
    If this parameter is enabled, the Dem calls the APIs FiM_DemInitMaster and FiM_DemInitSatellite
    instead of FiM_DemInit during initialization.
    
    This parameter is only relevant, if the FiM is notified about monitor status changes (see
    Dem/DemGeneral/DemTriggerFiMReports).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 89
  名称: DemReportSuppressedDTCsInService19x0A
  长名称: Report Suppressed DTCs In Service 19x0A
  描述: |
    If this parameter is enabled, suppressed DTCs are reported in UDS service $19 0A.
    
    If this parameter is disabled, suppressed DTCs are not reported in UDS service $19 0A.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 90
  名称: DemSupportAgingForAllDTCs
  长名称: Support Aging For All DTCs
  描述: |
    If this parameter is enabled, all DTCs can age independently of a memory entry.
    
    If this parameter is disabled, only DTCs with a memory entry can age.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 91
  名称: DemSupportStorageIndependentCycleCounters
  长名称: Event Storage Independent Cycle Counters
  描述: |
    If this parameter is enabled, Dem internal data elements FAILED_CYCLES and FAULT_PENDING_COUNTER
    are calculated and reported independently of an event memory entry (if configured for event).
    
    When activating this feature, the configuration needs an additional NV-RAM block with
    DemNvRamBlockIdType "DEM_NVBLOCK_CYCLECOUNTER". Additional two bytes per DTC are required for
    NVRAM.
    
    If this parameter is disabled or does not exist, the counters are only tracked and reported if
    the event has a memory entry.
    
    Set Dem/DemGeneral/DemExtendedDataVisibility to 'ALL_DTC' for full benefit of this feature.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 92
  名称: DemLatchTestFailedBehavior
  长名称: ''
  描述: |
    Defines the behavior of events that have DemConfigSet/DemEventParameter/DemEventLatchTestFailed
    enabled.
    
    DEM_LATCH_TF_ONLY_THIS_CYCLE:
    After a qualified FAILED result, a PASSED result for the event is ignored during the current
    operation cycle.
    
    DEM_LATCH_TF_CONFIRMED_AND_THIS_CYCLE:
    After a qualified FAILED result, a PASSED result for the event is ignored during the current
    operation cycle. Additionally if the event is confirmed, no PASSED result is processed for that
    event until it is cleared. As a consequence, the event cannot age.
  默认值: DEM_LATCH_TF_CONFIRMED_AND_THIS_CYCLE
  最小值: ''
  最大值: ''
- 
  序号: 93
  名称: DemSupportExtendedFiM
  长名称: Support Extended FiM
  描述: |
    This configuration switch defines whether the extended communication between FiM and Dem is
    enabled.
    
    When enabled, the extended status byte, in addition to the DTC status byte, and the APIs for the
    extended status byte handling, namely Dem_GetSI30Status() and Dem_SetSI30Symptom(), are
    supported. The DEM also invokes the extended FiM API FiM_DemTriggerOnUnconfirmed() when the
    event reaches the storage threshold.
    
    Precondition: If the extended communication between FiM and Dem is enabled, support for
    Powertrain features must be enabled (/Dem/DemGeneral/DemSupportPowertrain == true).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 94
  名称: DemSupportService19x16
  长名称: Support Service 19x16
  描述: If this parameter is enabled, subfunction 0x16 (reportDTCExtDataRecordByRecordNumber) of UDS
      service 0x19 (ReadDTCInformation) is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 95
  名称: DemSupportPowertrain
  长名称: Support Powertrain
  描述: This configuration switch defines whether Powertrain features are enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 96
  名称: DemSupportService19x56
  长名称: Support Service 19x56
  描述: |
    If this parameter is enabled, subfunction 0x56
    (reportDTCInformationByDTCReadinessGroupIdentifier) of UDS service 0x19 (ReadDTCInformation) is
    supported.
    Subfunction 0x56 provides a list of OBD relevant DTCs and their UDS status information for a
    requested readiness group.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 97
  名称: DemDevFreezeFrameSupport
  长名称: Support Development Freeze Frame
  描述: If this parameter is enabled, the following development snapshot records are supported: time
      series snapshot records (also known as multi-sample development snapshot records).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 98
  名称: DemSupportService19x1A
  长名称: Support Service 19x1A
  描述: |
    If this parameter is enabled, subfunction 0x1A (reportSupportedDTCExtDataRecord) of UDS service
    0x19 (ReadDTCInformation) is supported.
    
    Subfunction 0x1A provides a list of all DTCs and their UDS status that are configured for a
    requested Extended Data Record.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 99
  名称: DemSupportService19x04DIDLength
  长名称: Support Service 19x04 DID Length
  描述: |
    If this parameter is enabled, in the service 19x04 response an additional byte is added for each
    data identifier (DID) containing the size of the DID.
    This additional size byte is located between the DID and the DID data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 100
  名称: DemCalibrationSupport
  长名称: Calibration Support
  描述: |
    If this parameter is set to true, the Dem supports calibration. The calibratable parameters can
    be specified via Dem/DemGeneral/DemGeneralCalibration.
    
    If this parameter is set to false, all configuration options under
    Dem/DemGeneral/DemCalibrationGeneral will be ignored.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 101
  名称: DemSupportStorageIndependentMaxFDCSinceLastClear
  长名称: Event Storage Independent Max FDC Since Last Clear
  描述: |
    If this parameter is enabled, the Dem internal data element MAX_FDC_SINCE_LAST_CLEAR (if
    configured for the event) is calculated and stored independently of an event memory entry. In
    order for the data element to be reported for all DTCs independent of an existing memory entry,
    Dem/DemGeneral/DemExtendedDataVisibility must be set to ALL_DTC.
    
    If this parameter is enabled, the data element is stored in the Admin data block instead of in
    the memory entry and one additional byte per DTC is required for NVRAM.
    
    If this parameter is disabled or does not exist, MAX_FDC_SINCE_LAST_CLEAR is only tracked and
    reported if the event has a memory entry.
  默认值: false
  最小值: ''
  最大值: ''
```

### 25. DemAgingCycle

**描述**: Aging cycles are not supported.
Use OperationCycles instead.

该容器没有参数。

### 26. DemCallbackDTCStatusChanged

**描述**: The presence of this container sets up a callout function 'DTCStatusChanged' for this DTC. The Dem
will call this function each time a DTC status changes.

This function is usually called through a RTE port interface.
This behavior can be changed by creating the sub-parameter 'DemCallbackDTCStatusChangedFnc'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackDTCStatusChangedFnc
  长名称: Callback DTCStatusChanged Function
  描述: |
    Function name of a 'DTCStatusChanged' callout.
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 27. DemClient

**描述**: This container contains possible clients that are using the Dem APIs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemClientId
  长名称: ''
  描述: Defines a unique identifier for a Dem client. This number is used by this client in the
      ClientID parameter in all API with this parameter.
  默认值: 254
  最小值: 0
  最大值: 254
```

### 28. DemDataClass

**描述**: This container groups the configuration (parameters) of a data element.

Data elements are used to build DIDs, PIDs and ExtendedDataRecords

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataElementDataSize
  长名称: DataElement Data Size
  描述: |
    Defines the size of the data element in bytes.
    
    For Dem-internal data elements, the size shall be predefined according to the selected internal
    data element (see Dem/DemGeneral/DemDataClass/DemDataElementInternalData).
    
    For Dem-external data elements, the size depends on the data type and number of elements which
    needs to be stored.
    For array data classes, this field must contain the total size of the array in bytes. An example
    is provided below.
    
    BOOLEAN is a 8 bit data type and therefore needs 1 byte.
    UINT8, SINT8, UINT8_N and SINT8_N are 8 bit data types and therefore need 1 bytes per element.
    UINT16, SINT16, UINT16_N and SINT16_N are 16 bit data types and therefore need 2 bytes per
    element.
    UINT32, SINT32, UINT32_N and SINT32_N are 32 bit data types and therefore need 4 bytes per
    element.
    FLOAT and FLOAT_N entries are 32 bit data types and therefore need 4 bytes per element.
    
    Example: For example if an UINT16_N array data type is selected, of which 4 entries need to be
    stored, than a data size of 8 bytes needs to be allocated.
    
    
  默认值: ''
  最小值: 1
  最大值: 4096
- 
  序号: 2
  名称: DemDataElementDataType
  长名称: ''
  描述: |
    Provide the implementation data type of data belonging to a external data.
    
    For DemDataElementDataSize > 1 the configured data type UINT8/SINT8 is treated as
    UINT8_N/SINT8_N to establish compatibility with the DCM.
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
- 
  序号: 4
  名称: DemDataElementInternalData
  长名称: Internal DataElement
  描述: |
    Select the Dem-internal data value, which is mapped to the data element.
    
    AGINGCTR / AGINGCTR_UPCNT: (1 Byte) Current value of the aging counter, counting from
    1...DemAgingCycleCounterThreshold. The value latches at aging counter threshold (refer to
    DemGeneral/DemAgingCounterBehavior).
    If DemGeneral/DemSupportAgingForAllDTCs is disabled, this value is processed and readable only
    for currently stored events.
    If DemGeneral/DemSupportAgingForAllDTCs is enabled, depending on the configuration, this value
    is always readable (refer to Dem/DemGeneral/DemExtendedDataVisibility).
    
    AGINGCTR_INVERTED / AGINGCTR_DOWNCNT: (1 Byte) Current value of the aging counter, counting
    backwards from the configured aging cycle counter threshold value down to 0. If
    DemGeneral/DemSupportAgingForAllDTCs is disabled, this value is processed and readable only for
    currently stored events.
    If DemGeneral/DemSupportAgingForAllDTCs is enabled, depending on the configuration, this value
    is always readable (refer to Dem/DemGeneral/DemExtendedDataVisibility).
    
    OCCCTR: (1 Byte) Current value of the occurrence counter, counting from 1...255. The value is
    incremented on each transition of the TestFailed Bit from 0 to 1 and latches at 255. This value
    is processed and readable only for currently stored events.
    
    OCCCTR_2BYTE: (2 Byte) Current value of the occurrence counter, counting from 1...65535. The
    value is incremented on each transition of the TestFailed Bit from 0 to 1 and latches at 65535.
    This value is processed and readable only for currently stored events.
    
    OVFLIND: (1 Byte) Value 1 if the primary memory has overflown, 0 otherwise. Will be reset on
    ClearAllDTC request. This value is always available.
    
    SIGNIFICANCE: (1 Byte) Value 0 if the event is configured as OCCURRENCE, 1 if the event is
    configured as FAILURE. This value is always available.
    
    PRIORITY: (1 Byte) The DTC priority which is mapped into the environmental data. This value is
    always available.
    
    CURRENT_FDC: (1 Byte) Current value of the DTC fault detection counter. This value is always
    available.
    
    MAX_FDC_SINCE_LAST_CLEAR: (1 Byte) Maximum value of the DTC fault detection counter reached
    since last clear. 0 is the minimum value reported.
    If Dem/DemGeneral/DemSupportStorageIndependentMaxFDCSinceLastClear is not enabled the data
    element is processed and readable only for currently stored events. Otherwise it is processed
    and readable at all times (see also Dem/DemGeneral/DemExtendedDataVisibility).
    
    MAX_FDC_DURING_CURRENT_CYCLE: (1 Byte) Maximum value of the DTC fault detection counter reached
    in the current operation cycle. 0 is the minimum value reported. This value is always available.
    
    CYCLES_SINCE_FIRST_FAILED: (1 Byte) Number of completed operation cycles, since the cycle of the
    first transition of the TestFailed Bit from 0 to 1 of the DTC. The value latches at 255. The
    counter is processed and readable only for currently stored events.
    
    CYCLES_SINCE_LAST_FAILED: (1 Byte) Number of completed operation cycles, since the last
    transition of the TestFailed Bit from 0 to 1 of the DTC. The value is reset at the first failed
    result in the operation cycle, latches at 255. The counter is processed and readable only for
    currently stored events.
    
    FAILED_CYCLES: (1 Byte) Number of operation cycles, since last DTC clear in which the DTC was
    tested 'failed', including the current cycle. The value is incremented at the first failed
    result in the operation cycle, latches at 255.
    If Dem/DemGeneral/DemSupportStorageIndependentCycleCounters is not enabled the counter is
    processed and readable only for currently stored events. Otherwise the counter is processed and
    readable at all times (see also Dem/DemGeneral/DemExtendedDataVisibility).
    
    CONSECUTIVE_FAILED_CYCLES: (1 Byte): Number of consecutive operation cycles in which the DTC was
    tested 'failed', including the current cycle. The value is incremented at the first failed
    result in the operation cycle and reset at the end of an operation cycle that was tested and not
    tested 'failed'.The value latches at 255. The counter is processed and readable only for
    currently stored events.
    
    CYCLES_TESTED_SINCE_FIRST_FAILED: (1 Byte) Number of completed and tested operation cycles since
    the cycle of the first transition of the TestFailed Bit from 0 to 1 of the DTC. The value
    latches at 255. The counter is processed and readable only for currently stored events.
    
    CYCLES_TESTED_SINCE_LAST_FAILED: (1 Byte) Number of completed and tested operation cycles, since
    the last transition of the TestFailed Bit from 0 to 1 of the DTC (Healing  Counter). The value
    is reset at the first failed result in the operation cycle, latches at 255. The value is always
    available.
    
    HEALINGCTR_DOWNCNT: (1 Byte) Number of complete and tested operation cycles until WIR bit will
    be cleared (independently of whether
    Dem/DemConfigSet/DemEventParameter/DemEventClass/DemIndicatorAttribute/DemIndicatorRef is set or
    not). If healing has not started yet,
    Dem/DemConfigSet/DemEventParameter/DemEventClass/DemIndicatorAttribute/DemIndicatorHealingCycleCounterThreshold
    is reported. If healing is completed, 0 is reported. The value is always available.
    
    ROOTCAUSE_EVENTID: (2 Byte) The event id that caused the storage/update of the environmental
    data. Can be used in context of the feature 'combined event' to store the root cause DemEventId
    value. The value is processed and readable only for currently stored events
    
    OBDDTC: (2 Byte) The corresponding OBD II DTC for the requested UDS DTC. If no OBD II DTC is
    configured, the returned value will be 0. This value is always available.
    
    OBDDTC_3BYTE: (3 Byte)
    In OBDII configurations: The corresponding OBD II DTC for the requested UDS DTC in format [0x00
    LoByte HiByte].
    In OBD on UDS configurations: The corresponding 3 byte OBD DTC for the requested UDS DTC, if
    DemGeneral/DemGeneralOBD/DemSupportedObdUdsDtcSeparation == true.
    If no OBD II DTC resp. 3 byte OBD DTC is configured, the returned value will be 0. This value is
    always available.
    
    OBD_RATIO:  (4 Byte) If the DTC has a ratio attached, the numerator and denominator are returned
    in the following format: [NumHiByte NumLoByte DenomHiByte DenomLoByte].
    If the DTC does not have a ratio attached, the returned value is [0x00 0x00 0x00 0x00]. This
    value is always available.
    
    FAULT_PENDING_COUNTER: (1 Byte) Number of consecutive operation cycles in which the DTC was
    tested 'failed', including the current cycle. The value is incremented at the first failed
    result in the operation cycle and reset at the end of an operation cycle that was tested and not
    tested 'failed'. In contrast to the 'Consecutive Failed Cycle Counter' the value latches at
    DemEventFailureCycleCounterThreshold + 1.
    If Dem/DemGeneral/DemSupportStorageIndependentCycleCounters is not enabled the counter is
    processed and readable only for currently stored events. Otherwise the counter is processed and
    readable at all times (see also Dem/DemGeneral/DemExtendedDataVisibility).
    
    AGED_COUNTER: (1 Byte) Current value of the aged counter. The value is incremented, if the DTC
    is aged and reset, if the DTC is cleared. The value latches at 255 and is always available.
    
    WUC_SINCE_LAST_FAILED: (1 Byte) Number of completed warm up cycles, since the last transition of
    the TestFailed Bit from 0 to 1 of the DTC. The value latches at 255. The counter is processed
    and readable only for currently stored events.
    
    SI30_STATUS: (1 Byte) Extended status byte. The extended status is calculated and is always
    available.
    
    IUMPR: (4 Byte) The numerator and denominator of the ratio of a DTC are returned in the
    following format: [NumHiByte NumLoByte DenomHiByte DenomLoByte].
    This value can be used to configure extended data record number 0x91 according to SAE J1979-2.
    The value is only available, if OBD on UDS is supported (see
    Dem/DemGeneral/DemGeneralOBD/DemOBDLegislation).
    
    DTR: (1 Byte for the number of test results, 8 Byte for each test result) The Diagnostic Test
    Results (DTRs) of a DTC are returned in the following format: [NumberOfTestResults] and for each
    test result: [UaSIdHiByte UaSIdLoByte TestValueHiByte TestValueLoByte MinTestLimitHiByte
    MinTestLimitLoByte MaxTestLimitHiByte MaxTestLimitLoByte].
    The DTRs are returned in ascending order by Monitor Identifier (MID) and Test Identifier (TID).
    The size of this internal data element varies for each DTC based on the number of DTRs
    referencing the corresponding event. Due to this variability, size must be configured to
    the maximum supported value of 249 bytes (Dem supports a maximum of 31 DTRs with 8 byte each
    plus 1 byte for the number of test results, see
    Dem/DemGeneral/DemDataClass/DemDataElementDataSize). The actual size is calculated at runtime.
    This value can be used to configure extended data record number 0x92 according to SAE J1979-2.
    The value is only available, if OBD on UDS is supported (see
    Dem/DemGeneral/DemGeneralOBD/DemOBDLegislation).
    
    MONITOR_ACTIVITY_DATA: (2 Byte) The monitor activity numerator (MAN) and stored monitor activity
    ratio (SMAR) of a DTC are returned in the following format: [MAN SMAR].
    This value can be used to configure extended data record number 0x93 according to SAE J1979-2.
    The value is only available, if OBD on UDS is supported (see
    Dem/DemGeneral/DemGeneralOBD/DemOBDLegislation).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemDataElementReadFnc
  长名称: ''
  描述: In case of DemDataElementUsePort is USE_DATA_FUNCTION_CALL,
      USE_DATA_FUNCTION_CALL_WITH_EVENTID, USE_DATA_FUNCTION_CALL_WITH_EVENTID_BUFFERLENGTH or
      USE_DATA_FUNCTION_CALL_WITH_PROXY,  this parameter defines the prototype of the C
      function "ReadDataElement" used to get the according value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemDataElementStoreNonVolatile
  长名称: ''
  描述: |
    Select if the data element needs to be stored in NVRam.
    
    Ususally, snapshots of a system value (like temperature, voltage...) need to be stored in NVRam.
    If the data element is stored, the Dem will collect the current value into NVRam at the DTC
    storage time. Reading access will return the stored data (e.g. for diagnostic service $19)
    
    Disabling NV storage for this data element will cause the Dem to fetch the data with each read
    access. This is useful if this data element is something that will not change over time, or is
    already stored outside the Dem.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemDataElementUsePort
  长名称: ''
  描述: |
    Defines which interface shall be used to access the data.
    
    For data calculated internally by the Dem, use
    USE_DATA_INTERNAL
    
    For data provided by the application through a client/server port, use
    USE_DATA_CLIENT_SERVER_PORT
    USE_DATA_CLIENT_SERVER_PORT_WITH_EVENTID
    
    For data provided by the application through a C function-callback, use
    USE_DATA_FUNCTION_CALL
    USE_DATA_FUNCTION_CALL_WITH_EVENTID
    USE_DATA_FUNCTION_CALL_WITH_EVENTID_BUFFERLENGTH
    USE_DATA_FUNCTION_CALL_WITH_PROXY
    
    For data provided by the application through a sender/receiver port, use
    USE_DATA_SENDER_RECEIVER
  默认值: USE_DATA_CLIENT_SERVER_PORT
  最小值: ''
  最大值: ''
```

### 29. DemAlternativeDataInterface

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of a VariableDataPrototoype in a DataInterface.
(not supported)

该容器没有参数。

### 30. DemAlternativeDataProps

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of ECU configuration parameters.
(not supported)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDataTypeCategory
  长名称: ''
  描述: |
    Data category of the alternative Diagnosis Representation.
    (not supported)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 31. DemLinearScale

**描述**: This container contains the configuration (parameters) of an linear scale of the alternative
Diagnosis Representation.
(not supported)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataLowerRange
  长名称: ''
  描述: |
    Lower Range for this scale of the data in the alternative Diagnosis Representation.
    (not supported)
  默认值: ''
  最小值: -1.7976931348623157E+308
  最大值: 1.7976931348623157E+308
- 
  序号: 2
  名称: DemDiagnosisRepresentationDataOffset
  长名称: ''
  描述: |
    Data offset of the alternative Diagnosis Representation for this scale.
    (not supported)
  默认值: 0
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: DemDiagnosisRepresentationDataResolution
  长名称: ''
  描述: |
    Data resolution of the alternative Diagnosis Representation for this scale.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: DemDiagnosisRepresentationDataUpperRange
  长名称: ''
  描述: |
    Upper Range for this scale of the data in the alternative Diagnosis Representation.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
```

### 32. DemTextTableMapping

**描述**: This container contains the configuration (parameters) of the mapping a DataPrototype typed by
AutosarDataType that refer to a CompuMethods of category TEXTTABLE or SCALE_LINEAR_AND_TEXTTABLE.
(not supported)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataValue
  长名称: ''
  描述: |
    The data value in the diagnosis representation.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: DemInternalDataValue
  长名称: ''
  描述: |
    The ECU internal data value.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 33. DemAlternativeDataType

**描述**: This container contains the configuration (parameters) of an alternative Diagnosis Representation by
the means of an ApplicationDataType.
(not supported)

该容器没有参数。

### 34. DemTextTableMapping

**描述**: This container contains the configuration (parameters) of the mapping a DataPrototype typed by
AutosarDataType that refer to a CompuMethods of category TEXTTABLE or SCALE_LINEAR_AND_TEXTTABLE.
(not supported)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDiagnosisRepresentationDataValue
  长名称: ''
  描述: |
    The data value in the diagnosis representation.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: DemInternalDataValue
  长名称: ''
  描述: |
    The ECU internal data value.
    (not supported)
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 35. DemDataElementInstance

**描述**: Instance Reference to the primitive data in a port where the data element is typed with an
ApplicationPrimitveDataType or an ImplementationDataType.
(not supported)

该容器没有参数。

### 36. DemSubElementInDataElementInstance

**描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the
data element is typed with an ApplicationCompositeDataType.
(not supported)

该容器没有参数。

### 37. DemSubElementInImplDataElementInstance

**描述**: Instance Reference to the primitve sub-element (at any level) of composite data in a port where the
data element is typed with an ImplementationDataType of category STRUCTURE or ARRAY.
(not supported)

该容器没有参数。

### 38. DemDidClass

**描述**: This container represents a Data Identifier (DID) as defined by the UDS protocol.

Each DID is assembled out of one or several data elements.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemDidIdentifier
  长名称: ''
  描述: Identifier of the Data ID as returned e.g. in $19 04.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 39. DemEnableCondition

**描述**: This container represents a single enable condition.

Please note: enable conditions can not be used directly but must be grouped (see
DemEnableConditionGroup).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemEnableConditionId
  长名称: EnableCondition Id
  描述: |
    Internal identifier of the enable condition.
    
    This number is calculated internally and shall not be configured manually. This parameter is
    only available to publish the result of this calculation.
    Applications using Dem APIs must not rely on the value of this parameter. Instead, they must use
    the symbolic constant (SymbolicNameValue) DemConf_DemEnableCondition_{SHORT-NAME}.
    
    The ID value 0 is reserved for internal purpose.
  默认值: 255
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemEnableConditionStatus
  长名称: EnableCondition Status
  描述: |
    Defines the status of this enable condition after full initialization, i.e. when
    Dem_MasterInit() or Dem_Init() finished.
    After pre-initialization, but before the full intialization (between Dem_(Master)PreInit() and
    Dem_(Master)Init()) the status is always 'true'.
    Changes to the enable condition status during runtime are not persisted non-volatile. The status
    of this enable condition will always be reset to this configuration value during
    Dem_MasterInit() or Dem_Init().
  默认值: true
  最小值: ''
  最大值: ''
```

### 40. DemEnableConditionGroup

**描述**: This container groups several enable conditions.

EventParameters only reference one of these groups, not individual enable conditions.

该容器没有参数。

### 41. DemEventMemorySet

**描述**: This container is a collection of referenced event memories and related information for a Dem
client.

该容器没有参数。

### 42. DemClearDTCNotification

**描述**: Contains callback function definition which are called during clear DTC operations.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemClearDtcNotificationFnc
  长名称: ''
  描述: |
    Notification callback function name which is called on a clear DTC operation (refer to
    <Module>_ClearDtcNotification).
    
    If this parameter exists, it must give a valid C-Function which is called instead of using an
    RTE port interface.
    See DemGeneral/DemHeaderFileInclusion to specify a header file which declares this function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemClearDtcNotificationTime
  长名称: ''
  描述: Configure, whether the callback shall be called on start of a clear or after finishing a clear
      DTC operation (refer to <Module>_ClearDtcNotification)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 43. DemPrimaryMemory

**描述**: This container contains the primary event memory specific parameters
of the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemMaxNumberEventEntryPrimary
  长名称: ''
  描述: Maximum number of events which can be stored in the primary memory
  默认值: 8
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemTypeOfFreezeFrameRecordNumeration
  长名称: Type Of FreezeFrameRecord Numeration
  描述: |
    This parameter defines the type of assigning snapshot record numbers.
    
    CALCULATED: The snapshot records are enumerated from one (1) up to
    DemConfigSet/DemEventParameter/DemMaxNumberFreezeFrameRecords for each event. Once an event
    memory entry is created a snapshot is stored at each FAILED transition. After
    DemMaxNumberFreezeFrameRecords have been stored for the event, the last snapshot is updated with
    each FAILED transition.
    
    CALCULATED_FIFO: The snapshot records are enumerated from one (1) up to
    DemConfigSet/DemEventParameter/DemMaxNumberFreezeFrameRecords for each event. Once an event
    memory entry is created, a snapshot is stored at each FAILED transition of the event. After
    DemMaxNumberFreezeFrameRecords have been stored for the event, the oldest snapshot is
    overwritten during the next trigger. When a snapshot is overwritten, all snapshot records are
    renumbered in ascending order from oldest to newest snapshot record.
    
    CONFIGURED: The snapshot record numbers are taken from
    DemConfigSet/DemEventParameter/DemFreezeFrameRecNumClassRef. Storage triggers and update
    conditions can be configured.
  默认值: DEM_FF_RECNUM_CALCULATED
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemEventMemoryEntryStorageTrigger
  长名称: Event Memory Entry Storage Trigger
  描述: |
    This parameter describes the trigger for the allocation of an event memory entry, i.e. the point
    of time when the corresponding DTC is initially stored in the referenced event memory.
    
    CONFIRMED: An event entry is allocated once its corresponding DTC confirms (bit3 transitions
    0->1).
    
    FDC_THRESHOLD: An event entry is allocated once the fault detection counter of its corresponding
    DTC exceeds its storage threshold.
    
    PENDING: An event entry is allocated once its corresponding DTC gets pending (bit2 transitions
    0->1).
    
    TEST_FAILED: An event entry is allocated once its corresponding DTC fails (bit0 transitions
    0->1).
    
    Restriction: If FDC_THRESHOLD is selected, monitor internal debouncing cannot be used to store
    event data at pre-failed.
  默认值: DEM_STORAGE_ON_TEST_FAILED
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemMaxNumberTimeSeriesSnapshots
  长名称: Max Number Time Series Entries
  描述: |
    This parameter defines the maximum number of events for which time series snapshot records (also
    known as multi-sample development snapshot records) can be stored at the same time for this
    event memory.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: DemMaxNumberTimeSeriesSnapshotSets
  长名称: Max Number Time Series Sets
  描述: |
    The maximum number of time series snapshot record sets that can be stored for an event assigned
    to this memory. If the parameter is missing, only one set will be stored.
    
    A set of time series snapshot records consists of all past and future samples that are stored
    for an event after the freeze frame storage trigger has occurred. With each re-occurrence of the
    trigger, a new set can be stored.
    When the maximum number of time series snapshot record sets has been stored, the new set may
    overwrite the oldest set depending on the value of DemTimeSeriesSnapshotFifoSupport.
    
    For more information on how the time series snapshot records of the different sets are numbered,
    refer to DemTimeSeriesSnapshotRecordNumberOffset.
  默认值: 1
  最小值: 1
  最大值: 16
- 
  序号: 6
  名称: DemTimeSeriesSnapshotFifoSupport
  长名称: Time Series Fifo Support
  描述: |
    This configuration switch defines if the time series snapshot record sets of events assigned to
    this memory are stored in a circular buffer.
    
    If the switch is enabled and the configured maximum number of time series snapshot record sets
    (see DemMaxNumberTimeSeriesSnapshotSets) is stored for an event, the oldest set of time series
    snapshot records will be overwritten with each new storage trigger occurrence. Correspondingly,
    all time series snapshot records of the event will be renumbered in ascending order from oldest
    to newest.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemTimeSeriesSnapshotRecordNumberOffset
  长名称: Time Series Sets Record Number Offset
  描述: |
    This offset is used to calculate the first record number of all subsequent sets of time series
    snapshots that are stored for an event (see DemMaxNumberTimeSeriesSnapshotSets).
    
    This parameter only has an effect if DemMaxNumberTimeSeriesSnapshotSets is greater than 1.
    
    The first set of time series snapshot record numbers starts at the freeze frame recod number
    (see DemFreezeFrameRecordNumber) configured for the time series snapshot record (see
    DemFreezeFrameRecordIsTimeSeries).
    If DemMaxNumberTimeSeriesSnapshotSets is greater than 1, the records numbers of the subsequent
    sets will start at:
    - DemFreezeFrameRecordNumber + (1 * DemTimeSeriesSnapshotOffset),
    - DemFreezeFrameRecordNumber + (2 * DemTimeSeriesSnapshotOffset),
    ...
    - DemFreezeFrameRecordNumber + (n* DemTimeSeriesSnapshotOffset), where n equals
    (DemMaxNumberTimeSeriesSnapshotSets -1).
    
    Example:
    - DemFreezeFrameRecordNumber is set to 0x80,
    - DemTimeSeriesSnapshotOffset is set to 0x08 and
    - DemMaxNumberTimeSeriesSnapshotSets equals 3,
    the different sets of time series snapshot records stored for an event will start at record
    number
    - 0x80,
    - 0x88 and
    - 0x90.
  默认值: 8
  最小值: 1
  最大值: 32
- 
  序号: 8
  名称: DemMaxNumberCustomTriggeredSnapshots
  长名称: ''
  描述: |
    This parameter defines the maximum number of events for which custom triggered snapshot records
    and/or custom triggered time series snapshot records can be stored at the same time for this
    event memory.
    A snapshot record or time series snapshot record is custom triggered if the corresponding
    DemFreezeFrameRecordTrigger is configured to DEM_TRIGGER_ON_CUSTOM.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 44. DemUserDefinedMemory

**描述**: This container contains the user defined event memory specific
parameters of the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemMaxNumberEventEntryUserDefined
  长名称: ''
  描述: Maximum number of events which can be stored in the user defined memory.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 2
  名称: DemUserDefinedMemoryIdentifier
  长名称: ''
  描述: Identifier used by external tester to identify the User defined event memory
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DemTypeOfFreezeFrameRecordNumeration
  长名称: Type Of FreezeFrameRecord Numeration
  描述: |
    This parameter defines the type of assigning snapshot record numbers.
    
    CALCULATED: The snapshot records are enumerated from one (1) up to
    DemConfigSet/DemEventParameter/DemMaxNumberFreezeFrameRecords for each event. Once an event
    memory entry is created a snapshot is stored at each FAILED transition. After
    DemMaxNumberFreezeFrameRecords have been stored for the event, the last snapshot is updated with
    each FAILED transition.
    
    CALCULATED_FIFO: The snapshot records are enumerated from one (1) up to
    DemConfigSet/DemEventParameter/DemMaxNumberFreezeFrameRecords for each event. Once an event
    memory entry is created, a snapshot is stored at each FAILED transition of the event. After
    DemMaxNumberFreezeFrameRecords have been stored for the event, the oldest snapshot is
    overwritten during the next trigger. When a snapshot is overwritten, all snapshot records are
    renumbered in ascending order from oldest to newest snapshot record.
    
    CONFIGURED: The snapshot record numbers are taken from
    DemConfigSet/DemEventParameter/DemFreezeFrameRecNumClassRef. Storage triggers and update
    conditions can be configured.
  默认值: DEM_FF_RECNUM_CALCULATED
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemEventMemoryEntryStorageTrigger
  长名称: Event Memory Entry Storage Trigger
  描述: |
    This parameter describes the trigger for the allocation of an event memory entry, i.e. the point
    of time when the corresponding DTC is initially stored in the referenced event memory.
    
    CONFIRMED: An event entry is allocated once its corresponding DTC confirms (bit3 transitions
    0->1).
    
    FDC_THRESHOLD: An event entry is allocated once the fault detection counter of its corresponding
    DTC exceeds its storage threshold.
    
    PENDING: An event entry is allocated once its corresponding DTC gets pending (bit2 transitions
    0->1).
    
    TEST_FAILED: An event entry is allocated once its corresponding DTC fails (bit0 transitions
    0->1).
    
    Restriction: If FDC_THRESHOLD is selected, monitor internal debouncing cannot be used to store
    event data at pre-failed.
  默认值: DEM_STORAGE_ON_TEST_FAILED
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemMaxNumberTimeSeriesSnapshots
  长名称: Max Number Time Series Entries
  描述: |
    This parameter defines the maximum number of events for which time series snapshot records (also
    known as multi-sample development snapshot records) can be stored at the same time for this
    event memory.
    
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: DemMaxNumberTimeSeriesSnapshotSets
  长名称: Max Number Time Series Sets
  描述: |
    The maximum number of time series snapshot record sets that can be stored for an event assigned
    to this memory. If the parameter is missing, only one set will be stored.
    
    A set of time series snapshot records consists of all past and future samples that are stored
    for an event after the freeze frame storage trigger has occurred. With each re-occurrence of the
    trigger, a new set can be stored.
    When the maximum number of time series snapshot record sets has been stored, the new set may
    overwrite the oldest set depending on the value of DemTimeSeriesSnapshotFifoSupport.
    
    For more information on how the time series snapshot records of the different sets are numbered,
    refer to DemTimeSeriesSnapshotRecordNumberOffset.
  默认值: 1
  最小值: 1
  最大值: 16
- 
  序号: 7
  名称: DemTimeSeriesSnapshotFifoSupport
  长名称: Time Series Fifo Support
  描述: |
    This configuration switch defines if the time series snapshot record sets of events assigned to
    this memory are stored in a circular buffer.
    
    If the switch is enabled and the configured maximum number of time series snapshot record sets
    (see DemMaxNumberTimeSeriesSnapshotSets) is stored for an event, the oldest set of time series
    snapshot records will be overwritten with each new storage trigger occurrence. Correspondingly,
    all time series snapshot records of the event will be renumbered in ascending order from oldest
    to newest.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemTimeSeriesSnapshotRecordNumberOffset
  长名称: Time Series Sets Record Number Offset
  描述: |
    This offset is used to calculate the first record number of all subsequent sets of time series
    snapshots that are stored for an event (see DemMaxNumberTimeSeriesSnapshotSets).
    
    This parameter only has an effect if DemMaxNumberTimeSeriesSnapshotSets is greater than 1.
    
    The first set of time series snapshot record numbers starts at the freeze frame recod number
    (see DemFreezeFrameRecordNumber) configured for the time series snapshot record (see
    DemFreezeFrameRecordIsTimeSeries).
    If DemMaxNumberTimeSeriesSnapshotSets is greater than 1, the records numbers of the subsequent
    sets will start at:
    - DemFreezeFrameRecordNumber + (1 * DemTimeSeriesSnapshotOffset),
    - DemFreezeFrameRecordNumber + (2 * DemTimeSeriesSnapshotOffset),
    ...
    - DemFreezeFrameRecordNumber + (n* DemTimeSeriesSnapshotOffset), where n equals
    (DemMaxNumberTimeSeriesSnapshotSets -1).
    
    Example:
    - DemFreezeFrameRecordNumber is set to 0x80,
    - DemTimeSeriesSnapshotOffset is set to 0x08 and
    - DemMaxNumberTimeSeriesSnapshotSets equals 3,
    the different sets of time series snapshot records stored for an event will start at record
    number
    - 0x80,
    - 0x88 and
    - 0x90.
  默认值: 8
  最小值: 1
  最大值: 32
- 
  序号: 9
  名称: DemMaxNumberCustomTriggeredSnapshots
  长名称: ''
  描述: |
    This parameter defines the maximum number of events for which custom triggered snapshot records
    and/or custom triggered time series snapshot records can be stored at the same time for this
    event memory.
    A snapshot record or time series snapshot record is custom triggered if the corresponding
    DemFreezeFrameRecordTrigger is configured to DEM_TRIGGER_ON_CUSTOM.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 45. DemExtendedDataClass

**描述**: This class groups several extended data records.

EventParameters only reference these groups, not individual extended data records.

该容器没有参数。

### 46. DemExtendedDataRecordClass

**描述**: This container represents a single extended data record.

Each extended data record is assembled out of one or several data elements.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemExtendedDataRecordNumber
  长名称: ExtendedDataRecord Number
  描述: |
    The unique identifier of the extended data record as requested and reported by $19 06.
    
    Please note that extended data records are unique per ECU, e.g. the number references a defined
    set of data independent of the DTC it is related to.
  默认值: ''
  最小值: 1
  最大值: 253
- 
  序号: 2
  名称: DemExtendedDataRecordTrigger
  长名称: ''
  描述: |
    This parameter defines the trigger to store and update ExtendedDataRecords, if configured.
    
    FDC_FIRST_IN_CYCLE: The extended data record capture/ update is triggered by the event's fault
    detection counter exceeding the configured storage threshold. This trigger is only processed
    once per operationcycle.
    
    TEST_FAILED: The  extended data record capture/ update is triggered by the TestFailed bit
    transition from 0 to 1.
    
    CONFIRMED: The  extended data record capture is triggered by the Confirmed bit transition from 0
    to 1.
    
    PASSED: The  extended data record capture/ update is triggered by a qualified 'Passed' report
    that resets the TestFailed bit from 1 to 0.
  默认值: DEM_TRIGGER_ON_TEST_FAILED
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemExtendedDataRecordUpdate
  长名称: ExtendedDataRecord Update
  描述: |
    This parameter defines if this record is captured only once (UPDATE_RECORD_NO) or updated with
    each following trigger ((UPDATE_RECORD_YES).
    
    Please note that internal data elements are updated continuously and can not be frozen to their
    value at the time of confirmation.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 47. DemFreezeFrameClass

**描述**: This container groups DIDs into a snapshot record.

These records are sampled at different points in time, and each of these samples is identified by
the snapshot record number.

该容器没有参数。

### 48. DemFreezeFrameRecNumClass

**描述**: This container contains a list of dedicated, different snapshot record numbers assigned to an event.

These containers are relevant in case snapshot record numbers are CONFIGURED for an event (see
DemTypeOfFreezeFrameRecordNumeration of DemPrimaryMemory or DemUserDefinedMemory referenced by the
event)
and in case that an event uses time series snapshot records (See
Dem/DemGeneral/DemFreezeFrameRecordClass/DemFreezeFrameRecordIsTimeSeries).

该容器没有参数。

### 49. DemFreezeFrameRecordClass

**描述**: This container contains a list of dedicated, different freeze frame record numbers.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemFreezeFrameRecordNumber
  长名称: FreezeFrameRecord Number
  描述: |
    This parameter defines a record number for a freeze frame record.
    This record number is unique per freeze frame record number class.
    
    In case that DemFreezeFrameRecordIsTimeSeries is enabled, this parameter represents the first
    record number of the time series snapshot records.
  默认值: ''
  最小值: 1
  最大值: 254
- 
  序号: 2
  名称: DemFreezeFrameRecordTrigger
  长名称: FreezeFrameRecord Trigger
  描述: |
    Defines the trigger to store the FreezeFrameRecord.
    
    FDC_THRESHOLD: The snapshot data capture is triggered by a fault detection counter passing a
    storage threshold.
    
    CONFIRMED: The snapshot data capture is triggered by the ConfirmedDTC transition 0 -> 1.
    
    PENDING: The snapshot data capture is triggered by the PendingDTC transition 0 -> 1.
    
    TEST_FAILED: The snapshot data capture is triggered by the TestFailed transition 0 -> 1.
    
    TEST_FAILED_FIRST_IN_CYCLE: The snapshot data capture is triggered by the first TestFailed
    transition 0 -> 1 in an operation cycle (i.e TestFailedThisOperationCycle transition 0 -> 1).
    
    FDC_FIRST_IN_CYCLE: The snapshot data capture is triggered by the first DTC fault detection
    counter reaching the storage threshold in an operation cycle.
    
    PASSED: The snapshot data capture is triggered by the TestFailed transition 1 -> 0.
    
    CUSTOM: The snapshot data capture is triggered by API Dem_StoreCustomTriggeredFreezeFrame(). An
    event can only use this snapshot trigger, when the corresponding event memory has
    DemMaxNumberCustomTriggeredSnapshots > 0
    
    
    Please note:
    For all triggers except CUSTOM, snapshot trigger occuring before an event memory entry is
    allocated are postponed until the event memory entry gets allocated.
    Snapshot trigger CUSTOM can capture snapshot data even before an event memory entry is allocated
    to the event.
    
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemFreezeFrameRecordUpdate
  长名称: FreezeFrameRecord Update
  描述: |
    This parameter defines the case, when the freeze frame record is stored/updated.
    
    DEM_UPDATE_RECORD_NO - The snapshot record is captured only once.
    
    DEM_UPDATE_RECORD_YES - The snapshot is captured with each trigger, overwriting a previously
    captured snapshot.
    
    If option DEM_UPDATE_RECORD_YES is chosen for a snapshot record with DemFreezeFrameRecordTrigger
    CONFIRMED the snapshot record is initally stored on ConfirmedDTC transition 0 -> 1 and updated
    with each following TestFailed transition 0 -> 1.
    
    If option DEM_UPDATE_RECORD_YES is chosen for a time series snapshot record (see
    DemFreezeFrameRecordIsTimeSeries) all past samples are overwritten and future samples are
    collected anew with each trigger.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemFreezeFrameRecordIsTimeSeries
  长名称: FreezeFrameRecord Is TimeSeries
  描述: |
    Defines whether the record is used as a time series snapshot record.
    
    If this parameter is enabled, DemTimeSeriesSnapshotClassRef must contain a valid reference.
    
    If this parameter is disabled or not configured, the record is used as a configured freeze frame
    record and DemTimeSeriesSnapshotClassRef is ignored.
  默认值: false
  最小值: ''
  最大值: ''
```

### 50. DemGeneralJ1939

**描述**: This container contains the general J1939-specific configuration (parameters) of the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemJ1939ClearDtcSupport
  长名称: ''
  描述: |
    This configuration switch defines whether clearing J1939 DTCs is supported or not.
    
    If enabled, the following DMs are supported:
    - Clearing all active / previously Active DTCs (DM03 and DM11)
    - Clearing single active / previously Active DTC (DM22)
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemJ1939Dm31Support
  长名称: ''
  描述: This configuration switch defines whether J1939 DM31 is supported or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemJ1939ExpandedFreezeFrameSupport
  长名称: J1939 Expanded FreezeFrame Support
  描述: This configuration switch defines whether J1939 expanded freeze frames are supported or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemJ1939FreezeFrameSupport
  长名称: J1939 FreezeFrame Support
  描述: This configuration switch defines whether J1939 freeze frames are supported or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemJ1939RatioSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 performance ratios are supported or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemJ1939Readiness1Support
  长名称: ''
  描述: |
    This configuration switch defines whether J1939 diagnostic readiness 1 is supported or not.
    
    This switches on and off the API Dem_J1939DcmReadDiagnosticReadiness1.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemJ1939Readiness2Support
  长名称: ''
  描述: |
    This configuration switch defines whether J1939 diagnostic readiness 2 is supported or not.
    
    This switches on and off the API Dem_J1939DcmReadDiagnosticReadiness2.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemJ1939Readiness3Support
  长名称: ''
  描述: |
    This configuration switch defines whether J1939 diagnostic readiness 3 is supported or not.
    
    This switches on and off the API Dem_J1939DcmReadDiagnosticReadiness3.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemJ1939ReadingDtcSupport
  长名称: ''
  描述: This configuration switch defines whether J1939 DTC readout is supported or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemTriggerJ1939DcmReports
  长名称: ''
  描述: |
    If enabled, the J1939Dcm module is notified about DTC status changes in primary memory.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DemJ1939ReadingDTCRuntimeLimit
  长名称: ''
  描述: |
    If this parameter exists, Dem_J1939DcmGetNextFilteredDTC will test at most this amount of DTCs
    for matching the filter before returning DEM_PENDING.
    
    This parameter can be used to reduce the run time of the J1939Dcm_MainFunction when filtering
    for DTCs.
  默认值: ''
  最小值: 1
  最大值: 65534
```

### 51. DemCallbackJ1939DTCStatusChanged

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

### 52. DemJ1939FreezeFrameClass

**描述**: This container contains the combinations of SPNs s for a J1939 relevant freeze frame.

Your configuration must use one (1) common definition for all J1939 freeze frames and one (1) common
definition for all J1939 expanded freeze frames (use the event parameters
DemJ1939FreezeFrameClassRef and DemJ1939ExpandedFreezeFrameClassRef to use this definitions).
Therefore the multiplicity of this parameter is limited to 2.


该容器没有参数。

### 53. DemSPNClass

**描述**: This container contains the configuration (parameters) for a SPN.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemSPNId
  长名称: ''
  描述: Suspect parameter number.
  默认值: ''
  最小值: 0
  最大值: 524287
```

### 54. DemJ1939RatioClass

**描述**: This container is used to map Ratios (IUMPRs) to SPNs. The SPNs which are defined here will be
reported in DM20.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemSPN
  长名称: ''
  描述: Suspect parameter number of the ratios that shall be to be reported for DM20.
  默认值: ''
  最小值: 0
  最大值: 1048575
```

### 55. DemGeneralOBD

**描述**: This container will be used only, if the OBD support (for either OBD II or WWH-OBD or OBD on UDS or
ZEV on UDS) is activated (see DemGeneral/DemOBDSupport and
DemGeneral/DemGeneralOBD/DemOBDLegislation).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemOBDCentralizedPID21Handling
  长名称: ''
  描述: |
    Switch to enable the centralized handling of PID $21.
    (not supported, please use DemGeneral/DemPidConfiguration/DemSupportPid21 instead)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemOBDCentralizedPID31Handling
  长名称: ''
  描述: |
    Switch to enable the centralized handling of PID $31.
    (Not supported, please use DemGeneral/DemPidConfiguration/DemSupportPid31 instead)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemOBDCompliancy
  长名称: ''
  描述: Configuration value to define the appropriate value to PID$1C "OBD requirements to which
      vehicle or engine is certified." according to the respective standards, e.g. OBD I, OBD
      II, JOBD etc.
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DemOBDEngineType
  长名称: ''
  描述: |
    Switch to provide either Gasoline or Diesel parameters.
    
    Used for PID $01, PID $F501 and J1939 diagnostic readiness 1 if Major Monitors are supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemOBDDestinationOfEvents
  长名称: ''
  描述: |
    The destination of events assigns where the OBD events shall be stored.
    (not supported)
  默认值: DEM_DTC_ORIGIN_PRIMARY_MEMORY
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemOBDEventDisplacement
  长名称: ''
  描述: |
    Activate/Deactivate a different displacement behavior for OBD events.
    (not supported)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemDelayWarmUpCycleToDcyEnd
  长名称: Delay WarmUp Cycle To Driving Cycle End
  描述: |
    If enabled the DEM can only be triggered for the start of warm-Up cycle and it will ignore the
    trigger for the end of warm-up cycle.
    It will automatically restart the warm-up cycle at the end of a (qualified) driving cycle.
    
    Therefore the DTCs that have configured the warm-up cycle as their aging cycle will age at the
    end of the driving cycle.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemEngineRuntimePolling
  长名称: Engine Runtime Minutes Polling
  描述: |
    Allow to configure the time for the periodic polling of the engine runtime in minutes.
    
    The value must be a multiple of the DemGeneral/DemTaskTime. Otherwise it is rounded down to the
    next multiple value of DemTaskTime.
    
    This value is mandatory, when parameter DemOBDTimeSinceEngineStart is required. If missing, it
    defaults to the DemTaskTime.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a diffenent unit.
  默认值: 60
  最小值: 0.001
  最大值: 2678400
- 
  序号: 9
  名称: DemOBDFreezeFrameBehavior
  长名称: OBD Freeze Frame Behavior
  描述: |
    This configuration value defines, when the OBD II resp. WWH-OBD Freeze Frame is taken, stored
    and updated and when/how it is visible for diagnostic requests.
    
    DemOBDFreezeFrameBehavior has no effect on OBDonUDS Freeze Frame storage.The OBDonUDS FF is
    always stored when trigger conditions are met.
    
    OBD II, TYPE 1: OBD II Freeze Frame data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    If PendingDTC is healed without being ConfirmedDTC, the Freeze Frame will be cleared.
    The Freeze Frame is immediately visible in Mode02.
    
    OBD II, TYPE 2: OBD II Freeze Frame data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    If PendingDTC is healed without being ConfirmedDTC, the Freeze Frame will be cleared.
    The Freeze Frame is visible as soon as the ConfirmedDTC status bit of the DTC is visible. The
    visibility depends on parameter
    /DemEventParameter/DemEventClass/DemOBDVisibilityDelayedUntilDcyQualification. If this parameter
    is enabled, visibility is delayed until the OBD driving cycle is qualified.
    This option allows multiple Freeze Frames (see parameter
    /DemGeneral/DemMaxNumberEventEntryOBDFreezeFrame).
    
    OBD II, TYPE 3: OBD II Freeze Frame data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    The Pending Freeze Frame will be displaced if another DTC becomes a ConfirmedDTC.
    If PendingDTC is healed without being ConfirmedDTC the Freeze Frame will be cleared.
    The Freeze Frame is immediately visible in Mode02.
    
    OBD II, TYPE 4: OBD II Freeze Frame  data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    The Pending Freeze Frame will be updated if the DTC becomes a ConfirmedDTC.
    If PendingDTC is healed without being ConfirmedDTC the Freeze Frame will be cleared.
    The Freeze Frame is immediately visible in Mode02.
    
    OBD II, TYPE 5: OBD II Freeze Frame data capture is triggered when the trip condition is
    fulfilled.
    The Freeze Frame is visible as soon as the ConfirmedDTC status bit of the DTC is visible. The
    visibility depends on parameter
    /DemEventParameter/DemEventClass/DemOBDVisibilityDelayedUntilDcyQualification. If this parameter
    is enabled, visibility is delayed until the OBD driving cycle is qualified.
    For DTCs related to misfire or fuel system monitoring
    (DemEventOBDReadinessGroup = DEM_OBD_RDY_MISF or DEM_OBD_RDY_FLSYS or DEM_OBD_RDY_FLSYS_NONCONT)
    the Freeze Frame can also become visible without the need for a qualified driving cycle in some
    edge cases.
    A stored but not yet visible freeze frame will be displaced by the freeze frame of an event with
    parameter DemOBDVisibilityDelayedUntilDcyQualification disabled, if the invisible freeze frame
    is not related to a misfire and fuel system monitor.
    For more information refer to chapter "Reporting of Freeze Frame with Mode $02"  in the OBD
    Technical Reference.
    
    WWH-OBD, TYPE 1: WWH-OBD Freeze Frame data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    The Freeze Frame is immediately visible
    
    WWH-OBD, TYPE 2: WWH-OBD  Freeze Frame  data capture is triggered by the initial PendingDTC
    transition from 0 to 1.
    If DTC becomes a ConfirmedDTC the Freeze Frame data will be updated.
    The Freeze Frame is immediately visible.
    
    COMBINED, TYPE1: This behavior corresponds to 'Type 1' for OBDII and 'Type 1' for WWH-OBD.
    
    COMBINED, TYPE2: This behavior corresponds to 'Type 4' for OBDII and 'Type 2' for WWH-OBD.
    
    Use COMBINED values if and only if using OBDII and WWH-OBD in different PBS variants within one
    configuration.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemOBDFreezeFrameInService19
  长名称: OBD II FreezeFrame In Service 19
  描述: |
    Only relevant for OBD II legislation.
    Report the OBD II freeze frame in UDS Service $19 04 (with record number 0x00 or wildcard 0xFF).
    
    If enabled the OBD II Freeze Frame can be accessed in diagnostic service $19 04 and in Mode 02
    otherwise only in Mode 02.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DemOBDHideOccurrences
  长名称: OBD Hide Occurrences
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    Dependent OBD DTCs shall not appear in some UDS $19 sub-services.
    
    If enabled, the Dem hides dependent OBD DTCs from reporting.
    Also, operation 'HideOccurrences' in service 'DemOBDServices' is provided to change this
    behavior at run-time.
    Dependent OBD DTCs are identified via the parameter 'DemEventSignificance'. A setting of
    'OCCURRENCE' marks a dependent DTC.
    
    Note: Non-OBD DTCs are not affected by this feature.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: DemOBDLegislation
  长名称: ''
  描述: |
    The OBD legislation that shall be supported.
    
    OBDII: Support of OBD II.
    
    WWHOBD: Support of WWH-OBD.
    
    OBD_ON_UDS: Support of OBDonUDS.
    
    ZEV_ON_UDS: Support of ZEVonUDS.
    
    If OBD support is disabled (Dem/DemGeneral/DemOBDSupport == DEM_OBD_NO_OBD_SUPPORT), this
    parameter is ignored.
  默认值: DEM_OBD_LEGISLATION_OBDII
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: DemOBDPermanentDtcActivationDistance
  长名称: OBD PermanentDtc Activation Distance
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    Distance after first valid Odometer value was provided after which permanent DTC storage is
    activated.
    
    The resolution is the same as for PID$21 and PID$31 (see parameter
    DemOBDInputDistanceInformation).
    
    Providing this parameter will also enable an API to activate permanent DTC storage before the
    configured distance is reached.
    
    If this parameter is missing, permanent DTC storage is always active and can't be suppressed.
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 14
  名称: DemOBDPermanentEraseConditionDcy
  长名称: OBD Permanent Erase Condition Dcy
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    This parameter controls the behavior of a permanent fault after a clear DTC command issued while
    the OBD driving cycle (DCY) is not yet qualified.
    
    If enabled, the Dem checks the DCY qualification state during a Clear DTC request.
    - DCY not qualified: The permanent fault code can be removed from permanent memory in the same
    DCY as the clear DTC request was issued.
    - DCY qualified: The permanent fault code cannot be removed from permanent memory in the same
    DCY as the clear DTC request was issued.
    
    If disabled, the DCY qualification state has no effect.
    
    Note: To remove a DTC from permanent memory the PFC condition must be fulfilled and the DTC must
    be tested as passed and not failed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: DemOBDPermanentMandatoryPfcAfterClear
  长名称: OBD Permanent Mandatory Pfc After Clear
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    This configuration switch specifies, when a DTC will be removed from the permanent memory after
    the fault memory was cleared (e.g. Mode $04) and the DTC illuminates the MIL again.
    
    If this option is enabled, the DTC will be removed from permanent memory only if PFC cycle was
    active and MIL becomes inactive for this DTC.
    
    If this option is disabled, the DTC will be removed from permanent memory after the MIL becomes
    inactive for this event.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: DemOBDRestartDcyOnClearDTC
  长名称: OBD Restart Dcy On ClearDTC
  描述: |
    With ClearDTC (Mode $04 or Service $14FFFFFF) the DEM may restart the OBD driving cycle
    independent of its current qualification state.
    
    If enabled, the DEM restarts the OBD driving cycle (configured as
    DemOperationCycleType==DEM_OPCYC_OBD_DCY) with Mode $04 or Service $14 FFFFFF requests.
    
    If disabled, no cycle is restarted with Mode $04 or Service $14 FFFFFF requests.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: DemClearPermanentDtcBehavior
  长名称: OBD Clear Permanent Dtc Behavior
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    DEM_CLR_PERM_DTC_TYPE_1 (default):
        Permanent DTC is erased if only tested passed (and not tested failed) during the driving
    cycle and if permanent fault code condition is fulfilled.
    DEM_CLR_PERM_DTC_TYPE_2:
       Permanent DTC with IUMPR monitoring is erased if only tested passed (and not tested failed)
    during the driving cycle.
       Permanent DTC without IUMPR monitoring is erased if only tested passed (and not tested
    failed) during the driving cycle and if permanent fault code condition is fulfilled.
  默认值: DEM_CLR_PERM_DTC_TYPE_1
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: DemOBDSimilarConditionsSupport
  长名称: ''
  描述: This configuraton switch defines, whether support for similar conditions is enabled or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: DemOBDRdyThisDcyComprehensiveComponentsAlwaysComplete
  长名称: OBD Readiness This Driving Cycle Comprehensive Components Always Complete
  描述: Switch to control if Comprehensive Components Monitoring is always reported as complete or
      calculated based on current DTC status in PID $41 and J1939 diagnostic readiness 3.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: DemOBDSupportMajorMonitors
  长名称: ''
  描述: Allows to configure the event readiness group to something different to Comprehensive
      Components Monitoring.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: DemReportBlinkingMilAsActive
  长名称: Report Blinking Mil As Active
  描述: |
    If enabled, the DEM reports the MIL as 'activated' if its current state is BLINKING and/or
    CONTINUOUS.
    If disabled, the DEM reports the MIL as 'activated' only if its current state is CONTINUOUS (see
    parameter
    Dem/DemConfigSet/DemEventParameter/DemEventClass/DemIndicatorAttribute/DemIndicatorBehaviour).
    
    This influences the behavior of PID $01, PID $F501, PID $21 and PID $4D.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: DemOBDPermanentChronologyMaxNumberEvents
  长名称: OBD Permanent Chronology Max Number Events
  描述: |
    Maximum number of events which can be stored in the chronology of confirmed events.
    
    This chronology is used to identify the next DTC to be stored in the permanent memory, if the
    permanent memory was full and an entry gets freed.
    Each event in the chronology adds two more bytes to the Dem's status NvRAM block.
    
    It is recommended to configure a value that corresponds to the maximum number of DTCs fulfilling
    the criteria for permanent storage at the same time in a (realistic) worst case scenario.
    To ensure that always the oldest confirmed DTC is stored in the permanent memory or if NvRam
    consumption is not a critical restriction, set the value to the maximum number of DTCs having
    the MIL attached (OBDII or OBDonUDS) or the maximum number of class A and B1 DTCs (WWHOBD).
  默认值: ''
  最小值: 1
  最大值: 65534
- 
  序号: 23
  名称: DemOBDFuelSystemAlwaysComplete
  长名称: OBD PID Fuel System Always Complete
  描述: |
    This switch describes whether the completeness status for fuel system monitors is calculated or
    always indicated as complete in:
    - PID $01,
    - PID $41,
    - PID $F501.
    - J1939 diagnostic readiness 1 and
    - J1939 diagnostic readiness 3.
    
    True: Fuel system monitoring is always reported as complete.
    False: Completeness of fuel system monitoring is calculated based on non-continuous fuel system
    monitor status.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: DemOBDCompressionMisfireAlwaysComplete
  长名称: OBD PID Compression Misfire Always Complete
  描述: |
    This switch describes whether the completeness status for misfire monitors is calculated or
    always indicated as complete for compression ignition engines (DemGeneralOBD/DemOBDEngineType ==
    DEM_IGNITION_COMPRESSION) in
    - PID $01,
    - PID $41,
    - J1939 diagnostic readiness 1 and
    - J1939 diagnostic readiness 3.
    
    In the data contexts above, misfire monitors will always indicate completed for spark ignition
    engines independently of this parameter value.
    
    For PID $F501, the completion of readiness group Misfire is always calculated.
    
    True: Misfire monitoring is always reported as complete.
    False: Completeness of misfire monitors is calculated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: DemOBDPermanentDtcImmediateReport
  长名称: OBD PermanentDtc Immediate Report
  描述: |
    Only relevant for OBD II and OBD on UDS legislation.
    TRUE: All Permanent Dtcs are available via OBD  mode 0A immediately after WIR bit is visible
    FALSE: Only DTCs for which
    /DemEventParameter/DemEventClass/DemOBDVisibilityDelayedUntilDcyQualification is disabled and
    the /DemEventParameter/DemEventClass/DemEventFailureCycleCounterThreshold is configured to 0 are
    visible in mode 0A immediately, all other DTCs only after OBD driving cycle is restarted.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: DemOBDPermanentForWWHOBD
  长名称: OBD Support Permanent DTC for WWHOBD
  描述: |
    Only relevant for WWH-OBD legislation.
    If enabled, class A or B1 DTCs commanding the MIL can store a permanent DTC. See Technical
    Reference for OBD for more details.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: DemOBDPIDF501ComprehensiveComponentsAlwaysComplete
  长名称: OBD PIDF501 Comprehensive Components Always Complete
  描述: This switch describes whether the completeness status for comprehensive components monitors in
      PID $F501 is calculated or always indicated as complete.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: DemEngineRuntimeSecondsPolling
  长名称: Engine Runtime Seconds Polling
  描述: |
    Allow to configure the time for the periodic polling of the engine runtime in seconds.
    
    The value must be a multiple of the DemGeneral/DemTaskTime. Otherwise it is rounded down to the
    next multiple value of DemTaskTime.
    
    This value is mandatory, when parameter DemOBDTimeSinceEngineStartSeconds is required. If
    missing, it defaults to the DemTaskTime.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a diffenent unit.
  默认值: 60
  最小值: 0.001
  最大值: 2678400
- 
  序号: 29
  名称: DemSupportedObdUdsDtcSeparation
  长名称: OBD Support OBDonUDS DTC Separation
  描述: |
    Only relevant for OBDonUDS legislation.
    
    When this parameter is set to true, the OBD UDS DTC separation feature is enabled, i.e. the
    configured 3 byte OBD DTC value (DemConfigSet/DemDTCClass/DemObdDTC3Byte) is reported in all
    OBDonUDS related services (see SAE J1979-2).
    If this parameter is set to false, the OBD UDS DTC separation is disabled, i.e. the UDS DTC
    value (DemConfigSet/DemDTCClass/DemUdsDTC) is reported instead. This is the default behavior.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: DemDisableEventMonitoringInCurrentDcy
  长名称: ''
  描述: |
    This switch allows the user to disable event monitoring in current driving cycle.
    Usage of the API Dem_DisableEventMonitoringInCurrentDcy() will make the event be considered as
    tested completed during the readiness calculation of the following readiness data:
    
    - PID $01,
    - PID $F501.
    - DM05.
  默认值: false
  最小值: ''
  最大值: ''
```

### 56. DemCallbackOBDDTCStatusChanged

**描述**: The presence of this container indicates, that the Dem has access to a "DTCStatusChanged" callback,
which the Dem will call to notify other components about the change in the status of a DTC.
(not supported)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCallbackDTCStatusChangedFnc
  长名称: ''
  描述: |
    Function name of prototype "DTCStatusChanged".
    (not supported)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 57. DemGroupOfDTC

**描述**: This container represents a DTC group.

DTC groups can be cleared by service $14, if allowed by the OEM specification.
In case only $14 FFFFFF shall be offered, it is recommended to not configure DTC groups.

Defined groups are sorted according their 'DemGroupDTCs' value in increasing sequence and get
assigned these semantics: (1) PowertrainGroup, (2) ChassisGroup, (3) BodyGroup, (4) NetworkGroup.
For example when you define only 2 groups, the lower GroupDTC value represents the PowertrainGroup,
the higher GroupDTC value represents the ChassisGroup. Undefined are Body- and NetworkGroup.


#### 参数列表

```yaml
- 
  序号: 1
  名称: DemGroupDTCs
  长名称: Group DTCs
  描述: |
    DTC value of the selected group of DTC.
    
    A clear DTC request for this number will clear all DTCs that belong to this group.
  默认值: ''
  最小值: 1
  最大值: 16777214
```

### 58. DemIndicator

**描述**: This container represents a warning indicator (e.g. indicator lamp).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIndicatorID
  长名称: ''
  描述: |
    Internal identifier of the indicator.
    
    This number is calculated internally and shall not be configured manually. This parameter is
    only available to publish the result of this calculation.
    Applications using Dem APIs must not rely on the value of this parameter. Instead, they must use
    the symbolic constant (SymbolicNameValue) DemConf_DemIndicator_{SHORT-NAME}.
  默认值: 255
  最小值: 0
  最大值: 255
```

### 59. DemNvRamBlockId

**描述**: This container represent a non-volatile memory block used by the Dem.

If no permanent storage of event memory entries is required, no block needs to be configured.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemNvRamBlockIdIndex
  长名称: NvRam BlockId Index
  描述: |
    For non-unique block types, this index identifies the exact block (see DemNvRamBlockIdType).
    
    This parameter must exist and be able to identify all NvBlocks of following kind:
    PRIMARY: each index must have an unique value and the index values must complete the range 0 -
    (DemMaxNumberEventEntryPrimary -1),
    USERDEFINED: for all blocks with the same DemNvRamBlockIdEventMemoryRef reference, each index
    must have an unique value and all index values must complete the range 0 -
    (DemMaxNumberEventEntryUserDefined -1),
    TIMESERIES: for all blocks with the same DemNvRamBlockIdEventMemoryRef reference, each index
    must have an unique value and all index values must complete the range 0 -
    (DemMaxNumberTimeSeriesSnapshots -1),
    
    The value is necessary to store the correct memory entry in case it was changed.
    
    For all NvBlocks of other kind (e.g. ADMIN, STATUS,...) the parameter value will be ignored.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemNvRamBlockIdType
  长名称: NvRam BlockId Type
  描述: |
    Usage kind of this NvBlock.
    
    This parameter is used to identify which block data needs to be stored when event data is
    modified.
    
    Following block types exist at most once:
    ADMIN: Always required.
    
    STATUS: Always required.
    
    MIRROR: Only required if DemGeneral/DemMaxNumberEventEntryMirror > 0.
    
    PERMANENT: Only required if DemGeneral/DemMaxNumberEventEntryPermanent > 0.
    
    FREEZEFRAME: Only required if DemGeneral/DemOBDSupport is enabled and
    DemGeneral/DemGeneralOBD/DemOBDLegislation == OBDII or OBD_ON_UDS.
    
    OBDIUMPR: Only required if DemGeneral/DemOBDSupport is enabled and DemGeneral/DemRatioId
    containers are configured.
    
    DEBOUNCE: Only required if any event uses CounterBased Debouncing with
    DemDebounceCounterStorage==TRUE.
    
    AVAILABILITY: Only required if event availability status is persisted in non-volatile memory due
    DemAvailabilityStorage==TRUE.
    
    DTR: Only required if DemGeneral/DemOBDSupport is enabled and
    if DemConfigSet/DemDtrs/DemDtr container exist or
    DemGeneral/DemPostBuild/DemMaxNumberEventEntryPermanent > 0
    
    AGING: Only required if aging data is persisted in non-volatile memory due to
    DemGeneral/DemSupportAgingForAllDTCs==TRUE or if
    DemGeneral/DemDataClass/DemDataElementInternalData == AGED_COUNTER is used.
    
    CYCLECOUNTER: Only required if cycle counter data is persisted in non-volatile memory due to
    DemGeneral/DemSupportStorageIndependentCycleCounters ==TRUE.
    
    Following block types can exist several times, depending on the configuration:
    PRIMARY: The number of containers of this type must match
    DemGeneral/DemEventMemorySet/DemPrimaryMemory/DemMaxNumberEventEntryPrimary.
    
    USERDEFINED: The number of containers of this type must match the summarized number of all
    DemGeneral/DemEventMemorySet/DemUserDefinedMemory/DemMaxNumberEventEntryUserDefined.
    
    TIMESERIES: The number of containers of this type must match the summarized number of
    DemMaxNumberTimeSeriesSnapshots in DemGeneral/DemEventMemorySet/DemPrimaryMemory and all
    DemGeneral/DemEventMemorySet/DemUserDefinedMemory containers.
    
    CUSTOMTRIGGER: The number of containers of this type must match the summarized number of
    DemMaxNumberCustomTriggeredSnapshots in DemGeneral/DemEventMemorySet/DemPrimaryMemory and all
    DemGeneral/DemEventMemorySet/DemUserDefinedMemory containers.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 60. DemOperationCycle

**描述**: This container represents a monitoring cycle.

They are used to control event monitoring and aging.
Although this container does not define a symbolic name value, one is generated nonetheless.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemOperationCycleAutomaticEnd
  长名称: OperationCycle Automatic End
  描述: |
    If configured to true the DEM automatically ends the cycle during ECU restart (e.g. in
    Dem_Shutdown or Dem_Init).
    Otherwise the application has to end the cycle by calling Dem_SetOperationCycleState with state
    DEM_CYCLE_STATE_END.
    This option is only relevant when DemOperationCycleStatusStorage is TRUE.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemOperationCycleAutostart
  长名称: OperationCycle Automatic Start
  描述: |
    The autostart property defines if the operation cycles is automatically (re-)started during
    Dem_PreInit.
    (Not supported, please use DemGeneral/DemRestartCycleOnInitRef instead)
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemOperationCycleType
  长名称: OperationCycle Type
  描述: |
    Select the operation cycle type.
    
    This value only has an effect in case of OBD ECUs, as certain actions are triggered by
    legislated cycle types.
    Note: As there is no way to read the value of the parameter at run time, the short name of the
    DemOperationCycle container should have a meaningful name.
  默认值: DEM_OPCYC_OTHER
  最小值: ''
  最大值: ''
```

### 61. DemRatioId

**描述**: This container contains the OBD specific ratio Id configuration.

It is related to a specific event, a FID, and an IUMPR group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIUMPRDenGroup
  长名称: Dem IUMPR Denominator Group
  描述: |
    This parameter specifies the assigned denominator type which is applied in addition to the
    General Denominator conditions.
    
    NONE: The denominator is calculated based on the general individual denominator conditions.
    
    PHYS_API: The denominator is calculated based on the general individual denominator conditions.
    The denominator can be locked via dedicated APIs.
    
    COLDSTART, EVAP, 500MI: The denominator is calculated based on the general individual
    denominator conditions and additional conditions that must be fulfilled before the denominator
    is incremented.
    
    INDEPENDENT: Denominator may be incremented independently of the general individual denominator.
    The denominator may be locked via dedicated APIs.
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
  名称: DemRatioIdType
  长名称: RatioId Type
  描述: |
    This parameter specifies how the numerator of the ratio is calculated:
    
    OBSERVER: The numerator is incremented whenever a test result is reported. This setting is used
    for symmetrical monitors.
    
    API: The numerator is incremented if the related monitoring function is able to detect a fault
    (reported by dedicated API). This setting is used for asymmetrical monitors.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 62. DemRatio

**描述**: (Not supported yet, please use the AUTOSAR 4.0.3 compliant definition in /Dem/DemGeneral/DemRatioId)
This container contains the OBD specific ratio Id configuration. It is related to a specific event,
a FID, and an IUMPR group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemIUMPRDenGroup
  长名称: Dem IUMPR Denominator Group
  描述: |
    (Not supported yet, please use the AUTOSAR 4.0.3 compliant definition in
    /Dem/DemGeneral/DemRatioId)
    This parameter specifies the assigned denominator type which is applied in addition to the
    General Denominator conditions.
    
    NONE: The denominator is calculated based on the general denominator conditions.
    
    PHYS_API: The denominator can be locked via dedicated APIs.
    
    COLDSTART, EVAP, 500MILL: Additional conditions must be fulfilled before the denominator is
    incremented.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemIUMPRGroup
  长名称: ''
  描述: |
    (Not supported yet, please use the AUTOSAR 4.0.3 compliant definition in
    /Dem/DemGeneral/DemRatioId)
    This parameter specifies the assigned IUMPR group of the ratio Id.
    Currently it is not used by the DEM and has no effect.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemRatioId
  长名称: ''
  描述: |
    (Not supported yet, please use the AUTOSAR 4.0.3 compliant definition in
    /Dem/DemGeneral/DemRatioId)
    Defines a unique ratio Id.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: DemRatioKind
  长名称: RatioId Kind
  描述: |
    (Not supported yet, please use the AUTOSAR 4.0.3 compliant definition in
    /Dem/DemGeneral/DemRatioId)
    This parameter specifies how the numerator of the ratio is calculated:
    
    OBSERVER: The numerator is incremented whenever a test result is reported. This setting is used
    for symmetrical monitors.
    
    API: The numerator is incremented if the related monitoring function is able to detect a fault
    (reported by dedicated API). This setting is used for asymmetrical monitors.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 63. DemStorageCondition

**描述**: This container represents a single storage condition.

Please note: storage conditions can not be used directly but must be grouped (see
DemStorageConditionGroup).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemStorageConditionId
  长名称: StorageCondition Id
  描述: |
    Internal identifier of the storage condition.
    
    This number is calculated internally and shall not be configured manually. This parameter is
    only available to publish the result of this calculation.
    Applications using Dem APIs must not rely on the value of this parameter. Instead, they must use
    the symbolic constant (SymbolicNameValue) DemConf_DemStorageCondition_{SHORT-NAME}.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemStorageConditionStatus
  长名称: StorageCondition Status
  描述: |
    Defines the status of this storage condition after full initialization, i.e. when
    Dem_MasterInit() or Dem_Init() finished.
    After pre-initialization, but before the full intialization (between Dem_(Master)PreInit() and
    Dem_(Master)Init() ) the status is always 'true'.
    Changes to the storage condition status during runtime are not persisted non-volatile. The
    status of this storage condition will always be reset to this configuration value during
    Dem_MasterInit() or Dem_Init().
  默认值: true
  最小值: ''
  最大值: ''
```

### 64. DemStorageConditionGroup

**描述**: This container groups several storage conditions.

EventParameters only reference one of these groups, not individual storage conditions.

该容器没有参数。

### 65. DemPidConfiguration

**描述**: This container contains options controlling the support of OBD PIDs by the Dem module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemSupportPid01
  长名称: Support PID 01
  描述: Monitor status since DTCs were last cleared.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemSupportPid1C
  长名称: Support PID 1C
  描述: OBD requirements to which the vehicle is designed.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemSupportPid21
  长名称: Support PID 21
  描述: |
    Emission OBD:
    Distance travelled while MIL is active.
    
    ZEVonUDS:
    Distance travelled while any ZEV propulsion related DTC is confirmed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DemSupportPid30
  长名称: Support PID 30
  描述: Number of WarmUp cycles since DTCs were last cleared.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DemSupportPid31
  长名称: Support PID 31
  描述: Distance since DTCs were last cleared.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DemSupportPid41
  长名称: Support PID 41
  描述: Monitor status of this driving cycle.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DemSupportPid4D
  长名称: Support PID 4D
  描述: |
    Emission OBD:
    Engine run time while MIL is active.
    
    ZEVonUDS:
    Engine run time while any ZEV propulsion related DTC is confirmed.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DemSupportPid4E
  长名称: Support PID 4E
  描述: Engine run time since DTCs were last cleared
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DemSupportPid91
  长名称: Support PID 91
  描述: WWH-OBD ECU OBD System Information
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DemSupportVid08
  长名称: Support VID 08
  描述: |
    In-use performance tracking - spark ignition vehicle.
    
    This parameter is not supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DemSupportVid0B
  长名称: Support VID 0B
  描述: |
    In-use performance tracking - compression ignition vehicle.
    
    This parameter is not supported.
  默认值: false
  最小值: ''
  最大值: ''
```

### 66. DemMILGroup

**描述**: This container represents a group of events that use a common trip counter to determine their MIL
status.

Incrementing the common trip counter is triggered by any event of the MIL group.
Healing is performed individually for each event of the MIL group, but the common trip counter is
only reset after all events of the group have been healed.

The reference to a MIL group is configured at the DTCClass container.

该容器没有参数。

### 67. DemPostbuild

**描述**: The content of this container is only relevant for the implementation variant PostBuild
(POST-BUILD-LOADABLE).

For implementation variant PreCompile (and therfore PostBuild-Selectable without -Loadable) all
contained parameters are ignored.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemEventAvailableDefaultSupport
  长名称: ''
  描述: |
    Select whether the default availability value should be initialized with Dem_Init()
    
    TRUE: Use the default values from configuration parameter
    DemConfigSet/DemEventParameter/DemEventAvailable to set the initial value during Dem_Init()
    FALSE: The availability information is not changed during Dem_Init()
    
    If this setting is enabled, API Dem_SetEventAvailable cannot be used before Dem_Init() due to
    Dem_Init() overwriting the active setting.
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemMaxSizeFreezeFrame
  长名称: Max Size FreezeFrame
  描述: |
    Enlarge the (RAM/NvRAM) size of the largest FreezeFrame record.
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents the size of largest defined FreezeFrame record. The minimum value is
    auto-calculated when you start "Validate" or "Generate" - set value 0 to force the recalculation
    of the min value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve additional space in the NvRAM blocks. Later in the post-build phase you can
    choose different DIDs (or a different number of DIDs) for a defined FreezeFrame - as long as the
    size of the new selected DIDs still fit into the reserved space.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value (when it is smaller than the configured, largest FreezeFrame's size. Changing
    the FreezeFrame's DIDs afterwards may shorten the largest FreezeFrame's size - but this will NOT
    decrease this value again! Set the value to '0' and start "Validate" or "Generate" for the DEM
    to calculate again the minimum size.
    
    "Size of a freeze frame" is calculated as: Summarize the size of all referred DemDidClasses in a
    DemGeneral/DemFreezeFrameClass. The size of a DidClass is calculated as: Summarize the size of
    all referred DemNNDataElementClass elements by adding their DemDataElementDataSize values.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: DemMaxNumberDtr
  长名称: Max Number Dtr
  描述: |
    Enlarge the (RAM/NvRAM) to store an upper limit of Dtr elements.
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents an upper limit to the maximum value (+1) of the DemDtrId, calculated over all
    variants. This maximum value is auto-calculated when you start "Validate" or "Generate" - set
    value 0 to force the recalculation of the min value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve additional number of Dtr elements. Later in the post-build phase you can change
    Dtr configuration (also create and delete Dtrs) - as long as the maximum value (+1) of the
    DemDtrId calculated over all variants is smaller than this value.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value (when it is smaller than the configured). Deleting Dtrs afterwards may
    decrease the lowest possible value - but this will NOT decrease this configured value again! Set
    the value to '0' and start "Validate" or "Generate" for the DEM to calculate again the minimum
    size.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: DemMaxSizeGlobalFreezeFrame
  长名称: ''
  描述: |
    Enlarge the (RAM/NvRAM) size of the global freeze frame record.
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents the size of the global freeze frame record. The minimum value is auto-calculated
    when you start "Validate" or "Generate" - set value 0 to force the recalculation of the min
    value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve additional space in the NvRAM blocks. Later in the post-build phase you can
    choose different DIDs (or a different number of DIDs) for the global freeze frame - as long as
    the size of the new selected DIDs still fits into the reserved space.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value when it is smaller than the configured global freeze frame size. Changing the
    freeze frame's DIDs afterwards may shorten the global freeze frame size - but this will NOT
    decrease this value again! Set the value to '0' and start "Validate" or "Generate" for the DEM
    to calculate again the minimum size.
    
    "Size of the global freeze frame" is calculated as: Summarize the size of all referred
    DemDidClasses in the DemGeneral/DemGlobalFreezeFrame/DemGlobalFreezeFrameClassRef. The size of a
    DidClass is calculated as: Summarize the size of all referred DemDataClass elements by adding
    their DemDataElementDataSize values.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: DemMaxSizeTimeSeriesFreezeFrame
  长名称: ''
  描述: |
    Enlarge the (RAM/NvRAM) size of the time series snapshot records (also known as multi-sample
    development snapshot records).
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents the size of a time series snapshot record. The minimum value is auto-calculated
    when you start "Validate" or "Generate" - set value 0 to force the recalculation of the min
    value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve additional space in the NvRAM blocks. Later in the post-build phase you can
    choose different DIDs (or a different number of DIDs) for the time series snapshot record - as
    long as the size of the new selected DIDs still fits into the reserved space.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value when it is smaller than the configured time series snapshot record size.
    Changing the freeze frame's DIDs afterwards may shorten the time series snapshot record size -
    but this will NOT decrease this value again! Set the value to '0' and start "Validate" or
    "Generate" for the DEM to calculate again the minimum size.
    
    "Size of the time series snapshot record" is calculated as: Summarize the size of all referred
    DemDidClasses in the DemGeneral/DemFreezeFrameClass used in
    DemConfigSet/DemEventParameter/DemDevFreezeFrameBClassRef. The size of a DidClass is calculated
    as: Summarize the size of all referred DemDataClass elements by adding their
    DemDataElementDataSize values.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: DemMaxSizeOBDonUDSFreezeFrame
  长名称: Max Size OBD on UDS FreezeFrame
  描述: |
    Enlarge the (RAM/NvRAM) size of the largest OBD on UDS FreezeFrame record.
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents the size of largest defined OBD on UDS FreezeFrame record. The minimum value is
    auto-calculated when you start "Validate" or "Generate" - set value 0 to force the recalculation
    of the min value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve additional space in the NvRAM blocks. Later in the post-build phase you can
    choose different DIDs (or a different number of DIDs) for a defined FreezeFrame - as long as the
    size of the new selected DIDs still fit into the reserved space.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value (when it is smaller than the configured, largest FreezeFrame's size. Changing
    the FreezeFrame's DIDs afterwards may shorten the largest FreezeFrame's size - but this will NOT
    decrease this value again! Set the value to '0' and start "Validate" or "Generate" for the DEM
    to calculate again the minimum size.
    
    "Size of a freeze frame" is calculated as: Summarize the size of all referred DemDidClasses in a
    DemGeneral/DemFreezeFrameClass. The size of a DidClass is calculated as: Summarize the size of
    all referred DemDataElement Class elements by adding their DemDataElementDataSize values.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: DemMaxNumberEventsWithMonitorActivityData
  长名称: Max Number Events With Monitor Activity Data
  描述: |
    This parameter is only relevant for OBD on UDS legislation.
    
    Enlarge the (RAM/NvRAM) to store an upper limit of Monitor Activity Data (see
    Dem/DemGeneral/DemDataClass/DemDataElementInternalData MONITOR_ACTIVITY_DATA).
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents an upper limit for the number of events for which Monitor Activity Data can be
    stored. This maximum value is auto-calculated when you start "Validate" or "Generate" - set
    value 0 to force the recalculation of the min value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve an additional number of events with Monitor Activity Data. Later in the
    post-build phase you can change the DemExtendedDataClassRef of an event and thereby the
    DemExtendedDataRecordClasses referenced by an event - as long as the maximum number of events
    with Monitor Activity Data is smaller or equal to this value.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value (when it is smaller than the configured). Changing DemExtendedDataClassRefs
    or DemExtendedDataClasses afterwards may decrease the lowest possible value - but this will NOT
    decrease this configured value again! Set the value to '0' and start "Validate" or "Generate"
    for the DEM to calculate again the minimum number.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: DemMaxNumberEventsPtoTimer
  长名称: Max Number Events With PTO Timer
  描述: |
    This parameter is only relevant if any event is affected by the Dem PTO handling (see
    /DemEventParameter/DemEventClass/DemConsiderPtoStatus) and the Dem calculates the monitor status
    since DTCs cleared for PID $01, PID $F501 or J1939 diagnostic readiness 1.
    For each event affected by the Dem PTO handling that has an OBD Readiness group (see
    /DemEventParameter/DemEventClass/DemEventOBDReadinessGroup), an event specific PTO timer is
    maintained to track the cumulative engine runtime with PTO active.
    
    Enlarge the (RAM/NvRAM) to store an upper limit of event specific PTO timers.
    
    This parameter is mandatory for implementation variant PostBuild-Loadable, it will be ignored
    for other implementation variants.
    
    It represents an upper limit for the number of events for which a PTO timer can be maintained.
    This maximum value is auto-calculated when you start "Validate" or "Generate" - set value 0 to
    force the recalculation of the min value.
    For PostBuild-Loadable variants, during the pre-compile configuration phase you can enlarge the
    value to reserve an additional number of events with PTO timer. Later in the post-build phase
    you can change the DemEventOBDReadinessGroup of an event as long as the maximum number of events
    with PTO timer is smaller or equal to this value.
    
    Take care: for PostBuild-Loadable implementation variants the auto-calculation will only
    increase the value (when it is smaller than the configured). Changing the
    DemEventOBDReadinessGroup of an event afterwards may decrease the lowest possible value - but
    this will NOT decrease this configured value again! Set the value to '0' and start "Validate" or
    "Generate" for the DEM to calculate again the minimum number.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 68. DemGlobalFreezeFrame

**描述**: In this container the attributes and content of the global freeze frame can be configured.
If this container is configured, global freeze frame data is stored for each event (In addition to
Dem/DemConfigSet/DemEventParameter/DemFreezeFrameClassRef).

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemGlobalFreezeFrameRecordNumber
  长名称: ''
  描述: This parameter defines the record number of the global freeze frame.
  默认值: ''
  最小值: 1
  最大值: 254
- 
  序号: 2
  名称: DemGlobalFreezeFrameRecordUpdate
  长名称: ''
  描述: |
    This parameter defines, whether the global freeze frame is updated with each trigger.
    
    DEM_UPDATE_RECORD_NO: The global freeze frame is captured only once.
    
    DEM_UPDATE_RECORD_YES: The global freeze frame is captured with each trigger, overwriting the
    previously captured data (currently not supported).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DemGlobalFreezeFrameRecordTrigger
  长名称: ''
  描述: |
    This parameter defines the trigger to store the global freeze frame. Currently only trigger
    CONFIRMED is supported.
    
    FDC_THRESHOLD: The global freeze frame capture is triggered by a fault detection counter passing
    a storage threshold.
    
    CONFIRMED: The global freeze frame capture is triggered by the ConfirmedDTC transition from 0 to
    1.
    
    PENDING: The global freeze frame capture is triggered by the PendingDTC transition from 0 to 1.
    
    TEST_FAILED: The global freeze frame capture is triggered by the TestFailed transition from 0 to
    1.
    
    TEST_FAILED_FIRST_IN_CYCLE: The global freeze frame capture is triggered by the first TestFailed
    transition from 0 to 1 in an operation cycle.
    
    FDC_FIRST_IN_CYCLE: The global freeze frame capture is triggered by the first DTC fault
    detection counter reaching the storage threshold in an operation cycle.
    
    Please note that triggers occuring before an event memory entry is allocated are discarded.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 69. DemTimeSeriesSnapshotClass

**描述**: This container contains a list of dedicated, different time series snapshot records (also known as
multi-sample development snapshot records)

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemTimeSeriesMaxNumberPastSamples
  长名称: ''
  描述: |
    This configuration value defines how many past samples are stored for an event at event FDC
    storage threshold,
    if the use of time series snapshot records (also known as multi-sample development snapshot
    records) is configured for the event.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: DemTimeSeriesMaxNumberFutureSamples
  长名称: ''
  描述: (not supported)
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DemTimeSeriesSamplingTime
  长名称: ''
  描述: |
    This configuration value defines the time interval for the periodic collection of the samples.
    
    The value must be a multiple of the DemGeneral/DemTaskTime. Otherwise it is rounded down to the
    next multiple value of DemTaskTime.
    
    The AUTOSAR configuration standard is to use SI units, so in the EcuC file this parameter is
    stored as float value in seconds - the DaVinci Configurator 5 GUI will convert the value when
    using a different unit.
  默认值: 1
  最小值: 0.001
  最大值: 65.535
- 
  序号: 4
  名称: DemTimeSeriesSampleBufferSize
  长名称: ''
  描述: |
    This configuration value defines the size of the ring buffer in RAM in which the collected DIDs
    are stored. The value is multiplied with the number of past samples configured in
    DemGeneral/DemTimeSeriesSnapshotClass/DemTimeSeriesMaxNumberPastSamples.
    
    The ring buffer has to be large enough to store all DIDs relevant for events referencing this
    DemTimeSeriesSnapshotClass container. You get an error message when the configured value is too
    small.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: DemTimeSeriesStartingSequentialDIDIdentifier
  长名称: ''
  描述: |
    This configuration value defines the starting sequential DID identifier.
    For events referencing this DemTimeSeriesSnapshotClass container, the sequential DID identifiers
    start from this value.
    
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 70. DemGeneralCalibration

**描述**: Contains configuration options for calibration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DemCalibrationCounterBasedDebouncingSupport
  长名称: Support Calibration for Counter Based Debouncing
  描述: |
    If this parameter is set to true, the following parameters of a
    DemConfigSet/DemDebounceCounterBasedClass can be calibrated:
    
    - DemDebounceCounterIncrementStepSize
    - DemDebounceCounterFailedThreshold
    - DemDebounceCounterPassedThreshold
    - DemDebounceCounterJumpUp
    - DemDebounceCounterJumpUpValue
    - DemDebounceCounterJumpDown
    - DemDebounceCounterJumpDownValue
    - DemCounterBasedFdcThresholdStorageValue
    - DemDebounceContinuous
    - DemDebounceBehavior
    - DemDebounceCounterDecrementStepSize: In contrast to the initially configured value, when
    calibrating this parameter the modified value needs to be negative, i.e. it is equal to
    configured value * (-1).
    
    For events with counter based debouncing it is also possible to calibrate which event references
    which counter based debouncing class.
    
    Note: To support calibration of counter based debounce classes, optimizations are disabled for
    the tables containing these classes. This can lead to increased memory consumption.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DemCalibrationAdditionalCounterBasedDebouncingClasses
  长名称: Additional Counter Based Debounce Classes
  描述: |
    This parameter is only relevant if
    DemGeneral/DemGeneralCalibration/DemCalibrationCounterBasedDebouncingSupport is set to true.
    
    This parameter specifies the number of DemCounterBasedDebouncingClasses that shall be
    calibratable in addition the configured and referenced
    DemConfigSet/DemDebounceCounterBasedClasses.
    The values of these additional classes can be calibrated (see
    DemCalibrationCounterBasedDebouncingSupport) and can be referenced by any event using counter
    based debouncing via calibration.
  默认值: 0
  最小值: 0
  最大值: 65535
```

