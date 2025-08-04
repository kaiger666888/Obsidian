# vMem - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vMem](#vmem)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vMem

#### 基本信息

- **UUID**: `48cffb55-4e61-4712-b163-21cde00d2068`
- **模块名称**: `vMem`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the vMem driver (internal or external memory driver) module.
Its multiplicity describes the present number of memory drivers, so there will be one container for each memory driver.

#### 版本历史

共有 **14** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-04-24T08:04:38+01:00
- **发布者**: virchl, viroto

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-05-24T12:29:43+02:00
- **发布者**: viroto

**变更内容**:

##### 3. 版本 

- **状态**: released
- **发布日期**: 2018-06-28T10:47:17+02:00
- **发布者**: vircre

**变更内容**:

##### 4. 版本 1.02.00

- **状态**: released
- **发布日期**: 2018-07-12T09:11:45+02:00
- **发布者**: vircre

**变更内容**:

##### 5. 版本 1.03.00

- **状态**: released
- **发布日期**: 2018-08-09T02:18:26+02:00
- **发布者**: vircre

**变更内容**:

##### 6. 版本 1.04.00

- **状态**: released
- **发布日期**: 2018-10-01T16:11:37+02:00
- **发布者**: virbmz

**变更内容**:

##### 7. 版本 

- **状态**: released
- **发布日期**: 2019-02-18T10:47:54+01:00
- **发布者**: vircre

**变更内容**:

##### 8. 版本 1.05.00

- **状态**: released
- **发布日期**: 2019-03-19T14:21:24+01:00
- **发布者**: virstl

**变更内容**:

##### 9. 版本 1.06.00

- **状态**: released
- **发布日期**: 2019-06-18T09:29:00+02:00
- **发布者**: vircre

**变更内容**:

##### 10. 版本 1.07.00

- **状态**: released
- **发布日期**: 2019-12-06T07:23:00+01:00
- **发布者**: virstl

**变更内容**:

##### 11. 版本 2.00.00

- **状态**: released
- **发布日期**: 2020-01-02T15:16:12+01:00
- **发布者**: virstl

**变更内容**:

##### 12. 版本 2.00.01

- **状态**: released
- **发布日期**: 2020-04-15T10:32:40+02:00
- **发布者**: virpam

**变更内容**:

##### 13. 版本 2.00.02

- **状态**: released
- **发布日期**: 2020-06-08T11:00:13+02:00
- **发布者**: virpam

**变更内容**:

##### 14. 版本 2.00.03

- **状态**: released
- **发布日期**: 2021-02-26T10:12:39+01:00
- **发布者**: virepm

**变更内容**:

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. vMemGeneral

**容器属性**:

- **UUID**: `d5216919-534b-48b9-96df-1eb8377e7128`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Container for general configuration parameters of the memory driver. These parameters are always pre-compile.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. vMemDevErrorDetect

- **UUID**: `de80623e-90f1-497f-86d1-24faf0f98dbc`
- **参数名**: `vMemDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Reporting ON or OFF.
true:	Development error detection and reporting is enabled.
false:	Development error detection and reporting is disabled.

Note: 
In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. vMemSafeBswChecks

- **UUID**: `8be8a17d-dfcc-4d5e-88c7-d839d65748ab`
- **参数名**: `vMemSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used.

These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 3. vMemVersionInfoApi

- **UUID**: `725b09c5-85c0-4abf-8914-d852c1e60b57`
- **参数名**: `vMemVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function GetVersionInfo() to get major, minor and patch version information.

######## 4. vMemUsePeripheralAccessApi

- **UUID**: `4420c3e6-c95d-4475-947a-110d2d4169e0`
- **参数名**: `vMemUsePeripheralAccessApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies whether the module should use OsPeripheralAccess-API (e.g. because memory access is restricted by MMU) to access memory mapped registers.

true: Module uses APIs provided by OS to access memory mapped registers.
false: Module uses direct memory access to access memory mapped registers.

####### FLOAT 类型参数

######## 1. vMemMainFunctionPeriod

- **UUID**: `aab37ce9-bf0c-4374-8563-6d392649cb07`
- **参数名**: `vMemMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0.0001..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the fixed call cycle for vMem_MainFunction().
This information affects RTE's (SchM's) settings.

##### 2. vMemInstance

**容器属性**:

- **UUID**: `10f4d36b-bcd4-4e6b-bfd9-59dad460c16b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemInstance`
- **多重性**: [1..65536]
- **构建后可变**: false

**容器描述**:

This container includes the memory driver instance specific configuration parameters. 
Its multiplicity describes the number of memory driver instances of this memory driver, so there will be one container for each memory driver instance.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vMemInstanceId

- **UUID**: `561315df-d9d0-409c-9ac6-fcbdeff579b7`
- **参数名**: `vMemInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference a memory driver instance. It is used in order to distinguish between several memory driver instances with the same physical addresses.
This value will be assigned to the symbolic name derived of the vMemInstance container short name.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vMemSectorList

**容器属性**:

- **UUID**: `a9ec9b32-acd2-48c6-8937-fd5c1b5549ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSectorList`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

List of programmable sectors and pages.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vMemSector

**容器属性**:

- **UUID**: `80b5ec36-8d07-4675-830c-2d2092bc9d28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

########## 参数配置

此容器包含 **6** 个参数：

########### INTEGER 类型参数

############ 1. vMemNumberOfSectors

- **UUID**: `39332aaf-4e21-4a99-8ab5-9fef18aeb1a2`
- **参数名**: `vMemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65536]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for vMemSectorSize and vMemPageSize.

If this parameter is configured to be greater than 1, this will result in a so called "sector batch".

############ 2. vMemPageSize

- **UUID**: `7372f58c-f222-4fc8-84e1-633613f970fe`
- **参数名**: `vMemPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector in bytes.

A page is the smallest writeable unit.

############ 3. vMemSectorSize

- **UUID**: `b9121981-5ac7-4354-91ee-541dfb435ae1`
- **参数名**: `vMemSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector in bytes.

A sector is the smallest erasable unit.

############ 4. vMemStartAddress

- **UUID**: `a539c4c9-38f3-4aa9-a1a4-f3c9c09431df`
- **参数名**: `vMemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Physical start address of this sector. 

In case of a sector batch this physical start address is the address of the first sector. The physical start address of the other sectors can be calculated by usage of parameter vMemSectorSize.

############ 5. vMemProgramFlashId

- **UUID**: `6c8d9ebb-e40d-4e48-9b03-c15e0120890d`
- **参数名**: `vMemProgramFlashId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference Program Flash Bank. It is primarily used for the replace logical sector feature.
Refer to the technical reference of this driver and the hardware manual for more information.

############ 6. vMemPhysicalSectorId

- **UUID**: `19cb39be-07c6-4487-84f5-a1907d1ba584`
- **参数名**: `vMemPhysicalSectorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference a Physical Sector within a Program Flash Bank. A Program Flash Bank generally consists of 1 to 3 Physical Sectors of size 1 Mbyte. It is primarily used for the replace logical sector feature. 
Refer to the technical reference of this driver and the hardware manual for more information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vMemAlternateMapSectorRef

- **UUID**: `a5fac944-e288-413d-b469-90fb2efb7641`
- **引用名**: `vMemAlternateMapSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to corresponding sector batch in alternate address map for SOTA.

If SOTA is enabled the Tc3xx platform uses a standard and an alternate address map, in order to swap two PFLASH address regions.
Therefore, the sector batch which has the same start address in the alternate address map must be referenced here in the SOTA use case. The referenced sector batch must be identical in regards to number of sectors, page size and sector size.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############## 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############## 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

######### 2. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

####### 2. vMemSector

**容器属性**:

- **UUID**: `80b5ec36-8d07-4675-830c-2d2092bc9d28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vMemNumberOfSectors

- **UUID**: `39332aaf-4e21-4a99-8ab5-9fef18aeb1a2`
- **参数名**: `vMemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65536]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for vMemSectorSize and vMemPageSize.

If this parameter is configured to be greater than 1, this will result in a so called "sector batch".

########## 2. vMemPageSize

- **UUID**: `7372f58c-f222-4fc8-84e1-633613f970fe`
- **参数名**: `vMemPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector in bytes.

A page is the smallest writeable unit.

########## 3. vMemSectorSize

- **UUID**: `b9121981-5ac7-4354-91ee-541dfb435ae1`
- **参数名**: `vMemSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector in bytes.

A sector is the smallest erasable unit.

########## 4. vMemStartAddress

- **UUID**: `a539c4c9-38f3-4aa9-a1a4-f3c9c09431df`
- **参数名**: `vMemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Physical start address of this sector. 

In case of a sector batch this physical start address is the address of the first sector. The physical start address of the other sectors can be calculated by usage of parameter vMemSectorSize.

########## 5. vMemProgramFlashId

- **UUID**: `6c8d9ebb-e40d-4e48-9b03-c15e0120890d`
- **参数名**: `vMemProgramFlashId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference Program Flash Bank. It is primarily used for the replace logical sector feature.
Refer to the technical reference of this driver and the hardware manual for more information.

########## 6. vMemPhysicalSectorId

- **UUID**: `19cb39be-07c6-4487-84f5-a1907d1ba584`
- **参数名**: `vMemPhysicalSectorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference a Physical Sector within a Program Flash Bank. A Program Flash Bank generally consists of 1 to 3 Physical Sectors of size 1 Mbyte. It is primarily used for the replace logical sector feature. 
Refer to the technical reference of this driver and the hardware manual for more information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vMemAlternateMapSectorRef

- **UUID**: `a5fac944-e288-413d-b469-90fb2efb7641`
- **引用名**: `vMemAlternateMapSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to corresponding sector batch in alternate address map for SOTA.

If SOTA is enabled the Tc3xx platform uses a standard and an alternate address map, in order to swap two PFLASH address regions.
Therefore, the sector batch which has the same start address in the alternate address map must be referenced here in the SOTA use case. The referenced sector batch must be identical in regards to number of sectors, page size and sector size.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

####### 3. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

##### 3. vMemSectorList

**容器属性**:

- **UUID**: `a9ec9b32-acd2-48c6-8937-fd5c1b5549ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSectorList`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

List of programmable sectors and pages.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vMemSector

**容器属性**:

- **UUID**: `80b5ec36-8d07-4675-830c-2d2092bc9d28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. vMemNumberOfSectors

- **UUID**: `39332aaf-4e21-4a99-8ab5-9fef18aeb1a2`
- **参数名**: `vMemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65536]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for vMemSectorSize and vMemPageSize.

If this parameter is configured to be greater than 1, this will result in a so called "sector batch".

########## 2. vMemPageSize

- **UUID**: `7372f58c-f222-4fc8-84e1-633613f970fe`
- **参数名**: `vMemPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector in bytes.

A page is the smallest writeable unit.

########## 3. vMemSectorSize

- **UUID**: `b9121981-5ac7-4354-91ee-541dfb435ae1`
- **参数名**: `vMemSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector in bytes.

A sector is the smallest erasable unit.

########## 4. vMemStartAddress

- **UUID**: `a539c4c9-38f3-4aa9-a1a4-f3c9c09431df`
- **参数名**: `vMemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Physical start address of this sector. 

In case of a sector batch this physical start address is the address of the first sector. The physical start address of the other sectors can be calculated by usage of parameter vMemSectorSize.

########## 5. vMemProgramFlashId

- **UUID**: `6c8d9ebb-e40d-4e48-9b03-c15e0120890d`
- **参数名**: `vMemProgramFlashId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference Program Flash Bank. It is primarily used for the replace logical sector feature.
Refer to the technical reference of this driver and the hardware manual for more information.

########## 6. vMemPhysicalSectorId

- **UUID**: `19cb39be-07c6-4487-84f5-a1907d1ba584`
- **参数名**: `vMemPhysicalSectorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference a Physical Sector within a Program Flash Bank. A Program Flash Bank generally consists of 1 to 3 Physical Sectors of size 1 Mbyte. It is primarily used for the replace logical sector feature. 
Refer to the technical reference of this driver and the hardware manual for more information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vMemAlternateMapSectorRef

- **UUID**: `a5fac944-e288-413d-b469-90fb2efb7641`
- **引用名**: `vMemAlternateMapSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to corresponding sector batch in alternate address map for SOTA.

If SOTA is enabled the Tc3xx platform uses a standard and an alternate address map, in order to swap two PFLASH address regions.
Therefore, the sector batch which has the same start address in the alternate address map must be referenced here in the SOTA use case. The referenced sector batch must be identical in regards to number of sectors, page size and sector size.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

####### 2. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

##### 4. vMemSector

**容器属性**:

- **UUID**: `80b5ec36-8d07-4675-830c-2d2092bc9d28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. vMemNumberOfSectors

- **UUID**: `39332aaf-4e21-4a99-8ab5-9fef18aeb1a2`
- **参数名**: `vMemNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..65536]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of continuous sectors with identical values for vMemSectorSize and vMemPageSize.

If this parameter is configured to be greater than 1, this will result in a so called "sector batch".

######## 2. vMemPageSize

- **UUID**: `7372f58c-f222-4fc8-84e1-633613f970fe`
- **参数名**: `vMemPageSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of one page of this sector in bytes.

A page is the smallest writeable unit.

######## 3. vMemSectorSize

- **UUID**: `b9121981-5ac7-4354-91ee-541dfb435ae1`
- **参数名**: `vMemSectorSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of this sector in bytes.

A sector is the smallest erasable unit.

######## 4. vMemStartAddress

- **UUID**: `a539c4c9-38f3-4aa9-a1a4-f3c9c09431df`
- **参数名**: `vMemStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Physical start address of this sector. 

In case of a sector batch this physical start address is the address of the first sector. The physical start address of the other sectors can be calculated by usage of parameter vMemSectorSize.

######## 5. vMemProgramFlashId

- **UUID**: `6c8d9ebb-e40d-4e48-9b03-c15e0120890d`
- **参数名**: `vMemProgramFlashId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..5]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference Program Flash Bank. It is primarily used for the replace logical sector feature.
Refer to the technical reference of this driver and the hardware manual for more information.

######## 6. vMemPhysicalSectorId

- **UUID**: `19cb39be-07c6-4487-84f5-a1907d1ba584`
- **参数名**: `vMemPhysicalSectorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique numeric identifier which is used to reference a Physical Sector within a Program Flash Bank. A Program Flash Bank generally consists of 1 to 3 Physical Sectors of size 1 Mbyte. It is primarily used for the replace logical sector feature. 
Refer to the technical reference of this driver and the hardware manual for more information.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vMemAlternateMapSectorRef

- **UUID**: `a5fac944-e288-413d-b469-90fb2efb7641`
- **引用名**: `vMemAlternateMapSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to corresponding sector batch in alternate address map for SOTA.

If SOTA is enabled the Tc3xx platform uses a standard and an alternate address map, in order to swap two PFLASH address regions.
Therefore, the sector batch which has the same start address in the alternate address map must be referenced here in the SOTA use case. The referenced sector batch must be identical in regards to number of sectors, page size and sector size.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

##### 5. vMemBurstSettings

**容器属性**:

- **UUID**: `beabfe68-7960-442f-904e-59f6225479a3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemBurstSettings`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for burst setting configuration parameters of the memory driver.

A sector burst can be used for improved performance.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vMemEraseBurstSize

- **UUID**: `e1286682-87c8-4102-a37e-1a2a4ea85f0c`
- **参数名**: `vMemEraseBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `65536`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of sector erase burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

######## 2. vMemWriteBurstSize

- **UUID**: `28bce305-198d-43ca-8b5f-7607515c6c85`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

######## 3. vMemPageBurstRamAlignment

- **UUID**: `07739ca9-fdb1-47eb-b727-4f4b742db31b`
- **参数名**: `vMemPageBurstRamAlignment`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..256]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: In order to make use of page write bursts, a device might require a specific alignment of the data buffer (containing the data to be programmed to NV memory).

E.g. a device specific assembly buffer must be filled dword (32bit) wise. To avoid additionaly over head the buffer passed to write routine shall be correctly aligned according to this setting in order to use bursts.

Unless no alignment is necessary (value equals 1), the implementation shall check for expected alignment, and it shall reject a burst request if this check failed.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. vMem_30_Tc3xxInf01

- **UUID**: `402409a7-b72d-4f0c-839d-f14c929abc33`
- **包名称**: `vMem_30_Tc3xxInf01`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **vMem**

##### BSW-IMPLEMENTATION 类型元素

1. **vMem_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vMem_Rec**
2. **vMem_Pre**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vMem_Impl

- **UUID**: `3aa26c5b-f2ed-4368-8441-bb87dcc04333`
- **实现名称**: `vMem_Impl`
- **编程语言**: C
- **软件版本**: 2.01.00
- **供应商ID**: 30
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vMem_Rec

- **UUID**: `bc746c5b-257b-4425-b169-4799ec4bb9e0`
- **配置名称**: `vMem_Rec`
- **定义引用**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem`

### 2. vMem_Pre

- **UUID**: `853b0014-4473-4024-b3bf-b519d3d084b2`
- **配置名称**: `vMem_Pre`
- **定义引用**: `/MICROSAR/vMem_30_Tc3xxInf01/vMem`
