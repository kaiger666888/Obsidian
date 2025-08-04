# FrTrcv - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:47

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrTrcv](#frtrcv)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrTrcv

#### 基本信息

- **UUID**: `ECUC:71aa9d63-f92e-4346-88ee-2d691845f729`
- **模块名称**: `FrTrcv`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FrTrcv (FlexRay Transceiver driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **8** 个配置容器：

##### 1. FrTrcvChannel

**容器属性**:

- **UUID**: `ECUC:27a48bc7-ab60-4e05-b3c9-6cb90cc0e80d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Container gives FlexRay transceiver driver information about a single FlexRay transceiver channel.

###### 参数配置

此容器包含 **7** 个参数：

####### INTEGER 类型参数

######## 1. FrTrcvChannelId

- **UUID**: `ECUC:67510191-07a2-4733-bacb-b855ed5e9848`
- **参数名**: `FrTrcvChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique identifier of the FlexRay Transceiver Channel.

####### BOOLEAN 类型参数

######## 1. FrTrcvChannelUsed

- **UUID**: `ECUC:3c0da124-1720-4525-9c77-6197ec38db66`
- **参数名**: `FrTrcvChannelUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Shall the related FlexRay transceiver channel be used?

######## 2. FrTrcvControlsPowerSupply

- **UUID**: `ECUC:c0cabff2-370d-46a9-898e-642bd09bc754`
- **参数名**: `FrTrcvControlsPowerSupply`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is ECU power supply controlled by this transceiver?

######## 3. FrTrcvWakeupByBusUsed

- **UUID**: `ECUC:89e14001-00b1-46e0-9477-f15b92505ef8`
- **参数名**: `FrTrcvWakeupByBusUsed`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Is wake up by node supported? If FlexRay transceiver hardware does not support wake up by node value is always FALSE. If FlexRay transceiver hardware supports wake up by node value is TRUE or FALSE depending whether it is used or not.

####### ENUMERATION 类型参数

######## 1. FrTrcvInitState

- **UUID**: `ECUC:bdad88e9-d322-46c4-b541-bd98b14993a6`
- **参数名**: `FrTrcvInitState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `FRTRCV_OP_MODE_NORMAL`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRTRCV_TRCVMODE_NORMAL` (来源: AUTOSAR_ECUC)
  - `FRTRCV_TRCVMODE_RECEIVEONLY` (来源: AUTOSAR_ECUC)
  - `FRTRCV_TRCVMODE_SLEEP` (来源: AUTOSAR_ECUC)
  - `FRTRCV_TRCVMODE_STANDBY` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: State of FlexRay transceiver after power on.

######## 2. FrTrcvMaxBaudrate

- **UUID**: `ECUC:0a4a52b2-f873-4328-a06f-23c424748826`
- **参数名**: `FrTrcvMaxBaudrate`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_10M` (来源: AUTOSAR_ECUC)
  - `FR_2M5` (来源: AUTOSAR_ECUC)
  - `FR_5M0` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max baudrate for transceiver hardware type. Only used for validation purposes. Value shall be configured by configuration tool based on

####### FUNCTION-NAME 类型参数

######## 1. FrTrcvEnableInterruptCallout

- **UUID**: `ECUC:b7d9b677-ea64-4b95-928c-52e149bbfd47`
- **参数名**: `FrTrcvEnableInterruptCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the existence and the name of a callout function that enables the interrupt pin for the wakeup. If this parameter is omitted no callout shall take place.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrTrcvIcuChannelRef

- **UUID**: `ECUC:41f5e91b-e5b1-4d1b-8c4d-dedbed7268a1`
- **引用名**: `FrTrcvIcuChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `IcuChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Icu/IcuConfigSet/IcuChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the IcuChannel to enable/disable the interrupts for wakeups.

######## 2. FrTrcvWakeupSourceRef

- **UUID**: `ECUC:457a74d4-b12c-4daf-ba4e-671aa8b5e471`
- **引用名**: `FrTrcvWakeupSourceRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `EcuMWakeupSource`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuM/EcuMConfiguration/EcuMCommonConfiguration/EcuMWakeupSource`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a wakeup source in the EcuM configuration. If

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. FrTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:017c4e37-64c2-49c3-96dc-3e8581246ed7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives FR transceiver driver information about accessing ports and port pins. If a FR transceiver hardware has no Dio interface, there is no instance of this container.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. FrTrcvHardwareInterfaceName

- **UUID**: `ECUC:3801a24c-fcd3-4f0f-acc3-3d9768c585e9`
- **参数名**: `FrTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FR transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either FRTRCV_DIO_PORT_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The FR transceiver driver implementation description shall list up this name for the appropriate FR transceiver hardware.

########## 引用关系

此容器包含 **1** 个引用：

########### CHOICE-REFERENCE 类型引用

############ 1. FrTrcvDioSymNameRef

- **UUID**: `ECUC:203b8070-d42e-4e9d-b69a-ab7fb502ab86`
- **引用名**: `FrTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the FRTRCV_DIO_PORT_SYM_NAME, FRTRCV_DIO_CHANNEL_SYM_NAME and FRTRCV_DIO_GROUP_SYM_NAME references in the Fr Trcv SWS.

####### 2. FrTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. FrTrcvHardwareInterfaceName

- **UUID**: `ECUC:3801a24c-fcd3-4f0f-acc3-3d9768c585e9`
- **参数名**: `FrTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FR transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either FRTRCV_DIO_PORT_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The FR transceiver driver implementation description shall list up this name for the appropriate FR transceiver hardware.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. FrTrcvDioSymNameRef

- **UUID**: `ECUC:203b8070-d42e-4e9d-b69a-ab7fb502ab86`
- **引用名**: `FrTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the FRTRCV_DIO_PORT_SYM_NAME, FRTRCV_DIO_CHANNEL_SYM_NAME and FRTRCV_DIO_GROUP_SYM_NAME references in the Fr Trcv SWS.

####### 3. FrTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:8094373c-1435-4ce2-9060-88ed58ee2b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvSpiSequence`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives FlexRay transceiver driver information about one SPI sequence. One SPI sequence used by FlexRay transceiver driver is in exclusive use for it. No other driver is allowed to access this sequence. FlexRay transceiver driver may use one sequence to access n FlexRay transceiver hardwares chips of the same type or n sequences are used to access one single FlexRay transceiver hardware chip. If a FlexRay transceiver hardware has no SPI interface, there is no instance of this container.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrTrcvSpiSequenceName

- **UUID**: `ECUC:226694f7-3ba5-4bb2-bbe4-cef2c5e5a057`
- **引用名**: `FrTrcvSpiSequenceName`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

####### 4. FrTrcvBranchIdContainer

**容器属性**:

- **UUID**: `ECUC:5524e0a8-0fd6-4fd6-893c-8798cd442f3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvBranchIdContainer`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Only one SymbolicNameValue can be defined per container. Therefore this container is necessary.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTrcvBranchId

- **UUID**: `ECUC:fbe17363-0924-4881-b863-220e9319c4fc`
- **参数名**: `FrTrcvBranchId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique branch id. It is used by CDDs and internally.

####### 5. FrTrcvChannelDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:40a82e90-ce95-414b-b2cd-21f5fad10e7e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvChannelDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FRTRCV_E_FR_BUSERROR_TRCV

- **UUID**: `ECUC:d4fdf986-ec85-4372-9173-283ee02c5204`
- **引用名**: `FRTRCV_E_FR_BUSERROR_TRCV`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Error Status of Class B (SPI) transceiver bus errors where TrcvIdx is the transceiver index"

########## 2. FRTRCV_E_FR_ERRN_TRCV

- **UUID**: `ECUC:ec2d5975-e047-4131-9c9f-f37c0e0468cd`
- **引用名**: `FRTRCV_E_FR_ERRN_TRCV`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Error Status of Class A (GPIO) transceiver"

####### 6. FrTrcvAccess

**容器属性**:

- **UUID**: `ECUC:90eb74ea-b108-416d-8567-3a9c6e60d6d7`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **FrTrcvDioAccess**
  - UUID: `ECUC:017c4e37-64c2-49c3-96dc-3e8581246ed7`
  - 描述: Container gives FR transceiver driver information about accessing ports and port pins. If a FR transceiver hardware has no Dio interface, there is no instance of this container.
- **FrTrcvDioChannelAccess**
  - UUID: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
  - 描述: In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.
- **FrTrcvSpiSequence**
  - UUID: `ECUC:8094373c-1435-4ce2-9060-88ed58ee2b78`
  - 描述: Container gives FlexRay transceiver driver information about one SPI sequence. One SPI sequence used by FlexRay transceiver driver is in exclusive use for it. No other driver is allowed to access this sequence. FlexRay transceiver driver may use one sequence to access n FlexRay transceiver hardwares chips of the same type or n sequences are used to access one single FlexRay transceiver hardware chip. If a FlexRay transceiver hardware has no SPI interface, there is no instance of this container.

##### 2. FrTrcvDioAccess

**容器属性**:

- **UUID**: `ECUC:017c4e37-64c2-49c3-96dc-3e8581246ed7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioAccess`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives FR transceiver driver information about accessing ports and port pins. If a FR transceiver hardware has no Dio interface, there is no instance of this container.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. FrTrcvHardwareInterfaceName

- **UUID**: `ECUC:3801a24c-fcd3-4f0f-acc3-3d9768c585e9`
- **参数名**: `FrTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FR transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either FRTRCV_DIO_PORT_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The FR transceiver driver implementation description shall list up this name for the appropriate FR transceiver hardware.

######## 引用关系

此容器包含 **1** 个引用：

######### CHOICE-REFERENCE 类型引用

########## 1. FrTrcvDioSymNameRef

- **UUID**: `ECUC:203b8070-d42e-4e9d-b69a-ab7fb502ab86`
- **引用名**: `FrTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the FRTRCV_DIO_PORT_SYM_NAME, FRTRCV_DIO_CHANNEL_SYM_NAME and FRTRCV_DIO_GROUP_SYM_NAME references in the Fr Trcv SWS.

##### 3. FrTrcvDioChannelAccess

**容器属性**:

- **UUID**: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvDioChannelAccess`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. FrTrcvHardwareInterfaceName

- **UUID**: `ECUC:3801a24c-fcd3-4f0f-acc3-3d9768c585e9`
- **参数名**: `FrTrcvHardwareInterfaceName`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: FR transceiver hardware interface name. It is typically the name of a pin. From a Dio point of view it is either a port, a single channel or a channel group. Depending on this fact either FRTRCV_DIO_PORT_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_SYMBOLIC_NAME or FRTRCV_DIO_CHANNEL_GROUP_SYMBOLIC_NAME shall reference a Dio configuration. The FR transceiver driver implementation description shall list up this name for the appropriate FR transceiver hardware.

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. FrTrcvDioSymNameRef

- **UUID**: `ECUC:203b8070-d42e-4e9d-b69a-ab7fb502ab86`
- **引用名**: `FrTrcvDioSymNameRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannel`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort/DioChannelGroup`
  - `/AUTOSAR/EcucDefs/Dio/DioConfig/DioPort`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Choice Reference to a DIO Port, DIO Channel or DIO Channel Group. This reference replaces the FRTRCV_DIO_PORT_SYM_NAME, FRTRCV_DIO_CHANNEL_SYM_NAME and FRTRCV_DIO_GROUP_SYM_NAME references in the Fr Trcv SWS.

##### 4. FrTrcvSpiSequence

**容器属性**:

- **UUID**: `ECUC:8094373c-1435-4ce2-9060-88ed58ee2b78`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvSpiSequence`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container gives FlexRay transceiver driver information about one SPI sequence. One SPI sequence used by FlexRay transceiver driver is in exclusive use for it. No other driver is allowed to access this sequence. FlexRay transceiver driver may use one sequence to access n FlexRay transceiver hardwares chips of the same type or n sequences are used to access one single FlexRay transceiver hardware chip. If a FlexRay transceiver hardware has no SPI interface, there is no instance of this container.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrTrcvSpiSequenceName

- **UUID**: `ECUC:226694f7-3ba5-4bb2-bbe4-cef2c5e5a057`
- **引用名**: `FrTrcvSpiSequenceName`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `SpiSequence`
- **完整路径**: `/AUTOSAR/EcucDefs/Spi/SpiDriver/SpiSequence`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Spi sequence configuration container.

##### 5. FrTrcvBranchIdContainer

**容器属性**:

- **UUID**: `ECUC:5524e0a8-0fd6-4fd6-893c-8798cd442f3b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvBranchIdContainer`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Only one SymbolicNameValue can be defined per container. Therefore this container is necessary.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTrcvBranchId

- **UUID**: `ECUC:fbe17363-0924-4881-b863-220e9319c4fc`
- **参数名**: `FrTrcvBranchId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique branch id. It is used by CDDs and internally.

##### 6. FrTrcvChannelDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:40a82e90-ce95-414b-b2cd-21f5fad10e7e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvChannelDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FRTRCV_E_FR_BUSERROR_TRCV

- **UUID**: `ECUC:d4fdf986-ec85-4372-9173-283ee02c5204`
- **引用名**: `FRTRCV_E_FR_BUSERROR_TRCV`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Error Status of Class B (SPI) transceiver bus errors where TrcvIdx is the transceiver index"

######## 2. FRTRCV_E_FR_ERRN_TRCV

- **UUID**: `ECUC:ec2d5975-e047-4131-9c9f-f37c0e0468cd`
- **引用名**: `FRTRCV_E_FR_ERRN_TRCV`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to configured DEM event to report "Error Status of Class A (GPIO) transceiver"

##### 7. FrTrcvGeneral

**容器属性**:

- **UUID**: `ECUC:5a6841e4-4dc0-4860-9204-018b12dde294`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTrcvGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Container gives FlexRay transceiver driver basic information.

###### 参数配置

此容器包含 **10** 个参数：

####### INTEGER 类型参数

######## 1. FrTrcvIndex

- **UUID**: `ECUC:f49fa7ab-6ea2-4827-9084-9c9402d4acf4`
- **参数名**: `FrTrcvIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. FrTrcvRetryCountInInit

- **UUID**: `ECUC:1db1dc75-0a03-416c-bc7f-8805c44c0d24`
- **参数名**: `FrTrcvRetryCountInInit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the number of retry count when error occurs while initialization process of FrTrcv.

######## 3. FrTrcvWaitCount

- **UUID**: `ECUC:e1cfbbc9-9605-4ea1-8289-9990499d7462`
- **参数名**: `FrTrcvWaitCount`
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

######## 1. FrTrcvDevErrorDetect

- **UUID**: `ECUC:1c51d5a8-a933-40f2-946f-0184c5c69105`
- **参数名**: `FrTrcvDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches development error detection and notification on and off.

######## 2. FrTrcvErrorCheckDuringCommunication

- **UUID**: `ECUC:64ba621e-c7dc-4521-9afa-f983429af91e`
- **参数名**: `FrTrcvErrorCheckDuringCommunication`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable a functionality to check transceiver's state during communication.

######## 3. FrTrcvErrorCheckInInit

- **UUID**: `ECUC:99f6f586-4c3a-47e6-95e8-ad1758eb2d9d`
- **参数名**: `FrTrcvErrorCheckInInit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enable a functionality to check transceiver's state while initialization process of FrTrcv.

######## 4. FrTrcvGetVersionInfo

- **UUID**: `ECUC:f5957278-1a3f-467b-bcd5-ce90157a7f7a`
- **参数名**: `FrTrcvGetVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches version information API on and off. If switched off, function need not be present in compiled code.

####### FLOAT 类型参数

######## 1. FrTrcvMainFunctionCycleTime

- **UUID**: `ECUC:ceab3479-8179-441d-880e-885d36609f71`
- **参数名**: `FrTrcvMainFunctionCycleTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Cyclic call time for function FrTrcvMainFunction in seconds. A call time of 0ms indicates no calls for this function. In this case function need not be present in compiled code.

####### ENUMERATION 类型参数

######## 1. FrTrcvWakeUpSupport

- **UUID**: `ECUC:eeab06d7-a456-47ef-b4a2-a313a9619688`
- **参数名**: `FrTrcvWakeUpSupport`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRTRCV_WAKEUP_BY_POLLING` (来源: AUTOSAR_ECUC)
  - `FRTRCV_WAKEUP_NOT_SUPPORTED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Informs whether wake up is supported by polling or whether it is not supported.

####### FUNCTION-NAME 类型参数

######## 1. FrTrcvDemReportErrorStatusConfiguration

- **UUID**: `ECUC:2078af64-4a4a-4eff-9fe2-7878ad8fd90d`
- **参数名**: `FrTrcvDemReportErrorStatusConfiguration`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of a C function which substitutes Dem_ReportErrorStatus.

##### 8. FrTrcvAccess

**容器属性**:

- **UUID**: `ECUC:90eb74ea-b108-416d-8567-3a9c6e60d6d7`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrTrcvAccess`
- **多重性**: [1..1]

**容器选择**:

- **FrTrcvDioAccess**
  - UUID: `ECUC:017c4e37-64c2-49c3-96dc-3e8581246ed7`
  - 描述: Container gives FR transceiver driver information about accessing ports and port pins. If a FR transceiver hardware has no Dio interface, there is no instance of this container.
- **FrTrcvDioChannelAccess**
  - UUID: `ECUC:21266d48-9151-4727-b32d-10f3140ddff1`
  - 描述: In this Container the relation between FR transceiver hardware pin names and Dio port access information is given.
- **FrTrcvSpiSequence**
  - UUID: `ECUC:8094373c-1435-4ce2-9060-88ed58ee2b78`
  - 描述: Container gives FlexRay transceiver driver information about one SPI sequence. One SPI sequence used by FlexRay transceiver driver is in exclusive use for it. No other driver is allowed to access this sequence. FlexRay transceiver driver may use one sequence to access n FlexRay transceiver hardwares chips of the same type or n sequences are used to access one single FlexRay transceiver hardware chip. If a FlexRay transceiver hardware has no SPI interface, there is no instance of this container.

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

1. **FrTrcv**
