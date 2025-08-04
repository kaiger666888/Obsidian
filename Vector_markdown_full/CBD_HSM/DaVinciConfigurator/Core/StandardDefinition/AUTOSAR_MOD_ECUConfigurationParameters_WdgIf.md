# WdgIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:52:00

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [WdgIf](#wdgif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. WdgIf

#### 基本信息

- **UUID**: `ECUC:a2dc5f81-f4d5-4986-bf4b-38652d4a8126`
- **模块名称**: `WdgIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the WdgIf (Watchdog Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **2** 个配置容器：

##### 1. WdgIfDevice

**容器属性**:

- **UUID**: `ECUC:b5418b77-eccf-4831-acdd-b50dbb01413b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfDevice`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

It contains the information for the selection of a particular Watchdog device in case multiple Watchdog drivers are connected.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. WdgIfDeviceIndex

- **UUID**: `ECUC:41e5cd64-56e8-4593-b945-b615918cd5a7`
- **参数名**: `WdgIfDeviceIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Represents the watchdog interface ID so that it can be referenced by the watchdog manager.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. WdgIfDriverRef

- **UUID**: `ECUC:c18b762d-1ffc-4203-9936-4e4539c6fea6`
- **引用名**: `WdgIfDriverRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `WdgGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Wdg/WdgGeneral`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the watchdog drivers that are controlled by the watchdog interface.

##### 2. WdgIfGeneral

**容器属性**:

- **UUID**: `ECUC:2199b96d-33aa-488f-a1ae-99f6d4bd3c6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `WdgIfGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container collects all generic watchdog interface parameters.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. WdgIfDevErrorDetect

- **UUID**: `ECUC:4363aa34-c419-4350-b2cb-75ec7dfda67f`
- **参数名**: `WdgIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch for enabling the development error detection and reporting.

######## 2. WdgIfVersionInfoApi

- **UUID**: `ECUC:313c10c6-c907-4f72-a6d8-722b8886775b`
- **参数名**: `WdgIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the service returning the version information.

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

1. **WdgIf**
