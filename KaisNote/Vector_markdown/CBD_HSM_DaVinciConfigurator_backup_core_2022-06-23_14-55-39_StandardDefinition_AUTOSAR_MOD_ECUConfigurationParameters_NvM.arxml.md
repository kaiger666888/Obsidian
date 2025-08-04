# NvM

## 模块描述

Configuration of the NvM (NvRam Manager) module.

## 容器列表

### 1. NvMBlockDescriptor

**描述**: Container for a management structure to configure the composition of a given NVRAM Block Management
Type. Its multiplicity describes the number of configured NVRAM blocks, one block is required to be
configured. The NVRAM block descriptors are condensed in the NVRAM block descriptor table.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NvMBlockCrcType
  长名称: ''
  描述: Defines CRC data width for the NVRAM block. Default: NVM_CRC16, i.e. CRC16 will be used  if
      NVM_BLOCK_USE_CRC==true
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NvMBlockJobPriority
  长名称: ''
  描述: Defines the job priority for a NVRAM block (0 = Immediate priority).
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: NvMBlockManagementType
  长名称: ''
  描述: Defines the block management type for the NVRAM block.[NVM137]
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NvMBlockUseCrc
  长名称: ''
  描述: Defines CRC usage for the NVRAM block, i.e. memory space for CRC is reserved in RAM and NV
      memory.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NvMBlockUseSyncMechanism
  长名称: ''
  描述: Defines whether an explicit synchronization mechanism with a RAM mirror and callback routiness
      for transferring data to and from NvM module's RAM mirror is used for NV block. true if
      synchronization mechanism is used, false otherwise.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NvMBlockWriteProt
  长名称: ''
  描述: Defines an initial write protection of the NV block
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NvMBswMBlockStatusInformation
  长名称: ''
  描述: This parameter specifies whether BswM is informed about the current status of the specified
      block.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NvMCalcRamBlockCrc
  长名称: ''
  描述: Defines CRC (re)calculation for the permanent RAM block
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NvMInitBlockCallback
  长名称: ''
  描述: Entry address of a block specific callback routine which shall be called if no ROM data is
      available for initialization of the NVRAM block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NvMMaxNumOfReadRetries
  长名称: ''
  描述: Defines the maximum number of read retries.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 11
  名称: NvMMaxNumOfWriteRetries
  长名称: ''
  描述: Defines the maximum number of write retries for a NVRAM block with [NVM061_Conf]. Regardless
      of configuration a consistency check (and maybe write retries) are always forced for
      each block which is processed by the request NvM_WriteAll and NvM_WriteBlock.
  默认值: ''
  最小值: 0
  最大值: 7
- 
  序号: 12
  名称: NvMNvBlockBaseNumber
  长名称: ''
  描述: Configuration parameter to perform the link between the NVM_NVRAM_BLOCK_IDENTIFIER used by the
      SW-Cs and the FEE_BLOCK_NUMBER expected by the memory abstraction modules. The parameter
      value equals the FEE_BLOCK_NUMBER or EA_BLOCK_NUMBER shifted to the right by
      NvMDatasetSelectionBits bits. (ref. to chapter 7.1.2.1).
  默认值: ''
  最小值: 1
  最大值: 65534
- 
  序号: 13
  名称: NvMNvBlockLength
  长名称: ''
  描述: Defines the NV block data length in bytes.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 14
  名称: NvMNvBlockNum
  长名称: ''
  描述: Defines the number of multiple NV blocks in a contiguous area according to the given block
      management type.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: NvMNvramBlockIdentifier
  长名称: ''
  描述: Identification of a NVRAM block via a unique block identifier.
  默认值: ''
  最小值: 2
  最大值: 65535
- 
  序号: 16
  名称: NvMNvramDeviceId
  长名称: ''
  描述: Defines the NVRAM device ID where the NVRAM block is located.
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 17
  名称: NvMRamBlockDataAddress
  长名称: ''
  描述: Defines the start address of the RAM block data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: NvMReadRamBlockFromNvCallback
  长名称: ''
  描述: Entry address of a block specific callback routine which shall be called in order to let the
      application copy data from the NvM module's mirror to RAM block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: NvMResistantToChangedSw
  长名称: ''
  描述: Defines whether a NVRAM block shall be treated resistant to configuration changes or not. If
      there is no default data available at configuration time then the application shall be
      responsible for providing the default initialization data. In this case the application
      has to use NvM_GetErrorStatus()to be able to distinguish between first initialization
      and corrupted data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: NvMRomBlockDataAddress
  长名称: ''
  描述: Defines the start address of the ROM block data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: NvMRomBlockNum
  长名称: ''
  描述: Defines the number of multiple ROM blocks in a contiguous area according to the given block
      management type.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: NvMSelectBlockForReadAll
  长名称: ''
  描述: NVM117: Defines whether a NVRAM block shall be processed during NvM_ReadAll or not. This
      configuration parameter has only influence on those NVRAM blocks which are configured to
      have a permanent RAM block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: NvMSelectBlockForWriteAll
  长名称: ''
  描述: Defines whether a NVRAM block shall be processed during NvM_WriteAll or not. This
      configuration parameter has only influence on those NVRAM blocks which are configured to
      have a permanent RAM block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: NvMSingleBlockCallback
  长名称: ''
  描述: Entry address of the block specific callback routine which shall be invoked on termination of
      each asynchronous single block request [NVM113].
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: NvMStaticBlockIDCheck
  长名称: ''
  描述: Defines if the Static Block ID check is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: NvMWriteBlockOnce
  长名称: ''
  描述: Defines write protection after first write. The NVRAM manager sets the write protection bit
      after the NV block was written the first time. This means that some of the NV blocks in
      the NVRAM should never be erased nor be replaced with the default ROM data after first
      initialization. [NVM276].
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: NvMWriteRamBlockToNvCallback
  长名称: ''
  描述: Entry address of a block specific callback routine which shall be called in order to let the
      application copy data from RAM block to NvM module's mirror.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: NvMWriteVerification
  长名称: ''
  描述: Defines if Write Verification is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: NvMWriteVerificationDataSize
  长名称: ''
  描述: Defines the number of bytes to compare in each step when comparing the content of a RAM Block
      and a block read back.
  默认值: 0
  最小值: 1
  最大值: 65536
```

### 2. NvMEaRef

**描述**: EEPROM Abstraction

该容器没有参数。

### 3. NvMFeeRef

**描述**: Flash EEPROM Emulation

该容器没有参数。

### 4. NvMCommon

**描述**: Container for common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NvMApiConfigClass
  长名称: ''
  描述: Preprocessor switch to enable some API calls which are related to NVM API configuration
      classes.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NvMBswMMultiBlockJobStatusInformation
  长名称: ''
  描述: This parameter specifies whether BswM is informed about the current status of the multiblock
      job.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NvMCompiledConfigId
  长名称: ''
  描述: Configuration ID regarding the NV memory layout. This configuration ID shall be published as
      e.g. a SW-C shall have the possibility to write it to NV memory.
  默认值: ''
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: NvMCrcNumOfBytes
  长名称: ''
  描述: If CRC is configured for at least one NVRAM block, this parameter defines the maximum number
      of bytes which shall be processed within one cycle of job processing.
  默认值: ''
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: NvMDatasetSelectionBits
  长名称: ''
  描述: Defines the number of least significant bits which shall be used to address a certain dataset
      of a NVRAM block within the interface to the memory hardware abstraction.
  默认值: ''
  最小值: 0
  最大值: 8
- 
  序号: 6
  名称: NvMDevErrorDetect
  长名称: ''
  描述: Pre-processor switch to enable and disable development error detection.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NvMDrvModeSwitch
  长名称: ''
  描述: Preprocessor switch to enable switching memory drivers to fast mode during performing
      NvM_ReadAll and NvM_WriteAll
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NvMDynamicConfiguration
  长名称: ''
  描述: Preprocessor switch to enable the dynamic configuration management handling by the NvM_ReadAll
      request.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NvMJobPrioritization
  长名称: ''
  描述: Preprocessor switch to enable job prioritization handling
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NvMMultiBlockCallback
  长名称: ''
  描述: Entry address of the common callback routine which shall be invoked on termination of each
      asynchronous multi block request
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: NvMPollingMode
  长名称: ''
  描述: Preprocessor switch to enable/disable the polling mode in the NVRAM Manager and at the same
      time disable/enable the callback functions useable by lower layers
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: NvMRepeatMirrorOperations
  长名称: ''
  描述: Defines the number of retries to let the application copy data to or from the NvM module's
      mirror before postponing the current job.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 13
  名称: NvMSetRamBlockStatusApi
  长名称: ''
  描述: Preprocessor switch to enable the API NvM_SetRamBlockStatus.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: NvMSizeImmediateJobQueue
  长名称: ''
  描述: Defines the number of queue entries for the immediate priority job queue. If
      NVM_JOB_PRIORITIZATION is switched OFF this parameter shall be out of scope.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: NvMSizeStandardJobQueue
  长名称: ''
  描述: Defines the number of queue entries for the standard job queue.
  默认值: ''
  最小值: 1
  最大值: 255
- 
  序号: 16
  名称: NvMVersionInfoApi
  长名称: ''
  描述: Pre-processor switch to enable / disable the API to read out the modules version information
      [NVM285], [NVM286].
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. NvmDemEventParameterRefs

**描述**: Container for the references to DemEventParameter elements which shall be invoked using the API
Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value. The standardized errors are provided in the
container and can be extended by vendor specific error references.

该容器没有参数。

