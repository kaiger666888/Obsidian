# vDem42 - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:01

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vDem42](#vdem42)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vDem42

#### 基本信息

- **UUID**: `32a616ec-5d83-4ff8-ad6e-786b17399581`
- **模块名称**: `vDem42`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Diagnostic Software Component vDem42. vDem42 is an adapter component which translates certain DEM AUTOSAR 4.3 
interfaces to AUTOSAR 4.2.2.
#Diag
#Vector #ServiceComponent

#### 版本历史

共有 **4** 个版本记录：

##### 1. 版本 1.1.0

- **状态**: release
- **发布日期**: 2017-10-05T02:16:05+02:00
- **发布者**: visstk

**变更内容**:

##### 2. 版本 1.2.0

- **状态**: release
- **发布日期**: 2018-03-02T08:53:48+01:00
- **发布者**: visaey

**变更内容**:

##### 3. 版本 1.3.1

- **状态**: release
- **发布日期**: 2021-11-30T18:15:15+01:00
- **发布者**: visygr

**变更内容**:

##### 4. 版本 2.0.0

- **状态**: release
- **发布日期**: 2022-02-18T14:19:13+01:00
- **发布者**: visepp

**变更内容**:

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 2

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vDem42_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vDem42**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vDem42_Impl

- **UUID**: `d7cc4baa-7d44-4399-8032-f72a038be15f`
- **实现名称**: `vDem42_Impl`
- **编程语言**: C
- **软件版本**: 2.0.0
- **供应商ID**: 30
- **AUTOSAR版本**: 4.2.2
