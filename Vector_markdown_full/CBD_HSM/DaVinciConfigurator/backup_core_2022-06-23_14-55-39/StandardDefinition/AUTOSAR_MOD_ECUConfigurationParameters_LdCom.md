# LdCom - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:24

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LdCom](#ldcom)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LdCom

#### 基本信息

- **UUID**: `ECUC:f37b1fb2-3601-4250-bb03-e60b1049e8eb`
- **模块名称**: `LdCom`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD-SELECTABLE
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the AUTOSAR LdCom module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. LdComGeneral

**容器属性**:

- **UUID**: `e142d6ea-69e7-4d37-9426-46faa8145b84`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the general configuration parameters of the AUTOSAR LdCom module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. LdComDevErrorDetect

- **UUID**: `d749b603-bd69-4eea-97ee-35c569dbcf94`
- **参数名**: `LdComDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If 'Development Error Detection' is enabled, all development errors are reported to the Development Error Tracer (DET). The errors are described in the technical reference.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. LdComVersionInfoApi

- **UUID**: `dc6d6589-e06d-4c2a-9f69-88adf1420c92`
- **参数名**: `LdComVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Activate/Deactivate the version information API (LdCom_GetVersionInfo).

Activate/Deactivate the version information API LdCom_GetVersionInfo().
- True: version information API activated
- False: version information API deactivated

####### STRING 类型参数

######## 1. LdComUserConfigFile

- **UUID**: `28b36950-464d-4a21-99fb-c6dfbb7d71aa`
- **参数名**: `LdComUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LdComGeneration

**容器属性**:

- **UUID**: `8c969514-9d47-420f-beaa-f7d9d165793d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module LdCom.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. LdComReduceBoolDataByNumericalComparisonThreshold

- **UUID**: `07d40547-9b44-4fb5-b6d1-28ddb59f36d8`
- **参数名**: `LdComReduceBoolDataByNumericalComparisonThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using numerical comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

########## 2. LdComReduceBoolDataByNumericalRelationThreshold

- **UUID**: `ac822960-d169-4ed4-8898-311c4cf5c498`
- **参数名**: `LdComReduceBoolDataByNumericalRelationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using relational comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

######### BOOLEAN 类型参数

########## 1. LdComReduceConstantData2Define

- **UUID**: `f9148797-3fb9-4ed5-8fd7-0e2eda19c0b1`
- **参数名**: `LdComReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

########## 2. LdComReduceDataByStreaming

- **UUID**: `33e2ec1f-f3f5-411b-af80-66db322fb3e9`
- **参数名**: `LdComReduceDataByStreaming`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE ROM data into a data type dependent stream.

TRUE: generated const data is packed into a data type dependent stream.
Code: no change expected.
RAM: no change expected.
ROM: configuration dependent smaller than with FALSE.
Runtime: no change expected.

FALSE: generated const data is not packed into a data type dependent stream.

########## 3. LdComOutOfBoundsReadSanitizer

- **UUID**: `29eccc22-89af-471f-8908-04be19acc5c8`
- **参数名**: `LdComOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 4. LdComShortSymbols

- **UUID**: `4611d007-41d7-42d9-85c4-4bf02bd5dac2`
- **参数名**: `LdComShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

########## 5. LdComInterfacesForDeactivatedData

- **UUID**: `737f2624-e769-46a0-99e2-2be7a848b329`
- **参数名**: `LdComInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

########## 6. LdComReferringKeysInComments

- **UUID**: `a1b45fc0-5ed1-4e27-896e-5d6257f3c56a`
- **参数名**: `LdComReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

##### 2. LdComGeneration

**容器属性**:

- **UUID**: `8c969514-9d47-420f-beaa-f7d9d165793d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module LdCom.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. LdComReduceBoolDataByNumericalComparisonThreshold

- **UUID**: `07d40547-9b44-4fb5-b6d1-28ddb59f36d8`
- **参数名**: `LdComReduceBoolDataByNumericalComparisonThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using numerical comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

######## 2. LdComReduceBoolDataByNumericalRelationThreshold

- **UUID**: `ac822960-d169-4ed4-8898-311c4cf5c498`
- **参数名**: `LdComReduceBoolDataByNumericalRelationThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to compress boolean CONFIG-CLASS PRE-COMPILE ROM data by using relational comparison with other ROM data.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the operation in the data access.

####### BOOLEAN 类型参数

######## 1. LdComReduceConstantData2Define

- **UUID**: `f9148797-3fb9-4ed5-8fd7-0e2eda19c0b1`
- **参数名**: `LdComReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

######## 2. LdComReduceDataByStreaming

- **UUID**: `33e2ec1f-f3f5-411b-af80-66db322fb3e9`
- **参数名**: `LdComReduceDataByStreaming`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to pack generated CONFIG-CLASS PRE-COMPILE ROM data into a data type dependent stream.

TRUE: generated const data is packed into a data type dependent stream.
Code: no change expected.
RAM: no change expected.
ROM: configuration dependent smaller than with FALSE.
Runtime: no change expected.

FALSE: generated const data is not packed into a data type dependent stream.

######## 3. LdComOutOfBoundsReadSanitizer

- **UUID**: `29eccc22-89af-471f-8908-04be19acc5c8`
- **参数名**: `LdComOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 4. LdComShortSymbols

- **UUID**: `4611d007-41d7-42d9-85c4-4bf02bd5dac2`
- **参数名**: `LdComShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 5. LdComInterfacesForDeactivatedData

- **UUID**: `737f2624-e769-46a0-99e2-2be7a848b329`
- **参数名**: `LdComInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 6. LdComReferringKeysInComments

- **UUID**: `a1b45fc0-5ed1-4e27-896e-5d6257f3c56a`
- **参数名**: `LdComReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

##### 3. LdComConfig

**容器属性**:

- **UUID**: `d31ac675-d820-4baa-987f-9ce82857a632`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComConfig`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR LdCom module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LdComIPdu

**容器属性**:

- **UUID**: `2329f7d3-56aa-4afc-974b-9fa63c07465e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Contains the configuration parameters of the IPdu inside LdCom.

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. LdComHandleId

- **UUID**: `fb9715c7-982c-4cc3-8965-a14288a38f38`
- **参数名**: `LdComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The numerical value used as the ID of this I-PDU. This ID is used by Rte to invoke LdCom. A corresponding shortName is created, which is used for the invocations of the Rte. The same ID is used for invocations by PduR.

######### ENUMERATION 类型参数

########## 1. LdComApiType

- **UUID**: `554d7289-7f79-4749-8b01-71699d7d01d3`
- **参数名**: `LdComApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LDCOM_IF`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LDCOM_IF` (来源: Vector Informatik)
  - `LDCOM_TP` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the desired API Type of the I-PDU.

IF: indicates that the I-PDU is sent/received via interface API.
TP: indicates that the I-PDU is send/received via transport protocol API.

########## 2. LdComIPduDirection

- **UUID**: `aad9d36e-c484-4241-b323-4418247a39ee`
- **参数名**: `LdComIPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LDCOM_RECEIVE` (来源: Vector Informatik)
  - `LDCOM_SEND` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The direction defines if this I-PDU, and therefore the contributing signal, shall be sent or received.

######### FUNCTION-NAME 类型参数

########## 1. LdComRxIndication

- **UUID**: `a8011ff4-603b-4fb9-bbd0-395c9b0b4019`
- **参数名**: `LdComRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkRxIndication callback function to be called.

########## 2. LdComRxStartOfReception

- **UUID**: `25fe4b12-6cf4-422b-98c2-f231bd0ed227`
- **参数名**: `LdComRxStartOfReception`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkStartOfReception callback function to be called.

########## 3. LdComRxCopyRxData

- **UUID**: `6e478bf5-bf71-421d-9910-05213a0fd9a8`
- **参数名**: `LdComRxCopyRxData`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkCopyRxData callback function to be called.

########## 4. LdComTpRxIndication

- **UUID**: `9a966c5e-b357-4e06-a25d-2cd8c5719645`
- **参数名**: `LdComTpRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkTpRxIndication callback function to be called.

########## 5. LdComTxTriggerTransmit

- **UUID**: `c6d9af97-9d39-4456-94cc-da4fe223f3e0`
- **参数名**: `LdComTxTriggerTransmit`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkTriggerTransmit callback function to be called.

########## 6. LdComTxConfirmation

- **UUID**: `ca0ad87e-020c-4984-8b41-9f01ebb9ac6d`
- **参数名**: `LdComTxConfirmation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkTxConfirmation callback function to be called.

########## 7. LdComTxCopyTxData

- **UUID**: `dc6c8fc4-bfb9-4bf7-b7bc-023ed6c43093`
- **参数名**: `LdComTxCopyTxData`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkCopyTxData callback function to be called.

########## 8. LdComTpTxConfirmation

- **UUID**: `57b9a652-c194-4449-b559-3ccb4be2f23c`
- **参数名**: `LdComTpTxConfirmation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only on sender side: Name of Rte_LdComCbkTpTxConfirmation callback function to be called.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LdComPduRef

- **UUID**: `f1320b61-b4b4-4020-a0e2-e79cdcc32c3c`
- **引用名**: `LdComPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU.

######### FOREIGN-REFERENCE 类型引用

########## 1. LdComSystemTemplateSystemSignalRef

- **UUID**: `760ae3de-90ef-473d-9a71-cd631e0fa276`
- **引用名**: `LdComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this LdCom signal represents.

##### 4. LdComIPdu

**容器属性**:

- **UUID**: `2329f7d3-56aa-4afc-974b-9fa63c07465e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LdComIPdu`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Contains the configuration parameters of the IPdu inside LdCom.

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. LdComHandleId

- **UUID**: `fb9715c7-982c-4cc3-8965-a14288a38f38`
- **参数名**: `LdComHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The numerical value used as the ID of this I-PDU. This ID is used by Rte to invoke LdCom. A corresponding shortName is created, which is used for the invocations of the Rte. The same ID is used for invocations by PduR.

####### ENUMERATION 类型参数

######## 1. LdComApiType

- **UUID**: `554d7289-7f79-4749-8b01-71699d7d01d3`
- **参数名**: `LdComApiType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `LDCOM_IF`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LDCOM_IF` (来源: Vector Informatik)
  - `LDCOM_TP` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the desired API Type of the I-PDU.

IF: indicates that the I-PDU is sent/received via interface API.
TP: indicates that the I-PDU is send/received via transport protocol API.

######## 2. LdComIPduDirection

- **UUID**: `aad9d36e-c484-4241-b323-4418247a39ee`
- **参数名**: `LdComIPduDirection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `LDCOM_RECEIVE` (来源: Vector Informatik)
  - `LDCOM_SEND` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The direction defines if this I-PDU, and therefore the contributing signal, shall be sent or received.

####### FUNCTION-NAME 类型参数

######## 1. LdComRxIndication

- **UUID**: `a8011ff4-603b-4fb9-bbd0-395c9b0b4019`
- **参数名**: `LdComRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkRxIndication callback function to be called.

######## 2. LdComRxStartOfReception

- **UUID**: `25fe4b12-6cf4-422b-98c2-f231bd0ed227`
- **参数名**: `LdComRxStartOfReception`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkStartOfReception callback function to be called.

######## 3. LdComRxCopyRxData

- **UUID**: `6e478bf5-bf71-421d-9910-05213a0fd9a8`
- **参数名**: `LdComRxCopyRxData`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkCopyRxData callback function to be called.

######## 4. LdComTpRxIndication

- **UUID**: `9a966c5e-b357-4e06-a25d-2cd8c5719645`
- **参数名**: `LdComTpRxIndication`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on receiver side: Name of Rte_LdComCbkTpRxIndication callback function to be called.

######## 5. LdComTxTriggerTransmit

- **UUID**: `c6d9af97-9d39-4456-94cc-da4fe223f3e0`
- **参数名**: `LdComTxTriggerTransmit`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkTriggerTransmit callback function to be called.

######## 6. LdComTxConfirmation

- **UUID**: `ca0ad87e-020c-4984-8b41-9f01ebb9ac6d`
- **参数名**: `LdComTxConfirmation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkTxConfirmation callback function to be called.

######## 7. LdComTxCopyTxData

- **UUID**: `dc6c8fc4-bfb9-4bf7-b7bc-023ed6c43093`
- **参数名**: `LdComTxCopyTxData`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Only on sender side: Name of Rte_LdComCbkCopyTxData callback function to be called.

######## 8. LdComTpTxConfirmation

- **UUID**: `57b9a652-c194-4449-b559-3ccb4be2f23c`
- **参数名**: `LdComTpTxConfirmation`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Only on sender side: Name of Rte_LdComCbkTpTxConfirmation callback function to be called.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. LdComPduRef

- **UUID**: `f1320b61-b4b4-4020-a0e2-e79cdcc32c3c`
- **引用名**: `LdComPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the global PDU.

####### FOREIGN-REFERENCE 类型引用

######## 1. LdComSystemTemplateSystemSignalRef

- **UUID**: `760ae3de-90ef-473d-9a71-cd631e0fa276`
- **引用名**: `LdComSystemTemplateSystemSignalRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: I-SIGNAL-TO-I-PDU-MAPPING
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ISignalToIPduMapping that contains a reference to the ISignal (System Template) which this LdCom signal represents.

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

1. **LdCom**
