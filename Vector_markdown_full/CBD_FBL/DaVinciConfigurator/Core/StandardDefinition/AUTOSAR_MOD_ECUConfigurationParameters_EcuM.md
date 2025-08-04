# EcuM - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:42

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EcuM](#ecum)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EcuM

#### 基本信息

- **UUID**: `ECUC:2cef58ce-79fe-4a40-935b-ee76b6a60605`
- **模块名称**: `EcuM`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD

#### 模块描述

Configuration of the EcuM (ECU State Manager) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **30** 个配置容器：

##### 1. EcuMConfiguration

**容器属性**:

- **UUID**: `ECUC:16fb469f-1f19-45e7-b4e5-555ae0f14089`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMConfiguration`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration (parameters) of the ECU State Manager.

###### 配置容器

本模块包含 **26** 个配置容器：

####### 1. EcuMCommonConfiguration

**容器属性**:

- **UUID**: `ECUC:8e610dbe-ea33-4a18-bca8-c4d70a9da2f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMCommonConfiguration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the common configuration (parameters) of the ECU State Manager.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMConfigConsistencyHash

- **UUID**: `ECUC:0bae5ee1-7bcc-4635-a400-d245750296dd`
- **参数名**: `EcuMConfigConsistencyHash`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-POST-BUILD
- **描述**: A hash value generated across all pre-compile and link-time parameters of all BSW modules. This hash value is compared against a field in the EcuM_ConfigType and hence allows checking the consistency of the entire configuration.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMDefaultAppMode

- **UUID**: `ECUC:65c6e769-6d64-4d96-8675-7983ccee0258`
- **引用名**: `EcuMDefaultAppMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: The default application mode loaded when the ECU comes out of reset.

########## 2. EcuMOSResource

- **UUID**: `ECUC:c2dcaae0-bc92-410f-bdb9-adf1d91ecffc`
- **引用名**: `EcuMOSResource`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a OS ressource which is used to bring the ECU into sleep mode.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `ECUC:aebde982-c84c-47f2-ac81-1989258cbaef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container describes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EcuMDefaultState

- **UUID**: `ECUC:ccac5543-c698-41bb-869a-fa1a6acbf26f`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EcuMStateOff` (来源: AUTOSAR_ECUC)
  - `EcuMStateReset` (来源: AUTOSAR_ECUC)
  - `EcuMStateSleep` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: This parameter describes the state part of the default shutdown target selected when the ECU comes out of reset. If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMDefaultResetModeRef

- **UUID**: `ECUC:68b39a3a-9e3c-40c0-8b2f-d30262687598`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

############ 2. EcuMDefaultSleepModeRef

- **UUID**: `ECUC:7cf854cf-a9cb-4ead-8eae-96bd1592bd0a`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

######### 2. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4f500e7d-fe92-4b94-8eed-941c9828f1aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

########## 引用关系

此容器包含 **3** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `ECUC:179e9f2b-bbea-4ec1-994c-cec0fe876e0e`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

############ 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `ECUC:112330d7-eec4-4496-8b57-5c65e6e0b079`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occured.

############ 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `ECUC:61a2ab39-ed3f-42e5-9ec4-2f9920eb091a`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occured.

######### 3. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `ECUC:e108fe98-dc5c-4f3c-9d9e-5a4989fb20d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block I.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 5. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `ECUC:320a0bfb-905f-484f-89cb-c8938c1921b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block 0.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 7. EcuMDriverRestartList

**容器属性**:

- **UUID**: `ECUC:a32e3888-bdad-4685-bcb5-18248c199379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

List of module IDs.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 9. EcuMSleepMode

**容器属性**:

- **UUID**: `ECUC:a9cbddde-5cd2-4616-9604-6041afbe9990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured sleep modes.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EcuMSleepModeId

- **UUID**: `ECUC:6575d26f-25a3-419a-a1f9-73e213842f07`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this sleep mode in services like EcuM_SelectShutdownTarget.

########### BOOLEAN 类型参数

############ 1. EcuMSleepModeSuspend

- **UUID**: `ECUC:3da7b115-6bc9-4855-a744-83e78ae2f17b`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Flag, which is set true, if the CPU is suspended, halted, or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSleepModeMcuModeRef

- **UUID**: `ECUC:f6907e19-209e-44bc-b8f4-08b7922a9adb`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the corresponding MCU mode for this sleep mode.

############ 2. EcuMWakeupSourceMask

- **UUID**: `ECUC:35ef3ce4-a034-4906-8400-3b4b02eaa0b8`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters are references to the wakeup sources that shall be enabled for this sleep mode.

######### 10. EcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:0a729dd6-2641-4d68-95a0-5a26ca418457`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured wakeup sources.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. EcuMWakeupSourceId

- **UUID**: `ECUC:bdc9686e-5683-43b0-95b2-0f1cd8114964`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the identifier of this wakeup source.

########### BOOLEAN 类型参数

############ 1. EcuMWakeupSourcePolling

- **UUID**: `ECUC:5af33790-8355-4594-8989-195b1e09d64a`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes if the wakeup source needs polling.

########### FLOAT 类型参数

############ 1. EcuMValidationTimeout

- **UUID**: `ECUC:db82044d-d3a9-40b9-a9f5-6d2f788d3266`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. The timeout is specified in seconds.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMComMChannelRef

- **UUID**: `ECUC:7ad19fd1-f48a-43da-9491-0efb37cd51df`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a Network (channel) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

############ 2. EcuMResetReasonRef

- **UUID**: `ECUC:be6be3ac-3dd8-4fb4-9890-c767597eb3ef`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes the mapping of reset reasons detected by the MCU driver into wakeup sources.

####### 2. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `ECUC:aebde982-c84c-47f2-ac81-1989258cbaef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container describes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EcuMDefaultState

- **UUID**: `ECUC:ccac5543-c698-41bb-869a-fa1a6acbf26f`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EcuMStateOff` (来源: AUTOSAR_ECUC)
  - `EcuMStateReset` (来源: AUTOSAR_ECUC)
  - `EcuMStateSleep` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: This parameter describes the state part of the default shutdown target selected when the ECU comes out of reset. If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMDefaultResetModeRef

- **UUID**: `ECUC:68b39a3a-9e3c-40c0-8b2f-d30262687598`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

########## 2. EcuMDefaultSleepModeRef

- **UUID**: `ECUC:7cf854cf-a9cb-4ead-8eae-96bd1592bd0a`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

####### 3. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4f500e7d-fe92-4b94-8eed-941c9828f1aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `ECUC:179e9f2b-bbea-4ec1-994c-cec0fe876e0e`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

########## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `ECUC:112330d7-eec4-4496-8b57-5c65e6e0b079`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occured.

########## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `ECUC:61a2ab39-ed3f-42e5-9ec4-2f9920eb091a`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occured.

####### 4. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `ECUC:e108fe98-dc5c-4f3c-9d9e-5a4989fb20d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block I.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 5. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 6. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `ECUC:320a0bfb-905f-484f-89cb-c8938c1921b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block 0.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 7. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 8. EcuMDriverRestartList

**容器属性**:

- **UUID**: `ECUC:a32e3888-bdad-4685-bcb5-18248c199379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

List of module IDs.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 9. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 10. EcuMSleepMode

**容器属性**:

- **UUID**: `ECUC:a9cbddde-5cd2-4616-9604-6041afbe9990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured sleep modes.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMSleepModeId

- **UUID**: `ECUC:6575d26f-25a3-419a-a1f9-73e213842f07`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this sleep mode in services like EcuM_SelectShutdownTarget.

######### BOOLEAN 类型参数

########## 1. EcuMSleepModeSuspend

- **UUID**: `ECUC:3da7b115-6bc9-4855-a744-83e78ae2f17b`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Flag, which is set true, if the CPU is suspended, halted, or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeMcuModeRef

- **UUID**: `ECUC:f6907e19-209e-44bc-b8f4-08b7922a9adb`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the corresponding MCU mode for this sleep mode.

########## 2. EcuMWakeupSourceMask

- **UUID**: `ECUC:35ef3ce4-a034-4906-8400-3b4b02eaa0b8`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters are references to the wakeup sources that shall be enabled for this sleep mode.

####### 11. EcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:0a729dd6-2641-4d68-95a0-5a26ca418457`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured wakeup sources.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EcuMWakeupSourceId

- **UUID**: `ECUC:bdc9686e-5683-43b0-95b2-0f1cd8114964`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the identifier of this wakeup source.

######### BOOLEAN 类型参数

########## 1. EcuMWakeupSourcePolling

- **UUID**: `ECUC:5af33790-8355-4594-8989-195b1e09d64a`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes if the wakeup source needs polling.

######### FLOAT 类型参数

########## 1. EcuMValidationTimeout

- **UUID**: `ECUC:db82044d-d3a9-40b9-a9f5-6d2f788d3266`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. The timeout is specified in seconds.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMChannelRef

- **UUID**: `ECUC:7ad19fd1-f48a-43da-9491-0efb37cd51df`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a Network (channel) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

########## 2. EcuMResetReasonRef

- **UUID**: `ECUC:be6be3ac-3dd8-4fb4-9890-c767597eb3ef`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes the mapping of reset reasons detected by the MCU driver into wakeup sources.

####### 12. EcuMFixedConfiguration

**容器属性**:

- **UUID**: `ECUC:df793d0e-5c7f-4d1f-bbfe-b2caf6cf9d01`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the EcuMFixed.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. EcuMNvramReadallTimeout

- **UUID**: `ECUC:18ebaefe-ddcf-47af-afa4-e15ec35d34b2`
- **参数名**: `EcuMNvramReadallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll job of the NVRAM Manager as failed.

########## 2. EcuMNvramWriteallTimeout

- **UUID**: `ECUC:e0d3746c-c2d8-4c81-b84b-83d3b7476c03`
- **参数名**: `EcuMNvramWriteallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a WriteAll job of the NVRAM Manager as failed.

########## 3. EcuMRunMinimumDuration

- **UUID**: `ECUC:a4efee28-153a-4570-b592-7f3b06c25f7d`
- **参数名**: `EcuMRunMinimumDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Duration given in seconds for which the ECU State Manager will

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMCommunicationAllowedList

- **UUID**: `ECUC:c1f1e7ec-cac9-4949-921e-cbc8701996a8`
- **引用名**: `EcuMComMCommunicationAllowedList`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the ComMChannels for which EcuM has to call ComM_CommunicationAllowed.

########## 2. EcuMNormalMcuModeRef

- **UUID**: `ECUC:da472057-880c-4613-9d87-e4d06c173ae6`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

######### CHOICE-REFERENCE 类型引用

########## 1. EcuMFixedModuleConfigurationRef

- **UUID**: `ECUC:339c0a67-2745-468f-84b9-50ce45393058`
- **引用名**: `EcuMFixedModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
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
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `ECUC:a83f64ee-812b-4e3b-b0d6-c4f289040010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 2. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 3. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `ECUC:0f68e708-3206-4ec1-9bd7-c829398045a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

############ 参数配置

此容器包含 **2** 个参数：

############# STRING 类型参数

############## 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############## 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

######### 5. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `ECUC:6b792715-f9f3-4d2e-a927-5b9685082fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMFixedUser

- **UUID**: `ECUC:08fe9652-c3bc-4795-87d0-6a44d67c541e`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

######### 6. EcuMTTII

**容器属性**:

- **UUID**: `ECUC:f21cd27b-2d15-499c-861f-6495cccfc5ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMDivisor

- **UUID**: `ECUC:a3491391-905c-4db0-833b-00a997c65d1f`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the divisor preload value.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSleepModeRef

- **UUID**: `ECUC:b2b38b93-dca9-4b83-8eb5-a18d722c300d`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

############ 2. EcuMSuccessorRef

- **UUID**: `ECUC:e0264bd4-2ca3-42fc-b149-44a8d3014a41`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

####### 13. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `ECUC:a83f64ee-812b-4e3b-b0d6-c4f289040010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 14. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 15. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `ECUC:0f68e708-3206-4ec1-9bd7-c829398045a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 16. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 17. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `ECUC:6b792715-f9f3-4d2e-a927-5b9685082fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFixedUser

- **UUID**: `ECUC:08fe9652-c3bc-4795-87d0-6a44d67c541e`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

####### 18. EcuMTTII

**容器属性**:

- **UUID**: `ECUC:f21cd27b-2d15-499c-861f-6495cccfc5ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMDivisor

- **UUID**: `ECUC:a3491391-905c-4db0-833b-00a997c65d1f`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the divisor preload value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeRef

- **UUID**: `ECUC:b2b38b93-dca9-4b83-8eb5-a18d722c300d`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

########## 2. EcuMSuccessorRef

- **UUID**: `ECUC:e0264bd4-2ca3-42fc-b149-44a8d3014a41`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

####### 19. EcuMFlexConfiguration

**容器属性**:

- **UUID**: `ECUC:e088e752-6fde-4e09-9190-f0619180e9b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the EcuMFlex.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMNormalMcuModeRef

- **UUID**: `ECUC:ef0eb80f-8127-45a4-8e24-04744d48a5f8`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

######### CHOICE-REFERENCE 类型引用

########## 1. EcuMFlexModuleConfigurationRef

- **UUID**: `ECUC:e927b74c-cd3f-496d-b60a-2e1d8628e268`
- **引用名**: `EcuMFlexModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
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
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. EcuMAlarmClock

**容器属性**:

- **UUID**: `ECUC:750dd6de-13ec-48cf-befd-615fde9145b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured alarm clocks.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EcuMAlarmClockId

- **UUID**: `ECUC:49861b32-83d2-464f-afd2-24fb12a3e1e0`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this alarmclock.

########### FLOAT 类型参数

############ 1. EcuMAlarmClockTimeOut

- **UUID**: `ECUC:9677f083-e76f-486e-8634-df1555753290`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows to define a timout for this alarm clock.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMAlarmClockUser

- **UUID**: `ECUC:e6ff4bc0-7648-4128-b239-de3f273d33d2`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows an alarm to be assigned to a user.

######### 2. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `ECUC:3058925d-af3b-4a8a-9252-bd6700407009`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMFlexUser

- **UUID**: `ECUC:7cefee01-1e46-45e6-b582-678888f226cc`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. EcuMFlexEcucPartitionRef

- **UUID**: `ECUC:fe138ccd-1882-4c4c-ad96-ce9be41c7a07`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Denotes in which "EcucPartition" the user of the EcuM is executed.

######### 3. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `ECUC:7d3d53a3-4f3d-4595-9bd9-4c2e42819a48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_GoDown API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMGoDownAllowedUserRef

- **UUID**: `ECUC:79119397-b629-4210-a818-6071972fb77f`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_GoDown API.

######### 4. EcuMResetMode

**容器属性**:

- **UUID**: `ECUC:f2f88c2c-79a4-47d4-8e3a-750f1bb3624e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured reset modes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMResetModeId

- **UUID**: `ECUC:0a945601-d809-4f20-9ffe-e90e4d9a60a4`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this reset mode in services like EcuM_SelectShutdownTarget.

######### 5. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `ECUC:b2941bdd-11fe-440e-a773-bce84948a4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_SetClock API.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EcuMSetClockAllowedUserRef

- **UUID**: `ECUC:6c8dce8f-f2da-4d1f-9a06-da9d9829e14e`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_SetClock API.

######### 6. EcuMShutdownCause

**容器属性**:

- **UUID**: `ECUC:76c32704-2514-4828-a00c-c26c6ae45534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down or reset causes.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMShutdownCauseId

- **UUID**: `ECUC:596b234d-0197-46f6-87ee-f6a25635fa91`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down cause.

######### 7. EcuMShutdownTarget

**容器属性**:

- **UUID**: `ECUC:e55d1cfa-47ca-42b7-a22c-38a105284cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down targets.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. EcuMShutdownTargetId

- **UUID**: `ECUC:0d27bade-16c3-4e3e-bbff-b6cf696e01b8`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down target in services like EcuM_SelectShutdownTarget.

####### 20. EcuMAlarmClock

**容器属性**:

- **UUID**: `ECUC:750dd6de-13ec-48cf-befd-615fde9145b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured alarm clocks.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMAlarmClockId

- **UUID**: `ECUC:49861b32-83d2-464f-afd2-24fb12a3e1e0`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this alarmclock.

######### FLOAT 类型参数

########## 1. EcuMAlarmClockTimeOut

- **UUID**: `ECUC:9677f083-e76f-486e-8634-df1555753290`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows to define a timout for this alarm clock.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMAlarmClockUser

- **UUID**: `ECUC:e6ff4bc0-7648-4128-b239-de3f273d33d2`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows an alarm to be assigned to a user.

####### 21. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `ECUC:3058925d-af3b-4a8a-9252-bd6700407009`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFlexUser

- **UUID**: `ECUC:7cefee01-1e46-45e6-b582-678888f226cc`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMFlexEcucPartitionRef

- **UUID**: `ECUC:fe138ccd-1882-4c4c-ad96-ce9be41c7a07`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Denotes in which "EcucPartition" the user of the EcuM is executed.

####### 22. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `ECUC:7d3d53a3-4f3d-4595-9bd9-4c2e42819a48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_GoDown API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMGoDownAllowedUserRef

- **UUID**: `ECUC:79119397-b629-4210-a818-6071972fb77f`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_GoDown API.

####### 23. EcuMResetMode

**容器属性**:

- **UUID**: `ECUC:f2f88c2c-79a4-47d4-8e3a-750f1bb3624e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured reset modes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMResetModeId

- **UUID**: `ECUC:0a945601-d809-4f20-9ffe-e90e4d9a60a4`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this reset mode in services like EcuM_SelectShutdownTarget.

####### 24. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `ECUC:b2941bdd-11fe-440e-a773-bce84948a4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_SetClock API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSetClockAllowedUserRef

- **UUID**: `ECUC:6c8dce8f-f2da-4d1f-9a06-da9d9829e14e`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_SetClock API.

####### 25. EcuMShutdownCause

**容器属性**:

- **UUID**: `ECUC:76c32704-2514-4828-a00c-c26c6ae45534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down or reset causes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownCauseId

- **UUID**: `ECUC:596b234d-0197-46f6-87ee-f6a25635fa91`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down cause.

####### 26. EcuMShutdownTarget

**容器属性**:

- **UUID**: `ECUC:e55d1cfa-47ca-42b7-a22c-38a105284cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down targets.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownTargetId

- **UUID**: `ECUC:0d27bade-16c3-4e3e-bbff-b6cf696e01b8`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down target in services like EcuM_SelectShutdownTarget.

##### 2. EcuMCommonConfiguration

**容器属性**:

- **UUID**: `ECUC:8e610dbe-ea33-4a18-bca8-c4d70a9da2f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMCommonConfiguration`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the common configuration (parameters) of the ECU State Manager.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMConfigConsistencyHash

- **UUID**: `ECUC:0bae5ee1-7bcc-4635-a400-d245750296dd`
- **参数名**: `EcuMConfigConsistencyHash`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-POST-BUILD
- **描述**: A hash value generated across all pre-compile and link-time parameters of all BSW modules. This hash value is compared against a field in the EcuM_ConfigType and hence allows checking the consistency of the entire configuration.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. EcuMDefaultAppMode

- **UUID**: `ECUC:65c6e769-6d64-4d96-8675-7983ccee0258`
- **引用名**: `EcuMDefaultAppMode`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsAppMode`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAppMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: The default application mode loaded when the ECU comes out of reset.

######## 2. EcuMOSResource

- **UUID**: `ECUC:c2dcaae0-bc92-410f-bdb9-adf1d91ecffc`
- **引用名**: `EcuMOSResource`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `OsResource`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsResource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a OS ressource which is used to bring the ECU into sleep mode.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `ECUC:aebde982-c84c-47f2-ac81-1989258cbaef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container describes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EcuMDefaultState

- **UUID**: `ECUC:ccac5543-c698-41bb-869a-fa1a6acbf26f`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EcuMStateOff` (来源: AUTOSAR_ECUC)
  - `EcuMStateReset` (来源: AUTOSAR_ECUC)
  - `EcuMStateSleep` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: This parameter describes the state part of the default shutdown target selected when the ECU comes out of reset. If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMDefaultResetModeRef

- **UUID**: `ECUC:68b39a3a-9e3c-40c0-8b2f-d30262687598`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

########## 2. EcuMDefaultSleepModeRef

- **UUID**: `ECUC:7cf854cf-a9cb-4ead-8eae-96bd1592bd0a`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

####### 2. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4f500e7d-fe92-4b94-8eed-941c9828f1aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **3** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `ECUC:179e9f2b-bbea-4ec1-994c-cec0fe876e0e`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

########## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `ECUC:112330d7-eec4-4496-8b57-5c65e6e0b079`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occured.

########## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `ECUC:61a2ab39-ed3f-42e5-9ec4-2f9920eb091a`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occured.

####### 3. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `ECUC:e108fe98-dc5c-4f3c-9d9e-5a4989fb20d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block I.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 5. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `ECUC:320a0bfb-905f-484f-89cb-c8938c1921b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block 0.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 7. EcuMDriverRestartList

**容器属性**:

- **UUID**: `ECUC:a32e3888-bdad-4685-bcb5-18248c199379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

List of module IDs.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 9. EcuMSleepMode

**容器属性**:

- **UUID**: `ECUC:a9cbddde-5cd2-4616-9604-6041afbe9990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured sleep modes.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMSleepModeId

- **UUID**: `ECUC:6575d26f-25a3-419a-a1f9-73e213842f07`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this sleep mode in services like EcuM_SelectShutdownTarget.

######### BOOLEAN 类型参数

########## 1. EcuMSleepModeSuspend

- **UUID**: `ECUC:3da7b115-6bc9-4855-a744-83e78ae2f17b`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Flag, which is set true, if the CPU is suspended, halted, or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeMcuModeRef

- **UUID**: `ECUC:f6907e19-209e-44bc-b8f4-08b7922a9adb`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the corresponding MCU mode for this sleep mode.

########## 2. EcuMWakeupSourceMask

- **UUID**: `ECUC:35ef3ce4-a034-4906-8400-3b4b02eaa0b8`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters are references to the wakeup sources that shall be enabled for this sleep mode.

####### 10. EcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:0a729dd6-2641-4d68-95a0-5a26ca418457`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured wakeup sources.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. EcuMWakeupSourceId

- **UUID**: `ECUC:bdc9686e-5683-43b0-95b2-0f1cd8114964`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the identifier of this wakeup source.

######### BOOLEAN 类型参数

########## 1. EcuMWakeupSourcePolling

- **UUID**: `ECUC:5af33790-8355-4594-8989-195b1e09d64a`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes if the wakeup source needs polling.

######### FLOAT 类型参数

########## 1. EcuMValidationTimeout

- **UUID**: `ECUC:db82044d-d3a9-40b9-a9f5-6d2f788d3266`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. The timeout is specified in seconds.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMComMChannelRef

- **UUID**: `ECUC:7ad19fd1-f48a-43da-9491-0efb37cd51df`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a Network (channel) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

########## 2. EcuMResetReasonRef

- **UUID**: `ECUC:be6be3ac-3dd8-4fb4-9890-c767597eb3ef`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes the mapping of reset reasons detected by the MCU driver into wakeup sources.

##### 3. EcuMDefaultShutdownTarget

**容器属性**:

- **UUID**: `ECUC:aebde982-c84c-47f2-ac81-1989258cbaef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDefaultShutdownTarget`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container describes the default shutdown target to be selected by EcuM. The actual shutdown target may be overridden by the EcuM_SelectShutdownTarget service.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EcuMDefaultState

- **UUID**: `ECUC:ccac5543-c698-41bb-869a-fa1a6acbf26f`
- **参数名**: `EcuMDefaultState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EcuMStateOff` (来源: AUTOSAR_ECUC)
  - `EcuMStateReset` (来源: AUTOSAR_ECUC)
  - `EcuMStateSleep` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: This parameter describes the state part of the default shutdown target selected when the ECU comes out of reset. If EcuMStateSleep is selected, the parameter EcuMDefaultSleepModeRef selects the specific sleep mode.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMDefaultResetModeRef

- **UUID**: `ECUC:68b39a3a-9e3c-40c0-8b2f-d30262687598`
- **引用名**: `EcuMDefaultResetModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMResetMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMResetMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateReset, this parameter selects the default reset mode. Otherwise this parameter may be ignored.

######## 2. EcuMDefaultSleepModeRef

- **UUID**: `ECUC:7cf854cf-a9cb-4ead-8eae-96bd1592bd0a`
- **引用名**: `EcuMDefaultSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: If EcuMDefaultShutdownTarget is EcuMStateSleep, this parameter selects the default sleep mode. Otherwise this parameter may be ignored.

##### 4. EcuMDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:4f500e7d-fe92-4b94-8eed-941c9828f1aa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ECUM_E_ALL_RUN_REQUESTS_KILLED

- **UUID**: `ECUC:179e9f2b-bbea-4ec1-994c-cec0fe876e0e`
- **引用名**: `ECUM_E_ALL_RUN_REQUESTS_KILLED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_ALL_RUN_REQUESTS_KILLED" has occured.

######## 2. ECUM_E_CONFIGURATION_DATA_INCONSISTENT

- **UUID**: `ECUC:112330d7-eec4-4496-8b57-5c65e6e0b079`
- **引用名**: `ECUM_E_CONFIGURATION_DATA_INCONSISTENT`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_CONFIGURATION_DATA_INCONSISTENT" has occured.

######## 3. ECUM_E_RAM_CHECK_FAILED

- **UUID**: `ECUC:61a2ab39-ed3f-42e5-9ec4-2f9920eb091a`
- **引用名**: `ECUM_E_RAM_CHECK_FAILED`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Reference to the DemEventParameter which shall be issued when the error "ECUM_E_RAM_CHECK_FAILED" has occured.

##### 5. EcuMDriverInitListOne

**容器属性**:

- **UUID**: `ECUC:e108fe98-dc5c-4f3c-9d9e-5a4989fb20d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListOne`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block I.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 6. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:b37908f7-5536-96bf-545e-fa7e8d6d11e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `ECUC:d3117de4-d573-e62d-12aa-c0febc0b1cc6`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `ECUC:f7b11899-50e8-e38b-ef40-30412ee7e758`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 7. EcuMDriverInitListZero

**容器属性**:

- **UUID**: `ECUC:320a0bfb-905f-484f-89cb-c8938c1921b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListZero`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block 0.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 8. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:047a165a-0939-8fd2-408c-68c88f8b12c4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `ECUC:24128b47-8976-df40-fed8-2f48be291daa`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `ECUC:48b225fc-04eb-dc9e-db6d-9e8b3105e83c`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 9. EcuMDriverRestartList

**容器属性**:

- **UUID**: `ECUC:a32e3888-bdad-4685-bcb5-18248c199379`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverRestartList`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

List of module IDs.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 10. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:759e42e7-3687-8e08-7375-b8598f8b8489`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `ECUC:9536b7d4-b6c4-dd76-31c1-7ed9be298f6f`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `ECUC:b9d65289-3239-dad4-0e56-ee1c31065a01`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 11. EcuMSleepMode

**容器属性**:

- **UUID**: `ECUC:a9cbddde-5cd2-4616-9604-6041afbe9990`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSleepMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured sleep modes.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EcuMSleepModeId

- **UUID**: `ECUC:6575d26f-25a3-419a-a1f9-73e213842f07`
- **参数名**: `EcuMSleepModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this sleep mode in services like EcuM_SelectShutdownTarget.

####### BOOLEAN 类型参数

######## 1. EcuMSleepModeSuspend

- **UUID**: `ECUC:3da7b115-6bc9-4855-a744-83e78ae2f17b`
- **参数名**: `EcuMSleepModeSuspend`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Flag, which is set true, if the CPU is suspended, halted, or powered off in the sleep mode. If the CPU keeps running in this sleep mode, then this flag must be set to false.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSleepModeMcuModeRef

- **UUID**: `ECUC:f6907e19-209e-44bc-b8f4-08b7922a9adb`
- **引用名**: `EcuMSleepModeMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the corresponding MCU mode for this sleep mode.

######## 2. EcuMWakeupSourceMask

- **UUID**: `ECUC:35ef3ce4-a034-4906-8400-3b4b02eaa0b8`
- **引用名**: `EcuMWakeupSourceMask`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters are references to the wakeup sources that shall be enabled for this sleep mode.

##### 12. EcuMWakeupSource

**容器属性**:

- **UUID**: `ECUC:0a729dd6-2641-4d68-95a0-5a26ca418457`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMWakeupSource`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured wakeup sources.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. EcuMWakeupSourceId

- **UUID**: `ECUC:bdc9686e-5683-43b0-95b2-0f1cd8114964`
- **参数名**: `EcuMWakeupSourceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the identifier of this wakeup source.

####### BOOLEAN 类型参数

######## 1. EcuMWakeupSourcePolling

- **UUID**: `ECUC:5af33790-8355-4594-8989-195b1e09d64a`
- **参数名**: `EcuMWakeupSourcePolling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes if the wakeup source needs polling.

####### FLOAT 类型参数

######## 1. EcuMValidationTimeout

- **UUID**: `ECUC:db82044d-d3a9-40b9-a9f5-6d2f788d3266`
- **参数名**: `EcuMValidationTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The validation timeout (period for which the ECU State Manager will wait for the validation of a wakeup event) can be defined for each wakeup source independently. The timeout is specified in seconds.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMComMChannelRef

- **UUID**: `ECUC:7ad19fd1-f48a-43da-9491-0efb37cd51df`
- **引用名**: `EcuMComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to a Network (channel) defined in the Communication Manager. No reference indicates that the wakeup source is not a communication channel.

######## 2. EcuMResetReasonRef

- **UUID**: `ECUC:be6be3ac-3dd8-4fb4-9890-c767597eb3ef`
- **引用名**: `EcuMResetReasonRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuResetReasonConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuPublishedInformation/McuResetReasonConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes the mapping of reset reasons detected by the MCU driver into wakeup sources.

##### 13. EcuMFixedConfiguration

**容器属性**:

- **UUID**: `ECUC:df793d0e-5c7f-4d1f-bbfe-b2caf6cf9d01`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the EcuMFixed.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. EcuMNvramReadallTimeout

- **UUID**: `ECUC:18ebaefe-ddcf-47af-afa4-e15ec35d34b2`
- **参数名**: `EcuMNvramReadallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a ReadAll job of the NVRAM Manager as failed.

######## 2. EcuMNvramWriteallTimeout

- **UUID**: `ECUC:e0d3746c-c2d8-4c81-b84b-83d3b7476c03`
- **参数名**: `EcuMNvramWriteallTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Period given in seconds for which the ECU State Manager will wait until it considers a WriteAll job of the NVRAM Manager as failed.

######## 3. EcuMRunMinimumDuration

- **UUID**: `ECUC:a4efee28-153a-4570-b592-7f3b06c25f7d`
- **参数名**: `EcuMRunMinimumDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: Duration given in seconds for which the ECU State Manager will

###### 引用关系

此容器包含 **3** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMComMCommunicationAllowedList

- **UUID**: `ECUC:c1f1e7ec-cac9-4949-921e-cbc8701996a8`
- **引用名**: `EcuMComMCommunicationAllowedList`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the ComMChannels for which EcuM has to call ComM_CommunicationAllowed.

######## 2. EcuMNormalMcuModeRef

- **UUID**: `ECUC:da472057-880c-4613-9d87-e4d06c173ae6`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

####### CHOICE-REFERENCE 类型引用

######## 1. EcuMFixedModuleConfigurationRef

- **UUID**: `ECUC:339c0a67-2745-468f-84b9-50ce45393058`
- **引用名**: `EcuMFixedModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
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
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `ECUC:a83f64ee-812b-4e3b-b0d6-c4f289040010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 2. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 3. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `ECUC:0f68e708-3206-4ec1-9bd7-c829398045a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

########## 参数配置

此容器包含 **2** 个参数：

########### STRING 类型参数

############ 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

############ 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 4. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

####### 5. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `ECUC:6b792715-f9f3-4d2e-a927-5b9685082fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFixedUser

- **UUID**: `ECUC:08fe9652-c3bc-4795-87d0-6a44d67c541e`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

####### 6. EcuMTTII

**容器属性**:

- **UUID**: `ECUC:f21cd27b-2d15-499c-861f-6495cccfc5ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMDivisor

- **UUID**: `ECUC:a3491391-905c-4db0-833b-00a997c65d1f`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the divisor preload value.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSleepModeRef

- **UUID**: `ECUC:b2b38b93-dca9-4b83-8eb5-a18d722c300d`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

########## 2. EcuMSuccessorRef

- **UUID**: `ECUC:e0264bd4-2ca3-42fc-b149-44a8d3014a41`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

##### 14. EcuMDriverInitListThree

**容器属性**:

- **UUID**: `ECUC:a83f64ee-812b-4e3b-b0d6-c4f289040010`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListThree`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block III.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 15. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:7aaf6f4c-fa05-95be-6797-65278c75f120`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `ECUC:9a47e43a-7a42-e52c-25e3-2ba7bb13fc06`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `ECUC:bee77eee-f5b7-e28a-0278-9aea2df0c698`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 16. EcuMDriverInitListTwo

**容器属性**:

- **UUID**: `ECUC:0f68e708-3206-4ec1-9bd7-c829398045a8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitListTwo`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for Init Block II.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

######## 参数配置

此容器包含 **2** 个参数：

######### STRING 类型参数

########## 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

########## 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 17. EcuMDriverInitItem

**容器属性**:

- **UUID**: `ECUC:e1d8f166-aae0-9644-5298-685e3cf236b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMDriverInitItem`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the entries in a driver init list.

###### 参数配置

此容器包含 **2** 个参数：

####### STRING 类型参数

######## 1. EcuMModuleID

- **UUID**: `ECUC:01716654-2b1d-e5b2-10e4-2ede6b90419e`
- **参数名**: `EcuMModuleID`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Short name of the module to be initialized, e.g. Mcu, Gpt etc.

######## 2. EcuMModuleService

- **UUID**: `ECUC:26110108-a692-e310-ed79-9e20de6d0c30`
- **参数名**: `EcuMModuleService`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: The service to be called to initialize that module, e.g. Init, PreInit, Start etc.

##### 18. EcuMFixedUserConfig

**容器属性**:

- **UUID**: `ECUC:6b792715-f9f3-4d2e-a927-5b9685082fbc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which is designated to request the RUN state. Application requestors refer to entities above RTE, system requestors to entities below RTE (e.g. Communication Manager).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMFixedUser

- **UUID**: `ECUC:08fe9652-c3bc-4795-87d0-6a44d67c541e`
- **参数名**: `EcuMFixedUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

##### 19. EcuMTTII

**容器属性**:

- **UUID**: `ECUC:f21cd27b-2d15-499c-861f-6495cccfc5ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMTTII`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the structures and the following configuration items describe its elements. These structures are concatenated to build a list as indicated by Figure 27 - Configuration Container Diagram.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMDivisor

- **UUID**: `ECUC:a3491391-905c-4db0-833b-00a997c65d1f`
- **参数名**: `EcuMDivisor`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..18446744073709551615]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the divisor preload value.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSleepModeRef

- **UUID**: `ECUC:b2b38b93-dca9-4b83-8eb5-a18d722c300d`
- **引用名**: `EcuMSleepModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter is a reference to a configured sleep mode that is used for TTII.

######## 2. EcuMSuccessorRef

- **UUID**: `ECUC:e0264bd4-2ca3-42fc-b149-44a8d3014a41`
- **引用名**: `EcuMSuccessorRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMSleepMode`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMSleepMode`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the next sleep mode in the TTII protocol.

##### 20. EcuMFlexConfiguration

**容器属性**:

- **UUID**: `ECUC:e088e752-6fde-4e09-9190-f0619180e9b4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the EcuMFlex.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMNormalMcuModeRef

- **UUID**: `ECUC:ef0eb80f-8127-45a4-8e24-04744d48a5f8`
- **引用名**: `EcuMNormalMcuModeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `McuModeSettingConf`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuModeSettingConf`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter is a reference to the normal MCU mode to be restored after a sleep.

####### CHOICE-REFERENCE 类型引用

######## 1. EcuMFlexModuleConfigurationRef

- **UUID**: `ECUC:e927b74c-cd3f-496d-b60a-2e1d8628e268`
- **引用名**: `EcuMFlexModuleConfigurationRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
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
  - POST-BUILD: VARIANT-POST-BUILD
- **描述**: These parameters contain references to the init structure of the corresponding BSW module.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. EcuMAlarmClock

**容器属性**:

- **UUID**: `ECUC:750dd6de-13ec-48cf-befd-615fde9145b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured alarm clocks.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EcuMAlarmClockId

- **UUID**: `ECUC:49861b32-83d2-464f-afd2-24fb12a3e1e0`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this alarmclock.

######### FLOAT 类型参数

########## 1. EcuMAlarmClockTimeOut

- **UUID**: `ECUC:9677f083-e76f-486e-8634-df1555753290`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows to define a timout for this alarm clock.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMAlarmClockUser

- **UUID**: `ECUC:e6ff4bc0-7648-4128-b239-de3f273d33d2`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows an alarm to be assigned to a user.

####### 2. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `ECUC:3058925d-af3b-4a8a-9252-bd6700407009`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMFlexUser

- **UUID**: `ECUC:7cefee01-1e46-45e6-b582-678888f226cc`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EcuMFlexEcucPartitionRef

- **UUID**: `ECUC:fe138ccd-1882-4c4c-ad96-ce9be41c7a07`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Denotes in which "EcucPartition" the user of the EcuM is executed.

####### 3. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `ECUC:7d3d53a3-4f3d-4595-9bd9-4c2e42819a48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_GoDown API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMGoDownAllowedUserRef

- **UUID**: `ECUC:79119397-b629-4210-a818-6071972fb77f`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_GoDown API.

####### 4. EcuMResetMode

**容器属性**:

- **UUID**: `ECUC:f2f88c2c-79a4-47d4-8e3a-750f1bb3624e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured reset modes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMResetModeId

- **UUID**: `ECUC:0a945601-d809-4f20-9ffe-e90e4d9a60a4`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this reset mode in services like EcuM_SelectShutdownTarget.

####### 5. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `ECUC:b2941bdd-11fe-440e-a773-bce84948a4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_SetClock API.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EcuMSetClockAllowedUserRef

- **UUID**: `ECUC:6c8dce8f-f2da-4d1f-9a06-da9d9829e14e`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_SetClock API.

####### 6. EcuMShutdownCause

**容器属性**:

- **UUID**: `ECUC:76c32704-2514-4828-a00c-c26c6ae45534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down or reset causes.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownCauseId

- **UUID**: `ECUC:596b234d-0197-46f6-87ee-f6a25635fa91`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down cause.

####### 7. EcuMShutdownTarget

**容器属性**:

- **UUID**: `ECUC:e55d1cfa-47ca-42b7-a22c-38a105284cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down targets.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. EcuMShutdownTargetId

- **UUID**: `ECUC:0d27bade-16c3-4e3e-bbff-b6cf696e01b8`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down target in services like EcuM_SelectShutdownTarget.

##### 21. EcuMAlarmClock

**容器属性**:

- **UUID**: `ECUC:750dd6de-13ec-48cf-befd-615fde9145b3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMAlarmClock`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured alarm clocks.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EcuMAlarmClockId

- **UUID**: `ECUC:49861b32-83d2-464f-afd2-24fb12a3e1e0`
- **参数名**: `EcuMAlarmClockId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this alarmclock.

####### FLOAT 类型参数

######## 1. EcuMAlarmClockTimeOut

- **UUID**: `ECUC:9677f083-e76f-486e-8634-df1555753290`
- **参数名**: `EcuMAlarmClockTimeOut`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows to define a timout for this alarm clock.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMAlarmClockUser

- **UUID**: `ECUC:e6ff4bc0-7648-4128-b239-de3f273d33d2`
- **引用名**: `EcuMAlarmClockUser`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter allows an alarm to be assigned to a user.

##### 22. EcuMFlexUserConfig

**容器属性**:

- **UUID**: `ECUC:3058925d-af3b-4a8a-9252-bd6700407009`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexUserConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the identifiers that are needed to refer to a software component or another appropriate entity in the system which uses the EcuMFlex Interfaces.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMFlexUser

- **UUID**: `ECUC:7cefee01-1e46-45e6-b582-678888f226cc`
- **参数名**: `EcuMFlexUser`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Parameter used to identify one user.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EcuMFlexEcucPartitionRef

- **UUID**: `ECUC:fe138ccd-1882-4c4c-ad96-ce9be41c7a07`
- **引用名**: `EcuMFlexEcucPartitionRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcucPartition`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPartitionCollection/EcucPartition`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Denotes in which "EcucPartition" the user of the EcuM is executed.

##### 23. EcuMGoDownAllowedUsers

**容器属性**:

- **UUID**: `ECUC:7d3d53a3-4f3d-4595-9bd9-4c2e42819a48`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGoDownAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_GoDown API.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMGoDownAllowedUserRef

- **UUID**: `ECUC:79119397-b629-4210-a818-6071972fb77f`
- **引用名**: `EcuMGoDownAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_GoDown API.

##### 24. EcuMResetMode

**容器属性**:

- **UUID**: `ECUC:f2f88c2c-79a4-47d4-8e3a-750f1bb3624e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMResetMode`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured reset modes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMResetModeId

- **UUID**: `ECUC:0a945601-d809-4f20-9ffe-e90e4d9a60a4`
- **参数名**: `EcuMResetModeId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this reset mode in services like EcuM_SelectShutdownTarget.

##### 25. EcuMSetClockAllowedUsers

**容器属性**:

- **UUID**: `ECUC:b2941bdd-11fe-440e-a773-bce84948a4fd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMSetClockAllowedUsers`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes the collection of allowed users which are allowed to call the EcuM_SetClock API.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMSetClockAllowedUserRef

- **UUID**: `ECUC:6c8dce8f-f2da-4d1f-9a06-da9d9829e14e`
- **引用名**: `EcuMSetClockAllowedUserRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..infinite]
- **目标**: `EcuMFlexUserConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMFlexConfiguration/EcuMFlexUserConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: These parameters describe the references to the users which are allowed to call the EcuM_SetClock API.

##### 26. EcuMShutdownCause

**容器属性**:

- **UUID**: `ECUC:76c32704-2514-4828-a00c-c26c6ae45534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownCause`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down or reset causes.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMShutdownCauseId

- **UUID**: `ECUC:596b234d-0197-46f6-87ee-f6a25635fa91`
- **参数名**: `EcuMShutdownCauseId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down cause.

##### 27. EcuMShutdownTarget

**容器属性**:

- **UUID**: `ECUC:e55d1cfa-47ca-42b7-a22c-38a105284cd1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMShutdownTarget`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

These containers describe the configured shut down targets.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. EcuMShutdownTargetId

- **UUID**: `ECUC:0d27bade-16c3-4e3e-bbff-b6cf696e01b8`
- **参数名**: `EcuMShutdownTargetId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This ID identifies this shut down target in services like EcuM_SelectShutdownTarget.

##### 28. EcuMFixedGeneral

**容器属性**:

- **UUID**: `ECUC:dbdde2a8-1a59-413e-9bd4-37c1fbfa00d1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFixedGeneral`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the general, pre-compile configuration parameters for the EcuMFixed.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMIncludeComM

- **UUID**: `ECUC:c001d57b-52b5-4868-9fce-780aaae852c3`
- **参数名**: `EcuMIncludeComM`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter defines whether the communication  manager is supported by EcuM. This feature is presented for development purpose to compile out the communication manager in the early debugging phase.

######## 2. EcuMIncludeNvM

- **UUID**: `ECUC:429e3d5a-5f8b-4dd3-a3c0-b22879eb3bfa`
- **参数名**: `EcuMIncludeNvM`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter defines whether the non volatile memory manager is supported by EcuM. This feature is presented for development purpose to compile out the volatile memory manager in the early debugging phase.

######## 3. EcuMIncludeNvramMgr

- **UUID**: `ECUC:65634043-e1b3-4f7e-bb12-34e0bf9fe643`
- **参数名**: `EcuMIncludeNvramMgr`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: If NVRAM manager is enabled but both flash and EEPROM driver are missing, then an error shall be flagged by the configuration tool

######## 4. EcuMTTIIEnabled

- **UUID**: `ECUC:f759ceef-b54a-461b-9878-7fbea25998c8`
- **参数名**: `EcuMTTIIEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Boolean switch to enable / disable TTII

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMTTIIWakeupSourceRef

- **UUID**: `ECUC:9f2cb71a-8f8b-4b0f-bb52-ccc6ac065b27`
- **引用名**: `EcuMTTIIWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This configuration parameter references the initial sleep mode to be used by TTII when TTII is activated after a RUN mode.

##### 29. EcuMFlexGeneral

**容器属性**:

- **UUID**: `ECUC:2042330b-0dc9-451d-9f4d-48e741cee88f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMFlexGeneral`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the general, pre-compile configuration parameters for the EcuMFlex.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMAlarmClockPresent

- **UUID**: `ECUC:b21df21d-f88f-4e68-a784-0b5b0836f989`
- **参数名**: `EcuMAlarmClockPresent`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This flag indicates whether the optional AlarmClock feature is present.

######## 2. EcuMEnableDefBehaviour

- **UUID**: `ECUC:7be4a46d-bc7e-4d31-b4f6-93cb16adc9be`
- **参数名**: `EcuMEnableDefBehaviour`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Switches the defensive behaviour on or off.

######## 3. EcuMResetLoopDetection

- **UUID**: `ECUC:53a6ceed-b5cc-4bd4-8741-60747b77dd76`
- **参数名**: `EcuMResetLoopDetection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: If false, no reset loop detection is performed.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EcuMAlarmWakeupSource

- **UUID**: `ECUC:824c1dac-d512-4089-aa9e-15bf7d01a829`
- **引用名**: `EcuMAlarmWakeupSource`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter describes the reference to the EcuMWakeupSource being used for the EcuM AlarmClock.

##### 30. EcuMGeneral

**容器属性**:

- **UUID**: `ECUC:fd0b9fcb-4de6-4f6d-9725-5c36640588db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EcuMGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds the general, pre-compile configuration parameters.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. EcuMDevErrorDetect

- **UUID**: `ECUC:07363168-09da-4d24-b4be-b85eba468e64`
- **参数名**: `EcuMDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: If false, no debug artifacts (e.g. calls to DET) shall remain in the executable object. Initialization of DET, however is controlled by configuration of optional BSW modules.

######## 2. EcuMIncludeDem

- **UUID**: `ECUC:af5750f4-9fc7-47b9-bcc2-2e0820256f3c`
- **参数名**: `EcuMIncludeDem`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: If enabled, the according BSW module will be included to the ECU State Manager.

######## 3. EcuMIncludeDet

- **UUID**: `ECUC:eb2066d7-d0e8-4fc5-bc8e-3a3d35c30a52`
- **参数名**: `EcuMIncludeDet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: If defined, the according BSW module will be initialized by the ECU State Manager

######## 4. EcuMVersionInfoApi

- **UUID**: `ECUC:fa4df206-514e-4273-98fe-65daf9b2536c`
- **参数名**: `EcuMVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: Switches the version info API on or off

####### FLOAT 类型参数

######## 1. EcuMMainFunctionPeriod

- **UUID**: `ECUC:40a1fc47-8607-49ff-be26-3f868176d15f`
- **参数名**: `EcuMMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
- **描述**: This parameter defines the schedule period of EcuM_MainFunction.

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

1. **EcuM**
