# Eth - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:16

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Eth](#eth)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Eth

#### 基本信息

- **UUID**: `ECUC:7330314e-e986-4763-8446-4fea1ec1f9db`
- **模块名称**: `Eth`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Eth (Ethernet Driver) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.4.0

- **发布日期**: 2013-10-31
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **4** 个配置容器：

##### 1. EthConfigSet

**容器属性**:

- **UUID**: `ECUC:5038b196-90f1-4b1e-991a-59d361bf33c9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthConfigSet`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

All included containers and parameters that may be part of a multiple configuration set.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. EthCtrlConfig

**容器属性**:

- **UUID**: `ECUC:56cd8c81-2738-4e37-9187-eb8d6838c4c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthCtrlConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual controller

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. EthCtrlIdx

- **UUID**: `ECUC:57bc491e-62f2-4d20-943a-0bf28cca2ac1`
- **参数名**: `EthCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the instance ID of the configured controller.

########## 2. EthCtrlRxBufLenByte

- **UUID**: `ECUC:6164a17c-2277-4d64-81a0-c03e219bdf8d`
- **参数名**: `EthCtrlRxBufLenByte`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1522]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximum receive buffer length (frame length) in bytes.

########## 3. EthCtrlTxBufLenByte

- **UUID**: `ECUC:f4b834a6-9fce-4cf9-9f80-98e4a6ad9eec`
- **参数名**: `EthCtrlTxBufLenByte`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1522]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximum transmit buffer length (frame length) in bytes.

########## 4. EthRxBufTotal

- **UUID**: `ECUC:139da546-28f2-4245-8429-9c05fa63efde`
- **参数名**: `EthRxBufTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the number of receive buffers.

########## 5. EthTxBufTotal

- **UUID**: `ECUC:3ea8a022-70b8-493a-9cf8-13ae8489d6b4`
- **参数名**: `EthTxBufTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the number of transmit buffers.

######### BOOLEAN 类型参数

########## 1. EthCtrlEnableMii

- **UUID**: `ECUC:5292ca43-a021-40dc-ad36-08a935433941`
- **参数名**: `EthCtrlEnableMii`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables Media Independent Interface (MII) for transceiver access

########## 2. EthCtrlEnableRxInterrupt

- **UUID**: `ECUC:1750d5cc-afcb-4d21-93b0-e29e9a41ea26`
- **参数名**: `EthCtrlEnableRxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables receive interrupt

########## 3. EthCtrlEnableTxInterrupt

- **UUID**: `ECUC:064b39a9-dca2-4886-a425-973de461e3d7`
- **参数名**: `EthCtrlEnableTxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables transmit interrupt

######### STRING 类型参数

########## 1. EthCtrlPhyAddress

- **UUID**: `ECUC:b7e156c0-3a45-42f1-b2f9-feb287415200`
- **参数名**: `EthCtrlPhyAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the unique 48-bit physical address (MAC address) of the controller in network byte order.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. EthDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:6c163108-f8fb-4e94-aee0-19a511446ffc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. ETH_E_ACCESS

- **UUID**: `ECUC:b4651d05-f83d-44c9-9d1e-21089a781293`
- **引用名**: `ETH_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Controller access failed" has occured.

####### 2. EthDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:6c163108-f8fb-4e94-aee0-19a511446ffc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETH_E_ACCESS

- **UUID**: `ECUC:b4651d05-f83d-44c9-9d1e-21089a781293`
- **引用名**: `ETH_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Controller access failed" has occured.

##### 2. EthCtrlConfig

**容器属性**:

- **UUID**: `ECUC:56cd8c81-2738-4e37-9187-eb8d6838c4c6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthCtrlConfig`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration of the individual controller

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. EthCtrlIdx

- **UUID**: `ECUC:57bc491e-62f2-4d20-943a-0bf28cca2ac1`
- **参数名**: `EthCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the instance ID of the configured controller.

######## 2. EthCtrlRxBufLenByte

- **UUID**: `ECUC:6164a17c-2277-4d64-81a0-c03e219bdf8d`
- **参数名**: `EthCtrlRxBufLenByte`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1522]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximum receive buffer length (frame length) in bytes.

######## 3. EthCtrlTxBufLenByte

- **UUID**: `ECUC:f4b834a6-9fce-4cf9-9f80-98e4a6ad9eec`
- **参数名**: `EthCtrlTxBufLenByte`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..1522]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the maximum transmit buffer length (frame length) in bytes.

######## 4. EthRxBufTotal

- **UUID**: `ECUC:139da546-28f2-4245-8429-9c05fa63efde`
- **参数名**: `EthRxBufTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the number of receive buffers.

######## 5. EthTxBufTotal

- **UUID**: `ECUC:3ea8a022-70b8-493a-9cf8-13ae8489d6b4`
- **参数名**: `EthTxBufTotal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configures the number of transmit buffers.

####### BOOLEAN 类型参数

######## 1. EthCtrlEnableMii

- **UUID**: `ECUC:5292ca43-a021-40dc-ad36-08a935433941`
- **参数名**: `EthCtrlEnableMii`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables Media Independent Interface (MII) for transceiver access

######## 2. EthCtrlEnableRxInterrupt

- **UUID**: `ECUC:1750d5cc-afcb-4d21-93b0-e29e9a41ea26`
- **参数名**: `EthCtrlEnableRxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables receive interrupt

######## 3. EthCtrlEnableTxInterrupt

- **UUID**: `ECUC:064b39a9-dca2-4886-a425-973de461e3d7`
- **参数名**: `EthCtrlEnableTxInterrupt`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables transmit interrupt

####### STRING 类型参数

######## 1. EthCtrlPhyAddress

- **UUID**: `ECUC:b7e156c0-3a45-42f1-b2f9-feb287415200`
- **参数名**: `EthCtrlPhyAddress`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 17
  - 最小长度: 17
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the unique 48-bit physical address (MAC address) of the controller in network byte order.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:6c163108-f8fb-4e94-aee0-19a511446ffc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. ETH_E_ACCESS

- **UUID**: `ECUC:b4651d05-f83d-44c9-9d1e-21089a781293`
- **引用名**: `ETH_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Controller access failed" has occured.

##### 3. EthDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:6c163108-f8fb-4e94-aee0-19a511446ffc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. ETH_E_ACCESS

- **UUID**: `ECUC:b4651d05-f83d-44c9-9d1e-21089a781293`
- **引用名**: `ETH_E_ACCESS`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when the error "Controller access failed" has occured.

##### 4. EthGeneral

**容器属性**:

- **UUID**: `ECUC:6f42d612-0b76-4acc-a377-9a35f3decf57`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

General configuration of Ethernet Driver module

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. EthIndex

- **UUID**: `ECUC:8f9f2801-a733-45ba-92c1-4f76e7239397`
- **参数名**: `EthIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the InstanceId of this module instance. If only one instance is present it shall have the Id 0.

######## 2. EthMaxCtrlsSupported

- **UUID**: `ECUC:5dd19540-c70f-4e65-b839-510b53e355c7`
- **参数名**: `EthMaxCtrlsSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Limits the total number of supported controllers.

####### BOOLEAN 类型参数

######## 1. EthDevErrorDetect

- **UUID**: `ECUC:e9f29dc0-4e38-4c7a-89f6-67505e301506`
- **参数名**: `EthDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables development error detection.

######## 2. EthUpdatePhysAddrFilter

- **UUID**: `ECUC:3f2394e5-bdde-4327-b254-10bfcbda919b`
- **参数名**: `EthUpdatePhysAddrFilter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables optional API Eth_UpdatePhysAddrFilter.

######## 3. EthVersionInfoApi

- **UUID**: `ECUC:aec58ac0-ad1c-4331-a535-7f4301e98577`
- **参数名**: `EthVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables version info API

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

1. **Eth**
