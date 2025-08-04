# vMemAccM

## 模块描述

Configuration of the vMemAccM (Memory Access Manager) module.

## 容器列表

### 1. vMemAccMGeneral

**描述**: General configuration parameters of the vMemAccM.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function vMemAccM_GetVersionInfo() to get major, minor and
      patch version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vMemAccMMainFunctionPeriod
  长名称: ''
  描述: |
    This value specifies the fixed call cycle for vMemAccM_MainFunction().
    This information affects RTE's (SchM's) settings.
    
    vMemAccM itself does not depend on a fixed cycle time; in can be triggered at arbitrary rates.
    
    It is not necessary to trigger vMemAccM faster than vMem.
    
    The faster you want vMemAccM_MainFunction being triggered, the smaller this value should be and
    vice versa.
  默认值: 0.005
  最小值: 0.0001
  最大值: 1
- 
  序号: 3
  名称: vMemAccMMainFunctionTriggering
  长名称: ''
  描述: |
    This parameter defines the way how vMemAccM_MainFunction() is called.
    The vMemAccM_MainFunction() can be scheduled in different ways, which allows adapting the
    runtime behavior
    - FixedCycleTime: All activities are executed in the vMemAccM_MainFunction() with the defined
    cycle time.
    - BackgroundTask: Activities that do not require a fixed cycle time run in the background task.
    The response time of such activities will depend on the current CPU load.
    Note
    If the system is overloaded, it may happen that the background task is no longer called.
  默认值: FixedCycleTime
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vMemAccMSafeBswChecks
  长名称: ''
  描述: This parameter defines if safety checks are used. These checks improve robustness as e.g.
      invalid parameters are checked before function is executed. This attribute has to be
      enabled for safety projects where this component is mapped to an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vMemAccMDevErrorDetect
  长名称: ''
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
  序号: 6
  名称: vMemAccMCompareApi
  长名称: ''
  描述: |
    This parameter enables/disables the function vMemAccM_Compare().
    This function allows to compare data stored in a buffer with data stored in memory.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. vMemAccMAddressAreaConfiguration

**描述**: This container includes the configuration of AddressArea specific parameters for the vMemAccM
module.
An AddressArea is a virtual area of memory. Upper layers only use virtual addresses to access the
address area. It is the job of vMemAccM to map between virtual and physical addresses. An
AddressArea contains SubAddressAreas and each SubAddressArea is part of a physically continuous
memory area (sector batch)

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMAddressAreaId
  长名称: ''
  描述: |
    This value specifies a unique identifier which is used to reference to an AddressArea.
    This identifier is used as parameter for vMemAccM jobs in order to distinguish between several
    AddressAreas with the same virtual addresses.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: vMemAccMAddressAreaPriority
  长名称: ''
  描述: |
    This value specifies the priority of an AddressArea compared to other AddressAreas.
    
    For each AddressArea one job may be pending at the same time. vMemAccM processes the jobs
    prioriry based.
    This priority even works preemptive. Higher priority jobs pause
    lower priority jobs in a non-destructive manner.
    
    Whereas 0 is the lowest priority, 65535 is the highest priority. It is furthermore not allowed
    for two AddressAreas to have the same priority.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: vMemAccMReadRequestLength
  长名称: ''
  描述: |
    This value specifies the maximum number of bytes the vMemAccM module requests within one vMem
    read request.
    Higher values might block jobs on AddressAreas even with higher priority because current vMem
    job must be finished before a job on another AddressArea can be started.
    Lower values might lead to a decreased performance, because more MainFunctionCycles (vMemAccM
    and vMem) are needed.
    Therefore this value has to be choosen with care!
    
    
  默认值: 64
  最小值: 8
  最大值: 4096
```

### 3. vMemAccMSubAddressAreaConfiguration

**描述**: This container includes the configuration parameters for a  physically continous area of memory.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMNumberOfSectors
  长名称: ''
  描述: This value specifies the number of physical sectors of this Sub-AddressArea.
  默认值: 1
  最小值: 1
  最大值: 4294967296
- 
  序号: 2
  名称: vMemAccMVirtualStartAddress
  长名称: ''
  描述: This value specifies the virtual start address of this Sub-AddressArea.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vMemAccMPhysicalStartAddress
  长名称: ''
  描述: This value specifies the physical start address of this Sub-AddressArea.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vMemAccMvMemFuncPtrTableSymbol
  长名称: ''
  描述: The symbol of the vMem function pointer table the vMemAccM uses to access the specific vMem
      API. vMemAccM expects this symbol to be provided by the specific vMem. The symbol may be
      changed by user, if necessary.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vMemAccMUseEraseBurst
  长名称: ''
  描述: |
    This parameter enables the erase bursting for the related sub address area.
    
    Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst,
    because of too long burst durations.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vMemAccMUseWriteBurst
  长名称: ''
  描述: |
    This parameter enables the write bursting for the related sub address area.
    
    Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst,
    because of too long burst durations.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vMemAccMNrOfWriteRetries
  长名称: ''
  描述: |
    This value specifies the number of retries of a failed write job.
    == 0: no retry, a failed job will be aborted immediately
    > 0: retry the number of times before aborting the job.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: vMemAccMNrOfEraseRetries
  长名称: ''
  描述: |
    This value specifies the number of retries of a failed erase job.
    == 0: no retry, a failed job will be aborted immediately
    > 0: retry the number of times before aborting the job.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 4. vMemAccMAddressAreaVariantConfiguration

**描述**: This container includes all sub address areas belonging to the one specific address area variant.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMAddressAreaVariantId
  长名称: ''
  描述: This value specifies a unique identifier which is used to reference to an AddressAreaVariant.
      The value will be used to set the currently active variant.
  默认值: 0
  最小值: 0
  最大值: 1
```

### 5. vMemAccMMultiPartitionConfiguration

**描述**: This container stores all configuration values required for a vMemAccM multi partition
synchronization.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMMultiPartitionUsecase
  长名称: ''
  描述: |
    This parameter describes the current use case of the vMemAccM multi partition synchronization:
    MultipleNVRAMUsers: each partition accesses the NV RAM peripheral on its own, the accesses need
    to be synchronized.
  默认值: SynchronizeMultipleNVRAMAccessors
  最小值: ''
  最大值: ''
```

### 6. vMemAccMPartitionConfiguration

**描述**: This container holds all required vMemAccM partition configuration parameters.

All of the partition containers act as slaves within the multi partition system - all publish their
next requests to the master partition and wait until the master partition sets the NV RAM access
token to their identifier.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMPartitionId
  长名称: ''
  描述: |
    This parameter defines the unique partition identifier. The value range is [1, 16].
    
    0 is reserved for the master partition.
    [254, 255] are reserved for internal usage.
  默认值: 253
  最小值: 1
  最大值: 253
- 
  序号: 2
  名称: vMemAccMNVRAMAccessToken
  长名称: ''
  描述: |
    This parameter defines the address of the NV RAM access token in shared RAM. The vMemAccM master
    defines and writes the variable with the symbol vMemAccM_NVRAMAccessToken. The other partions
    must not modify the token.
    
    The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or
    as a valid linker symbol.
    
    Caution: The address must be 4 bytes aligned.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vMemAccMPartitionPublishRequest
  长名称: ''
  描述: |
    This parameter defines the address of the variable holding the published partition request in
    shared RAM. The vMemAccM master defines the variable with the symbol
    vMemAccM_PublishReq_<SlaveName>_Id<SlaveId>.
    
    The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or
    as a valid linker symbol.
    
    Caution: The address must be 4 bytes aligned.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. vMemAccMMasterPartitionConfiguration

**描述**: This container holds all required vMemAccM master partition configuration parameters.

The container defines the master partition synchronizing the NV RAM accesses of all other partitions
via the NV RAM access token. If this container exists, the vMemAccM will act as a master. If this
container does not exist, the vMemAccM will act as slave.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemAccMMasterPartitionId
  长名称: ''
  描述: |
    This parameter defines the unique master partition identifier - always 0.
    
    [1, 253] are reserved for slave partitions.
    [254, 255] are reserved for internal usage.
  默认值: 0
  最小值: 0
  最大值: 0
```

