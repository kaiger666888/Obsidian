# Ea - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:41

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Ea](#ea)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Ea

#### 基本信息

- **UUID**: `ECUC:c6de96ce-a538-4309-b185-f7568c3162b6`
- **模块名称**: `Ea`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Ea (EEPROM Abstraction) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. EaBlockConfiguration

**容器属性**:

- **UUID**: `ECUC:9b7435b0-8e2b-4fa1-a37d-ddc652cf908c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EaBlockConfiguration`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of block specific parameters for the EEPROM abstraction module.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. EaBlockNumber

- **UUID**: `ECUC:997bcb48-170b-4a2d-ab97-3ba85568fcdf`
- **参数名**: `EaBlockNumber`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65534]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Block identifier (handle).

######## 2. EaBlockSize

- **UUID**: `ECUC:d93be6ac-f99a-4500-bf92-c61f222dad5d`
- **参数名**: `EaBlockSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of a logical block in bytes.

######## 3. EaNumberOfWriteCycles

- **UUID**: `ECUC:cd71c820-c85a-4055-97e2-3cce71bc93d3`
- **参数名**: `EaNumberOfWriteCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of write cycles required for this block.

####### BOOLEAN 类型参数

######## 1. EaImmediateData

- **UUID**: `ECUC:ceda93f2-07fd-44c2-8d31-b8aabbced641`
- **参数名**: `EaImmediateData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Marker for high priority data.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EaDeviceIndex

- **UUID**: `ECUC:735d011c-31e9-4235-ab22-d5c1a2647936`
- **引用名**: `EaDeviceIndex`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EepGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Eep/EepGeneral`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Device index (handle).

##### 2. EaGeneral

**容器属性**:

- **UUID**: `ECUC:03c545b5-0414-475e-b6c3-383d510bb159`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EaGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration of the EEPROM abstraction module. This container lists block independent configuration parameters.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. EaIndex

- **UUID**: `ECUC:724e4b9c-8ef7-4ebe-b3fe-ec26fa8dfdee`
- **参数名**: `EaIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. EaVirtualPageSize

- **UUID**: `ECUC:7e38c9b0-11ed-4af3-b258-c643137642d0`
- **参数名**: `EaVirtualPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The size in bytes to which logical blocks shall be aligned.

####### BOOLEAN 类型参数

######## 1. EaDevErrorDetect

- **UUID**: `ECUC:699071d4-4525-41af-8cd1-1bfe69f6798c`
- **参数名**: `EaDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable development error detection.

######## 2. EaPollingMode

- **UUID**: `ECUC:43431c0d-0ddd-4243-8eaa-e4ebe5013d20`
- **参数名**: `EaPollingMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable the polling mode for this module.

######## 3. EaSetModeSupported

- **UUID**: `ECUC:aed5447c-ebbe-4b22-878a-ee0ab4fe3622`
- **参数名**: `EaSetModeSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Compile switch to enable / disable the function Ea_SetMode.

######## 4. EaVersionInfoApi

- **UUID**: `ECUC:d2c0e417-0cc7-4b7e-9cfe-9052f4736927`
- **参数名**: `EaVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable / disable the API to read out the modules version information.

####### FUNCTION-NAME 类型参数

######## 1. EaNvmJobEndNotification

- **UUID**: `ECUC:791c602d-f757-476f-8535-129663700557`
- **参数名**: `EaNvmJobEndNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job end notification routine provided by the upper layer module (NvM_JobEndNotification).

######## 2. EaNvmJobErrorNotification

- **UUID**: `ECUC:82486646-4e38-4149-89db-6605202cce18`
- **参数名**: `EaNvmJobErrorNotification`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mapped to the job error notification routine provided by the upper layer module (NvM_JobErrorNotification).

##### 3. EaPublishedInformation

**容器属性**:

- **UUID**: `ECUC:dcc718b0-9772-4964-99d6-ab1aa86e8033`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EaPublishedInformation`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. EaBlockOverhead

- **UUID**: `ECUC:8f3bc078-5df6-437e-8a6e-1500dc5c5966`
- **参数名**: `EaBlockOverhead`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Management overhead per logical block in bytes.

######## 2. EaPageOverhead

- **UUID**: `ECUC:f5c6f8c3-943e-441b-a0b6-5f1f06db40f2`
- **参数名**: `EaPageOverhead`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Management overhead per page in bytes.

####### FLOAT 类型参数

######## 1. EaMaximumBlockingTime

- **UUID**: `ECUC:a0a01a68-e7b0-4ef3-bfa5-982737074034`
- **参数名**: `EaMaximumBlockingTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: The maximum time the EA module's API routines shall be blocked (delayed) by internal operations. (EA070)

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

1. **Ea**
