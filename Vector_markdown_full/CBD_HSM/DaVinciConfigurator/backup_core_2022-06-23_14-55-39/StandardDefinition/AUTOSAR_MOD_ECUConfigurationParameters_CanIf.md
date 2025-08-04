# CanIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:08

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [CanIf](#canif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. CanIf

#### 基本信息

- **UUID**: `ECUC:9fe4bd2d-b284-4b83-a09c-b4cebf548834`
- **模块名称**: `CanIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

This container includes all necessary configuration sub-containers according the CAN Interface configuration structure.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **19** 个配置容器：

##### 1. CanIfCtrlDrvCfg

**容器属性**:

- **UUID**: `ECUC:4ff0a387-1540-4a20-b4fd-7e4db255693c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfCtrlDrvCfg`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Configuration parameters for all the underlying CAN Driver modules are aggregated under this container. For each CAN Driver module a seperate instance of this container has to be provided.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. CanIfCtrlDrvTxCancellation

- **UUID**: `ECUC:b0707b5f-8882-4134-9c60-f9cf2b3dae69`
- **参数名**: `CanIfCtrlDrvTxCancellation`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether transmit cancellation is supported and if the appropriate callback will be provided to the CAN Driver module.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfCtrlDrvInitHohConfigRef

- **UUID**: `ECUC:7cc6ea68-c474-476c-bfa7-c708dc13b8e9`
- **引用名**: `CanIfCtrlDrvInitHohConfigRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfInitHohCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfInitHohCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Init Hoh Configuration

######## 2. CanIfCtrlDrvNameRef

- **UUID**: `ECUC:43775a13-040e-4111-8726-37ed6aaa2bad`
- **引用名**: `CanIfCtrlDrvNameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanGeneral`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanGeneral`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Interface Driver Reference.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanIfCtrlCfg

**容器属性**:

- **UUID**: `ECUC:246d0d0a-4754-4319-bd38-a8b3c421e928`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfCtrlCfg`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an adressed CAN controller by an underlying CAN Driver module. This container is configurable per CAN controller.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanIfCtrlId

- **UUID**: `ECUC:a8a153f3-d90b-4927-99eb-a14bf9c518e2`
- **参数名**: `CanIfCtrlId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter abstracts from the CAN Driver specific parameter Controller. Each controller of all connected CAN Driver modules shall be assigned to one specific ControllerId of the CanIf.

######### BOOLEAN 类型参数

########## 1. CanIfCtrlWakeupSupport

- **UUID**: `ECUC:a822b4db-6043-422c-aa90-e16e7963d3fd`
- **参数名**: `CanIfCtrlWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if a respective controller of the referenced CAN Driver modules is queriable for wake up events.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfCtrlCanCtrlRef

- **UUID**: `ECUC:04062985-d3bb-4998-9129-485e796c0950`
- **引用名**: `CanIfCtrlCanCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanController`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references to the logical handle of the underlying CAN controller from the CAN Driver module to be served by the CAN Interface module. The following parameters of CanController config container shall be referenced by this link: CanControllerId, CanWakeupSourceRef

##### 2. CanIfCtrlCfg

**容器属性**:

- **UUID**: `ECUC:246d0d0a-4754-4319-bd38-a8b3c421e928`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfCtrlCfg`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of an adressed CAN controller by an underlying CAN Driver module. This container is configurable per CAN controller.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanIfCtrlId

- **UUID**: `ECUC:a8a153f3-d90b-4927-99eb-a14bf9c518e2`
- **参数名**: `CanIfCtrlId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter abstracts from the CAN Driver specific parameter Controller. Each controller of all connected CAN Driver modules shall be assigned to one specific ControllerId of the CanIf.

####### BOOLEAN 类型参数

######## 1. CanIfCtrlWakeupSupport

- **UUID**: `ECUC:a822b4db-6043-422c-aa90-e16e7963d3fd`
- **参数名**: `CanIfCtrlWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if a respective controller of the referenced CAN Driver modules is queriable for wake up events.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanIfCtrlCanCtrlRef

- **UUID**: `ECUC:04062985-d3bb-4998-9129-485e796c0950`
- **引用名**: `CanIfCtrlCanCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanController`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references to the logical handle of the underlying CAN controller from the CAN Driver module to be served by the CAN Interface module. The following parameters of CanController config container shall be referenced by this link: CanControllerId, CanWakeupSourceRef

##### 3. CanIfDispatchCfg

**容器属性**:

- **UUID**: `ECUC:da4c74dd-cfdf-43a2-94c4-a32a24264e54`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfDispatchCfg`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Callback functions provided by upper layer modules of the CanIf. The callback functions defined in this container are common to all configured CAN Driver / CAN Transceiver Driver modules.

###### 参数配置

此容器包含 **14** 个参数：

####### ENUMERATION 类型参数

######## 1. CanIfDispatchUserCheckTrcvWakeFlagIndicationUL

- **UUID**: `ECUC:0bbaf0c7-4bc2-4004-add9-2e41e44b0cb3`
- **参数名**: `CanIfDispatchUserCheckTrcvWakeFlagIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer module to which the CheckTrcvWakeFlagIndication from the Driver modules have to be routed.

######## 2. CanIfDispatchUserClearTrcvWufFlagIndicationUL

- **UUID**: `ECUC:9547aae5-127b-4d0d-90a2-3ba8a27fcd9c`
- **参数名**: `CanIfDispatchUserClearTrcvWufFlagIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer module to which the ClearTrcvWufFlagIndication from the Driver modules have to be routed.

######## 3. CanIfDispatchUserConfirmPnAvailabilityUL

- **UUID**: `ECUC:e3ad75a1-387d-4959-a130-dbefbe31f022`
- **参数名**: `CanIfDispatchUserConfirmPnAvailabilityUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer module to which the ConfirmPnAvailability notification from the Driver modules have to be routed. If CANIF_PUBLIC_PN_SUPPORT equals False, this parameter shall not be configurable.

######## 4. CanIfDispatchUserCtrlBusOffUL

- **UUID**: `ECUC:8f40960d-471f-43b1-8ba4-02b4259d3ca5`
- **参数名**: `CanIfDispatchUserCtrlBusOffUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the notifications of all ControllerBusOff events from the CAN Driver modules have to be routed via <User_ControllerBusOff>.

######## 5. CanIfDispatchUserCtrlModeIndicationUL

- **UUID**: `ECUC:de1ff686-12ee-4ad7-9ec0-6be01bf31f78`
- **参数名**: `CanIfDispatchUserCtrlModeIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the notifications of all ControllerTransition events from the CAN Driver modules have to be routed

######## 6. CanIfDispatchUserTrcvModeIndicationUL

- **UUID**: `ECUC:239a6399-5602-4010-94b5-039c6223fed2`
- **参数名**: `CanIfDispatchUserTrcvModeIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_SM` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the notifications of all TransceiverTransition events from the CAN Transceiver Driver modules have to be routed via <User_TrcvModeIndication>. If no UL module is configured, no upper layer callback function will be called.

######## 7. CanIfDispatchUserValidateWakeupEventUL

- **UUID**: `ECUC:59b203fd-969e-44cd-afab-698d689e3bcf`
- **参数名**: `CanIfDispatchUserValidateWakeupEventUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `ECUM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the notifications about positive former requested wake up sources have to be routed via <User_ValidateWakeupEvent>. If parameter CANIF_WAKEUP_CHECK_VALIDATION_API is disabled, this parameter cannot be configured.

####### FUNCTION-NAME 类型参数

######## 1. CanIfDispatchUserCheckTrcvWakeFlagIndicationName

- **UUID**: `ECUC:b4cc3170-04f6-45b8-973b-353ede6489a7`
- **参数名**: `CanIfDispatchUserCheckTrcvWakeFlagIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ClearTrcvWufFlagIndication>.

######## 2. CanIfDispatchUserClearTrcvWufFlagIndicationName

- **UUID**: `ECUC:b0e98d0b-7b7f-42d7-accc-d19c2e52d62d`
- **参数名**: `CanIfDispatchUserClearTrcvWufFlagIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ClearTrcvWufFlagIndication>.

######## 3. CanIfDispatchUserConfirmPnAvailabilityName

- **UUID**: `ECUC:1956eddd-c62d-45f4-b50f-2836baf0b3b3`
- **参数名**: `CanIfDispatchUserConfirmPnAvailabilityName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ConfirmPnAvailability>. If CANIF_DISPATCH_USERCONFIRMPNAVAILABILITY_UL equals CAN_SM the name of <User_ConfirmPnAvailability> is fixed. If it equals CDD, the name is selectable. If CANIF_PUBLIC_PN_SUPPORT equals False, this parameter shall not be configurable.

######## 4. CanIfDispatchUserCtrlBusOffName

- **UUID**: `ECUC:52c27ccd-402a-494b-bd19-307b4fe68bc7`
- **参数名**: `CanIfDispatchUserCtrlBusOffName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ControllerBusOff>.

######## 5. CanIfDispatchUserCtrlModeIndicationName

- **UUID**: `ECUC:163858a2-5ab3-4b1e-979e-789380918c8d`
- **参数名**: `CanIfDispatchUserCtrlModeIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ControllerModeIndication>.

######## 6. CanIfDispatchUserTrcvModeIndicationName

- **UUID**: `ECUC:87fa49c3-2244-4fb9-9714-1ed1606100b8`
- **参数名**: `CanIfDispatchUserTrcvModeIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_TrcvModeIndication>.

######## 7. CanIfDispatchUserValidateWakeupEventName

- **UUID**: `ECUC:06a66545-ca16-4f21-ad87-0e7b360f802a`
- **参数名**: `CanIfDispatchUserValidateWakeupEventName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of <User_ValidateWakeupEvent>. This

##### 4. CanIfInitCfg

**容器属性**:

- **UUID**: `ECUC:5f4506a5-be5f-497c-9349-d69427ba9d24`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfInitCfg`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the init parameters of the CAN Interface.

###### 参数配置

此容器包含 **1** 个参数：

####### STRING 类型参数

######## 1. CanIfInitCfgSet

- **UUID**: `ECUC:f4e0b7a4-681f-4ad2-8372-a25c6eb1dae3`
- **参数名**: `CanIfInitCfgSet`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the CAN Interface specific configuration setup. This type of the external data structure shall contain the post build initialization data for the CAN Interface for all underlying CAN Dirvers.

###### 配置容器

本模块包含 **10** 个配置容器：

####### 1. CanIfBufferCfg

**容器属性**:

- **UUID**: `ECUC:2541ff9b-ca8a-4388-b3e9-4e893a369d4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfBufferCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Txbuffer configuration. Multiple buffers with different sizes could be configured. If CanIfBufferSize (CANIF834_Conf) equals 0, the CanIf Tx L-PDU only refers via this CanIfBufferCfg the corresponding CanIfHthCfg.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanIfBufferSize

- **UUID**: `ECUC:3e890c54-df3d-4d91-bee8-0f6ee7a81053`
- **参数名**: `CanIfBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of CanIf Tx L-PDUs which can be buffered in one Txbuffer. If this value equals 0, the CanIf does not perform Txbuffering for the CanIf Tx L-PDUs which are assigned to this Txbuffer. If CanIfPublicTxBuffering equals False, this parameter equals 0 for all TxBuffer. If the CanHandleType of the referred HTH equals FULL, this parameter equals 0 for this TxBuffer.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfBufferHthRef

- **UUID**: `ECUC:fb6c787d-41aa-4920-8680-030a0a2e8bc2`
- **引用名**: `CanIfBufferHthRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CanIfHthCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfInitHohCfg/CanIfHthCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to HTH, that defines the hardware object or the pool of hardware objects configured for transmission. All the CanIf Tx L-PDUs refer via the CanIfBufferCfg and this parameter to the HTHs if TxBuffering is enabled, or not.

####### 2. CanIfInitHohCfg

**容器属性**:

- **UUID**: `ECUC:c2f0d182-e8ee-4d61-8286-d2eeadc94428`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfInitHohCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the references to the configuration setup of each underlying CAN Driver.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfInitRefCfgSet

- **UUID**: `ECUC:71d02940-8e9e-4d69-94d7-09050c8d2a9a`
- **引用名**: `CanIfInitRefCfgSet`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanConfigSet`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the CAN Interface specific configuration setup. This type of external data structure shall contain the post build initialization data for the CAN Interface for all underlying CAN Drivers.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. CanIfHrhCfg

**容器属性**:

- **UUID**: `ECUC:a98b1f9b-0224-4f3b-80fc-49dc63340626`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains configuration parameters for each hardware receive object (HRH).

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. CanIfHrhSoftwareFilter

- **UUID**: `ECUC:60990db4-406e-4792-9c8f-82ebf55557e6`
- **参数名**: `CanIfHrhSoftwareFilter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the hardware receive objects by using the HRH range/list from CAN Driver configuration to define, for which HRH a software filtering has to be performed at during receive processing.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. CanIfHrhCanCtrlIdRef

- **UUID**: `ECUC:624b2048-16ec-4408-85dc-a82a5c93e09c`
- **引用名**: `CanIfHrhCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HRH belongs to. A controller can contain one or more HRHs.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CanIfHrhCanHandleTypeRef

- **UUID**: `ECUC:84efc600-5948-407e-9a17-57f955f0691c`
- **引用名**: `CanIfHrhCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CAN Driver Module configuration. The type of the HRH can either be Full-CAN or Basic-CAN. The type of HRHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object. If BasicCAN is configured, software filtering is enabled.

############ 2. CanIfHrhIdSymRef

- **UUID**: `ECUC:1fbf0d02-5160-4182-b3bd-488d490d9c7a`
- **引用名**: `CanIfHrhIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

############## 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

############# ENUMERATION 类型参数

############## 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

######### 2. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

############ 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########### ENUMERATION 类型参数

############ 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

######### 3. CanIfHthCfg

**容器属性**:

- **UUID**: `ECUC:5e0633ce-3473-4f6e-b7d5-51210b9247ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHthCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains parameters related to each HTH.

########## 引用关系

此容器包含 **3** 个引用：

########### REFERENCE 类型引用

############ 1. CanIfHthCanCtrlIdRef

- **UUID**: `ECUC:698f1110-fa03-4dd0-9eb2-035e074c3e3d`
- **引用名**: `CanIfHthCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HTH belongs to. A controller can contain one or more HTHs.

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. CanIfHthCanHandleTypeRef

- **UUID**: `ECUC:152513ea-515c-43da-9810-5e249ee4bf1e`
- **引用名**: `CanIfHthCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CAN Driver Module configuration. The type of the HTH can either be Full-CAN or Basic-CAN. The type of HTHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object.

############ 2. CanIfHthIdSymRef

- **UUID**: `ECUC:993e2b0d-53d4-43e5-9ef8-3dffe7bcd33b`
- **引用名**: `CanIfHthIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

####### 3. CanIfHrhCfg

**容器属性**:

- **UUID**: `ECUC:a98b1f9b-0224-4f3b-80fc-49dc63340626`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains configuration parameters for each hardware receive object (HRH).

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. CanIfHrhSoftwareFilter

- **UUID**: `ECUC:60990db4-406e-4792-9c8f-82ebf55557e6`
- **参数名**: `CanIfHrhSoftwareFilter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the hardware receive objects by using the HRH range/list from CAN Driver configuration to define, for which HRH a software filtering has to be performed at during receive processing.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfHrhCanCtrlIdRef

- **UUID**: `ECUC:624b2048-16ec-4408-85dc-a82a5c93e09c`
- **引用名**: `CanIfHrhCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HRH belongs to. A controller can contain one or more HRHs.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfHrhCanHandleTypeRef

- **UUID**: `ECUC:84efc600-5948-407e-9a17-57f955f0691c`
- **引用名**: `CanIfHrhCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CAN Driver Module configuration. The type of the HRH can either be Full-CAN or Basic-CAN. The type of HRHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object. If BasicCAN is configured, software filtering is enabled.

########## 2. CanIfHrhIdSymRef

- **UUID**: `ECUC:1fbf0d02-5160-4182-b3bd-488d490d9c7a`
- **引用名**: `CanIfHrhIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

############ 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########### ENUMERATION 类型参数

############ 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

####### 4. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########## 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

######### ENUMERATION 类型参数

########## 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

####### 5. CanIfHthCfg

**容器属性**:

- **UUID**: `ECUC:5e0633ce-3473-4f6e-b7d5-51210b9247ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHthCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains parameters related to each HTH.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfHthCanCtrlIdRef

- **UUID**: `ECUC:698f1110-fa03-4dd0-9eb2-035e074c3e3d`
- **引用名**: `CanIfHthCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HTH belongs to. A controller can contain one or more HTHs.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfHthCanHandleTypeRef

- **UUID**: `ECUC:152513ea-515c-43da-9810-5e249ee4bf1e`
- **引用名**: `CanIfHthCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CAN Driver Module configuration. The type of the HTH can either be Full-CAN or Basic-CAN. The type of HTHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object.

########## 2. CanIfHthIdSymRef

- **UUID**: `ECUC:993e2b0d-53d4-43e5-9ef8-3dffe7bcd33b`
- **引用名**: `CanIfHthIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

####### 6. CanIfRxPduCfg

**容器属性**:

- **UUID**: `ECUC:35904777-ce11-4a2b-afb3-88cc26d0aff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of each receive CAN L-PDU.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. CanIfRxPduCanId

- **UUID**: `ECUC:2db03b9b-a549-4a9e-bf76-578d1cf85678`
- **参数名**: `CanIfRxPduCanId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of Receive CAN L-PDUs used by the CAN Interface. Exa: Software Filtering. This parameter is used if exactly one Can Identifier is assigned to the Pdu. If a range is assigned then the CanIfRxPduCanIdRange parameter shall be used.

########## 2. CanIfRxPduDlc

- **UUID**: `ECUC:53e64697-6612-4c0c-80f4-25f5a9bd40d7`
- **参数名**: `CanIfRxPduDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length code of received CAN L-PDUs used by the CAN Interface. Exa: DLC check.

########## 3. CanIfRxPduId

- **UUID**: `ECUC:c80d7823-4185-4880-b74b-37aa9539864c`
- **参数名**: `CanIfRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for receive CAN L-PDU. The CanIfRxPduId is configurable at pre-compile and post-built time. It shall fulfill ANSI/AUTOSAR definitions for constant defines.

######### BOOLEAN 类型参数

########## 1. CanIfRxPduReadData

- **UUID**: `ECUC:033f6abe-47aa-459b-8fc6-188490b334a5`
- **参数名**: `CanIfRxPduReadData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the Rx buffering for reading of received L-PDU data.

########## 2. CanIfRxPduReadNotifyStatus

- **UUID**: `ECUC:d5c19c95-670e-4b7f-a56c-cf2f455409ba`
- **参数名**: `CanIfRxPduReadNotifyStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables receive indication for each receive CAN L-PDU for reading its notification status.

######### ENUMERATION 类型参数

########## 1. CanIfRxPduCanIdType

- **UUID**: `ECUC:b4e0eaf5-d039-4538-bb85-03228bf7a612`
- **参数名**: `CanIfRxPduCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_FD_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_NO_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_NO_FD_CAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of receive CAN L-PDUs used by the CAN Driver for CAN L-PDU reception.

########## 2. CanIfRxPduUserRxIndicationUL

- **UUID**: `ECUC:835e1440-d156-40fa-95df-59a1e9611bc5`
- **参数名**: `CanIfRxPduUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_NM` (来源: AUTOSAR_ECUC)
  - `CAN_TP` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
  - `J1939TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication

######### FUNCTION-NAME 类型参数

########## 1. CanIfRxPduUserRxIndicationName

- **UUID**: `ECUC:15d97844-3e67-4d9c-954e-4a9d5f077bc4`
- **参数名**: `CanIfRxPduUserRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfRxPduBswSchExclAreaIdRef

- **UUID**: `ECUC:5749eea5-4bf4-4055-96b1-146d118d6f2f`
- **引用名**: `CanIfRxPduBswSchExclAreaIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswExclusiveAreaImpl`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance/RteBswExclusiveAreaImpl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an exclusive area Id defined within the BSW Scheduler.

########## 2. CanIfRxPduHrhIdRef

- **UUID**: `ECUC:a7fc2ca7-7ef3-4285-b179-359afe3ea369`
- **引用名**: `CanIfRxPduHrhIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CanIfHrhCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfInitHohCfg/CanIfHrhCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HRH to which Rx L-PDU belongs to, is referred through this parameter.

########## 3. CanIfRxPduRef

- **UUID**: `ECUC:6ec97ca8-68cc-4aee-8f58-0955fd67cce5`
- **引用名**: `CanIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. CanIfRxPduCanIdRange

**容器属性**:

- **UUID**: `ECUC:4e391be4-9fc9-4eb0-9446-4c26dc19d1a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCanIdRange`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Optional container that allows to map a range of CAN Ids to one PduId.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. CanIfRxPduCanIdRangeLowerCanId

- **UUID**: `ECUC:c2e0f2db-8884-48ad-b435-c415923641fb`
- **参数名**: `CanIfRxPduCanIdRangeLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

############ 2. CanIfRxPduCanIdRangeUpperCanId

- **UUID**: `ECUC:0add622f-4049-4d75-80a6-d49bbef3c636`
- **参数名**: `CanIfRxPduCanIdRangeUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

######### 2. CanIfTTRxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:ff49ad92-d7b2-4951-85f0-3a14bea08dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTRxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanTTRxJoblistTimeMark

- **UUID**: `ECUC:6c211a8b-18cf-41b5-849d-67f232ff137d`
- **参数名**: `CanTTRxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced rx trigger. Value is given in cycle time. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanIfTTRxHwObjectTriggerIdRef

- **UUID**: `ECUC:f7d39f69-3d75-4b01-95b9-6ff94ab8450f`
- **引用名**: `CanIfTTRxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware receive object Trigger of a hardware object in the TTCAN Driver Module,  which is referred via plain CAN parameter CANIF_HRH_HANDLETYPE_REF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

####### 7. CanIfRxPduCanIdRange

**容器属性**:

- **UUID**: `ECUC:4e391be4-9fc9-4eb0-9446-4c26dc19d1a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCanIdRange`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Optional container that allows to map a range of CAN Ids to one PduId.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanIfRxPduCanIdRangeLowerCanId

- **UUID**: `ECUC:c2e0f2db-8884-48ad-b435-c415923641fb`
- **参数名**: `CanIfRxPduCanIdRangeLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

########## 2. CanIfRxPduCanIdRangeUpperCanId

- **UUID**: `ECUC:0add622f-4049-4d75-80a6-d49bbef3c636`
- **参数名**: `CanIfRxPduCanIdRangeUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

####### 8. CanIfTTRxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:ff49ad92-d7b2-4951-85f0-3a14bea08dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTRxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTTRxJoblistTimeMark

- **UUID**: `ECUC:6c211a8b-18cf-41b5-849d-67f232ff137d`
- **参数名**: `CanTTRxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced rx trigger. Value is given in cycle time. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfTTRxHwObjectTriggerIdRef

- **UUID**: `ECUC:f7d39f69-3d75-4b01-95b9-6ff94ab8450f`
- **引用名**: `CanIfTTRxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware receive object Trigger of a hardware object in the TTCAN Driver Module,  which is referred via plain CAN parameter CANIF_HRH_HANDLETYPE_REF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

####### 9. CanIfTxPduCfg

**容器属性**:

- **UUID**: `ECUC:fbae4c0d-ab4e-4c56-b9c6-e9c0f26634a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTxPduCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of a transmit CAN L-PDU. It has to be configured as often as a transmit CAN L-PDU is needed.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. CanIfTxPduCanId

- **UUID**: `ECUC:16f0cef0-b138-48c6-8afa-e89fbce39eca`
- **参数名**: `CanIfTxPduCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU transmission.

########## 2. CanIfTxPduDlc

- **UUID**: `ECUC:90884052-811a-4d7c-a071-e58bf6f26e25`
- **参数名**: `CanIfTxPduDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data length code (in bytes) of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU transmission.

########## 3. CanIfTxPduId

- **UUID**: `ECUC:c4a7fa6d-bcab-43c7-a46e-db0f7e5e5f8a`
- **参数名**: `CanIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for transmit CAN L-PDU. The CanIfTxPduId is configurable at pre-compile and post-built time.

######### BOOLEAN 类型参数

########## 1. CanIfTxPduPnFilterPdu

- **UUID**: `ECUC:8337463d-2539-45a5-9a20-c81e10305546`
- **参数名**: `CanIfTxPduPnFilterPdu`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CanIfPublicPnFilterSupport is enabled, by this parameter PDUs could be configured which will pass the CanIfPnFilter.

########## 2. CanIfTxPduReadNotifyStatus

- **UUID**: `ECUC:019d12d4-5a3d-44df-a3a4-467cf0674e1b`
- **参数名**: `CanIfTxPduReadNotifyStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables transmit confirmation for each transmit CAN L-PDU for reading its notification status.

######### ENUMERATION 类型参数

########## 1. CanIfTxPduCanIdType

- **UUID**: `ECUC:72a33032-3f7d-4524-9650-fc37d465decd`
- **参数名**: `CanIfTxPduCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_FD_CAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of CAN Identifier of the transmit CAN L-PDU used by the CAN Driver module for CAN L-PDU transmission.

########## 2. CanIfTxPduType

- **UUID**: `ECUC:9bee54f7-968d-4c20-98c6-cc78191209bd`
- **参数名**: `CanIfTxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC` (来源: AUTOSAR_ECUC)
  - `STATIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of each transmit CAN L-PDU.

########## 3. CanIfTxPduUserTxConfirmationUL

- **UUID**: `ECUC:5a98eb1e-b9af-441f-9726-b456b2d3c5a0`
- **参数名**: `CanIfTxPduUserTxConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_NM` (来源: AUTOSAR_ECUC)
  - `CAN_TP` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
  - `J1939TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the successfully transmitted CANTXPDUID has to be routed via the <User_TxConfirmation>.

######### FUNCTION-NAME 类型参数

########## 1. CanIfTxPduUserTxConfirmationName

- **UUID**: `ECUC:5d9ad8a6-ddcd-4e81-aae7-3c0b03321662`
- **参数名**: `CanIfTxPduUserTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfTxPduBswSchExclAreaIdRef

- **UUID**: `ECUC:5e265eee-1125-4812-9cce-4eb8fbb4eb1d`
- **引用名**: `CanIfTxPduBswSchExclAreaIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswExclusiveAreaImpl`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance/RteBswExclusiveAreaImpl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an exclusive area Id defined within the BSW Scheduler.

########## 2. CanIfTxPduBufferRef

- **UUID**: `ECUC:22c29721-2347-42d1-9d0f-5fdf9d5afd45`
- **引用名**: `CanIfTxPduBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfBufferCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfBufferCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configurable reference to a CanIf buffer configuration.

########## 3. CanIfTxPduRef

- **UUID**: `ECUC:cf0ea2f5-ea57-4256-a638-2c19b5c65fee`
- **引用名**: `CanIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanIfTTTxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:4e110edd-0521-4fe3-a213-8e2775651ecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTTxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. CanIfTTTxJoblistTimeMark

- **UUID**: `ECUC:a53187d3-37d7-469e-8a18-6bb564ded1bc`
- **参数名**: `CanIfTTTxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced tx frame trigger.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. CanIfTTTxHwObjectTriggerIdRef

- **UUID**: `ECUC:e97b8ed4-bfb6-4964-adc0-5dc3f80cd53d`
- **引用名**: `CanIfTTTxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware transmit object Trigger of a hardware object in the TTCAN Driver Module,

####### 10. CanIfTTTxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:4e110edd-0521-4fe3-a213-8e2775651ecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTTxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanIfTTTxJoblistTimeMark

- **UUID**: `ECUC:a53187d3-37d7-469e-8a18-6bb564ded1bc`
- **参数名**: `CanIfTTTxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced tx frame trigger.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfTTTxHwObjectTriggerIdRef

- **UUID**: `ECUC:e97b8ed4-bfb6-4964-adc0-5dc3f80cd53d`
- **引用名**: `CanIfTTTxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware transmit object Trigger of a hardware object in the TTCAN Driver Module,

##### 5. CanIfBufferCfg

**容器属性**:

- **UUID**: `ECUC:2541ff9b-ca8a-4388-b3e9-4e893a369d4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfBufferCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the Txbuffer configuration. Multiple buffers with different sizes could be configured. If CanIfBufferSize (CANIF834_Conf) equals 0, the CanIf Tx L-PDU only refers via this CanIfBufferCfg the corresponding CanIfHthCfg.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanIfBufferSize

- **UUID**: `ECUC:3e890c54-df3d-4d91-bee8-0f6ee7a81053`
- **参数名**: `CanIfBufferSize`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the number of CanIf Tx L-PDUs which can be buffered in one Txbuffer. If this value equals 0, the CanIf does not perform Txbuffering for the CanIf Tx L-PDUs which are assigned to this Txbuffer. If CanIfPublicTxBuffering equals False, this parameter equals 0 for all TxBuffer. If the CanHandleType of the referred HTH equals FULL, this parameter equals 0 for this TxBuffer.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfBufferHthRef

- **UUID**: `ECUC:fb6c787d-41aa-4920-8680-030a0a2e8bc2`
- **引用名**: `CanIfBufferHthRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CanIfHthCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfInitHohCfg/CanIfHthCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to HTH, that defines the hardware object or the pool of hardware objects configured for transmission. All the CanIf Tx L-PDUs refer via the CanIfBufferCfg and this parameter to the HTHs if TxBuffering is enabled, or not.

##### 6. CanIfInitHohCfg

**容器属性**:

- **UUID**: `ECUC:c2f0d182-e8ee-4d61-8286-d2eeadc94428`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfInitHohCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the references to the configuration setup of each underlying CAN Driver.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfInitRefCfgSet

- **UUID**: `ECUC:71d02940-8e9e-4d69-94d7-09050c8d2a9a`
- **引用名**: `CanIfInitRefCfgSet`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanConfigSet`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the CAN Interface specific configuration setup. This type of external data structure shall contain the post build initialization data for the CAN Interface for all underlying CAN Drivers.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. CanIfHrhCfg

**容器属性**:

- **UUID**: `ECUC:a98b1f9b-0224-4f3b-80fc-49dc63340626`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains configuration parameters for each hardware receive object (HRH).

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. CanIfHrhSoftwareFilter

- **UUID**: `ECUC:60990db4-406e-4792-9c8f-82ebf55557e6`
- **参数名**: `CanIfHrhSoftwareFilter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the hardware receive objects by using the HRH range/list from CAN Driver configuration to define, for which HRH a software filtering has to be performed at during receive processing.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfHrhCanCtrlIdRef

- **UUID**: `ECUC:624b2048-16ec-4408-85dc-a82a5c93e09c`
- **引用名**: `CanIfHrhCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HRH belongs to. A controller can contain one or more HRHs.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfHrhCanHandleTypeRef

- **UUID**: `ECUC:84efc600-5948-407e-9a17-57f955f0691c`
- **引用名**: `CanIfHrhCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CAN Driver Module configuration. The type of the HRH can either be Full-CAN or Basic-CAN. The type of HRHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object. If BasicCAN is configured, software filtering is enabled.

########## 2. CanIfHrhIdSymRef

- **UUID**: `ECUC:1fbf0d02-5160-4182-b3bd-488d490d9c7a`
- **引用名**: `CanIfHrhIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

############ 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########### ENUMERATION 类型参数

############ 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

####### 2. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########## 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

######### ENUMERATION 类型参数

########## 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

####### 3. CanIfHthCfg

**容器属性**:

- **UUID**: `ECUC:5e0633ce-3473-4f6e-b7d5-51210b9247ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHthCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains parameters related to each HTH.

######## 引用关系

此容器包含 **3** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfHthCanCtrlIdRef

- **UUID**: `ECUC:698f1110-fa03-4dd0-9eb2-035e074c3e3d`
- **引用名**: `CanIfHthCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HTH belongs to. A controller can contain one or more HTHs.

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfHthCanHandleTypeRef

- **UUID**: `ECUC:152513ea-515c-43da-9810-5e249ee4bf1e`
- **引用名**: `CanIfHthCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CAN Driver Module configuration. The type of the HTH can either be Full-CAN or Basic-CAN. The type of HTHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object.

########## 2. CanIfHthIdSymRef

- **UUID**: `ECUC:993e2b0d-53d4-43e5-9ef8-3dffe7bcd33b`
- **引用名**: `CanIfHthIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

##### 7. CanIfHrhCfg

**容器属性**:

- **UUID**: `ECUC:a98b1f9b-0224-4f3b-80fc-49dc63340626`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains configuration parameters for each hardware receive object (HRH).

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. CanIfHrhSoftwareFilter

- **UUID**: `ECUC:60990db4-406e-4792-9c8f-82ebf55557e6`
- **参数名**: `CanIfHrhSoftwareFilter`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the hardware receive objects by using the HRH range/list from CAN Driver configuration to define, for which HRH a software filtering has to be performed at during receive processing.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfHrhCanCtrlIdRef

- **UUID**: `ECUC:624b2048-16ec-4408-85dc-a82a5c93e09c`
- **引用名**: `CanIfHrhCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HRH belongs to. A controller can contain one or more HRHs.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanIfHrhCanHandleTypeRef

- **UUID**: `ECUC:84efc600-5948-407e-9a17-57f955f0691c`
- **引用名**: `CanIfHrhCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CAN Driver Module configuration. The type of the HRH can either be Full-CAN or Basic-CAN. The type of HRHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object. If BasicCAN is configured, software filtering is enabled.

######## 2. CanIfHrhIdSymRef

- **UUID**: `ECUC:1fbf0d02-5160-4182-b3bd-488d490d9c7a`
- **引用名**: `CanIfHrhIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HRH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

########## 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

######### ENUMERATION 类型参数

########## 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

##### 8. CanIfHrhRangeCfg

**容器属性**:

- **UUID**: `ECUC:ea579804-c8f4-484d-a3e7-da6a2b2e8e20`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHrhRangeCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Defines the parameters required for configurating multiple CANID ranges for a given same HRH.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. CanIfHrhRangeRxPduLowerCanId

- **UUID**: `ECUC:c7e748c7-9dca-45e2-b11a-67d270c02581`
- **参数名**: `CanIfHrhRangeRxPduLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

######## 2. CanIfHrhRangeRxPduUpperCanId

- **UUID**: `ECUC:a69ada24-f385-4751-96cd-05dd1b848ef5`
- **参数名**: `CanIfHrhRangeRxPduUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids shall pass the software filtering.

####### ENUMERATION 类型参数

######## 1. CanIfHrhRangeRxPduRangeCanIdType

- **UUID**: `ECUC:f99a4757-23c0-42fe-b751-733ccac9dc93`
- **参数名**: `CanIfHrhRangeRxPduRangeCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED` (来源: AUTOSAR_ECUC)
  - `STANDARD` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies whether a configured Range of CAN Ids shall only consider standard CAN Ids or extended CAN Ids.

##### 9. CanIfHthCfg

**容器属性**:

- **UUID**: `ECUC:5e0633ce-3473-4f6e-b7d5-51210b9247ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfHthCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains parameters related to each HTH.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfHthCanCtrlIdRef

- **UUID**: `ECUC:698f1110-fa03-4dd0-9eb2-035e074c3e3d`
- **引用名**: `CanIfHthCanCtrlIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfCtrlCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfCtrlDrvCfg/CanIfCtrlCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to controller Id to which the HTH belongs to. A controller can contain one or more HTHs.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanIfHthCanHandleTypeRef

- **UUID**: `ECUC:152513ea-515c-43da-9810-5e249ee4bf1e`
- **引用名**: `CanIfHthCanHandleTypeRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CAN Driver Module configuration. The type of the HTH can either be Full-CAN or Basic-CAN. The type of HTHs is defined in the CAN Driver Module and hence it is derived from CAN Driver Configuration of a Hardware Object.

######## 2. CanIfHthIdSymRef

- **UUID**: `ECUC:993e2b0d-53d4-43e5-9ef8-3dffe7bcd33b`
- **引用名**: `CanIfHthIdSymRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanHardwareObject`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The parameter refers to a particular HTH object in the CanDrv configuration (see CanHardwareObject CAN324_Conf).

##### 10. CanIfRxPduCfg

**容器属性**:

- **UUID**: `ECUC:35904777-ce11-4a2b-afb3-88cc26d0aff8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of each receive CAN L-PDU.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. CanIfRxPduCanId

- **UUID**: `ECUC:2db03b9b-a549-4a9e-bf76-578d1cf85678`
- **参数名**: `CanIfRxPduCanId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of Receive CAN L-PDUs used by the CAN Interface. Exa: Software Filtering. This parameter is used if exactly one Can Identifier is assigned to the Pdu. If a range is assigned then the CanIfRxPduCanIdRange parameter shall be used.

######## 2. CanIfRxPduDlc

- **UUID**: `ECUC:53e64697-6612-4c0c-80f4-25f5a9bd40d7`
- **参数名**: `CanIfRxPduDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data Length code of received CAN L-PDUs used by the CAN Interface. Exa: DLC check.

######## 3. CanIfRxPduId

- **UUID**: `ECUC:c80d7823-4185-4880-b74b-37aa9539864c`
- **参数名**: `CanIfRxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for receive CAN L-PDU. The CanIfRxPduId is configurable at pre-compile and post-built time. It shall fulfill ANSI/AUTOSAR definitions for constant defines.

####### BOOLEAN 类型参数

######## 1. CanIfRxPduReadData

- **UUID**: `ECUC:033f6abe-47aa-459b-8fc6-188490b334a5`
- **参数名**: `CanIfRxPduReadData`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the Rx buffering for reading of received L-PDU data.

######## 2. CanIfRxPduReadNotifyStatus

- **UUID**: `ECUC:d5c19c95-670e-4b7f-a56c-cf2f455409ba`
- **参数名**: `CanIfRxPduReadNotifyStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables receive indication for each receive CAN L-PDU for reading its notification status.

####### ENUMERATION 类型参数

######## 1. CanIfRxPduCanIdType

- **UUID**: `ECUC:b4e0eaf5-d039-4538-bb85-03228bf7a612`
- **参数名**: `CanIfRxPduCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_FD_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_NO_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_NO_FD_CAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of receive CAN L-PDUs used by the CAN Driver for CAN L-PDU reception.

######## 2. CanIfRxPduUserRxIndicationUL

- **UUID**: `ECUC:835e1440-d156-40fa-95df-59a1e9611bc5`
- **参数名**: `CanIfRxPduUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_NM` (来源: AUTOSAR_ECUC)
  - `CAN_TP` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
  - `J1939TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication

####### FUNCTION-NAME 类型参数

######## 1. CanIfRxPduUserRxIndicationName

- **UUID**: `ECUC:15d97844-3e67-4d9c-954e-4a9d5f077bc4`
- **参数名**: `CanIfRxPduUserRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>.

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfRxPduBswSchExclAreaIdRef

- **UUID**: `ECUC:5749eea5-4bf4-4055-96b1-146d118d6f2f`
- **引用名**: `CanIfRxPduBswSchExclAreaIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswExclusiveAreaImpl`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance/RteBswExclusiveAreaImpl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an exclusive area Id defined within the BSW Scheduler.

######## 2. CanIfRxPduHrhIdRef

- **UUID**: `ECUC:a7fc2ca7-7ef3-4285-b179-359afe3ea369`
- **引用名**: `CanIfRxPduHrhIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `CanIfHrhCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfInitHohCfg/CanIfHrhCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The HRH to which Rx L-PDU belongs to, is referred through this parameter.

######## 3. CanIfRxPduRef

- **UUID**: `ECUC:6ec97ca8-68cc-4aee-8f58-0955fd67cce5`
- **引用名**: `CanIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. CanIfRxPduCanIdRange

**容器属性**:

- **UUID**: `ECUC:4e391be4-9fc9-4eb0-9446-4c26dc19d1a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCanIdRange`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Optional container that allows to map a range of CAN Ids to one PduId.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanIfRxPduCanIdRangeLowerCanId

- **UUID**: `ECUC:c2e0f2db-8884-48ad-b435-c415923641fb`
- **参数名**: `CanIfRxPduCanIdRangeLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

########## 2. CanIfRxPduCanIdRangeUpperCanId

- **UUID**: `ECUC:0add622f-4049-4d75-80a6-d49bbef3c636`
- **参数名**: `CanIfRxPduCanIdRangeUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

####### 2. CanIfTTRxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:ff49ad92-d7b2-4951-85f0-3a14bea08dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTRxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanTTRxJoblistTimeMark

- **UUID**: `ECUC:6c211a8b-18cf-41b5-849d-67f232ff137d`
- **参数名**: `CanTTRxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced rx trigger. Value is given in cycle time. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfTTRxHwObjectTriggerIdRef

- **UUID**: `ECUC:f7d39f69-3d75-4b01-95b9-6ff94ab8450f`
- **引用名**: `CanIfTTRxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware receive object Trigger of a hardware object in the TTCAN Driver Module,  which is referred via plain CAN parameter CANIF_HRH_HANDLETYPE_REF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

##### 11. CanIfRxPduCanIdRange

**容器属性**:

- **UUID**: `ECUC:4e391be4-9fc9-4eb0-9446-4c26dc19d1a5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfRxPduCanIdRange`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Optional container that allows to map a range of CAN Ids to one PduId.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanIfRxPduCanIdRangeLowerCanId

- **UUID**: `ECUC:c2e0f2db-8884-48ad-b435-c415923641fb`
- **参数名**: `CanIfRxPduCanIdRangeLowerCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Lower CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

######## 2. CanIfRxPduCanIdRangeUpperCanId

- **UUID**: `ECUC:0add622f-4049-4d75-80a6-d49bbef3c636`
- **参数名**: `CanIfRxPduCanIdRangeUpperCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper CAN Identifier of a receive CAN L-PDU for identifier range definition, in which all CAN Ids are mapped to one PduId.

##### 12. CanIfTTRxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:ff49ad92-d7b2-4951-85f0-3a14bea08dc9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTRxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanTTRxJoblistTimeMark

- **UUID**: `ECUC:6c211a8b-18cf-41b5-849d-67f232ff137d`
- **参数名**: `CanTTRxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced rx trigger. Value is given in cycle time. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfTTRxHwObjectTriggerIdRef

- **UUID**: `ECUC:f7d39f69-3d75-4b01-95b9-6ff94ab8450f`
- **引用名**: `CanIfTTRxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware receive object Trigger of a hardware object in the TTCAN Driver Module,  which is referred via plain CAN parameter CANIF_HRH_HANDLETYPE_REF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

##### 13. CanIfTxPduCfg

**容器属性**:

- **UUID**: `ECUC:fbae4c0d-ab4e-4c56-b9c6-e9c0f26634a9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTxPduCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of a transmit CAN L-PDU. It has to be configured as often as a transmit CAN L-PDU is needed.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. CanIfTxPduCanId

- **UUID**: `ECUC:16f0cef0-b138-48c6-8afa-e89fbce39eca`
- **参数名**: `CanIfTxPduCanId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..536870911]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: CAN Identifier of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU transmission.

######## 2. CanIfTxPduDlc

- **UUID**: `ECUC:90884052-811a-4d7c-a071-e58bf6f26e25`
- **参数名**: `CanIfTxPduDlc`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Data length code (in bytes) of transmit CAN L-PDUs used by the CAN Driver for CAN L-PDU transmission.

######## 3. CanIfTxPduId

- **UUID**: `ECUC:c4a7fa6d-bcab-43c7-a46e-db0f7e5e5f8a`
- **参数名**: `CanIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4294967295]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: ECU wide unique, symbolic handle for transmit CAN L-PDU. The CanIfTxPduId is configurable at pre-compile and post-built time.

####### BOOLEAN 类型参数

######## 1. CanIfTxPduPnFilterPdu

- **UUID**: `ECUC:8337463d-2539-45a5-9a20-c81e10305546`
- **参数名**: `CanIfTxPduPnFilterPdu`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If CanIfPublicPnFilterSupport is enabled, by this parameter PDUs could be configured which will pass the CanIfPnFilter.

######## 2. CanIfTxPduReadNotifyStatus

- **UUID**: `ECUC:019d12d4-5a3d-44df-a3a4-467cf0674e1b`
- **参数名**: `CanIfTxPduReadNotifyStatus`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables transmit confirmation for each transmit CAN L-PDU for reading its notification status.

####### ENUMERATION 类型参数

######## 1. CanIfTxPduCanIdType

- **UUID**: `ECUC:72a33032-3f7d-4524-9650-fc37d465decd`
- **参数名**: `CanIfTxPduCanIdType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `EXTENDED_CAN` (来源: AUTOSAR_ECUC)
  - `EXTENDED_FD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_CAN` (来源: AUTOSAR_ECUC)
  - `STANDARD_FD_CAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of CAN Identifier of the transmit CAN L-PDU used by the CAN Driver module for CAN L-PDU transmission.

######## 2. CanIfTxPduType

- **UUID**: `ECUC:9bee54f7-968d-4c20-98c6-cc78191209bd`
- **参数名**: `CanIfTxPduType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DYNAMIC` (来源: AUTOSAR_ECUC)
  - `STATIC` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the type of each transmit CAN L-PDU.

######## 3. CanIfTxPduUserTxConfirmationUL

- **UUID**: `ECUC:5a98eb1e-b9af-441f-9726-b456b2d3c5a0`
- **参数名**: `CanIfTxPduUserTxConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CAN_NM` (来源: AUTOSAR_ECUC)
  - `CAN_TP` (来源: AUTOSAR_ECUC)
  - `CDD` (来源: AUTOSAR_ECUC)
  - `J1939TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the successfully transmitted CANTXPDUID has to be routed via the <User_TxConfirmation>.

####### FUNCTION-NAME 类型参数

######## 1. CanIfTxPduUserTxConfirmationName

- **UUID**: `ECUC:5d9ad8a6-ddcd-4e81-aae7-3c0b03321662`
- **参数名**: `CanIfTxPduUserTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This

###### 引用关系

此容器包含 **3** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfTxPduBswSchExclAreaIdRef

- **UUID**: `ECUC:5e265eee-1125-4812-9cce-4eb8fbb4eb1d`
- **引用名**: `CanIfTxPduBswSchExclAreaIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `RteBswExclusiveAreaImpl`
- **完整路径**: `/AUTOSAR/EcucDefs/Rte/RteBswModuleInstance/RteBswExclusiveAreaImpl`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an exclusive area Id defined within the BSW Scheduler.

######## 2. CanIfTxPduBufferRef

- **UUID**: `ECUC:22c29721-2347-42d1-9d0f-5fdf9d5afd45`
- **引用名**: `CanIfTxPduBufferRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanIfBufferCfg`
- **完整路径**: `/AUTOSAR/EcucDefs/CanIf/CanIfInitCfg/CanIfBufferCfg`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configurable reference to a CanIf buffer configuration.

######## 3. CanIfTxPduRef

- **UUID**: `ECUC:cf0ea2f5-ea57-4256-a638-2c19b5c65fee`
- **引用名**: `CanIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the "global" Pdu structure to allow harmonization of handle IDs in the COM-Stack.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanIfTTTxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:4e110edd-0521-4fe3-a213-8e2775651ecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTTxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. CanIfTTTxJoblistTimeMark

- **UUID**: `ECUC:a53187d3-37d7-469e-8a18-6bb564ded1bc`
- **参数名**: `CanIfTTTxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced tx frame trigger.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. CanIfTTTxHwObjectTriggerIdRef

- **UUID**: `ECUC:e97b8ed4-bfb6-4964-adc0-5dc3f80cd53d`
- **引用名**: `CanIfTTTxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware transmit object Trigger of a hardware object in the TTCAN Driver Module,

##### 14. CanIfTTTxFrameTriggering

**容器属性**:

- **UUID**: `ECUC:4e110edd-0521-4fe3-a213-8e2775651ecd`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTTxFrameTriggering`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. CanIfTTTxJoblistTimeMark

- **UUID**: `ECUC:a53187d3-37d7-469e-8a18-6bb564ded1bc`
- **参数名**: `CanIfTTTxJoblistTimeMark`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the point in time, when the joblist execution funciton (JLEF) shall be called for the referenced tx frame trigger.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. CanIfTTTxHwObjectTriggerIdRef

- **UUID**: `ECUC:e97b8ed4-bfb6-4964-adc0-5dc3f80cd53d`
- **引用名**: `CanIfTTTxHwObjectTriggerIdRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTTHardwareObjectTrigger`
- **完整路径**: `/AUTOSAR/EcucDefs/Can/CanConfigSet/CanHardwareObject/CanTTHardwareObjectTrigger`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter refers to a particular TTCAN hardware transmit object Trigger of a hardware object in the TTCAN Driver Module,

##### 15. CanIfPrivateCfg

**容器属性**:

- **UUID**: `ECUC:01e44938-bbb9-43e3-aebe-49b1e30f3619`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfPrivateCfg`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the private configuration (parameters) of the CAN Interface.

###### 参数配置

此容器包含 **3** 个参数：

####### BOOLEAN 类型参数

######## 1. CanIfPrivateDlcCheck

- **UUID**: `ECUC:9536b5c8-fdf5-47ae-8c8a-d74c2a2a28e6`
- **参数名**: `CanIfPrivateDlcCheck`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether the DLC check is supported.

######## 2. CanIfSupportTTCAN

- **UUID**: `ECUC:25a3bdb6-1fef-4c52-9fdb-c6a7b85e3d7c`
- **参数名**: `CanIfSupportTTCAN`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether TTCAN is supported.

####### ENUMERATION 类型参数

######## 1. CanIfPrivateSoftwareFilterType

- **UUID**: `ECUC:6cc3af1f-c6f0-4c59-b350-91e27d0e27f9`
- **参数名**: `CanIfPrivateSoftwareFilterType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BINARY` (来源: AUTOSAR_ECUC)
  - `INDEX` (来源: AUTOSAR_ECUC)
  - `LINEAR` (来源: AUTOSAR_ECUC)
  - `TABLE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects the desired software filter mechanism for reception only.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanIfTTGeneral

**容器属性**:

- **UUID**: `ECUC:21377386-cebf-4969-a0ce-c6ec4ac5a68e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTGeneral`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanIfTTMaxIsrDelay

- **UUID**: `ECUC:5f0125fa-613b-4f80-bdc3-6f44ea1d156b`
- **参数名**: `CanIfTTMaxIsrDelay`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum delay for the execution of the joblist execution function JLEF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

######### BOOLEAN 类型参数

########## 1. CanIfTTJoblist

- **UUID**: `ECUC:e2966695-ae7f-4e4d-8449-32cdc08be5ce`
- **参数名**: `CanIfTTJoblist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether TTCAN is processed via a joblist.

##### 16. CanIfTTGeneral

**容器属性**:

- **UUID**: `ECUC:21377386-cebf-4969-a0ce-c6ec4ac5a68e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTTGeneral`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container is only included and valid if TTCAN Interface SWS is used and TTCAN is enabled.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanIfTTMaxIsrDelay

- **UUID**: `ECUC:5f0125fa-613b-4f80-bdc3-6f44ea1d156b`
- **参数名**: `CanIfTTMaxIsrDelay`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum delay for the execution of the joblist execution function JLEF. This parameter is only configurable if a joblist is enabled by parameter CanIfTTJobList.

####### BOOLEAN 类型参数

######## 1. CanIfTTJoblist

- **UUID**: `ECUC:e2966695-ae7f-4e4d-8449-32cdc08be5ce`
- **参数名**: `CanIfTTJoblist`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether TTCAN is processed via a joblist.

##### 17. CanIfPublicCfg

**容器属性**:

- **UUID**: `ECUC:502a51ce-f751-4c9b-924e-ffbae9900c8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfPublicCfg`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the public configuration (parameters) of the CAN Interface.

###### 参数配置

此容器包含 **17** 个参数：

####### INTEGER 类型参数

######## 1. CanIfPublicNumberOfCanHwUnits

- **UUID**: `ECUC:c55459df-f3d5-43e0-9de7-b3661f752b8e`
- **参数名**: `CanIfPublicNumberOfCanHwUnits`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of served CAN hardware units.

####### BOOLEAN 类型参数

######## 1. CanIfPublicCancelTransmitSupport

- **UUID**: `ECUC:fee14bfa-eab6-48c7-866e-8859c924b34d`
- **参数名**: `CanIfPublicCancelTransmitSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable dummy API for upper layer modules which allows to request the cancellation of an I-PDU.

######## 2. CanIfPublicChangeBaudrateSupport

- **UUID**: `ECUC:3e8db06a-bfe0-4314-afbf-d4268b2e8ef4`
- **参数名**: `CanIfPublicChangeBaudrateSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable the API to change the baudrate of a CAN controller.

######## 3. CanIfPublicDevErrorDetect

- **UUID**: `ECUC:bda3c206-6356-44a5-b970-b4e664527452`
- **参数名**: `CanIfPublicDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the development error detection and notification mechanism.

######## 4. CanIfPublicMultipleDrvSupport

- **UUID**: `ECUC:35509619-6257-4662-ac03-646822b407e1`
- **参数名**: `CanIfPublicMultipleDrvSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects support for multiple CAN Drivers.

######## 5. CanIfPublicPnSupport

- **UUID**: `ECUC:fff9c277-fd5b-4ad8-abe0-0d37c399e744`
- **参数名**: `CanIfPublicPnSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects support of Partial Network features in CanIf.

######## 6. CanIfPublicReadRxPduDataApi

- **UUID**: `ECUC:e15b356a-4f8b-45fb-a300-3e94fdacf384`
- **参数名**: `CanIfPublicReadRxPduDataApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables / Disables the API CanIf_ReadRxPduData() for reading received L-PDU data.

######## 7. CanIfPublicReadRxPduNotifyStatusApi

- **UUID**: `ECUC:fa4c1be1-80a1-4f7a-a8bd-d3432310b57e`
- **参数名**: `CanIfPublicReadRxPduNotifyStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the API for reading the received L-PDU data.

######## 8. CanIfPublicReadTxPduNotifyStatusApi

- **UUID**: `ECUC:29f05183-12ad-4430-be8c-a14bee1b6fe2`
- **参数名**: `CanIfPublicReadTxPduNotifyStatusApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the API for reading the notification status of transmit and receive L-PDUs.

######## 9. CanIfPublicSetDynamicTxIdApi

- **UUID**: `ECUC:c24ab666-772e-460e-b1cc-36b17d5dc2fe`
- **参数名**: `CanIfPublicSetDynamicTxIdApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the API for reconfiguration of the CAN Identifier for each Transmit L-PDU.

######## 10. CanIfPublicTxBuffering

- **UUID**: `ECUC:389db7b3-a65d-45c4-975b-e3fcb0bcd720`
- **参数名**: `CanIfPublicTxBuffering`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the buffering of transmit L-PDUs (rejected by the CanDrv) within the CAN Interface module.

######## 11. CanIfPublicTxConfirmPollingSupport

- **UUID**: `ECUC:e6648967-6f80-4706-b518-0294ac4290c9`
- **参数名**: `CanIfPublicTxConfirmPollingSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable the API to poll for Tx Confirmation state.

######## 12. CanIfPublicVersionInfoApi

- **UUID**: `ECUC:0d9c523c-3ece-47aa-b2ad-2f68419e8511`
- **参数名**: `CanIfPublicVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables and disables the API  for reading the version information about the CAN Interface.

######## 13. CanIfPublicWakeupCheckValidByNM

- **UUID**: `ECUC:f40bc487-2f36-4863-8c3a-5359040783d5`
- **参数名**: `CanIfPublicWakeupCheckValidByNM`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: If enabled, only NM messages shall validate a detected wake-up event

######## 14. CanIfPublicWakeupCheckValidSupport

- **UUID**: `ECUC:51a2279f-2c49-4c87-be76-120819310d0a`
- **参数名**: `CanIfPublicWakeupCheckValidSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects support for wake up validation

####### STRING 类型参数

######## 1. CanIfPublicCddHeaderFile

- **UUID**: `ECUC:96734c03-ecd7-4feb-b393-997c0789cb13`
- **参数名**: `CanIfPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines header files for callback functions which shall be included in case of CDDs. Range of characters is 1.. 32.

####### ENUMERATION 类型参数

######## 1. CanIfPublicHandleTypeEnum

- **UUID**: `ECUC:067ae4bf-e18b-4359-bfc4-75b0b4b6e95a`
- **参数名**: `CanIfPublicHandleTypeEnum`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `UINT16` (来源: AUTOSAR_ECUC)
  - `UINT8` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter is used to configure the Can_HwHandleType. The Can_HwHandleType represents the hardware object handles of a CAN hardware unit. For CAN hardware units with more than 255 HW objects the extended range shall be used (UINT16).

##### 18. CanIfTrcvDrvCfg

**容器属性**:

- **UUID**: `ECUC:771f9925-1a46-450e-8781-b59e18884ef1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTrcvDrvCfg`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of all addressed CAN transceivers by each underlying CAN Transceiver Driver module. For each CAN transceiver Driver a seperate instance of this container shall be provided.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CanIfTrcvCfg

**容器属性**:

- **UUID**: `ECUC:cbf745e1-f2f4-44fa-8f5c-8b62c0aa1e7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTrcvCfg`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one addressed CAN transceiver by the underlying CAN Transceiver Driver module. For each CAN transceiver a seperate instance of this container has to be provided.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. CanIfTrcvId

- **UUID**: `ECUC:570cdbbe-8d21-4e58-8d5f-279580e40b03`
- **参数名**: `CanIfTrcvId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter abstracts from the CAN Transceiver Driver specific parameter Transceiver. Each transceiver of all connected CAN Transceiver Driver modules shall be assigned to one specific TransceiverId of the CanIf.

######### BOOLEAN 类型参数

########## 1. CanIfTrcvWakeupSupport

- **UUID**: `ECUC:a8aa0764-c417-48b3-8130-29ebadf1928e`
- **参数名**: `CanIfTrcvWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if a respective transceiver of the referenced CAN Transceiver Driver modules is queriable for wake up events.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. CanIfTrcvCanTrcvRef

- **UUID**: `ECUC:8254f029-a3a6-4174-b799-60a500098c1e`
- **引用名**: `CanIfTrcvCanTrcvRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CanTrcv/CanTrcvConfigSet/CanTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references to the logical handle of the underlying CAN

##### 19. CanIfTrcvCfg

**容器属性**:

- **UUID**: `ECUC:cbf745e1-f2f4-44fa-8f5c-8b62c0aa1e7c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CanIfTrcvCfg`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of one addressed CAN transceiver by the underlying CAN Transceiver Driver module. For each CAN transceiver a seperate instance of this container has to be provided.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. CanIfTrcvId

- **UUID**: `ECUC:570cdbbe-8d21-4e58-8d5f-279580e40b03`
- **参数名**: `CanIfTrcvId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter abstracts from the CAN Transceiver Driver specific parameter Transceiver. Each transceiver of all connected CAN Transceiver Driver modules shall be assigned to one specific TransceiverId of the CanIf.

####### BOOLEAN 类型参数

######## 1. CanIfTrcvWakeupSupport

- **UUID**: `ECUC:a8aa0764-c417-48b3-8130-29ebadf1928e`
- **参数名**: `CanIfTrcvWakeupSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines if a respective transceiver of the referenced CAN Transceiver Driver modules is queriable for wake up events.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. CanIfTrcvCanTrcvRef

- **UUID**: `ECUC:8254f029-a3a6-4174-b799-60a500098c1e`
- **引用名**: `CanIfTrcvCanTrcvRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `CanTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/CanTrcv/CanTrcvConfigSet/CanTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter references to the logical handle of the underlying CAN

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

1. **CanIf**
