# EthTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:44:55

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthTrcv](#ethtrcv)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthTrcv

#### 基本信息

- **UUID**: `192d065f-6ec8-4390-82ac-47b08b7a2701`
- **模块名称**: `EthTrcv`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the EthTrcv (Ethernet Transceiver driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 01.00.00

- **发布日期**: 2015-11-27T02:18:54+01:00
- **发布者**: vismha

**变更内容**:

#### 配置容器

本模块包含 **10** 个配置容器：

##### 1. EthTrcvGeneral

**容器属性**:

- **UUID**: `6715eb15-c5fb-4462-aa16-48c2492ca2c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

General configuration of Ethernet Transceiver Driver module

###### 参数配置

此容器包含 **22** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvMaxTrcvsSupported

- **UUID**: `af8a4727-aa8f-4c6e-9cff-ec5c200d2e0f`
- **参数名**: `EthTrcvMaxTrcvsSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value limits the maximum number of transceiver configurations per transceiver driver

######## 2. EthTrcvIndex

- **UUID**: `0fe521cc-7602-4623-93b0-ca5e83cab61b`
- **参数名**: `EthTrcvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 3. EthTrcvHwAccessLoopCount

- **UUID**: `98cd7391-47f7-46cb-803d-6c66e1a21027`
- **参数名**: `EthTrcvHwAccessLoopCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: On some platforms there is a additional waiting time required before the hardware access is possible. This waiting is implemented as busy waiting. The loop count can be configured using this parameter.

######## 4. EthTrcvCableDiagLoopCount

- **UUID**: `9e368639-465b-4331-805c-1b57ad3eafa3`
- **参数名**: `EthTrcvCableDiagLoopCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10000`
- **取值范围**: [0..4294967296]
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The cable diagnostic result can only be obtained after some waiting time. This parameter specifies the loop cycles the software performs until a timeout occurs.

####### BOOLEAN 类型参数

######## 1. EthTrcvDevErrorDetect

- **UUID**: `612d74b2-05e2-44c8-9b93-9eb3f7b0f576`
- **参数名**: `EthTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables development error detection.

######## 2. EthTrcvGetBaudRateApi

- **UUID**: `4c3a0e11-3309-4429-b47d-288903c5e4e5`
- **参数名**: `EthTrcvGetBaudRateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetBaudRate API

######## 3. EthTrcvGetDuplexModeApi

- **UUID**: `60d1cc58-9752-4687-a9bb-623b0a30369b`
- **参数名**: `EthTrcvGetDuplexModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetDuplexMode API

######## 4. EthTrcvGetLinkStateApi

- **UUID**: `09debea9-de31-42af-a1d5-1e5c571f3f59`
- **参数名**: `EthTrcvGetLinkStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetLinkState API

######## 5. EthTrcvGetTransceiverModeApi

- **UUID**: `dbb8cd04-6a3b-453f-b575-96cd2675ce9f`
- **参数名**: `EthTrcvGetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_GetTransceiverMode API

######## 6. EthTrcvSetTransceiverModeApi

- **UUID**: `4f8fd431-99d2-4193-bfd3-1aa95b3fa95a`
- **参数名**: `EthTrcvSetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_SetTransceiverMode API

######## 7. EthTrcvStartAutoNegotiationApi

- **UUID**: `d10ea345-dc0a-4035-b9c2-e19b77eaab15`
- **参数名**: `EthTrcvStartAutoNegotiationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables EthTrcv_StartAutoNegotiation API

######## 8. EthTrcvVersionInfoApi

- **UUID**: `6f524dd5-32b5-40d0-a902-1a650a5b1941`
- **参数名**: `EthTrcvVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API

######## 9. EthTrcvVersionInfoApiMacro

- **UUID**: `4c8a61bc-1fb4-478f-a31b-e26ae6d74959`
- **参数名**: `EthTrcvVersionInfoApiMacro`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If 'EthTrcvVersionInfoApiMacro' is enabled, macro will be used to get major, minor and patch version information.

RESTRICTIONS: 'EthTrcvVersionInfoApiMacro' is only available, if 'EthTrcvVersionInfoApi' is set to 'true'

(Vector spcific: not used)

######## 10. EthTrcvRuntimeMeasurementSupport

- **UUID**: `724812aa-74e4-4117-8b17-345cbe2b26c4`
- **参数名**: `EthTrcvRuntimeMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled runtime measurement points are added to the BSW module code and are added to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality.
Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

######## 11. EthTrcvGetTransceiverWakeupModeApi

- **UUID**: `81668c44-3190-4849-8e97-9e49a7335fbc`
- **参数名**: `EthTrcvGetTransceiverWakeupModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if the EthTrcv_GetTransceiverWakeupMode() API is enabled to get the current transceiver wakeup mode.

The API can only be used if EthTrcvWakeUpSupport is not configured to ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 12. EthTrcvSafeBswChecks

- **UUID**: `299998eb-87d3-42ef-9b29-f4989a51d3ee`
- **参数名**: `EthTrcvSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

######## 13. EthTrcvMacSecApi

- **UUID**: `4fe2f766-4b2b-4fd1-b855-328b4d674aef`
- **参数名**: `EthTrcvMacSecApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables the MACsec API

####### FLOAT 类型参数

######## 1. EthTrcvMainFunctionPeriod

- **UUID**: `1a889a69-cbe7-41dd-8afa-62248b212016`
- **参数名**: `EthTrcvMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the period the EthTrcv_MainFunction is called.

######## 2. EthTrcvMainFunctionMacSecPeriod

- **UUID**: `b5aef5cf-f701-43e3-92b2-f8c289fdad7f`
- **参数名**: `EthTrcvMainFunctionMacSecPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the period after which  the EthTrcv_MainFunctionMacSec is called.

####### STRING 类型参数

######## 1. EthTrcvUserConfigFile

- **UUID**: `a3073ba3-169f-4efd-8de7-0920a2fadc7f`
- **参数名**: `EthTrcvUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If a file path will be specified, the file is read and its contents are put at the end of the EthTrcv config file.

######## 2. EthTrcvWakeUpCalloutIncludeFiles

- **UUID**: `48e3bd65-2c45-4c3e-a79c-8a8f2645a3ea`
- **参数名**: `EthTrcvWakeUpCalloutIncludeFiles`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines include files for the declaration of wakeup callouts.

####### ENUMERATION 类型参数

######## 1. EthTrcvWakeUpSupport

- **UUID**: `9faed4e1-4eb6-4c39-9260-fc4edd93c59a`
- **参数名**: `EthTrcvWakeUpSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WAKEUP_NOT_SUPPORTED`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WAKEUP_BY_INTERRUPT` (来源: Vector Informatik)
  - `ETHTRCV_WAKEUP_BY_POLLING` (来源: Vector Informatik)
  - `ETHTRCV_WAKEUP_NOT_SUPPORTED` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the kinde of wakeup support the transceiver provides.

ETHTRCV_WAKEUP_BY_INTERRUPT:
Wakeup is realised through a interrupt triggered by Icu.

ETHTRCV_WAKEUP_BY_POLLING:
Wakeup is realised trough polling of EthTrcv_CheckWakeup() through EcuM.

ETHTRCV_WAKEUO_NOT_SUPPORTED:
Wakeup capability is either not supported by hardware/driver or is disabled.

##### 2. EthTrcvConfigSet

**容器属性**:

- **UUID**: `6d4ed8e3-2161-44f8-88c6-9e256bf531e1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfigSet`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

All underlying parameters may be part of a multiple configuration set.

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. EthTrcvConfig

**容器属性**:

- **UUID**: `eac2917b-ddc2-4380-8473-0fe1742ff3a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of the individual transceiver

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvIdx

- **UUID**: `0fb86327-a1df-4070-af3d-cb73f69a2f5e`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the instance ID of the configured transceiver.

########## 2. EthTrcvPhySignalQualityMeanValueLength

- **UUID**: `2ecb0058-decb-4b0a-b342-26f054ca1490`
- **参数名**: `EthTrcvPhySignalQualityMeanValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [1..1000]
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies how many consecutive data points of the phy's signal quality are used for the calculated mean value.

########## 3. EthTrcvSoftResetWaitCycles

- **UUID**: `c19066af-1c73-42c1-a87c-1c8213295bb1`
- **参数名**: `EthTrcvSoftResetWaitCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `120`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the wait time until a soft reset is performed. After soft reset the driver polls the transceiver register and checks that the reset is performed or not. This is the maximum wait time.

######### BOOLEAN 类型参数

########## 1. EthTrcvAutoNegotiationEnabled

- **UUID**: `69b1b429-a501-4a4e-abc6-02104e078502`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if Auto Negotiation is enabled or disabled for determination of the Ethernet Transceiver speed.

########## 2. EthTrcvSoftResetOnInit

- **UUID**: `0bfef0bf-23db-485e-8eba-d5087e8a8441`
- **参数名**: `EthTrcvSoftResetOnInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter speficies if a soft reset during transceiver initialization re-initializes all transceiver registers. In case the user sets some transceiver registers during runtime and wants to restore the default settings when transceiver is re-initialized, this option must be enabled.

######### ENUMERATION 类型参数

########## 1. EthTrcvSpeed

- **UUID**: `6688aae5-cd1d-44dd-a2f2-76c0bb9ae400`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TRCV_SPEED_100`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the speed of the Ethernet transceiver link in MBit/s.

RESTRICTION: If Auto Negotiation is enabled this is the maximum speed advertised for Auto-Negotiation

########## 2. EthTrcvWakeupInspectionType

- **UUID**: `de4b8981-cc9b-4b23-a783-59e7fd1c61f1`
- **参数名**: `EthTrcvWakeupInspectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ETHTRCV_ICU_CHANNEL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_ICU_CHANNEL` (来源: Vector Informatik)
  - `ETHTRCV_TRCV_REGISTERS` (来源: Vector Informatik)
  - `ETHTRCV_USER_CODE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the method used for inspection of wakeup events.

ETHTRCV_ICU_CHANNEL:
Uses the Icu_GetInputState() API for the related Icu channel to verify if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_TRCV_REGISTERS:
If hardware supports waking up by the transceiver itself the driver checks its registers if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_USER_CODE:
The user must provide integration code by itself for wakeup event inspection. This code must be embedded within the function EthTrcv_WakeupInspection generated into EthTrcv_Lcfg.c. For a more detailed information please refere to the Technical Reference of the driver.

########## 3. EthTrcvConnNeg

- **UUID**: `f3f2034e-0935-4bf6-b166-85968d40cdfb`
- **参数名**: `EthTrcvConnNeg`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_CONN_NEG_MANUAL`
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_CONN_NEG_AUTO` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_MASTER` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_SLAVE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the connection negotiation of the Ethernet transceiver link (Master/Slave or Auto Negotiation).

######### FUNCTION-NAME 类型参数

########## 1. EthTrcvWakeUpCallout

- **UUID**: `86e6aa1d-4d08-4cf2-9ea5-64aeca569801`
- **参数名**: `EthTrcvWakeUpCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies a callout function that is called during EthTrcv_SetTransceiverMode() for transceiver activation if a wakeup event has occured.

The callout can be used for e.g. initiating a remote wakeup of related ECUs by setting a activation line connected to them.
The function must be declared as followed:
void &lt;EthTrcvWakeUpCallout&gt;(uint8 TrcvIdx)

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. EthTrcvGenericDriverRef

- **UUID**: `44c51abb-bbbd-478d-8aee-1e001a325618`
- **引用名**: `EthTrcvGenericDriverRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthTrcvGenericDriver`
- **完整路径**: `/MICROSAR/EthTrcv_Generic/EthTrcv/EthTrcvConfigSet/EthTrcvGenericDriver`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an generic driver the transceiver instance is assigned to.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvIcuChannelRef

- **UUID**: `434cb20e-6996-41d8-aa4f-192716e3b09e`
- **引用名**: `EthTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Icu channel container.

The reference is used for enabling/disabling the wakeup notifications triggered by Icu in case EthTrcvWakeupSupport is configured to ETHTRCV_WAKEUP_BY_INTERRUPT.
Additionally the reference is used to check for a proper wakeup signal if the parameter EthTrcvWakeupVerificationType is set to ETHTRCV_ICU_CHANNEL.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `b9217833-76fa-47cf-820c-23a09a7fc693`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ETHTRCV_E_ACCESS

- **UUID**: `70bc3e2b-ad67-47e7-9f27-1c22c9188285`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

######### 2. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthTrcvMiiIdx

- **UUID**: `544e1640-88c9-45c3-ac33-597aaca4c2fb`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

########### ENUMERATION 类型参数

############ 1. EthTrcvMiiSelection

- **UUID**: `270183c4-3516-4cd1-8814-2885a4885c23`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MII`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MII` (来源: Vector Informatik)
  - `LIGHT_MII` (来源: Vector Informatik)
  - `RMII` (来源: Vector Informatik)
  - `GMII` (来源: Vector Informatik)
  - `RGMII` (来源: Vector Informatik)
  - `RMII_XTAL` (来源: Vector Informatik)
  - `RGMII_XTAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the type of transceiver/controller interface. The interface is either (G)MII, Light-MII or R(G)MII. In case of R(G)MII the refclock signal can be generated by the transceiver or applied externally. Choose R(G)MII_XTAL for transceiver clock generation and R(G)MII for an external clock. The interface must be selected according to your electric circuit design.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvCtrlRef

- **UUID**: `ffa90cf2-a083-4ac0-955a-be846beac3f6`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

######### 3. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvSwitchRef

- **UUID**: `31af7466-36c4-4c65-9417-c596c58106cf`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

############ 2. EthTrcvSwitchPortRef

- **UUID**: `6c30f214-8a8e-462d-bff1-2cc3b1a6c921`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

######### 4. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `68779b17-4ed9-41e1-9750-5633f93a47d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvCtrlRef

- **UUID**: `ec5d2e41-d061-4185-9701-d8f328722bb2`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

######### 5. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `73986fee-731c-445f-aedc-a42fc392adca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **构建后可变**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthTrcvWakeupReason

- **UUID**: `8310eb21-7505-44a8-8837-49cebef41f6f`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: Vector Informatik)
  - `ETHTRCV_WUR_GENERAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_INTERNAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_PIN` (来源: Vector Informatik)
  - `ETHTRCV_WUR_POWER_ON` (来源: Vector Informatik)
  - `ETHTRCV_WUR_RESET` (来源: Vector Informatik)
  - `ETHTRCV_WUR_SYSERR` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the corresponding wakeup reason mapped to the wakeup source of the EcuM.

ETHTRCV_WUR_BUS:
Reason for the wakeup is a event on the Ethernet network.

ETHTRCV_WUR_GENERAL:
Reason for the wakeup is a general event.

ETHTRCV_WUR_INTERNAL:
Reason for the wakeup is a internal transceiver event.

ETHTRCV_WUR_PIN:
Reason for the wakeup is a event on the related Icu channel.

ETHTRCV_WUR_POWER_ON:
Reason for the wakeup is the power on of the ECU.

ETHTRCV_WUR_RESET:
Reason for the wakeup is the reset of the ECU.

ETHTRCV_WUR_SYSERR:
Reason for the wakeup is a system error.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvWakeupSourceRef

- **UUID**: `dc11b9c7-0a70-4599-952e-69e0fd6e1beb`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

######### 6. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `0e1fb533-e77e-4ee3-be30-3b5c8d085ca4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `68779b17-4ed9-41e1-9750-5633f93a47d4`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

####### 2. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `b9217833-76fa-47cf-820c-23a09a7fc693`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `70bc3e2b-ad67-47e7-9f27-1c22c9188285`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

####### 3. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvMiiIdx

- **UUID**: `544e1640-88c9-45c3-ac33-597aaca4c2fb`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `270183c4-3516-4cd1-8814-2885a4885c23`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MII`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MII` (来源: Vector Informatik)
  - `LIGHT_MII` (来源: Vector Informatik)
  - `RMII` (来源: Vector Informatik)
  - `GMII` (来源: Vector Informatik)
  - `RGMII` (来源: Vector Informatik)
  - `RMII_XTAL` (来源: Vector Informatik)
  - `RGMII_XTAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the type of transceiver/controller interface. The interface is either (G)MII, Light-MII or R(G)MII. In case of R(G)MII the refclock signal can be generated by the transceiver or applied externally. Choose R(G)MII_XTAL for transceiver clock generation and R(G)MII for an external clock. The interface must be selected according to your electric circuit design.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `ffa90cf2-a083-4ac0-955a-be846beac3f6`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

####### 4. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvSwitchRef

- **UUID**: `31af7466-36c4-4c65-9417-c596c58106cf`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

########## 2. EthTrcvSwitchPortRef

- **UUID**: `6c30f214-8a8e-462d-bff1-2cc3b1a6c921`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

####### 5. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `68779b17-4ed9-41e1-9750-5633f93a47d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `ec5d2e41-d061-4185-9701-d8f328722bb2`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

####### 6. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `73986fee-731c-445f-aedc-a42fc392adca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **构建后可变**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvWakeupReason

- **UUID**: `8310eb21-7505-44a8-8837-49cebef41f6f`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: Vector Informatik)
  - `ETHTRCV_WUR_GENERAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_INTERNAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_PIN` (来源: Vector Informatik)
  - `ETHTRCV_WUR_POWER_ON` (来源: Vector Informatik)
  - `ETHTRCV_WUR_RESET` (来源: Vector Informatik)
  - `ETHTRCV_WUR_SYSERR` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the corresponding wakeup reason mapped to the wakeup source of the EcuM.

ETHTRCV_WUR_BUS:
Reason for the wakeup is a event on the Ethernet network.

ETHTRCV_WUR_GENERAL:
Reason for the wakeup is a general event.

ETHTRCV_WUR_INTERNAL:
Reason for the wakeup is a internal transceiver event.

ETHTRCV_WUR_PIN:
Reason for the wakeup is a event on the related Icu channel.

ETHTRCV_WUR_POWER_ON:
Reason for the wakeup is the power on of the ECU.

ETHTRCV_WUR_RESET:
Reason for the wakeup is the reset of the ECU.

ETHTRCV_WUR_SYSERR:
Reason for the wakeup is a system error.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvWakeupSourceRef

- **UUID**: `dc11b9c7-0a70-4599-952e-69e0fd6e1beb`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

####### 7. EthTrcvGenericDriver

**容器属性**:

- **UUID**: `ff877905-3107-4ee3-b3e3-f72b2335f4f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvGenericDriver`
- **多重性**: [1..infinite]
- **构建后可变**: false

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvGenericDriverVendorId

- **UUID**: `349a0470-ef83-46d2-9fa8-f9049f1f52a4`
- **参数名**: `EthTrcvGenericDriverVendorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the Vendor ID used for the API infixing of the drivers AUTOSAR API.

Example:
The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().

######### LINKER-SYMBOL 类型参数

########## 1. EthTrcvGenericDriverName

- **UUID**: `41c207ff-2c6f-4aee-933a-bcca022f6af5`
- **参数名**: `EthTrcvGenericDriverName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Gen`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier used for the API infixing of the drivers AUTOSAR API.

Example:
The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().

####### 8. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `0e1fb533-e77e-4ee3-be30-3b5c8d085ca4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `68779b17-4ed9-41e1-9750-5633f93a47d4`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

##### 3. EthTrcvConfig

**容器属性**:

- **UUID**: `eac2917b-ddc2-4380-8473-0fe1742ff3a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **构建后可变**: false

**容器描述**:

Configuration of the individual transceiver

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvIdx

- **UUID**: `0fb86327-a1df-4070-af3d-cb73f69a2f5e`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the instance ID of the configured transceiver.

######## 2. EthTrcvPhySignalQualityMeanValueLength

- **UUID**: `2ecb0058-decb-4b0a-b342-26f054ca1490`
- **参数名**: `EthTrcvPhySignalQualityMeanValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [1..1000]
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies how many consecutive data points of the phy's signal quality are used for the calculated mean value.

######## 3. EthTrcvSoftResetWaitCycles

- **UUID**: `c19066af-1c73-42c1-a87c-1c8213295bb1`
- **参数名**: `EthTrcvSoftResetWaitCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `120`
- **取值范围**: [1..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the wait time until a soft reset is performed. After soft reset the driver polls the transceiver register and checks that the reset is performed or not. This is the maximum wait time.

####### BOOLEAN 类型参数

######## 1. EthTrcvAutoNegotiationEnabled

- **UUID**: `69b1b429-a501-4a4e-abc6-02104e078502`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies if Auto Negotiation is enabled or disabled for determination of the Ethernet Transceiver speed.

######## 2. EthTrcvSoftResetOnInit

- **UUID**: `0bfef0bf-23db-485e-8eba-d5087e8a8441`
- **参数名**: `EthTrcvSoftResetOnInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter speficies if a soft reset during transceiver initialization re-initializes all transceiver registers. In case the user sets some transceiver registers during runtime and wants to restore the default settings when transceiver is re-initialized, this option must be enabled.

####### ENUMERATION 类型参数

######## 1. EthTrcvSpeed

- **UUID**: `6688aae5-cd1d-44dd-a2f2-76c0bb9ae400`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TRCV_SPEED_100`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the speed of the Ethernet transceiver link in MBit/s.

RESTRICTION: If Auto Negotiation is enabled this is the maximum speed advertised for Auto-Negotiation

######## 2. EthTrcvWakeupInspectionType

- **UUID**: `de4b8981-cc9b-4b23-a783-59e7fd1c61f1`
- **参数名**: `EthTrcvWakeupInspectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ETHTRCV_ICU_CHANNEL`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_ICU_CHANNEL` (来源: Vector Informatik)
  - `ETHTRCV_TRCV_REGISTERS` (来源: Vector Informatik)
  - `ETHTRCV_USER_CODE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the method used for inspection of wakeup events.

ETHTRCV_ICU_CHANNEL:
Uses the Icu_GetInputState() API for the related Icu channel to verify if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_TRCV_REGISTERS:
If hardware supports waking up by the transceiver itself the driver checks its registers if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_USER_CODE:
The user must provide integration code by itself for wakeup event inspection. This code must be embedded within the function EthTrcv_WakeupInspection generated into EthTrcv_Lcfg.c. For a more detailed information please refere to the Technical Reference of the driver.

######## 3. EthTrcvConnNeg

- **UUID**: `f3f2034e-0935-4bf6-b166-85968d40cdfb`
- **参数名**: `EthTrcvConnNeg`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_CONN_NEG_MANUAL`
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_CONN_NEG_AUTO` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_MASTER` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_SLAVE` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the connection negotiation of the Ethernet transceiver link (Master/Slave or Auto Negotiation).

####### FUNCTION-NAME 类型参数

######## 1. EthTrcvWakeUpCallout

- **UUID**: `86e6aa1d-4d08-4cf2-9ea5-64aeca569801`
- **参数名**: `EthTrcvWakeUpCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies a callout function that is called during EthTrcv_SetTransceiverMode() for transceiver activation if a wakeup event has occured.

The callout can be used for e.g. initiating a remote wakeup of related ECUs by setting a activation line connected to them.
The function must be declared as followed:
void &lt;EthTrcvWakeUpCallout&gt;(uint8 TrcvIdx)

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. EthTrcvGenericDriverRef

- **UUID**: `44c51abb-bbbd-478d-8aee-1e001a325618`
- **引用名**: `EthTrcvGenericDriverRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthTrcvGenericDriver`
- **完整路径**: `/MICROSAR/EthTrcv_Generic/EthTrcv/EthTrcvConfigSet/EthTrcvGenericDriver`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an generic driver the transceiver instance is assigned to.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvIcuChannelRef

- **UUID**: `434cb20e-6996-41d8-aa4f-192716e3b09e`
- **引用名**: `EthTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Icu channel container.

The reference is used for enabling/disabling the wakeup notifications triggered by Icu in case EthTrcvWakeupSupport is configured to ETHTRCV_WAKEUP_BY_INTERRUPT.
Additionally the reference is used to check for a proper wakeup signal if the parameter EthTrcvWakeupVerificationType is set to ETHTRCV_ICU_CHANNEL.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `b9217833-76fa-47cf-820c-23a09a7fc693`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `70bc3e2b-ad67-47e7-9f27-1c22c9188285`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

####### 2. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvMiiIdx

- **UUID**: `544e1640-88c9-45c3-ac33-597aaca4c2fb`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `270183c4-3516-4cd1-8814-2885a4885c23`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MII`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MII` (来源: Vector Informatik)
  - `LIGHT_MII` (来源: Vector Informatik)
  - `RMII` (来源: Vector Informatik)
  - `GMII` (来源: Vector Informatik)
  - `RGMII` (来源: Vector Informatik)
  - `RMII_XTAL` (来源: Vector Informatik)
  - `RGMII_XTAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the type of transceiver/controller interface. The interface is either (G)MII, Light-MII or R(G)MII. In case of R(G)MII the refclock signal can be generated by the transceiver or applied externally. Choose R(G)MII_XTAL for transceiver clock generation and R(G)MII for an external clock. The interface must be selected according to your electric circuit design.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `ffa90cf2-a083-4ac0-955a-be846beac3f6`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

####### 3. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvSwitchRef

- **UUID**: `31af7466-36c4-4c65-9417-c596c58106cf`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

########## 2. EthTrcvSwitchPortRef

- **UUID**: `6c30f214-8a8e-462d-bff1-2cc3b1a6c921`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

####### 4. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `68779b17-4ed9-41e1-9750-5633f93a47d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `ec5d2e41-d061-4185-9701-d8f328722bb2`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

####### 5. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `73986fee-731c-445f-aedc-a42fc392adca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **构建后可变**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvWakeupReason

- **UUID**: `8310eb21-7505-44a8-8837-49cebef41f6f`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: Vector Informatik)
  - `ETHTRCV_WUR_GENERAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_INTERNAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_PIN` (来源: Vector Informatik)
  - `ETHTRCV_WUR_POWER_ON` (来源: Vector Informatik)
  - `ETHTRCV_WUR_RESET` (来源: Vector Informatik)
  - `ETHTRCV_WUR_SYSERR` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the corresponding wakeup reason mapped to the wakeup source of the EcuM.

ETHTRCV_WUR_BUS:
Reason for the wakeup is a event on the Ethernet network.

ETHTRCV_WUR_GENERAL:
Reason for the wakeup is a general event.

ETHTRCV_WUR_INTERNAL:
Reason for the wakeup is a internal transceiver event.

ETHTRCV_WUR_PIN:
Reason for the wakeup is a event on the related Icu channel.

ETHTRCV_WUR_POWER_ON:
Reason for the wakeup is the power on of the ECU.

ETHTRCV_WUR_RESET:
Reason for the wakeup is the reset of the ECU.

ETHTRCV_WUR_SYSERR:
Reason for the wakeup is a system error.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvWakeupSourceRef

- **UUID**: `dc11b9c7-0a70-4599-952e-69e0fd6e1beb`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

####### 6. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `0e1fb533-e77e-4ee3-be30-3b5c8d085ca4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `68779b17-4ed9-41e1-9750-5633f93a47d4`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

##### 4. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `b9217833-76fa-47cf-820c-23a09a7fc693`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHTRCV_E_ACCESS

- **UUID**: `70bc3e2b-ad67-47e7-9f27-1c22c9188285`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

##### 5. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvMiiIdx

- **UUID**: `544e1640-88c9-45c3-ac33-597aaca4c2fb`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

####### ENUMERATION 类型参数

######## 1. EthTrcvMiiSelection

- **UUID**: `270183c4-3516-4cd1-8814-2885a4885c23`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `MII`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `MII` (来源: Vector Informatik)
  - `LIGHT_MII` (来源: Vector Informatik)
  - `RMII` (来源: Vector Informatik)
  - `GMII` (来源: Vector Informatik)
  - `RGMII` (来源: Vector Informatik)
  - `RMII_XTAL` (来源: Vector Informatik)
  - `RGMII_XTAL` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the type of transceiver/controller interface. The interface is either (G)MII, Light-MII or R(G)MII. In case of R(G)MII the refclock signal can be generated by the transceiver or applied externally. Choose R(G)MII_XTAL for transceiver clock generation and R(G)MII for an external clock. The interface must be selected according to your electric circuit design.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvCtrlRef

- **UUID**: `ffa90cf2-a083-4ac0-955a-be846beac3f6`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

##### 6. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **构建后可变**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvSwitchRef

- **UUID**: `31af7466-36c4-4c65-9417-c596c58106cf`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

######## 2. EthTrcvSwitchPortRef

- **UUID**: `6c30f214-8a8e-462d-bff1-2cc3b1a6c921`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

##### 7. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `68779b17-4ed9-41e1-9750-5633f93a47d4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **构建后可变**: false

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvCtrlRef

- **UUID**: `ec5d2e41-d061-4185-9701-d8f328722bb2`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a physical Ethernet controller configuration.

##### 8. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `73986fee-731c-445f-aedc-a42fc392adca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **构建后可变**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EthTrcvWakeupReason

- **UUID**: `8310eb21-7505-44a8-8837-49cebef41f6f`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: Vector Informatik)
  - `ETHTRCV_WUR_GENERAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_INTERNAL` (来源: Vector Informatik)
  - `ETHTRCV_WUR_PIN` (来源: Vector Informatik)
  - `ETHTRCV_WUR_POWER_ON` (来源: Vector Informatik)
  - `ETHTRCV_WUR_RESET` (来源: Vector Informatik)
  - `ETHTRCV_WUR_SYSERR` (来源: Vector Informatik)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies the corresponding wakeup reason mapped to the wakeup source of the EcuM.

ETHTRCV_WUR_BUS:
Reason for the wakeup is a event on the Ethernet network.

ETHTRCV_WUR_GENERAL:
Reason for the wakeup is a general event.

ETHTRCV_WUR_INTERNAL:
Reason for the wakeup is a internal transceiver event.

ETHTRCV_WUR_PIN:
Reason for the wakeup is a event on the related Icu channel.

ETHTRCV_WUR_POWER_ON:
Reason for the wakeup is the power on of the ECU.

ETHTRCV_WUR_RESET:
Reason for the wakeup is the reset of the ECU.

ETHTRCV_WUR_SYSERR:
Reason for the wakeup is a system error.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvWakeupSourceRef

- **UUID**: `dc11b9c7-0a70-4599-952e-69e0fd6e1beb`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

##### 9. EthTrcvGenericDriver

**容器属性**:

- **UUID**: `ff877905-3107-4ee3-b3e3-f72b2335f4f8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvGenericDriver`
- **多重性**: [1..infinite]
- **构建后可变**: false

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvGenericDriverVendorId

- **UUID**: `349a0470-ef83-46d2-9fa8-f9049f1f52a4`
- **参数名**: `EthTrcvGenericDriverVendorId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `30`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the Vendor ID used for the API infixing of the drivers AUTOSAR API.

Example:
The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().

####### LINKER-SYMBOL 类型参数

######## 1. EthTrcvGenericDriverName

- **UUID**: `41c207ff-2c6f-4aee-933a-bcca022f6af5`
- **参数名**: `EthTrcvGenericDriverName`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `Gen`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies the identifier used for the API infixing of the drivers AUTOSAR API.

Example:
The EthTrcv_Init() API will be generated as EthTrcv_<Vendor ID>_<Driver Name>_Init().

##### 10. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `0e1fb533-e77e-4ee3-be30-3b5c8d085ca4`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **构建后可变**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `12b07fc7-0442-4c4c-aa20-71a9d991445f`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `6a816382-40ea-4a8f-b808-a1139a01cfd2`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `68779b17-4ed9-41e1-9750-5633f93a47d4`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. EthTrcv_Generic

- **UUID**: `4ee0956d-7aae-4d40-8ef9-2f12345a1a92`
- **包名称**: `EthTrcv_Generic`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **EthTrcv**

##### BSW-IMPLEMENTATION 类型元素

1. **EthTrcv_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **EthTrcv_Pre**
2. **EthTrcv_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. EthTrcv_Impl

- **UUID**: `84149ffe-2633-4857-99eb-738748f33fce`
- **实现名称**: `EthTrcv_Impl`
- **编程语言**: C
- **软件版本**: 3.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.01.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. EthTrcv_Pre

- **UUID**: `ddedb1dc-bbcb-43ba-906d-47418e48ee80`
- **配置名称**: `EthTrcv_Pre`
- **定义引用**: `/MICROSAR/EthTrcv_Generic/EthTrcv`

### 2. EthTrcv_Rec

- **UUID**: `2d7f90f2-ca50-4d53-8d1d-d0fe88f00362`
- **配置名称**: `EthTrcv_Rec`
- **定义引用**: `/MICROSAR/EthTrcv_Generic/EthTrcv`
