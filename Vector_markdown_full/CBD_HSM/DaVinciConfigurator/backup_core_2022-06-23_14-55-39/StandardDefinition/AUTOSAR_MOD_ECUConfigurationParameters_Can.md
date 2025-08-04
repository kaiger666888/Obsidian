# Can - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:07

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Can](#can)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Can

#### 基本信息

- **UUID**: `ECUC:f7ca73a3-b05b-4f6a-a64d-9a6e8da3314e`
- **模块名称**: `Can`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

This container holds the configuration of a single CAN Driver.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. CanConfigSet

**容器属性**:

- **UUID**: `ECUC:e28c636a-f5f1-4503-b0ad-aed7fbed80d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This is the multiple configuration set container for CAN Driver

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. CanController

**容器属性**:

- **UUID**: `ECUC:a79e276f-cf20-496c-8587-edf4d9d2f01b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the CAN controller(s).

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CanControllerBaseAddress

- **UUID**: `ECUC:69afaa0c-2dc7-4390-a7c9-c605ae01c22f`
- **参数名**: `CanControllerBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the CAN controller base address.

########## 2. CanControllerId

- **UUID**: `ECUC:efc9b48f-271a-4833-9ba0-aa53aa4cf278`
- **参数名**: `CanControllerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides the controller ID which is unique in a given CAN Driver. The value for this parameter starts with 0 and continue without any gaps.

######### BOOLEAN 类型参数

########## 1. CanControllerActivation

- **UUID**: `ECUC:e12d871d-e196-46d8-a5a5-454f8475061f`
- **参数名**: `CanControllerActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a CAN controller is used in the configuration.

########## 2. CanWakeupSupport

- **UUID**: `ECUC:48e0b1e7-b421-4388-ac6c-04b471380664`
- **参数名**: `CanWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN driver support for wakeup over CAN Bus.

######### ENUMERATION 类型参数

########## 1. CanBusoffProcessing

- **UUID**: `ECUC:1ac4345e-22de-49c3-8bb0-053a8e121758`
- **参数名**: `CanBusoffProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

########## 2. CanRxProcessing

- **UUID**: `ECUC:60718366-d647-4c8c-95ea-bc42b9536786`
- **参数名**: `CanRxProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Read() for handling PDU reception events in polling mode.

########## 3. CanTxProcessing

- **UUID**: `ECUC:87199697-72c8-46ee-b7c7-276cc811d697`
- **参数名**: `CanTxProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Write() for handling PDU transmission events in polling mode.

########## 4. CanWakeupProcessing

- **UUID**: `ECUC:826d181c-d6ad-4d64-93a2-bf529c8481e4`
- **参数名**: `CanWakeupProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Wakeup() for handling wakeup events in polling mode.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanControllerDefaultBaudrate

- **UUID**: `ECUC:aef302e1-1821-4e87-8041-e542f92cb963`
- **引用名**: `CanControllerDefaultBaudrate`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanControllerBaudrateConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController/CanControllerBaudrateConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to baudrate configuration container configured for the Can Controller.

########## 2. CanCpuClockRef

- **UUID**: `ECUC:2e20d271-b4b3-47cc-a0ee-a6e49b8373ec`
- **引用名**: `CanCpuClockRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CPU clock configuration, which is set in the MCU driver configuration

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanWakeupSourceRef

- **UUID**: `ECUC:61a02a48-1812-4052-8e57-b48bc38ce491`
- **引用名**: `CanWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the Wakeup Source for this controller as defined in the ECU State Manager.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. CanControllerBaudrateConfig

**容器属性**:

- **UUID**: `ECUC:7380e54a-e891-4fb8-88e8-459dc7c59aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanControllerBaudrateConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains bit timing related configuration parameters of the CAN controller(s).

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. CanControllerBaudRate

- **UUID**: `ECUC:e5ae7b80-e6c2-4e56-8ccd-5dce07379977`
- **参数名**: `CanControllerBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baudrate of the controller in kbps.

############ 2. CanControllerPropSeg

- **UUID**: `ECUC:669827f7-fac2-42e8-870b-8003e83a0cbc`
- **参数名**: `CanControllerPropSeg`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies propagation delay in time quantas.

############ 3. CanControllerSeg1

- **UUID**: `ECUC:2ff9d8a8-d32b-4a08-85d7-8cc51effa452`
- **参数名**: `CanControllerSeg1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 1 in time quantas.

############ 4. CanControllerSeg2

- **UUID**: `ECUC:755cccd2-d9a8-4df1-9cdb-6a9c5f850a12`
- **参数名**: `CanControllerSeg2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 2 in time quantas.

############ 5. CanControllerSyncJumpWidth

- **UUID**: `ECUC:70cfe32e-1160-408d-be3c-9e8a789a5bb9`
- **参数名**: `CanControllerSyncJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the synchronization jump width for the controller in time quantas.

######### 2. CanFilterMask

**容器属性**:

- **UUID**: `ECUC:be9f285a-0eda-475e-9def-ef440e3c84c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanFilterMask`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the CAN Filter Mask(s).

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanFilterMaskValue

- **UUID**: `ECUC:0b97bc36-d3d1-4d14-af96-e57e293fc3e1`
- **参数名**: `CanFilterMaskValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes a mask for hardware-based filtering of CAN identifiers. The CAN identifiers of incoming messages are masked with the appropriate CanFilterMaskValue. Bits holding a 0 mean don't care, i.e. do not compare the message's identifier in the respective bit position.

######### 3. CanTTController

**容器属性**:

- **UUID**: `ECUC:03522dfa-716f-4cae-b216-c32f5ff584ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTController`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

########## 参数配置

此容器包含 **18** 个参数：

########### INTEGER 类型参数

############ 1. CanTTControllerApplWatchdogLimit

- **UUID**: `ECUC:58bdc478-e74c-42df-8d3d-0ba19ae24008`
- **参数名**: `CanTTControllerApplWatchdogLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum time period (unit is 256 times NTU) after which the application has to serve the watchdog.

############ 2. CanTTControllerCycleCountMax

- **UUID**: `ECUC:fafa672b-b0c5-4c09-9035-06e2461576cf`
- **参数名**: `CanTTControllerCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value for cycle_count_max.

############ 3. CanTTControllerExpectedTxTrigger

- **UUID**: `ECUC:91b067db-e57d-432f-9093-262d567242ec`
- **参数名**: `CanTTControllerExpectedTxTrigger`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of expected_tx_trigger.

############ 4. CanTTControllerInitialRefOffset

- **UUID**: `ECUC:25750102-31df-4bed-91cf-01253dc78faf`
- **参数名**: `CanTTControllerInitialRefOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial value for ref trigger offset.

############ 5. CanTTControllerInterruptEnable

- **UUID**: `ECUC:6d752b5f-31aa-4e11-915c-cbe1e1a0f01a`
- **参数名**: `CanTTControllerInterruptEnable`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the respective interrupts.

############ 6. CanTTControllerTimeMasterPriority

- **UUID**: `ECUC:64837877-30b7-48a4-9f87-a7e4e959010f`
- **参数名**: `CanTTControllerTimeMasterPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time master priority.

############ 7. CanTTControllerTxEnableWindowLength

- **UUID**: `ECUC:432b3c85-542c-48e3-ab51-3944e1d6e421`
- **参数名**: `CanTTControllerTxEnableWindowLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the tx enable window given in CAN bit times.

############ 8. CanTTControllerWatchTriggerGapTimeMark

- **UUID**: `ECUC:a880dad8-6591-4dbc-a3d4-8057ff9b6931`
- **参数名**: `CanTTControllerWatchTriggerGapTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark after a gap

############ 9. CanTTControllerWatchTriggerTimeMark

- **UUID**: `ECUC:496f1799-9365-4e5b-878a-dd8cab58f338`
- **参数名**: `CanTTControllerWatchTriggerTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark

########### BOOLEAN 类型参数

############ 1. CanTTControllerExternalClockSynchronisation

- **UUID**: `ECUC:1f319887-2617-4190-b5d6-95b9e555b180`
- **参数名**: `CanTTControllerExternalClockSynchronisation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the external clock synchronization.

############ 2. CanTTControllerGlobalTimeFiltering

- **UUID**: `ECUC:ced20e88-c426-42a9-bce0-ed1a2a5f3797`
- **参数名**: `CanTTControllerGlobalTimeFiltering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the global time filtering.

############ 3. CanTTControllerLevel2

- **UUID**: `ECUC:91462836-5301-42da-8b89-dad7c7ddeb2c`
- **参数名**: `CanTTControllerLevel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether Level 2 or Level 1 is used.

############ 4. CanTTControllerTURRestore

- **UUID**: `ECUC:e5b66746-4e6e-47f5-b62b-ab6452a49082`
- **参数名**: `CanTTControllerTURRestore`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the TUR restore.

############ 5. CanTTControllerTimeMaster

- **UUID**: `ECUC:68c24e85-bb75-4b38-b9af-05947b2f0f27`
- **参数名**: `CanTTControllerTimeMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the controller acts as a potential time master.

########### FLOAT 类型参数

############ 1. CanTTControllerNTUConfig

- **UUID**: `ECUC:fc8b7d0e-677b-4c04-b547-ef6602271c33`
- **参数名**: `CanTTControllerNTUConfig`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the config value for NTU (network time unit).

############ 2. CanTTControllerSyncDeviation

- **UUID**: `ECUC:26f778c8-15de-4c4a-b05e-fff49e20b233`
- **参数名**: `CanTTControllerSyncDeviation`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum synchronization deviation:

########### ENUMERATION 类型参数

############ 1. CanTTControllerOperationMode

- **UUID**: `ECUC:fd04f084-a5cc-4c27-9d75-7e1a46e86bfa`
- **参数名**: `CanTTControllerOperationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_EVENT_SYNC_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the operation mode.

############ 2. CanTTIRQProcessing

- **UUID**: `ECUC:089059db-bfe6-43a7-9fa7-99b4b583a2bf`
- **参数名**: `CanTTIRQProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

####### 2. CanControllerBaudrateConfig

**容器属性**:

- **UUID**: `ECUC:7380e54a-e891-4fb8-88e8-459dc7c59aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanControllerBaudrateConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains bit timing related configuration parameters of the CAN controller(s).

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanControllerBaudRate

- **UUID**: `ECUC:e5ae7b80-e6c2-4e56-8ccd-5dce07379977`
- **参数名**: `CanControllerBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baudrate of the controller in kbps.

########## 2. CanControllerPropSeg

- **UUID**: `ECUC:669827f7-fac2-42e8-870b-8003e83a0cbc`
- **参数名**: `CanControllerPropSeg`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies propagation delay in time quantas.

########## 3. CanControllerSeg1

- **UUID**: `ECUC:2ff9d8a8-d32b-4a08-85d7-8cc51effa452`
- **参数名**: `CanControllerSeg1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 1 in time quantas.

########## 4. CanControllerSeg2

- **UUID**: `ECUC:755cccd2-d9a8-4df1-9cdb-6a9c5f850a12`
- **参数名**: `CanControllerSeg2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 2 in time quantas.

########## 5. CanControllerSyncJumpWidth

- **UUID**: `ECUC:70cfe32e-1160-408d-be3c-9e8a789a5bb9`
- **参数名**: `CanControllerSyncJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the synchronization jump width for the controller in time quantas.

####### 3. CanFilterMask

**容器属性**:

- **UUID**: `ECUC:be9f285a-0eda-475e-9def-ef440e3c84c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanFilterMask`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the CAN Filter Mask(s).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanFilterMaskValue

- **UUID**: `ECUC:0b97bc36-d3d1-4d14-af96-e57e293fc3e1`
- **参数名**: `CanFilterMaskValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes a mask for hardware-based filtering of CAN identifiers. The CAN identifiers of incoming messages are masked with the appropriate CanFilterMaskValue. Bits holding a 0 mean don't care, i.e. do not compare the message's identifier in the respective bit position.

####### 4. CanTTController

**容器属性**:

- **UUID**: `ECUC:03522dfa-716f-4cae-b216-c32f5ff584ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTController`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **18** 个参数：

######### INTEGER 类型参数

########## 1. CanTTControllerApplWatchdogLimit

- **UUID**: `ECUC:58bdc478-e74c-42df-8d3d-0ba19ae24008`
- **参数名**: `CanTTControllerApplWatchdogLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum time period (unit is 256 times NTU) after which the application has to serve the watchdog.

########## 2. CanTTControllerCycleCountMax

- **UUID**: `ECUC:fafa672b-b0c5-4c09-9035-06e2461576cf`
- **参数名**: `CanTTControllerCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value for cycle_count_max.

########## 3. CanTTControllerExpectedTxTrigger

- **UUID**: `ECUC:91b067db-e57d-432f-9093-262d567242ec`
- **参数名**: `CanTTControllerExpectedTxTrigger`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of expected_tx_trigger.

########## 4. CanTTControllerInitialRefOffset

- **UUID**: `ECUC:25750102-31df-4bed-91cf-01253dc78faf`
- **参数名**: `CanTTControllerInitialRefOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial value for ref trigger offset.

########## 5. CanTTControllerInterruptEnable

- **UUID**: `ECUC:6d752b5f-31aa-4e11-915c-cbe1e1a0f01a`
- **参数名**: `CanTTControllerInterruptEnable`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the respective interrupts.

########## 6. CanTTControllerTimeMasterPriority

- **UUID**: `ECUC:64837877-30b7-48a4-9f87-a7e4e959010f`
- **参数名**: `CanTTControllerTimeMasterPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time master priority.

########## 7. CanTTControllerTxEnableWindowLength

- **UUID**: `ECUC:432b3c85-542c-48e3-ab51-3944e1d6e421`
- **参数名**: `CanTTControllerTxEnableWindowLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the tx enable window given in CAN bit times.

########## 8. CanTTControllerWatchTriggerGapTimeMark

- **UUID**: `ECUC:a880dad8-6591-4dbc-a3d4-8057ff9b6931`
- **参数名**: `CanTTControllerWatchTriggerGapTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark after a gap

########## 9. CanTTControllerWatchTriggerTimeMark

- **UUID**: `ECUC:496f1799-9365-4e5b-878a-dd8cab58f338`
- **参数名**: `CanTTControllerWatchTriggerTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark

######### BOOLEAN 类型参数

########## 1. CanTTControllerExternalClockSynchronisation

- **UUID**: `ECUC:1f319887-2617-4190-b5d6-95b9e555b180`
- **参数名**: `CanTTControllerExternalClockSynchronisation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the external clock synchronization.

########## 2. CanTTControllerGlobalTimeFiltering

- **UUID**: `ECUC:ced20e88-c426-42a9-bce0-ed1a2a5f3797`
- **参数名**: `CanTTControllerGlobalTimeFiltering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the global time filtering.

########## 3. CanTTControllerLevel2

- **UUID**: `ECUC:91462836-5301-42da-8b89-dad7c7ddeb2c`
- **参数名**: `CanTTControllerLevel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether Level 2 or Level 1 is used.

########## 4. CanTTControllerTURRestore

- **UUID**: `ECUC:e5b66746-4e6e-47f5-b62b-ab6452a49082`
- **参数名**: `CanTTControllerTURRestore`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the TUR restore.

########## 5. CanTTControllerTimeMaster

- **UUID**: `ECUC:68c24e85-bb75-4b38-b9af-05947b2f0f27`
- **参数名**: `CanTTControllerTimeMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the controller acts as a potential time master.

######### FLOAT 类型参数

########## 1. CanTTControllerNTUConfig

- **UUID**: `ECUC:fc8b7d0e-677b-4c04-b547-ef6602271c33`
- **参数名**: `CanTTControllerNTUConfig`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the config value for NTU (network time unit).

########## 2. CanTTControllerSyncDeviation

- **UUID**: `ECUC:26f778c8-15de-4c4a-b05e-fff49e20b233`
- **参数名**: `CanTTControllerSyncDeviation`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum synchronization deviation:

######### ENUMERATION 类型参数

########## 1. CanTTControllerOperationMode

- **UUID**: `ECUC:fd04f084-a5cc-4c27-9d75-7e1a46e86bfa`
- **参数名**: `CanTTControllerOperationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_EVENT_SYNC_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the operation mode.

########## 2. CanTTIRQProcessing

- **UUID**: `ECUC:089059db-bfe6-43a7-9fa7-99b4b583a2bf`
- **参数名**: `CanTTIRQProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

####### 5. CanHardwareObject

**容器属性**:

- **UUID**: `ECUC:ee3d6577-0017-42fc-b4d6-8d27c2e66563`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanHardwareObject`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of CAN Hardware Objects.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanIdValue

- **UUID**: `ECUC:615fef00-eb96-4bbb-afd7-cef66a67db46`
- **参数名**: `CanIdValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies (together with the filter mask) the identifiers range that passes the hardware filter.

########## 2. CanObjectId

- **UUID**: `ECUC:5049e195-870c-490c-ac6d-745aae833d04`
- **参数名**: `CanObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the handle ID of HRH or HTH. The value of this parameter is unique in a given CAN Driver, and it should start with 0 and continue without any gaps.

######### ENUMERATION 类型参数

########## 1. CanHandleType

- **UUID**: `ECUC:6c58c09a-9aa2-4e4d-8ae3-8eba40a77aaf`
- **参数名**: `CanHandleType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BASIC` (来源: AUTOSAR_ECUC)
  - `FULL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the type (Full-CAN or Basic-CAN) of a hardware object.

########## 2. CanIdType

- **UUID**: `ECUC:f8442a9b-7752-416c-ac68-8cd3080589c0`
- **参数名**: `CanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether the IdValue is of type

########## 3. CanObjectType

- **UUID**: `ECUC:b8abf5c9-4e6a-46bf-a1ae-63b191e72d04`
- **参数名**: `CanObjectType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RECEIVE` (来源: AUTOSAR_ECUC)
  - `TRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the HardwareObject is used as Transmit or as Receive object

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanControllerRef

- **UUID**: `ECUC:e2b98fcd-3e29-4041-a480-aed31e706d97`
- **引用名**: `CanControllerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanController`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to CAN Controller to which the HOH is associated to.

########## 2. CanFilterMaskRef

- **UUID**: `ECUC:d0683493-3c90-46c3-815f-5a3dabb20a7a`
- **引用名**: `CanFilterMaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CanFilterMask`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController/CanFilterMask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the filter mask that is used for hardware filtering together with the CAN_ID_VALUE.

########## 3. CanMainFunctionRWPeriodRef

- **UUID**: `ECUC:185477b7-2192-42b1-9dad-c72942a94b7c`
- **引用名**: `CanMainFunctionRWPeriodRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CanMainFunctionRWPeriods`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanGeneral/CanMainFunctionRWPeriods`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to CAN Controller to which the HOH is associated to.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTTHardwareObjectTrigger

**容器属性**:

- **UUID**: `ECUC:5c10353d-3ba8-4140-adf6-b5c02d28c9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTHardwareObjectTrigger`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. CanTTHardwareObjectBaseCycle

- **UUID**: `ECUC:bbb7fda0-3f86-4144-b471-33793652290e`
- **参数名**: `CanTTHardwareObjectBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the cycle_offset.

############ 2. CanTTHardwareObjectCycleRepetition

- **UUID**: `ECUC:6f58e444-b305-47d4-899b-38971bc77aa6`
- **参数名**: `CanTTHardwareObjectCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repeat_factor.

############ 3. CanTTHardwareObjectTimeMark

- **UUID**: `ECUC:737166e8-39c4-4d60-ac3f-00672a8ebf66`
- **参数名**: `CanTTHardwareObjectTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the trigger will be activated.

############ 4. CanTTHardwareObjectTriggerId

- **UUID**: `ECUC:0da05573-613f-45fd-94f7-68688e7bcf18`
- **参数名**: `CanTTHardwareObjectTriggerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sequential number which allows separation of different TTCAN triggers configured for one and the same hardware object.

########### ENUMERATION 类型参数

############ 1. CanTTHardwareObjectTriggerType

- **UUID**: `ECUC:b15710a4-a4ef-45a8-830a-33d47a8b386c`
- **参数名**: `CanTTHardwareObjectTriggerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_RX_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER_GAP` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_EXCLUSIVE` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_MERGED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_SINGLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the trigger associated with the hardware object. This parameter depends on plain CAN parameter CAN_OBJECT_TYPE.

####### 6. CanTTHardwareObjectTrigger

**容器属性**:

- **UUID**: `ECUC:5c10353d-3ba8-4140-adf6-b5c02d28c9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTHardwareObjectTrigger`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanTTHardwareObjectBaseCycle

- **UUID**: `ECUC:bbb7fda0-3f86-4144-b471-33793652290e`
- **参数名**: `CanTTHardwareObjectBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the cycle_offset.

########## 2. CanTTHardwareObjectCycleRepetition

- **UUID**: `ECUC:6f58e444-b305-47d4-899b-38971bc77aa6`
- **参数名**: `CanTTHardwareObjectCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repeat_factor.

########## 3. CanTTHardwareObjectTimeMark

- **UUID**: `ECUC:737166e8-39c4-4d60-ac3f-00672a8ebf66`
- **参数名**: `CanTTHardwareObjectTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the trigger will be activated.

########## 4. CanTTHardwareObjectTriggerId

- **UUID**: `ECUC:0da05573-613f-45fd-94f7-68688e7bcf18`
- **参数名**: `CanTTHardwareObjectTriggerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sequential number which allows separation of different TTCAN triggers configured for one and the same hardware object.

######### ENUMERATION 类型参数

########## 1. CanTTHardwareObjectTriggerType

- **UUID**: `ECUC:b15710a4-a4ef-45a8-830a-33d47a8b386c`
- **参数名**: `CanTTHardwareObjectTriggerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_RX_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER_GAP` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_EXCLUSIVE` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_MERGED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_SINGLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the trigger associated with the hardware object. This parameter depends on plain CAN parameter CAN_OBJECT_TYPE.

##### 2. CanController

**容器属性**:

- **UUID**: `ECUC:a79e276f-cf20-496c-8587-edf4d9d2f01b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters of the CAN controller(s).

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. CanControllerBaseAddress

- **UUID**: `ECUC:69afaa0c-2dc7-4390-a7c9-c605ae01c22f`
- **参数名**: `CanControllerBaseAddress`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the CAN controller base address.

######## 2. CanControllerId

- **UUID**: `ECUC:efc9b48f-271a-4833-9ba0-aa53aa4cf278`
- **参数名**: `CanControllerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides the controller ID which is unique in a given CAN Driver. The value for this parameter starts with 0 and continue without any gaps.

####### BOOLEAN 类型参数

######## 1. CanControllerActivation

- **UUID**: `ECUC:e12d871d-e196-46d8-a5a5-454f8475061f`
- **参数名**: `CanControllerActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines if a CAN controller is used in the configuration.

######## 2. CanWakeupSupport

- **UUID**: `ECUC:48e0b1e7-b421-4388-ac6c-04b471380664`
- **参数名**: `CanWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN driver support for wakeup over CAN Bus.

####### ENUMERATION 类型参数

######## 1. CanBusoffProcessing

- **UUID**: `ECUC:1ac4345e-22de-49c3-8bb0-053a8e121758`
- **参数名**: `CanBusoffProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

######## 2. CanRxProcessing

- **UUID**: `ECUC:60718366-d647-4c8c-95ea-bc42b9536786`
- **参数名**: `CanRxProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Read() for handling PDU reception events in polling mode.

######## 3. CanTxProcessing

- **UUID**: `ECUC:87199697-72c8-46ee-b7c7-276cc811d697`
- **参数名**: `CanTxProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Write() for handling PDU transmission events in polling mode.

######## 4. CanWakeupProcessing

- **UUID**: `ECUC:826d181c-d6ad-4d64-93a2-bf529c8481e4`
- **参数名**: `CanWakeupProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_Wakeup() for handling wakeup events in polling mode.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanControllerDefaultBaudrate

- **UUID**: `ECUC:aef302e1-1821-4e87-8041-e542f92cb963`
- **引用名**: `CanControllerDefaultBaudrate`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanControllerBaudrateConfig`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController/CanControllerBaudrateConfig`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to baudrate configuration container configured for the Can Controller.

######## 2. CanCpuClockRef

- **UUID**: `ECUC:2e20d271-b4b3-47cc-a0ee-a6e49b8373ec`
- **引用名**: `CanCpuClockRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `McuClockReferencePoint`
- **完整路径**: `/AUTOSAR/EcucDefs/Mcu/McuModuleConfiguration/McuClockSettingConfig/McuClockReferencePoint`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the CPU clock configuration, which is set in the MCU driver configuration

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanWakeupSourceRef

- **UUID**: `ECUC:61a02a48-1812-4052-8e57-b48bc38ce491`
- **引用名**: `CanWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the Wakeup Source for this controller as defined in the ECU State Manager.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CanControllerBaudrateConfig

**容器属性**:

- **UUID**: `ECUC:7380e54a-e891-4fb8-88e8-459dc7c59aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanControllerBaudrateConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains bit timing related configuration parameters of the CAN controller(s).

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanControllerBaudRate

- **UUID**: `ECUC:e5ae7b80-e6c2-4e56-8ccd-5dce07379977`
- **参数名**: `CanControllerBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baudrate of the controller in kbps.

########## 2. CanControllerPropSeg

- **UUID**: `ECUC:669827f7-fac2-42e8-870b-8003e83a0cbc`
- **参数名**: `CanControllerPropSeg`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies propagation delay in time quantas.

########## 3. CanControllerSeg1

- **UUID**: `ECUC:2ff9d8a8-d32b-4a08-85d7-8cc51effa452`
- **参数名**: `CanControllerSeg1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 1 in time quantas.

########## 4. CanControllerSeg2

- **UUID**: `ECUC:755cccd2-d9a8-4df1-9cdb-6a9c5f850a12`
- **参数名**: `CanControllerSeg2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 2 in time quantas.

########## 5. CanControllerSyncJumpWidth

- **UUID**: `ECUC:70cfe32e-1160-408d-be3c-9e8a789a5bb9`
- **参数名**: `CanControllerSyncJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the synchronization jump width for the controller in time quantas.

####### 2. CanFilterMask

**容器属性**:

- **UUID**: `ECUC:be9f285a-0eda-475e-9def-ef440e3c84c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanFilterMask`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the CAN Filter Mask(s).

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanFilterMaskValue

- **UUID**: `ECUC:0b97bc36-d3d1-4d14-af96-e57e293fc3e1`
- **参数名**: `CanFilterMaskValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes a mask for hardware-based filtering of CAN identifiers. The CAN identifiers of incoming messages are masked with the appropriate CanFilterMaskValue. Bits holding a 0 mean don't care, i.e. do not compare the message's identifier in the respective bit position.

####### 3. CanTTController

**容器属性**:

- **UUID**: `ECUC:03522dfa-716f-4cae-b216-c32f5ff584ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTController`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **18** 个参数：

######### INTEGER 类型参数

########## 1. CanTTControllerApplWatchdogLimit

- **UUID**: `ECUC:58bdc478-e74c-42df-8d3d-0ba19ae24008`
- **参数名**: `CanTTControllerApplWatchdogLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum time period (unit is 256 times NTU) after which the application has to serve the watchdog.

########## 2. CanTTControllerCycleCountMax

- **UUID**: `ECUC:fafa672b-b0c5-4c09-9035-06e2461576cf`
- **参数名**: `CanTTControllerCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value for cycle_count_max.

########## 3. CanTTControllerExpectedTxTrigger

- **UUID**: `ECUC:91b067db-e57d-432f-9093-262d567242ec`
- **参数名**: `CanTTControllerExpectedTxTrigger`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of expected_tx_trigger.

########## 4. CanTTControllerInitialRefOffset

- **UUID**: `ECUC:25750102-31df-4bed-91cf-01253dc78faf`
- **参数名**: `CanTTControllerInitialRefOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial value for ref trigger offset.

########## 5. CanTTControllerInterruptEnable

- **UUID**: `ECUC:6d752b5f-31aa-4e11-915c-cbe1e1a0f01a`
- **参数名**: `CanTTControllerInterruptEnable`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the respective interrupts.

########## 6. CanTTControllerTimeMasterPriority

- **UUID**: `ECUC:64837877-30b7-48a4-9f87-a7e4e959010f`
- **参数名**: `CanTTControllerTimeMasterPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time master priority.

########## 7. CanTTControllerTxEnableWindowLength

- **UUID**: `ECUC:432b3c85-542c-48e3-ab51-3944e1d6e421`
- **参数名**: `CanTTControllerTxEnableWindowLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the tx enable window given in CAN bit times.

########## 8. CanTTControllerWatchTriggerGapTimeMark

- **UUID**: `ECUC:a880dad8-6591-4dbc-a3d4-8057ff9b6931`
- **参数名**: `CanTTControllerWatchTriggerGapTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark after a gap

########## 9. CanTTControllerWatchTriggerTimeMark

- **UUID**: `ECUC:496f1799-9365-4e5b-878a-dd8cab58f338`
- **参数名**: `CanTTControllerWatchTriggerTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark

######### BOOLEAN 类型参数

########## 1. CanTTControllerExternalClockSynchronisation

- **UUID**: `ECUC:1f319887-2617-4190-b5d6-95b9e555b180`
- **参数名**: `CanTTControllerExternalClockSynchronisation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the external clock synchronization.

########## 2. CanTTControllerGlobalTimeFiltering

- **UUID**: `ECUC:ced20e88-c426-42a9-bce0-ed1a2a5f3797`
- **参数名**: `CanTTControllerGlobalTimeFiltering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the global time filtering.

########## 3. CanTTControllerLevel2

- **UUID**: `ECUC:91462836-5301-42da-8b89-dad7c7ddeb2c`
- **参数名**: `CanTTControllerLevel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether Level 2 or Level 1 is used.

########## 4. CanTTControllerTURRestore

- **UUID**: `ECUC:e5b66746-4e6e-47f5-b62b-ab6452a49082`
- **参数名**: `CanTTControllerTURRestore`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the TUR restore.

########## 5. CanTTControllerTimeMaster

- **UUID**: `ECUC:68c24e85-bb75-4b38-b9af-05947b2f0f27`
- **参数名**: `CanTTControllerTimeMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the controller acts as a potential time master.

######### FLOAT 类型参数

########## 1. CanTTControllerNTUConfig

- **UUID**: `ECUC:fc8b7d0e-677b-4c04-b547-ef6602271c33`
- **参数名**: `CanTTControllerNTUConfig`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the config value for NTU (network time unit).

########## 2. CanTTControllerSyncDeviation

- **UUID**: `ECUC:26f778c8-15de-4c4a-b05e-fff49e20b233`
- **参数名**: `CanTTControllerSyncDeviation`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum synchronization deviation:

######### ENUMERATION 类型参数

########## 1. CanTTControllerOperationMode

- **UUID**: `ECUC:fd04f084-a5cc-4c27-9d75-7e1a46e86bfa`
- **参数名**: `CanTTControllerOperationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_EVENT_SYNC_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the operation mode.

########## 2. CanTTIRQProcessing

- **UUID**: `ECUC:089059db-bfe6-43a7-9fa7-99b4b583a2bf`
- **参数名**: `CanTTIRQProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

##### 3. CanControllerBaudrateConfig

**容器属性**:

- **UUID**: `ECUC:7380e54a-e891-4fb8-88e8-459dc7c59aaf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanControllerBaudrateConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains bit timing related configuration parameters of the CAN controller(s).

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CanControllerBaudRate

- **UUID**: `ECUC:e5ae7b80-e6c2-4e56-8ccd-5dce07379977`
- **参数名**: `CanControllerBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the baudrate of the controller in kbps.

######## 2. CanControllerPropSeg

- **UUID**: `ECUC:669827f7-fac2-42e8-870b-8003e83a0cbc`
- **参数名**: `CanControllerPropSeg`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies propagation delay in time quantas.

######## 3. CanControllerSeg1

- **UUID**: `ECUC:2ff9d8a8-d32b-4a08-85d7-8cc51effa452`
- **参数名**: `CanControllerSeg1`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 1 in time quantas.

######## 4. CanControllerSeg2

- **UUID**: `ECUC:755cccd2-d9a8-4df1-9cdb-6a9c5f850a12`
- **参数名**: `CanControllerSeg2`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies phase segment 2 in time quantas.

######## 5. CanControllerSyncJumpWidth

- **UUID**: `ECUC:70cfe32e-1160-408d-be3c-9e8a789a5bb9`
- **参数名**: `CanControllerSyncJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the synchronization jump width for the controller in time quantas.

##### 4. CanFilterMask

**容器属性**:

- **UUID**: `ECUC:be9f285a-0eda-475e-9def-ef440e3c84c2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanFilterMask`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of the CAN Filter Mask(s).

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanFilterMaskValue

- **UUID**: `ECUC:0b97bc36-d3d1-4d14-af96-e57e293fc3e1`
- **参数名**: `CanFilterMaskValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Describes a mask for hardware-based filtering of CAN identifiers. The CAN identifiers of incoming messages are masked with the appropriate CanFilterMaskValue. Bits holding a 0 mean don't care, i.e. do not compare the message's identifier in the respective bit position.

##### 5. CanTTController

**容器属性**:

- **UUID**: `ECUC:03522dfa-716f-4cae-b216-c32f5ff584ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTController`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

###### 参数配置

此容器包含 **18** 个参数：

####### INTEGER 类型参数

######## 1. CanTTControllerApplWatchdogLimit

- **UUID**: `ECUC:58bdc478-e74c-42df-8d3d-0ba19ae24008`
- **参数名**: `CanTTControllerApplWatchdogLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum time period (unit is 256 times NTU) after which the application has to serve the watchdog.

######## 2. CanTTControllerCycleCountMax

- **UUID**: `ECUC:fafa672b-b0c5-4c09-9035-06e2461576cf`
- **参数名**: `CanTTControllerCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the value for cycle_count_max.

######## 3. CanTTControllerExpectedTxTrigger

- **UUID**: `ECUC:91b067db-e57d-432f-9093-262d567242ec`
- **参数名**: `CanTTControllerExpectedTxTrigger`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of expected_tx_trigger.

######## 4. CanTTControllerInitialRefOffset

- **UUID**: `ECUC:25750102-31df-4bed-91cf-01253dc78faf`
- **参数名**: `CanTTControllerInitialRefOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the initial value for ref trigger offset.

######## 5. CanTTControllerInterruptEnable

- **UUID**: `ECUC:6d752b5f-31aa-4e11-915c-cbe1e1a0f01a`
- **参数名**: `CanTTControllerInterruptEnable`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the respective interrupts.

######## 6. CanTTControllerTimeMasterPriority

- **UUID**: `ECUC:64837877-30b7-48a4-9f87-a7e4e959010f`
- **参数名**: `CanTTControllerTimeMasterPriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the time master priority.

######## 7. CanTTControllerTxEnableWindowLength

- **UUID**: `ECUC:432b3c85-542c-48e3-ab51-3944e1d6e421`
- **参数名**: `CanTTControllerTxEnableWindowLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the tx enable window given in CAN bit times.

######## 8. CanTTControllerWatchTriggerGapTimeMark

- **UUID**: `ECUC:a880dad8-6591-4dbc-a3d4-8057ff9b6931`
- **参数名**: `CanTTControllerWatchTriggerGapTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark after a gap

######## 9. CanTTControllerWatchTriggerTimeMark

- **UUID**: `ECUC:496f1799-9365-4e5b-878a-dd8cab58f338`
- **参数名**: `CanTTControllerWatchTriggerTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: watch trigger time mark

####### BOOLEAN 类型参数

######## 1. CanTTControllerExternalClockSynchronisation

- **UUID**: `ECUC:1f319887-2617-4190-b5d6-95b9e555b180`
- **参数名**: `CanTTControllerExternalClockSynchronisation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the external clock synchronization.

######## 2. CanTTControllerGlobalTimeFiltering

- **UUID**: `ECUC:ced20e88-c426-42a9-bce0-ed1a2a5f3797`
- **参数名**: `CanTTControllerGlobalTimeFiltering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the global time filtering.

######## 3. CanTTControllerLevel2

- **UUID**: `ECUC:91462836-5301-42da-8b89-dad7c7ddeb2c`
- **参数名**: `CanTTControllerLevel2`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether Level 2 or Level 1 is used.

######## 4. CanTTControllerTURRestore

- **UUID**: `ECUC:e5b66746-4e6e-47f5-b62b-ab6452a49082`
- **参数名**: `CanTTControllerTURRestore`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the TUR restore.

######## 5. CanTTControllerTimeMaster

- **UUID**: `ECUC:68c24e85-bb75-4b38-b9af-05947b2f0f27`
- **参数名**: `CanTTControllerTimeMaster`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the controller acts as a potential time master.

####### FLOAT 类型参数

######## 1. CanTTControllerNTUConfig

- **UUID**: `ECUC:fc8b7d0e-677b-4c04-b547-ef6602271c33`
- **参数名**: `CanTTControllerNTUConfig`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the config value for NTU (network time unit).

######## 2. CanTTControllerSyncDeviation

- **UUID**: `ECUC:26f778c8-15de-4c4a-b05e-fff49e20b233`
- **参数名**: `CanTTControllerSyncDeviation`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum synchronization deviation:

####### ENUMERATION 类型参数

######## 1. CanTTControllerOperationMode

- **UUID**: `ECUC:fd04f084-a5cc-4c27-9d75-7e1a46e86bfa`
- **参数名**: `CanTTControllerOperationMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_EVENT_SYNC_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TIME_TRIGGERED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the operation mode.

######## 2. CanTTIRQProcessing

- **UUID**: `ECUC:089059db-bfe6-43a7-9fa7-99b4b583a2bf`
- **参数名**: `CanTTIRQProcessing`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `INTERRUPT` (来源: AUTOSAR_ECUC)
  - `POLLING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / disables API Can_MainFunction_BusOff() for handling busoff events in polling mode.

##### 6. CanHardwareObject

**容器属性**:

- **UUID**: `ECUC:ee3d6577-0017-42fc-b4d6-8d27c2e66563`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanHardwareObject`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of CAN Hardware Objects.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CanIdValue

- **UUID**: `ECUC:615fef00-eb96-4bbb-afd7-cef66a67db46`
- **参数名**: `CanIdValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies (together with the filter mask) the identifiers range that passes the hardware filter.

######## 2. CanObjectId

- **UUID**: `ECUC:5049e195-870c-490c-ac6d-745aae833d04`
- **参数名**: `CanObjectId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Holds the handle ID of HRH or HTH. The value of this parameter is unique in a given CAN Driver, and it should start with 0 and continue without any gaps.

####### ENUMERATION 类型参数

######## 1. CanHandleType

- **UUID**: `ECUC:6c58c09a-9aa2-4e4d-8ae3-8eba40a77aaf`
- **参数名**: `CanHandleType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BASIC` (来源: AUTOSAR_ECUC)
  - `FULL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the type (Full-CAN or Basic-CAN) of a hardware object.

######## 2. CanIdType

- **UUID**: `ECUC:f8442a9b-7752-416c-ac68-8cd3080589c0`
- **参数名**: `CanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `MIXED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether the IdValue is of type

######## 3. CanObjectType

- **UUID**: `ECUC:b8abf5c9-4e6a-46bf-a1ae-63b191e72d04`
- **参数名**: `CanObjectType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RECEIVE` (来源: AUTOSAR_ECUC)
  - `TRANSMIT` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if the HardwareObject is used as Transmit or as Receive object

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanControllerRef

- **UUID**: `ECUC:e2b98fcd-3e29-4041-a480-aed31e706d97`
- **引用名**: `CanControllerRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanController`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to CAN Controller to which the HOH is associated to.

######## 2. CanFilterMaskRef

- **UUID**: `ECUC:d0683493-3c90-46c3-815f-5a3dabb20a7a`
- **引用名**: `CanFilterMaskRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CanFilterMask`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController/CanFilterMask`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the filter mask that is used for hardware filtering together with the CAN_ID_VALUE.

######## 3. CanMainFunctionRWPeriodRef

- **UUID**: `ECUC:185477b7-2192-42b1-9dad-c72942a94b7c`
- **引用名**: `CanMainFunctionRWPeriodRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `CanMainFunctionRWPeriods`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanGeneral/CanMainFunctionRWPeriods`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to CAN Controller to which the HOH is associated to.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTTHardwareObjectTrigger

**容器属性**:

- **UUID**: `ECUC:5c10353d-3ba8-4140-adf6-b5c02d28c9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTHardwareObjectTrigger`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. CanTTHardwareObjectBaseCycle

- **UUID**: `ECUC:bbb7fda0-3f86-4144-b471-33793652290e`
- **参数名**: `CanTTHardwareObjectBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the cycle_offset.

########## 2. CanTTHardwareObjectCycleRepetition

- **UUID**: `ECUC:6f58e444-b305-47d4-899b-38971bc77aa6`
- **参数名**: `CanTTHardwareObjectCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repeat_factor.

########## 3. CanTTHardwareObjectTimeMark

- **UUID**: `ECUC:737166e8-39c4-4d60-ac3f-00672a8ebf66`
- **参数名**: `CanTTHardwareObjectTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the trigger will be activated.

########## 4. CanTTHardwareObjectTriggerId

- **UUID**: `ECUC:0da05573-613f-45fd-94f7-68688e7bcf18`
- **参数名**: `CanTTHardwareObjectTriggerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sequential number which allows separation of different TTCAN triggers configured for one and the same hardware object.

######### ENUMERATION 类型参数

########## 1. CanTTHardwareObjectTriggerType

- **UUID**: `ECUC:b15710a4-a4ef-45a8-830a-33d47a8b386c`
- **参数名**: `CanTTHardwareObjectTriggerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_RX_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER_GAP` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_EXCLUSIVE` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_MERGED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_SINGLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the trigger associated with the hardware object. This parameter depends on plain CAN parameter CAN_OBJECT_TYPE.

##### 7. CanTTHardwareObjectTrigger

**容器属性**:

- **UUID**: `ECUC:5c10353d-3ba8-4140-adf6-b5c02d28c9f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTTHardwareObjectTrigger`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN SWS is used and TTCAN is enabled.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. CanTTHardwareObjectBaseCycle

- **UUID**: `ECUC:bbb7fda0-3f86-4144-b471-33793652290e`
- **参数名**: `CanTTHardwareObjectBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the cycle_offset.

######## 2. CanTTHardwareObjectCycleRepetition

- **UUID**: `ECUC:6f58e444-b305-47d4-899b-38971bc77aa6`
- **参数名**: `CanTTHardwareObjectCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the repeat_factor.

######## 3. CanTTHardwareObjectTimeMark

- **UUID**: `ECUC:737166e8-39c4-4d60-ac3f-00672a8ebf66`
- **参数名**: `CanTTHardwareObjectTimeMark`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the trigger will be activated.

######## 4. CanTTHardwareObjectTriggerId

- **UUID**: `ECUC:0da05573-613f-45fd-94f7-68688e7bcf18`
- **参数名**: `CanTTHardwareObjectTriggerId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sequential number which allows separation of different TTCAN triggers configured for one and the same hardware object.

####### ENUMERATION 类型参数

######## 1. CanTTHardwareObjectTriggerType

- **UUID**: `ECUC:b15710a4-a4ef-45a8-830a-33d47a8b386c`
- **参数名**: `CanTTHardwareObjectTriggerType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_TT_RX_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_REF_TRIGGER_GAP` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_EXCLUSIVE` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_MERGED` (来源: AUTOSAR_ECUC)
  - `CAN_TT_TX_TRIGGER_SINGLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of the trigger associated with the hardware object. This parameter depends on plain CAN parameter CAN_OBJECT_TYPE.

##### 8. CanGeneral

**容器属性**:

- **UUID**: `ECUC:856dd730-a715-4e74-89f9-cd03e465c206`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the parameters related each CAN Driver Unit.

###### 参数配置

此容器包含 **12** 个参数：

####### INTEGER 类型参数

######## 1. CanIndex

- **UUID**: `ECUC:18b93eb8-b1dc-4779-9372-277b674dd618`
- **参数名**: `CanIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

####### BOOLEAN 类型参数

######## 1. CanChangeBaudrateApi

- **UUID**: `ECUC:68aba675-4594-4184-9615-4911b27827d4`
- **参数名**: `CanChangeBaudrateApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The support of the Can_ChangeBaudrate API is optional.

######## 2. CanDevErrorDetection

- **UUID**: `ECUC:00beaaf9-8ba3-448a-aa81-a27661c11c8b`
- **参数名**: `CanDevErrorDetection`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 3. CanHardwareCancellation

- **UUID**: `ECUC:ddb2d203-fc56-4784-98de-edbdb00d90ed`
- **参数名**: `CanHardwareCancellation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if hardware cancellation shall be supported.ON or OFF

######## 4. CanIdenticalIdCancellation

- **UUID**: `ECUC:33156f66-0274-4236-b05b-8cca84e9844f`
- **参数名**: `CanIdenticalIdCancellation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables cancellation of pending PDUs with identical ID.

######## 5. CanMultiplexedTransmission

- **UUID**: `ECUC:2eb95d32-92e6-407d-bae9-abac34896d07`
- **参数名**: `CanMultiplexedTransmission`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies if multiplexed transmission shall be supported.ON or OFF

######## 6. CanVersionInfoApi

- **UUID**: `ECUC:52d00b4f-174c-453b-8884-271b69795d80`
- **参数名**: `CanVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Can_GetVersionInfo() API ON or OFF.

####### FLOAT 类型参数

######## 1. CanMainFunctionBusoffPeriod

- **UUID**: `ECUC:12306b16-f8b2-418a-9262-e10b8222f967`
- **参数名**: `CanMainFunctionBusoffPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Busoff. Unit is seconds.

######## 2. CanMainFunctionModePeriod

- **UUID**: `ECUC:a4a82737-e923-4dd2-a0c3-8e56b5c0ce7c`
- **参数名**: `CanMainFunctionModePeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Mode. Unit is seconds.

######## 3. CanMainFunctionWakeupPeriod

- **UUID**: `ECUC:c25c3355-86db-4423-a9cb-3f081c873488`
- **参数名**: `CanMainFunctionWakeupPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Wakeup. Unit is seconds.

######## 4. CanTimeoutDuration

- **UUID**: `ECUC:b395c86f-3f7f-42d0-8b8a-94cdc17d2246`
- **参数名**: `CanTimeoutDuration`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the maximum time for blocking function until a timeout is detected. Unit is seconds.

####### FUNCTION-NAME 类型参数

######## 1. CanLPduReceiveCalloutFunction

- **UUID**: `ECUC:0bf48002-3ae8-405d-8e51-63cbb66a3f2a`
- **参数名**: `CanLPduReceiveCalloutFunction`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the existence and the name of a callout function that is called after a successful

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CanCounterRef

- **UUID**: `ECUC:0f0c8933-6ce9-4a53-90cc-31b61ca90e25`
- **引用名**: `CanCounterRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsCounter`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsCounter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains a reference to the counter, which is used by the CAN driver.

######## 2. CanSupportTTCANRef

- **UUID**: `ECUC:3fc9831b-0db6-41a2-8700-1b0dbcf79da4`
- **引用名**: `CanSupportTTCANRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfPrivateCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfPrivateCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to CanIfSupportTTCAN parameter in the CAN Interface Module configuration.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanMainFunctionRWPeriods

**容器属性**:

- **UUID**: `ECUC:e19259ca-56e6-476f-8828-152be61457d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanMainFunctionRWPeriods`
- **多重性**: [1..1]
- **多配置容器**: false

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. CanMainFunctionReadPeriod

- **UUID**: `ECUC:e168d193-1b8a-4de0-a93b-0993b8972e22`
- **参数名**: `CanMainFunctionReadPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..infinite]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Read. Unit is seconds. Different poll-cycles will be configurable if more than one CanMainFunctionReadPeriod is configured. In this case multiple Can_MainFunction_Read() will be provided by the CAN Driver module.

########## 2. CanMainFunctionWritePeriod

- **UUID**: `ECUC:3144d1f4-d927-4535-88fe-584a942a90c4`
- **参数名**: `CanMainFunctionWritePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..infinite]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Write. Unit is seconds. Different poll-cycles will be configurable if more than one CanMainFunctionWritePeriod is configured. In this case multiple Can_MainFunction_Write() will be provided by the CAN Driver module.

##### 9. CanMainFunctionRWPeriods

**容器属性**:

- **UUID**: `ECUC:e19259ca-56e6-476f-8828-152be61457d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanMainFunctionRWPeriods`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. CanMainFunctionReadPeriod

- **UUID**: `ECUC:e168d193-1b8a-4de0-a93b-0993b8972e22`
- **参数名**: `CanMainFunctionReadPeriod`
- **数据类型**: FLOAT
- **多重性**: [0..infinite]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Read. Unit is seconds. Different poll-cycles will be configurable if more than one CanMainFunctionReadPeriod is configured. In this case multiple Can_MainFunction_Read() will be provided by the CAN Driver module.

######## 2. CanMainFunctionWritePeriod

- **UUID**: `ECUC:3144d1f4-d927-4535-88fe-584a942a90c4`
- **参数名**: `CanMainFunctionWritePeriod`
- **数据类型**: FLOAT
- **多重性**: [0..infinite]
- **取值范围**: [0.001..65.535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter describes the period for cyclic call to Can_MainFunction_Write. Unit is seconds. Different poll-cycles will be configurable if more than one CanMainFunctionWritePeriod is configured. In this case multiple Can_MainFunction_Write() will be provided by the CAN Driver module.

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

1. **Can**
