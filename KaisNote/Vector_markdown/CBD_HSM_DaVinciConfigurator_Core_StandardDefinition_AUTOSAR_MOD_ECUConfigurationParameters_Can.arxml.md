# Can

## 模块描述

This container holds the configuration of a single CAN Driver.

## 容器列表

### 1. CanConfigSet

**描述**: This is the multiple configuration set container for CAN Driver

该容器没有参数。

### 2. CanController

**描述**: This container contains the configuration parameters of the CAN controller(s).

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanBusoffProcessing
  长名称: ''
  描述: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanControllerActivation
  长名称: ''
  描述: Defines if a CAN controller is used in the configuration.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanControllerBaseAddress
  长名称: ''
  描述: Specifies the CAN controller base address.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: CanControllerId
  长名称: ''
  描述: This parameter provides the controller ID which is unique in a given CAN Driver. The value for
      this parameter starts with 0 and continue without any gaps.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: CanRxProcessing
  长名称: ''
  描述: Enables / disables API Can_MainFunction_Read() for handling PDU reception events in polling
      mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanTxProcessing
  长名称: ''
  描述: Enables / disables API Can_MainFunction_Write() for handling PDU transmission events in
      polling mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanWakeupProcessing
  长名称: ''
  描述: Enables / disables API Can_MainFunction_Wakeup() for handling wakeup events in polling mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: CanWakeupSupport
  长名称: ''
  描述: CAN driver support for wakeup over CAN Bus.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. CanControllerBaudrateConfig

**描述**: This container contains bit timing related configuration parameters of the CAN controller(s).

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanControllerBaudRate
  长名称: ''
  描述: Specifies the baudrate of the controller in kbps.
  默认值: ''
  最小值: 0
  最大值: 2000
- 
  序号: 2
  名称: CanControllerPropSeg
  长名称: ''
  描述: Specifies propagation delay in time quantas.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: CanControllerSeg1
  长名称: ''
  描述: Specifies phase segment 1 in time quantas.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: CanControllerSeg2
  长名称: ''
  描述: Specifies phase segment 2 in time quantas.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: CanControllerSyncJumpWidth
  长名称: ''
  描述: Specifies the synchronization jump width for the controller in time quantas.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 4. CanFilterMask

**描述**: This container contains the configuration (parameters) of the CAN Filter Mask(s).

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanFilterMaskValue
  长名称: ''
  描述: Describes a mask for hardware-based filtering of CAN identifiers. The CAN identifiers of
      incoming messages are masked with the appropriate CanFilterMaskValue. Bits holding a 0
      mean don't care, i.e. do not compare the message's identifier in the respective bit
      position.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 5. CanTTController

**描述**: This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTTControllerApplWatchdogLimit
  长名称: ''
  描述: Defines the maximum time period (unit is 256 times NTU) after which the application has to
      serve the watchdog.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: CanTTControllerCycleCountMax
  长名称: ''
  描述: Defines the value for cycle_count_max.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 3
  名称: CanTTControllerExpectedTxTrigger
  长名称: ''
  描述: Number of expected_tx_trigger.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: CanTTControllerExternalClockSynchronisation
  长名称: ''
  描述: Enables/disables the external clock synchronization.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanTTControllerGlobalTimeFiltering
  长名称: ''
  描述: Enables/disables the global time filtering.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: CanTTControllerInitialRefOffset
  长名称: ''
  描述: Defines the initial value for ref trigger offset.
  默认值: ''
  最小值: 0
  最大值: 127
- 
  序号: 7
  名称: CanTTControllerInterruptEnable
  长名称: ''
  描述: Enables/disables the respective interrupts.
  默认值: ''
  最小值: 0
  最大值: 1023
- 
  序号: 8
  名称: CanTTControllerLevel2
  长名称: ''
  描述: Defines whether Level 2 or Level 1 is used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: CanTTControllerNTUConfig
  长名称: ''
  描述: Defines the config value for NTU (network time unit).
  默认值: ''
  最小值: 0
  最大值: 100
- 
  序号: 10
  名称: CanTTControllerOperationMode
  长名称: ''
  描述: Defines the operation mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CanTTControllerSyncDeviation
  长名称: ''
  描述: Defines the maximum synchronization deviation:
  默认值: ''
  最小值: 0
  最大值: 100
- 
  序号: 12
  名称: CanTTControllerTURRestore
  长名称: ''
  描述: Enables/disables the TUR restore.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: CanTTControllerTimeMaster
  长名称: ''
  描述: Defines whether the controller acts as a potential time master.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: CanTTControllerTimeMasterPriority
  长名称: ''
  描述: Defines the time master priority.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 15
  名称: CanTTControllerTxEnableWindowLength
  长名称: ''
  描述: Length of the tx enable window given in CAN bit times.
  默认值: ''
  最小值: 1
  最大值: 16
- 
  序号: 16
  名称: CanTTControllerWatchTriggerGapTimeMark
  长名称: ''
  描述: watch trigger time mark after a gap
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 17
  名称: CanTTControllerWatchTriggerTimeMark
  长名称: ''
  描述: watch trigger time mark
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 18
  名称: CanTTIRQProcessing
  长名称: ''
  描述: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. CanHardwareObject

**描述**: This container contains the configuration (parameters) of CAN Hardware Objects.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanHandleType
  长名称: ''
  描述: Specifies the type (Full-CAN or Basic-CAN) of a hardware object.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanIdType
  长名称: ''
  描述: Specifies whether the IdValue is of type
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanIdValue
  长名称: ''
  描述: Specifies (together with the filter mask) the identifiers range that passes the hardware
      filter.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: CanObjectId
  长名称: ''
  描述: Holds the handle ID of HRH or HTH. The value of this parameter is unique in a given CAN
      Driver, and it should start with 0 and continue without any gaps.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 5
  名称: CanObjectType
  长名称: ''
  描述: Specifies if the HardwareObject is used as Transmit or as Receive object
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. CanTTHardwareObjectTrigger

**描述**: This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanTTHardwareObjectBaseCycle
  长名称: ''
  描述: Defines the cycle_offset.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 2
  名称: CanTTHardwareObjectCycleRepetition
  长名称: ''
  描述: Defines the repeat_factor.
  默认值: ''
  最小值: 1
  最大值: 64
- 
  序号: 3
  名称: CanTTHardwareObjectTimeMark
  长名称: ''
  描述: Defines the point in time, when the trigger will be activated.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: CanTTHardwareObjectTriggerId
  长名称: ''
  描述: Sequential number which allows separation of different TTCAN triggers configured for one and
      the same hardware object.
  默认值: ''
  最小值: 0
  最大值: 63
- 
  序号: 5
  名称: CanTTHardwareObjectTriggerType
  长名称: ''
  描述: Defines the type of the trigger associated with the hardware object. This parameter depends on
      plain CAN parameter CAN_OBJECT_TYPE.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. CanGeneral

**描述**: This container contains the parameters related each CAN Driver Unit.

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanChangeBaudrateApi
  长名称: ''
  描述: The support of the Can_ChangeBaudrate API is optional.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CanDevErrorDetection
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CanHardwareCancellation
  长名称: ''
  描述: Specifies if hardware cancellation shall be supported.ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CanIdenticalIdCancellation
  长名称: ''
  描述: Enables/disables cancellation of pending PDUs with identical ID.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: CanIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: CanLPduReceiveCalloutFunction
  长名称: ''
  描述: This parameter defines the existence and the name of a callout function that is called after a
      successful
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: CanMainFunctionBusoffPeriod
  长名称: ''
  描述: This parameter describes the period for cyclic call to Can_MainFunction_Busoff. Unit is
      seconds.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 8
  名称: CanMainFunctionModePeriod
  长名称: ''
  描述: This parameter describes the period for cyclic call to Can_MainFunction_Mode. Unit is seconds.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 9
  名称: CanMainFunctionWakeupPeriod
  长名称: ''
  描述: This parameter describes the period for cyclic call to Can_MainFunction_Wakeup. Unit is
      seconds.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 10
  名称: CanMultiplexedTransmission
  长名称: ''
  描述: Specifies if multiplexed transmission shall be supported.ON or OFF
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: CanTimeoutDuration
  长名称: ''
  描述: Specifies the maximum time for blocking function until a timeout is detected. Unit is seconds.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 12
  名称: CanVersionInfoApi
  长名称: ''
  描述: Switches the Can_GetVersionInfo() API ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. CanMainFunctionRWPeriods

#### 参数列表

```yaml
- 
  序号: 1
  名称: CanMainFunctionReadPeriod
  长名称: ''
  描述: This parameter describes the period for cyclic call to Can_MainFunction_Read. Unit is seconds.
      Different poll-cycles will be configurable if more than one CanMainFunctionReadPeriod is
      configured. In this case multiple Can_MainFunction_Read() will be provided by the CAN
      Driver module.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
- 
  序号: 2
  名称: CanMainFunctionWritePeriod
  长名称: ''
  描述: This parameter describes the period for cyclic call to Can_MainFunction_Write. Unit is
      seconds. Different poll-cycles will be configurable if more than one
      CanMainFunctionWritePeriod is configured. In this case multiple Can_MainFunction_Write()
      will be provided by the CAN Driver module.
  默认值: ''
  最小值: 0.001
  最大值: 65.535
```

