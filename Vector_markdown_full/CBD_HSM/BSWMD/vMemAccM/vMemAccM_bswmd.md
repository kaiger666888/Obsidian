# vMemAccM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:02

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vMemAccM](#vmemaccm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vMemAccM

#### 基本信息

- **UUID**: `8450a790-7469-4c0f-8e01-cb073c5023bf`
- **模块名称**: `vMemAccM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the vMemAccM (Memory Access Manager) module.

#### 版本历史

共有 **14** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-01-17T08:24:36+01:00
- **发布者**: virjwa

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-04-09T01:17:46+02:00
- **发布者**: viroto, vircre

**变更内容**:

##### 3. 版本 1.01.01

- **状态**: released
- **发布日期**: 2018-06-07T13:50:04+02:00
- **发布者**: viroto

**变更内容**:

##### 4. 版本 1.02.00

- **状态**: released
- **发布日期**: 2018-09-17T07:23:52+02:00
- **发布者**: viroto

**变更内容**:

##### 5. 版本 1.03.00

- **状态**: released
- **发布日期**: 2018-12-17T10:46:37+01:00
- **发布者**: viroto

**变更内容**:

##### 6. 版本 1.04.00

- **状态**: released
- **发布日期**: 2019-01-03T13:49:27+01:00
- **发布者**: viroto, vircre

**变更内容**:

##### 7. 版本 1.05.00

- **状态**: released
- **发布日期**: 2019-01-24T13:44:25+01:00
- **发布者**: viroto

**变更内容**:

##### 8. 版本 1.06.00

- **状态**: released
- **发布日期**: 2019-02-28T06:52:50+01:00
- **发布者**: viroto

**变更内容**:

##### 9. 版本 1.07.00

- **状态**: released
- **发布日期**: 2019-06-27T08:32:50+02:00
- **发布者**: viroto

**变更内容**:

##### 10. 版本 2.00.00

- **状态**: released
- **发布日期**: 2019-07-25T09:25:35+02:00
- **发布者**: virsrl

**变更内容**:

##### 11. 版本 2.00.01

- **状态**: released
- **发布日期**: 2019-10-29T12:11:13+01:00
- **发布者**: virewe

**变更内容**:

##### 12. 版本 2.01.00

- **状态**: released
- **发布日期**: 2020-03-02T12:37:32+01:00
- **发布者**: viroto

**变更内容**:

##### 13. 版本 2.01.01

- **状态**: released
- **发布日期**: 2020-04-17T13:11:39+02:00
- **发布者**: viroto

**变更内容**:

##### 14. 版本 3.00.00

- **状态**: released
- **发布日期**: 2020-05-11T11:36:53+02:00
- **发布者**: virsrl

**变更内容**:

#### 配置容器

本模块包含 **7** 个配置容器：

##### 1. vMemAccMGeneral

**容器属性**:

- **UUID**: `13710ce2-af07-4af0-b6ca-1deb91ba178c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the vMemAccM.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. vMemAccMVersionInfoApi

- **UUID**: `af2ad231-abe2-470f-a43f-7e15a95f78c9`
- **参数名**: `vMemAccMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function vMemAccM_GetVersionInfo() to get major, minor and patch version information.

######## 2. vMemAccMSafeBswChecks

- **UUID**: `97750fde-04df-4e97-b0be-1a709df01f1c`
- **参数名**: `vMemAccMSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 3. vMemAccMDevErrorDetect

- **UUID**: `d2049265-c662-4503-b48b-9759e2dedca6`
- **参数名**: `vMemAccMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 4. vMemAccMCompareApi

- **UUID**: `94604b97-5a53-4921-b0eb-2fb0b8d888ba`
- **参数名**: `vMemAccMCompareApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function vMemAccM_Compare().
This function allows to compare data stored in a buffer with data stored in memory.

####### FLOAT 类型参数

######## 1. vMemAccMMainFunctionPeriod

- **UUID**: `6ede0c27-768c-4737-8735-7282fb10282a`
- **参数名**: `vMemAccMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0.0001..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the fixed call cycle for vMemAccM_MainFunction().
This information affects RTE's (SchM's) settings.

vMemAccM itself does not depend on a fixed cycle time; in can be triggered at arbitrary rates.

It is not necessary to trigger vMemAccM faster than vMem.

The faster you want vMemAccM_MainFunction being triggered, the smaller this value should be and vice versa.

####### ENUMERATION 类型参数

######## 1. vMemAccMMainFunctionTriggering

- **UUID**: `e5c46e2b-cae6-44e0-b9fb-530f37930333`
- **参数名**: `vMemAccMMainFunctionTriggering`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FixedCycleTime`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FixedCycleTime` (来源: Vector Informatik)
  - `BackgroundTask` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the way how vMemAccM_MainFunction() is called.
The vMemAccM_MainFunction() can be scheduled in different ways, which allows adapting the runtime behavior
- FixedCycleTime: All activities are executed in the vMemAccM_MainFunction() with the defined cycle time.
- BackgroundTask: Activities that do not require a fixed cycle time run in the background task. The response time of such activities will depend on the current CPU load.
Note
If the system is overloaded, it may happen that the background task is no longer called.

##### 2. vMemAccMAddressAreaConfiguration

**容器属性**:

- **UUID**: `314f4a0d-1eb6-45be-b7ea-d1e8fe8232b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMAddressAreaConfiguration`
- **多重性**: [1..65536]
- **构建后可变**: false

**容器描述**:

This container includes the configuration of AddressArea specific parameters for the vMemAccM module.
An AddressArea is a virtual area of memory. Upper layers only use virtual addresses to access the address area. It is the job of vMemAccM to map between virtual and physical addresses. An AddressArea contains SubAddressAreas and each SubAddressArea is part of a physically continuous memory area (sector batch)

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vMemAccMAddressAreaId

- **UUID**: `0ad5003e-f93a-4dbc-86c8-0e2e36d9a1cb`
- **参数名**: `vMemAccMAddressAreaId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies a unique identifier which is used to reference to an AddressArea.
This identifier is used as parameter for vMemAccM jobs in order to distinguish between several AddressAreas with the same virtual addresses.

######## 2. vMemAccMAddressAreaPriority

- **UUID**: `8c99bc03-1040-422b-a189-4aa2e80192fd`
- **参数名**: `vMemAccMAddressAreaPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the priority of an AddressArea compared to other AddressAreas.

For each AddressArea one job may be pending at the same time. vMemAccM processes the jobs prioriry based.
This priority even works preemptive. Higher priority jobs pause
lower priority jobs in a non-destructive manner.

Whereas 0 is the lowest priority, 65535 is the highest priority. It is furthermore not allowed for two AddressAreas to have the same priority.

######## 3. vMemAccMReadRequestLength

- **UUID**: `38807e6e-e6ee-498b-b72c-5cf2108e8dd5`
- **参数名**: `vMemAccMReadRequestLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `64`
- **取值范围**: [8..4096]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of bytes the vMemAccM module requests within one vMem read request.
Higher values might block jobs on AddressAreas even with higher priority because current vMem job must be finished before a job on another AddressArea can be started.
Lower values might lead to a decreased performance, because more MainFunctionCycles (vMemAccM and vMem) are needed.
Therefore this value has to be choosen with care!

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vMemAccMSubAddressAreaConfiguration

**容器属性**:

- **UUID**: `d1afb210-1a14-49d8-a094-819a663745b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMSubAddressAreaConfiguration`
- **多重性**: [1..65536]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters for a  physically continous area of memory.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. vMemAccMNumberOfSectors

- **UUID**: `c0c8c702-dd7c-4fcb-a739-aecda5760a95`
- **参数名**: `vMemAccMNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of physical sectors of this Sub-AddressArea.

########## 2. vMemAccMVirtualStartAddress

- **UUID**: `b1b6f8e4-1d1a-4179-b052-6b3b5ecc57f6`
- **参数名**: `vMemAccMVirtualStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the virtual start address of this Sub-AddressArea.

########## 3. vMemAccMPhysicalStartAddress

- **UUID**: `48c1da69-04da-4fd9-a545-b387d680e1b0`
- **参数名**: `vMemAccMPhysicalStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical start address of this Sub-AddressArea.

########## 4. vMemAccMNrOfWriteRetries

- **UUID**: `50d7fa3b-ac54-47cc-96eb-24a721d5efe6`
- **参数名**: `vMemAccMNrOfWriteRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of retries of a failed write job.
== 0: no retry, a failed job will be aborted immediately
> 0: retry the number of times before aborting the job.

########## 5. vMemAccMNrOfEraseRetries

- **UUID**: `768e24c2-6f3a-41d9-8a2e-2adbeeb20ee3`
- **参数名**: `vMemAccMNrOfEraseRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of retries of a failed erase job.
== 0: no retry, a failed job will be aborted immediately
> 0: retry the number of times before aborting the job.

######### BOOLEAN 类型参数

########## 1. vMemAccMUseEraseBurst

- **UUID**: `0fb9a052-84d8-4e9f-80c9-70e0fd69673f`
- **参数名**: `vMemAccMUseEraseBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables the erase bursting for the related sub address area. 

Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst, because of too long burst durations.

########## 2. vMemAccMUseWriteBurst

- **UUID**: `ab03ba2c-a6f8-4df4-94a3-4be5e62f6e7f`
- **参数名**: `vMemAccMUseWriteBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables the write bursting for the related sub address area. 

Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst, because of too long burst durations.

######### STRING 类型参数

########## 1. vMemAccMvMemFuncPtrTableSymbol

- **UUID**: `a87f59b1-6909-4577-8e56-b2a148f1e008`
- **参数名**: `vMemAccMvMemFuncPtrTableSymbol`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The symbol of the vMem function pointer table the vMemAccM uses to access the specific vMem API. vMemAccM expects this symbol to be provided by the specific vMem. The symbol may be changed by user, if necessary.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vMemAccMSectorRef

- **UUID**: `63c7c4cc-0db7-4b9c-bf53-ed8e5cfaf03c`
- **引用名**: `vMemAccMSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to vMem's sector batch where the Sub-AddressArea is located.

####### 2. vMemAccMAddressAreaVariantConfiguration

**容器属性**:

- **UUID**: `c139836e-2c60-4998-a63a-ff2d2a7db0b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMAddressAreaVariantConfiguration`
- **多重性**: [0..2]
- **构建后可变**: false

**容器描述**:

This container includes all sub address areas belonging to the one specific address area variant.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vMemAccMAddressAreaVariantId

- **UUID**: `faf320f4-7c91-4009-8b22-7957be210733`
- **参数名**: `vMemAccMAddressAreaVariantId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies a unique identifier which is used to reference to an AddressAreaVariant. The value will be used to set the currently active variant.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vMemAccMSubAddressAreaRef

- **UUID**: `43fbb56b-ae95-4a31-9fbe-0fe72e5339e0`
- **引用名**: `vMemAccMSubAddressAreaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `vMemAccMSubAddressAreaConfiguration`
- **完整路径**: `/MICROSAR/vMemAccM/vMemAccMAddressAreaConfiguration/vMemAccMSubAddressAreaConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all SubAddressAreas relevant for this variant.

##### 3. vMemAccMSubAddressAreaConfiguration

**容器属性**:

- **UUID**: `d1afb210-1a14-49d8-a094-819a663745b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMSubAddressAreaConfiguration`
- **多重性**: [1..65536]
- **构建后可变**: false

**容器描述**:

This container includes the configuration parameters for a  physically continous area of memory.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. vMemAccMNumberOfSectors

- **UUID**: `c0c8c702-dd7c-4fcb-a739-aecda5760a95`
- **参数名**: `vMemAccMNumberOfSectors`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of physical sectors of this Sub-AddressArea.

######## 2. vMemAccMVirtualStartAddress

- **UUID**: `b1b6f8e4-1d1a-4179-b052-6b3b5ecc57f6`
- **参数名**: `vMemAccMVirtualStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the virtual start address of this Sub-AddressArea.

######## 3. vMemAccMPhysicalStartAddress

- **UUID**: `48c1da69-04da-4fd9-a545-b387d680e1b0`
- **参数名**: `vMemAccMPhysicalStartAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the physical start address of this Sub-AddressArea.

######## 4. vMemAccMNrOfWriteRetries

- **UUID**: `50d7fa3b-ac54-47cc-96eb-24a721d5efe6`
- **参数名**: `vMemAccMNrOfWriteRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of retries of a failed write job.
== 0: no retry, a failed job will be aborted immediately
> 0: retry the number of times before aborting the job.

######## 5. vMemAccMNrOfEraseRetries

- **UUID**: `768e24c2-6f3a-41d9-8a2e-2adbeeb20ee3`
- **参数名**: `vMemAccMNrOfEraseRetries`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the number of retries of a failed erase job.
== 0: no retry, a failed job will be aborted immediately
> 0: retry the number of times before aborting the job.

####### BOOLEAN 类型参数

######## 1. vMemAccMUseEraseBurst

- **UUID**: `0fb9a052-84d8-4e9f-80c9-70e0fd69673f`
- **参数名**: `vMemAccMUseEraseBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables the erase bursting for the related sub address area. 

Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst, because of too long burst durations.

######## 2. vMemAccMUseWriteBurst

- **UUID**: `ab03ba2c-a6f8-4df4-94a3-4be5e62f6e7f`
- **参数名**: `vMemAccMUseWriteBurst`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables the write bursting for the related sub address area. 

Use case: the vMem may be burst capable, but the user does not want the vMemAccM to burst, because of too long burst durations.

####### STRING 类型参数

######## 1. vMemAccMvMemFuncPtrTableSymbol

- **UUID**: `a87f59b1-6909-4577-8e56-b2a148f1e008`
- **参数名**: `vMemAccMvMemFuncPtrTableSymbol`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The symbol of the vMem function pointer table the vMemAccM uses to access the specific vMem API. vMemAccM expects this symbol to be provided by the specific vMem. The symbol may be changed by user, if necessary.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vMemAccMSectorRef

- **UUID**: `63c7c4cc-0db7-4b9c-bf53-ed8e5cfaf03c`
- **引用名**: `vMemAccMSectorRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `vMemSector`
- **完整路径**: `/MICROSAR/vMem/vMem/vMemInstance/vMemSectorList/vMemSector`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to vMem's sector batch where the Sub-AddressArea is located.

##### 4. vMemAccMAddressAreaVariantConfiguration

**容器属性**:

- **UUID**: `c139836e-2c60-4998-a63a-ff2d2a7db0b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMAddressAreaVariantConfiguration`
- **多重性**: [0..2]
- **构建后可变**: false

**容器描述**:

This container includes all sub address areas belonging to the one specific address area variant.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vMemAccMAddressAreaVariantId

- **UUID**: `faf320f4-7c91-4009-8b22-7957be210733`
- **参数名**: `vMemAccMAddressAreaVariantId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies a unique identifier which is used to reference to an AddressAreaVariant. The value will be used to set the currently active variant.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vMemAccMSubAddressAreaRef

- **UUID**: `43fbb56b-ae95-4a31-9fbe-0fe72e5339e0`
- **引用名**: `vMemAccMSubAddressAreaRef`
- **引用类型**: REFERENCE
- **多重性**: [1..65535]
- **目标**: `vMemAccMSubAddressAreaConfiguration`
- **完整路径**: `/MICROSAR/vMemAccM/vMemAccMAddressAreaConfiguration/vMemAccMSubAddressAreaConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to all SubAddressAreas relevant for this variant.

##### 5. vMemAccMMultiPartitionConfiguration

**容器属性**:

- **UUID**: `b937e2ca-5ce0-460c-8631-9393682aaa6b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMMultiPartitionConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container stores all configuration values required for a vMemAccM multi partition synchronization.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. vMemAccMMultiPartitionUsecase

- **UUID**: `6a7e5296-7ef0-4f1d-97ef-d34a01b4db5f`
- **参数名**: `vMemAccMMultiPartitionUsecase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SynchronizeMultipleNVRAMAccessors`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SynchronizeMultipleNVRAMAccessors` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the current use case of the vMemAccM multi partition synchronization:
MultipleNVRAMUsers: each partition accesses the NV RAM peripheral on its own, the accesses need to be synchronized.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vMemAccMPartitionConfiguration

**容器属性**:

- **UUID**: `13501a3f-cef3-46c4-8b79-908621fa1cbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMPartitionConfiguration`
- **多重性**: [1..16]
- **构建后可变**: false

**容器描述**:

This container holds all required vMemAccM partition configuration parameters. 

All of the partition containers act as slaves within the multi partition system - all publish their next requests to the master partition and wait until the master partition sets the NV RAM access token to their identifier.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vMemAccMPartitionId

- **UUID**: `c5b7a408-5297-4cbe-a0cf-143435c9e684`
- **参数名**: `vMemAccMPartitionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [1..253]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the unique partition identifier. The value range is [1, 16].

0 is reserved for the master partition.
[254, 255] are reserved for internal usage.

######### STRING 类型参数

########## 1. vMemAccMNVRAMAccessToken

- **UUID**: `22901fe5-d702-40b0-b0f1-89e2b4183a50`
- **参数名**: `vMemAccMNVRAMAccessToken`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `vMemAccM_NVRAMAccessToken`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the address of the NV RAM access token in shared RAM. The vMemAccM master defines and writes the variable with the symbol vMemAccM_NVRAMAccessToken. The other partions must not modify the token.

The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

Caution: The address must be 4 bytes aligned.

########## 2. vMemAccMPartitionPublishRequest

- **UUID**: `a07bf774-c223-4ae3-a8bd-9fb1c3103120`
- **参数名**: `vMemAccMPartitionPublishRequest`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the address of the variable holding the published partition request in shared RAM. The vMemAccM master defines the variable with the symbol vMemAccM_PublishReq_<SlaveName>_Id<SlaveId>.

The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

Caution: The address must be 4 bytes aligned.

####### 2. vMemAccMMasterPartitionConfiguration

**容器属性**:

- **UUID**: `c6c073fe-64e2-44e0-9e9d-49b2c844c8d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMMasterPartitionConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container holds all required vMemAccM master partition configuration parameters. 

The container defines the master partition synchronizing the NV RAM accesses of all other partitions via the NV RAM access token. If this container exists, the vMemAccM will act as a master. If this container does not exist, the vMemAccM will act as slave.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vMemAccMMasterPartitionId

- **UUID**: `a5ce847c-573e-4c1c-9aef-108a8e0758a7`
- **参数名**: `vMemAccMMasterPartitionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the unique master partition identifier - always 0.

[1, 253] are reserved for slave partitions.
[254, 255] are reserved for internal usage.

##### 6. vMemAccMPartitionConfiguration

**容器属性**:

- **UUID**: `13501a3f-cef3-46c4-8b79-908621fa1cbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMPartitionConfiguration`
- **多重性**: [1..16]
- **构建后可变**: false

**容器描述**:

This container holds all required vMemAccM partition configuration parameters. 

All of the partition containers act as slaves within the multi partition system - all publish their next requests to the master partition and wait until the master partition sets the NV RAM access token to their identifier.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vMemAccMPartitionId

- **UUID**: `c5b7a408-5297-4cbe-a0cf-143435c9e684`
- **参数名**: `vMemAccMPartitionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `253`
- **取值范围**: [1..253]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the unique partition identifier. The value range is [1, 16].

0 is reserved for the master partition.
[254, 255] are reserved for internal usage.

####### STRING 类型参数

######## 1. vMemAccMNVRAMAccessToken

- **UUID**: `22901fe5-d702-40b0-b0f1-89e2b4183a50`
- **参数名**: `vMemAccMNVRAMAccessToken`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `vMemAccM_NVRAMAccessToken`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the address of the NV RAM access token in shared RAM. The vMemAccM master defines and writes the variable with the symbol vMemAccM_NVRAMAccessToken. The other partions must not modify the token.

The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

Caution: The address must be 4 bytes aligned.

######## 2. vMemAccMPartitionPublishRequest

- **UUID**: `a07bf774-c223-4ae3-a8bd-9fb1c3103120`
- **参数名**: `vMemAccMPartitionPublishRequest`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the address of the variable holding the published partition request in shared RAM. The vMemAccM master defines the variable with the symbol vMemAccM_PublishReq_<SlaveName>_Id<SlaveId>.

The address can be specified either as a valid decimal (1024) or hexadecimal (0x4000) value, or as a valid linker symbol.

Caution: The address must be 4 bytes aligned.

##### 7. vMemAccMMasterPartitionConfiguration

**容器属性**:

- **UUID**: `c6c073fe-64e2-44e0-9e9d-49b2c844c8d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vMemAccMMasterPartitionConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container holds all required vMemAccM master partition configuration parameters. 

The container defines the master partition synchronizing the NV RAM accesses of all other partitions via the NV RAM access token. If this container exists, the vMemAccM will act as a master. If this container does not exist, the vMemAccM will act as slave.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vMemAccMMasterPartitionId

- **UUID**: `a5ce847c-573e-4c1c-9aef-108a8e0758a7`
- **参数名**: `vMemAccMMasterPartitionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..0]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the unique master partition identifier - always 0.

[1, 253] are reserved for slave partitions.
[254, 255] are reserved for internal usage.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vMemAccM_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vMemAccM**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vMemAccM_Pre**
2. **vMemAccM_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vMemAccM_Impl

- **UUID**: `ebefc909-aef6-4895-ac3a-fd6042b80438`
- **实现名称**: `vMemAccM_Impl`
- **编程语言**: C
- **软件版本**: 4.00.00
- **供应商ID**: 30
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vMemAccM_Pre

- **UUID**: `e6c770b5-f093-4858-a685-47902e145592`
- **配置名称**: `vMemAccM_Pre`
- **定义引用**: `/MICROSAR/vMemAccM`

### 2. vMemAccM_Rec

- **UUID**: `1523d333-d443-466e-a5f7-9d2b6640c1bf`
- **配置名称**: `vMemAccM_Rec`
- **定义引用**: `/MICROSAR/vMemAccM`
