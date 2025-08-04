# CanTSyn

## 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module with respect to global time
handling on CAN.

## 容器列表

### 1. CanTSynGeneral

**描述**: This container holds the general parameters of the CAN-specific Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynDevErrorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanTSynMainFunctionPeriod
  长名称: ''
  描述: Schedule period of the main function CanTSyn_MainFunction. Unit: [s].
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: CanTSynVersionInfo
  长名称: ''
  描述: Activate/Deactivate the version information API (CanTSyn_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. CanTSynGlobalTimeFupDataIDList

**描述**: The DataIDList for FUP messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 3. CanTSynGlobalTimeFupDataIDListElement

**描述**: Element of the DataIDList for FUP messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeFupDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for FUP messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: CanTSynGlobalTimeFupDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for FUP messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. CanTSynGlobalTimeOfnsDataIDList

**描述**: The DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 5. CanTSynGlobalTimeOfnsDataIDListElement

**描述**: Element of the DataIDList for OFNS messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeOfnsDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for OFNS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: CanTSynGlobalTimeOfnsDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for OFNS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. CanTSynGlobalTimeOfsDataIDList

**描述**: The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 7. CanTSynGlobalTimeOfsDataIDListElement

**描述**: Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeOfsDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for OFS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: CanTSynGlobalTimeOfsDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for OFS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 8. CanTSynGlobalTimeSyncDataIDList

**描述**: The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 9. CanTSynGlobalTimeSyncDataIDListElement

**描述**: Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeSyncDataIDListIndex
  长名称: ''
  描述: Index for the DataIDList for SYNC messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: CanTSynGlobalTimeSyncDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for SYNC messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 10. CanTSynGlobalTimeDomain

**描述**: This represents the existence of a global time domain on CAN. The CanTSyn module can administrate
several global time domains at the same time that in itself form a hierarchy of domains and
sub-domains.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeDomainId
  长名称: ''
  描述: The global time domain ID.
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: CanTSynGlobalTimeFollowUpTimeout
  长名称: ''
  描述: Rx timeout for the follow-up message. This is only relevant for selected bus systems
      Unit:seconds
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: CanTSynGlobalTimeSequenceCounterJumpWidth
  长名称: ''
  描述: The SequenceCounterJumpWidth specifies the maximum allowed gap of the Sequence Counter between
      two SYNC resp. two OFS messages.
  默认值: ''
  最小值: 1
  最大值: 15
```

### 11. CanTSynGlobalTimeMaster

**描述**: Configuration of the global time master. Each global time domain is required to have exactly one
global time master. This master may or may not exist on the configured ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeTxCrcSecured
  长名称: ''
  描述: This represents the configuration of whether or not CRC is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanTSynGlobalTimeTxFollowUpOffset
  长名称: ''
  描述: This represents the transmission time offset between a SYNC message and the related FUP
      message resp. OFS message and related OFNS message. Unit: seconds.
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: CanTSynGlobalTimeTxPeriod
  长名称: ''
  描述: This represents configuration of the TX period. Unit: seconds
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 4
  名称: CanTSynMasterConfirmationTimeout
  长名称: ''
  描述: This represents the confirmation timeout after transmission of a SYNC message resp. OFS
      message. Unit: seconds.
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
```

### 12. CanTSynGlobalTimeMasterPdu

**描述**: This container encloses the configuration of the PDU that is supposed to contain the global time
information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeMasterConfirmationHandleId
  长名称: ''
  描述: This represents the handle ID of the PDU that contains the global time information.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 13. CanTSynGlobalTimeSlave

**描述**: Configuration of a global time slave. Each global time domain is required to have at least one time
slave. The configured ECU may or may not represent a time slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynRxCrcValidated
  长名称: ''
  描述: Definition of whether or not validation of the CRC is supported.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 14. CanTSynGlobalTimeSlavePdu

**描述**: This container encloses the configuration of the PDU that is supposed to contain the global time
information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTSynGlobalTimeSlaveHandleId
  长名称: ''
  描述: This represents the handle ID of the PDU that contains the global time information.
  默认值: 0
  最小值: 0
  最大值: 65535
```

