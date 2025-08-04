# vBRS - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:50:56

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

- **UUID**: `3d6c4b68-93ce-4e32-a675-63dc141ae480`
- **模块名称**: `vBRS`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Basic Runtime System.

#### 版本历史

共有 **5** 个版本记录：

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

#### 配置容器

本模块包含 **12** 个配置容器：

##### 1. vBRSGeneral

**容器属性**:

- **UUID**: `bb882025-f8ef-4820-b10a-520712c7af28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration parameters of the vBRS.

###### 参数配置

此容器包含 **12** 个参数：

####### BOOLEAN 类型参数

######## 1. vBRSEnableSupportLEDs

- **UUID**: `a475ebec-4229-4a0c-be19-d645882ffcf8`
- **参数名**: `vBRSEnableSupportLEDs`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a blinking live-LED for the used EvalBoard
Sets the following generated parameters:
BRS_ENABLE_SUPPORT_LEDS in vBrsCfg.h

######## 2. vBRSEnableSafeContextSupport

- **UUID**: `ec531c9c-dc87-448a-a404-1603ad6f9191`
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

- **UUID**: `3ffe05ed-defd-4255-9810-5eb28f663ad9`
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

- **UUID**: `2689f64a-3654-4ee4-82a7-c4f6e687821f`
- **参数名**: `vBRSEnableSupportToggleWdPin`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a blinking live-LED for the used EvalBoard
Sets the following generated parameters:
BRS_ENABLE_SUPPORT_TOGGLE_WD_PIN in vBrsCfg.h

######## 5. vBRSEnableSupportToggleCustomPin

- **UUID**: `a62f3135-661c-425d-8b3e-955cd933b056`
- **参数名**: `vBRSEnableSupportToggleCustomPin`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Use the functionality of a blinking live-LED for the used EvalBoard
Sets the following generated parameters:
BRS_ENABLE_SUPPORT_TOGGLE_CUSTOM_PIN in vBrsCfg.h

######## 6. vBRSEnableEcuMStubGeneration

- **UUID**: `1947fd9a-6d78-4444-997a-5602624f235e`
- **参数名**: `vBRSEnableEcuMStubGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If no real EcuM is part of the configuration this functionality generates an EcuM.c/h stub that calls the Init-functions of the Asr modules as specified in the EcuC configuration.

######## 7. vBRSDisableSetupSupport

- **UUID**: `c9bdd18d-7188-4912-bdfd-790973ad25b5`
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

- **UUID**: `15b41f44-cf5c-49f7-8d13-7050599cf9aa`
- **参数名**: `vBRSEnableSchmStubGeneration`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate this, if the SchM stubs containing the defines for EXCLUSIVE AREAs should be generated.

######## 9. vBRSEnableSchmStubSupportDrvCanAN

- **UUID**: `2d9c352f-b34c-49e2-8dcd-9a8f31878381`
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
As described within CanDriver ApplicationNote AN-ISC-8-1149

######## 10. vBRSEnableHSMSupport

- **UUID**: `02332af1-3dcf-401f-9231-b864e9ac6e7d`
- **参数名**: `vBRSEnableHSMSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable support of HSM Core UseCase.
Sets the following generated parameters:
BRS_ENABLE_HSM_SUPPORT in vBrsCfg.h

####### STRING 类型参数

######## 1. vBRSUserConfigFile

- **UUID**: `cc60ef48-3bc0-455d-a809-d4a07376982b`
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

######## 1. vBRSFblSupport

- **UUID**: `c9c9aa04-8669-4a13-9983-1a9eed8171db`
- **参数名**: `vBRSFblSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Disabled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Disabled` (来源: Vector Informatik)
  - `Legacy` (来源: Vector Informatik)
  - `WithoutOSScheduling` (来源: Vector Informatik)
  - `OSScheduling` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the support for FlashBootLoader projects.
Sets the following generated parameters:
BRS_ENABLE_FBL in vBrsCfg.h, additional to one of the following:
BRS_FBL_LEGACY, BRS_FBL_NO_OSSCHEDULE, BRS_FBL_OSSCHEDULE

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSToggleLEDDioChannel

- **UUID**: `a4e3946e-a6aa-4680-95ba-dbe6a0845946`
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

- **UUID**: `c6a7ce01-85cf-44fb-9d51-57922171864a`
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

- **UUID**: `06feb7af-96ea-4c15-8231-e0eec3651799`
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

##### 2. vBRSHwConfig

**容器属性**:

- **UUID**: `bacc25bd-3c8c-45e2-956b-eebd74fe88bb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSHwConfig`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. vBRSOscClock

- **UUID**: `49b3f15a-0e60-47c4-b9d4-a885be4ce6a4`
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
BRS_OSC_CLK  in BrsCfg.h 
MAIN_OSC_CLK in Makefile.config.generated

######## 2. vBRSTimebaseClock

- **UUID**: `3000fa4f-fdb3-4e27-ac75-02136f810785`
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
BRS_TIMEBASE_CLOCK in BrsCfg.h 
TIMEBASE_CLOCK in Makefile.config.generated

######## 3. vBRSPeriphClock

- **UUID**: `0cb893a3-c6c8-44fa-8cd6-65bd08431c38`
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
- **描述**: Frequency, used for PLL calculation (normally used as CPU core clock).
Sets the following generated parameters:
BRS_PERIPH_CLOCK in BrsCfg.h 
PERIPH_CLOCK in Makefile.config.generated

####### BOOLEAN 类型参数

######## 1. vBRSEnablePortHandling

- **UUID**: `54206c8d-cddf-44c6-a29d-4884d95a9c0e`
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
BRS_ENABLE_PORT in BrsCfg.h

######## 2. vBRSEnableWatchdogHandling

- **UUID**: `752d1115-29fb-45fa-8985-7d64e34d7873`
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
BRS_ENABLE_WATCHDOG in BrsCfg.h

######## 3. vBRSEnablePLLClocksHandling

- **UUID**: `d7e68e18-3245-46df-a02f-ae8d9b52b535`
- **参数名**: `vBRSEnablePLLClocksHandling`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable the handling of PLL&Clocks configuration inside BrsHw.
Sets the following generated parameter:
BRS_ENABLE_PLLCLOCKS in BrsCfg.h

######## 4. vBRSCompilerEnableFPU

- **UUID**: `127a23dc-aec7-4bbd-87d3-391e505c47a0`
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
BrsCfg.h: BRS_FPU_USED

####### STRING 类型参数

######## 1. vBRSPeriphClockDescription

- **UUID**: `3e40bec2-0481-4ec1-8354-1ed632289ac7`
- **参数名**: `vBRSPeriphClockDescription`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Platform/family specific preconfig parameter with description of the recommended platform/family clock values and for usage of the peripheral clock (connection to OS timer).

####### ENUMERATION 类型参数

######## 1. vBRSCompilerInstructionSet

- **UUID**: `dc60561f-3c86-46c6-960c-ce4adac23176`
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
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select the platform dependent Instruction Set for compile/link of the project.
Note: not all platforms are supporting different instruction sets.
Generated as the following:
Makefile.config.generated: INSTRUCTION_SET = xxx
BrsCfg.h: BRS_INSTRUCTION_SET_xxx

####### MULTILINE-STRING 类型参数

######## 1. vBRSMakefileUserCode

- **UUID**: `871793a1-d3c0-4855-b587-1e0c1639583f`
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

- **UUID**: `491b3333-9050-4e22-8ca4-755a2ee85de5`
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

- **UUID**: `562bb218-f781-4cf4-88b5-a8ee28db1948`
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
BRS_EVA_BOARD_xxx in BrsCfg.h 
EVA_BOARD in Makefile.config.generated

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `666d966b-dc52-4e56-b0d9-15333115de1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **13** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `a21ce4e9-2768-4c75-84bf-63c7790b5a4b`
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

- **UUID**: `7fa71e59-f71a-4202-9701-d1deccfb09b2`
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
is genrated.

########## 2. vBRSDriverHandlingCAN_channel0

- **UUID**: `f786037d-728d-47b1-84a8-b363b0bac48c`
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

- **UUID**: `bee954e4-f93a-488b-80fc-875588f4852f`
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

- **UUID**: `5f1a1d92-a22b-4e37-8873-8b74a63e8be3`
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

- **UUID**: `fbee95e3-c0e6-40e3-a36c-99d613ea2f1f`
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

- **UUID**: `27f469c1-5e15-4a24-aa9c-f3397780d64e`
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

- **UUID**: `b53498ad-013f-4ccb-8359-6333c1c1ad3a`
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

- **UUID**: `7a304631-7ec2-40a4-956a-72811143c4b9`
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

- **UUID**: `5f6e203f-b592-4289-b0f0-50ef7cbfaf7a`
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

- **UUID**: `dbdabdfa-1afb-4c1f-8dae-2cca12dd067a`
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

- **UUID**: `8a41b9cb-95b3-4e82-8c39-7b258bf981a3`
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

- **UUID**: `746b7558-b794-4dfc-bb4d-32658ef6d469`
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

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `8a8c5ec1-e018-4711-9114-f9047a977a5d`
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

- **UUID**: `72388ed4-e12a-4fa5-b9d7-f57089a4fddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **26** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `28b5975b-7499-45f0-b336-0aa3f120c67c`
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

- **UUID**: `44cf4bfc-3b59-4983-985f-e1e263c0959d`
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
is genrated.

########## 2. vBRSDriverHandlingLIN_channel0

- **UUID**: `95cc802a-1ff6-4598-953e-409c77fc443d`
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

- **UUID**: `2a73a38b-04b3-4367-93ea-187cb7bfe850`
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

- **UUID**: `5299ca95-7b22-4d5e-851a-36cdc1e1acfb`
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

- **UUID**: `9a7ba021-6492-4889-8674-401902135df4`
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

- **UUID**: `1267f38e-c1f1-46b0-b8a4-08b2e87ee325`
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

- **UUID**: `6055702f-147a-445b-b12b-baf1d6164c54`
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

- **UUID**: `ee28fb2e-8acc-4b97-8911-cc1b0047000e`
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

- **UUID**: `d52acda5-7ede-4d5c-86c3-18dfa7191e6c`
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

- **UUID**: `3d358a0c-8b7a-45e7-a60d-a4d392125430`
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

- **UUID**: `d26e53a4-930b-4ada-92cc-c50e61cca635`
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

- **UUID**: `306922d8-f561-4291-9302-9acc9e5559d4`
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

- **UUID**: `bee7c712-f8b4-4b84-b841-6a78d75a3f10`
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

- **UUID**: `63d36744-e6eb-4fbe-aa75-828c7f977384`
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

- **UUID**: `2a82d389-8b4c-4de7-ab3f-1d23f8c59c21`
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

- **UUID**: `8df52179-cb28-4950-a0e4-4f62cea86ea2`
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

- **UUID**: `1c8eafcc-d2ad-4462-808d-fd82cf5805e1`
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

- **UUID**: `ffd07b8d-f51d-4a21-bc80-4f7cad966af8`
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

- **UUID**: `c6317f3f-eba8-4be2-8a25-b506e7989d9b`
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

- **UUID**: `f1f0c9a5-786c-4e22-91aa-fef116911bd4`
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

- **UUID**: `5b8f3d86-d198-4b33-a653-db8738b6ad72`
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

- **UUID**: `3d0b4376-8c84-4a17-bec8-8349654d09f4`
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

- **UUID**: `6a508ea9-ff4a-491c-9db6-3f052f3f2ed1`
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

- **UUID**: `3fb2889a-1e7d-4fba-af5b-baa9a34b0ccf`
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

- **UUID**: `abd70e5c-070a-4736-b781-9b7606ab67bc`
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

- **UUID**: `4650b3d8-56a4-4c59-9e5d-88c55cd87c71`
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

- **UUID**: `9a69c72f-3c13-44b2-84c3-e642ecef1133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `7b3a0f78-776e-4161-bc9b-2c643578b4df`
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

- **UUID**: `aa7a9e83-b4ac-4ce8-9c26-8104e43e85cc`
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
is genrated.

########## 2. vBRSDriverHandlingFlexray_channel0A

- **UUID**: `9d140e60-c3a7-4be3-96b8-427b0f28c4bd`
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

- **UUID**: `fa9fd5a7-4ba9-4ed8-b3f8-b2188ab93db9`
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

- **UUID**: `b78c3ce9-17e9-41cd-9788-e91f67a88be9`
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

- **UUID**: `89bbf9c7-0204-446d-9d01-1080cbd7c45a`
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

- **UUID**: `36617ead-159a-4e0b-ac88-200453a85de6`
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

- **UUID**: `2b98fbfd-1e40-47d6-8ef0-db9d705599d9`
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

- **UUID**: `129f46fb-7cbd-42c7-a71d-26c4af70c239`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `904d3034-8c0b-4ea8-9a1b-34782fb12adc`
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

- **UUID**: `bf2cdb1c-0230-422b-8725-313b0112522e`
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
is genrated.

########## 2. vBRSDriverHandlingEthernet_PeripheralClock

- **UUID**: `0e9e5206-6ea9-4102-a535-b513da765524`
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

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingEthernet_ClockRef

- **UUID**: `d3d04cdf-337e-4541-ac17-077b5554d50e`
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

- **UUID**: `aaf1b66c-be23-42a0-ba74-67339fe1947c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBRSEvalBoardOscClock

- **UUID**: `067b0a10-9c71-4285-8c10-7e8dd71d0855`
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

- **UUID**: `19b52e1c-c70a-44f6-8cbe-1998f6dc3b1f`
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

- **UUID**: `e2189ef8-2b2c-4102-a78b-4291f53c4bb3`
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

##### 3. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `666d966b-dc52-4e56-b0d9-15333115de1c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **13** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `a21ce4e9-2768-4c75-84bf-63c7790b5a4b`
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

- **UUID**: `7fa71e59-f71a-4202-9701-d1deccfb09b2`
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
is genrated.

######## 2. vBRSDriverHandlingCAN_channel0

- **UUID**: `f786037d-728d-47b1-84a8-b363b0bac48c`
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

- **UUID**: `bee954e4-f93a-488b-80fc-875588f4852f`
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

- **UUID**: `5f1a1d92-a22b-4e37-8873-8b74a63e8be3`
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

- **UUID**: `fbee95e3-c0e6-40e3-a36c-99d613ea2f1f`
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

- **UUID**: `27f469c1-5e15-4a24-aa9c-f3397780d64e`
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

- **UUID**: `b53498ad-013f-4ccb-8359-6333c1c1ad3a`
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

- **UUID**: `7a304631-7ec2-40a4-956a-72811143c4b9`
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

- **UUID**: `5f6e203f-b592-4289-b0f0-50ef7cbfaf7a`
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

- **UUID**: `dbdabdfa-1afb-4c1f-8dae-2cca12dd067a`
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

- **UUID**: `8a41b9cb-95b3-4e82-8c39-7b258bf981a3`
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

- **UUID**: `746b7558-b794-4dfc-bb4d-32658ef6d469`
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

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `8a8c5ec1-e018-4711-9114-f9047a977a5d`
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

##### 4. vBRSDriverHandlingLIN

**容器属性**:

- **UUID**: `72388ed4-e12a-4fa5-b9d7-f57089a4fddf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **26** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `28b5975b-7499-45f0-b336-0aa3f120c67c`
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

- **UUID**: `44cf4bfc-3b59-4983-985f-e1e263c0959d`
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
is genrated.

######## 2. vBRSDriverHandlingLIN_channel0

- **UUID**: `95cc802a-1ff6-4598-953e-409c77fc443d`
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

- **UUID**: `2a73a38b-04b3-4367-93ea-187cb7bfe850`
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

- **UUID**: `5299ca95-7b22-4d5e-851a-36cdc1e1acfb`
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

- **UUID**: `9a7ba021-6492-4889-8674-401902135df4`
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

- **UUID**: `1267f38e-c1f1-46b0-b8a4-08b2e87ee325`
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

- **UUID**: `6055702f-147a-445b-b12b-baf1d6164c54`
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

- **UUID**: `ee28fb2e-8acc-4b97-8911-cc1b0047000e`
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

- **UUID**: `d52acda5-7ede-4d5c-86c3-18dfa7191e6c`
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

- **UUID**: `3d358a0c-8b7a-45e7-a60d-a4d392125430`
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

- **UUID**: `d26e53a4-930b-4ada-92cc-c50e61cca635`
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

- **UUID**: `306922d8-f561-4291-9302-9acc9e5559d4`
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

- **UUID**: `bee7c712-f8b4-4b84-b841-6a78d75a3f10`
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

- **UUID**: `63d36744-e6eb-4fbe-aa75-828c7f977384`
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

- **UUID**: `2a82d389-8b4c-4de7-ab3f-1d23f8c59c21`
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

- **UUID**: `8df52179-cb28-4950-a0e4-4f62cea86ea2`
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

- **UUID**: `1c8eafcc-d2ad-4462-808d-fd82cf5805e1`
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

- **UUID**: `ffd07b8d-f51d-4a21-bc80-4f7cad966af8`
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

- **UUID**: `c6317f3f-eba8-4be2-8a25-b506e7989d9b`
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

- **UUID**: `f1f0c9a5-786c-4e22-91aa-fef116911bd4`
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

- **UUID**: `5b8f3d86-d198-4b33-a653-db8738b6ad72`
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

- **UUID**: `3d0b4376-8c84-4a17-bec8-8349654d09f4`
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

- **UUID**: `6a508ea9-ff4a-491c-9db6-3f052f3f2ed1`
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

- **UUID**: `3fb2889a-1e7d-4fba-af5b-baa9a34b0ccf`
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

- **UUID**: `abd70e5c-070a-4736-b781-9b7606ab67bc`
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

- **UUID**: `4650b3d8-56a4-4c59-9e5d-88c55cd87c71`
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

##### 5. vBRSDriverHandlingFlexray

**容器属性**:

- **UUID**: `9a69c72f-3c13-44b2-84c3-e642ecef1133`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `7b3a0f78-776e-4161-bc9b-2c643578b4df`
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

- **UUID**: `aa7a9e83-b4ac-4ce8-9c26-8104e43e85cc`
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
is genrated.

######## 2. vBRSDriverHandlingFlexray_channel0A

- **UUID**: `9d140e60-c3a7-4be3-96b8-427b0f28c4bd`
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

- **UUID**: `fa9fd5a7-4ba9-4ed8-b3f8-b2188ab93db9`
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

- **UUID**: `b78c3ce9-17e9-41cd-9788-e91f67a88be9`
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

- **UUID**: `89bbf9c7-0204-446d-9d01-1080cbd7c45a`
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

- **UUID**: `36617ead-159a-4e0b-ac88-200453a85de6`
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

- **UUID**: `2b98fbfd-1e40-47d6-8ef0-db9d705599d9`
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

##### 6. vBRSDriverHandlingEthernet

**容器属性**:

- **UUID**: `129f46fb-7cbd-42c7-a71d-26c4af70c239`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `904d3034-8c0b-4ea8-9a1b-34782fb12adc`
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

- **UUID**: `bf2cdb1c-0230-422b-8725-313b0112522e`
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
is genrated.

######## 2. vBRSDriverHandlingEthernet_PeripheralClock

- **UUID**: `0e9e5206-6ea9-4102-a535-b513da765524`
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

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingEthernet_ClockRef

- **UUID**: `d3d04cdf-337e-4541-ac17-077b5554d50e`
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

##### 7. vBRSEvalBoardInfo

**容器属性**:

- **UUID**: `aaf1b66c-be23-42a0-ba74-67339fe1947c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBRSEvalBoardOscClock

- **UUID**: `067b0a10-9c71-4285-8c10-7e8dd71d0855`
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

- **UUID**: `19b52e1c-c70a-44f6-8cbe-1998f6dc3b1f`
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

- **UUID**: `e2189ef8-2b2c-4102-a78b-4291f53c4bb3`
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

##### 8. vBRSTestsuiteSupport

**容器属性**:

- **UUID**: `d4cf47a7-601c-43f3-9096-a9951bf4e007`
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

- **UUID**: `6775c756-daac-4d4f-89a8-601019dd1747`
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
Via the define BRS_ENABLE_TESTSUITE_SUPPORT, the Generic TestSuite concept headerfile BrsTestsuite.h will be included and the Generic Testsuite init function BrsTestsuiteInit()  will be called within BrsMain.c

####### ENUMERATION 类型参数

######## 1. vBRSTccSupport

- **UUID**: `4680cc87-4a96-4148-9861-18a805729bb3`
- **参数名**: `vBRSTccSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `None` (来源: Vector Informatik)
  - `TCCviaComIf` (来源: Vector Informatik)
  - `TCCviaTCM` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: vBRS Tcc Support

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. vBRSTcc

**容器属性**:

- **UUID**: `5746989b-50fb-465b-82ad-7a3b93b508b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `7c512a93-f20c-4929-afd3-3554e4c9b41c`
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

- **UUID**: `448ec58a-67b0-48b2-9a0d-f2984747fcd6`
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

- **UUID**: `a2e652a4-f08f-4d30-93ef-bdb7f0abb462`
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

- **UUID**: `57ae5c92-64c6-431f-ac96-d2c09b3127a9`
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

- **UUID**: `6d57d352-3f18-47b6-b3fe-1ae4a9a898c0`
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

- **UUID**: `fdf4a161-acf2-4a86-9e9c-21111fb278dc`
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

- **UUID**: `7c512a93-f20c-4929-afd3-3554e4c9b41c`
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

- **UUID**: `448ec58a-67b0-48b2-9a0d-f2984747fcd6`
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

- **UUID**: `a2e652a4-f08f-4d30-93ef-bdb7f0abb462`
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

- **UUID**: `57ae5c92-64c6-431f-ac96-d2c09b3127a9`
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

- **UUID**: `6d57d352-3f18-47b6-b3fe-1ae4a9a898c0`
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

- **UUID**: `fdf4a161-acf2-4a86-9e9c-21111fb278dc`
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

##### 9. vBRSTcc

**容器属性**:

- **UUID**: `5746989b-50fb-465b-82ad-7a3b93b508b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `7c512a93-f20c-4929-afd3-3554e4c9b41c`
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

- **UUID**: `448ec58a-67b0-48b2-9a0d-f2984747fcd6`
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

- **UUID**: `a2e652a4-f08f-4d30-93ef-bdb7f0abb462`
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

- **UUID**: `57ae5c92-64c6-431f-ac96-d2c09b3127a9`
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

- **UUID**: `6d57d352-3f18-47b6-b3fe-1ae4a9a898c0`
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

- **UUID**: `fdf4a161-acf2-4a86-9e9c-21111fb278dc`
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

##### 10. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `7c512a93-f20c-4929-afd3-3554e4c9b41c`
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

- **UUID**: `448ec58a-67b0-48b2-9a0d-f2984747fcd6`
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

- **UUID**: `a2e652a4-f08f-4d30-93ef-bdb7f0abb462`
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

##### 11. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `57ae5c92-64c6-431f-ac96-d2c09b3127a9`
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

- **UUID**: `6d57d352-3f18-47b6-b3fe-1ae4a9a898c0`
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

- **UUID**: `fdf4a161-acf2-4a86-9e9c-21111fb278dc`
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

##### 12. vBRSMemoryInit

**容器属性**:

- **UUID**: `3def5a32-9ec7-4be0-925c-a345cb687c53`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSMemoryInit`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBRSInitPatternBlocks

- **UUID**: `a67bd17f-9988-40cb-8f2c-b0c09cfa7526`
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
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
This value is for the blocks, configured with "Zero Init Policy" = ALWAYS within the vLinkGen configuration.
The pattern has to be 32-bit aligned.
Default value is 0x0.

######## 2. vBRSInitPatternHardResetBlocks

- **UUID**: `f96c22ed-8e23-44f8-a3db-ebc065504de1`
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
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
This value is for the blocks, configured with "Zero Init Policy" = HARD_RESET within the vLinkGen configuration.
The pattern has to be 32-bit aligned.
Default value is 0x0.

######## 3. vBRSInitPatternAreas

- **UUID**: `c736c634-41a5-4a71-8a3b-b1202c471231`
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
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
This value is for the areas, configured with "Zero Init Policy" = ALWAYS within the vLinkGen configuration.
The pattern has to be 32-bit aligned.
Default value is 0x0.

######## 4. vBRSInitPatternHardResetAreas

- **UUID**: `849945da-c15b-4518-a0f8-9b657f23813b`
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
- **描述**: Configure the init pattern for the Brs_MemoryZeroInit() call within Brs_PreMainStartup().
This value is for the areas, configured with "Zero Init Policy" = HARD_RESET within the vLinkGen configuration.
The pattern has to be 32-bit aligned.
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

- **UUID**: `29b74dcc-81cb-42ee-8659-7233b41a802a`
- **实现名称**: `vBRS_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vBRS_Pre

- **UUID**: `6c41a082-900a-4c56-9770-5ecf1d87cfe7`
- **配置名称**: `vBRS_Pre`
- **定义引用**: `/MICROSAR/vBRS`

### 2. vBRS_Rec

- **UUID**: `20bd2d98-c314-4887-bff4-25acc67bca4d`
- **配置名称**: `vBRS_Rec`
- **定义引用**: `/MICROSAR/vBRS`
