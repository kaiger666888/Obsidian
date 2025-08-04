# Dio - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:11

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dio](#dio)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-2-2.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dio

#### 基本信息

- **UUID**: `ECUC:8a22156a-f55e-407d-9677-9660dae4c9d4`
- **模块名称**: `Dio`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME

#### 模块描述

Configuration of the Dio (Digital IO) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.2

- **发布日期**: 2014-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. DioConfig

**容器属性**:

- **UUID**: `ECUC:b9ea6561-fd73-4381-bdb6-8e027a43ad62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioConfig`
- **多重性**: [0..1]

**容器描述**:

This container contains the configuration parameters and sub containers of the AUTOSAR DIO module.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. DioPort

**容器属性**:

- **UUID**: `ECUC:f85f480f-fee7-4a00-a99a-4aede301e703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioPort`
- **多重性**: [1..17]

**容器描述**:

Configuration of individual DIO ports, consisting of channels and possible channel groups.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioPortId

- **UUID**: `ECUC:d596f059-d21f-46fa-8c62-8eae8ff3d68d`
- **参数名**: `DioPortId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..40]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric identifier of the DIO port. Not all MCU ports may be used for DIO, thus there may be "gaps" in the list of all IDs. This value will be

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..16]

**容器描述**:

Configuration of an individual DIO channel.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

######### 2. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..1]

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This shall be the mask which defines the positions of the channel

############ 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Channel Group on the port, counted

########### STRING 类型参数

############ 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `DioChGrpId_P0_0`
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

####### 2. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..16]

**容器描述**:

Configuration of an individual DIO channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

####### 3. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..1]

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This shall be the mask which defines the positions of the channel

########## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Channel Group on the port, counted

######### STRING 类型参数

########## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `DioChGrpId_P0_0`
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 2. DioPort

**容器属性**:

- **UUID**: `ECUC:f85f480f-fee7-4a00-a99a-4aede301e703`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioPort`
- **多重性**: [1..17]

**容器描述**:

Configuration of individual DIO ports, consisting of channels and possible channel groups.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DioPortId

- **UUID**: `ECUC:d596f059-d21f-46fa-8c62-8eae8ff3d68d`
- **参数名**: `DioPortId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..40]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Numeric identifier of the DIO port. Not all MCU ports may be used for DIO, thus there may be "gaps" in the list of all IDs. This value will be

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..16]

**容器描述**:

Configuration of an individual DIO channel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

####### 2. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..1]

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This shall be the mask which defines the positions of the channel

########## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Channel Group on the port, counted

######### STRING 类型参数

########## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `DioChGrpId_P0_0`
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 3. DioChannel

**容器属性**:

- **UUID**: `ECUC:3160aae0-8510-4b1f-88ac-40f7c48a9e2d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannel`
- **多重性**: [0..16]

**容器描述**:

Configuration of an individual DIO channel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DioChannelId

- **UUID**: `ECUC:e87de39b-7754-4f85-816c-b58b7659a4e1`
- **参数名**: `DioChannelId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: Channel Id of the DIO channel. This value will be assigned to the symbolic names.

##### 4. DioChannelGroup

**容器属性**:

- **UUID**: `ECUC:8e498821-8d5c-4512-88fc-8d4d90dca1ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioChannelGroup`
- **多重性**: [0..1]

**容器描述**:

Definition and configuration of DIO channel groups. A channel group represents several adjoining DIO channels represented by a logical group.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DioPortMask

- **UUID**: `ECUC:c3f03c97-def2-40d9-bdd3-052b0acd5a91`
- **参数名**: `DioPortMask`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This shall be the mask which defines the positions of the channel

######## 2. DioPortOffset

- **UUID**: `ECUC:41125c72-502e-4fb4-b85c-1b499923b736`
- **参数名**: `DioPortOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..15]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The position of the Channel Group on the port, counted

####### STRING 类型参数

######## 1. DioChannelGroupIdentification

- **UUID**: `ECUC:c0a5ca8e-4bf0-4e03-83d7-6559e724a983`
- **参数名**: `DioChannelGroupIdentification`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: ECU
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **字符串变体**:
  - 默认值: `DioChGrpId_P0_0`
- **描述**: The DIO channel group is identified in DIO API by a pointer to a data structure (of type Dio_ChannelGroupType). That data structure contains the channel group information.

##### 5. DioGeneral

**容器属性**:

- **UUID**: `ECUC:ba24cf3d-7a2a-4465-a7a7-6a5f42c8e3ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DioGeneral`
- **多重性**: [0..1]

**容器描述**:

General DIO module configuration parameters.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. DioDevErrorDetect

- **UUID**: `ECUC:f82078d3-b78e-4805-8069-a1cb89699750`
- **参数名**: `DioDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 2. DioFlipChannelApi

- **UUID**: `ECUC:01513b33-8238-4e96-afe3-753cca65effa`
- **参数名**: `DioFlipChannelApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Dio_FlipChannel() from the code.

######## 3. DioVersionInfoApi

- **UUID**: `ECUC:20d99dc2-e3fe-4832-8ecf-379936ade262`
- **参数名**: `DioVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Adds / removes the service Dio_ GetVersionInfo() from the code.

######## 4. DioSafetyEnable

- **UUID**: `ECUC:412da385-6bf4-4819-87e4-8ec223fb5b17`
- **参数名**: `DioSafetyEnable`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Enable/Disable the Safety check and all associated notifications.

##### 6. CommonPublishedInformation

**容器属性**:

- **UUID**: `492f8482-3e2c-4bf1-b27f-01fd7ac35788`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CommonPublishedInformation`
- **多重性**: [0..1]

**容器描述**:

Common container, aggregated by all modules. It contains published information about vendor and versions.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. ArMajorVersion

- **UUID**: `bd0a8d38-4d8c-4ee9-88fe-1166b258bb8a`
- **参数名**: `ArMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `4`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 2. ArMinorVersion

- **UUID**: `73f87c7f-e230-4178-bff0-eb2704aae656`
- **参数名**: `ArMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 3. ArPatchVersion

- **UUID**: `2380135d-6778-417a-a34b-e10017d4dd54`
- **参数名**: `ArPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `2`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of AUTOSAR specification on which the appropriate implementation is based on.

######## 4. SwMajorVersion

- **UUID**: `fca015e3-5f28-4cbe-8949-8f4b87d86827`
- **参数名**: `SwMajorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `10`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Major version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 5. SwMinorVersion

- **UUID**: `14ab81e0-3d80-43dc-8b92-247e5a542df9`
- **参数名**: `SwMinorVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `40`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Minor version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 6. SwPatchVersion

- **UUID**: `32e37bfd-18b6-41d1-9248-a81dbe0fe4c5`
- **参数名**: `SwPatchVersion`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Patch level version number of the vendor specific implementation of the module. The numbering is vendor specific.

######## 7. ModuleId

- **UUID**: `3b407478-6902-4f80-b7cf-f33b0854e638`
- **参数名**: `ModuleId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `120`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Module ID of this module from Module List

######## 8. VendorId

- **UUID**: `7d650b2d-4adb-41f0-a68e-5f0c416501d1`
- **参数名**: `VendorId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **默认值**: `17`
- **取值范围**: [0..65535]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **描述**: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list

####### STRING 类型参数

######## 1. Release

- **UUID**: `3b407478-6902-4f40-b7cf-f33b0854e638`
- **参数名**: `Release`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: INFINEON_AURIX2G
- **符号名值**: false
- **字符串变体**:
  - 默认值: `_TRICORE_TC397`
- **描述**: Aurix2G derivative used for the implementation

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AURIX2G

- **UUID**: `ECUC:AUTOSAR`
- **包名称**: `AURIX2G`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ECUC:ECUCDEFS`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Dio**
