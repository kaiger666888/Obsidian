# Adc

## 模块描述

Configuration of the Adc (Analog Digital Conversion) module.

## 容器列表

### 1. AdcConfigSet

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Adc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcSyncClockDisable
  长名称: ''
  描述: This parameter determines whether the analog clock is generated in synchronized/unsynchronized
      mode. The configuration of the Converter  Control (CONVCTRL) clock is done by the MCU
      driver
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. AdcGlobalInputClass

**描述**: This container defines the Global Input Class for A-D conversion

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcChSampleTime
  长名称: ''
  描述: This parameter defines the number of additional clock cycles to be added to the minimum sample
      phase of 2 sample clock cycles.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: AdcChPreChargeClkCycles
  长名称: ''
  描述: This parameter defines the number of analog input precharge clock cycles for standard
      conversions.
  默认值: ADC_INPUT_PRECHARGE_CYCLES_0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcChConvMode
  长名称: ''
  描述: This parameter defines the noise reduction level for Standard Conversions.
  默认值: ADC_NOISE_REDUCTION_STEPS_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AdcChSESPSEnable
  长名称: ''
  描述: This parameter defines whether Spread Early Sample Point for Standard Conversions is
      enabled/disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. AdcHwUnit

**描述**: This container contains the Driver configuration (parameters) depending on grouping of channels

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcClockSource
  长名称: ''
  描述: The ADC module specific clock input for the ADC. This parameter is not used for AURIX 2G. The
      clock source for the complete EVADC IP can be selected through node Adc/AdcSystemClock
  默认值: ADC_SYSTEM_CLK
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcHwUnitId
  长名称: ''
  描述: Description: Numeric ID of the HW Unit. This symbolic name allows accessing Hw Unit data.
      Enumeration literals are defined vendor specific.
  默认值: HWUNIT_ADC0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcIdlePrechargeEnable
  长名称: ''
  描述: This parameter determines whether precharge of the sampling capacitor is enabled or not.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AdcInputBufferEnable
  长名称: ''
  描述: This parameter determines whether input buffering is enabled or not. If enabled buffering time
      is selected via AIPS(AdcChPreChargeClkCycles).
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AdcPrechargeReference
  长名称: ''
  描述: This parameter determines whether VDDM/VSSM is used for pre-charging or not.
  默认值: ADC_VDD_VSM_USED
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdcReferencePrechargePhases
  长名称: ''
  描述: This parameter determines the precharge clock phases for the reference input.
  默认值: ADC_PRECHARGE_PHASE_1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcCalibrationSampleTime
  长名称: ''
  描述: This parameter determines the calibration sample time.
  默认值: ADC_CAL_TIME_2_TIMES_TADCI
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcPostCalibrationDisable
  长名称: ''
  描述: This parameter determines whether the post calibration is enabled or disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: AdcAnalogClockSyncDelay
  长名称: ''
  描述: This parameter determines analog clock synchronization delay.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 10
  名称: AdcSampleSyncEnable
  长名称: ''
  描述: This parameter determines whether the Adc Sample Time Synchronization is enabled or disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: AdcMSBDoubleClkEnable
  长名称: ''
  描述: This parameter determines the number of clock cycles for MSB conversions.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: AdcRequestSource0ConvMode
  长名称: ''
  描述: This parameter determines conversion start mode for a request source.
  默认值: ADC_WAIT_FOR_START_MODE
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: AdcRequestSource1ConvMode
  长名称: ''
  描述: This parameter determines conversion start mode for a request source.
  默认值: ADC_WAIT_FOR_START_MODE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: AdcRequestSource2ConvMode
  长名称: ''
  描述: This parameter determines conversion start mode for a request source.
  默认值: ADC_WAIT_FOR_START_MODE
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: AdcSyncConvMode
  长名称: ''
  描述: Determines whether the HW groups operates in Stand-Alone or Master/Slave Sync Mode.
  默认值: ADC_STAND_ALONE
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: AdcPrescale
  长名称: ''
  描述: This parameter defines the divider for generating the analog internal clock (fADCDI) from
      fADC.
  默认值: 4
  最小值: 2
  最大值: 32
```

### 4. AdcHwUnitInputClass

**描述**: This container defines the Hw unit input class for A-D conversion

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcChSampleTime
  长名称: ''
  描述: This parameter defines the number of additional clock cycles to be added to the minimum sample
      phase of 2 sample clock cycles.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 2
  名称: AdcChPreChargeClkCycles
  长名称: ''
  描述: This parameter defines the number of analog input precharge clock cycles for standard
      conversions.
  默认值: ADC_INPUT_PRECHARGE_CYCLES_0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcChConvMode
  长名称: ''
  描述: This parameter defines the noise reduction level for Standard Conversions.
  默认值: ADC_NOISE_REDUCTION_STEPS_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AdcChSESPSEnable
  长名称: ''
  描述: This parameter defines whether Spread Early Sample Point for Standard Conversions is
      enabled/disabled.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. AdcChannel

**描述**: This container contains the channel configuration (parameters) depending on the hardware capability.
This value will be assigned to the symbolic name derived of the AdcChannel container short name.
Channel ID 0xFF is considered as invalid

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcChannelConvTime
  长名称: ''
  描述: Configuration of conversion time, i.e. the time during which the analogue value is converted
      into digital representation, (in clock cycles) for each channel, if supported by
      hardware.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 2
  名称: AdcChannelHighLimit
  长名称: ''
  描述: High limit - used for limit checking.
  默认值: 4095
  最小值: 0
  最大值: 4095
- 
  序号: 3
  名称: AdcChannelId
  长名称: ''
  描述: This parameter defines the assignment of the channel to the physical ADC  hardware channel.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 4
  名称: AdcChannelLimitCheck
  长名称: ''
  描述: Enables or disables limit checking for an ADC channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AdcChannelLowLimit
  长名称: ''
  描述: Low limit - used for limit checking.
  默认值: 0
  最小值: 0
  最大值: 4095
- 
  序号: 6
  名称: AdcChannelRangeSelect
  长名称: ''
  描述: In case of active limit checking: defines which conversion values are taken into account
      related to the boarders defined with AdcChannelLowLimit and AdcChannelHighLimit.
  默认值: ADC_RANGE_ALWAYS
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcChannelRefVoltsrcHigh
  长名称: ''
  描述: Upper reference voltage source for each channel.
  默认值: ADC_USES_VREF
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcChannelRefVoltsrcLow
  长名称: ''
  描述: Lower reference voltage source for each channel.
  默认值: ADC_USES_VAGND
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: AdcChannelResolution
  长名称: ''
  描述: Channel resolution in bits.
  默认值: 12
  最小值: 1
  最大值: 63
- 
  序号: 10
  名称: AdcChannelSampTime
  长名称: ''
  描述: Configuration of sampling time, i.e. the time during which the value is sampled, (in clock
      cycles) for each channel, if supported by hardware.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 11
  名称: AdcAnChannelNum
  长名称: ''
  描述: Analog Input Channel Number.There are upto 8 analog inputs for each Primary Kernel and upto 16
      analog inputs for each Secondary Kernel.
  默认值: G0CH0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: AdcInputClassSelection
  长名称: ''
  描述: defines the input class for the analog channel. Input class determines the channel conversion
      properties like sample time and data conversion mode for each channel.
  默认值: ADC_HWUNIT_CLASS_0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: AdcSyncConvChannelEnable
  长名称: ''
  描述: Enables the synchronous conversion for this channel.Conversion of this channel will trigger
      conversion for the same analog channel number on slave HW groups also.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: AdcBWDEnable
  长名称: ''
  描述: Enables or disables the broken wire detection feature for the channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: AdcBWDPrechargeLevel
  长名称: ''
  描述: Parameter determines the VAREF/VAGND pre-charging for the broken wire detection channel.
  默认值: ADC_BWD_PRECH_VAGND
  最小值: ''
  最大值: ''
```

### 6. AdcGroup

**描述**: This container contains the Group configuration (parameters).

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcGroupAccessMode
  长名称: ''
  描述: Type of access mode to group conversion results.
  默认值: ADC_ACCESS_MODE_SINGLE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcGroupConversionMode
  长名称: ''
  描述: Type of conversion mode supported by the driver.
  默认值: ADC_CONV_MODE_ONESHOT
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcGroupId
  长名称: ''
  描述: |
    Numeric Id of the ADC channel group.  This value will be assigned to the symbolic name derived
    of the AdcGroup containers short name. The range of IDs for each ADC Hw Unit:
                                        ADC0: 0 to 31, ADC1: 32 to 63, ADC2: 64 to 95, ADC3: 96 to
    127, ADC4: 128 to 159, ADC5: 160 to 191, ADC6: 192 to 223, ADC7: 224 to 255, ADC8: 256 to 287
                                        ADC9: 288 to 319, ADC10: 320 to 351, ADC11: 352 to 383
                                      Recommendation  : Use AUTO-CALCULATE-VALUE option for all
    nodes AdcGroupId
  默认值: 0
  最小值: 0
  最大值: 383
- 
  序号: 4
  名称: AdcGroupPriority
  长名称: ''
  描述: Priority level of the AdcGroup.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: AdcGroupReplacement
  长名称: ''
  描述: Replacement mechanism, which is used on ADC group level, if a group conversion is interrupted
      by a group which has a higher priority.
  默认值: ADC_GROUP_REPL_ABORT_RESTART
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdcGroupTriggSrc
  长名称: ''
  描述: Type of source event that starts a group conversion.
  默认值: ADC_TRIGG_SRC_SW
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcHwTrigSignal
  长名称: ''
  描述: Configures on which edge of the hardware trigger signal the driver should react, i.e. start
      the conversion (only if supported by the ADC hardware).
  默认值: ADC_HW_TRIG_RISING_EDGE
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcHwTrigTimer
  长名称: ''
  描述: Reload value of the ADC module embedded timer (only if supported by ADC hardware).
  默认值: 0
  最小值: 0
  最大值: 1023
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
  默认值: ADC_STREAM_BUFFER_LINEAR
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
- 
  序号: 12
  名称: AdcHwExtTrigSelect
  长名称: ''
  描述: This parameter configures the HW trigger source for the group.
  默认值: ADC_TRIG_NONE
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: AdcHwExtGateSelect
  长名称: ''
  描述: This parameter configures the HW gating source for the group.
  默认值: ADC_GATE_NONE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: AdcHwGateSignal
  长名称: ''
  描述: This parameter configures the HW gating signal level.
  默认值: ADC_GATE_LVL_HIGH
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: AdcChannel0Alias
  长名称: ''
  描述: This parameter configures the alias channel to be used for Channel 0.
  默认值: 0
  最小值: 0
  最大值: 31
- 
  序号: 16
  名称: AdcChannel1Alias
  长名称: ''
  描述: This parameter configures the alias channel to be used for Channel 1.
  默认值: 1
  最小值: 0
  最大值: 31
- 
  序号: 17
  名称: AdcResRegDefinition
  长名称: ''
  描述: This parameter defines the result register used for storing the result of this particular ADC
      conversion. This value of this parameter should be in descending order for the nodes of
      AdcGroupDefinition.
  默认值: 0
  最小值: 0
  最大值: 15
```

### 7. EruTriggerConfig

**描述**: This container configures the parameters for ERU triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcEruErsInputPin
  长名称: ''
  描述: This parameter determines the input pin for the selected ERS
  默认值: ERS_REQ0A_PORTS_P15_4_SEL0
  最小值: ''
  最大值: ''
```

### 8. EruGatingConfig

**描述**: This container configures the parameters for ERU Gating

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcEruErsInputPin
  长名称: ''
  描述: This parameter determines the input pin for the selected ERS
  默认值: ERS_REQ0A_PORTS_P15_4_SEL0
  最小值: ''
  最大值: ''
```

### 9. GtmTriggerTimerConfig

**描述**: Choose GTM TOM/ATOM channel which will be used by this AdcGroup for TRIGGER. Referred timer channel
in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

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
- 
  序号: 2
  名称: GtmTimerTimePeriod
  长名称: ''
  描述: This parameter is used for selecting the time period of the GTM timer in micro seconds.
  默认值: 20000
  最小值: 0
  最大值: 65536000
- 
  序号: 3
  名称: GtmTimerCM0Ticks
  长名称: ''
  描述: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 10. GtmGatingTimerConfig

**描述**: Choose GTM TOM/ATOM channel which will be used by this AdcGroup for GATING. Referred timer channel
in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_ADC_DRIVER

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
- 
  序号: 2
  名称: GtmTimerTimePeriod
  长名称: ''
  描述: This parameter is used for selecting the time period of the GTM timer in micro seconds.
  默认值: 20000
  最小值: 0
  最大值: 65536000
- 
  序号: 3
  名称: GtmTimerCM0Ticks
  长名称: ''
  描述: This parameter specifies the Period Compare value (CM0) for the TOM/ATOM Channel in ticks.
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 11. AdcDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId symbolic name.

该容器没有参数。

### 12. AdcGeneral

**描述**: General configuration (parameters) of the ADC Driver software module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: AdcDeInitApi
  长名称: ''
  描述: Adds / removes the service Adc_DeInit() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcSafetyEnable
  长名称: ''
  描述: Enable/Disable the Safety check and all associated notifications.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: AdcMultiCoreErrorDetect
  长名称: ''
  描述: Adds / removes the Multicore error detection feature from the code.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: AdcInitCheckApi
  长名称: ''
  描述: Adds / removes the service Adc_InitCheck() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: AdcEnableLimitCheck
  长名称: ''
  描述: Enables or disables limit checking feature in the ADC driver.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: AdcEnableQueuing
  长名称: ''
  描述: Determines, if the queuing mechanism is active in case of priority mechanism disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: AdcEnableStartStopGroupApi
  长名称: ''
  描述: Adds / removes the services Adc_StartGroupConversion() and Adc_StopGroupConversion() from the
      code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: AdcGrpNotifCapability
  长名称: ''
  描述: Determines, if the group notification mechanism (the functions to enable and disable the
      notifications) is available at runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: AdcHwTriggerApi
  长名称: ''
  描述: Adds / removes the services Adc_EnableHardwareTrigger() and Adc_DisableHardwareTrigger() from
      the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: AdcReadGroupApi
  长名称: ''
  描述: Adds / removes the service Adc_ReadGroup() and from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: AdcVersionInfoApi
  长名称: ''
  描述: Adds / removes the service Adc_GetVersionInfo() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: AdcStartupCalibApi
  长名称: ''
  描述: Adds / removes the service Adc_GetStartupCalStatus() and Adc_TriggerStartupCal() from the
      code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: AdcTriggerOneConversionEnable
  长名称: ''
  描述: This parameter enables the execution of one dummy conversion for each configured HW unit,
      before start-up calibration is triggered in the API Adc_TriggerStartupCal(). Refer
      Errata ADC_TC.083
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: AdcSyncConvEnable
  长名称: ''
  描述:  Enables the synchronous conversions across ADC HW groups.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: AdcLowPowerStatesSupport
  长名称: ''
  描述: Adds / removes all power state management related APIs (ADC_SetPowerState,
      ADC_GetCurrentPowerState, ADC_GetTargetPowerState, ADC_PreparePowerState), indicating if
      the HW offers low power state management.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: AdcPowerStateAsynchTransitionMode
  长名称: ''
  描述: Enables / disables support of the ADCDriver to the asynchronous power state transition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: AdcPriorityImplementation
  长名称: ''
  描述: Determines whether a priority mechanism is available for prioritization of the conversion
      requests and if available, the type of prioritization mechanism. The selection applies
      for groups with trigger source software and trigger source hardware. Two
  默认值: ADC_PRIORITY_NONE
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: AdcResultHandlingImplementation
  长名称: ''
  描述: Determines the result handling mode for the ADC driver.ADC_INTERRUPT_MODE_RESULT_HANDLING:
      Conversion results are transferred in the Request Source ISR (AUTOSAR Mode).
      ADC_DMA_MODE_RESULT_HANDLING: Conversion results are transferred using a DMA channel.
      ADC_POLLING_MODE_RESULT_HANDLING: Conversion results are transferred using synchronous
      APIs.
  默认值: ADC_INTERRUPT_MODE_RESULT_HANDLING
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: AdcResultAlignment
  长名称: ''
  描述: Alignment of ADC raw results in ADC result buffer (left/right alignment).
  默认值: ADC_ALIGN_RIGHT
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: AdcMaxChConvTimeCount
  长名称: ''
  描述: On stop of conversion request, the ongoing channel conversion in the A/D converter cannot be
      stopped immediately. Instead the software needs to wait for the channel conversion to
      get over. Inorder to ensure the converter is idle, a wait on coverter status polling is
      required and its maximum wait time is defined by the value entered in the
      AdcMaxChConvTimeCount
  默认值: 6000
  最小值: 0
  最大值: 16962
- 
  序号: 22
  名称: AdcSleepMode
  长名称: ''
  描述: This parameter determines whether, ADC Driver accepts or rejects the sleep mode request from
      SCU.
  默认值: ADC_SLEEP_MODE_ACCEPT
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: AdcSupplyVoltage
  长名称: ''
  描述: This parameter adjusts the analog circuitry to the selected supply voltage.
  默认值: ADC_VOLTAGE_CONTROLLED_BY_SUPPLY
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: AdcRuntimeApiMode
  长名称: ''
  描述: Defines the privilege mode in which the runtime APIs would operate.
  默认值: ADC_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: AdcInitDeInitApiMode
  长名称: ''
  描述: Defines the privilege mode in which the Initialization and De-initialization APIs would
      operate.
  默认值: ADC_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
```

### 13. AdcPowerStateConfig

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
  默认值: 0
  最小值: 0
  最大值: 3
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

### 14. AdcPublishedInformation

**描述**: Additional published parameters not covered by Common Published Information. Note that these
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
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: AdcGroupFirstChannelFixed
  长名称: ''
  描述: Information whether the first channel of an ADC Channel group can be configured (false) or is
      fixed (true) to a value determined by the ADC HW Unit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: AdcMaxChannelResolution
  长名称: ''
  描述: Maximum Channel resolution in bits (does not specify accuracy).
  默认值: 12
  最小值: 1
  最大值: 63
```

### 15. CommonPublishedInformation

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
  默认值: 10
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 40
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 123
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

