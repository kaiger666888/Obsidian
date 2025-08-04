# I2c

## 模块描述

Inter-Integrated Circuit. The driver provides services for reading from and writing to devices
connected via I2c buses. It provides access to I2c communication to several users (e.g. EEPROM,
Watchdog, I/O ASICs) and the required mechanism to configure the onchip I2c peripheral.

#I2c #Driver
#MICROSAR #Vector



## 容器列表

### 1. I2cConfigSet

**描述**: This container includes the base for a multiple configuration set.

该容器没有参数。

### 2. I2cChannel

**描述**: Channel specific configuration parameters of the I2c.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cChannelId
  长名称: ''
  描述: This parameter specifies the identifier of a channel.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: I2cDeviceAddress
  长名称: ''
  描述: This parameter specifies the address of a slave device which is accessed by the master.
  默认值: 0
  最小值: 0
  最大值: 1023
- 
  序号: 3
  名称: I2cChainChannel
  长名称: ''
  描述: |
    This parameter defines whether the channel is chained.
    
    True: The channel is chained.
    False: The channel is not chained.
    
    Note: A chained channel requires follow up to be set. It does not set a restart condition and
    the retransmission of the slave address is ommited.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: I2cDefaultData
  长名称: ''
  描述: |
    This parameter specifies the default value of the channel.
    
    Note: The default data is transmitted in case of TxBuffer and RxBuffer of the channel is set to
    NULL_PTR (e.g. via API I2c_SetupEB).
  默认值: 255
  最小值: 0
  最大值: 255
```

### 3. I2cBus

**描述**: Bus specific configuration parameters of the I2c.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cBusId
  长名称: ''
  描述: This parameter specifies the identifier of a bus.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: I2cTransferRate
  长名称: ''
  描述: This parameter specifies the baudrate of the bus in KHz.
  默认值: 100
  最小值: 100
  最大值: 1001
- 
  序号: 3
  名称: I2cTimeout
  长名称: ''
  描述: |
    This parameter specifies the timeout for I2c in ms.
    
    Note: If the timeout expires, the driver applies the configured timeout handling (via API
    I2c_SetTimeoutHandling).
  默认值: 0.01
  最小值: 0.001
  最大值: 10
```

### 4. I2cHardwareUnit

**描述**: Hardware unit specific configuration parameters of the I2c.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cUnitId
  长名称: ''
  描述: This parameter specifies the identifier of the hardware unit.
  默认值: 0
  最小值: 0
  最大值: 10
- 
  序号: 2
  名称: I2cClockFrequencyManual
  长名称: ''
  描述: |
    This parameter specifies the clock rate (in MHz) of the I2C hardware unit.
    
    Note: This parameter is used to calculate baudrate settings in case the reference
    I2cClockConfiguration is not configured.
  默认值: 8000000
  最小值: 1
  最大值: 1.7976931348623157E+308
- 
  序号: 3
  名称: I2cClockDivider
  长名称: ''
  描述: This parameter sets the clock divider for the i2c module.
  默认值: 2
  最小值: 1
  最大值: 255
- 
  序号: 4
  名称: I2cPortSelect
  长名称: ''
  描述: This parameter specifices the selected pins providing the serial data (SDA) and clock (SCL)
      signals.
  默认值: PORTA
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: I2cDelayStageSDA
  长名称: ''
  描述: |
    SDA Delay stages for data hold time. The standard delay time is 0x00.
    note: SDA delay from the SCL falling edge. This  will also affect SDA setup time relative to the
    next SCL rising edge.
    
  默认值: 0
  最小值: 0
  最大值: 63
```

### 5. I2cRecovery

**描述**: This container includes parameters which are required to perform I2c bus free.

该容器没有参数。

### 6. I2cPinMode

**描述**: This container includes the configuration parameters to switch the SCL pin between Dio/I2c function.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cPortPinModeI2c
  长名称: ''
  描述: This parameter defines the symbolic define from the generated PORT files for the pin mode
      which is used for switching the pin into I2c mode.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: I2cPortPinModeDio
  长名称: ''
  描述: This parameter defines the symbolic define from the generated PORT files for the pin mode
      which is used for switching the pin into DIO mode.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. I2cDemEventParameterRefs

**描述**: This container includes the configuration of the DemEvents.

该容器没有参数。

### 8. I2cSequence

**描述**: Sequence specific configuration parameters of the I2c.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cPriority
  长名称: Priority of a sequence
  描述: This parameter specifies the priority of a sequence. Going from 0 (highest)  to 255 (lowest).
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: I2cEndNotification
  长名称: Transmission end notification
  描述: |
    This parameter specifies the transmission end notification to inform the user that a
    transmission request has been serviced.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: I2cSequenceId
  长名称: ''
  描述: This parameter specifies the Id of a I2c Sequence.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 4
  名称: I2cHandleNackAsError
  长名称: Handle missing ACK as error
  描述: |
    This parameter defines whether a NACK is handeld as error.
    
    True: NACK is handled as error (I2cErrorNotification callback is called, DEM event is reported).
    False: NACK is not handled as error (I2cEndNotification is called).
    
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: I2cErrorNotification
  长名称: Transmission error notification
  描述: This parameter specifies the transmission error notification to inform the user that a
      transmission request has failed.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. I2cChannelList

**描述**: References to channels and their order within the Sequence.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cChannelIndex
  长名称: ''
  描述: |
    This parameter specifies the position of a channel in list.
    A channel with index 0 is processed first.
    The index is incremented an the next channel is processed.
    The index shall not have gaps.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 10. I2cGeneral

**描述**: General configuration parameters of the I2c.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    
    True: Development error detection is enabled.
    False: Development error detection is disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: I2cGetStatusApi
  长名称: ''
  描述: This parameter enables/disables the function I2c_GetStatus() to get the status of a channel.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: I2cCancelApi
  长名称: ''
  描述: This parameter enables/disables the function I2c_Cancel() to cancel the transmission request
      of a sequence.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: I2cVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function I2c_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: I2cUserCallbackHeaderFile
  长名称: ''
  描述: This parameter defines header file name which will be included by the I2c.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: I2cIrqType
  长名称: ''
  描述: |
    This parameter defines the type of the generated ISR functions.
    
    I2C_ISR_VOID: void function (void)
    I2C_ISR_CAT1: CAT1 interrupt (__isr void function(void))
    I2C_ISR_CAT2: CAT2 interrupt (ISR(function))
    
    
  默认值: I2C_ISR_CAT2
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: I2cQueueDepth
  长名称: ''
  描述: This parameter specifies the depth of the queue.
  默认值: 10
  最小值: 1
  最大值: 255
- 
  序号: 8
  名称: I2cMainFunctionPeriod
  长名称: ''
  描述: This parameter specifies the main function period of the I2c in ms.
  默认值: 0.01
  最小值: 0.001
  最大值: 10
- 
  序号: 9
  名称: I2cProtectedMode
  长名称: ''
  描述: |
    This parameter specifies whether the module should use osPeripheralAccess-API (e.g. because
    memory access is restricted by MMU)  to access memory mapped registers.
    
    True: Module uses APIs provided by OS to access memory mapped registers.
    False: Module uses direct memory access to access memory mapped registers.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: I2cSafeBswChecks
  长名称: ''
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: I2cUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to I2c_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: I2cMaxHwLoopCycles
  长名称: ''
  描述: The maximum amount of HW-loops waited before a DEM-error is thrown.
  默认值: 1000
  最小值: 1
  最大值: 65534
- 
  序号: 13
  名称: I2cMcalSetAccess
  长名称: ''
  描述: |
    This function enables access to protected registers.
    
    Note: Add the dependend header file to the user defined header files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: I2cMcalClearAccess
  长名称: ''
  描述: |
    This function clears access to protected registers.
    
    Note: Add the dependend header file to the user defined header files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: I2cMcalPortSetPinMode
  长名称: ''
  描述: |
    This function changes the mode of the pin.
    
    Note: Add the dependend heade rfile to the user defined header files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: I2cMcalDioFlipChannel
  长名称: ''
  描述: |
    This function changes the channel level.
    
    Note: Add the dependend header file to the user defined header files.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: I2cUserDefinedHeaderFile
  长名称: ''
  描述: This parameter defines header file name which will be included by the I2c.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: I2cPollingMode
  长名称: ''
  描述: |
    This parameter specifies whether I2c Polling mode is used.
    When enabled:
    - Transactions are carried out without CPU interrupts.
    - User needs to call I2c_PollingModeProcessing() repeatedly after triggering the transmission
    until the end of the transmission. Repeated call needs to be in regular intervals (typ. 100us -
    2ms) depending on the platform specific I2c implementation and configured I2c transfer rate. For
    more information on regular intervals please refer to the documentation of the I2c low-level
    part and check your communication timings manually with logic analyzer.
    
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. I2cHardwareConfiguration

**描述**: This container includes the hardware specific configuration.

#### 参数列表

```yaml
- 
  序号: 1
  名称: I2cUnitBase
  长名称: ''
  描述: |
    This value specifies the hardware unit base address.
    
    Caution: An incorrect address may lead to system crash.
  默认值: 0
  最小值: 0
  最大值: 4294967296
```

