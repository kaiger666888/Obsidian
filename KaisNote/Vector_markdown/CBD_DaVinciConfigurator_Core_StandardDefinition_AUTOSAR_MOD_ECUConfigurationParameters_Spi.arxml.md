# Spi

## 模块描述

Configuration of the Spi (Serial Peripheral Interface) module.

## 容器列表

### 1. SpiDriver

**描述**: Configuration of one instance (if multiplicity is 1, it is the sole configuration) of an SPI driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiMaxChannel
  长名称: ''
  描述: This parameter contains the number of Channels configured. It will be gathered by tools during
      the configuration stage.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SpiMaxJob
  长名称: ''
  描述: Total number of Jobs configured.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: SpiMaxSequence
  长名称: ''
  描述: Total number of Sequences configured.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 2. SpiChannel

**描述**: All data needed to configure one SPI-channel

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiChannelId
  长名称: ''
  描述: SPI Channel ID, used as parameter in SPI API functions.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: SpiChannelType
  长名称: ''
  描述: Buffer usage with EB/IB channel.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: SpiDataWidth
  长名称: ''
  描述: This parameter is the width of a transmitted data unit.
  默认值: ''
  最小值: 1
  最大值: 32
- 
  序号: 4
  名称: SpiDefaultData
  长名称: ''
  描述: The default data to be transmitted when (for internal buffer or external buffer) the pointer
      passed to Spi_WriteIB (for internal buffer) or to Spi_SetupEB (for external buffer) is
      NULL.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: SpiEbMaxLength
  长名称: ''
  描述: This parameter contains the maximum size (in bytes) of data buffers in case of EB Channels and
      only.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 6
  名称: SpiIbNBuffers
  长名称: ''
  描述: This parameter contains the maximum number of data buffers in case of IB Channels and only.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 7
  名称: SpiTransferStart
  长名称: ''
  描述: This parameter defines the first starting bit for transmission.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. SpiDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 4. SpiExternalDevice

**描述**: The communication settings of an external device. Closely linked to SpiJob.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiBaudrate
  长名称: ''
  描述: This parameter is the communication baudrate - This parameter allows
  默认值: ''
  最小值: 0
  最大值: Inf
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
  默认值: ''
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
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SpiEnableCs
  长名称: ''
  描述: This parameter enables or not the Chip Select handling functions. If this parameter is enabled
      then parameter SpiCsSelection further details the type of chip selection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: SpiHwUnit
  长名称: ''
  描述: This parameter is the symbolic name to identify the HW SPI Hardware
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SpiShiftClockIdleLevel
  长名称: ''
  描述: This parameter defines the SPI shift clock idle level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: SpiTimeClk2Cs
  长名称: ''
  描述: Timing between clock and chip select (in seconds) - This parameter allows to use a range of
      values from 0 up to 0.0001 seconds.
  默认值: ''
  最小值: 0
  最大值: 1E-4
```

### 5. SpiJob

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
  默认值: ''
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
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: SpiJobPriority
  长名称: ''
  描述: Priority set accordingly to SPI093: 0, lowest, 3, highest priority
  默认值: ''
  最小值: 0
  最大值: 3
```

### 6. SpiChannelList

**描述**: References to SPI channels and their order within the Job.

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiChannelIndex
  长名称: ''
  描述: This parameter specifies the order of Channels within the Job.
  默认值: ''
  最小值: 0
  最大值: 255
```

### 7. SpiSequence

**描述**: All data needed to configure one SPI-sequence

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiInterruptibleSequence
  长名称: ''
  描述: This parameter allows or not this Sequence to be suspended by another one.
  默认值: ''
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
  默认值: ''
  最小值: 0
  最大值: 255
```

### 8. SpiGeneral

**描述**: General configuration settings for SPI-Handler

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiCancelApi
  长名称: ''
  描述: Switches the Spi_Cancel function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: SpiChannelBuffersAllowed
  长名称: ''
  描述: Selects the SPI Handler/Driver Channel Buffers usage allowed and
  默认值: ''
  最小值: 0
  最大值: 2
- 
  序号: 3
  名称: SpiDevErrorDetect
  长名称: ''
  描述: Switches the Development Error Detection and Notification ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: SpiHwStatusApi
  长名称: ''
  描述: Switches the Spi_GetHWUnitStatus function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: SpiInterruptibleSeqAllowed
  长名称: ''
  描述: Switches the Interruptible Sequences handling functionality ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: SpiLevelDelivered
  长名称: ''
  描述: Selects the SPI Handler/Driver level of scalable functionality that is
  默认值: ''
  最小值: 0
  最大值: 2
- 
  序号: 7
  名称: SpiSupportConcurrentSyncTransmit
  长名称: ''
  描述: Specifies whether concurrent Spi_SyncTransmit() calls for different sequences shall be
      configurable.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: SpiVersionInfoApi
  长名称: ''
  描述: Switches the Spi_GetVersionInfo function ON or OFF.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. SpiPublishedInformation

**描述**: Container holding all SPI specific published information parameters

#### 参数列表

```yaml
- 
  序号: 1
  名称: SpiMaxHwUnit
  长名称: ''
  描述: Number of different SPI hardware microcontroller peripherals (units/busses) available and
      handled by this SPI Handler/Driver module.
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
```

