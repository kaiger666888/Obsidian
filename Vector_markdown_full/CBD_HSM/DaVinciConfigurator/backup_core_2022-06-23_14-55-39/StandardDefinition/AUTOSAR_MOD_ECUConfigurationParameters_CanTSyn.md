# CanTSyn - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:09

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanTSyn](#cantsyn)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanTSyn

#### 基本信息

- **UUID**: `eba84a57-5c11-41dd-b908-2176663a2cc4`
- **模块名称**: `CanTSyn`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module with respect to global time handling on CAN.

#### 版本历史

共有 **5** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2014-08-25T05:10:29+02:00
- **发布者**: visssf

**变更内容**:

##### 2. 版本 1.01.00

- **发布日期**: 2014-12-04T11:01:52+01:00
- **发布者**: visssf

**变更内容**:

##### 3. 版本 1.02.00

- **发布日期**: 2015-07-14T04:16:14+02:00
- **发布者**: visssf

**变更内容**:

##### 4. 版本 2.00.00

- **发布日期**: 2015-09-22T09:22:59+02:00
- **发布者**: visssf

**变更内容**:

##### 5. 版本 2.01.00

- **发布日期**: 2016-02-26T01:39:24+01:00
- **发布者**: visssf

**变更内容**:

#### 配置容器

本模块包含 **14** 个配置容器：

##### 1. CanTSynGeneral

**容器属性**:

- **UUID**: `3382b529-a397-45f2-b808-d912a45980f4`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGeneral`
- **多重性**: [1..1]

**容器描述**:

This container holds the general parameters of the CAN-specific Synchronized Time-base Manager

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. CanTSynDevErrorDetect

- **UUID**: `203c4ddc-448c-4f33-8b0c-6d7fcf088b6a`
- **参数名**: `CanTSynDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch for enabling the development error detection.

######## 2. CanTSynVersionInfo

- **UUID**: `b06337f6-4cee-4d9a-9080-f95e6bfc9607`
- **参数名**: `CanTSynVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Activate/Deactivate the version information API (CanTSyn_GetVersionInfo). True: version information API activated False: version information API deactivated.

####### FLOAT 类型参数

######## 1. CanTSynMainFunctionPeriod

- **UUID**: `e63c7a9a-cae1-4cc3-a7c8-2b2bcc21210b`
- **参数名**: `CanTSynMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Schedule period of the main function CanTSyn_MainFunction. Unit: [s].

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. CanTSynGlobalTimeFupDataIDList

**容器属性**:

- **UUID**: `4e4f73f8-e829-4f3e-b07f-974aa62b9a5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeFupDataIDListElement

**容器属性**:

- **UUID**: `47228971-6b1a-40c6-8dad-42fedfe5b17c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeFupDataIDListIndex

- **UUID**: `d88c08dd-3788-497f-902b-ec6c08915549`
- **参数名**: `CanTSynGlobalTimeFupDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

############ 2. CanTSynGlobalTimeFupDataIDListValue

- **UUID**: `62f22ae0-1796-4f11-a14a-4d21081523f3`
- **参数名**: `CanTSynGlobalTimeFupDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

####### 2. CanTSynGlobalTimeFupDataIDListElement

**容器属性**:

- **UUID**: `47228971-6b1a-40c6-8dad-42fedfe5b17c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeFupDataIDListIndex

- **UUID**: `d88c08dd-3788-497f-902b-ec6c08915549`
- **参数名**: `CanTSynGlobalTimeFupDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeFupDataIDListValue

- **UUID**: `62f22ae0-1796-4f11-a14a-4d21081523f3`
- **参数名**: `CanTSynGlobalTimeFupDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

####### 3. CanTSynGlobalTimeOfnsDataIDList

**容器属性**:

- **UUID**: `011ec66b-71b1-4637-bbf6-d38a140f301c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeOfnsDataIDListElement

**容器属性**:

- **UUID**: `7fad34bf-3421-493d-9812-b5836ba40e22`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeOfnsDataIDListIndex

- **UUID**: `dc82f823-5ff8-41e3-8631-1470b810d4c2`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

############ 2. CanTSynGlobalTimeOfnsDataIDListValue

- **UUID**: `7b714c16-a3c9-4e09-8c7b-a87ee4dc09b4`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

####### 4. CanTSynGlobalTimeOfnsDataIDListElement

**容器属性**:

- **UUID**: `7fad34bf-3421-493d-9812-b5836ba40e22`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeOfnsDataIDListIndex

- **UUID**: `dc82f823-5ff8-41e3-8631-1470b810d4c2`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeOfnsDataIDListValue

- **UUID**: `7b714c16-a3c9-4e09-8c7b-a87ee4dc09b4`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

####### 5. CanTSynGlobalTimeOfsDataIDList

**容器属性**:

- **UUID**: `54722541-7465-4314-9ab7-c6053c065ecc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `ec80be40-6a04-48ac-8670-1e1804b462a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `2b37266e-c350-4fb8-9b58-39e650d72ec7`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

############ 2. CanTSynGlobalTimeOfsDataIDListValue

- **UUID**: `b514073a-b3c0-4cf3-bd4c-be9b03878b62`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

####### 6. CanTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `ec80be40-6a04-48ac-8670-1e1804b462a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `2b37266e-c350-4fb8-9b58-39e650d72ec7`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeOfsDataIDListValue

- **UUID**: `b514073a-b3c0-4cf3-bd4c-be9b03878b62`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

####### 7. CanTSynGlobalTimeSyncDataIDList

**容器属性**:

- **UUID**: `c2180445-f3e5-4172-92bc-d1ad2135cfbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `7bcbb251-748b-4f96-bd5e-380cc45bc0e3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `0f9bbeea-4b20-4524-b83a-acbcc487709d`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index for the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

############ 2. CanTSynGlobalTimeSyncDataIDListValue

- **UUID**: `b8aa78f2-4bd3-42d2-9b0a-04e650b9d025`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

####### 8. CanTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `7bcbb251-748b-4f96-bd5e-380cc45bc0e3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `0f9bbeea-4b20-4524-b83a-acbcc487709d`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index for the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeSyncDataIDListValue

- **UUID**: `b8aa78f2-4bd3-42d2-9b0a-04e650b9d025`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 2. CanTSynGlobalTimeFupDataIDList

**容器属性**:

- **UUID**: `4e4f73f8-e829-4f3e-b07f-974aa62b9a5d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeFupDataIDListElement

**容器属性**:

- **UUID**: `47228971-6b1a-40c6-8dad-42fedfe5b17c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeFupDataIDListIndex

- **UUID**: `d88c08dd-3788-497f-902b-ec6c08915549`
- **参数名**: `CanTSynGlobalTimeFupDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeFupDataIDListValue

- **UUID**: `62f22ae0-1796-4f11-a14a-4d21081523f3`
- **参数名**: `CanTSynGlobalTimeFupDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

##### 3. CanTSynGlobalTimeFupDataIDListElement

**容器属性**:

- **UUID**: `47228971-6b1a-40c6-8dad-42fedfe5b17c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeFupDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeFupDataIDListIndex

- **UUID**: `d88c08dd-3788-497f-902b-ec6c08915549`
- **参数名**: `CanTSynGlobalTimeFupDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

######## 2. CanTSynGlobalTimeFupDataIDListValue

- **UUID**: `62f22ae0-1796-4f11-a14a-4d21081523f3`
- **参数名**: `CanTSynGlobalTimeFupDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for FUP messages ensures the identification of data elements due to CRC calculation process.

##### 4. CanTSynGlobalTimeOfnsDataIDList

**容器属性**:

- **UUID**: `011ec66b-71b1-4637-bbf6-d38a140f301c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeOfnsDataIDListElement

**容器属性**:

- **UUID**: `7fad34bf-3421-493d-9812-b5836ba40e22`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeOfnsDataIDListIndex

- **UUID**: `dc82f823-5ff8-41e3-8631-1470b810d4c2`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeOfnsDataIDListValue

- **UUID**: `7b714c16-a3c9-4e09-8c7b-a87ee4dc09b4`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

##### 5. CanTSynGlobalTimeOfnsDataIDListElement

**容器属性**:

- **UUID**: `7fad34bf-3421-493d-9812-b5836ba40e22`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfnsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeOfnsDataIDListIndex

- **UUID**: `dc82f823-5ff8-41e3-8631-1470b810d4c2`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

######## 2. CanTSynGlobalTimeOfnsDataIDListValue

- **UUID**: `7b714c16-a3c9-4e09-8c7b-a87ee4dc09b4`
- **参数名**: `CanTSynGlobalTimeOfnsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFNS messages ensures the identification of data elements due to CRC calculation process.

##### 6. CanTSynGlobalTimeOfsDataIDList

**容器属性**:

- **UUID**: `54722541-7465-4314-9ab7-c6053c065ecc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `ec80be40-6a04-48ac-8670-1e1804b462a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `2b37266e-c350-4fb8-9b58-39e650d72ec7`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeOfsDataIDListValue

- **UUID**: `b514073a-b3c0-4cf3-bd4c-be9b03878b62`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

##### 7. CanTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `ec80be40-6a04-48ac-8670-1e1804b462a2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `2b37266e-c350-4fb8-9b58-39e650d72ec7`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 2. CanTSynGlobalTimeOfsDataIDListValue

- **UUID**: `b514073a-b3c0-4cf3-bd4c-be9b03878b62`
- **参数名**: `CanTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

##### 8. CanTSynGlobalTimeSyncDataIDList

**容器属性**:

- **UUID**: `c2180445-f3e5-4172-92bc-d1ad2135cfbd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `7bcbb251-748b-4f96-bd5e-380cc45bc0e3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `0f9bbeea-4b20-4524-b83a-acbcc487709d`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index for the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 2. CanTSynGlobalTimeSyncDataIDListValue

- **UUID**: `b8aa78f2-4bd3-42d2-9b0a-04e650b9d025`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 9. CanTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `7bcbb251-748b-4f96-bd5e-380cc45bc0e3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `0f9bbeea-4b20-4524-b83a-acbcc487709d`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index for the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 2. CanTSynGlobalTimeSyncDataIDListValue

- **UUID**: `b8aa78f2-4bd3-42d2-9b0a-04e650b9d025`
- **参数名**: `CanTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 10. CanTSynGlobalTimeDomain

**容器属性**:

- **UUID**: `dd476b72-786b-4117-9254-242370e89290`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeDomain`
- **多重性**: [1..infinite]

**容器描述**:

This represents the existence of a global time domain on CAN. The CanTSyn module can administrate several global time domains at the same time that in itself form a hierarchy of domains and sub-domains.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeDomainId

- **UUID**: `0d7f9a6e-a3d6-4eef-b3dd-640d819f13e3`
- **参数名**: `CanTSynGlobalTimeDomainId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The global time domain ID.

######## 2. CanTSynGlobalTimeSequenceCounterJumpWidth

- **UUID**: `addb4646-3ca6-4123-b601-c8fbd956d96c`
- **参数名**: `CanTSynGlobalTimeSequenceCounterJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The SequenceCounterJumpWidth specifies the maximum allowed gap of the Sequence Counter between two SYNC resp. two OFS messages.

####### FLOAT 类型参数

######## 1. CanTSynGlobalTimeFollowUpTimeout

- **UUID**: `c153ed9a-184d-4bca-8b2a-bbfa82bbc53d`
- **参数名**: `CanTSynGlobalTimeFollowUpTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Rx timeout for the follow-up message. This is only relevant for selected bus systems Unit:seconds

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanTSynSynchronizedTimeBaseRef

- **UUID**: `54ef0005-8f97-4870-b93d-fb2c78a00c92`
- **引用名**: `CanTSynSynchronizedTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **描述**: Mandatory reference to the required synchronized time-base.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. CanTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `e2a7d862-fc1b-420e-a0dd-dbd35bb9e147`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMaster`
- **多重性**: [0..infinite]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

######## 参数配置

此容器包含 **4** 个参数：

######### FLOAT 类型参数

########## 1. CanTSynGlobalTimeTxFollowUpOffset

- **UUID**: `acdaf4e6-57c6-48d8-bff5-7a921363bd75`
- **参数名**: `CanTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the transmission time offset between a SYNC message and the related FUP message resp. OFS message and related OFNS message. Unit: seconds.

########## 2. CanTSynGlobalTimeTxPeriod

- **UUID**: `d928eace-ac32-4067-b2f9-38dde1ad107c`
- **参数名**: `CanTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period. Unit: seconds

########## 3. CanTSynMasterConfirmationTimeout

- **UUID**: `9f6a97ff-2266-4af0-bf51-4771c29db32c`
- **参数名**: `CanTSynMasterConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the confirmation timeout after transmission of a SYNC message resp. OFS message. Unit: seconds.

######### ENUMERATION 类型参数

########## 1. CanTSynGlobalTimeTxCrcSecured

- **UUID**: `028c9dae-7cc2-48c1-b3cd-78f7a829f450`
- **参数名**: `CanTSynGlobalTimeTxCrcSecured`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_NOT_SUPPORTED` (来源: AUTOSAR_ECUC)
  - `CRC_SUPPORTED` (来源: AUTOSAR_ECUC)
- **描述**: This represents the configuration of whether or not CRC is supported.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `224dae13-8577-42b2-914b-a481e307a9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `3cac33bb-89fa-43ca-b863-1b4d7b552d56`
- **参数名**: `CanTSynGlobalTimeMasterConfirmationHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTSynGlobalTimePduRef

- **UUID**: `ed4fbecb-709f-443e-a33e-255d09f6d2de`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 2. CanTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `224dae13-8577-42b2-914b-a481e307a9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `3cac33bb-89fa-43ca-b863-1b4d7b552d56`
- **参数名**: `CanTSynGlobalTimeMasterConfirmationHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTSynGlobalTimePduRef

- **UUID**: `ed4fbecb-709f-443e-a33e-255d09f6d2de`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 3. CanTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `e38377b2-690c-4029-a86c-8d889be07808`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

Configuration of a global time slave. Each global time domain is required to have at least one time slave. The configured ECU may or may not represent a time slave.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. CanTSynRxCrcValidated

- **UUID**: `6126e429-bd7f-4ad2-97ec-944474cb6481`
- **参数名**: `CanTSynRxCrcValidated`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_IGNORED` (来源: AUTOSAR_ECUC)
  - `CRC_NOT_VALIDATED` (来源: AUTOSAR_ECUC)
  - `CRC_VALIDATED` (来源: AUTOSAR_ECUC)
- **描述**: Definition of whether or not validation of the CRC is supported.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `288a4d2d-b0d8-44d8-8ba9-c27d7bc5461d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTSynGlobalTimeSlaveHandleId

- **UUID**: `244aa8ff-670f-456e-a25c-eac05b1df60c`
- **参数名**: `CanTSynGlobalTimeSlaveHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanTSynGlobalTimePduRef

- **UUID**: `ff0ee991-ccdc-469a-89ff-16cfc8b8acc1`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 4. CanTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `288a4d2d-b0d8-44d8-8ba9-c27d7bc5461d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeSlaveHandleId

- **UUID**: `244aa8ff-670f-456e-a25c-eac05b1df60c`
- **参数名**: `CanTSynGlobalTimeSlaveHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTSynGlobalTimePduRef

- **UUID**: `ff0ee991-ccdc-469a-89ff-16cfc8b8acc1`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 11. CanTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `e2a7d862-fc1b-420e-a0dd-dbd35bb9e147`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMaster`
- **多重性**: [0..infinite]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

###### 参数配置

此容器包含 **4** 个参数：

####### FLOAT 类型参数

######## 1. CanTSynGlobalTimeTxFollowUpOffset

- **UUID**: `acdaf4e6-57c6-48d8-bff5-7a921363bd75`
- **参数名**: `CanTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the transmission time offset between a SYNC message and the related FUP message resp. OFS message and related OFNS message. Unit: seconds.

######## 2. CanTSynGlobalTimeTxPeriod

- **UUID**: `d928eace-ac32-4067-b2f9-38dde1ad107c`
- **参数名**: `CanTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period. Unit: seconds

######## 3. CanTSynMasterConfirmationTimeout

- **UUID**: `9f6a97ff-2266-4af0-bf51-4771c29db32c`
- **参数名**: `CanTSynMasterConfirmationTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the confirmation timeout after transmission of a SYNC message resp. OFS message. Unit: seconds.

####### ENUMERATION 类型参数

######## 1. CanTSynGlobalTimeTxCrcSecured

- **UUID**: `028c9dae-7cc2-48c1-b3cd-78f7a829f450`
- **参数名**: `CanTSynGlobalTimeTxCrcSecured`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_NOT_SUPPORTED` (来源: AUTOSAR_ECUC)
  - `CRC_SUPPORTED` (来源: AUTOSAR_ECUC)
- **描述**: This represents the configuration of whether or not CRC is supported.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `224dae13-8577-42b2-914b-a481e307a9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `3cac33bb-89fa-43ca-b863-1b4d7b552d56`
- **参数名**: `CanTSynGlobalTimeMasterConfirmationHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTSynGlobalTimePduRef

- **UUID**: `ed4fbecb-709f-443e-a33e-255d09f6d2de`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 12. CanTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `224dae13-8577-42b2-914b-a481e307a9a7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `3cac33bb-89fa-43ca-b863-1b4d7b552d56`
- **参数名**: `CanTSynGlobalTimeMasterConfirmationHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTSynGlobalTimePduRef

- **UUID**: `ed4fbecb-709f-443e-a33e-255d09f6d2de`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 13. CanTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `e38377b2-690c-4029-a86c-8d889be07808`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

Configuration of a global time slave. Each global time domain is required to have at least one time slave. The configured ECU may or may not represent a time slave.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. CanTSynRxCrcValidated

- **UUID**: `6126e429-bd7f-4ad2-97ec-944474cb6481`
- **参数名**: `CanTSynRxCrcValidated`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_IGNORED` (来源: AUTOSAR_ECUC)
  - `CRC_NOT_VALIDATED` (来源: AUTOSAR_ECUC)
  - `CRC_VALIDATED` (来源: AUTOSAR_ECUC)
- **描述**: Definition of whether or not validation of the CRC is supported.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `288a4d2d-b0d8-44d8-8ba9-c27d7bc5461d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTSynGlobalTimeSlaveHandleId

- **UUID**: `244aa8ff-670f-456e-a25c-eac05b1df60c`
- **参数名**: `CanTSynGlobalTimeSlaveHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanTSynGlobalTimePduRef

- **UUID**: `ff0ee991-ccdc-469a-89ff-16cfc8b8acc1`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 14. CanTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `288a4d2d-b0d8-44d8-8ba9-c27d7bc5461d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container encloses the configuration of the PDU that is supposed to contain the global time information.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTSynGlobalTimeSlaveHandleId

- **UUID**: `244aa8ff-670f-456e-a25c-eac05b1df60c`
- **参数名**: `CanTSynGlobalTimeSlaveHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This represents the handle ID of the PDU that contains the global time information.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanTSynGlobalTimePduRef

- **UUID**: `ff0ee991-ccdc-469a-89ff-16cfc8b8acc1`
- **引用名**: `CanTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

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

1. **CanTSyn**
