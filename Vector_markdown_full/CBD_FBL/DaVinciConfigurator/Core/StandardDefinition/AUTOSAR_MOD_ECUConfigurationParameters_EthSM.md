# EthSM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:43

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthSM](#ethsm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthSM

#### 基本信息

- **UUID**: `ECUC:6f8c16f8-2680-4ddd-9b38-31fd814152b8`
- **模块名称**: `EthSM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Ethernet State Manager

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **3** 个配置容器：

##### 1. EthSMGeneral

**容器属性**:

- **UUID**: `ECUC:78fcf290-0b0b-492a-af4e-69b20bc58c9f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the global parameter of the Ethernet State Manager.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. EthSMDevErrorDetect

- **UUID**: `ECUC:8d8442fe-424d-4bf4-b0b0-a6cc37dee29b`
- **参数名**: `EthSMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the development error detection and notification mechanism.

######## 2. EthSMDummyMode

- **UUID**: `ECUC:f081696f-77a7-4ebd-9df9-400a656ab75f`
- **参数名**: `EthSMDummyMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Disables the API to the EthIf. The API to the ComM is available but the functionality is deactivated. The function calls from the ComM will be answered with the return value E_OK.

######## 3. EthSMVersionInfoApi

- **UUID**: `ECUC:0cd3155a-3f2b-4ad8-bcc7-36205264a3f4`
- **参数名**: `EthSMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the version info API.

####### FLOAT 类型参数

######## 1. EthSMMainFunctionPeriod

- **UUID**: `ECUC:e46ee864-8ae6-4a07-8e2f-817073cbecb6`
- **参数名**: `EthSMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.005..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the period in seconds that the MainFunction has to be triggered with.

##### 2. EthSMNetwork

**容器属性**:

- **UUID**: `ECUC:b14ff5a3-8d2d-4f9b-aed4-508801a04f62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMNetwork`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Ethernet network-specific parameters of each Ethernet network. It also contains the controller and transceiver IDs assigned to a Ethernet network.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. EthSMConfirmationTimeout

- **UUID**: `ECUC:721b10c3-a34d-4b9c-8249-306c48c324fa`
- **参数名**: `EthSMConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Timeout in seconds for the calls to EthIf:

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthSMComMNetworkHandleRef

- **UUID**: `ECUC:90fd482d-e9f2-436b-8dd2-ca69eccc3407`
- **引用名**: `EthSMComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain Ethernet network. Reference to one of the network handles configured for the ComM.

######## 2. EthSMEthIfControllerRef

- **UUID**: `ECUC:ca206552-a24a-42d9-a7a4-222ecba045e6`
- **引用名**: `EthSMEthIfControllerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to EthIfCtrl container where a ETH controller and

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:afdeaabf-81fe-4291-b326-292ae18ea6ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHSM_E_LINK_DOWN

- **UUID**: `ECUC:402b4fad-2686-4096-a2fd-aeab95f3b91a`
- **引用名**: `ETHSM_E_LINK_DOWN`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this Eth network.

##### 3. EthSMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:afdeaabf-81fe-4291-b326-292ae18ea6ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthSMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHSM_E_LINK_DOWN

- **UUID**: `ECUC:402b4fad-2686-4096-a2fd-aeab95f3b91a`
- **引用名**: `ETHSM_E_LINK_DOWN`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report bus off errors for this Eth network.

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

1. **EthSM**
