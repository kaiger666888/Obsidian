# LinTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:26

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LinTrcv](#lintrcv)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LinTrcv

#### 基本信息

- **UUID**: `ECUC:c59b866e-f4e6-458a-9035-29a85b418af1`
- **模块名称**: `LinTrcv`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of LIN Transceiver Driver module

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. LinTrcvChannel

**容器属性**:

- **UUID**: `ECUC:5519f98a-d432-484f-b653-445226eca31a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver information about a single LIN transceiver channel. Any LIN transceiver driver has such LIN transceiver channels.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinTrcvChannelId

- **UUID**: `ECUC:ea720240-7002-4a3b-8cec-9e7d8615d120`
- **参数名**: `LinTrcvChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of the LIN Transceiver Channel.

####### BOOLEAN 类型参数

######## 1. LinTrcvChannelUsed

- **UUID**: `ECUC:884f60c8-028b-4855-aff0-3f97451c988e`
- **参数名**: `LinTrcvChannelUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Shall the related LIN transceiver channel be used?

######## 2. LinTrcvWakeupByBusUsed

- **UUID**: `ECUC:7f058deb-29b5-4646-a085-759f9a2406cd`
- **参数名**: `LinTrcvWakeupByBusUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is wake up by bus supported? If LIN transceiver hardware does not support wake up by bus value is always FALSE. If LIN transceiver hardware supports wake up by bus value is TRUE or FALSE depending whether it is used or not.

####### ENUMERATION 类型参数

######## 1. LinTrcvInitState

- **UUID**: `ECUC:4e9ab320-a49a-456e-a4b4-90244009f7ea`
- **参数名**: `LinTrcvInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LINTRCV_TRCV_MODE_NORMAL` (来源: AUTOSAR_ECUC)
  - `LINTRCV_TRCV_MODE_SLEEP` (来源: AUTOSAR_ECUC)
  - `LINTRCV_TRCV_MODE_STANDBY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: State of LIN transceiver after call to LinTrcv_Init.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinTrcvIcuChannelRef

- **UUID**: `ECUC:0b855299-4d08-4de1-a437-5059825c76ea`
- **引用名**: `LinTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the IcuChannel to enable/disable the interrupts for wakeups.

######## 2. LinTrcvWakeupSourceRef

- **UUID**: `ECUC:6c159cde-405c-4220-b459-9036157b36b8`
- **引用名**: `LinTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a wakeup source in the EcuM configuration. This reference is only needed if LinTrcvWakeupByBusUsed is true. Implementation Type: reference to EcuM_WakeupSourceType.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. LinTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:5097db74-73a0-4c39-a04d-2bc2b00d47ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver information about accessing ports and port pins. In addition relation between LIN transceiver hardware pin names and Dio port access information is given. If a LIN transceiver hardware has no Dio interface, there is no instance of this container.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. LinTrcvHardwareInterfaceName

- **UUID**: `ECUC:1bb5ccfc-4a1b-4d05-94aa-b4f31d5fe9ae`
- **参数名**: `LinTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either LINTRCV_DIO_PORT_SYMBOLIC_NAME or LINTRCV_DIO_CHANNEL_SYMBOLIC_NAME or LINTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The LIN transceiver driver implementation description shall list up this name for the appropriate LIN transceiver hardware.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. LinTrcvDioSymRefName

- **UUID**: `ECUC:de9282c6-6a65-47db-95ff-aa3fe4b97a0a`
- **引用名**: `LinTrcvDioSymRefName`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the LINTRCV_DIO_PORT_SYM_NAME, LINTRCV_DIO_CHANNEL_SYM_NAME and LINTRCV_DIO_GROUP_SYM_NAME references in the Lin Trcv SWS.

####### 2. LinTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:b4dd521f-0d5c-4e82-b30d-8a192720ba27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvSpiSequence`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver information about one SPI sequence.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinTrcvSpiSequenceName

- **UUID**: `ECUC:606dedc9-d5fb-4881-b88f-f39e2c10008a`
- **引用名**: `LinTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

####### 3. LinTrcvAccess

**容器属性**:

- **UUID**: `ECUC:5eacba8a-9292-46db-a06e-3a7cf400b449`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **LinTrcvDioAccess**
  - UUID: `ECUC:5097db74-73a0-4c39-a04d-2bc2b00d47ef`
  - 描述: Container gives LIN transceiver driver information about accessing ports and port pins. In addition relation between LIN transceiver hardware pin names and Dio port access information is given. If a LIN transceiver hardware has no Dio interface, there is no instance of this container.
- **LinTrcvSpiSequence**
  - UUID: `ECUC:b4dd521f-0d5c-4e82-b30d-8a192720ba27`
  - 描述: Container gives LIN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives LIN transceiver driver access about a single LIN transceiver channel.

##### 2. LinTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:5097db74-73a0-4c39-a04d-2bc2b00d47ef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver information about accessing ports and port pins. In addition relation between LIN transceiver hardware pin names and Dio port access information is given. If a LIN transceiver hardware has no Dio interface, there is no instance of this container.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. LinTrcvHardwareInterfaceName

- **UUID**: `ECUC:1bb5ccfc-4a1b-4d05-94aa-b4f31d5fe9ae`
- **参数名**: `LinTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either LINTRCV_DIO_PORT_SYMBOLIC_NAME or LINTRCV_DIO_CHANNEL_SYMBOLIC_NAME or LINTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The LIN transceiver driver implementation description shall list up this name for the appropriate LIN transceiver hardware.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. LinTrcvDioSymRefName

- **UUID**: `ECUC:de9282c6-6a65-47db-95ff-aa3fe4b97a0a`
- **引用名**: `LinTrcvDioSymRefName`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the LINTRCV_DIO_PORT_SYM_NAME, LINTRCV_DIO_CHANNEL_SYM_NAME and LINTRCV_DIO_GROUP_SYM_NAME references in the Lin Trcv SWS.

##### 3. LinTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:b4dd521f-0d5c-4e82-b30d-8a192720ba27`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvSpiSequence`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver information about one SPI sequence.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinTrcvSpiSequenceName

- **UUID**: `ECUC:606dedc9-d5fb-4881-b88f-f39e2c10008a`
- **引用名**: `LinTrcvSpiSequenceName`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

##### 4. LinTrcvGeneral

**容器属性**:

- **UUID**: `ECUC:f54ae770-970c-4e6f-9558-edcb05029375`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinTrcvGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container gives LIN transceiver driver basic information.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. LinTrcvIndex

- **UUID**: `ECUC:77460cdb-d56a-4a49-8614-b9e15d69dc07`
- **参数名**: `LinTrcvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. LinTrcvWaitCount

- **UUID**: `ECUC:6ed49957-dbf9-4059-927d-8c3f990fca2f`
- **参数名**: `LinTrcvWaitCount`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Wait count for transceiver state changes.

####### BOOLEAN 类型参数

######## 1. LinTrcvDevErrorDetect

- **UUID**: `ECUC:4fc91bfc-86af-4a83-99a7-973f2b5be813`
- **参数名**: `LinTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches development error detection and notification on and off. If switched on, #define LINTRCV_DEV_ERROR_DETECT ON shall be generated. If switched off, #define LINTRCV_DEV_ERROR_DETECT OFF shall be generated. Define shall be part of file LinTrcv_Cfg.h.

######## 2. LinTrcvGetVersionInfo

- **UUID**: `ECUC:88361779-3793-47d9-8acc-ad065a048c2d`
- **参数名**: `LinTrcvGetVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches version information API on and off. If switched off, function need not be present in compiled code.

######## 3. LinTrcvWakeUpSupport

- **UUID**: `ECUC:6da8ded4-8d8a-4f7d-97de-c40d9e3b8ee4`
- **参数名**: `LinTrcvWakeUpSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Informs whether wake up is supported or not. In case wake up is not supported by LIN transceiver hardware the setting shall be false. The wake up ability may be switched on or off for each channel of one LIN transceiver by LinTrcvWakeupSourceRef.

##### 5. LinTrcvAccess

**容器属性**:

- **UUID**: `ECUC:5eacba8a-9292-46db-a06e-3a7cf400b449`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **LinTrcvDioAccess**
  - UUID: `ECUC:5097db74-73a0-4c39-a04d-2bc2b00d47ef`
  - 描述: Container gives LIN transceiver driver information about accessing ports and port pins. In addition relation between LIN transceiver hardware pin names and Dio port access information is given. If a LIN transceiver hardware has no Dio interface, there is no instance of this container.
- **LinTrcvSpiSequence**
  - UUID: `ECUC:b4dd521f-0d5c-4e82-b30d-8a192720ba27`
  - 描述: Container gives LIN transceiver driver information about one SPI sequence.

**容器描述**:

Container gives LIN transceiver driver access about a single LIN transceiver channel.

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

1. **LinTrcv**
