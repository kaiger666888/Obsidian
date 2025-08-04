# vSet - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:06

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

#### 版本历史

共有 **3** 个版本记录：

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

#### 配置容器

本模块包含 **3** 个配置容器：

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
