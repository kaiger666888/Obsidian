# WrapNv

## 模块描述

Configuration of the WrapNv (Wrapper non-volatile) module.

## 容器列表

### 1. WrapNvGeneral

#### 参数列表

```yaml
- 
  序号: 1
  名称: WrapNvUserConfigFile
  长名称: ''
  描述: If a file path will be specified, the file is read and its content is put at the end of the
      generated file.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WrapNvEEPROMBaseAddress
  长名称: ''
  描述: The Base Address of the EEPROM memory. This parameter is only relevant if EEPROM Driver is
      chosen.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: WrapNvFirstHandle
  长名称: ''
  描述: Specify the first handle of the EEPROM Manger.
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: WrapNvNVMDataHandling
  长名称: ''
  描述: |
    This parameter specifies the underlying memory driver which should be wrapped.
    
    EXTERNAL_EEPROM_DRIVER: a simple EEPROM driver
    EEPROM_EMULATION_FOR_HIS_FLASH_DRIVER: EEPROM Manager
    MSR_NVM: Microsar NvM
    FEE: Fee / Fls driver (without NvM)
    EA: Ea / Eep driver (without NvM)
  默认值: EXTERNAL_EEPROM_DRIVER
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: WrapNvMainFunctionPolling
  长名称: ''
  描述: This parameter specifies whether main functions should be polled automatically.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. WrapNvMainFunctionCycle

**描述**: Determines the value in which the MainFunction of the referenced module shall be called [in MS].

0: call it as soon as possible
> 0: call the mainfunction each [value] MS

#### 参数列表

```yaml
- 
  序号: 1
  名称: WrapNvMainFunctionCycleValue
  长名称: Value
  描述: The cycle in MS.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 3. WrapNvMemoryLayout

该容器没有参数。

### 4. WrapNvDataBlock

#### 参数列表

```yaml
- 
  序号: 1
  名称: WrapNvDbType
  长名称: Type
  描述: |
    Defines the type of the data block.
    SINGLE: An atomic element
    LIST: An array
    STRUCT: A struct
    TABLE: An array of structs
  默认值: SINGLE
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: WrapNvDbIndex
  长名称: Index
  描述: Specify the order in which the data blocks are generated.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: WrapNvDbCount
  长名称: Count
  描述: Defines the number of multiple data blocks in a contiguous area.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 4
  名称: WrapNvDbDescription
  长名称: Description
  描述: Description of the data block.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. WrapNvDataElement

**描述**: Contains a list of data elements, which are associated with the data block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: WrapNvDeIndex
  长名称: Index
  描述: Specify the order in which the data elements are generated within the data block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: WrapNvDeLength
  长名称: Length
  描述: Defines the data element length in bytes.
  默认值: 1
  最小值: 1
  最大值: 4294967295
- 
  序号: 3
  名称: WrapNvDeDescription
  长名称: Description
  描述: Description of the data element.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: WrapNvDeDefaultValue
  长名称: Default Value
  描述: |
    The default value of this data element.
    Only used by NVM, FEE and EA configurations.
  默认值: ''
  最小值: ''
  最大值: ''
```

