# EthTSyn - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:17

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [EthTSyn](#ethtsyn)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. EthTSyn

#### 基本信息

- **UUID**: `627dd85d-46ff-4fcb-9dae-b2bfd55de964`
- **模块名称**: `EthTSyn`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the Synchronized Time-base Manager (StbM) module with respect to global time handling on Ethernet.

#### 版本历史

共有 **15** 个版本记录：

##### 1. 版本 1.00.00

- **发布日期**: 2014-09-24
- **发布者**: vislje

*此版本无详细变更记录*

##### 2. 版本 1.00.01

- **发布日期**: 2014-11-11
- **发布者**: vislje

**变更内容**:

##### 3. 版本 1.00.02

- **发布日期**: 2015-01-08
- **发布者**: vissem

**变更内容**:

##### 4. 版本 1.00.03

- **发布日期**: 2015-02-18
- **发布者**: vissem

**变更内容**:

##### 5. 版本 1.00.04

- **发布日期**: 2015-02-19
- **发布者**: vissem

**变更内容**:

##### 6. 版本 1.00.05

- **发布日期**: 2015-03-26
- **发布者**: vissem

**变更内容**:

##### 7. 版本 1.01.00

- **发布日期**: 2015-02-27
- **发布者**: vissem

**变更内容**:

##### 8. 版本 01.01.01

- **发布日期**: 2015-07-10
- **发布者**: vissem

**变更内容**:

##### 9. 版本 01.01.02

- **发布日期**: 2015-07-08
- **发布者**: vissem

**变更内容**:

##### 10. 版本 01.02.00

- **发布日期**: 2015-07-09
- **发布者**: vissem

**变更内容**:

##### 11. 版本 01.02.01

- **发布日期**: 2015-09-01
- **发布者**: vissem

**变更内容**:

##### 12. 版本 02.00.00

- **发布日期**: 2015-09-01
- **发布者**: vissem

**变更内容**:

##### 13. 版本 02.00.01

- **发布日期**: 2016-01-26
- **发布者**: vissem

**变更内容**:

##### 14. 版本 02.00.02

- **发布日期**: 2016-02-22
- **发布者**: vissem

**变更内容**:

##### 15. 版本 02.01.00

- **发布日期**: 2016-02-22
- **发布者**: vissem

**变更内容**:

#### 配置容器

本模块包含 **6** 个配置容器：

##### 1. EthTSynGeneral

**容器属性**:

- **UUID**: `a258f9cf-c87e-481e-ac20-324c15f93fef`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container holds the general parameters of the Ethernet-specific Synchronized Time-base Manager

###### 参数配置

此容器包含 **8** 个参数：

####### BOOLEAN 类型参数

######## 1. EthTSynDevErrorDetect

- **UUID**: `7d918638-3b1d-4dce-ae12-0baf3c4ca5f4`
- **参数名**: `EthTSynDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter switches the Development Error Detection and Notification ON or OFF.
true:	Development error detection is enabled.
false:	Development error detection is disabled.

Note: In general, the development error detection is recommended during pre-test phase. It is not recommended to enable the development error detection in production code due to increased runtime and ROM needs.

######## 2. EthTSynHardwareTimestampSupport

- **UUID**: `8c6d0fcd-aafe-437f-833d-d87f363de28d`
- **参数名**: `EthTSynHardwareTimestampSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Activate/Deactivate the hardware time stamping functionality of the Ethernet hardware. 
True: Clock is administrated by EthIf-Lower layer (e.g. Eth). Timestamps are requested from EthIf (e.g. EthIf_GetIngressTimestamp()) 
False: Clock is administrated by StbM, therefore timestamps are provided by the StbM.

######## 3. EthTSynVersionInfo

- **UUID**: `ef73f771-f5de-4b97-a8ba-96ce3d616b91`
- **参数名**: `EthTSynVersionInfo`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: Activate/Deactivate the version information API (EthTSyn_GetVersionInfo) to get major, minor and patch version information.
True: version information API activated 
False: version information API deactivated.

######## 4. EthTSynGmCapable

- **UUID**: `7548b071-a37e-49e1-9461-fdb4ca4fd77d`
- **参数名**: `EthTSynGmCapable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **描述**: Select whether the EthTSyn can act as Grand Master. In a bridge configuration, the ECU will take over the role of the GM in case a Sync-Timeout is detected on the Slave-Por

####### FLOAT 类型参数

######## 1. EthTSynMainFunctionPeriod

- **UUID**: `9fd56f11-928d-4310-96d3-e2031da6391a`
- **参数名**: `EthTSynMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.005`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Schedule period of the main function EthTSyn_MainFunction. Unit: [s].

####### STRING 类型参数

######## 1. EthTSynDestPhyAddr

- **UUID**: `7c67e6b3-ddbd-42fa-b641-cfa90a68a311`
- **参数名**: `EthTSynDestPhyAddr`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 默认值: `01:80:C2:00:00:0E`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Destination Physical Hardware Address (MAC-Address) of EthTSyn-gPTP Frames. Input format has to match xx::xx::xx::xx::xx::xx, where x stands for a hex value between 0 and F.

######## 2. EthTSynUserConfigFile

- **UUID**: `bc661a29-f070-464a-b45f-46e08859377a`
- **参数名**: `EthTSynUserConfigFile`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an external user configuration file that will be included during generation.
The content of the user configuration file will be added at the end of the generated module configuration file and allows altering or extending the generated code.
Caution: User configuration files can cause the software module to malfunction and must only be used with great care!

######## 3. EthTSynPublicCddHeaderFile

- **UUID**: `a438cb59-e7ed-4df1-b671-7357add8c814`
- **参数名**: `EthTSynPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: Vector Informatik
- **符号名值**: false
- **字符串变体**:
  - 最大长度: 32
  - 最小长度: 1
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines header files for call-back functions (e.g. Sync / FollowUp sent) which shall be included in case of CDDs. Range of characters is 1.. 32.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EthTSynEthIfFrameType

- **UUID**: `fb7b6805-4434-4706-bb86-adf0aa63b1f4`
- **引用名**: `EthTSynEthIfFrameType`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfFrameOwnerConfig`
- **完整路径**: `/MICROSAR/EthIf/EthIfConfigSet/EthIfFrameOwnerConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The chosen frame owner determines which frames (in respect to ethertype) are received.

##### 2. EthTSynGlobalTimeDomain

**容器属性**:

- **UUID**: `ea7c3071-1841-4467-b7c8-7bcc761329f6`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGlobalTimeDomain`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This represents the existence of a global time domain on Ethernet. The EthTSyn module can administrate several global time domains at the same time that in itself form a hierarchy of domains and sub-domains.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. EthTSynGlobalTimeDomainId

- **UUID**: `17baeae0-c720-4952-ba54-cb53c7467639`
- **参数名**: `EthTSynGlobalTimeDomainId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `0`
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The global time domain ID.

####### BOOLEAN 类型参数

######## 1. EthTSynBridgeKeepSourcePortIdentity

- **UUID**: `ea0d5919-e83e-4b60-b61c-3e63f5e58cb9`
- **参数名**: `EthTSynBridgeKeepSourcePortIdentity`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **描述**: This parameter is only used in a bridge configuration.

When this parameter is enabled, the source port identity of forwarded Sync/FollowUp messages is not modified.

####### FLOAT 类型参数

######## 1. EthTSynGlobalTimeFollowUpTimeout

- **UUID**: `6c55b223-1b24-4988-849c-b273172e0a34`
- **参数名**: `EthTSynGlobalTimeFollowUpTimeout`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `0.125`
- **取值范围**: [0..1.7976931348623157E+308]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the time waited for the reception of a FollowUp message after receiving a Sync message. After the Timeout the Sync message will be discarded. Unit: seconds

######## 2. EthTSynGlobalTimeSyncTimeout

- **UUID**: `f84c9461-8e4e-4717-b89f-c529908cd5cf`
- **参数名**: `EthTSynGlobalTimeSyncTimeout`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **默认值**: `0.25`
- **取值范围**: [0..255]
- **来源**: Vector Informatik
- **符号名值**: false
- **描述**: This parameter is only used in a Bridge configuration. It specifies the time, the bridge is waiting for the reception of a new Sync message on its slave port before a Grand Master timeout is assumed and the Bridge begins to generate its own Sync and FollowUp messages.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. EthTSynTimeSourceRef

- **UUID**: `5ad6b517-af0d-4d2a-a549-6148f661a47e`
- **引用名**: `EthTSynTimeSourceRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthTSynTimeSourceConfig`
- **完整路径**: `/MICROSAR/EthTSyn/EthTSynTimeSourceConfig`
- **来源**: Vector Informatik
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Refernece to the Time Source which will be used for the TimeDomain.

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. EthTSynSynchronizedTimeBaseRef

- **UUID**: `1b6287ba-bceb-43e3-b897-f8f3bb03edca`
- **引用名**: `EthTSynSynchronizedTimeBaseRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `StbMSynchronizedTimeBase`
- **完整路径**: `/AUTOSAR/EcucDefs/StbM/StbMSynchronizedTimeBase`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional reference to the synchronized time-base.
The refernece is only used when a TimeSource with STBM_TIMESTAMPING as TimestampMethdo is used.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. EthTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `ECUC:20d1e409-b2eb-4086-bbe6-0525aff7c21c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGlobalTimeMaster`
- **多重性**: [0..1]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. EthTSynGlobalTimeTxFollowUpOffset

- **UUID**: `ECUC:144256e5-4ef8-8799-714a-f1273c3b0ee6`
- **参数名**: `EthTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages. Unit: seconds

########## 2. EthTSynGlobalTimeTxPdelayReqPeriod

- **UUID**: `ECUC:20432b32-7ee2-81fc-6476-e8f0ef2d1ef4`
- **参数名**: `EthTSynGlobalTimeTxPdelayReqPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds

########## 3. EthTSynGlobalTimeTxPeriod

- **UUID**: `ECUC:895a28b4-2c4e-4b59-ac47-70aadc1de237`
- **参数名**: `EthTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period. Unit: seconds

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthTSynGlobalTimeEthIfRef

- **UUID**: `ECUC:c6496c14-1aaf-8d15-615b-86889b88b373`
- **引用名**: `EthTSynGlobalTimeEthIfRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Ethernet interface taken to fetch the global time information.

####### 2. EthTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `ECUC:06ad6036-fb6a-450e-a8c1-7509babd6012`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

Configuration of a time slave. Each global time domain is required to have at least one time slave. The configured ECU may or may not represent a time slave.

######## 参数配置

此容器包含 **3** 个参数：

######### FLOAT 类型参数

########## 1. EthTSynGlobalTimeTxFollowUpOffset

- **UUID**: `ECUC:fa1dd312-9777-8c21-5e26-610b4700acdc`
- **参数名**: `EthTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages. Unit: seconds

########## 2. EthTSynGlobalTimeTxPdelayReqPeriod

- **UUID**: `ECUC:061ea75f-c761-8684-5152-58d4f9f2bcea`
- **参数名**: `EthTSynGlobalTimeTxPdelayReqPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds

########## 3. EthTSynTimeHardwareCorrectionThreshold

- **UUID**: `ECUC:b7b5155b-b081-440e-9987-7ec76ab8e9d9`
- **参数名**: `EthTSynTimeHardwareCorrectionThreshold`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter can be taken to define the maximum deviation between the local time and the time obtained from SYNC message that triggers a correction of the time drift caused by the hardware on the local node.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. EthTSynGlobalTimeEthIfRef

- **UUID**: `ECUC:ac24e841-632e-919d-4e36-f66ca64e5169`
- **引用名**: `EthTSynGlobalTimeEthIfRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Ethernet interface taken to fetch the global time information.

##### 3. EthTSynGlobalTimeMaster

**容器属性**:

- **UUID**: `ECUC:20d1e409-b2eb-4086-bbe6-0525aff7c21c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGlobalTimeMaster`
- **多重性**: [0..1]

**容器描述**:

Configuration of the global time master. Each global time domain is required to have exactly one global time master. This master may or may not exist on the configured ECU.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. EthTSynGlobalTimeTxFollowUpOffset

- **UUID**: `ECUC:144256e5-4ef8-8799-714a-f1273c3b0ee6`
- **参数名**: `EthTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages. Unit: seconds

######## 2. EthTSynGlobalTimeTxPdelayReqPeriod

- **UUID**: `ECUC:20432b32-7ee2-81fc-6476-e8f0ef2d1ef4`
- **参数名**: `EthTSynGlobalTimeTxPdelayReqPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds

######## 3. EthTSynGlobalTimeTxPeriod

- **UUID**: `ECUC:895a28b4-2c4e-4b59-ac47-70aadc1de237`
- **参数名**: `EthTSynGlobalTimeTxPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period. Unit: seconds

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EthTSynGlobalTimeEthIfRef

- **UUID**: `ECUC:c6496c14-1aaf-8d15-615b-86889b88b373`
- **引用名**: `EthTSynGlobalTimeEthIfRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Ethernet interface taken to fetch the global time information.

##### 4. EthTSynGlobalTimeSlave

**容器属性**:

- **UUID**: `ECUC:06ad6036-fb6a-450e-a8c1-7509babd6012`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynGlobalTimeSlave`
- **多重性**: [0..1]

**容器描述**:

Configuration of a time slave. Each global time domain is required to have at least one time slave. The configured ECU may or may not represent a time slave.

###### 参数配置

此容器包含 **3** 个参数：

####### FLOAT 类型参数

######## 1. EthTSynGlobalTimeTxFollowUpOffset

- **UUID**: `ECUC:fa1dd312-9777-8c21-5e26-610b4700acdc`
- **参数名**: `EthTSynGlobalTimeTxFollowUpOffset`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX offset for Follow_Up / Pdelay_Resp_Follow_Up messages. Unit: seconds

######## 2. EthTSynGlobalTimeTxPdelayReqPeriod

- **UUID**: `ECUC:061ea75f-c761-8684-5152-58d4f9f2bcea`
- **参数名**: `EthTSynGlobalTimeTxPdelayReqPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This represents configuration of the TX period for Pdelay_Req messages. Unit: seconds

######## 3. EthTSynTimeHardwareCorrectionThreshold

- **UUID**: `ECUC:b7b5155b-b081-440e-9987-7ec76ab8e9d9`
- **参数名**: `EthTSynTimeHardwareCorrectionThreshold`
- **数据类型**: FLOAT
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **描述**: This parameter can be taken to define the maximum deviation between the local time and the time obtained from SYNC message that triggers a correction of the time drift caused by the hardware on the local node.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. EthTSynGlobalTimeEthIfRef

- **UUID**: `ECUC:ac24e841-632e-919d-4e36-f66ca64e5169`
- **引用名**: `EthTSynGlobalTimeEthIfRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `EthIfController`
- **完整路径**: `/AUTOSAR/EcucDefs/EthIf/EthIfConfigSet/EthIfController`
- **来源**: AUTOSAR_ECUC
- **描述**: This represents the reference to the Ethernet interface taken to fetch the global time information.

##### 5. EthTSynTimeSourceConfig

**容器属性**:

- **UUID**: `233c922e-e57a-4479-8c57-4a710e54102b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynTimeSourceConfig`
- **多重性**: [1..infinite]

**容器描述**:

Configuration of the Time Sources used by the EthTSyn module

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. EthTSynTimestampMethod

- **UUID**: `e98bd81f-ccdd-476b-a502-af659ed3c16e`
- **参数名**: `EthTSynTimestampMethod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **默认值**: `HW_TIMESTAMPING`
- **来源**: Vector Informatik
- **符号名值**: false
- **可选值**:
  - `HW_TIMESTAMPING` (来源: FEAT-1268: SW-Timestamp support)
  - `STBM_TIMESTAMPING` (来源: FEAT-1268: SW-Timestamp support)
  - `GPT_TIMESTAMPING` (来源: FEAT-1268: SW-Timestamp support)
  - `OS_TIMESTAMPING` (来源: FEAT-1268: SW-Timestamp support)
  - `CALLOUT_TIMESTAMPING` (来源: FEAT-1268: SW-Timestamp support)
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Select which timestamping method is used.
HW_TIMESTAMPING:
- Clock is managed in HW

STBM_TIMESTAMPING:
- Clock is managed in StbM

OS/GPT/CALLOUT_TIMESTAMPING:
- Clock is managed in EthTSyn
- Local Time is derived from Os/Gpt Counter or from UserCallout

###### 引用关系

此容器包含 **1** 个引用：

####### CHOICE-REFERENCE 类型引用

######## 1. EthTSynTimeBaseRef

- **UUID**: `accdb8c3-3244-4eba-aa83-059df00d703c`
- **引用名**: `EthTSynTimeBaseRef`
- **引用类型**: CHOICE-REFERENCE
- **多重性**: [0..1]
- **来源**: Vector Informatik
- **目标引用列表**:
  - `/AUTOSAR/EcucDefs/Os/OsCounter`
  - `/AUTOSAR/EcucDefs/Gpt/GptChannelConfigSet/GptChannelConfiguration`
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Counter/EthIfController used as Time base.

This parameter is only used if EthTSynTImestampMethod is set to:
GPT_TIMESTAMPING
OS_TIMESTAMPING

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. EthTSynTimestampCalloutConfig

**容器属性**:

- **UUID**: `884a38a6-cc65-41b0-9a37-43644eb67560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynTimestampCalloutConfig`
- **多重性**: [0..1]

**容器描述**:

Configuration of Timestamp Usercallout.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. EthTSynUserCalloutMaxValue

- **UUID**: `056b41cf-1e7b-4372-9c8c-695d90ac37a3`
- **参数名**: `EthTSynUserCalloutMaxValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1000000000`
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max Tick Value returned by the Usercallout.

######### FLOAT 类型参数

########## 1. EthTSynUserCalloutNsPerTick

- **UUID**: `a4cc02f0-c5d7-4e79-a54c-6c77ab82ba6c`
- **参数名**: `EthTSynUserCalloutNsPerTick`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1000000000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time of one "Tick" (returned by the Usercallout) in Nanoseconds.

######### STRING 类型参数

########## 1. EthTSynUserIncludeFile

- **UUID**: `e1e1bab4-7bdc-4d7f-8917-37df3a25176b`
- **参数名**: `EthTSynUserIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a header file name which shall be included by EthTSyn for the Timestamp UserCallout.

######### FUNCTION-NAME 类型参数

########## 1. EthTSynTimestampUserCallout

- **UUID**: `ec1ead39-ad3f-4ea5-96dd-2b26deb5b5c0`
- **参数名**: `EthTSynTimestampUserCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the User-Callout function when Timestamp Method is set to "CALLOUT-TIMESTAMPING".
This Function is called when EthTSyn_GetCurrentTimeRaw is invoked.
The Callout-function has the following signature:

Std_ReturnType TimestampUserCallout(EthTSyn_TimestampTickType *CurrentTickTime)

The function shall return "E_OK" when the retrieval of the Time was successful and "E_NOT_OK" otherwise.

##### 6. EthTSynTimestampCalloutConfig

**容器属性**:

- **UUID**: `884a38a6-cc65-41b0-9a37-43644eb67560`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `EthTSynTimestampCalloutConfig`
- **多重性**: [0..1]

**容器描述**:

Configuration of Timestamp Usercallout.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. EthTSynUserCalloutMaxValue

- **UUID**: `056b41cf-1e7b-4372-9c8c-695d90ac37a3`
- **参数名**: `EthTSynUserCalloutMaxValue`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **默认值**: `1000000000`
- **取值范围**: [1..4294967296]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Max Tick Value returned by the Usercallout.

####### FLOAT 类型参数

######## 1. EthTSynUserCalloutNsPerTick

- **UUID**: `a4cc02f0-c5d7-4e79-a54c-6c77ab82ba6c`
- **参数名**: `EthTSynUserCalloutNsPerTick`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **默认值**: `1`
- **取值范围**: [1..1000000000]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Time of one "Tick" (returned by the Usercallout) in Nanoseconds.

####### STRING 类型参数

######## 1. EthTSynUserIncludeFile

- **UUID**: `e1e1bab4-7bdc-4d7f-8917-37df3a25176b`
- **参数名**: `EthTSynUserIncludeFile`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines a header file name which shall be included by EthTSyn for the Timestamp UserCallout.

####### FUNCTION-NAME 类型参数

######## 1. EthTSynTimestampUserCallout

- **UUID**: `ec1ead39-ad3f-4ea5-96dd-2b26deb5b5c0`
- **参数名**: `EthTSynTimestampUserCallout`
- **数据类型**: FUNCTION-NAME
- **多重性**: [1..1]
- **来源**: Vector Informatik
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Name of the User-Callout function when Timestamp Method is set to "CALLOUT-TIMESTAMPING".
This Function is called when EthTSyn_GetCurrentTimeRaw is invoked.
The Callout-function has the following signature:

Std_ReturnType TimestampUserCallout(EthTSyn_TimestampTickType *CurrentTickTime)

The function shall return "E_OK" when the retrieval of the Time was successful and "E_NOT_OK" otherwise.

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

1. **EthTSyn**
