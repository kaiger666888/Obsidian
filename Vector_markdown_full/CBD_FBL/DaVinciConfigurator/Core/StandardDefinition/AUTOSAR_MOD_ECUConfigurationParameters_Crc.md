# Crc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:37

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Crc](#crc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Crc

#### 基本信息

- **UUID**: `ECUC:8fc09477-4d31-48bf-9fcc-0f2e51345aad`
- **模块名称**: `Crc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Crc (Crc routines) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **1** 个配置容器：

##### 1. CrcGeneral

**容器属性**:

- **UUID**: `ECUC:022760ec-ae2e-4125-96ad-ca206d355f95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CrcGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration of CRC module

###### 参数配置

此容器包含 **4** 个参数：

####### ENUMERATION 类型参数

######## 1. Crc16Mode

- **UUID**: `ECUC:57dcff50-89c4-444b-b345-2c797a2880f7`
- **参数名**: `Crc16Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_16_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_16_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_16_TABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to select one of the available CRC 16-bit (CCITT) calculation methods

######## 2. Crc32Mode

- **UUID**: `ECUC:17071ba5-9db3-4cb9-a8ec-b5c97e935977`
- **参数名**: `Crc32Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_32_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_32_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_32_TABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to select one of the available CRC 32-bit (IEEE-802.3 CRC32 Ethernet Standard) calculation methods

######## 3. Crc8H2FMode

- **UUID**: `ECUC:4e2ed5e0-022e-415d-9e9c-ce4263e08b97`
- **参数名**: `Crc8H2FMode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_8H2F_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_8H2F_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_8H2F_TABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to select one of the available CRC 8-bit (2Fh polynomial) calculation methods

######## 4. Crc8Mode

- **UUID**: `ECUC:965dd362-cb66-40a5-bdb1-1b6521fc6a0e`
- **参数名**: `Crc8Mode`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_8_HARDWARE` (来源: AUTOSAR_ECUC)
  - `CRC_8_RUNTIME` (来源: AUTOSAR_ECUC)
  - `CRC_8_TABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch to select one of the available CRC 8-bit (SAE J1850) calculation methods

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

1. **Crc**
