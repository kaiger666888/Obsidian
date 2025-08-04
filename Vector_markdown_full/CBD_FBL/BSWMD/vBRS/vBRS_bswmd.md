# vBRS - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:29

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

- **UUID**: `4567c974-b4cd-4d72-88ec-0966c533cbd5`
- **模块名称**: `vBRS`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Basic Runtime System.

#### 版本历史

共有 **11** 个版本记录：

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

- **发布日期**: 2021-01-25
- **发布者**: visjhr

**变更内容**:

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. vBRSGeneral

**容器属性**:

- **UUID**: `fbe5c474-0976-419d-900b-50911102684b`
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

- **UUID**: `31a8fe3e-f382-45f4-ab5e-698cb6b1cae2`
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

- **UUID**: `b9ad9768-cb8c-4178-8fc5-1b0a84d8c217`
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

- **UUID**: `67d04e7d-2ac4-410b-a5bc-b3c7d954c42b`
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

- **UUID**: `c0480a39-df21-4f0b-889c-f9684289535a`
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

- **UUID**: `30423176-e2ef-4082-b407-7f205f7990b2`
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

- **UUID**: `46bea823-6f9e-4553-b68f-407c66bc4616`
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

- **UUID**: `cbe446bd-242a-4678-9ac5-36fbdfd2cb6a`
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

- **UUID**: `5c569b9c-2a0c-4770-bc58-57265d82b10c`
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

- **UUID**: `4ffb4197-57f2-4ed2-8ce8-b8e3db020968`
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

- **UUID**: `ee0788f3-f54d-489b-91fe-68066761e420`
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

- **UUID**: `15661404-2c78-4296-b0d4-cbf539f7cda5`
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

- **UUID**: `c49bd151-5df1-4cf3-a77b-6c0380569a14`
- **参数名**: `vBRSFblSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `Disabled`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `Disabled` (来源: Vector Informatik)
  - `FBL_without_EcuMInit` (来源: Vector Informatik)
  - `FBL_with_EcuMInit` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configure the support for FlashBootLoader projects.
Sets the following generated parameters:
BRS_ENABLE_FBL in vBrsCfg.h, additional to one of the following:
BRS_FBL_NO_ECUMINIT, BRS_FBL_WITH_ECUMINIT

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSToggleLEDDioChannel

- **UUID**: `727acc16-341d-4cb5-bada-2ec8822dc659`
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

- **UUID**: `61277d0e-a92c-4acb-9b7b-f9c0d88fb015`
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

- **UUID**: `e404e4af-6892-4bb9-a4ff-7c52f8b0e1b1`
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

- **UUID**: `341c5e33-33ea-4271-b17d-908e5415bbce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSHwConfig`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. vBRSOscClock

- **UUID**: `83a56bc0-963a-448f-bb1c-5d34b5f0bdf3`
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

- **UUID**: `b622045c-db08-4735-8662-9c96c5a1bc77`
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

- **UUID**: `d87eaba7-d28e-4966-9688-b098405a54a1`
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

- **UUID**: `ba602f7d-b00b-4878-8b3c-e65491fa9c6d`
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

- **UUID**: `fee9892e-3919-4fbf-b3e0-c8a0d6595062`
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

- **UUID**: `8efcc163-90f7-4247-9a71-d4debc149999`
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

- **UUID**: `84ce1599-7271-4d3c-bd90-a04d2473dc9d`
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

- **UUID**: `5fcd375f-824a-4c83-ae32-0bc4199923c4`
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
This will cause the depending init calls, previous to init stage One, inside the callout BrsMain_MemoryInit_StageOne_Hook() of BrsMain_Callout_Stubs.c.

Sets the following generated parameter:
BRS_ENABLE_PREFER_PLL_WATCHDOG_INIT in vBrsCfg.h

####### STRING 类型参数

######## 1. vBRSPeriphClockDescription

- **UUID**: `605cfe0b-c35a-40b0-9225-6310313a6c1d`
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

- **UUID**: `ae2fc98e-31e2-48b0-9a32-b36771233ae7`
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
vBrsCfg.h: BRS_INSTRUCTION_SET_xxx

####### MULTILINE-STRING 类型参数

######## 1. vBRSMakefileUserCode

- **UUID**: `28733a24-a510-4254-bde9-d39243bb1ce5`
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

- **UUID**: `18eb7706-7b49-4a19-a226-cc54081e8017`
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

- **UUID**: `932d1ea4-54fe-4eef-a5a5-bb9078abe167`
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

本模块包含 **7** 个配置容器：

####### 1. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `9c526675-8c09-4e83-8041-aeeedf359ac8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **23** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `d0ff26e5-90bc-487d-8fa3-958ca7313aba`
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

- **UUID**: `1b5887a7-ca9d-42cf-a073-0e25f5d01f09`
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

- **UUID**: `64d07f7a-e117-49ef-99d0-cc5e6a8a36c4`
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

- **UUID**: `cf4e1d09-bb6a-43b5-ae83-507bce97357d`
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

- **UUID**: `065ba7ab-199f-4c37-aeac-cf26fd1ea3c9`
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

- **UUID**: `0abddcce-26ad-446c-9d4b-435ce069cc37`
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

- **UUID**: `09b68aaf-c509-4150-af60-f619b051feb0`
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

- **UUID**: `b32813cf-cac5-4fb0-b603-e12d6ca91a90`
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

- **UUID**: `1c9e0f22-60c7-453d-8c7d-018bccc08b4c`
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

- **UUID**: `c25b11b8-6611-4c86-99de-699ff7cfa4e8`
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

- **UUID**: `74b66617-479e-4798-a6d7-e2f60d48a6e7`
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

- **UUID**: `6dd5faba-edfa-4e69-8f6b-11207eb5fe2c`
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

- **UUID**: `7aa73d25-eb5d-45ee-a4b5-75fb9ee1c19a`
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

- **UUID**: `13686d7e-1c71-4326-a5ae-a3199c99dd20`
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

- **UUID**: `efaed9db-43c7-4627-9d46-71fdf694c91a`
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

- **UUID**: `28d75af5-5fdf-4f30-b17d-520827ae1827`
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

- **UUID**: `451a3101-6d00-489c-9844-2a0e9eca39a1`
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

- **UUID**: `56572362-4021-4d53-80de-9ebb32b3406b`
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

- **UUID**: `5a6a94b8-ee43-4401-a20c-ef4fddbb65e8`
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

- **UUID**: `260e9325-d76f-494b-84a6-bcc1c701924e`
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

- **UUID**: `344f3dcc-a474-4fe6-8a0b-a1792b0b4885`
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

- **UUID**: `a5bdebea-bc09-423d-85db-05137543278c`
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

- **UUID**: `8d4736f4-f9e5-4793-9786-e12aef0eed7c`
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

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `fd3775c1-0cc7-43a5-83b3-cf0fc95b84f0`
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

- **UUID**: `1797024b-760a-4e11-8803-fe979cce0c3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **26** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `37063324-cb29-46c7-ab9f-d6ed0b4107bd`
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

- **UUID**: `25695e7f-4ca8-4bf9-9c80-55e5988c4063`
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

- **UUID**: `1d735ab6-e222-4913-a37f-7da30ca7a1d8`
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

- **UUID**: `6ed3f346-d366-4ff2-b47e-b0ad55a1387c`
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

- **UUID**: `661fda2a-bac9-4249-8218-ecb4a20e7010`
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

- **UUID**: `5b164196-7df8-4856-bff9-74499181f4e2`
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

- **UUID**: `2e2169af-0901-4a35-9f01-7ec095164590`
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

- **UUID**: `1a1da468-ce76-4f2f-94af-456f7829672f`
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

- **UUID**: `3b8f330c-f45a-4572-b792-544548c65b70`
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

- **UUID**: `da7d560b-538f-4fed-9dbd-d11fa566036a`
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

- **UUID**: `bf8bbcdd-0c33-45ed-a448-c828233d2480`
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

- **UUID**: `0277c059-67c5-484f-b07b-ed59bfcf27cb`
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

- **UUID**: `fb14ebec-3376-4d06-be10-b3435a79f749`
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

- **UUID**: `e9060c3b-487d-4fd3-b8ca-1d6ea2adc119`
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

- **UUID**: `c3033552-ee6a-4b81-80f0-05ebd41a26ad`
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

- **UUID**: `7b441ce7-fa00-4cef-83de-a3a5cbc3b950`
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

- **UUID**: `176240a3-05c7-4da2-8163-1fd0d9dd09f7`
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

- **UUID**: `6605731a-e6b5-4115-bb72-d61a09b56ae2`
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

- **UUID**: `b9d143e6-aef6-4183-9223-95b96ccd6091`
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

- **UUID**: `c0605c6e-d72b-40be-9eef-7fc0678b4d3f`
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

- **UUID**: `010f272a-a2b9-4aec-9717-18f1b6d907a7`
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

- **UUID**: `c80e17bd-fb30-4fa5-b1fb-b55dd7e72a4c`
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

- **UUID**: `1708e884-58a2-4ced-9bdc-ea9dd5bee4a4`
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

- **UUID**: `ff24f23c-bb50-40b6-a8c2-d287f8351702`
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

- **UUID**: `c9472bd5-fe05-4e70-9f34-3a731d9a2657`
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

- **UUID**: `5721899e-6781-4026-a850-b6c02fed74da`
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

- **UUID**: `8f133872-6b03-42fb-bae5-5bf3c6da1905`
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

- **UUID**: `50b003d1-5df3-403f-bd81-ea46ba56e80c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `49fdf240-17df-425b-a899-b9528c0efb48`
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

- **UUID**: `98c24ab8-0216-4a25-a6ea-d9f6986148a6`
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

- **UUID**: `815c333e-2189-418d-814f-538451d17e8c`
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

- **UUID**: `7b0fe418-9f3c-4224-9b0e-ebfd847dc35f`
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

- **UUID**: `2eda5910-d4e6-4ba9-982a-88920e7b4696`
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

- **UUID**: `c639f8bc-f042-474e-b94b-a7c045320fda`
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

- **UUID**: `caf84f1d-1cb8-409f-9c71-9955bee53a32`
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

- **UUID**: `8bf298f7-c5b0-469e-85d5-fe0e67d1c04e`
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

- **UUID**: `0aea12e3-328f-4e24-90da-a78e15416c3e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `7de941af-be3c-4b5e-b5ea-42806814b8fd`
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

- **UUID**: `e1a15c5b-a00c-43f6-b1ff-538ad6933954`
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

- **UUID**: `f831caa1-71b3-47d4-b801-287af6ea0807`
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

- **UUID**: `ca3414f0-4b8c-4947-8f18-864a09605b8b`
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

- **UUID**: `0d160158-0782-4fd0-b8a8-d2e3069f2402`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. vBRSEvalBoardOscClock

- **UUID**: `b59b39ad-27a9-4bdf-8b84-5f1eeeb99f2e`
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

- **UUID**: `608dba05-6ac0-4bfb-88da-a41f9d8401a6`
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

- **UUID**: `8ac5418a-56c4-40ab-af1c-5d61a237f565`
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

- **UUID**: `31620a0d-dacd-4448-b015-44595f941617`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingHyperbus_Clock

- **UUID**: `5a0c4240-647a-4be3-984d-426fcac96b88`
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

- **UUID**: `946adc8f-7fac-4165-b10b-7607ed90c05e`
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
is genrated.

########## 2. vBRSDriverHandlingHyperbus_channel0

- **UUID**: `d916ed03-1708-4d29-a9bf-0b12aeb4d23c`
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

- **UUID**: `ca24f379-8836-4047-8f09-9822fcbcf26d`
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

- **UUID**: `575646a4-d16d-4d3e-a6fa-53d740c73e53`
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

- **UUID**: `e136af63-45f2-42dc-ac27-7ffafa02f401`
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

- **UUID**: `3da7cb1c-7cf3-442b-9df9-96236e0a8099`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingI2C`
- **多重性**: [0..1]
- **构建后可变**: false

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. vBRSDriverHandlingI2C_Clock

- **UUID**: `87c66926-0ee2-4c6b-a23d-38b489d5204f`
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

- **UUID**: `376380bb-ce88-4cff-b7cb-1b65680b5c58`
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
is genrated.

########## 2. vBRSDriverHandlingI2C_channel0

- **UUID**: `a1f806d1-4ce4-416f-8c4a-fa1868e756bb`
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

- **UUID**: `5936ba74-41e0-4de0-832a-4a24ea831416`
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

- **UUID**: `0e12e9d2-3616-4530-af2f-b0de815052a5`
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

- **UUID**: `9cf0decc-4eba-4d4f-9763-a66a28b86f7c`
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

##### 3. vBRSDriverHandlingCAN

**容器属性**:

- **UUID**: `9c526675-8c09-4e83-8041-aeeedf359ac8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingCAN`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **23** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingCAN_Clock

- **UUID**: `d0ff26e5-90bc-487d-8fa3-958ca7313aba`
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

- **UUID**: `1b5887a7-ca9d-42cf-a073-0e25f5d01f09`
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

- **UUID**: `64d07f7a-e117-49ef-99d0-cc5e6a8a36c4`
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

- **UUID**: `cf4e1d09-bb6a-43b5-ae83-507bce97357d`
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

- **UUID**: `065ba7ab-199f-4c37-aeac-cf26fd1ea3c9`
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

- **UUID**: `0abddcce-26ad-446c-9d4b-435ce069cc37`
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

- **UUID**: `09b68aaf-c509-4150-af60-f619b051feb0`
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

- **UUID**: `b32813cf-cac5-4fb0-b603-e12d6ca91a90`
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

- **UUID**: `1c9e0f22-60c7-453d-8c7d-018bccc08b4c`
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

- **UUID**: `c25b11b8-6611-4c86-99de-699ff7cfa4e8`
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

- **UUID**: `74b66617-479e-4798-a6d7-e2f60d48a6e7`
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

- **UUID**: `6dd5faba-edfa-4e69-8f6b-11207eb5fe2c`
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

- **UUID**: `7aa73d25-eb5d-45ee-a4b5-75fb9ee1c19a`
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

- **UUID**: `13686d7e-1c71-4326-a5ae-a3199c99dd20`
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

- **UUID**: `efaed9db-43c7-4627-9d46-71fdf694c91a`
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

- **UUID**: `28d75af5-5fdf-4f30-b17d-520827ae1827`
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

- **UUID**: `451a3101-6d00-489c-9844-2a0e9eca39a1`
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

- **UUID**: `56572362-4021-4d53-80de-9ebb32b3406b`
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

- **UUID**: `5a6a94b8-ee43-4401-a20c-ef4fddbb65e8`
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

- **UUID**: `260e9325-d76f-494b-84a6-bcc1c701924e`
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

- **UUID**: `344f3dcc-a474-4fe6-8a0b-a1792b0b4885`
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

- **UUID**: `a5bdebea-bc09-423d-85db-05137543278c`
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

- **UUID**: `8d4736f4-f9e5-4793-9786-e12aef0eed7c`
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

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. vBRSDriverHandlingCAN_ClockRef

- **UUID**: `fd3775c1-0cc7-43a5-83b3-cf0fc95b84f0`
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

- **UUID**: `1797024b-760a-4e11-8803-fe979cce0c3f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingLIN`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **26** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingLIN_Clock

- **UUID**: `37063324-cb29-46c7-ab9f-d6ed0b4107bd`
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

- **UUID**: `25695e7f-4ca8-4bf9-9c80-55e5988c4063`
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

- **UUID**: `1d735ab6-e222-4913-a37f-7da30ca7a1d8`
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

- **UUID**: `6ed3f346-d366-4ff2-b47e-b0ad55a1387c`
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

- **UUID**: `661fda2a-bac9-4249-8218-ecb4a20e7010`
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

- **UUID**: `5b164196-7df8-4856-bff9-74499181f4e2`
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

- **UUID**: `2e2169af-0901-4a35-9f01-7ec095164590`
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

- **UUID**: `1a1da468-ce76-4f2f-94af-456f7829672f`
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

- **UUID**: `3b8f330c-f45a-4572-b792-544548c65b70`
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

- **UUID**: `da7d560b-538f-4fed-9dbd-d11fa566036a`
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

- **UUID**: `bf8bbcdd-0c33-45ed-a448-c828233d2480`
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

- **UUID**: `0277c059-67c5-484f-b07b-ed59bfcf27cb`
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

- **UUID**: `fb14ebec-3376-4d06-be10-b3435a79f749`
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

- **UUID**: `e9060c3b-487d-4fd3-b8ca-1d6ea2adc119`
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

- **UUID**: `c3033552-ee6a-4b81-80f0-05ebd41a26ad`
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

- **UUID**: `7b441ce7-fa00-4cef-83de-a3a5cbc3b950`
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

- **UUID**: `176240a3-05c7-4da2-8163-1fd0d9dd09f7`
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

- **UUID**: `6605731a-e6b5-4115-bb72-d61a09b56ae2`
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

- **UUID**: `b9d143e6-aef6-4183-9223-95b96ccd6091`
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

- **UUID**: `c0605c6e-d72b-40be-9eef-7fc0678b4d3f`
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

- **UUID**: `010f272a-a2b9-4aec-9717-18f1b6d907a7`
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

- **UUID**: `c80e17bd-fb30-4fa5-b1fb-b55dd7e72a4c`
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

- **UUID**: `1708e884-58a2-4ced-9bdc-ea9dd5bee4a4`
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

- **UUID**: `ff24f23c-bb50-40b6-a8c2-d287f8351702`
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

- **UUID**: `c9472bd5-fe05-4e70-9f34-3a731d9a2657`
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

- **UUID**: `5721899e-6781-4026-a850-b6c02fed74da`
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

- **UUID**: `8f133872-6b03-42fb-bae5-5bf3c6da1905`
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

- **UUID**: `50b003d1-5df3-403f-bd81-ea46ba56e80c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingFlexray`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingFlexray_Clock

- **UUID**: `49fdf240-17df-425b-a899-b9528c0efb48`
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

- **UUID**: `98c24ab8-0216-4a25-a6ea-d9f6986148a6`
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

- **UUID**: `815c333e-2189-418d-814f-538451d17e8c`
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

- **UUID**: `7b0fe418-9f3c-4224-9b0e-ebfd847dc35f`
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

- **UUID**: `2eda5910-d4e6-4ba9-982a-88920e7b4696`
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

- **UUID**: `c639f8bc-f042-474e-b94b-a7c045320fda`
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

- **UUID**: `caf84f1d-1cb8-409f-9c71-9955bee53a32`
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

- **UUID**: `8bf298f7-c5b0-469e-85d5-fe0e67d1c04e`
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

- **UUID**: `0aea12e3-328f-4e24-90da-a78e15416c3e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingEthernet`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingEthernet_Clock

- **UUID**: `7de941af-be3c-4b5e-b5ea-42806814b8fd`
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

- **UUID**: `e1a15c5b-a00c-43f6-b1ff-538ad6933954`
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

- **UUID**: `f831caa1-71b3-47d4-b801-287af6ea0807`
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

- **UUID**: `ca3414f0-4b8c-4947-8f18-864a09605b8b`
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

- **UUID**: `0d160158-0782-4fd0-b8a8-d2e3069f2402`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSEvalBoardInfo`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. vBRSEvalBoardOscClock

- **UUID**: `b59b39ad-27a9-4bdf-8b84-5f1eeeb99f2e`
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

- **UUID**: `608dba05-6ac0-4bfb-88da-a41f9d8401a6`
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

- **UUID**: `8ac5418a-56c4-40ab-af1c-5d61a237f565`
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

##### 8. vBRSDriverHandlingHyperbus

**容器属性**:

- **UUID**: `31620a0d-dacd-4448-b015-44595f941617`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingHyperbus`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingHyperbus_Clock

- **UUID**: `5a0c4240-647a-4be3-984d-426fcac96b88`
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

- **UUID**: `946adc8f-7fac-4165-b10b-7607ed90c05e`
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
is genrated.

######## 2. vBRSDriverHandlingHyperbus_channel0

- **UUID**: `d916ed03-1708-4d29-a9bf-0b12aeb4d23c`
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

- **UUID**: `ca24f379-8836-4047-8f09-9822fcbcf26d`
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

- **UUID**: `575646a4-d16d-4d3e-a6fa-53d740c73e53`
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

- **UUID**: `e136af63-45f2-42dc-ac27-7ffafa02f401`
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

##### 9. vBRSDriverHandlingI2C

**容器属性**:

- **UUID**: `3da7cb1c-7cf3-442b-9df9-96236e0a8099`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSDriverHandlingI2C`
- **多重性**: [0..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. vBRSDriverHandlingI2C_Clock

- **UUID**: `87c66926-0ee2-4c6b-a23d-38b489d5204f`
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

- **UUID**: `376380bb-ce88-4cff-b7cb-1b65680b5c58`
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
is genrated.

######## 2. vBRSDriverHandlingI2C_channel0

- **UUID**: `a1f806d1-4ce4-416f-8c4a-fa1868e756bb`
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

- **UUID**: `5936ba74-41e0-4de0-832a-4a24ea831416`
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

- **UUID**: `0e12e9d2-3616-4530-af2f-b0de815052a5`
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

- **UUID**: `9cf0decc-4eba-4d4f-9763-a66a28b86f7c`
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

##### 10. vBRSTestsuiteSupport

**容器属性**:

- **UUID**: `93183885-6b49-495e-ad50-76f67b8fa43f`
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

- **UUID**: `8573c31a-13d2-4c0c-baac-367016947358`
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

- **UUID**: `bbee5374-8d27-4f1d-8b3d-1861b9d2371e`
- **参数名**: `vBRSTccSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `None`
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

- **UUID**: `c32fef59-bc9e-43d5-9ad1-c39c99590e2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `e6da48c5-4e8c-4032-ae05-5a37a76b764a`
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

- **UUID**: `2bc72872-70f8-4eaf-91f6-32204129958b`
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

- **UUID**: `d9575d08-fcc2-4b47-a090-f109ee829fcb`
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

- **UUID**: `aca4eaa2-1d97-419a-be1d-927e431cea33`
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

- **UUID**: `ef8a2bb6-d2c1-4a70-8b01-409ab6f113b1`
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

- **UUID**: `1ceba0ba-1b14-45ae-a19c-adafc5f719f8`
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

- **UUID**: `e6da48c5-4e8c-4032-ae05-5a37a76b764a`
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

- **UUID**: `2bc72872-70f8-4eaf-91f6-32204129958b`
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

- **UUID**: `d9575d08-fcc2-4b47-a090-f109ee829fcb`
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

- **UUID**: `aca4eaa2-1d97-419a-be1d-927e431cea33`
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

- **UUID**: `ef8a2bb6-d2c1-4a70-8b01-409ab6f113b1`
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

- **UUID**: `1ceba0ba-1b14-45ae-a19c-adafc5f719f8`
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

##### 11. vBRSTcc

**容器属性**:

- **UUID**: `c32fef59-bc9e-43d5-9ad1-c39c99590e2c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSTcc`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `e6da48c5-4e8c-4032-ae05-5a37a76b764a`
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

- **UUID**: `2bc72872-70f8-4eaf-91f6-32204129958b`
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

- **UUID**: `d9575d08-fcc2-4b47-a090-f109ee829fcb`
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

- **UUID**: `aca4eaa2-1d97-419a-be1d-927e431cea33`
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

- **UUID**: `ef8a2bb6-d2c1-4a70-8b01-409ab6f113b1`
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

- **UUID**: `1ceba0ba-1b14-45ae-a19c-adafc5f719f8`
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

##### 12. vBRSComIfUpperLayerRxPdu

**容器属性**:

- **UUID**: `e6da48c5-4e8c-4032-ae05-5a37a76b764a`
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

- **UUID**: `2bc72872-70f8-4eaf-91f6-32204129958b`
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

- **UUID**: `d9575d08-fcc2-4b47-a090-f109ee829fcb`
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

##### 13. vBRSComIfUpperLayerTxPdu

**容器属性**:

- **UUID**: `aca4eaa2-1d97-419a-be1d-927e431cea33`
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

- **UUID**: `ef8a2bb6-d2c1-4a70-8b01-409ab6f113b1`
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

- **UUID**: `1ceba0ba-1b14-45ae-a19c-adafc5f719f8`
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

##### 14. vBRSMemoryInit

**容器属性**:

- **UUID**: `71a9f23c-f234-4b17-9a83-b2afa76a8a18`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `vBRSMemoryInit`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. vBRSInitPatternBlocks

- **UUID**: `21a5ddf2-121d-466e-bf54-9b3233db09e3`
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

- **UUID**: `57e3e46f-8b19-4d7f-9e87-e89bc98b2496`
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

- **UUID**: `f1f60720-1249-435f-963a-2fce2209b9dd`
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

- **UUID**: `418ae636-75bb-4646-a896-36404f6003b9`
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

- **UUID**: `7d1300b5-94dc-4571-bf52-c923c336419a`
- **实现名称**: `vBRS_Impl`
- **编程语言**: C
- **软件版本**: 1.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. vBRS_Pre

- **UUID**: `430937c6-724e-4c68-a37b-63e448c85d5e`
- **配置名称**: `vBRS_Pre`
- **定义引用**: `/MICROSAR/vBRS`

### 2. vBRS_Rec

- **UUID**: `2b542dc7-8f65-494e-95bd-b180f7624c7d`
- **配置名称**: `vBRS_Rec`
- **定义引用**: `/MICROSAR/vBRS`
