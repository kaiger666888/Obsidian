# Dio - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:42

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dio](#dio)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dio

#### 基本信息

- **UUID**: `ECUC:8a22156a-f55e-407d-9677-9660dae4c9d4`
- **模块名称**: `Dio`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Dio (Digital IO) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **5** 个配置容器：

##### 1. DioConfig

**容器属性**:

- **UUID**: `ECUC:b9ea6561-fd73-4381-bdb6-8e027a43ad62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR DIO module. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DioPort

**容器属性**:

- **UUID**: `ECUC:f85f480f-fee7-4a00-a99a-4aede301e703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioPort`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of individual DIO ports, consisting of channels and possible channel groups.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioPortId

- **UUID**: `ECUC:d596f059-d21f-46fa-8c62-8eae8ff3d68d`
- **参数名**: `DioPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric identifier of the DIO port. Not all MCU ports may be used for DIO, thus there may be "gaps" in the list of all IDs. This value will be

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual DIO channel. Besides a HW specific channel name which is typically fixed for a specific micro controller, additional symbolic names can be defined per channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

######### 2. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This shall be the mask which defines the positions of the channel

############ 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The position of the Channel Group on the port, counted

########### STRING 类型参数

############ 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

####### 2. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual DIO channel. Besides a HW specific channel name which is typically fixed for a specific micro controller, additional symbolic names can be defined per channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

####### 3. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This shall be the mask which defines the positions of the channel

########## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The position of the Channel Group on the port, counted

######### STRING 类型参数

########## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 2. DioPort

**容器属性**:

- **UUID**: `ECUC:f85f480f-fee7-4a00-a99a-4aede301e703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioPort`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of individual DIO ports, consisting of channels and possible channel groups.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DioPortId

- **UUID**: `ECUC:d596f059-d21f-46fa-8c62-8eae8ff3d68d`
- **参数名**: `DioPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Numeric identifier of the DIO port. Not all MCU ports may be used for DIO, thus there may be "gaps" in the list of all IDs. This value will be

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual DIO channel. Besides a HW specific channel name which is typically fixed for a specific micro controller, additional symbolic names can be defined per channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

####### 2. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This shall be the mask which defines the positions of the channel

########## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The position of the Channel Group on the port, counted

######### STRING 类型参数

########## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 3. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of an individual DIO channel. Besides a HW specific channel name which is typically fixed for a specific micro controller, additional symbolic names can be defined per channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

##### 4. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This shall be the mask which defines the positions of the channel

######## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The position of the Channel Group on the port, counted

####### STRING 类型参数

######## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 5. DioGeneral

**容器属性**:

- **UUID**: `ECUC:ba24cf3d-7a2a-4465-a7a7-6a5f42c8e3ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General DIO module configuration parameters.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. DioDevErrorDetect

- **UUID**: `ECUC:f82078d3-b78e-4805-8069-a1cb89699750`
- **参数名**: `DioDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification

######## 2. DioFlipChannelApi

- **UUID**: `ECUC:01513b33-8238-4e96-afe3-753cca65effa`
- **参数名**: `DioFlipChannelApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Dio_FlipChannel() from the code.

######## 3. DioVersionInfoApi

- **UUID**: `ECUC:20d99dc2-e3fe-4832-8ecf-379936ade262`
- **参数名**: `DioVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Adds / removes the service Dio_ GetVersionInfo() from the code.

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

1. **Dio**
