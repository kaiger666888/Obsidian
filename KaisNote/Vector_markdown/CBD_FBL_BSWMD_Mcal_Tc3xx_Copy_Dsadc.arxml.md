# Dsadc

## 模块描述

Configuration of the Dsadc (Delta Sigma Analog Digital Conversion) module.

## 容器列表

### 1. DsadcGeneral

**描述**: This Container contains all the general configuration parameters for the DSADC driver

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcDevErrorDetect
  长名称: ''
  描述: This Parameter Enables/Disables the Development Error Detection and reporting in the Dsadc
      Driver
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcSafetyEnable
  长名称: ''
  描述: ThisParameter determines whether to Enable/Disable the safety check and reporting.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcDeInitApi
  长名称: ''
  描述: This Parameter adds or removes the service Dsadc_DeInit() API from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcInitCheckApi
  长名称: ''
  描述: This Parameter adds or removes the service Dsadc_InitCheck() API from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcVersionInfoApi
  长名称: ''
  描述: This Parameter adds or removes the service Dsadc_GetVersionInfo() API from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcInitDeInitApiMode
  长名称: ''
  描述: This parameter defines the privilege mode in which the Initialization and De-initialization
      APIs would operate.
  默认值: DSADC_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DsadcRuntimeApiMode
  长名称: ''
  描述: This Parameter defines the privilege mode in which the runtime APIs would operate.
  默认值: DSADC_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
```

### 2. CommonPublishedInformation

**描述**: This container contains the published information of the DSADC driver.

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
  描述: Patch version number of AUTOSAR specification on which the appropriate implementation is based
      on.
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
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 255
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

### 3. DsadcDemEventParameterRefs

**描述**: Container list down the production errors supported by the DSADC driver.

该容器没有参数。

### 4. DsadcConfigSet

**描述**: This is the base container that contains Dsadc module related parameters

该容器没有参数。

### 5. DsadcGlobalConfiguration

**描述**: This container contains the parameters to configure DSADC IP global configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcDitheringTrimValue
  长名称: ''
  描述: Defines trimming value for internal dithering function. This trimming value is used for all
      the modulators of DSADC
  默认值: DSADC_DITHERING_MIN_50_MILVLT
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcSleepMode
  长名称: ''
  描述: Parameter defines EDSADC reaction to the Sleep mode requests 
  默认值: SLEEP_ENABLE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcSupplyVoltageLevel
  长名称: ''
  描述: Parameter defines the supply voltage level to be used for DSADC internal operations 
  默认值: VOLTAGESUPPLY_AUTO
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcSyncClockGen
  长名称: ''
  描述: Parameter defines the influence of Analog Phase synchronizer on the clock generated 
  默认值: UNSYNCHRONIZED_MODE
  最小值: ''
  最大值: ''
```

### 6. DsadcCarrierGeneratorConfiguration

**描述**: This container contains the Carrier Generation related Parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcPwmGenerationMode
  长名称: ''
  描述: This parameter defines the mode in which the Carrier Generator signal is generated.
      In case of Bit Reverse generation mode, it increases the frequency spectrum to yield a
      smoother induced sine signal. This is done by distributing the 0 and 1 bits over the 32
      cycles of a PWM period.
  默认值: DSADC_NORMAL_MODE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcCarrierFrequencyClockDiv
  长名称: ''
  描述: This parameter defines the divider factor, which is used to define the frequency of the
      carrier signal generator, which is derived from the selected internal clock source and
      divider factor.
  默认值: DSADC_CG_CLOCKDIVIDER_DIV2
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcCarrierSignalPolarity
  长名称: ''
  描述: This parameter defines the starting polarity of the carrier signal.
  默认值: DSADC_CARR_SIG_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcCarrierSignalType
  长名称: ''
  描述: This parameter determines the carrier signal type to be generated.
  默认值: DSADC_CARR_SIG_STOPPED
  最小值: ''
  最大值: ''
```

### 7. DsadcErsEtlConfig

**描述**: This container configures the parameters for ERU input triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcEruStatusFlagConfig
  长名称: ''
  描述: This parameters defines the condition on which the status flag in ETL block of ERU is set. On
      the inverse of the edge selected, the status flag is cleared.
  默认值: DSADC_ETL_FALLING_EDGE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcEruErsInputPin
  长名称: ''
  描述: This parameter determines the input pin for the selected ERS
  默认值: ERS_0_REQ0A_PORTS_P15_4
  最小值: ''
  最大值: ''
```

### 8. DsadcChannelConfiguration

**描述**: This container contains the channel configuration (parameters) depending on the hardware capability.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcChannelId
  长名称: ''
  描述: Unique number to identify the channel
  默认值: 0
  最小值: 0
  最大值: 5
- 
  序号: 2
  名称: DsadcHwChannelNum
  长名称: ''
  描述: Hardware EDSADC channel number
  默认值: DSADC_CHANNEL_0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcAccessMode
  长名称: ''
  描述: This parameter determines the access mode selection for DSADC Driver. The available access
      mode is depends on parameter DsdcTriggerMode.If the DsadcTriggerMode is configured as
      TRIGGER_MODE_NORMAL then DsadcAccessMode can be any inside the Range. If
      DsadcTriggerMode is Configured as TRIGGER_MODE_WINDOW then DsadcAccessMode can be
      DSADC_SINGLE_READ or DSADC_STRERAM_LINEAR_BUFFER or DSADC_DMA_ACCESS.
  默认值: DSADC_SINGLE_READ
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcTriggerMode
  长名称: ''
  描述: This parameter is used to define the trigger mode. possbile conversion modes are
      DSADC_TRIGGER_MODE_NORMAL and DSADC_TRIGGER_MODE_WINDOW.
      DSADC_TRIGGER_MODE_NORMAL: Conversion starts after calling Dsadc_StartModulation() API.
      DSADC_TRIGGER_MODE_WINDOW: The result values are considered after Hardware trigger
      signal(GTM or ERU) is arrived.
  默认值: DSADC_TRIGGER_MODE_NORMAL
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcTimestampFeature
  长名称: ''
  描述: This Parameter is used to define the timestamp Functionality availability for the DSADC
      Channel.
      DSADC_TIMESTAMP_ENABLED: Enable the Timestamp functionality.
      DSADC_TIMESTAMP_DISABLED: Disable the Timestamp Functionality.
  默认值: DSADC_TIMESTAMP_DISABLED
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcGateActiveLevel
  长名称: ''
  描述: This parameter is used to define the active level for the trigger gate signal.
  默认值: DSADC_GATE_HIGH_LEVEL
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DsadcBufferFullNotification
  长名称: ''
  描述: Callback function for buffer full event. The availablity of this parameter depends on
      DsadcAccessMode. If the DsadcAccessMode is configured as ACCESS_MODE_SINGLE OR
      ACCESS_MODE_CIRCULAR_BUFFER or DSADC_DMA_ACCESS then this parameter is not available.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DsadcNewResultNotification
  长名称: ''
  描述: Callback function for new result event.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DsadcWindowCloseNotification
  长名称: ''
  描述: Callback function for window close event, the availability of this parameter depends on
      DsadcTriggerMode configured as DSADC_TRIGGER_MODE_NORMAL
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. DsadcModulatorConfiguration

**描述**: This container contains configuration parameters related to the On-chip modulator, input pin
selection and modulator clock configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcAnalogClockSyncDelay
  长名称: ''
  描述: This parameter defines the delay in clock cycles after the sync signal provided from Phase
      synchronizer.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: DsadcClockDivider
  长名称: ''
  描述: This parameter defines the divider factor, which defines the frequency of the modulator clock,
      which is derived from the peripheral clock
  默认值: DSADC_CLOCKDIVIDER_DIV4
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcDitheringEnable
  长名称: ''
  描述: This parameter defines the availability of internal dithering functionality for the modulator.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcInputGain
  长名称: ''
  描述: This parameter defines multiplication Gain factor for the analog input signal. 
  默认值: DSADC_INPUT_GAIN_FACTOR_1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcInputMuxActionMode
  长名称: ''
  描述: This parameter defines the control mechanism for input multiplexer. It defines the action to
      be taken for the input multiplexer upon a trigger event for pin selection.
  默认值: DSADC_INPUTMUX_PRESET_MODE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcInputMuxControlMode
  长名称: ''
  描述: This parameter defines the condition for a trigger event to control the input multiplexer. 
  默认值: DSADC_INMUX_SOFTWARE_CONTROL
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DsadcInputPinSelection
  长名称: ''
  描述: This parameter defines the initial/permanent setting for the input multiplexer, based on the
      operating mode selected.
  默认值: INPUT_PIN_0_AN2_AN3
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DsadcIntegratorResetEnable
  长名称: ''
  描述: This parameter defines the modulator overload handling. 
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DsadcNegativeInputLine
  长名称: ''
  描述: This parameter defines the modulator internal connection of the negative input. 
  默认值: DSADC_NEG_INPUT_PIN
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DsadcPositiveInputLine
  长名称: ''
  描述: This parameter defines the modulator internal connection of the positive input. 
  默认值: DSADC_POS_INPUT_PIN
  最小值: ''
  最大值: ''
```

### 10. DsadcDemodulatorConfiguration

**描述**: This container contains configuration parameters related to the de-modulator, input data stream and
trigger selection.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcIntegratorTriggerMode
  长名称: ''
  描述: This parameter defines the Integrator trigger mode. 
  默认值: DSADC_INTR_BYPASSED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcResultDisplayMode
  长名称: ''
  描述: This parameter defines the ranges of the result values i.e. result display modes. 
  默认值: DSADC_RES_SIGNED_MODE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcTriggerSelect
  长名称: ''
  描述: This parameter defines EDSADC channel trigger source. 
  默认值: TRIGGER_0_NO_DSADC_TRIG
  最小值: ''
  最大值: ''
```

### 11. DsadcOguConfig

**描述**: This container configures the parameters for ERU triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcEruErsCh0PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 0 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcEruErsCh1PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 1 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcEruErsCh2PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 2 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcEruErsCh3PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 3 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcEruErsCh4PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 4 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcEruErsCh5PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 5 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DsadcEruErsCh6PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 6 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DsadcEruErsCh7PatternFlagEnable
  长名称: ''
  描述: This parameter determines the ERU ERS channel 7 is used for pattern detection for the selected
      OGU channel
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. DsadcTimestampConfiguration

**描述**: This container provides configuration parameters regarding the timestamp counter configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcTimestampCounterClockSel
  长名称: ''
  描述: This parameter defines the divider factor, which defines the clock used for Timestamp counter.
  默认值: CLOCKDIVIDER_DIV1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcInputMuxSetCopyEnable
  长名称: ''
  描述: This parameter defines the availability of Analog MUX setting in the timestamp information.
  默认值: false
  最小值: ''
  最大值: ''
```

### 13. DsadcIntegratorConfiguration

**描述**: This container provides configuration parameter related to the Integrator functional block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcDiscardCount
  长名称: ''
  描述: This parameter defines the number of result values to be discarded before the start of the
      integration cycle.
  默认值: 0
  最小值: 0
  最大值: 63
- 
  序号: 2
  名称: DsadcIntegrationCount
  长名称: ''
  描述: This parameter defines the number of result values to be integrated. 
  默认值: 2
  最小值: 2
  最大值: 64
```

### 14. DsadcRectificationConfiguration

**描述**: This container provides configuration parameters of the rectifier block, used for resolver support,
to determine position of the motor.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcRectificationEnable
  长名称: ''
  描述: This parameter controls the action of the rectifier circuit on the input data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcSignSignalSource
  长名称: ''
  描述: This parameter selects the source of the sign signal, which is to be delayed for the purpose
      of rectification.
  默认值: SRC_0_ON_CHIP_CARRIER_GENERATOR
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcSignSignalChannel
  长名称: ''
  描述: This parameter selects the DSADC channel which provides the source of the sign signal, which
      is to be delayed for the purpose of rectification.
  默认值: DSADC_CHANNEL_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcPosSignDelayValue
  长名称: ''
  描述: This parameter determines the value of Sign Delay counter (number of result values), for which
      to generate a positive delayed sign signal.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: DsadcNegSignDelayValue
  长名称: ''
  描述: This parameter determines the value of Sign Delay counter (number of result values), for which
      to generate a negative delayed sign signal.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 15. DsadcCommonModeVoltConfig

**描述**: This container provides configuration parameter related to common mode voltage application to the
inputs of the modulator channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcCommonModeVoltageEnable
  长名称: ''
  描述: This parameter defines the availability of Common Mode voltage to the input pins.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcCommonModeVoltageSelect
  长名称: ''
  描述: This parameter defines the voltage level configured as Common Mode voltage, which can be
      connected to the input pins.
  默认值: DSADC_VCM_VREFX_2
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcComModeVoltPosAEnable
  长名称: ''
  描述: This parameter defines if the positive analog line connected to position A in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcComModeVoltPosBEnable
  长名称: ''
  描述: This parameter defines if the positive analog line connected to position B in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcComModeVoltPosCEnable
  长名称: ''
  描述: This parameter defines if the positive analog line connected to position C in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcComModeVoltPosDEnable
  长名称: ''
  描述: This parameter defines if the positive analog line connected to position D in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: DsadcComModeVoltNegAEnable
  长名称: ''
  描述: This parameter defines if the negative analog line connected to position A in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: DsadcComModeVoltNegBEnable
  长名称: ''
  描述: This parameter defines if the negative analog line connected to position B in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DsadcComModeVoltNegCEnable
  长名称: ''
  描述: This parameter defines if the negative analog line connected to position C in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DsadcComModeVoltNegDEnable
  长名称: ''
  描述: This parameter defines if the negative analog line connected to position D in the MUX needs to
      be connected to the Common Mode Voltage.
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. DsadcFilterConfiguration

**描述**: This container provides configuration parameter related to main filter chain.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcFIR0FilterEnable
  长名称: ''
  描述: This parameter defines the availability of FIR0 filter in the filter chain of the DSADC
      channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcFIR1FilterEnable
  长名称: ''
  描述: This parameter defines the availability of FIR1 filter in the filter chain of the DSADC
      channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcFIR1FilterDecimationEnable
  长名称: ''
  描述: This parameter defines the decimation rate of FIR1 filter.If selected as TRUE, then the filter
      decimates with a ratio 2:1
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcPreFilterEnable
  长名称: ''
  描述: This parameter defines the availability of Prefilter in the filter chain of the DSADC channel 
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: DsadcOvershootCompensationEn
  长名称: ''
  描述: This parameter defines the availability of Overshoot compensation block in the filter chain of
      the DSADC channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: DsadcCICFilterDecimationFactor
  长名称: ''
  描述: This parameter defines the oversampling rate/Decimation factor for the CIC filter. 
  默认值: 4
  最小值: 4
  最大值: 512
- 
  序号: 7
  名称: DsadcCICFilterStartValue
  长名称: ''
  描述: This parameter defines the starting value of decimation counter, when the CIC filter is
      started/restarted.
  默认值: 4
  最小值: 4
  最大值: 512
- 
  序号: 8
  名称: DsadcAlternateServiceReq
  长名称: ''
  描述: This parameter is used to generate alternate service request for any one of the following
      events, comparator event, time stamp event or alternate source.
  默认值: DSADC_ALT_SERVICE_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: DsadcOffsetCompFilterEnable
  长名称: ''
  描述: This parameter indicates availability of an Offset Compensation (IIR) filter (and its various
      operation modes) in Offset Compensation block.
  默认值: DSADC_OFFCOMP_FILTER_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: DsadcOffsetCompValueProtect
  长名称: ''
  描述: This parameter defines the protection of the Offset Compensation register from the calibration
      algorithm.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: DsadcOffsetCompValue
  长名称: ''
  描述: This parameter defines the offset component value to be removed(subtracted) from each result
      from the filter chain.
  默认值: 0
  最小值: -32768
  最大值: 32767
```

### 17. DsadcAuxFilterConfig

**描述**: This configuration container provides parameters related to Dsadc Auxiliary Filter configuration..

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcAuxCicFilterEnable
  长名称: ''
  描述: This parameter defines the availability of Dsadc Auxiliary filter.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcAuxFilterCicDecimationFactor
  长名称: ''
  描述: This parameter defines the over sampling rate/decimation factor for the Auxiliary CIC filter.
  默认值: DSADC_AUXCIC_OSR_16
  最小值: ''
  最大值: ''
```

### 18. DsadcGainCalibConfig

**描述**: This container provides configuration parameters for Gain calibration.

该容器没有参数。

### 19. DsadcGainCorrConfig

**描述**: This container provides configuration parameters for Gain correction.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcCICFilterOutputShiftPos
  长名称: ''
  描述: This parameter defines the position of the CIC output shifter, which is to be used to select
      the valid output bits from the CIC filter.
  默认值: BITS_0_TO_16
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcGainCorrMulFactor
  长名称: ''
  描述: This parameter defines multiplication factor for Gain correction.
  默认值: 1.0000
  最小值: 0.0
  最大值: 1.9999
```

### 20. DsadcCalibAlgoConfig

**描述**: This container provides configuration parmaters for gain calibration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcCalibCICFilterOutputShiftPos
  长名称: ''
  描述: This parameter defines the position of the CIC output shifter, which is to be used to select
      the valid output bits from the CIC filter. This is valid only during execution of the
      calibration algorithm.
  默认值: BITS_0_TO_16
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcCalibGainCorrMulFactor
  长名称: ''
  描述: This parameter defines multiplication factor for Gain correction. This is valid only during
      execution of the calibration algorithm
  默认值: 1.0000
  最小值: 0.0
  最大值: 1.9999
- 
  序号: 3
  名称: DsadcCICDecimationRate
  长名称: ''
  描述: This parameter defines Decimation factor for the CIC filter. This is for only valid during
      execution of the calibration algorithm.
  默认值: DSADC_CIC_DECIMATION_RATE_8
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcGainCalibMulFactor
  长名称: ''
  描述: This parameter defines multiplication factor for Gain calibration. This is valid only during
      execution of the calibration algorithm.
  默认值: 1.0000
  最小值: 0.0
  最大值: 1.9999
- 
  序号: 5
  名称: DsadcCalibAlgoTargetValue
  长名称: ''
  描述: This parameter defines the full scale target value for calibration algorithm 
  默认值: 25000
  最小值: 0
  最大值: 32767
```

### 21. DsadcComparatorConfiguration

**描述**: This container provides configuration parameters for comparator configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcComparatorEventSelect
  长名称: ''
  描述: This parameter defines the comparator mode selected to generate an alarm event (and also a
      service request, if selected auxiliary service request generation).
  默认值: DSADC_RESULT_ALWAYS
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: DsadcLowerBoundaryValue
  长名称: ''
  描述: This parameter defines the lower boundary used for limit checking. 
  默认值: 0
  最小值: -32768
  最大值: 32767
- 
  序号: 3
  名称: DsadcUpperBoundaryValue
  长名称: ''
  描述: This parameter defines the upper boundary used for limit checking. 
  默认值: 0
  最小值: -32768
  最大值: 32767
```

### 22. DsadcOvershootCompenConfig

**描述**: This container configures the parameters for ERU input triggering

#### 参数列表

```yaml
- 
  序号: 1
  名称: DsadcStepDetectionThreshold
  长名称: ''
  描述: This parameter defines the threshold value (magnitude) used for step detection. The threshold
      value is DsadcStepDetctionthreshold ? 32
  默认值: 0
  最小值: 0
  最大值: 2047
- 
  序号: 2
  名称: DsadcStepDetectionMode
  长名称: ''
  描述: This parameter defines the when the slew rate filter has to be activated
  默认值: DSADC_STEP_DETECT_CMP_LAST
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: DsadcSlewRateFilterStrength
  长名称: ''
  描述: This parameter defines the filter strength for the slew rate filter
  默认值: DSADC_MINIMUM_FILTER_EFFECT
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: DsadcSlewRateFilterRunTime
  长名称: ''
  描述: This parameter defines the time constant for the slew rate filter
  默认值: DSADC_SLEWRATE_FILTR_RUNTIME_2
  最小值: ''
  最大值: ''
```

