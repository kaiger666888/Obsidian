# FrSM

## 模块描述

Configuration of the FlexRay State Manager

## 容器列表

### 1. FrSMConfig

**描述**: This container comprises the cluster specific configuration of the FlexRay State Manager.

该容器没有参数。

### 2. FrSMCluster

**描述**: This container specifies a FlexRay cluster and all related data. A FlexRay cluster may consist of
more than one controller per ECU.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrSMCheckWakeupReason
  长名称: ''
  描述: If FrSMCheckWakeupReason  is true, the FrSM will check the wakeup reason in order to skip the
      wakeup in case of wakeup by bus. If FrSMCheckWakeupReason  is false, the FrSM will
      always try to perform a wakeup.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrSMDelayStartupWithoutWakeup
  长名称: ''
  描述: If true, timer t1 shall be started instead of immediately calling FrIf_AllowColdstart in case
      of a startup without wakeup.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrSMDurationT1
  长名称: ''
  描述: The duration of timer t1 in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: FrSMDurationT2
  长名称: ''
  描述: The duration of timer t2 in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 5
  名称: FrSMDurationT3
  长名称: ''
  描述: The duration of timer t3 in seconds. The value of this parameter shall be larger than the
      value of FrSMDurationT1 parameter.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: FrSMIsColdstartEcu
  长名称: ''
  描述: True: The ECU is a coldstart node for this FlexRay cluster.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FrSMIsWakeupEcu
  长名称: ''
  描述: True: FrSM shall perform a wakeup for this cluster.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FrSMMainFunctionCycleTime
  长名称: ''
  描述: This parameter defines the cycle time in seconds of the periodic calling of FrSM main
      function.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 9
  名称: FrSMMinNumberOfColdstarter
  长名称: ''
  描述: This parameter defines the number of coldstarter that should not be underrun. If this
      parameter is not configured the mainfunction shall not check the number of startup
      frames.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: FrSMNumWakeupPatterns
  长名称: ''
  描述: Maximum number of Wakeup Patterns the node may send before going to FRSM_STARTUP.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 11
  名称: FrSMStartupRepetitions
  长名称: ''
  描述: The number of times an ECU may repeat the startup procedure for a FlexRay cluster.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 12
  名称: FrSMStartupRepetitionsWithWakeup
  长名称: ''
  描述: The number of times an ECU may repeat the startup procedure including a wakeup for a FlexRay
      cluster.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 3. FrSMClusterDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 4. FrSMGeneral

**描述**: This container contains the general configuration parameters of the FlexRay State Manager.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FrSMDevErrorDetect
  长名称: ''
  描述: Enables and disables the development error detection and
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FrSMSyncLossErrorIndicationName
  长名称: ''
  描述: Name of <Cdd>_SyncLossErrorIndication function that shall be called on loss of
      synchronization. If this parameter is omitted no indication shall take place.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FrSMVersionInfoApi
  长名称: ''
  描述: Enables and disables the version info API
  默认值: false
  最小值: ''
  最大值: ''
```

