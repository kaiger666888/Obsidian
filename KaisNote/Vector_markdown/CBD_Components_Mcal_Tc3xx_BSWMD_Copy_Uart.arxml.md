# Uart

## 模块描述

Configuration of the UART Module.

## 容器列表

### 1. UartGeneral

**描述**: General configuration (parameters) of the UART driver software module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: UartDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: UartRunTimeErrorDetect
  长名称: ''
  描述: Switches the Runtime Error Detection and Notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: UartSafetyEnable
  长名称: ''
  描述: Enable/Disable safety feature in Uart driver
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: UartVersionInfoApi
  长名称: ''
  描述: Switches the Uart_GetVersionInfo function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: UartInitCheckApi
  长名称: ''
  描述: Switches the Uart_InitCheck function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: UartDeInitApi
  长名称: ''
  描述: Switches the Uart_Deinit function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: UartAbortReadApi
  长名称: ''
  描述: Switches the Uart_AbortRead function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: UartAbortWriteApi
  长名称: ''
  描述: Switches the Uart_AbortWrite function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: UartCsrClksel
  长名称: ''
  描述: This parameter selects the Baud Rate Logic Clock for the Uart Driver.
  默认值: ASCLINF
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: UartSleepEnable
  长名称: ''
  描述: Enable/Disable parameter for the ASCLIN Hw module Sleep triggered by SCU
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UartIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: UartInitDeInitApiMode
  长名称: ''
  描述: Defines the privilege mode in which the Initialization and De-initialization APIs would
      operate.
  默认值: MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: UartTimeoutCount
  长名称: ''
  描述: Specifies the maximum time in nanoseconds to wait for hardware timeout errors(Reported as
      hardware access error).
  默认值: 4294967295
  最小值: 100
  最大值: 4294967295
- 
  序号: 14
  名称: UartMainFunctionReadPeriod
  长名称: ''
  描述: Specifies the period of main function Uart_MainFunction_Read in seconds. Uart driver does not
      require this information but the BSW scheduler.
  默认值: 0.005
  最小值: 0.0
  最大值: 10.0
- 
  序号: 15
  名称: UartMainFunctionWritePeriod
  长名称: ''
  描述: Specifies the period of main function Uart_MainFunction_Write in seconds. Uart driver does not
      require this information but the BSW scheduler.
  默认值: 0.005
  最小值: 0.0
  最大值: 10.0
```

### 2. UartConfigSet

**描述**: This container contains the Channel configuration of the Uart driver. This container is a
MultipleConfigurationContainer, i.e. this container and its sub-containers exit once per
configuration set.

该容器没有参数。

### 3. UartChannel

**描述**: This container contains the configuration (parameters) of the UART Controller(s).

#### 参数列表

```yaml
- 
  序号: 1
  名称: UartBaudRate
  长名称: ''
  描述: Specifies the baud rate in bits per second of the UART channel. This parameter shall be
      disabled when 'UartAutoCalcBaudParams' is false
  默认值: 9600
  最小值: 1000
  最大值: 6250000
- 
  序号: 2
  名称: UartHwUnit
  长名称: ''
  描述: This parameter selects the hardware unit used by Uart channel.
  默认值: ASCLIN0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: UartChannelId
  长名称: ''
  描述: Identifies the UART channel.
  默认值: 0
  最小值: 0
  最大值: 11
- 
  序号: 4
  名称: UartAutoCalcBaudParams
  长名称: ''
  描述: Enable/Disable Automatic calculation of Asclin Baudrate params UartChanBaudNumerator,
      UartChanBaudDenominator, UartChanBaudPrescalar,UartChanBaudOVERSAMPLING
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: UartChanBaudNumerator
  长名称: ''
  描述: Specifies the BRG register numerator value used for Baudrate calculation. The value configured
      in this parameter will be written to the BRG.NUMERATOR register field. This parameter
      will be disabled when 'UartAutoCalcBaudParams' is true
  默认值: 24
  最小值: 1
  最大值: 4095
- 
  序号: 6
  名称: UartChanBaudDenominator
  长名称: ''
  描述: Specifies the BRG register Denominator value used for Baudrate calculation. The value
      configured in this parameter will be written to the BRG.DENOMINATOR register field.This
      parameter will be disabled when 'UartAutoCalcBaudParams' is true
  默认值: 1000
  最小值: 1
  最大值: 4095
- 
  序号: 7
  名称: UartChanBaudPrescalar
  长名称: ''
  描述: Specifies the BITCON register Prescalar value used for Baudrate calculation. The value
      configured in this parameter will be written to the BITCON.PRESCALAR register field.This
      parameter will be disabled when 'UartAutoCalcBaudParams' is true
  默认值: 4
  最小值: 0
  最大值: 4095
- 
  序号: 8
  名称: UartChanBaudOverSampling
  长名称: ''
  描述: Specifies the BITCON register Oversampling value used for Baudrate calculation.The value
      configured in this parameter will be written to the BITCON.OVERSAMPLING register field.
      This parameter will be disabled when 'UartAutoCalcBaudParams' is true
  默认值: 9
  最小值: 3
  最大值: 15
- 
  序号: 9
  名称: UartRxPinSelection
  长名称: ''
  描述: Selects the alternate input for the RX signal for the given Uart channel
  默认值: SELECT_A_PORT14_PIN1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: UartCTSEnable
  长名称: ''
  描述: Switch to enable the CTS signal .
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: UartCTSPinSelection
  长名称: ''
  描述: Selects the alternate input for the CTS signal for the given Uart channel
  默认值: SELECT_CTS_A_PORT14_PIN9
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: UartCTSPolarity
  长名称: ''
  描述: This parameter defines the active level or the RTS and CTS signals. Active means ready/clear
      to send.
  默认值: HIGH
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: UartDataLength
  长名称: ''
  描述: Specifies the number of bits to be transmitted or recieved. 
  默认值: 8
  最小值: 2
  最大值: 16
- 
  序号: 14
  名称: UartStopBits
  长名称: ''
  描述: Specifies the number of stop bits Range is one or two. 
  默认值: 1
  最小值: 1
  最大值: 2
- 
  序号: 15
  名称: UartParityBit
  长名称: ''
  描述: This parameter selects the parity even or odd or no parity.
  默认值: NOPARITY
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: UartTxChannelMode
  长名称: ''
  描述: This parameter selects the Tx channel mode polling or interrupt.
  默认值: INTERRUPT
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: UartRxChannelMode
  长名称: ''
  描述: This parameter selects the Rx channel mode polling or interrupt.
  默认值: INTERRUPT
  最小值: ''
  最大值: ''
```

### 4. UartNotification

**描述**: This container contains the Notification function pointers .

#### 参数列表

```yaml
- 
  序号: 1
  名称: UartTransmitNotifPtr
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: UartReceiveNotifPtr
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: UartAbortTransmitNotifPtr
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: UartAbortReceiveNotifPtr
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. CommonPublishedInformation

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

