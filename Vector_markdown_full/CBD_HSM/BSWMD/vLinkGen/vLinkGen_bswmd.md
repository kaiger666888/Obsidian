# vLinkGen - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:01

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

共有 **10** 个版本记录：

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

##### 10. 版本 1.07.02

- **状态**: released
- **发布日期**: 2020-03-11
- **发布者**: virbse

**变更内容**:

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. vLinkGenMemLayout

**容器属性**:

- **UUID**: `206c6b28-e87f-468e-ad64-7c4b11901201`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemLayout`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure all memory layout relevant configuration parameters.

###### 配置容器

本模块包含 **17** 个配置容器：

####### 1. vLinkGenLinkerSections

**容器属性**:

- **UUID**: `4e46e9f1-968e-4e87-a986-8ea535c78fbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure the configuration parameters of the different linker section types.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE linker section.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

######### 2. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

######### 3. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

######### 4. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK linker section.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 2. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 3. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 4. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 5. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 6. vLinkGenLinkerSectionConstGroup

**容器属性**:

- **UUID**: `ab65a9ff-f823-411f-b21f-520210c41419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionConstGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section group.
It can be used to map several CONST or CODE linker sections to a specific memory region.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstGroupPosition

- **UUID**: `6f281aef-1545-48ad-b39f-6df49f8f0163`
- **参数名**: `vLinkGenConstGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the linker section group in the selected hardware memory location.
Relative to other section groups within the same hardware memory location.
If equal, the generation order depends on the order of the group within the configuration file.

########## 2. vLinkGenConstGroupAlignment

- **UUID**: `949b2bc4-5910-40ce-a463-3f52a1c9672e`
- **参数名**: `vLinkGenConstGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the section group in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 3. vLinkGenConstGroupGapSize

- **UUID**: `51280186-aa9e-4eb5-a5b4-6e22c383524c`
- **参数名**: `vLinkGenConstGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the section group in bytes.
If zero, no gap is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenConstGroupPreUserCode

- **UUID**: `3d4453d7-d6ac-4306-bfaa-87e79cf53973`
- **参数名**: `vLinkGenConstGroupPreUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#if 0`
- **描述**: Specifies optional preprocessor condition to be generated right before the linker section group.

Example:
#ifdef MIP_USED

########## 2. vLinkGenConstGroupPostUserCode

- **UUID**: `afc47e74-687c-4c10-885e-8197196a2d09`
- **参数名**: `vLinkGenConstGroupPostUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#endif`
- **描述**: Specifies optional end of preprocessor condition to be generated right after the linker section group.

Example:
#endif /* MIP_USED */

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstGroupHwRegion

- **UUID**: `1fc2ee6d-7403-4656-b77c-fb59f57c4c5f`
- **引用名**: `vLinkGenConstGroupHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region where the linker section group should be linked to.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vLinkGenConstGroupUserSection

**容器属性**:

- **UUID**: `85bc2b62-6e9d-446a-8a25-8f09a6a4c97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenConstGroupUserSectionPosition

- **UUID**: `a1df2da8-e74d-4d69-a537-88976ee99b70`
- **参数名**: `vLinkGenConstGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### MULTILINE-STRING 类型参数

############ 1. vLinkGenConstGroupUserSectionValue

- **UUID**: `3accfb5f-fcc7-4abd-8a75-aab86f24edef`
- **参数名**: `vLinkGenConstGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

######### 2. vLinkGenConstGroupCodeSection

**容器属性**:

- **UUID**: `b15a2206-5109-48bb-ad87-ca4def0b4388`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CODE linker sections whose data shall be linked to the linker section group.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenCodeSectionPosition

- **UUID**: `c48d6daa-d471-48d9-b60e-202a645b5c1f`
- **参数名**: `vLinkGenCodeSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### BOOLEAN 类型参数

############ 1. vLinkGenCodeSectionCachePolicyCache

- **UUID**: `116c4b0f-83dc-4a51-9035-b489f26d678e`
- **参数名**: `vLinkGenCodeSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

############ 2. vLinkGenCodeSectionCachePolicyNoCache

- **UUID**: `b83c0503-fd93-4640-97c8-ba08c5138b21`
- **参数名**: `vLinkGenCodeSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

############ 3. vLinkGenCodeSectionAddressingModeNear

- **UUID**: `2088029f-75e4-466e-9528-d60411bdf0c7`
- **参数名**: `vLinkGenCodeSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CODE_FAST) are linked into the linker section group.

############ 4. vLinkGenCodeSectionAddressingModeFar

- **UUID**: `d2e0b324-3489-45bb-8d06-bed3085e446d`
- **参数名**: `vLinkGenCodeSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CODE) are linked into the linker section group.

############ 5. vLinkGenCodeSectionFlagNoLoad

- **UUID**: `3425b75d-a1aa-4ebf-931a-a0728527edaf`
- **参数名**: `vLinkGenCodeSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

############ 6. vLinkGenCodeSectionFlagKeep

- **UUID**: `00926987-ffd5-4ccb-9c40-aa149294ac09`
- **参数名**: `vLinkGenCodeSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenCodeSectionRef

- **UUID**: `7fe98336-2a64-4085-89fd-dc90447e5f64`
- **引用名**: `vLinkGenCodeSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerCodeSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

######### 3. vLinkGenConstGroupConstSection

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CONST linker sections whose data shall be linked to the linker section group.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenConstSectionPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### BOOLEAN 类型参数

############ 1. vLinkGenConstSectionCachePolicyCache

- **UUID**: `ad075b49-088b-465a-8a6e-384b11665caa`
- **参数名**: `vLinkGenConstSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

############ 2. vLinkGenConstSectionCachePolicyNoCache

- **UUID**: `42242b75-91d2-4542-be72-413597ce023f`
- **参数名**: `vLinkGenConstSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

############ 3. vLinkGenConstSectionAddressingModeNear

- **UUID**: `0d9a8462-0b61-46df-baaa-521292f096f0`
- **参数名**: `vLinkGenConstSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CONST_FAST) are linked into the linker section group.

############ 4. vLinkGenConstSectionAddressingModeFar

- **UUID**: `13807cc8-9719-4b0a-92b0-4715989654c5`
- **参数名**: `vLinkGenConstSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CONST) are linked into the linker section group.

############ 5. vLinkGenConstSectionFlagNoLoad

- **UUID**: `e6c017bc-356a-4952-83c2-81e4521ee261`
- **参数名**: `vLinkGenConstSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

############ 6. vLinkGenConstSectionFlagKeep

- **UUID**: `477d7990-dce8-4f56-8b37-966c830ea12f`
- **参数名**: `vLinkGenConstSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenConstSectionRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerConstSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 7. vLinkGenConstGroupUserSection

**容器属性**:

- **UUID**: `85bc2b62-6e9d-446a-8a25-8f09a6a4c97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstGroupUserSectionPosition

- **UUID**: `a1df2da8-e74d-4d69-a537-88976ee99b70`
- **参数名**: `vLinkGenConstGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenConstGroupUserSectionValue

- **UUID**: `3accfb5f-fcc7-4abd-8a75-aab86f24edef`
- **参数名**: `vLinkGenConstGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

####### 8. vLinkGenConstGroupCodeSection

**容器属性**:

- **UUID**: `b15a2206-5109-48bb-ad87-ca4def0b4388`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CODE linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenCodeSectionPosition

- **UUID**: `c48d6daa-d471-48d9-b60e-202a645b5c1f`
- **参数名**: `vLinkGenCodeSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenCodeSectionCachePolicyCache

- **UUID**: `116c4b0f-83dc-4a51-9035-b489f26d678e`
- **参数名**: `vLinkGenCodeSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 2. vLinkGenCodeSectionCachePolicyNoCache

- **UUID**: `b83c0503-fd93-4640-97c8-ba08c5138b21`
- **参数名**: `vLinkGenCodeSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 3. vLinkGenCodeSectionAddressingModeNear

- **UUID**: `2088029f-75e4-466e-9528-d60411bdf0c7`
- **参数名**: `vLinkGenCodeSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CODE_FAST) are linked into the linker section group.

########## 4. vLinkGenCodeSectionAddressingModeFar

- **UUID**: `d2e0b324-3489-45bb-8d06-bed3085e446d`
- **参数名**: `vLinkGenCodeSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CODE) are linked into the linker section group.

########## 5. vLinkGenCodeSectionFlagNoLoad

- **UUID**: `3425b75d-a1aa-4ebf-931a-a0728527edaf`
- **参数名**: `vLinkGenCodeSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 6. vLinkGenCodeSectionFlagKeep

- **UUID**: `00926987-ffd5-4ccb-9c40-aa149294ac09`
- **参数名**: `vLinkGenCodeSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenCodeSectionRef

- **UUID**: `7fe98336-2a64-4085-89fd-dc90447e5f64`
- **引用名**: `vLinkGenCodeSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerCodeSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 9. vLinkGenConstGroupConstSection

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CONST linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstSectionPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenConstSectionCachePolicyCache

- **UUID**: `ad075b49-088b-465a-8a6e-384b11665caa`
- **参数名**: `vLinkGenConstSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 2. vLinkGenConstSectionCachePolicyNoCache

- **UUID**: `42242b75-91d2-4542-be72-413597ce023f`
- **参数名**: `vLinkGenConstSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 3. vLinkGenConstSectionAddressingModeNear

- **UUID**: `0d9a8462-0b61-46df-baaa-521292f096f0`
- **参数名**: `vLinkGenConstSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CONST_FAST) are linked into the linker section group.

########## 4. vLinkGenConstSectionAddressingModeFar

- **UUID**: `13807cc8-9719-4b0a-92b0-4715989654c5`
- **参数名**: `vLinkGenConstSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CONST) are linked into the linker section group.

########## 5. vLinkGenConstSectionFlagNoLoad

- **UUID**: `e6c017bc-356a-4952-83c2-81e4521ee261`
- **参数名**: `vLinkGenConstSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 6. vLinkGenConstSectionFlagKeep

- **UUID**: `477d7990-dce8-4f56-8b37-966c830ea12f`
- **参数名**: `vLinkGenConstSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstSectionRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerConstSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 10. vLinkGenLinkerSectionVarGroup

**容器属性**:

- **UUID**: `8b49ddd5-843c-439b-a745-971b7bf2f5c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionVarGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section group.
It can be used to map several VAR or STACK linker sections to a specific memory region.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarGroupPosition

- **UUID**: `39cfef63-abe5-4308-ab2b-ba4b18c57c8e`
- **参数名**: `vLinkGenVarGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the linker section group in the selected hardware memory location.
Relative to other section groups within the same hardware memory location.
If equal, the generation order depends on the order of the group within the configuration file.

########## 2. vLinkGenVarGroupAlignment

- **UUID**: `c0d180bc-a616-4a1a-b2b2-b45da7fb5dbd`
- **参数名**: `vLinkGenVarGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the section group in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 3. vLinkGenVarGroupInitCore

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
- **描述**: Specifies the physical core ID which shall perform the initialization of all INIT or ZERO_INIT sections assigned to the linker section group.

########## 4. vLinkGenVarGroupGapSize

- **UUID**: `9a680a42-3998-4fb6-b654-91bb68d4b25e`
- **参数名**: `vLinkGenVarGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the section group in bytes.
If zero, no gap is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######### ENUMERATION 类型参数

########## 1. vLinkGenVarGroupInitPolicy

- **UUID**: `5727461f-2b2d-431b-9794-1d6771509c1a`
- **参数名**: `vLinkGenVarGroupInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the ZERO_INIT sections of the linker section group shall be initialized with zeros and when.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for groups containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitAreas*) which can be used to initialize the linker section groups with zeros.
This is normally done by the startup code of the vBRS.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenVarGroupPreUserCode

- **UUID**: `cf10ce38-5f77-427b-a81f-4608f6ebe3b3`
- **参数名**: `vLinkGenVarGroupPreUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#if 0`
- **描述**: Specifies optional preprocessor condition to be generated right before the linker section group.

Example:
#ifdef MIP_USED

########## 2. vLinkGenVarGroupPostUserCode

- **UUID**: `6f82e09b-ab0c-4736-bad5-15a477377b00`
- **参数名**: `vLinkGenVarGroupPostUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#endif`
- **描述**: Specifies optional end of preprocessor condition to be generated right after the linker section group.

Example:
#endif /* MIP_USED */

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarGroupHwRegion

- **UUID**: `3cddb3c3-ee5b-4964-95ac-7d90dcabaf63`
- **引用名**: `vLinkGenVarGroupHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region where the linker section group should be linked to.

########## 2. vLinkGenVarGroupInitDataHwRegion

- **UUID**: `e1b48eab-1434-4092-8b3d-b08f423f3644`
- **引用名**: `vLinkGenVarGroupInitDataHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region block where the init data of the linker section group should be linked to.
This is typically used for initialization of INIT data (ROM to RAM copy).

Note:
Depending on this parameter, the vLinkGen only generates a structure (vLinkGen_DataInitAreas) which can be used to initialize the linker section groups with concrete data.
This is normally done by the startup code of the vBRS.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. vLinkGenVarGroupUserSection

**容器属性**:

- **UUID**: `8320d903-5424-4717-b4db-ae97fcc708c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenVarGroupUserSectionPosition

- **UUID**: `25e1b9cc-45d6-4499-abba-18f7eab3e380`
- **参数名**: `vLinkGenVarGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### MULTILINE-STRING 类型参数

############ 1. vLinkGenVarGroupUserSectionValue

- **UUID**: `5d50f6b3-0851-4b5e-b6d7-77cddbae6822`
- **参数名**: `vLinkGenVarGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

######### 2. vLinkGenVarGroupVarSection

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of VAR linker sections whose data shall be linked to the linker section group.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenVarSectionPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### BOOLEAN 类型参数

############ 1. vLinkGenVarSectionInitPolicyInit

- **UUID**: `ba72293b-ad79-4ccf-8a9d-36b38bf44e14`
- **参数名**: `vLinkGenVarSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

############ 2. vLinkGenVarSectionInitPolicyNoInit

- **UUID**: `e435b476-4ddb-4010-89ea-88e24f4f7ebf`
- **参数名**: `vLinkGenVarSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

############ 3. vLinkGenVarSectionInitPolicyZeroInit

- **UUID**: `4b017c9c-1905-4b5e-977c-f5c08a2fb14d`
- **参数名**: `vLinkGenVarSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

############ 4. vLinkGenVarSectionCachePolicyCache

- **UUID**: `d3c634a3-11cf-45d2-943a-e8cccc2737d3`
- **参数名**: `vLinkGenVarSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

############ 5. vLinkGenVarSectionCachePolicyNoCache

- **UUID**: `67dd430d-fb7e-4b01-9f76-1fcafce20ffa`
- **参数名**: `vLinkGenVarSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

############ 6. vLinkGenVarSectionAddressingModeNear

- **UUID**: `16e76f72-56de-4c05-ac78-13d92534cd3e`
- **参数名**: `vLinkGenVarSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

############ 7. vLinkGenVarSectionAddressingModeFar

- **UUID**: `ddb4f185-a1c7-4b78-b131-b19d4ef71a45`
- **参数名**: `vLinkGenVarSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

############ 8. vLinkGenVarSectionFlagNoLoad

- **UUID**: `8878fa0b-1181-45a8-a7fc-e29483b45857`
- **参数名**: `vLinkGenVarSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

############ 9. vLinkGenVarSectionFlagKeep

- **UUID**: `2067c503-94ef-4bc7-9ec9-cbc576fb831d`
- **参数名**: `vLinkGenVarSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenVarSectionRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerVarSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

######### 3. vLinkGenVarGroupStackSection

**容器属性**:

- **UUID**: `cd4f60ea-6af8-4ae3-adfc-0853a02ac536`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of STACK linker sections whose data shall be linked to the linker section group.

########## 参数配置

此容器包含 **10** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenStackSectionPosition

- **UUID**: `ec7c1492-54cc-43f3-8039-1c4206bbff32`
- **参数名**: `vLinkGenStackSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### BOOLEAN 类型参数

############ 1. vLinkGenStackSectionInitPolicyInit

- **UUID**: `25730b52-4b03-47ef-b575-6c1d100fb1ff`
- **参数名**: `vLinkGenStackSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

############ 2. vLinkGenStackSectionInitPolicyNoInit

- **UUID**: `a0d8710d-4317-405c-8c2d-89f1091e6ac6`
- **参数名**: `vLinkGenStackSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

############ 3. vLinkGenStackSectionInitPolicyZeroInit

- **UUID**: `67069945-12a2-41f9-a48d-ec923c37c2ad`
- **参数名**: `vLinkGenStackSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

############ 4. vLinkGenStackSectionCachePolicyCache

- **UUID**: `cbb08269-4994-41c3-85fd-dfe3b761dcf7`
- **参数名**: `vLinkGenStackSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

############ 5. vLinkGenStackSectionCachePolicyNoCache

- **UUID**: `226c2c8a-146e-41c6-b877-a50df88e9ed0`
- **参数名**: `vLinkGenStackSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

############ 6. vLinkGenStackSectionAddressingModeNear

- **UUID**: `6d22d7fc-1b12-4f3d-afae-c1d69d280baf`
- **参数名**: `vLinkGenStackSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

############ 7. vLinkGenStackSectionAddressingModeFar

- **UUID**: `b01de2b8-5363-4b09-a547-460b0633c92d`
- **参数名**: `vLinkGenStackSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

############ 8. vLinkGenStackSectionFlagNoLoad

- **UUID**: `20b0dd8b-4d4c-4a73-a548-1076034b1a93`
- **参数名**: `vLinkGenStackSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

############ 9. vLinkGenStackSectionFlagKeep

- **UUID**: `75b1000d-c372-430c-a821-8039562ae2b2`
- **参数名**: `vLinkGenStackSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vLinkGenStackSectionRef

- **UUID**: `643d6ec7-9fc8-4803-9280-f5bf59280576`
- **引用名**: `vLinkGenStackSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerStackSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 11. vLinkGenVarGroupUserSection

**容器属性**:

- **UUID**: `8320d903-5424-4717-b4db-ae97fcc708c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarGroupUserSectionPosition

- **UUID**: `25e1b9cc-45d6-4499-abba-18f7eab3e380`
- **参数名**: `vLinkGenVarGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenVarGroupUserSectionValue

- **UUID**: `5d50f6b3-0851-4b5e-b6d7-77cddbae6822`
- **参数名**: `vLinkGenVarGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

####### 12. vLinkGenVarGroupVarSection

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of VAR linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarSectionPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenVarSectionInitPolicyInit

- **UUID**: `ba72293b-ad79-4ccf-8a9d-36b38bf44e14`
- **参数名**: `vLinkGenVarSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

########## 2. vLinkGenVarSectionInitPolicyNoInit

- **UUID**: `e435b476-4ddb-4010-89ea-88e24f4f7ebf`
- **参数名**: `vLinkGenVarSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

########## 3. vLinkGenVarSectionInitPolicyZeroInit

- **UUID**: `4b017c9c-1905-4b5e-977c-f5c08a2fb14d`
- **参数名**: `vLinkGenVarSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

########## 4. vLinkGenVarSectionCachePolicyCache

- **UUID**: `d3c634a3-11cf-45d2-943a-e8cccc2737d3`
- **参数名**: `vLinkGenVarSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 5. vLinkGenVarSectionCachePolicyNoCache

- **UUID**: `67dd430d-fb7e-4b01-9f76-1fcafce20ffa`
- **参数名**: `vLinkGenVarSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 6. vLinkGenVarSectionAddressingModeNear

- **UUID**: `16e76f72-56de-4c05-ac78-13d92534cd3e`
- **参数名**: `vLinkGenVarSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

########## 7. vLinkGenVarSectionAddressingModeFar

- **UUID**: `ddb4f185-a1c7-4b78-b131-b19d4ef71a45`
- **参数名**: `vLinkGenVarSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

########## 8. vLinkGenVarSectionFlagNoLoad

- **UUID**: `8878fa0b-1181-45a8-a7fc-e29483b45857`
- **参数名**: `vLinkGenVarSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 9. vLinkGenVarSectionFlagKeep

- **UUID**: `2067c503-94ef-4bc7-9ec9-cbc576fb831d`
- **参数名**: `vLinkGenVarSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarSectionRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerVarSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 13. vLinkGenVarGroupStackSection

**容器属性**:

- **UUID**: `cd4f60ea-6af8-4ae3-adfc-0853a02ac536`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of STACK linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenStackSectionPosition

- **UUID**: `ec7c1492-54cc-43f3-8039-1c4206bbff32`
- **参数名**: `vLinkGenStackSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenStackSectionInitPolicyInit

- **UUID**: `25730b52-4b03-47ef-b575-6c1d100fb1ff`
- **参数名**: `vLinkGenStackSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

########## 2. vLinkGenStackSectionInitPolicyNoInit

- **UUID**: `a0d8710d-4317-405c-8c2d-89f1091e6ac6`
- **参数名**: `vLinkGenStackSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

########## 3. vLinkGenStackSectionInitPolicyZeroInit

- **UUID**: `67069945-12a2-41f9-a48d-ec923c37c2ad`
- **参数名**: `vLinkGenStackSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

########## 4. vLinkGenStackSectionCachePolicyCache

- **UUID**: `cbb08269-4994-41c3-85fd-dfe3b761dcf7`
- **参数名**: `vLinkGenStackSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 5. vLinkGenStackSectionCachePolicyNoCache

- **UUID**: `226c2c8a-146e-41c6-b877-a50df88e9ed0`
- **参数名**: `vLinkGenStackSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 6. vLinkGenStackSectionAddressingModeNear

- **UUID**: `6d22d7fc-1b12-4f3d-afae-c1d69d280baf`
- **参数名**: `vLinkGenStackSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

########## 7. vLinkGenStackSectionAddressingModeFar

- **UUID**: `b01de2b8-5363-4b09-a547-460b0633c92d`
- **参数名**: `vLinkGenStackSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

########## 8. vLinkGenStackSectionFlagNoLoad

- **UUID**: `20b0dd8b-4d4c-4a73-a548-1076034b1a93`
- **参数名**: `vLinkGenStackSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 9. vLinkGenStackSectionFlagKeep

- **UUID**: `75b1000d-c372-430c-a821-8039562ae2b2`
- **参数名**: `vLinkGenStackSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenStackSectionRef

- **UUID**: `643d6ec7-9fc8-4803-9280-f5bf59280576`
- **引用名**: `vLinkGenStackSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerStackSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 14. vLinkGenLinkerSectionUserGroup

**容器属性**:

- **UUID**: `6973e9c1-cf16-46f5-be08-019313cfe6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionUserGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for an user code group.
User code groups are generated either at the beginning or at the end of the linker script.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserGroupPosition

- **UUID**: `f41e4a9d-884e-411a-b8ff-b0332bfe6028`
- **参数名**: `vLinkGenUserGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code group.
If equal, the generation order depends on the order of the group within the configuration file.

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
- **描述**: Specifies whether the user code group is generated at the beginning or the end of the linker script.

PRE: The user code group is generated at the beginning of the linker script.
POST: The user code group is generated at the end of the linker script.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vLinkGenUserGroupUserSection

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. vLinkGenUserGroupUserSectionPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code section within the user code group.
If equal, the generation order depends on the order of the sections within the configuration file.

########### MULTILINE-STRING 类型参数

############ 1. vLinkGenUserGroupUserSectionValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

####### 15. vLinkGenUserGroupUserSection

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserGroupUserSectionPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code section within the user code group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenUserGroupUserSectionValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

####### 16. vLinkGenLinkerMemoryRegion

**容器属性**:

- **UUID**: `b5e4333c-3c89-4262-a6ee-433bce751d7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerMemoryRegion`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for one memory region.
Memory regions has to be mapped to concrete hardware regions which are predefined in vBaseEnv.

######## 参数配置

此容器包含 **2** 个参数：

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
- **描述**: Specifies the offset of the memory rergion to the referenced hardware region start address.

Memory Region Start Address = Hardware Region Start Address + Address Offset

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
- **描述**: This value specifies the size of the memory region in bytes.

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
- **描述**: Reference to the hardware memory area where the memory region should be mapped to.

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

This container includes all configuration parameters for a memory region block.
Memory region blocks can be used to partition a memory region.

########## 参数配置

此容器包含 **5** 个参数：

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
- **描述**: This value specifies the position of the memory region block within the memory region.

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
- **描述**: This value specifies the size of the memory region block in bytes.

############ 3. vLinkGenMemoryRegionBlockInitCore

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
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the memory region block.

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
- **描述**: This value defines the boundary of the memory region block.

LOWER: The memory region block is linked to the lower boundary of the memory region
UPPER: The memory region block is linked to the upper boundary of the memory region

############ 2. vLinkGenMemoryRegionBlockInitPolicy

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete memory region block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if a hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for memory region blocks containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitBlocks*) which can be used to initialize the memory region blocks with zeros.
This is normally done by the startup code of the vBRS.

####### 17. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a memory region block.
Memory region blocks can be used to partition a memory region.

######## 参数配置

此容器包含 **5** 个参数：

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
- **描述**: This value specifies the position of the memory region block within the memory region.

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
- **描述**: This value specifies the size of the memory region block in bytes.

########## 3. vLinkGenMemoryRegionBlockInitCore

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
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the memory region block.

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
- **描述**: This value defines the boundary of the memory region block.

LOWER: The memory region block is linked to the lower boundary of the memory region
UPPER: The memory region block is linked to the upper boundary of the memory region

########## 2. vLinkGenMemoryRegionBlockInitPolicy

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete memory region block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if a hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for memory region blocks containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitBlocks*) which can be used to initialize the memory region blocks with zeros.
This is normally done by the startup code of the vBRS.

##### 2. vLinkGenLinkerSections

**容器属性**:

- **UUID**: `4e46e9f1-968e-4e87-a986-8ea535c78fbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSections`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Container to structure the configuration parameters of the different linker section types.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 2. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 3. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

####### 4. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK linker section.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

##### 3. vLinkGenLinkerCodeSection

**容器属性**:

- **UUID**: `3a3e3223-5997-4558-8ca9-bae8bbf0d448`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CODE linker section.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerCodeSectionAlignment

- **UUID**: `16294775-320c-430f-a1c1-561444cee737`
- **参数名**: `vLinkGenLinkerCodeSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

##### 4. vLinkGenLinkerConstSection

**容器属性**:

- **UUID**: `3e57951c-37be-4e82-8452-def98b358150`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerConstSectionAlignment

- **UUID**: `63868933-f8a9-4a70-a160-9f5356262a9a`
- **参数名**: `vLinkGenLinkerConstSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

##### 5. vLinkGenLinkerVarSection

**容器属性**:

- **UUID**: `69dbfdb1-23c9-439a-860a-18a30e066f43`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerVarSectionAlignment

- **UUID**: `882ff07d-d444-4aab-a708-1e806ccc8605`
- **参数名**: `vLinkGenLinkerVarSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

##### 6. vLinkGenLinkerStackSection

**容器属性**:

- **UUID**: `4a0bd071-a7ea-47fd-96cc-1cb4a79d2162`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a STACK linker section.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenLinkerStackSectionAlignment

- **UUID**: `b877bcf7-4f52-47fc-bd22-759a7dc0b9d0`
- **参数名**: `vLinkGenLinkerStackSectionAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the linker section in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

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
- **描述**: This parameter specifies the name of the linker section.

##### 7. vLinkGenLinkerSectionConstGroup

**容器属性**:

- **UUID**: `ab65a9ff-f823-411f-b21f-520210c41419`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionConstGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a CONST linker section group.
It can be used to map several CONST or CODE linker sections to a specific memory region.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenConstGroupPosition

- **UUID**: `6f281aef-1545-48ad-b39f-6df49f8f0163`
- **参数名**: `vLinkGenConstGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the linker section group in the selected hardware memory location.
Relative to other section groups within the same hardware memory location.
If equal, the generation order depends on the order of the group within the configuration file.

######## 2. vLinkGenConstGroupAlignment

- **UUID**: `949b2bc4-5910-40ce-a463-3f52a1c9672e`
- **参数名**: `vLinkGenConstGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the section group in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 3. vLinkGenConstGroupGapSize

- **UUID**: `51280186-aa9e-4eb5-a5b4-6e22c383524c`
- **参数名**: `vLinkGenConstGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the section group in bytes.
If zero, no gap is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenConstGroupPreUserCode

- **UUID**: `3d4453d7-d6ac-4306-bfaa-87e79cf53973`
- **参数名**: `vLinkGenConstGroupPreUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#if 0`
- **描述**: Specifies optional preprocessor condition to be generated right before the linker section group.

Example:
#ifdef MIP_USED

######## 2. vLinkGenConstGroupPostUserCode

- **UUID**: `afc47e74-687c-4c10-885e-8197196a2d09`
- **参数名**: `vLinkGenConstGroupPostUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#endif`
- **描述**: Specifies optional end of preprocessor condition to be generated right after the linker section group.

Example:
#endif /* MIP_USED */

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenConstGroupHwRegion

- **UUID**: `1fc2ee6d-7403-4656-b77c-fb59f57c4c5f`
- **引用名**: `vLinkGenConstGroupHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region where the linker section group should be linked to.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vLinkGenConstGroupUserSection

**容器属性**:

- **UUID**: `85bc2b62-6e9d-446a-8a25-8f09a6a4c97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstGroupUserSectionPosition

- **UUID**: `a1df2da8-e74d-4d69-a537-88976ee99b70`
- **参数名**: `vLinkGenConstGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenConstGroupUserSectionValue

- **UUID**: `3accfb5f-fcc7-4abd-8a75-aab86f24edef`
- **参数名**: `vLinkGenConstGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

####### 2. vLinkGenConstGroupCodeSection

**容器属性**:

- **UUID**: `b15a2206-5109-48bb-ad87-ca4def0b4388`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CODE linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenCodeSectionPosition

- **UUID**: `c48d6daa-d471-48d9-b60e-202a645b5c1f`
- **参数名**: `vLinkGenCodeSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenCodeSectionCachePolicyCache

- **UUID**: `116c4b0f-83dc-4a51-9035-b489f26d678e`
- **参数名**: `vLinkGenCodeSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 2. vLinkGenCodeSectionCachePolicyNoCache

- **UUID**: `b83c0503-fd93-4640-97c8-ba08c5138b21`
- **参数名**: `vLinkGenCodeSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 3. vLinkGenCodeSectionAddressingModeNear

- **UUID**: `2088029f-75e4-466e-9528-d60411bdf0c7`
- **参数名**: `vLinkGenCodeSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CODE_FAST) are linked into the linker section group.

########## 4. vLinkGenCodeSectionAddressingModeFar

- **UUID**: `d2e0b324-3489-45bb-8d06-bed3085e446d`
- **参数名**: `vLinkGenCodeSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CODE) are linked into the linker section group.

########## 5. vLinkGenCodeSectionFlagNoLoad

- **UUID**: `3425b75d-a1aa-4ebf-931a-a0728527edaf`
- **参数名**: `vLinkGenCodeSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 6. vLinkGenCodeSectionFlagKeep

- **UUID**: `00926987-ffd5-4ccb-9c40-aa149294ac09`
- **参数名**: `vLinkGenCodeSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenCodeSectionRef

- **UUID**: `7fe98336-2a64-4085-89fd-dc90447e5f64`
- **引用名**: `vLinkGenCodeSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerCodeSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 3. vLinkGenConstGroupConstSection

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CONST linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenConstSectionPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenConstSectionCachePolicyCache

- **UUID**: `ad075b49-088b-465a-8a6e-384b11665caa`
- **参数名**: `vLinkGenConstSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 2. vLinkGenConstSectionCachePolicyNoCache

- **UUID**: `42242b75-91d2-4542-be72-413597ce023f`
- **参数名**: `vLinkGenConstSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 3. vLinkGenConstSectionAddressingModeNear

- **UUID**: `0d9a8462-0b61-46df-baaa-521292f096f0`
- **参数名**: `vLinkGenConstSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CONST_FAST) are linked into the linker section group.

########## 4. vLinkGenConstSectionAddressingModeFar

- **UUID**: `13807cc8-9719-4b0a-92b0-4715989654c5`
- **参数名**: `vLinkGenConstSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CONST) are linked into the linker section group.

########## 5. vLinkGenConstSectionFlagNoLoad

- **UUID**: `e6c017bc-356a-4952-83c2-81e4521ee261`
- **参数名**: `vLinkGenConstSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 6. vLinkGenConstSectionFlagKeep

- **UUID**: `477d7990-dce8-4f56-8b37-966c830ea12f`
- **参数名**: `vLinkGenConstSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenConstSectionRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerConstSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 8. vLinkGenConstGroupUserSection

**容器属性**:

- **UUID**: `85bc2b62-6e9d-446a-8a25-8f09a6a4c97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenConstGroupUserSectionPosition

- **UUID**: `a1df2da8-e74d-4d69-a537-88976ee99b70`
- **参数名**: `vLinkGenConstGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenConstGroupUserSectionValue

- **UUID**: `3accfb5f-fcc7-4abd-8a75-aab86f24edef`
- **参数名**: `vLinkGenConstGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

##### 9. vLinkGenConstGroupCodeSection

**容器属性**:

- **UUID**: `b15a2206-5109-48bb-ad87-ca4def0b4388`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupCodeSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CODE linker sections whose data shall be linked to the linker section group.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenCodeSectionPosition

- **UUID**: `c48d6daa-d471-48d9-b60e-202a645b5c1f`
- **参数名**: `vLinkGenCodeSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### BOOLEAN 类型参数

######## 1. vLinkGenCodeSectionCachePolicyCache

- **UUID**: `116c4b0f-83dc-4a51-9035-b489f26d678e`
- **参数名**: `vLinkGenCodeSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

######## 2. vLinkGenCodeSectionCachePolicyNoCache

- **UUID**: `b83c0503-fd93-4640-97c8-ba08c5138b21`
- **参数名**: `vLinkGenCodeSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

######## 3. vLinkGenCodeSectionAddressingModeNear

- **UUID**: `2088029f-75e4-466e-9528-d60411bdf0c7`
- **参数名**: `vLinkGenCodeSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CODE_FAST) are linked into the linker section group.

######## 4. vLinkGenCodeSectionAddressingModeFar

- **UUID**: `d2e0b324-3489-45bb-8d06-bed3085e446d`
- **参数名**: `vLinkGenCodeSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CODE) are linked into the linker section group.

######## 5. vLinkGenCodeSectionFlagNoLoad

- **UUID**: `3425b75d-a1aa-4ebf-931a-a0728527edaf`
- **参数名**: `vLinkGenCodeSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 6. vLinkGenCodeSectionFlagKeep

- **UUID**: `00926987-ffd5-4ccb-9c40-aa149294ac09`
- **参数名**: `vLinkGenCodeSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenCodeSectionRef

- **UUID**: `7fe98336-2a64-4085-89fd-dc90447e5f64`
- **引用名**: `vLinkGenCodeSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerCodeSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerCodeSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 10. vLinkGenConstGroupConstSection

**容器属性**:

- **UUID**: `713f30b9-83ca-4caa-bda2-169b627ef9e2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenConstGroupConstSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of CONST linker sections whose data shall be linked to the linker section group.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenConstSectionPosition

- **UUID**: `e9de6c3a-d906-44d5-973d-a50258fe5b6d`
- **参数名**: `vLinkGenConstSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### BOOLEAN 类型参数

######## 1. vLinkGenConstSectionCachePolicyCache

- **UUID**: `ad075b49-088b-465a-8a6e-384b11665caa`
- **参数名**: `vLinkGenConstSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

######## 2. vLinkGenConstSectionCachePolicyNoCache

- **UUID**: `42242b75-91d2-4542-be72-413597ce023f`
- **参数名**: `vLinkGenConstSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

######## 3. vLinkGenConstSectionAddressingModeNear

- **UUID**: `0d9a8462-0b61-46df-baaa-521292f096f0`
- **参数名**: `vLinkGenConstSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (CONST_FAST) are linked into the linker section group.

######## 4. vLinkGenConstSectionAddressingModeFar

- **UUID**: `13807cc8-9719-4b0a-92b0-4715989654c5`
- **参数名**: `vLinkGenConstSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (CONST) are linked into the linker section group.

######## 5. vLinkGenConstSectionFlagNoLoad

- **UUID**: `e6c017bc-356a-4952-83c2-81e4521ee261`
- **参数名**: `vLinkGenConstSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 6. vLinkGenConstSectionFlagKeep

- **UUID**: `477d7990-dce8-4f56-8b37-966c830ea12f`
- **参数名**: `vLinkGenConstSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenConstSectionRef

- **UUID**: `f3aa9e28-141b-40d4-9e84-5688355844fe`
- **引用名**: `vLinkGenConstSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerConstSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerConstSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 11. vLinkGenLinkerSectionVarGroup

**容器属性**:

- **UUID**: `8b49ddd5-843c-439b-a745-971b7bf2f5c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionVarGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a VAR linker section group.
It can be used to map several VAR or STACK linker sections to a specific memory region.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenVarGroupPosition

- **UUID**: `39cfef63-abe5-4308-ab2b-ba4b18c57c8e`
- **参数名**: `vLinkGenVarGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the linker section group in the selected hardware memory location.
Relative to other section groups within the same hardware memory location.
If equal, the generation order depends on the order of the group within the configuration file.

######## 2. vLinkGenVarGroupAlignment

- **UUID**: `c0d180bc-a616-4a1a-b2b2-b45da7fb5dbd`
- **参数名**: `vLinkGenVarGroupAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the alignment of the section group in bytes.
If zero, no alignment is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 3. vLinkGenVarGroupInitCore

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
- **描述**: Specifies the physical core ID which shall perform the initialization of all INIT or ZERO_INIT sections assigned to the linker section group.

######## 4. vLinkGenVarGroupGapSize

- **UUID**: `9a680a42-3998-4fb6-b654-91bb68d4b25e`
- **参数名**: `vLinkGenVarGroupGapSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the size of the optional gap to be kept free after the section group in bytes.
If zero, no gap is generated.

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

####### ENUMERATION 类型参数

######## 1. vLinkGenVarGroupInitPolicy

- **UUID**: `5727461f-2b2d-431b-9794-1d6771509c1a`
- **参数名**: `vLinkGenVarGroupInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the ZERO_INIT sections of the linker section group shall be initialized with zeros and when.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for groups containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitAreas*) which can be used to initialize the linker section groups with zeros.
This is normally done by the startup code of the vBRS.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenVarGroupPreUserCode

- **UUID**: `cf10ce38-5f77-427b-a81f-4608f6ebe3b3`
- **参数名**: `vLinkGenVarGroupPreUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#if 0`
- **描述**: Specifies optional preprocessor condition to be generated right before the linker section group.

Example:
#ifdef MIP_USED

######## 2. vLinkGenVarGroupPostUserCode

- **UUID**: `6f82e09b-ab0c-4736-bad5-15a477377b00`
- **参数名**: `vLinkGenVarGroupPostUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **多行字符串变体**:
  - 默认值: `#endif`
- **描述**: Specifies optional end of preprocessor condition to be generated right after the linker section group.

Example:
#endif /* MIP_USED */

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenVarGroupHwRegion

- **UUID**: `3cddb3c3-ee5b-4964-95ac-7d90dcabaf63`
- **引用名**: `vLinkGenVarGroupHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region where the linker section group should be linked to.

######## 2. vLinkGenVarGroupInitDataHwRegion

- **UUID**: `e1b48eab-1434-4092-8b3d-b08f423f3644`
- **引用名**: `vLinkGenVarGroupInitDataHwRegion`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenMemoryRegionBlock`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerMemoryRegion/vLinkGenMemoryRegionBlock`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the memory region block where the init data of the linker section group should be linked to.
This is typically used for initialization of INIT data (ROM to RAM copy).

Note:
Depending on this parameter, the vLinkGen only generates a structure (vLinkGen_DataInitAreas) which can be used to initialize the linker section groups with concrete data.
This is normally done by the startup code of the vBRS.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vLinkGenVarGroupUserSection

**容器属性**:

- **UUID**: `8320d903-5424-4717-b4db-ae97fcc708c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarGroupUserSectionPosition

- **UUID**: `25e1b9cc-45d6-4499-abba-18f7eab3e380`
- **参数名**: `vLinkGenVarGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenVarGroupUserSectionValue

- **UUID**: `5d50f6b3-0851-4b5e-b6d7-77cddbae6822`
- **参数名**: `vLinkGenVarGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

####### 2. vLinkGenVarGroupVarSection

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of VAR linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenVarSectionPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenVarSectionInitPolicyInit

- **UUID**: `ba72293b-ad79-4ccf-8a9d-36b38bf44e14`
- **参数名**: `vLinkGenVarSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

########## 2. vLinkGenVarSectionInitPolicyNoInit

- **UUID**: `e435b476-4ddb-4010-89ea-88e24f4f7ebf`
- **参数名**: `vLinkGenVarSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

########## 3. vLinkGenVarSectionInitPolicyZeroInit

- **UUID**: `4b017c9c-1905-4b5e-977c-f5c08a2fb14d`
- **参数名**: `vLinkGenVarSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

########## 4. vLinkGenVarSectionCachePolicyCache

- **UUID**: `d3c634a3-11cf-45d2-943a-e8cccc2737d3`
- **参数名**: `vLinkGenVarSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 5. vLinkGenVarSectionCachePolicyNoCache

- **UUID**: `67dd430d-fb7e-4b01-9f76-1fcafce20ffa`
- **参数名**: `vLinkGenVarSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 6. vLinkGenVarSectionAddressingModeNear

- **UUID**: `16e76f72-56de-4c05-ac78-13d92534cd3e`
- **参数名**: `vLinkGenVarSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

########## 7. vLinkGenVarSectionAddressingModeFar

- **UUID**: `ddb4f185-a1c7-4b78-b131-b19d4ef71a45`
- **参数名**: `vLinkGenVarSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

########## 8. vLinkGenVarSectionFlagNoLoad

- **UUID**: `8878fa0b-1181-45a8-a7fc-e29483b45857`
- **参数名**: `vLinkGenVarSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 9. vLinkGenVarSectionFlagKeep

- **UUID**: `2067c503-94ef-4bc7-9ec9-cbc576fb831d`
- **参数名**: `vLinkGenVarSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenVarSectionRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerVarSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

####### 3. vLinkGenVarGroupStackSection

**容器属性**:

- **UUID**: `cd4f60ea-6af8-4ae3-adfc-0853a02ac536`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of STACK linker sections whose data shall be linked to the linker section group.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenStackSectionPosition

- **UUID**: `ec7c1492-54cc-43f3-8039-1c4206bbff32`
- **参数名**: `vLinkGenStackSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### BOOLEAN 类型参数

########## 1. vLinkGenStackSectionInitPolicyInit

- **UUID**: `25730b52-4b03-47ef-b575-6c1d100fb1ff`
- **参数名**: `vLinkGenStackSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

########## 2. vLinkGenStackSectionInitPolicyNoInit

- **UUID**: `a0d8710d-4317-405c-8c2d-89f1091e6ac6`
- **参数名**: `vLinkGenStackSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

########## 3. vLinkGenStackSectionInitPolicyZeroInit

- **UUID**: `67069945-12a2-41f9-a48d-ec923c37c2ad`
- **参数名**: `vLinkGenStackSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

########## 4. vLinkGenStackSectionCachePolicyCache

- **UUID**: `cbb08269-4994-41c3-85fd-dfe3b761dcf7`
- **参数名**: `vLinkGenStackSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

########## 5. vLinkGenStackSectionCachePolicyNoCache

- **UUID**: `226c2c8a-146e-41c6-b877-a50df88e9ed0`
- **参数名**: `vLinkGenStackSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

########## 6. vLinkGenStackSectionAddressingModeNear

- **UUID**: `6d22d7fc-1b12-4f3d-afae-c1d69d280baf`
- **参数名**: `vLinkGenStackSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

########## 7. vLinkGenStackSectionAddressingModeFar

- **UUID**: `b01de2b8-5363-4b09-a547-460b0633c92d`
- **参数名**: `vLinkGenStackSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

########## 8. vLinkGenStackSectionFlagNoLoad

- **UUID**: `20b0dd8b-4d4c-4a73-a548-1076034b1a93`
- **参数名**: `vLinkGenStackSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

########## 9. vLinkGenStackSectionFlagKeep

- **UUID**: `75b1000d-c372-430c-a821-8039562ae2b2`
- **参数名**: `vLinkGenStackSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vLinkGenStackSectionRef

- **UUID**: `643d6ec7-9fc8-4803-9280-f5bf59280576`
- **引用名**: `vLinkGenStackSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerStackSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 12. vLinkGenVarGroupUserSection

**容器属性**:

- **UUID**: `8320d903-5424-4717-b4db-ae97fcc708c7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies compiler specific user code that is directly generated into the linker section group at the specified position.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenVarGroupUserSectionPosition

- **UUID**: `25e1b9cc-45d6-4499-abba-18f7eab3e380`
- **参数名**: `vLinkGenVarGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenVarGroupUserSectionValue

- **UUID**: `5d50f6b3-0851-4b5e-b6d7-77cddbae6822`
- **参数名**: `vLinkGenVarGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code.

##### 13. vLinkGenVarGroupVarSection

**容器属性**:

- **UUID**: `25ad9ad6-9ddd-4504-8f22-8cbb10bc9fba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupVarSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of VAR linker sections whose data shall be linked to the linker section group.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenVarSectionPosition

- **UUID**: `7162d559-55e9-4e8c-993b-643d9085b7d8`
- **参数名**: `vLinkGenVarSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### BOOLEAN 类型参数

######## 1. vLinkGenVarSectionInitPolicyInit

- **UUID**: `ba72293b-ad79-4ccf-8a9d-36b38bf44e14`
- **参数名**: `vLinkGenVarSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

######## 2. vLinkGenVarSectionInitPolicyNoInit

- **UUID**: `e435b476-4ddb-4010-89ea-88e24f4f7ebf`
- **参数名**: `vLinkGenVarSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

######## 3. vLinkGenVarSectionInitPolicyZeroInit

- **UUID**: `4b017c9c-1905-4b5e-977c-f5c08a2fb14d`
- **参数名**: `vLinkGenVarSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

######## 4. vLinkGenVarSectionCachePolicyCache

- **UUID**: `d3c634a3-11cf-45d2-943a-e8cccc2737d3`
- **参数名**: `vLinkGenVarSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

######## 5. vLinkGenVarSectionCachePolicyNoCache

- **UUID**: `67dd430d-fb7e-4b01-9f76-1fcafce20ffa`
- **参数名**: `vLinkGenVarSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

######## 6. vLinkGenVarSectionAddressingModeNear

- **UUID**: `16e76f72-56de-4c05-ac78-13d92534cd3e`
- **参数名**: `vLinkGenVarSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

######## 7. vLinkGenVarSectionAddressingModeFar

- **UUID**: `ddb4f185-a1c7-4b78-b131-b19d4ef71a45`
- **参数名**: `vLinkGenVarSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

######## 8. vLinkGenVarSectionFlagNoLoad

- **UUID**: `8878fa0b-1181-45a8-a7fc-e29483b45857`
- **参数名**: `vLinkGenVarSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 9. vLinkGenVarSectionFlagKeep

- **UUID**: `2067c503-94ef-4bc7-9ec9-cbc576fb831d`
- **参数名**: `vLinkGenVarSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenVarSectionRef

- **UUID**: `5751946f-bec9-4c43-92ca-7f86e72172c1`
- **引用名**: `vLinkGenVarSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerVarSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerVarSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 14. vLinkGenVarGroupStackSection

**容器属性**:

- **UUID**: `cd4f60ea-6af8-4ae3-adfc-0853a02ac536`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenVarGroupStackSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies a group of STACK linker sections whose data shall be linked to the linker section group.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenStackSectionPosition

- **UUID**: `ec7c1492-54cc-43f3-8039-1c4206bbff32`
- **参数名**: `vLinkGenStackSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the sections within the linker section group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### BOOLEAN 类型参数

######## 1. vLinkGenStackSectionInitPolicyInit

- **UUID**: `25730b52-4b03-47ef-b575-6c1d100fb1ff`
- **参数名**: `vLinkGenStackSectionInitPolicyInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if INIT sections are linked into the linker section group.

######## 2. vLinkGenStackSectionInitPolicyNoInit

- **UUID**: `a0d8710d-4317-405c-8c2d-89f1091e6ac6`
- **参数名**: `vLinkGenStackSectionInitPolicyNoInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if NOINIT sections are linked into the linker section group.

######## 3. vLinkGenStackSectionInitPolicyZeroInit

- **UUID**: `67069945-12a2-41f9-a48d-ec923c37c2ad`
- **参数名**: `vLinkGenStackSectionInitPolicyZeroInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if ZERO_INIT sections are linked into the linker section group.

######## 4. vLinkGenStackSectionCachePolicyCache

- **UUID**: `cbb08269-4994-41c3-85fd-dfe3b761dcf7`
- **参数名**: `vLinkGenStackSectionCachePolicyCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if cachable sections are linked into the linker section group.

######## 5. vLinkGenStackSectionCachePolicyNoCache

- **UUID**: `226c2c8a-146e-41c6-b877-a50df88e9ed0`
- **参数名**: `vLinkGenStackSectionCachePolicyNoCache`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if non cachable sections (NOCACHE) are linked into the linker section group.

######## 6. vLinkGenStackSectionAddressingModeNear

- **UUID**: `6d22d7fc-1b12-4f3d-afae-c1d69d280baf`
- **参数名**: `vLinkGenStackSectionAddressingModeNear`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with near addressing mode (VAR_FAST) are linked into the linker section group.

######## 7. vLinkGenStackSectionAddressingModeFar

- **UUID**: `b01de2b8-5363-4b09-a547-460b0633c92d`
- **参数名**: `vLinkGenStackSectionAddressingModeFar`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if sections with far addressing mode (VAR) are linked into the linker section group.

######## 8. vLinkGenStackSectionFlagNoLoad

- **UUID**: `20b0dd8b-4d4c-4a73-a548-1076034b1a93`
- **参数名**: `vLinkGenStackSectionFlagNoLoad`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections content shall be loaded into the target system or not.
If enabled the content has to be loaded in some other way into the target system.

true: Do not load sections content into the target system
false: Load sections content into the target system

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

######## 9. vLinkGenStackSectionFlagKeep

- **UUID**: `75b1000d-c372-430c-a821-8039562ae2b2`
- **参数名**: `vLinkGenStackSectionFlagKeep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if the sections shall be forced to be kept by the linker, although it is empty.

true: All sections within this group shall be marked with keep
false: Keep is not generated for the sections

Note:
If the parameter is ReadOnly, it is not supported by the selected compiler.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vLinkGenStackSectionRef

- **UUID**: `643d6ec7-9fc8-4803-9280-f5bf59280576`
- **引用名**: `vLinkGenStackSectionRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `vLinkGenLinkerStackSection`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenMemLayout/vLinkGenLinkerSections/vLinkGenLinkerStackSection`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the sections which shall be linked into the linker section group.

##### 15. vLinkGenLinkerSectionUserGroup

**容器属性**:

- **UUID**: `6973e9c1-cf16-46f5-be08-019313cfe6a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerSectionUserGroup`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for an user code group.
User code groups are generated either at the beginning or at the end of the linker script.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenUserGroupPosition

- **UUID**: `f41e4a9d-884e-411a-b8ff-b0332bfe6028`
- **参数名**: `vLinkGenUserGroupPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code group.
If equal, the generation order depends on the order of the group within the configuration file.

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
- **描述**: Specifies whether the user code group is generated at the beginning or the end of the linker script.

PRE: The user code group is generated at the beginning of the linker script.
POST: The user code group is generated at the end of the linker script.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vLinkGenUserGroupUserSection

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vLinkGenUserGroupUserSectionPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code section within the user code group.
If equal, the generation order depends on the order of the sections within the configuration file.

######### MULTILINE-STRING 类型参数

########## 1. vLinkGenUserGroupUserSectionValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

##### 16. vLinkGenUserGroupUserSection

**容器属性**:

- **UUID**: `68364a08-4209-43f6-b6ad-e1ade434e36a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenUserGroupUserSection`
- **多重性**: [0..infinite]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

Specifies an user code section that is generated into the linker script at the specified position.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vLinkGenUserGroupUserSectionPosition

- **UUID**: `654f97b7-0899-499c-91fd-d50f4486fb41`
- **参数名**: `vLinkGenUserGroupUserSectionPosition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the position of the user code section within the user code group.
If equal, the generation order depends on the order of the sections within the configuration file.

####### MULTILINE-STRING 类型参数

######## 1. vLinkGenUserGroupUserSectionValue

- **UUID**: `df8dbbd8-aa6a-4065-9249-312ce6082125`
- **参数名**: `vLinkGenUserGroupUserSectionValue`
- **数据类型**: MULTILINE-STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the compiler specific user code that is directly generated into the linker script.

##### 17. vLinkGenLinkerMemoryRegion

**容器属性**:

- **UUID**: `b5e4333c-3c89-4262-a6ee-433bce751d7f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenLinkerMemoryRegion`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for one memory region.
Memory regions has to be mapped to concrete hardware regions which are predefined in vBaseEnv.

###### 参数配置

此容器包含 **2** 个参数：

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
- **描述**: Specifies the offset of the memory rergion to the referenced hardware region start address.

Memory Region Start Address = Hardware Region Start Address + Address Offset

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
- **描述**: This value specifies the size of the memory region in bytes.

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
- **描述**: Reference to the hardware memory area where the memory region should be mapped to.

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

This container includes all configuration parameters for a memory region block.
Memory region blocks can be used to partition a memory region.

######## 参数配置

此容器包含 **5** 个参数：

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
- **描述**: This value specifies the position of the memory region block within the memory region.

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
- **描述**: This value specifies the size of the memory region block in bytes.

########## 3. vLinkGenMemoryRegionBlockInitCore

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
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the memory region block.

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
- **描述**: This value defines the boundary of the memory region block.

LOWER: The memory region block is linked to the lower boundary of the memory region
UPPER: The memory region block is linked to the upper boundary of the memory region

########## 2. vLinkGenMemoryRegionBlockInitPolicy

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete memory region block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if a hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for memory region blocks containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitBlocks*) which can be used to initialize the memory region blocks with zeros.
This is normally done by the startup code of the vBRS.

##### 18. vLinkGenMemoryRegionBlock

**容器属性**:

- **UUID**: `df9c02a1-2077-423f-bed0-4840b6904709`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vLinkGenMemoryRegionBlock`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes all configuration parameters for a memory region block.
Memory region blocks can be used to partition a memory region.

###### 参数配置

此容器包含 **5** 个参数：

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
- **描述**: This value specifies the position of the memory region block within the memory region.

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
- **描述**: This value specifies the size of the memory region block in bytes.

######## 3. vLinkGenMemoryRegionBlockInitCore

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
- **描述**: Specifies the physical core ID which shall perform the zero initialization of the memory region block.

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
- **描述**: This value defines the boundary of the memory region block.

LOWER: The memory region block is linked to the lower boundary of the memory region
UPPER: The memory region block is linked to the upper boundary of the memory region

######## 2. vLinkGenMemoryRegionBlockInitPolicy

- **UUID**: `64acba45-2880-4fd7-a131-faf2be46b417`
- **参数名**: `vLinkGenMemoryRegionBlockInitPolicy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `ALWAYS` (来源: Vector Informatik)
  - `HARD_RESET` (来源: Vector Informatik)
  - `FOREIGN` (来源: Vector Informatik)
  - `STARTUP` (来源: Vector Informatik)
- **描述**: This parameter defines whether the complete memory region block shall be initialized with zeros and when.
This is typically required for ECC protected memory areas before the first read or write access.

NONE: No zero initialization required.
ALWAYS: Initialize always after the PLL initialization is done.
HARD_RESET: Initialize after the PLL initialization is done, only if a hardware reset occured.
FOREIGN: Initialization is done by another instance.
STARTUP: Initialize always directly after reset. Normally only for memory region blocks containing the startup stack.

Note:
Depending on this parameter, the vLinkGen only generates structures (vLinkGen_ZeroInitBlocks*) which can be used to initialize the memory region blocks with zeros.
This is normally done by the startup code of the vBRS.

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
- **软件版本**: 1.07.03
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator
