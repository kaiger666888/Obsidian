# MemIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:19

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [MemIf](#memif)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. MemIf

#### 基本信息

- **UUID**: `d8c86b6b-2f23-4269-bd81-bc8715465bdd`
- **模块名称**: `MemIf`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Memory Abstraction Interface. The interface abstracts from the number of
underlying FEE or EA modules.

#NVRAM #NVMemory #Memory #DataStorage
#AUTOSAR

#### 版本历史

共有 **15** 个版本记录：

##### 1. 版本 4.00.00

- **状态**: released
- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

**变更内容**:

##### 2. 版本 4.00.01

- **状态**: released
- **发布日期**: 2013-02-18T09:34:20+01:00
- **发布者**: virdu

**变更内容**:

##### 3. 版本 4.01.00

- **状态**: released
- **发布日期**: 2013-07-05T02:24:43+02:00
- **发布者**: virdu

**变更内容**:

##### 4. 版本 

- **发布日期**: 2013-09-16T02:54:11+02:00
- **发布者**: virjas

**变更内容**:

##### 5. 版本 4.01.01

- **状态**: released
- **发布日期**: 2013-10-30
- **发布者**: virdu

**变更内容**:

##### 6. 版本 4.01.02

- **状态**: released
- **发布日期**: 2014-11-21T11:23:44+01:00
- **发布者**: virgmi

**变更内容**:

##### 7. 版本 4.02.00

- **状态**: released
- **发布日期**: 2015-04-21T10:01:45+02:00
- **发布者**: virgmi

**变更内容**:

##### 8. 版本 4.03.00

- **状态**: released
- **发布日期**: 2015-09-18T03:20:01+02:00
- **发布者**: virgmi

**变更内容**:

##### 9. 版本 4.04.00

- **状态**: released
- **发布日期**: 2016-02-08T01:57:19+01:00
- **发布者**: virgmi

**变更内容**:

##### 10. 版本 4.05.00

- **状态**: released
- **发布日期**: 2016-12-19T12:56:17+01:00
- **发布者**: virgmi

**变更内容**:

##### 11. 版本 

- **状态**: released
- **发布日期**: 2017-01-26T05:51:45+01:00
- **发布者**: virgmi

**变更内容**:

##### 12. 版本 4.06.00

- **状态**: released
- **发布日期**: 2019-05-28T08:46:06+02:00
- **发布者**: virsrl

**变更内容**:

##### 13. 版本 4.06.01

- **状态**: released
- **发布日期**: 2021-07-26T13:05:46+02:00
- **发布者**: virljs

**变更内容**:

##### 14. 版本 5.00.00

- **状态**: released
- **发布日期**: 2022-02-08T18:31:14+01:00
- **发布者**: virlra

**变更内容**:

##### 15. 版本 5.00.01

- **状态**: released
- **发布日期**: 2022-10-05T14:16:46+02:00
- **发布者**: vireno

**变更内容**:

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. MemIfGeneral

**容器属性**:

- **UUID**: `5844f24a-5769-4bbc-a295-9891247a3bfb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemIfGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the MemIf.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. MemIfNumberOfDevices

- **UUID**: `9713090c-6f01-46d6-9506-c93c115289c4`
- **参数名**: `MemIfNumberOfDevices`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the concrete number of underlying memory abstraction modules.

Note: Parameter not used.

####### BOOLEAN 类型参数

######## 1. MemIfDevErrorDetect

- **UUID**: `1ef88c2c-8e6b-47ba-bbbb-91f87bcc1b45`
- **参数名**: `MemIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. MemIfVersionInfoApi

- **UUID**: `bee0de14-dd7d-4ba4-9422-161df7ea212e`
- **参数名**: `MemIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function MemIf_GetVersionInfo() to get major, minor and patch version information.

######## 3. MemIfSafeBswChecks

- **UUID**: `dd3dbff3-d118-4401-85c1-c8bd6ec90b85`
- **参数名**: `MemIfSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

True: safety checks shall be enabled.
False: safety checks shall NOT be enabled.

##### 2. MemIfMemHwA

**容器属性**:

- **UUID**: `2d484599-bede-4f24-bf5c-96ef74186f4f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemIfMemHwA`
- **多重性**: [1..16]
- **构建后可变**: false

**容器描述**:

This container includes the configuration of one underlaying Memory Hardware Abstraction module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. MemIfMemHwAId

- **UUID**: `4f496248-1a61-47a1-b82a-a2b88b60a8bd`
- **参数名**: `MemIfMemHwAId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..254]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the unique handle to address the underlaying Memory Hardware Abstraction module.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. MemIfMemHwARef

- **UUID**: `13ebb825-dd30-47df-8888-26c6a6d702c1`
- **引用名**: `MemIfMemHwARef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Fee/FeeGeneral`
  - `/AUTOSAR/EcucDefs/Ea/EaGeneral`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the underlying Memory Hardware Abstraction module (FEE or EA).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. MemIfMemHwAAPI

**容器属性**:

- **UUID**: `342fe3e5-78f4-4caa-9966-5bf89b2be987`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemIfMemHwAAPI`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes API names of memory hardware abstraction device.

######## 参数配置

此容器包含 **9** 个参数：

######### STRING 类型参数

########## 1. MemIfMemHwAIncludeFile

- **UUID**: `c7b1b3ec-82d5-4df8-8b3e-244bfe7ae033`
- **参数名**: `MemIfMemHwAIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Fee.h`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the include file of the FEE / EA which declares the API service names.

######### FUNCTION-NAME 类型参数

########## 1. MemIfMemHwACancel

- **UUID**: `da4b7f25-a435-46e5-8180-7f1c869507f9`
- **参数名**: `MemIfMemHwACancel`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Cancel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to cancel a current job.

########## 2. MemIfMemHwAEraseImmediateBlock

- **UUID**: `f6c52089-7d74-4806-a24c-078c0a0c53dc`
- **参数名**: `MemIfMemHwAEraseImmediateBlock`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_EraseImmediateBlock`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to erase a block which is configured to hold high priority data.

########## 3. MemIfMemHwAGetJobResult

- **UUID**: `b90d7a70-f803-4a50-ac23-d9189a85517f`
- **参数名**: `MemIfMemHwAGetJobResult`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_GetJobResult`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to get the result of the last requested job.

########## 4. MemIfMemHwAGetStatus

- **UUID**: `86c05953-2de1-4092-9cd8-4a8bdbe133f1`
- **参数名**: `MemIfMemHwAGetStatus`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_GetStatus`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to get the current status of the FEE / EA.

########## 5. MemIfMemHwAInvalidateBlock

- **UUID**: `a71f57ae-fe1b-47fd-acf8-7f48564c21cb`
- **参数名**: `MemIfMemHwAInvalidateBlock`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_InvalidateBlock`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to invalidate a block.

########## 6. MemIfMemHwARead

- **UUID**: `7eeff580-8ea3-4395-ae7c-f1030f127965`
- **参数名**: `MemIfMemHwARead`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Read`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to read data.

########## 7. MemIfMemHwASetMode

- **UUID**: `960e668b-4885-431e-8c25-913f84dd93ce`
- **参数名**: `MemIfMemHwASetMode`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_SetMode`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to set the mode.

########## 8. MemIfMemHwAWrite

- **UUID**: `af656c30-5393-4db2-ab79-ab2f17ddf02c`
- **参数名**: `MemIfMemHwAWrite`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Write`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to write data.

##### 3. MemIfMemHwAAPI

**容器属性**:

- **UUID**: `342fe3e5-78f4-4caa-9966-5bf89b2be987`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `MemIfMemHwAAPI`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes API names of memory hardware abstraction device.

###### 参数配置

此容器包含 **9** 个参数：

####### STRING 类型参数

######## 1. MemIfMemHwAIncludeFile

- **UUID**: `c7b1b3ec-82d5-4df8-8b3e-244bfe7ae033`
- **参数名**: `MemIfMemHwAIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Fee.h`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the include file of the FEE / EA which declares the API service names.

####### FUNCTION-NAME 类型参数

######## 1. MemIfMemHwACancel

- **UUID**: `da4b7f25-a435-46e5-8180-7f1c869507f9`
- **参数名**: `MemIfMemHwACancel`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Cancel`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to cancel a current job.

######## 2. MemIfMemHwAEraseImmediateBlock

- **UUID**: `f6c52089-7d74-4806-a24c-078c0a0c53dc`
- **参数名**: `MemIfMemHwAEraseImmediateBlock`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_EraseImmediateBlock`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to erase a block which is configured to hold high priority data.

######## 3. MemIfMemHwAGetJobResult

- **UUID**: `b90d7a70-f803-4a50-ac23-d9189a85517f`
- **参数名**: `MemIfMemHwAGetJobResult`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_GetJobResult`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to get the result of the last requested job.

######## 4. MemIfMemHwAGetStatus

- **UUID**: `86c05953-2de1-4092-9cd8-4a8bdbe133f1`
- **参数名**: `MemIfMemHwAGetStatus`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_GetStatus`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to get the current status of the FEE / EA.

######## 5. MemIfMemHwAInvalidateBlock

- **UUID**: `a71f57ae-fe1b-47fd-acf8-7f48564c21cb`
- **参数名**: `MemIfMemHwAInvalidateBlock`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_InvalidateBlock`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to invalidate a block.

######## 6. MemIfMemHwARead

- **UUID**: `7eeff580-8ea3-4395-ae7c-f1030f127965`
- **参数名**: `MemIfMemHwARead`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Read`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to read data.

######## 7. MemIfMemHwASetMode

- **UUID**: `960e668b-4885-431e-8c25-913f84dd93ce`
- **参数名**: `MemIfMemHwASetMode`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_SetMode`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to set the mode.

######## 8. MemIfMemHwAWrite

- **UUID**: `af656c30-5393-4db2-ab79-ab2f17ddf02c`
- **参数名**: `MemIfMemHwAWrite`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Fee_Write`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the API service name of the FEE / EA which is used to write data.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **MemIf**

##### BSW-IMPLEMENTATION 类型元素

1. **MemIf_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **MemIf_Pre**
2. **MemIf_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. MemIf_Impl

- **UUID**: `a4824c1e-a2d9-4829-9bed-13cef6f49483`
- **实现名称**: `MemIf_Impl`
- **编程语言**: C
- **软件版本**: 4.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. MemIf_Pre

- **UUID**: `09e55617-d83f-4447-b37b-fd73509e69c3`
- **配置名称**: `MemIf_Pre`
- **定义引用**: `/MICROSAR/MemIf`

### 2. MemIf_Rec

- **UUID**: `ba628155-ce89-4e3d-812f-04b362c8dc70`
- **配置名称**: `MemIf_Rec`
- **定义引用**: `/MICROSAR/MemIf`
