# vSet - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vSet](#vset)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vSet

#### 基本信息

- **UUID**: `c4d6e280-1fca-43b1-8dd2-d622ab48ee13`
- **模块名称**: `vSet`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The virtual Vector Common Settings module collects global and ECU specific configuration information.

#### 版本历史

共有 **9** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2017-02-20
- **发布者**: visms

**变更内容**:

##### 2. 版本 2.00.00

- **发布日期**: 2018-03-26T14:22:20+02:00
- **发布者**: visms

**变更内容**:

##### 3. 版本 2.00.00

- **发布日期**: 2018-03-26T14:48:29+02:00
- **发布者**: visms

**变更内容**:

##### 4. 版本 2.01.00

- **发布日期**: 2021-06-29T14:48:29+02:00
- **发布者**: visms

**变更内容**:

##### 5. 版本 3.00.00

- **发布日期**: 2021-10-19T14:48:29+02:00
- **发布者**: visms

**变更内容**:

##### 6. 版本 3.00.00

- **发布日期**: 2021-10-27T12:57:54+02:00
- **发布者**: visms

**变更内容**:

##### 7. 版本 3.00.00

- **发布日期**: 2021-10-27T12:57:56+02:00
- **发布者**: visms

**变更内容**:

##### 8. 版本 3.00.01

- **发布日期**: 2022-01-31T10:41:03+01:00
- **发布者**: visms

**变更内容**:

##### 9. 版本 3.01.00

- **发布日期**: 2022-04-12T10:41:03+01:00
- **发布者**: visms

**变更内容**:

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. vSetGeneral

**容器属性**:

- **UUID**: `2a8265a4-bf89-4189-ae04-6fbf5b5dd00e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. vSetDummyStatementKind

- **UUID**: `f691fcc2-b1ef-4e27-99d4-80cf10db8943`
- **参数名**: `vSetDummyStatementKind`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `None`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `None` (来源: Vector Informatik)
  - `VoidCast` (来源: Vector Informatik)
  - `SelfAssignment` (来源: Vector Informatik)
  - `UserDefined` (来源: Vector Informatik)
- **描述**: Dummy statements used to avoid compiler warnings about e.g. unused parameters.

##### 2. vSetPlatform

**容器属性**:

- **UUID**: `c6b2a864-4d19-46bf-8511-32780b6b40d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetPlatform`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General platform and compiler specific parameters.

###### 参数配置

此容器包含 **7** 个参数：

####### ENUMERATION 类型参数

######## 1. vSetByteOrder

- **UUID**: `b54c8e07-5a67-44e3-9813-93587a4928d3`
- **参数名**: `vSetByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: Vector Informatik)
  - `LITTLE_ENDIAN` (来源: Vector Informatik)
- **描述**: Byte order on memory level.

######## 2. vSetBitOrder

- **UUID**: `95c710a7-d933-4f75-acde-7101af946fd7`
- **参数名**: `vSetBitOrder`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LSB_to_MSB` (来源: Vector Informatik)
  - `MSB_to_LSB` (来源: Vector Informatik)
- **描述**: Bit order on register level.

######## 3. vSetCPUType

- **UUID**: `3af8ac42-5ed5-4dbd-aa2c-22bd6f3a68dc`
- **参数名**: `vSetCPUType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CPU8Bit` (来源: Vector Informatik)
  - `CPU16Bit` (来源: Vector Informatik)
  - `CPU32Bit` (来源: Vector Informatik)
  - `CPU64Bit` (来源: Vector Informatik)
- **描述**: Register width of the CPU in bit.

######## 4. vSetSizeOfEnum

- **UUID**: `7a331f19-8133-45a6-ab80-22ebf18b5fea`
- **参数名**: `vSetSizeOfEnum`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size8Bit` (来源: Vector Informatik)
  - `Size16Bit` (来源: Vector Informatik)
  - `Size32Bit` (来源: Vector Informatik)
- **描述**: Size of type enum in bit.

######## 5. vSetSizeOfInt

- **UUID**: `deae1120-8220-4a8f-9507-89a314f42889`
- **参数名**: `vSetSizeOfInt`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit` (来源: Vector Informatik)
  - `Size32Bit` (来源: Vector Informatik)
- **描述**: Size of type int in bit.

######## 6. vSetSizeOfROMPointer

- **UUID**: `30dbc95a-6c19-495c-943b-b7a69a514fb9`
- **参数名**: `vSetSizeOfROMPointer`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit` (来源: Vector Informatik)
  - `Size24Bit` (来源: Vector Informatik)
  - `Size32Bit` (来源: Vector Informatik)
  - `Size64Bit` (来源: Vector Informatik)
- **描述**: Size of ROM pointer in bit.

######## 7. vSetSizeOfRAMPointer

- **UUID**: `4272f486-5b0b-4bb9-b30d-6461ed776365`
- **参数名**: `vSetSizeOfRAMPointer`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Size16Bit` (来源: Vector Informatik)
  - `Size24Bit` (来源: Vector Informatik)
  - `Size32Bit` (来源: Vector Informatik)
  - `Size64Bit` (来源: Vector Informatik)
- **描述**: Size of RAM pointer in bit.

##### 3. vSetCalibration

**容器属性**:

- **UUID**: `182db01f-1a8d-4a5b-b23f-cf1b1677d008`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetCalibration`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General calibration specific parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vSetPBCalibrationVirtualStartAddress

- **UUID**: `8bac8384-4730-4640-9cc3-68abc25ae0be`
- **参数名**: `vSetPBCalibrationVirtualStartAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Start address of the virtual memory segment for calibration of post-build loadable parameters.

The memory segment is used by standard calibration tools like vCDMStudio to display and manage post-build loadable parameters in a physical representation. The segment is only available in the HEX-file and the data base of the calibration tool. It is not transferred to the ECU's memory. The address should not lie in the address range of the ECU. Recommended is an address beyond the ECU's address range because the virtual memory segment size depends on the concrete configuration and is calculated automatically.

##### 4. vSetBswInitialization

**容器属性**:

- **UUID**: `4f598c5c-13c0-4810-b873-2c14405d8cd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetBswInitialization`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

General BSW initialization specific parameters.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vSetInitFunction

**容器属性**:

- **UUID**: `d3bc0d27-2a62-408d-968a-0cc12e56da8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunction`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. vSetHeader

- **UUID**: `35723054-7b81-443b-9602-93c45191d322`
- **参数名**: `vSetHeader`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Header which declares function and types.

########## 2. vSetConfigType

- **UUID**: `a2e751d0-35d6-440c-bfbc-7f1d5e7b64fc`
- **参数名**: `vSetConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of ConfigType

########## 3. vSetConfigPtrClass

- **UUID**: `4deef034-a7b5-4178-aea8-317624cddf3c`
- **参数名**: `vSetConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Memory class of Config Pointer.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. vSetModuleRef

- **UUID**: `f079f99e-85e7-48af-941a-c599c6117196`
- **引用名**: `vSetModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to module for initialization.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vSetInitFunctionInstance

**容器属性**:

- **UUID**: `a8714000-6e2e-466f-a28d-d1c1f370d6ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunctionInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an instance of the Init Function. For each partition which needs initialization, one container instance needs to be created.

########## 参数配置

此容器包含 **3** 个参数：

########### STRING 类型参数

############ 1. vSetAdditionalInitCode

- **UUID**: `c2685740-2596-46e5-b367-77f803f9c19e`
- **参数名**: `vSetAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

############ 2. vSetConfigPtrName

- **UUID**: `bb1fa8ec-a493-4d3b-a26e-39c2a7fb2a83`
- **参数名**: `vSetConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

########### ENUMERATION 类型参数

############ 1. vSetInitPhase

- **UUID**: `0f55b944-625b-40a4-8fc9-401537fa2151`
- **参数名**: `vSetInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **描述**: Phase in which this init function shall be called.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vSetEcuCPartitionRef

- **UUID**: `59d826f0-cc91-4e5b-b881-dbc6aa7186bf`
- **引用名**: `vSetEcuCPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the EcuC Partition this init function belongs to.

####### 2. vSetInitFunctionInstance

**容器属性**:

- **UUID**: `a8714000-6e2e-466f-a28d-d1c1f370d6ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunctionInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an instance of the Init Function. For each partition which needs initialization, one container instance needs to be created.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. vSetAdditionalInitCode

- **UUID**: `c2685740-2596-46e5-b367-77f803f9c19e`
- **参数名**: `vSetAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

########## 2. vSetConfigPtrName

- **UUID**: `bb1fa8ec-a493-4d3b-a26e-39c2a7fb2a83`
- **参数名**: `vSetConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

######### ENUMERATION 类型参数

########## 1. vSetInitPhase

- **UUID**: `0f55b944-625b-40a4-8fc9-401537fa2151`
- **参数名**: `vSetInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **描述**: Phase in which this init function shall be called.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vSetEcuCPartitionRef

- **UUID**: `59d826f0-cc91-4e5b-b881-dbc6aa7186bf`
- **引用名**: `vSetEcuCPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the EcuC Partition this init function belongs to.

##### 5. vSetInitFunction

**容器属性**:

- **UUID**: `d3bc0d27-2a62-408d-968a-0cc12e56da8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunction`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Name of the init function.

E.g. ComM_Init

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. vSetHeader

- **UUID**: `35723054-7b81-443b-9602-93c45191d322`
- **参数名**: `vSetHeader`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Header which declares function and types.

######## 2. vSetConfigType

- **UUID**: `a2e751d0-35d6-440c-bfbc-7f1d5e7b64fc`
- **参数名**: `vSetConfigType`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of ConfigType

######## 3. vSetConfigPtrClass

- **UUID**: `4deef034-a7b5-4178-aea8-317624cddf3c`
- **参数名**: `vSetConfigPtrClass`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Memory class of Config Pointer.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. vSetModuleRef

- **UUID**: `f079f99e-85e7-48af-941a-c599c6117196`
- **引用名**: `vSetModuleRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: ECUC-MODULE-CONFIGURATION-VALUES
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to module for initialization.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vSetInitFunctionInstance

**容器属性**:

- **UUID**: `a8714000-6e2e-466f-a28d-d1c1f370d6ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunctionInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an instance of the Init Function. For each partition which needs initialization, one container instance needs to be created.

######## 参数配置

此容器包含 **3** 个参数：

######### STRING 类型参数

########## 1. vSetAdditionalInitCode

- **UUID**: `c2685740-2596-46e5-b367-77f803f9c19e`
- **参数名**: `vSetAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

########## 2. vSetConfigPtrName

- **UUID**: `bb1fa8ec-a493-4d3b-a26e-39c2a7fb2a83`
- **参数名**: `vSetConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

######### ENUMERATION 类型参数

########## 1. vSetInitPhase

- **UUID**: `0f55b944-625b-40a4-8fc9-401537fa2151`
- **参数名**: `vSetInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **描述**: Phase in which this init function shall be called.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vSetEcuCPartitionRef

- **UUID**: `59d826f0-cc91-4e5b-b881-dbc6aa7186bf`
- **引用名**: `vSetEcuCPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the EcuC Partition this init function belongs to.

##### 6. vSetInitFunctionInstance

**容器属性**:

- **UUID**: `a8714000-6e2e-466f-a28d-d1c1f370d6ad`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vSetInitFunctionInstance`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

This container represents an instance of the Init Function. For each partition which needs initialization, one container instance needs to be created.

###### 参数配置

此容器包含 **3** 个参数：

####### STRING 类型参数

######## 1. vSetAdditionalInitCode

- **UUID**: `c2685740-2596-46e5-b367-77f803f9c19e`
- **参数名**: `vSetAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Specify additional code which can be referenced from the initialization callouts of EcuM and BswM.

E.g.: Mcu_InitClock()

If it is necessary to call a function with a module pointer from the global postbuild-loadable configuration, the placeholder %CONFIGPTR% can be used:

E.g.: Mcu_Init(%CONFIGPTR%)

######## 2. vSetConfigPtrName

- **UUID**: `bb1fa8ec-a493-4d3b-a26e-39c2a7fb2a83`
- **参数名**: `vSetConfigPtrName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Name of Config Pointer which shall be passed to function. If Empty no parameter is passed. If Init Function has a pointer, at least a NULL_PTR should be inserted here.

####### ENUMERATION 类型参数

######## 1. vSetInitPhase

- **UUID**: `0f55b944-625b-40a4-8fc9-401537fa2151`
- **参数名**: `vSetInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `INIT_TWO_POST_NVMREADALL`
- **作用域**: ECU
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **描述**: Phase in which this init function shall be called.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vSetEcuCPartitionRef

- **UUID**: `59d826f0-cc91-4e5b-b881-dbc6aa7186bf`
- **引用名**: `vSetEcuCPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **作用域**: ECU
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the EcuC Partition this init function belongs to.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vSet_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vSet**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vSet_Pre**
2. **vSet_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vSet_Impl

- **UUID**: `f31abfdd-507b-42af-8f51-688c536289c0`
- **实现名称**: `vSet_Impl`
- **编程语言**: C
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vSet_Pre

- **UUID**: `6cd518c0-b6e2-4237-8ea5-296f67ddf0f8`
- **配置名称**: `vSet_Pre`
- **定义引用**: `/MICROSAR/vSet`

### 2. vSet_Rec

- **UUID**: `e630bc81-3bf5-4f6a-8b06-89e111edc4bb`
- **配置名称**: `vSet_Rec`
- **定义引用**: `/MICROSAR/vSet`
