# vLinkGen

## 模块描述

The MICROSAR linker script generator provides an abstract way to create compiler specfic linker
scripts, so that code, constants and variables (linker symbols) in a binary are placed at the
intended location in the target memory (e.g. ROM, RAM, etc.).
The basic idea of vLinkGen is to have a compiler independent description of the linker script to be
able to apply it in a similar way for several projects.
#Memory #MemoryMapping
#Vector

## 容器列表

### 1. vLinkGenGeneral

**描述**: General configuration parameters of the vLinkGen.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenFileGeneration
  长名称: File Generation
  描述: |
    Specifies how the linker script shall be generated. The different types of generation are
    described below.
    
    STANDARD:
    Generate one complete compiler specific linker script.
    Logical groups that are assigned to one or more variants are encapsulated with C preprocessor
    macros.
    If variants are configured, this file may need to be preprocessed before it can be passed to the
    linker.
    This applies to all linkers that do not have their own preprocessor that can resolve C
    preprocessor macros (e.g. #ifdef ...).
    The name of the generated linker script is: 'vLinkGen_Template.<ext>'
    
    ONE_FILE_PER_VARIANT:
    Generate complete linker scripts per variant containing all Logical Groups assigned to the
    variant as well as all without a variant.
    They can be used as they are and passed to the linker.
    These files are generated as follows: 'vLinkGen_Template_<VariantName>.<ext>'
    
    MODULE_SNIPPETS:
    Generate several linker script snippets containing all Logical Groups (including all Section
    Groups) with a module reference. See notes below.
    These snippets are generated as follows: 'vLinkGen_Inc_<ModuleName>.<ext>'
    
    VARIANT_SNIPPETS:
    Generate several linker script snippets containing all Logical Groups (including all Section
    Groups) of a variant. See notes below.
    These snippets are generated as follows: 'vLinkGen_Inc_<VariantName>.<ext>'
    
    LOGICAL_GROUP_SNIPPETS:
    Generate several linker script snippets containing all Section Groups of a Logical Group. See
    notes below.
    These snippets are generated as follows: 'vLinkGen_Inc_<LogicalGroupName>.<ext>'
    
    Note:
    - Snippets are not supported by all compilers.
    - Snippets only contain the corresponding logical groups and nothing else.
    - Snippets cannot be passed directly to the linker. They must be included by other linker
    scripts.
      However, the names of the Memory Region Blocks (e.g. FLASH) must match the memory definitions
    from the linker script into which the snippets are to be included.
    - If variants are configured, logical groups inside the snippets are encapsulated the same way
    as for STANDARD generation.
    - Snippets never contain memory definitions and global (Pre/Post) user groups.
    - <ext> means the compiler specific file extension of the linker script.
  默认值: STANDARD
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenEntrySymbol
  长名称: Startup Entry Symbol
  描述: |
    Defines the symbol for the startup entry. This symbol is required by some compilers to define
    the entry point of the program code.
    
    Note:
    This parameter is currently only evaluated in projects with Tasking Compiler.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenUserConfigFile
  长名称: User Config File
  描述: |
    Reference to an external text file that will be included during generation to vLinkGen_Cfg.h.
    The content of the user configuration file will be added at the beginning of the generated
    module configuration file and allows altering or extending the generated code.
    
    Note:
    In contrast to the other MICROSAR components, vLinkGen inserts the user config file at the
    beginning of vLinkGen_Cfg.h.
    This is necessary to make possible defined variant macros also known in the file itself.
    
    Caution:
    User configuration files can cause the software module to malfunction and must only be used with
    great care!
  默认值: ''
  最小值: ''
  最大值: ''
```

### 2. vLinkGenMemLayout

**描述**: Container to structure all memory layout relevant configuration parameters.

该容器没有参数。

### 3. vLinkGenLinkerSections

**描述**: Container to structure the configuration parameters of the different Linker Section types.

Note:
Linker Sections are comparable to so called input sections from (some) compiler manuals.

该容器没有参数。

### 4. vLinkGenLinkerCodeSection

**描述**: This container includes all configuration parameters for a CODE Linker Section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerCodeSectionName
  长名称: Name
  描述: |
    This parameter specifies the name of the Linker Section to be generated in the linker script.
    
    Note:
    Preceding periods ('.') need not be specified here. They will be added by vLinkGen if necessary.
    If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerCodeSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the optional alignment of the Linker Section in bytes.
    This allows the start address of the Linker Section to be aligned accordingly after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenLinkerCodeSectionFast
  长名称: Fast Addressing
  描述: |
    Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).
    
    Note:
    This parameter is only needed for a few compilers, but should always be set correctly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenLinkerCodeSectionFiles
  长名称: Filenames
  描述: |
    Specifies the name of one ore more files from which the content of the Linker Section is to be
    linked.
    Whereby the names of individual files or archives (libraries) with the files they contain can be
    specified.
    So it is possible to place the content of a linker section only from one or more files to a
    certain position.
    
    If several files or archives are to be specified, they must be entered as a semicolon-separated
    list.
    Where an archive is defined by a name followed by parentheses. Within these parentheses, members
    of the archive can optionally be specified as a comma-separated list.
    See examples below.
    
    From this, vLinkGen generates, if necessary for the selected compiler, individual selection
    commands for each file or archive.
    For individual selection commands, the file names are generated according to their specified
    order.
    
    Examples:
    - file.o
    - file_a.o;file_b.o;file_c.o
    - lib.a()
    - lib.a(file_a.o,file_b.o)
    - lib1.a(file_*); lib2.a(*); file_?.o
    - /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
    - C:/folder/lib/lib.a(C:/folder/source/file1.o)
    
    Note:
    - The specified file or archive names will be generated as they are. The string is only split
    and whitespaces are removed.
    - That means for most compilers it is also possible to specify wildcards (*, ?) and complete
    paths.
    - Ensure that UNIX style file paths do not contain parentheses.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 5. vLinkGenLinkerConstSection

**描述**: This container includes all configuration parameters for a CONST Linker Section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerConstSectionName
  长名称: Name
  描述: |
    This parameter specifies the name of the Linker Section to be generated in the linker script.
    
    Note:
    Preceding periods ('.') need not be specified here. They will be added by vLinkGen if necessary.
    If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerConstSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the optional alignment of the Linker Section in bytes.
    This allows the start address of the Linker Section to be aligned accordingly after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenLinkerConstSectionFast
  长名称: Fast Addressing
  描述: |
    Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).
    
    Note:
    This parameter is only needed for a few compilers, but should always be set correctly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenLinkerConstSectionFiles
  长名称: Filenames
  描述: |
    Specifies the name of one ore more files from which the content of the Linker Section is to be
    linked.
    Whereby the names of individual files or archives (libraries) with the files they contain can be
    specified.
    So it is possible to place the content of a linker section only from one or more files to a
    certain position.
    
    If several files or archives are to be specified, they must be entered as a semicolon-separated
    list.
    Where an archive is defined by a name followed by parentheses. Within these parentheses, members
    of the archive can optionally be specified as a comma-separated list.
    See examples below.
    
    From this, vLinkGen generates, if necessary for the selected compiler, individual selection
    commands for each file or archive.
    For individual selection commands, the file names are generated according to their specified
    order.
    
    Examples:
    - file.o
    - file_a.o;file_b.o;file_c.o
    - lib.a()
    - lib.a(file_a.o,file_b.o)
    - lib1.a(file_*); lib2.a(*); file_?.o
    - /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
    - C:/folder/lib/lib.a(C:/folder/source/file1.o)
    
    Note:
    - The specified file or archive names will be generated as they are. The string is only split
    and whitespaces are removed.
    - That means for most compilers it is also possible to specify wildcards (*, ?) and complete
    paths.
    - Ensure that UNIX style file paths do not contain parentheses.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 6. vLinkGenLinkerVarSection

**描述**: This container includes all configuration parameters for a VAR Linker Section.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerVarSectionName
  长名称: Name
  描述: |
    This parameter specifies the name of the Linker Section to be generated in the linker script.
    
    Note:
    Preceding periods ('.') need not be specified here. They will be added by vLinkGen if necessary.
    If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerVarSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the optional alignment of the Linker Section in bytes.
    This allows the start address of the Linker Section to be aligned accordingly after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenLinkerVarSectionFast
  长名称: Fast Addressing
  描述: |
    Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).
    
    Note:
    This parameter is only needed for a few compilers, but should always be set correctly.
  默认值: false
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: vLinkGenLinkerVarSectionFiles
  长名称: Filenames
  描述: |
    Specifies the name of one ore more files from which the content of the Linker Section is to be
    linked.
    Whereby the names of individual files or archives (libraries) with the files they contain can be
    specified.
    So it is possible to place the content of a linker section only from one or more files to a
    certain position.
    
    If several files or archives are to be specified, they must be entered as a semicolon-separated
    list.
    Where an archive is defined by a name followed by parentheses. Within these parentheses, members
    of the archive can optionally be specified as a comma-separated list.
    See examples below.
    
    From this, vLinkGen generates, if necessary for the selected compiler, individual selection
    commands for each file or archive.
    For individual selection commands, the file names are generated according to their specified
    order.
    
    Examples:
    - file.o
    - file_a.o;file_b.o;file_c.o
    - lib.a()
    - lib.a(file_a.o,file_b.o)
    - lib1.a(file_*); lib2.a(*); file_?.o
    - /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
    - C:/folder/lib/lib.a(C:/folder/source/file1.o)
    
    Note:
    - The specified file or archive names will be generated as they are. The string is only split
    and whitespaces are removed.
    - That means for most compilers it is also possible to specify wildcards (*, ?) and complete
    paths.
    - Ensure that UNIX style file paths do not contain parentheses.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 7. vLinkGenLinkerStackSection

**描述**: This container includes all configuration parameters for a STACK Linker Section.

Caution:
STACK Linker Sections are special variable sections, which shall only be used by the operating
system.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerStackSectionName
  长名称: Name
  描述: |
    This parameter specifies the name of the Linker Section to be generated in the linker script.
    
    Note:
    Preceding periods ('.') need not be specified here. They will be added by vLinkGen if necessary.
    If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerStackSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the optional alignment of the Linker Section in bytes.
    This allows the start address of the Linker Section to be aligned accordingly after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 8. vLinkGenLinkerSpecSection

**描述**: This container includes all configuration parameters for a compiler specific Linker Section.

Note:
These sections are generated as configured, so the entered values must contain linker specific code.
For details, see chapter "Sections with Special Values" of the Technical Reference.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerSpecSectionValue
  长名称: Value
  描述: |
    This parameter specifies the compiler specific section value.
    
    Note:
    For details about the generation of the specific section values, see chapter "Special Section
    Generation" of the Technical Reference.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: vLinkGenLinkerSpecSectionAlignment
  长名称: Alignment
  描述: |
    This value specifies the optional alignment of the Linker Section in bytes.
    This allows the start address of the Linker Section to be aligned accordingly after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenLinkerSpecSectionPad
  长名称: Padding
  描述: This value specifies the optional padding (reserved size) of the Linker Section in bytes.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 9. vLinkGenLogicalConstGroup

**描述**: This container includes all configuration parameters for a Logical CONST Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory
Region Block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Logical Group within all Logical Groups.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
    
    Note:
    With some compilers, the actual order of the Logical Group after linking may differ from the
    configured one.
    This is a compiler limitation and cannot be influenced by vLinkGen.
  默认值: 5
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenConstGroupCore
  长名称: Core Id
  描述: |
    Specifies the physical core ID to which the Logical Group is assigned.
    Only relevant for groups with core local content. Which is defined by the optionally referenced
    Content Type.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenConstGroupInitCore
  长名称: Core Id (ROM to RAM copy)
  描述: |
    Specifies the physical core ID which shall perform the copying from ROM to RAM for all assigned
    sections.
    This applies to all sections which are assigned to an underlying Section Group with Init Policy
    set to COPY_TO_RAM.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 10. vLinkGenConstSectionGroup

**描述**: Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstSectionGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Section Group within its parent Logical Group.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenConstSectionGroupAlignment
  长名称: Alignment
  描述: This value specifies the optional start address alignment of the Section Group in bytes.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenConstSectionGroupEndAlignment
  长名称: End Alignment
  描述: |
    This value specifies the optional end (length) alignment of the Section Group in bytes.
    This allows the generated END or LIMIT labels to be aligned accordingly.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vLinkGenConstSectionGroupSize
  长名称: Group Size
  描述: |
    This value specifies the optional size of the Section Group in bytes.
    This can be used to keep an area free in the memory layout for groups without any Linker
    Sections (empty groups).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vLinkGenConstSectionGroupGapSize
  长名称: Gap Size
  描述: |
    This value specifies the size of the optional gap to be kept free after the Section Group in
    bytes.
    In order to correctly configure the MPU on some platforms, a certain area must be left free
    after the individual MPU regions. This area can be configured via this parameter.
    The vLinkGen then generates the linker script in the appropriate way so the configured area
    after the section group is kept free after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: vLinkGenConstSectionGroupInit
  长名称: Init Policy
  描述: |
    Specifies whether the Section Group shall be copied from ROM to RAM at ECU startup or not.
    This is typically used to execute code from RAM.
    
    NONE:
    Default behavior for the CONST Section Group. No copying from ROM to RAM.
    
    COPY_TO_RAM:
    Copy Section Group from ROM to RAM at ECU startup.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenConstSectionGroupInitStage
  长名称: Init Stage
  描述: |
    Specifies the stage at ECU startup for the copying of the Section Group.
    This parameter is only evaluated if the Init Policy is set to COPY_TO_RAM.
    
    NONE:
    No initialization configured.
    
    ZERO:
    Always initialized first during the default vBRS startup routine.
    
    HARD_RESET_ONLY:
    Same initialization stage as ONE. However, initialization is only done if a hardware reset
    occurred.
    
    ONE:
    Always initialized second during the default vBRS startup routine.
    By default, this value should be used if an initialization is required.
    
    TWO, THREE:
    Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall
    only be used if really necessary.
    One use case might be to reset the Wdg between the initialization of two stages.
    
  默认值: ONE
  最小值: ''
  最大值: ''
```

### 11. vLinkGenConstGroupVariantHandling

**描述**: Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section
Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

该容器没有参数。

### 12. vLinkGenConstGroupVariantSpecifics

**描述**: Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

该容器没有参数。

### 13. vLinkGenLogicalVarGroup

**描述**: This container includes all configuration parameters for a Logical VAR Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory
Region Block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Logical Group within all Logical Groups.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
    
    Note:
    With some compilers, the actual order of the Logical Group after linking may differ from the
    configured one.
    This is a compiler limitation and cannot be influenced by vLinkGen.
  默认值: 5
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenVarGroupCore
  长名称: Core Id
  描述: |
    Specifies the physical core ID to which the Logical Group is assigned.
    Only relevant for groups with core local content. Which is defined by the optionally referenced
    Content Type.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenVarGroupInitCore
  长名称: Core Id (ROM to RAM copy)
  描述: |
    Specifies the physical core ID which shall perform the initialization of all assigned INIT and
    ZERO_INIT sections.
    This applies to all sections which are assigned to an underlying Section Group with Init Policy
    set to INIT or ZERO_INIT.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 14. vLinkGenVarSectionGroup

**描述**: Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarSectionGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Section Group within its parent Logical Group.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenVarSectionGroupAlignment
  长名称: Alignment
  描述: This value specifies the optional start address alignment of the Section Group in bytes.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenVarSectionGroupEndAlignment
  长名称: End Alignment
  描述: |
    This value specifies the optional end (length) alignment of the Section Group in bytes.
    This allows the generated END or LIMIT labels to be aligned accordingly.
  默认值: 4
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vLinkGenVarSectionGroupSize
  长名称: Group Size
  描述: |
    This value specifies the optional size of the Section Group in bytes.
    This can be used to keep an area free in the memory layout for groups without any Linker
    Sections (empty groups).
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 5
  名称: vLinkGenVarSectionGroupGapSize
  长名称: Gap Size
  描述: |
    This value specifies the size of the optional gap to be kept free after the Section Group in
    bytes.
    In order to correctly configure the MPU on some platforms, a certain area must be left free
    after the individual MPU regions. This area can be configured via this parameter.
    The vLinkGen then generates the linker script in the appropriate way so the configured area
    after the section group is kept free after linking.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 6
  名称: vLinkGenVarSectionGroupInit
  长名称: Init Policy
  描述: |
    Specifies whether the Section Group shall be initialized at ECU startup or not.
    
    NONE:
    No initialization required.
    
    INIT:
    Initialize all variable data within the Section Group with predefined values (ROM to RAM copy).
    
    ZERO_INIT:
    Initialize all variable data within the Section Group with completely with zeros.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: vLinkGenVarSectionGroupInitStage
  长名称: Init Stage
  描述: |
    Specifies the stage at ECU startup for the initialization of the Section Group.
    This parameter is only evaluated if the Init Policy is set to value other than NONE.
    
    NONE:
    No initialization configured.
    
    EARLY:
    Initialize always directly after reset. Shall only be used if really necessary.
    Since the PLL might not be initialized at that time, the initialization of large areas may take
    a long time.
    Only supported for ZERO_INIT Section Groups.
    
    ZERO:
    Always initialized first during the default vBRS startup routine.
    
    HARD_RESET_ONLY:
    Same initialization stage as ONE. However, initialization is only done if a hardware reset
    occurred.
    
    ONE:
    Always initialized second during the default vBRS startup routine.
    By default, this value should be used if an initialization is required.
    
    TWO, THREE:
    Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall
    only be used if really necessary.
    One use case might be to reset the Wdg between the initialization of two stages.
    
  默认值: ONE
  最小值: ''
  最大值: ''
```

### 15. vLinkGenVarGroupVariantHandling

**描述**: Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section
Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

该容器没有参数。

### 16. vLinkGenVarGroupVariantSpecifics

**描述**: Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

该容器没有参数。

### 17. vLinkGenLogicalSymbolGroup

**描述**: This container includes all configuration parameters for a Logical Symbol Group.
Logical Symbol Groups are an abstraction layer to group multiple Linker Symbols and generate them in
the list of Logical Groups.

Note:
Some compilers expect global symbols to be defined at a certain position in the linker script. In
this case the configured position is simply ignored.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenSymbolGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Logical Group within all Logical Groups.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
    
    Note:
    With some compilers, the actual order of the Logical Group after linking may differ from the
    configured one.
    This is a compiler limitation and cannot be influenced by vLinkGen.
  默认值: 5
  最小值: 0
  最大值: 4294967295
```

### 18. vLinkGenLinkerSymbol

**描述**: This container includes all configuration parameters for a compiler independent symbol definition
which can have a name and a value.
That means it is possible to assign values to own symbols, and vLinkGen will generate these
assignments in the appropriate syntax into the linker script.

Note:
Some compilers do not support the definition of global Linker Symbols at all or only to a limited
extent.
This should be considered when using Linker Symbols. However, vLinkGen will issue warnings if a
compiler does not support them or only to a limited extent.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenLinkerSymbolPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Linker Symbol within its parent Logical Group.
    If multiple symbols have the same position, they are sorted alphabetically by their container
    names.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenLinkerSymbolName
  长名称: Name
  描述: |
    This parameter specifies the name of the symbol.
    
    Note:
    The symbol must be a valid linker symbol.
  默认值: ''
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: vLinkGenLinkerSymbolValue
  长名称: Value
  描述: This parameter specifies the value that the symbol should get.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 19. vLinkGenLogicalUserGroup

**描述**: This container includes all configuration parameters for a Logical User Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory
Region Block.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenUserGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Logical Group within all Logical Groups.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
    
    Note:
    With some compilers, the actual order of the Logical Group after linking may differ from the
    configured one.
    This is a compiler limitation and cannot be influenced by vLinkGen.
  默认值: 5
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenUserGroupPlacement
  长名称: Placement
  描述: |
    Specifies where the user code group should be generated in the linker script.
    
    PRE:
    The user code is generated at the beginning of the linker script.
    
    POST:
    The user code is generated at the end of the linker script.
    
    GROUP_LIST:
    The user code is generated within the Section Groups list at the specified position.
    If set, the Memory Region Block reference need also to be set for some compilers.
  默认值: PRE
  最小值: ''
  最大值: ''
```

### 20. vLinkGenUserSectionGroup

**描述**: Specifies an user code section that is generated into the linker script at the specified position.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenUserSectionGroupPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Section Group within its parent Logical Group.
    If multiple groups have the same position, they are sorted alphabetically by their container
    names.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenUserSectionGroupValue
  长名称: User Code
  描述: Specifies the compiler specific user code that is directly generated into the linker script.
  默认值: ''
  最小值: ''
  最大值: ''
```

### 21. vLinkGenMemoryRegion

**描述**: This container includes all configuration parameters for one Memory Region.
Memory Regions are a logical abstraction layer to separate the configuration from the actual memory
layout and to make it hardware independent.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenMemoryRegionAddrOffset
  长名称: Offset
  描述: |
    Specifies the offset of the Memory Region to the referenced hardware region start address.
    
    The resulting start address of the Memory Region is calculated from the start address of the
    hardware memory area in vBaseEnv and this offset value.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenMemoryRegionSize
  长名称: Size
  描述: |
    This value specifies the size of the Memory Region in bytes.
    
    A hardware memory area can be splitted into multiple Memory Regions in vLinkGen.
    In this the sizes of all Memory Regions must not exceed the size of the actual hardware memory
    area.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenMemoryRegionAddress
  长名称: Calculated Start Address
  描述: |
    Shows the calculated start address of the Memory Region.
    
    The displayed value is the actual start address of the Memory Region after linking.
    It is calculated from the start address of the hardware memory area in vBaseEnv and the address
    offset of the Memory Region.
    
    Caution:
    This parameter is for information only and must not be changed manually.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vLinkGenMemoryRegionAvailable
  长名称: Calculated Availability
  描述: |
    Specifies whether or not this Memory Region is available. What means the referenced Hardware
    Memory Area exists on the tested derivative or not.
    To change, either select a different Hardware Memory Area or change the tested derivative in the
    vBaseEnv configuration.
    
    Note:
    The tested derivative is defined by '/vBaseEnv/vBaseEnvGeneral/vBaseEnvTestedDerivativeRef'.
    
    Caution:
    This parameter is for information only and must not be changed manually.
  默认值: true
  最小值: ''
  最大值: ''
```

### 22. vLinkGenMemoryRegionBlock

**描述**: This container includes all configuration parameters for a Memory Region Block.
Memory Region Blocks can be used to partition a Memory Region. They are used for the actual memory
definitions in the generated linker script.

Note:
The position of a Memory Region Block in the memory area is determined by its position, size and
boundary.
The actual start addresses of several blocks within a Memory Region are calculated using these
parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenMemoryRegionBlockPosition
  长名称: Position
  描述: |
    Specifies the relative position of the Memory Region Block within its parent Memory Region.
    If multiple blocks have the same position, they are sorted alphabetically by their container
    names.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenMemoryRegionBlockSize
  长名称: Size
  描述: |
    This value specifies the size of the Memory Region Block in bytes.
    
    A Memory Region can be splitted into multiple Memory Region Blocks.
    In this the sizes of all blocks must not exceed the size of the parent Memory Region.
    
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenMemoryRegionBlockAddress
  长名称: Calculated Start Address
  描述: |
    Shows the calculated start address of the Memory Region Block.
    
    The displayed value is the actual start address of the Memory Region Block after linking.
    It is derived from the calculated start address of its parent Memory Region and its own boundary
    and position.
    
    Caution:
    This parameter is for information only and must not be changed manually.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vLinkGenMemoryRegionBlockBoundary
  长名称: Boundary
  描述: |
    This value defines the location of the memory area block within its parent memory area.
    
    Memory Region Blocks can be mapped either to the lower (lower address value) or upper (higher
    address value) end of the Memory Region.
    Their start address is then calculated based on the boundary value, their position and the size
    of their preceding blocks.
    This can be useful if, for example, between two Memory Region Blocks within a Memory Region an
    area in memory is to be left free.
    
    LOWER:
    The Memory Region Block is linked to the lower boundary of the Memory Region.
    
    UPPER:
    The Memory Region Block is linked to the upper boundary of the Memory Region.
  默认值: LOWER
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: vLinkGenMemoryRegionBlockInitStage
  长名称: Init Stage
  描述: |
    This parameter defines whether the complete Memory Region Block shall be initialized with zeros
    and when.
    This is typically required for ECC protected memory areas before the first read or write access.
    
    NONE:
    No initialization required.
    
    EARLY:
    Initialize always directly after reset. Shall only be used if really necessary.
    Since the PLL might not be initialized at that time, the initialization of large areas may take
    a long time.
    
    HARD_RESET_ONLY:
    Same initialization stage as ONE. However, initialization is only done if a hardware reset
    occurred.
    
    ONE:
    Always initialized second during the default vBRS startup routine.
    By default, this value should be used if an initialization is required.
  默认值: NONE
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: vLinkGenMemoryRegionBlockCore
  长名称: Core Id
  描述: |
    Specifies the physical core ID to which the Memory Region Block is assigned.
    Only relevant for core local Memory Region Blocks, respectively core local hardware memory
    areas.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 7
  名称: vLinkGenMemoryRegionBlockInitCore
  长名称: Core Id (zero initialization)
  描述: |
    Specifies the physical core ID which shall perform the zero initialization of the Memory Region
    Block.
    Only relevant if Init Stage is set to a value other than NONE.
  默认值: 0
  最小值: 0
  最大值: 4294967295
```

### 23. vLinkGenPublishedInformation

**描述**: Contains additional published compiler specific informations.

Caution:
This container (and all including sub-elements) must not be changed manually.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenGeneration
  长名称: ''
  描述: Defines the internal vLinkGen code generation.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 2
  名称: vLinkGenDefaultConstGroupAlignment
  长名称: Default CONST Group Start Alignment
  描述: |
    Specifies the optional default start address alignment for all CONST Section Groups in bytes.
    
    Note:
    It is only used for newly created groups that have no predefined values (e.g. recommended
    configuration).
    It can, however, be changed in the groups later.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 3
  名称: vLinkGenDefaultVarGroupAlignment
  长名称: Default VAR Group Start Alignment
  描述: |
    Specifies the optional default start address alignment for all VAR Section Groups in bytes.
    
    Note:
    It is only used for newly created groups that have no predefined values (e.g. recommended
    configuration).
    It can, however, be changed in the groups later.
  默认值: 0
  最小值: 0
  最大值: 4294967295
- 
  序号: 4
  名称: vLinkGenDuplicatedLabels
  长名称: Duplicated Labels
  描述: |
    Specifies whether the vLinkGen shall generate duplicated labels or not.
    
    true: Generate additional labels with double underscores ("__") at the beginning
    false: Normal label generation. No duplicated labels
  默认值: false
  最小值: ''
  最大值: ''
```

### 24. vLinkGenRegionBlockFlags

**描述**: Collection of compiler specific Memory Region Block flags.

该容器没有参数。

### 25. vLinkGenRegionBlockFlag

**描述**: Definition of a compiler specific Memory Region Block flag.

该容器没有参数。

### 26. vLinkGenLogicalConstGroupFlags

**描述**: Collection of compiler specific Logical Group flags.

该容器没有参数。

### 27. vLinkGenLogicalConstGroupFlag

**描述**: Definition of a compiler specific Logical Group flag.

该容器没有参数。

### 28. vLinkGenConstGroupFlags

**描述**: Collection of compiler specific Section Group flags.

该容器没有参数。

### 29. vLinkGenConstGroupFlag

**描述**: Definition of a compiler specific Section Group flag.

该容器没有参数。

### 30. vLinkGenConstSectionFlags

**描述**: Collection of compiler specific Linker Section flags.

该容器没有参数。

### 31. vLinkGenConstSectionFlag

**描述**: Definition of a compiler specific Linker Section flag.

该容器没有参数。

### 32. vLinkGenLogicalVarGroupFlags

**描述**: Collection of compiler specific Logical Group flags.

该容器没有参数。

### 33. vLinkGenLogicalVarGroupFlag

**描述**: Definition of a compiler specific Logical Group flag.

该容器没有参数。

### 34. vLinkGenVarGroupFlags

**描述**: Collection of compiler specific Section Group flags.

该容器没有参数。

### 35. vLinkGenVarGroupFlag

**描述**: Definition of a compiler specific Section Group flag.

该容器没有参数。

### 36. vLinkGenVarSectionFlags

**描述**: Collection of compiler specific Linker Section flags.

该容器没有参数。

### 37. vLinkGenVarSectionFlag

**描述**: Definition of a compiler specific Linker Section flag.

该容器没有参数。

### 38. vLinkGenSpecSectionFlags

**描述**: Collection of compiler specific Linker Section flags.

该容器没有参数。

### 39. vLinkGenSpecSectionFlag

**描述**: Definition of a compiler specific Linker Section flag.

该容器没有参数。

### 40. vLinkGenVariantHandling

**描述**: This container contains all configuration parameters for the variant handling.

Caution:
If variants are configured, exactly one of them must always be defined in a build process.
For example, by passing it as compiler and/or linker option (e.g. -D<VariantName>).

该容器没有参数。

### 41. vLinkGenVariant

**描述**: This container specifies one linker script variant.

该容器没有参数。

### 42. vLinkGenContentTypes

**描述**: This container contains all content types.

Content types can be used to automatically assign Logical Groups to an appropriate Memory Region
Block depending on their expected content.


Note:
The vLinkGen comes with a predefined set of default content types. However, it is always possible to
define additional ones.

该容器没有参数。

### 43. vLinkGenConstContentType

**描述**: Definition of a constant (code or data) content type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenConstContentTypeLocal
  长名称: Core Local Content
  描述: Specifies whether or not this type of content has to be linked to a core local Memory Region,
      respectively a core local hardware memory area.
  默认值: false
  最小值: ''
  最大值: ''
```

### 44. vLinkGenVarContentType

**描述**: Definition of a variable (data) content type.

#### 参数列表

```yaml
- 
  序号: 1
  名称: vLinkGenVarContentTypeLocal
  长名称: Core Local Content
  描述: Specifies whether or not this type of content has to be linked to a core local Memory Region,
      respectively a core local hardware memory area.
  默认值: false
  最小值: ''
  最大值: ''
```

