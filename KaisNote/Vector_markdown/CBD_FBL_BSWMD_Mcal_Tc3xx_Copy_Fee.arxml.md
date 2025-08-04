# Fee

## 模块描述

Configuration of the Fee (Flash EEPROM Emulation) module.

## 容器列表

### 1. FeeBlockConfiguration

**描述**: Configuration of block specific parameters for the Flash EEPROM Emulation module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeBlockNumber
  长名称: ''
  描述: Block identifier (handle).
  默认值: 1
  最小值: 1
  最大值: 65534
- 
  序号: 2
  名称: FeeQsBlockInstances
  长名称: ''
  描述: number of Block instances (handle).
  默认值: 0
  最小值: 0
  最大值: 256
- 
  序号: 3
  名称: FeeQsBlockAddress
  长名称: ''
  描述: Block address in DFlash (handle).
  默认值: 0
  最小值: 0
  最大值: 1048575
- 
  序号: 4
  名称: FeeQuasiStaticManager
  长名称: ''
  描述: Indicates whether the Block configures is for NVM or Quasi static data Manager.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FeeBlockSize
  长名称: ''
  描述: Size of a logical block in bytes.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 6
  名称: FeeImmediateData
  长名称: ''
  描述: Marker for high priority data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FeeNumberOfWriteCycles
  长名称: ''
  描述: Number of write cycles required for this block.
  默认值: 0
  最小值: 0
  最大值: 16777215
```

### 2. FeeGeneral

**描述**: Container for general parameters. These parameters are not specific to a block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeDevErrorDetect
  长名称: ''
  描述: Switches the Default Error Tracer (Det) detection and notification ON or OFF.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FeeSafetyEnable
  长名称: ''
  描述: This parameter enables the user to avail the functionality to detect and report the safety
      errors.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FeeInitCheckApi
  长名称: ''
  描述: This parameter enables the user to avail the functionality to check if FEE initialisation is
      proper.                            true: Fee_17_InitCheck() API is enabled for use.
      false: Fee_17_InitCheck() API is disabled for use.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FeeMainFunctionPeriod
  长名称: ''
  描述: The period between successive calls to the main function in seconds.
  默认值: 0.01
  最小值: 0.001
  最大值: 1.0
- 
  序号: 5
  名称: FeeNvmJobEndNotification
  长名称: ''
  描述: Mapped to the job end notification routine provided by the upper layer module
      (NvM_JobEndNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FeeNvmJobErrorNotification
  长名称: ''
  描述: Mapped to the job error notification routine provided by the upper layer module
      (NvM_JobErrorNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FeeQsJobEndNotification
  长名称: ''
  描述: Mapped to the job end notification routine provided by the upper layer module
      (Qs_JobEndNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FeeQsJobErrorNotification
  长名称: ''
  描述: Mapped to the job error notification routine provided by the upper layer module
      (Qs_JobErrorNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FeePollingMode
  长名称: ''
  描述: Pre-processor switch to enable and disable the polling mode for this module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FeeSetModeSupported
  长名称: ''
  描述: Compiler switch to enable/disable the 'SetMode' functionality of the FEE module.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FeeVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FeeVirtualPageSize
  长名称: ''
  描述: The size in bytes to which logical blocks shall be aligned.
  默认值: 8
  最小值: 8
  最大值: 8
- 
  序号: 13
  名称: FeeBlockTypeConfigured
  长名称: ''
  描述: This parameter is used to configure the type of Blocks configured
  默认值: FEE_DOUBLE_SECTOR_DATA_ONLY
  最小值: ''
  最大值: ''
```

### 3. FeePublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeBlockOverhead
  长名称: ''
  描述: Management overhead per logical block in bytes. The actual overhead per block is calculated
      as:     (i) If ((FeeBlockSize % 7) == 0): FeeBlockOverhead = ((FeeBlockSize / 7) * 8) +
      16 - FeeBlockSize.     (ii)If ((FeeBlockSize % 7) != 0): FeeBlockOverhead =
      (((FeeBlockSize / 7) + 1) * 8) + 16 - FeeBlockSize.     Note: Integer arithmetic is used
      in the above calculation.
  默认值: 17
  最小值: 17
  最大值: 17
- 
  序号: 2
  名称: FeePageOverhead
  长名称: ''
  描述: Block management overhead per page in bytes.     Note: This value is applicable only for the
      pages containing logical block data bytes (i.e., it is not applicable for the pages
      which contain only implementation specific management data).
  默认值: 1
  最小值: 1
  最大值: 1
```

### 4. FeeIfxSpecificConfig

**描述**: This container has IFX specific parameters required for the working of FEE

#### 参数列表

```yaml
- 
  序号: 1
  名称: FeeThresholdValue
  长名称: ''
  描述: This parameter describes the threshold value (in bytes from the end of FEE sector) for
      triggering garbage collection/sector change.
  默认值: 200
  最小值: 0
  最大值: 523240
- 
  序号: 2
  名称: FeeMaxBlockCount
  长名称: ''
  描述: This configuration parameter specifies the total number of blocks throughout all
      configurations; Note that the blocks which are shared across configurations are counted
      only once.     This parameter decides the cache table size at pre-compile time. The
      cache table holds the information of both configured and un-configured blocks.
      Configuration of this parameter shall be carefully done. Higher value implies higher RAM
      area consumption for cache table. Lower value would result in loss of un-configured
      block(s) during GC (if FeeUnConfigBlkOverflowHandle is FEE_CONTINUE) or illegal state of
      FEE (if FeeUnConfigBlkOverflowHandle is FEE_STOP_AT_GC).      Example 1: Configuration
      sets having mutually exclusive blocks:     Configuration A: Number of blocks configured
      is 10.     Configuration B: Number of blocks configured is 25.     Then,
      FeeMaxBlockCount = 35.      Example 2: 5 blocks are shared/used by both Configuration A
      and Configuration B:     Configuration A: Number of blocks configured is 10.
      Configuration B: Number of blocks configured is 25.     Then, FeeMaxBlockCount = 30
      (i.e., shared blocks are counted only once).
  默认值: 1
  最小值: 1
  最大值: 21792
- 
  序号: 3
  名称: FeeUseEraseSuspend
  长名称: ''
  描述: This parameter specifies the usage of the erase suspend feature provided by the DFLASH
      hardware.     If it is configured as TRUE, then the read/write requests from the user
      are serviced during the erase operation of the GC.     If it is configured as FALSE,
      then the user request is kept pending till the erase operation is completed.     Note:
      This parameter can be true only if FlsUseEraseSuspend is true.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: FeeStateVarStructure
  长名称: ''
  描述: This parameter is the name of the structure, which would contain all the global variables of
      FEE. Using this user can allocate the space for the variables at his behest to avoid any
      possible linking problems.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: FeeUnConfigBlock
  长名称: ''
  描述: This parameter is used to configure if unconfigured blocks should be copied or not during GC
      operation
  默认值: FEE_UNCONFIG_BLOCK_IGNORE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: FeeUnConfigBlkOverflowHandle
  长名称: ''
  描述: This parameter is used to configure the behavior of FEE upon detection of overflow of number
      of unconfigured blocks.     FEE_CONTINUE: Un-configured blocks which could not be
      accommodated in the cache table, will be lost after the GC. FEE will continue as
      expected for the currently active configuration.     FEE_STOP_AT_GC: During GC, FEE will
      enter a pseudo illegal state where only read is allowed but write is not allowed.
  默认值: FEE_CONTINUE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: FeeGcRestart
  长名称: ''
  描述: This parameter is used to configure Garbage Collection restarting point.
      FEE_GC_RESTART_INIT: (if GC was interrupted in previous run) Restart GC after FEE
      Initialization. Hence, internal activities like repairing state pages, building lookup
      table are done after Fee_Init is called.     FEE_GC_RESTART_WRITE: (if GC was
      interrupted in previous run) Restart GC when the first read/write/invalidate request is
      issued. Also, other internal activities like repairing state pages, building lookup
      table are done only after the first Read/write/invalidate request is issued
  默认值: FEE_GC_RESTART_INIT
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: FeeGetCycleCountApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to get the block cycle count and erase cycle
      count.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: FeeEraseAllEnable
  长名称: ''
  描述: This parameter allows the user to configure if the sectors should be erased when FEE reaches
      an illegal state.     TRUE: An erase all (DF_EEPROM Erase and Format) is performed. In
      such a case FEE shall resume back to normal state but previous data (if any) cannot be
      recovered.     FALSE: FEE settles in the illegal state and cannot continue normally.
      However, data is kept intact in DF_EEPROM and may be recovered.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: FeeGetPrevDataApi
  长名称: ''
  描述: This parameter allows the user to read old copy (one instance old) of the required block.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: FeeCancelAllApi
  长名称: ''
  描述: This parameter allows the user to enable cancelling ongoing operation to write high priority
      quasi static data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: FeeMaxBytesPerCycle
  长名称: ''
  描述: This parameter allows user to configure maximum number of bytes to be processed in one FEE
      MAIN Function cycle.                       The value is including the extra FEE overhead
      like header, consecutive page id etc
  默认值: FEE_MAX_BYTES_512
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: FeeNvmIllegalStateNotification
  长名称: ''
  描述: This parameter is a pointer to a notification API which is called when Fee (NVM part) reaches
      an Illegal state. Illegal state here means that FEE is not able to proceed and user
      should do a power-on reset.                 Illegal notification can also be raised due
      to HW errors during FEE's internal activities like GC, Initialisation of GC
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: FeeQsIllegalStateNotification
  长名称: ''
  描述: This parameter is a pointer to a notification API which is called when Fee (QS part) reaches
      an Illegal state.                 Illegal notification is raised If QS area happens to
      be in virgin state and FeeVirginFlashIllegalState is not set
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: FeeQsHardenErrorNotification
  长名称: ''
  描述: This is a pointer to a notification API which is called by Fee when an error is encountered
      while performing hardening operation.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: FeeVirginFlashIllegalState
  长名称: ''
  描述: This parameter enables FEE to reach illegal state upon detection of virgin flash (DF_EEPROM).
      TRUE: Upon detection of virgin flash (DF_EEPROM) - FEE reaches illegal state and calls
      the configured illegal state notification function.               FALSE: Upon detection
      of virgin flash (DF_EEPROM) - FEE programs the initial state pages and will be available
      for user requests.
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. FeeDemEventParameterRefs

**描述**: This container contains the references to DemEventParameter elements.

该容器没有参数。

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
  默认值: 21
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

