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
  默认值: 50
  最小值: 0
  最大值: 500
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
  默认值: 8
  最小值: 1
  最大值: 65535
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
  默认值: 8
  最小值: 1
  最大值: 65535
```

### 6. SbcLinTrcvPeripheral

**描述**: This container includes the configuration for LIN transceiver peripherals.

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

该容器没有参数。

### 11. SbcDeviceAccess

该容器没有参数。

### 12. SbcDioAccess

该容器没有参数。

### 13. SbcDioChannel

该容器没有参数。

### 14. SbcSpiAccess

**描述**: This container includes the SPI-specific configuration to access the Sbc device.

该容器没有参数。

### 15. SbcSpiSequence

**描述**: This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the
container instance specifies the name of the Sbc module.

该容器没有参数。

### 16. SbcSpiChannel

**描述**: This containers represents one Spi Channel that is used by the Sbc module. The short-name of the
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

