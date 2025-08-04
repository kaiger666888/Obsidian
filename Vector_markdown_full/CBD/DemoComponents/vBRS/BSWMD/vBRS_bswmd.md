# vBRS - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:47:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [vBRS](#vbrs)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. vBRS

#### 基本信息

- **UUID**: `2a529512-0c79-453f-ba41-bd3983d8a550`
- **模块名称**: `vBRS`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

The Vector Basic Runtime System (vBRS) provides functionality to initialize a microcontrollers' memory, PLL, Ports and Watchdog. It also provides startup code and functionalities for basic initialization and handling of the different Vector Software stacks.
It is part of the vBaseEnv.
For internal development and external use.
#vBaseEnv #Startup
#Vector

#### 版本历史

共有 **27** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2018-05-03
- **发布者**: vibwa

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2018-08-15
- **发布者**: visbwa

**变更内容**:

##### 3. 版本 1.01.00

- **状态**: released
- **发布日期**: 2018-10-10
- **发布者**: visbwa

**变更内容**:

##### 4. 版本 1.02.00

- **状态**: released
- **发布日期**: 2019-03-11
- **发布者**: visbwa

**变更内容**:

##### 5. 版本 1.03.00

- **状态**: released
- **发布日期**: 2019-05-23
- **发布者**: visbwa

**变更内容**:

##### 6. 版本 1.05.00

- **状态**: released
- **发布日期**: 2019-08-09
- **发布者**: visbwa

**变更内容**:

##### 7. 版本 1.06.00

- **状态**: released
- **发布日期**: 2020-02-19
- **发布者**: visbwa

**变更内容**:

##### 8. 版本 2.01.00

- **状态**: released
- **发布日期**: 2020-06-29
- **发布者**: visbwa

**变更内容**:

##### 9. 版本 2.01.01

- **状态**: released
- **发布日期**: 2020-07-20
- **发布者**: visbwa

**变更内容**:

##### 10. 版本 2.02.00

- **状态**: released
- **发布日期**: 2020-08-10
- **发布者**: visbwa

**变更内容**:

##### 11. 版本 2.03.00

- **状态**: released
- **发布日期**: 2021-01-25
- **发布者**: visjhr

**变更内容**:

##### 12. 版本 2.04.00

- **状态**: released
- **发布日期**: 2021-03-12
- **发布者**: visjhr

**变更内容**:

##### 13. 版本 2.05.00

- **状态**: released
- **发布日期**: 2021-05-03
- **发布者**: visjhr

**变更内容**:

##### 14. 版本 2.06.00

- **状态**: released
- **发布日期**: 2021-10-11
- **发布者**: visbwa

**变更内容**:

##### 15. 版本 2.07.00

- **状态**: released
- **发布日期**: 2021-11-09
- **发布者**: visbwa

**变更内容**:

##### 16. 版本 2.08.00

- **状态**: released
- **发布日期**: 2021-12-21
- **发布者**: visjhr

**变更内容**:

##### 17. 版本 2.08.01

- **状态**: released
- **发布日期**: 2022-08-09
- **发布者**: visjhr

**变更内容**:

##### 18. 版本 2.09.00

- **状态**: released
- **发布日期**: 2022-10-10
- **发布者**: visbwa

**变更内容**:

##### 19. 版本 2.10.00

- **状态**: released
- **发布日期**: 2022-12-14
- **发布者**: visbwa

**变更内容**:

##### 20. 版本 2.11.00

- **状态**: released
- **发布日期**: 2023-01-10
- **发布者**: visqli

**变更内容**:

##### 21. 版本 2.12.00

- **状态**: released
- **发布日期**: 2023-03-21
- **发布者**: visbwa

**变更内容**:

##### 22. 版本 2.13.00

- **状态**: released
- **发布日期**: 2023-05-12
- **发布者**: visbwa

**变更内容**:

##### 23. 版本 2.14.00

- **状态**: released
- **发布日期**: 2023-06-28
- **发布者**: visbwa

**变更内容**:

##### 24. 版本 2.14.01

- **状态**: released
- **发布日期**: 2023-07-17
- **发布者**: visbwa

**变更内容**:

##### 25. 版本 2.14.02

- **状态**: released
- **发布日期**: 2023-10-27
- **发布者**: vcbjhao

**变更内容**:

##### 26. 版本 2.15.00

- **状态**: released
- **发布日期**: 2023-11-14
- **发布者**: visbwa

**变更内容**:

##### 27. 版本 2.16.00

- **状态**: released
- **发布日期**: 2024-01-10
- **发布者**: visbwa

**变更内容**:

#### 配置容器

本模块包含 **16** 个配置容器：

##### 1. vBRSGeneral

**容器属性**:

- **UUID**: `6c44f8bf-2186-43e5-a31a-2453435a5bb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the vBRS.

###### 参数配置

此容器包含 **17** 个参数：

####### BOOLEAN 类型参数

######## 1. vBRSEnableSupportLEDs

- **UUID**: `cae43535-f63a-4d6b-a299-871d2996457f`
- **参数名**: `vBRSEnableSupportLEDs`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a blinking live-LED for the used EvalBoard.

Sets the following generated parameters:
BRS_ENABLE_SUPPORT_LEDS in vBrsCfg.h

######## 2. vBRSEnableSafeContextSupport

- **UUID**: `92a9e551-84c5-4710-ba0f-3d0cad504cea`
- **参数名**: `vBRSEnableSafeContextSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support of SafeContext OS (used for OS partitioning UseCase).

Sets the following generated parameters:
BRS_ENABLE_SAFECTXSUPPORT in vBrsCfg.h

######## 3. vBRSEnableMultiCoreSupport

- **UUID**: `b661a32e-8d6d-4bd0-8d46-847d9dcd39ea`
- **参数名**: `vBRSEnableMultiCoreSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support of MultiCore OS.

Sets the following generated parameters:
BRS_ENABLE_OS_MULTICORESUPPORT in vBrsCfg.h

######## 4. vBRSEnableSupportToggleWdPin

- **UUID**: `34fc22a9-a7bd-4dbf-bd72-7ea22a83a5d5`
- **参数名**: `vBRSEnableSupportToggleWdPin`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a toggling pin to trigger external watchdogs for the used EvalBoard.

Sets the following generated parameters:
BRS_ENABLE_SUPPORT_TOGGLE_WD_PIN in vBrsCfg.h

######## 5. vBRSEnableSupportToggleCustomPin

- **UUID**: `70edd99d-d9b8-4517-8b10-3045a3d6a303`
- **参数名**: `vBRSEnableSupportToggleCustomPin`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a toggling pin for the used EvalBoard.

Sets the following generated parameters:
BRS_ENABLE_SUPPORT_TOGGLE_CUSTOM_PIN in vBrsCfg.h

######## 6. vBRSEnableEcuMStubGeneration

- **UUID**: `c710f131-ad37-47b5-b725-f0c8fe35db82`
- **参数名**: `vBRSEnableEcuMStubGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If no real EcuM is part of the configuration, this functionality generates an EcuM.c/h stub, that calls the Init-functions of the ASR modules as specified in the EcuC/EcucGeneral/BswInitialization configuration.

######## 7. vBRSDisableSetupSupport

- **UUID**: `1d8ad5b1-dd16-4291-93af-7c9015eb7f33`
- **参数名**: `vBRSDisableSetupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate this, if you don't want the BRS to guide you through the default MSR stack configuration (e.g. AutosolvingActions for mandatory tasks).

######## 8. vBRSEnableSchmStubGeneration

- **UUID**: `7561d8d6-c79a-4e87-bd1d-6bdc23fd8cbb`
- **参数名**: `vBRSEnableSchmStubGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate this, if the SchM stubs, containing the defines for EXCLUSIVE AREAs, should be generated. Needed, if the ASR RTE/SchM is not part of the configuration, but modules are using the SchM exclusive area mechanism.

######## 9. vBRSEnableSchmStubSupportDrvCanAN

- **UUID**: `5b5a84da-099c-48ea-b263-75d9f455b97e`
- **参数名**: `vBRSEnableSchmStubSupportDrvCanAN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Prevents the SchM stub from generation of the following exclusive areas:
CAN Driver (CAN_EXCLUSIVE_AREA_6) 
CAN Interface (CANIF_EXCLUSIVE_AREA_0) 
CANSM (CANSM_ EXCLUSIVE_AREA_1, CANSM_ EXCLUSIVE_AREA_4) 
COMM (COMM_ EXCLUSIVE_AREA_1)
As described within CanDriver ApplicationNote AN-ISC-8-1149.
The implementation of these APIs, under consideration of this AN, is already part of static BrsMain_Appl.c.

######## 10. vBRSEnableSchmStubEmptyExclusiveAreaHandling

- **UUID**: `d4e04271-7fea-4e7c-b458-4ad97dff2c01`
- **参数名**: `vBRSEnableSchmStubEmptyExclusiveAreaHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For normal, all module specific exclusive are calls are mapped to SuspendAllInterrupts()/ResumeAllInterrupts().
If this feature is activated, the SchM stub will generate them as empty calls instead.
E.g. in SchM_Mcu.h:
# define SchM_Enter_Mcu_MCU_EXCLUSIVE_AREA_00()
# define SchM_Exit_Mcu_MCU_EXCLUSIVE_AREA_00()
instead of
# define SchM_Enter_Mcu_MCU_EXCLUSIVE_AREA_00() SuspendAllInterrupts()
# define SchM_Exit_Mcu_MCU_EXCLUSIVE_AREA_00() ResumeAllInterrupts()

This is mainly for polling environments, where no OS is used and therefore no specific disabling of interrupts is necessary.

######## 11. vBRSFirstInstance

- **UUID**: `79064ffe-a1dd-4097-b0d9-fb5e5c4fd36c`
- **参数名**: `vBRSFirstInstance`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if this executable is the first instance of the system.
Set this parameter to enabled, if this instance should contain the brsStartupEntry and initialize the core.
Only one single executable of a system with several executables should be the first instance. All other executables are starting with Brs_ApplicationEntry().
E.g. in a FBL UseCase with standalone BM, the BM is the first executable and the FBL, Updater, MSR-Application are not.
If there is only a single executable in the system, of course this application is also the first one.

Sets the following generated parameters:
BRS_FIRST_EXECUTION_INSTANCE in vBrsCfg.h

######## 12. vBRSEnableCoreSpecificVLinkGenConfig

- **UUID**: `f3f8d8e2-bf36-4b86-b7c1-df38ce24843a`
- **参数名**: `vBRSEnableCoreSpecificVLinkGenConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the validation of core specific vLinkGen config data based on cores configured within /EcuC/EcucHardware/EcucCoreDefinitions and /Os/OsCores.

######## 13. vBRSFblSupportEcuMInit

- **UUID**: `007687b4-bfa3-49be-b6a7-e8a7dfa2a855`
- **参数名**: `vBRSFblSupportEcuMInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if the FBL stack should be started inside main() via a call of EcuM_Init() or a call of FblMain().
This parameter only has an effect, if Execution Instance is "FBL", "FBL_Updater", "BM" or "BM_FBL".
FBL without EcuM_Init() is the oldstyle FBL integration, started with a direct call of FblMain().
FBL with EcuM_Init() means, module initialization is done in EcuM_Init() (real EcuM or EcuM Stub), but the cyclic handling is done in FBL.

Sets the following generated parameters:
BRS_FBL_WITH_ECUMINIT or BRS_FBL_NO_ECUMINIT in vBrsCfg.h

######## 14. vBRSFblSupportExceptionTableInRam

- **UUID**: `7361ac9d-524f-4ff4-8bd3-3e012b151238`
- **参数名**: `vBRSFblSupportExceptionTableInRam`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure, if the additional ExceptionTable in RAM should be initialized. This will cause a call of BrsHw_ExceptionTable_Init() in main(), which will program the vector table base address to Brs_ExcVectRam. The depending SectionGroup needs to be configured with Init Policy COPY_TO_RAM in vLinkGen as well.
This allows proper exception handling during erase/re-program of flash.
The parameter only has an effect, if Execution Instance is "FBL", "FBL_Updater", "BM" or "BM_FBL".

Sets the following generated parameter:
BRS_FBL_EXCEPTIONTABLE_IN_RAM in vBrsCfg.h

######## 15. vBRSEnableSmallDevicesOptimization

- **UUID**: `98941c58-7e0e-4b07-8c8d-33cda49e96a1`
- **参数名**: `vBRSEnableSmallDevicesOptimization`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This functionality will help to setup the environment for controllers with less available memory. The OS default stack sizes of some basic setup parameters will be decreased, to reduce the RAM consumption to a minimum. Additionally, some hooks will be checked to be disabled. Please consider the vBaseEnv UserManual for details.
Be aware, that this will increase the risk of runtime errors, in consequence of stack overflows. But, the OS stack monitoring feature (Os/OsOS/OsStackMonitoring) should be able to detect them. The features main focus is to support the fast initial setup of basic environments on so called "Small Devices".
The feature is only available for singleCore and SC1 configurations.

####### STRING 类型参数

######## 1. vBRSUserConfigFile

- **UUID**: `1f3915bc-5e49-4a48-b27b-5622bcfd1b83`
- **参数名**: `vBRSUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If a file name is entered here, it will be included in vBrsCfg.h.

####### ENUMERATION 类型参数

######## 1. vBRSExecutionInstance

- **UUID**: `75ff9472-6359-4afd-bf37-fffce3c3ad82`
- **参数名**: `vBRSExecutionInstance`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Application`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Application` (来源: Vector Informatik)
  - `FBL` (来源: Vector Informatik)
  - `FBL_Updater` (来源: Vector Informatik)
  - `BM` (来源: Vector Informatik)
  - `BM_FBL` (来源: Vector Informatik)
  - `HSM` (来源: Vector Informatik)
  - `HSM_Updater` (来源: Vector Informatik)
  - `FlashDriver` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the execution instance of the application, handled by this configuration.
As sometimes, there exist several applications in one system, they need to be separated.
"Application" stands for a "normal" application executable (e.g. MSR or CANbedded stack), which could be standalone or called out of a FBL or BM.
"FBL" stands for a FlashBootLoader executable, which could be standalone or called out of a BM.
"FBL_Updater" stands for a FlashBootLoader Updater executable, which could be standalone or called out of a BM.
"BM" stands for a Boot Manager executable, which is the startup entry and decides to call a FBL, Updater or Application.
"BM_FBL" stands for a Boot Manager and FlashBootLoader executable, which are compiled together. The BootManager part is the startup entry and decides to call the FBL part, Updater or Application.
"HSM" stands for a HSM executable, which could be standalone or called out of the HSM Updater (if a HSM Updater is present).
"HSM_Updater" stands for a HSM Updater executable, which is the startup entry and decides to call the HSM or update the HSM.
"FlashDriver" stands for a standalone binary, containing a flasher driver instance only. There is no runtime part included.

Sets the following generated parameters in vBrsCfg.h:
BRS_ENABLE_FBL for the values "FBL", "FBL_Updater", "BM" and "BM_FBL"
BRS_ENABLE_HSM_SUPPORT for the value "HSM"
BRS_ENABLE_HSM_UPDATER_SUPPORT for the value "HSM_Updater"

Sets the following generated parameters in Makefile.config.generated:
BRS_ENABLE_HSM_SUPPORT, BRS_ENABLE_FBL_SUPPORT

###### 引用关系

此容器包含 **4** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSToggleLEDDioChannel

- **UUID**: `cd00b1f8-d266-4de5-91fe-e562f9cfff96`
- **引用名**: `vBRSToggleLEDDioChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Dio channel reference setting for toggling the LED port.
Only relevant if non-stub Dio is part of the configuration.

######## 2. vBRSToggleWdPinDioChannel

- **UUID**: `432ac26a-f48c-4aaa-8497-b88ce5bca6d4`
- **引用名**: `vBRSToggleWdPinDioChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Dio channel reference setting for toggling the WD port.
Only relevant if non-stub Dio is part of the configuration.

######## 3. vBRSToggleCustomPinDioChannel

- **UUID**: `f7f8b5b7-7ae1-4cb6-9bf1-58324958d07e`
- **引用名**: `vBRSToggleCustomPinDioChannel`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Dio channel reference setting for toggling the Custom port.
Only relevant if non-stub Dio is part of the configuration.

######## 4. vBRSVariantUsageOfvLinkGen

- **UUID**: `5467bf63-a327-4fdf-a15e-5566ad268841`
- **引用名**: `vBRSVariantUsageOfvLinkGen`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vLinkGenVariant`
- **完整路径**: `/MICROSAR/vLinkGen/vLinkGenVariantHandling/vLinkGenVariant`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: vLinkGenVariant reference for current executable.
The chosen variant will be generated into vBrsCfg.h and then be used in vLinkGen_Lcfg.c.
Furthermore, it will also be generated as BRS_LINKER_COMMAND_FILE_POSTFIX into Makefile.config.generated.
This will override the LINKER_COMMAND_FILE parameter in the Makefile. LINKER_COMMAND_FILE is used for the linkage target of the MakeSupport.

Note: /MICROSAR/vLinkGen/vLinkGenGeneral/vLinkGenFileGeneration shall be set to ONE_FILE_PER_VARIANT, in order to generate the corresponding link file for each variant.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. vBRSOverrideInitPhase

**容器属性**:

- **UUID**: `d7e392af-102e-43ea-8ed7-aea132403f8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSOverrideInitPhase`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes all configuration parameters for the EcuM Stub, to override the EcuC/EcucGeneral/BswInitialization/InitFunction InitPhase configuration, if needed.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. vBRSInitPhase

- **UUID**: `c6fd6122-e455-4548-aa2b-4954d9430cb1`
- **参数名**: `vBRSInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: InitPhase, the InitFunction should be called instead

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSInitFunction

- **UUID**: `cc3941e1-11ab-4cd3-be37-6444a9c5a5ba`
- **引用名**: `vBRSInitFunction`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `InitFunction`
- **完整路径**: `/MICROSAR/EcuC/EcucGeneral/BswInitialization/InitFunction`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the InitFunction, whose init phase should be overwritten

##### 2. vBRSOverrideInitPhase

**容器属性**:

- **UUID**: `d7e392af-102e-43ea-8ed7-aea132403f8c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSOverrideInitPhase`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes all configuration parameters for the EcuM Stub, to override the EcuC/EcucGeneral/BswInitialization/InitFunction InitPhase configuration, if needed.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. vBRSInitPhase

- **UUID**: `c6fd6122-e455-4548-aa2b-4954d9430cb1`
- **参数名**: `vBRSInitPhase`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `NO_INIT` (来源: Vector Informatik)
  - `INIT_MEMORY` (来源: Vector Informatik)
  - `INIT_ZERO` (来源: Vector Informatik)
  - `INIT_ONE_EARLY` (来源: Vector Informatik)
  - `INIT_ONE` (来源: Vector Informatik)
  - `INIT_ONE_LATE` (来源: Vector Informatik)
  - `INIT_TWO_MCAL` (来源: Vector Informatik)
  - `INIT_TWO_TRCV` (来源: Vector Informatik)
  - `INIT_TWO_DRV` (来源: Vector Informatik)
  - `INIT_TWO_IF` (来源: Vector Informatik)
  - `INIT_TWO_COM` (来源: Vector Informatik)
  - `INIT_TWO_SM` (来源: Vector Informatik)
  - `INIT_TWO_NM` (来源: Vector Informatik)
  - `INIT_TWO_TP` (来源: Vector Informatik)
  - `INIT_TWO_SYS` (来源: Vector Informatik)
  - `INIT_TWO_POST_NVMREADALL` (来源: Vector Informatik)
  - `INIT_THREE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: InitPhase, the InitFunction should be called instead

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSInitFunction

- **UUID**: `cc3941e1-11ab-4cd3-be37-6444a9c5a5ba`
- **引用名**: `vBRSInitFunction`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `InitFunction`
- **完整路径**: `/MICROSAR/EcuC/EcucGeneral/BswInitialization/InitFunction`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the InitFunction, whose init phase should be overwritten

##### 3. vBRSHwConfig

**容器属性**:

- **UUID**: `501793dc-6a15-4987-a313-284e87fb3a23`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSHwConfig`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. vBRSOscClock

- **UUID**: `c882c5f9-27a7-4f55-a40c-3d3babe1c4b8`
- **参数名**: `vBRSOscClock`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the board specific external oscillator.

Sets the following generated parameters:
BRS_OSC_CLK  in vBrsCfg.h 
MAIN_OSC_CLK in Makefile.config.generated

######## 2. vBRSTimebaseClock

- **UUID**: `c656bbe0-791f-45cc-a9eb-f361bdec10bc`
- **参数名**: `vBRSTimebaseClock`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).

Sets the following generated parameters:
BRS_TIMEBASE_CLOCK in vBrsCfg.h 
TIMEBASE_CLOCK in Makefile.config.generated

######## 3. vBRSPeriphClock

- **UUID**: `bb5dd84b-f2f9-464d-b7df-f20fdcbd0e67`
- **参数名**: `vBRSPeriphClock`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency of the controller peripherals, at least for the default timer, used by the OS.
This frequency value is used to calculate the proper value of the TicksPerBase value inside the OS configuration.
If the frequencies for communication peripherals differ from this peripheral clock, they could be configured within the depending communictaion channel configuration (e.g. vBRSHwConfig/vBRSDriverHandlingCAN/vBRSDriverHandlingCAN_Clock).

Sets the following generated parameters:
BRS_PERIPH_CLOCK in vBrsCfg.h 
PERIPH_CLOCK in Makefile.config.generated

####### BOOLEAN 类型参数

######## 1. vBRSEnablePortHandling

- **UUID**: `06984b04-0874-4c47-b22f-3ae1a16562c1`
- **参数名**: `vBRSEnablePortHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the handling of Ports configuration inside BrsHw.

Sets the following generated parameter:
BRS_ENABLE_PORT in vBrsCfg.h

######## 2. vBRSEnableWatchdogHandling

- **UUID**: `31ce358b-89ec-41da-9a69-984b71d65cd5`
- **参数名**: `vBRSEnableWatchdogHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the handling of Watchdog configuration inside BrsHw.

Sets the following generated parameter:
BRS_ENABLE_WATCHDOG in vBrsCfg.h

######## 3. vBRSEnablePLLClocksHandling

- **UUID**: `cece3cbb-75b7-4ab6-9a17-5ee815b3726b`
- **参数名**: `vBRSEnablePLLClocksHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the handling of PLL and Clocks configuration inside BrsHw.

Sets the following generated parameter:
BRS_ENABLE_PLLCLOCKS in vBrsCfg.h

######## 4. vBRSCompilerEnableFPU

- **UUID**: `0102a66c-ce72-4747-9618-8035b4f5866c`
- **参数名**: `vBRSCompilerEnableFPU`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable FPU usage on the controller. This has effect on the compiler/linker options.
Note: not all platforms are supporting enabling/disabling of FPU usage.

Generated as the following:
Makefile.config.generated: FPU_USED = 1/0
vBrsCfg.h: BRS_FPU_USED

######## 5. vBRSPreferPLLWatchdogInit

- **UUID**: `e06b809a-e37a-4308-9dc5-f232b823220e`
- **参数名**: `vBRSPreferPLLWatchdogInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Prefer the initialization of PLL and Watchdog, previous to memory initialization.
This will cause the depending init calls, previous to init stage HardReset, inside the callout BrsMain_MemoryInit_StageHardReset_Hook() of BrsMain_Callout_Stubs.c.

Sets the following generated parameter:
BRS_ENABLE_PREFER_PLL_WATCHDOG_INIT in vBrsCfg.h

####### STRING 类型参数

######## 1. vBRSPeriphClockDescription

- **UUID**: `be9814e8-5ca2-49ef-a586-2ac9f07d624f`
- **参数名**: `vBRSPeriphClockDescription`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Platform/family specific preconfig parameter with description of the recommended platform/family clock values and for usage of the peripheral clock (connection to OS timer).

######## 2. vBRSCompilerPath

- **UUID**: `7a9386eb-49f8-4882-a31a-0c7a14f14da1`
- **参数名**: `vBRSCompilerPath`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Base path of the embedded compiler, to be used from the MakeSupport.
This parameter allows to override the COMPILER_BASE_WIN parameter in the Makefile.
Use absolute paths, w/o blanks. See default path in Makefile for an example.

Generated as BRS_COMPILER_PATH into Makefile.config.generated.

######## 3. vBRSProjectName

- **UUID**: `f7cc575f-ad05-4ac3-8393-1b6e3eb52f7e`
- **参数名**: `vBRSProjectName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of this project, to be used by the MakeSupport.
This parameter allows to override the PROJECT_NAME parameter in the Makefile.static. PROJECT_NAME is used as target name by the MakeSupport.

Generated as BRS_PROJECT_NAME into Makefile.config.generated.

####### ENUMERATION 类型参数

######## 1. vBRSCompilerInstructionSet

- **UUID**: `3a95dc8e-27db-477d-8e95-0cd9fdfa5ac2`
- **参数名**: `vBRSCompilerInstructionSet`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `THUMB` (来源: Vector Informatik)
  - `ARM` (来源: Vector Informatik)
  - `VLE` (来源: Vector Informatik)
  - `BOOKE` (来源: Vector Informatik)
  - `RV32I` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select the platform dependent Instruction Set for compile/link of the project.
Note: not all platforms are supporting different instruction sets.

Generated as the following:
Makefile.config.generated: INSTRUCTION_SET = xxx
vBrsCfg.h: BRS_INSTRUCTION_SET_xxx

####### MULTILINE-STRING 类型参数

######## 1. vBRSMakefileUserCode

- **UUID**: `0d592350-b679-4336-aa3a-6440f9bfce3e`
- **参数名**: `vBRSMakefileUserCode`
- **数据类型**: MULTILINE-STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define here additional UserCode, to be generated into Makefile.config.generated

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSMcuClockReferencePointForBrsPeriphClock

- **UUID**: `132cb904-2a23-40f2-8d45-61dbbd6f6344`
- **引用名**: `vBRSMcuClockReferencePointForBrsPeriphClock`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the BrsPeriphClock to the value, this reference is pointing to.

######## 2. vBRSEvaluationBoard

- **UUID**: `4e70c0d3-b86e-4e0e-ae43-bb2511a7aae9`
- **引用名**: `vBRSEvaluationBoard`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `vBRSEvalBoardInfo`
- **完整路径**: `/MICROSAR/vBRS/vBRSHwConfig/vBRSEvalBoardInfo`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select a Eval Board from the list of supported ones.
Sets the following generated parameters:
BRS_EVA_BOARD_xxx in vBrsCfg.h 
EVA_BOARD in Makefile.config.generated

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `e710850b-9807-403a-a15e-dac30eca6b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..2]
- **构建后可变**: false

######## 参数配置

此容器包含 **24** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `112689a5-074f-44e8-b676-ed5849623dba`
- **参数名**: `vBRSDriverHandlingCAN_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of CAN driver peripheral clock.
Sets the following generated parameters:
BRS_CAN_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingCAN

- **UUID**: `e60a211b-4c23-410a-9bd3-72452fa2a8c9`
- **参数名**: `vBRSEnableDriverHandlingCAN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_CAN_SUPPORT
is generated.

########## 2. vBRSDriverHandlingCAN_channel0

- **UUID**: `50125c4d-f36d-4638-a9a0-72f5b05f5b7f`
- **参数名**: `vBRSDriverHandlingCAN_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_0 in vBrsCfg.h

########## 3. vBRSDriverHandlingCAN_channel1

- **UUID**: `a130e052-d944-4329-8577-03c0ac13cae9`
- **参数名**: `vBRSDriverHandlingCAN_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_1 in vBrsCfg.h

########## 4. vBRSDriverHandlingCAN_channel2

- **UUID**: `a2bc1791-d245-439f-a962-38125a6fde63`
- **参数名**: `vBRSDriverHandlingCAN_channel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 2.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_2 in vBrsCfg.h

########## 5. vBRSDriverHandlingCAN_channel3

- **UUID**: `42ecea7d-a9d9-483f-8e18-f50586965fab`
- **参数名**: `vBRSDriverHandlingCAN_channel3`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 3.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_3 in vBrsCfg.h

########## 6. vBRSDriverHandlingCAN_channel4

- **UUID**: `4327e1eb-4c6f-4605-a1b4-4f7e7bed847f`
- **参数名**: `vBRSDriverHandlingCAN_channel4`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 4.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_4 in vBrsCfg.h

########## 7. vBRSDriverHandlingCAN_channel5

- **UUID**: `6af209a2-dc6a-4180-b8ac-7fcca0fe1877`
- **参数名**: `vBRSDriverHandlingCAN_channel5`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 5.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_5 in vBrsCfg.h

########## 8. vBRSDriverHandlingCAN_channel6

- **UUID**: `b0a1b96e-1f62-4c9f-902f-f5d1b6812793`
- **参数名**: `vBRSDriverHandlingCAN_channel6`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 6.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_6 in vBrsCfg.h

########## 9. vBRSDriverHandlingCAN_channel7

- **UUID**: `ca77e2e1-6584-42dd-aaa9-23c7c625d9e6`
- **参数名**: `vBRSDriverHandlingCAN_channel7`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 7.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_7 in vBrsCfg.h

########## 10. vBRSDriverHandlingCAN_channel8

- **UUID**: `a0442dec-5f06-4ffb-bb1f-d9d3f85f499a`
- **参数名**: `vBRSDriverHandlingCAN_channel8`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 8.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_8 in vBrsCfg.h

########## 11. vBRSDriverHandlingCAN_channel9

- **UUID**: `be55876a-53b0-4b46-97a2-89fbb7d5b8b6`
- **参数名**: `vBRSDriverHandlingCAN_channel9`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 9.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_9 in vBrsCfg.h

########## 12. vBRSDriverHandlingCAN_PeripheralClock

- **UUID**: `a9a9162b-d922-400f-b8c8-24fe94f354e1`
- **参数名**: `vBRSDriverHandlingCAN_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the CAN driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingCAN_Clock or
vBRSDriverHandlingCAN_ClockRef (if Mcu is used)

########## 13. vBRSDriverHandlingCAN_channel10

- **UUID**: `481a90cb-0a99-4e08-8ab2-098dc99e58d6`
- **参数名**: `vBRSDriverHandlingCAN_channel10`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_10 in vBrsCfg.h

########## 14. vBRSDriverHandlingCAN_channel11

- **UUID**: `0bc5d44c-682c-4753-b305-0b3d4eecf6bb`
- **参数名**: `vBRSDriverHandlingCAN_channel11`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 11.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_11 in vBrsCfg.h

########## 15. vBRSDriverHandlingCAN_channel12

- **UUID**: `47d5d281-f54d-4a56-b154-6c36bc13e935`
- **参数名**: `vBRSDriverHandlingCAN_channel12`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 12.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_12 in vBrsCfg.h

########## 16. vBRSDriverHandlingCAN_channel13

- **UUID**: `90757915-e827-4d00-896b-a9896a6d5699`
- **参数名**: `vBRSDriverHandlingCAN_channel13`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 13.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_13 in vBrsCfg.h

########## 17. vBRSDriverHandlingCAN_channel14

- **UUID**: `821f913f-46f4-429f-a39c-0a414315db86`
- **参数名**: `vBRSDriverHandlingCAN_channel14`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 14.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_14 in vBrsCfg.h

########## 18. vBRSDriverHandlingCAN_channel15

- **UUID**: `208aca06-801c-4164-ba7c-4caedbec05bb`
- **参数名**: `vBRSDriverHandlingCAN_channel15`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 15.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_15 in vBrsCfg.h

########## 19. vBRSDriverHandlingCAN_channel16

- **UUID**: `3a141e0c-a8e1-40eb-a420-187cd50e0166`
- **参数名**: `vBRSDriverHandlingCAN_channel16`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 16.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_16 in vBrsCfg.h

########## 20. vBRSDriverHandlingCAN_channel17

- **UUID**: `75d995a3-8ec5-4cff-af82-f20b4b16de02`
- **参数名**: `vBRSDriverHandlingCAN_channel17`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 17.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_17 in vBrsCfg.h

########## 21. vBRSDriverHandlingCAN_channel18

- **UUID**: `2ef82ccb-dd98-4755-a214-5d50f9e54419`
- **参数名**: `vBRSDriverHandlingCAN_channel18`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 18.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_18 in vBrsCfg.h

########## 22. vBRSDriverHandlingCAN_channel19

- **UUID**: `540e669a-e37c-4ea2-a62c-3925fc05e7c0`
- **参数名**: `vBRSDriverHandlingCAN_channel19`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 19.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_19 in vBrsCfg.h

######### ENUMERATION 类型参数

########## 1. vBRSDriverHandlingCAN_Instance

- **UUID**: `f9262aa0-308f-4f81-b8a2-1a95cb83d5c8`
- **参数名**: `vBRSDriverHandlingCAN_Instance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MCAN` (来源: Vector Informatik)
  - `XCAN` (来源: Vector Informatik)
  - `RCAN` (来源: Vector Informatik)
  - `FlexCAN` (来源: Vector Informatik)
  - `RSCAN` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On platforms with several, different CAN-IPs, the depending instance should be configured.
A selection of the instance gets mandatory, if two vBRSDriverHandlingCAN instances are configured (two different CAN IPs are used in parallel).

If a value is selected, vBRS will generate all depending defines with a value depending infix:
BRS_CAN_infix_CLOCK
BRS_ENABLE_CAN_infix_CHANNEL_x
additional to BRS_ENABLE_CAN_SUPPORT, also BRS_ENABLE_CAN_infix_SUPPORT will be generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `433ce5f3-8da2-4cf3-9b16-f74b4106fb60`
- **引用名**: `vBRSDriverHandlingCAN_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 2. vBRSDriverHandlingLIN

**容器属性**:

- **UUID**: `5e2190c8-c50c-4d5e-8016-0e4701ca5942`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **26** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `86bb466d-32d9-4e43-8be0-b070f3e687f7`
- **参数名**: `vBRSDriverHandlingLIN_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of LIN driver peripheral clock.
Sets the following generated parameters:
BRS_LIN_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingLIN

- **UUID**: `78774246-5ee1-4168-8ce2-2634743d093c`
- **参数名**: `vBRSEnableDriverHandlingLIN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_LIN_SUPPORT
is generated.

########## 2. vBRSDriverHandlingLIN_channel0

- **UUID**: `d30da48f-414c-4ee6-a1a9-63c5ea871dfb`
- **参数名**: `vBRSDriverHandlingLIN_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_0 in vBrsCfg.h

########## 3. vBRSDriverHandlingLIN_channel1

- **UUID**: `a69c1cea-aaf4-44a9-9a8e-07686ecf004e`
- **参数名**: `vBRSDriverHandlingLIN_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_1 in vBrsCfg.h

########## 4. vBRSDriverHandlingLIN_channel2

- **UUID**: `e3ce23cf-4b68-4796-8807-0862ea36f6ea`
- **参数名**: `vBRSDriverHandlingLIN_channel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 2.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_2 in vBrsCfg.h

########## 5. vBRSDriverHandlingLIN_channel3

- **UUID**: `de9ffd37-8380-460f-b949-ff2f6f4972e0`
- **参数名**: `vBRSDriverHandlingLIN_channel3`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 3.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_3 in vBrsCfg.h

########## 6. vBRSDriverHandlingLIN_channel4

- **UUID**: `10b111d3-402e-427b-a9e6-94dd4a5d6579`
- **参数名**: `vBRSDriverHandlingLIN_channel4`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 4.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_4 in vBrsCfg.h

########## 7. vBRSDriverHandlingLIN_channel5

- **UUID**: `2e035b56-0468-451e-9716-2398852d2804`
- **参数名**: `vBRSDriverHandlingLIN_channel5`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 5.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_5 in vBrsCfg.h

########## 8. vBRSDriverHandlingLIN_channel6

- **UUID**: `65305d56-0a4f-48a8-bd84-10a135022aba`
- **参数名**: `vBRSDriverHandlingLIN_channel6`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 6.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_6 in vBrsCfg.h

########## 9. vBRSDriverHandlingLIN_channel7

- **UUID**: `3786ef43-2b1b-4240-b05a-2070eb326495`
- **参数名**: `vBRSDriverHandlingLIN_channel7`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 7.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_7 in vBrsCfg.h

########## 10. vBRSDriverHandlingLIN_channel8

- **UUID**: `8ba49f7c-806e-4cfb-adcf-9e9c85423b1b`
- **参数名**: `vBRSDriverHandlingLIN_channel8`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 8.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_8 in vBrsCfg.h

########## 11. vBRSDriverHandlingLIN_channel9

- **UUID**: `456f6947-6b07-4ab7-b5f2-d8a3da160dae`
- **参数名**: `vBRSDriverHandlingLIN_channel9`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 9.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_9 in vBrsCfg.h

########## 12. vBRSDriverHandlingLIN_PeripheralClock

- **UUID**: `b73200bf-b18d-4616-b908-cd567a1fa6d0`
- **参数名**: `vBRSDriverHandlingLIN_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the LIN driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingLIN_Clock or
vBRSDriverHandlingLIN_ClockRef (if Mcu is used)

########## 13. vBRSDriverHandlingLIN_channel10

- **UUID**: `3f000c86-1a21-4efe-8258-ac78bc9e1ec9`
- **参数名**: `vBRSDriverHandlingLIN_channel10`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h

########## 14. vBRSDriverHandlingLIN_channel11

- **UUID**: `6e89c7de-e098-4c90-b055-312edefc5589`
- **参数名**: `vBRSDriverHandlingLIN_channel11`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 11.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_11 in vBrsCfg.h

########## 15. vBRSDriverHandlingLIN_channel12

- **UUID**: `0ccbc3f6-d72a-4f4b-8065-bd092f602579`
- **参数名**: `vBRSDriverHandlingLIN_channel12`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 12.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_12 in vBrsCfg.h

########## 16. vBRSDriverHandlingLIN_channel13

- **UUID**: `c875065b-9fe4-449e-a09d-d8ae31db66bc`
- **参数名**: `vBRSDriverHandlingLIN_channel13`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 13.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_13 in vBrsCfg.h

########## 17. vBRSDriverHandlingLIN_channel14

- **UUID**: `363a6dd5-65bd-406f-b2da-316397e63245`
- **参数名**: `vBRSDriverHandlingLIN_channel14`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 14.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_14 in vBrsCfg.h

########## 18. vBRSDriverHandlingLIN_channel15

- **UUID**: `59debbd1-bc45-49a8-a21c-d5accb87f3cc`
- **参数名**: `vBRSDriverHandlingLIN_channel15`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 15.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_15 in vBrsCfg.h

########## 19. vBRSDriverHandlingLIN_channel16

- **UUID**: `0751be5d-10cd-4e24-8223-f5d6cf603408`
- **参数名**: `vBRSDriverHandlingLIN_channel16`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 16.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_16 in vBrsCfg.h

########## 20. vBRSDriverHandlingLIN_channel17

- **UUID**: `7cc2ab64-38c6-4125-af24-6301bd82996f`
- **参数名**: `vBRSDriverHandlingLIN_channel17`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h

########## 21. vBRSDriverHandlingLIN_channel18

- **UUID**: `0d27b238-0896-447f-854e-8a4fda158331`
- **参数名**: `vBRSDriverHandlingLIN_channel18`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 18.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_18 in vBrsCfg.h

########## 22. vBRSDriverHandlingLIN_channel19

- **UUID**: `96f2ae35-33a7-430c-a64e-9abafee0cd07`
- **参数名**: `vBRSDriverHandlingLIN_channel19`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 19.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_19 in vBrsCfg.h

########## 23. vBRSDriverHandlingLIN_channel20

- **UUID**: `6fc81233-0869-4205-80cf-aeb70c0a2b1a`
- **参数名**: `vBRSDriverHandlingLIN_channel20`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 20.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_20 in vBrsCfg.h

########## 24. vBRSDriverHandlingLIN_channel21

- **UUID**: `a952f3f5-691c-40dc-a12a-20d9553adc2f`
- **参数名**: `vBRSDriverHandlingLIN_channel21`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 21.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_21 in vBrsCfg.h

########## 25. vBRSDriverHandlingLIN_channel22

- **UUID**: `b16a55c5-7691-44e4-b577-73b87cc4e009`
- **参数名**: `vBRSDriverHandlingLIN_channel22`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 22.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_22 in vBrsCfg.h

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingLIN_ClockRef

- **UUID**: `8e4b594f-ed1f-4fcd-a882-902d0df26452`
- **引用名**: `vBRSDriverHandlingLIN_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 3. vBRSDriverHandlingFlexray

**容器属性**:

- **UUID**: `0d48f4f4-19f1-4842-86f6-4ac169fcf2c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `b6ed573f-f27c-4dc9-87e9-cdadbab6a6bf`
- **参数名**: `vBRSDriverHandlingFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of FlexRay driver peripheral clock.
Sets the following generated parameters:
BRS_FLEXRAY_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingFlexray

- **UUID**: `dc711d46-cf94-4771-a785-5ceaebc3cd80`
- **参数名**: `vBRSEnableDriverHandlingFlexray`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_FLEXRAY_SUPPORT
is generated.

########## 2. vBRSDriverHandlingFlexray_channel0A

- **UUID**: `59e82502-9ca0-463d-8b5a-d349a5b30c26`
- **参数名**: `vBRSDriverHandlingFlexray_channel0A`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0A.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_0A in vBrsCfg.h

########## 3. vBRSDriverHandlingFlexray_channel0B

- **UUID**: `ab83f595-87e1-4ff6-a7fb-cc294d8b44aa`
- **参数名**: `vBRSDriverHandlingFlexray_channel0B`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0B.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_0B in vBrsCfg.h

########## 4. vBRSDriverHandlingFlexray_channel1A

- **UUID**: `4bb3d532-9cbd-4170-b3c2-3e47ecbf4810`
- **参数名**: `vBRSDriverHandlingFlexray_channel1A`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1A.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_1A in vBrsCfg.h

########## 5. vBRSDriverHandlingFlexray_channel1B

- **UUID**: `5f4a7d2e-d24f-492e-ba11-c71fbf838bb1`
- **参数名**: `vBRSDriverHandlingFlexray_channel1B`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1B.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_1B in vBrsCfg.h

########## 6. vBRSDriverHandlingFlexray_PeripheralClock

- **UUID**: `4215e850-d032-4a46-a43e-729ec70da3e1`
- **参数名**: `vBRSDriverHandlingFlexray_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the FlexRay driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingFlexray_Clock or
vBRSDriverHandlingFlexray_ClockRef (if Mcu is used)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingFlexray_ClockRef

- **UUID**: `774d8637-f957-417c-bf57-2faeb6fc9d0a`
- **引用名**: `vBRSDriverHandlingFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 4. vBRSDriverHandlingEthernet

**容器属性**:

- **UUID**: `9e8fd1a8-b15f-4924-a93a-fc89db6b3b2a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..2]
- **构建后可变**: false

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `a775d1eb-7505-4353-8be1-b81a0899d624`
- **参数名**: `vBRSDriverHandlingEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of EtherNet driver peripheral clock.
Sets the following generated parameters:
BRS_ETHERNET_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingEthernet

- **UUID**: `e2ef25f0-1815-43b4-83ed-49f60f5850f0`
- **参数名**: `vBRSEnableDriverHandlingEthernet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_ETHERNET_SUPPORT
is generated.

########## 2. vBRSDriverHandlingEthernet_PeripheralClock

- **UUID**: `d438db9e-a3de-4f39-bf25-35f80bda0348`
- **参数名**: `vBRSDriverHandlingEthernet_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the EtherNet driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingEthernet_Clock or
vBRSDriverHandlingEthernet_ClockRef (if Mcu is used)

######### ENUMERATION 类型参数

########## 1. vBRSDriverHandlingEthernet_Instance

- **UUID**: `3fe35d0d-047e-432c-acbc-4f6d8457ad3c`
- **参数名**: `vBRSDriverHandlingEthernet_Instance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETNA` (来源: Vector Informatik)
  - `ETNB` (来源: Vector Informatik)
  - `ETNF` (来源: Vector Informatik)
  - `GETH` (来源: Vector Informatik)
  - `GMAC` (来源: Vector Informatik)
  - `LETH` (来源: Vector Informatik)
  - `RSWITCH2` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On platforms with several, different Ethernet-IPs, the depending instance should be configured.
A selection of the instance gets mandatory, if two vBRSDriverHandlingEthernet instances are configured (two different Ethernet IPs are used in parallel).

If a value is selected, vBRS will generate all depending defines with a value depending infix:
BRS_ETH_infix_CLOCK
BRS_ENABLE_ETH_infix_CHANNEL_x
additional to BRS_ENABLE_ETHERNET_SUPPORT, also BRS_ENABLE_ETHERNET_infix_SUPPORT will be generated.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingEthernet_ClockRef

- **UUID**: `18859f66-fcfe-4f4a-acdf-38c53eb4be50`
- **引用名**: `vBRSDriverHandlingEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 5. vBRSEvalBoardInfo

**容器属性**:

- **UUID**: `94697fbd-11c3-444a-8789-e57280359553`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBRSEvalBoardOscClock

- **UUID**: `6321af1b-4330-4c76-bad2-fd8c1890e847`
- **参数名**: `vBRSEvalBoardOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the frequency of the oscillator clock, equipped on the specific evaluation board.
This valus will be verified through the vBRS generator to fit with the configured value of vBRSOscClock.

######### STRING 类型参数

########## 1. vBRSEvalBoardDescription

- **UUID**: `49a72bc9-badc-4c5f-be8c-9bc30795b80d`
- **参数名**: `vBRSEvalBoardDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: General description of the supported evaluation board.

########## 2. vBRSEvalBoard

- **UUID**: `ac4d3732-3fbb-4e5c-b909-97780c7e6b75`
- **参数名**: `vBRSEvalBoard`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define, used in SourceCode, for this specific Evaluation Board.
Most times, this is used for board specific pin settings.
Sets the following generated parameters:
BRS_EVA_BOARD_x in vBrsCfg.h

####### 6. vBRSDriverHandlingHyperbus

**容器属性**:

- **UUID**: `94ec0d6d-9b00-4479-bcef-7644a11dcb60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingHyperbus_Clock

- **UUID**: `d2811305-cc77-47ad-a252-860be59cd299`
- **参数名**: `vBRSDriverHandlingHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of Hyperbus driver peripheral clock.
Sets the following generated parameters:
BRS_HYPERBUS_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingHyperbus

- **UUID**: `7ff763a6-c675-4525-b636-5a0b5aaf32b8`
- **参数名**: `vBRSEnableDriverHandlingHyperbus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_HYPERBUS_SUPPORT
is generated.

########## 2. vBRSDriverHandlingHyperbus_channel0

- **UUID**: `9aba9992-d702-49c1-885c-1005b1ba0ba6`
- **参数名**: `vBRSDriverHandlingHyperbus_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_HYPERBUS_CHANNEL_0 in vBrsCfg.h

########## 3. vBRSDriverHandlingHyperbus_channel1

- **UUID**: `938e915b-ad51-4761-8b75-37a5f42f28e8`
- **参数名**: `vBRSDriverHandlingHyperbus_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_HYPERBUS_CHANNEL_1 in vBrsCfg.h

########## 4. vBRSDriverHandlingHyperbus_PeripheralClock

- **UUID**: `aa557a6f-6d48-486c-8d5f-dcb4f9c57c1d`
- **参数名**: `vBRSDriverHandlingHyperbus_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the Hyperbus driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingHyperbus_Clock or
vBRSDriverHandlingHyperbus_ClockRef (if Mcu is used)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingHyperbus_ClockRef

- **UUID**: `c6b56a3c-2f11-4bf4-ad42-f57d2f5f0318`
- **引用名**: `vBRSDriverHandlingHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 7. vBRSDriverHandlingI2C

**容器属性**:

- **UUID**: `c8b7cfe0-99d0-49f2-8b5b-a8e4d32fd201`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingI2C`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingI2C_Clock

- **UUID**: `b8fc738c-618a-4b14-9333-34ed107d9f2e`
- **参数名**: `vBRSDriverHandlingI2C_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of I2C driver peripheral clock.
Sets the following generated parameters:
BRS_I2C_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingI2C

- **UUID**: `6fe706bb-acf4-4ec6-a5c9-3ac1107c255b`
- **参数名**: `vBRSEnableDriverHandlingI2C`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_I2C_SUPPORT
is generated.

########## 2. vBRSDriverHandlingI2C_channel0

- **UUID**: `e7564965-91c3-4212-bb9d-f312224f6ed0`
- **参数名**: `vBRSDriverHandlingI2C_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_I2C_CHANNEL_0 in vBrsCfg.h

########## 3. vBRSDriverHandlingI2C_channel1

- **UUID**: `e0f2f15b-5fa1-4650-9a05-3767be1cc0f7`
- **参数名**: `vBRSDriverHandlingI2C_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_I2C_CHANNEL_1 in vBrsCfg.h

########## 4. vBRSDriverHandlingI2C_PeripheralClock

- **UUID**: `baab4cb7-6b61-47ba-9356-bded12be7749`
- **参数名**: `vBRSDriverHandlingI2C_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the I2C driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingI2C_Clock or
vBRSDriverHandlingI2C_ClockRef (if Mcu is used)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingI2C_ClockRef

- **UUID**: `f28d38a4-057e-43aa-a43a-fb27a4db476a`
- **引用名**: `vBRSDriverHandlingI2C_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

####### 8. vBRSDriverHandlingSpi

**容器属性**:

- **UUID**: `ebc72176-013f-4c58-870f-863185c22bde`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingSpi`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingSpi_Clock

- **UUID**: `23f2c923-9cec-45e3-964e-236b3ac7a757`
- **参数名**: `vBRSDriverHandlingSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of Hyperbus driver peripheral clock.
Sets the following generated parameters:
BRS_SPI_CLOCK in vBrsCfg.h

######### BOOLEAN 类型参数

########## 1. vBRSEnableDriverHandlingSpi

- **UUID**: `6373335a-4f6d-4e31-a0c5-3397946e5399`
- **参数名**: `vBRSEnableDriverHandlingSpi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_SPI_SUPPORT
is generated.

########## 2. vBRSDriverHandlingSpi_channel0

- **UUID**: `c314af5e-24aa-4469-aa99-138f88a77544`
- **参数名**: `vBRSDriverHandlingSpi_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_SPI_CHANNEL_0 in vBrsCfg.h

########## 3. vBRSDriverHandlingSpi_PeripheralClock

- **UUID**: `67821834-0e8f-40e0-b639-3b49c638e0cb`
- **参数名**: `vBRSDriverHandlingSpi_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the Spi driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingSpi_Clock or
vBRSDriverHandlingSpi_ClockRef (if Mcu is used)

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingSpi_ClockRef

- **UUID**: `26b94041-4967-4abe-86f2-1a06182f3a3e`
- **引用名**: `vBRSDriverHandlingSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 4. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `e710850b-9807-403a-a15e-dac30eca6b32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..2]
- **构建后可变**: false

###### 参数配置

此容器包含 **24** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `112689a5-074f-44e8-b676-ed5849623dba`
- **参数名**: `vBRSDriverHandlingCAN_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of CAN driver peripheral clock.
Sets the following generated parameters:
BRS_CAN_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingCAN

- **UUID**: `e60a211b-4c23-410a-9bd3-72452fa2a8c9`
- **参数名**: `vBRSEnableDriverHandlingCAN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_CAN_SUPPORT
is generated.

######## 2. vBRSDriverHandlingCAN_channel0

- **UUID**: `50125c4d-f36d-4638-a9a0-72f5b05f5b7f`
- **参数名**: `vBRSDriverHandlingCAN_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_0 in vBrsCfg.h

######## 3. vBRSDriverHandlingCAN_channel1

- **UUID**: `a130e052-d944-4329-8577-03c0ac13cae9`
- **参数名**: `vBRSDriverHandlingCAN_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_1 in vBrsCfg.h

######## 4. vBRSDriverHandlingCAN_channel2

- **UUID**: `a2bc1791-d245-439f-a962-38125a6fde63`
- **参数名**: `vBRSDriverHandlingCAN_channel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 2.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_2 in vBrsCfg.h

######## 5. vBRSDriverHandlingCAN_channel3

- **UUID**: `42ecea7d-a9d9-483f-8e18-f50586965fab`
- **参数名**: `vBRSDriverHandlingCAN_channel3`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 3.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_3 in vBrsCfg.h

######## 6. vBRSDriverHandlingCAN_channel4

- **UUID**: `4327e1eb-4c6f-4605-a1b4-4f7e7bed847f`
- **参数名**: `vBRSDriverHandlingCAN_channel4`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 4.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_4 in vBrsCfg.h

######## 7. vBRSDriverHandlingCAN_channel5

- **UUID**: `6af209a2-dc6a-4180-b8ac-7fcca0fe1877`
- **参数名**: `vBRSDriverHandlingCAN_channel5`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 5.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_5 in vBrsCfg.h

######## 8. vBRSDriverHandlingCAN_channel6

- **UUID**: `b0a1b96e-1f62-4c9f-902f-f5d1b6812793`
- **参数名**: `vBRSDriverHandlingCAN_channel6`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 6.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_6 in vBrsCfg.h

######## 9. vBRSDriverHandlingCAN_channel7

- **UUID**: `ca77e2e1-6584-42dd-aaa9-23c7c625d9e6`
- **参数名**: `vBRSDriverHandlingCAN_channel7`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 7.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_7 in vBrsCfg.h

######## 10. vBRSDriverHandlingCAN_channel8

- **UUID**: `a0442dec-5f06-4ffb-bb1f-d9d3f85f499a`
- **参数名**: `vBRSDriverHandlingCAN_channel8`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 8.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_8 in vBrsCfg.h

######## 11. vBRSDriverHandlingCAN_channel9

- **UUID**: `be55876a-53b0-4b46-97a2-89fbb7d5b8b6`
- **参数名**: `vBRSDriverHandlingCAN_channel9`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 9.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_9 in vBrsCfg.h

######## 12. vBRSDriverHandlingCAN_PeripheralClock

- **UUID**: `a9a9162b-d922-400f-b8c8-24fe94f354e1`
- **参数名**: `vBRSDriverHandlingCAN_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the CAN driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingCAN_Clock or
vBRSDriverHandlingCAN_ClockRef (if Mcu is used)

######## 13. vBRSDriverHandlingCAN_channel10

- **UUID**: `481a90cb-0a99-4e08-8ab2-098dc99e58d6`
- **参数名**: `vBRSDriverHandlingCAN_channel10`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_10 in vBrsCfg.h

######## 14. vBRSDriverHandlingCAN_channel11

- **UUID**: `0bc5d44c-682c-4753-b305-0b3d4eecf6bb`
- **参数名**: `vBRSDriverHandlingCAN_channel11`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 11.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_11 in vBrsCfg.h

######## 15. vBRSDriverHandlingCAN_channel12

- **UUID**: `47d5d281-f54d-4a56-b154-6c36bc13e935`
- **参数名**: `vBRSDriverHandlingCAN_channel12`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 12.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_12 in vBrsCfg.h

######## 16. vBRSDriverHandlingCAN_channel13

- **UUID**: `90757915-e827-4d00-896b-a9896a6d5699`
- **参数名**: `vBRSDriverHandlingCAN_channel13`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 13.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_13 in vBrsCfg.h

######## 17. vBRSDriverHandlingCAN_channel14

- **UUID**: `821f913f-46f4-429f-a39c-0a414315db86`
- **参数名**: `vBRSDriverHandlingCAN_channel14`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 14.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_14 in vBrsCfg.h

######## 18. vBRSDriverHandlingCAN_channel15

- **UUID**: `208aca06-801c-4164-ba7c-4caedbec05bb`
- **参数名**: `vBRSDriverHandlingCAN_channel15`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 15.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_15 in vBrsCfg.h

######## 19. vBRSDriverHandlingCAN_channel16

- **UUID**: `3a141e0c-a8e1-40eb-a420-187cd50e0166`
- **参数名**: `vBRSDriverHandlingCAN_channel16`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 16.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_16 in vBrsCfg.h

######## 20. vBRSDriverHandlingCAN_channel17

- **UUID**: `75d995a3-8ec5-4cff-af82-f20b4b16de02`
- **参数名**: `vBRSDriverHandlingCAN_channel17`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 17.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_17 in vBrsCfg.h

######## 21. vBRSDriverHandlingCAN_channel18

- **UUID**: `2ef82ccb-dd98-4755-a214-5d50f9e54419`
- **参数名**: `vBRSDriverHandlingCAN_channel18`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 18.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_18 in vBrsCfg.h

######## 22. vBRSDriverHandlingCAN_channel19

- **UUID**: `540e669a-e37c-4ea2-a62c-3925fc05e7c0`
- **参数名**: `vBRSDriverHandlingCAN_channel19`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 19.
Sets the following generated parameter:
BRS_ENABLE_CAN_CHANNEL_19 in vBrsCfg.h

####### ENUMERATION 类型参数

######## 1. vBRSDriverHandlingCAN_Instance

- **UUID**: `f9262aa0-308f-4f81-b8a2-1a95cb83d5c8`
- **参数名**: `vBRSDriverHandlingCAN_Instance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MCAN` (来源: Vector Informatik)
  - `XCAN` (来源: Vector Informatik)
  - `RCAN` (来源: Vector Informatik)
  - `FlexCAN` (来源: Vector Informatik)
  - `RSCAN` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On platforms with several, different CAN-IPs, the depending instance should be configured.
A selection of the instance gets mandatory, if two vBRSDriverHandlingCAN instances are configured (two different CAN IPs are used in parallel).

If a value is selected, vBRS will generate all depending defines with a value depending infix:
BRS_CAN_infix_CLOCK
BRS_ENABLE_CAN_infix_CHANNEL_x
additional to BRS_ENABLE_CAN_SUPPORT, also BRS_ENABLE_CAN_infix_SUPPORT will be generated.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `433ce5f3-8da2-4cf3-9b16-f74b4106fb60`
- **引用名**: `vBRSDriverHandlingCAN_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 5. vBRSDriverHandlingLIN

**容器属性**:

- **UUID**: `5e2190c8-c50c-4d5e-8016-0e4701ca5942`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **26** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `86bb466d-32d9-4e43-8be0-b070f3e687f7`
- **参数名**: `vBRSDriverHandlingLIN_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of LIN driver peripheral clock.
Sets the following generated parameters:
BRS_LIN_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingLIN

- **UUID**: `78774246-5ee1-4168-8ce2-2634743d093c`
- **参数名**: `vBRSEnableDriverHandlingLIN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_LIN_SUPPORT
is generated.

######## 2. vBRSDriverHandlingLIN_channel0

- **UUID**: `d30da48f-414c-4ee6-a1a9-63c5ea871dfb`
- **参数名**: `vBRSDriverHandlingLIN_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_0 in vBrsCfg.h

######## 3. vBRSDriverHandlingLIN_channel1

- **UUID**: `a69c1cea-aaf4-44a9-9a8e-07686ecf004e`
- **参数名**: `vBRSDriverHandlingLIN_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_1 in vBrsCfg.h

######## 4. vBRSDriverHandlingLIN_channel2

- **UUID**: `e3ce23cf-4b68-4796-8807-0862ea36f6ea`
- **参数名**: `vBRSDriverHandlingLIN_channel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 2.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_2 in vBrsCfg.h

######## 5. vBRSDriverHandlingLIN_channel3

- **UUID**: `de9ffd37-8380-460f-b949-ff2f6f4972e0`
- **参数名**: `vBRSDriverHandlingLIN_channel3`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 3.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_3 in vBrsCfg.h

######## 6. vBRSDriverHandlingLIN_channel4

- **UUID**: `10b111d3-402e-427b-a9e6-94dd4a5d6579`
- **参数名**: `vBRSDriverHandlingLIN_channel4`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 4.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_4 in vBrsCfg.h

######## 7. vBRSDriverHandlingLIN_channel5

- **UUID**: `2e035b56-0468-451e-9716-2398852d2804`
- **参数名**: `vBRSDriverHandlingLIN_channel5`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 5.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_5 in vBrsCfg.h

######## 8. vBRSDriverHandlingLIN_channel6

- **UUID**: `65305d56-0a4f-48a8-bd84-10a135022aba`
- **参数名**: `vBRSDriverHandlingLIN_channel6`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 6.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_6 in vBrsCfg.h

######## 9. vBRSDriverHandlingLIN_channel7

- **UUID**: `3786ef43-2b1b-4240-b05a-2070eb326495`
- **参数名**: `vBRSDriverHandlingLIN_channel7`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 7.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_7 in vBrsCfg.h

######## 10. vBRSDriverHandlingLIN_channel8

- **UUID**: `8ba49f7c-806e-4cfb-adcf-9e9c85423b1b`
- **参数名**: `vBRSDriverHandlingLIN_channel8`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 8.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_8 in vBrsCfg.h

######## 11. vBRSDriverHandlingLIN_channel9

- **UUID**: `456f6947-6b07-4ab7-b5f2-d8a3da160dae`
- **参数名**: `vBRSDriverHandlingLIN_channel9`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 9.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_9 in vBrsCfg.h

######## 12. vBRSDriverHandlingLIN_PeripheralClock

- **UUID**: `b73200bf-b18d-4616-b908-cd567a1fa6d0`
- **参数名**: `vBRSDriverHandlingLIN_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the LIN driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingLIN_Clock or
vBRSDriverHandlingLIN_ClockRef (if Mcu is used)

######## 13. vBRSDriverHandlingLIN_channel10

- **UUID**: `3f000c86-1a21-4efe-8258-ac78bc9e1ec9`
- **参数名**: `vBRSDriverHandlingLIN_channel10`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h

######## 14. vBRSDriverHandlingLIN_channel11

- **UUID**: `6e89c7de-e098-4c90-b055-312edefc5589`
- **参数名**: `vBRSDriverHandlingLIN_channel11`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 11.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_11 in vBrsCfg.h

######## 15. vBRSDriverHandlingLIN_channel12

- **UUID**: `0ccbc3f6-d72a-4f4b-8065-bd092f602579`
- **参数名**: `vBRSDriverHandlingLIN_channel12`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 12.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_12 in vBrsCfg.h

######## 16. vBRSDriverHandlingLIN_channel13

- **UUID**: `c875065b-9fe4-449e-a09d-d8ae31db66bc`
- **参数名**: `vBRSDriverHandlingLIN_channel13`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 13.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_13 in vBrsCfg.h

######## 17. vBRSDriverHandlingLIN_channel14

- **UUID**: `363a6dd5-65bd-406f-b2da-316397e63245`
- **参数名**: `vBRSDriverHandlingLIN_channel14`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 14.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_14 in vBrsCfg.h

######## 18. vBRSDriverHandlingLIN_channel15

- **UUID**: `59debbd1-bc45-49a8-a21c-d5accb87f3cc`
- **参数名**: `vBRSDriverHandlingLIN_channel15`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 15.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_15 in vBrsCfg.h

######## 19. vBRSDriverHandlingLIN_channel16

- **UUID**: `0751be5d-10cd-4e24-8223-f5d6cf603408`
- **参数名**: `vBRSDriverHandlingLIN_channel16`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 16.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_16 in vBrsCfg.h

######## 20. vBRSDriverHandlingLIN_channel17

- **UUID**: `7cc2ab64-38c6-4125-af24-6301bd82996f`
- **参数名**: `vBRSDriverHandlingLIN_channel17`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 10.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_10 in vBrsCfg.h

######## 21. vBRSDriverHandlingLIN_channel18

- **UUID**: `0d27b238-0896-447f-854e-8a4fda158331`
- **参数名**: `vBRSDriverHandlingLIN_channel18`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 18.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_18 in vBrsCfg.h

######## 22. vBRSDriverHandlingLIN_channel19

- **UUID**: `96f2ae35-33a7-430c-a64e-9abafee0cd07`
- **参数名**: `vBRSDriverHandlingLIN_channel19`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 19.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_19 in vBrsCfg.h

######## 23. vBRSDriverHandlingLIN_channel20

- **UUID**: `6fc81233-0869-4205-80cf-aeb70c0a2b1a`
- **参数名**: `vBRSDriverHandlingLIN_channel20`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 20.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_20 in vBrsCfg.h

######## 24. vBRSDriverHandlingLIN_channel21

- **UUID**: `a952f3f5-691c-40dc-a12a-20d9553adc2f`
- **参数名**: `vBRSDriverHandlingLIN_channel21`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 21.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_21 in vBrsCfg.h

######## 25. vBRSDriverHandlingLIN_channel22

- **UUID**: `b16a55c5-7691-44e4-b577-73b87cc4e009`
- **参数名**: `vBRSDriverHandlingLIN_channel22`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 22.
Sets the following generated parameter:
BRS_ENABLE_LIN_CHANNEL_22 in vBrsCfg.h

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingLIN_ClockRef

- **UUID**: `8e4b594f-ed1f-4fcd-a882-902d0df26452`
- **引用名**: `vBRSDriverHandlingLIN_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 6. vBRSDriverHandlingFlexray

**容器属性**:

- **UUID**: `0d48f4f4-19f1-4842-86f6-4ac169fcf2c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `b6ed573f-f27c-4dc9-87e9-cdadbab6a6bf`
- **参数名**: `vBRSDriverHandlingFlexray_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of FlexRay driver peripheral clock.
Sets the following generated parameters:
BRS_FLEXRAY_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingFlexray

- **UUID**: `dc711d46-cf94-4771-a785-5ceaebc3cd80`
- **参数名**: `vBRSEnableDriverHandlingFlexray`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_FLEXRAY_SUPPORT
is generated.

######## 2. vBRSDriverHandlingFlexray_channel0A

- **UUID**: `59e82502-9ca0-463d-8b5a-d349a5b30c26`
- **参数名**: `vBRSDriverHandlingFlexray_channel0A`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0A.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_0A in vBrsCfg.h

######## 3. vBRSDriverHandlingFlexray_channel0B

- **UUID**: `ab83f595-87e1-4ff6-a7fb-cc294d8b44aa`
- **参数名**: `vBRSDriverHandlingFlexray_channel0B`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0B.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_0B in vBrsCfg.h

######## 4. vBRSDriverHandlingFlexray_channel1A

- **UUID**: `4bb3d532-9cbd-4170-b3c2-3e47ecbf4810`
- **参数名**: `vBRSDriverHandlingFlexray_channel1A`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1A.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_1A in vBrsCfg.h

######## 5. vBRSDriverHandlingFlexray_channel1B

- **UUID**: `5f4a7d2e-d24f-492e-ba11-c71fbf838bb1`
- **参数名**: `vBRSDriverHandlingFlexray_channel1B`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1B.
Sets the following generated parameter:
BRS_ENABLE_FLEXRAY_CHANNEL_1B in vBrsCfg.h

######## 6. vBRSDriverHandlingFlexray_PeripheralClock

- **UUID**: `4215e850-d032-4a46-a43e-729ec70da3e1`
- **参数名**: `vBRSDriverHandlingFlexray_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the FlexRay driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingFlexray_Clock or
vBRSDriverHandlingFlexray_ClockRef (if Mcu is used)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingFlexray_ClockRef

- **UUID**: `774d8637-f957-417c-bf57-2faeb6fc9d0a`
- **引用名**: `vBRSDriverHandlingFlexray_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 7. vBRSDriverHandlingEthernet

**容器属性**:

- **UUID**: `9e8fd1a8-b15f-4924-a93a-fc89db6b3b2a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..2]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `a775d1eb-7505-4353-8be1-b81a0899d624`
- **参数名**: `vBRSDriverHandlingEthernet_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of EtherNet driver peripheral clock.
Sets the following generated parameters:
BRS_ETHERNET_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingEthernet

- **UUID**: `e2ef25f0-1815-43b4-83ed-49f60f5850f0`
- **参数名**: `vBRSEnableDriverHandlingEthernet`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_ETHERNET_SUPPORT
is generated.

######## 2. vBRSDriverHandlingEthernet_PeripheralClock

- **UUID**: `d438db9e-a3de-4f39-bf25-35f80bda0348`
- **参数名**: `vBRSDriverHandlingEthernet_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the EtherNet driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingEthernet_Clock or
vBRSDriverHandlingEthernet_ClockRef (if Mcu is used)

####### ENUMERATION 类型参数

######## 1. vBRSDriverHandlingEthernet_Instance

- **UUID**: `3fe35d0d-047e-432c-acbc-4f6d8457ad3c`
- **参数名**: `vBRSDriverHandlingEthernet_Instance`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETNA` (来源: Vector Informatik)
  - `ETNB` (来源: Vector Informatik)
  - `ETNF` (来源: Vector Informatik)
  - `GETH` (来源: Vector Informatik)
  - `GMAC` (来源: Vector Informatik)
  - `LETH` (来源: Vector Informatik)
  - `RSWITCH2` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On platforms with several, different Ethernet-IPs, the depending instance should be configured.
A selection of the instance gets mandatory, if two vBRSDriverHandlingEthernet instances are configured (two different Ethernet IPs are used in parallel).

If a value is selected, vBRS will generate all depending defines with a value depending infix:
BRS_ETH_infix_CLOCK
BRS_ENABLE_ETH_infix_CHANNEL_x
additional to BRS_ENABLE_ETHERNET_SUPPORT, also BRS_ENABLE_ETHERNET_infix_SUPPORT will be generated.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingEthernet_ClockRef

- **UUID**: `18859f66-fcfe-4f4a-acdf-38c53eb4be50`
- **引用名**: `vBRSDriverHandlingEthernet_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 8. vBRSEvalBoardInfo

**容器属性**:

- **UUID**: `94697fbd-11c3-444a-8789-e57280359553`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBRSEvalBoardOscClock

- **UUID**: `6321af1b-4330-4c76-bad2-fd8c1890e847`
- **参数名**: `vBRSEvalBoardOscClock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the frequency of the oscillator clock, equipped on the specific evaluation board.
This valus will be verified through the vBRS generator to fit with the configured value of vBRSOscClock.

####### STRING 类型参数

######## 1. vBRSEvalBoardDescription

- **UUID**: `49a72bc9-badc-4c5f-be8c-9bc30795b80d`
- **参数名**: `vBRSEvalBoardDescription`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: General description of the supported evaluation board.

######## 2. vBRSEvalBoard

- **UUID**: `ac4d3732-3fbb-4e5c-b909-97780c7e6b75`
- **参数名**: `vBRSEvalBoard`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Define, used in SourceCode, for this specific Evaluation Board.
Most times, this is used for board specific pin settings.
Sets the following generated parameters:
BRS_EVA_BOARD_x in vBrsCfg.h

##### 9. vBRSDriverHandlingHyperbus

**容器属性**:

- **UUID**: `94ec0d6d-9b00-4479-bcef-7644a11dcb60`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingHyperbus_Clock

- **UUID**: `d2811305-cc77-47ad-a252-860be59cd299`
- **参数名**: `vBRSDriverHandlingHyperbus_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of Hyperbus driver peripheral clock.
Sets the following generated parameters:
BRS_HYPERBUS_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingHyperbus

- **UUID**: `7ff763a6-c675-4525-b636-5a0b5aaf32b8`
- **参数名**: `vBRSEnableDriverHandlingHyperbus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_HYPERBUS_SUPPORT
is generated.

######## 2. vBRSDriverHandlingHyperbus_channel0

- **UUID**: `9aba9992-d702-49c1-885c-1005b1ba0ba6`
- **参数名**: `vBRSDriverHandlingHyperbus_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_HYPERBUS_CHANNEL_0 in vBrsCfg.h

######## 3. vBRSDriverHandlingHyperbus_channel1

- **UUID**: `938e915b-ad51-4761-8b75-37a5f42f28e8`
- **参数名**: `vBRSDriverHandlingHyperbus_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_HYPERBUS_CHANNEL_1 in vBrsCfg.h

######## 4. vBRSDriverHandlingHyperbus_PeripheralClock

- **UUID**: `aa557a6f-6d48-486c-8d5f-dcb4f9c57c1d`
- **参数名**: `vBRSDriverHandlingHyperbus_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the Hyperbus driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingHyperbus_Clock or
vBRSDriverHandlingHyperbus_ClockRef (if Mcu is used)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingHyperbus_ClockRef

- **UUID**: `c6b56a3c-2f11-4bf4-ad42-f57d2f5f0318`
- **引用名**: `vBRSDriverHandlingHyperbus_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 10. vBRSDriverHandlingI2C

**容器属性**:

- **UUID**: `c8b7cfe0-99d0-49f2-8b5b-a8e4d32fd201`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingI2C`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingI2C_Clock

- **UUID**: `b8fc738c-618a-4b14-9333-34ed107d9f2e`
- **参数名**: `vBRSDriverHandlingI2C_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of I2C driver peripheral clock.
Sets the following generated parameters:
BRS_I2C_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingI2C

- **UUID**: `6fe706bb-acf4-4ec6-a5c9-3ac1107c255b`
- **参数名**: `vBRSEnableDriverHandlingI2C`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_I2C_SUPPORT
is generated.

######## 2. vBRSDriverHandlingI2C_channel0

- **UUID**: `e7564965-91c3-4212-bb9d-f312224f6ed0`
- **参数名**: `vBRSDriverHandlingI2C_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_I2C_CHANNEL_0 in vBrsCfg.h

######## 3. vBRSDriverHandlingI2C_channel1

- **UUID**: `e0f2f15b-5fa1-4650-9a05-3767be1cc0f7`
- **参数名**: `vBRSDriverHandlingI2C_channel1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 1.
Sets the following generated parameter:
BRS_ENABLE_I2C_CHANNEL_1 in vBrsCfg.h

######## 4. vBRSDriverHandlingI2C_PeripheralClock

- **UUID**: `baab4cb7-6b61-47ba-9356-bded12be7749`
- **参数名**: `vBRSDriverHandlingI2C_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the I2C driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingI2C_Clock or
vBRSDriverHandlingI2C_ClockRef (if Mcu is used)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingI2C_ClockRef

- **UUID**: `f28d38a4-057e-43aa-a43a-fb27a4db476a`
- **引用名**: `vBRSDriverHandlingI2C_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 11. vBRSDriverHandlingSpi

**容器属性**:

- **UUID**: `ebc72176-013f-4c58-870f-863185c22bde`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingSpi`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingSpi_Clock

- **UUID**: `23f2c923-9cec-45e3-964e-236b3ac7a757`
- **参数名**: `vBRSDriverHandlingSpi_Clock`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..18446744073709551615]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Frequency, used for PLL calculation of Hyperbus driver peripheral clock.
Sets the following generated parameters:
BRS_SPI_CLOCK in vBrsCfg.h

####### BOOLEAN 类型参数

######## 1. vBRSEnableDriverHandlingSpi

- **UUID**: `6373335a-4f6d-4e31-a0c5-3397946e5399`
- **参数名**: `vBRSEnableDriverHandlingSpi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This switch enables the handling of driver specific settings of
- PLL and clock settings
- Port Pin settings
- On some platforms additional register settings, e.g. inside BrsHwPreInitPowerOn() or BrsHw_EnableHwAccess()

To handle this inside the BrsHw Sourcecode, the define
BRS_ENABLE_SPI_SUPPORT
is generated.

######## 2. vBRSDriverHandlingSpi_channel0

- **UUID**: `c314af5e-24aa-4469-aa99-138f88a77544`
- **参数名**: `vBRSDriverHandlingSpi_channel0`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the configuration of communication channel 0.
Sets the following generated parameter:
BRS_ENABLE_SPI_CHANNEL_0 in vBrsCfg.h

######## 3. vBRSDriverHandlingSpi_PeripheralClock

- **UUID**: `67821834-0e8f-40e0-b639-3b49c638e0cb`
- **参数名**: `vBRSDriverHandlingSpi_PeripheralClock`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, the clock defined in 
vBRSHwConfig/vBRSPeriphClock
will also be used for the peripheral clock, used by the Spi driver.

If the clock, provided to the driver cell, is different, disable this parameter and configure the valid frequency within the paramter 
vBRSDriverHandlingSpi_Clock or
vBRSDriverHandlingSpi_ClockRef (if Mcu is used)

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingSpi_ClockRef

- **UUID**: `26b94041-4967-4abe-86f2-1a06182f3a3e`
- **引用名**: `vBRSDriverHandlingSpi_ClockRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: McuClockReferencePoint reference for peripheral clock setting.
If set, a solving action is provided to set the peripheral clock to the value, this reference is pointing to.

##### 12. vBRSTestsuiteSupport

**容器属性**:

- **UUID**: `e0512161-63a8-4f3b-a119-88900ca77b73`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTestsuiteSupport`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Support for Vector internal Testsuites

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. vBRSEnableTestsuiteSupport

- **UUID**: `920114e9-4ef0-46bc-bf7e-75a5671f200c`
- **参数名**: `vBRSEnableTestsuiteSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support of the Generic TestSuite connectioin.
Via the define BRS_ENABLE_TESTSUITE_SUPPORT, the Generic TestSuite concept headerfile BrsTestsuite.h will be included and the Generic Testsuite init function BrsTestsuiteInit() will be called within BrsMain.c

####### ENUMERATION 类型参数

######## 1. vBRSTccSupport

- **UUID**: `a039648c-5e17-40b9-b56e-dbc8f6732015`
- **参数名**: `vBRSTccSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `None` (来源: Vector Informatik)
  - `TCCviaComIf` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: vBRS Tcc Support

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vBRSTcc

**容器属性**:

- **UUID**: `fc68bdb3-81f7-4ae7-abbb-6a9a95884ce6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `90335ddf-0ae0-4625-80a6-f5925e54e0ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDU that is received by the BRS through communication stack.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBRSComIfHandleId

- **UUID**: `a9af495c-2ff2-41d5-9ce1-7a0df2927e79`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBRSComIfPduRef

- **UUID**: `35d7b521-ee05-40aa-8668-4950c1e236fd`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######### 2. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `e104cbb9-8f6c-474c-9cc3-77dca44bbe35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Tx PDU that is transmitted by the CDD through communication stack.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. vBRSComIfHandleId

- **UUID**: `a4f39e98-4026-4ad3-93f9-59b932cb8f1e`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. vBRSComIfPduRef

- **UUID**: `d271a034-cc35-4231-b7fa-0e5f2eb38833`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `90335ddf-0ae0-4625-80a6-f5925e54e0ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDU that is received by the BRS through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBRSComIfHandleId

- **UUID**: `a9af495c-2ff2-41d5-9ce1-7a0df2927e79`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSComIfPduRef

- **UUID**: `35d7b521-ee05-40aa-8668-4950c1e236fd`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 3. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `e104cbb9-8f6c-474c-9cc3-77dca44bbe35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Tx PDU that is transmitted by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBRSComIfHandleId

- **UUID**: `a4f39e98-4026-4ad3-93f9-59b932cb8f1e`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSComIfPduRef

- **UUID**: `d271a034-cc35-4231-b7fa-0e5f2eb38833`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 13. vBRSTcc

**容器属性**:

- **UUID**: `fc68bdb3-81f7-4ae7-abbb-6a9a95884ce6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `90335ddf-0ae0-4625-80a6-f5925e54e0ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDU that is received by the BRS through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBRSComIfHandleId

- **UUID**: `a9af495c-2ff2-41d5-9ce1-7a0df2927e79`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSComIfPduRef

- **UUID**: `35d7b521-ee05-40aa-8668-4950c1e236fd`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

####### 2. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `e104cbb9-8f6c-474c-9cc3-77dca44bbe35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Tx PDU that is transmitted by the CDD through communication stack.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. vBRSComIfHandleId

- **UUID**: `a4f39e98-4026-4ad3-93f9-59b932cb8f1e`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSComIfPduRef

- **UUID**: `d271a034-cc35-4231-b7fa-0e5f2eb38833`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 14. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `90335ddf-0ae0-4625-80a6-f5925e54e0ed`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerRxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Rx PDU that is received by the BRS through communication stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBRSComIfHandleId

- **UUID**: `a9af495c-2ff2-41d5-9ce1-7a0df2927e79`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSComIfPduRef

- **UUID**: `35d7b521-ee05-40aa-8668-4950c1e236fd`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 15. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `e104cbb9-8f6c-474c-9cc3-77dca44bbe35`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSComIfUpperLayerTxPdu`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container specifies Tx PDU that is transmitted by the CDD through communication stack.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. vBRSComIfHandleId

- **UUID**: `a4f39e98-4026-4ad3-93f9-59b932cb8f1e`
- **参数名**: `vBRSComIfHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for the Pdu.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSComIfPduRef

- **UUID**: `d271a034-cc35-4231-b7fa-0e5f2eb38833`
- **引用名**: `vBRSComIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

##### 16. vBRSMemoryInit

**容器属性**:

- **UUID**: `13a9d13b-6a98-4309-83fa-9ffc896db970`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSMemoryInit`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBRSInitPatternBlocks

- **UUID**: `66116b34-b15d-46ec-b6be-77f7ce9562dd`
- **参数名**: `vBRSInitPatternBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_ApplicationEntry().
This value is for the blocks, configured with "Init Policy" = ZERO_INIT and a "Init Stage" from ZERO up to THREE within the vLinkGen configuration.
The pattern must be 32-bit aligned.
Default value is 0x0.

######## 2. vBRSInitPatternHardResetBlocks

- **UUID**: `74533119-ca7a-4f27-8c66-27d671cfe458`
- **参数名**: `vBRSInitPatternHardResetBlocks`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_ApplicationEntry().
This value is for the blocks, configured with "Init Policy" = ZERO_INIT and the "Init Stage" HARD_RESET_ONLY within the vLinkGen configuration.
The pattern must be 32-bit aligned.
Default value is 0x0.

######## 3. vBRSInitPatternAreas

- **UUID**: `68ad48d0-dce0-4081-9761-828c0e031021`
- **参数名**: `vBRSInitPatternAreas`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_ApplicationEntry().
This value is for the groups, configured with "Init Policy" = ZERO_INIT and a "Init Stage" from ZERO up to THREE within the vLinkGen configuration.
The pattern must be 32-bit aligned.
Default value is 0x0.

######## 4. vBRSInitPatternHardResetAreas

- **UUID**: `9a1260c8-939d-4d0a-b4cd-a2a800922711`
- **参数名**: `vBRSInitPatternHardResetAreas`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_ApplicationEntry().
This value is for the groups, configured with "Init Policy" = ZERO_INIT and the "Init Stage" HARD_RESET_ONLY within the vLinkGen configuration.
The pattern must be 32-bit aligned.
Default value is 0x0.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **vBRS_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **vBRS**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **vBRS_Pre**
2. **vBRS_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. vBRS_Impl

- **UUID**: `3a4be892-fa67-4225-9a50-4d0320007c32`
- **实现名称**: `vBRS_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vBRS_Pre

- **UUID**: `f8a1a2cd-4bbe-4695-bee8-e04f388ec86e`
- **配置名称**: `vBRS_Pre`
- **定义引用**: `/MICROSAR/vBRS`

### 2. vBRS_Rec

- **UUID**: `efcc141c-7aa6-4a8b-9344-d0e8100cd765`
- **配置名称**: `vBRS_Rec`
- **定义引用**: `/MICROSAR/vBRS`
