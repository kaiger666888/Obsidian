# EthSM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:55

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthSM](#ethsm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthSM

#### 基本信息

- **UUID**: `e1914d66-8fd8-4792-9f2b-5874cb6e9996`
- **模块名称**: `EthSM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Ethernet State Manager (EthSM). The EthSM realizes a software layer between the Communication Manager (ComM) and the Ethernet Interface (EthIf). The EthSM handles start-up and shutdown of the communication of an Ethernet network.
#Ethernet #State #StateManager #ModeManagement #Startup #Shutdown #Wakeup
#AUTOSAR

#### 版本历史

共有 **11** 个版本记录：

##### 1. 版本 3.00.00

- **发布日期**: 2012-08-01
- **发布者**: vismha

**变更内容**:

##### 2. 版本 3.00.00

- **状态**: beta
- **发布日期**: 2013-10-22T01:41:29+02:00
- **发布者**: vismha

**变更内容**:

##### 3. 版本 3.00.01

- **发布日期**: 2014-07-10T11:21:30+02:00
- **发布者**: vismha

**变更内容**:

##### 4. 版本 3.01.00

- **发布日期**: 2014-07-15T09:56:17+02:00
- **发布者**: vismha

**变更内容**:

##### 5. 版本 3.01.01

- **发布日期**: 2015-04-29T07:56:52+02:00
- **发布者**: vismha

**变更内容**:

##### 6. 版本 3.01.02

- **发布日期**: 2015-11-06T04:34:52+01:00
- **发布者**: vismha

**变更内容**:

##### 7. 版本 4.00.00

- **状态**: released
- **发布日期**: 2018-04-09T02:00:48+02:00
- **发布者**: vischh

**变更内容**:

##### 8. 版本 5.00.00

- **状态**: released
- **发布日期**: 2022-02-01T13:03:29+01:00
- **发布者**: visvjn

**变更内容**:

##### 9. 版本 5.00.01

- **状态**: released
- **发布日期**: 2022-02-16T16:28:38+01:00
- **发布者**: visvjn

**变更内容**:

##### 10. 版本 5.00.02

- **状态**: released
- **发布日期**: 2023-03-14T16:53:54+01:00
- **发布者**: vischh

**变更内容**:

##### 11. 版本 6.00.00

- **状态**: released
- **发布日期**: 2024-05-02T09:28:30+02:00
- **发布者**: visuca

**变更内容**:

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. EthSMGeneral

**容器属性**:

- **UUID**: `56e0feab-1aa5-46bc-9b5c-2a1630cd8b17`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the EthSM.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. EthSMDevErrorDetect

- **UUID**: `f4b1bff6-5def-4f5a-b43e-2e76116de758`
- **参数名**: `EthSMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.

True: Development error detection is enabled.
False: Development error detection is disabeld.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. EthSMVersionInfoApi

- **UUID**: `dd747976-a692-4eac-82a7-dfc3b4c5b473`
- **参数名**: `EthSMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function EthSM_GetVersionInfo() to get major, minor and patch version information.

######## 3. EthSMEnableEthIfApiTimeout

- **UUID**: `c40d29e2-02fa-4d3e-b2ce-59bc98d8b83c`
- **参数名**: `EthSMEnableEthIfApiTimeout`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if a error handling for possibly unsuccessful calls to the EthIf APIs is actived.

false:
The error handling is disabled and the EthSM will call EthIf APIs endlessly every main function cycle until they return successfully.

true:
The error handling is enabled and the EthSM will call the EthIf APIs with a time gap specified by 'EthSMConfirmationTimeout' and as often as specified by 'EthSMMaxNumRetry'. (Both configurable Ethernet network-specific)

Error handling of unsuccessful calls will be as followed:

DET:
(only enabled if 'EthSMDevErrorDetect' is enabled)
EthSM will report the error ETHSM_E_ETHIF_TIMEOUT to DET by calling Det_ReportError.

DEM:
(only enabled if Ethernet network-specific DEM event 'ETHSM_E_TIMEOUT' is configured)
EthSM will report the error with the specific DEM event ID by calling Dem_ReportErrorStatus.

######## 4. EthSMSafeBswChecks

- **UUID**: `5b1d78a7-5abf-41d5-a922-3bb394a30839`
- **参数名**: `EthSMSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. EthSMMainFunctionPeriod

- **UUID**: `a3c7945a-6e3b-4e9a-aa03-8ec46be1264a`
- **参数名**: `EthSMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.02`
- **取值范围**: [0.005..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the period that the Main Function of the EthSM has to be triggered with.

####### STRING 类型参数

######## 1. EthSMUserConfigFile

- **UUID**: `49c7c99a-ab6b-4af5-96ac-3fad1b062a5a`
- **参数名**: `EthSMUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external file that will be included during generation to EthSM_Cfg.h.

The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with greate care!

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthSMGeneration

**容器属性**:

- **UUID**: `f7d4050b-133b-4c4f-a4d9-da4b0c42ef85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains parameters which have influence on the generation of the module.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. EthSMOutOfBoundsWriteSanitizer

- **UUID**: `9180b5bd-a139-41f8-93ae-7e5d6e9c5462`
- **参数名**: `EthSMOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 2. EthSMOutOfBoundsReadSanitizer

- **UUID**: `193dd0e1-46cc-4ce1-9af4-a37787709af6`
- **参数名**: `EthSMOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

########## 3. EthSMShortSymbols

- **UUID**: `9568f0b1-792e-4fcb-83ad-4e705dcac0f3`
- **参数名**: `EthSMShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

##### 2. EthSMGeneration

**容器属性**:

- **UUID**: `f7d4050b-133b-4c4f-a4d9-da4b0c42ef85`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains parameters which have influence on the generation of the module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. EthSMOutOfBoundsWriteSanitizer

- **UUID**: `9180b5bd-a139-41f8-93ae-7e5d6e9c5462`
- **参数名**: `EthSMOutOfBoundsWriteSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 2. EthSMOutOfBoundsReadSanitizer

- **UUID**: `193dd0e1-46cc-4ce1-9af4-a37787709af6`
- **参数名**: `EthSMOutOfBoundsReadSanitizer`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds read problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

######## 3. EthSMShortSymbols

- **UUID**: `9568f0b1-792e-4fcb-83ad-4e705dcac0f3`
- **参数名**: `EthSMShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

##### 3. EthSMNetwork

**容器属性**:

- **UUID**: `5210a71a-1bcc-407c-b1b9-46326c62ecf2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMNetwork`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the Ethernet network-specific parameters of each Ethernet network.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. EthSMMaxNumRetry

- **UUID**: `6355895e-672f-4def-a13b-cee7254b48e8`
- **参数名**: `EthSMMaxNumRetry`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the maximum number of retries for EthIf API calls.

One try to call the EthIf API successfully is done without taking the specified value into account.

For further information of EthIf API timeout handling please refere to the description of 'EthSMEnableEthIfApiTimeout'.

####### FLOAT 类型参数

######## 1. EthSMConfirmationTimeout

- **UUID**: `68aa6945-fa51-49aa-9d0d-a0bf94e1c00b`
- **参数名**: `EthSMConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.1`
- **取值范围**: [0.001..10]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifes the time gap between the retries of the calls to EthIf:
-EthIf_ControllerInit
-EthIf_TransceiverInit
-EthIf_SetControllerMode
-EthIf_SetTransceiverMode

For further information of EthIf API timeout handling please refere to the description of 'EthSMEnableEthIfApiTimeout'.

####### ENUMERATION 类型参数

######## 1. EthSMStackType

- **UUID**: `812e69c7-90ec-48cb-b6c2-a64e1bd0b7ec`
- **参数名**: `EthSMStackType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TcpIp`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TcpIp` (来源: Vector Informatik)
  - `Avb` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Parameter defines the communication stack using this Ethernet network.

TcpIp:

The Ethernet network is used by a TcpIp communication stack. The two-stage communication request for this network specified by AUTOSAR will be used.
The EthIf APIs are used to change activate/deactivate the Ethernet controller and transceiver and the TcpIp API is used to change the TcpIp mode.
Also the EthSM relies on the indications of the transceiver link and the TcpIp mode for state handling.

Avb:

The Ethernet network is used by a Avb communication stack. The two-stage communication request for this network specified by AUTOSAR will be tailored into a one-stage request.
The EthIf APIs are used to change activate/deactivate the Ethernet controller and transceiver. The TcpIp APIs aren't used anymore.
Also the EthSM only relies on the indications of the transceiver link for state handling.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthSMComMNetworkHandleRef

- **UUID**: `d07d2204-ee6a-401e-9149-645b4e8974a1`
- **引用名**: `EthSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a ComM channel representing this Ethernet network in ComM configuration.

######## 2. EthSMEthIfControllerRef

- **UUID**: `ea0847a2-4a45-44dd-a7e2-31712972cbdd`
- **引用名**: `EthSMEthIfControllerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a EthIfController which abstracts the underlying Ethernet controller and transceiver to be controlled.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthSMDemEventParameterRefs

**容器属性**:

- **UUID**: `afdf76a4-6b26-4c74-a996-1c8d94b4a8c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHSM_E_LINK_DOWN

- **UUID**: `03d7a0df-c7c6-464f-be5b-6c627a832ed4`
- **引用名**: `ETHSM_E_LINK_DOWN`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this Ethernet network.

The event will be reported in two situations:

1) Ethernet network is in STATE_ONLINE and loses transceiver link

The event will be reported to the DEM by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_FAILED.

2) Ethernet network is in STATE_ONHOLD and gains transceiver link

The event will be reported to the DEM by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_PASSED.

########## 2. ETHSM_E_TIMEOUT

- **UUID**: `f5d50caf-477d-411a-bcd4-3a2672449ffd`
- **引用名**: `ETHSM_E_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report a timeout of EthIf API calls.

The event will be reported to the DEM if the EthIf API error handling is processed by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_FAILED.

##### 4. EthSMDemEventParameterRefs

**容器属性**:

- **UUID**: `afdf76a4-6b26-4c74-a996-1c8d94b4a8c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHSM_E_LINK_DOWN

- **UUID**: `03d7a0df-c7c6-464f-be5b-6c627a832ed4`
- **引用名**: `ETHSM_E_LINK_DOWN`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this Ethernet network.

The event will be reported in two situations:

1) Ethernet network is in STATE_ONLINE and loses transceiver link

The event will be reported to the DEM by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_FAILED.

2) Ethernet network is in STATE_ONHOLD and gains transceiver link

The event will be reported to the DEM by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_PASSED.

######## 2. ETHSM_E_TIMEOUT

- **UUID**: `f5d50caf-477d-411a-bcd4-3a2672449ffd`
- **引用名**: `ETHSM_E_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report a timeout of EthIf API calls.

The event will be reported to the DEM if the EthIf API error handling is processed by calling Dem_ReportErrorStatus with the status DEM_EVENT_STATUS_FAILED.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **EthSM**

##### BSW-IMPLEMENTATION 类型元素

1. **EthSM_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **EthSM_Pre**
2. **EthSM_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. EthSM_Impl

- **UUID**: `14ed274d-8604-44d3-8079-226fc493758d`
- **实现名称**: `EthSM_Impl`
- **编程语言**: C
- **软件版本**: 6.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.01.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. EthSM_Pre

- **UUID**: `9423647c-c41a-4516-8b70-4d187e71fe3b`
- **配置名称**: `EthSM_Pre`
- **定义引用**: `/MICROSAR/EthSM`

### 2. EthSM_Rec

- **UUID**: `639ad405-41e5-44d0-9769-0c223d03cb1a`
- **配置名称**: `EthSM_Rec`
- **定义引用**: `/MICROSAR/EthSM`
