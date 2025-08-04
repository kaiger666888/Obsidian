# Port

## 模块描述

Configuration of the Port module.

## 容器列表

### 1. PortConfigSet

**描述**: This container contains the configuration parameters and sub containers of the Port module.

该容器没有参数。

### 2. PortContainer

**描述**: Container collecting the PortPins.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortNumber
  长名称: ''
  描述: The specified port number of this PortContainer.
  默认值: 0
  最小值: 0
  最大值: 40
- 
  序号: 2
  名称: PortNumberOfPortPins
  长名称: ''
  描述: The number of specified PortPins in this PortContainer.
  默认值: 13
  最小值: 1
  最大值: 16
```

### 3. PortPin

**描述**: Configuration of the individual port pins.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortPinId
  长名称: ''
  描述: Pin Id of the port pin. This value will be assigned to the symbolic name derived from the port
      pin container short name.
  默认值: 0
  最小值: 0
  最大值: 654
- 
  序号: 2
  名称: PortPinSymbolicName
  长名称: ''
  描述: Symbolic name of the Port Pin.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PortPinDirection
  长名称: ''
  描述: The initial direction of the pin (IN or OUT). If the direction is not changeable, the value
      configured here is fixed.
  默认值: PORT_PIN_IN
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PortPinDirectionChangeable
  长名称: ''
  描述: |
    Parameter to indicate if the direction is changeable on a port pin during runtime.
                                      true: Port Pin direction changeable enabled.
                                      false: Port Pin direction changeable disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PortPinInitialMode
  长名称: ''
  描述: Port pin mode from mode list for use with Port_Init() function.
  默认值: GPIO
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PortPinLevelValue
  长名称: ''
  描述: Port Pin Level value from Port pin list.
  默认值: PORT_PIN_LEVEL_LOW
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PortPinMode
  长名称: ''
  描述: Supported modes for Port pin from mode list.
  默认值: PORT_PIN_MODE_ALL
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PortPinModeChangeable
  长名称: ''
  描述: Parameter to indicate if the mode is changeable on a port pin during runtime. True: Port Pin
      mode changeable allowed. False: Port Pin mode changeable not permitted.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PortPinInputPullResistor
  长名称: ''
  描述: Parameter to indicate to the driver what type of internal Pull resistor [up/down] is to be
      connected to the PORT Pin.
  默认值: PORT_PIN_IN_PULL_UP
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: PortPinOutputPadDriveStrength
  长名称: ''
  描述: Parameter to configure the output drive strength and slew rate of a PORT pin.
  默认值: PORT_PIN_DEFAULT_DRIVER
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: PortPinOutputPinDriveMode
  长名称: ''
  描述: Parameter to indicate how the output of the pad is to be connected to the package pin.
  默认值: PORT_PIN_OUT_PUSHPULL
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: PortPinInputPadLevel
  长名称: ''
  描述: Parameter to select between TTL and automotive level for input function of Port Pin.
  默认值: PORT_INPUT_LEVEL_CMOS_AUTOMOTIVE
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: PortPinEnableAnalogInputOnly
  长名称: ''
  描述: This parameter allows configuration of the PDISC register.
      Range:                                 ENABLE: Pin has support for Analog Input.
      DISABLE: Pin do not have support for Analog Input.
  默认值: PORT_PIN_ANALOG_INPUT_DISABLE
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: PortPinEmergencyStop
  长名称: ''
  描述: Parameter to enable/disable the Emergency Stop functionality of a pin configured as an output
      pin.                               With this feature enabled, an output pin will
      automatically be reconfigured as an input pin when emergency conditions are encountered.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: PortPinControllerSelect
  长名称: ''
  描述: With this feature enabled, certain controllers can be allowed to take control of certain ports
      [e.g. SCR, VADC, ETH and SMU].
  默认值: DISABLE
  最小值: ''
  最大值: ''
```

### 4. PortLVDS

**描述**: Configuration of the individual port pins.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortLVDSPinPair
  长名称: ''
  描述: Parameter identifies the PortPinPair supporting the LVDS feature..
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PortLVDSRxEnController
  长名称: ''
  描述: This parameter determines who controls the LVDS enable/disable function - PORT controlled or
      HSCT controlled.
  默认值: PORT_CONTROLLED
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PortLVDSRxPathEnable
  长名称: ''
  描述: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PortLVDSRxTerminationMode
  长名称: ''
  描述: This parameter selects the internal load capacitance,
      EXTERNAL_TERMINATION selects external termination on the PCB,
      INTERNAL_TERMINATION selects an 100ohm Receiver internal termination
  默认值: INTERNAL_TERMINATION
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PortLVDSMode
  长名称: ''
  描述: Parameter to select reduced frequency mode LVDS-M of the receiver 
  默认值: LVDSH
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PortLVDSPadSupply
  长名称: ''
  描述: Parameter to select  pad supply value 
  默认值: V3_3
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PortLVDSTxEnController
  长名称: ''
  描述: This parameter determines who controls the LVDS enable/disable function - PORT controlled or
      HSCT controlled.
  默认值: PORT_CONTROLLED
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: PortLVDSTxPathEnable
  长名称: ''
  描述: This parameter specifies whether the Pin-Pair is in LVDS mode or CMOS mode.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: PortLVDSTxPowerDownPullDown
  长名称: ''
  描述: This parameter specifies the state of the Transmit Pull down resistor.
  默认值: DISABLE
  最小值: ''
  最大值: ''
```

### 5. PortGeneral

**描述**: Module wide configuration parameters of the PORT driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: PortDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: PortSetPinDirectionApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Port_SetPinDirection().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: PortSetPinModeApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the use of the function Port_SetPinMode().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: PortVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: PortInitApiMode
  长名称: ''
  描述: This configuration parameter defines the mode in which the Port Init  API will be used.
  默认值: PORT_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: PortSafetyEnable
  长名称: ''
  描述: Enable/Disable the Safety check and all associated notifications.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: PortInitCheckApi
  长名称: ''
  描述: Adds / removes the service  Port_InitCheck() from the code.
  默认值: false
  最小值: ''
  最大值: ''
```

### 6. CommonPublishedInformation

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
  默认值: 124
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

