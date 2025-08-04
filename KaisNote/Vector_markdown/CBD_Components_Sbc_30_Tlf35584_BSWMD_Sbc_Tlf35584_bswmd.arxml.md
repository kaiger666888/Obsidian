# Sbc

## 模块描述

Driver for System Basis Chip devices. Incorporates, manages / abstracts HW in regard to the AUTOSAR
defined functionalities of respective CAN- / LIN-transceivers as well as Watchdog functionality
which are part of single chip ICs. Vectors SBC driver requires MCAL SPI driver for communication
purposes towards the external device.
#CAN #LIN #TRANSCEIVER #WDG #SPI #PowerManagement #PMIC
#AUTOSAR #Vector

## 容器列表

### 1. SbcPublicCfg

**描述**: This container includes general configuration options for the Sbc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcSingleInstanceApi
  长名称: ''
  描述: |
    This parameter enables/disables the SingleInstanceApi feature.
    
    True: The SingleInstanceApi feature is enabled. The module defines its APIs without infix.
    False: The SingleInstanceApi feature is disabled. The module defines its APIs with infix.
    
    Note: Normally, all API names are infixed by a combination of VendorId and VendorApiInfix in
    order to allow the usage of multiple different Sbc drivers within one stack.
    When this feature is enabled the module defines the APIs without an infix. This can be set only
    if there is not more than one Sbc driver active in this configuration.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SbcDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    
    True: Development error detection is enabled.
    False: Development error detection is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcGetVersionInfo
  长名称: ''
  描述: |
    This parameter enables/disables the function Sbc_30_Tlf35584_GetVersionInfo() to get major,
    minor and patch version information.
    
    True: GetVersionInfo-API is available.
    False:  GetVersionInfo-API is not available.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SbcUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to <Module>_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SbcSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used.
    
    These checks improve robustness as e.g. invalid parameters are checked before function is
    executed. This attribute has to be enabled for safety projects where this component is mapped to
    an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SbcParityBitCalculation
  长名称: ''
  描述: |
    Selects if parity bit calculation is enabled or disabled.
    
    FALSE: Parity bit calculation is disabled.
    TRUE:  Parity bit calculation in enabled.
  默认值: true
  最小值: ''
  最大值: ''
```

### 2. SbcDevice

**描述**: This container includes configuration of specific Sbc devices.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcDeviceId
  长名称: ''
  描述: This value specifies the identifier for the Sbc device. The value must be unique on one device
      instance.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SbcCtrlLoopMaxCycles
  长名称: ''
  描述: This value specifies the number of loop cycles after hardware-dependent loop timeout occurs.
  默认值: 15
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: SbcDerivative
  长名称: ''
  描述: This value specifies the used derivative.
  默认值: TLF35584
  最小值: ''
  最大值: ''
```

### 3. SbcWatchdogPeripheral

**描述**: This container includes the watchdog configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcWatchdogPeripheralId
  长名称: ''
  描述: This value specifies the identifier for the watchdog peripheral. The value must be unique on
      one device instance.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: SbcWatchdogInitialMode
  长名称: ''
  描述: |
    This parameter defines the mode of the watchdog that is selected during the initialization of
    the Sbc.
    
    WDGIF_OFF_MODE: Watchdog is disabled during initialization.
    WDGIF_SLOW_MODE: Watchdog is initialized with SLOW mode.
    WDGIF_FAST_MODE: Watchdog is initialized with FAST mode.
  默认值: WDGIF_FAST_MODE
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcWatchdogTriggerOffset
  长名称: ''
  描述: This value specifies the offset in percent for the first trigger point to be located in the
      specified watchdog trigger interval.
  默认值: 60
  最小值: 0
  最大值: 100
- 
  序号: 4
  名称: SbcWatchdogPeripheralType
  长名称: ''
  描述: |
    This parameter defines whether the functional watchdog peripheral or the window watchdog
    peripheral is used.
    
    FWD: Functional watchdog peripheral is used.
    WWD: Window watchdog peripheral is used.
  默认值: WWD
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SbcWatchdogPeripheralCycleTime
  长名称: ''
  描述: |
    This parameter defines the watchdog cycle time.
    
    WDCYC_100US: Watchdog cycle time is set to 0.1 ms tick period.
    WDCYC_1MS: Watchdog cycle time is set to 1 ms tick period.
  默认值: WDCYC_100US
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SbcWatchdogErrorThreshold
  长名称: ''
  描述: |
    This parameter defines the watchdog (FWD/WWD) error threshold to generate reset and enter into
    INIT state.
    
    Note: Depending on the value of parameter SbcWatchdogPeripheralType this value is written to
    WDCFG0.WWDETHR or FWDCFG.FWDETHR.
  默认值: 9
  最小值: 0
  最大值: 15
```

### 4. SbcWatchdogPeripheralFastMode

**描述**: This container includes configuration of watchdog FAST mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcWatchdogTriggerPeriod
  长名称: ''
  描述: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has
      to be configured according to the requirements of the hardware configuration.
  默认值: 70
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: SbcWwdClosedWindow
  长名称: ''
  描述: |
    This value specifies the closed window time as multiple of 50 watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written
    to WWDCFG0.CW.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 6
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: SbcWwdOpenWindow
  长名称: ''
  描述: |
    This value specifies the open window time as multiple of 50 watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written
    to WWDCFG1.OW.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 6
  最小值: 0
  最大值: 31
- 
  序号: 4
  名称: SbcFwdHeartbeatTimerPeriod
  长名称: ''
  描述: |
    This parameter defines the functional watchdog heartbeat timer period as a multiple of 50
    watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written
    to FWDCFG.WDHBTP.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 11
  最小值: 0
  最大值: 31
```

### 5. SbcWatchdogPeripheralSlowMode

**描述**: This container includes configuration of watchdog SLOW mode.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcWatchdogTriggerPeriod
  长名称: ''
  描述: The value species the period (in milliseconds) of the hardware watchdog triggering. This has
      to be configured according to the requirements of the hardware configuration.
  默认值: 70
  最小值: 1
  最大值: 65535
- 
  序号: 2
  名称: SbcWwdClosedWindow
  长名称: ''
  描述: |
    This value specifies the closed window time as multiple of 50 watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written
    to WWDCFG0.CW.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 6
  最小值: 0
  最大值: 31
- 
  序号: 3
  名称: SbcWwdOpenWindow
  长名称: ''
  描述: |
    This value specifies the open window time as multiple of 50 watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written
    to WWDCFG1.OW.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 6
  最小值: 0
  最大值: 31
- 
  序号: 4
  名称: SbcFwdHeartbeatTimerPeriod
  长名称: ''
  描述: |
    This parameter defines the functional watchdog heartbeat timer period as a multiple of 50
    watchdog cycles.
    
    Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written
    to FWDCFG.WDHBTP.
    
    0 = 50 wd cycles
    1 = 100 wd cycles
    2 = 150 wd cycles
    ...
    31 = 1600 wd cycles
  默认值: 11
  最小值: 0
  最大值: 31
```

### 6. SbcLinTrcvPeripheral

**描述**: This container includes the configuration for LIN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a LIN transceiver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcLinTrcvPeripheralId
  长名称: ''
  描述: This value specifies the identifier for the LIN transceiver peripheral. The value must be
      unique on one device instance.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 7. SbcCanTrcvPeripheral

**描述**: This container includes the configuration for CAN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a CAN transceiver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcCanTrcvPeripheralId
  长名称: ''
  描述: This parameter specifies the identifier for the CAN transceiver peripheral. The value must be
      unique on one device instance.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 8. SbcCanTrcvPartialNetwork

**描述**: This container includes the CAN transceiver driver information about the configuration of Partial
Networking functionality. If the container is intantiated the selective wakeup functionality is
activated on the CanTrcv peripheral.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcCanTrcvBaudRate
  长名称: ''
  描述: This value specifies the CAN Bus communication baud rate in kbps.
  默认值: 500
  最小值: 0
  最大值: 1000
- 
  序号: 2
  名称: SbcCanTrcvPnCanIdIsExtended
  长名称: ''
  描述: |
    This parameter defines whether extended or standard identifier is used for wake-up frames.
    
    True: Extended CAN identifier is used.
    False: Standard CAN identifier is used.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcCanTrcvPnEnabled
  长名称: ''
  描述: |
    This parameter defines whether the selective wake-up function is enabled or disabled in HW.
    
    True: Selective wakeup feature is enabled in the transceiver hardware.
    False: Selective wakeup feature is disabled in the transceiver hardware.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SbcCanTrcvPnFrameCanId
  长名称: ''
  描述: This value specifies the CAN ID of the Wake-up Frame (WUF).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: SbcCanTrcvPnFrameCanIdMask
  长名称: ''
  描述: This value specifies the ID Mask for the selective activation of the transceiver. It is used
      to configure a Wake-up frame (WUF) which consists of a group of CAN identifiers.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: SbcCanTrcvPnFrameDlc
  长名称: ''
  描述: This value specifies the data length of the Wake-up Frame (WUF).
  默认值: 0
  最小值: 0
  最大值: 8
- 
  序号: 7
  名称: SbcCanTrcvVerifyPnConfig
  长名称: ''
  描述: |
    This parameter defines whether the selective wake-up configuration should be verified after it
    has been written to the hardware.
    
    TRUE  = The selective wakeup configuration written to the hardware is compared to the configured
    values.
    FALSE = The selective wakeup configuration written to the hardware is not compared to the
    configured values.
  默认值: true
  最小值: ''
  最大值: ''
```

### 9. SbcCanTrcvPnFrameDataMaskSpec

**描述**: This container includes the data payload mask to be used on the received payload in order to
determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcCanTrcvPnFrameDataMask
  长名称: ''
  描述: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the
      received payload in order to determine if the transceiver must be woken up by the
      received Wake-up Frame (WUF).
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SbcCanTrcvPnFrameDataMaskIndex
  长名称: ''
  描述: This value specifies the position n in frame of the mask-part.
  默认值: 0
  最小值: 0
  最大值: 7
```

### 10. SbcInitConfig

**描述**: This container includes the initialization configuration of the Sbc device.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcErrPinMonitor
  长名称: ''
  描述: |
    This parameter defines whether the ERR pin monitor functionality is enabled.
    
    True: ERR pin monitor functionality is enabled.
    Flase: ERR pin monitor functionality is disabled.
    
    Note: If this parameter is enabled the ERR pin monitoring supervision function has to be
    serviced properly, otherwise resets will occur.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SbcErrPinMonitorRecovery
  长名称: ''
  描述: |
    This parameter defines whether error pin monitor recovery enable is requested during
    initialization.
    
    True: Error pin monitor recovery enable is requested.
    False: Error pin monitor recovery enable is not requested.
    
    
    Note: This value is used to set register field SYSPCFG1.ERRREC.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcErrPinRecoveryTime
  长名称: ''
  描述: |
    This parameter defines the ERR pin monitor recovery time which is requested during
    initialization.
    
    ERREC_1_MS: An ERR pin monitor recovery time of 1 ms is requested.
    ERREC_2_5MS: An ERR pin monitor recovery time of 2.5 ms is requested.
    ERREC_5MS: An ERR pin monitor recovery time of 5 ms is requested.
    ERREC_10MS : An ERR pin monitor recovery time of 10 ms is requested.
    
    
    Note: This value is used to set register field SYSPCFG1.ERR.
  默认值: ERREC_1_MS
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SbcErrPinMonitorInSleep
  长名称: ''
  描述: |
    This parameter defines whether error pin monitoring is active in SLEEP.
    
    True: Error pin monitoring is active in SLEEP.
    False: Error pin monitoring is not active in SLEEP.
    
    Note: This value is used to write register field SYSPCFG1.ERRSLPEN.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SbcSafeState2Delay
  长名称: ''
  描述: |
    This parameter defines the delay applied for transitions from NORMAL to INIT, WAKE and SLEEP
    state.
    
    SS2DEL_NODELAY: Delay of 0 ms is request.
    SS2DEL_10MS: Delay of 10 ms is requested.
    SS2DEL_50MS: Delay of 50 ms is requested.
    SS2DEL_100MS: Delay of 100 ms is requested.
    SS2DEL_250MS: Delay of 250 ms is requested.
    SS2DEL_1250MS: Delay of 1250 ms is requested. (This value is only available for the TLF35585)
    SS2DEL_2500MS: Delay of 2500 ms is requested. (This value is only available for the TLF35585)
    
    Note: This value is related with register field SYSPCFG1.SS2DEL.
  默认值: SS2DEL_NODELAY
  最小值: ''
  最大值: ''
```

### 11. SbcDeviceAccess

**描述**: This container includes the configuration to access the specific Sbc hardware instance.

该容器没有参数。

### 12. SbcDioAccess

**描述**: This container includes the Dio-specific configuration to access the Sbc device.

Note: The existence of this container in combination with the usage of the SbcWatchdogPeripheralType
'WWD' means that the window watchdog is not triggered via SPI, but via the input pin WDI.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcWaitLoopCycles
  长名称: ''
  描述: This value specifies the number of loop cycles to perform a wait until the WDI high level is
      sampled by the device.
  默认值: 6000
  最小值: 1
  最大值: 65535
```

### 13. SbcDioChannel

**描述**: This containers includes the reference to one Dio Channel that is used by the Sbc module.

该容器没有参数。

### 14. SbcSpiAccess

该容器没有参数。

### 15. SbcSpiSequence

**描述**: This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the
container instance specifies the name of the Sbc module.

该容器没有参数。

### 16. SbcSpiChannel

**描述**: This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the
container instance specifies the name of the Sbc module.

该容器没有参数。

### 17. SbcI2cAccess

**描述**: This container includes the I2C-specific configuration to access the Sbc device.

该容器没有参数。

### 18. SbcI2cSequence

**描述**: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the
container instance specifies the name of the Sbc module.

该容器没有参数。

### 19. SbcI2cChannel

**描述**: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the
container instance specifies the name of the Sbc module.

该容器没有参数。

### 20. SbcSystemConfig

**描述**: This container includes system specific configuration.

该容器没有参数。

### 21. SbcEnableSupplyNormal

**描述**: This container includes mode-specific configuration of power supplies for system mode NORMAL.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcEnableLDO_Stby
  长名称: ''
  描述: |
    This parameter defines whether LDO_Stby is switched on during a mode change to system mode
    'NORMAL'.
    
    True: LDO_Stby is switched on during mode change to 'NORMAL'.
    False: LDO_Stby is switched off during mode change to 'NORMAL'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SbcEnableTracker1
  长名称: ''
  描述: |
    This parameter defines whether Tracker1 is switched on during a mode change to system mode
    'NORMAL'.
    
    True: Tracker1 is switched on during mode change to 'NORMAL'.
    False: Tracker1 is switched off during mode change to 'NORMAL'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcEnableTracker2
  长名称: ''
  描述: |
    This parameter defines whether Tracker2 is switched on during a mode change to system mode
    'NORMAL'.
    
    True: Tracker2 is switched on during mode change to 'NORMAL'.
    False: Tracker2 is switched off during mode change to 'NORMAL'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SbcEnableLDO_Com
  长名称: ''
  描述: |
    This parameter defines whether LDO_Com is switched on during a mode change to system mode
    'NORMAL'.
    
    True: LDO_Com is switched on during mode change to 'NORMAL'.
    False: LDO_Com is switched off during mode change to 'NORMAL'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SbcEnableVoltRef
  长名称: ''
  描述: |
    This parameter defines whether Volt_Ref is switched on during a mode change to system mode
    'NORMAL'.
    
    True: Volt_Ref is switched on during mode change to 'NORMAL'.
    False: Volt_Ref is switched off during mode change to 'NORMAL'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SbcDisableOffset
  长名称: ''
  描述: |
    This parameter defines whether offset regulation is disabled during a mode change to system mode
    'NORMAL'.
    
    True: Offset regulation disabled during mode change to 'NORMAL'.
    False: Offset regulation enabled during mode change to 'NORMAL'.
    
    Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has
    to be false!
  默认值: false
  最小值: ''
  最大值: ''
```

### 22. SbcEnableSupplyStandby

**描述**: This container includes mode-specific configuration of power supplies for system mode STANDBY.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcEnableLDO_Stby
  长名称: ''
  描述: |
    This parameter defines whether LDO_Stby is switched on during a mode change to system mode
    'STANDBY'.
    
    True: LDO_Stby is switched on during mode change to 'STANDBY'.
    False: LDO_Stby is switched off during mode change to 'STANDBY'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SbcEnableTracker1
  长名称: ''
  描述: |
    This parameter defines whether Tracker1 is switched on during a mode change to system mode
    'STANDBY'.
    
    True: Tracker1 is switched on during mode change to 'STANDBY'.
    False: Tracker1 is switched off during mode change to 'STANDBY'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SbcEnableTracker2
  长名称: ''
  描述: |
    This parameter defines whether Tracker2 is switched on during a mode change to system mode
    'STANDBY'.
    
    True: Tracker2 is switched on during mode change to 'STANDBY'.
    False: Tracker2 is switched off during mode change to 'STANDBY'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SbcEnableLDO_Com
  长名称: ''
  描述: |
    This parameter defines whether LDO_Com is switched on during a mode change to system mode
    'STANDBY'.
    
    True: LDO_Com is switched on during mode change to 'STANDBY'.
    False: LDO_Com is switched off during mode change to 'STANDBY'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SbcEnableVoltRef
  长名称: ''
  描述: |
    This parameter defines whether Volt_Ref is switched on during a mode change to system mode
    'STANDBY'.
    
    True: Volt_Ref is switched on during mode change to 'STANDBY'.
    False: Volt_Ref is switched off during mode change to 'STANDBY'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SbcDisableOffset
  长名称: ''
  描述: |
    This parameter defines whether offset regulation is disabled during a mode change to system mode
    'STANDBY'.
    
    True: Offset regulation disabled during mode change to 'STANDBY'.
    False: Offset regulation enabled during mode change to 'STANDBY'.
    
    Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has
    to be false!
  默认值: false
  最小值: ''
  最大值: ''
```

### 23. SbcEnableSupplySleep

**描述**: This container includes mode-specific configuration of power supplies for system mode 'SLEEP'.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SbcEnableLDO_Stby
  长名称: ''
  描述: |
    This parameter defines whether LDO_Stby is switched on during a mode change to system mode
    'SLEEP'.
    
    True: LDO_Stby is switched on during mode change to 'SLEEP'.
    False: LDO_Stby is switched off during mode change to 'SLEEP'.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SbcDisableOffset
  长名称: ''
  描述: |
    This parameter defines whether  offset regulation is disabled during a mode change to system
    mode 'SLEEP'.
    
    True: Offset regulation disabled during mode change to 'SLEEP'.
    False: Offset regulation enabled during mode change to 'SLEEP'.
    
    Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has
    to be false!
  默认值: false
  最小值: ''
  最大值: ''
```

