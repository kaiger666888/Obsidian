# Icu

## 模块描述

Configuration of the Icu (Input Capture Unit) module.

## 容器列表

### 1. IcuConfigSet

**描述**: This container is the base for a multiple configuration set

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuMaxChannel
  长名称: ''
  描述: |
    This parameter contains the number of Channels configured. It will be gathered by tools during
    the configuration stage.
                                calculation Formula = Number of configured Icu Channels
    Implementation Type: Icu_ChannelType.
                                This parameter doesn't have any influence on the generated
                                code file
  默认值: 1
  最小值: 0
  最大值: 65535
```

### 2. IcuChannel

**描述**: Configuration of an individual ICU channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuChannelId
  长名称: ''
  描述: Channel Id of the ICU channel. This value will be assigned to the symbolic name derived of the
      IcuChannel container short name.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: IcuDefaultStartEdge
  长名称: ''
  描述: Configures the default-activation-edge which shall be used for this channel if there was no
      activation-edge configured by the call of service Icu_SetActivationCondition().For
      PERIOD signal measurement, the configured edge is the start of period. For DUTY
      measurement, the configured edge is the start of Active time and period. Both Edges can
      not be configured for PERIOD. For DUTY measurement, BOTH EDGES, First edge seen after
      call of Icu_StartSignalMeasurement is considered as the start of measurement. The
      parameter is un-editable for HIGH TIME and LOW TIME measurement. Implementation Type:
      Icu_ActivationType
  默认值: ICU_RISING_EDGE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IcuMeasurementMode
  长名称: ''
  描述: |
    Configures the measurement mode of this channel.
                                 Implementation Type: Icu_MeasurementModeType
  默认值: ICU_MODE_SIGNAL_EDGE_DETECT
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IcuWakeupCapability
  长名称: ''
  描述: |
    Information about the wakeup-capability of this channel.
                              true: Channel is wakeup capable.
                              false: Channel is not wakeup capable.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IcuAssignedHwUnit
  长名称: ''
  描述: |
    The HW resource required for the measurement.
                                       TIM, ERU and CCU
  默认值: GTM
  最小值: ''
  最大值: ''
```

### 3. IcuSignalEdgeDetection

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuSignalEdgeDetection"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuSignalNotification
  长名称: ''
  描述: Notification function for signal notification.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. IcuSignalMeasurement

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuSignalMeasurement"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuSignalMeasurementProperty
  长名称: ''
  描述: |
    Configures the property that could be measured in case the mode is IcuSignalMeasurement.
                                    This property can not be changed during runtime.Implementation
    Type: Icu_SignalMeasurementPropertyType
  默认值: ICU_LOW_TIME
  最小值: ''
  最大值: ''
```

### 5. IcuTimestampMeasurement

**描述**: This container contains the configuration (parameters) in case the measurement mode is
"IcuTimestamp"

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuTimestampMeasurementProperty
  长名称: ''
  描述: Configures the handling of the buffer in case the mode is Timestamp; Implementation Type:
      Icu_TimestampBufferType
  默认值: ICU_LINEAR_BUFFER
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuTimestampNotification
  长名称: ''
  描述: Notification function if the number of requested timestamps (Notification interval is greater
      0) are acquired.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. IcuWakeup

**描述**: This container contains the configuration (parameters) needed to configure a wakeup capable channel

该容器没有参数。

### 7. GtmTimerInputConfiguration

**描述**: This container contains the TIM Configuration for GTM

该容器没有参数。

### 8. TimChannelGeneral

**描述**: This container contains the TIM Channel General Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: TimChannelInputSelect
  长名称: ''
  描述: |
    This decides the Input for the channel
                                        INPUT_OF_CURRENT_TIM_CHANNEL: Input to the current TIM
    Channel will be the input assigned to this channel.
                                        INPUT_OF_PREVIOUS_TIM_CHANNEL: Input to the current TIM
    channel will be the input assigned to the previous channel. Please note, the Port and Pin number
    applicable in this case is
                                        the configuration in TimChannelPortPinSelect for the
    previous channel and not the Port and Pin configured for this channel.
  默认值: INPUT_OF_CURRENT_TIM_CHANNEL
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TimChannelPortPinSelect
  长名称: ''
  描述: This decides the input port and pin of the TIM Channel. This value is applicable for this
      channel only if TimChannelInputSelect is configured as 'INPUT_OF_CURRENT_TIM_CHANNEL'
  默认值: SEL0_NONE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TimChannelClockSelect
  长名称: ''
  描述: This decides the Clock Source for TIM Channel
  默认值: GTM_CONFIGURABLE_CLOCK_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TimChannelGpr0InputSelect
  长名称: ''
  描述: This decides the value captured in GPR0 register of TIM Channel.
  默认值: TIMEBASE_TBU_TS0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TimInterruptMode
  长名称: ''
  描述: This decides the Interrupt mode to use.
  默认值: GTM_INTERRUPT_LEVEL_MODE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OverflowISRThreshold
  长名称: ''
  描述: The threshold denotes the maximum latency between the actual TIM counter overflow interrupt
      and execution flow entering ICU ISR. User must configure the threshold to contain the
      maximum latency and must be lesser than the actual measured time. The threshold will be
      in the ticks of the CMU_CLK selected for that TIM channel.
      The threshold should consider interrupt latency, other high priority interrupts and the
      latency to reach the ICU ISR.                                               The
      threshold is applicable only for Signal measurement, HIGH TIME and LOW TIME.
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 9. TimChannelFilterConfig

**描述**: This holds the filter specific configurations for the channels.

#### 参数列表

```yaml
- 
  序号: 1
  名称: TimChannelFilterEnable
  长名称: ''
  描述: Enables Filter for the Channel. This sets FLT_EN for the channel
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: TimChFilterCounterFreqSelect
  长名称: ''
  描述: This decides the Filter Counter frequency for the TIM Channel. This modifies the FLT_CNT_FRQ
      for the channel
  默认值: GTM_CONFIGURABLE_CLOCK_0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: TimChFilterModeForRisingEdge
  长名称: ''
  描述: This decides the Filter Mode for Rising Edge of the TIM Channel Input
  默认值: IMMEDIATE_EDGE_PROPAGATION_MODE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: TimChFilterModeForFallingEdge
  长名称: ''
  描述: This decides the Filter Mode for Falling Edge of the TIM Channel Input
  默认值: IMMEDIATE_EDGE_PROPAGATION_MODE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: TimChFilterTimeForRisingEdge
  长名称: ''
  描述: This parameter specifies the Filter Time for Rising Edge of the TIM Channel Input
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 6
  名称: TimChFilterTimeForFallingEdge
  长名称: ''
  描述: This parameter specifies the Filter Time for Falling Edge of the TIM Channel Input
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 10. CCU6CC6Configuration

**描述**: This container contains the TIM Configuration for GTM

#### 参数列表

```yaml
- 
  序号: 1
  名称: Cc6xChannel
  长名称: ''
  描述: Cc6 channel selection from the selected kernel
  默认值: Cc60
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: CCChannelInputSelection
  长名称: ''
  描述: Input Selection for CCx channel.
  默认值: CCINA_PORT2_PIN0
  最小值: ''
  最大值: ''
```

### 11. CCU6xParameters

**描述**: This holds the filter specific configurations for the channels.

#### 参数列表

```yaml
- 
  序号: 1
  名称: T12ClkSelection
  长名称: ''
  描述: |
    T12 configuration - clock selection
                                        if T12PrescalerEnabled -false
                                        ft12 = fcc6 divided by (2 power T12ClkSelection)
                                        if T12PrescalerEnabled -true
                                        ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: T12PrescalerEnabled
  长名称: ''
  描述: |
    if T12PrescalerEnabled -false
                                        ft12 = fcc6 divided by (2 power T12ClkSelection)
                                        if T12PrescalerEnabled -true
                                        ft12 = fcc6 divided by (2 power (T12ClkSelection + 8) )
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CCU6InterruptNode
  长名称: ''
  描述: Interrupt node to be used for the kernel
  默认值: NODE_SR0
  最小值: ''
  最大值: ''
```

### 12. ERUInputConfiguration

**描述**: This container contains the ERS and OGU Configuration

#### 参数列表

```yaml
- 
  序号: 1
  名称: EruInputPin
  长名称: ''
  描述: Eru Input selection for the ERU unit
  默认值: ERU_INPUT0A_PORT15_PIN4
  最小值: ''
  最大值: ''
```

### 13. GPT12Configuration

**描述**: This container contains the GPT12 Configuration for GPT12

#### 参数列表

```yaml
- 
  序号: 1
  名称: GPT12InputPortSelection
  长名称: ''
  描述: GPT12 Input selection for the GPT12 unit
  默认值: GPT12_T2INA_PORT00_PIN7
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: GPT12DirPortSelection
  长名称: ''
  描述: GPT12 Direction Input selection for the GPT12 unit
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: GPT12CounterType
  长名称: ''
  描述: GPT12 Counting mechanism
  默认值: ICU_1_COUNT_INPUT
  最小值: ''
  最大值: ''
```

### 14. IcuGeneral

**描述**: Configuration of general ICU parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection on or off. true: Enabled. false: Disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuMultiCoreErrorDetect
  长名称: ''
  描述: Switches the MultiCore Development Error Detection on or off. true: Enabled. false: Disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IcuIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IcuReportWakeupSource
  长名称: ''
  描述: Switch for enabling Wakeup source reporting. true: Report Wakeup source. false: Do not report
      Wakeup source.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IcuSafetyEnable
  长名称: ''
  描述: Switch for enabling/Disabling IcuSafetyEnable
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IcuRuntimeApiMode
  长名称: ''
  描述: IcuRuntimeApiMode for ICU_MCAL_USER1, ICU_MCAL_SUPERVISOR
  默认值: ICU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IcuInitDeInitApiMode
  长名称: ''
  描述: IcuInitDeInitApiMode for ICU_MCAL_USER1, ICU_MCAL_SUPERVISOR
  默认值: ICU_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
```

### 15. IcuOptionalApis

**描述**: This container contains all configuration switches for configuring optional API services of the ICU
driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IcuDeInitApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_DeInit() from the code.
                            true: Icu_17_TimerIp_DeInit() can be used.
                            false: Icu_17_TimerIp_DeInit() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IcuInitCheckApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_InitCheck() from the code.
                            true: Icu_17_TimerIp_InitCheck() can be used.
                            false: Icu_17_TimerIp_InitCheck() can not be used.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IcuDisableWakeupApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_DisableWakeup() from the code.
                            true: Icu_17_TimerIp_DisableWakeup() can be used.
                            false: Icu_17_TimerIp_DisableWakeup() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IcuEdgeCountApi
  长名称: ''
  描述: |
    Adds / removes all services related to the edge counting functionality as listed below, from the
    code: Icu_17_TimerIp_ResetEdgeCount(), Icu_17_TimerIp_EnableEdgeCount(),
    Icu_17_TimerIp_DisableEdgeCount(), Icu_17_TimerIp_GetEdgeNumbers().
                        true: The services listed above can be used.
                        false: The services listed above can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IcuEdgeDetectApi
  长名称: ''
  描述: |
    Adds / removes all services related to the edge detection functionality as listed below from the
    code: Icu_17_TimerIp_EnableEdgeDetection(),Icu_17_TimerIp_DisableEdgeDetection().
                        true: The services listed above can be used.
                        false: The services listed above can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IcuEnableWakeupApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_EnableWakeup() from the code.
                            true: Icu_17_TimerIp_EnableWakeup() can be used.
                            false: Icu_17_TimerIp_EnableWakeup() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IcuGetDutyCycleValuesApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_GetDutyCycleValues() from the code.
                        true: Icu_17_TimerIp_GetDutyCycleValues() can be used.
                        false: Icu_17_TimerIp_GetDutyCycleValues() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IcuGetInputStateApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_GetInputState() from the code.
                        true: Icu_17_TimerIp_GetInputState() can be used.
                        false: Icu_17_TimerIp_GetInputState() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IcuGetTimeElapsedApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_GetTimeElapsed() from the code.
                        true: Icu_17_TimerIp_GetTimeElapsed() can be used.
                        false: Icu_17_TimerIp_GetTimeElapsed() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IcuGetVersionInfoApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_GetVersionInfo() from the code.
                        true: Icu_17_TimerIp_GetVersionInfo() can be used.
                        false: Icu_17_TimerIp_GetVersionInfo() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IcuSetModeApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_SetMode() from the code.
                        true: Icu_17_TimerIp_SetMode() can be used.
                        false: Icu_17_TimerIp_SetMode() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IcuSignalMeasurementApi
  长名称: ''
  描述: |
    Adds / removes the services Icu_17_TimerIp_StartSignalMeasurement() and
    Icu_17_TimerIp_StopSignalMeasurement() from the code.
                        true: Icu_17_TimerIp_StartSignalMeasurement() and
    Icu_17_TimerIp_StopSignalMeasurement() can be used.
                        false: Icu_17_TimerIp_StartSignalMeasurement() and
    Icu_17_TimerIp_StopSignalMeasurement() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IcuTimestampApi
  长名称: ''
  描述: |
    Adds / removes all services related to the timestamping functionality as listed below from the
    code: Icu_17_TimerIp_StartTimestamp(), Icu_17_TimerIp_StopTimestamp(),
    Icu_17_TimerIp_GetTimestampIndex().
                        true: The services listed above can be used.
                        false: The services listed above can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IcuWakeupFunctionalityApi
  长名称: ''
  描述: |
    Adds / removes the service Icu_17_TimerIp_CheckWakeup() from the code.
                        true: Icu_17_TimerIp_CheckWakeup() can be used.
                        false: Icu_17_TimerIp_CheckWakeup() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IcuIncrementalInterfaceApi
  长名称: ''
  描述: |
    Adds / removes the services related to incremental interface mode from the code.
                        true: Incremental Interface mode API can be used.
                        false: Incremental Interface mode API can not be used.
  默认值: false
  最小值: ''
  最大值: ''
```

### 16. CommonPublishedInformation

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
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 122
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
  名称: VendorApiInfix
  长名称: ''
  描述: |
    In driver modules which can be instantiated several times on a single ECU, BSW00347 requires
    that the name of APIs is extended by the VendorId and a vendor specific name.
                  This parameter is used to specify the vendor specific name. In total, the
    implementation specific name is generated as follows:
                  <ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>.
    
                  E.g.  assuming that the VendorId of the implementor is 123 and the implementer
    chose a VendorApiInfix of "v11r456" a api name Can_Write defined in the SWS will translate to
    Can_123_v11r456Write.
    
                  This parameter is mandatory for all modules with upper multiplicity > 1. It shall
    not be used for modules with upper multiplicity =1.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Release
  长名称: ''
  描述: Aurix derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

