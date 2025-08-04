# FrTSyn - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:21

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrTSyn](#frtsyn)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrTSyn

#### 基本信息

- **UUID**: `95583b1d-b9f2-456d-9cfb-aa5cead70c54`
- **模块名称**: `FrTSyn`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

This represents the specific configuration variant for the TSyn on Flexray.

#### 版本历史

共有 **4** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2014-08-26T09:27:58+02:00
- **发布者**: visssf

**变更内容**:

##### 2. 版本 1.00.01

- **发布日期**: 2015-03-20T08:57:30+01:00
- **发布者**: visssf

**变更内容**:

##### 3. 版本 2.00.00

- **发布日期**: 2015-09-22T09:26:14+02:00
- **发布者**: visssf

**变更内容**:

##### 4. 版本 2.01.00

- **发布日期**: 2016-02-26T11:52:11+01:00
- **发布者**: visssf

**变更内容**:

#### 配置容器

本模块包含 **10** 个配置容器：

##### 1. FrTSynGeneral

**容器属性**:

- **UUID**: `b2d6f6c6-03f1-4c43-93b9-22d55f02c31f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGeneral`
- **多重性**: [1..1]

**容器描述**:

This container holds the general parameters of the Flexray-specific Synchronized Time-base Manager

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. FrTSynDevErrorDetect

- **UUID**: `1983eba3-afd9-4a67-9f25-63424e723066`
- **参数名**: `FrTSynDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switch for enabling the development error detection.

######## 2. FrTSynVersionInfo

- **UUID**: `3d6306e8-fdeb-4c0c-9c2d-25060b66ca48`
- **参数名**: `FrTSynVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Activate/Deactivate the version information API (FrTSyn_GetVersionInfo). True: version information API activated False: version information API deactivated.

####### FLOAT 类型参数

######## 1. FrTSynMainFunctionPeriod

- **UUID**: `c15e73f2-c481-411d-8ed4-cd8f86d91466`
- **参数名**: `FrTSynMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Schedule period of the main function FrTSyn_MainFunction. Unit: [s].

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FrTSynGlobalTimeOfsDataIDList

**容器属性**:

- **UUID**: `8742b81d-4ed1-48a5-90ba-f1c0b0bdb779`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `4d325d1c-c117-4e13-a0e3-d1910c6df658`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `1957894f-9379-4a47-b0c0-49dc1304a620`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

############ 2. FrTSynGlobalTimeOfsDataIDListValue

- **UUID**: `f8c7d06a-4e4f-4d11-afc3-e12ef6ea0f5a`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

####### 2. FrTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `4d325d1c-c117-4e13-a0e3-d1910c6df658`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `1957894f-9379-4a47-b0c0-49dc1304a620`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 2. FrTSynGlobalTimeOfsDataIDListValue

- **UUID**: `f8c7d06a-4e4f-4d11-afc3-e12ef6ea0f5a`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

####### 3. FrTSynGlobalTimeSyncDataIDList

**容器属性**:

- **UUID**: `57afac1e-9b6c-42e8-8b2b-944692f70263`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `3efc7ecd-5afe-4744-8c05-286189157d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `3ce0ec93-3a30-4499-8590-89064491c8e5`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

############ 2. FrTSynGlobalTimeSyncDataIDListValue

- **UUID**: `bb8efba2-cc58-40a1-b5d6-857850c7f461`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

####### 4. FrTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `3efc7ecd-5afe-4744-8c05-286189157d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `3ce0ec93-3a30-4499-8590-89064491c8e5`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 2. FrTSynGlobalTimeSyncDataIDListValue

- **UUID**: `bb8efba2-cc58-40a1-b5d6-857850c7f461`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 2. FrTSynGlobalTimeOfsDataIDList

**容器属性**:

- **UUID**: `8742b81d-4ed1-48a5-90ba-f1c0b0bdb779`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `4d325d1c-c117-4e13-a0e3-d1910c6df658`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `1957894f-9379-4a47-b0c0-49dc1304a620`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

########## 2. FrTSynGlobalTimeOfsDataIDListValue

- **UUID**: `f8c7d06a-4e4f-4d11-afc3-e12ef6ea0f5a`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

##### 3. FrTSynGlobalTimeOfsDataIDListElement

**容器属性**:

- **UUID**: `4d325d1c-c117-4e13-a0e3-d1910c6df658`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeOfsDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrTSynGlobalTimeOfsDataIDListIndex

- **UUID**: `1957894f-9379-4a47-b0c0-49dc1304a620`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

######## 2. FrTSynGlobalTimeOfsDataIDListValue

- **UUID**: `f8c7d06a-4e4f-4d11-afc3-e12ef6ea0f5a`
- **参数名**: `FrTSynGlobalTimeOfsDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for OFS messages ensures the identification of data elements due to CRC calculation process.

##### 4. FrTSynGlobalTimeSyncDataIDList

**容器属性**:

- **UUID**: `57afac1e-9b6c-42e8-8b2b-944692f70263`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDList`
- **多重性**: [1..1]

**容器描述**:

The DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `3efc7ecd-5afe-4744-8c05-286189157d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `3ce0ec93-3a30-4499-8590-89064491c8e5`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

########## 2. FrTSynGlobalTimeSyncDataIDListValue

- **UUID**: `bb8efba2-cc58-40a1-b5d6-857850c7f461`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 5. FrTSynGlobalTimeSyncDataIDListElement

**容器属性**:

- **UUID**: `3efc7ecd-5afe-4744-8c05-286189157d62`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSyncDataIDListElement`
- **多重性**: [16..16]

**容器描述**:

Element of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrTSynGlobalTimeSyncDataIDListIndex

- **UUID**: `3ce0ec93-3a30-4499-8590-89064491c8e5`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Index of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

######## 2. FrTSynGlobalTimeSyncDataIDListValue

- **UUID**: `bb8efba2-cc58-40a1-b5d6-857850c7f461`
- **参数名**: `FrTSynGlobalTimeSyncDataIDListValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Value of the DataIDList for SYNC messages ensures the identification of data elements due to CRC calculation process.

##### 6. FrTSynGlobalTimeDomain

**容器属性**:

- **UUID**: `2a2c3403-f52d-4f26-90dd-a3373cbbd944`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeDomain`
- **多重性**: [1..infinite]

**容器描述**:

This represents the existence of a global time domain on Flexray. The FrTSyn module can administrate several global time domains at the same time that in itself form a hierarchy of domains and sub-domains.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrTSynGlobalTimeDomainId

- **UUID**: `6bd287d0-cd0f-49d5-917c-246ba8261671`
- **参数名**: `FrTSynGlobalTimeDomainId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The global time domain ID.

######## 2. FrTSynGlobalTimeSequenceCounterJumpWidth

- **UUID**: `6797a71b-7add-4a3d-973d-408880680034`
- **参数名**: `FrTSynGlobalTimeSequenceCounterJumpWidth`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: The SequenceCounterJumpWidth specifies the maximum allowed gap of the Sequence Counter between two SYNC resp. two OFS messages.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrTSynSynchronizedTimeBaseRef

- **UUID**: `70f35333-f467-40f7-9292-2e4d36af7623`
- **引用名**: `FrTSynSynchronizedTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **描述**: Mandatory reference to the required synchronized time-base.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FrTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `d51d41f6-629c-42ed-956e-938c0a6df97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMaster`
- **多重性**: [0..infinite]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. FrTSynGlobalTimeTxPeriod

- **UUID**: `c6061087-9a2f-439d-9c0f-dcadb24bb670`
- **参数名**: `FrTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the TX period. Unit: seconds

######### ENUMERATION 类型参数

########## 1. FrTSynGlobalTimeTxCrcSecured

- **UUID**: `1e4a4108-0c3f-45cc-b3fb-9d7440bf3cdb`
- **参数名**: `FrTSynGlobalTimeTxCrcSecured`
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

######### 1. FrTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `9df6d907-25b1-4119-9386-a68a6b472c1e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU sent by the global time master for the given global time domain.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `258138b9-5ecb-4638-bb88-0861f76cf520`
- **参数名**: `FrTSynGlobalTimeMasterConfirmationHandleId`
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

############ 1. FrTSynGlobalTimePduRef

- **UUID**: `d341c0f4-e9fb-4453-a0c4-8bf17b699bed`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 2. FrTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `9df6d907-25b1-4119-9386-a68a6b472c1e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU sent by the global time master for the given global time domain.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `258138b9-5ecb-4638-bb88-0861f76cf520`
- **参数名**: `FrTSynGlobalTimeMasterConfirmationHandleId`
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

########## 1. FrTSynGlobalTimePduRef

- **UUID**: `d341c0f4-e9fb-4453-a0c4-8bf17b699bed`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 3. FrTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `4c8dc0c1-cd5e-4583-9868-e7316f09d987`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

This represents the time slave for the enclosing global time domain.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FrTSynRxCrcValidated

- **UUID**: `1b9ad55b-62e9-47f1-8975-8e79a79c98cc`
- **参数名**: `FrTSynRxCrcValidated`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_IGNORED` (来源: AUTOSAR_ECUC)
  - `CRC_NOT_VALIDATED` (来源: AUTOSAR_ECUC)
  - `CRC_VALIDATED` (来源: AUTOSAR_ECUC)
- **描述**: This parameter controls whether or not CRC validation shall be supported.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `b9ed61bc-d1f3-4624-aec4-f782c64e66d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU received by the time slave for the given global time domain.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrTSynGlobalTimeSlaveHandleId

- **UUID**: `82b3005b-09cd-49ab-81ca-8675dc9251bd`
- **参数名**: `FrTSynGlobalTimeSlaveHandleId`
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

############ 1. FrTSynGlobalTimePduRef

- **UUID**: `c1f89a23-dd78-46bb-863e-80213c975069`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

####### 4. FrTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `b9ed61bc-d1f3-4624-aec4-f782c64e66d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU received by the time slave for the given global time domain.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeSlaveHandleId

- **UUID**: `82b3005b-09cd-49ab-81ca-8675dc9251bd`
- **参数名**: `FrTSynGlobalTimeSlaveHandleId`
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

########## 1. FrTSynGlobalTimePduRef

- **UUID**: `c1f89a23-dd78-46bb-863e-80213c975069`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 7. FrTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `d51d41f6-629c-42ed-956e-938c0a6df97f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMaster`
- **多重性**: [0..infinite]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. FrTSynGlobalTimeTxPeriod

- **UUID**: `c6061087-9a2f-439d-9c0f-dcadb24bb670`
- **参数名**: `FrTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents the TX period. Unit: seconds

####### ENUMERATION 类型参数

######## 1. FrTSynGlobalTimeTxCrcSecured

- **UUID**: `1e4a4108-0c3f-45cc-b3fb-9d7440bf3cdb`
- **参数名**: `FrTSynGlobalTimeTxCrcSecured`
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

####### 1. FrTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `9df6d907-25b1-4119-9386-a68a6b472c1e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU sent by the global time master for the given global time domain.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `258138b9-5ecb-4638-bb88-0861f76cf520`
- **参数名**: `FrTSynGlobalTimeMasterConfirmationHandleId`
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

########## 1. FrTSynGlobalTimePduRef

- **UUID**: `d341c0f4-e9fb-4453-a0c4-8bf17b699bed`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 8. FrTSynGlobalTimeMasterPdu

**容器属性**:

- **UUID**: `9df6d907-25b1-4119-9386-a68a6b472c1e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeMasterPdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU sent by the global time master for the given global time domain.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTSynGlobalTimeMasterConfirmationHandleId

- **UUID**: `258138b9-5ecb-4638-bb88-0861f76cf520`
- **参数名**: `FrTSynGlobalTimeMasterConfirmationHandleId`
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

######## 1. FrTSynGlobalTimePduRef

- **UUID**: `d341c0f4-e9fb-4453-a0c4-8bf17b699bed`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 9. FrTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `4c8dc0c1-cd5e-4583-9868-e7316f09d987`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

This represents the time slave for the enclosing global time domain.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FrTSynRxCrcValidated

- **UUID**: `1b9ad55b-62e9-47f1-8975-8e79a79c98cc`
- **参数名**: `FrTSynRxCrcValidated`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CRC_IGNORED` (来源: AUTOSAR_ECUC)
  - `CRC_NOT_VALIDATED` (来源: AUTOSAR_ECUC)
  - `CRC_VALIDATED` (来源: AUTOSAR_ECUC)
- **描述**: This parameter controls whether or not CRC validation shall be supported.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `b9ed61bc-d1f3-4624-aec4-f782c64e66d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU received by the time slave for the given global time domain.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrTSynGlobalTimeSlaveHandleId

- **UUID**: `82b3005b-09cd-49ab-81ca-8675dc9251bd`
- **参数名**: `FrTSynGlobalTimeSlaveHandleId`
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

########## 1. FrTSynGlobalTimePduRef

- **UUID**: `c1f89a23-dd78-46bb-863e-80213c975069`
- **引用名**: `FrTSynGlobalTimePduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Pdu taken to transmit the global time information. The global time master of a global time domain acts as the sender of the Pdu while all the time slaves are supposed to receive the Pdu.

##### 10. FrTSynGlobalTimeSlavePdu

**容器属性**:

- **UUID**: `b9ed61bc-d1f3-4624-aec4-f782c64e66d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrTSynGlobalTimeSlavePdu`
- **多重性**: [1..1]

**容器描述**:

This container carries all properties required to configure the PDU received by the time slave for the given global time domain.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrTSynGlobalTimeSlaveHandleId

- **UUID**: `82b3005b-09cd-49ab-81ca-8675dc9251bd`
- **参数名**: `FrTSynGlobalTimeSlaveHandleId`
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

######## 1. FrTSynGlobalTimePduRef

- **UUID**: `c1f89a23-dd78-46bb-863e-80213c975069`
- **引用名**: `FrTSynGlobalTimePduRef`
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

1. **FrTSyn**
