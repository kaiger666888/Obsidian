# FiM

## 模块描述

Configuration of the FiM (Function Inhibition Manager) module.

## 容器列表

### 1. FiMConfigSet

**描述**: This container contains the configuration parameters and sub containers of the FiM module supporting
multiple configuration sets.

该容器没有参数。

### 2. FiMEventSummary

**描述**: The summarized EventId definition record consists of a summarized event ID and a specific EventId.

该容器没有参数。

### 3. FiMFID

**描述**: This container includes symbolic names of all FIDs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FiMFunctionId
  长名称: ''
  描述: The configuration parameter is used as an ID which represents a functionality. FiMFunctionId
      is the unique identifier assigned during FIM configuration.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 4. FiMInhibitionConfiguration

**描述**: This container includes all configuration parameters concerning the relationship between event and
FID.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FiMInhInhibitionMask
  长名称: ''
  描述: The configuration parameter is used to specify the inhibition mask for an event - FID
      relation.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. FiMInhEventId

**描述**: The configuration parameter is used for an existing DEM event and summarized events as well.

该容器没有参数。

### 6. FiMInhChoiceDemRef

该容器没有参数。

### 7. FiMInhChoiceSumRef

该容器没有参数。

### 8. FiMSummaryEventId

**描述**: This container defines the name of a summarized event.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FiMEventSumId
  长名称: ''
  描述: The summarized EventId definition record defines the existence of a summarized event with a
      specific name. This summarized event can be referenced in the EventSummary (as
      FimSummaryEventId) and Inhibition configuration (as FimInhEventId).
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 9. FiMGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: FiMDataFixed
  长名称: ''
  描述: Enable or disable calibration of inhibit relations The scope of the parameter is to meet the
      requirement (FIM008) to have the option to calibrate inhibit data on the one hand side
      and also to provide the option to protect inhibit data for consistency reasons.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FiMDevErrorDetect
  长名称: ''
  描述: This configuration parameter is used to switch on or to switch off the detection of
      development errors during development.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FiMEventUpdateTriggeredByDem
  长名称: ''
  描述: This configuration parameter specifies the way FIM obtains status of EventIds.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FiMMaxEventFidLinks
  长名称: ''
  描述: This configuration parameter specifies the total maximum number of links between EventIds and
      FIDs.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: FiMMaxEventsPerFid
  长名称: ''
  描述: This configuration parameter specifies the maximum number of EventIds that can be linked to a
      single FID.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: FiMMaxFidsPerEvent
  长名称: ''
  描述: This configuration parameter specifies the maximum number of FIDs that can be linked to a
      single event.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 7
  名称: FiMMaxSummaryEvents
  长名称: ''
  描述: This configuration parameter specifies the maximum number of summarized events that can be
      configured.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: FiMMaxSummaryLinks
  长名称: ''
  描述: This configuration parameter specifies the total maximum number of links between EventIds and
      summarized events.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: FiMMaxTotalLinks
  长名称: ''
  描述: This configuration parameter specifies the total maximum number of links between EventIds and
      FIDs plus the number of links between EventIds and summarized events.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 10
  名称: FiMTaskTime
  长名称: ''
  描述: Allow to configure the time for the periodic cyclic task. Please note: This configuration
      value shall be equal to the value in the Basic Software Scheduler configuration of the
      RTE module.
  默认值: ''
  最小值: 0
  最大值: 0.1
- 
  序号: 11
  名称: FiMVersionInfoApi
  长名称: ''
  描述: This configuration parameter is used to switch on or to switch off the API to get the version
      information.
  默认值: ''
  最小值: ''
  最大值: ''
```

