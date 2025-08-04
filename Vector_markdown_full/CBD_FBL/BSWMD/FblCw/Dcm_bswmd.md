# Dcm - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:48:08

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Dcm](#dcm)
- [📦 包结构](#-包结构)
- [⚡ 实现信息](#-实现信息)
- [⚙️ 配置信息](#️-配置信息)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Dcm

#### 基本信息

- **UUID**: `aa02627c-6ffa-45d1-b4c4-61a587dff2f5`
- **模块名称**: `Dcm`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE
  - VARIANT-POST-BUILD-LOADABLE
  - VARIANT-POST-BUILD-SELECTABLE

#### 模块描述

Configuration of the Dcm (Diagnostic Communications Manager) module.

#### 版本历史

共有 **2** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2017-07-18
- **发布者**: visms vismvi

**变更内容**:

##### 2. 版本 1.01.00

- **发布日期**: 2017-07-18
- **发布者**: visms

**变更内容**:

#### 配置容器

本模块包含 **17** 个配置容器：

##### 1. DcmConfigSet

**容器属性**:

- **UUID**: `70912165-81e3-4034-b36a-c039e8651886`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmConfigSet`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration parameters and sub containers of the Dcm module supporting multiple configuration sets.

###### 配置容器

本模块包含 **16** 个配置容器：

####### 1. DcmDsl

**容器属性**:

- **UUID**: `0c37b574-5200-4e95-a460-8ab79ce23d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDsl`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These parameters apply to a Diagnostic Session Layer. There may be a parameter set (DSL Configuration) per protocol.

######## 配置容器

本模块包含 **10** 个配置容器：

######### 1. DcmDslBuffer

**容器属性**:

- **UUID**: `8104c964-4ec8-4548-82d8-c287320615b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBuffer`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the diagnostic buffer.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBufferSize

- **UUID**: `341ebcd8-9933-47aa-8e89-654e7f334603`
- **参数名**: `DcmDslBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `50`
- **取值范围**: [8..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the size of a diagnostic buffer (in Bytes).

Effect:
------------------------------------
Determines the longest request and in some cases - response the Dcm will be able to receive, resp. transmit.

Constraints:
------------------------------------
It depends on the communication bus system how much buffer shall be reserved. For example on CAN a buffer of more than 4095 will not bring any advantage since the CanTp can transfer only up to 4095 bytes.

Dependencies:
------------------------------------
In case of Paged Buffer usage (refer to DcmPageBufferCfg), the buffer size shall be chosen such that at least the longest snapshot record/extended data record of the Dem plus some additional bytes (i.e. in case of CAN -> 6 additional bytes) will fit it.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The greater the buffer the more RAM will be required.

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslDiagResp

**容器属性**:

- **UUID**: `681203d2-5f46-42e9-be66-f653e1641960`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslDiagResp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the ResponsePending handling

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslDiagRespMaxNumOfDeclinedRequests

- **UUID**: `b8a4cc8e-379a-4c11-8525-8c824318acb7`
- **参数名**: `DcmDslDiagRespMaxNumOfDeclinedRequests`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the maximum number of reactions upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
The Dcm will calculate the required amount of resources upon the specified by this option resource for parallel client processing.

Constraints:
------------------------------------
If the amount of configured requests exceeds the total number of Dcm connections, during the code generation the resource usage optimization will be disabled and only as many as available diagnostic connection objects will be allocated. This will also shorten the run time usage (see below).

Dependencies:
------------------------------------
Has any effect only if DcmDslDiagRespOnSecondDeclinedRequest is enabled.

Runtime effects:
------------------------------------
The more clients to be handled the longer the run time for looking up for free resources. If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the run time will be minimal.

Code ROM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the code ROM will be minimal.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The more clients to be handled the more RAM will be required for handling them.

Stack RAM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the stack usage will be minimal.

########### BOOLEAN 类型参数

############ 1. DcmDslDiagRespOnSecondDeclinedRequest

- **UUID**: `86bd212d-f489-4881-a9ac-230cd0222f33`
- **参数名**: `DcmDslDiagRespOnSecondDeclinedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
If enabled, the Dcm will reject any nested diagnostic request by NRC 0x21 (BusyRepeatRequest).

Constraints:
------------------------------------
For optimization reasons not all Dcm managed connection will support this feature by default. It is configurable how many parallel (nested) request to be handled at a time to save RAM and run time resources.

Dependencies:
------------------------------------
Refer to DcmDslDiagRespMaxNumOfDeclinedRequests.

Runtime effects:
------------------------------------
If enabled the Dcm diagnostic request reception functionality will have slightly increased run time usage.

Code ROM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased RAM usage.

Stack RAM usage effects:
------------------------------------
If enabled the Dcm will have insignificantly increased stack usage within the Rx ISRs.

######### 3. DcmDslProtocol

**容器属性**:

- **UUID**: `566ab607-9811-4e9a-9e18-761c606d4d87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocol`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the protocol configuration (for each protocol) The following parameters needs to be configured per protocol.

########## 配置容器

本模块包含 **7** 个配置容器：

########### 1. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 配置容器

本模块包含 **6** 个配置容器：

############# 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

############## 配置容器

本模块包含 **2** 个配置容器：

############### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################ 参数配置

此容器包含 **2** 个参数：

################# INTEGER 类型参数

################## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################# ENUMERATION 类型参数

################## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################ 引用关系

此容器包含 **2** 个引用：

################# REFERENCE 类型引用

################## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################# SYMBOLIC-NAME-REFERENCE 类型引用

################## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################ 参数配置

此容器包含 **1** 个参数：

################# INTEGER 类型参数

################## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

################ 引用关系

此容器包含 **1** 个引用：

################# REFERENCE 类型引用

################## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### ENUMERATION 类型参数

################ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

############# 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

################ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

############# 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

########### 2. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### ENUMERATION 类型参数

################ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 3. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 4. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 5. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 6. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 7. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

######### 4. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 配置容器

本模块包含 **6** 个配置容器：

########### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### ENUMERATION 类型参数

################ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

######### 5. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 6. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 7. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 8. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 9. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 10. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 2. DcmDslBuffer

**容器属性**:

- **UUID**: `8104c964-4ec8-4548-82d8-c287320615b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBuffer`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the diagnostic buffer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBufferSize

- **UUID**: `341ebcd8-9933-47aa-8e89-654e7f334603`
- **参数名**: `DcmDslBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `50`
- **取值范围**: [8..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the size of a diagnostic buffer (in Bytes).

Effect:
------------------------------------
Determines the longest request and in some cases - response the Dcm will be able to receive, resp. transmit.

Constraints:
------------------------------------
It depends on the communication bus system how much buffer shall be reserved. For example on CAN a buffer of more than 4095 will not bring any advantage since the CanTp can transfer only up to 4095 bytes.

Dependencies:
------------------------------------
In case of Paged Buffer usage (refer to DcmPageBufferCfg), the buffer size shall be chosen such that at least the longest snapshot record/extended data record of the Dem plus some additional bytes (i.e. in case of CAN -> 6 additional bytes) will fit it.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The greater the buffer the more RAM will be required.

Stack RAM usage effects:
------------------------------------
none

####### 3. DcmDslDiagResp

**容器属性**:

- **UUID**: `681203d2-5f46-42e9-be66-f653e1641960`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslDiagResp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the ResponsePending handling

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslDiagRespMaxNumOfDeclinedRequests

- **UUID**: `b8a4cc8e-379a-4c11-8525-8c824318acb7`
- **参数名**: `DcmDslDiagRespMaxNumOfDeclinedRequests`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the maximum number of reactions upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
The Dcm will calculate the required amount of resources upon the specified by this option resource for parallel client processing.

Constraints:
------------------------------------
If the amount of configured requests exceeds the total number of Dcm connections, during the code generation the resource usage optimization will be disabled and only as many as available diagnostic connection objects will be allocated. This will also shorten the run time usage (see below).

Dependencies:
------------------------------------
Has any effect only if DcmDslDiagRespOnSecondDeclinedRequest is enabled.

Runtime effects:
------------------------------------
The more clients to be handled the longer the run time for looking up for free resources. If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the run time will be minimal.

Code ROM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the code ROM will be minimal.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The more clients to be handled the more RAM will be required for handling them.

Stack RAM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the stack usage will be minimal.

######### BOOLEAN 类型参数

########## 1. DcmDslDiagRespOnSecondDeclinedRequest

- **UUID**: `86bd212d-f489-4881-a9ac-230cd0222f33`
- **参数名**: `DcmDslDiagRespOnSecondDeclinedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
If enabled, the Dcm will reject any nested diagnostic request by NRC 0x21 (BusyRepeatRequest).

Constraints:
------------------------------------
For optimization reasons not all Dcm managed connection will support this feature by default. It is configurable how many parallel (nested) request to be handled at a time to save RAM and run time resources.

Dependencies:
------------------------------------
Refer to DcmDslDiagRespMaxNumOfDeclinedRequests.

Runtime effects:
------------------------------------
If enabled the Dcm diagnostic request reception functionality will have slightly increased run time usage.

Code ROM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased RAM usage.

Stack RAM usage effects:
------------------------------------
If enabled the Dcm will have insignificantly increased stack usage within the Rx ISRs.

####### 4. DcmDslProtocol

**容器属性**:

- **UUID**: `566ab607-9811-4e9a-9e18-761c606d4d87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocol`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the protocol configuration (for each protocol) The following parameters needs to be configured per protocol.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 配置容器

本模块包含 **6** 个配置容器：

########### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### ENUMERATION 类型参数

################ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

######### 2. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 3. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 4. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 5. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 6. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 7. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 5. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 6. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 7. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 8. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 9. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 10. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

########## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 11. DcmDsp

**容器属性**:

- **UUID**: `d5467754-0556-48c7-9c8a-9d2c033866a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDsp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These parameters apply to Diagnostic Service Processing. There will always be one set of these parameters per DCM.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DcmDspSession

**容器属性**:

- **UUID**: `d32a2b80-994d-4157-927d-da1695c68655`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSession`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes all diagnostic sessions the Dcm shall support.

Effect:
------------------------------------
For each diagnostic session to be supported by Dcm a DcmDspSessionRow sub-container shall be defined.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of sessions defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# FLOAT 类型参数

############## 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### FLOAT 类型参数

############ 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 12. DcmDspSession

**容器属性**:

- **UUID**: `d32a2b80-994d-4157-927d-da1695c68655`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSession`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes all diagnostic sessions the Dcm shall support.

Effect:
------------------------------------
For each diagnostic session to be supported by Dcm a DcmDspSessionRow sub-container shall be defined.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of sessions defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### FLOAT 类型参数

############ 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 13. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### FLOAT 类型参数

########## 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 14. DcmGeneral

**容器属性**:

- **UUID**: `ca892183-66d6-4a91-bef4-34c98a2ee15a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for Component wide parameters

######## 参数配置

此容器包含 **11** 个参数：

######### INTEGER 类型参数

########## 1. DcmNwStatusRxBufferSize

- **UUID**: `b276419f-daab-4a5c-be70-95651af81c4f`
- **参数名**: `DcmNwStatusRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Buffer size for the network status reception buffer.

########## 2. DcmCanHardwareLoopTimeout

- **UUID**: `7767ddb0-0006-4465-82a4-6c8b1699c1dd`
- **参数名**: `DcmCanHardwareLoopTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Timeout value for CAN hardware loops (in cycles, typically 1 ms)

########## 3. DcmTaskCycle

- **UUID**: `51bb97da-a9ec-415f-b718-fdfe9a7e4eb0`
- **参数名**: `DcmTaskCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Cycle count of CanTp, FrSM, EthSM and ComM tasks. Other tasks are either called every timer cycle (Ethernet) or polled (CAN)

######### BOOLEAN 类型参数

########## 1. DcmQueuedRequest

- **UUID**: `087031f4-ff23-43eb-9593-667b54f9580a`
- **参数名**: `DcmQueuedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 2. DcmKeySlotMode

- **UUID**: `56729bdb-1932-4a86-9af6-6d5ef2f69122`
- **参数名**: `DcmKeySlotMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable switching from key slot to all slot mode.

########## 3. DcmBaudrateSwitch

- **UUID**: `9ebffaa5-cae0-40b6-9203-88900e2aabe3`
- **参数名**: `DcmBaudrateSwitch`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the APIs FblCwCheckBaudrate and FblCwSwitchBaudrate ON or OFF.
true: APIs are enabled.
false: APIs are disabled.

########## 4. DcmVersionInfoApi

- **UUID**: `98b138ad-3fe8-45bb-922a-1b79f18a099a`
- **参数名**: `DcmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Preprocessor switch to enable or disable the output Version info of the functionality.

########## 5. DcmDevErrorDetect

- **UUID**: `5c1785d4-21d8-4f87-b076-905ff53284ac`
- **参数名**: `DcmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

########## 6. DcmRespondAllRequest

- **UUID**: `5ef12de4-4f82-4ed9-8888-74411a19551d`
- **参数名**: `DcmRespondAllRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to FALSE the Dcm will not respond to diagnostic request  that contains a service ID which is in the range from 0x40 to 0x7F or in the  range from 0xC0 to 0xFF (Response IDs).

######### FLOAT 类型参数

########## 1. DcmTaskTime

- **UUID**: `7b09f5ff-359b-42e1-8167-f0e8559cf91d`
- **参数名**: `DcmTaskTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Allow to configure the time for the periodic cyclic task in seconds.

Effect:
-----------------------------------------
This value is used to set up the Dcm Service-Description and BSW scheduler. All diagnostic timers managed by Dcm use this setting as a base time for the internal time constants' calculation.

Constraints:
-----------------------------------------
The specified time shall be a multiple of the time values defined in all diagnostic timing settings in the Dcm configuration.

Dependencies:
-----------------------------------------
All diagnostic timing parameters.

Runtime effects:
-----------------------------------------
Too low values will increase the Dcm responsiveness, but will increase the CPU load. Too high values of this parameter will lead to rear Dcm task activation (lower CPU load), but the Dcm internal timers' accuracy will not be optimal.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
-----------------------------------------
none

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
none

######### STRING 类型参数

########## 1. DcmUserConfigFile

- **UUID**: `9ca97de0-16fe-4beb-b27d-52482ec00324`
- **参数名**: `DcmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Path to an external user configuration file used by the Configurator 5 generation tool.

Effect:
-----------------------------------------
If you want to overwrite some of the settings in the generated configuration file (Dcm_Cfg.h), you can specify a path to a user defined configuration file. The user defined configuration file will be included at the end of the generated preprocessor switches. Definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The path shall be a valid path to the user configuration file. For simplified and project specific user configuration files references, the following Configurator 5 environment variables can be used:

$(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
$(EcuProjectName) Name of the project defined in the loaded *.dpa file.
$(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
$(EcucFolder) Parent directory of $(EcucFile).
$(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
$(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting "Root Target Folder" of Configurator 5.
$(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.


Constraints:
-----------------------------------------
Not all of the settings can be overwritten simply by triggering the preprocessor switch. Some of the options are complex and the code generator generates less or more code depending on the setting.

USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.

Dependencies:
-----------------------------------------
none

Runtime effects:
-----------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
-----------------------------------------
none

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
none

####### 15. DcmGeneration

**容器属性**:

- **UUID**: `ba671fb2-6bd9-48e6-840c-839be96b46b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. DcmReduceNumericalDataByOffsetThreshold

- **UUID**: `47eeafcf-4fe1-4bb7-8dea-9e1be908afd8`
- **参数名**: `DcmReduceNumericalDataByOffsetThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a constant offset.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the constant offset operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the constant offset operation in the data access.

######### BOOLEAN 类型参数

########## 1. DcmReduceConstantData2Define

- **UUID**: `386752e4-bb7d-4da9-aa68-51a9a10d7463`
- **参数名**: `DcmReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

########## 2. DcmShortSymbols

- **UUID**: `ebcee410-b23c-420f-b66f-ab98f67f425e`
- **参数名**: `DcmShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

########## 3. DcmInterfacesForDeactivatedData

- **UUID**: `132320e3-4ee1-43fc-b68e-542ac9bf3a56`
- **参数名**: `DcmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

########## 4. DcmReferringKeysInComments

- **UUID**: `d2d99bed-162b-4950-8616-703ddc1f5684`
- **参数名**: `DcmReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

####### 16. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

##### 2. DcmDsl

**容器属性**:

- **UUID**: `0c37b574-5200-4e95-a460-8ab79ce23d3a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDsl`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These parameters apply to a Diagnostic Session Layer. There may be a parameter set (DSL Configuration) per protocol.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. DcmDslBuffer

**容器属性**:

- **UUID**: `8104c964-4ec8-4548-82d8-c287320615b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBuffer`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the diagnostic buffer.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBufferSize

- **UUID**: `341ebcd8-9933-47aa-8e89-654e7f334603`
- **参数名**: `DcmDslBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `50`
- **取值范围**: [8..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the size of a diagnostic buffer (in Bytes).

Effect:
------------------------------------
Determines the longest request and in some cases - response the Dcm will be able to receive, resp. transmit.

Constraints:
------------------------------------
It depends on the communication bus system how much buffer shall be reserved. For example on CAN a buffer of more than 4095 will not bring any advantage since the CanTp can transfer only up to 4095 bytes.

Dependencies:
------------------------------------
In case of Paged Buffer usage (refer to DcmPageBufferCfg), the buffer size shall be chosen such that at least the longest snapshot record/extended data record of the Dem plus some additional bytes (i.e. in case of CAN -> 6 additional bytes) will fit it.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The greater the buffer the more RAM will be required.

Stack RAM usage effects:
------------------------------------
none

####### 2. DcmDslDiagResp

**容器属性**:

- **UUID**: `681203d2-5f46-42e9-be66-f653e1641960`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslDiagResp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the ResponsePending handling

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslDiagRespMaxNumOfDeclinedRequests

- **UUID**: `b8a4cc8e-379a-4c11-8525-8c824318acb7`
- **参数名**: `DcmDslDiagRespMaxNumOfDeclinedRequests`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the maximum number of reactions upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
The Dcm will calculate the required amount of resources upon the specified by this option resource for parallel client processing.

Constraints:
------------------------------------
If the amount of configured requests exceeds the total number of Dcm connections, during the code generation the resource usage optimization will be disabled and only as many as available diagnostic connection objects will be allocated. This will also shorten the run time usage (see below).

Dependencies:
------------------------------------
Has any effect only if DcmDslDiagRespOnSecondDeclinedRequest is enabled.

Runtime effects:
------------------------------------
The more clients to be handled the longer the run time for looking up for free resources. If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the run time will be minimal.

Code ROM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the code ROM will be minimal.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The more clients to be handled the more RAM will be required for handling them.

Stack RAM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the stack usage will be minimal.

######### BOOLEAN 类型参数

########## 1. DcmDslDiagRespOnSecondDeclinedRequest

- **UUID**: `86bd212d-f489-4881-a9ac-230cd0222f33`
- **参数名**: `DcmDslDiagRespOnSecondDeclinedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
If enabled, the Dcm will reject any nested diagnostic request by NRC 0x21 (BusyRepeatRequest).

Constraints:
------------------------------------
For optimization reasons not all Dcm managed connection will support this feature by default. It is configurable how many parallel (nested) request to be handled at a time to save RAM and run time resources.

Dependencies:
------------------------------------
Refer to DcmDslDiagRespMaxNumOfDeclinedRequests.

Runtime effects:
------------------------------------
If enabled the Dcm diagnostic request reception functionality will have slightly increased run time usage.

Code ROM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased RAM usage.

Stack RAM usage effects:
------------------------------------
If enabled the Dcm will have insignificantly increased stack usage within the Rx ISRs.

####### 3. DcmDslProtocol

**容器属性**:

- **UUID**: `566ab607-9811-4e9a-9e18-761c606d4d87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocol`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the protocol configuration (for each protocol) The following parameters needs to be configured per protocol.

######## 配置容器

本模块包含 **7** 个配置容器：

######### 1. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 配置容器

本模块包含 **6** 个配置容器：

########### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

############ 配置容器

本模块包含 **2** 个配置容器：

############# 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### ENUMERATION 类型参数

################ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **2** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 参数配置

此容器包含 **1** 个参数：

############### INTEGER 类型参数

################ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

########### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

######### 2. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 3. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 4. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 5. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 6. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 7. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 4. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 5. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 6. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 7. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 8. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 9. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

########## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 10. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

##### 3. DcmDslBuffer

**容器属性**:

- **UUID**: `8104c964-4ec8-4548-82d8-c287320615b8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBuffer`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the diagnostic buffer.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslBufferSize

- **UUID**: `341ebcd8-9933-47aa-8e89-654e7f334603`
- **参数名**: `DcmDslBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `50`
- **取值范围**: [8..4294967294]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the size of a diagnostic buffer (in Bytes).

Effect:
------------------------------------
Determines the longest request and in some cases - response the Dcm will be able to receive, resp. transmit.

Constraints:
------------------------------------
It depends on the communication bus system how much buffer shall be reserved. For example on CAN a buffer of more than 4095 will not bring any advantage since the CanTp can transfer only up to 4095 bytes.

Dependencies:
------------------------------------
In case of Paged Buffer usage (refer to DcmPageBufferCfg), the buffer size shall be chosen such that at least the longest snapshot record/extended data record of the Dem plus some additional bytes (i.e. in case of CAN -> 6 additional bytes) will fit it.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The greater the buffer the more RAM will be required.

Stack RAM usage effects:
------------------------------------
none

##### 4. DcmDslDiagResp

**容器属性**:

- **UUID**: `681203d2-5f46-42e9-be66-f653e1641960`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslDiagResp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the ResponsePending handling

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslDiagRespMaxNumOfDeclinedRequests

- **UUID**: `b8a4cc8e-379a-4c11-8525-8c824318acb7`
- **参数名**: `DcmDslDiagRespMaxNumOfDeclinedRequests`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `3`
- **取值范围**: [1..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the maximum number of reactions upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
The Dcm will calculate the required amount of resources upon the specified by this option resource for parallel client processing.

Constraints:
------------------------------------
If the amount of configured requests exceeds the total number of Dcm connections, during the code generation the resource usage optimization will be disabled and only as many as available diagnostic connection objects will be allocated. This will also shorten the run time usage (see below).

Dependencies:
------------------------------------
Has any effect only if DcmDslDiagRespOnSecondDeclinedRequest is enabled.

Runtime effects:
------------------------------------
The more clients to be handled the longer the run time for looking up for free resources. If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the run time will be minimal.

Code ROM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the code ROM will be minimal.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
The more clients to be handled the more RAM will be required for handling them.

Stack RAM usage effects:
------------------------------------
If the number of declined requests matches the total number of Dcm connection, no look up will be necessary, and the stack usage will be minimal.

####### BOOLEAN 类型参数

######## 1. DcmDslDiagRespOnSecondDeclinedRequest

- **UUID**: `86bd212d-f489-4881-a9ac-230cd0222f33`
- **参数名**: `DcmDslDiagRespOnSecondDeclinedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC V1.0.0
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Defines the reaction upon a second request (ClientB) that can not be processed (e.g. due to priority assessment).

Effect:
------------------------------------
If enabled, the Dcm will reject any nested diagnostic request by NRC 0x21 (BusyRepeatRequest).

Constraints:
------------------------------------
For optimization reasons not all Dcm managed connection will support this feature by default. It is configurable how many parallel (nested) request to be handled at a time to save RAM and run time resources.

Dependencies:
------------------------------------
Refer to DcmDslDiagRespMaxNumOfDeclinedRequests.

Runtime effects:
------------------------------------
If enabled the Dcm diagnostic request reception functionality will have slightly increased run time usage.

Code ROM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased code ROM usage.

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
If enabled the Dcm will have slightly increased RAM usage.

Stack RAM usage effects:
------------------------------------
If enabled the Dcm will have insignificantly increased stack usage within the Rx ISRs.

##### 5. DcmDslProtocol

**容器属性**:

- **UUID**: `566ab607-9811-4e9a-9e18-761c606d4d87`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocol`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for the protocol configuration (for each protocol) The following parameters needs to be configured per protocol.

###### 配置容器

本模块包含 **7** 个配置容器：

####### 1. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 配置容器

本模块包含 **6** 个配置容器：

######### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# ENUMERATION 类型参数

############## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

############ 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

######### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

####### 2. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 3. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 4. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 5. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 6. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

########## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 7. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

##### 6. DcmDslProtocolRow

**容器属性**:

- **UUID**: `69397f01-5f41-444d-80c0-3d223cd144dd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRow`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of configuration for the protocol configuration (for each protocol)

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. DcmDslProtocolID

- **UUID**: `7cacd112-3d73-47b3-bfad-759306b9f934`
- **参数名**: `DcmDslProtocolID`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `DCM_UDS_ON_CAN`
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **可选值**:
  - `DCM_OBD_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_OBD_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODICTRANS_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_PERIODIC_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_ROE_ON_IP` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_1` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_10` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_11` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_12` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_13` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_14` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_15` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_2` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_3` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_4` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_5` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_6` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_7` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_8` (来源: AUTOSAR_ECUC)
  - `DCM_SUPPLIER_9` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_CAN` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_FLEXRAY` (来源: AUTOSAR_ECUC)
  - `DCM_UDS_ON_IP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the diagnostic protocol type the Dcm shall manage.

Effect:
------------------------------------
On a multi protocol configuration Dcm will be able to distinguish among different protocols and notify the application for activation/deactivation of a concrete protocol, specified by this parameter.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
Has any effect only if multi protocol configuration is used.

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 配置容器

本模块包含 **6** 个配置容器：

####### 1. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### ENUMERATION 类型参数

############ 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 2. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 3. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 4. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 5. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

########## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

####### 6. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

##### 7. DcmDslMainConnection

**容器属性**:

- **UUID**: `b6223664-f4c0-4643-bf58-d60542a8bd76`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslMainConnection`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains configuration for Diagnostic Main Connection

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslProtocolRxTesterSourceAddr

- **UUID**: `57e3434f-43b4-47a9-bed5-464edc2858c7`
- **参数名**: `DcmDslProtocolRxTesterSourceAddr`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies a unique identifier of a diagnostic client connection.

Effect:
------------------------------------
The Dcm is able to identify different clients or the same client on multiple channels using this identifier.

Constraints:
------------------------------------
For each DcmDslConnection there shall be a unique value assigned to this parameter.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 2. DcmDslPayloadLimit

- **UUID**: `de24719f-368d-459b-ba47-c4a382c2c9d6`
- **参数名**: `DcmDslPayloadLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `4095`
- **取值范围**: [0..4294967295]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### ENUMERATION 类型参数

########## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 2. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 8. DcmDslProtocolRx

**容器属性**:

- **UUID**: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolRx`
- **多重性**: [1..infinite]
- **构建后可变**: true
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslProtocolRxPduId

- **UUID**: `c1878cd5-53e7-4aac-967a-d45a3a0a5bf7`
- **参数名**: `DcmDslProtocolRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm receive PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### ENUMERATION 类型参数

######## 1. DcmDslProtocolRxAddrType

- **UUID**: `cf7494dd-519f-47da-8153-500cd836732c`
- **参数名**: `DcmDslProtocolRxAddrType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **可选值**:
  - `DCM_FUNCTIONAL_TYPE` (来源: AUTOSAR_ECUC)
  - `DCM_PHYSICAL_TYPE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the request addressing type on a concrete receive Dcm PduId.

Effect:
------------------------------------
Depending on the request type specified here, the Dcm will be able to react correctly according to the ISO14229-1.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DcmDslProtocolRxPduRef

- **UUID**: `3959fea7-2e1f-44d0-afe4-78b7d314f138`
- **引用名**: `DcmDslProtocolRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm receive PduId with a concrete Dcm receive PDU.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only receive PDUs for the ECU diagnostics shall be assigned here.
The same receive PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. DcmDslProtocolRxComMChannelRef

- **UUID**: `ef9ab668-4550-4a6e-ba0f-cfe452ce0475`
- **引用名**: `DcmDslProtocolRxComMChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a specific ComMChannel with a Dcm logical receive PduId.

Effect:
------------------------------------
With this parameter the Dcm will be able to keep the communication on the specified ComMChannel awake as required by AR 4 DCM SWS.

Constraints:
------------------------------------
The ComMChannel shall be exactly the one that corresponds to the communication channel on which the PDU linked in DcmDslProtocolRxPduRef is to be received.

Dependencies:
------------------------------------
Refer to: /Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection/DcmDslMainConnection/DcmDslProtocolRx/DcmDslProtocolRxPduRef

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 9. DcmDslProtocolTx

**容器属性**:

- **UUID**: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslProtocolTx`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslTxConfirmationPduId

- **UUID**: `6999d354-09d4-4652-a3c2-3702e8c1a726`
- **参数名**: `DcmDslTxConfirmationPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete Dcm transmit PDU.
NOTE: This value is generated automatically by the Configurator 5 tool.

Effect:
------------------------------------
Using this value Dcm is able to distinguish the different transport layer connections at response confirmation time.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DcmDslProtocolTxPduRef

- **UUID**: `ef40b7c1-70bf-42aa-b6ed-af3ba92ec4c9`
- **引用名**: `DcmDslProtocolTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Links a logical Dcm transmit PDU with a concrete Dcm transmit PDU, that will be used for diagnostic response transmission.

Effect:
------------------------------------
This setting connects the Dcm to the outside world.

Constraints:
------------------------------------
Only transmit PDUs for the ECU diagnostics shall be assigned here.
The same transmit PDU shall not be used again in other Dcm connections.

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 10. DcmDslConnectionGroup

**容器属性**:

- **UUID**: `a46a85c7-05cc-4b11-b2a0-b81fe61d771e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslConnectionGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslConnectionGroupId

- **UUID**: `1b8b357b-2ee4-4143-8483-ed81fe665943`
- **参数名**: `DcmDslConnectionGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. DcmDslConnectionConcurrentRef

- **UUID**: `60997db5-f564-4200-9e6e-55f8b3016e16`
- **引用名**: `DcmDslConnectionConcurrentRef`
- **引用类型**: REFERENCE
- **多重性**: [2..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

##### 11. DcmDslBroadcastGroup

**容器属性**:

- **UUID**: `dcc5d3a5-9efc-4cdb-82e8-611cde8e7179`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDslBroadcastGroup`
- **多重性**: [0..infinite]
- **构建后可变**: true

**容器描述**:

Aggregate DcmDslMainConnections to a group.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. DcmDslBroadcastGroupId

- **UUID**: `c1a1a294-8a95-4c16-ba7f-a5d04a170f81`
- **参数名**: `DcmDslBroadcastGroupId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..65535]
- **来源**: Vector Informatik
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the logical handle value of a concrete DcmDslConnectionGroup.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. DcmDslConnectionBroadCastRef

- **UUID**: `82730a03-8527-40aa-807b-a58436e2f45f`
- **引用名**: `DcmDslConnectionBroadCastRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a broadcast DcmDslConnection using surrogates.

######## 2. DcmDslConnectionSurrogateRef

- **UUID**: `a5329195-c7b6-4a88-a959-6ac9343a28cc`
- **引用名**: `DcmDslConnectionSurrogateRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `DcmDslConnection`
- **完整路径**: `/AUTOSAR/EcucDefs/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmDslConnection`
- **来源**: Vector Informatik
- **需要索引**: false
- **实现配置类**:
  - POST-BUILD: VARIANT-POST-BUILD-LOADABLE
  - POST-BUILD: VARIANT-POST-BUILD-SELECTABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a list of surrigates for DcmDslConnectionRef.

##### 12. DcmDsp

**容器属性**:

- **UUID**: `d5467754-0556-48c7-9c8a-9d2c033866a6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDsp`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

These parameters apply to Diagnostic Service Processing. There will always be one set of these parameters per DCM.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. DcmDspSession

**容器属性**:

- **UUID**: `d32a2b80-994d-4157-927d-da1695c68655`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSession`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes all diagnostic sessions the Dcm shall support.

Effect:
------------------------------------
For each diagnostic session to be supported by Dcm a DcmDspSessionRow sub-container shall be defined.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of sessions defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########### FLOAT 类型参数

############ 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

############ 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### 2. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### FLOAT 类型参数

########## 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 13. DcmDspSession

**容器属性**:

- **UUID**: `d32a2b80-994d-4157-927d-da1695c68655`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSession`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container includes all diagnostic sessions the Dcm shall support.

Effect:
------------------------------------
For each diagnostic session to be supported by Dcm a DcmDspSessionRow sub-container shall be defined.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration data ROM usage scales straight proportionally to the number of sessions defined.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######### FLOAT 类型参数

########## 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

########## 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 14. DcmDspSessionRow

**容器属性**:

- **UUID**: `474e897a-1f11-4a6a-b12b-6833a1ec743f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmDspSessionRow`
- **多重性**: [1..31]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

Definition of a single Row of session control configuration (per session control)

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. DcmDspSessionLevel

- **UUID**: `0f638658-eb25-4b3e-b1e0-47676a032f21`
- **参数名**: `DcmDspSessionLevel`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Specifies the value of the corresponding diagnostic session.

Effect:
------------------------------------
This value will be used when the Dcm_GetSesCtrlType API is called from the application to report the currently active session.

Constraints:
------------------------------------
For each session level, there shall always be a corresponding sub-services for service 0x10.

Dependencies:
------------------------------------
Refer to "Dcm/DcmConfigSet/DcmDsd/DcmDsdServiceTable/DcmDsdService/DcmDsdSubService/DcmDsdSubServiceId".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

####### FLOAT 类型参数

######## 1. DcmDspSessionP2ServerMax

- **UUID**: `ab56e33f-a4fb-44dd-92c1-10d05ac17dcf`
- **参数名**: `DcmDspSessionP2ServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.05`
- **取值范围**: [0..1000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2 time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2ServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

######## 2. DcmDspSessionP2StarServerMax

- **UUID**: `af4586fc-14c1-422b-b2e5-f1bf5e275db9`
- **参数名**: `DcmDspSessionP2StarServerMax`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `5`
- **取值范围**: [0..100000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Determines the diagnostic session specific P2* time in seconds.

Effect:
------------------------------------
This parameter will be reported by Dcm within the positive response to the corresponding session activation request. The really monitored time by Dcm is specified from the currently active protocol.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
For the real monitored time adjustment refer to "/Dcm/DcmConfigSet/DcmDsl/DcmDslProtocol/DcmDslProtocolRow/DcmTimStrP2StarServerAdjust".

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
none

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

##### 15. DcmGeneral

**容器属性**:

- **UUID**: `ca892183-66d6-4a91-bef4-34c98a2ee15a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmGeneral`
- **多重性**: [1..1]
- **构建后可变**: false
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) for Component wide parameters

###### 参数配置

此容器包含 **11** 个参数：

####### INTEGER 类型参数

######## 1. DcmNwStatusRxBufferSize

- **UUID**: `b276419f-daab-4a5c-be70-95651af81c4f`
- **参数名**: `DcmNwStatusRxBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `32`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Buffer size for the network status reception buffer.

######## 2. DcmCanHardwareLoopTimeout

- **UUID**: `7767ddb0-0006-4465-82a4-6c8b1699c1dd`
- **参数名**: `DcmCanHardwareLoopTimeout`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `100`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Timeout value for CAN hardware loops (in cycles, typically 1 ms)

######## 3. DcmTaskCycle

- **UUID**: `51bb97da-a9ec-415f-b718-fdfe9a7e4eb0`
- **参数名**: `DcmTaskCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `5`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Cycle count of CanTp, FrSM, EthSM and ComM tasks. Other tasks are either called every timer cycle (Ethernet) or polled (CAN)

####### BOOLEAN 类型参数

######## 1. DcmQueuedRequest

- **UUID**: `087031f4-ff23-43eb-9593-667b54f9580a`
- **参数名**: `DcmQueuedRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE

######## 2. DcmKeySlotMode

- **UUID**: `56729bdb-1932-4a86-9af6-6d5ef2f69122`
- **参数名**: `DcmKeySlotMode`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Enable switching from key slot to all slot mode.

######## 3. DcmBaudrateSwitch

- **UUID**: `9ebffaa5-cae0-40b6-9203-88900e2aabe3`
- **参数名**: `DcmBaudrateSwitch`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter switches the APIs FblCwCheckBaudrate and FblCwSwitchBaudrate ON or OFF.
true: APIs are enabled.
false: APIs are disabled.

######## 4. DcmVersionInfoApi

- **UUID**: `98b138ad-3fe8-45bb-922a-1b79f18a099a`
- **参数名**: `DcmVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Preprocessor switch to enable or disable the output Version info of the functionality.

######## 5. DcmDevErrorDetect

- **UUID**: `5c1785d4-21d8-4f87-b076-905ff53284ac`
- **参数名**: `DcmDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Switches the Default Error Tracer (Det) detection and notification ON or OFF.

######## 6. DcmRespondAllRequest

- **UUID**: `5ef12de4-4f82-4ed9-8888-74411a19551d`
- **参数名**: `DcmRespondAllRequest`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: If set to FALSE the Dcm will not respond to diagnostic request  that contains a service ID which is in the range from 0x40 to 0x7F or in the  range from 0xC0 to 0xFF (Response IDs).

####### FLOAT 类型参数

######## 1. DcmTaskTime

- **UUID**: `7b09f5ff-359b-42e1-8167-f0e8559cf91d`
- **参数名**: `DcmTaskTime`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.01`
- **取值范围**: [0..100]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Allow to configure the time for the periodic cyclic task in seconds.

Effect:
-----------------------------------------
This value is used to set up the Dcm Service-Description and BSW scheduler. All diagnostic timers managed by Dcm use this setting as a base time for the internal time constants' calculation.

Constraints:
-----------------------------------------
The specified time shall be a multiple of the time values defined in all diagnostic timing settings in the Dcm configuration.

Dependencies:
-----------------------------------------
All diagnostic timing parameters.

Runtime effects:
-----------------------------------------
Too low values will increase the Dcm responsiveness, but will increase the CPU load. Too high values of this parameter will lead to rear Dcm task activation (lower CPU load), but the Dcm internal timers' accuracy will not be optimal.

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
-----------------------------------------
none

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
none

####### STRING 类型参数

######## 1. DcmUserConfigFile

- **UUID**: `9ca97de0-16fe-4beb-b27d-52482ec00324`
- **参数名**: `DcmUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: Path to an external user configuration file used by the Configurator 5 generation tool.

Effect:
-----------------------------------------
If you want to overwrite some of the settings in the generated configuration file (Dcm_Cfg.h), you can specify a path to a user defined configuration file. The user defined configuration file will be included at the end of the generated preprocessor switches. Definitions in the user defined configuration file can overwrite definitions in the generated configuration file.

The path shall be a valid path to the user configuration file. For simplified and project specific user configuration files references, the following Configurator 5 environment variables can be used:

$(DpaProjectFolder) Absolute directory of the loaded *.dpa file.
$(EcuProjectName) Name of the project defined in the loaded *.dpa file.
$(EcucFile) Absolute directory "ECUC", defined by the loaded *.dpa file, containing files $(EcuProjectName).ecuc.arxml and $(EcuProjectName).ecuc.Initial.arxml .
$(EcucFolder) Parent directory of $(EcucFile).
$(SipRootPath) Absolute directory "SIP", defined by the loaded *.dpa file.
$(OutputFolder) (Relative) directory "GenData", defined by the loaded *.dpa file. See setting "Root Target Folder" of Configurator 5.
$(ServiceSwcFolder) Absolute directory "ServiceComponents", defined by the loaded *.dpa file.


Constraints:
-----------------------------------------
Not all of the settings can be overwritten simply by triggering the preprocessor switch. Some of the options are complex and the code generator generates less or more code depending on the setting.

USE SUCH A FILE ONLY AFTER DISCUSSION WITH VECTOR.

Dependencies:
-----------------------------------------
none

Runtime effects:
-----------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
-----------------------------------------
none

Global RAM usage effects:
-----------------------------------------
none

Stack RAM usage effects:
-----------------------------------------
none

##### 16. DcmGeneration

**容器属性**:

- **UUID**: `ba671fb2-6bd9-48e6-840c-839be96b46b7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `DcmGeneration`
- **多重性**: [1..1]
- **构建后可变**: false

**容器描述**:

Contains the generation configuration parameters of the module.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. DcmReduceNumericalDataByOffsetThreshold

- **UUID**: `47eeafcf-4fe1-4bb7-8dea-9e1be908afd8`
- **参数名**: `DcmReduceNumericalDataByOffsetThreshold`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `2`
- **取值范围**: [0..]
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to compress numerical CONFIG-CLASS PRE-COMPILE ROM data by using a constant offset.
0: The optimization is not performed.
>0: This is the threshold to activate the data optimization.

Code: the code size is increased due to the usage of the constant offset operation in the data access.
RAM: no change expected.
ROM: the ROM size is minimized.
Runtime: the runtime is increased due to the usage of the constant offset operation in the data access.

####### BOOLEAN 类型参数

######## 1. DcmReduceConstantData2Define

- **UUID**: `386752e4-bb7d-4da9-aa68-51a9a10d7463`
- **参数名**: `DcmReduceConstantData2Define`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate CONFIG-CLASS PRE-COMPILE ROM arrays as constant define.

FALSE: ROM arrays are generated as data even if all values are identical.
TRUE: ROM arrays are generated as constant define if all values are identical.

######## 2. DcmShortSymbols

- **UUID**: `ebcee410-b23c-420f-b66f-ab98f67f425e`
- **参数名**: `DcmShortSymbols`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate shortened symbol names.

FALSE: symbol names are generated in a human readable style based on the MIP, tags and variant names.
TRUE: symbol names are generated based on the MIP and a CRC32.

######## 3. DcmInterfacesForDeactivatedData

- **UUID**: `132320e3-4ee1-43fc-b68e-542ac9bf3a56`
- **参数名**: `DcmInterfacesForDeactivatedData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate bsw data interfaces for deactivated data elements. This is an advantage for the BSW developer to reduce the time to market with a development environment using auto completition and to investigate potential interfaces.

FALSE: data interfaces are not generated if the data elementis deactivated.
TRUE: data interfaces are generated as e.g. emty macros.

######## 4. DcmReferringKeysInComments

- **UUID**: `d2d99bed-162b-4950-8616-703ddc1f5684`
- **参数名**: `DcmReferringKeysInComments`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
  - PRE-COMPILE: VARIANT-POST-BUILD-LOADABLE
  - PRE-COMPILE: VARIANT-POST-BUILD-SELECTABLE
- **描述**: This parameter activates/deactivates the capability to generate referring keys in comments. This is an advantage for the developer to investigate indirections, but this feature reduces the overall readability of the generated data.

FALSE: referring keys are not generated in comments.
TRUE: referring keys are generated in comments.

##### 17. DcmDslConnection

**容器属性**:

- **UUID**: `461bf004-6e77-4807-a2ab-69e5c8a916db`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `DcmDslConnection`
- **多重性**: [1..254]
- **构建后可变**: true

**容器选择**:

- **DcmDslMainConnection**
  - UUID: `b6223664-f4c0-4643-bf58-d60542a8bd76`
  - 描述: This container contains configuration for Diagnostic Main Connection
- **DcmDslProtocolRx**
  - UUID: `7913793a-1b8e-42d9-bcf3-e65ed2640add`
  - 描述: This container describes a single Dcm logical receive PDU.

Effect:
------------------------------------
For each defined DcmDslProtocolRx, the Dcm will be able to receive a diagnostic request.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm receive PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none
- **DcmDslProtocolTx**
  - UUID: `ab98c28c-4cd8-42e4-a56d-72a011a08b95`
  - 描述: This container describes a single Dcm logical transmit PDU.

Effect:
------------------------------------
If DcmDslProtocolTx is defined, the Dcm will be able to respond to a diagnostic request on the associated main-connection.

Constraints:
------------------------------------
none

Dependencies:
------------------------------------
none

Runtime effects:
------------------------------------
none

Code ROM usage effects:
------------------------------------
none

Const data ROM usage effects:
------------------------------------
The Dcm configuration ROM usage scales straight proportionally with the number of Dcm transmit PDUs.

Global RAM usage effects:
------------------------------------
none

Stack RAM usage effects:
------------------------------------
none

**容器描述**:

This container contains links between Diagnostic Protocol (=DcmDslProtocolRow) and the according Rx or Tx channel.

## 📦 包结构

此ARXML文件包含 **1** 个包：

### 1. MICROSARFBL

- **UUID**: `2e83f445-6582-4070-922e-cd2fec8bf60a`
- **包名称**: `MICROSARFBL`
- **包含元素数量**: 4

#### 包含的元素

##### BSW-IMPLEMENTATION 类型元素

1. **Dcm_Impl**

##### ECUC-MODULE-DEF 类型元素

1. **Dcm**

##### ECUC-MODULE-CONFIGURATION-VALUES 类型元素

1. **Dcm_Pre**
2. **Dcm_Rec**

## ⚡ 实现信息

此ARXML文件包含 **1** 个实现：

### 1. Dcm_Impl

- **UUID**: `c2d49cc4-56d4-45bc-b9e1-498ac0f93e78`
- **实现名称**: `Dcm_Impl`
- **编程语言**: C
- **软件版本**: 8.03.00
- **供应商ID**: 30
- **AUTOSAR版本**: 4.00.03
- **代码生成器**: DaVinci Configurator

## ⚙️ 配置信息

此ARXML文件包含 **2** 个配置：

### 1. Dcm_Pre

- **UUID**: `dc343c54-4292-499a-8b9f-1d7e37445ef5`
- **配置名称**: `Dcm_Pre`
- **定义引用**: `/MICROSARFBL/Dcm`

### 2. Dcm_Rec

- **UUID**: `d28aaede-e8d6-41bc-b5ec-f46192909c7a`
- **配置名称**: `Dcm_Rec`
- **定义引用**: `/MICROSARFBL/Dcm`
