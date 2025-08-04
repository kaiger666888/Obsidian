# StbM

## 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module.

## 容器列表

### 1. StbMDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 2. StbMGeneral

**描述**: This container holds the general parameters of the Synchronized Time-base Manager

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMAbsoluteTimeApi
  长名称: ''
  描述: Enables/Disables the StbM_GetAbsoluteTime API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMDevErrorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMTickTypeRange
  长名称: ''
  描述: Defines the upper range of the type "StbM_TickType".
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: StbMVersionInfo
  长名称: ''
  描述: Activate/Deactivate the version information API (StbM_GetVersionInfo). True: version
      information API activated False: version information API deactivated.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. StbMSynchronizedTimeBase

**描述**: Synchronized time.base collects the information about a specific time-base provider within the
system.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMGlobalTimeProviderCallout
  长名称: ''
  描述: Entry address of the time-base specific callout routine which shall be invoked by the StbM for
      gathering the current time-base value.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMSyncStateProviderCallout
  长名称: ''
  描述: Entry address of the time-base specific callout routine which shall be invoked by the StbM for
      gathering the current time-base status.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMSynchronizedTimeBaseIdentifier
  长名称: ''
  描述: Identification of a synchronized time-base via a unique identifier.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: StbMTickDurationProviderCallout
  长名称: ''
  描述: Entry address of the time-base specific callout routine which shall be invoked by the StbM for
      gathering the current time-base tick duration.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. StbMTriggeredCustomer

**描述**: The triggered customer is directliy triggered by the Synchronized Time-base Manager by getting
synchronized with the current (global) definition of time and passage of time.

#### 参数列表

```yaml
- 
  序号: 1
  名称: StbMGlobalTimeCustomerCallback
  长名称: ''
  描述: Entry address of the customer specific call-back routine which shall be invoked by the StbM
      periodically for time value propagation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: StbMSyncStateCustomerCallback
  长名称: ''
  描述: Entry address of the customer specific call-back routine which shall be invoked by the StbM
      when state changes occur.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: StbMTriggerInSyncState
  长名称: ''
  描述: Activate/Deactivate the triggering of the customer in case the related time-base
      (StbmSynchronizedTimeBaseRef) is not synchronized.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: StbMTriggeredCustomerPeriod
  长名称: ''
  描述: The triggering period of the triggered customer, called by the StbM_MainFunction.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

