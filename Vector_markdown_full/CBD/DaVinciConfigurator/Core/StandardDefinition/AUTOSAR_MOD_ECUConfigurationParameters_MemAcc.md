# MemAcc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:27

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [MemAcc](#memacc)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00052.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. MemAcc

#### 基本信息

- **UUID**: `ECUC:4212adf9-1244-4ddb-90bf-e6cbb22e6541`
- **模块名称**: `MemAcc`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

The MemAcc (Memory Access module) coordinates the memory access by multiple users in order to avoid conflicts with this shared memory resource.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.9.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. MemAccAddressAreaConfiguration

**容器属性**:

- **UUID**: `ECUC:45ebc730-20b2-4d42-9005-330413a1129b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemAccAddressAreaConfiguration`
- **多重性**: [1..65535]

**容器描述**:

This container includes the configuration of AddressArea specific parameters for the MemAcc module.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. MemAccAddressAreaId

- **UUID**: `ECUC:f948c054-627c-410b-a324-9b45c2f3fa5f`
- **参数名**: `MemAccAddressAreaId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This value specifies a unique identifier which is used to reference to an AddressArea.

######## 2. MemAccAddressAreaPriority

- **UUID**: `ECUC:5e15534f-228c-4421-b2d7-e30ca1983462`
- **参数名**: `MemAccAddressAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the priority of an AddressArea compared to other AddressAreas (0 = lowest priority, 65535 = highest priority).

######## 3. MemAccBufferAlignmentValue

- **UUID**: `ECUC:6514eae0-8aef-4551-bbe7-f91a8dfeb208`
- **参数名**: `MemAccBufferAlignmentValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Buffer alignment value inherited by MemAcc upper layer modules. The value must be a multiple of MinReadSize.

####### FUNCTION-NAME 类型参数

######## 1. MemAccJobEndNotificationName

- **UUID**: `ECUC:d72e0b95-3fd4-4495-b1b8-1a1734f2c6bf`
- **参数名**: `MemAccJobEndNotificationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **描述**: Job end notification function which is called after MemAcc job completion. If this parameter is left empty, no job end notification is triggered and the upper layer module needs to poll the job results.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemAccSubAddressAreaConfiguration

**容器属性**:

- **UUID**: `ECUC:73208405-b241-41ca-9e96-61ced69f93f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemAccSubAddressAreaConfiguration`
- **多重性**: [1..65536]

**容器描述**:

This container includes the configuration parameters for a physically continuous area of memory.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. MemAccLogicalStartAddress

- **UUID**: `ECUC:586dd3cc-8617-47f1-a34a-46ed02a932db`
- **参数名**: `MemAccLogicalStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the logical start address of the SubAddressArea.

########## 2. MemAccNumberOfEraseRetries

- **UUID**: `ECUC:d19910ad-87a6-4160-b36b-fa7a186ce0a3`
- **参数名**: `MemAccNumberOfEraseRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of retries of a failed erase job.

########## 3. MemAccNumberOfSectors

- **UUID**: `ECUC:146096d5-55e2-47ee-b417-063440e9f973`
- **参数名**: `MemAccNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of physical sectors of the SubAddressArea.

########## 4. MemAccNumberOfWriteRetries

- **UUID**: `ECUC:171c9972-51ea-4654-b0c2-c7f8865417f8`
- **参数名**: `MemAccNumberOfWriteRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of retries of a failed write job.

########## 5. MemAccSectorOffset

- **UUID**: `ECUC:282684a6-a8d7-4397-b1d0-a01b7de25923`
- **参数名**: `MemAccSectorOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the sector offset of the SubAddressArea in case the SubAddressArea should not start with the first sector of the referenced MemSectorBatch.

######### BOOLEAN 类型参数

########## 1. MemAccUseEraseBurst

- **UUID**: `ECUC:6dc692a5-9afe-4a92-b831-0faadaffe883`
- **参数名**: `MemAccUseEraseBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables erase bursting for the related sub address area.

########## 2. MemAccUseWriteBurst

- **UUID**: `ECUC:27bdc622-e7b5-410c-b4cb-1da7b5d082a5`
- **参数名**: `MemAccUseWriteBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables write bursting for the related sub address area.

######### STRING 类型参数

########## 1. MemAccMemNamePrefix

- **UUID**: `ECUC:180ca96a-0830-4c7c-9d1e-d3e5bb9b50f1`
- **参数名**: `MemAccMemNamePrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Depending on the MemAccUseMemFuncPtrTable configuration, this prefix is either used to reference the Mem driver header structure or the according Mem API function.

######### ENUMERATION 类型参数

########## 1. MemAccMemInvocation

- **UUID**: `ECUC:327ea341-ecf2-439e-a569-ce671ca1ce91`
- **参数名**: `MemAccMemInvocation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DIRECT_STATIC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT_STATIC` (来源: AUTOSAR_ECUC)
  - `INDIRECT_DYNAMIC` (来源: AUTOSAR_ECUC)
  - `INDIRECT_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the Mem driver services are accessed and how the Mem driver is scheduled and activated/initialized.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. MemAccSectorBatchRef

- **UUID**: `ECUC:fe16cc80-63fc-41b9-aaa2-387f8c3eb3d1`
- **引用名**: `MemAccSectorBatchRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemSectorBatch`
- **完整路径**: `/AUTOSAR/EcucDefs/Mem/MemInstance/MemSectorBatch`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to MemSectorBatch mapped to the SubAddressArea.

##### 2. MemAccSubAddressAreaConfiguration

**容器属性**:

- **UUID**: `ECUC:73208405-b241-41ca-9e96-61ced69f93f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemAccSubAddressAreaConfiguration`
- **多重性**: [1..65536]

**容器描述**:

This container includes the configuration parameters for a physically continuous area of memory.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. MemAccLogicalStartAddress

- **UUID**: `ECUC:586dd3cc-8617-47f1-a34a-46ed02a932db`
- **参数名**: `MemAccLogicalStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the logical start address of the SubAddressArea.

######## 2. MemAccNumberOfEraseRetries

- **UUID**: `ECUC:d19910ad-87a6-4160-b36b-fa7a186ce0a3`
- **参数名**: `MemAccNumberOfEraseRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of retries of a failed erase job.

######## 3. MemAccNumberOfSectors

- **UUID**: `ECUC:146096d5-55e2-47ee-b417-063440e9f973`
- **参数名**: `MemAccNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of physical sectors of the SubAddressArea.

######## 4. MemAccNumberOfWriteRetries

- **UUID**: `ECUC:171c9972-51ea-4654-b0c2-c7f8865417f8`
- **参数名**: `MemAccNumberOfWriteRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the number of retries of a failed write job.

######## 5. MemAccSectorOffset

- **UUID**: `ECUC:282684a6-a8d7-4397-b1d0-a01b7de25923`
- **参数名**: `MemAccSectorOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the sector offset of the SubAddressArea in case the SubAddressArea should not start with the first sector of the referenced MemSectorBatch.

####### BOOLEAN 类型参数

######## 1. MemAccUseEraseBurst

- **UUID**: `ECUC:6dc692a5-9afe-4a92-b831-0faadaffe883`
- **参数名**: `MemAccUseEraseBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables erase bursting for the related sub address area.

######## 2. MemAccUseWriteBurst

- **UUID**: `ECUC:27bdc622-e7b5-410c-b4cb-1da7b5d082a5`
- **参数名**: `MemAccUseWriteBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables write bursting for the related sub address area.

####### STRING 类型参数

######## 1. MemAccMemNamePrefix

- **UUID**: `ECUC:180ca96a-0830-4c7c-9d1e-d3e5bb9b50f1`
- **参数名**: `MemAccMemNamePrefix`
- **数据类型**: STRING
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **描述**: Depending on the MemAccUseMemFuncPtrTable configuration, this prefix is either used to reference the Mem driver header structure or the according Mem API function.

####### ENUMERATION 类型参数

######## 1. MemAccMemInvocation

- **UUID**: `ECUC:327ea341-ecf2-439e-a569-ce671ca1ce91`
- **参数名**: `MemAccMemInvocation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DIRECT_STATIC`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DIRECT_STATIC` (来源: AUTOSAR_ECUC)
  - `INDIRECT_DYNAMIC` (来源: AUTOSAR_ECUC)
  - `INDIRECT_STATIC` (来源: AUTOSAR_ECUC)
- **描述**: Defines how the Mem driver services are accessed and how the Mem driver is scheduled and activated/initialized.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. MemAccSectorBatchRef

- **UUID**: `ECUC:fe16cc80-63fc-41b9-aaa2-387f8c3eb3d1`
- **引用名**: `MemAccSectorBatchRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `MemSectorBatch`
- **完整路径**: `/AUTOSAR/EcucDefs/Mem/MemInstance/MemSectorBatch`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to MemSectorBatch mapped to the SubAddressArea.

##### 3. MemAccGeneral

**容器属性**:

- **UUID**: `ECUC:1b34beae-8474-4ee9-a639-05776988ecae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemAccGeneral`
- **多重性**: [1..1]

**容器描述**:

General configuration parameters of the MemAcc.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. MemAcc64BitSupport

- **UUID**: `ECUC:07b4dc39-eef4-4529-93ef-0594b19232fd`
- **参数名**: `MemAcc64BitSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: If this option is selected, the address type shall be implemented in 64Bit.

######## 2. MemAccCompareApi

- **UUID**: `ECUC:8fd286ce-5621-4b6e-92f7-36aa68a4236c`
- **参数名**: `MemAccCompareApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter enables/disables the function MemAcc_Compare().

######## 3. MemAccDevErrorDetect

- **UUID**: `ECUC:74255c6a-e605-4194-afdc-6f8f24315e73`
- **参数名**: `MemAccDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the development error detection and notification on or off.

######## 4. MemAccUseMemFuncPtrTable

- **UUID**: `ECUC:3b73b736-31e7-4ee5-b88c-7df3503d52d4`
- **参数名**: `MemAccUseMemFuncPtrTable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines if the Mem driver functions are called using the Mem function pointer table API.

####### FLOAT 类型参数

######## 1. MemAccMainFunctionPeriod

- **UUID**: `ECUC:c26cca1f-ac56-49eb-9f05-45be07674962`
- **参数名**: `MemAccMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [1E-4..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This value specifies the fixed call cycle for MemAcc_MainFunction().

####### STRING 类型参数

######## 1. MemAccPublicCddHeaderFile

- **UUID**: `ECUC:e66f59a1-3d2b-4638-9494-ee136fac050c`
- **参数名**: `MemAccPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **描述**: Defines header files for callback functions which shall be included in case of CDDs. Range of characters is 1.. 32.

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

1. **MemAcc**
