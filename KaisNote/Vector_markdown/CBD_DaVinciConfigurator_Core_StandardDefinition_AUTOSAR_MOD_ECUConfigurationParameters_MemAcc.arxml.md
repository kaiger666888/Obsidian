# MemAcc

## 模块描述

The MemAcc (Memory Access module) coordinates the memory access by multiple users in order to avoid
conflicts with this shared memory resource.

## 容器列表

### 1. MemAccAddressAreaConfiguration

**描述**: This container includes the configuration of AddressArea specific parameters for the MemAcc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemAccAddressAreaId
  长名称: ''
  描述: This value specifies a unique identifier which is used to reference to an AddressArea.
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 2
  名称: MemAccAddressAreaPriority
  长名称: ''
  描述: This value specifies the priority of an AddressArea compared to other AddressAreas (0 = lowest
      priority, 65535 = highest priority).
  默认值: 0
  最小值: 0
  最大值: 65535
- 
  序号: 3
  名称: MemAccBufferAlignmentValue
  长名称: ''
  描述: Buffer alignment value inherited by MemAcc upper layer modules. The value must be a multiple
      of MinReadSize.
  默认值: ''
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: MemAccJobEndNotificationName
  长名称: ''
  描述: Job end notification function which is called after MemAcc job completion. If this parameter
      is left empty, no job end notification is triggered and the upper layer module needs to
      poll the job results.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. MemAccSubAddressAreaConfiguration

**描述**: This container includes the configuration parameters for a physically continuous area of memory.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemAccLogicalStartAddress
  长名称: ''
  描述: This value specifies the logical start address of the SubAddressArea.
  默认值: 0
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 2
  名称: MemAccMemInvocation
  长名称: ''
  描述: Defines how the Mem driver services are accessed and how the Mem driver is scheduled and
      activated/initialized.
  默认值: DIRECT_STATIC
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemAccMemNamePrefix
  长名称: ''
  描述: Depending on the MemAccUseMemFuncPtrTable configuration, this prefix is either used to
      reference the Mem driver header structure or the according Mem API function.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemAccNumberOfEraseRetries
  长名称: ''
  描述: This value specifies the number of retries of a failed erase job.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: MemAccNumberOfSectors
  长名称: ''
  描述: This value specifies the number of physical sectors of the SubAddressArea.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 6
  名称: MemAccNumberOfWriteRetries
  长名称: ''
  描述: This value specifies the number of retries of a failed write job.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: MemAccSectorOffset
  长名称: ''
  描述: This value specifies the sector offset of the SubAddressArea in case the SubAddressArea should
      not start with the first sector of the referenced MemSectorBatch.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 8
  名称: MemAccUseEraseBurst
  长名称: ''
  描述: This parameter enables erase bursting for the related sub address area.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: MemAccUseWriteBurst
  长名称: ''
  描述: This parameter enables write bursting for the related sub address area.
  默认值: false
  最小值: ''
  最大值: ''
```

### 3. MemAccGeneral

**描述**: General configuration parameters of the MemAcc.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemAcc64BitSupport
  长名称: ''
  描述: If this option is selected, the address type shall be implemented in 64Bit.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemAccCompareApi
  长名称: ''
  描述: This parameter enables/disables the function MemAcc_Compare().
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemAccDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemAccMainFunctionPeriod
  长名称: ''
  描述: This value specifies the fixed call cycle for MemAcc_MainFunction().
  默认值: 0.005
  最小值: 1E-4
  最大值: 1
- 
  序号: 5
  名称: MemAccPublicCddHeaderFile
  长名称: ''
  描述: Defines header files for callback functions which shall be included in case of CDDs. Range of
      characters is 1.. 32.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: MemAccUseMemFuncPtrTable
  长名称: ''
  描述: This parameter defines if the Mem driver functions are called using the Mem function pointer
      table API.
  默认值: true
  最小值: ''
  最大值: ''
```

