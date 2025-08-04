# Lin - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:52

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Lin](#lin)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Lin

#### 基本信息

- **UUID**: `ECUC:cce1bea0-f990-4c41-b8fd-2b0f0e590935`
- **模块名称**: `Lin`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Lin (LIN driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. LinGeneral

**容器属性**:

- **UUID**: `ECUC:1d543976-f649-42c3-b4ac-ad3abf68201a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the parameters related to each LIN Driver Unit.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinIndex

- **UUID**: `ECUC:6d8fcd10-4bde-4582-99fd-4e98b7c25839`
- **参数名**: `LinIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. LinTimeoutDuration

- **UUID**: `ECUC:4c279681-63d2-4125-b3a0-36aabd53153b`
- **参数名**: `LinTimeoutDuration`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum number of loops for blocking function until a timeout is raised in short term wait loops

####### BOOLEAN 类型参数

######## 1. LinDevErrorDetect

- **UUID**: `ECUC:6f7825c9-bce4-4f50-8643-1f8fcef24d80`
- **参数名**: `LinDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. LinVersionInfoApi

- **UUID**: `ECUC:03f6c9e0-e3b7-4907-84c0-a96e099b4431`
- **参数名**: `LinVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Lin_GetVersionInfo function ON or OFF.

##### 2. LinGlobalConfig

**容器属性**:

- **UUID**: `ECUC:5bf7d5c4-2ce3-45ef-9aa4-694ae888aef1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the global configuration parameter of the Lin driver. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exit once per configuration set.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. LinChannel

**容器属性**:

- **UUID**: `ECUC:5068d91d-ca0a-460f-9f6a-21f7ad18d591`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the LIN Controller(s).

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. LinChannelBaudRate

- **UUID**: `ECUC:16748716-3f59-4064-a8ef-ca1ab0b00deb`
- **参数名**: `LinChannelBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1000..20000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baud rate of the LIN channel

########## 2. LinChannelId

- **UUID**: `ECUC:c3ebc9ff-d623-4c49-ac91-241dec476a8d`
- **参数名**: `LinChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the LIN channel. Replaces LIN_CHANNEL_INDEX_NAME from the LIN SWS.

######### BOOLEAN 类型参数

########## 1. LinChannelWakeupSupport

- **UUID**: `ECUC:644aeda6-9c40-4e6d-945f-555f9c2b0c56`
- **参数名**: `LinChannelWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the LIN hardware channel supports wake up functionality

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinClockRef

- **UUID**: `ECUC:df926436-58ac-4912-beb2-b6a951d5f244`
- **引用名**: `LinClockRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the LIN clock source configuration, which is set in the MCU driver configuration.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinChannelEcuMWakeupSource

- **UUID**: `ECUC:c24ae6cb-a145-4c7d-a7e1-7493da1e0df8`
- **引用名**: `LinChannelEcuMWakeupSource`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the Wakeup Source for this controller as defined in the ECU State Manager.

####### 2. LinDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4d8e20c9-6d9d-4ed9-8556-977fd239ecbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LIN_E_TIMEOUT

- **UUID**: `ECUC:479d9631-3cd7-4995-ada9-6163ae75fd71`
- **引用名**: `LIN_E_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Timeout caused by hardware error" has occured. If the reference is not configured the error shall be reported as DET error.

##### 3. LinChannel

**容器属性**:

- **UUID**: `ECUC:5068d91d-ca0a-460f-9f6a-21f7ad18d591`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the LIN Controller(s).

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. LinChannelBaudRate

- **UUID**: `ECUC:16748716-3f59-4064-a8ef-ca1ab0b00deb`
- **参数名**: `LinChannelBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1000..20000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baud rate of the LIN channel

######## 2. LinChannelId

- **UUID**: `ECUC:c3ebc9ff-d623-4c49-ac91-241dec476a8d`
- **参数名**: `LinChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifies the LIN channel. Replaces LIN_CHANNEL_INDEX_NAME from the LIN SWS.

####### BOOLEAN 类型参数

######## 1. LinChannelWakeupSupport

- **UUID**: `ECUC:644aeda6-9c40-4e6d-945f-555f9c2b0c56`
- **参数名**: `LinChannelWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the LIN hardware channel supports wake up functionality

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. LinClockRef

- **UUID**: `ECUC:df926436-58ac-4912-beb2-b6a951d5f244`
- **引用名**: `LinClockRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the LIN clock source configuration, which is set in the MCU driver configuration.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinChannelEcuMWakeupSource

- **UUID**: `ECUC:c24ae6cb-a145-4c7d-a7e1-7493da1e0df8`
- **引用名**: `LinChannelEcuMWakeupSource`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the Wakeup Source for this controller as defined in the ECU State Manager.

##### 4. LinDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4d8e20c9-6d9d-4ed9-8556-977fd239ecbf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LIN_E_TIMEOUT

- **UUID**: `ECUC:479d9631-3cd7-4995-ada9-6163ae75fd71`
- **引用名**: `LIN_E_TIMEOUT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Timeout caused by hardware error" has occured. If the reference is not configured the error shall be reported as DET error.

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

1. **Lin**
