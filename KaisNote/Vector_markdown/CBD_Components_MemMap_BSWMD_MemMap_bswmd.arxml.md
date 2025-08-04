# MemMap

## 模块描述

The Memory Mapping (MemMap) module is used to generate memory mapping
header files for BSW modules as well as SWCs. These files control
the assigment of code, constants and variables to linker sections.
#Memory #MemoryMapping
#AUTOSAR

## 容器列表

### 1. MemMapAddressingModeSet

**描述**: Defines a set of addressing modes which might apply to a SwAddrMethod.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapCompilerMemClassSymbolImpl
  长名称: ''
  描述: |
    Defines the implementation behind a MemClassSymbol and configures the Compiler Abstraction.
    
    Note: Parameter not used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapSupportedAddressingMethodOption
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapSupportedMemoryAllocationKeywordPolicy
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemMapSupportedSectionInitializationPolicy
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: MemMapSupportedSectionType
  长名称: ''
  描述: This constrains the usage of this addressing mode set for Generic Mappings to swAddrMethods.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. MemMapAddressingMode

**描述**: Defines a addressing mode with a set of #pragma statements implementing the start and the stop of a
section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapAddressingModeStart
  长名称: ''
  描述: Defines a set of #pragma statements implementing the start of a section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapAddressingModeStop
  长名称: ''
  描述: Defines a set of #pragma statements implementing the start of a section.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapAlignmentSelector
  长名称: ''
  描述: Defines a the alignments for which the MemMapAddressingMode applies.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 3. MemMapAllocation

**描述**: Defines which MemorySection of a BSW Module or a Software Component is implemented with which
MemMapAddressingModeSet.

该容器没有参数。

### 4. MemMapGenericMapping

**描述**: Defines which SwAddrMethod is implemented with which MemMapAddressingModeSet.

该容器没有参数。

### 5. MemMapMappingSelector

**描述**: The container holds a section criteria reusable for MemMapGenericMappings.

Note: Container not used.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapPrefixSelector
  长名称: ''
  描述: |
    The parameter MemMapPrefixSelector defines a regular expression which shall be applied to the
    <PREFIX> part of the memory allocation keywords.
    
    Note: Parameter not used.
    
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. MemMapSectionSpecificMapping

**描述**: Defines which MemorySection of a BSW Module or a Software Component is implemented with which
MemMapAddressingModeSet.

该容器没有参数。

### 7. MemMapAdditionalSpecificMapping

**描述**: Defines which AdditionalMemorySection is implemented with which MemMapAddressingModeSet.

该容器没有参数。

### 8. MemMapGenericCompilerMemClass

**描述**: The shortName of the container defines the name of the generic Compiler memclass which is global for
all using modules, e.g. REGSPACE.

Note: Container not used.


#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapGenericCompilerMemClassSymbolImpl
  长名称: ''
  描述: |
    Defines the implementation behind the generic MemClassSymbol and configures the Compiler
    Abstraction.
    
    Note: Parameter not used.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 9. MemMapGeneral

**描述**: General configuration parameters of the MemMap.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapGeneration
  长名称: MemMap Generation
  描述: |
    Specifies how the module specific memory mapping header file(s) shall be generated.
    
    FULL:
    Generates a memory mapping header file for each BSW module and software component type
    in the project that has MemorySections configured. In addition the
    MemMapAdditionalMemorySection(s)
    are generated into their respective files.
    
    EMPTY:
    Creates the same files as with the generation type FULL. However, the files will be empty in
    this case.
    
    USER_CONFIG_ONLY:
    Creates the same files as with the generation type FULL. However, the files will only contain
    the contents
    of 'Pre User Config File' and 'Post User Config File'.
    
    NON:
    None of the files that would be generated with generation type FULL will be created.
  默认值: FULL
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapCompatibilityGeneration
  长名称: MemMap Compatibility Generation
  描述: |
    Specifies if and how the compatibility memory mapping header file (MemMap_Compatibility.h) shall
    be generated.
    
    FULL:
    Generates a compatibility memory mapping header file that contains the MemorySections of all BSW
    modules in the project.
    
    EMPTY:
    Generates a compatibility memory mapping header file that is empty.
    
    USER_CONFIG_ONLY:
    Generates a compatibility memory mapping header file that only contains the contents of 'Pre
    User Config File' and 'Post User Config File'.
    
    NON:
    No compatibility memory mapping header file will be generated.
  默认值: FULL
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapTypedPragmas
  长名称: Generate Typed Pragmas
  描述: |
    Specifies whether pragmas are generated with types.
    Pragmas that are entered manually are not affected by this parameter.
    
    Note:
    This parameter only affects the automatic pragma generation for the Tasking compiler.
    The parameter should only be set to "false" when using the platform "ARM". Otherwise it should
    be set to "true".
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemMapGeneratePragmas
  长名称: Generate Pragmas
  描述: |
    Specifies whether pragmas are generated into the memory mapping header file(s).
    If set to "false" the memory mapping header file(s) will not contain any pragmas and
    therefore there will be no mapping to linker sections.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: MemMapErrorChecks
  长名称: Error Checks
  描述: |
    Specifies if and which error checks shall be added to the generated memory mapping header
    file(s).
    
    Note:
    Error checks with a higher level also include the error checks of lower levels, e.g. ALL
    includes the
    error checks of AUTOSAR.
    
    ALL (Level 2):
    All possible error checks are added to the memory mapping header file(s).
    
    AUTOSAR (Level 1):
    All error checks defined by AUTOSAR are added to the memory mapping header file(s).
    
    NON (Level 0):
    No error checks are added to the memory mapping header file(s).
  默认值: ALL
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: MemMapGeneratePragmasForNearAddressing
  长名称: Generate Pragmas For Near Addressing
  描述: |
    Specifies whether pragmas are generated for near addressing modes (e.g. sdata, sbss, sconst).
    If the near addressing mode is not necessary according to the compiler options used, generation
    can be disabled with this parameter.
  默认值: true
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: MemMapPreUserConfigFile
  长名称: Pre User Config File
  描述: |
    Reference to an external text file that will be included during generation to ANY memory mapping
    header file.
    The content of the user configuration file will be added at the beginning of the generated files
    and allows altering or extending the generated code.
    
    Note:
    In contrast to the other MICROSAR components, MemMap provides the possibility to insert user
    config files at the beginning and end of the generated memory mapping header files.
    See also 'Post User Config File'.
    
    Caution:
    User configuration files can cause the software module to malfunction and must only be used with
    great care!
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: MemMapPostUserConfigFile
  长名称: Post User Config File
  描述: |
    Reference to an external text file that will be included during generation to ANY memory mapping
    header file.
    The content of the user configuration file will be added at the end of the generated files and
    allows altering or extending the generated code.
    
    Note:
    In contrast to the other MICROSAR components, MemMap provides the possibility to insert user
    config files at the beginning and end of the generated memory mapping header files.
    See also 'Pre User Config File'.
    
    Caution:
    User configuration files can cause the software module to malfunction and must only be used with
    great care!
  默认值: ''
  最小值: ''
  最大值: ''
```

### 10. MemMapModule

**描述**: Abstraction layer for grouping AdditionalMemorySections that belong to the same module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapGenerateAdditionalMemorySections
  长名称: Generate Additional Memory Sections
  描述: |
    Specifies whether the AdditionalMemorySection(s) defined for this module should be
    generated into the memory mapping header file(s).
  默认值: true
  最小值: ''
  最大值: ''
```

### 11. MemMapAdditionalMemorySection

**描述**: Vector MemorySections that can be configured in the ECUC.

These MemorySections are generated in addition to the MemorySections
configured according to AUTOSAR.

#### 参数列表

```yaml
- 
  序号: 1
  名称: MemMapMemorySectionAlignment
  长名称: Alignment
  描述: |
    The alignment of objects within this AdditionalMemorySection.
    The following alignments are supported: BOOLEAN, 8, 16, 32, 64, UNSPECIFIED.
    
    Note:
    If this parameter is not set the default alignment "UNSPECIFIED" will be used.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: MemMapMemorySectionFileName
  长名称: Filename
  描述: |
    Specifies the name of the file this AdditionalMemorySection shall be generated into.
    
    Note:
    If this parameter is not set the MemMapModuleRef in the parent container
    MemMapModule needs to be set.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: MemMapMemorySectionPrefix
  长名称: Prefix
  描述: |
    Specifies the {PREFIX} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.
    
    Note:
    If this parameter is not set the MemMapModuleRef in the parent container
    MemMapModule needs to be set.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: MemMapMemorySectionSymbol
  长名称: Symbol
  描述: |
    Specifies the {SYMBOL} part in the memory allocation keyword {PREFIX}_(START|STOP)_SEC_{SYMBOL}.
    
    Note:
    If this parameter is not set the ShortName of the container this parameter
    is contained in will be used as {SYMBOL}.
  默认值: ''
  最小值: ''
  最大值: ''
```

