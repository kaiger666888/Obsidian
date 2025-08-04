# FrTSyn

## 模块描述

This represents the specific configuration variant for the TSyn on Flexray.

## 容器列表

### 1. FrTSynGeneral

**描述**: This container holds the general parameters of the Flexray-specific Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynDevErrorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTSynMainFunctionPeriod
  长名称: ''
  描述: Schedule period of the main function FrTSyn_MainFunction. Unit: [s].
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: FrTSynVersionInfo
  长名称: ''
  描述: Activate/Deactivate the version information API (FrTSyn_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. FrTSynGlobalTimeOfsDataIDList

**描述**: The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 3. FrTSynGlobalTimeOfsDataIDListElement

**描述**: Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeOfsDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for OFS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: FrTSynGlobalTimeOfsDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for OFS messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. FrTSynGlobalTimeSyncDataIDList

**描述**: The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation
process.

该容器没有参数。

### 5. FrTSynGlobalTimeSyncDataIDListElement

**描述**: Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC
calculation process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeSyncDataIDListIndex
  长名称: ''
  描述: Index of the DataIDList for SYNC messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: FrTSynGlobalTimeSyncDataIDListValue
  长名称: ''
  描述: Value of the DataIDList for SYNC messages ensures the identification of data elements due to
      CRC calculation process.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 6. FrTSynGlobalTimeDomain

**描述**: This represents the existence of a global time domain on Flexray. The FrTSyn module can administrate
several global time domains at the same time that in itself form a hierarchy of domains and
sub-domains.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeDomainId
  长名称: ''
  描述: The global time domain ID.
  默认值: ''
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: FrTSynGlobalTimeSequenceCounterJumpWidth
  长名称: ''
  描述: The SequenceCounterJumpWidth specifies the maximum allowed gap of the Sequence Counter between
      two SYNC resp. two OFS messages.
  默认值: ''
  最小值: 1
  最大值: 15
```

### 7. FrTSynGlobalTimeMaster

**描述**: Configuration of the global time master. Each global time domain is required to have exactly one
global time master. This master may or may not exist on the configured ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeTxCrcSecured
  长名称: ''
  描述: This represents the configuration of whether or not CRC is supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrTSynGlobalTimeTxPeriod
  长名称: ''
  描述: This represents the TX period. Unit: seconds
  默认值: ''
  最小值: 0
  最大值: 1.7976931348623157E+308
```

### 8. FrTSynGlobalTimeMasterPdu

**描述**: This container carries all properties required to configure the PDU sent by the global time master
for the given global time domain.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeMasterConfirmationHandleId
  长名称: ''
  描述: This represents the handle ID of the PDU that contains the global time information.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 9. FrTSynGlobalTimeSlave

**描述**: This represents the time slave for the enclosing global time domain.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynRxCrcValidated
  长名称: ''
  描述: This parameter controls whether or not CRC validation shall be supported.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. FrTSynGlobalTimeSlavePdu

**描述**: This container carries all properties required to configure the PDU received by the time slave for
the given global time domain.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrTSynGlobalTimeSlaveHandleId
  长名称: ''
  描述: This represents the handle ID of the PDU that contains the global time information.
  默认值: 0
  最小值: 0
  最大值: 65535
```

