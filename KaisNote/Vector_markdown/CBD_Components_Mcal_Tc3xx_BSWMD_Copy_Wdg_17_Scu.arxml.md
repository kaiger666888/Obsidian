# Wdg

## 模块描述

Configuration of the Wdg (Watchdog driver) module.

## 容器列表

### 1. WdgGeneral

**描述**: All general parameters of the watchdog driver are collected here.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WdgSafetyEnable
  长名称: ''
  描述: Switches the Safety Error detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgInitCheckApi
  长名称: ''
  描述: Switches the Init Check API to ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WdgDisableAllowed
  长名称: ''
  描述: This parameter is disabled.                        Instead, WdgCPUDisableAllowed is provided
      to enable/disable CPU specific Wdg for every CPU Wdg configured.
      Compile switch to allow / forbid disabling the watchdog driver during runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: WdgIndex
  长名称: ''
  描述: Represents the watchdog driver's ID so that it can be referenced by the watchdog interface.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: WdgInitialTimeout
  长名称: ''
  描述: This parameter is disabled.                                   Instead, WdgCPUInitialTimeout is
      provided as initial timeout for every CPU Wdg configured.
      This initial timeout (sec) for the trigger condition to be initialized during Init
      function. It shall be not larger than WdgMaxTimeout.
  默认值: 5
  最小值: 0.001
  最大值: 65.535
- 
  序号: 7
  名称: WdgMaxTimeout
  长名称: ''
  描述: This parameter is disabled.                        Instead, WdgCPUMaxTimeout is provided as
      maximum CPU specific Wdg timeout for every CPU Wdg configured.
      The maximum timeout (sec) to which the watchdog trigger condition can be initialized.
  默认值: 32
  最小值: 0.001
  最大值: 65.535
- 
  序号: 8
  名称: WdgTriggerTimerSelection
  长名称: ''
  描述: Hardware timer used to service WDG during STC window period.
  默认值: STM_TIMER
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: WdgRunArea
  长名称: ''
  描述: This feature is not provided by IFX.This parameter is disabled.
      Represents the watchdog driver execution area is either from ROM(Flash) or RAM as
      required with the particular microcontroller.
  默认值: ROM
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: WdgTriggerLocation
  长名称: ''
  描述: This feature is not provided by IFX.This parameter is disabled.Location (memory address) of
      the watchdog trigger routine.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: WdgInitApiMode
  长名称: ''
  描述: This parameter selects the operating modes for WDG initialization API.
  默认值: WDG_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: WdgRuntimeApiMode
  长名称: ''
  描述: This parameter selects the operating modes for WDG runtime APIs
  默认值: WDG_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: WdgVersionInfoApi
  长名称: ''
  描述: Compile switch to enable / disable the version information API
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. WdgSettingsConfig

**描述**: Configuration items for the different watchdog settings, including those for external watchdog
hardware.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgCoreId
  长名称: ''
  描述: This parameter refers to CORE ID to which the watchdog settings belong
  默认值: 0
  最小值: 0
  最大值: 5
- 
  序号: 2
  名称: WdgCPUDisableAllowed
  长名称: ''
  描述: Core specific switch to allow / forbid disabling the watchdog driver during runtime.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: WdgCPUInitialTimeout
  长名称: ''
  描述: The initial timeout (sec) for the trigger condition to be initialized during Init function for
      a core. It shall be not larger than WdgMaxTimeout of the core.
  默认值: 5
  最小值: 0.001
  最大值: 65.535
- 
  序号: 4
  名称: WdgCPUMaxTimeout
  长名称: ''
  描述: The maximum timeout (sec) to which the watchdog trigger condition can be initialized for a
      core.
  默认值: 32
  最小值: 0.0
  最大值: 65.535
- 
  序号: 5
  名称: WdgCPUInitialPassword
  长名称: ''
  描述: Initial password for the password access.
  默认值: 60
  最小值: 0
  最大值: 16383
- 
  序号: 6
  名称: WdgDefaultMode
  长名称: ''
  描述: Default mode for watchdog driver initialization.
  默认值: WDGIF_SLOW_MODE
  最小值: ''
  最大值: ''
```

### 3. WdgExternalConfiguration

**描述**: This configuration is not provided as the external watchdog is not supported by IFX.Configuration
items for an external watchdog hardware

该容器没有参数。

### 4. WdgSettingsFast

**描述**: Hardware dependent settings for the watchdog drivers fast mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgFastModeTimeoutValue
  长名称: ''
  描述: Fast mode timeout in seconds for WDT
  默认值: 0.01
  最小值: 0.001
  最大值: 0.16777216
```

### 5. WdgSettingsSlow

**描述**: Hardware dependent settings for the watchdog driver's "slow" mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgSlowModeTimeoutValue
  长名称: ''
  描述: Slow mode timeout in seconds for WDT
  默认值: 0.02
  最小值: 0.001
  最大值: 10.73741824
```

### 6. WdgSettingsOff

**描述**: Hardware dependent settings for the watchdog driver's "off" mode.

该容器没有参数。

### 7. WdgTriggerTimerSetting

**描述**: This container contains the configuration elements for configuring GTM\STM hardware

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgSlowRefreshTime
  长名称: ''
  描述: Slow mode Gtm/Stm callback period in seconds for WDT.
  默认值: 0.015
  最小值: 0.001
  最大值: 10.73741824
- 
  序号: 2
  名称: WdgFastRefreshTime
  长名称: ''
  描述: Fast mode Gtm/Stm callback period in seconds for WDT.
  默认值: 0.007
  最小值: 0.001
  最大值: 0.16777216
```

### 8. GtmTimerConfiguration

**描述**: This container contains the configuration elements for configuring GTM timer hardware.

该容器没有参数。

### 9. GtmTimerOutputModuleConfiguration

**描述**: This container contains the TOM/ATOM channel Configuration for GTM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: GtmTimerClockSelect
  长名称: ''
  描述: This parameter decides the Clock Source for GTM timer.
  默认值: GTM_FIXED_CLOCK_0
  最小值: ''
  最大值: ''
```

### 10. WdgDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 11. WdgPublishedInformation

**描述**: Container holding all WDG specific published information parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: WdgTriggerMode
  长名称: ''
  描述: Watchdog trigger mode (toggle/window/both)
  默认值: WDG_WINDOW
  最小值: ''
  最大值: ''
```

### 12. CommonPublishedInformation

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
  默认值: 102
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
- 
  序号: 10
  名称: VendorApiInfix
  长名称: ''
  描述: |
    In driver modules which can be instantiated several times on a single ECU, BSW00347 requires
    that the name of APIs is extended by the VendorId and a vendor specific name.
    This parameter is used to specify the vendor specific name. In total, the implementation
    specific name is generated as follows:
    <ModuleName>_>VendorId>_<VendorApiInfix><Api name from SWS>.
    
    E.g.  assuming that the VendorId of the implementer is 17 and the implementer chose a
    VendorApiInfix of "Scu" a api name Wdg_SetMode defined in the SWS will translate to
    Wdg_17_Scu_SetMode.
    
    This parameter is mandatory for all modules with upper multiplicity > 1. It shall not be used
    for modules with upper multiplicity =1.
  默认值: ''
  最小值: ''
  最大值: ''
```

