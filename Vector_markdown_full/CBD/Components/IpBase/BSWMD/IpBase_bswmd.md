# IpBase - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [IpBase](#ipbase)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. IpBase

#### 基本信息

- **UUID**: `32a616ec-5d83-4ff8-ad6e-786b17399581`
- **模块名称**: `IpBase`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 版本历史

共有 **2** 个版本记录：

##### 1. 版本 1.02.00

- **状态**: release
- **发布日期**: 2023-09-26T16:06:59+02:00
- **发布者**: visalr

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: release
- **发布日期**: 2023-04-12T16:06:59+02:00
- **发布者**: vissop

**变更内容**:

#### 配置容器

本模块包含 **1** 个配置容器：

##### 1. IpBaseGeneral

**容器属性**:

- **UUID**: `2fea153c-34d4-40d7-8e41-bbde15b2b4a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `IpBaseGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. IpBaseDevErrorReport

- **UUID**: `52d891f1-e899-4802-8f15-ce1502a8b1be`
- **参数名**: `IpBaseDevErrorReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true then IpBase will enable the error-reporting to the Development Error Tracer (DET).

######## 2. IpBaseEnableInlineFunctions

- **UUID**: `52d891f1-e899-4802-8f15-ce1502a8b1bd`
- **参数名**: `IpBaseEnableInlineFunctions`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true then IpBase will enable inline functions for Byte swap, put and get macros and internal functions. Can be switched off to ease white box testing and debugging.

######## 3. IpBaseOneStepChecksumCopy

- **UUID**: `52d891f1-e899-4802-8f15-ce1502a8b1ce`
- **参数名**: `IpBaseOneStepChecksumCopy`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If true then IpBase will copy and checksum calculation in one step. Enabling will speed up the calculation but increase the code size (ROM). Switching off may help in case of memory alignment issues.

####### ENUMERATION 类型参数

######## 1. IpBaseSizeOfRamPointer

- **UUID**: `e4d9d1de-c2ea-471f-9be9-c30941b6ed05`
- **参数名**: `IpBaseSizeOfRamPointer`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `uint32`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `uint32` (来源: Vector Informatik)
  - `uint64` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the bit size of RAM pointers used for the UDP and TCP data type for the checksumm calculation. Pointer size equals the CPU register size on most platforms.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **IpBase_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **IpBase**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. IpBase_Impl

- **UUID**: `d7cc4baa-7d44-4399-8032-f72a038be15f`
- **实现名称**: `IpBase_Impl`
- **编程语言**: C
- **软件版本**: 4.02.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
