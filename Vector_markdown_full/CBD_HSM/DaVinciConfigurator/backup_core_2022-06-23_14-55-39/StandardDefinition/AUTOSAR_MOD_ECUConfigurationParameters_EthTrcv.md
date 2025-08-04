# EthTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthTrcv](#ethtrcv)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthTrcv

#### 基本信息

- **UUID**: `ECUC:8a2137e1-bc21-4205-904d-0ffa23a64aee`
- **模块名称**: `EthTrcv`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of Ethernet Transceiver Driver module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. EthTrcvConfigSet

**容器属性**:

- **UUID**: `ECUC:9ae2997a-58f0-41bb-9d5e-0ca61818ef46`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

All underlying parameters may be part of a multiple configuration set.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. EthTrcvConfig

**容器属性**:

- **UUID**: `ECUC:d73b4a97-6573-48c2-9220-27f3cbd1c8b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual transceiver

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvCtrlIdx

- **UUID**: `ECUC:a9f1668e-9b43-4f20-8336-f4620d06cb77`
- **参数名**: `EthTrcvCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the controller used for MII access to the transceiver

########## 2. EthTrcvIdx

- **UUID**: `ECUC:263fe8ad-020a-41f7-84a2-83f5c4c9183c`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the instance ID of the configured transceiver.

########## 3. EthTrcvMiiIdx

- **UUID**: `ECUC:44681cf8-9a5a-481c-a8a8-6d3689cd8c16`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the transceiver index used for MII access to the transceiver

######### BOOLEAN 类型参数

########## 1. EthTrcvAutoNegotiationEnabled

- **UUID**: `ECUC:90e21e15-d837-4125-9d89-59ecb4250959`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the Ethernet transceiver speed.

######### ENUMERATION 类型参数

########## 1. EthTrcvDuplexMode

- **UUID**: `ECUC:333302ac-659a-4f79-a5c8-db6bbb2be7f6`
- **参数名**: `EthTrcvDuplexMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHTRCV_DUPLEX_MODE_FULL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_DUPLEX_MODE_HALF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the duplex mode of the Ethernet transceiver link if Auto-Negotiation is disabled. This parameter is ignored if Auto-Negotiation is enabled.

########## 2. EthTrcvSpeed

- **UUID**: `ECUC:590693dd-4179-4283-b0c4-5ce0e3df301c`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the speed of the Ethernet transceiver link in [MBit/s]. If AutoNegotiation is enabled this is the maximum speed advertised for Auto-Negotiation.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:10b3c818-b338-4fd9-a41d-ea351fb84cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ETHTRCV_E_ACCESS

- **UUID**: `ECUC:a5dcc018-60fd-4aeb-9e03-8206f2fc7688`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Transceiver access failed" has occurred.

####### 2. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:10b3c818-b338-4fd9-a41d-ea351fb84cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `ECUC:a5dcc018-60fd-4aeb-9e03-8206f2fc7688`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Transceiver access failed" has occurred.

##### 2. EthTrcvConfig

**容器属性**:

- **UUID**: `ECUC:d73b4a97-6573-48c2-9220-27f3cbd1c8b9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual transceiver

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvCtrlIdx

- **UUID**: `ECUC:a9f1668e-9b43-4f20-8336-f4620d06cb77`
- **参数名**: `EthTrcvCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the controller used for MII access to the transceiver

######## 2. EthTrcvIdx

- **UUID**: `ECUC:263fe8ad-020a-41f7-84a2-83f5c4c9183c`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the instance ID of the configured transceiver.

######## 3. EthTrcvMiiIdx

- **UUID**: `ECUC:44681cf8-9a5a-481c-a8a8-6d3689cd8c16`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the transceiver index used for MII access to the transceiver

####### BOOLEAN 类型参数

######## 1. EthTrcvAutoNegotiationEnabled

- **UUID**: `ECUC:90e21e15-d837-4125-9d89-59ecb4250959`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the Ethernet transceiver speed.

####### ENUMERATION 类型参数

######## 1. EthTrcvDuplexMode

- **UUID**: `ECUC:333302ac-659a-4f79-a5c8-db6bbb2be7f6`
- **参数名**: `EthTrcvDuplexMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ETHTRCV_DUPLEX_MODE_FULL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_DUPLEX_MODE_HALF` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the duplex mode of the Ethernet transceiver link if Auto-Negotiation is disabled. This parameter is ignored if Auto-Negotiation is enabled.

######## 2. EthTrcvSpeed

- **UUID**: `ECUC:590693dd-4179-4283-b0c4-5ce0e3df301c`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the speed of the Ethernet transceiver link in [MBit/s]. If AutoNegotiation is enabled this is the maximum speed advertised for Auto-Negotiation.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:10b3c818-b338-4fd9-a41d-ea351fb84cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `ECUC:a5dcc018-60fd-4aeb-9e03-8206f2fc7688`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Transceiver access failed" has occurred.

##### 3. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:10b3c818-b338-4fd9-a41d-ea351fb84cb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHTRCV_E_ACCESS

- **UUID**: `ECUC:a5dcc018-60fd-4aeb-9e03-8206f2fc7688`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Transceiver access failed" has occurred.

##### 4. EthTrcvGeneral

**容器属性**:

- **UUID**: `ECUC:03f52c10-8440-4280-94f9-f2c30bc12ef9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration of Ethernet Transceiver Driver module

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvIndex

- **UUID**: `ECUC:a09d571b-f281-410f-9854-ab60d9e99820`
- **参数名**: `EthTrcvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. EthTrcvMaxTrcvsSupported

- **UUID**: `ECUC:f912f21a-b10e-40c9-b18e-1827e6835c2c`
- **参数名**: `EthTrcvMaxTrcvsSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE

####### BOOLEAN 类型参数

######## 1. EthTrcvDevErrorDetect

- **UUID**: `ECUC:2b1fefe7-0a85-4d66-b9b0-1967fcf3150d`
- **参数名**: `EthTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables development error detection

######## 2. EthTrcvGetBaudRateApi

- **UUID**: `ECUC:94c93620-cb83-4164-a9cc-99e7ef6fec09`
- **参数名**: `EthTrcvGetBaudRateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetBaudRate API

######## 3. EthTrcvGetDuplexModeApi

- **UUID**: `ECUC:c507c2fa-9b22-47bc-9dd8-c20bcb67303f`
- **参数名**: `EthTrcvGetDuplexModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetDuplexMode API

######## 4. EthTrcvGetLinkStateApi

- **UUID**: `ECUC:78915de9-b681-473c-bca0-3a774a77cc61`
- **参数名**: `EthTrcvGetLinkStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetLinkState API

######## 5. EthTrcvGetTransceiverModeApi

- **UUID**: `ECUC:3ef394b1-05e6-4e5c-8c27-6ff875c95e3f`
- **参数名**: `EthTrcvGetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetTransceiverMode API

######## 6. EthTrcvSetTransceiverModeApi

- **UUID**: `ECUC:d3a5ce17-1c57-48b3-bfa6-29ff7ce4b14e`
- **参数名**: `EthTrcvSetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_SetTransceiverMode API

######## 7. EthTrcvStartAutoNegotiationApi

- **UUID**: `ECUC:255ab38d-b416-4252-9f2c-74cbc6e19fb1`
- **参数名**: `EthTrcvStartAutoNegotiationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_StartAutoNegotiation API

######## 8. EthTrcvVersionInfoApi

- **UUID**: `ECUC:b5e403a5-ecce-425e-b641-5f1de9a2b30a`
- **参数名**: `EthTrcvVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API

######## 9. EthTrcvVersionInfoApiMacro

- **UUID**: `ECUC:56d5fcd3-0662-4ee5-bbbc-f15a5edb0f95`
- **参数名**: `EthTrcvVersionInfoApiMacro`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API macro implementation

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

1. **EthTrcv**
