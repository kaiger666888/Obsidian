# vSet

## 模块描述

The virtual Vector Common Settings module collects global and ECU specific configuration
information.

## 容器列表

### 1. vSetGeneral

**描述**: General parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetDummyStatementKind
  长名称: ''
  描述: Dummy statements used to avoid compiler warnings about e.g. unused parameters.
  默认值: None
  最小值: ''
  最大值: ''
```

### 2. vSetPlatform

**描述**: General platform and compiler specific parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetByteOrder
  长名称: ''
  描述: Byte order on memory level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSetBitOrder
  长名称: ''
  描述: Bit order on register level.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSetCPUType
  长名称: ''
  描述: Register width of the CPU in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vSetSizeOfEnum
  长名称: ''
  描述: Size of type enum in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vSetSizeOfInt
  长名称: ''
  描述: Size of type int in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vSetSizeOfROMPointer
  长名称: ''
  描述: Size of ROM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vSetSizeOfRAMPointer
  长名称: ''
  描述: Size of RAM pointer in bit.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. vSetCalibration

**描述**: General calibration specific parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetPBCalibrationVirtualStartAddress
  长名称: ''
  描述: |
    Start address of the virtual memory segment for calibration of post-build loadable parameters.
    
    The memory segment is used by standard calibration tools like vCDMStudio to display and manage
    post-build loadable parameters in a physical representation. The segment is only available in
    the HEX-file and the data base of the calibration tool. It is not transferred to the ECU's
    memory. The address should not lie in the address range of the ECU. Recommended is an address
    beyond the ECU's address range because the virtual memory segment size depends on the concrete
    configuration and is calculated automatically.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 4. vSetBswInitialization

**描述**: General BSW initialization specific parameters.

该容器没有参数。

### 5. vSetInitFunction

**描述**: Name of the init function.

E.g. ComM_Init

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetHeader
  长名称: ''
  描述: Header which declares function and types.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSetConfigType
  长名称: ''
  描述: Name of ConfigType
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSetConfigPtrClass
  长名称: ''
  描述: Memory class of Config Pointer.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. vSetInitFunctionInstance

**描述**: This container represents an instance of the Init Function. For each partition which needs
initialization, one container instance needs to be created.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vSetInitPhase
  长名称: ''
  描述: Phase in which this init function shall be called.
  默认值: INIT_TWO_POST_NVMREADALL
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vSetAdditionalInitCode
  长名称: ''
  描述: |
    Specify additional code which can be referenced from the initialization callouts of EcuM and
    BswM.
    
    E.g.: Mcu_InitClock()
    
    If it is necessary to call a function with a module pointer from the global postbuild-loadable
    configuration, the placeholder %CONFIGPTR% can be used:
    
    E.g.: Mcu_Init(%CONFIGPTR%)
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vSetConfigPtrName
  长名称: ''
  描述: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If
      Init Function has a pointer, at least a NULL_PTR should be inserted here.
  默认值: ''
  最小值: ''
  最大值: ''
```

