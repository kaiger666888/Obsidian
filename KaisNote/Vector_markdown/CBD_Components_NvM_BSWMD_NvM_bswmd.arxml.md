# NvM

## 模块描述

NV RAM Manager. Provides services to ensure the data storage and maintenance of NV data according to
their individual requirements in an automotive environment. The NvM administrates the NV data of an
EEPROM and/or a FLASH EEPROM emulation device.


#NVRAM #NVMemory #DataStorage

#AUTOSAR #ServiceComponent

## 容器列表

### 1. NvMBlockDescriptor

**描述**: This container includes the configuration of one NVM block. At least one block is required to be
configured. The NVRAM block descriptors are condensed in the NVRAM block descriptor table.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NvMBlockCrcType
  长名称: Crc Type
  描述: This parameter defines CRC data width for the NVRAM block. Hint: The parameter is only
      applicable if (NvMBlockUseCrc == true).
  默认值: NVM_CRC32
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NvMBlockJobPriority
  长名称: Priority
  描述: This value specifies the job priority for a NVRAM block (0 = Immediate priority).
  默认值: 127
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: NvMBlockManagementType
  长名称: Management Type
  描述: |
    Defines the block management type for the NVRAM block.
    NVM_BLOCK_DATASET: NVRAM  block  is configured to be of dataset type. The application has to
    decide which of the n data set is handled.
    NVM_BLOCK_NATIVE: NVRAM block is configured to be of native type. The data is stored at one
    position.
    NVM_BLOCK_REDUNDANT : NVRAM block is configured to be of redundant type. The data is stored
    twice. If reading the first element fails, the modules automatically tries to read the second
    element.
  默认值: NVM_BLOCK_NATIVE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NvMBlockUseCrc
  长名称: Crc usage
  描述: |
    This parameter defines if CRC usage for the NVRAM block is enabled.
    Hint: The type of CRC has to be configured in NvMBlockCrcType.
    Hint: If CRC is enabled, please make sure to align NvMNvBlockLength and
    NvMDataIntegrityIntBuffer
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NvMBlockUseSyncMechanism
  长名称: Use Synchronization Mechanism
  描述: |
    This parameter defines whether an explicit synchronization mechanism with a RAM mirror and
    callback routines for transferring data to and from NvM module's RAM mirror is used for this
    block.
    If used, both, NvMReadRamBlockFromNvCallback and NvMWriteRamBlockToNvCallback must be set to
    names of appropriate functions.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: NvMBlockWriteProt
  长名称: Write Protection
  描述: |
    This parameter defines the initial write protection of the NV block.
    true:   Initial block write protection is enabled.
    false:  Initial block write protection is disabled.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NvMBswMBlockStatusInformation
  长名称: Block Status Information
  描述: This parameter defines whether BswM is informed about the current status of this block.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NvMCalcRamBlockCrc
  长名称: Calculate Ram Block Crc
  描述: |
    This parameter defines CRC (re)calculation for the permanent RAM block.
    true:   CRC will be (re)calculated for this permanent RAM block.
    false:  CRC will not be (re)calculated for this permanent RAM block.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NvMInitBlockCallback
  长名称: Init Block Callback
  描述: |
    This parameter defines the block specific callback routine which shall be called if no ROM data
    is available for initialization of the NVRAM block.
    If a NULL pointer is configured, no specific callback routine shall be called for initialization
    of the NVRAM block with default data.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NvMMaxNumOfReadRetries
  长名称: Maximum number of read retries
  描述: |
    Not used!
    
    This parameter defines the maximum number of read retries.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 11
  名称: NvMMaxNumOfWriteRetries
  长名称: Maximum number of write retries
  描述: |
    Not used!
    
    This parameter defines the maximum number of write retries for a NVRAM block
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 12
  名称: NvMNvBlockBaseNumber
  长名称: Block Base Number
  描述: |
    Not Used!
    This value specifies the link between the NVM_NVRAM_BLOCK_IDENTIFIER used by the SW-Cs and the
    FEE_BLOCK_NUMBER expected by the memory abstraction modules. The parameter value equals the
    FEE_BLOCK_NUMBER or EA_BLOCK_NUMBER shifted to the right by NvMDatasetSelectionBits bits.
  默认值: ''
  最小值: 1
  最大值: 65534
- 
  序号: 13
  名称: NvMNvBlockLength
  长名称: Block Length
  描述: |
    This value defines the NV block data length in bytes.
    
    Hint: If a NvMRamBlockDataAddress or NvMRomBlockDataAddress is given for this block, the length
    given here has to match exactly the variable sizes.
    Hint: If CRC or MAC is used for this block, please check the setting of parameter
    NvMDataIntegrityIntBuffer.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 14
  名称: NvMNvBlockNum
  长名称: Datasets
  描述: |
    This value specifies the number of multiple NV blocks in a contiguous area according to the
    given block management type.
    1-255   For NVRAM blocks to be configured of block management type NVM_BLOCK_DATASET. The actual
    range is limited according to NVM148.
    
    1       For NVRAM blocks to be configured of block management type NVM_BLOCK_NATIVE
    
    2       For NVRAM blocks to be configured of block management type NVM_BLOCK_REDUNDANT
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: NvMNvramBlockIdentifier
  长名称: Block Identifier
  描述: |
    This value specifies the identification of a NVRAM block via a unique block identifier.
    Implementation Type: NvM_BlockIdType.
    
                                    min = 0
                                    max = 2^(16- NVM_DATASET_SELECTION_BITS)-1
    
    Reserved NVRAM block IDs:
    0 -> to derive multi block request results via NvM_GetErrorStatus
    1 -> redundant NVRAM block which holds the configuration ID
  默认值: 65535
  最小值: 1
  最大值: 65535
- 
  序号: 16
  名称: NvMNvramDeviceId
  长名称: Device Id
  描述: |
    Not used!
    This value specifies the NVRAM device ID where the NVRAM block is located.
    Calculation Formula:
    "value = TargetBlockReference.[Ea/Fee]BlockConfiguration.[Ea/Fee]DeviceIndex"
  默认值: ''
  最小值: 0
  最大值: 254
- 
  序号: 17
  名称: NvMRamBlockDataAddress
  长名称: Ram Block Data
  描述: |
    This parameter defines the variable name of the RAM block data.
    If a NULL pointer is configured, no permanent RAM data block is available for this block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: NvMReadRamBlockFromNvCallback
  长名称: Read Ram Block From Nv Callback
  描述: This parameter defines the block specific callback routine which shall be called in order to
      let the application copy data from the NvM module's mirror to RAM block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: NvMResistantToChangedSw
  长名称: Resistant To Changed Software
  描述: |
    This parameter defines whether a NVRAM block shall be treated resistant to configuration changes
    or not. If there is no default data available at configuration time then the application shall
    be responsible for providing the default initialization data. In this case the application has
    to use NvM_GetErrorStatus() to be able to distinguish between first initialization and corrupted
    data.
    
    This parameter is only relevant if NvMCommon/NvMDynamicConfiguration is set to True.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: NvMRomBlockDataAddress
  长名称: Rom Block Data
  描述: |
    This parameter defines the variable name of the ROM block data.
    
    If a NULL pointer is configured, no ROM block is available for this block.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: NvMRomBlockNum
  长名称: Rom Block Number
  描述: |
    Not Used!
    This value specifies the number of multiple ROM blocks in a contiguous area according to the
    given block management type.
    
    0-255   For NVRAM blocks to be configured of block management type NVM_BLOCK_DATASET. The actual
    range is limited according to NVM148.
    
    0-1     For NVRAM blocks to be configured of block management type NVM_BLOCK_NATIVE
    
    0-1     For NVRAM blocks to be configured of block management type NVM_BLOCK_REDUNDANT
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: NvMSelectBlockForReadAll
  长名称: Select Block For ReadAll
  描述: This parameter defines whether the NVRAM block shall be processed during NvM_ReadAll or not.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: NvMSelectBlockForWriteAll
  长名称: Select Block For WriteAll
  描述: This parameter defines whether the NVRAM block shall be processed during NvM_WriteAll or not.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: NvMSingleBlockCallback
  长名称: Single Block Callback
  描述: |
    This parameter defines the block specific callback routine which shall be invoked on termination
    of each asynchronous single block request.
    Does not care, if "Use Job End Callback" was disabled, or if  "Use Service Ports" was enabled
    (then the name is derived automatically).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: NvMStaticBlockIDCheck
  长名称: Static Block Id Check
  描述: |
    Not used!
    
    This parameter defines if the Static Block ID check is enabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: NvMWriteBlockOnce
  长名称: Write Block Once
  描述: This parameter defines if write protection after first write is enabled. The NVRAM manager
      sets the write protection bit after the NV block was written the first time. This means
      that some of the NV blocks in the NVRAM should never be erased nor be replaced with the
      default ROM data after first initialization.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: NvMWriteRamBlockToNvCallback
  长名称: Write Ram Block To Nv Callback
  描述: This parameter defines the block specific callback routine which shall be called in order to
      let the application copy data from RAM block to NvM module's mirror.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: NvMWriteVerification
  长名称: Write Verification
  描述: |
    Not used!
    
    This parameter defines if Write Verification is enabled.
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: NvMWriteVerificationDataSize
  长名称: Write Verification Data Size
  描述: |
    Not used!
    
    This value specifies the number of bytes to compare in each step when comparing the content of a
    RAM Block and a block read back.
  默认值: 1
  最小值: 1
  最大值: 65536
- 
  序号: 30
  名称: NvMUseServicePorts
  长名称: Use Service Ports
  描述: This parameter defines if this block is accessible via service ports. The PortName will be
      derived from the block name.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: NvMUseJobendCallback
  长名称: Use Job End Callback
  描述: |
    This parameter defines whether the block specific "Single Block Job End Notification" shall be
    invoked upon completion of block processing.
    If enabled, the name of the function must be specified in "Single Block Callback", unless "Use
    Service Ports" was enabled (then the name is derived automatically).
    
    
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: NvMUseInitCallback
  长名称: Use Init Callback
  描述: |
    This parameter defines if the configured Init Callback is used to provide default data.
    Note: Since the initialization status of the RTE during ReadAll processing is currently unclear
    (according to AUTOSAR it is not initialized), the init callback cannot be used by SW-Cs via RTE
    - the setting will be ignored.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: NvMAutomaticBlockLength
  长名称: Automatic Block Length
  描述: |
    If enabled, the actual block length will be set via sizeof(configured permanent RAM). The
    configurated block length marks the maximal block length, which must not be exceeded by
    sizeof(configured permanent RAM) - to check the configuration it is recomended to enabled block
    length check.
    
    Only available for blocks with permanent RAM.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: NvMBlockLengthCheck
  长名称: Block Length Check
  描述: |
    Enable or disable the block length checks. Block lengths are checked during compile time,
    invalid lengths shall lead to compiler errors.
    
    Only available for blocks with permanent RAM or permanent ROM.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 35
  名称: NvMBlockLengthCheckType
  长名称: Block Length Check Strict
  描述: |
    Decide whether the block length check shall be strict or non-strict
    strict: configured length has to exactly match the corresponding RAM or ROM length
    non strict: configured block length has to be lower than or equal to the corresponding RAM or
    ROM length
    
    Available only if block length check is enabled and automatic block length disabled (automatic
    block length has its own length check type).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: NvMBlockUseCRCCompMechanism
  长名称: ''
  描述: |
    Defines whether the CRC of the RAM Block shall be compared during a write job with the CRC which
    was calculated during the last successful read or write job.
    CRC does not match: NvM will write data
    CRC matches: NvM won't write the data, but behave as if done so
    
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 37
  名称: NvMBlockUseSetRamBlockStatus
  长名称: ''
  描述: |
    Defines if NvMSetRamBlockStatusApi shall be used for this block or not.
    
    Note: If NvMSetRamBlockStatusApi is disabled this configuration parameter shall be ignored.
    true: calling of NvMSetRamBlockStatus for this RAM block shall set the status of the RAM block.
    false: calling of NvMSetRamBlockStatus for this RAM block shall be ignored.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: NvMBlockPreWriteTransformCallback
  长名称: ''
  描述: |
    Function symbol called by NvM to let the user transform the data before writing it into the NV
    RAM.
    
    Can only be used together with NvMBlockPostReadTransformCallback.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 39
  名称: NvMBlockPostReadTransformCallback
  长名称: ''
  描述: |
    Function symbol called by NvM to let the user transform the read data back, to verify the data
    and to tell the NvM whether the data is valid or not.
    
    Can only be used together with NvMBlockPreWriteTransformCallback
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: NvMInitBlockCallbackExtended
  长名称: Init Block Callback (Extended)
  描述: |
    This parameter defines the block specific callback routine which shall be called if no ROM data
    is available for initialization of the NVRAM block.
    If a NULL pointer is configured, no specific callback routine shall be called for initialization
    of the NVRAM block with default data.
    
    Note:
    This parameter is the extended version of "Init Block Callback" (NvMInitBlockCallback).
    Functionality is equal, but the signature of this callback allows the integrator to write the
    data pointer directly and to re-use the callback implementation.
    Using this callback is not conform to the AUTOSAR standard and therefore cannot be used via RTE
    nor the "Use Service Ports" option.
    It is possible to use only one version of the Init Callbacks provided by NvM in order to prevent
    configurations with duplicated RAM initialization.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: NvMSingleBlockCallbackExtended
  长名称: Single Block Callback (Extended)
  描述: |
    This parameter defines the block specific callback routine which shall be invoked on termination
    of each asynchronous single block request. This callback is invoked independently from "Single
    Block Callback" (NvMSingleBlockCallback).
    When both NvMSingleBlockCallback and this parameter are configured the NvMSingleBlockCallback
    will be invoked first.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: NvMNvBlockNVRAMDataLength
  长名称: Block NV RAM Data Length
  描述: |
    This value specified the block length in case ciphered data is stored in NV RAM - in that case
    the plain data length may not match the ciphered data length.
    
    This value must be filled out, if the ciphering, encryption and decryption, of the data is
    enabled for this block. It will be used instead of the NvMNvBlockLength to access the NV RAM.
    
    Hint: This value can be equal or bigger than 'NvMNvBlockLength' depending on the characteristics
    of the referenced CSM Job inside 'NvMNameOfEncryptionJob' (e.g. CSM job adds padding
    information)
  默认值: 16
  最小值: 1
  最大值: 65535
- 
  序号: 43
  名称: NvMInvokeCallbacksForReadAll
  长名称: ''
  描述: |
    This parameter controls whether NvMSingleBlockCallback and NvMInitBlockCallback shall be invoked
    during NvM_ReadAll()/(optional) NvM_PreReadAll().
    
    Note: Some components may not be initialized yet when NvM_ReadAll()/(optional) NvM_PreReadAll()
    is executed (e.g. startup behavior). Invoking callbacks to an uninitialized component may lead
    to DET or even undefined behavior.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 44
  名称: NvMInvokeCallbacksForWriteAll
  长名称: ''
  描述: |
    This parameter controls whether NvMSingleBlockCallback's shall be invoked during NvM_WriteAll().
    
    Note: Some components may not be initialized anymore when NvM_WriteAll() is executed (e.g.
    shutdown behavior). Invoking callbacks to an uninitialized component may lead to DET or even
    undefined behavior.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 45
  名称: NvMCheckLossOfRedundancy
  长名称: ''
  描述: |
    This parameter defines if reading redundant blocks shall also check the block's redundant data.
    If the block's data is no longer redundant (i.e. the data of the blocks differs) it will be
    reported via DEM and will no be repaired automatically.
    This may have a negative impact on the read performance.
    
    Note: Can only be used for redundant blocks with an enabled data integrity mechanism.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 46
  名称: NvMCsmMacSize
  长名称: ''
  描述: |
    This parameter represents the size of the actual MAC used for ensuring the blocks data
    integrity.
    
    If configured, NvM uses MAC as the only data integrity strategy for the block. This also
    requires to CSM MAC generation job and the CSM MAC validation job to be configured.
    
    Hint: As a consequence of using MAC, all CRC related features such as NvMCalcRamBlockCrc and
    NvMBlockUseCRCCompMechanism are no longer available for the block.
  默认值: 16
  最小值: 1
  最大值: 1024
- 
  序号: 47
  名称: NvMSelectBlockForPreReadAll
  长名称: Select Block For Pre ReadAll
  描述: |
    This parameter defines whether the NVRAM block shall be processed during NvM_PreReadAll or not.
    
    Note:
    If the parameters NvMSelectBlockForReadAll and NvMSelectBlockForPreReadAll both are selected the
    block is only processed during NvM_PreReadAll.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 48
  名称: NvMBlockUseAutoValidation
  长名称: ''
  描述: |
    Not used!
    
    This parameter defines whether the RAM Block shall be auto validated during shutdown phase.
    
    true: if auto validation mechanism is used,
    false: otherwise
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 49
  名称: NvMBlockUseMACCompMechanism
  长名称: ''
  描述: |
    Defines whether the MAC of the RAM Block shall be compared during a write job with the MAC which
    was calculated during the last successful read or write job.
    If it does not match: NvM will write data
    If it matches: NvM won't write the data, but behave as if done so
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. NvMEaRef

**描述**: This container includes the reference to an EEPROM Abstraction block.

该容器没有参数。

### 3. NvMFeeRef

**描述**: This container includes the reference to a FEE block.

该容器没有参数。

### 4. NvMCommon

**描述**: This container includes the common configuration options.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NvMApiConfigClass
  长名称: API Configuration Class
  描述: |
    This parameter specifies the available set of NvM services.
    For each configuration class the available services are listed below.
    
    The following services are available in all configuration classes:
    - NvM_Init
    - NvM_SetDataIndex
    - NvM_GetDataIndex
    - NvM_GetErrorStatus
    - NvM_GetVersionInfo
    - NvM_SetRamBlockStatus
    - NvM_ReadAll
    - NvM_PreReadAll
    - NvM_KillReadAll
    - NvM_WriteAll
    - NvM_CancelWriteAll
    - NvM_KillWriteAll
    - NvM_RepairRedundantBlocks
    - NvM_MainFunction
    - NvM_SetBlockLockStatus
    
    The following services are available in NVM_API_CONFIG_CLASS_2 and NVM_API_CONFIG_CLASS_3:
    - NvM_ReadBlock
    - NvM_WriteBlock
    - NvM_RestoreBlockDefaults
    - NvM_CancelJobs
    
    The following services are available in NVM_API_CONFIG_CLASS_3:
    - NvM_SetBlockProtection
    - NvM_EraseNvBlock
    - NvM_InvalidateNvBlock
  默认值: NVM_API_CONFIG_CLASS_3
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NvMBswMMultiBlockJobStatusInformation
  长名称: Multiblock Job Status Information
  描述: This parameter defines whether BswM is informed about the current status of the multi block
      job.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NvMCompiledConfigId
  长名称: Compiled Configuration Id
  描述: |
    This value specifies the Configuration ID regarding the NV memory layout.
    The NvM stores the Configuration ID in the NV RAM. On startup it compares the compiled and the
    stored configuration ID. If both values match, a normal NvM_ReadAll service will be executed. If
    the values mismatch a configuration update is detected and depending on the parameter
    /MICROSAR/NvM/NvMBlockDescriptor/NvMResistantToChangedSw either a normal or an extended runtime
    preparation will be executed (see AUTOSAR specification)
  默认值: 1
  最小值: 0
  最大值: 65535
- 
  序号: 4
  名称: NvMCrcNumOfBytes
  长名称: Crc Number of Bytes
  描述: |
    This parameter defines the maximum number of bytes which shall be processed within one single
    NvM_MainFunctionCall for CRC calculation as well as for internal copy operations.
    Therefore this parameter has influence on maximum duration of NvM_MainFucntion, hence it also
    influences the setting of "Call Cycle of NvM_MainFunction" (NvMMainFunctionPeriod).
    In general, smaller values of "Crc Number of Bytes" allow smaller (faster) call cycles, and vice
    versa.
    
    Note that one NvM_MainFunction call may perform two CRC calculations of "Crc Number of Bytes".
    Additionally an internal copy operation (performed instead of a CRC calculation) processes more
    bytes (because copying step requires less CPU-instructions than CRC clacluation).
  默认值: 64
  最小值: 1
  最大值: 65535
- 
  序号: 5
  名称: NvMDatasetSelectionBits
  长名称: Dataset Selection Bits
  描述: |
    This value specifies the number of least significant bits which shall be used to address a
    certain dataset of a NVRAM block within the interface to the memory hardware abstraction.
    
    0..8: Number of bits which are used for dataset or redundant block addressing.
    
    0: No dataset or redundant NVRAM blocks are configured at all, no selection bits required.
    
    1: In case of redundant NVRAM blocks are configured, but no dataset NVRAM blocks.
  默认值: 4
  最小值: 0
  最大值: 8
- 
  序号: 6
  名称: NvMDevErrorDetect
  长名称: Development Error Detection
  描述: |
    This parameter switches the Development Error Detection and Notification ON or OFF.
    true:   Development error detection is enabled.
    false:  Development error detection is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: NvMDrvModeSwitch
  长名称: Drivers Mode Switch
  描述: |
    This parameter defines switching memory drivers to fast mode during performing NvM_ReadAll,
    NvM_WriteAll and (optional) NvM_PreReadAll.
    
    true:   Fast mode enabled.
    false:  Fast mode disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: NvMDynamicConfiguration
  长名称: Dynamic Configuration Handling
  描述: |
    This parameter defines to enable the dynamic configuration management handling by the
    NvM_ReadAll request.
    
    true:   Dynamic configuration management handling enabled.
    false:  Dynamic configuration management handling disabled.
    
    This parameter affects all NvM processing related to Block with ID 1 (=ConfigBlock) and all
    processing related to Resistant to Changed Software. If the Dynamic Configuration is disabled,
    Block 1 cannot be used by NvM.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: NvMJobPrioritization
  长名称: Job Prioritization
  描述: |
    This parameter defines if job prioritization handling is enabled.
    
    true:   Job prioritization handling enabled.
    false:  Job prioritization handling disabled.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: NvMMultiBlockCallback
  长名称: Multi Block Callback
  描述: This parameter defines the common callback routine which shall be invoked on termination of
      each asynchronous multi block request.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: NvMPollingMode
  长名称: Polling Mode
  描述: |
    This parameter defines if the polling mode in the NVRAM Manager is enabled. At the same time the
    callback functions useable by lower layers is disabled.
    
    true:   Polling mode enabled, callback function usage disabled.
    false:  Polling mode disabled, callback function usage enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: NvMRepeatMirrorOperations
  长名称: Repeat Mirror Operations
  描述: |
    Not used!
    
    This value specifies the number of retries to let the application copy data to or from the NvM
    module's mirror before postponing the current job.
  默认值: 0
  最小值: 0
  最大值: 7
- 
  序号: 13
  名称: NvMSetRamBlockStatusApi
  长名称: SetRamBlockStatus API
  描述: |
    This parameter defines if API NvM_SetRamBlockStatus is available.
    
    true:   API NvM_SetRamBlockStatus enabled.
    false:  API NvM_SetRamBlockStatus disabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: NvMSizeImmediateJobQueue
  长名称: Size Of Immediate Job Queue
  描述: |
    This value specifies the number of queue entries for the immediate priority job queue.
    Hint: If (NvMJobPrioritization == false) this parameter is ignored.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 15
  名称: NvMSizeStandardJobQueue
  长名称: Size Of Standard Job Queue
  描述: This value specifies the number of queue entries for the standard job queue.
  默认值: 8
  最小值: 1
  最大值: 255
- 
  序号: 16
  名称: NvMVersionInfoApi
  长名称: Version Information API
  描述: This parameter enables/disables the function NvM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: NvMMaxNoOfWriteRetries
  长名称: Maximum Number of Write Retries
  描述: This value specifies the maximum number of write retries for a NVRAM block. Regardless of
      configuration a consistency check and write retries are always forced for each block
      which is processed by the request NvM_WriteAll and NvM_WriteBlock.
  默认值: 1
  最小值: 0
  最大值: 7
- 
  序号: 18
  名称: NvMMainFunctionPeriod
  长名称: Call Cycle of NvM_MainFunction
  描述: |
    Specify fixed call cycle for NvM_MainFunction.
    This information affects RTE's (SchM's) settings.
    
    NVM itself does not depend on a fixed cycle time; in can be triggered at arbitrary rates.
    
    It is not necessary to rigger NVM faster than its lower layers (FEE/EA and FLS/EEP).
    Also consider NvMCrcNumOf Bytes, which limits the maximim MainFunction processing times during
    CRC Calculation as well as internal copie operations.
    The faster you want NvM_MainFunction being triggered, the smaller this value should be and vice
    versa.
    
    Note, that notifcation functions may arbitrarily extend NvM_MainFunction's maximum duration.
    This is an issue especially for init callbacks as well as for explicit synchronization
    callbacks, as they would have to process a block at once.
  默认值: 0.01
  最小值: 0.001
  最大值: 1
- 
  序号: 19
  名称: NvMUseBlockIdCheck
  长名称: Use Block Id Check for Blocks with Crc
  描述: If enabled, the NvM checks the data, delivered via underlying modules, to belong to the
      requested NvM Block. Since the NvM uses the Crc, this is only working for Blocks
      configured with Crc! If there is no Block with Crc, this feature will remain unused!
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: NvMRepairRedundantBlocksApi
  长名称: Repair Redundant Blocks Api
  描述: Enables the NvM background job "Repair Redundant Blocks", which iterates over all configured
      redundant blocks and checks their redundancy within the NV RAM. If the redundancy is
      lost, the job will try to repair it.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: NvMSafeBswChecks
  长名称: Safe BSW Checks
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: NvMCsmRetryCounter
  长名称: ''
  描述: |
    This value specifies the number of CSM encryption/decryption job retry attempts.
    
    CSM jobs for block reading and writing may fail (e.g. module busy, queue full, ...).
    To not directly abort the read/write with an error status, the NvM will retry the CSM job for
    the configured NvMCsmRetryCounter times.
    
    Configuring 0 means: no retry behavior; job will be aborted directly.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: NvMDetectedLossOfRedundancyCallback
  长名称: ''
  描述: |
    This parameter defines the notification callback routine that will be called when a loss of
    redundancy was detected when reading a block.
    
    Note: Will only be invoked for blocks with enabled
    NvM/NvMBlockDescriptor/NvMCheckLossOfRedundancy.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: NvMUseAsr440CallbackInterface
  长名称: ''
  描述: |
    If enabled, the signature of following parameters will be used as defined since AUTOSAR version
    4.4.0:
    
    - NvM/NvMBlockDescriptor/NvMSingleBlockCallback
    - NvM/NvMCommon/NvMMultiBlockCallback
    
  默认值: false
  最小值: ''
  最大值: ''
```

### 5. NvmDemEventParameterRefs

**描述**: This container includes references to DemEventParameter elements which shall be invoked using the
API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the
referenced DemEventParameter's DemEventId value.

该容器没有参数。

### 6. NvMCommonVendorParams

**描述**: This container includes Vector specific Module Configuration Parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: NvMCfgCbkIncludeList
  长名称: Callback Include File List
  描述: This parameter contains the header file(s) declaring the call back functions, and the blocks'
      symbol declarations, i.e. the multi block callback the single block call backs, the
      block init callbacks, the ram block symbols as well as the rom block symbols.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: NvMDataIntegrityIntBuffer
  长名称: Data Integrity Buffer
  描述: |
    This paremter defines if the data integrity buffer is module internally.
    true: The NVM provides the buffer for the data integrity value internally. Memory for data
    integrity must not be allocated at the end of Ram Block variable.
    false: The NVM does not provide the buffer for the data integrity value. Memory for data
    integrity value at the end of Ram Block variable is necessary!
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: NvMKillWriteAllApi
  长名称: Kill WriteAll Api
  描述: This parameter defines if the API NvM_KillWriteAll  is available. The API gives users (i.e.
      EcuM) the possibility to time-out WriteAll cancellation (NvM_CancelWriteAll).
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: NvMPreReadAllApi
  长名称: Pre ReadAll Api
  描述: This parameter defines if the API NvM_PreReadAll is available. The API gives users the
      possibility to split the read all into two seperate phases.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: NvMJobForwardingToMemoryCore
  长名称: Job Forwarding To Memory Core
  描述: This parameter defines if the NvM forwards the jobs from the core which runs the application
      to a core which runs the memory stack. This feature must be enabled if the application
      which uses the NvM and the memory stack are located on different cores.
  默认值: false
  最小值: ''
  最大值: ''
```

