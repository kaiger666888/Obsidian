# FblBmHdr

## 模块描述

Configuration of the FblBmHdr (Boot Manager Header) module.

## 容器列表

### 1. FblBmHdrGeneral

**描述**: General configuration parameters of the FblBmHdr.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHdrUserConfigFile
  长名称: ''
  描述: |
    Reference to an external text file that will be included during generation to FblBmHdr_Cfg.h.
    The content of the user configuration file will be added at the end of the generated module
    configuration file and allows altering or extending the generated code.
    
    Caution: User configuration files can cause the software module to malfunction and must only be
    used with great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblBmHdrMaxVerificationEntries
  长名称: ''
  描述: Specify the maximum number verification ranges, which can be used.
  默认值: 1
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FblBmHdrSbVerificationList
  长名称: ''
  描述: ''
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. FblBmHdrTarget

**描述**: Container to configure the targets.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHdrTargetId
  长名称: Target Id
  描述: Identifier of the Target.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 3. FblBmHdrHeader

**描述**: Container to configure the BootManagerHeader.
The generated header needs to be linked to a specific location, which is defined in the
LogicalBlockTable.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHdrEntryAddress
  长名称: Entry Address
  描述: |
    Entry address of the software.
    The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or
    as a valid linker symbol.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblBmHdrEntryAddressInclude
  长名称: Entry Address Include
  描述: |
    Specify an include file, which contains the declaration of the FblBmHdrEntryAddress symbol in
    case a linker symbol is used as Entry Address.
    If no include file is specified and a linker symbol is used, an extern uint8 array is declared
    to resolve potential compiler errors.
    
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: FblBmHdrBlockStartAddress
  长名称: Block Start Address
  描述: Start address of the complete block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: FblBmHdrBlockLength
  长名称: Block Length
  描述: Length of the complete block in bytes.
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

### 4. FblBmHdrAuthenticationHeader

**描述**: Configure the address/symbol of the authentication header

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHdrAuthenticationHeaderAddress
  长名称: Authentication Header Address
  描述: |
    Address of the authentication header.
    The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or
    as a valid linker symbol.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: FblBmHdrAuthenticationHeaderAddressInclude
  长名称: Authentication Header Address Include
  描述: |
    Specify an include file, which contains the declaration of the
    FblBmHdrAuthenticationHeaderAddress symbol in case a linker symbol is used as Entry Address.
    If no include file is specified and a linker symbol is used, an extern uint8 array is declared
    to resolve potential compiler errors.
    
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. FblBmHdrVerificationList

该容器没有参数。

### 6. FblBmHdrVerificationRange

**描述**: Container to configure the verification ranges.

#### 参数列表

```yaml
- 
  序号: 1
  名称: FblBmHdrVerificationId
  长名称: Verification Id
  描述: Identifier of the verification range.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: FblBmHdrVerificationStartAddress
  长名称: Start Address
  描述: This parameter specifies the start address of the verification range.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: FblBmHdrVerificationLength
  长名称: Length
  描述: This parameter specifies the length of the verification range in bytes.
  默认值: 1
  最小值: 1
  最大值: 4294967295
```

