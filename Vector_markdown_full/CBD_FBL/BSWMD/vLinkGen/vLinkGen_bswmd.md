# vLinkGen - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:29

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vLinkGen](#vlinkgen)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-1.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vLinkGen

#### 基本信息

- **UUID**: `86dbbcb5-bd6a-4dd9-96a0-dd9dede7218b`
- **模块名称**: `vLinkGen`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the MICROSAR vLinkGen module.

#### 版本历史

共有 **19** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-02-07
- **发布者**: visdfe

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-11-23
- **发布者**: visces

**变更内容**:

##### 3. 版本 1.02.00

- **状态**: released
- **发布日期**: 2019-01-03
- **发布者**: virbse

**变更内容**:

##### 4. 版本 1.03.00

- **状态**: released
- **发布日期**: 2019-02-28
- **发布者**: virbse

**变更内容**:

##### 5. 版本 1.04.00

- **状态**: released
- **发布日期**: 2019-05-03
- **发布者**: virbse

**变更内容**:

##### 6. 版本 1.05.00

- **状态**: released
- **发布日期**: 2019-07-05
- **发布者**: virbse

**变更内容**:

##### 7. 版本 1.06.00

- **状态**: released
- **发布日期**: 2019-08-02
- **发布者**: virbse

**变更内容**:

##### 8. 版本 1.07.00

- **状态**: released
- **发布日期**: 2019-09-27
- **发布者**: virbse

**变更内容**:

##### 9. 版本 1.07.01

- **状态**: released
- **发布日期**: 2019-12-19
- **发布者**: virbse

**变更内容**:

##### 10. 版本 2.00.00

- **状态**: released
- **发布日期**: 2020-02-28
- **发布者**: virbse

**变更内容**:

##### 11. 版本 2.00.01

- **状态**: released
- **发布日期**: 2020-06-17
- **发布者**: virbse

**变更内容**:

##### 12. 版本 2.01.00

- **状态**: released
- **发布日期**: 2020-08-26
- **发布者**: virbse

**变更内容**:

##### 13. 版本 2.01.01

- **状态**: released
- **发布日期**: 2020-09-03
- **发布者**: virbse

**变更内容**:

##### 14. 版本 2.01.02

- **状态**: released
- **发布日期**: 2020-09-22
- **发布者**: virbse

**变更内容**:

##### 15. 版本 2.01.03

- **状态**: released
- **发布日期**: 2020-09-28
- **发布者**: virbse

**变更内容**:

##### 16. 版本 2.01.04

- **状态**: released
- **发布日期**: 2020-10-27
- **发布者**: virbse

**变更内容**:

##### 17. 版本 2.01.05

- **状态**: released
- **发布日期**: 2020-11-02
- **发布者**: virbse

**变更内容**:

##### 18. 版本 2.02.00

- **状态**: released
- **发布日期**: 2020-11-18
- **发布者**: virbse, virleh

**变更内容**:

##### 19. 版本 2.02.01

- **状态**: released
- **发布日期**: 2021-01-07
- **发布者**: virbse

**变更内容**:

#### 配置容器

本模块包含 **37** 个配置容器：

##### 1. vLinkGenGeneral

**容器属性**:

- **UUID**: `59082afe-de43-4df7-83e6-263bbf34a0b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration parameters of the vLinkGen.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. vLinkGenEntrySymbol

- **UUID**: `0fd4d310-4927-40ff-abef-74392dc42ebf`
- **参数名**: `vLinkGenEntrySymbol`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `StartupEntry`
- **描述**: Defines the symbol for the startup entry. This symbol is required by some compilers to define the entry point of the program code.

Note:
This parameter is currently only evaluated in projects with Tasking Compiler.

######## 2. vLinkGenUserConfigFile

- **UUID**: `abc743c7-4fce-4024-b132-b5e7889c3650`
- **参数名**: `vLinkGenUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external text file that will be included during generation to vLinkGen_Cfg.h.
The content of the user configuration file will be added at the beginning of the generated module configuration file and allows altering or extending the generated code.

Note:
In contrast to the other MICROSAR components, vLinkGen inserts the user config file at the beginning of vLinkGen_Cfg.h.
This is necessary to make possible defined variant macros also known in the file itself.

Caution:
User configuration files can cause the software module to malfunction and must only be used with great care!

####### ENUMERATION 类型参数

######## 1. vLinkGenFileGeneration

- **UUID**: `47407139-fa26-40bf-beeb-9d60ffa1b8e6`
- **参数名**: `vLinkGenFileGeneration`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `STANDARD`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `STANDARD` (来源: Vector Informatik)
  - `ONE_FILE_PER_VARIANT` (来源: Vector Informatik)
  - `MODULE_SNIPPETS` (来源: Vector Informatik)
  - `VARIANT_SNIPPETS` (来源: Vector Informatik)
  - `LOGICAL_GROUP_SNIPPETS` (来源: Vector Informatik)
- **描述**: Specifies how the linker script shall be generated. The different types of generation are described below.

STANDARD:
Generate one complete compiler specific linker script.
Logical groups that are assigned to one or more variants are encapsulated with C preprocessor macros.
If variants are configured, this file may need to be preprocessed before it can be passed to the linker. 
This applies to all linkers that do not have their own preprocessor that can resolve C preprocessor macros (e.g. #ifdef ...).
The name of the generated linker script is: 'vLinkGen_Template.<ext>'

ONE_FILE_PER_VARIANT:
Generate complete linker scripts per variant containing all Logical Groups assigned to the variant as well as all without a variant.
They can be used as they are and passed to the linker.
These files are generated as follows: 'vLinkGen_Template_<VariantName>.<ext>'

MODULE_SNIPPETS:
Generate several linker script snippets containing all Logical Groups (including all Section Groups) with a module reference. See notes below.
These snippets are generated as follows: 'vLinkGen_Inc_<ModuleName>.<ext>'

VARIANT_SNIPPETS:
Generate several linker script snippets containing all Logical Groups (including all Section Groups) of a variant. See notes below.
These snippets are generated as follows: 'vLinkGen_Inc_<VariantName>.<ext>'

LOGICAL_GROUP_SNIPPETS:
Generate several linker script snippets containing all Section Groups of a Logical Group. See notes below.
These snippets are generated as follows: 'vLinkGen_Inc_<LogicalGroupName>.<ext>'

Note:
- Snippets are not supported by all compilers.
- Snippets only contain the corresponding logical groups and nothing else.
- Snippets cannot be passed directly to the linker. They must be included by other linker scripts.
  However, the names of the Memory Region Blocks (e.g. FLASH) must match the memory definitions from the linker script into which the snippets are to be included.
- If variants are configured, logical groups inside the snippets are encapsulated the same way as for STANDARD generation.
- Snippets never contain memory definitions and global (Pre/Post) user groups.
- <ext> means the compiler specific file extension of the linker script.

##### 2. vLinkGenMemLayout

**容器属性**:

- **UUID**: `206c6b28-e87f-468e-ad64-7c4b11901201`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemLayout`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure all memory layout relevant configuration parameters.

###### 配置容器

本模块包含 **20** 个配置容器：

####### 1. vLinkGenLinkerSections

**容器属性**:

- **UUID**: `4e46e9f1-968e-4e87-a986-8ea535c78fbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure the configuration parameters of the different Linker Section types.

Note:
Linker Sections are comparable to so called input sections from (some) compiler manuals.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE Linker Section.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########### BOOLEAN 类型参数

############ 1. vLinkGenLinkerCodeSectionFast

- **UUID**: `9c46e17a-d9ae-45cc-92de-db19a96bedcb`
- **参数名**: `vLinkGenLinkerCodeSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

########### STRING 类型参数

############ 1. vLinkGenLinkerCodeSectionFiles

- **UUID**: `1136b7f1-f436-4be3-9fcf-6703702709ba`
- **参数名**: `vLinkGenLinkerCodeSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

########### LINKER-SYMBOL 类型参数

############ 1. vLinkGenLinkerCodeSectionName

- **UUID**: `a7d2809c-6b5a-4a9a-bb37-689c892cadb0`
- **参数名**: `vLinkGenLinkerCodeSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `text`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenLinkerCodeSectionFlag

- **UUID**: `f0b695f6-f45c-4878-b8a4-dfa76a3e41db`
- **引用名**: `vLinkGenLinkerCodeSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

########### FOREIGN-REFERENCE 类型引用

############ 1. vLinkGenLinkerCodeSectionModule

- **UUID**: `0a7eaeec-3b2e-4d04-8339-1db2f31051b2`
- **引用名**: `vLinkGenLinkerCodeSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

######### 2. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST Linker Section.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########### BOOLEAN 类型参数

############ 1. vLinkGenLinkerConstSectionFast

- **UUID**: `e7655877-dea1-4c4f-a79e-010d9ebc2dea`
- **参数名**: `vLinkGenLinkerConstSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

########### STRING 类型参数

############ 1. vLinkGenLinkerConstSectionFiles

- **UUID**: `38bd2f8f-dc58-4209-9a21-e16b0f25f4fd`
- **参数名**: `vLinkGenLinkerConstSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

########### LINKER-SYMBOL 类型参数

############ 1. vLinkGenLinkerConstSectionName

- **UUID**: `b5f5d853-c782-47b5-a161-e7d5e6dcdd11`
- **参数名**: `vLinkGenLinkerConstSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `rodata`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenLinkerConstSectionFlag

- **UUID**: `fd8e4959-090f-4ce9-bf69-46b46ed337e3`
- **引用名**: `vLinkGenLinkerConstSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

########### FOREIGN-REFERENCE 类型引用

############ 1. vLinkGenLinkerConstSectionModule

- **UUID**: `24d39de4-a3ac-412d-8caa-200bb29f2724`
- **引用名**: `vLinkGenLinkerConstSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

######### 3. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR Linker Section.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########### BOOLEAN 类型参数

############ 1. vLinkGenLinkerVarSectionFast

- **UUID**: `2a927e16-8e03-4a82-b171-e00f4ccd5525`
- **参数名**: `vLinkGenLinkerVarSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

########### STRING 类型参数

############ 1. vLinkGenLinkerVarSectionFiles

- **UUID**: `52432307-4db7-4085-9bbb-3a0f016c5647`
- **参数名**: `vLinkGenLinkerVarSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

########### LINKER-SYMBOL 类型参数

############ 1. vLinkGenLinkerVarSectionName

- **UUID**: `d38e1bc0-df92-4991-bd76-37689549d04e`
- **参数名**: `vLinkGenLinkerVarSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `data`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenLinkerVarSectionFlag

- **UUID**: `bae1e992-aa3e-423b-ae5c-d2fa446dda81`
- **引用名**: `vLinkGenLinkerVarSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

########### FOREIGN-REFERENCE 类型引用

############ 1. vLinkGenLinkerVarSectionModule

- **UUID**: `cf978dd6-ee5a-4d4c-8bf0-960a265bd84b`
- **引用名**: `vLinkGenLinkerVarSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

######### 4. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK Linker Section.

Caution:
STACK Linker Sections are special variable sections, which shall only be used by the operating system.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########### LINKER-SYMBOL 类型参数

############ 1. vLinkGenLinkerStackSectionName

- **UUID**: `c5558d41-eecc-4737-b4a7-2e0fd0ea945b`
- **参数名**: `vLinkGenLinkerStackSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `stack`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenLinkerStackSectionFlag

- **UUID**: `fd96917a-360e-487a-aaca-89cf471b2d82`
- **引用名**: `vLinkGenLinkerStackSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

########### FOREIGN-REFERENCE 类型引用

############ 1. vLinkGenLinkerStackSectionModule

- **UUID**: `03c329ad-7605-4d73-9fd1-315c8bcec759`
- **引用名**: `vLinkGenLinkerStackSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

######### 5. vLinkGenLinkerSpecSection

**容器属性**:

- **UUID**: `0617fa65-db5e-4abb-86eb-1376948a8c39`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSpecSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler specific Linker Section.

Note:
These sections are generated as configured, so the entered values must contain linker specific code. For details, see chapter "Sections with Special Values" of the Technical Reference.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerSpecSectionAlignment

- **UUID**: `4d0f6201-6011-46b4-8aac-2f0116915d18`
- **参数名**: `vLinkGenLinkerSpecSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

############ 2. vLinkGenLinkerSpecSectionPad

- **UUID**: `a4c65c14-4289-4f66-97d2-4c1534d4b73d`
- **参数名**: `vLinkGenLinkerSpecSectionPad`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional padding (reserved size) of the Linker Section in bytes.

########### STRING 类型参数

############ 1. vLinkGenLinkerSpecSectionValue

- **UUID**: `9e6f22db-98aa-4fb8-ba22-e5de9a7621cf`
- **参数名**: `vLinkGenLinkerSpecSectionValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the compiler specific section value.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenLinkerSpecSectionFlag

- **UUID**: `904c4eb4-3acd-4bcc-a90a-ffd540070c48`
- **引用名**: `vLinkGenLinkerSpecSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenSpecSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenSpecSectionFlags/vLinkGenSpecSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

########### FOREIGN-REFERENCE 类型引用

############ 1. vLinkGenLinkerSpecSectionModule

- **UUID**: `a5580389-43e3-4e39-9d45-d5db7bee5912`
- **引用名**: `vLinkGenLinkerSpecSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 2. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerCodeSectionFast

- **UUID**: `9c46e17a-d9ae-45cc-92de-db19a96bedcb`
- **参数名**: `vLinkGenLinkerCodeSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerCodeSectionFiles

- **UUID**: `1136b7f1-f436-4be3-9fcf-6703702709ba`
- **参数名**: `vLinkGenLinkerCodeSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerCodeSectionName

- **UUID**: `a7d2809c-6b5a-4a9a-bb37-689c892cadb0`
- **参数名**: `vLinkGenLinkerCodeSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `text`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerCodeSectionFlag

- **UUID**: `f0b695f6-f45c-4878-b8a4-dfa76a3e41db`
- **引用名**: `vLinkGenLinkerCodeSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerCodeSectionModule

- **UUID**: `0a7eaeec-3b2e-4d04-8339-1db2f31051b2`
- **引用名**: `vLinkGenLinkerCodeSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 3. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerConstSectionFast

- **UUID**: `e7655877-dea1-4c4f-a79e-010d9ebc2dea`
- **参数名**: `vLinkGenLinkerConstSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerConstSectionFiles

- **UUID**: `38bd2f8f-dc58-4209-9a21-e16b0f25f4fd`
- **参数名**: `vLinkGenLinkerConstSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerConstSectionName

- **UUID**: `b5f5d853-c782-47b5-a161-e7d5e6dcdd11`
- **参数名**: `vLinkGenLinkerConstSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `rodata`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerConstSectionFlag

- **UUID**: `fd8e4959-090f-4ce9-bf69-46b46ed337e3`
- **引用名**: `vLinkGenLinkerConstSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerConstSectionModule

- **UUID**: `24d39de4-a3ac-412d-8caa-200bb29f2724`
- **引用名**: `vLinkGenLinkerConstSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 4. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerVarSectionFast

- **UUID**: `2a927e16-8e03-4a82-b171-e00f4ccd5525`
- **参数名**: `vLinkGenLinkerVarSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerVarSectionFiles

- **UUID**: `52432307-4db7-4085-9bbb-3a0f016c5647`
- **参数名**: `vLinkGenLinkerVarSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerVarSectionName

- **UUID**: `d38e1bc0-df92-4991-bd76-37689549d04e`
- **参数名**: `vLinkGenLinkerVarSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `data`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerVarSectionFlag

- **UUID**: `bae1e992-aa3e-423b-ae5c-d2fa446dda81`
- **引用名**: `vLinkGenLinkerVarSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerVarSectionModule

- **UUID**: `cf978dd6-ee5a-4d4c-8bf0-960a265bd84b`
- **引用名**: `vLinkGenLinkerVarSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 5. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK Linker Section.

Caution:
STACK Linker Sections are special variable sections, which shall only be used by the operating system.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerStackSectionName

- **UUID**: `c5558d41-eecc-4737-b4a7-2e0fd0ea945b`
- **参数名**: `vLinkGenLinkerStackSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `stack`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerStackSectionFlag

- **UUID**: `fd96917a-360e-487a-aaca-89cf471b2d82`
- **引用名**: `vLinkGenLinkerStackSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerStackSectionModule

- **UUID**: `03c329ad-7605-4d73-9fd1-315c8bcec759`
- **引用名**: `vLinkGenLinkerStackSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 6. vLinkGenLinkerSpecSection

**容器属性**:

- **UUID**: `0617fa65-db5e-4abb-86eb-1376948a8c39`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSpecSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler specific Linker Section.

Note:
These sections are generated as configured, so the entered values must contain linker specific code. For details, see chapter "Sections with Special Values" of the Technical Reference.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerSpecSectionAlignment

- **UUID**: `4d0f6201-6011-46b4-8aac-2f0116915d18`
- **参数名**: `vLinkGenLinkerSpecSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########## 2. vLinkGenLinkerSpecSectionPad

- **UUID**: `a4c65c14-4289-4f66-97d2-4c1534d4b73d`
- **参数名**: `vLinkGenLinkerSpecSectionPad`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional padding (reserved size) of the Linker Section in bytes.

######### STRING 类型参数

########## 1. vLinkGenLinkerSpecSectionValue

- **UUID**: `9e6f22db-98aa-4fb8-ba22-e5de9a7621cf`
- **参数名**: `vLinkGenLinkerSpecSectionValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the compiler specific section value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerSpecSectionFlag

- **UUID**: `904c4eb4-3acd-4bcc-a90a-ffd540070c48`
- **引用名**: `vLinkGenLinkerSpecSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenSpecSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenSpecSectionFlags/vLinkGenSpecSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerSpecSectionModule

- **UUID**: `a5580389-43e3-4e39-9d45-d5db7bee5912`
- **引用名**: `vLinkGenLinkerSpecSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 7. vLinkGenLogicalConstGroup

**容器属性**:

- **UUID**: `ab65a9ff-f823-411f-b21f-520210c41419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalConstGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical CONST Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstGroupPosition

- **UUID**: `6f281aef-1545-48ad-b39f-6df49f8f0163`
- **参数名**: `vLinkGenConstGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

########## 2. vLinkGenConstGroupInitCore

- **UUID**: `5b73e106-7dd6-424c-9d2e-376d370deb1a`
- **参数名**: `vLinkGenConstGroupInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the copying of all sections (configured as COPY_TO_RAM) assigned to the Section Group from ROM to RAM.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstGroupRegion

- **UUID**: `1fc2ee6d-7403-4656-b77c-fb59f57c4c5f`
- **引用名**: `vLinkGenConstGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the ROM Memory Region Block where the containing Section Groups shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenConstGroupVariantHandling for details.

########## 2. vLinkGenConstGroupRamRegion

- **UUID**: `c10c6794-0d8e-434d-9430-1dcc6186392b`
- **引用名**: `vLinkGenConstGroupRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the RAM Memory Region Block where the containing Section Groups shall be copied to at ECU startup by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenConstGroupVariantHandling for details.

Note:
Depending on this parameter, the vLinkGen only generates a structure which can be used to copy code or constants from ROM to RAM.
This is normally done by the startup code of the vBRS. For details please refer to the TechnicalReference.

########## 3. vLinkGenConstGroupVariant

- **UUID**: `0a69152e-39d2-41b6-8d1a-c23b832d9cfa`
- **引用名**: `vLinkGenConstGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants in which this group should be used.

Note:
- If variants are configured but this group is not assigned to one, it applies to all of them.
- If it is not possible to delete a variant from the list, please check if there is a vLinkGenConstGroupVariantSpecifics subcontainer that refers to this variant.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenConstGroupModule

- **UUID**: `b64cff49-832b-4637-9734-b48694bf12ff`
- **引用名**: `vLinkGenConstGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vLinkGenConstSectionGroup

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenConstSectionGroupPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

############ 2. vLinkGenConstSectionGroupAlignment

- **UUID**: `8059a6cc-ee09-4d99-a3c5-f4757b516d71`
- **参数名**: `vLinkGenConstSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

############ 3. vLinkGenConstSectionGroupEndAlignment

- **UUID**: `cb0bf2be-1db7-43a1-8cba-f44fac7cace9`
- **参数名**: `vLinkGenConstSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

############ 4. vLinkGenConstSectionGroupSize

- **UUID**: `d4de87e8-9701-4121-aadf-0a9eaf00faca`
- **参数名**: `vLinkGenConstSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

############ 5. vLinkGenConstSectionGroupGapSize

- **UUID**: `412a475e-5dba-46bf-9027-563acbad6035`
- **参数名**: `vLinkGenConstSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

########### ENUMERATION 类型参数

############ 1. vLinkGenConstSectionGroupInit

- **UUID**: `2f450cc3-5518-4b52-8518-a8762e38b1b3`
- **参数名**: `vLinkGenConstSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `COPY_TO_RAM` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be copied from ROM to RAM at ECU startup or not.
This is typically used to execute code from RAM.

NONE:
Default behavior for the CONST Section Group. No copying from ROM to RAM.

COPY_TO_RAM:
Copy Section Group from ROM to RAM at ECU startup.

############ 2. vLinkGenConstSectionGroupInitStage

- **UUID**: `a915d76d-1755-45f8-bfba-26b9816f31b0`
- **参数名**: `vLinkGenConstSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the copying of the Section Group.
This parameter is only evaluated if the Init Policy is set to COPY_TO_RAM.

NONE:
No initialization configured.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

########## 引用关系

此容器包含 **2** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. vLinkGenConstSectionGroupRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

############ 2. vLinkGenConstSectionGroupFlag

- **UUID**: `1d57c78d-c0a3-4189-b707-bc1dad01efa2`
- **引用名**: `vLinkGenConstSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstGroupFlags/vLinkGenConstGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

######### 2. vLinkGenConstGroupVariantHandling

**容器属性**:

- **UUID**: `af91ceb9-cc0e-44ed-af6e-f1a56798b255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

############ 引用关系

此容器包含 **3** 个引用：

############# REFERENCE 类型引用

############## 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############## 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

############## 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

######### 3. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 8. vLinkGenConstSectionGroup

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstSectionGroupPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenConstSectionGroupAlignment

- **UUID**: `8059a6cc-ee09-4d99-a3c5-f4757b516d71`
- **参数名**: `vLinkGenConstSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

########## 3. vLinkGenConstSectionGroupEndAlignment

- **UUID**: `cb0bf2be-1db7-43a1-8cba-f44fac7cace9`
- **参数名**: `vLinkGenConstSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

########## 4. vLinkGenConstSectionGroupSize

- **UUID**: `d4de87e8-9701-4121-aadf-0a9eaf00faca`
- **参数名**: `vLinkGenConstSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

########## 5. vLinkGenConstSectionGroupGapSize

- **UUID**: `412a475e-5dba-46bf-9027-563acbad6035`
- **参数名**: `vLinkGenConstSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

######### ENUMERATION 类型参数

########## 1. vLinkGenConstSectionGroupInit

- **UUID**: `2f450cc3-5518-4b52-8518-a8762e38b1b3`
- **参数名**: `vLinkGenConstSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `COPY_TO_RAM` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be copied from ROM to RAM at ECU startup or not.
This is typically used to execute code from RAM.

NONE:
Default behavior for the CONST Section Group. No copying from ROM to RAM.

COPY_TO_RAM:
Copy Section Group from ROM to RAM at ECU startup.

########## 2. vLinkGenConstSectionGroupInitStage

- **UUID**: `a915d76d-1755-45f8-bfba-26b9816f31b0`
- **参数名**: `vLinkGenConstSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the copying of the Section Group.
This parameter is only evaluated if the Init Policy is set to COPY_TO_RAM.

NONE:
No initialization configured.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. vLinkGenConstSectionGroupRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

########## 2. vLinkGenConstSectionGroupFlag

- **UUID**: `1d57c78d-c0a3-4189-b707-bc1dad01efa2`
- **引用名**: `vLinkGenConstSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstGroupFlags/vLinkGenConstGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

####### 9. vLinkGenConstGroupVariantHandling

**容器属性**:

- **UUID**: `af91ceb9-cc0e-44ed-af6e-f1a56798b255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 10. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 11. vLinkGenLogicalVarGroup

**容器属性**:

- **UUID**: `8b49ddd5-843c-439b-a745-971b7bf2f5c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalVarGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical VAR Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarGroupPosition

- **UUID**: `39cfef63-abe5-4308-ab2b-ba4b18c57c8e`
- **参数名**: `vLinkGenVarGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

########## 2. vLinkGenVarGroupInitCore

- **UUID**: `187b4cba-71cb-4e5d-8577-df75fb614950`
- **参数名**: `vLinkGenVarGroupInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the initialization for all INIT or ZERO_INIT sections assigned to the Section Group.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarGroupRegion

- **UUID**: `3cddb3c3-ee5b-4964-95ac-7d90dcabaf63`
- **引用名**: `vLinkGenVarGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the RAM Memory Region Block where the containing Section Groups shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenVarGroupVariantHandling for details.

########## 2. vLinkGenVarGroupRomRegion

- **UUID**: `e1b48eab-1434-4092-8b3d-b08f423f3644`
- **引用名**: `vLinkGenVarGroupRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the ROM Memory Region Block where the predefined data of the containing Section Groups variables shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenVarGroupVariantHandling for details.

Typically used for initialization of INIT data (ROM to RAM copy).

Note:
Depending on this parameter, the vLinkGen only generates a structure which can be used to initialize configured Linker Sections with concrete data.
This is normally done by the startup code of the vBRS. For details please refer to the TechnicalReference.

########## 3. vLinkGenVarGroupVariant

- **UUID**: `44ec7bf3-bb4d-4ce5-941e-90e26f74233b`
- **引用名**: `vLinkGenVarGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants in which this group should be used.

Note:
- If variants are configured but this group is not assigned to one, it applies to all of them.
- If it is not possible to delete a variant from the list, please check if there is a vLinkGenVarGroupVariantSpecifics subcontainer that refers to this variant.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenVarGroupModule

- **UUID**: `0c1923e3-2fa4-4155-a551-3e9aa62efa8c`
- **引用名**: `vLinkGenVarGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vLinkGenVarSectionGroup

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenVarSectionGroupPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

############ 2. vLinkGenVarSectionGroupAlignment

- **UUID**: `f823dec9-f76a-4255-b67e-ea070b38345e`
- **参数名**: `vLinkGenVarSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

############ 3. vLinkGenVarSectionGroupEndAlignment

- **UUID**: `4852b354-a36e-474b-8853-3b792f27d17c`
- **参数名**: `vLinkGenVarSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

############ 4. vLinkGenVarSectionGroupSize

- **UUID**: `c4182c49-a2a5-4447-856e-1516e5a7e5f1`
- **参数名**: `vLinkGenVarSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

############ 5. vLinkGenVarSectionGroupGapSize

- **UUID**: `eef518cc-a439-4b8e-899b-6a4ce28f9409`
- **参数名**: `vLinkGenVarSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

########### ENUMERATION 类型参数

############ 1. vLinkGenVarSectionGroupInit

- **UUID**: `bc9d56fe-986a-4919-be00-01b67614db27`
- **参数名**: `vLinkGenVarSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INIT` (来源: Vector Informatik)
  - `ZERO_INIT` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be initialized at ECU startup or not.

NONE:
No initialization required.

INIT:
Initialize all variable data within the Section Group with predefined values (ROM to RAM copy).

ZERO_INIT:
Initialize all variable data within the Section Group with completely with zeros.

############ 2. vLinkGenVarSectionGroupInitStage

- **UUID**: `cbdc9e29-6ad3-493d-9829-33f52acf5b21`
- **参数名**: `vLinkGenVarSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the initialization of the Section Group.
This parameter is only evaluated if the Init Policy is set to value other than NONE.

NONE:
No initialization configured.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.
Only supported for ZERO_INIT Section Groups.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

########## 引用关系

此容器包含 **2** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. vLinkGenVarSectionGroupRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

############ 2. vLinkGenVarSectionGroupFlag

- **UUID**: `16954758-1aec-4579-8769-4c1a7e6c687e`
- **引用名**: `vLinkGenVarSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarGroupFlags/vLinkGenVarGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

######### 2. vLinkGenVarGroupVariantHandling

**容器属性**:

- **UUID**: `f6f3b789-0fa8-462b-97c8-e902941b1bc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

############ 引用关系

此容器包含 **3** 个引用：

############# REFERENCE 类型引用

############## 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############## 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

############## 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

######### 3. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 12. vLinkGenVarSectionGroup

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarSectionGroupPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenVarSectionGroupAlignment

- **UUID**: `f823dec9-f76a-4255-b67e-ea070b38345e`
- **参数名**: `vLinkGenVarSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

########## 3. vLinkGenVarSectionGroupEndAlignment

- **UUID**: `4852b354-a36e-474b-8853-3b792f27d17c`
- **参数名**: `vLinkGenVarSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

########## 4. vLinkGenVarSectionGroupSize

- **UUID**: `c4182c49-a2a5-4447-856e-1516e5a7e5f1`
- **参数名**: `vLinkGenVarSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

########## 5. vLinkGenVarSectionGroupGapSize

- **UUID**: `eef518cc-a439-4b8e-899b-6a4ce28f9409`
- **参数名**: `vLinkGenVarSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

######### ENUMERATION 类型参数

########## 1. vLinkGenVarSectionGroupInit

- **UUID**: `bc9d56fe-986a-4919-be00-01b67614db27`
- **参数名**: `vLinkGenVarSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INIT` (来源: Vector Informatik)
  - `ZERO_INIT` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be initialized at ECU startup or not.

NONE:
No initialization required.

INIT:
Initialize all variable data within the Section Group with predefined values (ROM to RAM copy).

ZERO_INIT:
Initialize all variable data within the Section Group with completely with zeros.

########## 2. vLinkGenVarSectionGroupInitStage

- **UUID**: `cbdc9e29-6ad3-493d-9829-33f52acf5b21`
- **参数名**: `vLinkGenVarSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the initialization of the Section Group.
This parameter is only evaluated if the Init Policy is set to value other than NONE.

NONE:
No initialization configured.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.
Only supported for ZERO_INIT Section Groups.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. vLinkGenVarSectionGroupRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

########## 2. vLinkGenVarSectionGroupFlag

- **UUID**: `16954758-1aec-4579-8769-4c1a7e6c687e`
- **引用名**: `vLinkGenVarSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarGroupFlags/vLinkGenVarGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

####### 13. vLinkGenVarGroupVariantHandling

**容器属性**:

- **UUID**: `f6f3b789-0fa8-462b-97c8-e902941b1bc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 14. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 15. vLinkGenLogicalSymbolGroup

**容器属性**:

- **UUID**: `4e8e0822-f983-40b4-ae5c-2c30eeb6d77a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalSymbolGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical Symbol Group.
Logical Symbol Groups are an abstraction layer to group multiple Linker Symbols and generate them in the list of Logical Groups.

Note:
Some compilers expect global symbols to be defined at a certain position in the linker script. In this case the configured position is simply ignored.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenSymbolGroupPosition

- **UUID**: `9470f57f-fc97-4d2b-97a0-41e246a7dfce`
- **参数名**: `vLinkGenSymbolGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenSymbolGroupVariant

- **UUID**: `7baa5367-ae78-4bea-baae-51308545d368`
- **引用名**: `vLinkGenSymbolGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the linker script variants in which this group should be used.

Note:
If variants are configured but this group is not assigned to one, it applies to all of them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenSymbolGroupModule

- **UUID**: `c06a72c0-fdf1-44bd-bb0f-7799f4093436`
- **引用名**: `vLinkGenSymbolGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenLinkerSymbol

**容器属性**:

- **UUID**: `815ffcb1-74d6-474e-a77c-c2751c0dcaee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSymbol`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler independent symbol definition which can have a name and a value.
That means it is possible to assign values to own symbols, and vLinkGen will generate these assignments in the appropriate syntax into the linker script.

Note:
Some compilers do not support the definition of global Linker Symbols at all or only to a limited extent.
This should be considered when using Linker Symbols. However, vLinkGen will issue warnings if a compiler does not support them or only to a limited extent.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerSymbolPosition

- **UUID**: `bf59ab66-24a1-4988-9911-30e65d15d2e8`
- **参数名**: `vLinkGenLinkerSymbolPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Linker Symbol within its parent Logical Group.
If multiple symbols have the same position, they are sorted alphabetically by their container names.

########### STRING 类型参数

############ 1. vLinkGenLinkerSymbolValue

- **UUID**: `f9e91d17-49be-445a-b3ec-35989fc7fa72`
- **参数名**: `vLinkGenLinkerSymbolValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the value that the symbol should get.

########### LINKER-SYMBOL 类型参数

############ 1. vLinkGenLinkerSymbolName

- **UUID**: `ce606404-8ea4-4795-9878-28d344a8e4fb`
- **参数名**: `vLinkGenLinkerSymbolName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the name of the symbol.

Note:
The symbol must be a valid linker symbol.

####### 16. vLinkGenLinkerSymbol

**容器属性**:

- **UUID**: `815ffcb1-74d6-474e-a77c-c2751c0dcaee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSymbol`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler independent symbol definition which can have a name and a value.
That means it is possible to assign values to own symbols, and vLinkGen will generate these assignments in the appropriate syntax into the linker script.

Note:
Some compilers do not support the definition of global Linker Symbols at all or only to a limited extent.
This should be considered when using Linker Symbols. However, vLinkGen will issue warnings if a compiler does not support them or only to a limited extent.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerSymbolPosition

- **UUID**: `bf59ab66-24a1-4988-9911-30e65d15d2e8`
- **参数名**: `vLinkGenLinkerSymbolPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Linker Symbol within its parent Logical Group.
If multiple symbols have the same position, they are sorted alphabetically by their container names.

######### STRING 类型参数

########## 1. vLinkGenLinkerSymbolValue

- **UUID**: `f9e91d17-49be-445a-b3ec-35989fc7fa72`
- **参数名**: `vLinkGenLinkerSymbolValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the value that the symbol should get.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerSymbolName

- **UUID**: `ce606404-8ea4-4795-9878-28d344a8e4fb`
- **参数名**: `vLinkGenLinkerSymbolName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the name of the symbol.

Note:
The symbol must be a valid linker symbol.

####### 17. vLinkGenLogicalUserGroup

**容器属性**:

- **UUID**: `6973e9c1-cf16-46f5-be08-019313cfe6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalUserGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical User Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserGroupPosition

- **UUID**: `f41e4a9d-884e-411a-b8ff-b0332bfe6028`
- **参数名**: `vLinkGenUserGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

######### ENUMERATION 类型参数

########## 1. vLinkGenUserGroupPlacement

- **UUID**: `5aedaf13-5a69-43f0-bf22-03c25f6348c6`
- **参数名**: `vLinkGenUserGroupPlacement`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `PRE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `PRE` (来源: Vector Informatik)
  - `POST` (来源: Vector Informatik)
  - `GROUP_LIST` (来源: Vector Informatik)
- **描述**: Specifies where the user code group should be generated in the linker script.

PRE:
The user code is generated at the beginning of the linker script.

POST:
The user code is generated at the end of the linker script.

GROUP_LIST:
The user code is generated within the Section Groups list at the specified position.
If set, the Memory Region Block reference need also to be set for some compilers.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenUserGroupRegion

- **UUID**: `9371b3bd-09d7-4299-9905-481bd08f2bc2`
- **引用名**: `vLinkGenUserGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the Memory Region Block where the user Section Group should be linked to.

Note:
Only applicable if, vLinkGenUserGroupPlacement is set to GROUP_LIST and the compiler requires the configuration.

########## 2. vLinkGenUserGroupVariant

- **UUID**: `af403cbc-13af-4c42-8177-f564bd10de01`
- **引用名**: `vLinkGenUserGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the linker script variants in which this group should be used.

Note:
If variants are configured but this group is not assigned to one, it applies to all of them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenUserGroupModule

- **UUID**: `b4dfb785-ab0d-44b8-87f9-ec80de7ac902`
- **引用名**: `vLinkGenUserGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenUserSectionGroup

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenUserSectionGroupPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

########### MULTILINE-STRING 类型参数

############ 1. vLinkGenUserSectionGroupValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserSectionGroupValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

####### 18. vLinkGenUserSectionGroup

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserSectionGroupPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenUserSectionGroupValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserSectionGroupValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

####### 19. vLinkGenMemoryRegion

**容器属性**:

- **UUID**: `b5e4333c-3c89-4262-a6ee-433bce751d7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegion`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for one Memory Region.
Memory Regions are a logical abstraction layer to separate the configuration from the actual memory layout and to make it hardware independent.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenMemoryRegionAddrOffset

- **UUID**: `e18ca48d-c067-4e67-9676-fafd6f439169`
- **参数名**: `vLinkGenMemoryRegionAddrOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the offset of the memory region to the referenced hardware region start address.

The resulting start address of the Memory Region is calculated from the start address of the hardware memory area in vBaseEnv and this offset value.

########## 2. vLinkGenMemoryRegionSize

- **UUID**: `8f69cfe8-8d7f-4d6a-a49a-5f9f293adc70`
- **参数名**: `vLinkGenMemoryRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region in bytes.

A hardware memory area can be splitted into multiple Memory Regions in vLinkGen.
In this the sizes of all Memory Regions must not exceed the size of the actual hardware memory area.

########## 3. vLinkGenMemoryRegionAddress

- **UUID**: `327e4cd6-b8a2-4c03-913e-da9741f45889`
- **参数名**: `vLinkGenMemoryRegionAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region.

The displayed value is the actual start address of the Memory Region after linking.
It is calculated from the start address of the hardware memory area in vBaseEnv and the address offset of the Memory Region.

Caution:
This parameter is for information only and must not be changed manually.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenMemoryRegionHwRegion

- **UUID**: `1293eae4-9fe7-4b3b-9521-2059d7de5ceb`
- **引用名**: `vLinkGenMemoryRegionHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vBaseEnvMemLayoutHwRegion`
- **完整路径**: `/MICROSAR/vBaseEnv/vBaseEnvGeneral/vBaseEnvMemLayoutHwRegion`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the hardware memory area where the Memory Region should be mapped to.

The hardware memory areas are predefined in the vBaseEnv and cannot be changed.
They reflect the actual memory layout in the hardware.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Memory Region Block.
Memory Region Blocks can be used to partition a Memory Region. They are used for the actual memory definitions in the generated linker script.

Note:
The position of a Memory Region Block in the memory area is determined by its position, size and boundary.
The actual start addresses of several blocks within a Memory Region are calculated using these parameters.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenMemoryRegionBlockPosition

- **UUID**: `b3303934-13e7-4bb9-ab01-e518d00fa0d5`
- **参数名**: `vLinkGenMemoryRegionBlockPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Memory Region Block within its parent Memory Region.
If multiple blocks have the same position, they are sorted alphabetically by their container names.

############ 2. vLinkGenMemoryRegionBlockSize

- **UUID**: `800b2308-fb88-4aed-849f-a57ec4658829`
- **参数名**: `vLinkGenMemoryRegionBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region Block in bytes.

A Memory Region can be splitted into multiple Memory Region Blocks.
In this the sizes of all blocks must not exceed the size of the parent Memory Region.

############ 3. vLinkGenMemoryRegionBlockAddress

- **UUID**: `a7d596ff-0f27-4443-a45f-1899a261e600`
- **参数名**: `vLinkGenMemoryRegionBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region Block.

The displayed value is the actual start address of the Memory Region Block after linking.
It is derived from the calculated start address of its parent Memory Region and its own boundary and position.

Caution:
This parameter is for information only and must not be changed manually.

############ 4. vLinkGenMemoryRegionBlockInitCore

- **UUID**: `1598ebbf-97f2-4c2a-999f-eec67aad5ea7`
- **参数名**: `vLinkGenMemoryRegionBlockInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the Memory Region Block.

########### ENUMERATION 类型参数

############ 1. vLinkGenMemoryRegionBlockBoundary

- **UUID**: `802bd1fd-1dc2-4020-a6bc-e81a313684c2`
- **参数名**: `vLinkGenMemoryRegionBlockBoundary`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LOWER`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LOWER` (来源: Vector Informatik)
  - `UPPER` (来源: Vector Informatik)
- **描述**: This value defines the location of the memory area block within its parent memory area.

Memory Region Blocks can be mapped either to the lower (lower address value) or upper (higher address value) end of the Memory Region.
Their start address is then calculated based on the boundary value, their position and the size of their preceding blocks.
This can be useful if, for example, between two Memory Region Blocks within a Memory Region an area in memory is to be left free.

LOWER:
The Memory Region Block is linked to the lower boundary of the Memory Region.

UPPER:
The Memory Region Block is linked to the upper boundary of the Memory Region.

############ 2. vLinkGenMemoryRegionBlockInitStage

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete Memory Region Block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE:
No initialization required.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenMemoryRegionBlockFlag

- **UUID**: `11a14ac7-e7c5-4f2c-8ca1-7121c9e35468`
- **引用名**: `vLinkGenMemoryRegionBlockFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenRegionBlockFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenRegionBlockFlags/vLinkGenRegionBlockFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Memory Region Block.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on Memory Region Block level or the vLinkGen doesn't support them.

####### 20. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Memory Region Block.
Memory Region Blocks can be used to partition a Memory Region. They are used for the actual memory definitions in the generated linker script.

Note:
The position of a Memory Region Block in the memory area is determined by its position, size and boundary.
The actual start addresses of several blocks within a Memory Region are calculated using these parameters.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenMemoryRegionBlockPosition

- **UUID**: `b3303934-13e7-4bb9-ab01-e518d00fa0d5`
- **参数名**: `vLinkGenMemoryRegionBlockPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Memory Region Block within its parent Memory Region.
If multiple blocks have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenMemoryRegionBlockSize

- **UUID**: `800b2308-fb88-4aed-849f-a57ec4658829`
- **参数名**: `vLinkGenMemoryRegionBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region Block in bytes.

A Memory Region can be splitted into multiple Memory Region Blocks.
In this the sizes of all blocks must not exceed the size of the parent Memory Region.

########## 3. vLinkGenMemoryRegionBlockAddress

- **UUID**: `a7d596ff-0f27-4443-a45f-1899a261e600`
- **参数名**: `vLinkGenMemoryRegionBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region Block.

The displayed value is the actual start address of the Memory Region Block after linking.
It is derived from the calculated start address of its parent Memory Region and its own boundary and position.

Caution:
This parameter is for information only and must not be changed manually.

########## 4. vLinkGenMemoryRegionBlockInitCore

- **UUID**: `1598ebbf-97f2-4c2a-999f-eec67aad5ea7`
- **参数名**: `vLinkGenMemoryRegionBlockInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the Memory Region Block.

######### ENUMERATION 类型参数

########## 1. vLinkGenMemoryRegionBlockBoundary

- **UUID**: `802bd1fd-1dc2-4020-a6bc-e81a313684c2`
- **参数名**: `vLinkGenMemoryRegionBlockBoundary`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LOWER`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LOWER` (来源: Vector Informatik)
  - `UPPER` (来源: Vector Informatik)
- **描述**: This value defines the location of the memory area block within its parent memory area.

Memory Region Blocks can be mapped either to the lower (lower address value) or upper (higher address value) end of the Memory Region.
Their start address is then calculated based on the boundary value, their position and the size of their preceding blocks.
This can be useful if, for example, between two Memory Region Blocks within a Memory Region an area in memory is to be left free.

LOWER:
The Memory Region Block is linked to the lower boundary of the Memory Region.

UPPER:
The Memory Region Block is linked to the upper boundary of the Memory Region.

########## 2. vLinkGenMemoryRegionBlockInitStage

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete Memory Region Block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE:
No initialization required.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenMemoryRegionBlockFlag

- **UUID**: `11a14ac7-e7c5-4f2c-8ca1-7121c9e35468`
- **引用名**: `vLinkGenMemoryRegionBlockFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenRegionBlockFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenRegionBlockFlags/vLinkGenRegionBlockFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Memory Region Block.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on Memory Region Block level or the vLinkGen doesn't support them.

##### 3. vLinkGenLinkerSections

**容器属性**:

- **UUID**: `4e46e9f1-968e-4e87-a986-8ea535c78fbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure the configuration parameters of the different Linker Section types.

Note:
Linker Sections are comparable to so called input sections from (some) compiler manuals.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerCodeSectionFast

- **UUID**: `9c46e17a-d9ae-45cc-92de-db19a96bedcb`
- **参数名**: `vLinkGenLinkerCodeSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerCodeSectionFiles

- **UUID**: `1136b7f1-f436-4be3-9fcf-6703702709ba`
- **参数名**: `vLinkGenLinkerCodeSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerCodeSectionName

- **UUID**: `a7d2809c-6b5a-4a9a-bb37-689c892cadb0`
- **参数名**: `vLinkGenLinkerCodeSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `text`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerCodeSectionFlag

- **UUID**: `f0b695f6-f45c-4878-b8a4-dfa76a3e41db`
- **引用名**: `vLinkGenLinkerCodeSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerCodeSectionModule

- **UUID**: `0a7eaeec-3b2e-4d04-8339-1db2f31051b2`
- **引用名**: `vLinkGenLinkerCodeSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 2. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerConstSectionFast

- **UUID**: `e7655877-dea1-4c4f-a79e-010d9ebc2dea`
- **参数名**: `vLinkGenLinkerConstSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerConstSectionFiles

- **UUID**: `38bd2f8f-dc58-4209-9a21-e16b0f25f4fd`
- **参数名**: `vLinkGenLinkerConstSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerConstSectionName

- **UUID**: `b5f5d853-c782-47b5-a161-e7d5e6dcdd11`
- **参数名**: `vLinkGenLinkerConstSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `rodata`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerConstSectionFlag

- **UUID**: `fd8e4959-090f-4ce9-bf69-46b46ed337e3`
- **引用名**: `vLinkGenLinkerConstSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerConstSectionModule

- **UUID**: `24d39de4-a3ac-412d-8caa-200bb29f2724`
- **引用名**: `vLinkGenLinkerConstSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 3. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR Linker Section.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### BOOLEAN 类型参数

########## 1. vLinkGenLinkerVarSectionFast

- **UUID**: `2a927e16-8e03-4a82-b171-e00f4ccd5525`
- **参数名**: `vLinkGenLinkerVarSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

######### STRING 类型参数

########## 1. vLinkGenLinkerVarSectionFiles

- **UUID**: `52432307-4db7-4085-9bbb-3a0f016c5647`
- **参数名**: `vLinkGenLinkerVarSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerVarSectionName

- **UUID**: `d38e1bc0-df92-4991-bd76-37689549d04e`
- **参数名**: `vLinkGenLinkerVarSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `data`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerVarSectionFlag

- **UUID**: `bae1e992-aa3e-423b-ae5c-d2fa446dda81`
- **引用名**: `vLinkGenLinkerVarSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerVarSectionModule

- **UUID**: `cf978dd6-ee5a-4d4c-8bf0-960a265bd84b`
- **引用名**: `vLinkGenLinkerVarSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 4. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK Linker Section.

Caution:
STACK Linker Sections are special variable sections, which shall only be used by the operating system.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerStackSectionName

- **UUID**: `c5558d41-eecc-4737-b4a7-2e0fd0ea945b`
- **参数名**: `vLinkGenLinkerStackSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `stack`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerStackSectionFlag

- **UUID**: `fd96917a-360e-487a-aaca-89cf471b2d82`
- **引用名**: `vLinkGenLinkerStackSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerStackSectionModule

- **UUID**: `03c329ad-7605-4d73-9fd1-315c8bcec759`
- **引用名**: `vLinkGenLinkerStackSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

####### 5. vLinkGenLinkerSpecSection

**容器属性**:

- **UUID**: `0617fa65-db5e-4abb-86eb-1376948a8c39`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSpecSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler specific Linker Section.

Note:
These sections are generated as configured, so the entered values must contain linker specific code. For details, see chapter "Sections with Special Values" of the Technical Reference.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerSpecSectionAlignment

- **UUID**: `4d0f6201-6011-46b4-8aac-2f0116915d18`
- **参数名**: `vLinkGenLinkerSpecSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

########## 2. vLinkGenLinkerSpecSectionPad

- **UUID**: `a4c65c14-4289-4f66-97d2-4c1534d4b73d`
- **参数名**: `vLinkGenLinkerSpecSectionPad`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional padding (reserved size) of the Linker Section in bytes.

######### STRING 类型参数

########## 1. vLinkGenLinkerSpecSectionValue

- **UUID**: `9e6f22db-98aa-4fb8-ba22-e5de9a7621cf`
- **参数名**: `vLinkGenLinkerSpecSectionValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the compiler specific section value.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenLinkerSpecSectionFlag

- **UUID**: `904c4eb4-3acd-4bcc-a90a-ffd540070c48`
- **引用名**: `vLinkGenLinkerSpecSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenSpecSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenSpecSectionFlags/vLinkGenSpecSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

######### FOREIGN-REFERENCE 类型引用

########## 1. vLinkGenLinkerSpecSectionModule

- **UUID**: `a5580389-43e3-4e39-9d45-d5db7bee5912`
- **引用名**: `vLinkGenLinkerSpecSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 4. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE Linker Section.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

####### BOOLEAN 类型参数

######## 1. vLinkGenLinkerCodeSectionFast

- **UUID**: `9c46e17a-d9ae-45cc-92de-db19a96bedcb`
- **参数名**: `vLinkGenLinkerCodeSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

####### STRING 类型参数

######## 1. vLinkGenLinkerCodeSectionFiles

- **UUID**: `1136b7f1-f436-4be3-9fcf-6703702709ba`
- **参数名**: `vLinkGenLinkerCodeSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

####### LINKER-SYMBOL 类型参数

######## 1. vLinkGenLinkerCodeSectionName

- **UUID**: `a7d2809c-6b5a-4a9a-bb37-689c892cadb0`
- **参数名**: `vLinkGenLinkerCodeSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `text`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenLinkerCodeSectionFlag

- **UUID**: `f0b695f6-f45c-4878-b8a4-dfa76a3e41db`
- **引用名**: `vLinkGenLinkerCodeSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenLinkerCodeSectionModule

- **UUID**: `0a7eaeec-3b2e-4d04-8339-1db2f31051b2`
- **引用名**: `vLinkGenLinkerCodeSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 5. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST Linker Section.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

####### BOOLEAN 类型参数

######## 1. vLinkGenLinkerConstSectionFast

- **UUID**: `e7655877-dea1-4c4f-a79e-010d9ebc2dea`
- **参数名**: `vLinkGenLinkerConstSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

####### STRING 类型参数

######## 1. vLinkGenLinkerConstSectionFiles

- **UUID**: `38bd2f8f-dc58-4209-9a21-e16b0f25f4fd`
- **参数名**: `vLinkGenLinkerConstSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

####### LINKER-SYMBOL 类型参数

######## 1. vLinkGenLinkerConstSectionName

- **UUID**: `b5f5d853-c782-47b5-a161-e7d5e6dcdd11`
- **参数名**: `vLinkGenLinkerConstSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `rodata`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenLinkerConstSectionFlag

- **UUID**: `fd8e4959-090f-4ce9-bf69-46b46ed337e3`
- **引用名**: `vLinkGenLinkerConstSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenConstSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstSectionFlags/vLinkGenConstSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenLinkerConstSectionModule

- **UUID**: `24d39de4-a3ac-412d-8caa-200bb29f2724`
- **引用名**: `vLinkGenLinkerConstSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 6. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR Linker Section.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

####### BOOLEAN 类型参数

######## 1. vLinkGenLinkerVarSectionFast

- **UUID**: `2a927e16-8e03-4a82-b171-e00f4ccd5525`
- **参数名**: `vLinkGenLinkerVarSectionFast`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the Linker Section shall be linked for fast addressing (NEAR) or not (FAR).

Note:
This parameter is only needed for a few compilers, but should always be set correctly.

####### STRING 类型参数

######## 1. vLinkGenLinkerVarSectionFiles

- **UUID**: `52432307-4db7-4085-9bbb-3a0f016c5647`
- **参数名**: `vLinkGenLinkerVarSectionFiles`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the name of one ore more files from which the content of the Linker Section is to be linked.
Whereby the names of individual files or archives (libraries) with the files they contain can be specified.
So it is possible to place the content of a linker section only from one or more files to a certain position.

If several files or archives are to be specified, they must be entered as a semicolon-separated list.
Where an archive is defined by a name followed by parentheses. Within these parentheses, members of the archive can optionally be specified as a comma-separated list.
See examples below.

From this, vLinkGen generates, if necessary for the selected compiler, individual selection commands for each file or archive.
For individual selection commands, the file names are generated according to their specified order.

Examples:
- file.o
- file_a.o;file_b.o;file_c.o
- lib.a()
- lib.a(file_a.o,file_b.o)
- lib1.a(file_*); lib2.a(*); file_?.o
- /usr/folder/lib/lib.a(/usr/folder/source/file1.o)
- C:/folder/lib/lib.a(C:/folder/source/file1.o)

Note:
- The specified file or archive names will be generated as they are. The string is only split and whitespaces are removed.
- That means for most compilers it is also possible to specify wildcards (*, ?) and complete paths.
- Ensure that UNIX style file paths do not contain parentheses.

####### LINKER-SYMBOL 类型参数

######## 1. vLinkGenLinkerVarSectionName

- **UUID**: `d38e1bc0-df92-4991-bd76-37689549d04e`
- **参数名**: `vLinkGenLinkerVarSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `data`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenLinkerVarSectionFlag

- **UUID**: `bae1e992-aa3e-423b-ae5c-d2fa446dda81`
- **引用名**: `vLinkGenLinkerVarSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenLinkerVarSectionModule

- **UUID**: `cf978dd6-ee5a-4d4c-8bf0-960a265bd84b`
- **引用名**: `vLinkGenLinkerVarSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 7. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK Linker Section.

Caution:
STACK Linker Sections are special variable sections, which shall only be used by the operating system.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

####### LINKER-SYMBOL 类型参数

######## 1. vLinkGenLinkerStackSectionName

- **UUID**: `c5558d41-eecc-4737-b4a7-2e0fd0ea945b`
- **参数名**: `vLinkGenLinkerStackSectionName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `stack`
- **描述**: This parameter specifies the name of the Linker Section to be generated in the linker script.

Note:
Leading points (.) need not be specified here. They will be added by vLinkGen if necessary.
If sections with special values are required, a vLinkGenLinkerSpecSection can be used instead.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenLinkerStackSectionFlag

- **UUID**: `fd96917a-360e-487a-aaca-89cf471b2d82`
- **引用名**: `vLinkGenLinkerStackSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVarSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarSectionFlags/vLinkGenVarSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenLinkerStackSectionModule

- **UUID**: `03c329ad-7605-4d73-9fd1-315c8bcec759`
- **引用名**: `vLinkGenLinkerStackSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 8. vLinkGenLinkerSpecSection

**容器属性**:

- **UUID**: `0617fa65-db5e-4abb-86eb-1376948a8c39`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSpecSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler specific Linker Section.

Note:
These sections are generated as configured, so the entered values must contain linker specific code. For details, see chapter "Sections with Special Values" of the Technical Reference.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerSpecSectionAlignment

- **UUID**: `4d0f6201-6011-46b4-8aac-2f0116915d18`
- **参数名**: `vLinkGenLinkerSpecSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional alignment of the Linker Section in bytes.
This allows the start address of the Linker Section to be aligned accordingly after linking.

######## 2. vLinkGenLinkerSpecSectionPad

- **UUID**: `a4c65c14-4289-4f66-97d2-4c1534d4b73d`
- **参数名**: `vLinkGenLinkerSpecSectionPad`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional padding (reserved size) of the Linker Section in bytes.

####### STRING 类型参数

######## 1. vLinkGenLinkerSpecSectionValue

- **UUID**: `9e6f22db-98aa-4fb8-ba22-e5de9a7621cf`
- **参数名**: `vLinkGenLinkerSpecSectionValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the compiler specific section value.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenLinkerSpecSectionFlag

- **UUID**: `904c4eb4-3acd-4bcc-a90a-ffd540070c48`
- **引用名**: `vLinkGenLinkerSpecSectionFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenSpecSectionFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenSpecSectionFlags/vLinkGenSpecSectionFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Linker Section.

Note:
The flags to be selected are predefined and cannot be changed.
If no flags are selectable, the compiler either does not support flags on section level or the vLinkGen doesn't support them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenLinkerSpecSectionModule

- **UUID**: `a5580389-43e3-4e39-9d45-d5db7bee5912`
- **引用名**: `vLinkGenLinkerSpecSectionModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Linker Section.

Note:
If this reference is set, the container is typically created by another module's generator.

##### 9. vLinkGenLogicalConstGroup

**容器属性**:

- **UUID**: `ab65a9ff-f823-411f-b21f-520210c41419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalConstGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical CONST Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenConstGroupPosition

- **UUID**: `6f281aef-1545-48ad-b39f-6df49f8f0163`
- **参数名**: `vLinkGenConstGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

######## 2. vLinkGenConstGroupInitCore

- **UUID**: `5b73e106-7dd6-424c-9d2e-376d370deb1a`
- **参数名**: `vLinkGenConstGroupInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the copying of all sections (configured as COPY_TO_RAM) assigned to the Section Group from ROM to RAM.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenConstGroupRegion

- **UUID**: `1fc2ee6d-7403-4656-b77c-fb59f57c4c5f`
- **引用名**: `vLinkGenConstGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the ROM Memory Region Block where the containing Section Groups shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenConstGroupVariantHandling for details.

######## 2. vLinkGenConstGroupRamRegion

- **UUID**: `c10c6794-0d8e-434d-9430-1dcc6186392b`
- **引用名**: `vLinkGenConstGroupRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the RAM Memory Region Block where the containing Section Groups shall be copied to at ECU startup by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenConstGroupVariantHandling for details.

Note:
Depending on this parameter, the vLinkGen only generates a structure which can be used to copy code or constants from ROM to RAM.
This is normally done by the startup code of the vBRS. For details please refer to the TechnicalReference.

######## 3. vLinkGenConstGroupVariant

- **UUID**: `0a69152e-39d2-41b6-8d1a-c23b832d9cfa`
- **引用名**: `vLinkGenConstGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants in which this group should be used.

Note:
- If variants are configured but this group is not assigned to one, it applies to all of them.
- If it is not possible to delete a variant from the list, please check if there is a vLinkGenConstGroupVariantSpecifics subcontainer that refers to this variant.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenConstGroupModule

- **UUID**: `b64cff49-832b-4637-9734-b48694bf12ff`
- **引用名**: `vLinkGenConstGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vLinkGenConstSectionGroup

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstSectionGroupPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenConstSectionGroupAlignment

- **UUID**: `8059a6cc-ee09-4d99-a3c5-f4757b516d71`
- **参数名**: `vLinkGenConstSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

########## 3. vLinkGenConstSectionGroupEndAlignment

- **UUID**: `cb0bf2be-1db7-43a1-8cba-f44fac7cace9`
- **参数名**: `vLinkGenConstSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

########## 4. vLinkGenConstSectionGroupSize

- **UUID**: `d4de87e8-9701-4121-aadf-0a9eaf00faca`
- **参数名**: `vLinkGenConstSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

########## 5. vLinkGenConstSectionGroupGapSize

- **UUID**: `412a475e-5dba-46bf-9027-563acbad6035`
- **参数名**: `vLinkGenConstSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

######### ENUMERATION 类型参数

########## 1. vLinkGenConstSectionGroupInit

- **UUID**: `2f450cc3-5518-4b52-8518-a8762e38b1b3`
- **参数名**: `vLinkGenConstSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `COPY_TO_RAM` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be copied from ROM to RAM at ECU startup or not.
This is typically used to execute code from RAM.

NONE:
Default behavior for the CONST Section Group. No copying from ROM to RAM.

COPY_TO_RAM:
Copy Section Group from ROM to RAM at ECU startup.

########## 2. vLinkGenConstSectionGroupInitStage

- **UUID**: `a915d76d-1755-45f8-bfba-26b9816f31b0`
- **参数名**: `vLinkGenConstSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the copying of the Section Group.
This parameter is only evaluated if the Init Policy is set to COPY_TO_RAM.

NONE:
No initialization configured.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. vLinkGenConstSectionGroupRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

########## 2. vLinkGenConstSectionGroupFlag

- **UUID**: `1d57c78d-c0a3-4189-b707-bc1dad01efa2`
- **引用名**: `vLinkGenConstSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstGroupFlags/vLinkGenConstGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

####### 2. vLinkGenConstGroupVariantHandling

**容器属性**:

- **UUID**: `af91ceb9-cc0e-44ed-af6e-f1a56798b255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 3. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 10. vLinkGenConstSectionGroup

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenConstSectionGroupPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

######## 2. vLinkGenConstSectionGroupAlignment

- **UUID**: `8059a6cc-ee09-4d99-a3c5-f4757b516d71`
- **参数名**: `vLinkGenConstSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

######## 3. vLinkGenConstSectionGroupEndAlignment

- **UUID**: `cb0bf2be-1db7-43a1-8cba-f44fac7cace9`
- **参数名**: `vLinkGenConstSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

######## 4. vLinkGenConstSectionGroupSize

- **UUID**: `d4de87e8-9701-4121-aadf-0a9eaf00faca`
- **参数名**: `vLinkGenConstSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

######## 5. vLinkGenConstSectionGroupGapSize

- **UUID**: `412a475e-5dba-46bf-9027-563acbad6035`
- **参数名**: `vLinkGenConstSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

####### ENUMERATION 类型参数

######## 1. vLinkGenConstSectionGroupInit

- **UUID**: `2f450cc3-5518-4b52-8518-a8762e38b1b3`
- **参数名**: `vLinkGenConstSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `COPY_TO_RAM` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be copied from ROM to RAM at ECU startup or not.
This is typically used to execute code from RAM.

NONE:
Default behavior for the CONST Section Group. No copying from ROM to RAM.

COPY_TO_RAM:
Copy Section Group from ROM to RAM at ECU startup.

######## 2. vLinkGenConstSectionGroupInitStage

- **UUID**: `a915d76d-1755-45f8-bfba-26b9816f31b0`
- **参数名**: `vLinkGenConstSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the copying of the Section Group.
This parameter is only evaluated if the Init Policy is set to COPY_TO_RAM.

NONE:
No initialization configured.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

###### 引用关系

此容器包含 **2** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. vLinkGenConstSectionGroupRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

######## 2. vLinkGenConstSectionGroupFlag

- **UUID**: `1d57c78d-c0a3-4189-b707-bc1dad01efa2`
- **引用名**: `vLinkGenConstSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenConstGroupFlags/vLinkGenConstGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

##### 11. vLinkGenConstGroupVariantHandling

**容器属性**:

- **UUID**: `af91ceb9-cc0e-44ed-af6e-f1a56798b255`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 12. vLinkGenConstGroupVariantSpecifics

**容器属性**:

- **UUID**: `d046d9f3-fcca-4db3-a481-5e534d5fcc46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenConstGroupVariantHandling description for details.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenConstGroupSpecificRegion

- **UUID**: `0adb1a87-a4e4-4bcc-bc56-aac19783026a`
- **引用名**: `vLinkGenConstGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

######## 2. vLinkGenConstGroupSpecificRamRegion

- **UUID**: `93c1b9c4-c03b-40c7-815e-cdc2be3fffaa`
- **引用名**: `vLinkGenConstGroupSpecificRamRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (RAM Copy) from the parent Logical Group in the variants listed below.

######## 3. vLinkGenConstGroupSpecificVariant

- **UUID**: `c111bd81-385c-4f6c-a04a-91971ced3e7d`
- **引用名**: `vLinkGenConstGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 13. vLinkGenLogicalVarGroup

**容器属性**:

- **UUID**: `8b49ddd5-843c-439b-a745-971b7bf2f5c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalVarGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical VAR Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenVarGroupPosition

- **UUID**: `39cfef63-abe5-4308-ab2b-ba4b18c57c8e`
- **参数名**: `vLinkGenVarGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

######## 2. vLinkGenVarGroupInitCore

- **UUID**: `187b4cba-71cb-4e5d-8577-df75fb614950`
- **参数名**: `vLinkGenVarGroupInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the initialization for all INIT or ZERO_INIT sections assigned to the Section Group.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenVarGroupRegion

- **UUID**: `3cddb3c3-ee5b-4964-95ac-7d90dcabaf63`
- **引用名**: `vLinkGenVarGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the RAM Memory Region Block where the containing Section Groups shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenVarGroupVariantHandling for details.

######## 2. vLinkGenVarGroupRomRegion

- **UUID**: `e1b48eab-1434-4092-8b3d-b08f423f3644`
- **引用名**: `vLinkGenVarGroupRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the ROM Memory Region Block where the predefined data of the containing Section Groups variables shall be linked to by default.
Where default means, in case it is not specifically overwritten for variants. See optional vLinkGenVarGroupVariantHandling for details.

Typically used for initialization of INIT data (ROM to RAM copy).

Note:
Depending on this parameter, the vLinkGen only generates a structure which can be used to initialize configured Linker Sections with concrete data.
This is normally done by the startup code of the vBRS. For details please refer to the TechnicalReference.

######## 3. vLinkGenVarGroupVariant

- **UUID**: `44ec7bf3-bb4d-4ce5-941e-90e26f74233b`
- **引用名**: `vLinkGenVarGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants in which this group should be used.

Note:
- If variants are configured but this group is not assigned to one, it applies to all of them.
- If it is not possible to delete a variant from the list, please check if there is a vLinkGenVarGroupVariantSpecifics subcontainer that refers to this variant.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenVarGroupModule

- **UUID**: `0c1923e3-2fa4-4155-a551-3e9aa62efa8c`
- **引用名**: `vLinkGenVarGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vLinkGenVarSectionGroup

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarSectionGroupPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenVarSectionGroupAlignment

- **UUID**: `f823dec9-f76a-4255-b67e-ea070b38345e`
- **参数名**: `vLinkGenVarSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

########## 3. vLinkGenVarSectionGroupEndAlignment

- **UUID**: `4852b354-a36e-474b-8853-3b792f27d17c`
- **参数名**: `vLinkGenVarSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

########## 4. vLinkGenVarSectionGroupSize

- **UUID**: `c4182c49-a2a5-4447-856e-1516e5a7e5f1`
- **参数名**: `vLinkGenVarSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

########## 5. vLinkGenVarSectionGroupGapSize

- **UUID**: `eef518cc-a439-4b8e-899b-6a4ce28f9409`
- **参数名**: `vLinkGenVarSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

######### ENUMERATION 类型参数

########## 1. vLinkGenVarSectionGroupInit

- **UUID**: `bc9d56fe-986a-4919-be00-01b67614db27`
- **参数名**: `vLinkGenVarSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INIT` (来源: Vector Informatik)
  - `ZERO_INIT` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be initialized at ECU startup or not.

NONE:
No initialization required.

INIT:
Initialize all variable data within the Section Group with predefined values (ROM to RAM copy).

ZERO_INIT:
Initialize all variable data within the Section Group with completely with zeros.

########## 2. vLinkGenVarSectionGroupInitStage

- **UUID**: `cbdc9e29-6ad3-493d-9829-33f52acf5b21`
- **参数名**: `vLinkGenVarSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the initialization of the Section Group.
This parameter is only evaluated if the Init Policy is set to value other than NONE.

NONE:
No initialization configured.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.
Only supported for ZERO_INIT Section Groups.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

######## 引用关系

此容器包含 **2** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. vLinkGenVarSectionGroupRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

########## 2. vLinkGenVarSectionGroupFlag

- **UUID**: `16954758-1aec-4579-8769-4c1a7e6c687e`
- **引用名**: `vLinkGenVarSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarGroupFlags/vLinkGenVarGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

####### 2. vLinkGenVarGroupVariantHandling

**容器属性**:

- **UUID**: `f6f3b789-0fa8-462b-97c8-e902941b1bc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

############ 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

############ 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

####### 3. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 14. vLinkGenVarSectionGroup

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies a group of Linker Sections whose content shall be linked into this Section Group.

Note:
Section Groups are comparable to output sections from (some) compiler manuals.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenVarSectionGroupPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

######## 2. vLinkGenVarSectionGroupAlignment

- **UUID**: `f823dec9-f76a-4255-b67e-ea070b38345e`
- **参数名**: `vLinkGenVarSectionGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional start address alignment of the Section Group in bytes.

######## 3. vLinkGenVarSectionGroupEndAlignment

- **UUID**: `4852b354-a36e-474b-8853-3b792f27d17c`
- **参数名**: `vLinkGenVarSectionGroupEndAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional end (length) alignment of the Section Group in bytes.
This allows the generated END or LIMIT labels to be aligned accordingly.

######## 4. vLinkGenVarSectionGroupSize

- **UUID**: `c4182c49-a2a5-4447-856e-1516e5a7e5f1`
- **参数名**: `vLinkGenVarSectionGroupSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the optional size of the Section Group in bytes.
This can be used to keep an area free in the memory layout for groups without any Linker Sections (empty groups).

######## 5. vLinkGenVarSectionGroupGapSize

- **UUID**: `eef518cc-a439-4b8e-899b-6a4ce28f9409`
- **参数名**: `vLinkGenVarSectionGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the Section Group in bytes.
In order to correctly configure the MPU on some platforms, a certain area must be left free after the individual MPU regions. This area can be configured via this parameter.
The vLinkGen then generates the linker script in the appropriate way so the configured area after the section group is kept free after linking.

####### ENUMERATION 类型参数

######## 1. vLinkGenVarSectionGroupInit

- **UUID**: `bc9d56fe-986a-4919-be00-01b67614db27`
- **参数名**: `vLinkGenVarSectionGroupInit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INIT` (来源: Vector Informatik)
  - `ZERO_INIT` (来源: Vector Informatik)
- **描述**: Specifies whether the Section Group shall be initialized at ECU startup or not.

NONE:
No initialization required.

INIT:
Initialize all variable data within the Section Group with predefined values (ROM to RAM copy).

ZERO_INIT:
Initialize all variable data within the Section Group with completely with zeros.

######## 2. vLinkGenVarSectionGroupInitStage

- **UUID**: `cbdc9e29-6ad3-493d-9829-33f52acf5b21`
- **参数名**: `vLinkGenVarSectionGroupInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ZERO` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
  - `TWO` (来源: Vector Informatik)
  - `THREE` (来源: Vector Informatik)
- **描述**: Specifies the stage at ECU startup for the initialization of the Section Group.
This parameter is only evaluated if the Init Policy is set to value other than NONE.

NONE:
No initialization configured.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.
Only supported for ZERO_INIT Section Groups.

ZERO:
Always initialized first during the default vBRS startup routine.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

TWO, THREE:
Optional init stages, which are initialized accordingly after the HARD_RESET_ONLY stage. Shall only be used if really necessary.
One use case might be to reset the Wdg between the initialization of two stages.

###### 引用关系

此容器包含 **2** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. vLinkGenVarSectionGroupRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionGroupRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
  - `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerSpecSection`
- **描述**: Reference to the sections which shall be linked into the Section Group.

######## 2. vLinkGenVarSectionGroupFlag

- **UUID**: `16954758-1aec-4579-8769-4c1a7e6c687e`
- **引用名**: `vLinkGenVarSectionGroupFlag`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenVarGroupFlags/vLinkGenVarGroupFlag`
- **描述**: Defines compiler specific flags to be generated for the Section Group.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on group level or the vLinkGen doesn't support them.

##### 15. vLinkGenVarGroupVariantHandling

**容器属性**:

- **UUID**: `f6f3b789-0fa8-462b-97c8-e902941b1bc1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of variant specific Memory Region Block mappings,
with which it is possible to link a logical group (respectively all of their containing Section Groups) to different memory areas in different variants.

The following behavior applies when setting the Memory Region Block references:
- For all variants, the "default" references from the Logical Group are used
- If a variant is specified in a variant specifics, then the "overwriting" references are used
- Where the "overwriting" references in the variant specifics are optional.
- This means that for a variant, for example, only the ROM/RAM copy can be linked elsewhere.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

########## 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

########## 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 16. vLinkGenVarGroupVariantSpecifics

**容器属性**:

- **UUID**: `1bd6167a-fa30-4a35-9e99-ec3ecf24879b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVariantSpecifics`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies variant specific Memory Region Block overwrites.
See vLinkGenVarGroupVariantHandling description for details.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenVarGroupSpecificRegion

- **UUID**: `7cfee69d-b8bf-4df3-9713-449b0b99aa4b`
- **引用名**: `vLinkGenVarGroupSpecificRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block from the parent Logical Group in the variants listed below.

######## 2. vLinkGenVarGroupSpecificRomRegion

- **UUID**: `7810504d-e7ff-42a4-ab36-c1bf057b75ae`
- **引用名**: `vLinkGenVarGroupSpecificRomRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Overwrites the default Memory Region Block (ROM Copy) from the parent Logical Group in the variants listed below.

######## 3. vLinkGenVarGroupSpecificVariant

- **UUID**: `bea4241c-2ab5-4e78-9958-7a6349bb8745`
- **引用名**: `vLinkGenVarGroupSpecificVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: References to the linker script variants for which the overwritten Memory Region Block references are to apply.

Note:
- Variants specified here must also be added to the parent Logical Group Variants.

##### 17. vLinkGenLogicalSymbolGroup

**容器属性**:

- **UUID**: `4e8e0822-f983-40b4-ae5c-2c30eeb6d77a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalSymbolGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical Symbol Group.
Logical Symbol Groups are an abstraction layer to group multiple Linker Symbols and generate them in the list of Logical Groups.

Note:
Some compilers expect global symbols to be defined at a certain position in the linker script. In this case the configured position is simply ignored.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenSymbolGroupPosition

- **UUID**: `9470f57f-fc97-4d2b-97a0-41e246a7dfce`
- **参数名**: `vLinkGenSymbolGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenSymbolGroupVariant

- **UUID**: `7baa5367-ae78-4bea-baae-51308545d368`
- **引用名**: `vLinkGenSymbolGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the linker script variants in which this group should be used.

Note:
If variants are configured but this group is not assigned to one, it applies to all of them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenSymbolGroupModule

- **UUID**: `c06a72c0-fdf1-44bd-bb0f-7799f4093436`
- **引用名**: `vLinkGenSymbolGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenLinkerSymbol

**容器属性**:

- **UUID**: `815ffcb1-74d6-474e-a77c-c2751c0dcaee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSymbol`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler independent symbol definition which can have a name and a value.
That means it is possible to assign values to own symbols, and vLinkGen will generate these assignments in the appropriate syntax into the linker script.

Note:
Some compilers do not support the definition of global Linker Symbols at all or only to a limited extent.
This should be considered when using Linker Symbols. However, vLinkGen will issue warnings if a compiler does not support them or only to a limited extent.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerSymbolPosition

- **UUID**: `bf59ab66-24a1-4988-9911-30e65d15d2e8`
- **参数名**: `vLinkGenLinkerSymbolPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Linker Symbol within its parent Logical Group.
If multiple symbols have the same position, they are sorted alphabetically by their container names.

######### STRING 类型参数

########## 1. vLinkGenLinkerSymbolValue

- **UUID**: `f9e91d17-49be-445a-b3ec-35989fc7fa72`
- **参数名**: `vLinkGenLinkerSymbolValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the value that the symbol should get.

######### LINKER-SYMBOL 类型参数

########## 1. vLinkGenLinkerSymbolName

- **UUID**: `ce606404-8ea4-4795-9878-28d344a8e4fb`
- **参数名**: `vLinkGenLinkerSymbolName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the name of the symbol.

Note:
The symbol must be a valid linker symbol.

##### 18. vLinkGenLinkerSymbol

**容器属性**:

- **UUID**: `815ffcb1-74d6-474e-a77c-c2751c0dcaee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSymbol`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a compiler independent symbol definition which can have a name and a value.
That means it is possible to assign values to own symbols, and vLinkGen will generate these assignments in the appropriate syntax into the linker script.

Note:
Some compilers do not support the definition of global Linker Symbols at all or only to a limited extent.
This should be considered when using Linker Symbols. However, vLinkGen will issue warnings if a compiler does not support them or only to a limited extent.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerSymbolPosition

- **UUID**: `bf59ab66-24a1-4988-9911-30e65d15d2e8`
- **参数名**: `vLinkGenLinkerSymbolPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Linker Symbol within its parent Logical Group.
If multiple symbols have the same position, they are sorted alphabetically by their container names.

####### STRING 类型参数

######## 1. vLinkGenLinkerSymbolValue

- **UUID**: `f9e91d17-49be-445a-b3ec-35989fc7fa72`
- **参数名**: `vLinkGenLinkerSymbolValue`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the value that the symbol should get.

####### LINKER-SYMBOL 类型参数

######## 1. vLinkGenLinkerSymbolName

- **UUID**: `ce606404-8ea4-4795-9878-28d344a8e4fb`
- **参数名**: `vLinkGenLinkerSymbolName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies the name of the symbol.

Note:
The symbol must be a valid linker symbol.

##### 19. vLinkGenLogicalUserGroup

**容器属性**:

- **UUID**: `6973e9c1-cf16-46f5-be08-019313cfe6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLogicalUserGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Logical User Group.
Logical Groups are an abstraction layer to group multiple Section Groups and map them to a Memory Region Block.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenUserGroupPosition

- **UUID**: `f41e4a9d-884e-411a-b8ff-b0332bfe6028`
- **参数名**: `vLinkGenUserGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Logical Group within all Logical Groups.
If multiple groups have the same position, they are sorted alphabetically by their container names.

Note:
With some compilers, the actual order of the Logical Group after linking may differ from the configured one.
This is a compiler limitation and cannot be influenced by vLinkGen.

####### ENUMERATION 类型参数

######## 1. vLinkGenUserGroupPlacement

- **UUID**: `5aedaf13-5a69-43f0-bf22-03c25f6348c6`
- **参数名**: `vLinkGenUserGroupPlacement`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `PRE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `PRE` (来源: Vector Informatik)
  - `POST` (来源: Vector Informatik)
  - `GROUP_LIST` (来源: Vector Informatik)
- **描述**: Specifies where the user code group should be generated in the linker script.

PRE:
The user code is generated at the beginning of the linker script.

POST:
The user code is generated at the end of the linker script.

GROUP_LIST:
The user code is generated within the Section Groups list at the specified position.
If set, the Memory Region Block reference need also to be set for some compilers.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenUserGroupRegion

- **UUID**: `9371b3bd-09d7-4299-9905-481bd08f2bc2`
- **引用名**: `vLinkGenUserGroupRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the Memory Region Block where the user Section Group should be linked to.

Note:
Only applicable if, vLinkGenUserGroupPlacement is set to GROUP_LIST and the compiler requires the configuration.

######## 2. vLinkGenUserGroupVariant

- **UUID**: `af403cbc-13af-4c42-8177-f564bd10de01`
- **引用名**: `vLinkGenUserGroupVariant`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the linker script variants in which this group should be used.

Note:
If variants are configured but this group is not assigned to one, it applies to all of them.

####### FOREIGN-REFERENCE 类型引用

######## 1. vLinkGenUserGroupModule

- **UUID**: `b4dfb785-ab0d-44b8-87f9-ec80de7ac902`
- **引用名**: `vLinkGenUserGroupModule`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Optional reference to the module which owns (requires) this Logical Group.

Note:
If this reference is set, the container is typically created by another module's generator.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenUserSectionGroup

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserSectionGroupPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenUserSectionGroupValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserSectionGroupValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

##### 20. vLinkGenUserSectionGroup

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserSectionGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenUserSectionGroupPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserSectionGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Section Group within its parent Logical Group.
If multiple groups have the same position, they are sorted alphabetically by their container names.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenUserSectionGroupValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserSectionGroupValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

##### 21. vLinkGenMemoryRegion

**容器属性**:

- **UUID**: `b5e4333c-3c89-4262-a6ee-433bce751d7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegion`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for one Memory Region.
Memory Regions are a logical abstraction layer to separate the configuration from the actual memory layout and to make it hardware independent.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenMemoryRegionAddrOffset

- **UUID**: `e18ca48d-c067-4e67-9676-fafd6f439169`
- **参数名**: `vLinkGenMemoryRegionAddrOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the offset of the memory region to the referenced hardware region start address.

The resulting start address of the Memory Region is calculated from the start address of the hardware memory area in vBaseEnv and this offset value.

######## 2. vLinkGenMemoryRegionSize

- **UUID**: `8f69cfe8-8d7f-4d6a-a49a-5f9f293adc70`
- **参数名**: `vLinkGenMemoryRegionSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region in bytes.

A hardware memory area can be splitted into multiple Memory Regions in vLinkGen.
In this the sizes of all Memory Regions must not exceed the size of the actual hardware memory area.

######## 3. vLinkGenMemoryRegionAddress

- **UUID**: `327e4cd6-b8a2-4c03-913e-da9741f45889`
- **参数名**: `vLinkGenMemoryRegionAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region.

The displayed value is the actual start address of the Memory Region after linking.
It is calculated from the start address of the hardware memory area in vBaseEnv and the address offset of the Memory Region.

Caution:
This parameter is for information only and must not be changed manually.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenMemoryRegionHwRegion

- **UUID**: `1293eae4-9fe7-4b3b-9521-2059d7de5ceb`
- **引用名**: `vLinkGenMemoryRegionHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vBaseEnvMemLayoutHwRegion`
- **完整路径**: `/MICROSAR/vBaseEnv/vBaseEnvGeneral/vBaseEnvMemLayoutHwRegion`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the hardware memory area where the Memory Region should be mapped to.

The hardware memory areas are predefined in the vBaseEnv and cannot be changed.
They reflect the actual memory layout in the hardware.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Memory Region Block.
Memory Region Blocks can be used to partition a Memory Region. They are used for the actual memory definitions in the generated linker script.

Note:
The position of a Memory Region Block in the memory area is determined by its position, size and boundary.
The actual start addresses of several blocks within a Memory Region are calculated using these parameters.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenMemoryRegionBlockPosition

- **UUID**: `b3303934-13e7-4bb9-ab01-e518d00fa0d5`
- **参数名**: `vLinkGenMemoryRegionBlockPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Memory Region Block within its parent Memory Region.
If multiple blocks have the same position, they are sorted alphabetically by their container names.

########## 2. vLinkGenMemoryRegionBlockSize

- **UUID**: `800b2308-fb88-4aed-849f-a57ec4658829`
- **参数名**: `vLinkGenMemoryRegionBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region Block in bytes.

A Memory Region can be splitted into multiple Memory Region Blocks.
In this the sizes of all blocks must not exceed the size of the parent Memory Region.

########## 3. vLinkGenMemoryRegionBlockAddress

- **UUID**: `a7d596ff-0f27-4443-a45f-1899a261e600`
- **参数名**: `vLinkGenMemoryRegionBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region Block.

The displayed value is the actual start address of the Memory Region Block after linking.
It is derived from the calculated start address of its parent Memory Region and its own boundary and position.

Caution:
This parameter is for information only and must not be changed manually.

########## 4. vLinkGenMemoryRegionBlockInitCore

- **UUID**: `1598ebbf-97f2-4c2a-999f-eec67aad5ea7`
- **参数名**: `vLinkGenMemoryRegionBlockInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the Memory Region Block.

######### ENUMERATION 类型参数

########## 1. vLinkGenMemoryRegionBlockBoundary

- **UUID**: `802bd1fd-1dc2-4020-a6bc-e81a313684c2`
- **参数名**: `vLinkGenMemoryRegionBlockBoundary`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LOWER`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LOWER` (来源: Vector Informatik)
  - `UPPER` (来源: Vector Informatik)
- **描述**: This value defines the location of the memory area block within its parent memory area.

Memory Region Blocks can be mapped either to the lower (lower address value) or upper (higher address value) end of the Memory Region.
Their start address is then calculated based on the boundary value, their position and the size of their preceding blocks.
This can be useful if, for example, between two Memory Region Blocks within a Memory Region an area in memory is to be left free.

LOWER:
The Memory Region Block is linked to the lower boundary of the Memory Region.

UPPER:
The Memory Region Block is linked to the upper boundary of the Memory Region.

########## 2. vLinkGenMemoryRegionBlockInitStage

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete Memory Region Block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE:
No initialization required.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenMemoryRegionBlockFlag

- **UUID**: `11a14ac7-e7c5-4f2c-8ca1-7121c9e35468`
- **引用名**: `vLinkGenMemoryRegionBlockFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenRegionBlockFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenRegionBlockFlags/vLinkGenRegionBlockFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Memory Region Block.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on Memory Region Block level or the vLinkGen doesn't support them.

##### 22. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a Memory Region Block.
Memory Region Blocks can be used to partition a Memory Region. They are used for the actual memory definitions in the generated linker script.

Note:
The position of a Memory Region Block in the memory area is determined by its position, size and boundary.
The actual start addresses of several blocks within a Memory Region are calculated using these parameters.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenMemoryRegionBlockPosition

- **UUID**: `b3303934-13e7-4bb9-ab01-e518d00fa0d5`
- **参数名**: `vLinkGenMemoryRegionBlockPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the relative position of the Memory Region Block within its parent Memory Region.
If multiple blocks have the same position, they are sorted alphabetically by their container names.

######## 2. vLinkGenMemoryRegionBlockSize

- **UUID**: `800b2308-fb88-4aed-849f-a57ec4658829`
- **参数名**: `vLinkGenMemoryRegionBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the Memory Region Block in bytes.

A Memory Region can be splitted into multiple Memory Region Blocks.
In this the sizes of all blocks must not exceed the size of the parent Memory Region.

######## 3. vLinkGenMemoryRegionBlockAddress

- **UUID**: `a7d596ff-0f27-4443-a45f-1899a261e600`
- **参数名**: `vLinkGenMemoryRegionBlockAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Shows the calculated start address of the Memory Region Block.

The displayed value is the actual start address of the Memory Region Block after linking.
It is derived from the calculated start address of its parent Memory Region and its own boundary and position.

Caution:
This parameter is for information only and must not be changed manually.

######## 4. vLinkGenMemoryRegionBlockInitCore

- **UUID**: `1598ebbf-97f2-4c2a-999f-eec67aad5ea7`
- **参数名**: `vLinkGenMemoryRegionBlockInitCore`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the Memory Region Block.

####### ENUMERATION 类型参数

######## 1. vLinkGenMemoryRegionBlockBoundary

- **UUID**: `802bd1fd-1dc2-4020-a6bc-e81a313684c2`
- **参数名**: `vLinkGenMemoryRegionBlockBoundary`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LOWER`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LOWER` (来源: Vector Informatik)
  - `UPPER` (来源: Vector Informatik)
- **描述**: This value defines the location of the memory area block within its parent memory area.

Memory Region Blocks can be mapped either to the lower (lower address value) or upper (higher address value) end of the Memory Region.
Their start address is then calculated based on the boundary value, their position and the size of their preceding blocks.
This can be useful if, for example, between two Memory Region Blocks within a Memory Region an area in memory is to be left free.

LOWER:
The Memory Region Block is linked to the lower boundary of the Memory Region.

UPPER:
The Memory Region Block is linked to the upper boundary of the Memory Region.

######## 2. vLinkGenMemoryRegionBlockInitStage

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitStage`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `EARLY` (来源: Vector Informatik)
  - `ONE` (来源: Vector Informatik)
  - `HARD_RESET_ONLY` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete Memory Region Block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE:
No initialization required.

EARLY:
Initialize always directly after reset. Shall only be used if really necessary.
Since the PLL might not be initialized at that time, the initialization of large areas may take a long time.

ONE:
Always initialized second during the default vBRS startup routine.
By default, this value should be used if an initialization is required.

HARD_RESET_ONLY:
Initialized right after stage ONE. However, initialization is only done if a hardware reset occurred.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenMemoryRegionBlockFlag

- **UUID**: `11a14ac7-e7c5-4f2c-8ca1-7121c9e35468`
- **引用名**: `vLinkGenMemoryRegionBlockFlag`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `vLinkGenRegionBlockFlag`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenPublishedInformation/vLinkGenRegionBlockFlags/vLinkGenRegionBlockFlag`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Defines compiler specific flags to be generated for the Memory Region Block.

Note:
The flags to be selected are predefined and cannot be changed.
If none are selectable, the compiler either does not support flags on Memory Region Block level or the vLinkGen doesn't support them.

##### 23. vLinkGenPublishedInformation

**容器属性**:

- **UUID**: `244f13d8-6387-43bf-8e40-55bb08b37456`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenPublishedInformation`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains additional published compiler specific informations.

Caution:
This container (and all including sub-elements) must not be changed manually.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenGeneration

- **UUID**: `5701aaf4-98b1-40cc-a591-4183a3033d3f`
- **参数名**: `vLinkGenGeneration`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Defines the internal vLinkGen code generation.

######## 2. vLinkGenDefaultConstGroupAlignment

- **UUID**: `c7e03d89-092e-4b1b-9c45-970619ff849a`
- **参数名**: `vLinkGenDefaultConstGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the optional default start address alignment for all CONST Section Groups in bytes.

Note:
It is only used for newly created groups that have no predefined values (e.g. recommended configuration).
It can, however, be changed in the groups later.

######## 3. vLinkGenDefaultVarGroupAlignment

- **UUID**: `3166b268-6c30-476f-af02-8ce7ea49b00e`
- **参数名**: `vLinkGenDefaultVarGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the optional default start address alignment for all VAR Section Groups in bytes.

Note:
It is only used for newly created groups that have no predefined values (e.g. recommended configuration).
It can, however, be changed in the groups later.

####### BOOLEAN 类型参数

######## 1. vLinkGenDuplicatedLabels

- **UUID**: `8a74bf37-0320-4e49-9e30-6371157df14f`
- **参数名**: `vLinkGenDuplicatedLabels`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies whether the vLinkGen shall generate duplicated labels or not.

true: Generate additional labels with double underscores ("__") at the beginning
false: Normal label generation. No duplicated labels

###### 配置容器

本模块包含 **12** 个配置容器：

####### 1. vLinkGenRegionBlockFlags

**容器属性**:

- **UUID**: `a9f18960-a32a-47c5-843e-86c5e4c58302`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Memory Region Block flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenRegionBlockFlag

**容器属性**:

- **UUID**: `6e3bdae1-be72-498f-ae9f-b1146b8f0f0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Memory Region Block flag.

####### 2. vLinkGenRegionBlockFlag

**容器属性**:

- **UUID**: `6e3bdae1-be72-498f-ae9f-b1146b8f0f0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Memory Region Block flag.

####### 3. vLinkGenConstGroupFlags

**容器属性**:

- **UUID**: `c6781e24-acae-47c1-8647-4f2bf9639a53`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Section Group flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenConstGroupFlag

**容器属性**:

- **UUID**: `c35002ce-db9a-4af4-90d3-c1e9c55b6f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

####### 4. vLinkGenConstGroupFlag

**容器属性**:

- **UUID**: `c35002ce-db9a-4af4-90d3-c1e9c55b6f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

####### 5. vLinkGenConstSectionFlags

**容器属性**:

- **UUID**: `a3defa47-ad5e-4292-8b75-35522b6d2f6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenConstSectionFlag

**容器属性**:

- **UUID**: `2dc3e3ec-e69d-4b61-af6e-6e76d627aa7b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

####### 6. vLinkGenConstSectionFlag

**容器属性**:

- **UUID**: `2dc3e3ec-e69d-4b61-af6e-6e76d627aa7b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

####### 7. vLinkGenVarGroupFlags

**容器属性**:

- **UUID**: `94d980f4-e280-4d58-980c-934c43772861`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Section Group flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenVarGroupFlag

**容器属性**:

- **UUID**: `d42af726-d14a-4128-a70c-7bb7ac4d7163`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

####### 8. vLinkGenVarGroupFlag

**容器属性**:

- **UUID**: `d42af726-d14a-4128-a70c-7bb7ac4d7163`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

####### 9. vLinkGenVarSectionFlags

**容器属性**:

- **UUID**: `1d207e60-d361-4801-a650-41c6e0a69304`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenVarSectionFlag

**容器属性**:

- **UUID**: `b7f8b083-dfb2-4753-ad43-1ead3f5dfa82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

####### 10. vLinkGenVarSectionFlag

**容器属性**:

- **UUID**: `b7f8b083-dfb2-4753-ad43-1ead3f5dfa82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

####### 11. vLinkGenSpecSectionFlags

**容器属性**:

- **UUID**: `74a5b7b0-d4aa-4218-9ad7-044fa507a5a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenSpecSectionFlag

**容器属性**:

- **UUID**: `1df25bf0-f6db-4aac-97c3-ca148ad0d57f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

####### 12. vLinkGenSpecSectionFlag

**容器属性**:

- **UUID**: `1df25bf0-f6db-4aac-97c3-ca148ad0d57f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 24. vLinkGenRegionBlockFlags

**容器属性**:

- **UUID**: `a9f18960-a32a-47c5-843e-86c5e4c58302`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Memory Region Block flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenRegionBlockFlag

**容器属性**:

- **UUID**: `6e3bdae1-be72-498f-ae9f-b1146b8f0f0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Memory Region Block flag.

##### 25. vLinkGenRegionBlockFlag

**容器属性**:

- **UUID**: `6e3bdae1-be72-498f-ae9f-b1146b8f0f0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenRegionBlockFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Memory Region Block flag.

##### 26. vLinkGenConstGroupFlags

**容器属性**:

- **UUID**: `c6781e24-acae-47c1-8647-4f2bf9639a53`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Section Group flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenConstGroupFlag

**容器属性**:

- **UUID**: `c35002ce-db9a-4af4-90d3-c1e9c55b6f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

##### 27. vLinkGenConstGroupFlag

**容器属性**:

- **UUID**: `c35002ce-db9a-4af4-90d3-c1e9c55b6f17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

##### 28. vLinkGenConstSectionFlags

**容器属性**:

- **UUID**: `a3defa47-ad5e-4292-8b75-35522b6d2f6d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenConstSectionFlag

**容器属性**:

- **UUID**: `2dc3e3ec-e69d-4b61-af6e-6e76d627aa7b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 29. vLinkGenConstSectionFlag

**容器属性**:

- **UUID**: `2dc3e3ec-e69d-4b61-af6e-6e76d627aa7b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 30. vLinkGenVarGroupFlags

**容器属性**:

- **UUID**: `94d980f4-e280-4d58-980c-934c43772861`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Section Group flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenVarGroupFlag

**容器属性**:

- **UUID**: `d42af726-d14a-4128-a70c-7bb7ac4d7163`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

##### 31. vLinkGenVarGroupFlag

**容器属性**:

- **UUID**: `d42af726-d14a-4128-a70c-7bb7ac4d7163`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Section Group flag.

##### 32. vLinkGenVarSectionFlags

**容器属性**:

- **UUID**: `1d207e60-d361-4801-a650-41c6e0a69304`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenVarSectionFlag

**容器属性**:

- **UUID**: `b7f8b083-dfb2-4753-ad43-1ead3f5dfa82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 33. vLinkGenVarSectionFlag

**容器属性**:

- **UUID**: `b7f8b083-dfb2-4753-ad43-1ead3f5dfa82`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 34. vLinkGenSpecSectionFlags

**容器属性**:

- **UUID**: `74a5b7b0-d4aa-4218-9ad7-044fa507a5a1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlags`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

Collection of compiler specific Linker Section flags.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenSpecSectionFlag

**容器属性**:

- **UUID**: `1df25bf0-f6db-4aac-97c3-ca148ad0d57f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 35. vLinkGenSpecSectionFlag

**容器属性**:

- **UUID**: `1df25bf0-f6db-4aac-97c3-ca148ad0d57f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenSpecSectionFlag`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

Definition of a compiler specific Linker Section flag.

##### 36. vLinkGenVariantHandling

**容器属性**:

- **UUID**: `8113f31a-2d7f-47f0-86b1-5359359105ac`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVariantHandling`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container contains all configuration parameters for the variant handling.

Caution:
If variants are configured, exactly one of them must always be defined in a build process.
For example, by passing it as compiler and/or linker option (e.g. -D<VariantName>).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenVariant

**容器属性**:

- **UUID**: `6ffe8e03-bd32-4960-a13c-bdfffcc0a42c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVariant`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container specifies one linker script variant.

##### 37. vLinkGenVariant

**容器属性**:

- **UUID**: `6ffe8e03-bd32-4960-a13c-bdfffcc0a42c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVariant`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container specifies one linker script variant.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vLinkGen_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vLinkGen**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vLinkGen_Impl

- **UUID**: `279b8d1f-cc47-41cd-b47f-cb88db0d739a`
- **实现名称**: `vLinkGen_Impl`
- **编程语言**: C
- **软件版本**: 2.02.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.02.01
- **代码生成器**: DaVinci Configurator
