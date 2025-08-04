# Spi

## 模块描述

Configuration of the Spi (Serial Peripheral Interface) module.

## 容器列表

### 1. SpiDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 2. SpiDriver

**描述**: This container contains the configuration parameters and sub containers of the AUTOSAR Spi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiMaxChannel
  长名称: ''
  描述: This parameter contains the number of Channels configured. It will be gathered by tools during
      the configuration stage. Note: this parameter should be Removed and Added after the
      SpiChannel configuration is completed(Since, tool does not auto-refresh the default
      value)
  默认值: 1
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SpiMaxJob
  长名称: ''
  描述: Total number of Jobs configured. It will be gathered by tools during the configuration stage.
      Note: this parameter should be Removed and Added after the SpiJob configuration is
      completed(Since, tool does not auto-refresh the default value)
  默认值: 1
  最小值: 1
  最大值: 5000
- 
  序号: 3
  名称: SpiMaxSequence
  长名称: ''
  描述: Total number of Sequences configured. It will be gathered by tools during the configuration
      stage. Note: this parameter should be Removed and Added after the SpiSequence
      configuration is completed(Since, tool does not auto-refresh the default value)
  默认值: 1
  最小值: 0
  最大值: 255
```

### 3. SpiChannel

**描述**: All data needed to configure one SPI-channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiChannelId
  长名称: ''
  描述: SPI Channel ID, used as parameter in SPI API functions. It is published in the Spi_Cfg.h file
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SpiChannelType
  长名称: ''
  描述: Buffer usage with EB/IB channel.
  默认值: EB
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SpiDataWidth
  长名称: ''
  描述: This parameter is the width of a transmitted data unit.
  默认值: 8
  最小值: 2
  最大值: 32
- 
  序号: 4
  名称: SpiDefaultData
  长名称: ''
  描述: The default data to be transmitted when (for internal buffer or external buffer) the pointer
      passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is
      NULL.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: SpiEbMaxLength
  长名称: ''
  描述: This parameter contains the maximum size (number of data elements) of data buffers in case of
      EB Channels and only.
  默认值: 8190
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: SpiIbNBuffers
  长名称: ''
  描述: This parameter contains the maximum number of data buffers in case of IB Channels and only.
  默认值: 10
  最小值: 1
  最大值: 65535
- 
  序号: 7
  名称: SpiTransferStart
  长名称: ''
  描述: This parameter defines the first starting bit for transmission.
  默认值: LSB
  最小值: ''
  最大值: ''
```

### 4. SpiExternalDevice

**描述**: The communication settings of an external device. Closely linked to SpiJob.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiBaudrate
  长名称: ''
  描述: This parameter is the communication baudrate - This parameter allows
  默认值: 640000.0
  最小值: 9600.0
  最大值: 5.0E7
- 
  序号: 2
  名称: SpiCsIdentifier
  长名称: ''
  描述: This parameter is the symbolic name to identify the Chip Select (CS) allocated to this Job.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SpiCsPolarity
  长名称: ''
  描述: This parameter defines the active polarity of Chip Select.
  默认值: LOW
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SpiCsSelection
  长名称: ''
  描述: When the Chip select handling is enabled (see SpiEnableCs), then this parameter specifies if
      the chip select is handled automatically by Peripheral HW engine or via general purpose
      IO by Spi driver.
  默认值: CS_VIA_PERIPHERAL_ENGINE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SpiDataShiftEdge
  长名称: ''
  描述: This parameter defines the SPI data shift edge.
  默认值: LEADING
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SpiEnableCs
  长名称: ''
  描述: This parameter enables or not the Chip Select handling functions. If this parameter is enabled
      then parameter SpiCsSelection further details the type of chip selection.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SpiHwUnit
  长名称: ''
  描述: This parameter is the symbolic name to identify the HW SPI Hardware
  默认值: QSPI0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SpiAutoCalcBaudParams
  长名称: ''
  描述: This parameter enables or not the automatic calculation of qspi baudrate parameters.  If this
      value is ON, then the Hw parameters TQ,Q,A,B,C are calculated based on SpiBaudrate
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SpiAutoCalcDelayParams
  长名称: ''
  描述: This parameter enables or not the automatic calculation of qspi Delay parameters.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SpiIdleTime
  长名称: ''
  描述: IDLEA / IDLEB Time .
  默认值: 0.0000001
  最小值: 4.0E-8
  最大值: 0.098304
- 
  序号: 11
  名称: SpiTrailingTime
  长名称: ''
  描述: Trailing Time - the time between the last edge of the clock and the CS De-assertion. It is
      also the time between the data elements in the SpiChannel
  默认值: 0.0000001
  最小值: 4.0E-8
  最大值: 0.098304
- 
  序号: 12
  名称: SpiShiftClockIdleLevel
  长名称: ''
  描述: This parameter defines the SPI shift clock idle level.
  默认值: LOW
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: SpiTimeClk2Cs
  长名称: ''
  描述: Timing between clock and chip select (in seconds) or the Lead time - This parameter allows to
      use a range of values from 0 up to 0.0001 seconds.
  默认值: 0.0000001
  最小值: 4.0E-8
  最大值: 1.0E-4
- 
  序号: 14
  名称: SpiParitySupport
  长名称: ''
  描述: When the SpiParitySupport is selected SPI data Transmission/Reception incorporates an
      additional bit making the parity EVEN or ODD based on selection
  默认值: UNUSED
  最小值: ''
  最大值: ''
```

### 5. SpiCsGpio

**描述**: Container for the selection of Chipselect

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiCsGpioPortSelection
  长名称: ''
  描述: Gpio port no used for Chipselect
  默认值: 1
  最小值: 0
  最大值: 41
- 
  序号: 2
  名称: SpiCsGpioPinSelection
  长名称: ''
  描述: Gpio port pin no used for Chipselect
  默认值: 1
  最小值: 0
  最大值: 15
```

### 6. SpiBaudrateParams

**描述**: This container has the parameters which are responsible for the Baudrate

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiBaudParamTQ
  长名称: ''
  描述: This parameter defines Global time quantum value, Qspi TQ Hw parameter. If
      SpiAutoCalcBaudParams value is ON, then the HW baudrate parameters TQ,Q,A,B,C are
      calculated based on SpiBaudrate
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SpiBaudParamQ
  长名称: ''
  描述: This parameter defines Qspi Q Hw parameter
  默认值: 10
  最小值: 0
  最大值: 63
- 
  序号: 3
  名称: SpiBaudParamA
  长名称: ''
  描述: This parameter defines one of the bit segment A in a period, Qspi A Hw parameter
  默认值: 1
  最小值: 0
  最大值: 3
- 
  序号: 4
  名称: SpiBaudParamB
  长名称: ''
  描述: Qspi B Hw parameter
  默认值: 0
  最小值: 0
  最大值: 3
- 
  序号: 5
  名称: SpiBaudParamC
  长名称: ''
  描述: Qspi C Hw parameter
  默认值: 1
  最小值: 0
  最大值: 3
```

### 7. SpiDelayParams

**描述**: THis container has the parameters which are responsible for the delay configuration during
transmission

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiDelayParamTrailPre
  长名称: ''
  描述: Qspi Trail delay prescalar Hw parameter
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 2
  名称: SpiDelayParamTrailLength
  长名称: ''
  描述: Qspi Trail Hw parameter
  默认值: 5
  最小值: 0
  最大值: 7
- 
  序号: 3
  名称: SpiDelayParamIdlePre
  长名称: ''
  描述: Qspi Idle delay prescalar Hw parameter
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 4
  名称: SpiDelayParamIdleLength
  长名称: ''
  描述: Qspi IDLE delay Hw parameter
  默认值: 1
  最小值: 0
  最大值: 7
- 
  序号: 5
  名称: SpiDelayParamLeadPre
  长名称: ''
  描述: Qspi Lead delay prescalar Hw parameter
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 6
  名称: SpiDelayParamLeadLength
  长名称: ''
  描述: Qspi LEAD delay Hw parameter
  默认值: 7
  最小值: 0
  最大值: 7
```

### 8. SpiJob

**描述**: All data needed to configure one SPI-Job, amongst others the connection between the internal SPI
unit and the special settings for an external device is done.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiHwUnitSynchronous
  长名称: ''
  描述: If SpiHwUnitSynchronous is set to "SYNCHRONOUS", the SpiJob uses its containing SpiDriver in a
      synchronous manner. If it is set to "ASYNCHRONOUS", it uses the driver in an
      asynchronous way. If the parameter is not set, the SpiChannel uses the driver also in an
      asynchronous way.
  默认值: ASYNCHRONOUS
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SpiJobEndNotification
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SpiJobId
  长名称: ''
  描述: SPI Job ID, used as parameter in SPI API functions.
  默认值: 0
  最小值: 0
  最大值: 5000
- 
  序号: 4
  名称: SpiFrameBasedCS
  长名称: ''
  描述: enable frame based chip select
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SpiJobPriority
  长名称: ''
  描述: Priority set accordingly to SPI093: 0, lowest, 3, highest priority
  默认值: 0
  最小值: 0
  最大值: 3
```

### 9. SpiChannelList

**描述**: References to SPI channels and their order within the Job.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiChannelIndex
  长名称: ''
  描述: This parameter specifies the order of Channels within the Job.
  默认值: 0
  最小值: 0
  最大值: 254
```

### 10. SpiSequence

**描述**: All data needed to configure one SPI-sequence

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiInterruptibleSequence
  长名称: ''
  描述: This parameter allows or not this Sequence to be suspended by another one.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SpiSeqEndNotification
  长名称: ''
  描述: This parameter is a reference to a notification function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SpiSequenceId
  长名称: ''
  描述: SPI Sequence ID, used as parameter in SPI API functions.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 11. SpiGeneral

**描述**: General configuration settings for SPI-Handler

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiCancelApi
  长名称: ''
  描述: Switches the Spi_Cancel function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SpiChannelBuffersAllowed
  长名称: ''
  描述: Selects the SPI Handler/Driver Channel Buffers usage 0 - IB (Internal Buffer), 1 - EB
      (External Buffer), 2 - Both
  默认值: 1
  最小值: 0
  最大值: 2
- 
  序号: 3
  名称: SpiInitDeInitApiMode
  长名称: ''
  描述: This parameter selects the operating modes for MCU initialization, de-initialization APIs
  默认值: SPI_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SpiInitCheckApi
  长名称: ''
  描述: This parameter enables init checks for APIs
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SpiMulticoreCheckEnable
  长名称: ''
  描述: This parameter disables multicore configuration checks
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SpiRuntimeApiMode
  长名称: ''
  描述: This parameter selects the operating modes for SPI runtime APIs
  默认值: SPI_MCAL_SUPERVISOR
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SpiDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SpiSafetyCheckEnable
  长名称: ''
  描述: Switches the Default safety check for QSPI ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SpiHwStatusApi
  长名称: ''
  描述: Switches the Spi_GetHWUnitStatus function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: SpiInterruptibleSeqAllowed
  长名称: ''
  描述: Switches the Interruptible Sequences handling functionality ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: SpiLevelDelivered
  长名称: ''
  描述: Selects the SPI Handler/Driver level of scalable functionality that is
      available and delivered.                            SpiLevelDelivered is 0(LEVEL0): The
      driver handles only simple synchronous transmission on all available SPI busses(QSPIx)
      SpiLevelDelivered is 1(LEVEL1): The driver handles only simple asynchronous transmission
      on all available SPI busses(QSPIx)                            SpiLevelDelivered is
      2(LEVEL2): The LEVEL2 which is an enhanced behavior of the driver will handle both
      synchronous and asynchronous                            transmissions.
  默认值: 1
  最小值: 0
  最大值: 2
- 
  序号: 12
  名称: SpiMainFunctionPeriod
  长名称: ''
  描述: This parameter defines the cycle time of the function Spi_MainFunction_Handling in seconds.
      The parameter is not used by the driver it self, but it is used by upper layer.
  默认值: 0.01
  最小值: 1.0E-7
  最大值: 1.0
- 
  序号: 13
  名称: SpiSupportConcurrentSyncTransmit
  长名称: ''
  描述: Specifies whether concurrent Spi_SyncTransmit() calls for different sequences shall be
      configurable.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: SpiSyncTransmitTimeoutDuration
  长名称: ''
  描述: The parameter is used as timeout loop counter while waiting for data transmission/reception of
      1 data element.
  默认值: 65535
  最小值: 100
  最大值: 4294967295
- 
  序号: 15
  名称: SpiUserCallbackHeaderFile
  长名称: ''
  描述: Header file name which will be included by the Spi. The value of this parameter shall be used
      as q-char-sequence according to ISO C90 section 6.10.2 "source file inclusion". The
      parameter value MUST NOT represent a path, since ISO C90 does not specify how such a
      path is treated (i.e., this is implementation defined (and additionally depends on the
      operating system and the underlying file system)).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: SpiVersionInfoApi
  长名称: ''
  描述: Switches the Spi_GetVersionInfo function ON or OFF.
  默认值: false
  最小值: ''
  最大值: ''
```

### 12. SpiHwConfiguration

**描述**: This container has the QSPI specific configuration which is PC type

该容器没有参数。

### 13. SpiHwConfigurationQspi

**描述**: Container for the SpiHwConfigurationQspix

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiHwConfigKernel
  长名称: ''
  描述: This parameter is the symbolic name to identify the Kernel ID configuration
  默认值: QSPI0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SpiJobQueueLengthQspix
  长名称: ''
  描述: The parameter is used to specify the Job Queue size. The size should be chosen properly so as
      to accommodate the runtime Sequence transmission requests. Note: in SpiLevelDelivered =
      2, if the HW is Synchronous, configuring this parameter should be ignored and default
      value could be kept.
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SpiSleepEnableQspix
  长名称: ''
  描述: To control QSPIx sleep mode
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SpiHWPinMRSTQspix
  长名称: ''
  描述: Port Pin selection for Master_Receive_Slave_Transmit
  默认值: MRST0A_PORT20_PIN12
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SpiExternalDemux
  长名称: ''
  描述: This parameter enables/disables the external demultiplexer feature of QSPI HW
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SpiSLSO0StrobeDelay
  长名称: ''
  描述: The parameter is used to specify the Strobe delay to be configured for SLSO0 in External
      Demultiplexer mode
  默认值: 2
  最小值: 2
  最大值: 31
```

### 14. SpiHwDmaConfigurationQspi

**描述**: Spi DMA Configuration For QSPI node

该容器没有参数。

### 15. SpiPublishedInformation

**描述**: Container holding all SPI specific published information parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiMaxHwUnit
  长名称: ''
  描述: Number of different SPI hardware microcontroller peripherals (units/busses) available and
      handled by this SPI Handler/Driver module.
  默认值: 6
  最小值: 0
  最大值: 6
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
  默认值: 83
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

