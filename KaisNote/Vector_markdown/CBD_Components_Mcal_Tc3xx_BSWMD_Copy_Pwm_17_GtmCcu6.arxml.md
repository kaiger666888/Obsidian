# Pwm

## 模块描述

Configuration of Pwm (Pulse Width Modulation) module.

## 容器列表

### 1. PwmChannelConfigSet

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Pwm module.

该容器没有参数。

### 2. PwmChannel

**描述**: Configuration of an individual PWM channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmChannelClass
  长名称: ''
  描述: Class of PWM Channel.  ImplementationType: Pwm_17_GtmCcu6_ChannelClassType.
  默认值: PWM_FIXED_PERIOD
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmChannelId
  长名称: ''
  描述: Channel Id of the PWM channel. This value will be assigned to the symbolic name derived of the
      PwmChannel container short name.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: PwmAssignedHwUnit
  长名称: ''
  描述: The HW resource used for PWM Generation.
  默认值: GTM
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PwmDutycycleDefault
  长名称: ''
  描述: |
    Value of duty cycle used for Initialization
                                   Depends on PwmDutyShiftInTicks parameter.
                                   When the PwmDutyShiftInTicks is OFF, the Dutycyle should be
    entered as percentage:
                                   0, represents 0%
                                   0x8000 represents 100%
                                   When the PwmDutyShiftInTicks is ON, the Dutycyle should be
    entered as absolute ticks:
                                   0, represents 0%
                                   Same value as Period value represents 100%
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 5
  名称: PwmIdleState
  长名称: ''
  描述: The parameter PWM_IDLE_STATE represents the output state of the PWM after the signal is
      stopped (e.g. call of Pwm_SetOutputToIdle).
  默认值: PWM_LOW
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PwmNotification
  长名称: ''
  描述: Definition of the Callback function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PwmPeriodDefault
  长名称: ''
  描述: |
    Default Period of the channel. Input Value in absolute ticks.
                                     This parameter does not impact the channels of class
    PWM_FIXED_PERIOD_SHIFTED and PWM_FIXED_PERIOD_CENTER_ALIGNED.
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 8
  名称: PwmPolarity
  长名称: ''
  描述: Defines the starting polarity of each PWM channel.
  默认值: PWM_LOW
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PwmShiftValue
  长名称: ''
  描述: |
    Shift Value for PWM_FIXED_PERIOD_SHIFTED Signal.
                                     Valid only when PwmChannelClass is PWM_FIXED_PERIOD_SHIFTED.
                                     This depends on PwmDutyShiftInTicks parameter.
                                     When the PwmDutyShiftInTicks is OFF, the Shift value should be
    entered as percentage:
                                     0, represents 0%
                                     0x8000 represents 100%
                                     When the PwmDutyShiftInTicks is ON, the Shift value should be
    entered as absolute ticks:
                                     0, represents 0%
                                     Same value as Period value represents 100%
  默认值: 0
  最小值: 0
  最大值: 16777215
- 
  序号: 10
  名称: PwmCoherentUpdate
  长名称: ''
  描述: Setting this parameter to true determines channel is coherent or not.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. GtmTimerOutputModuleConfiguration

**描述**: Choose GTM TOM/ATOM channel which will be used by this PWM Channel.
Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_PWM_DRIVER

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

### 4. CCU6CC6Configuration

**描述**: Choose CCU6 T12/T13 channel which will be used by this PWM Channel.
Referred timer channel in MCU should have CCU6ChannelUsage as USED_BY_PWM_DRIVER

#### 参数列表

```yaml
- 
  序号: 1
  名称: CCU6TimerUsed
  长名称: ''
  描述: Selects Timer T12/T13.                                                       Note: Kernel
      selection is done in parameter CCU6KernelUsed.
  默认值: T12
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Cc6xChannel
  长名称: ''
  描述: Cc6 channel selection from the selected kernel
  默认值: Cc60
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: CCU6TimerClockSelect
  长名称: ''
  描述: This parameter decides the Clock Source for T12/T13 timer.
  默认值: CCU6_CONFIGURABLE_CLOCK_0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: CCU6TimerPrescalarEnabled
  长名称: ''
  描述: if CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power
      CCU6TimerClockSelect)                                          if
      CCU6TimerPrescalarEnabled is false then T12/T13 Clock = fcc6 divided by (2 power
      (CCU6TimerClockSelect+8) )
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. PwmConfigurationOfOptApiServices

**描述**: This container has global switches of PWM APIs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmDeInitApi
  长名称: ''
  描述: Adds / removes the service Pwm_DeInit() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmGetOutputState
  长名称: ''
  描述: Adds / removes the service Pwm_GetOutputState() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PwmSetDutyCycle
  长名称: ''
  描述: Adds / removes the service Pwm_SetDutyCycle() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PwmSetOutputToIdle
  长名称: ''
  描述: Adds / removes the service Pwm_SetOutputToIdle() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PwmSetPeriodAndDuty
  长名称: ''
  描述: Adds / removes the service Pwm_SetPeriodAndDuty() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PwmVersionInfoApi
  长名称: ''
  描述: Switch to indicate that the Pwm_ GetVersionInfo is supported
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. PwmGeneral

**描述**: General settings for the PWM driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PwmMultiCoreErrorDetect
  长名称: ''
  描述: Switches the Multicore error detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PwmDutycycleUpdatedEndperiod
  长名称: ''
  描述: Switch for enabling the update of the duty cycle parameter at the end of the current period.
      PWM_VARIABLE_PERIOD channel class will not get affected with this parameter setting.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PwmIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: PwmLowPowerStatesSupport
  长名称: ''
  描述: Adds / removes all power state management related APIs (PWM_SetPowerState,
      PWM_GetCurrentPowerState, PWM_GetTargetPowerState, PWM_PreparePowerState,
      PWM_Main_PowerTransitionManager), indicating if the HW offers low power state
      management.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PwmNotificationSupported
  长名称: ''
  描述: Switch to indicate that the notifications are supported
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PwmPeriodUpdatedEndperiod
  长名称: ''
  描述: Switch for enabling the update of the period parameter at the end of the current period.
      PWM_FIXED_PERIOD, PWM_FIXED_PERIOD_SHIFTED and PWM_FIXED_PERIOD_CENTER_ALIGNED channel
      class will not get affected with this parameter setting.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PwmChannelCoherentSelection
  长名称: ''
  描述: |
    Switch for enabling the update of the period / duty parameter at the end of the current period
                                 channel wise. Switching on this parameter obsoletes
    PwmDutycycleUpdatedEndperiod and
                                 PwmPeriodUpdatedEndperiod.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PwmHandleShiftByOffset
  长名称: ''
  描述: Switch for enabling Speacial handling for shifted channels.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: PwmDutyShiftInTicks
  长名称: ''
  描述: |
    Switch for Pwm Duty Cycle type:
                                 Disabled - Duty Cycle and Shift value in percentage.
                                 Enabled - Duty Cycle and Shift value in timer ticks.
                                 User has to take care of entering the right values for
    PwmDutycycleDefault and PwmShiftValue based on this selection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: PwmEnable0Or100DutyNotification
  长名称: ''
  描述: Switch to enable notification for 0% and 100% duty for variable and fixed period channels.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: PwmPowerStateAsynchTransitionMode
  长名称: ''
  描述: Enables / disables support of the PWM Driver to the asynchronous power state transition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: PwmSafetyEnable
  长名称: ''
  描述: Enable/Disable the Safety check and all associated notifications.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: PwmInitCheckApi
  长名称: ''
  描述: Adds / removes the service Pwm_17_GtmCcu6_InitCheck() from the code.
  默认值: true
  最小值: ''
  最大值: ''
```

### 7. PwmPowerStateConfig

**描述**: Each instance of this parameter defines a power state and the callback to be called when this power
state is reached.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PwmPowerState
  长名称: ''
  描述: Each instance of this parameter describes a different power state supported by the PWM HW. It
      should be defined by the HW supplier and used by the PWMDriver to reference specific HW
      configurations which set the PWM HW module in the referenced power state.
  默认值: 0
  最小值: 0
  最大值: 9223372036854775807
- 
  序号: 2
  名称: PwmPowerStateReadyCbkRef
  长名称: ''
  描述: Each instance of this parameter contains a reference to a power mode callback defined in a CDD
      or IoHwAbs component.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 8. CommonPublishedInformation

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
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module from Module List
  默认值: 121
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
                                 This parameter is used to specify the vendor specific name. In
    total, the implementation specific name is generated as follows:
                                 <ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>.
    
                                 E.g.  assuming that the VendorId of the implementor is 123 and the
    implementer chose a VendorApiInfix of "v11r456" a api name Can_Write defined in the SWS will
    translate to Can_123_v11r456Write.
                                 This parameter is mandatory for all modules with upper multiplicity
    > 1. It shall not be used for modules with upper multiplicity =1.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Release
  长名称: ''
  描述: Aurix2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

