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

共有 **19** 个版本记录：

##### 1. 版本 1.00.00

- **状态**: released
- **发布日期**: 2014-09-04T11:07:41+02:00
- **发布者**: visrse

**变更内容**:

##### 2. 版本 1.01.00

- **状态**: released
- **发布日期**: 2015-09-04T06:42:19+02:00
- **发布者**: visrse

**变更内容**:

##### 3. 版本 2.00.00

- **状态**: released
- **发布日期**: 2015-11-28T11:45:50+01:00
- **发布者**: visrse

**变更内容**:

##### 4. 版本 2.01.00

- **状态**: released
- **发布日期**: 2016-04-20T08:33:50+02:00
- **发布者**: visrse

**变更内容**:

##### 5. 版本 2.01.01

- **状态**: released
- **发布日期**: 2019-05-16T13:49:33+02:00
- **发布者**: virmid

**变更内容**:

##### 6. 版本 2.02.00

- **状态**: released
- **发布日期**: 2019-11-15T14:18:35+01:00
- **发布者**: visjan

**变更内容**:

##### 7. 版本 2.03.00

- **状态**: released
- **发布日期**: 2020-02-24T17:49:50+01:00
- **发布者**: virmid

**变更内容**:

##### 8. 版本 2.03.01

- **状态**: released
- **发布日期**: 2020-10-30T09:56:33+01:00
- **发布者**: virmcn

**变更内容**:

##### 9. 版本 2.04.00

- **状态**: released
- **发布日期**: 2021-04-26T09:59:20+02:00
- **发布者**: visjan

**变更内容**:

##### 10. 版本 2.04.01

- **状态**: released
- **发布日期**: 2022-03-15T15:49:49+01:00
- **发布者**: visjan

**变更内容**:

##### 11. 版本 2.04.02

- **状态**: released
- **发布日期**: 2022-06-02T08:38:14+02:00
- **发布者**: visjan

**变更内容**:

##### 12. 版本 2.04.03

- **状态**: released
- **发布日期**: 2022-07-14T11:02:27+02:00
- **发布者**: virmcn

**变更内容**:

##### 13. 版本 2.04.04

- **状态**: released
- **发布日期**: 2022-10-12T11:22:40+02:00
- **发布者**: coberpriller

**变更内容**:

##### 14. 版本 2.05.00

- **状态**: released
- **发布日期**: 2022-12-14T13:53:02+01:00
- **发布者**: visjan, rwerhahn

**变更内容**:

##### 15. 版本 2.05.01

- **状态**: released
- **发布日期**: 2023-03-20T09:16:32+01:00
- **发布者**: virmcn

**变更内容**:

##### 16. 版本 2.06.00

- **状态**: released
- **发布日期**: 2023-06-20T10:35:12+02:00
- **发布者**: coberpriller

**变更内容**:

##### 17. 版本 2.06.01

- **状态**: relesaed
- **发布日期**: 2023-10-04T08:57:10+02:00
- **发布者**: virmcn

**变更内容**:

##### 18. 版本 2.06.02

- **状态**: released
- **发布日期**: 2024-01-10T11:00:04+01:00
- **发布者**: virmcn

**变更内容**:

##### 19. 版本 2.06.03

- **状态**: released
- **发布日期**: 2024-02-29T08:41:06+01:00
- **发布者**: rwerhahn

**变更内容**:

#### 配置容器

本模块包含 **20** 个配置容器：

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

此容器包含 **5** 个参数：

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

- **UUID**: `ed3d9a71-6a9d-4a99-86de-2e91ca26acda`
- **参数名**: `SbcSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Selects if safety checks are used.

These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

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

此容器包含 **1** 个参数：

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

###### 配置容器

本模块包含 **18** 个配置容器：

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

此容器包含 **3** 个参数：

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
- **默认值**: `50`
- **取值范围**: [0..500]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the offset in percent for the first trigger point to be located in the specified watchdog trigger interval.

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

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

######### 2. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `2f599b0d-a65c-402b-a6a6-f331c11cd738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SbcWatchdogTriggerPeriod

- **UUID**: `b2bf758a-0ccc-417e-9cd0-fc6f4a1f8d05`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

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

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

####### 3. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `2f599b0d-a65c-402b-a6a6-f331c11cd738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `b2bf758a-0ccc-417e-9cd0-fc6f4a1f8d05`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

####### 4. SbcLinTrcvPeripheral

**容器属性**:

- **UUID**: `e7a6f2c5-221e-480c-b326-c7bb6402c2e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcLinTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for LIN transceiver peripherals.

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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

############ 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `d1bbe442-e23c-473d-b0cc-15ece0843270`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

########## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `d1bbe442-e23c-473d-b0cc-15ece0843270`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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

####### 9. SbcDeviceAccess

**容器属性**:

- **UUID**: `53833c01-800a-40d8-b626-75d91c8e4c56`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDeviceAccess`
- **多重性**: [1..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. SbcDioAccess

**容器属性**:

- **UUID**: `e53c9f29-1961-4fb5-a7bd-cbf135fd58d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

######### 2. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

######### 3. SbcSpiAccess

**容器属性**:

- **UUID**: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the SPI-specific configuration to access the Sbc device.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `f8f14e3b-d97f-4b10-9036-756d49145d79`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
  - 描述: This container includes the SPI-specific configuration to access the Sbc device.
- **SbcSpiSequence**
  - UUID: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `b573d4b8-6d72-4034-a6c4-5965debce854`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

####### 10. SbcDioAccess

**容器属性**:

- **UUID**: `e53c9f29-1961-4fb5-a7bd-cbf135fd58d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

####### 11. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

####### 12. SbcSpiAccess

**容器属性**:

- **UUID**: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the SPI-specific configuration to access the Sbc device.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

####### 18. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `f8f14e3b-d97f-4b10-9036-756d49145d79`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
  - 描述: This container includes the SPI-specific configuration to access the Sbc device.
- **SbcSpiSequence**
  - UUID: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `b573d4b8-6d72-4034-a6c4-5965debce854`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

此容器包含 **3** 个参数：

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
- **默认值**: `50`
- **取值范围**: [0..500]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This value specifies the offset in percent for the first trigger point to be located in the specified watchdog trigger interval.

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

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

####### 2. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `2f599b0d-a65c-402b-a6a6-f331c11cd738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SbcWatchdogTriggerPeriod

- **UUID**: `b2bf758a-0ccc-417e-9cd0-fc6f4a1f8d05`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

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

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SbcWatchdogTriggerPeriod

- **UUID**: `bea22fe9-0611-48b7-b9fe-1c69e8c404f3`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value specifies the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

##### 5. SbcWatchdogPeripheralSlowMode

**容器属性**:

- **UUID**: `2f599b0d-a65c-402b-a6a6-f331c11cd738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcWatchdogPeripheralSlowMode`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes configuration of watchdog SLOW mode.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SbcWatchdogTriggerPeriod

- **UUID**: `b2bf758a-0ccc-417e-9cd0-fc6f4a1f8d05`
- **参数名**: `SbcWatchdogTriggerPeriod`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `8`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: The value species the period (in milliseconds) of the hardware watchdog triggering. This has to be configured according to the requirements of the hardware configuration.

##### 6. SbcLinTrcvPeripheral

**容器属性**:

- **UUID**: `e7a6f2c5-221e-480c-b326-c7bb6402c2e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcLinTrcvPeripheral`
- **多重性**: [0..infinite]
- **构建后可变**: false

**容器描述**:

This container includes the configuration for LIN transceiver peripherals.

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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

########## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `d1bbe442-e23c-473d-b0cc-15ece0843270`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines whether the selective wake-up function is enabled or disabled in HW.

True: Selective wakeup feature is enabled in the transceiver hardware.
False: Selective wakeup feature is disabled in the transceiver hardware.

######## 3. SbcCanTrcvVerifyPnConfig

- **UUID**: `d1bbe442-e23c-473d-b0cc-15ece0843270`
- **参数名**: `SbcCanTrcvVerifyPnConfig`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
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

##### 11. SbcDeviceAccess

**容器属性**:

- **UUID**: `53833c01-800a-40d8-b626-75d91c8e4c56`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDeviceAccess`
- **多重性**: [1..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. SbcDioAccess

**容器属性**:

- **UUID**: `e53c9f29-1961-4fb5-a7bd-cbf135fd58d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

####### 2. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

####### 3. SbcSpiAccess

**容器属性**:

- **UUID**: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the SPI-specific configuration to access the Sbc device.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `f8f14e3b-d97f-4b10-9036-756d49145d79`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
  - 描述: This container includes the SPI-specific configuration to access the Sbc device.
- **SbcSpiSequence**
  - UUID: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `b573d4b8-6d72-4034-a6c4-5965debce854`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

##### 12. SbcDioAccess

**容器属性**:

- **UUID**: `e53c9f29-1961-4fb5-a7bd-cbf135fd58d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioAccess`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

##### 13. SbcDioChannel

**容器属性**:

- **UUID**: `16c603ff-f066-48ab-9e8c-525fe95ebd06`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcDioChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcDioChannelRef

- **UUID**: `fa49416d-81a2-4290-824d-c6ab04a0c4a4`
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
- **描述**: Reference to the Dio Channel that is used to access the Sbc.

##### 14. SbcSpiAccess

**容器属性**:

- **UUID**: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiAccess`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the SPI-specific configuration to access the Sbc device.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. SbcSpiSequence

**容器属性**:

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiSequence`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcSpiSequenceRef

- **UUID**: `55afb6de-125a-4f86-83cf-b6d4dfffc0f7`
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

- **UUID**: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SbcSpiChannel`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. SbcSpiChannelRef

- **UUID**: `6d686c4d-3ab4-4894-ab24-3922436b42ae`
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

- **UUID**: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

- **UUID**: `b573d4b8-6d72-4034-a6c4-5965debce854`
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

- **UUID**: `f7d36a65-8e74-44e0-8eff-5b0e3059a89f`
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

- **UUID**: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
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

- **UUID**: `81b05978-61e0-47fc-9d14-704d6a4bd26a`
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

##### 20. SbcDeviceAccessInterface

**容器属性**:

- **UUID**: `f8f14e3b-d97f-4b10-9036-756d49145d79`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `SbcDeviceAccessInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **SbcSpiAccess**
  - UUID: `14434683-c4c1-4cee-b8fe-42b967b1d8f2`
  - 描述: This container includes the SPI-specific configuration to access the Sbc device.
- **SbcSpiSequence**
  - UUID: `ea14f9cb-1adc-4a4d-bf24-2f07e1ad0fb3`
  - 描述: This containers represents one Spi Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcSpiChannel**
  - UUID: `6b0cf1be-1552-4b74-bf1b-8fdccb8bcf5e`
  - 描述: This containers represents one Spi Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cAccess**
  - UUID: `fdf2d482-7a55-45b3-a70b-a2545ee82a4e`
  - 描述: This container includes the I2C-specific configuration to access the Sbc device.
- **SbcI2cSequence**
  - UUID: `b573d4b8-6d72-4034-a6c4-5965debce854`
  - 描述: This containers represents one I2c Sequence that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.
- **SbcI2cChannel**
  - UUID: `a9eb190b-a683-4dd4-bbd6-dd6c788baa62`
  - 描述: This containers represents one I2c Channel that is used by the Sbc module. The short-name of the container instance specifies the name of the Sbc module.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. Sbc

- **UUID**: `5e99acbb-d00a-4f1d-ad9d-a851bd4ef4c8`
- **包名称**: `Sbc`
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
- **软件版本**: 2.06.03
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Sbc_Pre

- **UUID**: `f6ce79b4-a6e8-44f4-b6bf-067a2395f10a`
- **配置名称**: `Sbc_Pre`
- **定义引用**: `/MICROSAR/Sbc/Sbc`

### 2. Sbc_Rec

- **UUID**: `1d08d423-2cab-4fc3-8319-59a7a5482b2f`
- **配置名称**: `Sbc_Rec`
- **定义引用**: `/MICROSAR/Sbc/Sbc`
