# Adc

## 模块描述

Configuration of the Adc (Analog Digital Conversion) module.

## 容器列表

### 1. AdcConfigSet

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Adc module.

该容器没有参数。

### 2. AdcHwUnit

**描述**: This container contains the Driver configuration (parameters) depending on grouping of channels

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcClockSource
  长名称: ''
  描述: The ADC module specific clock input for the conversion  unit can
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcHwUnitId
  长名称: ''
  描述: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data.
      Enumeration literals are defined vendor specific.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcPrescale
  长名称: ''
  描述: Optional ADC module specific clock prescale factor, if supported by hardware.
  默认值: ''
  最小值: 0
  最大值: 65535
```

### 3. AdcChannel

**描述**: This container contains the channel configuration (parameters) depending on the hardware capability.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcChannelConvTime
  长名称: ''
  描述: Configuration of conversion time, i.e. the time during which the analogue value is converted
      into digital representation, (in clock cycles) for each channel, if supported by
      hardware.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: AdcChannelHighLimit
  长名称: ''
  描述: High limit - used for limit checking.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 3
  名称: AdcChannelId
  长名称: ''
  描述: This parameter defines the assignment of the channel to the physical ADC  hardware channel.
  默认值: ''
  最小值: 0
  最大值: 1024
- 
  序号: 4
  名称: AdcChannelLimitCheck
  长名称: ''
  描述: Enables or disables limit checking for an ADC channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AdcChannelLowLimit
  长名称: ''
  描述: Low limit - used for limit checking.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: AdcChannelRangeSelect
  长名称: ''
  描述: In case of active limit checking: defines which conversion values are taken into account
      related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcChannelRefVoltsrcHigh
  长名称: ''
  描述: Upper reference voltage source for each channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcChannelRefVoltsrcLow
  长名称: ''
  描述: Lower reference voltage source for each channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: AdcChannelResolution
  长名称: ''
  描述: Channel resolution in bits.
  默认值: ''
  最小值: 1
  最大值: 63
- 
  序号: 10
  名称: AdcChannelSampTime
  长名称: ''
  描述: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock
      cycles) for each channel, if supported by hardware.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

### 4. AdcGroup

**描述**: This container contains the Group configuration (parameters).

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcGroupAccessMode
  长名称: ''
  描述: Type of access mode to group conversion results.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcGroupConversionMode
  长名称: ''
  描述: Type of conversion mode supported by the driver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcGroupId
  长名称: ''
  描述: Numeric ID of the group. This parameter is the symbolic name to be used on the API. This
      symbolic name allows accessing Channel Group data. This value will be assigned to the
      symbolic name derived of the AdcGroup container shortName.
  默认值: ''
  最小值: 0
  最大值: 1023
- 
  序号: 4
  名称: AdcGroupPriority
  长名称: ''
  描述: Priority level of the AdcGroup.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: AdcGroupReplacement
  长名称: ''
  描述: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted
      by a group which has a higher priority.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdcGroupTriggSrc
  长名称: ''
  描述: Type of source event that starts a group conversion.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcHwTrigSignal
  长名称: ''
  描述: Configures on which edge of the hardware trigger signal the driver should react, i.e. start
      the conversion (only if supported by the ADC hardware).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcHwTrigTimer
  长名称: ''
  描述: Reload value of the ADC module embedded timer (only if supported by ADC hardware).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 9
  名称: AdcNotification
  长名称: ''
  描述: Callback function for each group
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: AdcStreamingBufferMode
  长名称: ''
  描述: Configure streaming buffer as "linear buffer" (i.e. the ADC Driver stops the conversion as
      soon as the stream buffer is full) or as "ring buffer" (wraps around if the end of the
      stream buffer is reached).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: AdcStreamingNumSamples
  长名称: ''
  描述: Number of ADC values to be acquired per channel in streaming access mode.
  默认值: 1
  最小值: 1
  最大值: 255
```

### 5. AdcGeneral

**描述**: General configuration (parameters) of the ADC Driver software module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcDeInitApi
  长名称: ''
  描述: Adds / removes the service Adc_DeInit() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcEnableLimitCheck
  长名称: ''
  描述: Enables or disables limit checking feature in the ADC driver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AdcEnableQueuing
  长名称: ''
  描述: Determines, if the queuing mechanism is active in case of priority mechanism disabled.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AdcEnableStartStopGroupApi
  长名称: ''
  描述: Adds / removes the services Adc_StartGroupConversion() and Adc_StopGroupConversion() from the
      code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdcGrpNotifCapability
  长名称: ''
  描述: Determines, if the group notification mechanism (the functions to enable and disable the
      notifications) is available at runtime.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcHwTriggerApi
  长名称: ''
  描述: Adds / removes the services Adc_EnableHardwareTrigger() and Adc_DisableHardwareTrigger() from
      the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcLowPowerStatesSupport
  长名称: ''
  描述: Adds / removes all power state management related APIs (ADC_SetPowerState,
      ADC_GetCurrentPowerState, ADC_GetTargetPowerState, ADC_PreparePowerState,
      ADC_Main_PowerTransitionManager), indicating if the HW offers low power state
      management.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: AdcPowerStateAsynchTransitionMode
  长名称: ''
  描述: Enables / disables support of the ADCDriver to the asynchronous power state transition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: AdcPriorityImplementation
  长名称: ''
  描述: Determines whether a priority mechanism is available for prioritization of the conversion
      requests and if available, the type of prioritization mechanism. The selection applies
      for groups with trigger source software and trigger source hardware. Two
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: AdcReadGroupApi
  长名称: ''
  描述: Adds / removes the service Adc_ReadGroup() and from the code.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: AdcResultAlignment
  长名称: ''
  描述: Alignment of ADC raw results in ADC result buffer (left/right alignment).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: AdcVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Adc_GetVersionInfo() from the code.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. AdcPowerStateConfig

**描述**: Each instance of this parameter defines a power state and the callback to be called when this power
state is reached.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcPowerState
  长名称: ''
  描述: Each instance of this parameter describes a different power state supported by the ADC HW. It
      should be defined by the HW supplier and used by the ADCDriver to reference specific HW
      configurations which set the  ADC HW module in the referenced power state.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: AdcPowerStateReadyCbkRef
  长名称: ''
  描述: Each instance of this parameter contains a reference to a power mode callback defined in a CDD
      or IoHwAbs component.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. AdcPublishedInformation

**描述**: Additional published parameters not covered by "Common" Published Information. Note that these
parameters have "PUBLISHED-INFORMATION" configuration class setting, since they are published
information.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcChannelValueSigned
  长名称: ''
  描述: Information whether the result value of the ADC driver has sign information (true) or not
      (false). If the result shall be interpreted as signed value it shall apply to C-language
      rules.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcGroupFirstChannelFixed
  长名称: ''
  描述: Information whether the first channel of an ADC Channel group can be configured (false) or is
      fixed (true) to a value determined by the ADC HW Unit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcMaxChannelResolution
  长名称: ''
  描述: Maximum Channel resolution in bits (does not specify accuracy).
  默认值: ''
  最小值: 1
  最大值: 63
```

