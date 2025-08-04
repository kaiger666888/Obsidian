# SomeIpTp - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:45:57

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [SomeIpTp](#someiptp)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-3-0.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. SomeIpTp

#### 基本信息

- **UUID**: `2a1aa01e-a087-499e-a6f3-f5eb34fde39b`
- **模块名称**: `SomeIpTp`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

SOME/IP Transport Protocol. SOME/IP TP module segments SOME/IP packets, which do not fit into one single UDP packet. On the reception side, it assembles the received SOME/IP segments.

#TP #Ethernet #SOMEIP
#AUTOSAR

#### 版本历史

共有 **9** 个版本记录：

##### 1. 版本 1.0.0

- **发布者**: AUTOSAR

*此版本无详细变更记录*

##### 2. 版本 1.1.0

- **发布日期**: 2018-01-19T10:46:04+01:00
- **发布者**: vissuk

**变更内容**:

##### 3. 版本 1.1.1

- **发布日期**: 2018-02-16T13:28:07+01:00
- **发布者**: visath

**变更内容**:

##### 4. 版本 1.1.2

- **发布日期**: 2018-09-24T12:49:09+02:00
- **发布者**: vissuk

**变更内容**:

##### 5. 版本 1.1.2

- **发布日期**: 2018-09-26T12:50:10+02:00
- **发布者**: visath

**变更内容**:

##### 6. 版本 2.0.0

- **发布日期**: 2020-03-04T16:03:12+01:00
- **发布者**: vissuk

**变更内容**:

##### 7. 版本 3.0.0

- **发布日期**: 2020-09-09T10:18:46+02:00
- **发布者**: vissuk

**变更内容**:

##### 8. 版本 4.0.1

- **发布日期**: 2020-11-25T10:58:34+01:00
- **发布者**: visath

**变更内容**:

##### 9. 版本 5.0.0

- **发布日期**: 2021-11-02T10:15:58+01:00
- **发布者**: vissuk

**变更内容**:

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. SomeIpTpChannel

**容器属性**:

- **UUID**: `5122ea80-4544-444c-b257-552f508c2dd2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpChannel`
- **多重性**: [1..infinite]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the SomeIpTp channel.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. SomeIpTpNPduSeparationTime

- **UUID**: `19ba0354-a0a0-46c3-84ff-b8047e8061f8`
- **参数名**: `SomeIpTpNPduSeparationTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.001`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Sets the duration of the minimum time in seconds the SomeIpTp module shall wait between the transmissions of N-PDUs.

######## 2. SomeIpTpRxTimeoutTime

- **UUID**: `d78d4ec0-f952-43e5-8976-7efebff5c2b1`
- **参数名**: `SomeIpTpRxTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Timer to monitor the successful reception. It is started when the first NPdu
is received, restarted after reception of intermediate NPdus, and is stopped when the last NPdu has been received.

######## 3. SomeIpTpTxConfTimeoutTime

- **UUID**: `e1ce68a7-6289-4ebe-a46f-a86fb845ce73`
- **参数名**: `SomeIpTpTxConfTimeoutTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.5`
- **取值范围**: [0..65.535]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Timer to monitor the successful Transmission Confirmation. It is started when the NPdu is triggered and is stopped when the Confirmation has been received.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. SomeIpTpRxNSdu

**容器属性**:

- **UUID**: `f1c7caab-8f29-49df-b206-27162fa231d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNSdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The following parameters needs to be configured for each N-SDU which has to be passed as one assembled RxPdu to the upper layer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxSduRef

- **UUID**: `4d96cf63-35a5-4d1e-9a26-b0aa930c9af3`
- **引用名**: `SomeIpTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a Pdu in the COM-Stack that represents the assembled RxPdu which is passed via the PduR to the upper layer.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `65ecbcf0-244a-4e14-bcf2-34d00966b846`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SomeIpTpRxNPduHandleId

- **UUID**: `83ff3ffb-b840-4a4f-8b15-c3590226eff2`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SomeIpTpRxNPduRef

- **UUID**: `01e4ff6f-ae20-4142-acfc-81b2a92162b1`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 2. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `65ecbcf0-244a-4e14-bcf2-34d00966b846`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpRxNPduHandleId

- **UUID**: `83ff3ffb-b840-4a4f-8b15-c3590226eff2`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxNPduRef

- **UUID**: `01e4ff6f-ae20-4142-acfc-81b2a92162b1`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 3. SomeIpTpTxNSdu

**容器属性**:

- **UUID**: `68f189b3-61db-41c6-adfd-5c697aa3a6cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNSdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The following parameters needs to be configured for each N-SDU that the SomeIpTp module transmits via the SomeIpTpChannel.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNSduHandleId

- **UUID**: `e97aac55-a600-414b-9967-f3844c2347d0`
- **参数名**: `SomeIpTpTxNSduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID of the NSdu that represents the original TxSdu which is segmented and passed via the PduR to the lower layer. This handle ID is used by PduR when calling SomeIpTp_Transmit.

########## 2. SomeIpTpTxBurstSize

- **UUID**: `e2365eb8-a6dd-41ed-9b02-ae1113810a5b`
- **参数名**: `SomeIpTpTxBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Number of SomeIpTp segments transmitted consecutively in the SomeIpTp mainfunction without waiting for separation time.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNSduRef

- **UUID**: `fca22875-05a8-4e2a-aa49-e93317bf028e`
- **引用名**: `SomeIpTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu in the COM-Stack that represents the original TxSdu which is segmented and passed via the PduR to the lower layer.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `2f254c47-6ac8-4d75-96ad-a0d32e40f392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. SomeIpTpTxNPduHandleId

- **UUID**: `b7bf3441-2417-4799-84d7-565edd283f21`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. SomeIpTpTxNPduRef

- **UUID**: `17640361-f9f2-420a-a927-e9229b5c0386`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

####### 4. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `2f254c47-6ac8-4d75-96ad-a0d32e40f392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNPduHandleId

- **UUID**: `b7bf3441-2417-4799-84d7-565edd283f21`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNPduRef

- **UUID**: `17640361-f9f2-420a-a927-e9229b5c0386`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 2. SomeIpTpRxNSdu

**容器属性**:

- **UUID**: `f1c7caab-8f29-49df-b206-27162fa231d8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNSdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The following parameters needs to be configured for each N-SDU which has to be passed as one assembled RxPdu to the upper layer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpRxSduRef

- **UUID**: `4d96cf63-35a5-4d1e-9a26-b0aa930c9af3`
- **引用名**: `SomeIpTpRxSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a Pdu in the COM-Stack that represents the assembled RxPdu which is passed via the PduR to the upper layer.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `65ecbcf0-244a-4e14-bcf2-34d00966b846`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpRxNPduHandleId

- **UUID**: `83ff3ffb-b840-4a4f-8b15-c3590226eff2`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpRxNPduRef

- **UUID**: `01e4ff6f-ae20-4142-acfc-81b2a92162b1`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 3. SomeIpTpRxNPdu

**容器属性**:

- **UUID**: `65ecbcf0-244a-4e14-bcf2-34d00966b846`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpRxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the NPdu that is received from a lower layer

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpRxNPduHandleId

- **UUID**: `83ff3ffb-b840-4a4f-8b15-c3590226eff2`
- **参数名**: `SomeIpTpRxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by the PduR when calling SomeIpTp_RxIndication.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpRxNPduRef

- **UUID**: `01e4ff6f-ae20-4142-acfc-81b2a92162b1`
- **引用名**: `SomeIpTpRxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 4. SomeIpTpTxNSdu

**容器属性**:

- **UUID**: `68f189b3-61db-41c6-adfd-5c697aa3a6cc`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNSdu`
- **多重性**: [0..infinite]
- **需要索引**: false

**容器描述**:

The following parameters needs to be configured for each N-SDU that the SomeIpTp module transmits via the SomeIpTpChannel.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpTxNSduHandleId

- **UUID**: `e97aac55-a600-414b-9967-f3844c2347d0`
- **参数名**: `SomeIpTpTxNSduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID of the NSdu that represents the original TxSdu which is segmented and passed via the PduR to the lower layer. This handle ID is used by PduR when calling SomeIpTp_Transmit.

######## 2. SomeIpTpTxBurstSize

- **UUID**: `e2365eb8-a6dd-41ed-9b02-ae1113810a5b`
- **参数名**: `SomeIpTpTxBurstSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Number of SomeIpTp segments transmitted consecutively in the SomeIpTp mainfunction without waiting for separation time.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpTxNSduRef

- **UUID**: `fca22875-05a8-4e2a-aa49-e93317bf028e`
- **引用名**: `SomeIpTpTxNSduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu in the COM-Stack that represents the original TxSdu which is segmented and passed via the PduR to the lower layer.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `2f254c47-6ac8-4d75-96ad-a0d32e40f392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. SomeIpTpTxNPduHandleId

- **UUID**: `b7bf3441-2417-4799-84d7-565edd283f21`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. SomeIpTpTxNPduRef

- **UUID**: `17640361-f9f2-420a-a927-e9229b5c0386`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 5. SomeIpTpTxNPdu

**容器属性**:

- **UUID**: `2f254c47-6ac8-4d75-96ad-a0d32e40f392`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpTxNPdu`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the configuration parameters of the segmented Tx NPdus that are transmitted to a lower layer.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. SomeIpTpTxNPduHandleId

- **UUID**: `b7bf3441-2417-4799-84d7-565edd283f21`
- **参数名**: `SomeIpTpTxNPduHandleId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **描述**: This parameter defines the handle ID that is used by PduR when calling SomeIpTp_TriggerTransmit.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. SomeIpTpTxNPduRef

- **UUID**: `17640361-f9f2-420a-a927-e9229b5c0386`
- **引用名**: `SomeIpTpTxNPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **描述**: Reference to a global Pdu that is used to harmonize HandleIDs in the COM-Stack.

##### 6. SomeIpTpGeneral

**容器属性**:

- **UUID**: `69ea9f82-5370-41aa-b68d-e4676d8131b5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `SomeIpTpGeneral`
- **多重性**: [1..1]
- **需要索引**: false

**容器描述**:

This container contains the general configuration parameters of the SomeIpTp module.

###### 参数配置

此容器包含 **7** 个参数：

####### BOOLEAN 类型参数

######## 1. SomeIpTpDevErrorDetect

- **UUID**: `5bc7d379-fe50-4290-a732-625c6846f939`
- **参数名**: `SomeIpTpDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 2. SomeIpTpVersionInfoApi

- **UUID**: `7945609a-7c85-4b4f-8c7c-06dc6c6299c8`
- **参数名**: `SomeIpTpVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: Activates the SomeIpTp_GetVersionInfo() API.

######## 3. SomeIpTpRuntimeErrorReport

- **UUID**: `68eacd33-ad73-4c95-a249-567f4ac3baf0`
- **参数名**: `SomeIpTpRuntimeErrorReport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Switches the Runtime Error Notification ON or OFF.

######## 4. SomeIpTpSafeBswChecks

- **UUID**: `2754de1b-bb4e-48aa-911d-14f268f7964c`
- **参数名**: `SomeIpTpSafeBswChecks`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Selects if safety checks are used. These checks improve robustness as e.g. invalid parameters are checked before function is executed. This attribute has to be enabled for safety projects where this component is mapped to an ASIL partition.

####### FLOAT 类型参数

######## 1. SomeIpTpRxMainFunctionPeriod

- **UUID**: `30425de9-3d10-4af0-a702-1de07ddcefeb`
- **参数名**: `SomeIpTpRxMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.001`
- **取值范围**: [0..1.7976931348623157E+308]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the cycle time in seconds of the periodic call of the SomeIpTp_MainFunctionRx.

######## 2. SomeIpTpTxMainFunctionPeriod

- **UUID**: `bba29731-fcaf-42a7-af94-e12024fbfc32`
- **参数名**: `SomeIpTpTxMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.001`
- **取值范围**: [0..1.7976931348623157E+308]
- **作用域**: LOCAL
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **描述**: This parameter defines the cycle time in seconds of the periodic call of the SomeIpTp_MainFunctionTx.

####### STRING 类型参数

######## 1. SomeIpTpUserConfigFile

- **UUID**: `0ec053fd-2c98-472e-a611-4a150f3b8bcb`
- **参数名**: `SomeIpTpUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **作用域**: LOCAL
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **描述**: Reference to an external text file that will be included during generation to SomeIpTp_Cfg.h.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSAR

- **UUID**: `ff55d029-386d-43a2-b3c2-dfef4c7a5e36`
- **包名称**: `MICROSAR`
- **包含元素数量**: 4

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **SomeIpTp**

##### BSW-IMPLEMENTATION 类型元素

1. **SomeIpTp_Impl**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **SomeIpTp_Pre**
2. **SomeIpTp_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. SomeIpTp_Impl

- **UUID**: `96c1d100-db3b-4d49-bddb-be13c0335c68`
- **实现名称**: `SomeIpTp_Impl`
- **编程语言**: C
- **软件版本**: 5.00.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.03.01
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. SomeIpTp_Pre

- **UUID**: `5f661863-677e-4a1f-9790-a5d7b2888bfd`
- **配置名称**: `SomeIpTp_Pre`
- **定义引用**: `/MICROSAR/SomeIpTp`

### 2. SomeIpTp_Rec

- **UUID**: `da948649-8415-4dab-a02b-b275848c84b2`
- **配置名称**: `SomeIpTp_Rec`
- **定义引用**: `/MICROSAR/SomeIpTp`
