# StbM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:59

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [StbM](#stbm)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. StbM

#### 基本信息

- **UUID**: `ECUC:506d0671-efed-4c60-bbf4-1a8c714a49ce`
- **模块名称**: `StbM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. StbMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4e91aaba-6482-4ff6-9b4a-5d3dcdb8b212`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `StbMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. STBM_E_INIT_FAILED

- **UUID**: `ECUC:67c11e8b-b684-48fe-b486-ce66edff1d63`
- **引用名**: `STBM_E_INIT_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "StbM initialization failed" has occured.

######## 2. STBM_E_INTEGRITY_FAILED

- **UUID**: `ECUC:45e96b1f-dad2-454a-9167-d23d288f8e39`
- **引用名**: `STBM_E_INTEGRITY_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "API request integrity failed" has occured.

######## 3. STBM_E_REQ_FAILED

- **UUID**: `ECUC:2104c443-c866-40d3-97d3-40c2daf55b60`
- **引用名**: `STBM_E_REQ_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "API request failed" has occured.

##### 2. StbMGeneral

**容器属性**:

- **UUID**: `ECUC:e3062823-830e-401e-ab3f-102908ca5111`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `StbMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds the general parameters of the Synchronized Time-base Manager

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. StbMTickTypeRange

- **UUID**: `ECUC:d2a34989-1c6b-4ba2-8a76-3ca07b924f2f`
- **参数名**: `StbMTickTypeRange`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the upper range of the type "StbM_TickType".

####### BOOLEAN 类型参数

######## 1. StbMAbsoluteTimeApi

- **UUID**: `ECUC:b01aba8a-dd01-49f2-82f2-b266a7909b4e`
- **参数名**: `StbMAbsoluteTimeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables the StbM_GetAbsoluteTime API.

######## 2. StbMDevErrorDetect

- **UUID**: `ECUC:7a01b1fa-4807-49ad-84ba-511286993060`
- **参数名**: `StbMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switch for enabling the development error detection.

######## 3. StbMVersionInfo

- **UUID**: `ECUC:16c0bfdf-bfa8-4261-b458-2efa197b30d0`
- **参数名**: `StbMVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the version information API (StbM_GetVersionInfo). True: version information API activated False: version information API deactivated.

##### 3. StbMSynchronizedTimeBase

**容器属性**:

- **UUID**: `ECUC:0eb5422e-e6ba-4303-8c41-1f56ad5d2f52`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `StbMSynchronizedTimeBase`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Synchronized time.base collects the information about a specific time-base provider within the system.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. StbMSynchronizedTimeBaseIdentifier

- **UUID**: `ECUC:3f37a751-19db-46c2-8fe8-727675c83547`
- **参数名**: `StbMSynchronizedTimeBaseIdentifier`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identification of a synchronized time-base via a unique identifier.

####### FUNCTION-NAME 类型参数

######## 1. StbMGlobalTimeProviderCallout

- **UUID**: `ECUC:10f0fea7-0cd4-4d0c-ac63-939652db3a4b`
- **参数名**: `StbMGlobalTimeProviderCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the time-base specific callout routine which shall be invoked by the StbM for gathering the current time-base value.

######## 2. StbMSyncStateProviderCallout

- **UUID**: `ECUC:cae3a69b-05bb-4cbb-9e59-5cc7c2f272ca`
- **参数名**: `StbMSyncStateProviderCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the time-base specific callout routine which shall be invoked by the StbM for gathering the current time-base status.

######## 3. StbMTickDurationProviderCallout

- **UUID**: `ECUC:e82e1513-825a-444b-8111-bc0cf61715ad`
- **参数名**: `StbMTickDurationProviderCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the time-base specific callout routine which shall be invoked by the StbM for gathering the current time-base tick duration.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. StbMLocalTimeRef

- **UUID**: `ECUC:9049f989-691f-409a-906d-e3ddffe934fa`
- **引用名**: `StbMLocalTimeRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional sub container in case a local time shall be accessed.

####### FOREIGN-REFERENCE 类型引用

######## 1. StbMFlexRayClusterRef

- **UUID**: `ECUC:fe2acf49-59c8-452b-8a79-c77027ae248e`
- **引用名**: `StbMFlexRayClusterRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: FLEXRAY-CLUSTER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the FlexRay cluster.

######## 2. StbMTtcanClusterRef

- **UUID**: `ECUC:0de45989-4c3e-4f5b-8e8f-499da82b05ff`
- **引用名**: `StbMTtcanClusterRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [0..1]
- **目标类型**: TTCAN-CLUSTER
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the Ttcan cluster.

##### 4. StbMTriggeredCustomer

**容器属性**:

- **UUID**: `ECUC:19e45c71-41c9-4253-a241-102f47f74b40`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `StbMTriggeredCustomer`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The triggered customer is directliy triggered by the Synchronized Time-base Manager by getting synchronized with the current (global) definition of time and passage of time.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. StbMTriggeredCustomerPeriod

- **UUID**: `ECUC:66300845-e1f9-4af6-be9e-6bd32cd2e858`
- **参数名**: `StbMTriggeredCustomerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The triggering period of the triggered customer, called by the StbM_MainFunction.

####### BOOLEAN 类型参数

######## 1. StbMTriggerInSyncState

- **UUID**: `ECUC:bcefeab6-eb5c-45f9-a320-c42e7ec1391d`
- **参数名**: `StbMTriggerInSyncState`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the triggering of the customer in case the related time-base (StbmSynchronizedTimeBaseRef) is not synchronized.

####### FUNCTION-NAME 类型参数

######## 1. StbMGlobalTimeCustomerCallback

- **UUID**: `ECUC:f0cb5415-8f6b-46a2-853a-10e02454e451`
- **参数名**: `StbMGlobalTimeCustomerCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the customer specific call-back routine which shall be invoked by the StbM periodically for time value propagation.

######## 2. StbMSyncStateCustomerCallback

- **UUID**: `ECUC:c1011a54-219e-440e-9002-fdf7b0d4c30f`
- **参数名**: `StbMSyncStateCustomerCallback`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Entry address of the customer specific call-back routine which shall be invoked by the StbM when state changes occur.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. StbMOSScheduleTableRef

- **UUID**: `ECUC:489979ba-a412-4da4-a60c-363cf7aec241`
- **引用名**: `StbMOSScheduleTableRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `OsScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to synchronized OS ScheduleTables.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. StbMSynchronizedTimeBaseRef

- **UUID**: `ECUC:265babaa-6c72-4d8f-b6fe-f4cd7ac08b90`
- **引用名**: `StbMSynchronizedTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Mandatory reference to the required synchronized time-base.

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

1. **StbM**
