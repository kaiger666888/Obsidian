# LinIf - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:46:25

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [LinIf](#linif)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. LinIf

#### 基本信息

- **UUID**: `ECUC:ac2ac1e0-b9bd-4f49-bfe2-3ce03cc8061d`
- **模块名称**: `LinIf`
- **多重性**: [0..1]
- **支持的变体**:
  - VARIANT-LINK-TIME
  - VARIANT-POST-BUILD
  - VARIANT-PRE-COMPILE

#### 模块描述

Configuration of the LinIf (LIN Interface) module.

#### 版本历史

共有 **1** 个版本记录：

##### 1. 版本 4.2.0

- **发布日期**: 2011-11-09
- **发布者**: AUTOSAR

*此版本无详细变更记录*

#### 配置容器

本模块包含 **17** 个配置容器：

##### 1. LinIfGeneral

**容器属性**:

- **UUID**: `ECUC:dc9a773a-d7ca-42ff-a751-8f35fc1171e3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfGeneral`
- **多重性**: [1..1]
- **多配置容器**: false

###### 参数配置

此容器包含 **9** 个参数：

####### BOOLEAN 类型参数

######## 1. LinIfCancelTransmitSupported

- **UUID**: `ECUC:d6679d00-fe67-48c5-9a7a-ffaeb82ebc57`
- **参数名**: `LinIfCancelTransmitSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Global Pre-Compile Switch to reliably prevent the generation of the dummy LinIf_CancelTransmit API.

######## 2. LinIfDevErrorDetect

- **UUID**: `ECUC:1786d1df-f161-4bd4-be94-d671b4335008`
- **参数名**: `LinIfDevErrorDetect`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the Development Error Detection and Notification ON or OFF.

######## 3. LinIfMultipleDriversSupported

- **UUID**: `ECUC:c3f20a68-c3db-4a68-b9e8-254e8873f238`
- **参数名**: `LinIfMultipleDriversSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: States if multiple drivers are included in the LIN Interface or not. The reason for this parameter is to reduce the size of LIN Interface if multiple drivers are not used.

######## 4. LinIfMultipleTrcvDriverSupported

- **UUID**: `ECUC:2265c857-1c3c-48fc-9e10-adeaa218d4d3`
- **参数名**: `LinIfMultipleTrcvDriverSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: States if multiple transceiver drivers are included in the LIN Interface or not. The reason for this parameter is to reduce the size of LIN Interface if multiple transceiver drivers are not used.

######## 5. LinIfNcOptionalRequestSupported

- **UUID**: `ECUC:43093996-93e3-461d-b50f-58021a6b42bc`
- **参数名**: `LinIfNcOptionalRequestSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: States if the node configuration commands Assign NAD and Conditional Change NAD are supported.

######## 6. LinIfTpSupported

- **UUID**: `ECUC:395fa338-8613-4555-b427-29807f920ac3`
- **参数名**: `LinIfTpSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: States if the TP is included in the LIN Interface or not. The reason for this parameter is to reduce the size of LIN Interface if the TP is not used.

######## 7. LinIfTrcvDriverSupported

- **UUID**: `ECUC:021681e4-7dd7-48b9-a0ae-f46ba162c147`
- **参数名**: `LinIfTrcvDriverSupported`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: States if transceiver drivers are included in the LIN Interface or not. The reason for this parameter is to reduce the size of LIN Interface if transceiver drivers are not used.

######## 8. LinIfVersionInfoApi

- **UUID**: `ECUC:8e091b33-0f2b-41ea-bdcd-4e7f273f4746`
- **参数名**: `LinIfVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Switches the LinIf_GetVersionInfo function ON or OFF.

####### STRING 类型参数

######## 1. LinIfPublicCddHeaderFile

- **UUID**: `ECUC:90188127-bfd2-42e2-aacc-20d2a3283e45`
- **参数名**: `LinIfPublicCddHeaderFile`
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

##### 2. LinIfGlobalConfig

**容器属性**:

- **UUID**: `ECUC:25d2741f-e24d-4278-923e-13bb5b219004`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfGlobalConfig`
- **多重性**: [1..1]
- **多配置容器**: true

**容器描述**:

This container contains the global configuration parameter of the LinIf.

###### 参数配置

此容器包含 **1** 个参数：

####### FLOAT 类型参数

######## 1. LinIfTimeBase

- **UUID**: `ECUC:d3d4848c-709e-4d4b-b219-c54ea93f1156`
- **参数名**: `LinIfTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The delay between processing two frames is a multiple of the LIN Interface time-base in seconds.

###### 配置容器

本模块包含 **15** 个配置容器：

####### 1. LinIfChannel

**容器属性**:

- **UUID**: `ECUC:acb64525-220b-48db-b6f0-5bb8fdb46ff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. LinIfChannelId

- **UUID**: `ECUC:0f6b0bda-545e-4531-baa3-9a231615e2f1`
- **参数名**: `LinIfChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter holds the unique channel index value. The value shall be the same as the ComMChannelId of the ComMChannel referenced by LinIfComMNetworkHandleRef.

######### ENUMERATION 类型参数

########## 1. LinIfGotoSleepConfirmationUL

- **UUID**: `ECUC:40dc162a-06e8-4aa7-846f-43facbc0272d`
- **参数名**: `LinIfGotoSleepConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the goto-sleep command shall be sent.

########## 2. LinIfScheduleRequestConfirmationUL

- **UUID**: `ECUC:8ed4be31-285b-4f4c-b944-2e349fe7185b`
- **参数名**: `LinIfScheduleRequestConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the successfully performed schedule table change.

########## 3. LinIfStartupState

- **UUID**: `ECUC:59a7fb27-4bdc-49b5-9d06-fe139cf39575`
- **参数名**: `LinIfStartupState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NORMAL` (来源: AUTOSAR_ECUC)
  - `SLEEP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the state of each LIN channel after startup

########## 4. LinIfWakeupConfirmationUL

- **UUID**: `ECUC:6eef5240-87ec-4625-bcd3-e7462d2b305c`
- **参数名**: `LinIfWakeupConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the wake-up shall be sent.

######## 引用关系

此容器包含 **2** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinIfChannelRef

- **UUID**: `ECUC:8715c30d-96ef-473d-bad1-16e8692c606c`
- **引用名**: `LinIfChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used channel in Lin.

########## 2. LinIfComMNetworkHandleRef

- **UUID**: `ECUC:d5db781e-486d-447c-93ff-e6a9cb25adcf`
- **引用名**: `LinIfComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain LIN network. Reference to one of the network handles configured for the ComM.

######## 配置容器

本模块包含 **14** 个配置容器：

######### 1. LinIfFrame

**容器属性**:

- **UUID**: `ECUC:1c7be285-63c0-4176-87e9-7af9e12e9593`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFrame`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Generic container for all types of LIN frames. The shortName of this container is used as LinIfFrameName.

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. LinIfLength

- **UUID**: `ECUC:9d278703-8bd9-4c02-b84a-82dbbe4347b2`
- **参数名**: `LinIfLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the LIN SDU in bytes.

############ 2. LinIfPid

- **UUID**: `ECUC:5ea9c5f4-9012-4f2c-925b-348b6fb424ea`
- **参数名**: `LinIfPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protected ID of the LIN frame. There is no reason to calculate the Parity in run-time.

########### ENUMERATION 类型参数

############ 1. LinIfChecksumType

- **UUID**: `ECUC:1c4bccbb-94d9-47a9-8818-ab3f131f67a4`
- **参数名**: `LinIfChecksumType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CLASSIC` (来源: AUTOSAR_ECUC)
  - `ENHANCED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of checksum that the frame is using.

############ 2. LinIfFrameType

- **UUID**: `ECUC:b9735872-2db9-41ef-9047-01d69eb83851`
- **参数名**: `LinIfFrameType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASSIGN` (来源: AUTOSAR_ECUC)
  - `ASSIGN_FRAME_ID_RANGE` (来源: AUTOSAR_ECUC)
  - `ASSIGN_NAD` (来源: AUTOSAR_ECUC)
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `FREE` (来源: AUTOSAR_ECUC)
  - `MRF` (来源: AUTOSAR_ECUC)
  - `SAVE_CONFIGURATION` (来源: AUTOSAR_ECUC)
  - `SPORADIC` (来源: AUTOSAR_ECUC)
  - `SRF` (来源: AUTOSAR_ECUC)
  - `UNASSIGN` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of frame that is described (e.g. sporadic frame).

########## 配置容器

本模块包含 **8** 个配置容器：

########### 1. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

############ 配置容器

本模块包含 **1** 个配置容器：

############# 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

############## 参数配置

此容器包含 **2** 个参数：

############### INTEGER 类型参数

################ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

################ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

########### 2. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

########### 3. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

########### 4. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

############ 参数配置

此容器包含 **2** 个参数：

############# ENUMERATION 类型参数

############## 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

############# FUNCTION-NAME 类型参数

############## 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

########### 5. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

########### 6. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

############ 参数配置

此容器包含 **4** 个参数：

############# INTEGER 类型参数

############## 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

############# ENUMERATION 类型参数

############## 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

############# FUNCTION-NAME 类型参数

############## 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

############## 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

########### 7. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

############ 参数配置

此容器包含 **1** 个参数：

############# INTEGER 类型参数

############## 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

############ 引用关系

此容器包含 **1** 个引用：

############# REFERENCE 类型引用

############## 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

########### 8. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

######### 2. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 3. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 4. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

######### 5. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

########### FUNCTION-NAME 类型参数

############ 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

######### 6. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

######### 7. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

########### ENUMERATION 类型参数

############ 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

########### FUNCTION-NAME 类型参数

############ 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

############ 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

######### 8. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

######### 9. LinIfMaster

**容器属性**:

- **UUID**: `ECUC:4f684fcc-d115-41c2-be8a-62a09a31f5e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfMaster`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Each Master can only be connected to one physical channel. This could be compared to the Node parameter in a LDF file.

########## 参数配置

此容器包含 **2** 个参数：

########### FLOAT 类型参数

############ 1. LinIfClusterTimeBase

- **UUID**: `ECUC:cc38fa34-ef1b-4471-b680-edb4c6116888`
- **参数名**: `LinIfClusterTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a time-base for one LIN cluster in seconds (normally 0.002, 0.005 or 0.010s).

############ 2. LinIfJitter

- **UUID**: `ECUC:120714ea-419a-4e88-aa67-01082afdc636`
- **参数名**: `LinIfJitter`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The jitter specifies the differences between the maximum and minimum delay from time base tick to the header sending start point in seconds.

######### 10. LinIfScheduleTable

**容器属性**:

- **UUID**: `ECUC:36bc9661-3231-4789-92b9-add11de9e32d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfScheduleTable`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes a schedule table. Each LinIfChannel may have several schedule tables. Each schedule table can only be connected to one channel.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. LinIfScheduleTableIndex

- **UUID**: `ECUC:fd890a6a-8cf9-4e03-b6dd-058f8d7dd274`
- **参数名**: `LinIfScheduleTableIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the unique index used by upper layers to identify a schedule. Note that the NULL_SCHEDULE for each channel has index 0.

########### STRING 类型参数

############ 1. LinIfScheduleTableName

- **UUID**: `ECUC:413fe6ac-3350-4a4d-896d-728cf69160a3`
- **参数名**: `LinIfScheduleTableName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional schedule name used to cross-reference with a LDF. This parameter shall always be accompanied by LIN_IF_SCHEDULE_INDEX.

########### ENUMERATION 类型参数

############ 1. LinIfResumePosition

- **UUID**: `ECUC:1241c21b-2b43-4b02-a0a5-d95aca248cfb`
- **参数名**: `LinIfResumePosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONTINUE_AT_IT_POINT` (来源: AUTOSAR_ECUC)
  - `START_FROM_BEGINNING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines, where a schedule table shall be proceeded in case if it has been interrupted by a RUN-ONCE table.

############ 2. LinIfRunMode

- **UUID**: `ECUC:1281d31b-3c9b-41a9-96cf-c05155bc3364`
- **参数名**: `LinIfRunMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RUN_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `RUN_ONCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in two different modes.

############ 3. LinIfScheduleMode

- **UUID**: `ECUC:86bbb55b-c6e6-4a39-be37-418f827cc427`
- **参数名**: `LinIfScheduleMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LINTP_APPLICATIVE_SCHEDULE` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_REQUEST` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_RESPONSE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in three different modes.

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

############# FLOAT 类型参数

############## 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

############ 引用关系

此容器包含 **2** 个引用：

############# REFERENCE 类型引用

############## 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

############## 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

######### 11. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

########### FLOAT 类型参数

############ 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

############ 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

######### 12. LinIfSlave

**容器属性**:

- **UUID**: `ECUC:e071b12c-44e9-4260-b1db-d54fc2e02a8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlave`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The Node attributes of the Slaves are provided with these parameter. The ShortName of this container is used as LinIfNodeName.

########## 参数配置

此容器包含 **5** 个参数：

########### INTEGER 类型参数

############ 1. LinIfConfiguredNad

- **UUID**: `ECUC:12ae340b-bce8-417e-8c8b-8fd78f073d91`
- **参数名**: `LinIfConfiguredNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initial node address

############ 2. LinIfFunctionId

- **UUID**: `ECUC:d42320ca-495a-4d03-8f65-51a1513c7bc5`
- **参数名**: `LinIfFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN function ID

############ 3. LinIfSupplierId

- **UUID**: `ECUC:58478360-77ad-41dc-a149-5196162b1f53`
- **参数名**: `LinIfSupplierId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN Supplier ID

############ 4. LinIfVariant

- **UUID**: `ECUC:1bec9005-853b-46dc-8607-091f91a537b5`
- **参数名**: `LinIfVariant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Variant ID

########### STRING 类型参数

############ 1. LinIfProtocolVersion

- **UUID**: `ECUC:cdaf5b4c-6111-4a97-a09e-614be235bd91`
- **参数名**: `LinIfProtocolVersion`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the LIN Protocol version which is used by the slave.

######### 13. LinIfTransceiverDrvConfig

**容器属性**:

- **UUID**: `ECUC:3ddbe282-a769-4c24-b63c-ec4af3e5b96c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTransceiverDrvConfig`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of all addressed LIN transceivers by each underlying LIN Transceiver Driver.

########## 参数配置

此容器包含 **1** 个参数：

########### BOOLEAN 类型参数

############ 1. LinIfTrcvWakeupNotification

- **UUID**: `ECUC:2cf0df6b-b5bc-4f50-b33f-2faf58ad5174`
- **参数名**: `LinIfTrcvWakeupNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether wakeup indication notification is supported.

########## 引用关系

此容器包含 **1** 个引用：

########### SYMBOLIC-NAME-REFERENCE 类型引用

############ 1. LinIfTrcvIdRef

- **UUID**: `ECUC:df3c8eae-155e-48a0-bdac-7438e0cdd781`
- **引用名**: `LinIfTrcvIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinTrcv/LinTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical handle of the underlying LIN transceiver to be served by the LIN Interface.

######### 14. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

####### 2. LinIfFrame

**容器属性**:

- **UUID**: `ECUC:1c7be285-63c0-4176-87e9-7af9e12e9593`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFrame`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Generic container for all types of LIN frames. The shortName of this container is used as LinIfFrameName.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinIfLength

- **UUID**: `ECUC:9d278703-8bd9-4c02-b84a-82dbbe4347b2`
- **参数名**: `LinIfLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the LIN SDU in bytes.

########## 2. LinIfPid

- **UUID**: `ECUC:5ea9c5f4-9012-4f2c-925b-348b6fb424ea`
- **参数名**: `LinIfPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protected ID of the LIN frame. There is no reason to calculate the Parity in run-time.

######### ENUMERATION 类型参数

########## 1. LinIfChecksumType

- **UUID**: `ECUC:1c4bccbb-94d9-47a9-8818-ab3f131f67a4`
- **参数名**: `LinIfChecksumType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CLASSIC` (来源: AUTOSAR_ECUC)
  - `ENHANCED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of checksum that the frame is using.

########## 2. LinIfFrameType

- **UUID**: `ECUC:b9735872-2db9-41ef-9047-01d69eb83851`
- **参数名**: `LinIfFrameType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASSIGN` (来源: AUTOSAR_ECUC)
  - `ASSIGN_FRAME_ID_RANGE` (来源: AUTOSAR_ECUC)
  - `ASSIGN_NAD` (来源: AUTOSAR_ECUC)
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `FREE` (来源: AUTOSAR_ECUC)
  - `MRF` (来源: AUTOSAR_ECUC)
  - `SAVE_CONFIGURATION` (来源: AUTOSAR_ECUC)
  - `SPORADIC` (来源: AUTOSAR_ECUC)
  - `SRF` (来源: AUTOSAR_ECUC)
  - `UNASSIGN` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of frame that is described (e.g. sporadic frame).

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 2. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 3. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

######### 4. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

########### FUNCTION-NAME 类型参数

############ 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

######### 5. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

######### 6. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

########### ENUMERATION 类型参数

############ 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

########### FUNCTION-NAME 类型参数

############ 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

############ 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

######### 7. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

######### 8. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

####### 3. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 4. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

########## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 5. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

####### 6. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

######### FUNCTION-NAME 类型参数

########## 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

####### 7. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

####### 8. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

######### ENUMERATION 类型参数

########## 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

######### FUNCTION-NAME 类型参数

########## 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

########## 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

####### 9. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

####### 10. LinIfMaster

**容器属性**:

- **UUID**: `ECUC:4f684fcc-d115-41c2-be8a-62a09a31f5e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfMaster`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Each Master can only be connected to one physical channel. This could be compared to the Node parameter in a LDF file.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. LinIfClusterTimeBase

- **UUID**: `ECUC:cc38fa34-ef1b-4471-b680-edb4c6116888`
- **参数名**: `LinIfClusterTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a time-base for one LIN cluster in seconds (normally 0.002, 0.005 or 0.010s).

########## 2. LinIfJitter

- **UUID**: `ECUC:120714ea-419a-4e88-aa67-01082afdc636`
- **参数名**: `LinIfJitter`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The jitter specifies the differences between the maximum and minimum delay from time base tick to the header sending start point in seconds.

####### 11. LinIfScheduleTable

**容器属性**:

- **UUID**: `ECUC:36bc9661-3231-4789-92b9-add11de9e32d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfScheduleTable`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes a schedule table. Each LinIfChannel may have several schedule tables. Each schedule table can only be connected to one channel.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. LinIfScheduleTableIndex

- **UUID**: `ECUC:fd890a6a-8cf9-4e03-b6dd-058f8d7dd274`
- **参数名**: `LinIfScheduleTableIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the unique index used by upper layers to identify a schedule. Note that the NULL_SCHEDULE for each channel has index 0.

######### STRING 类型参数

########## 1. LinIfScheduleTableName

- **UUID**: `ECUC:413fe6ac-3350-4a4d-896d-728cf69160a3`
- **参数名**: `LinIfScheduleTableName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional schedule name used to cross-reference with a LDF. This parameter shall always be accompanied by LIN_IF_SCHEDULE_INDEX.

######### ENUMERATION 类型参数

########## 1. LinIfResumePosition

- **UUID**: `ECUC:1241c21b-2b43-4b02-a0a5-d95aca248cfb`
- **参数名**: `LinIfResumePosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONTINUE_AT_IT_POINT` (来源: AUTOSAR_ECUC)
  - `START_FROM_BEGINNING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines, where a schedule table shall be proceeded in case if it has been interrupted by a RUN-ONCE table.

########## 2. LinIfRunMode

- **UUID**: `ECUC:1281d31b-3c9b-41a9-96cf-c05155bc3364`
- **参数名**: `LinIfRunMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RUN_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `RUN_ONCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in two different modes.

########## 3. LinIfScheduleMode

- **UUID**: `ECUC:86bbb55b-c6e6-4a39-be37-418f827cc427`
- **参数名**: `LinIfScheduleMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LINTP_APPLICATIVE_SCHEDULE` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_REQUEST` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_RESPONSE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in three different modes.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

########### FLOAT 类型参数

############ 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

############ 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

####### 12. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

######### FLOAT 类型参数

########## 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

########## 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

####### 13. LinIfSlave

**容器属性**:

- **UUID**: `ECUC:e071b12c-44e9-4260-b1db-d54fc2e02a8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlave`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The Node attributes of the Slaves are provided with these parameter. The ShortName of this container is used as LinIfNodeName.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. LinIfConfiguredNad

- **UUID**: `ECUC:12ae340b-bce8-417e-8c8b-8fd78f073d91`
- **参数名**: `LinIfConfiguredNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initial node address

########## 2. LinIfFunctionId

- **UUID**: `ECUC:d42320ca-495a-4d03-8f65-51a1513c7bc5`
- **参数名**: `LinIfFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN function ID

########## 3. LinIfSupplierId

- **UUID**: `ECUC:58478360-77ad-41dc-a149-5196162b1f53`
- **参数名**: `LinIfSupplierId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN Supplier ID

########## 4. LinIfVariant

- **UUID**: `ECUC:1bec9005-853b-46dc-8607-091f91a537b5`
- **参数名**: `LinIfVariant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Variant ID

######### STRING 类型参数

########## 1. LinIfProtocolVersion

- **UUID**: `ECUC:cdaf5b4c-6111-4a97-a09e-614be235bd91`
- **参数名**: `LinIfProtocolVersion`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the LIN Protocol version which is used by the slave.

####### 14. LinIfTransceiverDrvConfig

**容器属性**:

- **UUID**: `ECUC:3ddbe282-a769-4c24-b63c-ec4af3e5b96c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTransceiverDrvConfig`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of all addressed LIN transceivers by each underlying LIN Transceiver Driver.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. LinIfTrcvWakeupNotification

- **UUID**: `ECUC:2cf0df6b-b5bc-4f50-b33f-2faf58ad5174`
- **参数名**: `LinIfTrcvWakeupNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether wakeup indication notification is supported.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinIfTrcvIdRef

- **UUID**: `ECUC:df3c8eae-155e-48a0-bdac-7438e0cdd781`
- **引用名**: `LinIfTrcvIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinTrcv/LinTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical handle of the underlying LIN transceiver to be served by the LIN Interface.

####### 15. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

##### 3. LinIfChannel

**容器属性**:

- **UUID**: `ECUC:acb64525-220b-48db-b6f0-5bb8fdb46ff1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfChannel`
- **多重性**: [1..infinite]
- **多配置容器**: false

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. LinIfChannelId

- **UUID**: `ECUC:0f6b0bda-545e-4531-baa3-9a231615e2f1`
- **参数名**: `LinIfChannelId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter holds the unique channel index value. The value shall be the same as the ComMChannelId of the ComMChannel referenced by LinIfComMNetworkHandleRef.

####### ENUMERATION 类型参数

######## 1. LinIfGotoSleepConfirmationUL

- **UUID**: `ECUC:40dc162a-06e8-4aa7-846f-43facbc0272d`
- **参数名**: `LinIfGotoSleepConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the goto-sleep command shall be sent.

######## 2. LinIfScheduleRequestConfirmationUL

- **UUID**: `ECUC:8ed4be31-285b-4f4c-b944-2e349fe7185b`
- **参数名**: `LinIfScheduleRequestConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the successfully performed schedule table change.

######## 3. LinIfStartupState

- **UUID**: `ECUC:59a7fb27-4bdc-49b5-9d06-fe139cf39575`
- **参数名**: `LinIfStartupState`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `NORMAL` (来源: AUTOSAR_ECUC)
  - `SLEEP` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the state of each LIN channel after startup

######## 4. LinIfWakeupConfirmationUL

- **UUID**: `ECUC:6eef5240-87ec-4625-bcd3-e7462d2b305c`
- **参数名**: `LinIfWakeupConfirmationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `LIN_SM` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the confirmation of the wake-up shall be sent.

###### 引用关系

此容器包含 **2** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinIfChannelRef

- **UUID**: `ECUC:8715c30d-96ef-473d-bad1-16e8692c606c`
- **引用名**: `LinIfChannelRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/Lin/LinGlobalConfig/LinChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the used channel in Lin.

######## 2. LinIfComMNetworkHandleRef

- **UUID**: `ECUC:d5db781e-486d-447c-93ff-e6a9cb25adcf`
- **引用名**: `LinIfComMNetworkHandleRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `ComMChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/ComM/ComMConfigSet/ComMChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Unique handle to identify one certain LIN network. Reference to one of the network handles configured for the ComM.

###### 配置容器

本模块包含 **14** 个配置容器：

####### 1. LinIfFrame

**容器属性**:

- **UUID**: `ECUC:1c7be285-63c0-4176-87e9-7af9e12e9593`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFrame`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Generic container for all types of LIN frames. The shortName of this container is used as LinIfFrameName.

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinIfLength

- **UUID**: `ECUC:9d278703-8bd9-4c02-b84a-82dbbe4347b2`
- **参数名**: `LinIfLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the LIN SDU in bytes.

########## 2. LinIfPid

- **UUID**: `ECUC:5ea9c5f4-9012-4f2c-925b-348b6fb424ea`
- **参数名**: `LinIfPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protected ID of the LIN frame. There is no reason to calculate the Parity in run-time.

######### ENUMERATION 类型参数

########## 1. LinIfChecksumType

- **UUID**: `ECUC:1c4bccbb-94d9-47a9-8818-ab3f131f67a4`
- **参数名**: `LinIfChecksumType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CLASSIC` (来源: AUTOSAR_ECUC)
  - `ENHANCED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of checksum that the frame is using.

########## 2. LinIfFrameType

- **UUID**: `ECUC:b9735872-2db9-41ef-9047-01d69eb83851`
- **参数名**: `LinIfFrameType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASSIGN` (来源: AUTOSAR_ECUC)
  - `ASSIGN_FRAME_ID_RANGE` (来源: AUTOSAR_ECUC)
  - `ASSIGN_NAD` (来源: AUTOSAR_ECUC)
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `FREE` (来源: AUTOSAR_ECUC)
  - `MRF` (来源: AUTOSAR_ECUC)
  - `SAVE_CONFIGURATION` (来源: AUTOSAR_ECUC)
  - `SPORADIC` (来源: AUTOSAR_ECUC)
  - `SRF` (来源: AUTOSAR_ECUC)
  - `UNASSIGN` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of frame that is described (e.g. sporadic frame).

######## 配置容器

本模块包含 **8** 个配置容器：

######### 1. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

########## 配置容器

本模块包含 **1** 个配置容器：

########### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

############ 参数配置

此容器包含 **2** 个参数：

############# INTEGER 类型参数

############## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 2. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

######### 3. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

######### 4. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

########## 参数配置

此容器包含 **2** 个参数：

########### ENUMERATION 类型参数

############ 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

########### FUNCTION-NAME 类型参数

############ 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

######### 5. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

######### 6. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

########## 参数配置

此容器包含 **4** 个参数：

########### INTEGER 类型参数

############ 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

########### ENUMERATION 类型参数

############ 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

########### FUNCTION-NAME 类型参数

############ 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

############ 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

######### 7. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

########## 参数配置

此容器包含 **1** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

########## 引用关系

此容器包含 **1** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

######### 8. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

####### 2. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 3. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

########## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 4. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

####### 5. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

######### FUNCTION-NAME 类型参数

########## 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

####### 6. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

####### 7. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

######### ENUMERATION 类型参数

########## 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

######### FUNCTION-NAME 类型参数

########## 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

########## 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

####### 8. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

####### 9. LinIfMaster

**容器属性**:

- **UUID**: `ECUC:4f684fcc-d115-41c2-be8a-62a09a31f5e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfMaster`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Each Master can only be connected to one physical channel. This could be compared to the Node parameter in a LDF file.

######## 参数配置

此容器包含 **2** 个参数：

######### FLOAT 类型参数

########## 1. LinIfClusterTimeBase

- **UUID**: `ECUC:cc38fa34-ef1b-4471-b680-edb4c6116888`
- **参数名**: `LinIfClusterTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a time-base for one LIN cluster in seconds (normally 0.002, 0.005 or 0.010s).

########## 2. LinIfJitter

- **UUID**: `ECUC:120714ea-419a-4e88-aa67-01082afdc636`
- **参数名**: `LinIfJitter`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The jitter specifies the differences between the maximum and minimum delay from time base tick to the header sending start point in seconds.

####### 10. LinIfScheduleTable

**容器属性**:

- **UUID**: `ECUC:36bc9661-3231-4789-92b9-add11de9e32d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfScheduleTable`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes a schedule table. Each LinIfChannel may have several schedule tables. Each schedule table can only be connected to one channel.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. LinIfScheduleTableIndex

- **UUID**: `ECUC:fd890a6a-8cf9-4e03-b6dd-058f8d7dd274`
- **参数名**: `LinIfScheduleTableIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the unique index used by upper layers to identify a schedule. Note that the NULL_SCHEDULE for each channel has index 0.

######### STRING 类型参数

########## 1. LinIfScheduleTableName

- **UUID**: `ECUC:413fe6ac-3350-4a4d-896d-728cf69160a3`
- **参数名**: `LinIfScheduleTableName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional schedule name used to cross-reference with a LDF. This parameter shall always be accompanied by LIN_IF_SCHEDULE_INDEX.

######### ENUMERATION 类型参数

########## 1. LinIfResumePosition

- **UUID**: `ECUC:1241c21b-2b43-4b02-a0a5-d95aca248cfb`
- **参数名**: `LinIfResumePosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONTINUE_AT_IT_POINT` (来源: AUTOSAR_ECUC)
  - `START_FROM_BEGINNING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines, where a schedule table shall be proceeded in case if it has been interrupted by a RUN-ONCE table.

########## 2. LinIfRunMode

- **UUID**: `ECUC:1281d31b-3c9b-41a9-96cf-c05155bc3364`
- **参数名**: `LinIfRunMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RUN_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `RUN_ONCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in two different modes.

########## 3. LinIfScheduleMode

- **UUID**: `ECUC:86bbb55b-c6e6-4a39-be37-418f827cc427`
- **参数名**: `LinIfScheduleMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LINTP_APPLICATIVE_SCHEDULE` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_REQUEST` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_RESPONSE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in three different modes.

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

########### FLOAT 类型参数

############ 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

########## 引用关系

此容器包含 **2** 个引用：

########### REFERENCE 类型引用

############ 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

############ 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

####### 11. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

######### FLOAT 类型参数

########## 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

########## 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

####### 12. LinIfSlave

**容器属性**:

- **UUID**: `ECUC:e071b12c-44e9-4260-b1db-d54fc2e02a8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlave`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The Node attributes of the Slaves are provided with these parameter. The ShortName of this container is used as LinIfNodeName.

######## 参数配置

此容器包含 **5** 个参数：

######### INTEGER 类型参数

########## 1. LinIfConfiguredNad

- **UUID**: `ECUC:12ae340b-bce8-417e-8c8b-8fd78f073d91`
- **参数名**: `LinIfConfiguredNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initial node address

########## 2. LinIfFunctionId

- **UUID**: `ECUC:d42320ca-495a-4d03-8f65-51a1513c7bc5`
- **参数名**: `LinIfFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN function ID

########## 3. LinIfSupplierId

- **UUID**: `ECUC:58478360-77ad-41dc-a149-5196162b1f53`
- **参数名**: `LinIfSupplierId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN Supplier ID

########## 4. LinIfVariant

- **UUID**: `ECUC:1bec9005-853b-46dc-8607-091f91a537b5`
- **参数名**: `LinIfVariant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Variant ID

######### STRING 类型参数

########## 1. LinIfProtocolVersion

- **UUID**: `ECUC:cdaf5b4c-6111-4a97-a09e-614be235bd91`
- **参数名**: `LinIfProtocolVersion`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the LIN Protocol version which is used by the slave.

####### 13. LinIfTransceiverDrvConfig

**容器属性**:

- **UUID**: `ECUC:3ddbe282-a769-4c24-b63c-ec4af3e5b96c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTransceiverDrvConfig`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of all addressed LIN transceivers by each underlying LIN Transceiver Driver.

######## 参数配置

此容器包含 **1** 个参数：

######### BOOLEAN 类型参数

########## 1. LinIfTrcvWakeupNotification

- **UUID**: `ECUC:2cf0df6b-b5bc-4f50-b33f-2faf58ad5174`
- **参数名**: `LinIfTrcvWakeupNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether wakeup indication notification is supported.

######## 引用关系

此容器包含 **1** 个引用：

######### SYMBOLIC-NAME-REFERENCE 类型引用

########## 1. LinIfTrcvIdRef

- **UUID**: `ECUC:df3c8eae-155e-48a0-bdac-7438e0cdd781`
- **引用名**: `LinIfTrcvIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinTrcv/LinTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical handle of the underlying LIN transceiver to be served by the LIN Interface.

####### 14. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

##### 4. LinIfFrame

**容器属性**:

- **UUID**: `ECUC:1c7be285-63c0-4176-87e9-7af9e12e9593`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFrame`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Generic container for all types of LIN frames. The shortName of this container is used as LinIfFrameName.

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinIfLength

- **UUID**: `ECUC:9d278703-8bd9-4c02-b84a-82dbbe4347b2`
- **参数名**: `LinIfLength`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [1..8]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Length of the LIN SDU in bytes.

######## 2. LinIfPid

- **UUID**: `ECUC:5ea9c5f4-9012-4f2c-925b-348b6fb424ea`
- **参数名**: `LinIfPid`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Protected ID of the LIN frame. There is no reason to calculate the Parity in run-time.

####### ENUMERATION 类型参数

######## 1. LinIfChecksumType

- **UUID**: `ECUC:1c4bccbb-94d9-47a9-8818-ab3f131f67a4`
- **参数名**: `LinIfChecksumType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CLASSIC` (来源: AUTOSAR_ECUC)
  - `ENHANCED` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of checksum that the frame is using.

######## 2. LinIfFrameType

- **UUID**: `ECUC:b9735872-2db9-41ef-9047-01d69eb83851`
- **参数名**: `LinIfFrameType`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `ASSIGN` (来源: AUTOSAR_ECUC)
  - `ASSIGN_FRAME_ID_RANGE` (来源: AUTOSAR_ECUC)
  - `ASSIGN_NAD` (来源: AUTOSAR_ECUC)
  - `CONDITIONAL` (来源: AUTOSAR_ECUC)
  - `EVENT_TRIGGERED` (来源: AUTOSAR_ECUC)
  - `FREE` (来源: AUTOSAR_ECUC)
  - `MRF` (来源: AUTOSAR_ECUC)
  - `SAVE_CONFIGURATION` (来源: AUTOSAR_ECUC)
  - `SPORADIC` (来源: AUTOSAR_ECUC)
  - `SRF` (来源: AUTOSAR_ECUC)
  - `UNASSIGN` (来源: AUTOSAR_ECUC)
  - `UNCONDITIONAL` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Type of frame that is described (e.g. sporadic frame).

###### 配置容器

本模块包含 **8** 个配置容器：

####### 1. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

######## 配置容器

本模块包含 **1** 个配置容器：

######### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

########## 参数配置

此容器包含 **2** 个参数：

########### INTEGER 类型参数

############ 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

############ 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 2. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

########## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

####### 3. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

####### 4. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

######## 参数配置

此容器包含 **2** 个参数：

######### ENUMERATION 类型参数

########## 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

######### FUNCTION-NAME 类型参数

########## 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

####### 5. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

####### 6. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

######## 参数配置

此容器包含 **4** 个参数：

######### INTEGER 类型参数

########## 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

######### ENUMERATION 类型参数

########## 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

######### FUNCTION-NAME 类型参数

########## 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

########## 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

####### 7. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

######## 参数配置

此容器包含 **1** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

######## 引用关系

此容器包含 **1** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

####### 8. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

##### 5. LinIfFixedFrameSdu

**容器属性**:

- **UUID**: `ECUC:839c724c-3ce5-4a4f-8258-f9473b61cbd0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

In case this is a fixed frame this is the SDU (response).

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

########## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

##### 6. LinIfFixedFrameSduByte

**容器属性**:

- **UUID**: `ECUC:0aa8d449-7336-45d1-acf2-a79b1451a9ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfFixedFrameSduByte`
- **多重性**: [8..8]
- **多配置容器**: false

**容器描述**:

This container represents a byte within the 8 byte array.

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. LinIfFixedFrameSduBytePos

- **UUID**: `ECUC:0ab4ee67-172e-439e-bc01-1b107c277c05`
- **参数名**: `LinIfFixedFrameSduBytePos`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..7]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Index of the Byte in the SDU (response) 8 byte array.

######## 2. LinIfFixedFrameSduByteVal

- **UUID**: `ECUC:76133907-c78a-453d-bff1-c84964c755e6`
- **参数名**: `LinIfFixedFrameSduByteVal`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Byte value in the SDU (response) 8-byte array.

##### 7. LinIfInternalPdu

**容器属性**:

- **UUID**: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfInternalPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

Represents a Diagnostic or Configuration frame : no Message ID (no PduId).

##### 8. LinIfRxPdu

**容器属性**:

- **UUID**: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfRxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a received PDU/frame

###### 参数配置

此容器包含 **2** 个参数：

####### ENUMERATION 类型参数

######## 1. LinIfUserRxIndicationUL

- **UUID**: `ECUC:27972d9b-34b5-4115-bee3-e76a7f66edb5`
- **参数名**: `LinIfUserRxIndicationUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the indication of the successfully received LINRXPDUID has to be routed via <User_RxIndication>.

####### FUNCTION-NAME 类型参数

######## 1. LinIfRxIndicationUL

- **UUID**: `ECUC:29e68358-16ae-4dc8-b4da-1173c87ca2a4`
- **参数名**: `LinIfRxIndicationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_RxIndication>. This parameter depends on the parameter LinIfUserRxIndicationUL.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. LinIfRxPduRef

- **UUID**: `ECUC:a4b0259f-0d05-4a0e-b86a-89c2558bb7ba`
- **引用名**: `LinIfRxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is received in this frame.

##### 9. LinIfSlaveToSlavePdu

**容器属性**:

- **UUID**: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlaveToSlavePdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.

##### 10. LinIfTxPdu

**容器属性**:

- **UUID**: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTxPdu`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

represents a transmitted PDU/frame

###### 参数配置

此容器包含 **4** 个参数：

####### INTEGER 类型参数

######## 1. LinIfTxPduId

- **UUID**: `ECUC:dd139fd4-fcb7-4f6e-8311-f18bb2cfe5c3`
- **参数名**: `LinIfTxPduId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Identifier of the Pdu for the upper layer.

####### ENUMERATION 类型参数

######## 1. LinIfUserTxUL

- **UUID**: `ECUC:fe2c0d05-82ea-4af2-84db-989658a33d89`
- **参数名**: `LinIfUserTxUL`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CDD` (来源: AUTOSAR_ECUC)
  - `PDUR` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the upper layer (UL) module to which the trigger of the transmitted LinTxPdu (via the <User_TriggerTransmit>) or the confirmation of the successfully transmitted LinTxPdu has to be routed (via the <User_TxConfirmation>).

####### FUNCTION-NAME 类型参数

######## 1. LinIfTxConfirmationUL

- **UUID**: `ECUC:5ffc9a8f-527a-4206-9862-d45ec09056df`
- **参数名**: `LinIfTxConfirmationUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TxConfirmation>. This parameter depends on the parameter LinIfUserTxUL.

######## 2. LinIfTxTriggerTransmitUL

- **UUID**: `ECUC:02bbc963-0110-4f5b-8693-b62cab0c86af`
- **参数名**: `LinIfTxTriggerTransmitUL`
- **数据类型**: FUNCTION-NAME
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **函数变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This parameter defines the name of the <User_TriggerTransmit>. This parameter  depends on the parameter LinIfUserTxUL. If LinIfUserTxUL equals PDUR, the name  of the <User_TriggerTransmit> is fixed.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. LinIfTxPduRef

- **UUID**: `ECUC:78cf5840-3ad7-412d-ac03-c32aec40298b`
- **引用名**: `LinIfTxPduRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `Pdu`
- **完整路径**: `/AUTOSAR/EcucDefs/EcuC/EcucPduCollection/Pdu`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the PDU that is transmitted in this frame.

##### 11. LinIfSubstitutionFrames

**容器属性**:

- **UUID**: `ECUC:c9f2d77f-3e93-450d-b8d7-c9e1940c044d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSubstitutionFrames`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

List of unconditional Frames that can be sent in a sporadic Frame slot.

###### 参数配置

此容器包含 **1** 个参数：

####### INTEGER 类型参数

######## 1. LinIfFramePriority

- **UUID**: `ECUC:52c7ca27-7e7c-41f9-8a29-9660a446d4f7`
- **参数名**: `LinIfFramePriority`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Priority of an unconditional frame if used as a sporadic frame.

###### 引用关系

此容器包含 **1** 个引用：

####### REFERENCE 类型引用

######## 1. LinIfSubstitutionFrameRef

- **UUID**: `ECUC:d92f4f29-dbe9-4834-b3dd-031a34675f81`
- **引用名**: `LinIfSubstitutionFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..1]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to an unconditional Frame that can be sent in a sporadic Frame slot.

##### 12. LinIfMaster

**容器属性**:

- **UUID**: `ECUC:4f684fcc-d115-41c2-be8a-62a09a31f5e5`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfMaster`
- **多重性**: [1..1]
- **多配置容器**: false

**容器描述**:

Each Master can only be connected to one physical channel. This could be compared to the Node parameter in a LDF file.

###### 参数配置

此容器包含 **2** 个参数：

####### FLOAT 类型参数

######## 1. LinIfClusterTimeBase

- **UUID**: `ECUC:cc38fa34-ef1b-4471-b680-edb4c6116888`
- **参数名**: `LinIfClusterTimeBase`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines a time-base for one LIN cluster in seconds (normally 0.002, 0.005 or 0.010s).

######## 2. LinIfJitter

- **UUID**: `ECUC:120714ea-419a-4e88-aa67-01082afdc636`
- **参数名**: `LinIfJitter`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-LINK-TIME
  - PRE-COMPILE: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The jitter specifies the differences between the maximum and minimum delay from time base tick to the header sending start point in seconds.

##### 13. LinIfScheduleTable

**容器属性**:

- **UUID**: `ECUC:36bc9661-3231-4789-92b9-add11de9e32d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfScheduleTable`
- **多重性**: [1..infinite]
- **多配置容器**: false

**容器描述**:

Describes a schedule table. Each LinIfChannel may have several schedule tables. Each schedule table can only be connected to one channel.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. LinIfScheduleTableIndex

- **UUID**: `ECUC:fd890a6a-8cf9-4e03-b6dd-058f8d7dd274`
- **参数名**: `LinIfScheduleTableIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: true
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: This is the unique index used by upper layers to identify a schedule. Note that the NULL_SCHEDULE for each channel has index 0.

####### STRING 类型参数

######## 1. LinIfScheduleTableName

- **UUID**: `ECUC:413fe6ac-3350-4a4d-896d-728cf69160a3`
- **参数名**: `LinIfScheduleTableName`
- **数据类型**: STRING
- **多重性**: [0..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Optional schedule name used to cross-reference with a LDF. This parameter shall always be accompanied by LIN_IF_SCHEDULE_INDEX.

####### ENUMERATION 类型参数

######## 1. LinIfResumePosition

- **UUID**: `ECUC:1241c21b-2b43-4b02-a0a5-d95aca248cfb`
- **参数名**: `LinIfResumePosition`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `CONTINUE_AT_IT_POINT` (来源: AUTOSAR_ECUC)
  - `START_FROM_BEGINNING` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines, where a schedule table shall be proceeded in case if it has been interrupted by a RUN-ONCE table.

######## 2. LinIfRunMode

- **UUID**: `ECUC:1281d31b-3c9b-41a9-96cf-c05155bc3364`
- **参数名**: `LinIfRunMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `RUN_CONTINUOUS` (来源: AUTOSAR_ECUC)
  - `RUN_ONCE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in two different modes.

######## 3. LinIfScheduleMode

- **UUID**: `ECUC:86bbb55b-c6e6-4a39-be37-418f827cc427`
- **参数名**: `LinIfScheduleMode`
- **数据类型**: ENUMERATION
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **可选值**:
  - `LINTP_APPLICATIVE_SCHEDULE` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_REQUEST` (来源: AUTOSAR_ECUC)
  - `LINTP_DIAG_RESPONSE` (来源: AUTOSAR_ECUC)
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: The schedule table can be executed in three different modes.

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

######## 参数配置

此容器包含 **2** 个参数：

######### INTEGER 类型参数

########## 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

######### FLOAT 类型参数

########## 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

######## 引用关系

此容器包含 **2** 个引用：

######### REFERENCE 类型引用

########## 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

########## 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

##### 14. LinIfEntry

**容器属性**:

- **UUID**: `ECUC:5856d22c-f08e-4597-aa05-a2fa836b7ec8`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfEntry`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

Describes an entry in the schedule table (also known as Frame Slot).

###### 参数配置

此容器包含 **2** 个参数：

####### INTEGER 类型参数

######## 1. LinIfEntryIndex

- **UUID**: `ECUC:f0b28166-a295-4302-8662-4774593acd65`
- **参数名**: `LinIfEntryIndex`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Position of the Frame Entry in the Schedule Table. The first entry index in the schedule table is 0.

####### FLOAT 类型参数

######## 1. LinIfDelay

- **UUID**: `ECUC:d4db710c-4063-4b8d-81e4-d8cea455b14a`
- **参数名**: `LinIfDelay`
- **数据类型**: FLOAT
- **多重性**: [1..1]
- **取值范围**: [0..0.255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Delay to next entry in schedule table in seconds.

###### 引用关系

此容器包含 **2** 个引用：

####### REFERENCE 类型引用

######## 1. LinIfCollisionResolvingRef

- **UUID**: `ECUC:b0729f03-6459-4a96-b816-9e8aa89cab6e`
- **引用名**: `LinIfCollisionResolvingRef`
- **引用类型**: REFERENCE
- **多重性**: [0..1]
- **目标**: `LinIfScheduleTable`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfScheduleTable`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the schedule table, which resolves the collision.

######## 2. LinIfFrameRef

- **UUID**: `ECUC:5be22eba-daf3-4d41-b2ab-d9fe94e681a3`
- **引用名**: `LinIfFrameRef`
- **引用类型**: REFERENCE
- **多重性**: [1..infinite]
- **目标**: `LinIfFrame`
- **完整路径**: `/AUTOSAR/EcucDefs/LinIf/LinIfGlobalConfig/LinIfChannel/LinIfFrame`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - POST-BUILD: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Reference to the frames that belong to this schedule table entry.

##### 15. LinIfSlave

**容器属性**:

- **UUID**: `ECUC:e071b12c-44e9-4260-b1db-d54fc2e02a8f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfSlave`
- **多重性**: [0..infinite]
- **多配置容器**: false

**容器描述**:

The Node attributes of the Slaves are provided with these parameter. The ShortName of this container is used as LinIfNodeName.

###### 参数配置

此容器包含 **5** 个参数：

####### INTEGER 类型参数

######## 1. LinIfConfiguredNad

- **UUID**: `ECUC:12ae340b-bce8-417e-8c8b-8fd78f073d91`
- **参数名**: `LinIfConfiguredNad`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Definition of the initial node address

######## 2. LinIfFunctionId

- **UUID**: `ECUC:d42320ca-495a-4d03-8f65-51a1513c7bc5`
- **参数名**: `LinIfFunctionId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN function ID

######## 3. LinIfSupplierId

- **UUID**: `ECUC:58478360-77ad-41dc-a149-5196162b1f53`
- **参数名**: `LinIfSupplierId`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..65535]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: LIN Supplier ID

######## 4. LinIfVariant

- **UUID**: `ECUC:1bec9005-853b-46dc-8607-091f91a537b5`
- **参数名**: `LinIfVariant`
- **数据类型**: INTEGER
- **多重性**: [1..1]
- **取值范围**: [0..255]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Specifies the Variant ID

####### STRING 类型参数

######## 1. LinIfProtocolVersion

- **UUID**: `ECUC:cdaf5b4c-6111-4a97-a09e-614be235bd91`
- **参数名**: `LinIfProtocolVersion`
- **数据类型**: STRING
- **多重性**: [1..1]
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **字符串变体**:
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Defines the LIN Protocol version which is used by the slave.

##### 16. LinIfTransceiverDrvConfig

**容器属性**:

- **UUID**: `ECUC:3ddbe282-a769-4c24-b63c-ec4af3e5b96c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `LinIfTransceiverDrvConfig`
- **多重性**: [0..1]
- **多配置容器**: false

**容器描述**:

This container contains the configuration (parameters) of all addressed LIN transceivers by each underlying LIN Transceiver Driver.

###### 参数配置

此容器包含 **1** 个参数：

####### BOOLEAN 类型参数

######## 1. LinIfTrcvWakeupNotification

- **UUID**: `ECUC:2cf0df6b-b5bc-4f50-b33f-2faf58ad5174`
- **参数名**: `LinIfTrcvWakeupNotification`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: AUTOSAR_ECUC
- **符号名值**: false
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Selects whether wakeup indication notification is supported.

###### 引用关系

此容器包含 **1** 个引用：

####### SYMBOLIC-NAME-REFERENCE 类型引用

######## 1. LinIfTrcvIdRef

- **UUID**: `ECUC:df3c8eae-155e-48a0-bdac-7438e0cdd781`
- **引用名**: `LinIfTrcvIdRef`
- **引用类型**: SYMBOLIC-NAME-REFERENCE
- **多重性**: [1..1]
- **目标**: `LinTrcvChannel`
- **完整路径**: `/AUTOSAR/EcucDefs/LinTrcv/LinTrcvChannel`
- **来源**: AUTOSAR_ECUC
- **实现配置类**:
  - LINK: VARIANT-LINK-TIME
  - LINK: VARIANT-POST-BUILD
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Logical handle of the underlying LIN transceiver to be served by the LIN Interface.

##### 17. LinIfPduDirection

**容器属性**:

- **UUID**: `ECUC:ad560145-2b51-46ad-91c3-219c5c976f4c`
- **容器类型**: CHOICE-CONTAINER
- **容器名称**: `LinIfPduDirection`
- **多重性**: [1..1]

**容器选择**:

- **LinIfInternalPdu**
  - UUID: `ECUC:c126513a-cf29-4918-bb7e-aea26cd3f5df`
  - 描述: Represents a Diagnostic or Configuration frame : no Message ID (no PduId).
- **LinIfRxPdu**
  - UUID: `ECUC:13322c3b-51f2-40eb-b615-dfc3e665e5e8`
  - 描述: represents a received PDU/frame
- **LinIfSlaveToSlavePdu**
  - UUID: `ECUC:01088ba1-2498-4a9a-ab0c-a5fa045e5621`
  - 描述: represents a slave-to-slave PDU/frame. Master does only send the header but doesn't receive the response.
- **LinIfTxPdu**
  - UUID: `ECUC:7640ebc8-a9e9-4673-9ccd-ce63404a29ce`
  - 描述: represents a transmitted PDU/frame

**容器描述**:

Direction of the frame

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

1. **LinIf**
