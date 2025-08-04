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

- **UUID**: `57587968-e525-4cdd-b33f-d4f4fadef419`
- **模块名称**: `vMem`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the vMem driver (internal or external memory driver) module.
Its multiplicity describes the present number of memory drivers, so there will be one container for each memory driver.

#### 版本历史

共有 **4** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-01-24T12:21:38+01:00
- **发布者**: virchl

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-04-09T09:24:33+02:00
- **发布者**: vircre

**变更内容**:

##### 3. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-06-07T13:53:38+02:00
- **发布者**: viroto

**变更内容**:

##### 4. 版本 1.01.01

- **状态**: released
- **发布日期**: 2018-06-19T10:16:28+02:00
- **发布者**: viroto

**变更内容**:

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. vMemInstance

**容器属性**:

- **UUID**: `0892d3a4-297c-4cc0-8dcc-ab479bc53466`
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

- **UUID**: `981e4fd8-7a6b-4033-a3e8-cea7c11a016f`
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

- **UUID**: `7ae161cf-213a-47c3-9f4a-cd0158f1741d`
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

- **UUID**: `8b041bb4-9f6f-481e-bfcf-b5780816d095`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. vMemNumberOfSectors

- **UUID**: `b4b41691-c810-413a-851b-f9ab4d8eea15`
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

- **UUID**: `868a56d6-c9c3-489d-96a9-c1f7add2d507`
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

- **UUID**: `53525ed1-1715-4f93-a554-6faca2c59dc5`
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

- **UUID**: `281f7e10-e15e-4d4b-bc50-02d518fab8e3`
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

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############## 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

- **UUID**: `8b041bb4-9f6f-481e-bfcf-b5780816d095`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vMemNumberOfSectors

- **UUID**: `b4b41691-c810-413a-851b-f9ab4d8eea15`
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

- **UUID**: `868a56d6-c9c3-489d-96a9-c1f7add2d507`
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

- **UUID**: `53525ed1-1715-4f93-a554-6faca2c59dc5`
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

- **UUID**: `281f7e10-e15e-4d4b-bc50-02d518fab8e3`
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

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

##### 2. vMemSectorList

**容器属性**:

- **UUID**: `7ae161cf-213a-47c3-9f4a-cd0158f1741d`
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

- **UUID**: `8b041bb4-9f6f-481e-bfcf-b5780816d095`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vMemNumberOfSectors

- **UUID**: `b4b41691-c810-413a-851b-f9ab4d8eea15`
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

- **UUID**: `868a56d6-c9c3-489d-96a9-c1f7add2d507`
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

- **UUID**: `53525ed1-1715-4f93-a554-6faca2c59dc5`
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

- **UUID**: `281f7e10-e15e-4d4b-bc50-02d518fab8e3`
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

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

############ 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

##### 3. vMemSector

**容器属性**:

- **UUID**: `8b041bb4-9f6f-481e-bfcf-b5780816d095`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemSector`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration description of a programmable sector or sector batch. Sector batch means that homogenous and coherent sectors can be configured as one vMemSector element.
It is recommended to group as many identical sectors as possible together.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vMemNumberOfSectors

- **UUID**: `b4b41691-c810-413a-851b-f9ab4d8eea15`
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

- **UUID**: `868a56d6-c9c3-489d-96a9-c1f7add2d507`
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

- **UUID**: `53525ed1-1715-4f93-a554-6faca2c59dc5`
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

- **UUID**: `281f7e10-e15e-4d4b-bc50-02d518fab8e3`
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

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vMemBurstSettings

**容器属性**:

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

########## 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

##### 4. vMemBurstSettings

**容器属性**:

- **UUID**: `24b35a42-9d21-4887-bbb4-66f0f42e3610`
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

- **UUID**: `1e005ae3-c498-40c8-a07f-8ca94aba70ba`
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

- **UUID**: `992bf0e7-fc3f-4c3f-b2c3-f54716a785c1`
- **参数名**: `vMemWriteBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `128`
- **取值范围**: [0..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size of page write/program burst in bytes. A sector burst can be used for improved performance and is typically (a subset of) a sector batch.

Additionally the size also prescribes a necessary alignment: The phyiscal start address must be aligned to the size value, i.e. it must an integral multiple of the burst size.

######## 3. vMemPageBurstRamAlignment

- **UUID**: `aa93337a-c8a9-4f0d-87e7-e68d21a932f5`
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

### 2. vMem

- **UUID**: `e352fcf3-a8d2-4192-aea4-04c922edaa5b`
- **包名称**: `vMem`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vMem_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vMem**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vMem_Pre**
2. **vMem_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vMem_Impl

- **UUID**: `d338bee6-814b-4c55-8893-048e9623985f`
- **实现名称**: `vMem_Impl`
- **编程语言**: C
- **软件版本**: 2.00.02
- **供应商ID**: 30
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vMem_Pre

- **UUID**: `bb389734-e005-422d-a8e6-1868afee6c09`
- **配置名称**: `vMem_Pre`
- **定义引用**: `/MICROSAR/vMem/vMem`

### 2. vMem_Rec

- **UUID**: `e2552aac-70fd-4d1c-a92b-f162b8aaa082`
- **配置名称**: `vMem_Rec`
- **定义引用**: `/MICROSAR/vMem/vMem`
