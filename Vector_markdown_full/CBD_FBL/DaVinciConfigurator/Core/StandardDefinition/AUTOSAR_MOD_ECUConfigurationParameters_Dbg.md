# Dbg - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:39

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dbg](#dbg)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dbg

#### 基本信息

- **UUID**: `ECUC:07c05ff8-231b-470b-a8fe-eba6a00489ce`
- **模块名称**: `Dbg`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the debugging module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **19** 个配置容器：

##### 1. DbgBuffering

**容器属性**:

- **UUID**: `ECUC:3e528341-0f7c-4813-80cb-8b61f655cbb1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgBuffering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the parameters to manage the storage of debugging data in RAM.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DbgBufferSize

- **UUID**: `ECUC:7487025d-2e27-45a8-9522-d0020d108a1e`
- **参数名**: `DbgBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Size in bytes of the RAM for the ring buffer. A size of 0 means that no buffer exists. All data records are directly transferred.

####### ENUMERATION 类型参数

######## 1. DbgBufferStrategy

- **UUID**: `ECUC:2cd5e173-4584-4add-8e6a-79504f17972c`
- **参数名**: `DbgBufferStrategy`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `StopStorage`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `OverwriteOldestEntries` (来源: AUTOSAR_ECUC)
  - `StopStorage` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Strategy of buffer operations when it is full: overwrite oldest entries or stop the storage.

######## 2. DbgBufferTransmission

- **UUID**: `ECUC:9f873f88-b110-44e9-85e4-a0db93281b8f`
- **参数名**: `DbgBufferTransmission`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `StartOnHostRequest`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `StartAfterInitialization` (来源: AUTOSAR_ECUC)
  - `StartOnHostRequest` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Automatic or requested transmission of the buffer.

##### 2. DbgCommunication

**容器属性**:

- **UUID**: `ECUC:b1e1b4df-8ab3-4202-b42b-28b228340a19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgCommunication`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds all configuration parameters for communication.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DbgRxPdu

**容器属性**:

- **UUID**: `ECUC:52f45ef1-34e5-491f-99f1-5e83b0b3e3ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds configuration parameters for the receive-pdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DbgRxPduId

- **UUID**: `ECUC:762cbd3c-795f-4dbf-8e1a-ed6ec9520ff5`
- **参数名**: `DbgRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the PduR to indicate the reception of the DbgRxPdu to the Dbg module. The actual value of this parameter is fixed to 0 since there is only one RxPdu for the Dbg module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DbgReceiveIPduRef

- **UUID**: `ECUC:dd9962b2-145d-46fb-ba07-517fc24a910e`
- **引用名**: `DbgReceiveIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the receive I-PDU.

####### 2. DbgTxPdu

**容器属性**:

- **UUID**: `ECUC:99677725-a4f4-4c2f-8cd1-129e81237726`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds configuration parameters for the transmit-pdu.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DbgTxConfirmationPduId

- **UUID**: `ECUC:3f738332-5fe2-42f8-b16f-8205b807b0b1`
- **参数名**: `DbgTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the PduR to confirm the transmission of the DbgTxPdu to the Dbg module. The actual value of this parameter is fixed to 0 since there is only one TxPdu for the Dbg module.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DbgSendIPduRef

- **UUID**: `ECUC:c481ebfd-9efe-40e3-b63b-2a069b2db075`
- **引用名**: `DbgSendIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the send I-PDU.

##### 3. DbgRxPdu

**容器属性**:

- **UUID**: `ECUC:52f45ef1-34e5-491f-99f1-5e83b0b3e3ca`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgRxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds configuration parameters for the receive-pdu.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DbgRxPduId

- **UUID**: `ECUC:762cbd3c-795f-4dbf-8e1a-ed6ec9520ff5`
- **参数名**: `DbgRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the PduR to indicate the reception of the DbgRxPdu to the Dbg module. The actual value of this parameter is fixed to 0 since there is only one RxPdu for the Dbg module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DbgReceiveIPduRef

- **UUID**: `ECUC:dd9962b2-145d-46fb-ba07-517fc24a910e`
- **引用名**: `DbgReceiveIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the receive I-PDU.

##### 4. DbgTxPdu

**容器属性**:

- **UUID**: `ECUC:99677725-a4f4-4c2f-8cd1-129e81237726`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgTxPdu`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds configuration parameters for the transmit-pdu.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DbgTxConfirmationPduId

- **UUID**: `ECUC:3f738332-5fe2-42f8-b16f-8205b807b0b1`
- **参数名**: `DbgTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PUBLISHED-INFORMATION: VARIANT-POST-BUILD
  - PUBLISHED-INFORMATION: VARIANT-PRE-COMPILE
- **描述**: Handle Id to be used by the PduR to confirm the transmission of the DbgTxPdu to the Dbg module. The actual value of this parameter is fixed to 0 since there is only one TxPdu for the Dbg module.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DbgSendIPduRef

- **UUID**: `ECUC:c481ebfd-9efe-40e3-b63b-2a069b2db075`
- **引用名**: `DbgSendIPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the send I-PDU.

##### 5. DbgGeneral

**容器属性**:

- **UUID**: `ECUC:e08d9312-2e84-4b33-9269-9d8c45f325e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds the general parameters of the debugging module.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. DbgDevErrorDetect

- **UUID**: `ECUC:ad35a742-5ad7-439a-9794-45b351b1fa83`
- **参数名**: `DbgDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/Disables development error detection.

######## 2. DbgVersionInfoApi

- **UUID**: `ECUC:56b3a6b2-2016-4031-acbf-64554837a708`
- **参数名**: `DbgVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the version information API (Dbg_GetVersionInfo). True: version information API activated False: version information API deactivated.

####### STRING 类型参数

######## 1. DbgHeaderFileInclusion

- **UUID**: `ECUC:e7253f4f-b4ab-4a1e-91e2-cfeed9af7006`
- **参数名**: `DbgHeaderFileInclusion`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 正则表达式: `[a-zA-Z0-9_]([a-zA-Z0-9\._])*`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the header file(s) to be included by the Dbg module.

##### 6. DbgMultipleConfigurationContainer

**容器属性**:

- **UUID**: `ECUC:dee475e8-224f-4c2a-882c-2a118a83756a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgMultipleConfigurationContainer`
- **多重性**: [1..1]
- **多配置容器**: true

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DbgMaxDynamicDID

- **UUID**: `ECUC:4190c093-5ae2-4b40-a693-623f261d3de0`
- **参数名**: `DbgMaxDynamicDID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..200]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of dynamic DIDs. This value is only needed to reserve memory for dynamic DIDs added by the host at runtime. If this parameter is not supplied it is automatically set to the configured number of static DIDs.

######## 2. DbgMaxStaticDID

- **UUID**: `ECUC:294808d4-ad29-469a-918a-b2242e475a76`
- **参数名**: `DbgMaxStaticDID`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..200]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of static DIDs. This value is only needed to reserve memory for static DIDs added at post-build time. If this parameter is not supplied it is automatically set to the configured number of static DIDs. Static DIDs are zero based and consecutive.

###### 配置容器

本模块包含 **11** 个配置容器：

####### 1. DbgPredefinedDID

**容器属性**:

- **UUID**: `ECUC:afe660e4-4aff-458b-8bf2-22ab0c96c09e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgPredefinedDID`
- **多重性**: [0..16]
- **多配置容器**: false

**容器描述**:

This container holds all configuration parameters for predefined DIDs. For predefined DIDs, only certain values can be changed.

######## 参数配置

此容器包含 **4** 个参数：

######### BOOLEAN 类型参数

########## 1. DbgPredefinedDIDActivation

- **UUID**: `ECUC:1ac4cdc0-4d5d-4a46-8c33-8dd5fd8751ec`
- **参数名**: `DbgPredefinedDIDActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation or not of the DID for debugging.

########## 2. DbgPredefinedDIDBuffering

- **UUID**: `ECUC:bf471886-02b3-44f1-93fd-54e59e12b4b0`
- **参数名**: `DbgPredefinedDIDBuffering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer the data or transmit directly.

########## 3. DbgPredefinedDIDTimeStampActivation

- **UUID**: `ECUC:eeb0ed71-0274-4eb0-b157-272d5659625e`
- **参数名**: `DbgPredefinedDIDTimeStampActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using or not of time stamp.

######### ENUMERATION 类型参数

########## 1. DbgPredefinedDIDName

- **UUID**: `ECUC:626c00fd-f000-48cb-bb64-d8afab7e258f`
- **参数名**: `DbgPredefinedDIDName`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Dbg_PostTaskHook` (来源: AUTOSAR_ECUC)
  - `Dbg_PreTaskHook` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceDetCall` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceFunctionEntry` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceFunctionExit` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTECall` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComCallback` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalIv` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalRx` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalTx` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEVfbSignalReceive` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEVfbSignalSend` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRunnableStart` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRunnableTermination` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceTimestamps` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: List of possible names for predefined DIDs.

######## 配置容器

本模块包含 **5** 个配置容器：

######### 1. DbgAddInfoComSignal

**容器属性**:

- **UUID**: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

########## 参数配置

此容器包含 **1** 个参数：

########### STRING 类型参数

############ 1. DbgComSignalName

- **UUID**: `ECUC:6dbd955f-7512-4368-96db-ea416061cf2b`
- **参数名**: `DbgComSignalName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional name of the traced signal. If present it shall be used in the display of the debugging tool.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DbgComSignalRef

- **UUID**: `ECUC:f66a2085-299a-4095-8bce-8b0508a5bfff`
- **引用名**: `DbgComSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which shall be traced.

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:244bc45e-4f85-93e4-2e3e-ebb122bc3e3d`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######### 2. DbgAddInfoRteCall

**容器属性**:

- **UUID**: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRteCall`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DbgCallComponentId

- **UUID**: `ECUC:736adb6a-36d5-45cd-893b-7e9e586d9a25`
- **参数名**: `DbgCallComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

############ 2. DbgCallInstanceId

- **UUID**: `ECUC:118e0100-1a56-48c2-9346-9865c110d8e8`
- **参数名**: `DbgCallInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

############ 3. DbgCallPortId

- **UUID**: `ECUC:210dc890-99be-4d76-b7bf-fdd5d6d9d002`
- **参数名**: `DbgCallPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

############ 4. DbgCallServiceId

- **UUID**: `ECUC:3f7ff4c6-b29f-4e48-9b0a-acd6ad18f11c`
- **参数名**: `DbgCallServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the OperationProtoype.

########## 引用关系

此容器包含 **2** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:8ad5cf1e-2bda-8d20-4894-f472a472aba3`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

########### INSTANCE-REFERENCE 类型引用

############ 1. DbgServiceInstanceRef

- **UUID**: `ECUC:03eff3b0-d0e6-4cf1-8089-9e42115d6534`
- **引用名**: `DbgServiceInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: CLIENT-SERVER-OPERATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual OperationPrototype which shall be traced.

######### 3. DbgAddInfoRunnable

**容器属性**:

- **UUID**: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRunnable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DbgRunnableComponentId

- **UUID**: `ECUC:330f2bc2-66da-4d3a-a962-dc735fdab504`
- **参数名**: `DbgRunnableComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

############ 2. DbgRunnableId

- **UUID**: `ECUC:e7bd8351-2e31-4a79-b4ac-64ae1d49b11b`
- **参数名**: `DbgRunnableId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the RunnableEntity.

############ 3. DbgRunnableInstanceId

- **UUID**: `ECUC:271ce538-98bc-4a68-bb94-a0ba35360267`
- **参数名**: `DbgRunnableInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

########## 引用关系

此容器包含 **3** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:ac59971a-5cf3-8bbd-3dc9-6e794055dd17`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

############ 2. DbgRunnableEntityRef

- **UUID**: `ECUC:c67c3287-1ccb-4cd2-aa1e-32923e029818`
- **引用名**: `DbgRunnableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual RunnableEntity which shall be traced.

############ 3. DbgSoftwareComponentInstanceRef

- **UUID**: `ECUC:9a5d0a51-c1da-46a3-9ee1-55e5f53d51f9`
- **引用名**: `DbgSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SW-ComponentProtoype which shall be traced.

######### 4. DbgAddInfoVfbSignal

**容器属性**:

- **UUID**: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoVfbSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. DbgVfbComponentId

- **UUID**: `ECUC:01a8f701-a621-4511-99c8-9d021317bd06`
- **参数名**: `DbgVfbComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

############ 2. DbgVfbDataElementId

- **UUID**: `ECUC:892c1bda-20ff-4af1-a8b0-2343fb0aab15`
- **参数名**: `DbgVfbDataElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the DataElementPrototype.

############ 3. DbgVfbInstanceId

- **UUID**: `ECUC:a540b9b8-0038-43df-9a28-ee0e53da8645`
- **参数名**: `DbgVfbInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

############ 4. DbgVfbPortId

- **UUID**: `ECUC:6ba02548-b748-4777-84c8-b43da5b120a0`
- **参数名**: `DbgVfbPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

########## 引用关系

此容器包含 **2** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:b817debf-f439-94f4-2744-8c29e4fb33c8`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

########### INSTANCE-REFERENCE 类型引用

############ 1. DbgDataElementInstanceRef

- **UUID**: `ECUC:a3bba751-daa5-4367-93ae-e131fca20545`
- **引用名**: `DbgDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual DataElementPrototype which shall be traced.

######### 5. DbgPredefinedDIDAddInfo

**容器属性**:

- **UUID**: `ECUC:c4665b22-b9f7-4cfa-8af1-eb27f71154b9`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgPredefinedDIDAddInfo`
- **多重性**: [0..infinite]

**容器选择**:

- **DbgAddInfoComSignal**
  - UUID: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRteCall**
  - UUID: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRunnable**
  - UUID: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoVfbSignal**
  - UUID: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:

**容器描述**:

Additional information in case the Predefined DID needs further configuration parameters.

####### 2. DbgAddInfoComSignal

**容器属性**:

- **UUID**: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. DbgComSignalName

- **UUID**: `ECUC:6dbd955f-7512-4368-96db-ea416061cf2b`
- **参数名**: `DbgComSignalName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional name of the traced signal. If present it shall be used in the display of the debugging tool.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DbgComSignalRef

- **UUID**: `ECUC:f66a2085-299a-4095-8bce-8b0508a5bfff`
- **引用名**: `DbgComSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which shall be traced.

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:244bc45e-4f85-93e4-2e3e-ebb122bc3e3d`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

####### 3. DbgAddInfoRteCall

**容器属性**:

- **UUID**: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRteCall`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DbgCallComponentId

- **UUID**: `ECUC:736adb6a-36d5-45cd-893b-7e9e586d9a25`
- **参数名**: `DbgCallComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgCallInstanceId

- **UUID**: `ECUC:118e0100-1a56-48c2-9346-9865c110d8e8`
- **参数名**: `DbgCallInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

########## 3. DbgCallPortId

- **UUID**: `ECUC:210dc890-99be-4d76-b7bf-fdd5d6d9d002`
- **参数名**: `DbgCallPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

########## 4. DbgCallServiceId

- **UUID**: `ECUC:3f7ff4c6-b29f-4e48-9b0a-acd6ad18f11c`
- **参数名**: `DbgCallServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the OperationProtoype.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:8ad5cf1e-2bda-8d20-4894-f472a472aba3`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######### INSTANCE-REFERENCE 类型引用

########## 1. DbgServiceInstanceRef

- **UUID**: `ECUC:03eff3b0-d0e6-4cf1-8089-9e42115d6534`
- **引用名**: `DbgServiceInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: CLIENT-SERVER-OPERATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual OperationPrototype which shall be traced.

####### 4. DbgAddInfoRunnable

**容器属性**:

- **UUID**: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRunnable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DbgRunnableComponentId

- **UUID**: `ECUC:330f2bc2-66da-4d3a-a962-dc735fdab504`
- **参数名**: `DbgRunnableComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgRunnableId

- **UUID**: `ECUC:e7bd8351-2e31-4a79-b4ac-64ae1d49b11b`
- **参数名**: `DbgRunnableId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the RunnableEntity.

########## 3. DbgRunnableInstanceId

- **UUID**: `ECUC:271ce538-98bc-4a68-bb94-a0ba35360267`
- **参数名**: `DbgRunnableInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

######## 引用关系

此容器包含 **3** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:ac59971a-5cf3-8bbd-3dc9-6e794055dd17`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

########## 2. DbgRunnableEntityRef

- **UUID**: `ECUC:c67c3287-1ccb-4cd2-aa1e-32923e029818`
- **引用名**: `DbgRunnableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual RunnableEntity which shall be traced.

########## 3. DbgSoftwareComponentInstanceRef

- **UUID**: `ECUC:9a5d0a51-c1da-46a3-9ee1-55e5f53d51f9`
- **引用名**: `DbgSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SW-ComponentProtoype which shall be traced.

####### 5. DbgAddInfoVfbSignal

**容器属性**:

- **UUID**: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoVfbSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DbgVfbComponentId

- **UUID**: `ECUC:01a8f701-a621-4511-99c8-9d021317bd06`
- **参数名**: `DbgVfbComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgVfbDataElementId

- **UUID**: `ECUC:892c1bda-20ff-4af1-a8b0-2343fb0aab15`
- **参数名**: `DbgVfbDataElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the DataElementPrototype.

########## 3. DbgVfbInstanceId

- **UUID**: `ECUC:a540b9b8-0038-43df-9a28-ee0e53da8645`
- **参数名**: `DbgVfbInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

########## 4. DbgVfbPortId

- **UUID**: `ECUC:6ba02548-b748-4777-84c8-b43da5b120a0`
- **参数名**: `DbgVfbPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:b817debf-f439-94f4-2744-8c29e4fb33c8`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######### INSTANCE-REFERENCE 类型引用

########## 1. DbgDataElementInstanceRef

- **UUID**: `ECUC:a3bba751-daa5-4367-93ae-e131fca20545`
- **引用名**: `DbgDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual DataElementPrototype which shall be traced.

####### 6. DbgStaticDID

**容器属性**:

- **UUID**: `ECUC:6564daaf-5ff3-41cc-bee9-08fa2a4a5510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgStaticDID`
- **多重性**: [0..200]
- **多配置容器**: false

**容器描述**:

This container holds all configuration parameters for static DIDs. For predefined DIDs, only certain values can be changed.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DbgAutomaticCollectionFrequency

- **UUID**: `ECUC:5c3e24cd-a31d-490c-a62c-6814fbbe89c3`
- **参数名**: `DbgAutomaticCollectionFrequency`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Cycle time of collection in DataCollectionTicks. A value of "0" indicates that the collection takes place only on request.

######### BOOLEAN 类型参数

########## 1. DbgStaticDIDActivation

- **UUID**: `ECUC:be7f690d-86bb-4d8a-b09b-4b4322c8d4d5`
- **参数名**: `DbgStaticDIDActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation or not of the DID for debugging.

########## 2. DbgStaticDIDBuffering

- **UUID**: `ECUC:5f00590e-2b6a-4183-b878-7aec78c1f192`
- **参数名**: `DbgStaticDIDBuffering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer the data or transmit directly.

########## 3. DbgStaticTimeStampActivation

- **UUID**: `ECUC:120f194c-e1f8-4d25-a8c0-7e801f669d0e`
- **参数名**: `DbgStaticTimeStampActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using or not of time stamp.

######### STRING 类型参数

########## 1. DbgStaticDIDNameRef

- **UUID**: `ECUC:f18b6408-8c09-4aeb-ba6c-58ba776b15d3`
- **参数名**: `DbgStaticDIDNameRef`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the DID, translated by the configuration/generation tool into consecutive DID numbers starting from 0.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. DbgAddressSizePair

**容器属性**:

- **UUID**: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddressSizePair`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DbgASAbsoluteAddress

- **UUID**: `ECUC:f26ad0a2-2136-42e9-b018-a84e99287fac`
- **参数名**: `DbgASAbsoluteAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute address of memory location to be debugged.

############ 2. DbgASSize

- **UUID**: `ECUC:4b26a816-11ca-43c5-829d-03684d1605a1`
- **参数名**: `DbgASSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute size in Bytes of memory location to be debugged.

########### LINKER-SYMBOL 类型参数

############ 1. DbgASNameRef

- **UUID**: `ECUC:faf3a6cd-406e-4496-81b3-1af954633d1a`
- **参数名**: `DbgASNameRef`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Symbolic name of the variable, translated by the configuration/generation tool into the address and size of the variable.

######### 2. DbgDebugData

**容器属性**:

- **UUID**: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to staticMemory used for Debug Data.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgDebugDataRef

- **UUID**: `ECUC:8dfda3f1-4048-42bd-b6b4-52263cf45d62`
- **引用名**: `DbgDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to staticMemory used for Debug Data.

######### 3. DbgLocalDebugData

**容器属性**:

- **UUID**: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgLocalDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to a localDebugData.

########## 引用关系

此容器包含 **1** 个引用：

########### FOREIGN-REFERENCE 类型引用

############ 1. DbgLocalDebugDataRef

- **UUID**: `ECUC:9be85ef2-5b62-4543-8feb-bc8c62192cc1`
- **引用名**: `DbgLocalDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a localDebugData.

######### 4. DbgStaticDIDData

**容器属性**:

- **UUID**: `ECUC:d8ec1f61-b0c2-49bc-a6f3-a7eff6d5fd01`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgStaticDIDData`
- **多重性**: [1..65535]

**容器选择**:

- **DbgAddressSizePair**
  - UUID: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
  - 描述: This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.
- **DbgDebugData**
  - UUID: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
  - 描述: Reference to staticMemory used for Debug Data.
- **DbgLocalDebugData**
  - UUID: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
  - 描述: Reference to a localDebugData.

**容器描述**:

Choice how the DID is to be configured.

####### 7. DbgAddressSizePair

**容器属性**:

- **UUID**: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddressSizePair`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DbgASAbsoluteAddress

- **UUID**: `ECUC:f26ad0a2-2136-42e9-b018-a84e99287fac`
- **参数名**: `DbgASAbsoluteAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute address of memory location to be debugged.

########## 2. DbgASSize

- **UUID**: `ECUC:4b26a816-11ca-43c5-829d-03684d1605a1`
- **参数名**: `DbgASSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute size in Bytes of memory location to be debugged.

######### LINKER-SYMBOL 类型参数

########## 1. DbgASNameRef

- **UUID**: `ECUC:faf3a6cd-406e-4496-81b3-1af954633d1a`
- **参数名**: `DbgASNameRef`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Symbolic name of the variable, translated by the configuration/generation tool into the address and size of the variable.

####### 8. DbgDebugData

**容器属性**:

- **UUID**: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to staticMemory used for Debug Data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgDebugDataRef

- **UUID**: `ECUC:8dfda3f1-4048-42bd-b6b4-52263cf45d62`
- **引用名**: `DbgDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to staticMemory used for Debug Data.

####### 9. DbgLocalDebugData

**容器属性**:

- **UUID**: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgLocalDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to a localDebugData.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgLocalDebugDataRef

- **UUID**: `ECUC:9be85ef2-5b62-4543-8feb-bc8c62192cc1`
- **引用名**: `DbgLocalDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a localDebugData.

####### 10. DbgPredefinedDIDAddInfo

**容器属性**:

- **UUID**: `ECUC:c4665b22-b9f7-4cfa-8af1-eb27f71154b9`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgPredefinedDIDAddInfo`
- **多重性**: [0..infinite]

**容器选择**:

- **DbgAddInfoComSignal**
  - UUID: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRteCall**
  - UUID: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRunnable**
  - UUID: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoVfbSignal**
  - UUID: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:

**容器描述**:

Additional information in case the Predefined DID needs further configuration parameters.

####### 11. DbgStaticDIDData

**容器属性**:

- **UUID**: `ECUC:d8ec1f61-b0c2-49bc-a6f3-a7eff6d5fd01`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgStaticDIDData`
- **多重性**: [1..65535]

**容器选择**:

- **DbgAddressSizePair**
  - UUID: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
  - 描述: This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.
- **DbgDebugData**
  - UUID: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
  - 描述: Reference to staticMemory used for Debug Data.
- **DbgLocalDebugData**
  - UUID: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
  - 描述: Reference to a localDebugData.

**容器描述**:

Choice how the DID is to be configured.

##### 7. DbgPredefinedDID

**容器属性**:

- **UUID**: `ECUC:afe660e4-4aff-458b-8bf2-22ab0c96c09e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgPredefinedDID`
- **多重性**: [0..16]
- **多配置容器**: false

**容器描述**:

This container holds all configuration parameters for predefined DIDs. For predefined DIDs, only certain values can be changed.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. DbgPredefinedDIDActivation

- **UUID**: `ECUC:1ac4cdc0-4d5d-4a46-8c33-8dd5fd8751ec`
- **参数名**: `DbgPredefinedDIDActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation or not of the DID for debugging.

######## 2. DbgPredefinedDIDBuffering

- **UUID**: `ECUC:bf471886-02b3-44f1-93fd-54e59e12b4b0`
- **参数名**: `DbgPredefinedDIDBuffering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer the data or transmit directly.

######## 3. DbgPredefinedDIDTimeStampActivation

- **UUID**: `ECUC:eeb0ed71-0274-4eb0-b157-272d5659625e`
- **参数名**: `DbgPredefinedDIDTimeStampActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using or not of time stamp.

####### ENUMERATION 类型参数

######## 1. DbgPredefinedDIDName

- **UUID**: `ECUC:626c00fd-f000-48cb-bb64-d8afab7e258f`
- **参数名**: `DbgPredefinedDIDName`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `Dbg_PostTaskHook` (来源: AUTOSAR_ECUC)
  - `Dbg_PreTaskHook` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceDetCall` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceFunctionEntry` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceFunctionExit` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTECall` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComCallback` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalIv` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalRx` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEComSignalTx` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEVfbSignalReceive` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRTEVfbSignalSend` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRunnableStart` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceRunnableTermination` (来源: AUTOSAR_ECUC)
  - `Dbg_TraceTimestamps` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: List of possible names for predefined DIDs.

###### 配置容器

本模块包含 **5** 个配置容器：

####### 1. DbgAddInfoComSignal

**容器属性**:

- **UUID**: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **1** 个参数：

######### STRING 类型参数

########## 1. DbgComSignalName

- **UUID**: `ECUC:6dbd955f-7512-4368-96db-ea416061cf2b`
- **参数名**: `DbgComSignalName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional name of the traced signal. If present it shall be used in the display of the debugging tool.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DbgComSignalRef

- **UUID**: `ECUC:f66a2085-299a-4095-8bce-8b0508a5bfff`
- **引用名**: `DbgComSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which shall be traced.

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:244bc45e-4f85-93e4-2e3e-ebb122bc3e3d`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

####### 2. DbgAddInfoRteCall

**容器属性**:

- **UUID**: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRteCall`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DbgCallComponentId

- **UUID**: `ECUC:736adb6a-36d5-45cd-893b-7e9e586d9a25`
- **参数名**: `DbgCallComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgCallInstanceId

- **UUID**: `ECUC:118e0100-1a56-48c2-9346-9865c110d8e8`
- **参数名**: `DbgCallInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

########## 3. DbgCallPortId

- **UUID**: `ECUC:210dc890-99be-4d76-b7bf-fdd5d6d9d002`
- **参数名**: `DbgCallPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

########## 4. DbgCallServiceId

- **UUID**: `ECUC:3f7ff4c6-b29f-4e48-9b0a-acd6ad18f11c`
- **参数名**: `DbgCallServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the OperationProtoype.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:8ad5cf1e-2bda-8d20-4894-f472a472aba3`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######### INSTANCE-REFERENCE 类型引用

########## 1. DbgServiceInstanceRef

- **UUID**: `ECUC:03eff3b0-d0e6-4cf1-8089-9e42115d6534`
- **引用名**: `DbgServiceInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: CLIENT-SERVER-OPERATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual OperationPrototype which shall be traced.

####### 3. DbgAddInfoRunnable

**容器属性**:

- **UUID**: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRunnable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DbgRunnableComponentId

- **UUID**: `ECUC:330f2bc2-66da-4d3a-a962-dc735fdab504`
- **参数名**: `DbgRunnableComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgRunnableId

- **UUID**: `ECUC:e7bd8351-2e31-4a79-b4ac-64ae1d49b11b`
- **参数名**: `DbgRunnableId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the RunnableEntity.

########## 3. DbgRunnableInstanceId

- **UUID**: `ECUC:271ce538-98bc-4a68-bb94-a0ba35360267`
- **参数名**: `DbgRunnableInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

######## 引用关系

此容器包含 **3** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:ac59971a-5cf3-8bbd-3dc9-6e794055dd17`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

########## 2. DbgRunnableEntityRef

- **UUID**: `ECUC:c67c3287-1ccb-4cd2-aa1e-32923e029818`
- **引用名**: `DbgRunnableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual RunnableEntity which shall be traced.

########## 3. DbgSoftwareComponentInstanceRef

- **UUID**: `ECUC:9a5d0a51-c1da-46a3-9ee1-55e5f53d51f9`
- **引用名**: `DbgSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SW-ComponentProtoype which shall be traced.

####### 4. DbgAddInfoVfbSignal

**容器属性**:

- **UUID**: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoVfbSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. DbgVfbComponentId

- **UUID**: `ECUC:01a8f701-a621-4511-99c8-9d021317bd06`
- **参数名**: `DbgVfbComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

########## 2. DbgVfbDataElementId

- **UUID**: `ECUC:892c1bda-20ff-4af1-a8b0-2343fb0aab15`
- **参数名**: `DbgVfbDataElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the DataElementPrototype.

########## 3. DbgVfbInstanceId

- **UUID**: `ECUC:a540b9b8-0038-43df-9a28-ee0e53da8645`
- **参数名**: `DbgVfbInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

########## 4. DbgVfbPortId

- **UUID**: `ECUC:6ba02548-b748-4777-84c8-b43da5b120a0`
- **参数名**: `DbgVfbPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

######## 引用关系

此容器包含 **2** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:b817debf-f439-94f4-2744-8c29e4fb33c8`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######### INSTANCE-REFERENCE 类型引用

########## 1. DbgDataElementInstanceRef

- **UUID**: `ECUC:a3bba751-daa5-4367-93ae-e131fca20545`
- **引用名**: `DbgDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual DataElementPrototype which shall be traced.

####### 5. DbgPredefinedDIDAddInfo

**容器属性**:

- **UUID**: `ECUC:c4665b22-b9f7-4cfa-8af1-eb27f71154b9`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgPredefinedDIDAddInfo`
- **多重性**: [0..infinite]

**容器选择**:

- **DbgAddInfoComSignal**
  - UUID: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRteCall**
  - UUID: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRunnable**
  - UUID: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoVfbSignal**
  - UUID: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:

**容器描述**:

Additional information in case the Predefined DID needs further configuration parameters.

##### 8. DbgAddInfoComSignal

**容器属性**:

- **UUID**: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoComSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. DbgComSignalName

- **UUID**: `ECUC:6dbd955f-7512-4368-96db-ea416061cf2b`
- **参数名**: `DbgComSignalName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional name of the traced signal. If present it shall be used in the display of the debugging tool.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DbgComSignalRef

- **UUID**: `ECUC:f66a2085-299a-4095-8bce-8b0508a5bfff`
- **引用名**: `DbgComSignalRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `ComSignal`
- **完整路径**: `/AUTOSAR/EcucDefs/Com/ComConfig/ComSignal`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the ComSignal which shall be traced.

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:244bc45e-4f85-93e4-2e3e-ebb122bc3e3d`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

##### 9. DbgAddInfoRteCall

**容器属性**:

- **UUID**: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRteCall`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DbgCallComponentId

- **UUID**: `ECUC:736adb6a-36d5-45cd-893b-7e9e586d9a25`
- **参数名**: `DbgCallComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

######## 2. DbgCallInstanceId

- **UUID**: `ECUC:118e0100-1a56-48c2-9346-9865c110d8e8`
- **参数名**: `DbgCallInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

######## 3. DbgCallPortId

- **UUID**: `ECUC:210dc890-99be-4d76-b7bf-fdd5d6d9d002`
- **参数名**: `DbgCallPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

######## 4. DbgCallServiceId

- **UUID**: `ECUC:3f7ff4c6-b29f-4e48-9b0a-acd6ad18f11c`
- **参数名**: `DbgCallServiceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the OperationProtoype.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:8ad5cf1e-2bda-8d20-4894-f472a472aba3`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

####### INSTANCE-REFERENCE 类型引用

######## 1. DbgServiceInstanceRef

- **UUID**: `ECUC:03eff3b0-d0e6-4cf1-8089-9e42115d6534`
- **引用名**: `DbgServiceInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: CLIENT-SERVER-OPERATION
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual OperationPrototype which shall be traced.

##### 10. DbgAddInfoRunnable

**容器属性**:

- **UUID**: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoRunnable`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DbgRunnableComponentId

- **UUID**: `ECUC:330f2bc2-66da-4d3a-a962-dc735fdab504`
- **参数名**: `DbgRunnableComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

######## 2. DbgRunnableId

- **UUID**: `ECUC:e7bd8351-2e31-4a79-b4ac-64ae1d49b11b`
- **参数名**: `DbgRunnableId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the RunnableEntity.

######## 3. DbgRunnableInstanceId

- **UUID**: `ECUC:271ce538-98bc-4a68-bb94-a0ba35360267`
- **参数名**: `DbgRunnableInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

###### 引用关系

此容器包含 **3** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:ac59971a-5cf3-8bbd-3dc9-6e794055dd17`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

######## 2. DbgRunnableEntityRef

- **UUID**: `ECUC:c67c3287-1ccb-4cd2-aa1e-32923e029818`
- **引用名**: `DbgRunnableEntityRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: RUNNABLE-ENTITY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual RunnableEntity which shall be traced.

######## 3. DbgSoftwareComponentInstanceRef

- **UUID**: `ECUC:9a5d0a51-c1da-46a3-9ee1-55e5f53d51f9`
- **引用名**: `DbgSoftwareComponentInstanceRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: SW-COMPONENT-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the SW-ComponentProtoype which shall be traced.

##### 11. DbgAddInfoVfbSignal

**容器属性**:

- **UUID**: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddInfoVfbSignal`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Additional information for DIDs with the DbgPredefinedDIDName set to:

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. DbgVfbComponentId

- **UUID**: `ECUC:01a8f701-a621-4511-99c8-9d021317bd06`
- **参数名**: `DbgVfbComponentId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Type.

######## 2. DbgVfbDataElementId

- **UUID**: `ECUC:892c1bda-20ff-4af1-a8b0-2343fb0aab15`
- **参数名**: `DbgVfbDataElementId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the DataElementPrototype.

######## 3. DbgVfbInstanceId

- **UUID**: `ECUC:a540b9b8-0038-43df-9a28-ee0e53da8645`
- **参数名**: `DbgVfbInstanceId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the SW-Component Instance.

######## 4. DbgVfbPortId

- **UUID**: `ECUC:6ba02548-b748-4777-84c8-b43da5b120a0`
- **参数名**: `DbgVfbPortId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Id used to identify the Port.

###### 引用关系

此容器包含 **2** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgBswModuleEntryRef

- **UUID**: `ECUC:b817debf-f439-94f4-2744-8c29e4fb33c8`
- **引用名**: `DbgBswModuleEntryRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: BSW-MODULE-ENTRY
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Foreign reference to the BSWModuleEntry describing the trace function implementation.

####### INSTANCE-REFERENCE 类型引用

######## 1. DbgDataElementInstanceRef

- **UUID**: `ECUC:a3bba751-daa5-4367-93ae-e131fca20545`
- **引用名**: `DbgDataElementInstanceRef`
- **引用类型**: INSTANCE-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the actual DataElementPrototype which shall be traced.

##### 12. DbgStaticDID

**容器属性**:

- **UUID**: `ECUC:6564daaf-5ff3-41cc-bee9-08fa2a4a5510`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgStaticDID`
- **多重性**: [0..200]
- **多配置容器**: false

**容器描述**:

This container holds all configuration parameters for static DIDs. For predefined DIDs, only certain values can be changed.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DbgAutomaticCollectionFrequency

- **UUID**: `ECUC:5c3e24cd-a31d-490c-a62c-6814fbbe89c3`
- **参数名**: `DbgAutomaticCollectionFrequency`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Cycle time of collection in DataCollectionTicks. A value of "0" indicates that the collection takes place only on request.

####### BOOLEAN 类型参数

######## 1. DbgStaticDIDActivation

- **UUID**: `ECUC:be7f690d-86bb-4d8a-b09b-4b4322c8d4d5`
- **参数名**: `DbgStaticDIDActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activation or not of the DID for debugging.

######## 2. DbgStaticDIDBuffering

- **UUID**: `ECUC:5f00590e-2b6a-4183-b878-7aec78c1f192`
- **参数名**: `DbgStaticDIDBuffering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Buffer the data or transmit directly.

######## 3. DbgStaticTimeStampActivation

- **UUID**: `ECUC:120f194c-e1f8-4d25-a8c0-7e801f669d0e`
- **参数名**: `DbgStaticTimeStampActivation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using or not of time stamp.

####### STRING 类型参数

######## 1. DbgStaticDIDNameRef

- **UUID**: `ECUC:f18b6408-8c09-4aeb-ba6c-58ba776b15d3`
- **参数名**: `DbgStaticDIDNameRef`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the DID, translated by the configuration/generation tool into consecutive DID numbers starting from 0.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. DbgAddressSizePair

**容器属性**:

- **UUID**: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddressSizePair`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DbgASAbsoluteAddress

- **UUID**: `ECUC:f26ad0a2-2136-42e9-b018-a84e99287fac`
- **参数名**: `DbgASAbsoluteAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute address of memory location to be debugged.

########## 2. DbgASSize

- **UUID**: `ECUC:4b26a816-11ca-43c5-829d-03684d1605a1`
- **参数名**: `DbgASSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute size in Bytes of memory location to be debugged.

######### LINKER-SYMBOL 类型参数

########## 1. DbgASNameRef

- **UUID**: `ECUC:faf3a6cd-406e-4496-81b3-1af954633d1a`
- **参数名**: `DbgASNameRef`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Symbolic name of the variable, translated by the configuration/generation tool into the address and size of the variable.

####### 2. DbgDebugData

**容器属性**:

- **UUID**: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to staticMemory used for Debug Data.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgDebugDataRef

- **UUID**: `ECUC:8dfda3f1-4048-42bd-b6b4-52263cf45d62`
- **引用名**: `DbgDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to staticMemory used for Debug Data.

####### 3. DbgLocalDebugData

**容器属性**:

- **UUID**: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgLocalDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to a localDebugData.

######## 引用关系

此容器包含 **1** 个引用：

######### FOREIGN-REFERENCE 类型引用

########## 1. DbgLocalDebugDataRef

- **UUID**: `ECUC:9be85ef2-5b62-4543-8feb-bc8c62192cc1`
- **引用名**: `DbgLocalDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a localDebugData.

####### 4. DbgStaticDIDData

**容器属性**:

- **UUID**: `ECUC:d8ec1f61-b0c2-49bc-a6f3-a7eff6d5fd01`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgStaticDIDData`
- **多重性**: [1..65535]

**容器选择**:

- **DbgAddressSizePair**
  - UUID: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
  - 描述: This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.
- **DbgDebugData**
  - UUID: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
  - 描述: Reference to staticMemory used for Debug Data.
- **DbgLocalDebugData**
  - UUID: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
  - 描述: Reference to a localDebugData.

**容器描述**:

Choice how the DID is to be configured.

##### 13. DbgAddressSizePair

**容器属性**:

- **UUID**: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgAddressSizePair`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DbgASAbsoluteAddress

- **UUID**: `ECUC:f26ad0a2-2136-42e9-b018-a84e99287fac`
- **参数名**: `DbgASAbsoluteAddress`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute address of memory location to be debugged.

######## 2. DbgASSize

- **UUID**: `ECUC:4b26a816-11ca-43c5-829d-03684d1605a1`
- **参数名**: `DbgASSize`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Absolute size in Bytes of memory location to be debugged.

####### LINKER-SYMBOL 类型参数

######## 1. DbgASNameRef

- **UUID**: `ECUC:faf3a6cd-406e-4496-81b3-1af954633d1a`
- **参数名**: `DbgASNameRef`
- **数据类型**: LINKER-SYMBOL
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Symbolic name of the variable, translated by the configuration/generation tool into the address and size of the variable.

##### 14. DbgDebugData

**容器属性**:

- **UUID**: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to staticMemory used for Debug Data.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgDebugDataRef

- **UUID**: `ECUC:8dfda3f1-4048-42bd-b6b4-52263cf45d62`
- **引用名**: `DbgDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: VARIABLE-DATA-PROTOTYPE
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to staticMemory used for Debug Data.

##### 15. DbgLocalDebugData

**容器属性**:

- **UUID**: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgLocalDebugData`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Reference to a localDebugData.

###### 引用关系

此容器包含 **1** 个引用：

####### FOREIGN-REFERENCE 类型引用

######## 1. DbgLocalDebugDataRef

- **UUID**: `ECUC:9be85ef2-5b62-4543-8feb-bc8c62192cc1`
- **引用名**: `DbgLocalDebugDataRef`
- **引用类型**: FOREIGN-REFERENCE
- **多重性**: [1..1]
- **目标类型**: IMPLEMENTATION-DATA-TYPE-ELEMENT
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a localDebugData.

##### 16. DbgPeriodicDataCollection

**容器属性**:

- **UUID**: `ECUC:51c936fe-9b42-40c3-9d46-be86d581101b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgPeriodicDataCollection`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the parameters to manage the time base of the debugging module.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DbgDataCollectionTick

- **UUID**: `ECUC:4530c00b-8809-4a39-8353-c1426453bc0e`
- **参数名**: `DbgDataCollectionTick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of OS counter ticks to be used as data collection tick. The OS alarm used for periodic collection of DIDs is set with this value.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DbgAlarmReference

- **UUID**: `ECUC:4a84a3c6-c964-4e11-a62a-3976538694b2`
- **引用名**: `DbgAlarmReference`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `OsAlarm`
- **完整路径**: `/AUTOSAR/EcucDefs/Os/OsAlarm`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the OS alarm used for periodic collection of DIDs.

##### 17. DbgTimestampConfiguration

**容器属性**:

- **UUID**: `ECUC:a2003b89-33e4-4fba-8c20-e3b82aca9ca5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DbgTimestampConfiguration`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container holds the parameters to manage the time stamps of the debugging module.

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. DbgGlobalTimestampActivation

- **UUID**: `ECUC:eb1f2eaa-27a4-4655-9abd-48d3dfebd3de`
- **参数名**: `DbgGlobalTimestampActivation`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TimestampOff`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TimestampOff` (来源: AUTOSAR_ECUC)
  - `TimestampOn` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Initial value for timestamp collection.

######## 2. DbgTimeStampSize

- **UUID**: `ECUC:746409f8-40d5-45d5-bbf1-cf8273d480d8`
- **参数名**: `DbgTimeStampSize`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `TimeStampSize_16Bit`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `TimeStampSize_16Bit` (来源: AUTOSAR_ECUC)
  - `TimeStampSize_32Bit` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Memory size used for the time stamps of all DIDs.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DbgGptChannel

- **UUID**: `ECUC:de1e3f61-12db-4fb7-9015-2eac7100dad1`
- **引用名**: `DbgGptChannel`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `GptChannelConfiguration`
- **完整路径**: `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the hardware free running timer of the GPT module for time stamps (if no HWFRT is applied, calls to add timestamps are ignored)

##### 18. DbgPredefinedDIDAddInfo

**容器属性**:

- **UUID**: `ECUC:c4665b22-b9f7-4cfa-8af1-eb27f71154b9`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgPredefinedDIDAddInfo`
- **多重性**: [0..infinite]

**容器选择**:

- **DbgAddInfoComSignal**
  - UUID: `ECUC:0b5c3c1d-fd04-4e37-9b59-a21d022aa727`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRteCall**
  - UUID: `ECUC:71e646dd-d959-4773-b5af-aade83e1148d`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoRunnable**
  - UUID: `ECUC:936a0eda-0a72-4610-aae4-24e51fc44601`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:
- **DbgAddInfoVfbSignal**
  - UUID: `ECUC:9f28567f-a1b8-4f47-945f-4295c4699cb2`
  - 描述: Additional information for DIDs with the DbgPredefinedDIDName set to:

**容器描述**:

Additional information in case the Predefined DID needs further configuration parameters.

##### 19. DbgStaticDIDData

**容器属性**:

- **UUID**: `ECUC:d8ec1f61-b0c2-49bc-a6f3-a7eff6d5fd01`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DbgStaticDIDData`
- **多重性**: [1..65535]

**容器选择**:

- **DbgAddressSizePair**
  - UUID: `ECUC:b1218263-1ce5-4348-8cb0-799296d51c19`
  - 描述: This container describes address/size pairs. It is used for static DIDs and dynamic DIDs.
- **DbgDebugData**
  - UUID: `ECUC:22457d3c-51b6-49aa-a324-0832b797dc6a`
  - 描述: Reference to staticMemory used for Debug Data.
- **DbgLocalDebugData**
  - UUID: `ECUC:3558b31b-7110-47cc-975d-74f20df27299`
  - 描述: Reference to a localDebugData.

**容器描述**:

Choice how the DID is to be configured.

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

1. **Dbg**
