# StbM

## 模块描述

The Synchronized Time-Base Manager provides synchronized time bases to its customers, i.e., time
bases, which are synchronized with time bases on other nodes of a distributed system.
#TimeSync
#AUTOSAR #ServiceComponent

## 容器列表

### 1. StbMGeneral

**描述**: This container holds the general parameters of the Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMCustomerHeaderInclude
  长名称: ''
  描述: Defines the header file, which has the declaration of the callback function prototype for the
      notification customer of the reference Time Base.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMGetCurrentTimeExtendedAvailable
  长名称: ''
  描述: This allows to define whether an additional variant of the API GetCurrentTime with a 64 bit
      argument is provided.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: StbMMainFunctionPeriod
  长名称: ''
  描述: Schedule period of the main function StbM_MainFunction.
  默认值: 0.01
  最小值: 0
  最大值: 1
- 
  序号: 5
  名称: StbMTimeRecordingSupport
  长名称: ''
  描述: Enables/Disables the usage of the recording functionality for Synchronized and Offset
      timebases for Global Time precision measurement purpose.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: StbMVersionInfoApi
  长名称: ''
  描述: Activate/Deactivate the version information API (StbM_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: StbMSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: StbMFloat64Support
  长名称: ''
  描述: Selects if the time correction feature shall use 64 bit floating point for time correction
      calculation instead of 64 bit signed integer. If this parameter is unchecked, no
      floating point arithmetic is used within the StbM.
  默认值: true
  最小值: ''
  最大值: ''
```

### 2. StbMSynchronizedTimeBase

**描述**: Synchronized time.base collects the information about a specific time-base provider within the
system.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMAllowMasterRateCorrection
  长名称: ''
  描述: This attribute describes whether the rate correction value of a Time Base can be set by
      StbM_SetRateCorrection():
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMAllowSystemWideGlobalTimeMaster
  长名称: ''
  描述: For postbuild variant of the StbM this parameter has to be set to true for a Global Time
      Master that may act as a system-wide source of time. Otherwise no corresponding service
      ports/interfaces is provided.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMClearTimeleapCount
  长名称: ''
  描述: |
    This attribute describes the required number of updates to the Time Base where the time
    difference to the previous value has to remain below
    StbMTimeLeapPastThreshold/StbMTimeLeapFutureThreshold until the TIMELEAP_PAST/TIMELEAP_FUTURE
    bit within timeBaseStatus of the Time Base is cleared.
    
    Note: This parameter is only relevant for Time Slaves.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: StbMIsSystemWideGlobalTimeMaster
  长名称: ''
  描述: This parameter shall be set to true for a Global Time Master that acts as a system-wide source
      of time information with respect to Global Time.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: StbMMasterRateDeviationMax
  长名称: ''
  描述: |
    This attribute describes the maximum allowed absolute value of the rate deviation value to be
    set by StbM_SetRateCorrection().
    
    Note: This parameter is only relevant for Global Time Masters.
  默认值: 0
  最小值: 0
  最大值: 32000
- 
  序号: 6
  名称: StbMStatusNotificationCallback
  长名称: ''
  描述: Name of the customer specific status notification callback function, which shall be called, if
      a non-masked status event occurs.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: StbMStatusNotificationMask
  长名称: ''
  描述: The parameter defines the initial value for NotificationMask mask, which defines the events
      for which the event notification callback function shall be called.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: StbMStoreTimebaseNonVolatile
  长名称: ''
  描述: This allows for specifying that the Time Base shall be stored in the NvRam.
  默认值: NO_STORAGE
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: StbMSynchronizedTimeBaseIdentifier
  长名称: ''
  描述: Identification of a Synchronized TimeBase via a unique identifier.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 10
  名称: StbMSyncLossTimeout
  长名称: ''
  描述: |
    This attribute describes the timeout for the situation that the time synchronization gets lost
    in the scope of the time domain.
    
    Note: This parameter is only relevant for Time Slaves.
  默认值: 1
  最小值: 0
  最大值: 4294967
- 
  序号: 11
  名称: StbMTimeLeapFutureThreshold
  长名称: ''
  描述: |
    This represents the maximum allowed positive difference between the current Local Time Base
    value and a newly received Global Time Base value.
    A threshold of 0 deactivates the Time Leap check.
    
    Note: This parameter is only relevant for Time Slaves.
  默认值: 1
  最小值: 0
  最大值: 2
- 
  序号: 12
  名称: StbMTimeLeapPastThreshold
  长名称: ''
  描述: |
    This represents the maximum allowed negative difference between the current Local Time Base
    value and a newly received Global Time Base value.
    A threshold of 0 deactivates the Time Leap check.
    
    Note: This parameter is only relevant for Time Slaves.
  默认值: 1
  最小值: 0
  最大值: 2
```

### 3. StbMLocalTimeClock

**描述**: References the hardware reference clock of this Synchronized Time Base.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMClockFrequency
  长名称: ''
  描述: Represents the frequency of the HW reference clock used by the StbM.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: StbMClockPrescaler
  长名称: ''
  描述: Represents the prescaler to calculate the resulting frequency of the HW reference clock used
      by the StbM.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 4. StbMNotificationCustomer

**描述**: This container holds the configuration of a notification customer, which is notified is informed
about the occurance of a Time-base related event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMNotificationCustomerId
  长名称: ''
  描述: Identification of a event notification customer.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: StbMTimeNotificationCallback
  长名称: ''
  描述: Name of the customer specific notification callback function, which shall be called, if the
      time previously set by the customer is reached.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMTimerStartThreshold
  长名称: ''
  描述: This  interval defines, when a GPT Timer shall be started for Time Notification Customers for
      which the corresponding Customer Timer is running.
  默认值: 0.01
  最小值: 0
  最大值: 2
```

### 5. StbMTimeCorrection

**描述**: Collects the information relevant for the rate- and offset correction of a Time Base.

Note: This container is only relevant for Time Slaves.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMOffsetCorrectionAdaptionInterval
  长名称: ''
  描述: Defines the interval during which the adaptive rate correction cancels out the rate- and time
      deviation.
  默认值: 1
  最小值: 0
  最大值: 4
- 
  序号: 2
  名称: StbMOffsetCorrectionJumpThreshold
  长名称: ''
  描述: Threshold for the correction method. Deviations below this value will be corrected by a linear
      reduction over a defined timespan. Values equal- and greater than this value will be
      corrected by immediately setting the correct time- and rate in form of a jump.
  默认值: 1
  最小值: 0
  最大值: 4
- 
  序号: 3
  名称: StbMRateCorrectionMeasurementDuration
  长名称: ''
  描述: Definition of the time span which is used to calculate the rate deviation.
  默认值: 1
  最小值: 0
  最大值: 60
- 
  序号: 4
  名称: StbMRateCorrectionsPerMeasurementDuration
  长名称: ''
  描述: Number of simultaneous rate measurements to determine the current rate deviation.
  默认值: 1
  最小值: 1
  最大值: 65535
```

### 6. StbMTimeRecording

**描述**: Collects the information relevant for configuration of the precision measurement of a Time Base.

Note: This container is only relevant for Time Slaves.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMOffsetTimeRecordBlockCallback
  长名称: ''
  描述: Name of the customer specific callback function, which shall be called, if a measurement data
      for a Offset Time Base is available.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMOffsetTimeRecordTableBlockCount
  长名称: ''
  描述: Represents the number of Blocks used for queueing time measurement events for the Offset Time
      Base Record Table.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: StbMSyncTimeRecordBlockCallback
  长名称: ''
  描述: Name of the customer specific callback function, which shall be called, if a measurement data
      for a Synchronized Time Base is available.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: StbMSyncTimeRecordTableBlockCount
  长名称: ''
  描述: Represents the number of Blocks used for queueing time measurement events for the Synchronized
      Time Base Record Table.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 7. StbMTimeValidation

**描述**: Container with TimeValidation configuration for a TimeBase.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMTimingRecordTableBlockCount
  长名称: ''
  描述: Size of Timing Record Table used for storing TimeValidation timing data.
  默认值: ''
  最小值: 1
  最大值: 65535
```

### 8. StbMTriggeredCustomer

**描述**: The triggered customer is directly triggered by the Synchronized Time-base Manager by getting
synchronized with the current (global) definition of time and passage of time.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMTriggeredCustomerPeriod
  长名称: ''
  描述: The triggering period of the triggered customer, called by the StbM_MainFunction.
  默认值: 10000
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: StbMOSScheduleTableCounterTickDuration
  长名称: ''
  描述: Tick duration of the OS counter, which drives the synchronized OS ScheduleTable, in seconds.
  默认值: ''
  最小值: 1E-09
  最大值: 1E-06
```

