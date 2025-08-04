# Gpt

## 模块描述

Configuration of the Gpt (General Purpose Timer) module.

## 容器列表

### 1. GptChannelConfigSet

**描述**: This container is the base of a Configuration Set which contains the configured GPT channels. This
way, different configuration sets can be defined for post-build process.

该容器没有参数。

### 2. GptChannelConfiguration

**描述**: Configuration of an individual GPT channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GptChannelId
  长名称: ''
  描述: Channel Id of the GPT channel. This value will be assigned to the symbolic name derived of the
      GptChannelConfiguration container short name.
  默认值: 0
  最小值: 0
  最大值: 196
- 
  序号: 2
  名称: GptAssignedHwUnit
  长名称: ''
  描述: Specifies the timer hardware used for this Gpt channel.
  默认值: GPT12
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GptChannelMode
  长名称: ''
  描述: Specifies the behavior of the timer channel after the target time is reached.
  默认值: GPT_CH_MODE_CONTINUOUS
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GptTimerChannelUsage
  长名称: ''
  描述: Specifies the grade of enabling the GPT Predef Timers for this channel.
  默认值: GPT_TIMER_CHANNEL_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GptChannelTickFrequency
  长名称: ''
  描述: Specifies the tick frequency of the timer channel in Hz.
  默认值: 1.0
  最小值: 0.0
  最大值: 65535.0
- 
  序号: 6
  名称: GptChannelTickValueMax
  长名称: ''
  描述: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer
      rolls over to zero.
  默认值: 65535
  最小值: 0
  最大值: 16777215
- 
  序号: 7
  名称: GptEnableWakeup
  长名称: ''
  描述: Enables wakeup capability of MCU for a channel.                               Enabled only if
      GptReportWakeupSource is True.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: GptNotification
  长名称: ''
  描述: Function pointer to callback function (for non-wakeup notification)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. GptWakeupConfiguration

**描述**: Function pointer to callback function (for wakeup notification).

该容器没有参数。

### 4. GtmTimerOutputModuleConfiguration

**描述**: Choose GTM TOM/ATOM channel which will be used by this GPT Driver. Referred timer channel in MCU
should have TomChannelUsage/ AtomChannelUsage as USED_BY_GPT_DRIVER

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTimerClockSelect
  长名称: ''
  描述: This parameter decides the Clock Source for TOM/ATOM timer.
  默认值: GTM_FIXED_CLOCK_0
  最小值: ''
  最大值: ''
```

### 5. Gpt12TimerOutputModuleConfiguration

**描述**: Choose GPT12 channel which will be used by this GPT Driver.                                 Referred
timer channel in MCU should have GPT12Timerblock as USED_BY_GPT_DRIVER

#### 参数列表

```yaml
- 
  序号: 1
  名称: Gpt12ChannelClockDivider
  长名称: ''
  描述: This parameter decides the divider value of this timer channel. This value depends on the
      prescalar configured in MCU
  默认值: 0
  最小值: 0
  最大值: 7
```

### 6. GptConfigurationOfOptApiServices

**描述**: This container contains all configuration switches for configuring optional API services of the GPT
driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GptDeinitApi
  长名称: ''
  描述: Adds / removes the service Gpt_DeInit() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GptEnableDisableNotificationApi
  长名称: ''
  描述: Adds / removes the services Gpt_EnableNotification() and Gpt_DisableNotification from the
      code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GptTimeElapsedApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetTimeElapsed() from the code
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GptTimeRemainingApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetTimeRemaining() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GptVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GptWakeupFunctionalityApi
  长名称: ''
  描述: Adds / removes the services Gpt_SetMode(), Gpt_EnableWakeup() Gpt_DisableWakeup() and
      Gpt_CheckWakeup() from the code.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. GptDriverConfiguration

**描述**: This container contains the module-wide configuration (parameters) of the GPT Driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: GptDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GptMultiCoreErrorDetect
  长名称: ''
  描述: Switches the Multicore Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GptReportWakeupSource
  长名称: ''
  描述: Enables/Disables wakeup source reporting.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GptPredefTimer100us32bitEnable
  长名称: ''
  描述: Enables/disables the GPT Predef Timer 100?s32bit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GptPredefTimer1usEnablingGrade
  长名称: ''
  描述: Specifies the grade of enabling the GPT Predef Timers with 1?s tick duration.
  默认值: GPT_PREDEF_TIMER_1US_DISABLED
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GptSafetyEnable
  长名称: ''
  描述: Enable/Disable the Safety check and all associated notifications.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: GptReadAcrossCores
  长名称: ''
  描述: Enable/Disable reading the timer value from all cores.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: GptInitCheckApi
  长名称: ''
  描述: Adds / removes the service Gpt_InitCheck() from the code.
  默认值: false
  最小值: ''
  最大值: ''
```

### 8. GptClockReferencePoint

**描述**: This container contains a parameter, which represents a reference to a container of the type
McuClockReferencePoint (defined in module MCU).

该容器没有参数。

### 9. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArMajorVersion
  长名称: ''
  描述: Major version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ArMinorVersion
  长名称: ''
  描述: Minor version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ArPatchVersion
  长名称: ''
  描述: Patch level version number of AUTOSAR specification on which the appropriate implementation is
      based on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 20
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 100
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: VendorId
  长名称: ''
  描述: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: Aurix2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

