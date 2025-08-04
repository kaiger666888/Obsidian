# FvM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FvM](#fvm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FvM

#### 基本信息

- **UUID**: `1f892ebf-126e-4fa2-aaf1-91b82856fe42`
- **模块名称**: `FvM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The software component Freshness Value Manager provides freshness values to the Secure Onboard Communication module. The freshness values are used to counter replay-attacks.
#Security
#Vector

#### 版本历史

共有 **3** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2021-02-19T15:28:01+01:00
- **发布者**: vismvi

**变更内容**:

##### 2. 版本 1.01.00

- **发布日期**: 2021-05-12T10:56:10+02:00
- **发布者**: vishho

**变更内容**:

##### 3. 版本 1.02.00

- **发布日期**: 2021-06-08T14:13:13+02:00
- **发布者**: vismvi

**变更内容**:

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. FvMGeneral

**容器属性**:

- **UUID**: `f9f1aa51-35ca-4246-acc0-387a7bd89a5f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FvMGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Freshness Value Manager Time Based General Attributes Container.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. FvMDevErrorDetect

- **UUID**: `9ac912c5-1997-4c6b-ba84-ad54ac3b9613`
- **参数名**: `FvMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Pre-processor switch for enabling development error detection support.

######## 2. FvMVersionInfoApi

- **UUID**: `28ca2bd0-f3ab-4b74-8bbd-eb0b44da55b2`
- **参数名**: `FvMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If true the SecOC_GetVersionInfo API is available.

######## 3. FvMSafeBswChecks

- **UUID**: `8c5e63ed-0a0b-4d6e-8207-a1a0ea2b41db`
- **参数名**: `FvMSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed.
This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FUNCTION-NAME 类型参数

######## 1. FvMCheckTxTimeBaseStatusCallout

- **UUID**: `20af9ce9-fbd1-4de1-a56c-befbe4d4e90a`
- **参数名**: `FvMCheckTxTimeBaseStatusCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_CheckTxTimeBaseStatusCallout`
- **描述**: This callout gives the application the opportunity to evaluate the StbM_TimeBaseStatus.
Returns E_OK -> FvM will use the time stamp.
Retruns E_NOT_OK -> FvM will not provide a freshness value to the SecOC.

######## 2. FvMCheckRxTimeBaseStatusCallout

- **UUID**: `790cfeb5-0084-44cb-81c6-df27744488b8`
- **参数名**: `FvMCheckRxTimeBaseStatusCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **函数变体**:
  - 默认值: `Appl_CheckRxTimeBaseStatusCallout`
- **描述**: This callout gives the application the opportunity to evaluate the StbM_TimeBaseStatus.
Returns E_OK -> FvM will use the time stamp.
Retruns E_NOT_OK -> FvM will not provide a freshness value to the SecOC.

##### 2. FvMGeneration

**容器属性**:

- **UUID**: `5ec99edb-38b4-4669-b91a-a479a09ed2c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FvMGeneration`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

Contains the generation configuration parameters of the module FvM.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. FvMOutOfBoundsWriteSanitizer

- **UUID**: `8d908168-2427-443a-bd62-a2a225ba478b`
- **参数名**: `FvMOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. FvMOutOfBoundsReadSanitizer

- **UUID**: `9920f984-fca6-49b9-8638-11eb2d4a91e9`
- **参数名**: `FvMOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. FvMShortSymbols

- **UUID**: `75bbd788-1a3d-4245-bc7e-0d4477adc9b9`
- **参数名**: `FvMShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 4. FvMInterfacesForDeactivatedData

- **UUID**: `05fa8531-0b77-40c9-9853-5a33804ec704`
- **参数名**: `FvMInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 5. FvMReferringKeysInComments

- **UUID**: `3eba54b2-18af-45a0-88dd-b5c4f6ed4f65`
- **参数名**: `FvMReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

####### ENUMERATION 类型参数

######## 1. FvMOutOfBoundsWriteProtectionStrategy

- **UUID**: `273d4fdc-4f07-4c88-81b3-32c385689d1d`
- **参数名**: `FvMOutOfBoundsWriteProtectionStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `NONE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NONE` (来源: Vector Informatik)
  - `INDEX_SATURATION` (来源: Vector Informatik)
  - `INDEX_CHECKING` (来源: Vector Informatik)
- **描述**: This parameter is used to configure a strategy to protect the code to write out of bounds.

NONE: no protection strategy is generated in the data access.
INDEX_SATURATION: arrays are blown up and the data access index is saturated by an appropriate mask. The advantage is the speed of the data access, but own data elements at other indexes of the same variable can be overridden.
INDEX_CHECKING: the data access index is validated by a runtime check. The advantage is that values are never written to incorrect indexes of the data access.

##### 3. FvMTimeBasedOption

**容器属性**:

- **UUID**: `ea178bb5-f14a-46b1-927c-69b7f1be689a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FvMTimeBasedOption`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

Container to configure a timebase option. 
The parameters SecOCFreshnessValueLength, SecOCFreshnessValueTxLength and SecOCAuthenticationVerifyAttempts of the related SecOC(Rx|Tx)PduProcessing are used by the FvM for this option.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. FvMTimeBasedOptionId

- **UUID**: `f52c8d0d-2dbc-4697-a4d9-303a2e7cca8d`
- **参数名**: `FvMTimeBasedOptionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **描述**: Time Based Option Id. To use this option with a SecOC(Rx|Tx)PduProcessing the SecOCFreshnessValueId must match this Id.

######## 2. FvMNanosecondsBitSize

- **UUID**: `405b755b-1043-4893-93ba-a34d57d77037`
- **参数名**: `FvMNanosecondsBitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..30]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Number of nanoseconds bits that are transmitted on the bus (TFV) and are used as nanoseconds part of the freshness value (FV). The number of nanoseconds bits is always the same for the truncated freshness value and the freshness value.

######## 3. FvMSecondsBitSize

- **UUID**: `2ce8ac9b-c5f0-4ee0-872f-0dfd37009e96`
- **参数名**: `FvMSecondsBitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Number of seconds bits that are used as seconds part of the freshness value (FV).

######## 4. FvMTruncatedSecondsBitSize

- **UUID**: `2b08bfe6-6815-4088-98a8-bae4133d4eca`
- **参数名**: `FvMTruncatedSecondsBitSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **取值范围**: [0..32]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Number of seconds bits that are transmitted on the bus (TFV).

######## 5. FvMRxAcceptanceWindow

- **UUID**: `c1af09c2-8422-44e8-a66f-2cf9fdc0232f`
- **参数名**: `FvMRxAcceptanceWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1000000000`
- **取值范围**: [0..4294967295]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: A tolerant time window shall be defined as RX Acceptance Window.

The RX Acceptance Window shall be determined based on the worst-case message latency (i.e. procecssing and transmission time) and synchronized Local Time difference. The acceptance window shall be large enough for legitimate fresh messages to be accepted correctly by the receiver, while it shall be small enough to detect replayed messages. Depending on the use case requirement of Acceptance Window size, tuning may be required to find out the best and minimum Acceptance Window.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FvMStbMTimeBaseRef

- **UUID**: `a2e87476-2d5e-4847-bfd2-4ce0b7bf768a`
- **引用名**: `FvMStbMTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to the StbM Time Base.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **FvM**

##### BSW-IMPLEMENTATION 类型元素

1. **FvM_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **FvM_Pre**
2. **FvM_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. FvM_Impl

- **UUID**: `45dd709f-875d-4188-b40c-1e76f7e7dee9`
- **实现名称**: `FvM_Impl`
- **编程语言**: C
- **软件版本**: 1.02.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.00
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. FvM_Pre

- **UUID**: `3af69110-9a7e-48c4-8213-48576e76741c`
- **配置名称**: `FvM_Pre`
- **定义引用**: `/MICROSAR/FvM`

### 2. FvM_Rec

- **UUID**: `bac3363c-d709-4479-bd5c-38e51322a807`
- **配置名称**: `FvM_Rec`
- **定义引用**: `/MICROSAR/FvM`
