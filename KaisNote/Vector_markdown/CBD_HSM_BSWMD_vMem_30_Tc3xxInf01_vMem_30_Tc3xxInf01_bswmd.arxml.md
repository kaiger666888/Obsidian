# vMem

## 模块描述

Configuration of the vMem driver (internal or external memory driver) module.
Its multiplicity describes the present number of memory drivers, so there will be one container for
each memory driver.

## 容器列表

### 1. vMemGeneral

**描述**: Container for general configuration parameters of the memory driver. These parameters are always
pre-compile.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemDevErrorDetect
  长名称: ''
  描述: |
    This parameter switches the Development Error Detection and Reporting ON or OFF.
    true:   Development error detection and reporting is enabled.
    false:  Development error detection and reporting is disabled.
    
    Note:
    In general, the development error detection is recommended during pre-test phase. It is not
    recommended to enable the development error detection in production code due to increased
    runtime and ROM needs.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vMemSafeBswChecks
  长名称: ''
  描述: |
    Selects if safety checks are used.
    
    These checks improve robustness as e.g. invalid parameters are checked before function is
    executed. This attribute has to be enabled for safety projects where this component is mapped to
    an ASIL partition.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vMemVersionInfoApi
  长名称: ''
  描述: This parameter enables/disables the function GetVersionInfo() to get major, minor and patch
      version information.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vMemMainFunctionPeriod
  长名称: ''
  描述: |
    This value specifies the fixed call cycle for vMem_MainFunction().
    This information affects RTE's (SchM's) settings.
  默认值: 0.005
  最小值: 0.0001
  最大值: 1
- 
  序号: 5
  名称: vMemUsePeripheralAccessApi
  长名称: ''
  描述: |
    This parameter specifies whether the module should use OsPeripheralAccess-API (e.g. because
    memory access is restricted by MMU) to access memory mapped registers.
    
    true: Module uses APIs provided by OS to access memory mapped registers.
    false: Module uses direct memory access to access memory mapped registers.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. vMemInstance

**描述**: This container includes the memory driver instance specific configuration parameters.
Its multiplicity describes the number of memory driver instances of this memory driver, so there
will be one container for each memory driver instance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemInstanceId
  长名称: ''
  描述: |
    This value specifies the unique numeric identifier which is used to reference a memory driver
    instance. It is used in order to distinguish between several memory driver instances with the
    same physical addresses.
    This value will be assigned to the symbolic name derived of the vMemInstance container short
    name.
  默认值: 0
  最小值: 0
  最大值: 65535
```

### 3. vMemSectorList

**描述**: List of programmable sectors and pages.

该容器没有参数。

### 4. vMemSector

**描述**: Configuration description of a programmable sector or sector batch. Sector batch means that
homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemNumberOfSectors
  长名称: ''
  描述: |
    Number of continuous sectors with identical values for vMemSectorSize and vMemPageSize.
    
    If this parameter is configured to be greater than 1, this will result in a so called "sector
    batch".
  默认值: 1
  最小值: 1
  最大值: 65536
- 
  序号: 2
  名称: vMemPageSize
  长名称: ''
  描述: |
    Size of one page of this sector in bytes.
    
    A page is the smallest writeable unit.
  默认值: ''
  最小值: 1
  最大值: 4294967296
- 
  序号: 3
  名称: vMemSectorSize
  长名称: ''
  描述: |
    Size of this sector in bytes.
    
    A sector is the smallest erasable unit.
  默认值: ''
  最小值: 1
  最大值: 4294967296
- 
  序号: 4
  名称: vMemStartAddress
  长名称: ''
  描述: |
    Physical start address of this sector.
    
    In case of a sector batch this physical start address is the address of the first sector. The
    physical start address of the other sectors can be calculated by usage of parameter
    vMemSectorSize.
  默认值: ''
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vMemProgramFlashId
  长名称: ''
  描述: |
    This value specifies the unique numeric identifier which is used to reference Program Flash
    Bank. It is primarily used for the replace logical sector feature.
    Refer to the technical reference of this driver and the hardware manual for more information.
  默认值: ''
  最小值: 0
  最大值: 5
- 
  序号: 6
  名称: vMemPhysicalSectorId
  长名称: ''
  描述: |
    This value specifies the unique numeric identifier which is used to reference a Physical Sector
    within a Program Flash Bank. A Program Flash Bank generally consists of 1 to 3 Physical Sectors
    of size 1 Mbyte. It is primarily used for the replace logical sector feature.
    Refer to the technical reference of this driver and the hardware manual for more information.
  默认值: ''
  最小值: 0
  最大值: 2
```

### 5. vMemBurstSettings

**描述**: Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vMemEraseBurstSize
  长名称: ''
  描述: |
    Size of sector erase burst in bytes. A sector burst can be used for improved performance and is
    typically (a subset of) a sector batch.
    
    Additionally the size also prescribes a necessary alignment: The phyiscal start address must be
    aligned to the size value, i.e. it must an integral multiple of the burst size.
  默认值: 65536
  最小值: 0
  最大值: 4294967296
- 
  序号: 2
  名称: vMemWriteBurstSize
  长名称: ''
  描述: |
    Size of page write/program burst in bytes. A sector burst can be used for improved performance
    and is typically (a subset of) a sector batch.
    
    Additionally the size also prescribes a necessary alignment: The phyiscal start address must be
    aligned to the size value, i.e. it must an integral multiple of the burst size.
  默认值: 256
  最小值: 0
  最大值: 4294967296
- 
  序号: 3
  名称: vMemPageBurstRamAlignment
  长名称: ''
  描述: |
    In order to make use of page write bursts, a device might require a specific alignment of the
    data buffer (containing the data to be programmed to NV memory).
    
    E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly
    over head the buffer passed to write routine shall be correctly aligned according to this
    setting in order to use bursts.
    
    Unless no alignment is necessary (value equals 1), the implementation shall check for expected
    alignment, and it shall reject a burst request if this check failed.
  默认值: 1
  最小值: 1
  最大值: 256
```

