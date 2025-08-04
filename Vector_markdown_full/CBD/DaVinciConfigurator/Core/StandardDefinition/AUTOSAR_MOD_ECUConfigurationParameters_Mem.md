# Mem - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:27

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Mem](#mem)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00052.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Mem

#### 基本信息

- **UUID**: `ECUC:138bb6dc-63bb-4d04-b032-a59e5d97d479`
- **模块名称**: `Mem`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Mem driver (internal or external memory driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.9.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. MemGeneral

**容器属性**:

- **UUID**: `ECUC:3c9d1fc3-94c0-4881-9279-7bf9a9d9464e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemGeneral`
- **多重性**: [1..1]

**容器描述**:

Container for general configuration parameters of the Mem driver. These parameters are always pre-compile.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. MemIndex

- **UUID**: `ECUC:2b45184d-846c-424c-b62d-1e6ecb62b8f4`
- **参数名**: `MemIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. MemDevErrorDetect

- **UUID**: `ECUC:09eec05e-986a-45d9-95ff-d02f8d4b2a48`
- **参数名**: `MemDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the development error detection and notification on or off.

##### 2. MemInstance

**容器属性**:

- **UUID**: `ECUC:b01dec4a-dcdf-4f4d-b0b1-58b53f6ed9c5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemInstance`
- **多重性**: [1..65535]

**容器描述**:

This container includes the Mem driver instance specific configuration parameters.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. MemInstanceId

- **UUID**: `ECUC:c3f57eb2-b673-4a08-94ce-59b4dd5816a1`
- **参数名**: `MemInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the unique numeric identifier which is used to reference a Mem driver instance in case multiple devices of the same type shall be addressed by one Mem driver. This value will be assigned to the symbolic name derived of the MemInstance container short name.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. MemSectorBatch

**容器属性**:

- **UUID**: `ECUC:47068044-43bf-4333-82ed-8ba53a0e1c96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemSectorBatch`
- **多重性**: [1..infinite]

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one MemSector element.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. MemEraseSectorSize

- **UUID**: `ECUC:e6356d39-6215-4cfe-b41c-3cb075a212fa`
- **参数名**: `MemEraseSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector in bytes.

########## 2. MemMinReadSize

- **UUID**: `ECUC:9c04c206-1275-44e4-b73d-61c0754ac5f6`
- **参数名**: `MemMinReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Smallest readable unit in bytes.

########## 3. MemNumberOfSectors

- **UUID**: `ECUC:edbc77e8-2275-4d55-8543-77a32cd1bcf2`
- **参数名**: `MemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of contiguous sectors with identical values for MemSectorSize and MemPageSize.

########## 4. MemSpecifiedEraseCycles

- **UUID**: `ECUC:16c7af74-a34f-433e-9a26-5cdcf69aee92`
- **参数名**: `MemSpecifiedEraseCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of erase cycles specified for the memory device (usually given in the device data sheet).

########## 5. MemStartAddress

- **UUID**: `ECUC:464b7080-f9f1-4357-b2cc-bf7fb4646de8`
- **参数名**: `MemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Physical start address of the sector (batch).

########## 6. MemWritePageSize

- **UUID**: `ECUC:347de1d0-bc27-4e30-8ab3-c2933fbc1f43`
- **参数名**: `MemWritePageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of a write page of this sector in bytes.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. MemBurstSettings

**容器属性**:

- **UUID**: `ECUC:8d70158a-2ac9-4eeb-9894-07c1472eb8d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemBurstSettings`
- **多重性**: [0..1]

**容器描述**:

Container for burst setting configuration parameters of the Mem driver.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. MemEraseBurstSize

- **UUID**: `ECUC:01e81f42-e4b5-4e2e-b08f-59cc31a55a17`
- **参数名**: `MemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

############ 2. MemMaxReadSize

- **UUID**: `ECUC:07430cb1-fb83-4aa6-a7b3-d58b1c215ef5`
- **参数名**: `MemMaxReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the maximum number of bytes the MemAcc module requests within one Mem read request.

############ 3. MemWriteBurstSize

- **UUID**: `ECUC:d3ee57d0-2006-4018-aed1-541c1c47b3bf`
- **参数名**: `MemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

####### 2. MemBurstSettings

**容器属性**:

- **UUID**: `ECUC:8d70158a-2ac9-4eeb-9894-07c1472eb8d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemBurstSettings`
- **多重性**: [0..1]

**容器描述**:

Container for burst setting configuration parameters of the Mem driver.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MemEraseBurstSize

- **UUID**: `ECUC:01e81f42-e4b5-4e2e-b08f-59cc31a55a17`
- **参数名**: `MemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

########## 2. MemMaxReadSize

- **UUID**: `ECUC:07430cb1-fb83-4aa6-a7b3-d58b1c215ef5`
- **参数名**: `MemMaxReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the maximum number of bytes the MemAcc module requests within one Mem read request.

########## 3. MemWriteBurstSize

- **UUID**: `ECUC:d3ee57d0-2006-4018-aed1-541c1c47b3bf`
- **参数名**: `MemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

##### 3. MemSectorBatch

**容器属性**:

- **UUID**: `ECUC:47068044-43bf-4333-82ed-8ba53a0e1c96`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemSectorBatch`
- **多重性**: [1..infinite]

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one MemSector element.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. MemEraseSectorSize

- **UUID**: `ECUC:e6356d39-6215-4cfe-b41c-3cb075a212fa`
- **参数名**: `MemEraseSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of this sector in bytes.

######## 2. MemMinReadSize

- **UUID**: `ECUC:9c04c206-1275-44e4-b73d-61c0754ac5f6`
- **参数名**: `MemMinReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Smallest readable unit in bytes.

######## 3. MemNumberOfSectors

- **UUID**: `ECUC:edbc77e8-2275-4d55-8543-77a32cd1bcf2`
- **参数名**: `MemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of contiguous sectors with identical values for MemSectorSize and MemPageSize.

######## 4. MemSpecifiedEraseCycles

- **UUID**: `ECUC:16c7af74-a34f-433e-9a26-5cdcf69aee92`
- **参数名**: `MemSpecifiedEraseCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Number of erase cycles specified for the memory device (usually given in the device data sheet).

######## 5. MemStartAddress

- **UUID**: `ECUC:464b7080-f9f1-4357-b2cc-bf7fb4646de8`
- **参数名**: `MemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Physical start address of the sector (batch).

######## 6. MemWritePageSize

- **UUID**: `ECUC:347de1d0-bc27-4e30-8ab3-c2933fbc1f43`
- **参数名**: `MemWritePageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of a write page of this sector in bytes.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemBurstSettings

**容器属性**:

- **UUID**: `ECUC:8d70158a-2ac9-4eeb-9894-07c1472eb8d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemBurstSettings`
- **多重性**: [0..1]

**容器描述**:

Container for burst setting configuration parameters of the Mem driver.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. MemEraseBurstSize

- **UUID**: `ECUC:01e81f42-e4b5-4e2e-b08f-59cc31a55a17`
- **参数名**: `MemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

########## 2. MemMaxReadSize

- **UUID**: `ECUC:07430cb1-fb83-4aa6-a7b3-d58b1c215ef5`
- **参数名**: `MemMaxReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the maximum number of bytes the MemAcc module requests within one Mem read request.

########## 3. MemWriteBurstSize

- **UUID**: `ECUC:d3ee57d0-2006-4018-aed1-541c1c47b3bf`
- **参数名**: `MemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

##### 4. MemBurstSettings

**容器属性**:

- **UUID**: `ECUC:8d70158a-2ac9-4eeb-9894-07c1472eb8d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemBurstSettings`
- **多重性**: [0..1]

**容器描述**:

Container for burst setting configuration parameters of the Mem driver.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. MemEraseBurstSize

- **UUID**: `ECUC:01e81f42-e4b5-4e2e-b08f-59cc31a55a17`
- **参数名**: `MemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

######## 2. MemMaxReadSize

- **UUID**: `ECUC:07430cb1-fb83-4aa6-a7b3-d58b1c215ef5`
- **参数名**: `MemMaxReadSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the maximum number of bytes the MemAcc module requests within one Mem read request.

######## 3. MemWriteBurstSize

- **UUID**: `ECUC:d3ee57d0-2006-4018-aed1-541c1c47b3bf`
- **参数名**: `MemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

##### 5. MemPublishedInformation

**容器属性**:

- **UUID**: `ECUC:00e09212-d321-4b62-9a09-2fa0da152477`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemPublishedInformation`
- **多重性**: [1..1]

**容器描述**:

Additional published parameters not covered by CommonPublishedInformation container.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. MemErasedValue

- **UUID**: `ECUC:27a73679-2011-4f15-9293-1bb4d118601f`
- **参数名**: `MemErasedValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The contents of an erased memory cell.

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

1. **Mem**
