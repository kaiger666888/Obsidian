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
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: GptChannelMode
  长名称: ''
  描述: Specifies the behaviour of the timer channel after the target time is reached.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GptChannelTickFrequency
  长名称: ''
  描述: Specifies the tick frequency of the timer channel in Hz.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 4
  名称: GptChannelTickValueMax
  长名称: ''
  描述: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer
      rolls over to zero.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 5
  名称: GptEnableWakeup
  长名称: ''
  描述: Enables wakeup capability of MCU for a channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GptNotification
  长名称: ''
  描述: Function pointer to callback function (for non-wakeup notification)
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. GptWakeupConfiguration

**描述**: Function pointer to callback function (for non-wakeup notification).

该容器没有参数。

### 4. GptConfigurationOfOptApiServices

**描述**: This container contains all configuration switches for configuring optional API services of the GPT
driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GptDeinitApi
  长名称: ''
  描述: Adds / removes the service Gpt_DeInit() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GptEnableDisableNotificationApi
  长名称: ''
  描述: Adds / removes the services Gpt_EnableNotification() and Gpt_DisableNotification from the
      code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GptTimeElapsedApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetTimeElapsed() from the code
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: GptTimeRemainingApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetTimeRemaining() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: GptVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Gpt_GetVersionInfo() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: GptWakeupFunctionalityApi
  长名称: ''
  描述: Adds / removes the services Gpt_SetMode(), Gpt_EnableWakeup() Gpt_DisableWakeup() and
      Gpt_CheckWakeup() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. GptDriverConfiguration

**描述**: This container contains the module-wide configuration (parameters) of the GPT Driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: GptDevErrorDetect
  长名称: ''
  描述: Enables/Disables development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GptReportWakeupSource
  长名称: ''
  描述: Enables/Disables wakeup source reporting.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. GptClockReferencePoint

**描述**: This container contains a parameter, which represents a reference to a container of the type
McuClockReferencePoint (defined in module MCU).

该容器没有参数。

