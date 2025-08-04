# Ea

## 模块描述

EEPROM abstraction. Provides access to EEPROM for reading and storing data persistently.

#NVRAM #NVMemory #DataStorage #EEPROM
#AUTOSAR

## 容器列表

### 1. EaBlockConfiguration

**描述**: This container includes the configuration of block specific parameters for the EEPROM abstraction
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaBlockNumber
  长名称: Block Number
  描述: This value specifies the block identifier (handle).
  默认值: 1
  最小值: 1
  最大值: 65534
- 
  序号: 2
  名称: EaBlockSize
  长名称: Block Size
  描述: This value specifies the size of a logical block in bytes.
  默认值: 8
  最小值: 1
  最大值: 65535
- 
  序号: 3
  名称: EaImmediateData
  长名称: Immediate Data
  描述: This parameter defines if this block has high priority data.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EaNumberOfWriteCycles
  长名称: Number Of Write Cycles
  描述: This value specifies the number of write cycles required for this block.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: EaNumberOfDatasets
  长名称: Number Of Datasets
  描述: |
    This value specifies the number of datasets/clones. This specfies how often an individual block
    exists.
    
    Additional information related to the block configuration in the NvM :
    Native block in the NvM means 1 Dataset is configured.
    Redundant  block in the NvM means 2 Datasets are configured.
    Dataset block in the NvM means N Datasets can be configured. Maximum value depends on parameter
    NvMDatasetSelectionBits.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 6
  名称: EaNumberOfInstances
  长名称: Number Of Instances
  描述: This value specifies the number of instances needed for one dataset/clone. The value depends
      on the number of write cycles the EEPROM supports and the number of write cycles of the
      specific dataset/clone.
  默认值: 1
  最小值: 1
  最大值: 255
- 
  序号: 7
  名称: EaVerifyWrittenData
  长名称: Verify Written Data
  描述: This parameter defines if the written data shall be verified for consistency.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EaBlockId
  长名称: Block Id
  描述: |
    This value specifies the BlockID which indicates the base (aka: "tag") of a Block within its
    associated partition.
    The Block can be uniquely identified using partition.
    The ID must be unique within block's partition; blocks within different partitions may share the
    same value.
  默认值: 65534
  最小值: 0
  最大值: 65534
```

### 2. EaGeneral

**描述**: General configuration parameters of the EA.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaDevErrorDetect
  长名称: Development Error Detection
  描述: |
    This parameter switches the Development Error Detection and Reporting ON or OFF.
    true:   Development error detection and reporting is enabled.
    false:  Development error detection and reporting is disabled.
    
    Note: In general, the development error detection is recommended during pre-test phase. It is
    not recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EaIndex
  长名称: Index
  描述: This value specifies the InstanceId of this module instance. If only one instance is present
      it shall have the Id 0.
  默认值: 0
  最小值: 0
  最大值: 254
- 
  序号: 3
  名称: EaNvmJobEndNotification
  长名称: NvMJobEnd Notification
  描述: This parameter defines the job end notification routine provided by the upper layer module
      (normally NvM_JobEndNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EaNvmJobErrorNotification
  长名称: NvMJobError Notification
  描述: This parameter defines the job error notification routine provided by the upper layer module
      (normally NvM_JobErrorNotification).
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EaPollingMode
  长名称: Polling Mode
  描述: This parameter defines if the polling mode for this module is enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EaSetModeSupported
  长名称: Set Mode Api
  描述: This parameter defines if the function Ea_SetMode API is available.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EaVersionInfoApi
  长名称: Version Info Api
  描述: This parameter enables/disables the function Ea_GetVersionInfo() to get major, minor and patch
      version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EaVirtualPageSize
  长名称: Virtual Page Size
  描述: |
    Not used!
    EA provides configuration of partitions with different address and write alignments due to the
    fact that multiple EEP modules can be referenced and their alignments may not match.
    EaBlocks are always assigned to a certain EaPartition. Therefore, EaBlocks are aligned to
    EaPartitionAddressAlignment of its EaPartitions.
  默认值: 8
  最小值: 1
  最大值: 65535
- 
  序号: 9
  名称: EaNvMCallbackIncludeFile
  长名称: NvM Cbk Include File
  描述: This parameter defines the name of the include file for callback function declaration of the
      NvM.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: EaCorrectSingleBitFlips
  长名称: Correct Single Bit Flips
  描述: This parameter defines if the correction of single bit flips is enabled.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: EaMainFunctionPeriod
  长名称: ''
  描述: |
    Specify fixed call cycle for Ea_MainFunction.
    This information affects RTE's (SchM's) settings.
    
    It is not necessary to trigger Ea faster than its lower layer (EEP).
    The faster you want Ea_MainFunction being triggered, the smaller this value should be and vice
    versa.
  默认值: 0.005
  最小值: 0.0001
  最大值: 1
- 
  序号: 12
  名称: EaMainFunctionTriggering
  长名称: ''
  描述: |
    The MainFunction can be scheduled in different ways, which allows adapting the runtime behavior
    - FixedCycleTime: All activities are executed in the MainFunction with the defined cycle time.
    - BackgroundTask: Activities that do not require a fixed cycle time run in the background task.
    The response time of such activities will depend on the current CPU load.
    Note
    If the system is overloaded, it may happen that the background task is no longer called.
  默认值: FixedCycleTime
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: EaSafeBswChecks
  长名称: Safe Bsw Checks
  描述: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters
      are checked before function is executed. This attribute has to be enabled for safety
      projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. EaEepApi

**描述**: This container is used to announce the API service names and the include file of an Eep instance
manually.
API service names and include file can be typed manually and assigned to the corresponding Eep
instance via "Eeprom Device" reference.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaEepIncludeFile
  长名称: Eep Include File
  描述: This parameter defines the name of the header file of the EEPROM Driver.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: EaEepSetMode
  长名称: Eep SetMode API
  描述: This parameter defines the name of the EEPROM SetMode API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: EaEepRead
  长名称: Eep Read API
  描述: This parameter defines the name of the EEPROM Read API
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: EaEepWrite
  长名称: Eep Write API
  描述: This parameter defines the name of the EEPROM Write API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: EaEepCancel
  长名称: Eep Cancel API
  描述: This parameter defines the name of the EEPROM Cancel API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: EaEepGetStatus
  长名称: Eep GetStatus API
  描述: This parameter defines the name of the EEPROM GetStatus API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: EaEepGetJobResult
  长名称: Eep GetJobResult API
  描述: This parameter defines the name of the EEPROM GetJobResult API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: EaEepErase
  长名称: Eep Erase API
  描述: This parameter defines the name of the EEPROM Erase API.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: EaEepCompare
  长名称: Eep Compare API
  描述: This parameter defines the name of the EEPROM Compare API.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 4. EaPublishedInformation

**描述**: This container includes additional published parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaBlockOverhead
  长名称: Block Overhead
  描述: |
    Not used!
    
    This value specifies the management overhead per logical block.
  默认值: 2
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: EaMaximumBlockingTime
  长名称: Maximum Blocking Time
  描述: |
    Not used!
    
    This value specifies the maximum time the EA module's API routines shall be blocked (delayed) by
    internal operations.
  默认值: 0
  最小值: 0
  最大值: Inf
- 
  序号: 3
  名称: EaPageOverhead
  长名称: Page Overhead
  描述: |
    Not used!
    
    This value specifies the management overhead per page.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 5. EaPartitionConfiguration

**描述**: This container includes the configuration of partition specific parameters for the EEPROM
abstraction module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: EaPartitionStartAddress
  长名称: Partition Start Address
  描述: This value specifies the physical start address of the partition.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: EaPartitionSize
  长名称: Partition Size
  描述: This value specifies size of the partition in bytes.
  默认值: 256
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: EaPartitionAddressAlignment
  长名称: Address Alignment
  描述: |
    Address Alignment influences the way EA stores data entities in EEPROM.
    All single entities will start at addresses being an integral multiple of
    EaPartitionAddressAlignment.
    This alignment itself must be equal to or greater than this partition's write alignment.
  默认值: 1
  最小值: 1
  最大值: 65535
- 
  序号: 4
  名称: EaPartitionWriteAlignment
  长名称: Write Alignment
  描述: |
    Page size of EEPROM device for write jobs in bytes.
    This is the alignment of Eep_Write requests the EA issues to the EEPROM: Both EEP addresses and
    lengths are always multiples of this value.
    This value shall be at least equal to EEPROM's write unit size.
  默认值: 1
  最小值: 1
  最大值: 65535
```

