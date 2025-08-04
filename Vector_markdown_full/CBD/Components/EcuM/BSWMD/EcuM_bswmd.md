# EcuM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:53

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EcuM](#ecum)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EcuM

#### 基本信息

- **UUID**: `7f8544a9-05a3-4644-99f1-7fc184ef23d0`
- **模块名称**: `EcuM`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-LOADABLE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Configuration of the ECU State Manager (EcuM) module. The EcuM manages the intialization and de-initialization of OS, SchM, BswM and other base SW modules. It is responisble for startup, shutdown, sleep modes and wakeup sources of the ECU.
#ModeManagement #Startup #Shutdown #Wakeup
#AUTOSAR #ServiceComponent

#### 版本历史

共有 **34** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2012-02-01
- **发布者**: visvjn

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2012-12-07T01:11:31+01:00
- **发布者**: visvjn

**变更内容**:

##### 3. 版本 1.01.00

- **状态**: released
- **发布日期**: 2013-03-21T01:37:34+01:00
- **发布者**: visvjn

**变更内容**:

##### 4. 版本 2.00.00

- **状态**: released
- **发布日期**: 2013-07-12T08:54:21+02:00
- **发布者**: visvjn

**变更内容**:

##### 5. 版本 2.00.01

- **状态**: released
- **发布日期**: 2013-12-10T02:33:24+01:00
- **发布者**: visvjn

**变更内容**:

##### 6. 版本 2.01.00

- **状态**: released
- **发布日期**: 2013-12-06T10:41:03+01:00
- **发布者**: visvjn

**变更内容**:

##### 7. 版本 3.00.00

- **状态**: released
- **发布日期**: 2013-12-06T10:41:03+01:00
- **发布者**: visvjn

**变更内容**:

##### 8. 版本 3.00.01

- **状态**: released
- **发布日期**: 2014-06-25T10:40:15+02:00
- **发布者**: visrpp

**变更内容**:

##### 9. 版本 4.00.00

- **状态**: released
- **发布日期**: 2014-07-04T10:51:11+02:00
- **发布者**: visvjn

**变更内容**:

##### 10. 版本 4.00.01

- **状态**: released
- **发布日期**: 2014-11-26T05:25:36+01:00
- **发布者**: visvjn

**变更内容**:

##### 11. 版本 4.01.00

- **状态**: released
- **发布日期**: 2015-01-22T01:59:19+01:00
- **发布者**: visvjn

**变更内容**:

##### 12. 版本 4.02.00

- **状态**: released
- **发布日期**: 2015-02-20T10:23:11+01:00
- **发布者**: visvjn

**变更内容**:

##### 13. 版本 5.00.00

- **状态**: released
- **发布日期**: 2015-03-19T02:12:16+01:00
- **发布者**: visvjn

**变更内容**:

##### 14. 版本 6.00.00

- **状态**: released
- **发布日期**: 2015-11-20T10:01:44+01:00
- **发布者**: visvjn

**变更内容**:

##### 15. 版本 7.00.00

- **状态**: released
- **发布日期**: 2016-02-26T11:04:52+01:00
- **发布者**: visvjn

**变更内容**:

##### 16. 版本 8.00.00

- **状态**: released
- **发布日期**: 2016-09-26T02:19:58+02:00
- **发布者**: visvjn

**变更内容**:

##### 17. 版本 8.00.01

- **状态**: released
- **发布日期**: 2017-03-01T04:12:40+01:00
- **发布者**: visvjn

**变更内容**:

##### 18. 版本 8.00.02

- **状态**: released
- **发布日期**: 2017-04-12T05:47:30+02:00
- **发布者**: visvjn

**变更内容**:

##### 19. 版本 9.00.00

- **状态**: released
- **发布日期**: 2018-06-15T15:11:30+02:00
- **发布者**: visvjn

**变更内容**:

##### 20. 版本 9.01.00

- **状态**: released
- **发布日期**: 2018-07-27T15:24:18+02:00
- **发布者**: visvjn

**变更内容**:

##### 21. 版本 9.02.00

- **状态**: released
- **发布日期**: 2018-08-10T11:55:54+02:00
- **发布者**: visvjn

**变更内容**:

##### 22. 版本 10.00.00

- **状态**: released
- **发布日期**: 2018-12-06T11:46:39+01:00
- **发布者**: vislsi

**变更内容**:

##### 23. 版本 10.00.01

- **状态**: released
- **发布日期**: 2019-08-09T08:38:36+02:00
- **发布者**: visvjn

**变更内容**:

##### 24. 版本 10.00.02

- **状态**: released
- **发布日期**: 2020-02-06T08:38:36+02:00
- **发布者**: visols

**变更内容**:

##### 25. 版本 11.00.00

- **状态**: released
- **发布日期**: 2020-11-18T10:39:46+01:00
- **发布者**: visvjn

**变更内容**:

##### 26. 版本 11.00.00

- **状态**: released
- **发布日期**: 2020-11-27T15:48:56+01:00
- **发布者**: visols

**变更内容**:

##### 27. 版本 11.00.01

- **状态**: released
- **发布日期**: 2021-01-27T10:17:18+01:00
- **发布者**: visols

**变更内容**:

##### 28. 版本 11.00.02

- **状态**: released
- **发布日期**: 2021-02-16T10:52:01+01:00
- **发布者**: visols

**变更内容**:

##### 29. 版本 12.00.00

- **状态**: released
- **发布日期**: 2021-12-03T15:25:58+01:00
- **发布者**: visols

**变更内容**:

##### 30. 版本 13.00.00

- **状态**: released
- **发布日期**: 2022-06-28T09:22:53+02:00
- **发布者**: mbach

**变更内容**:

##### 31. 版本 14.00.00

- **状态**: released
- **发布日期**: 2022-11-18T10:27:04+01:00
- **发布者**: mbach

**变更内容**:

##### 32. 版本 14.00.01

- **状态**: released
- **发布日期**: 2023-01-04T17:18:17+01:00
- **发布者**: mbach

**变更内容**:

##### 33. 版本 14.00.02

- **状态**: released
- **发布日期**: 2023-02-01T14:04:56+01:00
- **发布者**: mbach

**变更内容**:

##### 34. 版本 15.00.01

- **状态**: released
- **发布日期**: 2024-02-09T17:30:32+01:00
- **发布者**: visuca

**变更内容**:

#### 配置容器

本模块包含 **33** 个配置容器：

##### 1. EcuMConfiguration

**容器属性**:

- **UUID**: `f8f54a42-5c62-45b8-91f9-31fecb991c86`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMConfiguration`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration (parameters) of the ECU State Manager.

###### 配置容器

本模块包含 **28** 个配置容器：

####### 1. EcuMCommonConfiguration

**容器属性**:

- **UUID**: `d99b6c74-04c0-4d2b-b106-9fe7e70e7eda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMCommonConfiguration`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the common configuration (parameters) of the ECU State Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMConfigConsistencyHash

- **UUID**: `adfd5b30-c251-4962-afc2-ccca10e0c280`
- **参数名**: `EcuMConfigConsistencyHash`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies a hash value generated across all pre-compile and link-time parameters of all BSW modules. This hash value is compared against a field in the EcuM_ConfigType and hence allows checking the consistency of the entire configuration.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMDefaultAppMode

- **UUID**: `ad05ac06-e400-403f-bdbe-12defb1fe02b`
- **引用名**: `EcuMDefaultAppMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the default application mode in the OS configuration, loaded when the ECU comes out of reset.

########## 2. EcuMOSResource

- **UUID**: `554b1a7e-11b6-4da2-8b8d-61a476112123`
- **引用名**: `EcuMOSResource`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS resource which is used to block the scheduler during a sleep phase. 

In the case of a multicore system the scheduler on the slave core must also be blocked during a sleep phase.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `104c6de4-eec5-433d-883d-041c6cae74ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EcuMDefaultState

- **UUID**: `ace41eeb-73c1-406d-ad52-a335e87f4440`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EcuMStateOff`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EcuMStateOff`
  - `EcuMStateReset`
  - `EcuMStateSleep`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the state part of the default shutdown target selected when the ECU comes out of reset. 
If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode. If EcuMStateReset is selected, the parameter EcuMDefaultResetModeRef selects the specific reset mode.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMDefaultResetModeRef

- **UUID**: `87d0d2ee-1f99-40a6-b36f-ecb3d3776dc8`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a reset mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

############ 2. EcuMDefaultSleepModeRef

- **UUID**: `622d2454-f8ad-4cdd-a31e-9f66b1b71dd2`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a sleep mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

######### 2. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `34410ce9-8619-4167-bdac-66d9ccb7c207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

########## 引用关系

此容器包含 **4** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `b37e982e-1d4c-4bca-a7af-4ef40bc814eb`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

This reference is only relevant for EcuM Fixed

############ 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `4528f2a9-2fcc-4c6d-8808-412ab707b3d5`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occurred.

############ 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `21017406-9114-4d40-8393-a787812b8ece`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occurred.

############ 4. ECUM_E_IMPROPER_CALLER

- **UUID**: `ef4ff3c8-178f-41ec-99cb-babd56045bb3`
- **引用名**: `ECUM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_IMPROPER_CALLER" has occurred.

######### 3. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `2996d6f5-c68a-4164-85fd-70e4e1936588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset from within EcuM_Init function after the module has entered the state ECUM_STATE_STARTUP_ONE. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############## 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############## 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

######### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

######### 5. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `5fe3f07c-769f-4535-b0a2-6906a16b345a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset almost directly after EcuM_Init has been called. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############## 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

############## 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

######### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

######### 7. EcuMDriverRestartList

**容器属性**:

- **UUID**: `449e3e32-d14c-4004-8b3f-c4d815f0fc23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a restart from SLEEP mode occurred. 

EcuMDriverRestartList shall normally do the same initialization calls listed in the order in which they occur in the EcuMDriverInitListZero and EcuMDriverInitListOne.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############## 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############## 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 9. EcuMSleepMode

**容器属性**:

- **UUID**: `f94e4a12-5655-4969-a5cb-2f7e2c2e158f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of one sleep modes. The name of this container specify the symbolic name of a sleep mode and identifies the corresponding sources which should be active during this sleep phase.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EcuMSleepModeId

- **UUID**: `9a8d1a86-1e4d-4110-a920-3d311a69852f`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this sleep mode in services like EcuM_SelectShutdownTarget.

########### BOOLEAN 类型参数

############ 1. EcuMSleepModeSuspend

- **UUID**: `7f3994c0-cdfe-4936-8ecd-60f211bb6cc9`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This parameter defines if the CPU is suspended, halted or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSleepModeMcuModeRef

- **UUID**: `6be090fb-c220-4cac-9d48-ee56021711cc`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the corresponding MCU mode for this sleep mode.

############ 2. EcuMWakeupSourceMask

- **UUID**: `8ad18005-51ae-45d7-904f-bdea951854e4`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the wakeup sources in this module that shall be enabled for this sleep mode.

######### 10. EcuMWakeupSource

**容器属性**:

- **UUID**: `485bc039-ae7a-4f9c-8024-5506de8a2444`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of a wakeup source.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. EcuMWakeupSourceId

- **UUID**: `a113b9ba-185f-4cdc-8653-a8d4ef83f606`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this wakeup source.

########### BOOLEAN 类型参数

############ 1. EcuMWakeupSourcePolling

- **UUID**: `2c5bbf69-b6cc-4d2f-b8c5-467ae85e0d20`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the wakeup source needs polling.

########### FLOAT 类型参数

############ 1. EcuMValidationTimeout

- **UUID**: `61777a90-79f7-42b7-8627-fff387cc1970`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. If the parameter is not defined or is defined to 0 the wakeup validation is disabled for this wakeup source.

############ 2. EcuMCheckWakeupTimeout

- **UUID**: `9c1217b0-509e-4633-a06f-442ed0b72e8e`
- **参数名**: `EcuMCheckWakeupTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum time between the call of EcuM_CheckWakeup and an asynchronous call of EcuM_SetWakeupEvent of the same wakeup source. If the timeout expires the ECU is allowed to go to sleep state. For wakeup sources where it is ensured that the EcuM_SetWakeupEvent is called before EcuM_CheckWakeup function ends the timeout value shall be 0 or the parameter shall be deleted.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMComMChannelRef

- **UUID**: `a260edc3-de17-4289-bb57-4171d50afe1e`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to multiple Networks (channels) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

############ 2. EcuMResetReasonRef

- **UUID**: `e8a4d8d9-55e4-4006-b316-220279ea6864`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a reset reason detected by the MCU driver.

############ 3. EcuMComMPNCRef

- **UUID**: `9d33d5ac-0e21-4472-91bb-1ae53698833b`
- **引用名**: `EcuMComMPNCRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one or more PNC's defined in the Communication Manager. No reference indicates that the wakeup source is not assigned to a partial network.

####### 2. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `104c6de4-eec5-433d-883d-041c6cae74ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EcuMDefaultState

- **UUID**: `ace41eeb-73c1-406d-ad52-a335e87f4440`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EcuMStateOff`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EcuMStateOff`
  - `EcuMStateReset`
  - `EcuMStateSleep`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the state part of the default shutdown target selected when the ECU comes out of reset. 
If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode. If EcuMStateReset is selected, the parameter EcuMDefaultResetModeRef selects the specific reset mode.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMDefaultResetModeRef

- **UUID**: `87d0d2ee-1f99-40a6-b36f-ecb3d3776dc8`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a reset mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

########## 2. EcuMDefaultSleepModeRef

- **UUID**: `622d2454-f8ad-4cdd-a31e-9f66b1b71dd2`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a sleep mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

####### 3. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `34410ce9-8619-4167-bdac-66d9ccb7c207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `b37e982e-1d4c-4bca-a7af-4ef40bc814eb`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

This reference is only relevant for EcuM Fixed

########## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `4528f2a9-2fcc-4c6d-8808-412ab707b3d5`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occurred.

########## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `21017406-9114-4d40-8393-a787812b8ece`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occurred.

########## 4. ECUM_E_IMPROPER_CALLER

- **UUID**: `ef4ff3c8-178f-41ec-99cb-babd56045bb3`
- **引用名**: `ECUM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_IMPROPER_CALLER" has occurred.

####### 4. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `2996d6f5-c68a-4164-85fd-70e4e1936588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset from within EcuM_Init function after the module has entered the state ECUM_STATE_STARTUP_ONE. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 5. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 6. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `5fe3f07c-769f-4535-b0a2-6906a16b345a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset almost directly after EcuM_Init has been called. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 7. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 8. EcuMDriverRestartList

**容器属性**:

- **UUID**: `449e3e32-d14c-4004-8b3f-c4d815f0fc23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a restart from SLEEP mode occurred. 

EcuMDriverRestartList shall normally do the same initialization calls listed in the order in which they occur in the EcuMDriverInitListZero and EcuMDriverInitListOne.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 9. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 10. EcuMSleepMode

**容器属性**:

- **UUID**: `f94e4a12-5655-4969-a5cb-2f7e2c2e158f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of one sleep modes. The name of this container specify the symbolic name of a sleep mode and identifies the corresponding sources which should be active during this sleep phase.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMSleepModeId

- **UUID**: `9a8d1a86-1e4d-4110-a920-3d311a69852f`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this sleep mode in services like EcuM_SelectShutdownTarget.

######### BOOLEAN 类型参数

########## 1. EcuMSleepModeSuspend

- **UUID**: `7f3994c0-cdfe-4936-8ecd-60f211bb6cc9`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This parameter defines if the CPU is suspended, halted or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeMcuModeRef

- **UUID**: `6be090fb-c220-4cac-9d48-ee56021711cc`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the corresponding MCU mode for this sleep mode.

########## 2. EcuMWakeupSourceMask

- **UUID**: `8ad18005-51ae-45d7-904f-bdea951854e4`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the wakeup sources in this module that shall be enabled for this sleep mode.

####### 11. EcuMWakeupSource

**容器属性**:

- **UUID**: `485bc039-ae7a-4f9c-8024-5506de8a2444`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of a wakeup source.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. EcuMWakeupSourceId

- **UUID**: `a113b9ba-185f-4cdc-8653-a8d4ef83f606`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this wakeup source.

######### BOOLEAN 类型参数

########## 1. EcuMWakeupSourcePolling

- **UUID**: `2c5bbf69-b6cc-4d2f-b8c5-467ae85e0d20`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the wakeup source needs polling.

######### FLOAT 类型参数

########## 1. EcuMValidationTimeout

- **UUID**: `61777a90-79f7-42b7-8627-fff387cc1970`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. If the parameter is not defined or is defined to 0 the wakeup validation is disabled for this wakeup source.

########## 2. EcuMCheckWakeupTimeout

- **UUID**: `9c1217b0-509e-4633-a06f-442ed0b72e8e`
- **参数名**: `EcuMCheckWakeupTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum time between the call of EcuM_CheckWakeup and an asynchronous call of EcuM_SetWakeupEvent of the same wakeup source. If the timeout expires the ECU is allowed to go to sleep state. For wakeup sources where it is ensured that the EcuM_SetWakeupEvent is called before EcuM_CheckWakeup function ends the timeout value shall be 0 or the parameter shall be deleted.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMChannelRef

- **UUID**: `a260edc3-de17-4289-bb57-4171d50afe1e`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to multiple Networks (channels) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

########## 2. EcuMResetReasonRef

- **UUID**: `e8a4d8d9-55e4-4006-b316-220279ea6864`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a reset reason detected by the MCU driver.

########## 3. EcuMComMPNCRef

- **UUID**: `9d33d5ac-0e21-4472-91bb-1ae53698833b`
- **引用名**: `EcuMComMPNCRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one or more PNC's defined in the Communication Manager. No reference indicates that the wakeup source is not assigned to a partial network.

####### 12. EcuMFixedConfiguration

**容器属性**:

- **UUID**: `4038a2de-096a-4576-aebc-6b3611faf200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration (parameters) of the EcuMFixed.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. EcuMNvramReadallTimeout

- **UUID**: `821c333e-5e21-409f-869c-36f46ab351ef`
- **参数名**: `EcuMNvramReadallTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll job of the NVRAM Manager as failed.

########## 2. EcuMNvramWriteallTimeout

- **UUID**: `5133df29-be6c-4cdf-b8a5-faff86cbf30a`
- **参数名**: `EcuMNvramWriteallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a WriteAll job of the NVRAM Manager as failed.

########## 3. EcuMRunMinimumDuration

- **UUID**: `6befb49a-2f71-49e0-a017-a003e02d529e`
- **参数名**: `EcuMRunMinimumDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration given in seconds for which the ECU State Manager will

########## 4. EcuMNvmCancelWriteAllTimeout

- **UUID**: `4ce85ce9-2579-4a32-b2c0-bc1017cf069f`
- **参数名**: `EcuMNvmCancelWriteAllTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the time in seconds which shall be waited for NvM_WriteAll in case NvM_CancelWriteAll was called due to a wakeup event.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMCommunicationAllowedList

- **UUID**: `194a4832-ce41-44c0-914d-a71bb6bbb3f6`
- **引用名**: `EcuMComMCommunicationAllowedList`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These parameters contain references to the ComMChannels for which EcuM has to call ComM_CommunicationAllowed.

########## 2. EcuMNormalMcuModeRef

- **UUID**: `a736eae6-a2a9-4470-ba85-79d3a5e32085`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

######### CHOICE-REFERENCE 类型引用

########## 1. EcuMFixedModuleConfigurationRef

- **UUID**: `d3638ed2-22f7-4783-a42d-b3eaffb1a94f`
- **引用名**: `EcuMFixedModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet`
  - `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg`
  - `/AUTOSAR/EcucDefs/CanNm/CanNmGlobalConfig`
  - `/AUTOSAR/EcucDefs/CanSM/CanSMConfiguration`
  - `/AUTOSAR/EcucDefs/CanTp/CanTpConfig`
  - `/AUTOSAR/EcucDefs/CanTrcv/CanTrcvConfigSet`
  - `/AUTOSAR/EcucDefs/Com/ComConfig`
  - `/AUTOSAR/EcucDefs/ComM/ComMConfigSet`
  - `/AUTOSAR/EcucDefs/Dbg/DbgMultipleConfigurationContainer`
  - `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet`
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig`
  - `/AUTOSAR/EcucDefs/Dlt/DltMultipleConfigurationContainer`
  - `/AUTOSAR/EcucDefs/Eep/EepInitConfiguration`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet`
  - `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet`
  - `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet`
  - `/AUTOSAR/EcucDefs/FiM/FiMConfigSet`
  - `/AUTOSAR/EcucDefs/Fls/FlsConfigSet`
  - `/AUTOSAR/EcucDefs/FlsTst/FlsTstConfigSet`
  - `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig`
  - `/AUTOSAR/EcucDefs/FrIf/FrIfConfig`
  - `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration`
  - `/AUTOSAR/EcucDefs/FrNm/FrNmChannelConfig`
  - `/AUTOSAR/EcucDefs/FrSM/FrSMConfig`
  - `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig`
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet`
  - `/AUTOSAR/EcucDefs/IpduM/IpduMConfig`
  - `/AUTOSAR/EcucDefs/J1939Tp/J1939TpConfiguration`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig`
  - `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig`
  - `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet`
  - `/AUTOSAR/EcucDefs/LinTp/LinTpGlobalConfig`
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration`
  - `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables`
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Rte/RtePostBuildVariantConfiguration`
  - `/AUTOSAR/EcucDefs/SoAd/SoAdDoIpConfig`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver`
  - `/AUTOSAR/EcucDefs/UdpNm/UdpNmGlobalConfig`
  - `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet`
  - `/AUTOSAR/EcucDefs/Wdg/WdgSettingsConfig`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `fb8d3224-7d59-40cd-95fb-506fd83659f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############## 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 2. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 3. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `34e86c5c-325c-4c8a-a0be-924090309799`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############## 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 5. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `1e6be767-c823-462f-883b-44e35803427e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMFixedUser

- **UUID**: `4f888481-0e5c-4b78-a917-efa5be2607f4`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Parameter used to identify one user.

######### 6. EcuMTTII

**容器属性**:

- **UUID**: `8cf03107-d2a4-4430-84a7-1367a65ba24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Not used!

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMDivisor

- **UUID**: `0c4351ff-3f8d-48a6-a3a1-6615ddd79e1c`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the divisor pre load value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSleepModeRef

- **UUID**: `ef5fb3b7-b0b9-43e3-8ed2-ce549d68c07f`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

############ 2. EcuMSuccessorRef

- **UUID**: `735cd32e-6814-4de8-b8f9-ec9e61776be7`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

####### 13. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `fb8d3224-7d59-40cd-95fb-506fd83659f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 14. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 15. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `34e86c5c-325c-4c8a-a0be-924090309799`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 16. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 17. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `1e6be767-c823-462f-883b-44e35803427e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFixedUser

- **UUID**: `4f888481-0e5c-4b78-a917-efa5be2607f4`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Parameter used to identify one user.

####### 18. EcuMTTII

**容器属性**:

- **UUID**: `8cf03107-d2a4-4430-84a7-1367a65ba24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Not used!

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMDivisor

- **UUID**: `0c4351ff-3f8d-48a6-a3a1-6615ddd79e1c`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the divisor pre load value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeRef

- **UUID**: `ef5fb3b7-b0b9-43e3-8ed2-ce549d68c07f`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

########## 2. EcuMSuccessorRef

- **UUID**: `735cd32e-6814-4de8-b8f9-ec9e61776be7`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

####### 19. EcuMFlexConfiguration

**容器属性**:

- **UUID**: `c9abdd8d-c489-4883-883d-206a63f973f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration (parameters) of the EcuMFlex.

######## 引用关系

此容器包含 **4** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMGptChannelRef

- **UUID**: `6ca310b8-c477-4b63-87cf-1c5db1da9558`
- **引用名**: `EcuMGptChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a GPT Channel which serves as the timebase for the EcuM Clock.The GPT Channel must be a Channel in GPT_CH_MODE_CONTINUOUS to guarantee permanent and exact counting of the EcuM clock.

########## 2. EcuMPartitionRef

- **UUID**: `b03b10b2-f932-4cb3-bbf7-4d6286d2e7b7`
- **引用名**: `EcuMPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference denotes the partition a EcuM and SchM shall run inside. 

Please note that in case of a multicore ECU this reference is mandatory and it is expected that the SchM and the EcuM run only once per core.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMNormalMcuModeRef

- **UUID**: `132fa71c-5870-4337-9f12-d7d4f3376463`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the normal MCU mode to be restored after a sleep.

######### CHOICE-REFERENCE 类型引用

########## 1. EcuMFlexModuleConfigurationRef

- **UUID**: `d085f9eb-9c47-48e4-a39c-a3d69910435b`
- **引用名**: `EcuMFlexModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet`
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet`
  - `/AUTOSAR/EcucDefs/Fls/FlsConfigSet`
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig`
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration`
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver`
  - `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet`
  - `/AUTOSAR/EcucDefs/Wdg/WdgSettingsConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to the initialization structure of the corresponding BSW module.

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. EcuMAlarmClock

**容器属性**:

- **UUID**: `01049a49-134d-4414-b6ec-8c33365bd8a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured alarm clocks.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EcuMAlarmClockId

- **UUID**: `f4883b50-0ab1-4b73-a1e2-0a99d883060a`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This ID identifies this alarmclock.

########### FLOAT 类型参数

############ 1. EcuMAlarmClockTimeOut

- **UUID**: `06999a88-336b-470b-98eb-8c2b9b40266c`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows to define a timeout for this alarm clock.

Not Used

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMAlarmClockUser

- **UUID**: `67afb42c-6829-4796-96a6-4b3bcccb3a14`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows an alarm to be assigned to a user.

######### 2. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `90b51b5d-19e7-4fc9-b12c-f303d0620f41`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces. This container is only needed if the parameter EcuMEnableDefBehaviour is active.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EcuMFlexUser

- **UUID**: `1617e119-9dbb-4fda-acfc-a094e03da217`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier of the EcuMFlex user.

############ 2. EcuMGoDownRequestID

- **UUID**: `92b50b0c-a210-4d74-94e0-dad54d98d79e`
- **参数名**: `EcuMGoDownRequestID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `42`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the corresponding BSW or SWC ModuleID. The parameter is necessary to translate the caller ID of the API EcuM_GoDown into an EcuM_FlexUser ID.

This value depends on the configuration item EcuMEnableDefBehaviour. If (EcuMEnableDefBehaviour == true) then this parameter is optional configurable otherwise this parameter is ignored.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EcuMFlexEcucPartitionRef

- **UUID**: `aa52827c-9105-403f-82fc-a4605817ca76`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..0]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!
Denotes in which "EcucPartition" the user of the EcuM is executed.

######### 3. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `c1453d6e-ec17-4cbd-8503-5db6c014135c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_GoDown API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMGoDownAllowedUserRef

- **UUID**: `d990691d-1ea9-4064-87c6-8bcd9dbef7fd`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_GoDown API. If a reference to an EcuM_User is set, this user must have a configured EcuMGoDownRequestID to translate the caller ID in the routine EcuM_GoDown.

######### 4. EcuMResetMode

**容器属性**:

- **UUID**: `3a7be8c5-e72c-4110-bdcc-8115e3bbf211`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured reset modes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMResetModeId

- **UUID**: `19e7a6e8-e504-482b-94eb-b70f0e2fe423`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier to be used in services like EcuM_SelectShutdownTarget.

######### 5. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `d9043323-9e03-4a73-abf6-ef24f97a90f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_SetClock API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSetClockAllowedUserRef

- **UUID**: `9ae28f79-117f-4e11-b200-5bd96786fbd8`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_SetClock API.

######### 6. EcuMShutdownCause

**容器属性**:

- **UUID**: `bd55945f-5876-43e5-bfde-ecf0b7afc657`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured shut down or reset causes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMShutdownCauseId

- **UUID**: `e84f9953-fe9d-4fcf-8fe0-a5836046deb3`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This values specifies the identifier for API calls for this shut down cause.

######### 7. EcuMShutdownTarget

**容器属性**:

- **UUID**: `8ccbec4c-d238-4e65-81e0-feeffc5257a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container is not used including the parameters.

These containers include the configured shut down targets.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMShutdownTargetId

- **UUID**: `959073ad-3b50-41a1-a53f-269b72c40b82`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier used for this shut down target in services like EcuM_SelectShutdownTarget.

######### 8. EcuMDriverInitListBswM

**容器属性**:

- **UUID**: `01820739-2c3d-45a2-9a3b-4926762ff2be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListBswM`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes a list of initialization items that will be handled after the BswM has been initialized.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

############ 参数配置

此容器包含 **4** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############## 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############## 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############## 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

######### 9. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 20. EcuMAlarmClock

**容器属性**:

- **UUID**: `01049a49-134d-4414-b6ec-8c33365bd8a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured alarm clocks.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMAlarmClockId

- **UUID**: `f4883b50-0ab1-4b73-a1e2-0a99d883060a`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This ID identifies this alarmclock.

######### FLOAT 类型参数

########## 1. EcuMAlarmClockTimeOut

- **UUID**: `06999a88-336b-470b-98eb-8c2b9b40266c`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows to define a timeout for this alarm clock.

Not Used

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMAlarmClockUser

- **UUID**: `67afb42c-6829-4796-96a6-4b3bcccb3a14`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows an alarm to be assigned to a user.

####### 21. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `90b51b5d-19e7-4fc9-b12c-f303d0620f41`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces. This container is only needed if the parameter EcuMEnableDefBehaviour is active.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFlexUser

- **UUID**: `1617e119-9dbb-4fda-acfc-a094e03da217`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier of the EcuMFlex user.

########## 2. EcuMGoDownRequestID

- **UUID**: `92b50b0c-a210-4d74-94e0-dad54d98d79e`
- **参数名**: `EcuMGoDownRequestID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `42`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the corresponding BSW or SWC ModuleID. The parameter is necessary to translate the caller ID of the API EcuM_GoDown into an EcuM_FlexUser ID.

This value depends on the configuration item EcuMEnableDefBehaviour. If (EcuMEnableDefBehaviour == true) then this parameter is optional configurable otherwise this parameter is ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMFlexEcucPartitionRef

- **UUID**: `aa52827c-9105-403f-82fc-a4605817ca76`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..0]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!
Denotes in which "EcucPartition" the user of the EcuM is executed.

####### 22. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `c1453d6e-ec17-4cbd-8503-5db6c014135c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_GoDown API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMGoDownAllowedUserRef

- **UUID**: `d990691d-1ea9-4064-87c6-8bcd9dbef7fd`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_GoDown API. If a reference to an EcuM_User is set, this user must have a configured EcuMGoDownRequestID to translate the caller ID in the routine EcuM_GoDown.

####### 23. EcuMResetMode

**容器属性**:

- **UUID**: `3a7be8c5-e72c-4110-bdcc-8115e3bbf211`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured reset modes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMResetModeId

- **UUID**: `19e7a6e8-e504-482b-94eb-b70f0e2fe423`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier to be used in services like EcuM_SelectShutdownTarget.

####### 24. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `d9043323-9e03-4a73-abf6-ef24f97a90f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_SetClock API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSetClockAllowedUserRef

- **UUID**: `9ae28f79-117f-4e11-b200-5bd96786fbd8`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_SetClock API.

####### 25. EcuMShutdownCause

**容器属性**:

- **UUID**: `bd55945f-5876-43e5-bfde-ecf0b7afc657`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured shut down or reset causes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownCauseId

- **UUID**: `e84f9953-fe9d-4fcf-8fe0-a5836046deb3`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This values specifies the identifier for API calls for this shut down cause.

####### 26. EcuMShutdownTarget

**容器属性**:

- **UUID**: `8ccbec4c-d238-4e65-81e0-feeffc5257a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container is not used including the parameters.

These containers include the configured shut down targets.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownTargetId

- **UUID**: `959073ad-3b50-41a1-a53f-269b72c40b82`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier used for this shut down target in services like EcuM_SelectShutdownTarget.

####### 27. EcuMDriverInitListBswM

**容器属性**:

- **UUID**: `01820739-2c3d-45a2-9a3b-4926762ff2be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListBswM`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes a list of initialization items that will be handled after the BswM has been initialized.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 28. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 2. EcuMCommonConfiguration

**容器属性**:

- **UUID**: `d99b6c74-04c0-4d2b-b106-9fe7e70e7eda`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMCommonConfiguration`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the common configuration (parameters) of the ECU State Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMConfigConsistencyHash

- **UUID**: `adfd5b30-c251-4962-afc2-ccca10e0c280`
- **参数名**: `EcuMConfigConsistencyHash`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies a hash value generated across all pre-compile and link-time parameters of all BSW modules. This hash value is compared against a field in the EcuM_ConfigType and hence allows checking the consistency of the entire configuration.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. EcuMDefaultAppMode

- **UUID**: `ad05ac06-e400-403f-bdbe-12defb1fe02b`
- **引用名**: `EcuMDefaultAppMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the default application mode in the OS configuration, loaded when the ECU comes out of reset.

######## 2. EcuMOSResource

- **UUID**: `554b1a7e-11b6-4da2-8b8d-61a476112123`
- **引用名**: `EcuMOSResource`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an OS resource which is used to block the scheduler during a sleep phase. 

In the case of a multicore system the scheduler on the slave core must also be blocked during a sleep phase.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `104c6de4-eec5-433d-883d-041c6cae74ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EcuMDefaultState

- **UUID**: `ace41eeb-73c1-406d-ad52-a335e87f4440`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EcuMStateOff`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EcuMStateOff`
  - `EcuMStateReset`
  - `EcuMStateSleep`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the state part of the default shutdown target selected when the ECU comes out of reset. 
If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode. If EcuMStateReset is selected, the parameter EcuMDefaultResetModeRef selects the specific reset mode.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMDefaultResetModeRef

- **UUID**: `87d0d2ee-1f99-40a6-b36f-ecb3d3776dc8`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a reset mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

########## 2. EcuMDefaultSleepModeRef

- **UUID**: `622d2454-f8ad-4cdd-a31e-9f66b1b71dd2`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a sleep mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

####### 2. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `34410ce9-8619-4167-bdac-66d9ccb7c207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **4** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `b37e982e-1d4c-4bca-a7af-4ef40bc814eb`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

This reference is only relevant for EcuM Fixed

########## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `4528f2a9-2fcc-4c6d-8808-412ab707b3d5`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occurred.

########## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `21017406-9114-4d40-8393-a787812b8ece`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occurred.

########## 4. ECUM_E_IMPROPER_CALLER

- **UUID**: `ef4ff3c8-178f-41ec-99cb-babd56045bb3`
- **引用名**: `ECUM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_IMPROPER_CALLER" has occurred.

####### 3. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `2996d6f5-c68a-4164-85fd-70e4e1936588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset from within EcuM_Init function after the module has entered the state ECUM_STATE_STARTUP_ONE. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 5. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `5fe3f07c-769f-4535-b0a2-6906a16b345a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset almost directly after EcuM_Init has been called. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

####### 7. EcuMDriverRestartList

**容器属性**:

- **UUID**: `449e3e32-d14c-4004-8b3f-c4d815f0fc23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a restart from SLEEP mode occurred. 

EcuMDriverRestartList shall normally do the same initialization calls listed in the order in which they occur in the EcuMDriverInitListZero and EcuMDriverInitListOne.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 9. EcuMSleepMode

**容器属性**:

- **UUID**: `f94e4a12-5655-4969-a5cb-2f7e2c2e158f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of one sleep modes. The name of this container specify the symbolic name of a sleep mode and identifies the corresponding sources which should be active during this sleep phase.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMSleepModeId

- **UUID**: `9a8d1a86-1e4d-4110-a920-3d311a69852f`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this sleep mode in services like EcuM_SelectShutdownTarget.

######### BOOLEAN 类型参数

########## 1. EcuMSleepModeSuspend

- **UUID**: `7f3994c0-cdfe-4936-8ecd-60f211bb6cc9`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This parameter defines if the CPU is suspended, halted or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeMcuModeRef

- **UUID**: `6be090fb-c220-4cac-9d48-ee56021711cc`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the corresponding MCU mode for this sleep mode.

########## 2. EcuMWakeupSourceMask

- **UUID**: `8ad18005-51ae-45d7-904f-bdea951854e4`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the wakeup sources in this module that shall be enabled for this sleep mode.

####### 10. EcuMWakeupSource

**容器属性**:

- **UUID**: `485bc039-ae7a-4f9c-8024-5506de8a2444`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of a wakeup source.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. EcuMWakeupSourceId

- **UUID**: `a113b9ba-185f-4cdc-8653-a8d4ef83f606`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this wakeup source.

######### BOOLEAN 类型参数

########## 1. EcuMWakeupSourcePolling

- **UUID**: `2c5bbf69-b6cc-4d2f-b8c5-467ae85e0d20`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the wakeup source needs polling.

######### FLOAT 类型参数

########## 1. EcuMValidationTimeout

- **UUID**: `61777a90-79f7-42b7-8627-fff387cc1970`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. If the parameter is not defined or is defined to 0 the wakeup validation is disabled for this wakeup source.

########## 2. EcuMCheckWakeupTimeout

- **UUID**: `9c1217b0-509e-4633-a06f-442ed0b72e8e`
- **参数名**: `EcuMCheckWakeupTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum time between the call of EcuM_CheckWakeup and an asynchronous call of EcuM_SetWakeupEvent of the same wakeup source. If the timeout expires the ECU is allowed to go to sleep state. For wakeup sources where it is ensured that the EcuM_SetWakeupEvent is called before EcuM_CheckWakeup function ends the timeout value shall be 0 or the parameter shall be deleted.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMChannelRef

- **UUID**: `a260edc3-de17-4289-bb57-4171d50afe1e`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to multiple Networks (channels) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

########## 2. EcuMResetReasonRef

- **UUID**: `e8a4d8d9-55e4-4006-b316-220279ea6864`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a reset reason detected by the MCU driver.

########## 3. EcuMComMPNCRef

- **UUID**: `9d33d5ac-0e21-4472-91bb-1ae53698833b`
- **引用名**: `EcuMComMPNCRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one or more PNC's defined in the Communication Manager. No reference indicates that the wakeup source is not assigned to a partial network.

##### 3. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `104c6de4-eec5-433d-883d-041c6cae74ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EcuMDefaultState

- **UUID**: `ace41eeb-73c1-406d-ad52-a335e87f4440`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `EcuMStateOff`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `EcuMStateOff`
  - `EcuMStateReset`
  - `EcuMStateSleep`
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the state part of the default shutdown target selected when the ECU comes out of reset. 
If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode. If EcuMStateReset is selected, the parameter EcuMDefaultResetModeRef selects the specific reset mode.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMDefaultResetModeRef

- **UUID**: `87d0d2ee-1f99-40a6-b36f-ecb3d3776dc8`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a reset mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

######## 2. EcuMDefaultSleepModeRef

- **UUID**: `622d2454-f8ad-4cdd-a31e-9f66b1b71dd2`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a sleep mode configuration within this module. If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

##### 4. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `34410ce9-8619-4167-bdac-66d9ccb7c207`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **4** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `b37e982e-1d4c-4bca-a7af-4ef40bc814eb`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

This reference is only relevant for EcuM Fixed

######## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `4528f2a9-2fcc-4c6d-8808-412ab707b3d5`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occurred.

######## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `21017406-9114-4d40-8393-a787812b8ece`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occurred.

######## 4. ECUM_E_IMPROPER_CALLER

- **UUID**: `ef4ff3c8-178f-41ec-99cb-babd56045bb3`
- **引用名**: `ECUM_E_IMPROPER_CALLER`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_IMPROPER_CALLER" has occurred.

##### 5. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `2996d6f5-c68a-4164-85fd-70e4e1936588`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset from within EcuM_Init function after the module has entered the state ECUM_STATE_STARTUP_ONE. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

##### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `2a66ac75-4a75-4b0a-a930-620ba696045b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `904b7c04-5726-4388-bb69-9eb4d034c145`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

######## 2. EcuMModuleService

- **UUID**: `c44db3e0-bcd5-4de0-8b9b-61c8e74190fa`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

######## 3. EcuMAdditionalInitCode

- **UUID**: `495eed83-d316-421b-a39d-0b61496309e0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `9e4109e6-820e-4447-aac6-0d985da9af74`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

##### 7. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `5fe3f07c-769f-4535-b0a2-6906a16b345a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a reset almost directly after EcuM_Init has been called. 

All items in this list are initialized before the post-build configuration has been loaded and the OS is initialized. Therefore none of these items may use post-build configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

##### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `dbd0bfd4-4cd4-4c21-9b71-18a0784db224`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `8137753a-720b-4341-a482-363ffa94a1df`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

######## 2. EcuMModuleService

- **UUID**: `514c870c-e483-4e73-a83d-7079537b6267`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the module(<MSN>_CtrlIdx) are be passed as arguments.

######## 3. EcuMAdditionalInitCode

- **UUID**: `798d7b4b-f82d-41e8-9424-96d7988f2830`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `7e9a45e9-52c6-4dfe-96f2-e66562ea66a4`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for this driver init item.

##### 9. EcuMDriverRestartList

**容器属性**:

- **UUID**: `449e3e32-d14c-4004-8b3f-c4d815f0fc23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes a list of initialization items that will be handled after a restart from SLEEP mode occurred. 

EcuMDriverRestartList shall normally do the same initialization calls listed in the order in which they occur in the EcuMDriverInitListZero and EcuMDriverInitListOne.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 10. EcuMDriverInitItem

**容器属性**:

- **UUID**: `9e209a19-aff0-43f7-8528-483f2cb4803d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `32f5569b-1698-4b55-bc52-04fdc00688cb`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc. For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

######## 2. EcuMModuleService

- **UUID**: `25cbf3fd-dc4d-431d-b014-1b98e6393014`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######## 3. EcuMAdditionalInitCode

- **UUID**: `4e4c2b77-9fc6-44fb-aa47-e7e4b21d45f3`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `2a68bd1a-de19-4b92-894a-fa8ed549ba9a`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 11. EcuMSleepMode

**容器属性**:

- **UUID**: `f94e4a12-5655-4969-a5cb-2f7e2c2e158f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [0..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of one sleep modes. The name of this container specify the symbolic name of a sleep mode and identifies the corresponding sources which should be active during this sleep phase.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EcuMSleepModeId

- **UUID**: `9a8d1a86-1e4d-4110-a920-3d311a69852f`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this sleep mode in services like EcuM_SelectShutdownTarget.

####### BOOLEAN 类型参数

######## 1. EcuMSleepModeSuspend

- **UUID**: `7f3994c0-cdfe-4936-8ecd-60f211bb6cc9`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This parameter defines if the CPU is suspended, halted or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSleepModeMcuModeRef

- **UUID**: `6be090fb-c220-4cac-9d48-ee56021711cc`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the corresponding MCU mode for this sleep mode.

######## 2. EcuMWakeupSourceMask

- **UUID**: `8ad18005-51ae-45d7-904f-bdea951854e4`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the wakeup sources in this module that shall be enabled for this sleep mode.

##### 12. EcuMWakeupSource

**容器属性**:

- **UUID**: `485bc039-ae7a-4f9c-8024-5506de8a2444`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container includes the configuration of a wakeup source.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. EcuMWakeupSourceId

- **UUID**: `a113b9ba-185f-4cdc-8653-a8d4ef83f606`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier of this wakeup source.

####### BOOLEAN 类型参数

######## 1. EcuMWakeupSourcePolling

- **UUID**: `2c5bbf69-b6cc-4d2f-b8c5-467ae85e0d20`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the wakeup source needs polling.

####### FLOAT 类型参数

######## 1. EcuMValidationTimeout

- **UUID**: `61777a90-79f7-42b7-8627-fff387cc1970`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. If the parameter is not defined or is defined to 0 the wakeup validation is disabled for this wakeup source.

######## 2. EcuMCheckWakeupTimeout

- **UUID**: `9c1217b0-509e-4633-a06f-442ed0b72e8e`
- **参数名**: `EcuMCheckWakeupTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..10]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the maximum time between the call of EcuM_CheckWakeup and an asynchronous call of EcuM_SetWakeupEvent of the same wakeup source. If the timeout expires the ECU is allowed to go to sleep state. For wakeup sources where it is ensured that the EcuM_SetWakeupEvent is called before EcuM_CheckWakeup function ends the timeout value shall be 0 or the parameter shall be deleted.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMComMChannelRef

- **UUID**: `a260edc3-de17-4289-bb57-4171d50afe1e`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to multiple Networks (channels) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

######## 2. EcuMResetReasonRef

- **UUID**: `e8a4d8d9-55e4-4006-b316-220279ea6864`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to a reset reason detected by the MCU driver.

######## 3. EcuMComMPNCRef

- **UUID**: `9d33d5ac-0e21-4472-91bb-1ae53698833b`
- **引用名**: `EcuMComMPNCRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMPnc`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMPnc`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to one or more PNC's defined in the Communication Manager. No reference indicates that the wakeup source is not assigned to a partial network.

##### 13. EcuMFixedConfiguration

**容器属性**:

- **UUID**: `4038a2de-096a-4576-aebc-6b3611faf200`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration (parameters) of the EcuMFixed.

###### 参数配置

此容器包含 **4** 个参数：

####### FLOAT 类型参数

######## 1. EcuMNvramReadallTimeout

- **UUID**: `821c333e-5e21-409f-869c-36f46ab351ef`
- **参数名**: `EcuMNvramReadallTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll job of the NVRAM Manager as failed.

######## 2. EcuMNvramWriteallTimeout

- **UUID**: `5133df29-be6c-4cdf-b8a5-faff86cbf30a`
- **参数名**: `EcuMNvramWriteallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a WriteAll job of the NVRAM Manager as failed.

######## 3. EcuMRunMinimumDuration

- **UUID**: `6befb49a-2f71-49e0-a017-a003e02d529e`
- **参数名**: `EcuMRunMinimumDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration given in seconds for which the ECU State Manager will

######## 4. EcuMNvmCancelWriteAllTimeout

- **UUID**: `4ce85ce9-2579-4a32-b2c0-bc1017cf069f`
- **参数名**: `EcuMNvmCancelWriteAllTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `60`
- **取值范围**: [0..60]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the time in seconds which shall be waited for NvM_WriteAll in case NvM_CancelWriteAll was called due to a wakeup event.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMComMCommunicationAllowedList

- **UUID**: `194a4832-ce41-44c0-914d-a71bb6bbb3f6`
- **引用名**: `EcuMComMCommunicationAllowedList`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: These parameters contain references to the ComMChannels for which EcuM has to call ComM_CommunicationAllowed.

######## 2. EcuMNormalMcuModeRef

- **UUID**: `a736eae6-a2a9-4470-ba85-79d3a5e32085`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

####### CHOICE-REFERENCE 类型引用

######## 1. EcuMFixedModuleConfigurationRef

- **UUID**: `d3638ed2-22f7-4783-a42d-b3eaffb1a94f`
- **引用名**: `EcuMFixedModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet`
  - `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg`
  - `/AUTOSAR/EcucDefs/CanNm/CanNmGlobalConfig`
  - `/AUTOSAR/EcucDefs/CanSM/CanSMConfiguration`
  - `/AUTOSAR/EcucDefs/CanTp/CanTpConfig`
  - `/AUTOSAR/EcucDefs/CanTrcv/CanTrcvConfigSet`
  - `/AUTOSAR/EcucDefs/Com/ComConfig`
  - `/AUTOSAR/EcucDefs/ComM/ComMConfigSet`
  - `/AUTOSAR/EcucDefs/Dbg/DbgMultipleConfigurationContainer`
  - `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet`
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig`
  - `/AUTOSAR/EcucDefs/Dlt/DltMultipleConfigurationContainer`
  - `/AUTOSAR/EcucDefs/Eep/EepInitConfiguration`
  - `/AUTOSAR/EcucDefs/Eth/EthConfigSet`
  - `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet`
  - `/AUTOSAR/EcucDefs/EthTrcv/EthTrcvConfigSet`
  - `/AUTOSAR/EcucDefs/FiM/FiMConfigSet`
  - `/AUTOSAR/EcucDefs/Fls/FlsConfigSet`
  - `/AUTOSAR/EcucDefs/FlsTst/FlsTstConfigSet`
  - `/AUTOSAR/EcucDefs/FrArTp/FrArTpMultipleConfig`
  - `/AUTOSAR/EcucDefs/FrIf/FrIfConfig`
  - `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration`
  - `/AUTOSAR/EcucDefs/FrNm/FrNmChannelConfig`
  - `/AUTOSAR/EcucDefs/FrSM/FrSMConfig`
  - `/AUTOSAR/EcucDefs/FrTp/FrTpMultipleConfig`
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet`
  - `/AUTOSAR/EcucDefs/IpduM/IpduMConfig`
  - `/AUTOSAR/EcucDefs/J1939Tp/J1939TpConfiguration`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig`
  - `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig`
  - `/AUTOSAR/EcucDefs/LinSM/LinSMConfigSet`
  - `/AUTOSAR/EcucDefs/LinTp/LinTpGlobalConfig`
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration`
  - `/AUTOSAR/EcucDefs/PduR/PduRRoutingTables`
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Rte/RtePostBuildVariantConfiguration`
  - `/AUTOSAR/EcucDefs/SoAd/SoAdDoIpConfig`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver`
  - `/AUTOSAR/EcucDefs/UdpNm/UdpNmGlobalConfig`
  - `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet`
  - `/AUTOSAR/EcucDefs/Wdg/WdgSettingsConfig`
  - `/AUTOSAR/EcucDefs/Xcp/XcpConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `fb8d3224-7d59-40cd-95fb-506fd83659f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 2. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 3. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `34e86c5c-325c-4c8a-a0be-924090309799`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

############ 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 5. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `1e6be767-c823-462f-883b-44e35803427e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFixedUser

- **UUID**: `4f888481-0e5c-4b78-a917-efa5be2607f4`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Parameter used to identify one user.

####### 6. EcuMTTII

**容器属性**:

- **UUID**: `8cf03107-d2a4-4430-84a7-1367a65ba24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Not used!

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMDivisor

- **UUID**: `0c4351ff-3f8d-48a6-a3a1-6615ddd79e1c`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the divisor pre load value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeRef

- **UUID**: `ef5fb3b7-b0b9-43e3-8ed2-ce549d68c07f`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

########## 2. EcuMSuccessorRef

- **UUID**: `735cd32e-6814-4de8-b8f9-ec9e61776be7`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

##### 14. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `fb8d3224-7d59-40cd-95fb-506fd83659f7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 15. EcuMDriverInitItem

**容器属性**:

- **UUID**: `8e87f35e-8af1-42c4-be54-58e5eee0f975`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `efd33a7d-c69a-4a81-90df-12505725d897`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `6991816d-1c9d-4c4a-80c0-7c7a3dea5716`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######## 3. EcuMAdditionalInitCode

- **UUID**: `0527f0e1-8347-4085-ba05-351c7f5a1831`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `267d9aac-5bce-4cc4-8e34-f794ed42d5e1`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 16. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `34e86c5c-325c-4c8a-a0be-924090309799`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

########## 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 17. EcuMDriverInitItem

**容器属性**:

- **UUID**: `a3c08bfe-b5d8-4f27-98e4-3ed04284be8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `6f04917e-cef6-4aef-bbe6-b296c56b3fe7`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `05e6128e-a9cd-45c0-b624-61b4dfd2f6f4`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######## 3. EcuMAdditionalInitCode

- **UUID**: `cda0c902-0796-4f2e-9234-4c613144c1f9`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `c56fd57b-e500-45f3-97c9-d0f212f224da`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 18. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `1e6be767-c823-462f-883b-44e35803427e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMFixedUser

- **UUID**: `4f888481-0e5c-4b78-a917-efa5be2607f4`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Parameter used to identify one user.

##### 19. EcuMTTII

**容器属性**:

- **UUID**: `8cf03107-d2a4-4430-84a7-1367a65ba24a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Not used!

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMDivisor

- **UUID**: `0c4351ff-3f8d-48a6-a3a1-6615ddd79e1c`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the divisor pre load value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSleepModeRef

- **UUID**: `ef5fb3b7-b0b9-43e3-8ed2-ce549d68c07f`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

######## 2. EcuMSuccessorRef

- **UUID**: `735cd32e-6814-4de8-b8f9-ec9e61776be7`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

##### 20. EcuMFlexConfiguration

**容器属性**:

- **UUID**: `c9abdd8d-c489-4883-883d-206a63f973f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexConfiguration`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the configuration (parameters) of the EcuMFlex.

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. EcuMGptChannelRef

- **UUID**: `6ca310b8-c477-4b63-87cf-1c5db1da9558`
- **引用名**: `EcuMGptChannelRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a GPT Channel which serves as the timebase for the EcuM Clock.The GPT Channel must be a Channel in GPT_CH_MODE_CONTINUOUS to guarantee permanent and exact counting of the EcuM clock.

######## 2. EcuMPartitionRef

- **UUID**: `b03b10b2-f932-4cb3-bbf7-4d6286d2e7b7`
- **引用名**: `EcuMPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..infinite]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference denotes the partition a EcuM and SchM shall run inside. 

Please note that in case of a multicore ECU this reference is mandatory and it is expected that the SchM and the EcuM run only once per core.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMNormalMcuModeRef

- **UUID**: `132fa71c-5870-4337-9f12-d7d4f3376463`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the normal MCU mode to be restored after a sleep.

####### CHOICE-REFERENCE 类型引用

######## 1. EcuMFlexModuleConfigurationRef

- **UUID**: `d085f9eb-9c47-48e4-a39c-a3d69910435b`
- **引用名**: `EcuMFlexModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Adc/AdcConfigSet`
  - `/AUTOSAR/EcucDefs/Can/CanConfigSet`
  - `/AUTOSAR/EcucDefs/Dem/DemConfigSet`
  - `/AUTOSAR/EcucDefs/Fls/FlsConfigSet`
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Icu/IcuConfigSet`
  - `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig`
  - `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration`
  - `/AUTOSAR/EcucDefs/Port/PortConfigSet`
  - `/AUTOSAR/EcucDefs/Pwm/PwmChannelConfigSet`
  - `/AUTOSAR/EcucDefs/Spi/SpiDriver`
  - `/AUTOSAR/EcucDefs/WdgM/WdgMConfigSet`
  - `/AUTOSAR/EcucDefs/Wdg/WdgSettingsConfig`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: References to the initialization structure of the corresponding BSW module.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. EcuMAlarmClock

**容器属性**:

- **UUID**: `01049a49-134d-4414-b6ec-8c33365bd8a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured alarm clocks.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMAlarmClockId

- **UUID**: `f4883b50-0ab1-4b73-a1e2-0a99d883060a`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This ID identifies this alarmclock.

######### FLOAT 类型参数

########## 1. EcuMAlarmClockTimeOut

- **UUID**: `06999a88-336b-470b-98eb-8c2b9b40266c`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows to define a timeout for this alarm clock.

Not Used

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMAlarmClockUser

- **UUID**: `67afb42c-6829-4796-96a6-4b3bcccb3a14`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows an alarm to be assigned to a user.

####### 2. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `90b51b5d-19e7-4fc9-b12c-f303d0620f41`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces. This container is only needed if the parameter EcuMEnableDefBehaviour is active.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFlexUser

- **UUID**: `1617e119-9dbb-4fda-acfc-a094e03da217`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier of the EcuMFlex user.

########## 2. EcuMGoDownRequestID

- **UUID**: `92b50b0c-a210-4d74-94e0-dad54d98d79e`
- **参数名**: `EcuMGoDownRequestID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `42`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the corresponding BSW or SWC ModuleID. The parameter is necessary to translate the caller ID of the API EcuM_GoDown into an EcuM_FlexUser ID.

This value depends on the configuration item EcuMEnableDefBehaviour. If (EcuMEnableDefBehaviour == true) then this parameter is optional configurable otherwise this parameter is ignored.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMFlexEcucPartitionRef

- **UUID**: `aa52827c-9105-403f-82fc-a4605817ca76`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..0]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!
Denotes in which "EcucPartition" the user of the EcuM is executed.

####### 3. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `c1453d6e-ec17-4cbd-8503-5db6c014135c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_GoDown API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMGoDownAllowedUserRef

- **UUID**: `d990691d-1ea9-4064-87c6-8bcd9dbef7fd`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_GoDown API. If a reference to an EcuM_User is set, this user must have a configured EcuMGoDownRequestID to translate the caller ID in the routine EcuM_GoDown.

####### 4. EcuMResetMode

**容器属性**:

- **UUID**: `3a7be8c5-e72c-4110-bdcc-8115e3bbf211`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured reset modes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMResetModeId

- **UUID**: `19e7a6e8-e504-482b-94eb-b70f0e2fe423`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier to be used in services like EcuM_SelectShutdownTarget.

####### 5. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `d9043323-9e03-4a73-abf6-ef24f97a90f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_SetClock API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSetClockAllowedUserRef

- **UUID**: `9ae28f79-117f-4e11-b200-5bd96786fbd8`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_SetClock API.

####### 6. EcuMShutdownCause

**容器属性**:

- **UUID**: `bd55945f-5876-43e5-bfde-ecf0b7afc657`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured shut down or reset causes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownCauseId

- **UUID**: `e84f9953-fe9d-4fcf-8fe0-a5836046deb3`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This values specifies the identifier for API calls for this shut down cause.

####### 7. EcuMShutdownTarget

**容器属性**:

- **UUID**: `8ccbec4c-d238-4e65-81e0-feeffc5257a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container is not used including the parameters.

These containers include the configured shut down targets.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownTargetId

- **UUID**: `959073ad-3b50-41a1-a53f-269b72c40b82`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier used for this shut down target in services like EcuM_SelectShutdownTarget.

####### 8. EcuMDriverInitListBswM

**容器属性**:

- **UUID**: `01820739-2c3d-45a2-9a3b-4926762ff2be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListBswM`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes a list of initialization items that will be handled after the BswM has been initialized.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

########## 参数配置

此容器包含 **4** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

############ 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

############ 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

############ 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

####### 9. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 21. EcuMAlarmClock

**容器属性**:

- **UUID**: `01049a49-134d-4414-b6ec-8c33365bd8a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured alarm clocks.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EcuMAlarmClockId

- **UUID**: `f4883b50-0ab1-4b73-a1e2-0a99d883060a`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This ID identifies this alarmclock.

####### FLOAT 类型参数

######## 1. EcuMAlarmClockTimeOut

- **UUID**: `06999a88-336b-470b-98eb-8c2b9b40266c`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows to define a timeout for this alarm clock.

Not Used

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMAlarmClockUser

- **UUID**: `67afb42c-6829-4796-96a6-4b3bcccb3a14`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter allows an alarm to be assigned to a user.

##### 22. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `90b51b5d-19e7-4fc9-b12c-f303d0620f41`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces. This container is only needed if the parameter EcuMEnableDefBehaviour is active.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EcuMFlexUser

- **UUID**: `1617e119-9dbb-4fda-acfc-a094e03da217`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier of the EcuMFlex user.

######## 2. EcuMGoDownRequestID

- **UUID**: `92b50b0c-a210-4d74-94e0-dad54d98d79e`
- **参数名**: `EcuMGoDownRequestID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `42`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the corresponding BSW or SWC ModuleID. The parameter is necessary to translate the caller ID of the API EcuM_GoDown into an EcuM_FlexUser ID.

This value depends on the configuration item EcuMEnableDefBehaviour. If (EcuMEnableDefBehaviour == true) then this parameter is optional configurable otherwise this parameter is ignored.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EcuMFlexEcucPartitionRef

- **UUID**: `aa52827c-9105-403f-82fc-a4605817ca76`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..0]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!
Denotes in which "EcucPartition" the user of the EcuM is executed.

##### 23. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `c1453d6e-ec17-4cbd-8503-5db6c014135c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_GoDown API.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMGoDownAllowedUserRef

- **UUID**: `d990691d-1ea9-4064-87c6-8bcd9dbef7fd`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_GoDown API. If a reference to an EcuM_User is set, this user must have a configured EcuMGoDownRequestID to translate the caller ID in the routine EcuM_GoDown.

##### 24. EcuMResetMode

**容器属性**:

- **UUID**: `3a7be8c5-e72c-4110-bdcc-8115e3bbf211`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured reset modes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMResetModeId

- **UUID**: `19e7a6e8-e504-482b-94eb-b70f0e2fe423`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier to be used in services like EcuM_SelectShutdownTarget.

##### 25. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `d9043323-9e03-4a73-abf6-ef24f97a90f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the collection of allowed users which are allowed to call the EcuM_SetClock API.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSetClockAllowedUserRef

- **UUID**: `9ae28f79-117f-4e11-b200-5bd96786fbd8`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: References to the users which are allowed to call the EcuM_SetClock API.

##### 26. EcuMShutdownCause

**容器属性**:

- **UUID**: `bd55945f-5876-43e5-bfde-ecf0b7afc657`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configured shut down or reset causes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMShutdownCauseId

- **UUID**: `e84f9953-fe9d-4fcf-8fe0-a5836046deb3`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This values specifies the identifier for API calls for this shut down cause.

##### 27. EcuMShutdownTarget

**容器属性**:

- **UUID**: `8ccbec4c-d238-4e65-81e0-feeffc5257a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container is not used including the parameters.

These containers include the configured shut down targets.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMShutdownTargetId

- **UUID**: `959073ad-3b50-41a1-a53f-269b72c40b82`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier used for this shut down target in services like EcuM_SelectShutdownTarget.

##### 28. EcuMDriverInitListBswM

**容器属性**:

- **UUID**: `01820739-2c3d-45a2-9a3b-4926762ff2be`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListBswM`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes a list of initialization items that will be handled after the BswM has been initialized.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

######## 参数配置

此容器包含 **4** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

########## 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

########## 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

########## 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 29. EcuMDriverInitItem

**容器属性**:

- **UUID**: `98199957-474e-49d2-bb7e-a011017fe990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [0..infinite]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These containers include the configuration of one initialization item. This may either be a module initialization function or any user defined code.

###### 参数配置

此容器包含 **4** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `993fe681-b643-49ba-a4cf-c941b8115998`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.  For user defined code given in EcuMAdditionalInitCode 'Code' has to be given.

######## 2. EcuMModuleService

- **UUID**: `fcb9f21b-7e95-4901-873e-a3651cedfe46`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the service to be called to initialize that module, e.g. Init, PreInit, Start etc. If the service is Init and the parameter EcuMModuleConfigurationRef has been set for that module, 
the corresponding pointer to the init structure (<Module>_ConfigType) and in case of multiple instantiation an uint8 value to identify the instance of the  module(<MSN>_CtrlIdx) are be passed as arguments.

######## 3. EcuMAdditionalInitCode

- **UUID**: `44f6516e-c901-44dc-94a2-ba09ff27bbe0`
- **参数名**: `EcuMAdditionalInitCode`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines an additional code in the callout function, e.g. Mcu_InitClock(). If this code needs other header files, they can be included via the parameter EcuMAdditionalIncludes. 

RESTRICTIONS: 'EcuMAdditionalInitCode' is only available, if 'EcuMModuleID' is set to 'Code'.

######## 4. EcuMModuleHeader

- **UUID**: `ac417f84-2673-4fdb-9b3c-a5755dfa6697`
- **参数名**: `EcuMModuleHeader`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines a header file needed for driver init items.

##### 30. EcuMFixedGeneral

**容器属性**:

- **UUID**: `9e9e2bd1-dc52-4660-933d-13478a923ff7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedGeneral`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container holds the general, pre-compile configuration parameters for the EcuMFixed.

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMIncludeComM

- **UUID**: `6ebc5d77-d9cd-44df-900d-eaebd800270d`
- **参数名**: `EcuMIncludeComM`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This configuration parameter defines whether the communication  manager is supported by EcuM. This feature is presented for development purpose to compile out the communication manager in the early debugging phase.

######## 2. EcuMIncludeNvM

- **UUID**: `d763ac38-0b91-41f4-adee-bfbaf7a3e06c`
- **参数名**: `EcuMIncludeNvM`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This configuration parameter defines whether the non volatile memory manager is supported by EcuM. This feature is presented for development purpose to compile out the volatile memory manager in the early debugging phase.

######## 3. EcuMIncludeNvramMgr

- **UUID**: `4d1e4599-baab-43d7-be20-d0a25311f538`
- **参数名**: `EcuMIncludeNvramMgr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This configuration parameter defines whether the non volatile memory manager is supported by EcuM. If this parameter is active, NvM_WriteAll() handling will be done by EcuM.

######## 4. EcuMTTIIEnabled

- **UUID**: `f1c2e610-a125-4b88-b73c-17b4ef0686d5`
- **参数名**: `EcuMTTIIEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

Boolean switch to enable / disable TTII

######## 5. EcuMIncludeRte

- **UUID**: `38b48fa1-2340-4825-9415-ede23dd6c904`
- **参数名**: `EcuMIncludeRte`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable/disables the use of the Rte.

######## 6. EcuMGenModeSwitchPort

- **UUID**: `3433e431-3207-49b2-83b8-af935d5306d1`
- **参数名**: `EcuMGenModeSwitchPort`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables the generation of the EcuM_CurrentMode sender-receiver interface within the SW-C description and the usage of a callback function for mode switch notification. If this parameter is set to ON the ECUM will use the provided RTE function Rte_Switch_currentMode_currentMode().

######## 7. EcuMModeSwitchRteAck

- **UUID**: `fb42c140-576a-4ee0-b793-a9b60a0b1705`
- **参数名**: `EcuMModeSwitchRteAck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables the synchronisation mechanism with RTE. In case this parameter is enabled, the EcuM waits on defined synchronistion points until the Rte switches into coresponding ECU mode. After receiving the ACK, EcuM will continue.

######## 8. EcuMIncludeDem

- **UUID**: `de5b3433-3992-4732-8706-d72d50321c45`
- **参数名**: `EcuMIncludeDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable/disables the use of the Dem.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMTTIIWakeupSourceRef

- **UUID**: `6e965ead-85e0-48ed-821e-5fce6597b359`
- **引用名**: `EcuMTTIIWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This configuration parameter references the initial sleep mode to be used by TTII when TTII is activated after a RUN mode.

##### 31. EcuMFlexGeneral

**容器属性**:

- **UUID**: `d4d26a7a-a9c1-4df5-846f-252f605ddcbb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexGeneral`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the EcuMFlex.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMAlarmClockPresent

- **UUID**: `e4476821-cb05-4ccd-b41f-fa75aac32a37`
- **参数名**: `EcuMAlarmClockPresent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This flag indicates whether the optional AlarmClock feature is present.

######## 2. EcuMEnableDefBehaviour

- **UUID**: `5272f4b8-6463-448c-a054-8b68976ec5e4`
- **参数名**: `EcuMEnableDefBehaviour`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines if the defensive behavior is enabled.

######## 3. EcuMResetLoopDetection

- **UUID**: `9f78510b-5c2b-4734-8f41-a5c7959c9948`
- **参数名**: `EcuMResetLoopDetection`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

If false, no reset loop detection is performed.

######## 4. EcuMModeHandling

- **UUID**: `f0e74e72-6a54-4ae6-b9d4-780d4bec128a`
- **参数名**: `EcuMModeHandling`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if the mode handling is enabled.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMAlarmWakeupSource

- **UUID**: `a2472941-40e2-46a2-98ea-34017daf85df`
- **引用名**: `EcuMAlarmWakeupSource`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter describes the reference to the EcuMWakeupSource being used for the EcuM AlarmClock.

##### 32. EcuMGeneral

**容器属性**:

- **UUID**: `600d55e8-c8b2-4a11-a1b9-2cfcd3e7a0a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

General configuration parameters of the ECUM.

###### 参数配置

此容器包含 **14** 个参数：

####### INTEGER 类型参数

######## 1. EcuMBswCoreId

- **UUID**: `e823ebb6-3279-4270-8d23-10b31828c481`
- **参数名**: `EcuMBswCoreId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies on which core the BSW shall run. This parameter is only relevant if more than one core is configured in the OS configuration.

####### BOOLEAN 类型参数

######## 1. EcuMDevErrorDetect

- **UUID**: `c8f3d760-c999-418e-95b9-c01af3d10b20`
- **参数名**: `EcuMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. EcuMIncludeDem

- **UUID**: `e1ea3892-dde3-44ff-8173-c83eae9a6d3c`
- **参数名**: `EcuMIncludeDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

This parameter defines if the header of the DEM module will be included within the source of the ECU State Manager.

######## 3. EcuMIncludeDet

- **UUID**: `7eada6dc-ef94-4f90-8679-7c02a21fbbc8`
- **参数名**: `EcuMIncludeDet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Not used!

If defined, the according BSW module will be initialized by the ECU State Manager

######## 4. EcuMVersionInfoApi

- **UUID**: `6f96cbdf-c476-4ebb-bd72-4b83749cd983`
- **参数名**: `EcuMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter enables/disables the function EcuM_GetVersionInfo() to get major, minor and patch version information.

######## 5. EcuMDeferredBswMNotification

- **UUID**: `2bf51d63-ecbd-4616-94a8-59ca9c59d27e`
- **参数名**: `EcuMDeferredBswMNotification`
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
- **描述**: Notification to the BswM via BswM_EcuM_CurrentWakeup is done immediate in the context of the EcuM API EcuM_SetWakeupEvent or EcuM_ValidateWakeupEvent. This APIs are often called in the context of an interrupt and the BswM notification will extend the interrupt runtime.

If the value is True, the notification will be done deferred in the next EcuM_MainFunction.

######## 6. EcuMSlaveCoreHandling

- **UUID**: `55c33327-7ac8-43dc-a340-81ae53c8f61f`
- **参数名**: `EcuMSlaveCoreHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter indicates if in case of a MultiCore Ecu the MasterCore synchronizes with the slave cores in sleep and off modes. If synchronization is active the MasterCore waits on the way to ECUM_STATE_SLEEP and ECUM_STATE_OFF till the SlaveCores has entered their state.

######## 7. EcuMEnableFixBehavior

- **UUID**: `f770761d-cd3d-4450-a293-4e098eaa5478`
- **参数名**: `EcuMEnableFixBehavior`
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
- **描述**: Enables or Disables the EcuM Fixed Behavior.

The EcuM Fixed Behavior does automatically control ECU phases like Startup / Run / PostRun / Sleep or Off.

######## 8. EcuMNonChannelWakeupInRun

- **UUID**: `a38e677e-4068-4890-aec3-927c39024eb3`
- **参数名**: `EcuMNonChannelWakeupInRun`
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
- **描述**: Allows wakeups for wakeup sources without referenced communication channel during the RUN phase. 

If this parameter is false, only wakeup sources with a communication channel refernce lead to a valid wakeup event.

######## 9. EcuMSchMStartInitialization

- **UUID**: `0ba19679-4eff-488b-9a8a-b894f369ea94`
- **参数名**: `EcuMSchMStartInitialization`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: In case that this parameter is set, the EcuM uses the SchM and BswM initialization sequence
SchM_Start(); SchM_Init(); BswM_Init(); SchM_StartTiming();
which uses additional SchM init functions defined in ASR 4.3.0 but keeps the old order of execution of SchM_Init and BswM_Init

If the parameter is false, the initialization sequence is
SchM_Init(); BswM_Init();

######## 10. EcuMSafeBswChecks

- **UUID**: `a63a1547-cbc8-4123-af4e-6b6b9c39fa62`
- **参数名**: `EcuMSafeBswChecks`
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
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects.

####### FLOAT 类型参数

######## 1. EcuMMainFunctionPeriod

- **UUID**: `9d30515b-76f9-48b5-9cfb-4a2e60aecd97`
- **参数名**: `EcuMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0.001..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the schedule period of EcuM_MainFunction.

####### STRING 类型参数

######## 1. EcuMAdditionalIncludes

- **UUID**: `df8bd383-75f1-4884-a62b-7a6ef9212972`
- **参数名**: `EcuMAdditionalIncludes`
- **数据类型**: STRING
- **多重性**: [0..*]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines header files needed for driver init lists.

######## 2. EcuMUserConfigurationFile

- **UUID**: `4e767ca5-c2cf-4f62-a08f-9ef83a1affed`
- **参数名**: `EcuMUserConfigurationFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external text file that will be included during generation to <Module>_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMGeneration

**容器属性**:

- **UUID**: `e0db28c6-e782-44f0-8485-b4be8c28f04b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module EcuM.

######## 参数配置

此容器包含 **3** 个参数：

######### BOOLEAN 类型参数

########## 1. EcuMOutOfBoundsWriteSanitizer

- **UUID**: `056bc29b-a3fa-43c6-86f2-cb9ed29d3133`
- **参数名**: `EcuMOutOfBoundsWriteSanitizer`
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
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

For more details, refer to TechnicalReference_ComStackLib.pdf

########## 2. EcuMOutOfBoundsReadSanitizer

- **UUID**: `8f9f6bb6-6a70-4c85-bd6f-852579a3f9d4`
- **参数名**: `EcuMOutOfBoundsReadSanitizer`
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

For more details, refer to TechnicalReference_ComStackLib.pdf

########## 3. EcuMInterfacesForDeactivatedData

- **UUID**: `5f216fc9-d7ab-4134-ac77-6135154e6bf6`
- **参数名**: `EcuMInterfacesForDeactivatedData`
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
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

For more details, refer to TechnicalReference_ComStackLib.pdf

##### 33. EcuMGeneration

**容器属性**:

- **UUID**: `e0db28c6-e782-44f0-8485-b4be8c28f04b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module EcuM.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMOutOfBoundsWriteSanitizer

- **UUID**: `056bc29b-a3fa-43c6-86f2-cb9ed29d3133`
- **参数名**: `EcuMOutOfBoundsWriteSanitizer`
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
- **描述**: This parameter activates/deactivates the generation of runtime checks which call a DET error notification function to find easily out of bounds write problems.

FALSE:  no checks are generated in the data access.
TRUE: the data access is enriched with DET checks to validate indexes.

For more details, refer to TechnicalReference_ComStackLib.pdf

######## 2. EcuMOutOfBoundsReadSanitizer

- **UUID**: `8f9f6bb6-6a70-4c85-bd6f-852579a3f9d4`
- **参数名**: `EcuMOutOfBoundsReadSanitizer`
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

For more details, refer to TechnicalReference_ComStackLib.pdf

######## 3. EcuMInterfacesForDeactivatedData

- **UUID**: `5f216fc9-d7ab-4134-ac77-6135154e6bf6`
- **参数名**: `EcuMInterfacesForDeactivatedData`
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
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

For more details, refer to TechnicalReference_ComStackLib.pdf

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 5

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **EcuM_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **EcuM**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **EcuM_Pre**
2. **EcuM_Rec**
3. **EcuM_Pre_Class1**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. EcuM_Impl

- **UUID**: `487e2e0d-92c2-4469-a75f-21e4b5b270a5`
- **实现名称**: `EcuM_Impl`
- **编程语言**: C
- **软件版本**: 15.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **3** 个配置：

### 1. EcuM_Pre

- **UUID**: `7ef575f0-c4a1-4921-82b4-4a4caa7d13fc`
- **配置名称**: `EcuM_Pre`
- **定义引用**: `/MICROSAR/EcuM`

### 2. EcuM_Rec

- **UUID**: `18c7aae7-d3e1-4a92-82a3-424e78f3d129`
- **配置名称**: `EcuM_Rec`
- **定义引用**: `/MICROSAR/EcuM`

### 3. EcuM_Pre_Class1

- **UUID**: `e9aceaf9-1117-4303-b0f8-9fd299607d22`
- **配置名称**: `EcuM_Pre_Class1`
- **定义引用**: `/MICROSAR/EcuM`
