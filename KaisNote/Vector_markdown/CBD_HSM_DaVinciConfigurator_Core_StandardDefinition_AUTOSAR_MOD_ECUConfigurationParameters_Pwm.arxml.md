# Pwm

## 模块描述

Configuration of Pwm (Pulse Width Modulation) module.

## 容器列表

### 1. PwmChannelConfigSet

**描述**: Multiple Configuration Set Container

该容器没有参数。

### 2. PwmChannel

**描述**: Configuration of an individual PWM channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmChannelClass
  长名称: ''
  描述: Class of PWM Channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmChannelId
  长名称: ''
  描述: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the
      PwmChannel container short name.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: PwmDutycycleDefault
  长名称: ''
  描述: Value of duty cycle used for Initialization
  默认值: ''
  最小值: 0
  最大值: 32768
- 
  序号: 4
  名称: PwmIdleState
  长名称: ''
  描述: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is
      stopped (e.g. call of Pwm_SetOutputToIdle).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PwmNotification
  长名称: ''
  描述: Definition of the Callback function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PwmPeriodDefault
  长名称: ''
  描述: Value of period used for Initialization.(in seconds).
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 7
  名称: PwmPolarity
  长名称: ''
  描述: Defines the starting polarity of each PWM channel.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. PwmConfigurationOfOptApiServices

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmDeInitApi
  长名称: ''
  描述: Adds / removes the service Pwm_DeInit() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmGetOutputState
  长名称: ''
  描述: ''
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PwmSetDutyCycle
  长名称: ''
  描述: ''
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PwmSetOutputToIdle
  长名称: ''
  描述: ''
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PwmSetPeriodAndDuty
  长名称: ''
  描述: ''
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PwmVersionInfoApi
  长名称: ''
  描述: Switch to indicate that the Pwm_ GetVersionInfo is supported
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. PwmGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmDevErorDetect
  长名称: ''
  描述: Switch for enabling the development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmDutycycleUpdatedEndperiod
  长名称: ''
  描述: Switch for enabling the update of the duty cycle parameter at the end of the current period.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PwmIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: PwmNotificationSupported
  长名称: ''
  描述: Switch to indicate that the notifications are supported
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PwmPeriodUpdatedEndperiod
  长名称: ''
  描述: Switch for enabling the update of the period parameter at the end of the current period.
  默认值: ''
  最小值: ''
  最大值: ''
```

