# Wdg

## 模块描述

Configuration of the Wdg (Watchdog driver) module.

## 容器列表

### 1. WdgDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 2. WdgGeneral

**描述**: All general parameters of the watchdog driver are collected here.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgDevErrorDetect
  长名称: ''
  描述: Compile switch to enable / disable development error detection for this module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgDisableAllowed
  长名称: ''
  描述: Compile switch to allow / forbid disabling the watchdog driver during runtime.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgIndex
  长名称: ''
  描述: Represents the watchdog driver's ID so that it can be referenced by the watchdog interface.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: WdgInitialTimeout
  长名称: ''
  描述: The initial timeout (sec) for the trigger condition to be initialized during Init function. It
      shall be not larger than WdgMaxTimeout.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 5
  名称: WdgMaxTimeout
  长名称: ''
  描述: The maximum timeout (sec) to which the watchdog trigger condition can be initialized.
  默认值: ''
  最小值: 0
  最大值: 65.535
- 
  序号: 6
  名称: WdgRunArea
  长名称: ''
  描述: |
    Not used.
    
    Represents the watchdog driver execution area is either from ROM(Flash) or RAM as required with
    the particular microcontroller.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: WdgTriggerLocation
  长名称: ''
  描述: Location (memory address) of the watchdog trigger routine.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: WdgVersionInfoApi
  长名称: ''
  描述: Compile switch to enable / disable the version information API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: WdgUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: WdgSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used.
    
    These checks improve robustness as e.g. invalid parameters are checked before function is
    executed. This attribute has to be enabled for safety projects where this component is mapped to
    an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. WdgPublishedInformation

**描述**: Container holding all Wdg specific published information parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgTriggerMode
  长名称: ''
  描述: Watchdog trigger mode (toggle/window/both)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgOffModeSupported
  长名称: ''
  描述: |
    This parameter indicates if WDGIF_OFF_MODE is supported.
    
    True: WDGIF_OFF_MODE is supported.
    False: WDGIF_OFF_MODE is not supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgSlowModeSupported
  长名称: ''
  描述: |
    This parameter indicates if WDGIF_SLOW_MODE is supported.
    
    True: WDGIF_SLOW_MODE is supported.
    False: WDGIF_SLOW_MODE is not supported.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgFastModeSupported
  长名称: ''
  描述: |
    This parameter indicates if WDGIF_FAST_MODE is supported.
    
    True: WDGIF_FAST_MODE is supported.
    False: WDGIF_FAST_MODE is not supported.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. WdgSettingsConfig

**描述**: Configuration items for the different watchdog settings, including those for external watchdog
hardware.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgDefaultMode
  长名称: ''
  描述: Default mode for watchdog driver initialization.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. WdgExternalConfiguration

**描述**: Configuration items for an external watchdog hardware.

Not used.

该容器没有参数。

### 6. WdgSettingsFast

**描述**: Hardware dependent settings for the watchdog driver's "fast" mode.

该容器没有参数。

### 7. WdgSettingsOff

**描述**: Hardware dependent settings for the watchdog driver's "off" mode.

该容器没有参数。

### 8. WdgSettingsSlow

**描述**: Hardware dependent settings for the watchdog driver's "slow" mode.

该容器没有参数。

### 9. WdgGptChannelParameterRef

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgTriggerTimerFreq
  长名称: ''
  描述: Frequency of gpt channel reference WdgTriggerTimer in Hz
  默认值: ''
  最小值: 1
  最大值: ''
- 
  序号: 2
  名称: WdgTickValueMax
  长名称: ''
  描述: Maximum value in ticks, the timer channel is able to count. With the next tick, the timer
      rolls over to zero.
  默认值: ''
  最小值: 1
  最大值: 18446744073709551615
```

### 10. WdgAsr3Compatibility

**描述**: Container to configure ASR3 compatibility

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgTriggerTimeout
  长名称: ''
  描述: The timeout (sec) for the trigger condition to be set everytime when Wdg_Trigger is called.
  默认值: ''
  最小值: 0
  最大值: 65.535
```

