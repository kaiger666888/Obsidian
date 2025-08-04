# Dbg

## 模块描述

Configuration of the debugging module.

## 容器列表

### 1. DbgBuffering

**描述**: This container holds the parameters to manage the storage of debugging data in RAM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgBufferSize
  长名称: ''
  描述: Size in bytes of the RAM for the ring buffer. A size of 0 means that no buffer exists. All
      data records are directly transferred.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DbgBufferStrategy
  长名称: ''
  描述: Strategy of buffer operations when it is full: overwrite oldest entries or stop the storage.
  默认值: StopStorage
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DbgBufferTransmission
  长名称: ''
  描述: Automatic or requested transmission of the buffer.
  默认值: StartOnHostRequest
  最小值: ''
  最大值: ''
```

### 2. DbgCommunication

**描述**: This container holds all configuration parameters for communication.

该容器没有参数。

### 3. DbgRxPdu

**描述**: This container holds configuration parameters for the receive-pdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgRxPduId
  长名称: ''
  描述: Handle Id to be used by the PduR to indicate the reception of the DbgRxPdu to the Dbg module.
      The actual value of this parameter is fixed to 0 since there is only one RxPdu for the
      Dbg module.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 4. DbgTxPdu

**描述**: This container holds configuration parameters for the transmit-pdu.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgTxConfirmationPduId
  长名称: ''
  描述: Handle Id to be used by the PduR to confirm the transmission of the DbgTxPdu to the Dbg
      module. The actual value of this parameter is fixed to 0 since there is only one TxPdu
      for the Dbg module.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. DbgGeneral

**描述**: This container holds the general parameters of the debugging module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgDevErrorDetect
  长名称: ''
  描述: Enables/Disables development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DbgHeaderFileInclusion
  长名称: ''
  描述: Name of the header file(s) to be included by the Dbg module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DbgVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API (Dbg_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. DbgMultipleConfigurationContainer

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgMaxDynamicDID
  长名称: ''
  描述: Maximum number of dynamic DIDs. This value is only needed to reserve memory for dynamic DIDs
      added by the host at runtime. If this parameter is not supplied it is automatically set
      to the configured number of static DIDs.
  默认值: ''
  最小值: 0
  最大值: 200
- 
  序号: 2
  名称: DbgMaxStaticDID
  长名称: ''
  描述: Maximum number of static DIDs. This value is only needed to reserve memory for static DIDs
      added at post-build time. If this parameter is not supplied it is automatically set to
      the configured number of static DIDs. Static DIDs are zero based and consecutive.
  默认值: ''
  最小值: 0
  最大值: 200
```

### 7. DbgPredefinedDID

**描述**: This container holds all configuration parameters for predefined DIDs. For predefined DIDs, only
certain values can be changed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgPredefinedDIDActivation
  长名称: ''
  描述: Activation or not of the DID for debugging.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DbgPredefinedDIDBuffering
  长名称: ''
  描述: Buffer the data or transmit directly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DbgPredefinedDIDName
  长名称: ''
  描述: List of possible names for predefined DIDs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DbgPredefinedDIDTimeStampActivation
  长名称: ''
  描述: Using or not of time stamp.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. DbgAddInfoComSignal

**描述**: Additional information for DIDs with the DbgPredefinedDIDName set to:

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgComSignalName
  长名称: ''
  描述: Optional name of the traced signal. If present it shall be used in the display of the
      debugging tool.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. DbgAddInfoRteCall

**描述**: Additional information for DIDs with the DbgPredefinedDIDName set to:

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgCallComponentId
  长名称: ''
  描述: Id used to identify the SW-Component Type.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DbgCallInstanceId
  长名称: ''
  描述: Id used to identify the SW-Component Instance.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DbgCallPortId
  长名称: ''
  描述: Id used to identify the Port.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: DbgCallServiceId
  长名称: ''
  描述: Id used to identify the OperationProtoype.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 10. DbgAddInfoRunnable

**描述**: Additional information for DIDs with the DbgPredefinedDIDName set to:

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgRunnableComponentId
  长名称: ''
  描述: Id used to identify the SW-Component Type.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DbgRunnableId
  长名称: ''
  描述: Id used to identify the RunnableEntity.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DbgRunnableInstanceId
  长名称: ''
  描述: Id used to identify the SW-Component Instance.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 11. DbgAddInfoVfbSignal

**描述**: Additional information for DIDs with the DbgPredefinedDIDName set to:

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgVfbComponentId
  长名称: ''
  描述: Id used to identify the SW-Component Type.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DbgVfbDataElementId
  长名称: ''
  描述: Id used to identify the DataElementPrototype.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: DbgVfbInstanceId
  长名称: ''
  描述: Id used to identify the SW-Component Instance.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: DbgVfbPortId
  长名称: ''
  描述: Id used to identify the Port.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 12. DbgStaticDID

**描述**: This container holds all configuration parameters for static DIDs. For predefined DIDs, only certain
values can be changed.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgAutomaticCollectionFrequency
  长名称: ''
  描述: Cycle time of collection in DataCollectionTicks. A value of "0" indicates that the collection
      takes place only on request.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: DbgStaticDIDActivation
  长名称: ''
  描述: Activation or not of the DID for debugging.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DbgStaticDIDBuffering
  长名称: ''
  描述: Buffer the data or transmit directly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DbgStaticDIDNameRef
  长名称: ''
  描述: Name of the DID, translated by the configuration/generation tool into consecutive DID numbers
      starting from 0.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DbgStaticTimeStampActivation
  长名称: ''
  描述: Using or not of time stamp.
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. DbgAddressSizePair

**描述**: This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgASAbsoluteAddress
  长名称: ''
  描述: Absolute address of memory location to be debugged.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: DbgASNameRef
  长名称: ''
  描述: Symbolic name of the variable, translated by the configuration/generation tool into the
      address and size of the variable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DbgASSize
  长名称: ''
  描述: Absolute size in Bytes of memory location to be debugged.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 14. DbgDebugData

**描述**: Reference to staticMemory used for Debug Data.

该容器没有参数。

### 15. DbgLocalDebugData

**描述**: Reference to a localDebugData.

该容器没有参数。

### 16. DbgPeriodicDataCollection

**描述**: This container holds the parameters to manage the time base of the debugging module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgDataCollectionTick
  长名称: ''
  描述: Number of OS counter ticks to be used as data collection tick. The OS alarm used for periodic
      collection of DIDs is set with this value.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 17. DbgTimestampConfiguration

**描述**: This container holds the parameters to manage the time stamps of the debugging module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DbgGlobalTimestampActivation
  长名称: ''
  描述: Initial value for timestamp collection.
  默认值: TimestampOff
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DbgTimeStampSize
  长名称: ''
  描述: Memory size used for the time stamps of all DIDs.
  默认值: TimeStampSize_16Bit
  最小值: ''
  最大值: ''
```

