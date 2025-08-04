# SomeIpTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:32

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [SomeIpTp](#someiptp)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_00048.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. SomeIpTp

#### 基本信息

- **UUID**: `ECUC:8508a798-1bdd-4654-9cac-cddeacb82ac3`
- **模块名称**: `SomeIpTp`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the SomeIpTp module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.5.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. SomeIpTpChannel

**容器属性**:

- **UUID**: `ECUC:10374864-f1f6-42a0-918c-1b442218a48f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpChannel`
- **多重性**: [1..infinite]

**容器描述**:

This container contains the configuration parameters of the SomeIpTp channel.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. SomeIpTpNPduSeparationTime

- **UUID**: `ECUC:ff78bd74-c4bc-4934-ac42-87f474aab487`
- **参数名**: `SomeIpTpNPduSeparationTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Sets the duration of the minimum time in seconds the SomeIpTp module shall wait between the transmissions of N-PDUs.

######## 2. SomeIpTpRxTimeoutTime

- **UUID**: `ECUC:87cecebc-07bc-49cd-8c6a-0eb649372b64`
- **参数名**: `SomeIpTpRxTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Timer to monitor the successful reception. It is started when the first NPdu is received, restarted after reception of intermediate NPdus, and is stopped when the last NPdu has been received. The value shall be calculated as follows: (SomeIpTpRxTimeoutTime = SomeIpTpNPduSeparationTime + budget), where the time budget compensates intermediary hops and jitters within the ECU implementation.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SomeIpTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:fb4de518-e66c-4194-9b85-8e3a6aa604d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNSdu`
- **多重性**: [0..infinite]

**容器描述**:

The following parameters needs to be configured for each N-SDU which has to be passed as one assembled RxPdu to the upper layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxSduRef

- **UUID**: `ECUC:7c683ac3-e363-4883-8a16-d11fd5e90756`
- **引用名**: `SomeIpTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Pdu in the COM-Stack that represents the assembled RxPdu which is passed via the PduR to the upper layer.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:99c5618e-07a1-4d61-94cd-2d666afc5e2b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SomeIpTpRxNPduHandleId

- **UUID**: `ECUC:3dd44cec-08af-4b6d-aae6-b04f2d563362`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SomeIpTpRxNPduRef

- **UUID**: `ECUC:bdbacebf-1ae7-46f2-a099-3b840c4305c0`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 2. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:99c5618e-07a1-4d61-94cd-2d666afc5e2b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpRxNPduHandleId

- **UUID**: `ECUC:3dd44cec-08af-4b6d-aae6-b04f2d563362`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxNPduRef

- **UUID**: `ECUC:bdbacebf-1ae7-46f2-a099-3b840c4305c0`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 3. SomeIpTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:68257886-3a18-4d42-af60-ed1452c9e9ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNSdu`
- **多重性**: [0..infinite]

**容器描述**:

The following parameters needs to be configured for each N-SDU that the SomeIpTp module transmits via the SomeIpTpChannel.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNSduHandleId

- **UUID**: `ECUC:d4bc82ab-fced-4af2-9524-33f3d34028ee`
- **参数名**: `SomeIpTpTxNSduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID of the NSdu that represents the original TxSdu which is segmented and passed via the PduR to the lower layer. This handle ID is used by PduR when calling SomeIpTp_Transmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNSduRef

- **UUID**: `ECUC:55449f11-e892-45d9-9534-8bd994baf8a9`
- **引用名**: `SomeIpTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu in the COM-Stack that represents the original TxSdu which is segmented and passed via the PduR to the lower layer.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:0f9acd13-d809-4e33-82e2-919ad0dc24d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SomeIpTpTxNPduHandleId

- **UUID**: `ECUC:b9d4c16d-bb26-494c-be50-f304d7078c48`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SomeIpTpTxNPduRef

- **UUID**: `ECUC:58b38392-11f7-4a74-8bf7-0a2ffae77f64`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 4. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:0f9acd13-d809-4e33-82e2-919ad0dc24d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNPduHandleId

- **UUID**: `ECUC:b9d4c16d-bb26-494c-be50-f304d7078c48`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNPduRef

- **UUID**: `ECUC:58b38392-11f7-4a74-8bf7-0a2ffae77f64`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 2. SomeIpTpRxNSdu

**容器属性**:

- **UUID**: `ECUC:fb4de518-e66c-4194-9b85-8e3a6aa604d0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNSdu`
- **多重性**: [0..infinite]

**容器描述**:

The following parameters needs to be configured for each N-SDU which has to be passed as one assembled RxPdu to the upper layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpRxSduRef

- **UUID**: `ECUC:7c683ac3-e363-4883-8a16-d11fd5e90756`
- **引用名**: `SomeIpTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a Pdu in the COM-Stack that represents the assembled RxPdu which is passed via the PduR to the upper layer.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:99c5618e-07a1-4d61-94cd-2d666afc5e2b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpRxNPduHandleId

- **UUID**: `ECUC:3dd44cec-08af-4b6d-aae6-b04f2d563362`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxNPduRef

- **UUID**: `ECUC:bdbacebf-1ae7-46f2-a099-3b840c4305c0`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 3. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `ECUC:99c5618e-07a1-4d61-94cd-2d666afc5e2b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpRxNPduHandleId

- **UUID**: `ECUC:3dd44cec-08af-4b6d-aae6-b04f2d563362`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpRxNPduRef

- **UUID**: `ECUC:bdbacebf-1ae7-46f2-a099-3b840c4305c0`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 4. SomeIpTpTxNSdu

**容器属性**:

- **UUID**: `ECUC:68257886-3a18-4d42-af60-ed1452c9e9ba`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNSdu`
- **多重性**: [0..infinite]

**容器描述**:

The following parameters needs to be configured for each N-SDU that the SomeIpTp module transmits via the SomeIpTpChannel.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpTxNSduHandleId

- **UUID**: `ECUC:d4bc82ab-fced-4af2-9524-33f3d34028ee`
- **参数名**: `SomeIpTpTxNSduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID of the NSdu that represents the original TxSdu which is segmented and passed via the PduR to the lower layer. This handle ID is used by PduR when calling SomeIpTp_Transmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpTxNSduRef

- **UUID**: `ECUC:55449f11-e892-45d9-9534-8bd994baf8a9`
- **引用名**: `SomeIpTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu in the COM-Stack that represents the original TxSdu which is segmented and passed via the PduR to the lower layer.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:0f9acd13-d809-4e33-82e2-919ad0dc24d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNPduHandleId

- **UUID**: `ECUC:b9d4c16d-bb26-494c-be50-f304d7078c48`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNPduRef

- **UUID**: `ECUC:58b38392-11f7-4a74-8bf7-0a2ffae77f64`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 5. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `ECUC:0f9acd13-d809-4e33-82e2-919ad0dc24d6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpTxNPduHandleId

- **UUID**: `ECUC:b9d4c16d-bb26-494c-be50-f304d7078c48`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpTxNPduRef

- **UUID**: `ECUC:58b38392-11f7-4a74-8bf7-0a2ffae77f64`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucConfigSet/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 6. SomeIpTpGeneral

**容器属性**:

- **UUID**: `ECUC:3e5d4236-84ee-441e-aee0-9969d97a67b2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpGeneral`
- **多重性**: [1..1]

**容器描述**:

This container contains the general configuration parameters of the SomeIpTp module.

###### 参数配置

此容器包含 **4** 个参数：

####### BOOLEAN 类型参数

######## 1. SomeIpTpDevErrorDetect

- **UUID**: `ECUC:79fe50f4-33c0-4faf-abd9-29eae413c097`
- **参数名**: `SomeIpTpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. SomeIpTpVersionInfoApi

- **UUID**: `ECUC:92e05511-a685-4847-9e89-f050b4595ca5`
- **参数名**: `SomeIpTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Activates the SomeIpTp_GetVersionInfo() API.

####### FLOAT 类型参数

######## 1. SomeIpTpRxMainFunctionPeriod

- **UUID**: `ECUC:234859cf-2d56-4497-8d76-c3a7e08c8ec3`
- **参数名**: `SomeIpTpRxMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the cycle time in seconds of the periodic call of the SomeIpTp_MainFunctionRx.

######## 2. SomeIpTpTxMainFunctionPeriod

- **UUID**: `ECUC:025b9b3f-b02d-408f-8a89-d5b75fbeff8d`
- **参数名**: `SomeIpTpTxMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..INF]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter defines the cycle time in seconds of the periodic call of the SomeIpTp_MainFunctionTx.

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

1. **SomeIpTp**
