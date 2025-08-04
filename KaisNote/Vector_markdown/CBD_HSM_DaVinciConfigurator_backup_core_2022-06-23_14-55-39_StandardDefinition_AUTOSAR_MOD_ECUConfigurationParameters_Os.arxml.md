# Os

## 模块描述

Configuration of the Os (Operating System) module.

## 容器列表

### 1. OsAlarm

**描述**: An OsAlarm may be used to asynchronously inform or activate a specific task. It is possible to start
alarms automatically at system start-up depending on the application mode.

该容器没有参数。

### 2. OsAlarmActivateTask

**描述**: This container specifies the parameters to activate a task.

该容器没有参数。

### 3. OsAlarmCallback

**描述**: This container specifies the parameters to call a callback OS alarm action.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAlarmCallbackName
  长名称: ''
  描述: Name of the function that is called when this alarm callback is triggered.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. OsAlarmIncrementCounter

**描述**: This container specifies the parameters to increment a counter.

该容器没有参数。

### 5. OsAlarmSetEvent

**描述**: This container specifies the parameters to set an event

该容器没有参数。

### 6. OsAlarmAutostart

**描述**: If present this container defines if an alarm is started automatically at system start-up depending
on the application mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAlarmAlarmTime
  长名称: ''
  描述: The relative or absolute tick value when the alarm expires for the first time. Note that for
      an alarm which is RELATIVE the value must be at bigger than 0.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: OsAlarmAutostartType
  长名称: ''
  描述: This specifies the type of autostart for the alarm..
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsAlarmCycleTime
  长名称: ''
  描述: Cycle time of a cyclic alarm in ticks. If the value is 0 than the alarm is not cyclic.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 7. OsAppMode

**描述**: OsAppMode is the object used to define OSEK OS properties for an OSEK OS application mode.

该容器没有参数。

### 8. OsApplication

**描述**: An AUTOSAR OS must be capable of supporting a collection of OS objects (tasks, interrupts, alarms,
hooks etc.) that form a cohesive functional unit. This collection of objects is termed an
OS-Application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTrusted
  长名称: ''
  描述: Parameter to specify if an OS-Application is trusted or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsTrustedApplicationDelayTimingViolationCall
  长名称: ''
  描述: Parameter to specify if a timing violation which occurs within an trusted OS-Application is
      raised immediately of if it is delayed until the current task returns to the calling
      OS-Application (return of CallTrustedFunction)
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsTrustedApplicationWithProtection
  长名称: ''
  描述: Parameter to specify if a trusted OS-Application is executed with memory protection or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 9. OsApplicationHooks

**描述**: Container to structure the OS-Application-specific hooks

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsAppErrorHook
  长名称: ''
  描述: Select the OS-Application error hook.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsAppShutdownHook
  长名称: ''
  描述: Select the OS-Application specific shutdown hook for the OS-Application.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsAppStartupHook
  长名称: ''
  描述: Select the OS-Application specific startup hook for the OS-Application.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. OsApplicationTrustedFunction

**描述**: Container to structure the configuration parameters of trusted functions

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTrustedFunctionName
  长名称: ''
  描述: Trusted function (as part of a trusted OS-Application) available to other OS-Applications.
      This also supersedes the OSEK OIL attribute TRUSTED in APPLICATION because the
      optionality of this parameter is describing that already.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 11. OsCounter

**描述**: Configuration information for the counters that belong to the OsApplication.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsCounterMaxAllowedValue
  长名称: ''
  描述: Maximum possible allowed value of the system counter in ticks.
  默认值: ''
  最小值: 1
  最大值: 18446744073709551615
- 
  序号: 2
  名称: OsCounterMinCycle
  长名称: ''
  描述: The MINCYCLE attribute specifies the minimum allowed number of counter ticks for a cyclic
      alarm linked to the counter.
  默认值: ''
  最小值: 1
  最大值: 18446744073709551615
- 
  序号: 3
  名称: OsCounterTicksPerBase
  长名称: ''
  描述: The TICKSPERBASE attribute specifies the number of ticks required to reach a counterspecific
      unit. The interpretation is implementation-specific.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: OsCounterType
  长名称: ''
  描述: This parameter contains the natural type or unit of the counter.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsSecondsPerTick
  长名称: ''
  描述: Time of one counter tick in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 12. OsDriver

**描述**: This Container contains the information who will drive the counter.

该容器没有参数。

### 13. OsTimeConstant

**描述**: Allows the user to define constants which can be e.g. used to compare time values with timer tick
values.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTimeValue
  长名称: ''
  描述: This parameter contains the value of the constant in seconds.
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 14. OsEvent

**描述**: Representation of OS events in the configuration context. Adopted from the OSEK OIL specification.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsEventMask
  长名称: ''
  描述: If event mask would be set to AUTO in OIL, this parameter should be omitted here.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 15. OsIoc

**描述**: Configuration of the IOC (Inter OS Application Communicator).

该容器没有参数。

### 16. OsIocCommunication

**描述**: Representation of a 1:1 or N:1 or N:M (unqueued only) communication between software parts located
in different OS-Applications that are bound to the same or to different cores.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocBufferLength
  长名称: ''
  描述: This attribute defines the size of the IOC internal queue to be allocated for a queued
      communication.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 17. OsIocDataProperties

**描述**: Data properties of the data to be transferred on the IOC communication channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocDataPropertyIndex
  长名称: ''
  描述: This parameter is used to define in which order the data is send, e.g. whether
      IocSendGroup(A,B) or IocSendGroup(B,A) shall be used.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: OsIocInitValue
  长名称: ''
  描述: Initial Value for the data to be transferred on the IOC communication channel.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 18. OsIocReceiverProperties

**描述**: Representation of receiver properties for one communication. For each OsIocCommunication one (1:1)
or many receivers (N:M) have to be defined.  This container should be instantiated within an
OsIocCommunication.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocFunctionImplementationKind
  长名称: ''
  描述: This parameter is used to select whether this communication is implemented as a macro or as a
      function.
  默认值: DO_NOT_CARE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsIocReceiverPullCB
  长名称: ''
  描述: This attribute defines the name of a callback function that the IOC shall call on the
      receiving core for each data reception.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 19. OsIocSenderProperties

**描述**: Representation of sender properties for one communication. For each OsIocCommunication one (1:1) or
many senders (N:1 or N:M) have to be defined. Multiplicity > 1 (N:1 or N:M communication) is only
allowed for Multiplicity of OsIocDataTypeRef = 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIocFunctionImplementationKind
  长名称: ''
  描述: This parameter is used to select whether this communication is implemented as a macro or as a
      function.
  默认值: DO_NOT_CARE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsIocSenderId
  长名称: ''
  描述: Representation of a sender in a N:1 or N:M communication to distinguish between senders.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 20. OsIsr

**描述**: The OsIsr container represents an OSEK interrupt service routine.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrCategory
  长名称: ''
  描述: This attribute specifies the category of this ISR.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. OsIsrTimingProtection

**描述**: This container contains all parameters which are related to timing protection

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrAllInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the ISR is allowed to lock all interrupts
      (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: OsIsrExecutionBudget
  长名称: ''
  描述: The parameter contains the maximum allowed execution time of the interrupt (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: OsIsrOsInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the ISR is allowed to lock all Category 2
      interrupts (via SuspendOSInterrupts()) (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: OsIsrTimeFrame
  长名称: ''
  描述: This parameter contains the minimum inter-arrival time between successive interrupts (in
      seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 22. OsIsrResourceLock

**描述**: This container contains a list of times the interrupt uses resources.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsIsrResourceLockBudget
  长名称: ''
  描述: This parameter contains the maximum time the interrupt is allowed to hold the given resource
      (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 23. OsOS

**描述**: OS is the object used to define OSEK OS properties for an OSEK application.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsNumberOfCores
  长名称: ''
  描述: Maximum number of cores that are controlled by the OS.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: OsScalabilityClass
  长名称: ''
  描述: A scalability class for each System Object "OS" has to be selected. In order to customize the
      operating system to the needs of the user and to take full advantage of the processor
      features the operating system can be scaled according to the scalability classes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsStackMonitoring
  长名称: ''
  描述: Select stack monitoring of Tasks/Category 2 ISRs
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsStatus
  长名称: ''
  描述: The Status attribute specifies whether a system with standard or extended status has to be
      used. Automatic assignment is not supported for this attribute.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsUseGetServiceId
  长名称: ''
  描述: As defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsUseParameterAccess
  长名称: ''
  描述: As defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OsUseResScheduler
  长名称: ''
  描述: The OsUseResScheduler attribute defines whether the resource RES_SCHEDULER is used within the
      application.
  默认值: true
  最小值: ''
  最大值: ''
```

### 24. OsHooks

**描述**: Container to structure all hooks belonging to the OS

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsErrorHook
  长名称: ''
  描述: Error hook as defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsPostTaskHook
  长名称: ''
  描述: Post-task hook as defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OsPreTaskHook
  长名称: ''
  描述: Pre-task hook as defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OsProtectionHook
  长名称: ''
  描述: Switch to enable/disable the call to the (user supplied) protection hook.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OsShutdownHook
  长名称: ''
  描述: Shutdown hook as defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OsStartupHook
  长名称: ''
  描述: Startup hook as defined by OSEK
  默认值: ''
  最小值: ''
  最大值: ''
```

### 25. OsResource

**描述**: An OsResource object is used to co-ordinate the concurrent access by tasks and ISRs to a shared
resource, e.g. the scheduler, any program sequence, memory or any hardware area.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsResourceProperty
  长名称: ''
  描述: This specifies the type of the resource.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 26. OsScheduleTable

**描述**: An OsScheduleTable addresses the synchronization issue by providing an encapsulation of a statically
defined set of alarms that cannot be modified at runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableDuration
  长名称: ''
  描述: This parameter defines the modulus of the schedule table (in ticks).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: OsScheduleTableRepeating
  长名称: ''
  描述: true: first expiry point on the schedule table shall be processed at final expiry point delay
      ticks after the final expiry point is processed.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 27. OsScheduleTableAutostart

**描述**: This container specifies if and how the schedule table is started on startup of the Operating
System. The options to start a schedule table correspond to the API calls to start schedule tables
during runtime.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableAutostartType
  长名称: ''
  描述: This specifies the type of the autostart for the schedule table.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OsScheduleTableStartValue
  长名称: ''
  描述: Absolute autostart tick value when the schedule table starts. Only used if the
      OsScheduleTableAutostartType is ABSOLUTE.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 28. OsScheduleTableExpiryPoint

**描述**: The point on a Schedule Table at which the OS activates tasks and/or sets events

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTblExpPointOffset
  长名称: ''
  描述: The offset from zero (in ticks) at which the expiry point is to be processed.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 29. OsScheduleTableEventSetting

**描述**: Event that is triggered by that schedule table.

该容器没有参数。

### 30. OsScheduleTableTaskActivation

**描述**: Task that is triggered by that schedule table.

该容器没有参数。

### 31. OsScheduleTblAdjustableExpPoint

**描述**: Adjustable expiry point

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTableMaxLengthen
  长名称: ''
  描述: The maximum positive adjustment that can be made to the expiry point offset (in ticks).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: OsScheduleTableMaxShorten
  长名称: ''
  描述: The maximum negative adjustment that can be made to the expiry point offset (in ticks).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 32. OsScheduleTableSync

**描述**: This container specifies the synchronization parameters of the schedule table.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsScheduleTblExplicitPrecision
  长名称: ''
  描述: This configuration is only valid if the explicit synchronization is used.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: OsScheduleTblSyncStrategy
  长名称: ''
  描述: AUTOSAR OS provides support for synchronization in two ways: explicit and implicit.
  默认值: NONE
  最小值: ''
  最大值: ''
```

### 33. OsSpinlock

**描述**: An OsSpinlock object is used to co-ordinate concurrent access by TASKs/ISR2s on different cores to a
shared resource.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsSpinlockLockMethod
  长名称: ''
  描述: Lock method which is used when a spinlock is taken. Note that it is possible that a user (e.g.
      a Task) might hold more than one spinlock. In this case the last lock taken is forced to
      use at least a lock methode which locks as strong as the current one.
  默认值: LOCK_NOTHING
  最小值: ''
  最大值: ''
```

### 34. OsTask

**描述**: This container represents an OSEK task.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskActivation
  长名称: ''
  描述: This attribute defines the maximum number of queued activation requests for the task. A value
      equal to "1" means that at any time only a single activation is permitted for this task.
      Note that the value must be a natural number starting at 1.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: OsTaskPriority
  长名称: ''
  描述: The priority of a task is defined by the value of this attribute. This value has to be
      understood as a relative value, i.e. the values show only the relative ordering of the
      tasks.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: OsTaskSchedule
  长名称: ''
  描述: The OsTaskSchedule attribute defines the preemptability of the task.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 35. OsTaskAutostart

**描述**: This container determines whether the task is activated during the system start-up procedure or not
for some specific application modes.

该容器没有参数。

### 36. OsTaskTimingProtection

**描述**: This container contains all parameters regarding timing protection of the task.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskAllInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the task is allowed to lock all interrupts
      (via SuspendAllInterrupts() or DisableAllInterrupts()) (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 2
  名称: OsTaskExecutionBudget
  长名称: ''
  描述: This parameter contains the maximum allowed execution time of the task (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: OsTaskOsInterruptLockBudget
  长名称: ''
  描述: This parameter contains the maximum time for which the task is allowed to lock all Category 2
      interrupts (via SuspendOSInterrupts()) (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: OsTaskTimeFrame
  长名称: ''
  描述: The minimum inter-arrival time between activations and/or releases of a task (in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
```

### 37. OsTaskResourceLock

**描述**: This container contains the worst case time between getting and releasing a given resource (in
seconds).

#### 参数列表

```yaml
- 
  序号: 1
  名称: OsTaskResourceLockBudget
  长名称: ''
  描述: This parameter contains the maximum time the task is allowed to lock the resource (in seconds)
  默认值: ''
  最小值: 0
  最大值: Inf
```

