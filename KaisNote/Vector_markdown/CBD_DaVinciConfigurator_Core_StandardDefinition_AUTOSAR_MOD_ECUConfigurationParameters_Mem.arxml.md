# Mem

## 模块描述

Configuration of the Mem driver (internal or external memory driver) module.

## 容器列表

### 1. MemGeneral

**描述**: Container for general configuration parameters of the Mem driver. These parameters are always
pre-compile.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemDevErrorDetect
  长名称: ''
  描述: Switches the development error detection and notification on or off.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemIndex
  长名称: ''
  描述: Specifies the InstanceId of this module instance. If only one instance is present it shall
      have the Id 0.
  默认值: ''
  最小值: 0
  最大值: 254
```

### 2. MemInstance

**描述**: This container includes the Mem driver instance specific configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemInstanceId
  长名称: ''
  描述: This value specifies the unique numeric identifier which is used to reference a Mem driver
      instance in case multiple devices of the same type shall be addressed by one Mem driver.
      This value will be assigned to the symbolic name derived of the MemInstance container
      short name.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 3. MemSectorBatch

**描述**: Configuration description of a programmable sector or sector batch. Sector batch means that
homogenous and coherent sectors can be configured as one MemSector element.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemEraseSectorSize
  长名称: ''
  描述: Size of this sector in bytes.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: MemMinReadSize
  长名称: ''
  描述: Smallest readable unit in bytes.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: MemNumberOfSectors
  长名称: ''
  描述: Number of contiguous sectors with identical values for MemSectorSize and MemPageSize.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: MemSpecifiedEraseCycles
  长名称: ''
  描述: Number of erase cycles specified for the memory device (usually given in the device data
      sheet).
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: MemStartAddress
  长名称: ''
  描述: Physical start address of the sector (batch).
  默认值: ''
  最小值: 0
  最大值: 18446744073709551615
- 
  序号: 6
  名称: MemWritePageSize
  长名称: ''
  描述: Size of a write page of this sector in bytes.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 4. MemBurstSettings

**描述**: Container for burst setting configuration parameters of the Mem driver.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemEraseBurstSize
  长名称: ''
  描述: Size of sector erase burst in bytes. A sector burst can be used for improved performance and
      is typically (a subset of) a sector batch.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 2
  名称: MemMaxReadSize
  长名称: ''
  描述: This value specifies the maximum number of bytes the MemAcc module requests within one Mem
      read request.
  默认值: ''
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: MemWriteBurstSize
  长名称: ''
  描述: Size of page write/program burst in bytes. A sector burst can be used for improved performance
      and is typically (a subset of) a sector batch.
  默认值: ''
  最小值: 1
  最大值: 4294967295
```

### 5. MemPublishedInformation

**描述**: Additional published parameters not covered by CommonPublishedInformation container.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemErasedValue
  长名称: ''
  描述: The contents of an erased memory cell.
  默认值: ''
  最小值: 0
  最大值: 4294967295
```

