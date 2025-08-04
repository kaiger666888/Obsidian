# Ocu

## 模块描述

Configuration of Ocu (Output Compare Unit) module.

## 容器列表

### 1. OcuConfigSet

**描述**: This container is the base of a Configuration Set, which contains the configured OCU channels. This
way, different configuration sets can be defined for post-build process.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuCountdirection
  长名称: ''
  描述: This parameter indicates the count direction for the whole OCU driver.
  默认值: OCU_UPCOUNTING
  最小值: ''
  最大值: ''
```

### 2. OcuChannel

**描述**: Configuration of an individual OCU channel.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuAssignedHardwareChannel
  长名称: ''
  描述: The physical hardware channel that is assigned to this logical channel. This parameter is
      not-editable or not used. Hardware Channel is configured through
      GtmTimerUsed(../GtmTimerOutputModuleConfiguration/..)
  默认值: 0
  最小值: 0
  最大值: 15
- 
  序号: 2
  名称: OcuChannelId
  长名称: ''
  描述: Channel Id of the OCU channel. This value will be assigned to the symbolic name derived from
      the OcuChannel container short name. It defines the assignment of the channel to the
      physical OCU hardware channel.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: OcuChannelTickDuration
  长名称: ''
  描述: Specifies the tick duration of the counter of the channel. This parameter is the number of the
      input clock edges (rising edges or falling edges exclusively) counted each time to
      increase the counter by one unit.Note: This parameter is not-used,not editable and
      default value is set to 1
  默认值: 1
  最小值: 1
  最大值: 32768
- 
  序号: 4
  名称: OcuDefaultThreshold
  长名称: ''
  描述: Value of comparison threshold used for Initialization.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: OcuHardwareTriggeredAdc
  长名称: ''
  描述: This parameter is used to allow the OCU channel to trigger an ADC channel upon compare match.
      The value of the parameter represents the ADC physical channel to trigger.
  默认值: 0
  最小值: 0
  最大值: 383
- 
  序号: 6
  名称: OcuHardwareTriggeredDMA
  长名称: ''
  描述: This parameter is used to allow the OCU channel to trigger a DMA channel upon compare match.
      The value of the parameter represents the DMA physical channel to trigger.
  默认值: 0
  最小值: 0
  最大值: 127
- 
  序号: 7
  名称: OcuMaxCounterValue
  长名称: ''
  描述: Maximum value in ticks, the counter of the OCU channel is able to count.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 8
  名称: OcuNotification
  长名称: ''
  描述: Definition of a function pointer to a Callback function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: OcuOuptutPinUsed
  长名称: ''
  描述: Information about the usage of an output pin on this channel.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: OcuOutputPinDefaultState
  长名称: ''
  描述: The parameter OcuOutputPinDefaultState represents the state that a pin associated with a
      channel shall be set to after initialisation.
  默认值: OCU_LOW
  最小值: ''
  最大值: ''
```

### 3. GtmTimerOutputModuleConfiguration

**描述**: Choose GTM TOM/ATOM channel which will be used by this OCU Channel.
Referred timer channel in MCU should have TomChannelUsage/ AtomChannelUsage as USED_BY_OCU_DRIVER

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

### 4. OcuGroup

**描述**: This container contains the parameters for configuring an OCU group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuGroupId
  长名称: ''
  描述: Numeric ID of the group. This parameter is the symbolic name of the group.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. OcuHWSpecificSettings

**描述**: This container contains Ocu-specific parameters for selecting the clock source and setting optional
prescalers if supported by hardware.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuClockSource
  长名称: ''
  描述: The OCU driver specific clock input for the unit can statically be configured to select
      different clock sources if provided by hardware. Enumeration literals are defined vendor
      specific.
  默认值: UNUSED
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OcuPrescale
  长名称: ''
  描述: Optional OCU driver specific clock prescale factor, if supported by hardware. Implementation
      is defined vendor specific.
  默认值: UNUSED
  最小值: ''
  最大值: ''
```

### 6. OcuConfigurationOfOptionalApis

**描述**: Configuration of optional APIs.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuDeInitApi
  长名称: ''
  描述: Adds / removes the service Ocu_DeInit() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OcuGetCounterApi
  长名称: ''
  描述: Adds / removes the service Ocu_GetCounter() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OcuNotificationSupported
  长名称: ''
  描述: Adds / removes the services Ocu_EnableNotification() and Ocu_DisableNotification() from the
      code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: OcuSetAbsoluteThresholdApi
  长名称: ''
  描述: Adds / removes the service Ocu_SetAbsoluteThreshold() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: OcuSetPinActionApi
  长名称: ''
  描述: Adds / removes the service Ocu_SetPinAction() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: OcuSetPinStateApi
  长名称: ''
  描述: Adds / removes the service Ocu_SetPinState() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: OcuSetRelativeThresholdApi
  长名称: ''
  描述: Adds / removes the service Ocu_SetRelativeThreshold() from the code.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: OcuVersionInfoApi
  长名称: ''
  描述: Switch to indicate that the Ocu_GetVersionInfo() is supported.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: OcuInitCheckApi
  长名称: ''
  描述: |
    Adds / removes the service Ocu_InitCheck() from the code.
                                true: Ocu_InitCheck() can be used.
                                false: Ocu_InitCheck() can not be used.
  默认值: false
  最小值: ''
  最大值: ''
```

### 7. OcuGeneral

**描述**: This container contains the module-wide configuration parameters of the OCU Driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: OcuDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: OcuMultiCoreErrorDetect
  长名称: ''
  描述: Switches the MultiCore Development Error Detection on or off. true: Enabled. false: Disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: OcuSafetyEnable
  长名称: ''
  描述: Switch for enabling/Disabling OcuSafetyEnable
  默认值: true
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
  默认值: 125
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
  描述: Aurix derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

