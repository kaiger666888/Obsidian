# FrIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:20

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [FrIf](#frif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. FrIf

#### 基本信息

- **UUID**: `ECUC:bcc30adc-d050-43fb-a38e-aee2c3e3abaf`
- **模块名称**: `FrIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the FrIf (FlexRay Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **18** 个配置容器：

##### 1. FrIfConfig

**容器属性**:

- **UUID**: `ECUC:0d627762-ad82-4f1b-91b1-20185e6a5a31`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

Configuration of the FlexRay Interface. This container is a MultipleConfigurationContainer, i.e. this container and its sub-containers exist once per configuration set.

###### 配置容器

本模块包含 **16** 个配置容器：

####### 1. FrIfCluster

**容器属性**:

- **UUID**: `ECUC:9c2eb2ed-9528-45d7-a875-28de20a06488`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCluster`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies a FrIf Cluster and all related data which is required to enable communication of the Cluster. A Cluster may consist of more than one Controller.

######## 参数配置

此容器包含 **37** 个参数：

######### INTEGER 类型参数

########## 1. FrIfClstIdx

- **UUID**: `ECUC:acba36f8-adeb-4c36-98e4-837e0f616935`
- **参数名**: `FrIfClstIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Clusters. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay Cluster.

########## 2. FrIfGColdStartAttempts

- **UUID**: `ECUC:fd06e4ae-2179-4ce0-855c-f4aa7f03b3b7`
- **参数名**: `FrIfGColdStartAttempts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of times a node in the cluster is permitted to attempt to start the cluster by initiating schedule synchronization

########## 3. FrIfGCycleCountMax

- **UUID**: `ECUC:5fd22705-bf85-4659-bf98-be6bfcc0abed`
- **参数名**: `FrIfGCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [7..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum cycle counter value in a given cluster.

########## 4. FrIfGListenNoise

- **UUID**: `ECUC:05659b06-1760-4f5a-af1f-35f0844d2a3a`
- **参数名**: `FrIfGListenNoise`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper limit for the start up listen timeout and wake up listen timeout in the presence of noise. It is used as a multiplier of the node

########## 5. FrIfGMacroPerCycle

- **UUID**: `ECUC:9b6b8aa9-7ad4-454b-a721-51641bb65c5b`
- **参数名**: `FrIfGMacroPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..16000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks in a communication cycle.

########## 6. FrIfGMaxWithoutClockCorrectFatal

- **UUID**: `ECUC:df1cf583-bf38-49a2-b150-95275930adf0`
- **参数名**: `FrIfGMaxWithoutClockCorrectFatal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of consecutive even/odd Cycle pairs with missing clock correction terms that will cause the protocol to transition from the POC:normal active or POC:normal passive state into the POC:halt state. [Even/odd cycle pairs].

########## 7. FrIfGMaxWithoutClockCorrectPassive

- **UUID**: `ECUC:9ab93616-b25c-4f80-aaa1-af10c35a2927`
- **参数名**: `FrIfGMaxWithoutClockCorrectPassive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of consecutive even/odd Cycle pairs with missing clock correction terms that will cause the protocol to transition from the POC:normal active state to the POC:normal passive state. [Even/Odd cycle pairs]

########## 8. FrIfGNetworkManagementVectorLength

- **UUID**: `ECUC:bbde5f64-38de-40ee-a656-1e4c515b3e38`
- **参数名**: `FrIfGNetworkManagementVectorLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..12]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Network Management vector in a cluster [bytes]

########## 9. FrIfGNumberOfMinislots

- **UUID**: `ECUC:d9f67d2c-e7dd-45f9-993e-3242ef59b478`
- **参数名**: `FrIfGNumberOfMinislots`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7988]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of minislots in the dynamic segment

########## 10. FrIfGNumberOfStaticSlots

- **UUID**: `ECUC:9210d68d-a1ee-436e-b951-3dc34765cb23`
- **参数名**: `FrIfGNumberOfStaticSlots`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of static slots in the static segment

########## 11. FrIfGPayloadLengthStatic

- **UUID**: `ECUC:7182990c-c42b-4d6a-a5ff-b542fcb4cd36`
- **参数名**: `FrIfGPayloadLengthStatic`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Payload length of a static frame [16 bit words]

########## 12. FrIfGSyncFrameIDCountMax

- **UUID**: `ECUC:f38bcebd-b881-4dac-9af7-53dcc1c26961`
- **参数名**: `FrIfGSyncFrameIDCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of distinct syncframe identifiers present in a  given cluster. This parameter maps to FlexRay Protocol 2.1 Rev. A parameter gSyncNodeMax.

########## 13. FrIfGdActionPointOffset

- **UUID**: `ECUC:7dad1bd0-f203-45cf-bed2-b8c487b27c60`
- **参数名**: `FrIfGdActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks the action point is offset from the beginning of a static slot.

########## 14. FrIfGdCasRxLowMax

- **UUID**: `ECUC:8e414515-2806-468b-810d-a2a0345e8757`
- **参数名**: `FrIfGdCasRxLowMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [28..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper limit of the CAS acceptance windows [gdBit]

########## 15. FrIfGdDynamicSlotIdlePhase

- **UUID**: `ECUC:36b405ab-0c5a-4b1e-b055-03cff003fc6d`
- **参数名**: `FrIfGdDynamicSlotIdlePhase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the idle phase within a dynamic slot [Minislots].

########## 16. FrIfGdIgnoreAfterTx

- **UUID**: `ECUC:55227fbf-ff62-4f17-86eb-fb3be77f6517`
- **参数名**: `FrIfGdIgnoreAfterTx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration for which the bitstrobing is paused after transmission [gdBit].

########## 17. FrIfGdMiniSlotActionPointOffset

- **UUID**: `ECUC:b31a710c-5b2f-41a2-8861-3902a6b62530`
- **参数名**: `FrIfGdMiniSlotActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Macroticks the Minislot action point is offset from the beginning of a Minislot [Macroticks].

########## 18. FrIfGdMinislot

- **UUID**: `ECUC:d925ca4b-2c55-4554-9e82-cb7e117367e7`
- **参数名**: `FrIfGdMinislot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a minislot [Macroticks]

########## 19. FrIfGdNit

- **UUID**: `ECUC:8d38067a-6d89-4e82-9dd2-28af28190db3`
- **参数名**: `FrIfGdNit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..15978]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the Network Idle Time [Macroticks]

########## 20. FrIfGdStaticSlot

- **UUID**: `ECUC:86eef347-5af3-44b5-ac4a-e799aed9ac97`
- **参数名**: `FrIfGdStaticSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [3..664]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a static slot [Macroticks].

########## 21. FrIfGdSymbolWindow

- **UUID**: `ECUC:3168f855-09f2-4dab-bbad-e53571fb477e`
- **参数名**: `FrIfGdSymbolWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..162]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the symbol window [Macroticks].

########## 22. FrIfGdSymbolWindowActionPointOffset

- **UUID**: `ECUC:c828edea-75dd-496a-92f9-4a69eb5279d8`
- **参数名**: `FrIfGdSymbolWindowActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks the action point offset is from the beginning of the symbol window [Macroticks].

########## 23. FrIfGdTSSTransmitter

- **UUID**: `ECUC:cd257190-952b-419a-8536-ff98206ba70a`
- **参数名**: `FrIfGdTSSTransmitter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits in the Transmission Start Sequence [gdBits].

########## 24. FrIfGdWakeupRxIdle

- **UUID**: `ECUC:5700e5c3-21b8-492e-a15a-e7b9f8890a47`
- **参数名**: `FrIfGdWakeupRxIdle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..59]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to test the duration of the 'idle' or HIGH phase of a received wakeup [gdBit]. Remarks: This parameter maps to FlexRay Protocol 2.1 Rev. A parameter gdWakeupSymbolRxIdle. Lower limit 14 for FlexRay Protocol 2.1 Rev. A compliance.

########## 25. FrIfGdWakeupRxLow

- **UUID**: `ECUC:49d8c5b9-e6ee-495e-8f08-214b329352ae`
- **参数名**: `FrIfGdWakeupRxLow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..59]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to test the duration of the LOW phase of a received wakeup [gdBit].

########## 26. FrIfGdWakeupRxWindow

- **UUID**: `ECUC:02c38e9b-73e1-4d76-b72b-cd837212b26b`
- **参数名**: `FrIfGdWakeupRxWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [76..485]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The size of the window used to detect wakeups [gdBit].

########## 27. FrIfGdWakeupTxActive

- **UUID**: `ECUC:87fda236-4246-4548-b42e-a2bb02e6842f`
- **参数名**: `FrIfGdWakeupTxActive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [15..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to transmit the LOW phase of awakeup symbol and  the HIGH and LOW phases of a WUDOP [gdBit].

########## 28. FrIfGdWakeupTxIdle

- **UUID**: `ECUC:5e28082c-931c-43e2-9d26-58297c3c9457`
- **参数名**: `FrIfGdWakeupTxIdle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [45..180]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to transmit the 'idle' part of a

########## 29. FrIfMaxIsrDelay

- **UUID**: `ECUC:336dfed2-bd0c-41a6-977d-eeda4d0431b6`
- **参数名**: `FrIfMaxIsrDelay`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum delay in macroticks the FrIf_JoblistExec_<cluster>() function is processed after the absolute timer interrupt was triggered.

########## 30. FrIfSafetyMargin

- **UUID**: `ECUC:2263fb3c-0a7b-44bd-b166-315865d5e4ee`
- **参数名**: `FrIfSafetyMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Additional timespan in macroticks which takes jitter into account to be able to set the JobListPointer to the next possible job which can be executed in case the FlexRay Job List Execution Function has be resynchronized.

######### BOOLEAN 类型参数

########## 1. FrIfDetectNITError

- **UUID**: `ECUC:cb95f335-435b-40cf-b7fd-5279da55e4a3`
- **参数名**: `FrIfDetectNITError`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether NIT error status of each cluster shall be detected or not.

######### FLOAT 类型参数

########## 1. FrIfGdCycle

- **UUID**: `ECUC:ef2961ff-251f-429b-abc4-31886a5e4554`
- **参数名**: `FrIfGdCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [2.4E-5..0.016]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the cycle, expressed in [s]

########## 2. FrIfGdMacrotick

- **UUID**: `ECUC:2ddc7ccb-cf16-4c68-8a38-0f6bbcf7a302`
- **参数名**: `FrIfGdMacrotick`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [1E-6..6E-6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the cluster wide nominal macrotick, expressed in s

########## 3. FrIfMainFunctionPeriod

- **UUID**: `ECUC:2b9c1311-89e5-40f8-bab5-cc2348c63164`
- **参数名**: `FrIfMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The execution cycle of the FrIf_MainFunction_<cluster>() in seconds. The FrIf does not require this information but the BSW scheduler, which invokes the cluster main functions, needs it in order to plan its tasks.

######### ENUMERATION 类型参数

########## 1. FrIfGChannels

- **UUID**: `ECUC:64cc84b8-ea52-4c55-a4cb-73f10cae16ab`
- **参数名**: `FrIfGChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The channels that are used by the cluster.

########## 2. FrIfGdBit

- **UUID**: `ECUC:90293137-f6e3-4280-b2b5-7ed9d9309231`
- **参数名**: `FrIfGdBit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T100NS` (来源: AUTOSAR_ECUC)
  - `T200NS` (来源: AUTOSAR_ECUC)
  - `T400NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Nominal bit time in seconds

########## 3. FrIfGdSampleClockPeriod

- **UUID**: `ECUC:074f785a-9b8a-4ff6-a534-cfa494526c18`
- **参数名**: `FrIfGdSampleClockPeriod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T12_5NS` (来源: AUTOSAR_ECUC)
  - `T25NS` (来源: AUTOSAR_ECUC)
  - `T50NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sample clock period

######## 配置容器

本模块包含 **9** 个配置容器：

######### 1. FrIfClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9ab089b7-07d7-440d-bd6d-c70f77e37907`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **6** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FRIF_E_ACS_CH_A

- **UUID**: `ECUC:eecb417f-3543-46e4-a490-b4fa44b5e7fe`
- **引用名**: `FRIF_E_ACS_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

############ 2. FRIF_E_ACS_CH_B

- **UUID**: `ECUC:fed44e24-f3a4-48ea-92c5-a85a3c783c3a`
- **引用名**: `FRIF_E_ACS_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

############ 3. FRIF_E_NIT_CH_A

- **UUID**: `ECUC:3ed9a300-0edf-46a7-8738-ed2a39b39bcd`
- **引用名**: `FRIF_E_NIT_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

############ 4. FRIF_E_NIT_CH_B

- **UUID**: `ECUC:7e84dc55-d758-475f-b52b-7339e0806d5f`
- **引用名**: `FRIF_E_NIT_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

############ 5. FRIF_E_SW_CH_A

- **UUID**: `ECUC:9f331ab9-6d57-49e9-858d-ed1891b44a9a`
- **引用名**: `FRIF_E_SW_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

############ 6. FRIF_E_SW_CH_B

- **UUID**: `ECUC:99ddec77-a532-48bd-9392-bc321a74c5cb`
- **引用名**: `FRIF_E_SW_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######### 2. FrIfController

**容器属性**:

- **UUID**: `ECUC:319d659e-1521-466e-a809-a086ba548c28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of FlexRay CC.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCtrlIdx

- **UUID**: `ECUC:5ef23942-3937-48ff-9a21-7da86923efa2`
- **参数名**: `FrIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Communication Controllers. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay CC.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfFrCtrlRef

- **UUID**: `ECUC:e2246aac-2074-48cb-a7b1-5d27c4d6b912`
- **引用名**: `FrIfFrCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrController`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Controller, which is handled by a specific Driver. This reference is unique for the ECU.

########## 配置容器

本模块包含 **4** 个配置容器：

########### 1. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

############ 参数配置

此容器包含 **9** 个参数：

############# INTEGER 类型参数

############## 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

############## 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

############## 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

############## 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

############## 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

############# BOOLEAN 类型参数

############## 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

############## 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

############## 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

############# ENUMERATION 类型参数

############## 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

############## 引用关系

此容器包含 **1** 个引用：

############### SYMBOLIC-NAME-REFERENCE 类型引用

################ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

########### 2. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

########### 3. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

############# BOOLEAN 类型参数

############## 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

########### 4. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

############ 参数配置

此容器包含 **1** 个参数：

############# ENUMERATION 类型参数

############## 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

######### 3. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

############ 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

############ 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

############ 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

############ 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

########### BOOLEAN 类型参数

############ 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

############ 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

############ 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

########### ENUMERATION 类型参数

############ 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 4. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 5. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

########### BOOLEAN 类型参数

############ 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

######### 6. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

######### 7. FrIfJobList

**容器属性**:

- **UUID**: `ECUC:55b15d51-51ba-463d-897e-aa9fdd385c07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJobList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies a list of all FlexRay Jobs of the Cluster to be performed by FrIf_JobListExec_<ClstIdx>().

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfAbsTimerRef

- **UUID**: `ECUC:1e2599bc-e492-4a05-afec-e92422c80f62`
- **引用名**: `FrIfAbsTimerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrAbsoluteTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController/FrAbsoluteTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the absolute timer to be used to trigger the interrupt whose ISR contains the FrIf_JobListExec_<ClstIdx>() function.

########## 配置容器

本模块包含 **2** 个配置容器：

########### 1. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

############## 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

############## 参数配置

此容器包含 **3** 个参数：

############### INTEGER 类型参数

################ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

################ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

############### ENUMERATION 类型参数

################ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

############## 引用关系

此容器包含 **1** 个引用：

############### REFERENCE 类型引用

################ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

########### 2. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

############# ENUMERATION 类型参数

############## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

######### 8. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

############ 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

############# ENUMERATION 类型参数

############## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

######### 9. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 2. FrIfClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9ab089b7-07d7-440d-bd6d-c70f77e37907`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **6** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FRIF_E_ACS_CH_A

- **UUID**: `ECUC:eecb417f-3543-46e4-a490-b4fa44b5e7fe`
- **引用名**: `FRIF_E_ACS_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 2. FRIF_E_ACS_CH_B

- **UUID**: `ECUC:fed44e24-f3a4-48ea-92c5-a85a3c783c3a`
- **引用名**: `FRIF_E_ACS_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 3. FRIF_E_NIT_CH_A

- **UUID**: `ECUC:3ed9a300-0edf-46a7-8738-ed2a39b39bcd`
- **引用名**: `FRIF_E_NIT_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 4. FRIF_E_NIT_CH_B

- **UUID**: `ECUC:7e84dc55-d758-475f-b52b-7339e0806d5f`
- **引用名**: `FRIF_E_NIT_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 5. FRIF_E_SW_CH_A

- **UUID**: `ECUC:9f331ab9-6d57-49e9-858d-ed1891b44a9a`
- **引用名**: `FRIF_E_SW_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 6. FRIF_E_SW_CH_B

- **UUID**: `ECUC:99ddec77-a532-48bd-9392-bc321a74c5cb`
- **引用名**: `FRIF_E_SW_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

####### 3. FrIfController

**容器属性**:

- **UUID**: `ECUC:319d659e-1521-466e-a809-a086ba548c28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of FlexRay CC.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCtrlIdx

- **UUID**: `ECUC:5ef23942-3937-48ff-9a21-7da86923efa2`
- **参数名**: `FrIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Communication Controllers. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay CC.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfFrCtrlRef

- **UUID**: `ECUC:e2246aac-2074-48cb-a7b1-5d27c4d6b912`
- **引用名**: `FrIfFrCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrController`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Controller, which is handled by a specific Driver. This reference is unique for the ECU.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

############ 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

############ 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

############ 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

############ 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

########### BOOLEAN 类型参数

############ 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

############ 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

############ 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

########### ENUMERATION 类型参数

############ 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 2. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 3. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

########### BOOLEAN 类型参数

############ 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

######### 4. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

####### 4. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

########## 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

########## 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

########## 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

########## 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

######### BOOLEAN 类型参数

########## 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

########## 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

########## 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

######### ENUMERATION 类型参数

########## 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 5. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 6. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

######### BOOLEAN 类型参数

########## 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

####### 7. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

####### 8. FrIfJobList

**容器属性**:

- **UUID**: `ECUC:55b15d51-51ba-463d-897e-aa9fdd385c07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJobList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies a list of all FlexRay Jobs of the Cluster to be performed by FrIf_JobListExec_<ClstIdx>().

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfAbsTimerRef

- **UUID**: `ECUC:1e2599bc-e492-4a05-afec-e92422c80f62`
- **引用名**: `FrIfAbsTimerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrAbsoluteTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController/FrAbsoluteTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the absolute timer to be used to trigger the interrupt whose ISR contains the FrIf_JobListExec_<ClstIdx>() function.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

############ 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

############# ENUMERATION 类型参数

############## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

######### 2. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 9. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

########## 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 10. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

########## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

######### ENUMERATION 类型参数

########## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 11. FrIfFrameStructure

**容器属性**:

- **UUID**: `ECUC:86823166-8a4c-4ed0-86e4-b0a7f1061baf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameStructure`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The Frame structure specifies a Construction Plan how a Frame is assembled with PDUs and their respective Update-Bits.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfByteOrder

- **UUID**: `ECUC:62ea32bc-7998-40bb-85c0-e25bdd260376`
- **参数名**: `FrIfByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder of all Pdus that are mapped into the Frame.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfPdusInFrame

**容器属性**:

- **UUID**: `ECUC:a237f92f-48d2-45d7-bcc3-527874a9c0d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdusInFrame`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container holds all the information about a PDU in a FlexRay Frame.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfPduOffset

- **UUID**: `ECUC:c5a3bed9-c29b-4599-aaba-26b8b0d9dc5d`
- **参数名**: `FrIfPduOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The value specifies the offset of the PDU within the Frame [bytes].

############ 2. FrIfPduUpdateBitOffset

- **UUID**: `ECUC:dfce126e-f600-4f8d-a070-d6726efdcda2`
- **参数名**: `FrIfPduUpdateBitOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Frame (bit location of PDU's Update-Bit in the FlexRay Frame).

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfPduRef

- **UUID**: `ECUC:c2d16d19-b167-4725-939d-8798a06455da`
- **引用名**: `FrIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the local definition of a PDU.

####### 12. FrIfPdusInFrame

**容器属性**:

- **UUID**: `ECUC:a237f92f-48d2-45d7-bcc3-527874a9c0d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdusInFrame`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container holds all the information about a PDU in a FlexRay Frame.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfPduOffset

- **UUID**: `ECUC:c5a3bed9-c29b-4599-aaba-26b8b0d9dc5d`
- **参数名**: `FrIfPduOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The value specifies the offset of the PDU within the Frame [bytes].

########## 2. FrIfPduUpdateBitOffset

- **UUID**: `ECUC:dfce126e-f600-4f8d-a070-d6726efdcda2`
- **参数名**: `FrIfPduUpdateBitOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Frame (bit location of PDU's Update-Bit in the FlexRay Frame).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfPduRef

- **UUID**: `ECUC:c2d16d19-b167-4725-939d-8798a06455da`
- **引用名**: `FrIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the local definition of a PDU.

####### 13. FrIfPdu

**容器属性**:

- **UUID**: `ECUC:6d311fa0-67ff-41db-a650-88f3f78a0738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains PDU information. A PDU may be either a transmission PDU or a reception PDU.

######## 配置容器

本模块包含 **3** 个配置容器：

######### 1. FrIfRxPdu

**容器属性**:

- **UUID**: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Receive PDU

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. FrIfUserRxIndicationUL

- **UUID**: `ECUC:5696974a-27c8-4ab3-a10c-9bc55592e3f4`
- **参数名**: `FrIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received FRIFRXPDU has to be routed via <User_RxIndication>. This <User_RxIndication> has to be invoked when the indication of the configured FRIFRXPDU will be received by a Rx indication event from the FR Driver module. If no upper layer (UL) module is configured, no <User_RxIndication> has to be called in case of a Rx indication event of the FRIFRXPDU from the FR Driver module.

########### FUNCTION-NAME 类型参数

############ 1. FrIfRxIndicationName

- **UUID**: `ECUC:dd2860dc-ad58-429d-bb84-83fb954a0c7c`
- **参数名**: `FrIfRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter FRIF_USERRXINDICATION_UL. If FRIF_USERRXINDICATION_UL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_RxIndication> is fixed. If FRIF_USERRXINDICATION_UL equals CDD, the name of the <User_RxIndication> is selectable.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfRxPduRef

- **UUID**: `ECUC:7190286e-add2-4918-8f5b-300faefa5e9b`
- **引用名**: `FrIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

######### 2. FrIfTxPdu

**容器属性**:

- **UUID**: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

########## 参数配置

此容器包含 **8** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCounterLimit

- **UUID**: `ECUC:c2fc5dd3-b3c4-4cd7-8be6-ac7f6d0578ab`
- **参数名**: `FrIfCounterLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value states the maximum number of indication of ready PDU data to the FrIf (i.e. maximum number of invocations of FrIf_Transmit) without an intermediate transmission of the PDU.

############ 2. FrIfTxPduId

- **UUID**: `ECUC:70a26482-2bb2-4f98-9e2c-50872cffe5c6`
- **参数名**: `FrIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The global PDU identifier, which has to be used by the upper layer BSW module. The identifier has to be zero based and consecutive.

########### BOOLEAN 类型参数

############ 1. FrIfConfirm

- **UUID**: `ECUC:572e1bf7-2cc9-4839-a685-06b9d25779da`
- **参数名**: `FrIfConfirm`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the transmission of a PDU should be checked and confirmed to the PDU owning BSW module.

############ 2. FrIfImmediate

- **UUID**: `ECUC:428461f7-aec1-48b0-b34b-9e60ca3b89eb`
- **参数名**: `FrIfImmediate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the PDU is transmitted immediate or decoupled.

############ 3. FrIfNoneMode

- **UUID**: `ECUC:8d686556-bea1-49a2-b933-397cc46d55a2`
- **参数名**: `FrIfNoneMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using the "None-Mode" which means that there is no API FrIf_Transmit call of the upper layer for this PDU.

########### ENUMERATION 类型参数

############ 1. FrIfUserTxUL

- **UUID**: `ECUC:54b68088-e78d-4488-84ca-c9a553e541be`
- **参数名**: `FrIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the to be transmitted FRIFTXPDUID (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted FRIFTXPDUID has to be routed (via the <User_TxConfirmation>).

########### FUNCTION-NAME 类型参数

############ 1. FrIfTxConfirmationName

- **UUID**: `ECUC:ab1a488a-7143-4c2a-a9c8-b1b974f5ad4f`
- **参数名**: `FrIfTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TxConfirmation> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TxConfirmation> is selectable.

############ 2. FrIfUserTriggerTransmitName

- **UUID**: `ECUC:a9f34f10-e503-47d7-919a-6e2962c07b92`
- **参数名**: `FrIfUserTriggerTransmitName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TriggerTransmit> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TriggerTransmit> is selectable.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfTxPduRef

- **UUID**: `ECUC:4a970f9f-975c-4907-8ca7-b54068ef093f`
- **引用名**: `FrIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

######### 3. FrIfPduDirection

**容器属性**:

- **UUID**: `ECUC:625dad92-ff44-4e22-b7c4-33b165770f14`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **FrIfRxPdu**
  - UUID: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
  - 描述: Receive PDU
- **FrIfTxPdu**
  - UUID: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

A PDU is either transmit or receive

####### 14. FrIfRxPdu

**容器属性**:

- **UUID**: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Receive PDU

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfUserRxIndicationUL

- **UUID**: `ECUC:5696974a-27c8-4ab3-a10c-9bc55592e3f4`
- **参数名**: `FrIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received FRIFRXPDU has to be routed via <User_RxIndication>. This <User_RxIndication> has to be invoked when the indication of the configured FRIFRXPDU will be received by a Rx indication event from the FR Driver module. If no upper layer (UL) module is configured, no <User_RxIndication> has to be called in case of a Rx indication event of the FRIFRXPDU from the FR Driver module.

######### FUNCTION-NAME 类型参数

########## 1. FrIfRxIndicationName

- **UUID**: `ECUC:dd2860dc-ad58-429d-bb84-83fb954a0c7c`
- **参数名**: `FrIfRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter FRIF_USERRXINDICATION_UL. If FRIF_USERRXINDICATION_UL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_RxIndication> is fixed. If FRIF_USERRXINDICATION_UL equals CDD, the name of the <User_RxIndication> is selectable.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfRxPduRef

- **UUID**: `ECUC:7190286e-add2-4918-8f5b-300faefa5e9b`
- **引用名**: `FrIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

####### 15. FrIfTxPdu

**容器属性**:

- **UUID**: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCounterLimit

- **UUID**: `ECUC:c2fc5dd3-b3c4-4cd7-8be6-ac7f6d0578ab`
- **参数名**: `FrIfCounterLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value states the maximum number of indication of ready PDU data to the FrIf (i.e. maximum number of invocations of FrIf_Transmit) without an intermediate transmission of the PDU.

########## 2. FrIfTxPduId

- **UUID**: `ECUC:70a26482-2bb2-4f98-9e2c-50872cffe5c6`
- **参数名**: `FrIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The global PDU identifier, which has to be used by the upper layer BSW module. The identifier has to be zero based and consecutive.

######### BOOLEAN 类型参数

########## 1. FrIfConfirm

- **UUID**: `ECUC:572e1bf7-2cc9-4839-a685-06b9d25779da`
- **参数名**: `FrIfConfirm`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the transmission of a PDU should be checked and confirmed to the PDU owning BSW module.

########## 2. FrIfImmediate

- **UUID**: `ECUC:428461f7-aec1-48b0-b34b-9e60ca3b89eb`
- **参数名**: `FrIfImmediate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the PDU is transmitted immediate or decoupled.

########## 3. FrIfNoneMode

- **UUID**: `ECUC:8d686556-bea1-49a2-b933-397cc46d55a2`
- **参数名**: `FrIfNoneMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using the "None-Mode" which means that there is no API FrIf_Transmit call of the upper layer for this PDU.

######### ENUMERATION 类型参数

########## 1. FrIfUserTxUL

- **UUID**: `ECUC:54b68088-e78d-4488-84ca-c9a553e541be`
- **参数名**: `FrIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the to be transmitted FRIFTXPDUID (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted FRIFTXPDUID has to be routed (via the <User_TxConfirmation>).

######### FUNCTION-NAME 类型参数

########## 1. FrIfTxConfirmationName

- **UUID**: `ECUC:ab1a488a-7143-4c2a-a9c8-b1b974f5ad4f`
- **参数名**: `FrIfTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TxConfirmation> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TxConfirmation> is selectable.

########## 2. FrIfUserTriggerTransmitName

- **UUID**: `ECUC:a9f34f10-e503-47d7-919a-6e2962c07b92`
- **参数名**: `FrIfUserTriggerTransmitName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TriggerTransmit> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TriggerTransmit> is selectable.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfTxPduRef

- **UUID**: `ECUC:4a970f9f-975c-4907-8ca7-b54068ef093f`
- **引用名**: `FrIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

####### 16. FrIfPduDirection

**容器属性**:

- **UUID**: `ECUC:625dad92-ff44-4e22-b7c4-33b165770f14`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **FrIfRxPdu**
  - UUID: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
  - 描述: Receive PDU
- **FrIfTxPdu**
  - UUID: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

A PDU is either transmit or receive

##### 2. FrIfCluster

**容器属性**:

- **UUID**: `ECUC:9c2eb2ed-9528-45d7-a875-28de20a06488`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCluster`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container specifies a FrIf Cluster and all related data which is required to enable communication of the Cluster. A Cluster may consist of more than one Controller.

###### 参数配置

此容器包含 **37** 个参数：

####### INTEGER 类型参数

######## 1. FrIfClstIdx

- **UUID**: `ECUC:acba36f8-adeb-4c36-98e4-837e0f616935`
- **参数名**: `FrIfClstIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Clusters. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay Cluster.

######## 2. FrIfGColdStartAttempts

- **UUID**: `ECUC:fd06e4ae-2179-4ce0-855c-f4aa7f03b3b7`
- **参数名**: `FrIfGColdStartAttempts`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of times a node in the cluster is permitted to attempt to start the cluster by initiating schedule synchronization

######## 3. FrIfGCycleCountMax

- **UUID**: `ECUC:5fd22705-bf85-4659-bf98-be6bfcc0abed`
- **参数名**: `FrIfGCycleCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [7..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum cycle counter value in a given cluster.

######## 4. FrIfGListenNoise

- **UUID**: `ECUC:05659b06-1760-4f5a-af1f-35f0844d2a3a`
- **参数名**: `FrIfGListenNoise`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..16]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper limit for the start up listen timeout and wake up listen timeout in the presence of noise. It is used as a multiplier of the node

######## 5. FrIfGMacroPerCycle

- **UUID**: `ECUC:9b6b8aa9-7ad4-454b-a721-51641bb65c5b`
- **参数名**: `FrIfGMacroPerCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..16000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks in a communication cycle.

######## 6. FrIfGMaxWithoutClockCorrectFatal

- **UUID**: `ECUC:df1cf583-bf38-49a2-b150-95275930adf0`
- **参数名**: `FrIfGMaxWithoutClockCorrectFatal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of consecutive even/odd Cycle pairs with missing clock correction terms that will cause the protocol to transition from the POC:normal active or POC:normal passive state into the POC:halt state. [Even/odd cycle pairs].

######## 7. FrIfGMaxWithoutClockCorrectPassive

- **UUID**: `ECUC:9ab93616-b25c-4f80-aaa1-af10c35a2927`
- **参数名**: `FrIfGMaxWithoutClockCorrectPassive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Threshold used for testing the vClockCorrectionFailed counter. Defines the number of consecutive even/odd Cycle pairs with missing clock correction terms that will cause the protocol to transition from the POC:normal active state to the POC:normal passive state. [Even/Odd cycle pairs]

######## 8. FrIfGNetworkManagementVectorLength

- **UUID**: `ECUC:bbde5f64-38de-40ee-a656-1e4c515b3e38`
- **参数名**: `FrIfGNetworkManagementVectorLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..12]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the Network Management vector in a cluster [bytes]

######## 9. FrIfGNumberOfMinislots

- **UUID**: `ECUC:d9f67d2c-e7dd-45f9-993e-3242ef59b478`
- **参数名**: `FrIfGNumberOfMinislots`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7988]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of minislots in the dynamic segment

######## 10. FrIfGNumberOfStaticSlots

- **UUID**: `ECUC:9210d68d-a1ee-436e-b951-3dc34765cb23`
- **参数名**: `FrIfGNumberOfStaticSlots`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..1023]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of static slots in the static segment

######## 11. FrIfGPayloadLengthStatic

- **UUID**: `ECUC:7182990c-c42b-4d6a-a5ff-b542fcb4cd36`
- **参数名**: `FrIfGPayloadLengthStatic`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..127]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Payload length of a static frame [16 bit words]

######## 12. FrIfGSyncFrameIDCountMax

- **UUID**: `ECUC:f38bcebd-b881-4dac-9af7-53dcc1c26961`
- **参数名**: `FrIfGSyncFrameIDCountMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of distinct syncframe identifiers present in a  given cluster. This parameter maps to FlexRay Protocol 2.1 Rev. A parameter gSyncNodeMax.

######## 13. FrIfGdActionPointOffset

- **UUID**: `ECUC:7dad1bd0-f203-45cf-bed2-b8c487b27c60`
- **参数名**: `FrIfGdActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks the action point is offset from the beginning of a static slot.

######## 14. FrIfGdCasRxLowMax

- **UUID**: `ECUC:8e414515-2806-468b-810d-a2a0345e8757`
- **参数名**: `FrIfGdCasRxLowMax`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [28..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Upper limit of the CAS acceptance windows [gdBit]

######## 15. FrIfGdDynamicSlotIdlePhase

- **UUID**: `ECUC:36b405ab-0c5a-4b1e-b055-03cff003fc6d`
- **参数名**: `FrIfGdDynamicSlotIdlePhase`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..2]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the idle phase within a dynamic slot [Minislots].

######## 16. FrIfGdIgnoreAfterTx

- **UUID**: `ECUC:55227fbf-ff62-4f17-86eb-fb3be77f6517`
- **参数名**: `FrIfGdIgnoreAfterTx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration for which the bitstrobing is paused after transmission [gdBit].

######## 17. FrIfGdMiniSlotActionPointOffset

- **UUID**: `ECUC:b31a710c-5b2f-41a2-8861-3902a6b62530`
- **参数名**: `FrIfGdMiniSlotActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of Macroticks the Minislot action point is offset from the beginning of a Minislot [Macroticks].

######## 18. FrIfGdMinislot

- **UUID**: `ECUC:d925ca4b-2c55-4554-9e82-cb7e117367e7`
- **参数名**: `FrIfGdMinislot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a minislot [Macroticks]

######## 19. FrIfGdNit

- **UUID**: `ECUC:8d38067a-6d89-4e82-9dd2-28af28190db3`
- **参数名**: `FrIfGdNit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [2..15978]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the Network Idle Time [Macroticks]

######## 20. FrIfGdStaticSlot

- **UUID**: `ECUC:86eef347-5af3-44b5-ac4a-e799aed9ac97`
- **参数名**: `FrIfGdStaticSlot`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [3..664]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of a static slot [Macroticks].

######## 21. FrIfGdSymbolWindow

- **UUID**: `ECUC:3168f855-09f2-4dab-bbad-e53571fb477e`
- **参数名**: `FrIfGdSymbolWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..162]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the symbol window [Macroticks].

######## 22. FrIfGdSymbolWindowActionPointOffset

- **UUID**: `ECUC:c828edea-75dd-496a-92f9-4a69eb5279d8`
- **参数名**: `FrIfGdSymbolWindowActionPointOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of macroticks the action point offset is from the beginning of the symbol window [Macroticks].

######## 23. FrIfGdTSSTransmitter

- **UUID**: `ECUC:cd257190-952b-419a-8536-ff98206ba70a`
- **参数名**: `FrIfGdTSSTransmitter`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits in the Transmission Start Sequence [gdBits].

######## 24. FrIfGdWakeupRxIdle

- **UUID**: `ECUC:5700e5c3-21b8-492e-a15a-e7b9f8890a47`
- **参数名**: `FrIfGdWakeupRxIdle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..59]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to test the duration of the 'idle' or HIGH phase of a received wakeup [gdBit]. Remarks: This parameter maps to FlexRay Protocol 2.1 Rev. A parameter gdWakeupSymbolRxIdle. Lower limit 14 for FlexRay Protocol 2.1 Rev. A compliance.

######## 25. FrIfGdWakeupRxLow

- **UUID**: `ECUC:49d8c5b9-e6ee-495e-8f08-214b329352ae`
- **参数名**: `FrIfGdWakeupRxLow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [8..59]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to test the duration of the LOW phase of a received wakeup [gdBit].

######## 26. FrIfGdWakeupRxWindow

- **UUID**: `ECUC:02c38e9b-73e1-4d76-b72b-cd837212b26b`
- **参数名**: `FrIfGdWakeupRxWindow`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [76..485]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The size of the window used to detect wakeups [gdBit].

######## 27. FrIfGdWakeupTxActive

- **UUID**: `ECUC:87fda236-4246-4548-b42e-a2bb02e6842f`
- **参数名**: `FrIfGdWakeupTxActive`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [15..60]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to transmit the LOW phase of awakeup symbol and  the HIGH and LOW phases of a WUDOP [gdBit].

######## 28. FrIfGdWakeupTxIdle

- **UUID**: `ECUC:5e28082c-931c-43e2-9d26-58297c3c9457`
- **参数名**: `FrIfGdWakeupTxIdle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [45..180]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Number of bits used by the node to transmit the 'idle' part of a

######## 29. FrIfMaxIsrDelay

- **UUID**: `ECUC:336dfed2-bd0c-41a6-977d-eeda4d0431b6`
- **参数名**: `FrIfMaxIsrDelay`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The maximum delay in macroticks the FrIf_JoblistExec_<cluster>() function is processed after the absolute timer interrupt was triggered.

######## 30. FrIfSafetyMargin

- **UUID**: `ECUC:2263fb3c-0a7b-44bd-b166-315865d5e4ee`
- **参数名**: `FrIfSafetyMargin`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Additional timespan in macroticks which takes jitter into account to be able to set the JobListPointer to the next possible job which can be executed in case the FlexRay Job List Execution Function has be resynchronized.

####### BOOLEAN 类型参数

######## 1. FrIfDetectNITError

- **UUID**: `ECUC:cb95f335-435b-40cf-b7fd-5279da55e4a3`
- **参数名**: `FrIfDetectNITError`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Indicates whether NIT error status of each cluster shall be detected or not.

####### FLOAT 类型参数

######## 1. FrIfGdCycle

- **UUID**: `ECUC:ef2961ff-251f-429b-abc4-31886a5e4554`
- **参数名**: `FrIfGdCycle`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [2.4E-5..0.016]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the cycle, expressed in [s]

######## 2. FrIfGdMacrotick

- **UUID**: `ECUC:2ddc7ccb-cf16-4c68-8a38-0f6bbcf7a302`
- **参数名**: `FrIfGdMacrotick`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [1E-6..6E-6]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Duration of the cluster wide nominal macrotick, expressed in s

######## 3. FrIfMainFunctionPeriod

- **UUID**: `ECUC:2b9c1311-89e5-40f8-bab5-cc2348c63164`
- **参数名**: `FrIfMainFunctionPeriod`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..Inf]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The execution cycle of the FrIf_MainFunction_<cluster>() in seconds. The FrIf does not require this information but the BSW scheduler, which invokes the cluster main functions, needs it in order to plan its tasks.

####### ENUMERATION 类型参数

######## 1. FrIfGChannels

- **UUID**: `ECUC:64cc84b8-ea52-4c55-a4cb-73f10cae16ab`
- **参数名**: `FrIfGChannels`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FR_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FR_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The channels that are used by the cluster.

######## 2. FrIfGdBit

- **UUID**: `ECUC:90293137-f6e3-4280-b2b5-7ed9d9309231`
- **参数名**: `FrIfGdBit`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T100NS` (来源: AUTOSAR_ECUC)
  - `T200NS` (来源: AUTOSAR_ECUC)
  - `T400NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Nominal bit time in seconds

######## 3. FrIfGdSampleClockPeriod

- **UUID**: `ECUC:074f785a-9b8a-4ff6-a534-cfa494526c18`
- **参数名**: `FrIfGdSampleClockPeriod`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `T12_5NS` (来源: AUTOSAR_ECUC)
  - `T25NS` (来源: AUTOSAR_ECUC)
  - `T50NS` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Sample clock period

###### 配置容器

本模块包含 **9** 个配置容器：

####### 1. FrIfClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9ab089b7-07d7-440d-bd6d-c70f77e37907`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **6** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FRIF_E_ACS_CH_A

- **UUID**: `ECUC:eecb417f-3543-46e4-a490-b4fa44b5e7fe`
- **引用名**: `FRIF_E_ACS_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 2. FRIF_E_ACS_CH_B

- **UUID**: `ECUC:fed44e24-f3a4-48ea-92c5-a85a3c783c3a`
- **引用名**: `FRIF_E_ACS_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 3. FRIF_E_NIT_CH_A

- **UUID**: `ECUC:3ed9a300-0edf-46a7-8738-ed2a39b39bcd`
- **引用名**: `FRIF_E_NIT_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 4. FRIF_E_NIT_CH_B

- **UUID**: `ECUC:7e84dc55-d758-475f-b52b-7339e0806d5f`
- **引用名**: `FRIF_E_NIT_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 5. FRIF_E_SW_CH_A

- **UUID**: `ECUC:9f331ab9-6d57-49e9-858d-ed1891b44a9a`
- **引用名**: `FRIF_E_SW_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

########## 6. FRIF_E_SW_CH_B

- **UUID**: `ECUC:99ddec77-a532-48bd-9392-bc321a74c5cb`
- **引用名**: `FRIF_E_SW_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

####### 2. FrIfController

**容器属性**:

- **UUID**: `ECUC:319d659e-1521-466e-a809-a086ba548c28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of FlexRay CC.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCtrlIdx

- **UUID**: `ECUC:5ef23942-3937-48ff-9a21-7da86923efa2`
- **参数名**: `FrIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Communication Controllers. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay CC.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfFrCtrlRef

- **UUID**: `ECUC:e2246aac-2074-48cb-a7b1-5d27c4d6b912`
- **引用名**: `FrIfFrCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrController`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Controller, which is handled by a specific Driver. This reference is unique for the ECU.

######## 配置容器

本模块包含 **4** 个配置容器：

######### 1. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

########## 参数配置

此容器包含 **9** 个参数：

########### INTEGER 类型参数

############ 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

############ 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

############ 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

############ 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

############ 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

########### BOOLEAN 类型参数

############ 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

############ 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

############ 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

########### ENUMERATION 类型参数

############ 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

############ 引用关系

此容器包含 **1** 个引用：

############# SYMBOLIC-NAME-REFERENCE 类型引用

############## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 2. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

######### 3. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

########### BOOLEAN 类型参数

############ 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

######### 4. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

########## 参数配置

此容器包含 **1** 个参数：

########### ENUMERATION 类型参数

############ 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

####### 3. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

########## 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

########## 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

########## 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

########## 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

######### BOOLEAN 类型参数

########## 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

########## 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

########## 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

######### ENUMERATION 类型参数

########## 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 4. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 5. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

######### BOOLEAN 类型参数

########## 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

####### 6. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

####### 7. FrIfJobList

**容器属性**:

- **UUID**: `ECUC:55b15d51-51ba-463d-897e-aa9fdd385c07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJobList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies a list of all FlexRay Jobs of the Cluster to be performed by FrIf_JobListExec_<ClstIdx>().

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfAbsTimerRef

- **UUID**: `ECUC:1e2599bc-e492-4a05-afec-e92422c80f62`
- **引用名**: `FrIfAbsTimerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrAbsoluteTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController/FrAbsoluteTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the absolute timer to be used to trigger the interrupt whose ISR contains the FrIf_JobListExec_<ClstIdx>() function.

######## 配置容器

本模块包含 **2** 个配置容器：

######### 1. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

############ 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

############ 参数配置

此容器包含 **3** 个参数：

############# INTEGER 类型参数

############## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

############# ENUMERATION 类型参数

############## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

######### 2. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 8. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

########## 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 9. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

########## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

######### ENUMERATION 类型参数

########## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

##### 3. FrIfClusterDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:9ab089b7-07d7-440d-bd6d-c70f77e37907`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfClusterDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **6** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FRIF_E_ACS_CH_A

- **UUID**: `ECUC:eecb417f-3543-46e4-a490-b4fa44b5e7fe`
- **引用名**: `FRIF_E_ACS_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######## 2. FRIF_E_ACS_CH_B

- **UUID**: `ECUC:fed44e24-f3a4-48ea-92c5-a85a3c783c3a`
- **引用名**: `FRIF_E_ACS_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in ACS on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######## 3. FRIF_E_NIT_CH_A

- **UUID**: `ECUC:3ed9a300-0edf-46a7-8738-ed2a39b39bcd`
- **引用名**: `FRIF_E_NIT_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######## 4. FRIF_E_NIT_CH_B

- **UUID**: `ECUC:7e84dc55-d758-475f-b52b-7339e0806d5f`
- **引用名**: `FRIF_E_NIT_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in NIT on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######## 5. FRIF_E_SW_CH_A

- **UUID**: `ECUC:9f331ab9-6d57-49e9-858d-ed1891b44a9a`
- **引用名**: `FRIF_E_SW_CH_A`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel A was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

######## 6. FRIF_E_SW_CH_B

- **UUID**: `ECUC:99ddec77-a532-48bd-9392-bc321a74c5cb`
- **引用名**: `FRIF_E_SW_CH_B`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the DemEventParameter which shall be issued when an error in SW on channel B was detected. If the reference is not configured the error shall not be reported (neither to DET nor to DEM).

##### 4. FrIfController

**容器属性**:

- **UUID**: `ECUC:319d659e-1521-466e-a809-a086ba548c28`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfController`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container contains the configuration of FlexRay CC.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. FrIfCtrlIdx

- **UUID**: `ECUC:5ef23942-3937-48ff-9a21-7da86923efa2`
- **参数名**: `FrIfCtrlIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..31]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter provides a zero-based consecutive index of the FlexRay Communication Controllers. Upper layer BSW modules and the FrIf itself use this index to identify a FlexRay CC.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrIfFrCtrlRef

- **UUID**: `ECUC:e2246aac-2074-48cb-a7b1-5d27c4d6b912`
- **引用名**: `FrIfFrCtrlRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrController`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Controller, which is handled by a specific Driver. This reference is unique for the ECU.

###### 配置容器

本模块包含 **4** 个配置容器：

####### 1. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

######## 参数配置

此容器包含 **9** 个参数：

######### INTEGER 类型参数

########## 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

########## 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

########## 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

########## 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

########## 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

######### BOOLEAN 类型参数

########## 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

########## 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

########## 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

######### ENUMERATION 类型参数

########## 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 2. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

####### 3. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

######### BOOLEAN 类型参数

########## 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

####### 4. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

######## 参数配置

此容器包含 **1** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

##### 5. FrIfFrameTriggering

**容器属性**:

- **UUID**: `ECUC:11018403-37a7-41de-a035-32dd93a0a75b`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggering`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A Frame triggering contains the communication parameters of the FlexRay Frame as well as a reference to the Frame Construction Plan.

###### 参数配置

此容器包含 **9** 个参数：

####### INTEGER 类型参数

######## 1. FrIfBaseCycle

- **UUID**: `ECUC:efe1b6a1-df0c-4b38-9f7a-50c6ae57547a`
- **参数名**: `FrIfBaseCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Base Cycle used to transmit this FlexRay Frame.

######## 2. FrIfCycleRepetition

- **UUID**: `ECUC:22ef3362-122d-484f-8da2-76180f177444`
- **参数名**: `FrIfCycleRepetition`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..64]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Cycle Repetition used to transmit this FlexRay Frame..

######## 3. FrIfLSduLength

- **UUID**: `ECUC:b4a19cfd-baa4-44ee-9dcc-068fff0c1aba`
- **参数名**: `FrIfLSduLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..254]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The payload length of the Frame is given here. This parameter is required for validation if configured PDUs and update information fits into the Frame at configuration time [bytes].

######## 4. FrIfMessageId

- **UUID**: `ECUC:b9158572-bb6a-42e3-b4ba-79060379728b`
- **参数名**: `FrIfMessageId`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The first two bytes of the payload segment of the FlexRay frame format for frames transmitted in the

######## 5. FrIfSlotId

- **UUID**: `ECUC:f7261522-87b8-4eed-b7db-d75e9b120582`
- **参数名**: `FrIfSlotId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..2047]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Slot ID used to transmit this FlexRay Frame.

####### BOOLEAN 类型参数

######## 1. FrIfAllowDynamicLSduLength

- **UUID**: `ECUC:e7730a8c-8ca8-42b2-b19c-4d579b622edf`
- **参数名**: `FrIfAllowDynamicLSduLength`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Allows L-PDU length reduction ('FrIfLSduLength' defines max. length) and indicates that the related CC buffer has to be reconfigured for the actual length and Header-CRC before transmission of the L-PDU.

######## 2. FrIfAlwaysTransmit

- **UUID**: `ECUC:4584bcbb-2679-4e49-85dc-0336bc90238f`
- **参数名**: `FrIfAlwaysTransmit`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines wether the driver's API function Fr_TransmitTxLPdu() shall always be called for this L-PDU.

######## 3. FrIfPayloadPreamble

- **UUID**: `ECUC:e1e62334-6870-46e2-b687-35576bace368`
- **参数名**: `FrIfPayloadPreamble`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switching the Payload Preamble bit.

####### ENUMERATION 类型参数

######## 1. FrIfChannel

- **UUID**: `ECUC:f9a10bc2-ba77-4ae4-9289-b04ab9217eb0`
- **参数名**: `FrIfChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_AB` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter contains the FlexRay Channel used to transmit this FlexRay Frame.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfFrameStructureRef

- **UUID**: `ECUC:d6e4667a-efce-4b60-b62d-e4b4da099dff`
- **引用名**: `FrIfFrameStructureRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameStructure`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfFrameStructure`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the Construction Plan of the FlexRay Frame.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

##### 6. FrIfFrameTriggeringDemEventParameterRefs

**容器属性**:

- **UUID**: `ECUC:5bdf8934-4088-4ae8-b0d0-281ce795dced`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameTriggeringDemEventParameterRefs`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Container for the references to DemEventParameter elements which shall be invoked using the API Dem_ReportErrorStatus API in case the corresponding error occurs. The EventId is taken from the referenced DemEventParameter's DemEventId value. The standardized errors are provided in the container and can be extended by vendor specific error references.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrIfDemFTSlotStatusRef

- **UUID**: `ECUC:c605160c-eb64-4bcc-a837-c62ad6941b8b`
- **引用名**: `FrIfDemFTSlotStatusRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [0..1]
- **目标**: `DemEventParameter`
- **完整路径**: `/AUTOSAR/EcucDefs/Dem/DemConfigSet/DemEventParameter`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to DEM event Id that is reported when FlexRay driver module detects slot errors. If this parameter is not configured, no event reporting happens.

##### 7. FrIfLPdu

**容器属性**:

- **UUID**: `ECUC:21590a50-51af-4b3c-928e-8d087639ea4e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfLPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Reference to a L-PDU index

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrIfLPduIdx

- **UUID**: `ECUC:f35915a8-fadb-430b-a3b6-9d5e157ecceb`
- **参数名**: `FrIfLPduIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..4095]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies the L-PDU in the interaction between FlexRay Interface and FlexRay Driver.

####### BOOLEAN 类型参数

######## 1. FrIfReconfigurable

- **UUID**: `ECUC:f7c78928-7331-4999-b9a2-d15f9ab61411`
- **参数名**: `FrIfReconfigurable`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter specifies that this LPdu is reconfigurable using FrIf_ReconfigLPdu. This means that this LPdu can be assigned to a different FrameTriggering at runtime. However, this reconfiguration is limited by hardware constraints. The direction of the LPdu cannot be reconfigured.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfVBTriggeringRef

- **UUID**: `ECUC:d72bf6de-9dad-4275-a2c9-861a4a43ce54`
- **引用名**: `FrIfVBTriggeringRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfFrameTriggering`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfFrameTriggering`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the assigned Frame triggering.

##### 8. FrIfTransceiver

**容器属性**:

- **UUID**: `ECUC:e031c398-1244-4908-8654-e4e58a1cbf51`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTransceiver`
- **多重性**: [1..2]
- **多配置容器**: false

**容器描述**:

Up to two FlexRay Transceivers may connect a Controller to a Cluster. This container realizes a Controller-Transceiver assignment.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FrIfClusterChannel

- **UUID**: `ECUC:dbf99760-3f35-415d-b4fd-b93477da72d5`
- **参数名**: `FrIfClusterChannel`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `FRIF_CHANNEL_A` (来源: AUTOSAR_ECUC)
  - `FRIF_CHANNEL_B` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter identifies to which one of the two Channels (A, B, A and B) of the Cluster the Transceiver is connected. FrIfClusterChannel shall map to Fr_ChannelType: FRIF_CHANNEL_A == FR_CHANNEL_A FRIF_CHANNEL_B == FR_CHANNEL_B FR_CHANNEL_AB shall not be used.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrIfFrTrcvChannelRef

- **UUID**: `ECUC:f9e24fbf-0c59-4b0f-8cc1-f3a810c3336b`
- **引用名**: `FrIfFrTrcvChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/FrTrcv/FrTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a Transceiver Driver Channel. This reference is unique for the ECU.

##### 9. FrIfJobList

**容器属性**:

- **UUID**: `ECUC:55b15d51-51ba-463d-897e-aa9fdd385c07`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJobList`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container specifies a list of all FlexRay Jobs of the Cluster to be performed by FrIf_JobListExec_<ClstIdx>().

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. FrIfAbsTimerRef

- **UUID**: `ECUC:1e2599bc-e492-4a05-afec-e92422c80f62`
- **引用名**: `FrIfAbsTimerRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `FrAbsoluteTimer`
- **完整路径**: `/AUTOSAR/EcucDefs/Fr/FrMultipleConfiguration/FrController/FrAbsoluteTimer`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the absolute timer to be used to trigger the interrupt whose ISR contains the FrIf_JobListExec_<ClstIdx>() function.

###### 配置容器

本模块包含 **2** 个配置容器：

####### 1. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

########## 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

########## 参数配置

此容器包含 **3** 个参数：

########### INTEGER 类型参数

############ 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

############ 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

########### ENUMERATION 类型参数

############ 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

####### 2. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

########## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

######### ENUMERATION 类型参数

########## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

##### 10. FrIfJob

**容器属性**:

- **UUID**: `ECUC:8ff6b311-4355-4f43-8089-12e995828aee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfJob`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A job may contain more than one operation that are executed at a specific point in time.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrIfCycle

- **UUID**: `ECUC:bfa2d171-ca87-48e2-817f-a74548011b9b`
- **参数名**: `FrIfCycle`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..63]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The FlexRay Cycle in which the communication operation will execute this job

######## 2. FrIfMacrotick

- **UUID**: `ECUC:44c6c409-9910-45fc-a634-f49e68633235`
- **参数名**: `FrIfMacrotick`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..10240000]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Macrotick offset in the Cycle [Macrotick]

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

######## 参数配置

此容器包含 **3** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

########## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

######### ENUMERATION 类型参数

########## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

##### 11. FrIfCommunicationOperation

**容器属性**:

- **UUID**: `ECUC:3151a42c-115f-4efe-bae7-b98607b1ed0c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfCommunicationOperation`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

A separate operation which is part of a FlexRay Job and defines what type of action is executed.

###### 参数配置

此容器包含 **3** 个参数：

####### INTEGER 类型参数

######## 1. FrIfCommunicationOperationIdx

- **UUID**: `ECUC:342471c5-1d12-48e4-aad6-1a0dc9670f48`
- **参数名**: `FrIfCommunicationOperationIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: For each FlexRay Communication Job, this index spans a range of zero-based consecutive values and thus defines the order of the FlexRay Communication Operation in the respective FlexRay Communication Job.

######## 2. FrIfRxComOpMaxLoop

- **UUID**: `ECUC:0814d3ca-b9b5-4c62-8cc6-037b9cefd9f9`
- **参数名**: `FrIfRxComOpMaxLoop`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..512]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the maximum number of loops for the receive RECEIVE_AND_INDICATE (Use case: emptying a FIFO).

####### ENUMERATION 类型参数

######## 1. FrIfCommunicationAction

- **UUID**: `ECUC:dc3b2d40-c065-44ee-8560-b142f21dc4d5`
- **参数名**: `FrIfCommunicationAction`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `DECOUPLED_TRANSMISSION` (来源: AUTOSAR_ECUC)
  - `FREE_OP_A` (来源: AUTOSAR_ECUC)
  - `FREE_OP_B` (来源: AUTOSAR_ECUC)
  - `PREPARE_LPDU` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_INDICATE` (来源: AUTOSAR_ECUC)
  - `RECEIVE_AND_STORE` (来源: AUTOSAR_ECUC)
  - `RX_INDICATION` (来源: AUTOSAR_ECUC)
  - `TX_CONFIRMATION` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The action to be performed in the FlexRay Operation

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfLPduIdxRef

- **UUID**: `ECUC:6027b4eb-5347-490a-a19b-dafb005075e0`
- **引用名**: `FrIfLPduIdxRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfLPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfCluster/FrIfController/FrIfLPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to a L-PDu index

##### 12. FrIfFrameStructure

**容器属性**:

- **UUID**: `ECUC:86823166-8a4c-4ed0-86e4-b0a7f1061baf`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfFrameStructure`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

The Frame structure specifies a Construction Plan how a Frame is assembled with PDUs and their respective Update-Bits.

###### 参数配置

此容器包含 **1** 个参数：

####### ENUMERATION 类型参数

######## 1. FrIfByteOrder

- **UUID**: `ECUC:62ea32bc-7998-40bb-85c0-e25bdd260376`
- **参数名**: `FrIfByteOrder`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `BIG_ENDIAN` (来源: AUTOSAR_ECUC)
  - `LITTLE_ENDIAN` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the ByteOrder of all Pdus that are mapped into the Frame.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. FrIfPdusInFrame

**容器属性**:

- **UUID**: `ECUC:a237f92f-48d2-45d7-bcc3-527874a9c0d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdusInFrame`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container holds all the information about a PDU in a FlexRay Frame.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. FrIfPduOffset

- **UUID**: `ECUC:c5a3bed9-c29b-4599-aaba-26b8b0d9dc5d`
- **参数名**: `FrIfPduOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The value specifies the offset of the PDU within the Frame [bytes].

########## 2. FrIfPduUpdateBitOffset

- **UUID**: `ECUC:dfce126e-f600-4f8d-a070-d6726efdcda2`
- **参数名**: `FrIfPduUpdateBitOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Frame (bit location of PDU's Update-Bit in the FlexRay Frame).

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfPduRef

- **UUID**: `ECUC:c2d16d19-b167-4725-939d-8798a06455da`
- **引用名**: `FrIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the local definition of a PDU.

##### 13. FrIfPdusInFrame

**容器属性**:

- **UUID**: `ECUC:a237f92f-48d2-45d7-bcc3-527874a9c0d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdusInFrame`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

This container holds all the information about a PDU in a FlexRay Frame.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. FrIfPduOffset

- **UUID**: `ECUC:c5a3bed9-c29b-4599-aaba-26b8b0d9dc5d`
- **参数名**: `FrIfPduOffset`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..253]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The value specifies the offset of the PDU within the Frame [bytes].

######## 2. FrIfPduUpdateBitOffset

- **UUID**: `ECUC:dfce126e-f600-4f8d-a070-d6726efdcda2`
- **参数名**: `FrIfPduUpdateBitOffset`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..2031]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value specifies where the PDU's Update-Bit is stored in the Frame (bit location of PDU's Update-Bit in the FlexRay Frame).

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfPduRef

- **UUID**: `ECUC:c2d16d19-b167-4725-939d-8798a06455da`
- **引用名**: `FrIfPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `FrIfPdu`
- **完整路径**: `/AUTOSAR/EcucDefs/FrIf/FrIfConfig/FrIfPdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the reference to the local definition of a PDU.

##### 14. FrIfPdu

**容器属性**:

- **UUID**: `ECUC:6d311fa0-67ff-41db-a650-88f3f78a0738`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfPdu`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Contains PDU information. A PDU may be either a transmission PDU or a reception PDU.

###### 配置容器

本模块包含 **3** 个配置容器：

####### 1. FrIfRxPdu

**容器属性**:

- **UUID**: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Receive PDU

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. FrIfUserRxIndicationUL

- **UUID**: `ECUC:5696974a-27c8-4ab3-a10c-9bc55592e3f4`
- **参数名**: `FrIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received FRIFRXPDU has to be routed via <User_RxIndication>. This <User_RxIndication> has to be invoked when the indication of the configured FRIFRXPDU will be received by a Rx indication event from the FR Driver module. If no upper layer (UL) module is configured, no <User_RxIndication> has to be called in case of a Rx indication event of the FRIFRXPDU from the FR Driver module.

######### FUNCTION-NAME 类型参数

########## 1. FrIfRxIndicationName

- **UUID**: `ECUC:dd2860dc-ad58-429d-bb84-83fb954a0c7c`
- **参数名**: `FrIfRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter FRIF_USERRXINDICATION_UL. If FRIF_USERRXINDICATION_UL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_RxIndication> is fixed. If FRIF_USERRXINDICATION_UL equals CDD, the name of the <User_RxIndication> is selectable.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfRxPduRef

- **UUID**: `ECUC:7190286e-add2-4918-8f5b-300faefa5e9b`
- **引用名**: `FrIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

####### 2. FrIfTxPdu

**容器属性**:

- **UUID**: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

######## 参数配置

此容器包含 **8** 个参数：

######### INTEGER 类型参数

########## 1. FrIfCounterLimit

- **UUID**: `ECUC:c2fc5dd3-b3c4-4cd7-8be6-ac7f6d0578ab`
- **参数名**: `FrIfCounterLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value states the maximum number of indication of ready PDU data to the FrIf (i.e. maximum number of invocations of FrIf_Transmit) without an intermediate transmission of the PDU.

########## 2. FrIfTxPduId

- **UUID**: `ECUC:70a26482-2bb2-4f98-9e2c-50872cffe5c6`
- **参数名**: `FrIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The global PDU identifier, which has to be used by the upper layer BSW module. The identifier has to be zero based and consecutive.

######### BOOLEAN 类型参数

########## 1. FrIfConfirm

- **UUID**: `ECUC:572e1bf7-2cc9-4839-a685-06b9d25779da`
- **参数名**: `FrIfConfirm`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the transmission of a PDU should be checked and confirmed to the PDU owning BSW module.

########## 2. FrIfImmediate

- **UUID**: `ECUC:428461f7-aec1-48b0-b34b-9e60ca3b89eb`
- **参数名**: `FrIfImmediate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the PDU is transmitted immediate or decoupled.

########## 3. FrIfNoneMode

- **UUID**: `ECUC:8d686556-bea1-49a2-b933-397cc46d55a2`
- **参数名**: `FrIfNoneMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using the "None-Mode" which means that there is no API FrIf_Transmit call of the upper layer for this PDU.

######### ENUMERATION 类型参数

########## 1. FrIfUserTxUL

- **UUID**: `ECUC:54b68088-e78d-4488-84ca-c9a553e541be`
- **参数名**: `FrIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the to be transmitted FRIFTXPDUID (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted FRIFTXPDUID has to be routed (via the <User_TxConfirmation>).

######### FUNCTION-NAME 类型参数

########## 1. FrIfTxConfirmationName

- **UUID**: `ECUC:ab1a488a-7143-4c2a-a9c8-b1b974f5ad4f`
- **参数名**: `FrIfTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TxConfirmation> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TxConfirmation> is selectable.

########## 2. FrIfUserTriggerTransmitName

- **UUID**: `ECUC:a9f34f10-e503-47d7-919a-6e2962c07b92`
- **参数名**: `FrIfUserTriggerTransmitName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TriggerTransmit> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TriggerTransmit> is selectable.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. FrIfTxPduRef

- **UUID**: `ECUC:4a970f9f-975c-4907-8ca7-b54068ef093f`
- **引用名**: `FrIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

####### 3. FrIfPduDirection

**容器属性**:

- **UUID**: `ECUC:625dad92-ff44-4e22-b7c4-33b165770f14`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **FrIfRxPdu**
  - UUID: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
  - 描述: Receive PDU
- **FrIfTxPdu**
  - UUID: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

A PDU is either transmit or receive

##### 15. FrIfRxPdu

**容器属性**:

- **UUID**: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Receive PDU

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. FrIfUserRxIndicationUL

- **UUID**: `ECUC:5696974a-27c8-4ab3-a10c-9bc55592e3f4`
- **参数名**: `FrIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received FRIFRXPDU has to be routed via <User_RxIndication>. This <User_RxIndication> has to be invoked when the indication of the configured FRIFRXPDU will be received by a Rx indication event from the FR Driver module. If no upper layer (UL) module is configured, no <User_RxIndication> has to be called in case of a Rx indication event of the FRIFRXPDU from the FR Driver module.

####### FUNCTION-NAME 类型参数

######## 1. FrIfRxIndicationName

- **UUID**: `ECUC:dd2860dc-ad58-429d-bb84-83fb954a0c7c`
- **参数名**: `FrIfRxIndicationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter FRIF_USERRXINDICATION_UL. If FRIF_USERRXINDICATION_UL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_RxIndication> is fixed. If FRIF_USERRXINDICATION_UL equals CDD, the name of the <User_RxIndication> is selectable.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfRxPduRef

- **UUID**: `ECUC:7190286e-add2-4918-8f5b-300faefa5e9b`
- **引用名**: `FrIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

##### 16. FrIfTxPdu

**容器属性**:

- **UUID**: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container specifies transmission PDUs.

###### 参数配置

此容器包含 **8** 个参数：

####### INTEGER 类型参数

######## 1. FrIfCounterLimit

- **UUID**: `ECUC:c2fc5dd3-b3c4-4cd7-8be6-ac7f6d0578ab`
- **参数名**: `FrIfCounterLimit`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This value states the maximum number of indication of ready PDU data to the FrIf (i.e. maximum number of invocations of FrIf_Transmit) without an intermediate transmission of the PDU.

######## 2. FrIfTxPduId

- **UUID**: `ECUC:70a26482-2bb2-4f98-9e2c-50872cffe5c6`
- **参数名**: `FrIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The global PDU identifier, which has to be used by the upper layer BSW module. The identifier has to be zero based and consecutive.

####### BOOLEAN 类型参数

######## 1. FrIfConfirm

- **UUID**: `ECUC:572e1bf7-2cc9-4839-a685-06b9d25779da`
- **参数名**: `FrIfConfirm`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the transmission of a PDU should be checked and confirmed to the PDU owning BSW module.

######## 2. FrIfImmediate

- **UUID**: `ECUC:428461f7-aec1-48b0-b34b-9e60ca3b89eb`
- **参数名**: `FrIfImmediate`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines whether the PDU is transmitted immediate or decoupled.

######## 3. FrIfNoneMode

- **UUID**: `ECUC:8d686556-bea1-49a2-b933-397cc46d55a2`
- **参数名**: `FrIfNoneMode`
- **数据类型**: BOOLEAN
- **多重性**: [0..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Using the "None-Mode" which means that there is no API FrIf_Transmit call of the upper layer for this PDU.

####### ENUMERATION 类型参数

######## 1. FrIfUserTxUL

- **UUID**: `ECUC:54b68088-e78d-4488-84ca-c9a553e541be`
- **参数名**: `FrIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `FR_NM` (来源: AUTOSAR_ECUC)
  - `FR_TP` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
  - `XCP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the to be transmitted FRIFTXPDUID (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted FRIFTXPDUID has to be routed (via the <User_TxConfirmation>).

####### FUNCTION-NAME 类型参数

######## 1. FrIfTxConfirmationName

- **UUID**: `ECUC:ab1a488a-7143-4c2a-a9c8-b1b974f5ad4f`
- **参数名**: `FrIfTxConfirmationName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TxConfirmation> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TxConfirmation> is selectable.

######## 2. FrIfUserTriggerTransmitName

- **UUID**: `ECUC:a9f34f10-e503-47d7-919a-6e2962c07b92`
- **参数名**: `FrIfUserTriggerTransmitName`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter depends on the parameter FrIfUserTxUL. If FrIfUserTxUL equals FR_TP, FR_NM, PDUR or XCP, the name of the <User_TriggerTransmit> is fixed. If FrIfUserTxUL equals CDD, the name of the <User_TriggerTransmit> is selectable.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. FrIfTxPduRef

- **UUID**: `ECUC:4a970f9f-975c-4907-8ca7-b54068ef093f`
- **引用名**: `FrIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the external PDU definition.

##### 17. FrIfGeneral

**容器属性**:

- **UUID**: `ECUC:c545a70b-e5a0-44d2-a641-bb3071fc0dee`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `FrIfGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

This container contains the general configuration parameters of the FlexRay Interface.

###### 参数配置

此容器包含 **21** 个参数：

####### INTEGER 类型参数

######## 1. FrIfAbsTimerIdx

- **UUID**: `ECUC:20fe6d05-3697-42fd-8135-3a9e3ac09367`
- **参数名**: `FrIfAbsTimerIdx`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of supported absolut timers.

######## 2. FrIfNumClstSupported

- **UUID**: `ECUC:1c250d63-196a-4a2d-b884-cb526bea7053`
- **参数名**: `FrIfNumClstSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of FlexRay Clusters that the FlexRay Interface supports.

######## 3. FrIfNumCtrlSupported

- **UUID**: `ECUC:23ab6efa-d8ba-48d2-bea2-0a750fe70c7f`
- **参数名**: `FrIfNumCtrlSupported`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..15]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Maximum number of FlexRay CCs that the FlexRay Interface supports

######## 4. FrIfUnusedBitValue

- **UUID**: `ECUC:91765af9-a9d5-4ad2-a08f-c48777b57527`
- **参数名**: `FrIfUnusedBitValue`
- **数据类型**: INTEGER
- **多重性**: [0..1]
- **取值范围**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Set unused bits to a defined value.

####### BOOLEAN 类型参数

######## 1. FrIfAllSlotsSupport

- **UUID**: `ECUC:c70c486e-90f1-436e-b993-9ed8c0936ff7`
- **参数名**: `FrIfAllSlotsSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable of switching from key-slot / single-slot mode to all slot mode.

######## 2. FrIfCancelTransmitSupport

- **UUID**: `ECUC:f396e40a-e843-4a4b-bbcb-a7aaae0add58`
- **参数名**: `FrIfCancelTransmitSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to request the cancellation of the I-PDU transmission to FrDrv.

######## 3. FrIfDevErrorDetect

- **UUID**: `ECUC:7bc14870-c4d6-415e-884c-82d4c5b7632f`
- **参数名**: `FrIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification on or off

######## 4. FrIfDisableLPduSupport

- **UUID**: `ECUC:50cc77d5-9e7a-4fae-b8e9-936f52340c9e`
- **参数名**: `FrIfDisableLPduSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to disables the hardware resource of a LPdu for transmission/reception.

######## 5. FrIfDisableTransceiverBranchSupport

- **UUID**: `ECUC:21cd0aca-0b01-42b6-82a9-adfd58975766`
- **参数名**: `FrIfDisableTransceiverBranchSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to disable branches of an active star.

######## 6. FrIfEnableTransceiverBranchSupport

- **UUID**: `ECUC:a53b9f4e-0034-4ae8-b4fe-0088a9d2bea5`
- **参数名**: `FrIfEnableTransceiverBranchSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable branches of an active star.

######## 7. FrIfGetClockCorrectionSupport

- **UUID**: `ECUC:e0c069dd-c930-4dad-91af-5eb7b49d739a`
- **参数名**: `FrIfGetClockCorrectionSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable of polling the FlexRay Driver to getting CC clock correction values.

######## 8. FrIfGetGetChannelStatusSupport

- **UUID**: `ECUC:9d05a8c2-9782-476d-8e38-53f74f790f6d`
- **参数名**: `FrIfGetGetChannelStatusSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable of polling the FlexRay Driver to getting error information about the FlexRay communications bus.

######## 9. FrIfGetNmVectorSupport

- **UUID**: `ECUC:e2a802b2-ee34-41d2-8551-f4a5658cec43`
- **参数名**: `FrIfGetNmVectorSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to request the FlexRay hardware NMVector.

######## 10. FrIfGetNumOfStartupFramesSupport

- **UUID**: `ECUC:d01cf312-d59f-4746-a0f2-381ceacba66c`
- **参数名**: `FrIfGetNumOfStartupFramesSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable of polling the FlexRay Driver for the actual number of received startup frames on the bus.

######## 11. FrIfGetSyncFrameListSupport

- **UUID**: `ECUC:3890b9ac-7bca-4b7c-821d-a35f9cf6447d`
- **参数名**: `FrIfGetSyncFrameListSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable of polling the FlexRay Driver to getting a list of actual received sync frames.

######## 12. FrIfGetTransceiverErrorSupport

- **UUID**: `ECUC:16aacd37-c3a0-40c2-8a2b-474ba2b38337`
- **参数名**: `FrIfGetTransceiverErrorSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to get the FlexRay Transceiver errors by calling the FlexRay Transceiver module.

######## 13. FrIfGetWakeupRxStatusSupport

- **UUID**: `ECUC:b1536c2c-6dec-4875-b347-7f1d59f4ebba`
- **参数名**: `FrIfGetWakeupRxStatusSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to get the wakeup received information from the FlexRay controller.

######## 14. FrIfReadCCConfigApi

- **UUID**: `ECUC:dba81588-b4e5-4e63-a111-3ac268ed361b`
- **参数名**: `FrIfReadCCConfigApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable the optional FrIf_ReadCCConfig API.

######## 15. FrIfReconfigLPduSupport

- **UUID**: `ECUC:836cf683-2406-40d6-a0a5-2993a236e434`
- **参数名**: `FrIfReconfigLPduSupport`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Configuration parameter to enable/disable FrIf support to enable/disable the reconfiguration of a given LPdu according to the parameters (FrameId, Channel, CycleRepetition, CycleOffset, PayloadLength, HeaderCRC) at runtime.

######## 16. FrIfVersionInfoApi

- **UUID**: `ECUC:012c4e5d-40a0-45d2-9dff-8a7009566ea6`
- **参数名**: `FrIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Enables/disables the existence of the FrIf_GetVersionInfo() API service

####### STRING 类型参数

######## 1. FrIfPublicCddHeaderFile

- **UUID**: `ECUC:48ba44e8-bb8c-4c07-9764-a1b0c28aaa45`
- **参数名**: `FrIfPublicCddHeaderFile`
- **数据类型**: STRING
- **多重性**: [0..infinite]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines header files for callback functions which shall be included in case of CDDs. Range of characters is 1.. 32.

##### 18. FrIfPduDirection

**容器属性**:

- **UUID**: `ECUC:625dad92-ff44-4e22-b7c4-33b165770f14`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `FrIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **FrIfRxPdu**
  - UUID: `ECUC:ec547c45-8289-40de-92a3-ee0e3abfe98c`
  - 描述: Receive PDU
- **FrIfTxPdu**
  - UUID: `ECUC:e1e2ec3c-b595-4259-be3d-d4f86ffc03c0`
  - 描述: This container specifies transmission PDUs.

**容器描述**:

A PDU is either transmit or receive

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

1. **FrIf**
