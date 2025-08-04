# EthTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:05

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthTrcv](#ethtrcv)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-1.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthTrcv

#### 基本信息

- **UUID**: `3711f01f-04cd-46dc-82b2-387d244992b0`
- **模块名称**: `EthTrcv`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the EthTrcv (Ethernet Transceiver driver) module.

#### 版本历史

共有 **5** 个版本记录：

##### 1. 版本 01.00.00

- **状态**: beta
- **发布日期**: 2011-09-26T09:43:19Z
- **发布者**: visfer

**变更内容**:

##### 2. 版本 01.01.00

- **状态**: beta
- **发布日期**: 2015-02-13T04:05:21+01:00
- **发布者**: vismha

**变更内容**:

##### 3. 版本 02.00.00

- **发布日期**: 2018-11-28T18:09:56+01:00
- **发布者**: visdrr

**变更内容**:

##### 4. 版本 03.00.00

- **发布日期**: 2019-09-13T14:26:26+02:00
- **发布者**: viskha

**变更内容**:

##### 5. 版本 03.00.01

- **发布日期**: 2020-05-13T09:12:53+02:00
- **发布者**: visdrr

**变更内容**:

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. EthTrcvGeneral

**容器属性**:

- **UUID**: `50c8237b-875d-48d6-bd0b-50f164f4a63f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

General configuration of Ethernet Transceiver Driver module.

###### 参数配置

此容器包含 **27** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvMaxTrcvsSupported

- **UUID**: `e1a1d6f0-672d-4a8a-9c46-e4ec50761c91`
- **参数名**: `EthTrcvMaxTrcvsSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the maximum number of transceiver configurations per transceiver driver.

######## 2. EthTrcvIndex

- **UUID**: `0cfac830-ec01-4fd1-93b9-4af6197718ee`
- **参数名**: `EthTrcvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 3. EthTrcvCableDiagLoopCount

- **UUID**: `89f892a9-ed9c-49ff-8925-d8a7936d52fa`
- **参数名**: `EthTrcvCableDiagLoopCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `10000`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: The cable diagnostic result can only be obtained after some waiting time. This parameter specifies the loop cycles the software performs until a timeout occurs.

######## 4. EthTrcvHwAccessLoopCount

- **UUID**: `2ff231fd-f76f-4550-886e-ae5e958289f3`
- **参数名**: `EthTrcvHwAccessLoopCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967296]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: On some platforms there is a additional waiting time required before the hardware access is possible. This waiting is implemented as busy waiting. The loop count can be configured using this parameter.

######## 5. EthTrcvHwAccessMonitorFailureDebounceValue

- **UUID**: `6913f43c-126f-4b87-975e-ff1217264a0f`
- **参数名**: `EthTrcvHwAccessMonitorFailureDebounceValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the hardware access failure debounce counter value limit. Once the limit is reached, the error reaction is triggered after a hardware access failure was detected by the hardware access monitor. If the limit is not reached and the condition of the hardware access remains in the failed state, the counter is incremented. The minimum value for the limit is 0 which means no debouncing, The maximum value is 255.

######## 6. EthTrcvHwAccessMonitorRecoveryDebounceValue

- **UUID**: `302d9b87-a447-468a-8138-2ccfab2dea79`
- **参数名**: `EthTrcvHwAccessMonitorRecoveryDebounceValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the hardware access recovery debounce counter value limit. Once the limit is reached, the reaction is triggered after a hardware access recovery was detected by the hardware access monitor. If the limit is not reached and the condition of the hardware access remains in the unfailed state, the counter is incremented. The minimum value for the limit is 0 which means no debouncing, The maximum value is 255.

####### BOOLEAN 类型参数

######## 1. EthTrcvGetBaudRateApi

- **UUID**: `553b5318-4af5-459a-bf13-828d44b069f7`
- **参数名**: `EthTrcvGetBaudRateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_GetBaudRate() API is enabled to get the current transceiver baud rate.

######## 2. EthTrcvGetDuplexModeApi

- **UUID**: `d14c7d54-2e49-4780-a9e8-a2aae08541c5`
- **参数名**: `EthTrcvGetDuplexModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_GetDuplexMode() API is enabled to get the current transceiver duplex mode.

######## 3. EthTrcvGetLinkStateApi

- **UUID**: `4cdea9cc-6911-41c4-ba57-8e05304f9e30`
- **参数名**: `EthTrcvGetLinkStateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_GetLinkState() API is enbled to get the current transceiver link state.

######## 4. EthTrcvGetTransceiverModeApi

- **UUID**: `6601814f-0163-4d5d-a577-f79ec74c23a3`
- **参数名**: `EthTrcvGetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_GetTransceiverMode() API is enabled to get the current transceiver mode.

######## 5. EthTrcvSetTransceiverModeApi

- **UUID**: `441bf6d2-e2d1-4003-a732-a3fa6361bf7f`
- **参数名**: `EthTrcvSetTransceiverModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_SetTransceiverMode() API is enabled to set the transceiver mode.

######## 6. EthTrcvStartAutoNegotiationApi

- **UUID**: `56a73ef9-e4fd-4115-b111-66d8ca640460`
- **参数名**: `EthTrcvStartAutoNegotiationApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_StartAutoNegotiation() is enabled to start the transceiver auto negotiation.

######## 7. EthTrcvVersionInfoApi

- **UUID**: `4f9369d3-bfb6-4e17-b919-869d230afd24`
- **参数名**: `EthTrcvVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter enables/disables the function EthTrcv_GetVersionInfo() to get major, minor and patch version information.

######## 8. EthTrcvRuntimeMeasurementSupport

- **UUID**: `26d126dd-b10a-4c4d-916d-f1489ae57006`
- **参数名**: `EthTrcvRuntimeMeasurementSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: If enabled runtime measurement points are added to the BSW module code and are added to the module configuration of MICROSAR RTM. The available measurement points can be seen and configured in the RTM module configuration. Availability of the MICROSAR RTM module is a prerequisite to make use of the runtime measurement functionality.
Runtime measurement should be disabled in production code as measurement points may inflict additional runtime.

######## 9. EthTrcvGetTransceiverWakeupModeApi

- **UUID**: `a0581213-aa00-41fc-b69d-e37e41736a31`
- **参数名**: `EthTrcvGetTransceiverWakeupModeApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines if the EthTrcv_GetTransceiverWakeupMode() API is enabled to get the current transceiver wakeup mode.

The API can only be used if EthTrcvWakeUpSupport is not configured to ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 10. EthTrcvDevErrorDetect

- **UUID**: `5a372686-17a4-45f0-80a8-30af680082ff`
- **参数名**: `EthTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Enables / Disables development error detection.

######## 11. EthTrcvSafeBswChecks

- **UUID**: `6bb6c283-438c-43aa-9934-37a76ec75f72`
- **参数名**: `EthTrcvSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. EthTrcvMainFunctionLinkHandlingPeriod

- **UUID**: `4fe74c48-d149-45ea-b759-10ceeda74795`
- **参数名**: `EthTrcvMainFunctionLinkHandlingPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.001`
- **取值范围**: [0.001..0.02]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the period the function for link handling is called.

######## 2. EthTrcvMainFunctionPeriod

- **UUID**: `5acce71e-82b7-413c-ae0f-421340235557`
- **参数名**: `EthTrcvMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.02`
- **取值范围**: [0.001..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the period the EthTrcv_MainFunction is called.

######## 3. EthTrcvHwAccessMonitorPeriod

- **UUID**: `300ffc23-3377-4dc6-9763-ac5f97489c86`
- **参数名**: `EthTrcvHwAccessMonitorPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.001`
- **取值范围**: [0.001..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the cyclical period time the hardware access monitor checks the accessibility of the hardware.

######## 4. EthTrcvWakeUpReasonPeriod

- **UUID**: `b19953af-838d-49bc-87ee-bb46a002ac54`
- **参数名**: `EthTrcvWakeUpReasonPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.001`
- **取值范围**: [0.001..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This is the cyclical period time the wake up reason check is performed, if EthTrcvWakeUpSupport is configured to POLLING.

####### STRING 类型参数

######## 1. EthTrcvUserConfigFile

- **UUID**: `38716dba-3102-448c-9bab-46a354fa07a2`
- **参数名**: `EthTrcvUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external text file that will be included during generation to EthTrcv_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.

Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 2. EthTrcvCalloutIncludeFiles

- **UUID**: `5027cfa3-ef4f-41ad-8c19-ba108e14b7f1`
- **参数名**: `EthTrcvCalloutIncludeFiles`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines include files for the declaration of callouts, i.e. Pre- and Post-TransceiverInit-Callout, WakeUpCallout, WakeUpInspectionCallout,...

####### ENUMERATION 类型参数

######## 1. EthTrcvWakeUpSupport

- **UUID**: `58aedd03-8f6d-40cd-816e-0967cb24b373`
- **参数名**: `EthTrcvWakeUpSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WAKEUP_NOT_SUPPORTED`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WAKEUP_BY_INTERRUPT` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WAKEUP_BY_POLLING` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WAKEUP_NOT_SUPPORTED` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies the kinde of wakeup support the transceiver provides.

ETHTRCV_WAKEUP_BY_INTERRUPT:
Wakeup is realised through a interrupt triggered by Icu.

ETHTRCV_WAKEUP_BY_POLLING:
Wakeup is realised trough polling of EthTrcv_CheckWakeup() through EcuM.

ETHTRCV_WAKEUO_NOT_SUPPORTED:
Wakeup capability is either not supported by hardware/driver or is disabled.

####### LINKER-SYMBOL 类型参数

######## 1. EthTrcvPreTrcvInitUserCallout

- **UUID**: `6c6424b5-da22-4593-b1be-c5474c7e4ac6`
- **参数名**: `EthTrcvPreTrcvInitUserCallout`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter defines the function to be called before the driver initializes a Ethernet transceiver.

The function that is provided here has to have following signature:
void <User>_PreTrcvInitCallout(uint8 EthTrcvIdx);

NULL_PTR as value disables the functionality.

With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet Transceiver, one can distinguish between the initialization context that is currently executed.

######## 2. EthTrcvPostTrcvInitUserCallout

- **UUID**: `e214c8af-dc7e-48a0-9b17-51286764fb0b`
- **参数名**: `EthTrcvPostTrcvInitUserCallout`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter defines the function to be called after the driver has initialized a Ethernet transceiver.

The function that is provided here has to have following signature:
void <User>_PostTrcvInitCallout(uint8 EthTrcvIdx);

NULL_PTR as value disables the functionality.

With the passed EthTrcvIdx, representing the Symbolic Name Value of the respective Ethernet Transceiver, one can distinguish between the initialization context that is currently executed.

######## 3. EthTrcvHwAccessMonitorFailureUserCallout

- **UUID**: `6333295e-3608-40cb-b600-97ba79799e87`
- **参数名**: `EthTrcvHwAccessMonitorFailureUserCallout`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [1..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **字符串变体**:
  - 默认值: `NULL_PTR`
- **描述**: This parameter defines a user callout which is called in case a hardware access failure is detected by the hardware access monitor.

##### 2. EthTrcvConfigSet

**容器属性**:

- **UUID**: `2959c22e-05f8-431f-b318-04d5df180be0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfigSet`
- **多重性**: [1..1]
- **需要索引**: false
- **多配置容器**: false

**容器描述**:

This conainter includes multiple configuration set containers.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. EthTrcvConfig

**容器属性**:

- **UUID**: `08e5c37f-0d70-4e2e-8a61-098ff1571f81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes the configuration of the individual transceiver.

######## 参数配置

此容器包含 **10** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvIdx

- **UUID**: `9c306c41-0fe6-4d22-98ac-258ad4dcc259`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This value specifies the instance ID of the configured transceiver.

########## 2. EthTrcvPhySignalQualityMeanValueLength

- **UUID**: `9424ac19-78c6-4d74-b638-ef9f3e8ded82`
- **参数名**: `EthTrcvPhySignalQualityMeanValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [1..1000]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies how many consecutive data points of the phy's signal quality are used for the calculated mean value.

########## 3. EthTrcvSoftResetWaitCycles

- **UUID**: `0818f81f-f7ca-49bd-a97a-b8f378f2074e`
- **参数名**: `EthTrcvSoftResetWaitCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `120`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the wait time until a soft reset is performed. After soft reset the driver polls the transceiver register and checks that the reset is performed or not. This is the maximum wait time.

######### BOOLEAN 类型参数

########## 1. EthTrcvSoftResetOnInit

- **UUID**: `a53fcbb2-8528-4e11-8527-4967bf72a42e`
- **参数名**: `EthTrcvSoftResetOnInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter speficies if a soft reset during transceiver initialization re-initializes all transceiver registers. In case the user sets some transceiver registers during runtime and wants to restore the default settings when transceiver is re-initialized, this option must be enabled.

########## 2. EthTrcvAutoNegotiationEnabled

- **UUID**: `82e27dbf-ecf4-4afa-bc6c-e9ac8d63705b`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the Ethernet transceiver speed.
Note: Since on 88Q1010, the setting of the transceiver speed is not available (only 100 Mbit/s supported), This settings is not enabled and the speed set to default 100Mbit/s

######### ENUMERATION 类型参数

########## 1. EthTrcvSpeed

- **UUID**: `de13e1e5-a34e-4215-951f-7c435c1b20e5`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TRCV_SPEED_100`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies the speed of the Ethernet transceiver link in MBit/s.

RESTRICTION: If Auto Negotiation is enabled this is the maximum speed advertised for Auto-Negotiation

########## 2. EthTrcvWakeupInspectionType

- **UUID**: `d530a5d8-1c0e-4e91-aabc-0571a90ebd76`
- **参数名**: `EthTrcvWakeupInspectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ETHTRCV_ICU_CHANNEL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_ICU_CHANNEL` (来源: Vector Informatik)
  - `ETHTRCV_TRCV_REGISTERS` (来源: Vector Informatik)
  - `ETHTRCV_USER_CODE` (来源: Vector Informatik)
- **描述**: This parameter specifies the method used for inspection of wakeup events.

ETHTRCV_ICU_CHANNEL:
Uses the Icu_GetInputState() API for the related Icu channel to verify if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_TRCV_REGISTERS:
If hardware supports waking up by the transceiver itself the driver checks its registers if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_USER_CODE:
The user must provide integration code by itself for wakeup event inspection. This code must be embedded within the function EthTrcv_WakeupInspection generated into EthTrcv_Lcfg.c. For a more detailed information please refere to the Technical Reference of the driver.

########## 3. EthTrcvConnNeg

- **UUID**: `11a530df-5836-42b6-a061-404da14a2865`
- **参数名**: `EthTrcvConnNeg`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_CONN_NEG_MASTER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_CONN_NEG_MASTER` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_SLAVE` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_AUTO` (来源: Vector Informatik)
- **描述**: This parameter specifies the connection negotiation of the Ethernet transceiver link.
Note: The ETHTRCV_CONN_NEG_AUTO setting affects the auto-negotiation mode of negotiation. This setting enables the auto negotiation with prefered mode and not advertised.

######### FUNCTION-NAME 类型参数

########## 1. EthTrcvWakeUpCallout

- **UUID**: `e48ca860-3a73-40cd-af2d-22886eb3d88e`
- **参数名**: `EthTrcvWakeUpCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies a callout function that is called during EthTrcv_SetTransceiverMode() for transceiver activation if a wakeup event has occured.

The callout can be used for e.g. initiating a remote wakeup of related ECUs by setting a activation line connected to them.
The function must be declared as followed:
void &lt;EthTrcvWakeUpCallout&gt;(uint8 TrcvIdx)

########## 2. EthTrcvWakeUpInspectionCallout

- **UUID**: `feedb40e-8a11-42df-a1f5-1a68b01d4053`
- **参数名**: `EthTrcvWakeUpInspectionCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies a callout function that is called if the Wakeup Inspection Type is set to "ETHTRCV_USER_CODE".

The callout can be used to realize a user-defined wake-up inspection and reporting.
 
The function must be declared as follows:
void &lt;EthTrcvWakeUpInspectionCallout&gt;(uint8 TrcvIdx)

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvIcuChannelRef

- **UUID**: `936e9bb4-fa9b-4617-85eb-c6629db4a42f`
- **引用名**: `EthTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a Icu channel container.

The reference is used for enabling/disabling the wakeup notifications triggered by Icu in case EthTrcvWakeupSupport is configured to ETHTRCV_WAKEUP_BY_INTERRUPT.
Additionally the reference is used to check for a proper wakeup signal if the parameter EthTrcvWakeupVerificationType is set to ETHTRCV_ICU_CHANNEL.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `d879c8ff-568a-4fd2-b313-edd7a8802637`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ETHTRCV_E_ACCESS

- **UUID**: `034c735c-38ce-494a-89b5-6b06d8349df5`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

######### 2. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. EthTrcvMiiIdx

- **UUID**: `a0eab56b-a1aa-4db6-8e8e-3f65545e9398`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

########### ENUMERATION 类型参数

############ 1. EthTrcvMiiSelection

- **UUID**: `0487db83-5d43-477d-9178-1532d78bd618`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_STRAPPING_CONFIG_ONLY`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_STRAPPING_CONFIG_ONLY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvCtrlRef

- **UUID**: `20aaa534-3c96-4404-b5b8-c35eb83436b1`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

######### 3. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `aa176d1c-219f-4780-b6fc-52673848df79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthTrcvMiiSelection

- **UUID**: `3c791576-7412-48ea-9067-f6e0a8388d1f`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_MII_MODE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_MII_MODE` (来源: Vector Informatik)
  - `ETHTRCV_INTERNAL_PHY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface.  In case the configured element is an intenal PHY choose INTERNAL PHY, in case it is an external PHY managed by a switch the interface must be selected. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

########## 引用关系

此容器包含 **2** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvSwitchRef

- **UUID**: `80d5fda3-24e8-4e6c-b6b5-169488db65b6`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

############ 2. EthTrcvSwitchPortRef

- **UUID**: `ceadd11b-8683-4411-8e61-799194101f4d`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

######### 4. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `19e7adab-92f9-4d65-b346-95411d30c557`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **需要索引**: false

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. EthTrcvCtrlRef

- **UUID**: `1d60c773-1b16-491a-a805-1736a0b65e56`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

######### 5. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `8d6e294c-f7f6-4e41-ba9e-8041b8bdbf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **需要索引**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. EthTrcvWakeupReason

- **UUID**: `d3a86e81-e11a-4347-adcd-9a194d410c49`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_GENERAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_INTERNAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_PIN` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_POWER_ON` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_RESET` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_SYSERR` (来源: AUTOSAR_ECUC)
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

- **UUID**: `c599449f-bd66-4b7d-b8a3-36f2346f6304`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

######### 6. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `4324364e-cf3d-46a4-a046-4ef169b00862`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `aa176d1c-219f-4780-b6fc-52673848df79`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `19e7adab-92f9-4d65-b346-95411d30c557`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

####### 2. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `d879c8ff-568a-4fd2-b313-edd7a8802637`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `034c735c-38ce-494a-89b5-6b06d8349df5`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

####### 3. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvMiiIdx

- **UUID**: `a0eab56b-a1aa-4db6-8e8e-3f65545e9398`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `0487db83-5d43-477d-9178-1532d78bd618`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_STRAPPING_CONFIG_ONLY`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_STRAPPING_CONFIG_ONLY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `20aaa534-3c96-4404-b5b8-c35eb83436b1`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

####### 4. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `aa176d1c-219f-4780-b6fc-52673848df79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `3c791576-7412-48ea-9067-f6e0a8388d1f`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_MII_MODE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_MII_MODE` (来源: Vector Informatik)
  - `ETHTRCV_INTERNAL_PHY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface.  In case the configured element is an intenal PHY choose INTERNAL PHY, in case it is an external PHY managed by a switch the interface must be selected. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvSwitchRef

- **UUID**: `80d5fda3-24e8-4e6c-b6b5-169488db65b6`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

########## 2. EthTrcvSwitchPortRef

- **UUID**: `ceadd11b-8683-4411-8e61-799194101f4d`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

####### 5. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `19e7adab-92f9-4d65-b346-95411d30c557`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **需要索引**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `1d60c773-1b16-491a-a805-1736a0b65e56`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

####### 6. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `8d6e294c-f7f6-4e41-ba9e-8041b8bdbf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **需要索引**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvWakeupReason

- **UUID**: `d3a86e81-e11a-4347-adcd-9a194d410c49`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_GENERAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_INTERNAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_PIN` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_POWER_ON` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_RESET` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_SYSERR` (来源: AUTOSAR_ECUC)
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

- **UUID**: `c599449f-bd66-4b7d-b8a3-36f2346f6304`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

####### 7. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `4324364e-cf3d-46a4-a046-4ef169b00862`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `aa176d1c-219f-4780-b6fc-52673848df79`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `19e7adab-92f9-4d65-b346-95411d30c557`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

##### 3. EthTrcvConfig

**容器属性**:

- **UUID**: `08e5c37f-0d70-4e2e-8a61-098ff1571f81`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvConfig`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container includes the configuration of the individual transceiver.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvIdx

- **UUID**: `9c306c41-0fe6-4d22-98ac-258ad4dcc259`
- **参数名**: `EthTrcvIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This value specifies the instance ID of the configured transceiver.

######## 2. EthTrcvPhySignalQualityMeanValueLength

- **UUID**: `9424ac19-78c6-4d74-b638-ef9f3e8ded82`
- **参数名**: `EthTrcvPhySignalQualityMeanValueLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **取值范围**: [1..1000]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies how many consecutive data points of the phy's signal quality are used for the calculated mean value.

######## 3. EthTrcvSoftResetWaitCycles

- **UUID**: `0818f81f-f7ca-49bd-a97a-b8f378f2074e`
- **参数名**: `EthTrcvSoftResetWaitCycles`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `120`
- **取值范围**: [1..65535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the wait time until a soft reset is performed. After soft reset the driver polls the transceiver register and checks that the reset is performed or not. This is the maximum wait time.

####### BOOLEAN 类型参数

######## 1. EthTrcvSoftResetOnInit

- **UUID**: `a53fcbb2-8528-4e11-8527-4967bf72a42e`
- **参数名**: `EthTrcvSoftResetOnInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter speficies if a soft reset during transceiver initialization re-initializes all transceiver registers. In case the user sets some transceiver registers during runtime and wants to restore the default settings when transceiver is re-initialized, this option must be enabled.

######## 2. EthTrcvAutoNegotiationEnabled

- **UUID**: `82e27dbf-ecf4-4afa-bc6c-e9ac8d63705b`
- **参数名**: `EthTrcvAutoNegotiationEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Specifies if Auto-Negotiation is enabled (TRUE) or disabled (FALSE) for determination of the Ethernet transceiver speed.
Note: Since on 88Q1010, the setting of the transceiver speed is not available (only 100 Mbit/s supported), This settings is not enabled and the speed set to default 100Mbit/s

####### ENUMERATION 类型参数

######## 1. EthTrcvSpeed

- **UUID**: `de13e1e5-a34e-4215-951f-7c435c1b20e5`
- **参数名**: `EthTrcvSpeed`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TRCV_SPEED_100`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `TRCV_SPEED_10` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_100` (来源: AUTOSAR_ECUC)
  - `TRCV_SPEED_1000` (来源: AUTOSAR_ECUC)
- **描述**: This parameter specifies the speed of the Ethernet transceiver link in MBit/s.

RESTRICTION: If Auto Negotiation is enabled this is the maximum speed advertised for Auto-Negotiation

######## 2. EthTrcvWakeupInspectionType

- **UUID**: `d530a5d8-1c0e-4e91-aabc-0571a90ebd76`
- **参数名**: `EthTrcvWakeupInspectionType`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **默认值**: `ETHTRCV_ICU_CHANNEL`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_ICU_CHANNEL` (来源: Vector Informatik)
  - `ETHTRCV_TRCV_REGISTERS` (来源: Vector Informatik)
  - `ETHTRCV_USER_CODE` (来源: Vector Informatik)
- **描述**: This parameter specifies the method used for inspection of wakeup events.

ETHTRCV_ICU_CHANNEL:
Uses the Icu_GetInputState() API for the related Icu channel to verify if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_TRCV_REGISTERS:
If hardware supports waking up by the transceiver itself the driver checks its registers if a wakeup event occured and the corresponding AUTOSAR wakeup reason must be set.

ETHTRCV_USER_CODE:
The user must provide integration code by itself for wakeup event inspection. This code must be embedded within the function EthTrcv_WakeupInspection generated into EthTrcv_Lcfg.c. For a more detailed information please refere to the Technical Reference of the driver.

######## 3. EthTrcvConnNeg

- **UUID**: `11a530df-5836-42b6-a061-404da14a2865`
- **参数名**: `EthTrcvConnNeg`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_CONN_NEG_MASTER`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_CONN_NEG_MASTER` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_SLAVE` (来源: Vector Informatik)
  - `ETHTRCV_CONN_NEG_AUTO` (来源: Vector Informatik)
- **描述**: This parameter specifies the connection negotiation of the Ethernet transceiver link.
Note: The ETHTRCV_CONN_NEG_AUTO setting affects the auto-negotiation mode of negotiation. This setting enables the auto negotiation with prefered mode and not advertised.

####### FUNCTION-NAME 类型参数

######## 1. EthTrcvWakeUpCallout

- **UUID**: `e48ca860-3a73-40cd-af2d-22886eb3d88e`
- **参数名**: `EthTrcvWakeUpCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies a callout function that is called during EthTrcv_SetTransceiverMode() for transceiver activation if a wakeup event has occured.

The callout can be used for e.g. initiating a remote wakeup of related ECUs by setting a activation line connected to them.
The function must be declared as followed:
void &lt;EthTrcvWakeUpCallout&gt;(uint8 TrcvIdx)

######## 2. EthTrcvWakeUpInspectionCallout

- **UUID**: `feedb40e-8a11-42df-a1f5-1a68b01d4053`
- **参数名**: `EthTrcvWakeUpInspectionCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter specifies a callout function that is called if the Wakeup Inspection Type is set to "ETHTRCV_USER_CODE".

The callout can be used to realize a user-defined wake-up inspection and reporting.
 
The function must be declared as follows:
void &lt;EthTrcvWakeUpInspectionCallout&gt;(uint8 TrcvIdx)

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvIcuChannelRef

- **UUID**: `936e9bb4-fa9b-4617-85eb-c6629db4a42f`
- **引用名**: `EthTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a Icu channel container.

The reference is used for enabling/disabling the wakeup notifications triggered by Icu in case EthTrcvWakeupSupport is configured to ETHTRCV_WAKEUP_BY_INTERRUPT.
Additionally the reference is used to check for a proper wakeup signal if the parameter EthTrcvWakeupVerificationType is set to ETHTRCV_ICU_CHANNEL.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `d879c8ff-568a-4fd2-b313-edd7a8802637`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETHTRCV_E_ACCESS

- **UUID**: `034c735c-38ce-494a-89b5-6b06d8349df5`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

####### 2. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. EthTrcvMiiIdx

- **UUID**: `a0eab56b-a1aa-4db6-8e8e-3f65545e9398`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `0487db83-5d43-477d-9178-1532d78bd618`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_STRAPPING_CONFIG_ONLY`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_STRAPPING_CONFIG_ONLY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `20aaa534-3c96-4404-b5b8-c35eb83436b1`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

####### 3. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `aa176d1c-219f-4780-b6fc-52673848df79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvMiiSelection

- **UUID**: `3c791576-7412-48ea-9067-f6e0a8388d1f`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_MII_MODE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_MII_MODE` (来源: Vector Informatik)
  - `ETHTRCV_INTERNAL_PHY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface.  In case the configured element is an intenal PHY choose INTERNAL PHY, in case it is an external PHY managed by a switch the interface must be selected. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvSwitchRef

- **UUID**: `80d5fda3-24e8-4e6c-b6b5-169488db65b6`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

########## 2. EthTrcvSwitchPortRef

- **UUID**: `ceadd11b-8683-4411-8e61-799194101f4d`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

####### 4. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `19e7adab-92f9-4d65-b346-95411d30c557`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **需要索引**: false

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. EthTrcvCtrlRef

- **UUID**: `1d60c773-1b16-491a-a805-1736a0b65e56`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

####### 5. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `8d6e294c-f7f6-4e41-ba9e-8041b8bdbf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **需要索引**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. EthTrcvWakeupReason

- **UUID**: `d3a86e81-e11a-4347-adcd-9a194d410c49`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_GENERAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_INTERNAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_PIN` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_POWER_ON` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_RESET` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_SYSERR` (来源: AUTOSAR_ECUC)
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

- **UUID**: `c599449f-bd66-4b7d-b8a3-36f2346f6304`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

####### 6. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `4324364e-cf3d-46a4-a046-4ef169b00862`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `aa176d1c-219f-4780-b6fc-52673848df79`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `19e7adab-92f9-4d65-b346-95411d30c557`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

##### 4. EthTrcvDemEventParameterRefs

**容器属性**:

- **UUID**: `d879c8ff-568a-4fd2-b313-edd7a8802637`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvDemEventParameterRefs`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETHTRCV_E_ACCESS

- **UUID**: `034c735c-38ce-494a-89b5-6b06d8349df5`
- **引用名**: `ETHTRCV_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: This parameter references the Ethernet Transceiver DEM Event.

##### 5. EthTrcvMiiInterface

**容器属性**:

- **UUID**: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvMiiInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. EthTrcvMiiIdx

- **UUID**: `a0eab56b-a1aa-4db6-8e8e-3f65545e9398`
- **参数名**: `EthTrcvMiiIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [0..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: This value specifies the transceiver index used for MII (Media Independent Interface) access of the transceiver. A transceiver is usually  associated with a constant MII address, that can be selected via strapping pins on the hardware. The adress is used to identify the transceiver during communication.

####### ENUMERATION 类型参数

######## 1. EthTrcvMiiSelection

- **UUID**: `0487db83-5d43-477d-9178-1532d78bd618`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_STRAPPING_CONFIG_ONLY`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_STRAPPING_CONFIG_ONLY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvCtrlRef

- **UUID**: `20aaa534-3c96-4404-b5b8-c35eb83436b1`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

##### 6. EthTrcvSwitchInterface

**容器属性**:

- **UUID**: `aa176d1c-219f-4780-b6fc-52673848df79`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSwitchInterface`
- **多重性**: [0..1]
- **需要索引**: false

**容器描述**:

This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EthTrcvMiiSelection

- **UUID**: `3c791576-7412-48ea-9067-f6e0a8388d1f`
- **参数名**: `EthTrcvMiiSelection`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_MII_MODE`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_MII_MODE` (来源: Vector Informatik)
  - `ETHTRCV_INTERNAL_PHY` (来源: Vector Informatik)
- **描述**: This parameter specifies the type of transceiver/controller interface.  In case the configured element is an intenal PHY choose INTERNAL PHY, in case it is an external PHY managed by a switch the interface must be selected. For the 88Q1010 transceiver driver this selection is not possible since vendor specific registers are used. Extended register acces can be used instead.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvSwitchRef

- **UUID**: `80d5fda3-24e8-4e6c-b6b5-169488db65b6`
- **引用名**: `EthTrcvSwitchRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch configuration container. The switch configuration is associated with the hardware switch this transceiver is connected into.

######## 2. EthTrcvSwitchPortRef

- **UUID**: `ceadd11b-8683-4411-8e61-799194101f4d`
- **引用名**: `EthTrcvSwitchPortRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthSwtPort`
- **完整路径**: `/AUTOSAR/EcucDefs/EthSwt/EthSwtConfig/EthSwtPort`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a switch port reference. The port configuration is associated with the port of a hardware switch this transceiver connected to.

##### 7. EthTrcvSpiInterface

**容器属性**:

- **UUID**: `19e7adab-92f9-4d65-b346-95411d30c557`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvSpiInterface`
- **多重性**: [0..1]
- **需要索引**: false

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTrcvCtrlRef

- **UUID**: `1d60c773-1b16-491a-a805-1736a0b65e56`
- **引用名**: `EthTrcvCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EthCtrlConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Eth/EthConfigSet/EthCtrlConfig`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **需要索引**: false
- **描述**: Reference to a physical Ethernet controller configuration.

##### 8. EthTrcvWakeupMap

**容器属性**:

- **UUID**: `8d6e294c-f7f6-4e41-ba9e-8041b8bdbf25`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTrcvWakeupMap`
- **多重性**: [0..7]
- **需要索引**: false

**容器描述**:

Container for the mapping of wake up reasons to wake up sources. At least one container is needed if EthTrcvWakeUpSupport is not ETHTRCV_WAKEUP_NOT_SUPPORTED.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EthTrcvWakeupReason

- **UUID**: `d3a86e81-e11a-4347-adcd-9a194d410c49`
- **参数名**: `EthTrcvWakeupReason`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `ETHTRCV_WUR_BUS`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `ETHTRCV_WUR_BUS` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_GENERAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_INTERNAL` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_PIN` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_POWER_ON` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_RESET` (来源: AUTOSAR_ECUC)
  - `ETHTRCV_WUR_SYSERR` (来源: AUTOSAR_ECUC)
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

- **UUID**: `c599449f-bd66-4b7d-b8a3-36f2346f6304`
- **引用名**: `EthTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a EcuM wakeup source container.

This wakeup source is mapped to the wakeup reason and is issued to the EcuM during EcuM_CheckWakeup() with EcuM_SetWakeupEvent() if the corresponding wakeup reason occured.

##### 9. EthTrcvMgmtInterface

**容器属性**:

- **UUID**: `4324364e-cf3d-46a4-a046-4ef169b00862`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `EthTrcvMgmtInterface`
- **多重性**: [1..1]
- **需要索引**: false

**容器选择**:

- **EthTrcvMiiInterface**
  - UUID: `1ecafd2a-e922-41d0-89a0-eeaafd8089df`
  - 描述: This container includes the MII interface configuration between an Ethernet Controller and the Ethernet Transceiver.
- **EthTrcvSwitchInterface**
  - UUID: `aa176d1c-219f-4780-b6fc-52673848df79`
  - 描述: This container includes the Switch interface configuration between an Ethernet Switch and an Ethernet Transceiver.
- **EthTrcvSpiInterface**
  - UUID: `19e7adab-92f9-4d65-b346-95411d30c557`

**容器描述**:

This container includes either a MII interface or Switch interface container. Depending on the physical hardware the transceiver is either connected to an Ethernet Controller via MII interface or is integrated into an Ethernet Switch.

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 0

### 2. EthTrcv_88Q1010

- **UUID**: `703f9a34-a4f6-4a42-8f53-11095317443f`
- **包名称**: `EthTrcv_88Q1010`
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

- **UUID**: `e44661bd-2950-433e-985e-1edc6d1a4a9c`
- **实现名称**: `EthTrcv_Impl`
- **编程语言**: C
- **软件版本**: 3.00.01
- **供应商ID**: 30
- **AUTOSAR版本**: 4.01.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. EthTrcv_Pre

- **UUID**: `6d2845f3-3b91-420f-811f-cbc1dde5b26a`
- **配置名称**: `EthTrcv_Pre`
- **定义引用**: `/MICROSAR/EthTrcv_88Q1010/EthTrcv`

### 2. EthTrcv_Rec

- **UUID**: `971cc533-fcba-42ae-b38f-96ef6a60d8be`
- **配置名称**: `EthTrcv_Rec`
- **定义引用**: `/MICROSAR/EthTrcv_88Q1010/EthTrcv`
