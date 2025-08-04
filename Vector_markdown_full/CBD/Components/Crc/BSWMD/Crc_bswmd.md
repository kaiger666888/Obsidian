# Crc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:41

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crc](#crc)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crc

#### 基本信息

- **UUID**: `0e4e0c80-fcde-4522-82f6-36f893c5725f`
- **模块名称**: `Crc`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Cyclic Redundancy Check Library. The library provides routines for several CRC calculation algorithms.
#Library #CRC #CyclicRedundancyCheck
#AUTOSAR

#### 版本历史

共有 **23** 个版本记录：

##### 1. 版本 4.0.0

- **状态**: released
- **发布日期**: 2012-08-21T01:00:28+02:00
- **发布者**: virmz

**变更内容**:

##### 2. 版本 4.0.1

- **状态**: released
- **发布日期**: 2012-08-21T01:00:28+02:00
- **发布者**: virtsd

**变更内容**:

##### 3. 版本 5.00.00

- **状态**: released
- **发布日期**: 2012-07-14T01:00:28+02:00
- **发布者**: virmfr

**变更内容**:

##### 4. 版本 

- **发布日期**: 2013-09-16T03:08:45+02:00
- **发布者**: virjas

**变更内容**:

##### 5. 版本 5.01.00

- **状态**: released
- **发布日期**: 2014-03-19T01:32:03+01:00
- **发布者**: virgmi

**变更内容**:

##### 6. 版本 5.02.00

- **发布日期**: 2014-03-21T08:23:14+01:00
- **发布者**: virgmi

**变更内容**:

##### 7. 版本 5.02.01

- **状态**: released
- **发布日期**: 2014-06-11T03:37:08+02:00
- **发布者**: virgmi

**变更内容**:

##### 8. 版本 5.02.02

- **状态**: released
- **发布日期**: 2014-11-17T08:42:59+01:00
- **发布者**: virgmi

**变更内容**:

##### 9. 版本 

- **状态**: released
- **发布日期**: 2014-11-17T03:47:07+01:00
- **发布者**: virgmi

**变更内容**:

##### 10. 版本 5.03.00

- **状态**: released
- **发布日期**: 2015-04-30T03:07:30+02:00
- **发布者**: virgmi

**变更内容**:

##### 11. 版本 5.04.00

- **状态**: released
- **发布日期**: 2015-09-18T03:29:27+02:00
- **发布者**: virgmi

**变更内容**:

##### 12. 版本 

- **状态**: released
- **发布日期**: 2015-09-18T03:29:45+02:00
- **发布者**: virgmi

**变更内容**:

##### 13. 版本 

- **状态**: released
- **发布日期**: 2015-10-06T09:37:54+02:00
- **发布者**: virgmi

**变更内容**:

##### 14. 版本 5.05.00

- **状态**: released
- **发布日期**: 2016-11-22T03:35:16+01:00
- **发布者**: virgmi

**变更内容**:

##### 15. 版本 5.05.01

- **状态**: released
- **发布日期**: 2017-06-08T08:25:43+02:00
- **发布者**: virgmi

**变更内容**:

##### 16. 版本 5.05.02

- **状态**: released
- **发布日期**: 2019-05-15T13:05:12+02:00
- **发布者**: virsrl

**变更内容**:

##### 17. 版本 6.00.00

- **状态**: released
- **发布日期**: 2020-05-25T10:19:52+02:00
- **发布者**: virljs

**变更内容**:

##### 18. 版本 

- **状态**: released
- **发布日期**: 2020-06-08T14:19:28+02:00
- **发布者**: virsrl

**变更内容**:

##### 19. 版本 6.00.01

- **状态**: released
- **发布日期**: 2020-09-03T10:17:36+02:00
- **发布者**: virljs

**变更内容**:

##### 20. 版本 6.00.02

- **状态**: released
- **发布日期**: 2021-08-09T14:08:40+02:00
- **发布者**: virljs

**变更内容**:

##### 21. 版本 7.00.00

- **状态**: released
- **发布日期**: 2022-02-22T09:51:11+01:00
- **发布者**: vireno

**变更内容**:

##### 22. 版本 7.00.01

- **状态**: released
- **发布日期**: 2022-10-04T16:31:01+02:00
- **发布者**: vireno

**变更内容**:

##### 23. 版本 8.00.00

- **状态**: released
- **发布日期**: 2024-02-08T15:53:16+01:00
- **发布者**: vireno

**变更内容**:

#### 配置容器

本模块包含 **1** 个配置容器：

##### 1. CrcGeneral

**容器属性**:

- **UUID**: `d52f25dc-f832-438d-b9d5-ffe669e31dda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CrcGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration of the CRC

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. CrcVersionInfoApi

- **UUID**: `68a496fa-6148-441b-971e-6ae523161d12`
- **参数名**: `CrcVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function Crc_GetVersionInfo() to get major, minor and patch version information.

####### ENUMERATION 类型参数

######## 1. Crc16Mode

- **UUID**: `a268280f-9479-4438-a41d-1ae2d19cfeb3`
- **参数名**: `Crc16Mode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_16_TABLE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_16_RUNTIME`
  - `CRC_16_TABLE`
  - `CRC_16_TABLE_4` (来源: Vector Informatik)
  - `CRC_16_TABLE_8` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch selects one of the available CRC16 calculation methods.

######## 2. Crc32Mode

- **UUID**: `0d6b225b-f092-4de0-9217-e68e0b468d4e`
- **参数名**: `Crc32Mode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_32_TABLE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_32_RUNTIME`
  - `CRC_32_TABLE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch selects one of the available CRC32 calculation methods.

######## 3. Crc8H2FMode

- **UUID**: `61f0d61f-ab57-4f96-afb8-72c18ed3c213`
- **参数名**: `Crc8H2FMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_8H2F_TABLE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_8H2F_RUNTIME`
  - `CRC_8H2F_TABLE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch selects one of the available CRC 8-bit calculation methods with 0x2F CRC polynomial.

######## 4. Crc8Mode

- **UUID**: `af7d2d32-5386-4923-b8b7-b3cac0455da5`
- **参数名**: `Crc8Mode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_8_TABLE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_8_RUNTIME`
  - `CRC_8_TABLE`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch selects one of the available CRC 8-bit (SAE J1850) calculation methods.

######## 5. Crc32P4Mode

- **UUID**: `ab130e6c-4883-4e0d-a2ac-2a1d09552a93`
- **参数名**: `Crc32P4Mode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_32P4_TABLE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_32P4_RUNTIME` (来源: Vector Informatik)
  - `CRC_32P4_TABLE` (来源: Vector Informatik)
  - `CRC_32P4_TABLE_4` (来源: Vector Informatik)
  - `CRC_32P4_TABLE_8` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to select one of the available CRC 32-bit E2E Profile 4 calculation methods.

######## 6. Crc64Mode

- **UUID**: `2b83c2e8-79bc-478d-929a-1c0ca73bb514`
- **参数名**: `Crc64Mode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CRC_64_TABLE`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `CRC_64_RUNTIME`
  - `CRC_64_TABLE`
  - `CRC_64_TABLE_4` (来源: Vector Informatik)
  - `CRC_64_TABLE_8` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch selects one of the available CRC 64-bit (ECMA) calculation methods.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Crc**

##### BSW-IMPLEMENTATION 类型元素

1. **Crc_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Crc_Pre**
2. **Crc_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Crc_Impl

- **UUID**: `672f90a8-afb4-45a6-bfe8-5fa8c6be9d73`
- **实现名称**: `Crc_Impl`
- **编程语言**: C
- **软件版本**: 8.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Crc_Pre

- **UUID**: `3f03a607-0aa4-4650-9ddf-82ab765f13ba`
- **配置名称**: `Crc_Pre`
- **定义引用**: `/MICROSAR/Crc`

### 2. Crc_Rec

- **UUID**: `72bef8a0-d678-4c0d-b5b1-767514d06e0e`
- **配置名称**: `Crc_Rec`
- **定义引用**: `/MICROSAR/Crc`
