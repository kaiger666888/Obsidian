# Fls

## 模块描述

Configuration of the Fls (internal or external flash driver) module.

## 容器列表

### 1. FlsConfigSet

**描述**: Container for runtime configuration parameters of the flash driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsAcErase
  长名称: ''
  描述: Address offset in RAM to which the erase flash access code shall be loaded.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FlsAcWrite
  长名称: ''
  描述: Address offset in RAM to which the write flash access code shall be loaded.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsCallCycle
  长名称: ''
  描述: Cycle time of calls of the flash driver's main function (in seconds).
  默认值: ''
  最小值: 0
  最大值: 1
- 
  序号: 4
  名称: FlsDefaultMode
  长名称: ''
  描述: This parameter is the default FLS device mode after initialization.
  默认值: MEMIF_MODE_SLOW
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FlsJobEndNotification
  长名称: ''
  描述: Mapped to the job end notification routine provided by some upper layer module, typically the
      Fee module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FlsJobErrorNotification
  长名称: ''
  描述: Mapped to the job error notification routine provided by some upper layer module, typically
      the Fee module.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FlsMaxReadFastMode
  长名称: ''
  描述: The maximum number of bytes to read or compare in one cycle of the flash driver's job
      processing function in fast mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: FlsMaxReadNormalMode
  长名称: ''
  描述: The maximum number of bytes to read or compare in one cycle of the flash driver's job
      processing function in normal mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: FlsMaxWriteFastMode
  长名称: ''
  描述: The maximum number of bytes to write in one cycle of the flash driver's job processing
      function in fast mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 10
  名称: FlsMaxWriteNormalMode
  长名称: ''
  描述: The maximum number of bytes to write in one cycle of the flash driver's job processing
      function in normal mode.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 11
  名称: FlsProtection
  长名称: ''
  描述: Erase/write protection settings. Only relevant if supported by hardware.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 2. FlsDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

### 3. FlsExternalDriver

**描述**: This container is present for external Flash drivers only. Internal Flash drivers do not use the
parameter listed in this container, hence its multiplicity is 0 for internal drivers.

该容器没有参数。

### 4. FlsSectorList

**描述**: List of flashable sectors and pages.

该容器没有参数。

### 5. FlsSector

**描述**: Configuration description of a flashable sector

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsNumberOfSectors
  长名称: ''
  描述: Number of continuous sectors with identical values for FlsSectorSize and
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: FlsPageSize
  长名称: ''
  描述: Size of one page of this sector.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsSectorSize
  长名称: ''
  描述: Size of this sector.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsSectorStartaddress
  长名称: ''
  描述: Start address of this sector.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

### 6. FlsGeneral

**描述**: Container for general parameters of the flash driver. These parameters are always pre-compile.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsAcLoadOnJobStart
  长名称: ''
  描述: The flash driver shall load the flash access code to RAM whenever an erase or write job is
      started and unload (overwrite) it after that job has been finished or canceled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FlsBaseAddress
  长名称: ''
  描述: The flash memory start address (see also FLS208 and FLS209).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsCancelApi
  长名称: ''
  描述: Compile switch to enable and disable the Fls_Cancel function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FlsCompareApi
  长名称: ''
  描述: Compile switch to enable and disable the Fls_Compare function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FlsDevErrorDetect
  长名称: ''
  描述: Pre-processor switch to enable and disable development error detection (see FLS077).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FlsDriverIndex
  长名称: ''
  描述: Index of the driver, used by FEE.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 7
  名称: FlsGetJobResultApi
  长名称: ''
  描述: Compile switch to enable and disable the Fls_GetJobResult function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FlsGetStatusApi
  长名称: ''
  描述: Compile switch to enable and disable the Fls_GetStatus function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FlsSetModeApi
  长名称: ''
  描述: Compile switch to enable and disable the Fls_SetMode function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FlsTotalSize
  长名称: ''
  描述: The total amount of flash memory in bytes (see also FLS208 and FLS209).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 11
  名称: FlsUseInterrupts
  长名称: ''
  描述: Job processing triggered by hardware interrupt.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FlsVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. FlsPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FlsAcLocationErase
  长名称: ''
  描述: Position in RAM, to which the erase flash access code has to be loaded.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FlsAcLocationWrite
  长名称: ''
  描述: Position in RAM, to which the write flash access code has to be loaded.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FlsAcSizeErase
  长名称: ''
  描述: Number of bytes in RAM needed for the erase flash access code.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FlsAcSizeWrite
  长名称: ''
  描述: Number of bytes in RAM needed for the write flash access code.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: FlsEraseTime
  长名称: ''
  描述: Maximum time to erase one complete flash sector.
  默认值: ''
  最小值: 0
  最大值: Inf
- 
  序号: 6
  名称: FlsErasedValue
  长名称: ''
  描述: The contents of an erased flash memory cell.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: FlsExpectedHwId
  长名称: ''
  描述: Unique identifier of the hardware device that is expected by this driver (the device for which
      this driver has been implemented).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FlsSpecifiedEraseCycles
  长名称: ''
  描述: Number of erase cycles specified for the flash device (usually given in the device data
      sheet).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 9
  名称: FlsWriteTime
  长名称: ''
  描述: Maximum time to program one complete flash page.
  默认值: ''
  最小值: 0
  最大值: Inf
```

