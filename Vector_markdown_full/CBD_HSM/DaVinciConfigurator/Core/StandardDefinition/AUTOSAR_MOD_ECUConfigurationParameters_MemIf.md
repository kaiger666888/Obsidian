# MemIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:54

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [MemIf](#memif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. MemIf

#### 基本信息

- **UUID**: `ECUC:e9996ea9-86d2-4fb6-84a8-ef41aa695198`
- **模块名称**: `MemIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the MemIf (Memory Abstraction Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **1** 个配置容器：

##### 1. MemIfGeneral

**容器属性**:

- **UUID**: `ECUC:e338145a-6813-4489-af1f-25eedc3a3b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemIfGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Configuration of the memory abstraction interface (Memif) module.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MemIfNumberOfDevices

- **UUID**: `ECUC:ceddbf0c-99ad-44b1-9f1f-08c2a65ca876`
- **参数名**: `MemIfNumberOfDevices`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Concrete number of underlying memory abstraction modules.

####### BOOLEAN 类型参数

######## 1. MemIfDevErrorDetect

- **UUID**: `ECUC:a26c464b-6da2-4a86-89e9-946ceb9024b0`
- **参数名**: `MemIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection.

######## 2. MemIfVersionInfoApi

- **UUID**: `ECUC:2ccf46a6-5f32-42c8-b33a-9be3d2b1f0a9`
- **参数名**: `MemIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **MemIf**
