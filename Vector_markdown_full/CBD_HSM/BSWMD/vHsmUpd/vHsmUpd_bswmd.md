# vHsmUpd - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:58

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vHsmUpd](#vhsmupd)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vHsmUpd

#### 基本信息

- **UUID**: `64c07e5f-0796-483b-81ed-d675e866a74d`
- **模块名称**: `vHsmUpd`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [1..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the vHsmUpd (Hsm Updater) module.

#### 版本历史

共有 **11** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2019-01-23T10:53:30+01:00
- **发布者**: virstl

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2019-03-21T12:27:53+01:00
- **发布者**: virstl

**变更内容**:

##### 3. 版本 2.00.00

- **状态**: released
- **发布日期**: 2019-04-15T10:24:34+02:00
- **发布者**: virstl

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2019-05-20T08:33:48+02:00
- **发布者**: virstl

**变更内容**:

##### 5. 版本 2.02.00

- **状态**: released
- **发布日期**: 2019-07-19T14:34:33+02:00
- **发布者**: virstl

**变更内容**:

##### 6. 版本 3.00.00

- **状态**: released
- **发布日期**: 2019-08-09T09:58:26+02:00
- **发布者**: virewe

**变更内容**:

##### 7. 版本 3.00.01

- **状态**: released
- **发布日期**: 2020-04-15T11:26:42+02:00
- **发布者**: visfnn

**变更内容**:

##### 8. 版本 3.00.02

- **状态**: released
- **发布日期**: 2020-04-15T12:06:46+02:00
- **发布者**: visfnn

**变更内容**:

##### 9. 版本 3.00.03

- **状态**: released
- **发布日期**: 2020-04-15T12:06:52+02:00
- **发布者**: visfnn

**变更内容**:

##### 10. 版本 3.00.04

- **状态**: released
- **发布日期**: 2020-05-06T13:14:26+02:00
- **发布者**: visfnn

**变更内容**:

##### 11. 版本 3.00.05

- **状态**: released
- **发布日期**: 2021-01-14T13:23:17+01:00
- **发布者**: visfnn

**变更内容**:

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. vHsmUpdGeneral

**容器属性**:

- **UUID**: `e884f3f6-2ab8-408a-b850-0e03c040285c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the vHsmUpd.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vHsmUpdRetryCounter

- **UUID**: `c1b31197-6793-4497-8a73-4b18a21452fb`
- **参数名**: `vHsmUpdRetryCounter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value defines the maximal number of retries the vHsmUpd does, before an error callout gets called.

######## 2. vHsmUpdDecryptionRamBufferSize

- **UUID**: `62736194-1927-4e37-b4c2-f3fd27bb2964`
- **参数名**: `vHsmUpdDecryptionRamBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `256`
- **取值范围**: [16..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value defines the size for the decryption buffer which is used for decrypting the update image. A greater value could speed up the update process but leads to more memory consumption in RAM.

There are three restrictions regarding this value:
    1) The size must be a multiple of 16Bytes.
    2) The size must be a multiple of the code flash page size.
    3) The update image size shall be at least equal to the configured value.

####### BOOLEAN 类型参数

######## 1. vHsmUpdEnableUserCompareMechanism

- **UUID**: `1a01ced8-86d9-4fc1-b348-05da6f34424d`
- **参数名**: `vHsmUpdEnableUserCompareMechanism`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether a user defined compare mechanism of the vHsm firmware is implemented.

The vHsmUpd normally decides whether an update of the vHsm firmware is necessary by comparing the given values by size.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. vHsmUpdUpdateHeaderFixAddress

**容器属性**:

- **UUID**: `5ca21f2d-7a27-46e7-9875-b4bba7d5239a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeaderFixAddress`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Exactly two header locations must be specified when using this choice. Location_A will be parsed and only if no valid header is found here, the second Location_B will be processed.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vHsmUpdHeaderLocation_A

- **UUID**: `34d3799c-a3da-4169-9343-db172e9cde25`
- **参数名**: `vHsmUpdHeaderLocation_A`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

########## 2. vHsmUpdHeaderLocation_B

- **UUID**: `30fa44b8-c3cd-4ecd-8ac5-9ec7167b84bf`
- **参数名**: `vHsmUpdHeaderLocation_B`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

####### 2. vHsmUpdUpdateHeaderVariableAddress

**容器属性**:

- **UUID**: `d48c2e13-1ff8-4155-8218-78e94703bc8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeaderVariableAddress`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Define a start address and the number of locations to search for an update header when using this choice. vHsmUpd searches these locations until the first valid update header is found.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. vHsmUpdFirstHeaderAddress

- **UUID**: `55ab9222-c723-45ba-b839-e9acf818a4c2`
- **参数名**: `vHsmUpdFirstHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

########## 2. vHsmUpdNumberOfPossibleHeaders

- **UUID**: `036edd74-ab6d-4114-884a-cfba5d5017a9`
- **参数名**: `vHsmUpdNumberOfPossibleHeaders`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of locations to search for the update header. vHsmUpd expects all header locations to be aligned to page size of the hardware. The next address to search for the update header will be calculated as the size of the update header is known.

Therefore, the update header area shall not contain any gaps, but lie sequentially in flash memory.

####### 3. vHsmUpdIpc

**容器属性**:

- **UUID**: `f63ccd94-1692-4760-b60b-12c9d10258a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdIpc`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configuration parameters for the Ipc-Communication, i.e. the communcation with the host core.

The communication takes place in both directions, i.e. both the Host and the HSM write information for the other. Therefore, two required areas have to be configured --- vHsmUpdIpcHsmToHost and vHsmUpdIpcHostToHsm.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vHsmUpdIpcBaseAddress

- **UUID**: `aa57a29a-1c91-4dda-afc3-82efed275956`
- **参数名**: `vHsmUpdIpcBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the vHsmUpd to communicate with the Host application. The address must be writeable by the vHsmUpd (shall be located within RAM) and should be readable by the Host. Just one byte is used.

Hardware restrictions regarding the address must be respected by the user.

########## 2. vHsmUpdIpcHsmToHost

- **UUID**: `2b0512af-fabc-484d-be3c-657745e1a227`
- **参数名**: `vHsmUpdIpcHsmToHost`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the HSM to communicate with the Host application. The address must be writable by the HSM and readable by the Host application. The vHsmUpd has to be able to evaluate this address and clear it.

vHsmUpdIpcHsmToHost specifies a 4 byte writable address.

Hardware restrictions regarding the address must be respected by the user.

########## 3. vHsmUpdIpcHostToHsm

- **UUID**: `e01c4277-7726-4243-a119-0b81d7f97e1c`
- **参数名**: `vHsmUpdIpcHostToHsm`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the Host application to communicate with the HSM. The address must be writable by the Host application and readable by the HSM. The vHsmUpd has to be able to evaluate this address.

vHsmUpdIpcHostToHsm specifies a 4 byte writable address.

Hardware restrictions regarding the address must be respected by the user.

########## 4. vHsmUpdIpcWaitMask

- **UUID**: `61e79baf-472f-4e01-b36e-2ebf77b63328`
- **参数名**: `vHsmUpdIpcWaitMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This mask value shall be written to the area specified by vHsmUpdIpcHostToHsm. 

The vHsmUpd polls this value to get the current state of the Host. If the value is written, the vHsmUpd assumes the Host to be ready for an update.

####### 4. vHsmUpdUpdateHeader

**容器属性**:

- **UUID**: `8de11624-6482-4663-a874-2a6f3a32da3e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeader`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmUpdUpdateHeaderFixAddress**
  - UUID: `5ca21f2d-7a27-46e7-9875-b4bba7d5239a`
  - 描述: Exactly two header locations must be specified when using this choice. Location_A will be parsed and only if no valid header is found here, the second Location_B will be processed.
- **vHsmUpdUpdateHeaderVariableAddress**
  - UUID: `d48c2e13-1ff8-4155-8218-78e94703bc8c`
  - 描述: Define a start address and the number of locations to search for an update header when using this choice. vHsmUpd searches these locations until the first valid update header is found.

**容器描述**:

Configuration parameters for an update header. The header contains information about a possible update of the vHsm firmware. To decide whether an update shall be executed the vHsmUpd must search for a header.
All info to find and parse an update header correctly shall be defined within the container.

There are two possible mechanisms available:
- Configure two fixed addresses where the vHsmUpd searches for the update header
- Configure a start address and the maximal number of locations for the update header

##### 2. vHsmUpdUpdateHeaderFixAddress

**容器属性**:

- **UUID**: `5ca21f2d-7a27-46e7-9875-b4bba7d5239a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeaderFixAddress`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Exactly two header locations must be specified when using this choice. Location_A will be parsed and only if no valid header is found here, the second Location_B will be processed.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vHsmUpdHeaderLocation_A

- **UUID**: `34d3799c-a3da-4169-9343-db172e9cde25`
- **参数名**: `vHsmUpdHeaderLocation_A`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

######## 2. vHsmUpdHeaderLocation_B

- **UUID**: `30fa44b8-c3cd-4ecd-8ac5-9ec7167b84bf`
- **参数名**: `vHsmUpdHeaderLocation_B`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

##### 3. vHsmUpdUpdateHeaderVariableAddress

**容器属性**:

- **UUID**: `d48c2e13-1ff8-4155-8218-78e94703bc8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeaderVariableAddress`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Define a start address and the number of locations to search for an update header when using this choice. vHsmUpd searches these locations until the first valid update header is found.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. vHsmUpdFirstHeaderAddress

- **UUID**: `55ab9222-c723-45ba-b839-e9acf818a4c2`
- **参数名**: `vHsmUpdFirstHeaderAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical flash address where an update header is located. The address to configure here is the address of the presence pattern and not the first content of the update header.

######## 2. vHsmUpdNumberOfPossibleHeaders

- **UUID**: `036edd74-ab6d-4114-884a-cfba5d5017a9`
- **参数名**: `vHsmUpdNumberOfPossibleHeaders`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of locations to search for the update header. vHsmUpd expects all header locations to be aligned to page size of the hardware. The next address to search for the update header will be calculated as the size of the update header is known.

Therefore, the update header area shall not contain any gaps, but lie sequentially in flash memory.

##### 4. vHsmUpdIpc

**容器属性**:

- **UUID**: `f63ccd94-1692-4760-b60b-12c9d10258a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vHsmUpdIpc`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Configuration parameters for the Ipc-Communication, i.e. the communcation with the host core.

The communication takes place in both directions, i.e. both the Host and the HSM write information for the other. Therefore, two required areas have to be configured --- vHsmUpdIpcHsmToHost and vHsmUpdIpcHostToHsm.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vHsmUpdIpcBaseAddress

- **UUID**: `aa57a29a-1c91-4dda-afc3-82efed275956`
- **参数名**: `vHsmUpdIpcBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the vHsmUpd to communicate with the Host application. The address must be writeable by the vHsmUpd (shall be located within RAM) and should be readable by the Host. Just one byte is used.

Hardware restrictions regarding the address must be respected by the user.

######## 2. vHsmUpdIpcHsmToHost

- **UUID**: `2b0512af-fabc-484d-be3c-657745e1a227`
- **参数名**: `vHsmUpdIpcHsmToHost`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the HSM to communicate with the Host application. The address must be writable by the HSM and readable by the Host application. The vHsmUpd has to be able to evaluate this address and clear it.

vHsmUpdIpcHsmToHost specifies a 4 byte writable address.

Hardware restrictions regarding the address must be respected by the user.

######## 3. vHsmUpdIpcHostToHsm

- **UUID**: `e01c4277-7726-4243-a119-0b81d7f97e1c`
- **参数名**: `vHsmUpdIpcHostToHsm`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the address, which is used by the Host application to communicate with the HSM. The address must be writable by the Host application and readable by the HSM. The vHsmUpd has to be able to evaluate this address.

vHsmUpdIpcHostToHsm specifies a 4 byte writable address.

Hardware restrictions regarding the address must be respected by the user.

######## 4. vHsmUpdIpcWaitMask

- **UUID**: `61e79baf-472f-4e01-b36e-2ebf77b63328`
- **参数名**: `vHsmUpdIpcWaitMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This mask value shall be written to the area specified by vHsmUpdIpcHostToHsm. 

The vHsmUpd polls this value to get the current state of the Host. If the value is written, the vHsmUpd assumes the Host to be ready for an update.

##### 5. vHsmUpdUpdateHeader

**容器属性**:

- **UUID**: `8de11624-6482-4663-a874-2a6f3a32da3e`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `vHsmUpdUpdateHeader`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **vHsmUpdUpdateHeaderFixAddress**
  - UUID: `5ca21f2d-7a27-46e7-9875-b4bba7d5239a`
  - 描述: Exactly two header locations must be specified when using this choice. Location_A will be parsed and only if no valid header is found here, the second Location_B will be processed.
- **vHsmUpdUpdateHeaderVariableAddress**
  - UUID: `d48c2e13-1ff8-4155-8218-78e94703bc8c`
  - 描述: Define a start address and the number of locations to search for an update header when using this choice. vHsmUpd searches these locations until the first valid update header is found.

**容器描述**:

Configuration parameters for an update header. The header contains information about a possible update of the vHsm firmware. To decide whether an update shall be executed the vHsmUpd must search for a header.
All info to find and parse an update header correctly shall be defined within the container.

There are two possible mechanisms available:
- Configure two fixed addresses where the vHsmUpd searches for the update header
- Configure a start address and the maximal number of locations for the update header

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vHsmUpd_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vHsmUpd**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vHsmUpd_Pre**
2. **vHsmUpd_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vHsmUpd_Impl

- **UUID**: `c4f498da-247d-4d2d-b080-0613470cbf1c`
- **实现名称**: `vHsmUpd_Impl`
- **编程语言**: C
- **软件版本**: 3.00.05
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vHsmUpd_Pre

- **UUID**: `075f5446-2ec5-4885-a361-5ec7ffdf34b8`
- **配置名称**: `vHsmUpd_Pre`
- **定义引用**: `/MICROSAR/vHsmUpd`

### 2. vHsmUpd_Rec

- **UUID**: `2ab5ee46-4f7f-4349-8c4a-4b98a7e65d90`
- **配置名称**: `vHsmUpd_Rec`
- **定义引用**: `/MICROSAR/vHsmUpd`
