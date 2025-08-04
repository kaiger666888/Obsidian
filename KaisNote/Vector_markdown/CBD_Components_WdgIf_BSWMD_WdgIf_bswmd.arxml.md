# WdgIf

## 模块描述

Watchdog Interface. The interface allows the Watchdog Manager to select the correct Watchdog Driver
- and thus the watchdog device - while retaining the API and functionality or the underlying driver.

#Safety #Supervision
#AUTOSAR

## 容器列表

### 1. WdgIfDevice

**描述**: It contains the information for the selection of a particular Watchdog device in case multiple
Watchdog drivers are connected.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfDeviceIndex
  长名称: ''
  描述: Represents the watchdog Device ID so that it can be referenced by the watchdog manager.
  默认值: 255
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: WdgIfDeviceIncludeFile
  长名称: ''
  描述: |
    This parameter contains the file name of the include file of the referenced watchdog device.
    
    If the information is present in the referenced watchdog driver's description file, this
    parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case
    this field stays empty or another include file is required, please enter the include file
    manually.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgIfDeviceSetMode
  长名称: ''
  描述: |
    This parameter contains the function name of the 'WdgIf_SetMode()'-service of the referenced
    watchdog device.
    
    If the information is present in the referenced watchdog driver's description file, this
    parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case
    this field stays empty or another include file is required, please enter the function name
    manually.
    
    The function to be called has to have a signature equal to the according AUTOSAR 4 API service
    specified in the Watchdog Driver:
    
    void Wdg_SetMode(WdgIf_ModeType Mode)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgIfDeviceSetTriggerCondition
  长名称: ''
  描述: |
    This parameter contains the function name of the 'WdgIf_SetTriggerCondition()'-service of the
    referenced watchdog device.
    
    If the information is present in the referenced watchdog driver's description file, this
    parameter is filled automatically by selecting the device reference 'WdgIfDriverRef'. In case
    this field stays empty or another include file is required, please enter the function name
    manually.
    
    The function to be called has to have a signature equal to the according AUTOSAR 4 API service
    specified in the Watchdog Driver:
    
    void Wdg_SetTriggerCondition(uint16 timeout)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. WdgIfGeneral

**描述**: This container collects all generic watchdog interface parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfDevErrorDetect
  长名称: ''
  描述: |
    Pre-processor switch for enabling the development error reporting.
    
    true: Development error reporting enabled
    false: Development error reporting disabled
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgIfVersionInfoApi
  长名称: ''
  描述: |
    Pre-processor switch to enable / disable the service returning the version information.
    
    true: Version information service enabled
    false: Version information service disabled
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgIfUseStateCombiner
  长名称: ''
  描述: |
    Pre-processor switch for enabling the usage of the State Combiner feature, which is part of the
    WdgIf. If enabled, it allows WdgM instances running on different processor cores to share and
    trigger one watchdog device.
    
    true: WdgIf State Combiner is enabled and must be configured.
    false: WdgIf State Combiner is disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. WdgIfStateCombiner

**描述**: This container describes the optional  feature of the Safe Watchdog Interface - the State Combiner.

该容器没有参数。

### 4. WdgIfStateCombinerGeneral

**描述**: All general parameters of the StateCombiner are collected here.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfStateCombinerUseOsSpinlock
  长名称: ''
  描述: |
    This preprocessor switch enables/disables the usage of OS spinlock mechanism.
    
    Note: If no OS spinlock is used a user-defined spinlock must be implemented - the file
    Appl_Spinlock.h will be inlcuded (instead of Os.h).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgIfStateCombinerSpinlockID
  长名称: ''
  描述: |
    ID of the spinlock used by the StateCombiner for inter-core synchronization.
    
    Note: A direct reference to a configured OSSpinlock can be set within the parameter State
    Combiner OS Spinlock.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: WdgIfStateCombinerStartUpSyncCycles
  长名称: ''
  描述: Number of master cycles during start-up in which the master does not check the slave
      triggering. Used to synchronize master and slave during start-up.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 5. WdgIfStateCombinerMaster

**描述**: Parameters for the State Combiner master device.

该容器没有参数。

### 6. WdgIfStateCombinerSlave

**描述**: Parameters for the State Combiner slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgIfStateCombinerReferenceCycle
  长名称: ''
  描述: This parameter specifies the reference cycle of the master for this slave.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: WdgIfStateCombinerSlaveIncrementsMin
  长名称: ''
  描述: |
    This parameter specifies the minimum allowed number of increments (triggers) for slave instance
    in one master check period.
    
    Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMin is equal to
    WdgIfStateCombinerSlaveIncrementsMax.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: WdgIfStateCombinerSlaveIncrementsMax
  长名称: ''
  描述: |
    This parameter specifies the maximum allowed number of increments (triggers) for slave instance
    in one master check period.
    
    Note: in synchronous mode WdgIfStateCombinerSlaveIncrementsMax is equal to
    WdgIfStateCombinerSlaveIncrementsMin.
  默认值: 0
  最小值: 0
  最大值: 65535
```

