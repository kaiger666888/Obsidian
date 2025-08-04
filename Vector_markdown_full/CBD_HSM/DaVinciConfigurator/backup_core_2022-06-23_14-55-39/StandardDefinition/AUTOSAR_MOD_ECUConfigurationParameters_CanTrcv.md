# CanTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:09

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanTrcv](#cantrcv)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanTrcv

#### 基本信息

- **UUID**: `ECUC:e1256557-38d2-4224-8563-f273b12e1ee8`
- **模块名称**: `CanTrcv`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the CanTrcv (CAN Transceiver driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **9** 个配置容器：

##### 1. CanTrcvConfigSet

**容器属性**:

- **UUID**: `ECUC:c20cd1af-0232-48fa-9f0b-f3d531f2fe20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This is the multiple configuration set container for CAN Transceiver.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTrcvSPICommRetries

- **UUID**: `ECUC:093c3711-8c92-4094-994a-a67de25b2cea`
- **参数名**: `CanTrcvSPICommRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the maximum number of communication retries in case of a failed SPI communication (applies both to timed out communication and to errors/NACK in the response data).

######## 2. CanTrcvSPICommTimeout

- **UUID**: `ECUC:a8bda218-8bf9-4dc0-86b1-cb9fa70fd9df`
- **参数名**: `CanTrcvSPICommTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the maximum time allowed to the CanTrcv for replying (either positively or negatively) to a SPI command.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. CanTrcvChannel

**容器属性**:

- **UUID**: `ECUC:4e6513a4-4c5a-4486-a836-f269d7e92dd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about a single CAN

######## 参数配置

此容器包含 **7** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvChannelId

- **UUID**: `ECUC:f1f3dba5-d4d7-43d3-8d03-2e0bb504e860`
- **参数名**: `CanTrcvChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of the CAN Transceiver Channel.

########## 2. CanTrcvMaxBaudrate

- **UUID**: `ECUC:b89bc632-1e2a-4709-ab62-957c7252e0fe`
- **参数名**: `CanTrcvMaxBaudrate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max baudrate for transceiver hardware type. Only used for validation purposes. Value shall be configured by configuration tool based on

######### BOOLEAN 类型参数

########## 1. CanTrcvChannelUsed

- **UUID**: `ECUC:88536366-15ed-4967-80dd-9974891b652e`
- **参数名**: `CanTrcvChannelUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Shall the related CAN transceiver channel be used?

########## 2. CanTrcvControlsPowerSupply

- **UUID**: `ECUC:1ab6ed3e-bf66-41ba-b2f6-a4d964b54744`
- **参数名**: `CanTrcvControlsPowerSupply`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is ECU power supply controlled by this transceiver?

########## 3. CanTrcvHwPnSupport

- **UUID**: `ECUC:ad140e6f-373b-4f3e-a7a5-87ba8b29e7e3`
- **参数名**: `CanTrcvHwPnSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the HW supports the selective wake-up function

########## 4. CanTrcvWakeupByBusUsed

- **UUID**: `ECUC:52db1d3e-02dd-4437-a377-00108ef8a886`
- **参数名**: `CanTrcvWakeupByBusUsed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is wake up by bus supported? If CAN transceiver hardware does not support wake up by bus value is always FALSE. If CAN transceiver hardware supports wake up by bus value is TRUE or FALSE depending whether it is used or not.

######### ENUMERATION 类型参数

########## 1. CanTrcvInitState

- **UUID**: `ECUC:8e511d66-410f-4c0c-8540-01776a793337`
- **参数名**: `CanTrcvInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CANTRCV_OP_MODE_NORMAL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTRCV_OP_MODE_NORMAL` (来源: AUTOSAR_ECUC)
  - `CANTRCV_OP_MODE_SLEEP` (来源: AUTOSAR_ECUC)
  - `CANTRCV_OP_MODE_STANDBY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: State of CAN transceiver after call to CanTrcv_Init.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTrcvWakeupSourceRef

- **UUID**: `ECUC:b00d0abd-0eaa-4026-9ec9-b035bb76ae17`
- **引用名**: `CanTrcvWakeupSourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a wakeup source in the EcuM configuration.

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. CanTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

############ 参数配置

此容器包含 **1** 个参数：

############# STRING 类型参数

############## 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

############ 引用关系

此容器包含 **1** 个引用：

############# CHOICE-REFERENCE 类型引用

############## 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

######### 2. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

######### 3. CanTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvSpiSequence`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about one SPI sequence.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. CanTrcvSpiAccessSynchronous

- **UUID**: `ECUC:7bcf2b70-75a7-41b5-ad47-bc7bfd282257`
- **参数名**: `CanTrcvSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CanTrcvSpiSequenceName

- **UUID**: `ECUC:67fba62d-4920-4112-80e9-839907bcc46a`
- **引用名**: `CanTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

######### 4. CanTrcvPartialNetwork

**容器属性**:

- **UUID**: `ECUC:ca5b30fc-a757-4af2-bd25-7f0bf8a13690`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPartialNetwork`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about the configuration of Partial Networking functionality.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. CanTrcvBaudRate

- **UUID**: `ECUC:9ab3dac1-5cd1-4a6b-a556-dbcb6bf39ff5`
- **参数名**: `CanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the CAN Bus communication baud rate in kbps.

############ 2. CanTrcvPnFrameCanId

- **UUID**: `ECUC:4eadd3d6-3770-462b-a515-9a677fe5d057`
- **参数名**: `CanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN ID of the Wake-up Frame (WUF).

############ 3. CanTrcvPnFrameCanIdMask

- **UUID**: `ECUC:138f069a-dcc3-403d-9398-9d247ccefbf8`
- **参数名**: `CanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID Mask for the selective activation of the transceiver. It is used to enableFrame Wake-up (WUF) on a group of IDs.

############ 4. CanTrcvPnFrameDlc

- **UUID**: `ECUC:35e1b603-21c3-4bad-aca7-ff1081d6f632`
- **参数名**: `CanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length of the Wake-up Frame (WUF).

########### BOOLEAN 类型参数

############ 1. CanTrcvBusErrFlag

- **UUID**: `ECUC:e7104ca6-1fad-4cfd-92c2-b18fac5c8a05`
- **参数名**: `CanTrcvBusErrFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates if the Bus Error (BUSERR) flag is managed by the BSW. This flag is set if a bus failure is detected by the transceiver.

############ 2. CanTrcvPnCanIdIsExtended

- **UUID**: `ECUC:bce803d7-e415-4177-a29f-ff17bdac4793`
- **参数名**: `CanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether extended or standard ID is used.

############ 3. CanTrcvPnEnabled

- **UUID**: `ECUC:a5cd2332-0b8f-4e8b-93f0-8c20e953d527`
- **参数名**: `CanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the selective wake-up function is enabled or disabled in HW.

############ 4. CanTrcvPowerOnFlag

- **UUID**: `ECUC:869324cb-1350-4b1c-b366-5b8b609b4ffc`
- **参数名**: `CanTrcvPowerOnFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Indicates if the Power On Reset (POR) flag is available and is managed by the transceiver.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############## 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

######### 5. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

######### 6. CanTrcvAccess

**容器属性**:

- **UUID**: `ECUC:9175045e-5280-4caf-a0c4-9033cb129316`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `CanTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **CanTrcvDioAccess**
  - UUID: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
  - 描述: Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.
- **CanTrcvDioChannelAccess**
  - UUID: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
  - 描述: Container gives DIO channel access by single Can transceiver channel.
- **CanTrcvSpiSequence**
  - UUID: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
  - 描述: Container gives CAN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives CanTrcv Driver information about access to a single CAN transceiver.

####### 2. CanTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

####### 3. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

####### 4. CanTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvSpiSequence`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about one SPI sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. CanTrcvSpiAccessSynchronous

- **UUID**: `ECUC:7bcf2b70-75a7-41b5-ad47-bc7bfd282257`
- **参数名**: `CanTrcvSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanTrcvSpiSequenceName

- **UUID**: `ECUC:67fba62d-4920-4112-80e9-839907bcc46a`
- **引用名**: `CanTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

####### 5. CanTrcvPartialNetwork

**容器属性**:

- **UUID**: `ECUC:ca5b30fc-a757-4af2-bd25-7f0bf8a13690`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPartialNetwork`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about the configuration of Partial Networking functionality.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvBaudRate

- **UUID**: `ECUC:9ab3dac1-5cd1-4a6b-a556-dbcb6bf39ff5`
- **参数名**: `CanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the CAN Bus communication baud rate in kbps.

########## 2. CanTrcvPnFrameCanId

- **UUID**: `ECUC:4eadd3d6-3770-462b-a515-9a677fe5d057`
- **参数名**: `CanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN ID of the Wake-up Frame (WUF).

########## 3. CanTrcvPnFrameCanIdMask

- **UUID**: `ECUC:138f069a-dcc3-403d-9398-9d247ccefbf8`
- **参数名**: `CanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID Mask for the selective activation of the transceiver. It is used to enableFrame Wake-up (WUF) on a group of IDs.

########## 4. CanTrcvPnFrameDlc

- **UUID**: `ECUC:35e1b603-21c3-4bad-aca7-ff1081d6f632`
- **参数名**: `CanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length of the Wake-up Frame (WUF).

######### BOOLEAN 类型参数

########## 1. CanTrcvBusErrFlag

- **UUID**: `ECUC:e7104ca6-1fad-4cfd-92c2-b18fac5c8a05`
- **参数名**: `CanTrcvBusErrFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates if the Bus Error (BUSERR) flag is managed by the BSW. This flag is set if a bus failure is detected by the transceiver.

########## 2. CanTrcvPnCanIdIsExtended

- **UUID**: `ECUC:bce803d7-e415-4177-a29f-ff17bdac4793`
- **参数名**: `CanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether extended or standard ID is used.

########## 3. CanTrcvPnEnabled

- **UUID**: `ECUC:a5cd2332-0b8f-4e8b-93f0-8c20e953d527`
- **参数名**: `CanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the selective wake-up function is enabled or disabled in HW.

########## 4. CanTrcvPowerOnFlag

- **UUID**: `ECUC:869324cb-1350-4b1c-b366-5b8b609b4ffc`
- **参数名**: `CanTrcvPowerOnFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Indicates if the Power On Reset (POR) flag is available and is managed by the transceiver.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

####### 6. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

####### 7. CanTrcvAccess

**容器属性**:

- **UUID**: `ECUC:9175045e-5280-4caf-a0c4-9033cb129316`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `CanTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **CanTrcvDioAccess**
  - UUID: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
  - 描述: Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.
- **CanTrcvDioChannelAccess**
  - UUID: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
  - 描述: Container gives DIO channel access by single Can transceiver channel.
- **CanTrcvSpiSequence**
  - UUID: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
  - 描述: Container gives CAN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives CanTrcv Driver information about access to a single CAN transceiver.

##### 2. CanTrcvChannel

**容器属性**:

- **UUID**: `ECUC:4e6513a4-4c5a-4486-a836-f269d7e92dd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about a single CAN

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. CanTrcvChannelId

- **UUID**: `ECUC:f1f3dba5-d4d7-43d3-8d03-2e0bb504e860`
- **参数名**: `CanTrcvChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of the CAN Transceiver Channel.

######## 2. CanTrcvMaxBaudrate

- **UUID**: `ECUC:b89bc632-1e2a-4709-ab62-957c7252e0fe`
- **参数名**: `CanTrcvMaxBaudrate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max baudrate for transceiver hardware type. Only used for validation purposes. Value shall be configured by configuration tool based on

####### BOOLEAN 类型参数

######## 1. CanTrcvChannelUsed

- **UUID**: `ECUC:88536366-15ed-4967-80dd-9974891b652e`
- **参数名**: `CanTrcvChannelUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Shall the related CAN transceiver channel be used?

######## 2. CanTrcvControlsPowerSupply

- **UUID**: `ECUC:1ab6ed3e-bf66-41ba-b2f6-a4d964b54744`
- **参数名**: `CanTrcvControlsPowerSupply`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is ECU power supply controlled by this transceiver?

######## 3. CanTrcvHwPnSupport

- **UUID**: `ECUC:ad140e6f-373b-4f3e-a7a5-87ba8b29e7e3`
- **参数名**: `CanTrcvHwPnSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the HW supports the selective wake-up function

######## 4. CanTrcvWakeupByBusUsed

- **UUID**: `ECUC:52db1d3e-02dd-4437-a377-00108ef8a886`
- **参数名**: `CanTrcvWakeupByBusUsed`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is wake up by bus supported? If CAN transceiver hardware does not support wake up by bus value is always FALSE. If CAN transceiver hardware supports wake up by bus value is TRUE or FALSE depending whether it is used or not.

####### ENUMERATION 类型参数

######## 1. CanTrcvInitState

- **UUID**: `ECUC:8e511d66-410f-4c0c-8540-01776a793337`
- **参数名**: `CanTrcvInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `CANTRCV_OP_MODE_NORMAL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTRCV_OP_MODE_NORMAL` (来源: AUTOSAR_ECUC)
  - `CANTRCV_OP_MODE_SLEEP` (来源: AUTOSAR_ECUC)
  - `CANTRCV_OP_MODE_STANDBY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: State of CAN transceiver after call to CanTrcv_Init.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTrcvWakeupSourceRef

- **UUID**: `ECUC:b00d0abd-0eaa-4026-9ec9-b035bb76ae17`
- **引用名**: `CanTrcvWakeupSourceRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a wakeup source in the EcuM configuration.

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. CanTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

####### 2. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

####### 3. CanTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvSpiSequence`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about one SPI sequence.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. CanTrcvSpiAccessSynchronous

- **UUID**: `ECUC:7bcf2b70-75a7-41b5-ad47-bc7bfd282257`
- **参数名**: `CanTrcvSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanTrcvSpiSequenceName

- **UUID**: `ECUC:67fba62d-4920-4112-80e9-839907bcc46a`
- **引用名**: `CanTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

####### 4. CanTrcvPartialNetwork

**容器属性**:

- **UUID**: `ECUC:ca5b30fc-a757-4af2-bd25-7f0bf8a13690`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPartialNetwork`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about the configuration of Partial Networking functionality.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvBaudRate

- **UUID**: `ECUC:9ab3dac1-5cd1-4a6b-a556-dbcb6bf39ff5`
- **参数名**: `CanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the CAN Bus communication baud rate in kbps.

########## 2. CanTrcvPnFrameCanId

- **UUID**: `ECUC:4eadd3d6-3770-462b-a515-9a677fe5d057`
- **参数名**: `CanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN ID of the Wake-up Frame (WUF).

########## 3. CanTrcvPnFrameCanIdMask

- **UUID**: `ECUC:138f069a-dcc3-403d-9398-9d247ccefbf8`
- **参数名**: `CanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID Mask for the selective activation of the transceiver. It is used to enableFrame Wake-up (WUF) on a group of IDs.

########## 4. CanTrcvPnFrameDlc

- **UUID**: `ECUC:35e1b603-21c3-4bad-aca7-ff1081d6f632`
- **参数名**: `CanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length of the Wake-up Frame (WUF).

######### BOOLEAN 类型参数

########## 1. CanTrcvBusErrFlag

- **UUID**: `ECUC:e7104ca6-1fad-4cfd-92c2-b18fac5c8a05`
- **参数名**: `CanTrcvBusErrFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates if the Bus Error (BUSERR) flag is managed by the BSW. This flag is set if a bus failure is detected by the transceiver.

########## 2. CanTrcvPnCanIdIsExtended

- **UUID**: `ECUC:bce803d7-e415-4177-a29f-ff17bdac4793`
- **参数名**: `CanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether extended or standard ID is used.

########## 3. CanTrcvPnEnabled

- **UUID**: `ECUC:a5cd2332-0b8f-4e8b-93f0-8c20e953d527`
- **参数名**: `CanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the selective wake-up function is enabled or disabled in HW.

########## 4. CanTrcvPowerOnFlag

- **UUID**: `ECUC:869324cb-1350-4b1c-b366-5b8b609b4ffc`
- **参数名**: `CanTrcvPowerOnFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Indicates if the Power On Reset (POR) flag is available and is managed by the transceiver.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

############ 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

####### 5. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

####### 6. CanTrcvAccess

**容器属性**:

- **UUID**: `ECUC:9175045e-5280-4caf-a0c4-9033cb129316`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `CanTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **CanTrcvDioAccess**
  - UUID: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
  - 描述: Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.
- **CanTrcvDioChannelAccess**
  - UUID: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
  - 描述: Container gives DIO channel access by single Can transceiver channel.
- **CanTrcvSpiSequence**
  - UUID: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
  - 描述: Container gives CAN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives CanTrcv Driver information about access to a single CAN transceiver.

##### 3. CanTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

##### 4. CanTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives DIO channel access by single Can transceiver channel.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. CanTrcvHardwareInterfaceName

- **UUID**: `ECUC:0ec03d65-0055-4853-8dc8-5fcd1ef5a43e`
- **参数名**: `CanTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. CanTrcvDioSymNameRef

- **UUID**: `ECUC:1e464264-ce16-4a16-87d1-89aab53d6a2b`
- **引用名**: `CanTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the CANTRCV_DIO_PORT_SYM_NAME,  CANTRCV_DIO_CHANNEL_SYM_NAME and  CANTRCV_DIO_GROUP_SYM_NAME references in the Can Trcv SWS.

##### 5. CanTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvSpiSequence`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about one SPI sequence.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. CanTrcvSpiAccessSynchronous

- **UUID**: `ECUC:7bcf2b70-75a7-41b5-ad47-bc7bfd282257`
- **参数名**: `CanTrcvSpiAccessSynchronous`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to define whether the access to the Spi sequence is synchronous or asynchronous.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanTrcvSpiSequenceName

- **UUID**: `ECUC:67fba62d-4920-4112-80e9-839907bcc46a`
- **引用名**: `CanTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..infinite]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

##### 6. CanTrcvPartialNetwork

**容器属性**:

- **UUID**: `ECUC:ca5b30fc-a757-4af2-bd25-7f0bf8a13690`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPartialNetwork`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver information about the configuration of Partial Networking functionality.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. CanTrcvBaudRate

- **UUID**: `ECUC:9ab3dac1-5cd1-4a6b-a556-dbcb6bf39ff5`
- **参数名**: `CanTrcvBaudRate`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the CAN Bus communication baud rate in kbps.

######## 2. CanTrcvPnFrameCanId

- **UUID**: `ECUC:4eadd3d6-3770-462b-a515-9a677fe5d057`
- **参数名**: `CanTrcvPnFrameCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN ID of the Wake-up Frame (WUF).

######## 3. CanTrcvPnFrameCanIdMask

- **UUID**: `ECUC:138f069a-dcc3-403d-9398-9d247ccefbf8`
- **参数名**: `CanTrcvPnFrameCanIdMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ID Mask for the selective activation of the transceiver. It is used to enableFrame Wake-up (WUF) on a group of IDs.

######## 4. CanTrcvPnFrameDlc

- **UUID**: `ECUC:35e1b603-21c3-4bad-aca7-ff1081d6f632`
- **参数名**: `CanTrcvPnFrameDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length of the Wake-up Frame (WUF).

####### BOOLEAN 类型参数

######## 1. CanTrcvBusErrFlag

- **UUID**: `ECUC:e7104ca6-1fad-4cfd-92c2-b18fac5c8a05`
- **参数名**: `CanTrcvBusErrFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates if the Bus Error (BUSERR) flag is managed by the BSW. This flag is set if a bus failure is detected by the transceiver.

######## 2. CanTrcvPnCanIdIsExtended

- **UUID**: `ECUC:bce803d7-e415-4177-a29f-ff17bdac4793`
- **参数名**: `CanTrcvPnCanIdIsExtended`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether extended or standard ID is used.

######## 3. CanTrcvPnEnabled

- **UUID**: `ECUC:a5cd2332-0b8f-4e8b-93f0-8c20e953d527`
- **参数名**: `CanTrcvPnEnabled`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether the selective wake-up function is enabled or disabled in HW.

######## 4. CanTrcvPowerOnFlag

- **UUID**: `ECUC:869324cb-1350-4b1c-b366-5b8b609b4ffc`
- **参数名**: `CanTrcvPowerOnFlag`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Description: Indicates if the Power On Reset (POR) flag is available and is managed by the transceiver.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

########## 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

##### 7. CanTrcvPnFrameDataMaskSpec

**容器属性**:

- **UUID**: `ECUC:a8cf14ab-3c00-4929-adf3-38a776992bf6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvPnFrameDataMaskSpec`
- **多重性**: [0..8]
- **多配置容器**: false

**容器描述**:

Defines data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTrcvPnFrameDataMask

- **UUID**: `ECUC:656a6966-3a40-4948-9b0a-562933acdeb9`
- **参数名**: `CanTrcvPnFrameDataMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the n byte (Byte0 = LSB) of the data payload mask to be used on the received payload in order to determine if the transceiver must be woken up by the received Wake-up Frame (WUF).

######## 2. CanTrcvPnFrameDataMaskIndex

- **UUID**: `ECUC:9693190e-eb2c-4688-a833-a834acc4d8d2`
- **参数名**: `CanTrcvPnFrameDataMaskIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: holds the position n in frame of the mask-part

##### 8. CanTrcvGeneral

**容器属性**:

- **UUID**: `ECUC:fce14966-e5e5-4705-80b8-c0fedce975d9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTrcvGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container gives CAN transceiver driver basic information.

###### 参数配置

此容器包含 **6** 个参数：

####### INTEGER 类型参数

######## 1. CanTrcvSPICommRetries

- **UUID**: `ECUC:220ac6dc-bb8e-451b-a63b-63d7aa6307ef`
- **参数名**: `CanTrcvSPICommRetries`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the maximal number of communication retries in case of failed SPI communication (applies both to timed out communication and to errors/NACK in the response data).

######## 2. CanTrcvSPICommTimeout

- **UUID**: `ECUC:4807a785-38d3-426c-ad25-f1d9988e46c4`
- **参数名**: `CanTrcvSPICommTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the maximal time allowed to the Transceiver in order to reply

######## 3. CanTrcvWaitCount

- **UUID**: `ECUC:3c48b6f3-61ff-4bd9-be07-4e0ed8351855`
- **参数名**: `CanTrcvWaitCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates the number of wait states to change the transceiver operation mode. Transceiver hardware may need wait states for some transitions.

####### BOOLEAN 类型参数

######## 1. CanTrcvDevErrorDetect

- **UUID**: `ECUC:305a9a10-11cc-4baf-a909-107f41bc5ad4`
- **参数名**: `CanTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches development error detection and notification on and off.

######## 2. CanTrcvGetVersionInfo

- **UUID**: `ECUC:2d33aa8f-dca2-4d91-bad7-b9cd268b182e`
- **参数名**: `CanTrcvGetVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches version information API on and off. If switched off, function need not be present in compiled code.

####### ENUMERATION 类型参数

######## 1. CanTrcvWakeUpSupport

- **UUID**: `ECUC:95db2b45-712c-42e8-88d9-8ca25bf4cd4d`
- **参数名**: `CanTrcvWakeUpSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CANTRCV_WAKEUP_BY_POLLING` (来源: AUTOSAR_ECUC)
  - `CANTRCV_WAKEUP_NOT_SUPPORTED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Informs whether wake up is supported by polling or not supported. In case no

##### 9. CanTrcvAccess

**容器属性**:

- **UUID**: `ECUC:9175045e-5280-4caf-a0c4-9033cb129316`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `CanTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **CanTrcvDioAccess**
  - UUID: `ECUC:1d8e654e-9746-428f-929d-ddefe3a44578`
  - 描述: Container gives CAN transceiver driver information about accessing ports and port pins. In addition relation between CAN transceiver hardware pin names and Dio port access information is given.
- **CanTrcvDioChannelAccess**
  - UUID: `ECUC:f3735ce7-dc10-4544-b55e-626808f713e0`
  - 描述: Container gives DIO channel access by single Can transceiver channel.
- **CanTrcvSpiSequence**
  - UUID: `ECUC:9b42b06c-0a7a-45e1-bd04-40ea181004db`
  - 描述: Container gives CAN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives CanTrcv Driver information about access to a single CAN transceiver.

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

1. **CanTrcv**
