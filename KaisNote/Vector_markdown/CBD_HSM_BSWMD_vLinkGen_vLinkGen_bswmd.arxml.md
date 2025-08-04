# vLinkGen

## 模块描述

Configuration of the MICROSAR vLinkGen module.

## 容器列表

### 1. vLinkGenMemLayout

**描述**: Container to structure all memory layout relevant configuration parameters.

该容器没有参数。

### 2. vLinkGenLinkerSections

**描述**: Container to structure the configuration parameters of the different linker section types.

该容器没有参数。

### 3. vLinkGenLinkerCodeSection

**描述**: This container includes all configuration parameters for a CODE linker section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerCodeSectionName
  长名称: Name
  描述: This parameter specifies the name of the linker section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerCodeSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the linker section in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 4. vLinkGenLinkerConstSection

**描述**: This container includes all configuration parameters for a CONST linker section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerConstSectionName
  长名称: Name
  描述: This parameter specifies the name of the linker section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerConstSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the linker section in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 5. vLinkGenLinkerVarSection

**描述**: This container includes all configuration parameters for a VAR linker section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerVarSectionName
  长名称: Name
  描述: This parameter specifies the name of the linker section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerVarSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the linker section in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 6. vLinkGenLinkerStackSection

**描述**: This container includes all configuration parameters for a STACK linker section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerStackSectionName
  长名称: Name
  描述: This parameter specifies the name of the linker section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerStackSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the linker section in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 7. vLinkGenLinkerSectionConstGroup

**描述**: This container includes all configuration parameters for a CONST linker section group.
It can be used to map several CONST or CODE linker sections to a specific memory region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstGroupPosition
  长名称: Position
  描述: |
    Specifies the position of the linker section group in the selected hardware memory location.
    Relative to other section groups within the same hardware memory location.
    If equal, the generation order depends on the order of the group within the configuration file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenConstGroupAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the section group in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenConstGroupPreUserCode
  长名称: Preprocessor Condition Begin
  描述: |
    Specifies optional preprocessor condition to be generated right before the linker section group.
    
    Example:
    #ifdef MIP_USED
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenConstGroupPostUserCode
  长名称: Preprocessor Condition End
  描述: |
    Specifies optional end of preprocessor condition to be generated right after the linker section
    group.
    
    Example:
    #endif /* MIP_USED */
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenConstGroupGapSize
  长名称: Gap Size
  描述: |
    This value specifies the size of the optional gap to be kept free after the section group in
    bytes.
    If zero, no gap is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 8. vLinkGenConstGroupUserSection

**描述**: Specifies compiler specific user code that is directly generated into the linker section group at
the specified position.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstGroupUserSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the user code within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenConstGroupUserSectionValue
  长名称: Value
  描述: Specifies the compiler specific user code.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. vLinkGenConstGroupCodeSection

**描述**: Specifies a group of CODE linker sections whose data shall be linked to the linker section group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenCodeSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the sections within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenCodeSectionCachePolicyCache
  长名称: Cache Policy CACHE
  描述: Specifies if cachable sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenCodeSectionCachePolicyNoCache
  长名称: Cache Policy NOCACHE
  描述: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenCodeSectionAddressingModeNear
  长名称: Addressing Mode NEAR
  描述: Specifies if sections with near addressing mode (CODE_FAST) are linked into the linker section
      group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenCodeSectionAddressingModeFar
  长名称: Addressing Mode FAR
  描述: Specifies if sections with far addressing mode (CODE) are linked into the linker section
      group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenCodeSectionFlagNoLoad
  长名称: Link Flag NOLOAD
  描述: |
    Specifies if the sections content shall be loaded into the target system or not.
    If enabled the content has to be loaded in some other way into the target system.
    
    true: Do not load sections content into the target system
    false: Load sections content into the target system
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenCodeSectionFlagKeep
  长名称: Link Flag KEEP
  描述: |
    Specifies if the sections shall be forced to be kept by the linker, although it is empty.
    
    true: All sections within this group shall be marked with keep
    false: Keep is not generated for the sections
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
```

### 10. vLinkGenConstGroupConstSection

**描述**: Specifies a group of CONST linker sections whose data shall be linked to the linker section group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the sections within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenConstSectionCachePolicyCache
  长名称: Cache Policy CACHE
  描述: Specifies if cachable sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenConstSectionCachePolicyNoCache
  长名称: Cache Policy NOCACHE
  描述: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenConstSectionAddressingModeNear
  长名称: Addressing Mode NEAR
  描述: Specifies if sections with near addressing mode (CONST_FAST) are linked into the linker
      section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenConstSectionAddressingModeFar
  长名称: Addressing Mode FAR
  描述: Specifies if sections with far addressing mode (CONST) are linked into the linker section
      group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenConstSectionFlagNoLoad
  长名称: Link Flag NOLOAD
  描述: |
    Specifies if the sections content shall be loaded into the target system or not.
    If enabled the content has to be loaded in some other way into the target system.
    
    true: Do not load sections content into the target system
    false: Load sections content into the target system
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenConstSectionFlagKeep
  长名称: Link Flag KEEP
  描述: |
    Specifies if the sections shall be forced to be kept by the linker, although it is empty.
    
    true: All sections within this group shall be marked with keep
    false: Keep is not generated for the sections
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
```

### 11. vLinkGenLinkerSectionVarGroup

**描述**: This container includes all configuration parameters for a VAR linker section group.
It can be used to map several VAR or STACK linker sections to a specific memory region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarGroupPosition
  长名称: Position
  描述: |
    Specifies the position of the linker section group in the selected hardware memory location.
    Relative to other section groups within the same hardware memory location.
    If equal, the generation order depends on the order of the group within the configuration file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenVarGroupAlignment
  长名称: Alignment
  描述: |
    This value specifies the alignment of the section group in bytes.
    If zero, no alignment is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenVarGroupInitPolicy
  长名称: Zero Init Policy
  描述: |
    This parameter defines whether the ZERO_INIT sections of the linker section group shall be
    initialized with zeros and when.
    
    NONE: No zero initialization required.
    ALWAYS: Initialize always after the PLL initialization is done.
    HARD_RESET: Initialize after the PLL initialization is done, only if hardware reset occured.
    FOREIGN: Initialization is done by another instance.
    STARTUP: Initialize always directly after reset. Normally only for groups containing the startup
    stack.
    
    Note:
    Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitAreas*)
    which can be used to initialize the linker section groups with zeros.
    This is normally done by the startup code of the vBRS.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenVarGroupInitCore
  长名称: Init Core ID
  描述: Specifies the physical core ID which shall perform the initialization of all INIT or ZERO_INIT
      sections assigned to the linker section group.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vLinkGenVarGroupPreUserCode
  长名称: Preprocessor Condition Begin
  描述: |
    Specifies optional preprocessor condition to be generated right before the linker section group.
    
    Example:
    #ifdef MIP_USED
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenVarGroupPostUserCode
  长名称: Preprocessor Condition End
  描述: |
    Specifies optional end of preprocessor condition to be generated right after the linker section
    group.
    
    Example:
    #endif /* MIP_USED */
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenVarGroupGapSize
  长名称: Gap Size
  描述: |
    This value specifies the size of the optional gap to be kept free after the section group in
    bytes.
    If zero, no gap is generated.
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 12. vLinkGenVarGroupUserSection

**描述**: Specifies compiler specific user code that is directly generated into the linker section group at
the specified position.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarGroupUserSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the user code within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenVarGroupUserSectionValue
  长名称: Value
  描述: Specifies the compiler specific user code.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 13. vLinkGenVarGroupVarSection

**描述**: Specifies a group of VAR linker sections whose data shall be linked to the linker section group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the sections within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenVarSectionInitPolicyInit
  长名称: Init Policy INIT
  描述: Specifies if INIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenVarSectionInitPolicyNoInit
  长名称: Init Policy NOINIT
  描述: Specifies if NOINIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenVarSectionInitPolicyZeroInit
  长名称: Init Policy ZERO_INIT
  描述: Specifies if ZERO_INIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenVarSectionCachePolicyCache
  长名称: Cache Policy CACHE
  描述: Specifies if cachable sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenVarSectionCachePolicyNoCache
  长名称: Cache Policy NOCACHE
  描述: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenVarSectionAddressingModeNear
  长名称: Addressing Mode NEAR
  描述: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section
      group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vLinkGenVarSectionAddressingModeFar
  长名称: Addressing Mode FAR
  描述: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vLinkGenVarSectionFlagNoLoad
  长名称: Link Flag NOLOAD
  描述: |
    Specifies if the sections content shall be loaded into the target system or not.
    If enabled the content has to be loaded in some other way into the target system.
    
    true: Do not load sections content into the target system
    false: Load sections content into the target system
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vLinkGenVarSectionFlagKeep
  长名称: Link Flag KEEP
  描述: |
    Specifies if the sections shall be forced to be kept by the linker, although it is empty.
    
    true: All sections within this group shall be marked with keep
    false: Keep is not generated for the sections
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
```

### 14. vLinkGenVarGroupStackSection

**描述**: Specifies a group of STACK linker sections whose data shall be linked to the linker section group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenStackSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the sections within the linker section group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenStackSectionInitPolicyInit
  长名称: Init Policy INIT
  描述: Specifies if INIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenStackSectionInitPolicyNoInit
  长名称: Init Policy NOINIT
  描述: Specifies if NOINIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenStackSectionInitPolicyZeroInit
  长名称: Init Policy ZERO_INIT
  描述: Specifies if ZERO_INIT sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenStackSectionCachePolicyCache
  长名称: Cache Policy CACHE
  描述: Specifies if cachable sections are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenStackSectionCachePolicyNoCache
  长名称: Cache Policy NOCACHE
  描述: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenStackSectionAddressingModeNear
  长名称: Addressing Mode NEAR
  描述: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section
      group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: vLinkGenStackSectionAddressingModeFar
  长名称: Addressing Mode FAR
  描述: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: vLinkGenStackSectionFlagNoLoad
  长名称: Link Flag NOLOAD
  描述: |
    Specifies if the sections content shall be loaded into the target system or not.
    If enabled the content has to be loaded in some other way into the target system.
    
    true: Do not load sections content into the target system
    false: Load sections content into the target system
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: vLinkGenStackSectionFlagKeep
  长名称: Link Flag KEEP
  描述: |
    Specifies if the sections shall be forced to be kept by the linker, although it is empty.
    
    true: All sections within this group shall be marked with keep
    false: Keep is not generated for the sections
    
    Note:
    If the parameter is ReadOnly, it is not supported by the selected compiler.
  默认值: false
  最小值: ''
  最大值: ''
```

### 15. vLinkGenLinkerSectionUserGroup

**描述**: This container includes all configuration parameters for an user code group.
User code groups are generated either at the beginning or at the end of the linker script.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenUserGroupPosition
  长名称: Position
  描述: |
    Specifies the position of the user code group.
    If equal, the generation order depends on the order of the group within the configuration file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenUserGroupPlacement
  长名称: Placement
  描述: |
    Specifies whether the user code group is generated at the beginning or the end of the linker
    script.
    
    PRE: The user code group is generated at the beginning of the linker script.
    POST: The user code group is generated at the end of the linker script.
  默认值: PRE
  最小值: ''
  最大值: ''
```

### 16. vLinkGenUserGroupUserSection

**描述**: Specifies an user code section that is generated into the linker script at the specified position.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenUserGroupUserSectionPosition
  长名称: Position
  描述: |
    Specifies the position of the user code section within the user code group.
    If equal, the generation order depends on the order of the sections within the configuration
    file.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenUserGroupUserSectionValue
  长名称: Value
  描述: Specifies the compiler specific user code that is directly generated into the linker script.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 17. vLinkGenLinkerMemoryRegion

**描述**: This container includes all configuration parameters for one memory region.
Memory regions has to be mapped to concrete hardware regions which are predefined in vBaseEnv.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenMemoryRegionAddrOffset
  长名称: Offset
  描述: |
    Specifies the offset of the memory rergion to the referenced hardware region start address.
    
    Memory Region Start Address = Hardware Region Start Address + Address Offset
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenMemoryRegionSize
  长名称: Size
  描述: This value specifies the size of the memory region in bytes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 18. vLinkGenMemoryRegionBlock

**描述**: This container includes all configuration parameters for a memory region block.
Memory region blocks can be used to partition a memory region.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenMemoryRegionBlockPosition
  长名称: Position
  描述: |
    This value specifies the position of the memory region block within the memory region.
    
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenMemoryRegionBlockSize
  长名称: Size
  描述: This value specifies the size of the memory region block in bytes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenMemoryRegionBlockBoundary
  长名称: Boundary
  描述: |
    This value defines the boundary of the memory region block.
    
    LOWER: The memory region block is linked to the lower boundary of the memory region
    UPPER: The memory region block is linked to the upper boundary of the memory region
  默认值: LOWER
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenMemoryRegionBlockInitPolicy
  长名称: Zero Init Policy
  描述: |
    This parameter defines whether the complete memory region block shall be initialized with zeros
    and when.
    This is typically required for ECC protected memory areas before the first read or write access.
    
    NONE: No zero initialization required.
    ALWAYS: Initialize always after the PLL initialization is done.
    HARD_RESET: Initialize after the PLL initialization is done, only if a hardware reset occured.
    FOREIGN: Initialization is done by another instance.
    STARTUP: Initialize always directly after reset. Normally only for memory region blocks
    containing the startup stack.
    
    Note:
    Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitBlocks*)
    which can be used to initialize the memory region blocks with zeros.
    This is normally done by the startup code of the vBRS.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenMemoryRegionBlockInitCore
  长名称: Init Core ID
  描述: Specifies the physical core ID which shall perform the zero initialization of the memory
      region block.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

