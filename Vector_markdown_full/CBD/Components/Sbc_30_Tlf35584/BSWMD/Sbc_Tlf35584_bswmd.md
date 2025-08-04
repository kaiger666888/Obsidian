# Sbc - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:55

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Sbc](#sbc)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Sbc

#### 基本信息

- **UUID**: `87d050f3-d7d2-435c-b517-ec9a238b4542`
- **模块名称**: `Sbc`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Driver for System Basis Chip devices. Incorporates, manages / abstracts HW in regard to the AUTOSAR defined functionalities of respective CAN- / LIN-transceivers as well as Watchdog functionality which are part of single chip ICs. Vectors SBC driver requires MCAL SPI driver for communication purposes towards the external device.
#CAN #LIN #TRANSCEIVER #WDG #SPI #PowerManagement #PMIC
#AUTOSAR #Vector

#### 版本历史

共有 **17** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2017-10-04T10:44:14+02:00
- **发布者**: virmid

**变更内容**:

##### 2. 版本 1.00.01

- **状态**: released
- **发布日期**: 2018-04-23T19:29:14+02:00
- **发布者**: virmid

**变更内容**:

##### 3. 版本 1.01.00

- **状态**: released
- **发布日期**: 2019-06-03T12:35:03+02:00
- **发布者**: virmid

**变更内容**:

##### 4. 版本 1.02.00

- **状态**: released
- **发布日期**: 2020-06-26T09:26:37+02:00
- **发布者**: virmcn

**变更内容**:

##### 5. 版本 1.02.01

- **状态**: released
- **发布日期**: 2020-10-30T11:11:20+01:00
- **发布者**: virmcn

**变更内容**:

##### 6. 版本 1.03.00

- **状态**: released
- **发布日期**: 2020-11-06T10:46:42+01:00
- **发布者**: coberpriller

**变更内容**:

##### 7. 版本 1.03.01

- **状态**: released
- **发布日期**: 2021-03-03T11:15:24+01:00
- **发布者**: virmcn

**变更内容**:

##### 8. 版本 1.03.02

- **状态**: released
- **发布日期**: 2022-05-30T13:25:06+02:00
- **发布者**: virmcn

**变更内容**:

##### 9. 版本 1.04.00

- **状态**: released
- **发布日期**: 2022-11-21T08:38:02+01:00
- **发布者**: coberpriller

**变更内容**:

##### 10. 版本 1.04.00

- **状态**: released
- **发布日期**: 2022-11-21T08:41:26+01:00
- **发布者**: coberpriller

**变更内容**:

##### 11. 版本 1.04.00

- **状态**: released
- **发布日期**: 2022-11-21T08:41:57+01:00
- **发布者**: coberpriller

**变更内容**:

##### 12. 版本 1.05.00

- **状态**: released
- **发布日期**: 2023-02-28T16:17:33+01:00
- **发布者**: coberpriller

**变更内容**:

##### 13. 版本 1.05.01

- **状态**: released
- **发布日期**: 2023-04-26T14:31:38+02:00
- **发布者**: virmcn

**变更内容**:

##### 14. 版本 1.05.01

- **状态**: released
- **发布日期**: 2023-05-10T10:34:44+02:00
- **发布者**: virmcn

**变更内容**:

##### 15. 版本 1.05.02

- **状态**: released
- **发布日期**: 2023-11-14T16:10:44+01:00
- **发布者**: rwerhahn

**变更内容**:

##### 16. 版本 1.05.03

- **状态**: released
- **发布日期**: 2023-12-04T10:32:21+01:00
- **发布者**: rwerhahn

**变更内容**:

##### 17. 版本 1.06.00

- **状态**: released
- **发布日期**: 2024-02-02T09:30:13+01:00
- **发布者**: makstaller

**变更内容**:

#### 配置容器

本模块包含 **24** 个配置容器：

##### 1. SbcPublicCfg

**容器属性**:

- **UUID**: `a79a7d09-066d-455e-8151-8a398b6fc31a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcPublicCfg`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes general configuration options for the Sbc module.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. SbcSingleInstanceApi

- **UUID**: `b14f65d2-471d-4a79-83bc-2ae7cfd2cdb9`
- **参数名**: `SbcSingleInstanceApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables the SingleInstanceApi feature.

True: The SingleInstanceApi feature is enabled. The module defines its APIs without infix.
False: The SingleInstanceApi feature is disabled. The module defines its APIs with infix.

Note: Normally, all API names are infixed by a combination of VendorId and VendorApiInfix in order to allow the usage of multiple different Sbc drivers within one stack.
When this feature is enabled the module defines the APIs without an infix. This can be set only if there is not more than one Sbc driver active in this configuration.

######## 2. SbcDevErrorDetect

- **UUID**: `c44f7763-24a7-464f-8f01-67046eabbf38`
- **参数名**: `SbcDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.

True: Development error detection is enabled.
False: Development error detection is disabled.

######## 3. SbcGetVersionInfo

- **UUID**: `6fc3a255-9ae4-4d8d-a3e9-cd5b0ef53e61`
- **参数名**: `SbcGetVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter enables/disables the function Sbc_30_Tlf35584_GetVersionInfo() to get major, minor and patch version information.

True: GetVersionInfo-API is available.
False:  GetVersionInfo-API is not available.

######## 4. SbcSafeBswChecks

- **UUID**: `29f28a04-f940-4a5b-a256-5224738f200f`
- **参数名**: `SbcSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used.

These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 5. SbcParityBitCalculation

- **UUID**: `fa80f6db-33aa-4dca-8919-ebb0f52da3e3`
- **参数名**: `SbcParityBitCalculation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if parity bit calculation is enabled or disabled.

FALSE: Parity bit calculation is disabled.
TRUE:  Parity bit calculation in enabled.

####### STRING 类型参数

######## 1. SbcUserConfigFile

- **UUID**: `c359c37e-22ad-4f75-8432-f2260205d9a0`
- **参数名**: `SbcUserConfigFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to an external text file that will be included during generation to <Module>_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

##### 2. SbcDevice

**容器属性**:

- **UUID**: `c5ff4f9e-7ab4-4b34-92e0-a2720eeda389`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDevice`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This container includes configuration of specific Sbc devices.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. SbcDeviceId

- **UUID**: `801d2d8d-a90a-4026-bc47-a25f89e919ac`
- **参数名**: `SbcDeviceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier for the Sbc device. The value must be unique on one device instance.

######## 2. SbcCtrlLoopMaxCycles

- **UUID**: `25b28323-b288-4a15-89d2-9ae43dd21631`
- **参数名**: `SbcCtrlLoopMaxCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `15`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the number of loop cycles after hardware-dependent loop timeout occurs.

####### ENUMERATION 类型参数

######## 1. SbcDerivative

- **UUID**: `778f49e5-1bdd-4117-8a3e-6265a8f1504c`
- **参数名**: `SbcDerivative`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TLF35584`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TLF35584` (来源: Vector Informatik)
  - `TLF35585` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the used derivative.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcPorWakeupSourceRef

- **UUID**: `c0bd3814-cda7-471e-bc32-e9affa94323e`
- **引用名**: `SbcPorWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to EcuMWakeupSource which should be used to report a power-on-reset (POR).

Note: Not used since peripheral is not able to detect power-on-reset. When this reference is specified the Sbc module reports a wakeup that was caused by a power-on-reset (POR) to the EcuM by using the specified wakeup source.

###### 配置容器

本模块包含 **22** 个配置容器：

####### 1. SbcWatchdogPeripheral

**容器属性**:

- **UUID**: `27e19832-9459-40c3-9c6f-ab9fe5018828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the watchdog configuration.

######## 参数配置

此容器包含 **6** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogPeripheralId

- **UUID**: `083b6cb8-e4e0-4136-a32e-c3c25c39a3e0`
- **参数名**: `SbcWatchdogPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier for the watchdog peripheral. The value must be unique on one device instance.

########## 2. SbcWatchdogTriggerOffset

- **UUID**: `5bda48b2-0183-435b-8191-370b90e72939`
- **参数名**: `SbcWatchdogTriggerOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the offset in percent for the first trigger point to be located in the specified watchdog trigger interval.

########## 3. SbcWatchdogErrorThreshold

- **UUID**: `f8260379-3aa3-47b3-99b9-02b71665bd00`
- **参数名**: `SbcWatchdogErrorThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `9`
- **取值范围**: [0..15]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the watchdog (FWD/WWD) error threshold to generate reset and enter into INIT state.

Note: Depending on the value of parameter SbcWatchdogPeripheralType this value is written to WDCFG0.WWDETHR or FWDCFG.FWDETHR.

######### ENUMERATION 类型参数

########## 1. SbcWatchdogInitialMode

- **UUID**: `e5aeba31-bfae-48e5-93a8-c414c99168ee`
- **参数名**: `SbcWatchdogInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGIF_FAST_MODE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_OFF_MODE` (来源: Vector Informatik)
  - `WDGIF_SLOW_MODE` (来源: Vector Informatik)
  - `WDGIF_FAST_MODE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the mode of the watchdog that is selected during the initialization of the Sbc.

WDGIF_OFF_MODE: Watchdog is disabled during initialization.
WDGIF_SLOW_MODE: Watchdog is initialized with SLOW mode.
WDGIF_FAST_MODE: Watchdog is initialized with FAST mode.

########## 2. SbcWatchdogPeripheralType

- **UUID**: `1b087f65-8ff0-41f7-9f34-5d604366675b`
- **参数名**: `SbcWatchdogPeripheralType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WWD`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FWD` (来源: Vector Informatik)
  - `WWD` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the functional watchdog peripheral or the window watchdog peripheral is used.

FWD: Functional watchdog peripheral is used.
WWD: Window watchdog peripheral is used.

########## 3. SbcWatchdogPeripheralCycleTime

- **UUID**: `8af0fb11-07ee-452c-b68a-373c4b2a0dda`
- **参数名**: `SbcWatchdogPeripheralCycleTime`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDCYC_100US`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDCYC_100US` (来源: Vector Informatik)
  - `WDCYC_1MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the watchdog cycle time.

WDCYC_100US: Watchdog cycle time is set to 0.1 ms tick period.
WDCYC_1MS: Watchdog cycle time is set to 1 ms tick period.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcWatchdogPeripheralFastMode

**容器属性**:

- **UUID**: `2d60d2d6-3ede-4dd9-95f0-c82a46a32437`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralFastMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog FAST mode.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

############ 2. SbcWwdClosedWindow

- **UUID**: `4cf282e0-99d3-4cc5-bfd8-f612c9dc27b0`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

############ 3. SbcWwdOpenWindow

- **UUID**: `7be92a08-70c0-4d6d-bcc8-a2f47ea40328`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

############ 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `33ac922c-3d6e-4606-aa63-aab3f7043e5c`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

######### 2. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `ce686104-af20-40a5-b4d5-3e75c0a85495`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. SbcWatchdogTriggerPeriod

- **UUID**: `f39de258-3fe1-4980-a6db-9af66e1fcf84`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

############ 2. SbcWwdClosedWindow

- **UUID**: `30ba22bc-98fe-4f68-8b7a-1509076630f6`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

############ 3. SbcWwdOpenWindow

- **UUID**: `38609e16-7170-418b-87f6-39723c6c14b4`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

############ 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `4a014b29-676b-4059-ab94-b04b9f7acbd7`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

####### 2. SbcWatchdogPeripheralFastMode

**容器属性**:

- **UUID**: `2d60d2d6-3ede-4dd9-95f0-c82a46a32437`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralFastMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog FAST mode.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

########## 2. SbcWwdClosedWindow

- **UUID**: `4cf282e0-99d3-4cc5-bfd8-f612c9dc27b0`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 3. SbcWwdOpenWindow

- **UUID**: `7be92a08-70c0-4d6d-bcc8-a2f47ea40328`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `33ac922c-3d6e-4606-aa63-aab3f7043e5c`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

####### 3. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `ce686104-af20-40a5-b4d5-3e75c0a85495`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `f39de258-3fe1-4980-a6db-9af66e1fcf84`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

########## 2. SbcWwdClosedWindow

- **UUID**: `30ba22bc-98fe-4f68-8b7a-1509076630f6`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 3. SbcWwdOpenWindow

- **UUID**: `38609e16-7170-418b-87f6-39723c6c14b4`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `4a014b29-676b-4059-ab94-b04b9f7acbd7`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

####### 4. SbcLinTrcvPeripheral

**容器属性**:

- **UUID**: `e7a6f2c5-221e-480c-b326-c7bb6402c2e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcLinTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for LIN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a LIN transceiver.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcLinTrcvPeripheralId

- **UUID**: `48130c2b-c138-46a0-a7c9-b74a366b0d24`
- **参数名**: `SbcLinTrcvPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier for the LIN transceiver peripheral. The value must be unique on one device instance.

####### 5. SbcCanTrcvPeripheral

**容器属性**:

- **UUID**: `7af1c6aa-d50a-437d-9483-8d0d2dd50f0e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for CAN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a CAN transceiver.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvPeripheralId

- **UUID**: `ec9e2dcb-68cc-4228-a900-bdd2ffa4bb52`
- **参数名**: `SbcCanTrcvPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the identifier for the CAN transceiver peripheral. The value must be unique on one device instance.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcCanTrcvPartialNetwork

**容器属性**:

- **UUID**: `281541fc-fe4c-406c-bae9-416404d2afae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPartialNetwork`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the CAN transceiver driver information about the configuration of Partial Networking functionality. If the container is intantiated the selective wakeup functionality is activated on the CanTrcv peripheral.

########## 参数配置

此容器包含 **7** 个参数：

########### INTEGER 类型参数

############ 1. SbcCanTrcvBaudRate

- **UUID**: `f4cb591f-de56-4630-a40a-2331a240410d`
- **参数名**: `SbcCanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `500`
- **取值范围**: [0..1000]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN Bus communication baud rate in kbps.

############ 2. SbcCanTrcvPnFrameCanId

- **UUID**: `5314551f-b6aa-4aac-89c3-e34f75341cbd`
- **参数名**: `SbcCanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN ID of the Wake-up Frame (WUF).

############ 3. SbcCanTrcvPnFrameCanIdMask

- **UUID**: `337fe92b-d89a-4e8c-95df-23dccc173abe`
- **参数名**: `SbcCanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the ID Mask for the selective activation of the transceiver. It is used to configure a Wake-up frame (WUF) which consists of a group of CAN identifiers.

############ 4. SbcCanTrcvPnFrameDlc

- **UUID**: `220f7504-983c-48ef-955d-9337e3af4a53`
- **参数名**: `SbcCanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..8]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the data length of the Wake-up Frame (WUF).

########### BOOLEAN 类型参数

############ 1. SbcCanTrcvPnCanIdIsExtended

- **UUID**: `820b3bbe-8556-40bf-a809-4036c277b07f`
- **参数名**: `SbcCanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether extended or standard identifier is used for wake-up frames.

True: Extended CAN identifier is used.
False: Standard CAN identifier is used.

############ 2. SbcCanTrcvPnEnabled

- **UUID**: `305fb7f5-1348-4837-9b3b-cf5eb89a320f`
- **参数名**: `SbcCanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

############ 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `e7755d91-7d2f-4102-92a2-4d3b13d8fc27`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up configuration should be verified after it has been written to the hardware.

TRUE  = The selective wakeup configuration written to the hardware is compared to the configured values.
FALSE = The selective wakeup configuration written to the hardware is not compared to the configured values.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############## 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

######### 2. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

####### 6. SbcCanTrcvPartialNetwork

**容器属性**:

- **UUID**: `281541fc-fe4c-406c-bae9-416404d2afae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPartialNetwork`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the CAN transceiver driver information about the configuration of Partial Networking functionality. If the container is intantiated the selective wakeup functionality is activated on the CanTrcv peripheral.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvBaudRate

- **UUID**: `f4cb591f-de56-4630-a40a-2331a240410d`
- **参数名**: `SbcCanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `500`
- **取值范围**: [0..1000]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN Bus communication baud rate in kbps.

########## 2. SbcCanTrcvPnFrameCanId

- **UUID**: `5314551f-b6aa-4aac-89c3-e34f75341cbd`
- **参数名**: `SbcCanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN ID of the Wake-up Frame (WUF).

########## 3. SbcCanTrcvPnFrameCanIdMask

- **UUID**: `337fe92b-d89a-4e8c-95df-23dccc173abe`
- **参数名**: `SbcCanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the ID Mask for the selective activation of the transceiver. It is used to configure a Wake-up frame (WUF) which consists of a group of CAN identifiers.

########## 4. SbcCanTrcvPnFrameDlc

- **UUID**: `220f7504-983c-48ef-955d-9337e3af4a53`
- **参数名**: `SbcCanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..8]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the data length of the Wake-up Frame (WUF).

######### BOOLEAN 类型参数

########## 1. SbcCanTrcvPnCanIdIsExtended

- **UUID**: `820b3bbe-8556-40bf-a809-4036c277b07f`
- **参数名**: `SbcCanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether extended or standard identifier is used for wake-up frames.

True: Extended CAN identifier is used.
False: Standard CAN identifier is used.

########## 2. SbcCanTrcvPnEnabled

- **UUID**: `305fb7f5-1348-4837-9b3b-cf5eb89a320f`
- **参数名**: `SbcCanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

########## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `e7755d91-7d2f-4102-92a2-4d3b13d8fc27`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up configuration should be verified after it has been written to the hardware.

TRUE  = The selective wakeup configuration written to the hardware is compared to the configured values.
FALSE = The selective wakeup configuration written to the hardware is not compared to the configured values.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

####### 7. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

####### 8. SbcInitConfig

**容器属性**:

- **UUID**: `88ea0b2f-3b3d-4b85-8cfd-2177032c69fc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcInitConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the initialization configuration of the Sbc device.

######## 参数配置

此容器包含 **5** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcErrPinMonitor

- **UUID**: `f93b059a-5e7b-4830-9b3c-72bffc96b215`
- **参数名**: `SbcErrPinMonitor`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the ERR pin monitor functionality is enabled.

True: ERR pin monitor functionality is enabled.
Flase: ERR pin monitor functionality is disabled.

Note: If this parameter is enabled the ERR pin monitoring supervision function has to be serviced properly, otherwise resets will occur.

########## 2. SbcErrPinMonitorRecovery

- **UUID**: `5285667b-fce2-4e1c-99e8-0f44a158a7a8`
- **参数名**: `SbcErrPinMonitorRecovery`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether error pin monitor recovery enable is requested during initialization.

True: Error pin monitor recovery enable is requested.
False: Error pin monitor recovery enable is not requested.


Note: This value is used to set register field SYSPCFG1.ERRREC.

########## 3. SbcErrPinMonitorInSleep

- **UUID**: `3c740928-0fe8-48b5-833b-55a88dc24a12`
- **参数名**: `SbcErrPinMonitorInSleep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether error pin monitoring is active in SLEEP.

True: Error pin monitoring is active in SLEEP.
False: Error pin monitoring is not active in SLEEP.

Note: This value is used to write register field SYSPCFG1.ERRSLPEN.

######### ENUMERATION 类型参数

########## 1. SbcErrPinRecoveryTime

- **UUID**: `efd145a6-25c6-46eb-8fb0-3566da59cbfe`
- **参数名**: `SbcErrPinRecoveryTime`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ERREC_1_MS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ERREC_1_MS` (来源: Vector Informatik)
  - `ERREC_2_5MS` (来源: Vector Informatik)
  - `ERREC_5MS` (来源: Vector Informatik)
  - `ERREC_10MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the ERR pin monitor recovery time which is requested during initialization.

ERREC_1_MS: An ERR pin monitor recovery time of 1 ms is requested.
ERREC_2_5MS: An ERR pin monitor recovery time of 2.5 ms is requested.
ERREC_5MS: An ERR pin monitor recovery time of 5 ms is requested.
ERREC_10MS : An ERR pin monitor recovery time of 10 ms is requested.


Note: This value is used to set register field SYSPCFG1.ERR.

########## 2. SbcSafeState2Delay

- **UUID**: `5dbd3e0f-27bb-4188-bfcb-c7063ddedcae`
- **参数名**: `SbcSafeState2Delay`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SS2DEL_NODELAY`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SS2DEL_NODELAY` (来源: Vector Informatik)
  - `SS2DEL_10MS` (来源: Vector Informatik)
  - `SS2DEL_50MS` (来源: Vector Informatik)
  - `SS2DEL_100MS` (来源: Vector Informatik)
  - `SS2DEL_250MS` (来源: Vector Informatik)
  - `SS2DEL_1250MS` (来源: Vector Informatik)
  - `SS2DEL_2500MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the delay applied for transitions from NORMAL to INIT, WAKE and SLEEP state.

SS2DEL_NODELAY: Delay of 0 ms is request.
SS2DEL_10MS: Delay of 10 ms is requested.
SS2DEL_50MS: Delay of 50 ms is requested.
SS2DEL_100MS: Delay of 100 ms is requested.
SS2DEL_250MS: Delay of 250 ms is requested.
SS2DEL_1250MS: Delay of 1250 ms is requested. (This value is only available for the TLF35585)
SS2DEL_2500MS: Delay of 2500 ms is requested. (This value is only available for the TLF35585)

Note: This value is related with register field SYSPCFG1.SS2DEL.

####### 9. SbcDeviceAccess

**容器属性**:

- **UUID**: `14af1db9-3f2c-4968-aaef-7d16666f06fa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDeviceAccess`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration to access the specific Sbc hardware instance.

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. SbcDioAccess

**容器属性**:

- **UUID**: `0eed5ef3-93c6-4814-8d28-205047c68ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Dio-specific configuration to access the Sbc device.

Note: The existence of this container in combination with the usage of the SbcWatchdogPeripheralType 'WWD' means that the window watchdog is not triggered via SPI, but via the input pin WDI.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SbcWaitLoopCycles

- **UUID**: `13937262-5ac4-4503-bb69-01b69183e95c`
- **参数名**: `SbcWaitLoopCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6000`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the number of loop cycles to perform a wait until the WDI high level is sampled by the device.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

######### 2. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

######### 3. SbcSpiAccess

**容器属性**:

- **UUID**: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

########### 2. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

######### 4. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

######### 5. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

######### 6. SbcI2cAccess

**容器属性**:

- **UUID**: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the I2C-specific configuration to access the Sbc device.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

########### 2. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

######### 7. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

######### 8. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

######### 9. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `2dad0642-ed59-4cdb-a065-11881e09d6e0`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **SbcSpiSequence**
  - UUID: `3efd54fd-abb3-4e66-9976-748858916ce8`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

####### 10. SbcDioAccess

**容器属性**:

- **UUID**: `0eed5ef3-93c6-4814-8d28-205047c68ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Dio-specific configuration to access the Sbc device.

Note: The existence of this container in combination with the usage of the SbcWatchdogPeripheralType 'WWD' means that the window watchdog is not triggered via SPI, but via the input pin WDI.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWaitLoopCycles

- **UUID**: `13937262-5ac4-4503-bb69-01b69183e95c`
- **参数名**: `SbcWaitLoopCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6000`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the number of loop cycles to perform a wait until the WDI high level is sampled by the device.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

####### 11. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

####### 12. SbcSpiAccess

**容器属性**:

- **UUID**: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

######### 2. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

####### 13. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

####### 14. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

####### 15. SbcI2cAccess

**容器属性**:

- **UUID**: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the I2C-specific configuration to access the Sbc device.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

######### 2. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

####### 16. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

####### 17. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

####### 18. SbcSystemConfig

**容器属性**:

- **UUID**: `25665cc7-d217-4b36-96da-a8ccde877534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSystemConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes system specific configuration.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. SbcEnableSupplyNormal

**容器属性**:

- **UUID**: `f652d512-f444-4be9-8c89-0d8724f4e22a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyNormal`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode NORMAL.

########## 参数配置

此容器包含 **6** 个参数：

########### BOOLEAN 类型参数

############ 1. SbcEnableLDO_Stby

- **UUID**: `eaa2599e-d46d-4498-8c0e-79560243b29f`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Stby is switched on during mode change to 'NORMAL'.
False: LDO_Stby is switched off during mode change to 'NORMAL'.

############ 2. SbcEnableTracker1

- **UUID**: `cd69a56b-1bda-4c9d-8701-ce7e9ae4c54d`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker1 is switched on during mode change to 'NORMAL'.
False: Tracker1 is switched off during mode change to 'NORMAL'.

############ 3. SbcEnableTracker2

- **UUID**: `3d0f4cc4-d9ae-43c8-b93b-15c8400fc79b`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker2 is switched on during mode change to 'NORMAL'.
False: Tracker2 is switched off during mode change to 'NORMAL'.

############ 4. SbcEnableLDO_Com

- **UUID**: `6389ecb6-e1ff-427e-89ce-66e04f6390df`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Com is switched on during mode change to 'NORMAL'.
False: LDO_Com is switched off during mode change to 'NORMAL'.

############ 5. SbcEnableVoltRef

- **UUID**: `f0e2b2d2-54b0-4ec9-9433-30aafb2f6adb`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'NORMAL'.

True: Volt_Ref is switched on during mode change to 'NORMAL'.
False: Volt_Ref is switched off during mode change to 'NORMAL'.

############ 6. SbcDisableOffset

- **UUID**: `f2fefd30-4cee-4fff-a8e5-08deb273b078`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'NORMAL'.

True: Offset regulation disabled during mode change to 'NORMAL'.
False: Offset regulation enabled during mode change to 'NORMAL'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

######### 2. SbcEnableSupplyStandby

**容器属性**:

- **UUID**: `d794ee1a-f9f4-448c-9a1d-69c51603ce3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyStandby`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode STANDBY.

########## 参数配置

此容器包含 **6** 个参数：

########### BOOLEAN 类型参数

############ 1. SbcEnableLDO_Stby

- **UUID**: `3401fd59-1909-44d3-a5a7-b61c1e25c294`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Stby is switched on during mode change to 'STANDBY'.
False: LDO_Stby is switched off during mode change to 'STANDBY'.

############ 2. SbcEnableTracker1

- **UUID**: `3a558b5b-2b62-4e41-929c-97de38573283`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker1 is switched on during mode change to 'STANDBY'.
False: Tracker1 is switched off during mode change to 'STANDBY'.

############ 3. SbcEnableTracker2

- **UUID**: `53a84dce-a809-4d16-9c4d-e85d0833bab9`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker2 is switched on during mode change to 'STANDBY'.
False: Tracker2 is switched off during mode change to 'STANDBY'.

############ 4. SbcEnableLDO_Com

- **UUID**: `10f1aecc-d8fe-4a44-aee0-4375c837e935`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Com is switched on during mode change to 'STANDBY'.
False: LDO_Com is switched off during mode change to 'STANDBY'.

############ 5. SbcEnableVoltRef

- **UUID**: `959f4cc8-78c2-4283-9aa2-eba305164a5a`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'STANDBY'.

True: Volt_Ref is switched on during mode change to 'STANDBY'.
False: Volt_Ref is switched off during mode change to 'STANDBY'.

############ 6. SbcDisableOffset

- **UUID**: `586454d6-d498-475b-afbe-7a60dc81cda4`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'STANDBY'.

True: Offset regulation disabled during mode change to 'STANDBY'.
False: Offset regulation enabled during mode change to 'STANDBY'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

######### 3. SbcEnableSupplySleep

**容器属性**:

- **UUID**: `32ebd3c0-490e-4401-abe6-6872488a6590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplySleep`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode 'SLEEP'.

########## 参数配置

此容器包含 **2** 个参数：

########### BOOLEAN 类型参数

############ 1. SbcEnableLDO_Stby

- **UUID**: `7da7cd6b-fd99-4777-9b53-85c4a1453c26`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'SLEEP'.

True: LDO_Stby is switched on during mode change to 'SLEEP'.
False: LDO_Stby is switched off during mode change to 'SLEEP'.

############ 2. SbcDisableOffset

- **UUID**: `a255d855-f43a-473c-b246-bd28faff302d`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether  offset regulation is disabled during a mode change to system mode 'SLEEP'.

True: Offset regulation disabled during mode change to 'SLEEP'.
False: Offset regulation enabled during mode change to 'SLEEP'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 19. SbcEnableSupplyNormal

**容器属性**:

- **UUID**: `f652d512-f444-4be9-8c89-0d8724f4e22a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyNormal`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode NORMAL.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `eaa2599e-d46d-4498-8c0e-79560243b29f`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Stby is switched on during mode change to 'NORMAL'.
False: LDO_Stby is switched off during mode change to 'NORMAL'.

########## 2. SbcEnableTracker1

- **UUID**: `cd69a56b-1bda-4c9d-8701-ce7e9ae4c54d`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker1 is switched on during mode change to 'NORMAL'.
False: Tracker1 is switched off during mode change to 'NORMAL'.

########## 3. SbcEnableTracker2

- **UUID**: `3d0f4cc4-d9ae-43c8-b93b-15c8400fc79b`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker2 is switched on during mode change to 'NORMAL'.
False: Tracker2 is switched off during mode change to 'NORMAL'.

########## 4. SbcEnableLDO_Com

- **UUID**: `6389ecb6-e1ff-427e-89ce-66e04f6390df`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Com is switched on during mode change to 'NORMAL'.
False: LDO_Com is switched off during mode change to 'NORMAL'.

########## 5. SbcEnableVoltRef

- **UUID**: `f0e2b2d2-54b0-4ec9-9433-30aafb2f6adb`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'NORMAL'.

True: Volt_Ref is switched on during mode change to 'NORMAL'.
False: Volt_Ref is switched off during mode change to 'NORMAL'.

########## 6. SbcDisableOffset

- **UUID**: `f2fefd30-4cee-4fff-a8e5-08deb273b078`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'NORMAL'.

True: Offset regulation disabled during mode change to 'NORMAL'.
False: Offset regulation enabled during mode change to 'NORMAL'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 20. SbcEnableSupplyStandby

**容器属性**:

- **UUID**: `d794ee1a-f9f4-448c-9a1d-69c51603ce3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyStandby`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode STANDBY.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `3401fd59-1909-44d3-a5a7-b61c1e25c294`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Stby is switched on during mode change to 'STANDBY'.
False: LDO_Stby is switched off during mode change to 'STANDBY'.

########## 2. SbcEnableTracker1

- **UUID**: `3a558b5b-2b62-4e41-929c-97de38573283`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker1 is switched on during mode change to 'STANDBY'.
False: Tracker1 is switched off during mode change to 'STANDBY'.

########## 3. SbcEnableTracker2

- **UUID**: `53a84dce-a809-4d16-9c4d-e85d0833bab9`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker2 is switched on during mode change to 'STANDBY'.
False: Tracker2 is switched off during mode change to 'STANDBY'.

########## 4. SbcEnableLDO_Com

- **UUID**: `10f1aecc-d8fe-4a44-aee0-4375c837e935`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Com is switched on during mode change to 'STANDBY'.
False: LDO_Com is switched off during mode change to 'STANDBY'.

########## 5. SbcEnableVoltRef

- **UUID**: `959f4cc8-78c2-4283-9aa2-eba305164a5a`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'STANDBY'.

True: Volt_Ref is switched on during mode change to 'STANDBY'.
False: Volt_Ref is switched off during mode change to 'STANDBY'.

########## 6. SbcDisableOffset

- **UUID**: `586454d6-d498-475b-afbe-7a60dc81cda4`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'STANDBY'.

True: Offset regulation disabled during mode change to 'STANDBY'.
False: Offset regulation enabled during mode change to 'STANDBY'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 21. SbcEnableSupplySleep

**容器属性**:

- **UUID**: `32ebd3c0-490e-4401-abe6-6872488a6590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplySleep`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode 'SLEEP'.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `7da7cd6b-fd99-4777-9b53-85c4a1453c26`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'SLEEP'.

True: LDO_Stby is switched on during mode change to 'SLEEP'.
False: LDO_Stby is switched off during mode change to 'SLEEP'.

########## 2. SbcDisableOffset

- **UUID**: `a255d855-f43a-473c-b246-bd28faff302d`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether  offset regulation is disabled during a mode change to system mode 'SLEEP'.

True: Offset regulation disabled during mode change to 'SLEEP'.
False: Offset regulation enabled during mode change to 'SLEEP'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 22. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `2dad0642-ed59-4cdb-a065-11881e09d6e0`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **SbcSpiSequence**
  - UUID: `3efd54fd-abb3-4e66-9976-748858916ce8`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

##### 3. SbcWatchdogPeripheral

**容器属性**:

- **UUID**: `27e19832-9459-40c3-9c6f-ab9fe5018828`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the watchdog configuration.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. SbcWatchdogPeripheralId

- **UUID**: `083b6cb8-e4e0-4136-a32e-c3c25c39a3e0`
- **参数名**: `SbcWatchdogPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier for the watchdog peripheral. The value must be unique on one device instance.

######## 2. SbcWatchdogTriggerOffset

- **UUID**: `5bda48b2-0183-435b-8191-370b90e72939`
- **参数名**: `SbcWatchdogTriggerOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `60`
- **取值范围**: [0..100]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the offset in percent for the first trigger point to be located in the specified watchdog trigger interval.

######## 3. SbcWatchdogErrorThreshold

- **UUID**: `f8260379-3aa3-47b3-99b9-02b71665bd00`
- **参数名**: `SbcWatchdogErrorThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `9`
- **取值范围**: [0..15]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the watchdog (FWD/WWD) error threshold to generate reset and enter into INIT state.

Note: Depending on the value of parameter SbcWatchdogPeripheralType this value is written to WDCFG0.WWDETHR or FWDCFG.FWDETHR.

####### ENUMERATION 类型参数

######## 1. SbcWatchdogInitialMode

- **UUID**: `e5aeba31-bfae-48e5-93a8-c414c99168ee`
- **参数名**: `SbcWatchdogInitialMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDGIF_FAST_MODE`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDGIF_OFF_MODE` (来源: Vector Informatik)
  - `WDGIF_SLOW_MODE` (来源: Vector Informatik)
  - `WDGIF_FAST_MODE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the mode of the watchdog that is selected during the initialization of the Sbc.

WDGIF_OFF_MODE: Watchdog is disabled during initialization.
WDGIF_SLOW_MODE: Watchdog is initialized with SLOW mode.
WDGIF_FAST_MODE: Watchdog is initialized with FAST mode.

######## 2. SbcWatchdogPeripheralType

- **UUID**: `1b087f65-8ff0-41f7-9f34-5d604366675b`
- **参数名**: `SbcWatchdogPeripheralType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WWD`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `FWD` (来源: Vector Informatik)
  - `WWD` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the functional watchdog peripheral or the window watchdog peripheral is used.

FWD: Functional watchdog peripheral is used.
WWD: Window watchdog peripheral is used.

######## 3. SbcWatchdogPeripheralCycleTime

- **UUID**: `8af0fb11-07ee-452c-b68a-373c4b2a0dda`
- **参数名**: `SbcWatchdogPeripheralCycleTime`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `WDCYC_100US`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `WDCYC_100US` (来源: Vector Informatik)
  - `WDCYC_1MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the watchdog cycle time.

WDCYC_100US: Watchdog cycle time is set to 0.1 ms tick period.
WDCYC_1MS: Watchdog cycle time is set to 1 ms tick period.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SbcWatchdogPeripheralFastMode

**容器属性**:

- **UUID**: `2d60d2d6-3ede-4dd9-95f0-c82a46a32437`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralFastMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog FAST mode.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

########## 2. SbcWwdClosedWindow

- **UUID**: `4cf282e0-99d3-4cc5-bfd8-f612c9dc27b0`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 3. SbcWwdOpenWindow

- **UUID**: `7be92a08-70c0-4d6d-bcc8-a2f47ea40328`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `33ac922c-3d6e-4606-aa63-aab3f7043e5c`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

####### 2. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `ce686104-af20-40a5-b4d5-3e75c0a85495`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `f39de258-3fe1-4980-a6db-9af66e1fcf84`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

########## 2. SbcWwdClosedWindow

- **UUID**: `30ba22bc-98fe-4f68-8b7a-1509076630f6`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 3. SbcWwdOpenWindow

- **UUID**: `38609e16-7170-418b-87f6-39723c6c14b4`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

########## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `4a014b29-676b-4059-ab94-b04b9f7acbd7`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

##### 4. SbcWatchdogPeripheralFastMode

**容器属性**:

- **UUID**: `2d60d2d6-3ede-4dd9-95f0-c82a46a32437`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralFastMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog FAST mode.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

######## 2. SbcWwdClosedWindow

- **UUID**: `4cf282e0-99d3-4cc5-bfd8-f612c9dc27b0`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

######## 3. SbcWwdOpenWindow

- **UUID**: `7be92a08-70c0-4d6d-bcc8-a2f47ea40328`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

######## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `33ac922c-3d6e-4606-aa63-aab3f7043e5c`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

##### 5. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `ce686104-af20-40a5-b4d5-3e75c0a85495`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. SbcWatchdogTriggerPeriod

- **UUID**: `f39de258-3fe1-4980-a6db-9af66e1fcf84`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `70`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

######## 2. SbcWwdClosedWindow

- **UUID**: `30ba22bc-98fe-4f68-8b7a-1509076630f6`
- **参数名**: `SbcWwdClosedWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the closed window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG0.CW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

######## 3. SbcWwdOpenWindow

- **UUID**: `38609e16-7170-418b-87f6-39723c6c14b4`
- **参数名**: `SbcWwdOpenWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the open window time as multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to WWD. It is written to WWDCFG1.OW.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

######## 4. SbcFwdHeartbeatTimerPeriod

- **UUID**: `4a014b29-676b-4059-ab94-b04b9f7acbd7`
- **参数名**: `SbcFwdHeartbeatTimerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `11`
- **取值范围**: [0..31]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the functional watchdog heartbeat timer period as a multiple of 50 watchdog cycles.

Note: This value only is required in case SbcWatchdogPeripheralType is set to FWD. It is written to FWDCFG.WDHBTP.

0 = 50 wd cycles
1 = 100 wd cycles
2 = 150 wd cycles
...
31 = 1600 wd cycles

##### 6. SbcLinTrcvPeripheral

**容器属性**:

- **UUID**: `e7a6f2c5-221e-480c-b326-c7bb6402c2e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcLinTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for LIN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a LIN transceiver.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SbcLinTrcvPeripheralId

- **UUID**: `48130c2b-c138-46a0-a7c9-b74a366b0d24`
- **参数名**: `SbcLinTrcvPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the identifier for the LIN transceiver peripheral. The value must be unique on one device instance.

##### 7. SbcCanTrcvPeripheral

**容器属性**:

- **UUID**: `7af1c6aa-d50a-437d-9483-8d0d2dd50f0e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for CAN transceiver peripherals.

Note: Not used, since TLF35584 does not provide a CAN transceiver.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SbcCanTrcvPeripheralId

- **UUID**: `ec9e2dcb-68cc-4228-a900-bdd2ffa4bb52`
- **参数名**: `SbcCanTrcvPeripheralId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter specifies the identifier for the CAN transceiver peripheral. The value must be unique on one device instance.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SbcCanTrcvPartialNetwork

**容器属性**:

- **UUID**: `281541fc-fe4c-406c-bae9-416404d2afae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPartialNetwork`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the CAN transceiver driver information about the configuration of Partial Networking functionality. If the container is intantiated the selective wakeup functionality is activated on the CanTrcv peripheral.

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvBaudRate

- **UUID**: `f4cb591f-de56-4630-a40a-2331a240410d`
- **参数名**: `SbcCanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `500`
- **取值范围**: [0..1000]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN Bus communication baud rate in kbps.

########## 2. SbcCanTrcvPnFrameCanId

- **UUID**: `5314551f-b6aa-4aac-89c3-e34f75341cbd`
- **参数名**: `SbcCanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN ID of the Wake-up Frame (WUF).

########## 3. SbcCanTrcvPnFrameCanIdMask

- **UUID**: `337fe92b-d89a-4e8c-95df-23dccc173abe`
- **参数名**: `SbcCanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the ID Mask for the selective activation of the transceiver. It is used to configure a Wake-up frame (WUF) which consists of a group of CAN identifiers.

########## 4. SbcCanTrcvPnFrameDlc

- **UUID**: `220f7504-983c-48ef-955d-9337e3af4a53`
- **参数名**: `SbcCanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..8]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the data length of the Wake-up Frame (WUF).

######### BOOLEAN 类型参数

########## 1. SbcCanTrcvPnCanIdIsExtended

- **UUID**: `820b3bbe-8556-40bf-a809-4036c277b07f`
- **参数名**: `SbcCanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether extended or standard identifier is used for wake-up frames.

True: Extended CAN identifier is used.
False: Standard CAN identifier is used.

########## 2. SbcCanTrcvPnEnabled

- **UUID**: `305fb7f5-1348-4837-9b3b-cf5eb89a320f`
- **参数名**: `SbcCanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

########## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `e7755d91-7d2f-4102-92a2-4d3b13d8fc27`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up configuration should be verified after it has been written to the hardware.

TRUE  = The selective wakeup configuration written to the hardware is compared to the configured values.
FALSE = The selective wakeup configuration written to the hardware is not compared to the configured values.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

####### 2. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

##### 8. SbcCanTrcvPartialNetwork

**容器属性**:

- **UUID**: `281541fc-fe4c-406c-bae9-416404d2afae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPartialNetwork`
- **多重性**: [0..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the CAN transceiver driver information about the configuration of Partial Networking functionality. If the container is intantiated the selective wakeup functionality is activated on the CanTrcv peripheral.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. SbcCanTrcvBaudRate

- **UUID**: `f4cb591f-de56-4630-a40a-2331a240410d`
- **参数名**: `SbcCanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `500`
- **取值范围**: [0..1000]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN Bus communication baud rate in kbps.

######## 2. SbcCanTrcvPnFrameCanId

- **UUID**: `5314551f-b6aa-4aac-89c3-e34f75341cbd`
- **参数名**: `SbcCanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the CAN ID of the Wake-up Frame (WUF).

######## 3. SbcCanTrcvPnFrameCanIdMask

- **UUID**: `337fe92b-d89a-4e8c-95df-23dccc173abe`
- **参数名**: `SbcCanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the ID Mask for the selective activation of the transceiver. It is used to configure a Wake-up frame (WUF) which consists of a group of CAN identifiers.

######## 4. SbcCanTrcvPnFrameDlc

- **UUID**: `220f7504-983c-48ef-955d-9337e3af4a53`
- **参数名**: `SbcCanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..8]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the data length of the Wake-up Frame (WUF).

####### BOOLEAN 类型参数

######## 1. SbcCanTrcvPnCanIdIsExtended

- **UUID**: `820b3bbe-8556-40bf-a809-4036c277b07f`
- **参数名**: `SbcCanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether extended or standard identifier is used for wake-up frames.

True: Extended CAN identifier is used.
False: Standard CAN identifier is used.

######## 2. SbcCanTrcvPnEnabled

- **UUID**: `305fb7f5-1348-4837-9b3b-cf5eb89a320f`
- **参数名**: `SbcCanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

######## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `e7755d91-7d2f-4102-92a2-4d3b13d8fc27`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the selective wake-up configuration should be verified after it has been written to the hardware.

TRUE  = The selective wakeup configuration written to the hardware is compared to the configured values.
FALSE = The selective wakeup configuration written to the hardware is not compared to the configured values.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

##### 9. SbcCanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `71e1b7d4-961e-4eae-89d6-0b67f5e32d51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcCanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SbcCanTrcvPnFrameDataMask

- **UUID**: `4f52a414-cfd9-4593-9b2b-a0748fed4bc3`
- **参数名**: `SbcCanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 2. SbcCanTrcvPnFrameDataMaskIndex

- **UUID**: `8856785f-0c42-4773-ac93-7b1cd33c7dfd`
- **参数名**: `SbcCanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..7]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the position n in frame of the mask-part.

##### 10. SbcInitConfig

**容器属性**:

- **UUID**: `88ea0b2f-3b3d-4b85-8cfd-2177032c69fc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcInitConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the initialization configuration of the Sbc device.

###### 参数配置

此容器包含 **5** 个参数：

####### BOOLEAN 类型参数

######## 1. SbcErrPinMonitor

- **UUID**: `f93b059a-5e7b-4830-9b3c-72bffc96b215`
- **参数名**: `SbcErrPinMonitor`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether the ERR pin monitor functionality is enabled.

True: ERR pin monitor functionality is enabled.
Flase: ERR pin monitor functionality is disabled.

Note: If this parameter is enabled the ERR pin monitoring supervision function has to be serviced properly, otherwise resets will occur.

######## 2. SbcErrPinMonitorRecovery

- **UUID**: `5285667b-fce2-4e1c-99e8-0f44a158a7a8`
- **参数名**: `SbcErrPinMonitorRecovery`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether error pin monitor recovery enable is requested during initialization.

True: Error pin monitor recovery enable is requested.
False: Error pin monitor recovery enable is not requested.


Note: This value is used to set register field SYSPCFG1.ERRREC.

######## 3. SbcErrPinMonitorInSleep

- **UUID**: `3c740928-0fe8-48b5-833b-55a88dc24a12`
- **参数名**: `SbcErrPinMonitorInSleep`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether error pin monitoring is active in SLEEP.

True: Error pin monitoring is active in SLEEP.
False: Error pin monitoring is not active in SLEEP.

Note: This value is used to write register field SYSPCFG1.ERRSLPEN.

####### ENUMERATION 类型参数

######## 1. SbcErrPinRecoveryTime

- **UUID**: `efd145a6-25c6-46eb-8fb0-3566da59cbfe`
- **参数名**: `SbcErrPinRecoveryTime`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ERREC_1_MS`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ERREC_1_MS` (来源: Vector Informatik)
  - `ERREC_2_5MS` (来源: Vector Informatik)
  - `ERREC_5MS` (来源: Vector Informatik)
  - `ERREC_10MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the ERR pin monitor recovery time which is requested during initialization.

ERREC_1_MS: An ERR pin monitor recovery time of 1 ms is requested.
ERREC_2_5MS: An ERR pin monitor recovery time of 2.5 ms is requested.
ERREC_5MS: An ERR pin monitor recovery time of 5 ms is requested.
ERREC_10MS : An ERR pin monitor recovery time of 10 ms is requested.


Note: This value is used to set register field SYSPCFG1.ERR.

######## 2. SbcSafeState2Delay

- **UUID**: `5dbd3e0f-27bb-4188-bfcb-c7063ddedcae`
- **参数名**: `SbcSafeState2Delay`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `SS2DEL_NODELAY`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `SS2DEL_NODELAY` (来源: Vector Informatik)
  - `SS2DEL_10MS` (来源: Vector Informatik)
  - `SS2DEL_50MS` (来源: Vector Informatik)
  - `SS2DEL_100MS` (来源: Vector Informatik)
  - `SS2DEL_250MS` (来源: Vector Informatik)
  - `SS2DEL_1250MS` (来源: Vector Informatik)
  - `SS2DEL_2500MS` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines the delay applied for transitions from NORMAL to INIT, WAKE and SLEEP state.

SS2DEL_NODELAY: Delay of 0 ms is request.
SS2DEL_10MS: Delay of 10 ms is requested.
SS2DEL_50MS: Delay of 50 ms is requested.
SS2DEL_100MS: Delay of 100 ms is requested.
SS2DEL_250MS: Delay of 250 ms is requested.
SS2DEL_1250MS: Delay of 1250 ms is requested. (This value is only available for the TLF35585)
SS2DEL_2500MS: Delay of 2500 ms is requested. (This value is only available for the TLF35585)

Note: This value is related with register field SYSPCFG1.SS2DEL.

##### 11. SbcDeviceAccess

**容器属性**:

- **UUID**: `14af1db9-3f2c-4968-aaef-7d16666f06fa`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDeviceAccess`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes the configuration to access the specific Sbc hardware instance.

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. SbcDioAccess

**容器属性**:

- **UUID**: `0eed5ef3-93c6-4814-8d28-205047c68ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Dio-specific configuration to access the Sbc device.

Note: The existence of this container in combination with the usage of the SbcWatchdogPeripheralType 'WWD' means that the window watchdog is not triggered via SPI, but via the input pin WDI.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWaitLoopCycles

- **UUID**: `13937262-5ac4-4503-bb69-01b69183e95c`
- **参数名**: `SbcWaitLoopCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6000`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the number of loop cycles to perform a wait until the WDI high level is sampled by the device.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

####### 2. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

####### 3. SbcSpiAccess

**容器属性**:

- **UUID**: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

######### 2. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

####### 4. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

####### 5. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

####### 6. SbcI2cAccess

**容器属性**:

- **UUID**: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the I2C-specific configuration to access the Sbc device.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

######### 2. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

####### 7. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

####### 8. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

####### 9. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `2dad0642-ed59-4cdb-a065-11881e09d6e0`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **SbcSpiSequence**
  - UUID: `3efd54fd-abb3-4e66-9976-748858916ce8`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

##### 12. SbcDioAccess

**容器属性**:

- **UUID**: `0eed5ef3-93c6-4814-8d28-205047c68ea4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Dio-specific configuration to access the Sbc device.

Note: The existence of this container in combination with the usage of the SbcWatchdogPeripheralType 'WWD' means that the window watchdog is not triggered via SPI, but via the input pin WDI.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SbcWaitLoopCycles

- **UUID**: `13937262-5ac4-4503-bb69-01b69183e95c`
- **参数名**: `SbcWaitLoopCycles`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `6000`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the number of loop cycles to perform a wait until the WDI high level is sampled by the device.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

##### 13. SbcDioChannel

**容器属性**:

- **UUID**: `44560ba8-4534-4595-acbe-9559264745c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers includes the reference to one Dio Channel that is used by the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcDioChannelRef

- **UUID**: `95789b1c-9f32-4f0a-9d30-617834df3749`
- **引用名**: `SbcDioChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `DioChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Dio Channel that is connected to the device input pin WDI.

Note: If this reference is instantiated, the window watchdog (WWD) is triggered using the WDI pin mechanism instead of SPI trigger mechanism.

##### 14. SbcSpiAccess

**容器属性**:

- **UUID**: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

####### 2. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

##### 15. SbcSpiSequence

**容器属性**:

- **UUID**: `3efd54fd-abb3-4e66-9976-748858916ce8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcSpiSequenceRef

- **UUID**: `ee28b0ff-efe6-4448-94b7-961d44fc2434`
- **引用名**: `SbcSpiSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Sequence that is used to access the Sbc.

##### 16. SbcSpiChannel

**容器属性**:

- **UUID**: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcSpiChannelRef

- **UUID**: `859a2f88-b9eb-4459-8baa-2f79acf65fdc`
- **引用名**: `SbcSpiChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the Spi Channel that is used to access the Sbc.

##### 17. SbcI2cAccess

**容器属性**:

- **UUID**: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the I2C-specific configuration to access the Sbc device.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

####### 2. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

##### 18. SbcI2cSequence

**容器属性**:

- **UUID**: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcI2cSequenceRef

- **UUID**: `4026a952-fc57-4396-b2b9-79c4078bb610`
- **引用名**: `SbcI2cSequenceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cSequence`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cSequence`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Sequence that is used to access the Sbc.

##### 19. SbcI2cChannel

**容器属性**:

- **UUID**: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcI2cChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcI2cChannelRef

- **UUID**: `e467a664-6f85-425f-9159-04705f4a0f25`
- **引用名**: `SbcI2cChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `I2cChannel`
- **完整路径**: `/MICROSAR/I2c/I2cConfigSet/I2cChannel`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Reference to the I2c Channel that is used to access the Sbc.

##### 20. SbcSystemConfig

**容器属性**:

- **UUID**: `25665cc7-d217-4b36-96da-a8ccde877534`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSystemConfig`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes system specific configuration.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. SbcEnableSupplyNormal

**容器属性**:

- **UUID**: `f652d512-f444-4be9-8c89-0d8724f4e22a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyNormal`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode NORMAL.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `eaa2599e-d46d-4498-8c0e-79560243b29f`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Stby is switched on during mode change to 'NORMAL'.
False: LDO_Stby is switched off during mode change to 'NORMAL'.

########## 2. SbcEnableTracker1

- **UUID**: `cd69a56b-1bda-4c9d-8701-ce7e9ae4c54d`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker1 is switched on during mode change to 'NORMAL'.
False: Tracker1 is switched off during mode change to 'NORMAL'.

########## 3. SbcEnableTracker2

- **UUID**: `3d0f4cc4-d9ae-43c8-b93b-15c8400fc79b`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker2 is switched on during mode change to 'NORMAL'.
False: Tracker2 is switched off during mode change to 'NORMAL'.

########## 4. SbcEnableLDO_Com

- **UUID**: `6389ecb6-e1ff-427e-89ce-66e04f6390df`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Com is switched on during mode change to 'NORMAL'.
False: LDO_Com is switched off during mode change to 'NORMAL'.

########## 5. SbcEnableVoltRef

- **UUID**: `f0e2b2d2-54b0-4ec9-9433-30aafb2f6adb`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'NORMAL'.

True: Volt_Ref is switched on during mode change to 'NORMAL'.
False: Volt_Ref is switched off during mode change to 'NORMAL'.

########## 6. SbcDisableOffset

- **UUID**: `f2fefd30-4cee-4fff-a8e5-08deb273b078`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'NORMAL'.

True: Offset regulation disabled during mode change to 'NORMAL'.
False: Offset regulation enabled during mode change to 'NORMAL'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 2. SbcEnableSupplyStandby

**容器属性**:

- **UUID**: `d794ee1a-f9f4-448c-9a1d-69c51603ce3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyStandby`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode STANDBY.

######## 参数配置

此容器包含 **6** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `3401fd59-1909-44d3-a5a7-b61c1e25c294`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Stby is switched on during mode change to 'STANDBY'.
False: LDO_Stby is switched off during mode change to 'STANDBY'.

########## 2. SbcEnableTracker1

- **UUID**: `3a558b5b-2b62-4e41-929c-97de38573283`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker1 is switched on during mode change to 'STANDBY'.
False: Tracker1 is switched off during mode change to 'STANDBY'.

########## 3. SbcEnableTracker2

- **UUID**: `53a84dce-a809-4d16-9c4d-e85d0833bab9`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker2 is switched on during mode change to 'STANDBY'.
False: Tracker2 is switched off during mode change to 'STANDBY'.

########## 4. SbcEnableLDO_Com

- **UUID**: `10f1aecc-d8fe-4a44-aee0-4375c837e935`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Com is switched on during mode change to 'STANDBY'.
False: LDO_Com is switched off during mode change to 'STANDBY'.

########## 5. SbcEnableVoltRef

- **UUID**: `959f4cc8-78c2-4283-9aa2-eba305164a5a`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'STANDBY'.

True: Volt_Ref is switched on during mode change to 'STANDBY'.
False: Volt_Ref is switched off during mode change to 'STANDBY'.

########## 6. SbcDisableOffset

- **UUID**: `586454d6-d498-475b-afbe-7a60dc81cda4`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'STANDBY'.

True: Offset regulation disabled during mode change to 'STANDBY'.
False: Offset regulation enabled during mode change to 'STANDBY'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

####### 3. SbcEnableSupplySleep

**容器属性**:

- **UUID**: `32ebd3c0-490e-4401-abe6-6872488a6590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplySleep`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode 'SLEEP'.

######## 参数配置

此容器包含 **2** 个参数：

######### BOOLEAN 类型参数

########## 1. SbcEnableLDO_Stby

- **UUID**: `7da7cd6b-fd99-4777-9b53-85c4a1453c26`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'SLEEP'.

True: LDO_Stby is switched on during mode change to 'SLEEP'.
False: LDO_Stby is switched off during mode change to 'SLEEP'.

########## 2. SbcDisableOffset

- **UUID**: `a255d855-f43a-473c-b246-bd28faff302d`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether  offset regulation is disabled during a mode change to system mode 'SLEEP'.

True: Offset regulation disabled during mode change to 'SLEEP'.
False: Offset regulation enabled during mode change to 'SLEEP'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

##### 21. SbcEnableSupplyNormal

**容器属性**:

- **UUID**: `f652d512-f444-4be9-8c89-0d8724f4e22a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyNormal`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode NORMAL.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. SbcEnableLDO_Stby

- **UUID**: `eaa2599e-d46d-4498-8c0e-79560243b29f`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Stby is switched on during mode change to 'NORMAL'.
False: LDO_Stby is switched off during mode change to 'NORMAL'.

######## 2. SbcEnableTracker1

- **UUID**: `cd69a56b-1bda-4c9d-8701-ce7e9ae4c54d`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker1 is switched on during mode change to 'NORMAL'.
False: Tracker1 is switched off during mode change to 'NORMAL'.

######## 3. SbcEnableTracker2

- **UUID**: `3d0f4cc4-d9ae-43c8-b93b-15c8400fc79b`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'NORMAL'.

True: Tracker2 is switched on during mode change to 'NORMAL'.
False: Tracker2 is switched off during mode change to 'NORMAL'.

######## 4. SbcEnableLDO_Com

- **UUID**: `6389ecb6-e1ff-427e-89ce-66e04f6390df`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'NORMAL'.

True: LDO_Com is switched on during mode change to 'NORMAL'.
False: LDO_Com is switched off during mode change to 'NORMAL'.

######## 5. SbcEnableVoltRef

- **UUID**: `f0e2b2d2-54b0-4ec9-9433-30aafb2f6adb`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'NORMAL'.

True: Volt_Ref is switched on during mode change to 'NORMAL'.
False: Volt_Ref is switched off during mode change to 'NORMAL'.

######## 6. SbcDisableOffset

- **UUID**: `f2fefd30-4cee-4fff-a8e5-08deb273b078`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'NORMAL'.

True: Offset regulation disabled during mode change to 'NORMAL'.
False: Offset regulation enabled during mode change to 'NORMAL'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

##### 22. SbcEnableSupplyStandby

**容器属性**:

- **UUID**: `d794ee1a-f9f4-448c-9a1d-69c51603ce3d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplyStandby`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode STANDBY.

###### 参数配置

此容器包含 **6** 个参数：

####### BOOLEAN 类型参数

######## 1. SbcEnableLDO_Stby

- **UUID**: `3401fd59-1909-44d3-a5a7-b61c1e25c294`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Stby is switched on during mode change to 'STANDBY'.
False: LDO_Stby is switched off during mode change to 'STANDBY'.

######## 2. SbcEnableTracker1

- **UUID**: `3a558b5b-2b62-4e41-929c-97de38573283`
- **参数名**: `SbcEnableTracker1`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker1 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker1 is switched on during mode change to 'STANDBY'.
False: Tracker1 is switched off during mode change to 'STANDBY'.

######## 3. SbcEnableTracker2

- **UUID**: `53a84dce-a809-4d16-9c4d-e85d0833bab9`
- **参数名**: `SbcEnableTracker2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Tracker2 is switched on during a mode change to system mode 'STANDBY'.

True: Tracker2 is switched on during mode change to 'STANDBY'.
False: Tracker2 is switched off during mode change to 'STANDBY'.

######## 4. SbcEnableLDO_Com

- **UUID**: `10f1aecc-d8fe-4a44-aee0-4375c837e935`
- **参数名**: `SbcEnableLDO_Com`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Com is switched on during a mode change to system mode 'STANDBY'.

True: LDO_Com is switched on during mode change to 'STANDBY'.
False: LDO_Com is switched off during mode change to 'STANDBY'.

######## 5. SbcEnableVoltRef

- **UUID**: `959f4cc8-78c2-4283-9aa2-eba305164a5a`
- **参数名**: `SbcEnableVoltRef`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether Volt_Ref is switched on during a mode change to system mode 'STANDBY'.

True: Volt_Ref is switched on during mode change to 'STANDBY'.
False: Volt_Ref is switched off during mode change to 'STANDBY'.

######## 6. SbcDisableOffset

- **UUID**: `586454d6-d498-475b-afbe-7a60dc81cda4`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether offset regulation is disabled during a mode change to system mode 'STANDBY'.

True: Offset regulation disabled during mode change to 'STANDBY'.
False: Offset regulation enabled during mode change to 'STANDBY'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

##### 23. SbcEnableSupplySleep

**容器属性**:

- **UUID**: `32ebd3c0-490e-4401-abe6-6872488a6590`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcEnableSupplySleep`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

This container includes mode-specific configuration of power supplies for system mode 'SLEEP'.

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. SbcEnableLDO_Stby

- **UUID**: `7da7cd6b-fd99-4777-9b53-85c4a1453c26`
- **参数名**: `SbcEnableLDO_Stby`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether LDO_Stby is switched on during a mode change to system mode 'SLEEP'.

True: LDO_Stby is switched on during mode change to 'SLEEP'.
False: LDO_Stby is switched off during mode change to 'SLEEP'.

######## 2. SbcDisableOffset

- **UUID**: `a255d855-f43a-473c-b246-bd28faff302d`
- **参数名**: `SbcDisableOffset`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter defines whether  offset regulation is disabled during a mode change to system mode 'SLEEP'.

True: Offset regulation disabled during mode change to 'SLEEP'.
False: Offset regulation enabled during mode change to 'SLEEP'.

Hint: This bit is only present for derivative Tlf35585. For derivative Tlf35584 this value has to be false!

##### 24. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `2dad0642-ed59-4cdb-a065-11881e09d6e0`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `93aef522-dfdd-4aba-8fae-cbe459666b69`
- **SbcSpiSequence**
  - UUID: `3efd54fd-abb3-4e66-9976-748858916ce8`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `76e3c69f-95e1-4a9b-89cc-29277fec02d2`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The Shortname of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `ff12b0ba-d475-460b-a7cc-14c15ee850de`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `f8bc67e1-39cd-422f-b7e8-25e7aebbba5a`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `d0e8ae03-39f3-4c5f-9af2-cd4206c808df`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Sbc_Tlf35584

- **UUID**: `5e99acbb-d00a-4f1d-ad9d-a851bd4ef4c8`
- **包名称**: `Sbc_Tlf35584`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Sbc_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Sbc**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Sbc_Pre**
2. **Sbc_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Sbc_Impl

- **UUID**: `31758edf-b892-49d2-bedd-97d1e783369c`
- **实现名称**: `Sbc_Impl`
- **编程语言**: C
- **软件版本**: 1.06.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Sbc_Pre

- **UUID**: `f6ce79b4-a6e8-44f4-b6bf-067a2395f10a`
- **配置名称**: `Sbc_Pre`
- **定义引用**: `/MICROSAR/Sbc_Tlf35584/Sbc`

### 2. Sbc_Rec

- **UUID**: `1d08d423-2cab-4fc3-8319-59a7a5482b2f`
- **配置名称**: `Sbc_Rec`
- **定义引用**: `/MICROSAR/Sbc_Tlf35584/Sbc`
